Last time we studied about Monotone Convergence Theorem, subsequences, how limits of subsequences relates to limit of sequences and accumulation values. Today we will continue where we left.


Today we will start with an important Theorem, $Bolzano-Weierstrass-Theorem$

## Theorem : Every bounded sequence has a (atleast one) convergent subsequence in $\R$ (atleast one accumulation point exists)

### Proof : 
   - Imagine a bounded sequence like this. It has both upper and lower bound so it's bounded in $\R$
![bounded sequence](/Real%20Analysis/media/bolzano1.png)
  - Define an interval from lower to upper bound. Call it [$c_0$,$d_0$]. Divide the interval in half, and choose the part which has infiniely many sequence members in it.
  ![bolzano2boundedsequence](/Real%20Analysis/media/bolzano2.png)
  - Let's say right half has infinitely many sequence members. Then let the midpoint be $c_1$ and $d_0$ := $d_1$. Now we have a new interval [$c_1$,$d_1$]
  ![b3](/Real%20Analysis/media/bolzano3.png)

  - Notice we can again divide the sequence in half. And keep on repeating the process. Each time the interval gets smaller and smaller and we take the interval which has infinitely many sequence members. So,
$$[c_0,d_0] \supset [c_1,d_1] \supset [c_3,d_3] \supset [c_4,d_4] ...\supset [c_n,d_n]...$$
  

  - Notice $c_0$,$c_1$,$c_2$,$c_3$,... forms an increasing sequence (monotonic). And $d_0$,$d_1$ forms a decreasing(monotonic) sequence. Which means they converge to some limit.
  We can try to find what these two sequences converge to.

  - Define $c_1$ - $d_1$ = $\frac{1}{2}$($c_0$ - $d_0$), similarly,
    $c_2$ - $d_2$ = $\frac{1}{2^2}$($c_1$ - $d_1$),..., $c_n$ - $d_n$ = $\frac{1}{2^n}$($c_{n-1}$ - $d_{n-1}$).
    If we take limit of this sequence $(c-d)_n$ as n tends to infinity, by p test it converges to zero.

$$ \lim_{n \to \infty} (c-d)_n = \lim_{n \to \infty} (c_n) - \lim_{n \to \infty} (d_n) = 0 $$
  - This means ($c_n$) and ($d_n$) have same limit. By using the limit laws we distributed the limits. We have studied about this before in lessons 1-3.

  - If you remember from previous lesson when we have a monotonic sequence which is convergent to a limit then every subsequence converges to same limit. But we won't use this fact for the proof here. We'll first create a subsequence.

  - You have seen

$$[c_0,d_0] \supset [c_1,d_1] \supset [c_3,d_3] \supset [c_4,d_4] ...\supset [c_n,d_n]...$$

 - We can create a subsequence using kth interval [$c_k$,$d_k$].
   Define a subsequence ($a_{n_k}$) where $a_{n_k}$ $\in$ [$c_k$,$d_k$] and $n_k$ is the index of the subsequence.

 - Since this subsequence lies between some $c_k$ and $d_k$ we can use sandwich theorem which we studied before.
 We know that $c_k$ $\leq$ $a_{n_k}$ $\leq$ $d_k$. And since both sequences are convergent then middle subsequence is also convergent. Infact to the same limit.
 Therefore, ($a_{n_k}$) where $n_k$, k $\in$ $\N$ is convergent.

$\blacksquare$

Note : This also holds for complex sequences (might be proved in complex analysis if i do a series in future)

# Limit Superior & Limit Inferior:

Let's recap what it means to be unbounded.

A sequence is divergent to $\infty$ if,

$$ \forall C > 0, \exists N \in \N | \forall n > N : a_n > C  $$

A sequence is divergent to - $\infty$ if,

$$ \forall C < 0, \exists N \in \N | \forall n > N : a_n < C  $$


Consider the following sequence,

![limsupinf](/Real%20Analysis/media/supinf1.png)


- Notice this sequence is divergent since it's increasing and unbounded (not bounded from above here). For these kinds of sequences we have improper accumulation values. We can choose any subsequence but eventually they will have improper limits.

- Okay so it's unbounded and keeps on increasing/ decreasing so it will have improper accumulation values. What about bounded?

- That's Just Bolzano-Weierstrass Theorem. Every bounded sequence has a convergent subsequence and hence an accumulation value.


