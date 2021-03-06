# A note on a Claim of Eldar & Hallgren: LLL already solves it

following up on the presentation of Sean Hallgren at the Simons Institute
https://simons.berkeley.edu/events/efficient-quantum-algorithm-lattice-problems-achieving-subexponential-approximation-factor

Wessel and myself wrote a note (available on this repository) 
on what the state of the art has to say on those specific 
BDD instances studied by Lior and Sean.
https://github.com/lducas/BDD-note/blob/main/note.pdf

The first remark is that they are already considered easy in
the average-case for standard classical lattice reduction 
algorithms. With due diligence, we can in fact prove this is 
also true in the worst-case. This requires no new idea. The
algorithm is just straight up LLL+Babai.

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

    k * log(q) / log^2(α) < cste .
