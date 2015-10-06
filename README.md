Lawley-Donovan-prime-probability
================================
Usage:
./{compiled program} [N] complexity]
where N is the maximum integer to stop at, and complexity is the factor to stop calculation at
(2, for the titular method.)

================================
Abstract from the Lawley paper:
The Lawley primality test is a constant-time, probabilistic primality testing algorithm that determines
if a number is a composite or a probable prime.
Let n be the positive integer to be tested. If n is even, the number is composite. If n is odd, the
number is "probably" prime; roll d6, and if you get 1 or 4*, return prime. Otherwise, return composite.
The algorithm has achieved phenomenal experimental results: for the first 100,000 positive integers, it
achieves a false negative rate as low as 6% and a false positive rate as low as 13%. These numbers place
it very close to leading probabilistic primality testing algorithms (most of which achieve 0% error
rates across the board) at a fraction of the complexity.
In the event of a user leveraging the Banner revision, the program simulates a large die collection, each die being sized based on theorems by Hadamard and Poussin indicating that for large x the likelihood that a number within (1, x) is prime approaches 1/ln(x). For a given number, n, the likelihood that n is prime would be 1/ln(n+1). Obviously, since one cannot have fractional sides on one's dice, the simulated dice collector opts to use a die with a number of faces equivalent to the ceiling of the natural log. Therefore, n is "probably" prime if, upon rolling a d*, where * = ceil(1/ln(n+1)), the result is a 1. Rigorous tests have not yet been performed to determine the algorithms accuracy, but, when approached for comment, Poussin and Hadamard said the work "seems to check out."

*modified to 1 by the now-famous "Donovan Revision".
*modified to 2 by the now-famous "Banner  Revision".
