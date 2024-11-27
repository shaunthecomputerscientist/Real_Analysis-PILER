### Introduction :
So far we covered really important ideas in real analysis. Most of these ideas form foundation of real analysis. If you read about [completeness axiom](/Real%20Analysis/extras/real_analysis/completeness.md) then you know the process. We start from defining natural numbers (you can use peano axioms), then integers. Then we define rationals. Since rationals were not complete we put even more restrictions and made it complete ordered space using reals.


- **We talked about notions of sequences of real numbers to study them better. These notions will further help us define functions of real numbers.**


- **Next we will talk about notions of closeness, compactness, boundary points, open/ closeness, etc.**

- **These notions are only possible when there is a metric defined along with a set. A metric helps us formulate idea of distances. But metric spaces are not the most general abstraction in itself. metric spaces are just a subset of topological spaces which we typically study in a topology course.**

- **With respect to reals and sets of real numbers, we can prove that it's a metric space so notion of distance is possible.**

Let's first formally define what a metric space is,


### Metric Spaces :

**Let X be a non empty set and define $d(x,y)$ as a metric function for x,y $\in$ X, where $d(x,y)$  : (X $\times$  X ---> $\R$)**
Then such a map is called a metric if,
1. d(x,y) $\geq$ 0 where equality occurs when x=y. (positive definiteness)
2. d(x,y)=d(y,x) (symmetric)
3. d(x,z) $\leq$ d(x,y) + d(y,z) (Triangle inequality)

Then such a map along with set X is called a metric space.

##### Now we can use the axioms to show $\R$ forms a metric space under a metric d(x,y)=|x-y|.
why is this metric sensible?

**- because x and y are scalars with 1 dimensional freedom (single number line) so we can define a metric which will measure distance between two points both of which are 1 dimensional by simply taking the magnitude of the diffference.**

- Proof :
    - |x-y| = 0 if x=y, else always positive (>0) since |element|>0 for all element $\in$ $R$
    - |x-y| = |-(y-x)| Then if 
        - y-x<0, |-(y-x)|= -(negative number) = positive number (mod opens with positive +)
        - y-x>0, |-(y-x)|= -( -(positive number)) = -negative number= positive number (mod opens with -)
        - So using the property |a|=|-a| we can conclude the symmetric property.
    
    This shows that result will always remain the magnitude of the difference and magnitude remains the same in both the cases, the internal sign may change, resulting in symmetric property.
    - Notice the triangle inequalities, ||a| - |b|| $\leq$ |a - b| $\leq$ |a + b| $\leq$ |a| + |b|. [We proved this here](/Real%20Analysis/extras/real_analysis/completeness.md).

    - Alternatively we can use Cauchy Swartz inequality to prove the triangle inequality.
      - Structure : Take (x-ay)^2 = (x-ay)(x-ay), on exapnding you get a quadratic whose discriminant resembles Cauchy swartz inequality (|xy|<=|x||y|). You can arrive at triangle inequality from there. (exercise)

**All these ideas carry forward to vector spaces as well.**

**In more general topological spaces we do not define notions of distances because thats', well, not general. It's important to note that in order to generalise these notions of spaces we need to remove specialised notions/characteristics. In topological spaces we define space using open sets which are more general and depends on your construction of open sets. That's story for another day.**




**Recall definition of epsilon neighbourhood**

1. **Definition** : For $\epsilon$>0 : (x+ $\epsilon$,   x-$\epsilon$ ) := $\beta_{\epsilon}$ (epsilon neighbourhood of x)
    - M $\subseteq$ $\R$ is called epsilon of x if there is $\epsilon$>0 such that M $\supseteq$ $\beta_{\epsilon}$.


[-2,2] is a neighbourhood of 0 and 1 but not of 2.

![neighbourhood12](/Real%20Analysis/media/epsiloneighbourhood1.png)

Notice there is a epsilon positive and interval [-2,2] is a superset of the epsilon neighbourhood of 0. Since there exists such an epsilon for which epsilon neighbourhood of 0 becomes subset of [-2,2] we can say [-2,2] becomes a neighbourhood of 0.

