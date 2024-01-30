# Little-o

In addition to the big-O, big-$\Omega$, and big-$\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little-$o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$


# My proof

For a function to be an element of big-oh there must exist constants $c$ and $n_0$ such that $T(n) \leq c f(n), \forall n \geq n_0$. 

And for a function to be an element of little-oh then for ANY positive constant $c$ there exists an $n_0$ such that $T(n) \lt c f(n), \forall n \geq n_0$. 

Using a direct proof let's assume that $f(n) \in o(n)$, meaning that for ANY positive constant $c$ there exists an $n_0$ such that $T(n) \lt c f(n), \forall n \geq n_0$. Since little-oh is simply a more strict bound than big-oh, if a function is an element of little-oh, it would HAVE to also be an element of big-oh. The reason being that a function can't be an element of little-oh, and still meet the conditions to be an element of big-oh.
