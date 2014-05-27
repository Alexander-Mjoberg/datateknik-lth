#Risk Management

"A risk is a potential problem; a problem is a risk that has materialized" [Fairley 1994]

##What can go wrong?
 * Staff turn-around: quit, moved to other project, illness
 * Tools do not work as anticipated
 * Requirements change more than expected
 * Effort estimates were wrong
 * Expected input/deliveries are delayed
 * Quality is not good enough in the end of the project

##What is risk?
 "An uncertain event or condition that, if it occurs, has a positive or negative effect on a project's objective"
 It consists of both a **cause** and an **effect**
 For example:

 - Use of new compiler (**cause**)
 
  Integration problem && delayed training phase (**effect**)

 - Low top management priority in Project A (**cause**)

   Resources (staff) moved from project A to another project (**effect**)

###Risky commitments - Overscoping
The main risk of overscoping is that the project target (scope)
will not be met in *time* and on budget (*cost/effort*).

 * The traditional dev model (waterfall) - sequential & doc-driven

   "*overpromise* software capabilities in cortractually binding requirements
   specification before they *understand* their risk implications."

 * Agile dev model (XP/Scrum) - iterative & code driven

   "... neat ideas... I'll code 'em up, and if they *don't fit* other 
   peoples ideas, we'll just evolve things until they work."
   
###Risk Management

 * Risk Assessment
   - Identification (What might go wrong?)
   - Analysis & prioritization (What are the most serious risks?)
 * Control of risk
   - Planning & Resolution
   - Monitoring

#### Approaches to risk identification:
 Includes but isn't limited to:
 * Use of checklists, check which risks may come up based on previous experience.
 * Brainstorming - getting knowledgeable stakeholders together to pool concerns.
 * Casual mapping - Identifying possible chains of cause and effect using a map.
 
##### Casual mapping (Applied example)
```
                                (DELAY IN PROJECT!)                                           
                               /                  \                
                              /                    \              
                             /                 (Poor project outcome)                     
                            /                            \              
                           /                              \              
                          /                                \              
(Unrealistic schedule estimates)                      (Lack of skill)
```

#### Risk assessment

Risk exposure = Potential Damage * Probability 

* Not neccesary nor possible to give exact estimates: Qualitative descriptors
  , e.g High, Significant, Moderate and Low.
* Pripritizethe worst risks (high probability and large damage)


##### Example of a probability/impact matrix
```
(cost)        _____________________________
             |       |xxxxxx|xxxxxx|xxxxxxx|
High         |       |xxxxxx|xxxxxx|xxxxxxx|                         
             |_______|xxxxxx|xxxxxx|xxxxxxx|    
             |       |      |      |xxxxxxx|
Significant  |       |      |      |xxxxxxx|                              
             |_______|______|______|xxxxxxx|      
             |       |      |      |       |
Moderate     |       |      |      |       |                                
             |_______|______|______|_______|      
             |       |      |      |       |
Low          |       |      |      |       |
             |_______|______|______|_______|
                Low    Med    Med+    High   (probability)                      
```
The worst risks are indicated by X'es since they both have a high cost and probability.

##### An example of a risk assessment technique is a decision tree.

In this scenario we ponder on wether or not to extend or replace a system.
The outcome of this depends on if the market expands or not.
If we extend the system and the market expands we lose -100.000$, if it doesn't expand
we will gain 75.000$.
If we replace the system and the market expands we gain 250.000$, if it doesn't
expand we lose 50.000$
```
                                                                             
                                                                                     
                    ,_______________     Net Product Value (NPV)                                               
      ,____________/ (20%) Expansion     -100.000 $                                                     
     /   Extend    \ (80%) No Expansion   75.000 $                                                              
    /               `---------------                                        
   /                                                  
  /                                                       
D                                                        
  \                                                       
   \                                 
    \               ,_______________                           
     `-------------´ (20%) Expansion      250.000 $                                          
         Replace   \ (80%) No Expansion  -50.000 $                                               
                    `---------------                                                 
```
If we extend the risk exposure is:
RE = -100.000 * 0.2 + 75.000 * 0.8 = 40.000
And if replace the risk exposure is:
RE = 250.000 * 0.2 - 50.000 * 0.8 = 10.000
Therefore in this example we should obviously **EXTEND THE SYSTEM!!!!!!**

