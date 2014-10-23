1.   
2.
3.  The instruction scheduler tries to rearrange the code so that many
    expressions are computed concurrently. By computing expressions
    concurrently, however, more registers are needed resulting in what's
    called *register pressure*.
4.  How - see book 233
    Why - avoid pipeline stalls
5.  `(sigma(v) + i) mod II`
6.  Loop's can use their own indices

Terminology
===========

## Matrix distance ##

Let's say we have the following:

```c
float a[N][M], b[N][M], c[N][M];

void foo()
{
    int     i, j;
    
    for (i = 2; i < 100; i++) {
        for (j = 2 + 3 * i; j < 1000; j++) {
            a[ i ][ j ] = [ i - 2 ][ j + 3 ];
            b[ i ][ j ] = [ i     ][ j - 2 ];
            c[ i ][ j ] = [ i + 1 ][ j + 2 ];
        }
    }
}
```

Finding the distance matrix of the loop above is done as follows.
We start of with calculating the distance vector for the `a` vector.

```
IA + a0 = JB + b0

where

A   = [1 0; 0 1]
a0  = [0 0]

B   = [1 0; 0 1]
b0  = [-2 3]
```

We then re-write `IA + a0 = JB + b0` to:

```
[I J][A; -B] = [i1 j1 i2 j2][A; -B] = b0 - a0
```

For the `a` vector this results in:

```
             [  1  0 ]
[i1 j1 i2 j2]|  0  1 | = [-2 3] - [0 0]
             | -1  0 | 
             [  0 -1 ]

```

Which in turn gives us:

```
(i1 - i2, j1 - j2) = (-2, 3)

if I = (t1, t2) =>

i1 - i2 = -2 => i2 = t1 + 2
j1 - j2 =  3 => j2 = t2 - 3

=>

J = (t1 + 2, t2 - 3)

=>

d_a = (2, -3)
```

In the case of the last vector's distance vector `d_c` we get a vector
that's negative when first examined. However we want a vector that's
lexicographically positive. As such we must check whether `I-J` or `J-I`
gives a positive distance vector. In this case `J - I` gives a positive
vector `d_c = (1, 2)`.

### TIP! ###
In this vector `(1, 2)` left is read right is write. I.e. if the first
element is larger than the second then the read occurs first.
