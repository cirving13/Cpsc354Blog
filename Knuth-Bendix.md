Knuth-Bendix Completion Algorithm
=================================
This is an algorithm that attempts to transform a finite set of identities into a finitely terminating, confluent term rewriting system whos reductions preserve the identity. This system serves as a procedure for validating identities.

The algorithm works by taking a set of equations, and a reduction ordering on the set of all terms, and tries to construct a confluent and terminating rewriting system that has the same closure as the initial set of equations. Proving the consequences from the initial set of equations most likely requires human intuition and reasoning , but there is no human involvement required for proving anything from the rewrite system produced by the algorithm. This algorithm has the potential to automatically prove confluence and termination, assuming the given set of equations and the reduction system are valid for all terms. 

The algorithm may:
  1. Terminate with success and have a confluent and terminating set of rules
  2. terminate with a failure
  3. loop endlessly without termination, resulting in a failure, or a program that must be killed manually

Group Theory
========================================
There are numerous applications for this algorithm, one of the most prevalent is in group theory with string rewriting. The Knuth-Bendix algorithm can be used to give canonical labels to elements or cosets in a finite group as products of the generators of such group. This happens by giving a set of lemmas and a term rewriting system and allowing it to run through a set of relations to prove that the rewriting system is confluent. This can go through a set of values and conclude that it is terminating, or non terminating depending on the monoid provided to the algorithm. 

Buchberger's Algorithm
======================
An algorithm that is similar to the Completion algorithm is one that is used in some fields of computational algebra, called Buchberger's Algorithm. It is a method of taking a set of polynomials (for an ideal, a subset of a ring) into a Grobner basis with respect to some monomial order. It is a more general way to view the Euclidian Algorithm for Greatest Common Denominator, as well as Gaussian elimination for linear systems (matrices). This algorithm acts very similarly to the Knuth-Bendix algorithm in the sense that it takes in a set of equations and attempts to compress it down into a terminating and confluent reduction system
