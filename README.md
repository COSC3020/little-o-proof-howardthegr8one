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
$f(n)\in o(g(n))$. 

And let Q be the
statement that $f(n)\in O(g(n))$.

Let's assume that P is true, that is $\forall c>0, \exists n_0, \forall n\ge n_0: f(n) \lt c g(n)$. Since we're assuming P is true then we know $f(n) \lt c g(n)$ given the previous conditions. 

For $f(n) \in O(g(n))$ then $f(n) \leq c g(n)$ for the given $c, n_0$, and $n$ conditions above. Since we know that $f(n) \lt c g(n)$ then it's obvious that $f(n) \leq c g(n)$. Therefore when $f(n) \in o(g(n)) \implies f(n) \in O(g(n))$.