[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/wM4-KOzy)

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

And for a function to be an element of little-oh then for ALL positive constant $c$ there exists an $n_0$ such that $T(n) \lt c f(n), \forall n \geq n_0$. 

Using a direct proof let's assume that $f(n) \in o(g(n))$, meaning that for ALL positive constant $c$ there exists an $n_0$ such that $T(n) \lt c f(n), \forall n \geq n_0$. Little-oh is simply a more strict bound than big-oh, reason being with little-oh $T(n) \lt c f(n)$ must be true for ALL positive $c$ and $n \geq n_0$, but with big-oh we simply have to find a single positive $c$ and $n_0$ such that  $\forall n \geq n_0, T(n) \leq c f(n)$ is true. Additionally little-oh requires $T(n) \lt c f(n)$ whereas big-oh loosens this bound to be $T(n) \leq c f(n)$.

Therefore if we assume that $f(n) \in o(g(n))$, based on our definitions the function would HAVE to also be an element of big-oh, as a function that meets the conditions for little-oh, would also meet the same looser requirements to be an element of big-oh. 
