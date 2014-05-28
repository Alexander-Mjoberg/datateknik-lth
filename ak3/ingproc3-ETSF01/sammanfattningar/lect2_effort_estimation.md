Effort Estimation
=================

## Problems with Effort Estimation ##
 Subjective nature of estimating
  * Difficult to produce evidence in support of decision
* Changing techologies
  * these bring uncertainties, especially in the early days when there is a
  'learning curve'
* Projects differ
  * Experience on one project may not be applicable to another
* Political pressure
  * Managers may wish to reduce estimated costs in order to win support for
  acceptance of a project proposal
* Covering your own back
  * Avoid later overtime

## Effort or Cost? ##

```
Effort == work required e.g. person/man-hours
```

__Cost includes:__
* Person-hours (salaries, benefits)
* Moving and living costs for new staff members
* Training
* Travel costs
* Legal & Licensing fees (software, patents, copyright)
* Contractors and subcontractors
* Equipment
* Currency exchange rates
* Marketing & Advertising
* Inflation rate

## Over- and under-estimating ##

### Parkinson's Law ###
> Work expands to fill the time available

### Brooks's ###
> Putting more people on a late job makes it later

### Weinberg's Zeroth Law of reliability ###
> a software project that does not have to meet a reliability requirement
> can meet any other requirement

Vad betyder då den här lagen? Jo det ska ni få veta! (Brace yourselves) Lagen
innebär att ifall projektet inte har en tydligt specificerad krav på 
tillförlitlighet när det ska skeppas så kan detta arbiträrt väljas. Vilket
resulterar i sämre kvalitet som sedan visas i __testning__ eller senare faser.

* Over-estimations => project likely to take longer
* Under-estimations => lower quality in order to meet target

## When & Why ##
* Strategic planning
* Feasability study
* Requirements spec
* Evaluation of suppliers' proposals
* Project planning

## What don't we know? ##
* Customers' needs & expectations - requirements
* Technical complexity & design components
* Reuse - internal and external components
* People
  * Skills, competence and experience
  * Co-operation & communication
* ... (srsly wtf, why the dots here grrl?)

## Bottom-up versus top-down estimation ##

### Bottom-up ###
* Identify all tasks that have to be done (top-down)
* Estimate tasks of 1-2 mw, accumulate effort bottom-up
* Time consuming
* Useful when no past project data for similar projects exist

### Top down ###
* Produce overall estimate based on project cost drivers
* Based on past project data
* Divide overall estimate between jobs done

```
effort = (system size) * (productivity rate)
```

## Estimation methods ##
* Analogy: case-based, comparative (from previous projects etc)
  * Look at previous similar tasks, base estimation from diff/error
* Parametric or algorithmic models, e.g. function points COCOMO
* Expert opinion - just guessing?
* Parkinson and 'price to win' - opportunistic estimates!

## Basis for successful estimation ##
* Information about past projects
  * Need to collect performance details about past project
* Need to be able to measure the amount of work involved
  * Traditional size measurement for software is 'lines of code' - ain't good

## Stages: Identify ##
1. Significant features of the current project
1. Previous project(s) with similar features
1. Base effort on previous similar project. Consider
  1. Differences between current and previous projects
  1. Possible reasons for error (risk)
  1. Measures to reduce uncertainty

## Algorithmic estimation ##
Estimates based on historical data in the form of measurements from earlier
projects, typically `effort = c * size^k`

Example:
```
size = lines of code
1/c  = productivity //e.g. lines of code per day
```

* Objective, but good estimate requires
  * Good experience base
  * Good size estimate

## Parametric Models ###
* Other models focus on productivity (e.g. COCOMO)
* Lines of code (or function points, FP etc) an input

### Function Points - Albrecht/IFPUG FP ###
Models system size

```
UFP* = SUM(i=1..15, n items of weight i * weight)
FP   = UFP * "technical complexity factor"
```

#### Albrecht function point analysis ####
* Top down method (IBM)
* Information systems compirsed of (5):
  * *External input types* - input transactions which update internal computer
    files
  * *External output types* - transactions where data is output to the user
  * *External inquiry types* - transactions initiated by the user, which provide
    information but do not update internal files
  * *Logical internal file types* - are the standing files (or datastore) used
    by the system.
  * *External interface file types* - allow for output and input that may pass
    to and from other computer applications
* A table consists of "low", "medium" and "high" complexity numbers for the above
  listed points. The amount of items in each category is then multiplied by its
  counterpart in the table. The sum of these are the Albrecht FPs.

### COCOMO ###
Focuses on productivity factors
1. COCOMO81 (original)
1. COCOMO2