#### Last time we also discussed a sequence can have many accumultion values. Can we comment anything on the smallest and largest accumulation values?

Both of these types of accumulation values get very special names.

Let ($a_n$) be a sequence $\in $ $\R$ Then a $\in$ $\R$ $\cup$ {- $\infty$,$\infty$} is called,
1. Limit Superior : if a is the largest accumulation value (proper/improper). Denoted by a = $\lim_{n \to \infty}$ sup $a_n$

2. Limit Inferior : if a is the smallest accumulation value (proper/improper). Denoted by a = $\lim_{n \to - \infty}$ inf $a_n$


Let's take an example,

![supinf2](/Real%20Analysis/media/supinf2.png)

#### This sequence looks chaotic. Sometimes it's up sometimes down, not very uniform.

### Observations :

  1. The top most point is an upper bound for the whole sequence and it's the least such upper bound so supremum. But if we remove finitely many points from this infinitely many points of the sequence we get a different supremum.

  what's the other name for removing finitely many points and choosing specific points in the sequence again?
  **It's called defining a subsequence**

  3. For example if a consider all k>=3 and ignore previous indices, we get a new supremum. Notice for points greater than points before index 3 has a new supremum if we start the sequence from there.

![supinf3](/Real%20Analysis/media/supinf3.png)

  4. If we consider terms greater than or equal to 9th term, then we get a different supremum. But also this becomes the accumulation value. Because from thereon the sequence members lie within some epsilon of the limit.


![supinf4](/Real%20Analysis/media/supinf4.png)

From this we have the following fact:
  
  - $\lim_{n \to \infty}$ sup $a_n$ = $\lim_{n \to \infty}$ Supremum{$a_k$ | k>=n}

  - $\lim_{n \to \infty}$ sup $a_n$ = $\lim_{n \to \infty}$ Infimum{$a_k$ | k>=n}

Obviously the largest accumulation value will become supremum of the subsequence similarly the smallest will become infimum.

#### Example : $(a_n)$= $(-1)^n n$ = (-1,2,-3,4,-5,6,-7,8,...)

In this case limit superior is + $\infty$ and limit inferior is - $\infty$. Also notice the fact that different subsequences (even and odd) are (divergent to positive infinity and divergent to negative infinity respectively) so the accumulation values become improper.

### Properties:

#### If the sequence was convergent we would get one accumulation value namely the limit. You know this fact from previous lesson. Because every term after some N will eventually become arbitrarily close to a limit no matter what the subsequence is taken.
So all accumulation values from any subsequence converges to limit of the sequence.
This leads us to conclude the following property.


1. ($a_n$) is convergent $iff$ $\lim_{n \to \infty}$ sup = $a_n$ $\lim_{n \to - \infty}$ inf $a_n$ $\notin$ {$\infty$, - $\infty$}

In other words the sequence is only convergent if limit superior and inferior are the same and they are not improper. (vice versa)

Similarly we can say that,

2. The sequence is divergent to + $\infty$ iff $\lim_{n \to \infty}$ sup $a_n$ = $\lim_{n \to - \infty}$ inf $a_n$ = + $\infty$

And similarly for - $\infty$.

3. For two sequences ($a_n$),($b_n$) we have,

$$ \lim_{n \to \infty} sup (a_n + b_n)  \leq \lim_{n \to \infty} sup a_n + \lim_{n \to \infty} sup b_n $$ 

only if **$RHS$** is defined (proper)

Similarly,

4. We have product rule for non negative sequences,

$$ \lim_{n \to \infty} sup (a_n * b_n)  \leq \lim_{n \to \infty} sup a_n * \lim_{n \to \infty} sup b_n $$

### These hold for infinums as well. The direction of inequality is flipped. Where equality occurs for convergent sequences.




You can check the validity of these inequalities yourself through examples. I will state one example here which might be tricky. You can take your own sequences and even prove the inequalities. You can use prove by contradiction for that.

**We shall now state an example :** ($a_n$)=(1,0,1,0,1,0,1,...) & ($b_n$)=(0,2,0,2,0,2,0,...)
Then ($a_n$*$b_n$) = (0,0,0,0,0,0,0,...)

$$0 = lim_{n \to \infty}sup(a_n * b_n) \leq lim_{n \to \infty} sup a_n *lim_{n \to \infty}b_n=1*2=2$$

These properties are useful when dealing with calculations proofs.