But for [-2,2] 2 is a point which is in the interval, but there does not exist any epsilon positive for which our interval becomes superset of 2.

![neighbourhoodofpoint2](/Real%20Analysis/media/epsilonneighbourhood2.png)

No matter what epsilon we take the interval [-2,2] won't be a superset of epsilon neighbourhood of 2.


***So here we have a set or interval where there are points within the interval whose epsilon neighbourhood is not in the set. Such a set is hence called open. COntrast it with the case where we do not include -2,2. See what will heppen.***

### Let's Briefly talk about boundary points and interior points;

1. #### Interior Points
- **Definition** : A point $x_{0}$ $\in$ D $\subset$ $\R$ is called interior point of D if there is a small epsilon neighbourhood $\beta_{\epsilon}$( $x_{0}$ ) such that D is a superset of $\beta_{\epsilon}$( $x_{0}$ ). The main thing here is that such an epsilon should exist, no matter how small or big. If there exists such an epsilon such that the interval,
$$ (x_{0} - \epsilon , x_{0} + \epsilon) \subset D$$

then we can say that **this point is an interior point.**

**In more general topological spaces apart from these metric spaces or limited space of Reals, we generalize this definition. There we do not talk about a neighbourhood which has one dimension to move like in real numberline. We talk about a more generalised ball on the set. If such a ball with epsilon radius is within the set, it becomes an interior point.**

![alt text](/Real%20Analysis/media/interior%20and%20boundary.png)

2. #### Boundary Points
- **Definition** : A point $x_{0}$ $\in$ D is called a boundary point if the set D and $D^c$ both have non empty intersections with any epsilon neighbouthood (ball generally) of the point $x_{0}$ as you can see in the picture as well. No matter how small or big epsilon is if we take intersection of that set with both D and it's complement we get non empty set, suggesting that it's at the boundary of those two interfaces. More formally,

$$\forall \epsilon > 0 , \exists p_1,p_2 \in \beta_{\epsilon}(x_{0}) | p_{1} \in D, p_{2} \in \R - D ~ or ~ (D^c)$$

**Note : The set of interior points in D constitutes its interior, int(D)
, and the set of boundary points its boundary, ∂D
. D
 is said to be open if any point in D
 is an interior point and it is closed if its boundary ∂D
 is contained in D
; the closure of D is the union of D
 and its boundary:**

$$ cl(D) := D \cup ∂D$$

where cl(D) is closure of D. We will define notion of closure after defining Open and Closed Sets.

***Let's take a moment to appreciate the genius of these definitions which are derived from these simple fundamental ideas. Without this mathematical rigour we won't have a concrete way to convey these ideas which are true universally with these constraints.***


- # Open Set:
  - Definition : M $\subseteq$ $\R$ is called open (in $\R$) if , for all x in M, M is a neighbourhood of x.

  $\forall$ x $\in$ M , $\exists$ $\epsilon$ > 0 : M $\supseteq$ $\beta_{\epsilon}$(x)

  ![alt text](/Real%20Analysis/media/opensetexample.png)

  Notice since we are not taking points at the boundary, for all the points we take, there will always exist an epsilon neighbourhood no matter how small. This neighbourhood will always remain within the set. And hence for all points in the open set we will always have their epsilon neighbourhood inside the set.

  Using this definition we can define closed sets now.

  - Alternate Definition : A $\subseteq$ $\R$ is called closed (in $\R$) if $A^c$ := $\R$ \ A is open. Which means if the complement of the set is open then the set is closed. Or if it doesn't contain it's boundary points.


#### - Common Misconception : It is important to note that the opposite of open set is not closed set and vice versa. Why?


Example : $\phi$ and $\R$ are both open and close. So these ideas of openness and closeness are not mutually exclusive.
**(Note here $\phi$ is the empty set so it complement of set of $\R$ which the universal set here)**

1. Why are they open? : For $\phi$ which is the empty set, it doesn't have any elements to satisfy the condition here (  $\forall$ x $\in$ M , $\exists$ $\epsilon$ > 0 : M $\supseteq$ $\beta_{\epsilon}$(x)). There is not for all x in M to begin with. So this set is open ***trivially***.

    For set of $\R$ if we take any element within the set, it's epsilon neighbourhood will always remin within R, no matter how smallor big. So it's trivial case.


