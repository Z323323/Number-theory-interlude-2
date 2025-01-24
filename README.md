# Number theory interlude 2

<p>
  This article extends [https://github.com/Z323323/Number-theory-interlude-1].
</p>

## Solovay-Strassen test

<p>
  To fully understand this section you should have read [https://github.com/Z323323/Quadratic-residues].
  
  I won't delve this test, since this test is worse than Miller-Rabin's and the linked resource is self-explainatory. Just note that everything reduces to

  $\displaystyle (\frac{b}{r})$

  which has $1/2$ probability of pass the test, thus ~half of the times a Carmichael number will fool this test too.
</p>

## $\sum_{d | n} \phi(d) = n$

<p>
  Refer to [https://crypto.stanford.edu/pbc/notes/numbertheory/mult.html].

#### Proof

You can find the proof at [https://crypto.stanford.edu/pbc/notes/numbertheory/cyclic.html] but I'm bringing it back here using different words and providing an example to show the actual power of this theorem.

The crazy intuition is considering $n$ as the order of a multiplicative group. This means that

$\phi(z) = n$

We know that every multiplicative subgroup of $Z_{z}^{\ast}$ will have order $o$ such that

$o | n$

This means that finding $\sum_{d | n} \phi(d)$, means finding the number of generators for every subgroup, (refer to 'Generators theorem' section at [https://github.com/Z323323/Group-theory-elements/blob/main/README.md]) and this in turn means that we are finding the whole number of subgroups. Since the whole number of subgroups equals $n$, the theorem follows.

These proofs really blow my mind since they prove such a complex theorem in such a quick way. 

Since this proof is quite unbelievable at first (note that the proof for 'Generators theorem' I linked has been refined after this one, hence why I was shocked about this theorem), I'm providing a quick example below. Let $Z_{41}^{\ast}$, then

$n = \phi(41) = 40$

Initially we can recognise that $\phi(40)$ should be the number of generators, and following this theorem we get that there are $\phi(2^35) = \phi(2^3)\phi(5) = 4*4 = 16$. Indeed if you shoot my Zn.py you'll notice that there exist exactly $16$ generators for $Z_{41}^{\ast}$, but this theorem allows us to get a new power, that is, taking a random $d$, like $10$, we get

$\phi(10) = \phi(2)\phi(5) = 4$

Remember that we will need to only consider the subgroups having exactly an order $o = 10$, since we will find $1$ at the the $10t\lambda$ position for subgroups having $o = 2$ and $o = 5$. If you check this result you will find out that it's correct, hence now we can immediately know how many subgroups exist for a given order $o | n$.

</p>

## Perfect numbers

<p>
  
</p>
