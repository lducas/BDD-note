# FAQ

** Does the note contain a new result on lattice problems ?

No. There is only a sudden focus on specific worst-case instances
that were previously undocumented, simply because the average-case
was the case of interest in crypto.

** Does the fact that it is a worst-case result invalidate the
underlying worst-case to average-case reasoning ?

No. Ajtai's and Regev worst-case reduction ranges over *all*
lattices. This polynomial time algorithm applies to a small
class of easy lattices.

** The note only deal with the case k=1, and q = c^n. What about
the general case ?

We will generalize the note as soon as we find the time to do so.
In the mean time, the best guess is that it would behaves as in
the random-case (LWE): BDD in deterministic poly-time for this
class of lattices when parameters satisfies:

    k * log(q) / log^2(α) > cste .