2. Why are they closed? : $\phi$ is complement of $\R$ and $\R$ is complement of $\phi$. What's complement ofopen set? It's closed. Since both are open, their complements will be closed. Hence both are closed.


Other examples : [-2,2] is closed, (-2,2) is open. (use definitions to verify). But if we take a set like (-2,2] it doesn't satisfy conditions for being open/close so it's neither open nor closed.

#### But these are simple intervals. Sets can be much more complicated, therefore we look at the next definition.


## Closed Sets:
  - Definition : A set A $\subseteq$ $\R$ is called a closed set (in $\R$) if and only if (bidirectional) $\forall$ convergent sequences $(a)_n$ with $a_n$ in A for all n $\in$ N, we have:

$$\lim_{{n \to \infty}} a_n = a$$
where a is in set A itself. For all such convergent sequences with sequence members in the set A, we basically have their limits within the set as well. This implies A is closed.

**We are studying this notion for real number line but just to introduce few ideas of topology i will present the more general version of this. You will see how sequences are so fundamental that we are using them to construct notion of closeness.**


### Theorem : A set if closed ***iff*** it contains all it's accumulation/limit points.

  - proof : We will use proof by contraposition here (if p => q then ~q =>~p is equivalent) in the later case i.e, A contain all it's limit points => it is closed.

    - (i)First we will use contradiction for p=>q :
        Suppose for contradiction, there exists a limit point x of A with x $\notin$ A. Recall definition of limit points:
        x is limit point of A if there is a sequence with it's members in A\ {x} and it converges to x.

        We assumed x is not in A. So x must be in $A^c$. Since A is closed => $A^c$ is open. This implies there is a neighbourhood let's say some delta neighbourhood of x in A which is entirely in A. ( Since $A^c$ is open)

        if $\epsilon$ = $\delta$ then since $(a)_n$ ---> x => $\exists$ N | $\forall$ n > N , |$(a)_n$ - x| < $\epsilon$ = $\delta$ and thus $(a)_n$ $\in$ (x-$\delta$, x+$\delta$).

        This is a contradiction because members of sequence $(a)_n$ can not lie outside set A by definition of limit point. But this shows that it lies in $A^c$.

    - (ii) Now we need to show that If a set contains all it's limit points => It is closed. We will prove contrapositive of this. Let the set be not closed => it will not contain all it's limit points. We do this by taking an element x from $A^c$ and showing it is a limit point of A.
      - Assume A is not closed => $A^c$ is not open. This means there exists some x in $A^c$ such that every $\delta$ neighbourhood of x not within $A^c$ => x $\in$ A.

      - For each n $\in$ $\N$ take $a_n$ $\in$ $\beta_{\frac{1}{n}}$(x) $\cap$ A. Then for $\epsilon$ > 0 and N > $\frac{1}{n}$ we have for all n > N, |$a_n$ - x | < $\epsilon$. Which means the sequence converges to x. So we took sequence members in  A but the limit point is outside A in $A^c$. Thus we proved if a set is not closed then it will not contail all it's limit points.


       $\blacksquare$







### Closure of a set : The closure of a set is the smallest closed set that contains the set. It can be defined as intersection of all closed supersets that contains the set. ***(Note intersection of closed sets in closed and union of open sets is open. Every finite union of closed sets is closed and finite intersection of open set is open.)***


**The idea of closeness of a set is a property of a set. A set may or may not be closed. But closure in itself is an action we perform on a set. By definition, closure of a set A is closed. Note we are not saying set A is necessarily closed or it has the property of being closed. But there is an action which gives us a closed set out of any set(loosely) A.In any case closure of A will be intersection of closed supersets of A.**


