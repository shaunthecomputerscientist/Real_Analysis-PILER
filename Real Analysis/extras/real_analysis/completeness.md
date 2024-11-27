# A Brief Theory on Reals :


## What is this section about?

### we will cover the following here:

- why do we need to study reals?
- #### what are reals? (**with a taste of abstract algebra**)
- what is completness axiom? why is it needed? what is irrational and rational?

Let's answer the first question. If you are here you probably would have taken calculus of real functions. Right now this is an analysis course. In both of these broad fields we use Real numbers explicitly. You must already know how we define numbers. Here we will dive only into how we deine reals.

This is how we write reals and rationals.

- $\mathbb{R}$
- $\mathbb{Q}$

$\mathbb{Q}$ is the set of all fractions of the form $\frac{a}{b}$ where $a, b \in \mathbb{Z}$ and $b \neq 0$

Here we will not construct $\mathbb{Q}$ from scratch. But we will use $\mathbb{Q}$ as a tool to construct $\mathbb{R}$

- ### Caution : you may skip this part if you are intimidated by abstract algebra and have no background. For those who have a little background can see how things connect.

If you are little famaliar with abstract algebra where we generalize numbers by studying fundamental algebraic structures.
We have following types of algebraic structures :
- [sets](/Real%20Analysis/extras/real_analysis/sets.md)
- groups
- fields
- Module
- Rings
- Algebras
An algebraic structure is so general that it ties all this with one string. One just needs to satisfy closure property to become an algebraic structure.

Then comes semi group, monoid, group and abelian group. All these you can learn in group theory.

We are specifically concerned with rings here.

### Definition : A non empty set R with two binary operation +, x is a ring if :

- x is closed for any a,b $\in$ R
- (R,+) is an abelian group.
- (R,x) is associative i.e, (axb)xc=ax(bxc)
- x is distributive over + : ax(b+c)=axb+axc

if $\exists$ 1 $\in$ R such that ax1=1xa=a $\forall$ a $\in$ R then the ring is said to be a ring with unity.
And if x is commutative, it becomes a commutative ring.

- If we have a ring which is commutative, has identidy element e (1), and does not have zero divisor (i.e, left and right cancellation law holds) then This kind of ring is an integral domain.

Notice we put stricter condition on ring to get integral domain. Now we will put even stricter condition on integral domain to get a narrow subset $\mathbb F$ (field).

What does zero divisor mean?

A ring has zero divisor if there is a non zero element in the ring that can be multiplied by another non zero element to produce zero (identity of +). So not having zero divisor mean if axb=0 then either a=0 or b=0.

- Theorem : A ring does not have zero divisor iff cancelletion law holds.

SO an integral domain does not have zero divisor. Applying even stricter consition to this, we get a field.

- If we have a ring which is commutative, has identidy element (1) wrt x, and every non zero (non identity) element has an inverse. Then it becomes a field.
Notice how this condition of having multiplicative inverse strictly enforce "not having zero divisor" condition. If aXb= 0 where a and b are not zero, that would not let our inverse wrt x to exist. Hence it's an even stricter condition.

With these rules we get a field $\mathbb F$.
------------------------------------------------------------------------------------------------------
Here are some key points :

### A total ordering on a field makes a field ordered. formally it should satisfy two axioms :
1. $\forall$ x,y,z $\in$ $\mathbb F$ if x<y then x+z<y+z
2. $\forall$ x,y $\in$ $\mathbb F$, x>0 and y>0 => xy>0.

It means that all elements are compareable with each other using the field operations.




### Archimedian ordered field : An ordered field which satisfied the Archimedian property (refer lesson 1)


- ### $\mathbb Q$ is the set of fractions that is an Archimedian ordered field.

- ### with this we define a very important map which is defined for all rational number $\mathbb Q$.
  - ### The absolute value map : |x|
    $\forall$ x $\in$ $\mathbb Q$ : |x| := { x if x>=0 else -x if x<0}
    
    This is our good old modulus map.
    This is more generalised using lp norm or metric in functional analysis.

Modulus essentially tells us the distance from 0 (identity element) in ordered field $\mathbb Q$

- IMAGE<image>


### Why isn't having rationals enough? Why do we need reals?

- This is because rational numbers are not complete. To put bluntly, there are holes in rational number set. There are sequences in rational numbers which has a limit outside of the set of rationals.

Take the infamous example:
 - There is no x in rationals such that $\ x^2$ = 2. We already know solution to this is irrational. But right now we only know about rationals and don't know if irrationals exist.

 Now we take a sequence of rationals to illustrate this even better.

