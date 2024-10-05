### A Brief Note on Where All this starts:

Algebraic structures provide a framework for studying and generalizing various mathematical concepts. Numbers which we deal with are itself not very general. Generalization allows us to see the true nature of mathematics and frees it from all underlying biases.

#### Abstracting away details from specific objects in mathematics and making them more general makes complex things simpler. It provides a strong foundation to mathematics and to the fact that it's the language of the universe.

#### This generalization also helps to transfer the abstracted knowledge and apply it in other fields in very specific form. Here for example we are talking about numbers but sets are more general form of these numbers. We are tranferring that general idea of sets and defining mechanisms to apply it here.

For example : 0 = {}, 1= {{}}, 2 = {{},{{}}},...

This better known as Von Neumann Construction helps us to abstract this idea of numbers to more general algebraic structure called sets.

### A short tour:

SImilarly we define integers, study cardinality and ordinality of integers, we see how natural and integers have same degrees of infinity. Which we later call countably infinite. Then we find that rationals and integers have same cardinality. We go a level higher and find real numbers which are complete (no holes). We also find that reals have a higher cardinality than all the former structures using **Cantor's Diagonalization Argument**. It gave rise to the concept of **varying sizes of infinities**. This resulted in a hypothesis called **continnum hypothesis** which says that there is no set whose cardinality is between rationals and reals. After which imaginary came into picture and we defined complex numbers from real numbers.

#### But notice within all this progress lies algebraic structures like sets,semigroups, monoids, groups,abelian groups, rings, fields, modules, vector spaces, algebras and lattices.
#### We can rigorously define all these here but we'll give a brief idea for now. For all their definitions you can check [here]()
You should know how everything falls into place so here is a brief introduction.
Starting with sets:

Sets: The most basic structure, consisting of a collection of distinct elements.

MAMGMA : sets with closed operation.

Semigroups: Magma with an associative binary operation.

Monoids: Semigroups with an identity element.

Groups: Monoids where every element has an inverse.

Abelian Groups: Groups where the operation is commutative.

Rings: Sets with two binary operations (addition and multiplication) that generalize the arithmetic of integers.

Fields: Rings where every non-zero element has a multiplicative inverse.

Modules: Generalizations of vector spaces where scalars come from a ring instead of a field.

Vector Spaces: Modules over a field.

Algebras: Vector spaces equipped with a bilinear multiplication operation.

Lattices: Sets with two binary operations (meet and join) that are commutative, associative, and idempotent.


#### We mostly dicussed about rings and fields in the [completeness](/Real%20Analysis/extras/real_analysis/completeness.md) page abstracting away details of other algebraic structures. This is the power of abstraction and a field like computer science heavily relies on it.

Here is a big picture,

![morenotegroup](/Real%20Analysis/media/morenotegroup.png)
![morenotering](/Real%20Analysis/media/morenotering.png)

### Note rng and ring are different, the former doesn't have 1 which is the identity eleement for '*' operation.

***The main thing to notice here is how vector spaces are defined using magma and field. This will come up in the linear algebra series.***