### Theorem : ***Closure of E = E iff E is closed***.

  - If we have a set E whose closure is the set itself then E must be closed and vice versa. It's fairly logical. Imagine a set E. And we take intersection of all closed supersets of E. If we get E as the result then E must be the smallest closed set here.

  - Proof : 
    - 1. Let cl(A)=A. Since closure of A is closed by definition it implies that A is also closed. (Easy Huh!!!)

    - 2. Let A be closed. Then we need to prove cl(A) = A
      - Let **x** $\in$ A, then cl(A)=$\cap${C| C is closed and A $\subseteq$ C} = $\cap${$C_{1}$,$C_{2}$,$C_{3}$,$C_{4}$,...} where all $C_{i}$ 's are closed and contain A. Then closure of A must contain our original point **x**. This imples,
      $$=> cl(A) \supset A -(i)$$

      Because for any arbitrary point x in A, x also lies in cl(A) which suggests that cl(A) is superset A.

      - Let x $\in$ cl(A). Spse for contradiction x not in A. Then x $\in$ $A^c$. Given A is closed => $A^c$ is open. But this is a contradiction since x can not lie in an open set as we assumed x lies in cl(A) which forms a closed set. Hence x lies in A.
      $$=> cl(A) \subset A -(ii)$$


      From -(i) and -(ii) cl(A) = A.

      $$\blacksquare$$


## Compact Sets:

- Definition : A $\subseteq$ $\R$ is called compact if for all sequences ($a_n$) with $a_n$ $\in$ A $\forall$ n $\in$ $\N$, there is a convergent subsequence $(a_{n_k})$ with $\lim_{k->\infty}$ $(a_{n_k})$ $\in$ A.

This essentially says for all sequences with sequence members in A, if there is a convergent subsequence with limit in A, then A is compact. Notice this definition necessarily makes A closed. So a compact set is **necessarily closed** .


This is because compact sets talk about subsequences as opposed to sequences in the definition of closed sets. Subsequences are a more general notion and we know every sequence is a subsequence of itself. So if every subsequences needs to converge in A, naturally every accumulation point will be in A. And from closed set definition if every sequence with terms in A converge in A, it's by deifinition closed.


A theorem which ties this notion of compactness with closeness and boundedness is the Heine Borel theorem.


Examples :

1. $\phi$ trivially compact since it does not have any element.
2. {5} this is a set with just one element. This is compact because it's sequence and subsequence will be the same and limit will lie inside the set itself which is 5.
3. $\R$ is not compact because there exists a seuqnece whose accumulation/limit point are not in $\R$ namely the divergent sequence ($a_{n}$) = $(n)_{n \in \N}$.
4. [c,d] be a closed set st c<=d. It is compact.

Proof : LEt $(a_{n})_{n \in \N}$ be a sequence in the interval. Since it's in a closed interval, the members of the sequence is bounded from above and below.

=> $(a_{n})_{n \in \N}$ is bounded.

By Bolzano Weirstrass theorem, every bounded sequence has a convergent subsequence so $(a_{n})_{n \in \N}$ has convergent subsequences for any subsequence. This accumulation point is trivially inside the interval because the interval is a closed set.
This ensures that for sequence members in the interval the must also lie within the interval. Therefore the interval is compact.

## Heine Borel Theorem :

- Statement : For A $\subseteq$ $\R$, we have
A is compact iff A is bounded and closed.

Proof : 
  - (<=) Use Bolzano Weirstrass Theorem

  - (=>) Assume set A is compact. Let ($a_n$) $\subseteq$ A be a convergent sequence with limit a' $\in$ $\R$. Since A is compact ($a_n$) must have accumulation value in A. Let this be a $\in$ A. Since ($a_n$) is a convergent sequence it should have only one accumulation value, namely limit. Therefore a=a' $\in$ A.

    - Hence A is closed.
  
    Proof for boundedness (contraposition):
      - Assume A is not bounded.Then since A is compact there is a sequence ($a_n$) $\subseteq$ A with |$a_n$|>n for all n $in$ $\N$. And such sequences do not have an accumulation value as any subsequence we choose will not converge,
      => A is not compact.

    $\blacksquare$

Note: here we explicitly did not use definition of bounded set. It's already known and discussed. A set if bounded if for all elements in the set the elements are between some m,M in R.