$$
x_1 = \frac{14}{10}, \quad x_1^2 = \frac{49}{25} \\[10pt]
x_2 = \frac{141}{100}, \quad x_2^2 = \frac{19881}{10000} \\[10pt]
x_3 = \frac{1414}{1000}, \quad x_3^2 = \frac{499849}{1000000} \\[10pt]
x_4 = \frac{14142}{10000}, \quad x_4^2 = \frac{49999011}{100000000} \\[10pt]
x_5 = \frac{141421}{100000}, \quad x_5^2 = \frac{19999899241}{10000000000}
$$

with each term in the sequence the square gets closer to sqrt(2).
We were finding such a x indeed. But we are only able to approximate such x.
This suggests the limit does not exist of such a sequence and there must be holes in rationals.
Hence this space is incomplete.

We can't define notions of continuity and differentiability without having complete spaces and hence need for reals. Reals are a by product of filling the holes in these rationals.

Therefore, we have to expand the number set even more.


### Notice the above sequence carefully. With each member the distance between adjacent members get smaller and smaller. What distance metric are we using here? It's |x|! Thats why we defined it earlier.
#### Notice $\ |x_2 - x_3|$ has a larger gap between them than $\ |x_4 - x_5|$ . This sequence of difference of absolute values, keeps getting smaller.

This notion of absolute value of differences of two terms give rise to Cauchy sequences, which is a generalization of convergent sequences. (refer lesson 3)

## Cauchy Sequnces :
  - Definition : A sequence $(x_n)$ is called a $\textbf Cauchy sequence$ if for every $\ epsilon > 0 $, there exists a positive integer $N$ $\in$ $\mathbb N$ such that for all $m, n \geq N$, we have $|x_n - x_m| < \epsilon$.

Formally, $(x_n)$ is a Cauchy sequence if:
$$
\forall \epsilon > 0, \exists N \in \mathbb{N} \text{ such that } \forall m, n \geq N, |x_n - x_m| < \epsilon.
$$

Here, $(x_n)$ is a sequence where $n \in \mathbb{N}$ and the sequence is a map from $\mathbb{N}$ to $\mathbb{Q}$.

Image<image>


### To make this cauchy sequence convergent we try to form a complete space with no holes. Resulting in reals.

This leads us to the completness axiom next.

### Few important properties of abs map :
  - |x * y| = |x| * |y|
  - | x+y | $\leq$ |x| + |y| (triangle inequality)
    - proof : We know, x,-x <= |x| ^ y,-y<=|y|  (^ is and).
    It means that x+y <=|x|+|y| ^ -(x+y)<=|x|+|y| ---(1)
    Note |x+y|= x+y when x+y>=0 else -(x+y) but from --(1) we know both of these are <= |x|+|y|
    Therefore, |x+y|<=|x|+|y|

    $\blacksquare$

Task : Prove reverse triangle inequality using first principles

We already proved convergent sequences are Cauchy in lessons 1-3. To see when Cauchy is convergent we define reals.

# Axiomatic Solution :

- A non empty set $\mathbb R$ together with operations +,* and ordering $\leq$
is called the real numbers if it satisfies:
  - ($\mathbb R$, +, 0) is an abelian group.
  - ($\mathbb R$ \\ {0}, *, 1) is an abelian group.
  - Operation * distributive over +

  First three properties makes it a field. Because it has identity element 1, properties of ring, commutative ring, multiplicative inverse for every element.
  - $\leq$ is a total order compatible with +,* and Archimedian property. These 4 together forms ordered field which satisfies $Archimedian-property$.
  These 4 are also satisfied by rationals. So we apply the most important axiom next. Which defines the reals.

  - Completeness Axiom. What that means in this context is "$every -Cauchy-Sequence-is-also-a-convergent-sequence$". This forces the space of reals to have no holes making it contain both rational and irrational.

### Important Facts : There $\exists$ a set S with all these properties. We can construct it from axioms of set theory (existence).
And
### It is uniquely determined with these properties.(uniqueness)


## Example Proofs :
  1. Prove $\forall$ x $\in$ $\mathbb R$, we have : 0 * x = 0 ( by only using axioms)

     - Proof : 0*x  $\in$ $\mathbb R$ by closure of *
    
       0 * x + (-0*x) = 0 (inverse exists)

       operating on lhs

       ((0+0)*x) + (-0*x) = (0*x + 0*x) + (-0*x) (identity and distributive property)

       0*x + (0*x + (-0*x)) = 0*x + 0 (associative property)

       => 0*x = 0

       $\blacksquare$

Similarly prove for : show $\forall$ x $\in$ $\mathbb R$, -1 * x = -x.

