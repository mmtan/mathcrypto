# Mathematics Foundation of Cryptography
Course website for Math Foundation of Cryptography

---
Instructor:  Dr. Ming Ming Tan

Email:  mtan@augusta.edu

Course Description:
In this course, students will learn about basic number theory and abstract algebra necessary to understand the definitional details of modern number-theoretic encryption schemes. All of the mathematical developments in this course are directly motivated by cryptographic applications.

Suggested Reference Books:
- **Textbook** [An Introduction to Mathematical Cryptography by Jeffrey Hoffstein, Jill Pipher, Joseph H. Silverman] (https://www.math.brown.edu/johsilve/MathCryptoHome.html)
- [Cryptography: An Introduction (3rd Edition) by Nigel Smart](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwitr7vL9a78AhVltjEKHbdQAhYQFnoECBEQAQ&url=https%3A%2F%2Fwww.cs.umd.edu%2F~waa%2F414-F11%2FIntroToCrypto.pdf&usg=AOvVaw2p0Q3HMItj7KaorAn67GJL)
- Introduction to Modern Cryptography by Jonathan Katz and Yehuda Lindell
- An Introduction to Mathematical Cryptography  by Jeffrey Hoffstein, Jill Pipher, Joseph H. Silverman

Syllabus: [spring 2023](/syllabus_spring_2023.md)

---

## Schedule and references
Monday (01/09/23): Introduction to classical ciphers
 * References : Textbook Section 1.1, 1.2, 1.3, 1.7.1, 2.5
 * Notes: [Lecture 1](/lec1.pdf)
 * Problem sets: NA
 * Content: shift cipher, the concept of divides and remainder, modular arithmetic, set of remainder modulo n
 
Wednesday (01/09/23): Introduction to group
 * References : Textbook Section 1.1, 1.2, 1.3, 1.7.1, 2.5
 * Notes: [Lecture 2](/lec2.pdf)
 * Problem sets: [Homework 1](/homework1.pdf)
 * Content: group, closure, identity element, inverse element, associativity, finite vs infinite group, abelian vs non-abelian group, order of group, operation table, direct product, isomorphism.
 
Monday (01/23/23): Discussion on Homework 1
* Content of discussion:
  * Given a group G, the identity of G is unique. For all g in G, the inverse of g is unique too. 
  * If f is isomorphism map between groups G and H, then f maps identity of G to the identity of H.
  * Suppose f is isomorphism map between groups G and H. If g_inverse is the inverse of g in G, then f(g_inverse) is the inverse of f(g) in H. 
  * $(Z_n, +)$ is a group
  * $(Z_n, .)$ is not a group because 0 is in $Z_n$ and 0 has no inverse. 0 can't be the identity because 0.a = 0 for all a in $Z_n$.
  * We observe that $(Z_n \text{without 0}, .)$ is not a group unless n is prime. 
  * We observe that $(Z_n^\*, .)$ a group where $Z_n^*$ is the set of all integers in $Z_n$ that has no common divisors with $n$. 
  * We observe that $(Z_{mn}, .)$ is isomorphic to $Z_m \times Z_n$ if and only if $gcd(m,n)=1$. 



