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

Let $P$ be the statement that 
$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$. 

And let Q be the
statement that $f(n)\in O(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) \leq c g(n)$.

To prove $P \implies Q$ we'll use a proof by contradiction, let's start by assuming:

$P \wedge \neg Q$

Or in other words using our definitions above:

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$ is true.

while

$f(n)\in O(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) \leq c g(n)$ is false.

This creates a mathematical contradiction, essentially what we've assumed is that:


$f(n) < c g(n)$ while simultaneously $f(n) > c g(n)$ when
$\forall c>0, \exists n_0, \forall n\ge n_0$

This means that the opposite of our assumption must be true, meaning that $P \implies Q$ is true by contradiction.