## Construction :
  - Outline - start with rationals then construct a complete ordered Archimedian field where every Cauchy sequence is convergent.


  - Define C := {($\ x_n$) | $\ x_n$ $\in$ $\mathbb Q$ $\forall$ n $\in$ $\mathbb N$ and ($\ x_n$) is a Cauchy sequence }

    
  - For two equivalent ($\ a_n$),($\ b_n$) sequences from C we can define ($\ a_n$) ~ ($\ b_n$) :<=> ($\ a_n - b_n$) convergent with limit 0.

  This means if we have two Cauchy sequences from C (set of all cauchy sequences with sequences members in rationals) such that they get arbitrarily close to each other. Since both sequence members get closer to eachother the limit is 0. We can choose such sequences from the set. And clearly we can define a equivalence relation that these two sequences are equivalent as they get approach the same limit.

  - Equivalence class [($\ x_n$)]eq ={($\ a_n$) | ($\ a_n$) ~ ($\ x_n$)}

  - From this equivalence class we define : { [($\ x_n$)]eq | ($\ x_n$) $\in$ C }

  This set of all equivalence classes of ($\ x_n$) where each ($\ x_n$) is an element of C defines the Reals. Can you see how it fills the gaps?



# Completness axiom (more generally)

- statement : if M subset R is non empty and has upper bound then it has a least upper bound (in $\mathbb R$).


![Let's recap upper and lower bounds and supremum and infimum](/Real%20Analysis/media/supinf.png)

Let's recap what we learnt earlier in the lessons.

Suppose we have a set (2,5) then every number greater than all the numbers in the set is the upper bound of the set. Among all these upper bounds we find the least one to get the Supremum. We do the opposite for infimum.


The statement of completeness axiom points towards existence of supremum. What about infimums?
The full picture is that infimums exist as well if subset of Reals is bounded below. Let's prove it.

### **Claim : Let A $\subseteq$ $\mathbb R$ and A is bounded below by m and non empty. Then infimum exists for set A.**
#### - Proof : **Define -A = { -a | a $\in$ A} we know m<=a $\forall$ a $\in$ A ; This implies -m>=-a $\forall$ -a $\in$ -A; So we found an upper bound for -A. So there exists a supremum of -A.**

#### **Now we need to show - sup(-A)=inf A to conclude the proof.**

#### **sup(-A)>=-a $\forall$ -a $\in$ A**
#### ** - sup(-A)<=a $\forall$ a $\in$ A**
#### ** - sup(-A) is lower bound of A**
#### we now need to show it is greatest lower bound of A.
#### SFC : $\exists$ x > -sup(-A) with x<a for all a in A.
#### Then by negation : -x < sup(-A) with -x>=-a for all -a in -A.
#### which means -x is less than supremum of -A but -x is also greater than all elements in -A. (><)

#### This is a contradiction so - sup(-A) is indeed the greatest lower bound of A (inf A)

#### $\blacksquare$


-------------------------------------------------------


## Nested Interval Property ( consequence of completeness axiom) aka Cantor's Intersection Theorem.

- statement : For each n $\in$ $\N$, assume we are given a closed interval $I_{n}$ = [$a_{n}$,$b_{n}$] = {x $\in$ $\R$ ; $a_{n}$<=x<=$b_{n}$}. Assume each such interval $I_{n}$ contains the next one $I_{n+1}$. Then we have

$$
I_n \supseteq I_{n+1} \supseteq I_{n+2} \supseteq I_{n+3}...
$$
where n belongs to Natural numbers. So it is for n=1,2,3,4...
This property claims that intersection of all these intervals is non empty.

![nested interval](/Real%20Analysis/media/nextedinterval.png)

Example : L = (0,1/n).
This set has open interval so nested interval property doesn't apply. Did you think it applies? Pay attention! Read the statement again.😉

Next one is a real example:
Let $k_n$ = [-1-$\frac{1}{n}$, -1+$\frac{1}{n}$]
Here it starts from [-2,2] for n=1 and tends to [-1,1].

## Proof : We need to show there exists an x in $ \R$ such that x lies in all of the $ I_n$ . Which will show that intersection of all these intervals is not empty and there exists atleast one element x.

  - structure : 
    - We will take set of all $ a_n$. Let's call this set A. Then all these $a_n$'s will be lower than any arbitrary $b_n$. Clearly $b_n$ is an upper bound of set A.

![nested interval 2](/Real%20Analysis/media/nextedinterval.png)
  -  - Then since A has a upper bound, by completeness of reals, it has a supremum. Let this supremum be x.

     - Then if we take any arbitrary interval $I_n$ = [$a_{n}$,$b_{n}$] we can say x belongs in that interval. Why?

     - x is supremum of set A. Which means it is the least upper bound. So all other upper bounds are greater than x. Which means x is less than or equal to all $b_n$. In particular $a_{n}$<=x<=$b_{n}$ for all Intervals.

  $ \blacksquare$


### This property highlights that there are no holes in reals. It uses the completeness axiom to do so.

