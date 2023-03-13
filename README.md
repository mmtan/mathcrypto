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
 
Wednesday (01/18/23): Introduction to group
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
  * We observe that $(Z_{mn}, +)$ is isomorphic to $Z_m \times Z_n$ (under addition) if and only if $gcd(m,n)=1$. 

Wednesday (01/25/23): Order of group element, cyclic group, and euler tortient function
 * References : Textbook Section 2.5
 * Notes: [Lecture 3](/lec3.pdf)
 * Problem sets: [Homework 2](/homework2.pdf)
 * Content:
   * order of group elements is finite if the group is finite
   * isomorphism preserves the order of group elements
   * Given a group element $g$ with order $d$. If $g^f$ is the identity then $f$ must be a multiple of $d$. 
   * Lagrange: The order of a group element is a divisor of the order of the group. 
   * Informal introduction to Chinese Remainder Theorem: The map $f$ from $Z_{mn}$ to $Z_m \times Z_n$ where $m$ and $n$ are coprime defined as follows: 
   $f(x) = (x \bmod m, x \bmod n)$ is a a bijective map. 
   * Euler tortient function $\phi(n)$ is the number of positive integer less than $n$ that is coprime to $n$. 

Monday (01/30/23): Chinese Remainder theorem and Discussion on Homework 2
 * References : Textbook Section 2.8
 * Notes: [Lecture 3](/lec3.pdf) (updated with the proofs for Chinese Remainder Theorem)
 * Homework Discussion: [Homework 2 Discussion](/homework2discussion.pdf)
 * Content:
   * Warm up: Prove that any element $g$ in a finite group $G$ satisfies $g^{\|G\|} = e$. That is, any group element, operates on itself $\|G\|$ times will lead to identity.
   * Formal proofs to Chinese Remainder Theorem. 
   * Revise the definitions of a function being one-to-one/injective and onto/surjective.
   * If a function $f$ maps a set $X$ to $Y$ such that $f$ is one-to-one and that $\|X\|$ equals $\|Y\|$, then $f$ is onto. 
   * Euler tortient function is multiplicative: $\phi(pq) = \phi(p)\phi(q)$ when $p$ and $q$ are coprimes. This can be seen as a consequence of Chinese Remainder Theorem. 
   * The formula for Euler tortient function for arbitrary integer $n$. 


Wednesday (02/01/23): Euclidean algorithm, prime factorization, multiplicative inverse
 * References : Textbook Section 1.2, 1.4
 * Notes: [Lecture 4](/lec4.pdf)
 * Homework: [Homework 3](/homework3.pdf)
 * Content:
   * Greatest common divisors
   * Euclidean algorithm 
   * Unique prime factorizations
   * Mulitplicative inverse

Monday (02/06/23): Discussion on Homework 3, Analysis of the running time on Euclidean algorithm
 * References : Textbook Section 1.2, 1.4
 * Notes: [Lecture 5](/lec5.pdf)
 * Homework discussion: [Homework 3 partial solution](/homework3discussion.pdf)
 * Content:
   * Running time of algorithm: How long it takes to solve the problem in terms of size of the input. We measure the size of the input by its number of bits. 
   * Notion of linear, quadratic, polynomial and exponential algorithm. 
   * Hardness of a problem based on running time. 
   * Prove that Euclidean algorithm for finding gcd(a,b) where $a \geq b$ has running time of $O(\log b)$ which is linear in the number of bits of the input $b$.
   
Wednesday (02/08/23): Efficient algorithm for Modular Exponentiation, The Discrete Logarithm Problem (DLP), Baby-step-Giant-step algorithm to solve DLP
 * References : Textbook Section 1.3.2
 * Notes: [Lecture 6](/lec6.pdf)
 * Homework: [Homework 4](/homework4.pdf)
 * Content:
   * Modular exponentiation using square and multiply method. 
   * Introduce the Discrete Logarithm Problem (DLP). Given $g, h$ in $G$, solve for $x$ such that $g^x = h$.
   * Hardness of DLP depends on the group strucutre. In particular, in $Z_n$ with + operation, DLP is easy. In $Z_n^\*$ with $\*$ operation, DLP is known to be a hard problem. 
   * Trivial running and space complexity using brute-force method to solve DLP: O(N) steps and O(1) space where N is the order of $g$. 
   * Running and space complexity using Baby-step-Giant-step (trading time with space): $O(\sqrt{N}\log N)$ steps and $O(\sqrt{N})$ space. 
   
Monday (02/13/23): Diffie-Hellman key exchange protocol, Fermat little theorem, Pohlig-Hellman algorithm
 * References : Textbook Section 2.3, Theorem 1.24, Section 2.9
 * Notes: [Lecture 7](/lec7.pdf) 
 * Content:
   * Diffie-Hellman Key Exchange Protocol
   * Fermat's little theorem: Let $p$ be prime. Then $a^{p-1} = 1 \bmod{p}$ for all integer $a$ coprime to $p$.
   * Properties of $ord(g)$ when $g \in Z_p^*$. 
   * Pohlig-Hellman algorithm: Reduces the problem of solving Discrete Logarithm Problem of order g being aribitray order to order g being prime power. 
   * Pohlig-Hellman algorithm implies that the discrete logarithm problem is easy to solve when the order of $g$ is a product of small prime powers. 
   * Diffie-Hellman key exchange protocol requires safe prime $p$ (such that $p-1 = 2q$ where $q$ is a prime). 
  
   
Wednesday (02/15/23): Primality Testing
 * References : Textbook Section 3.4
 * Notes: [Lecture 8](/lec8.pdf) 
 * Homework: [Homework 5](/homework5.pdf)
 * Content:
   * Primality testing: Checking whether an integer is a prime. This problm is easy to solve. There exits a polynomial deterministic algorithm. 
   * However, in practice, we use probabilistic algorithm that is more efficient and with low error rate. 
    * Fermat's little test 
    * Miller-Rabin's test 

Monday (02/20/23): Prime distribution
 * References : Textbook Section 3.4
 * Notes: [Lecture 9](/lec9.pdf) 
 * Content:
   * Analysis of Miller-Rabin's test
   * Distribution of primes
   * Use Miller-Rabin's test to generate large prime

Wednesday (02/22/23): Homework 5 discussion 
 * References : Textbook Section 3.4
 * Notes: [homeework5disccusion](/homework5discussion.pdf) 
 * Homework: [Homework 6](/homework6.pdf)
 * Content:
  * Proof of Pohlig-Hellman algorithm
  * Checking if an element $g$ is a generator a a group of order $n$ without having to generate $g^i$ for all $i$. Instead check if $g^{n/p} \neq 1$ for each prime divisor $p$ of $n$.
  * Recap: Fermat's little theorem: If $p$ is prime, then 
       * for all integers $a$ coprime to $p$, we have $a^{p-1} \equiv 1 \bmod{p}$. 
       * for all integers $a$, we have $a^p \equiv a \bmod{p}$. 
  * Recap: A Carmichael number $n$ is a composite integer such that $a^n \equiv a \bmod{n}$ for all $a$. Hence, Fermat little test on input $n$ will output that $n$ is probably prime but $n$ is not a prime. 
  * Self-practice exercises: Prove that if $n$ is a Carmichael number then $n$ is a product of disctinct primes. 
  

Monday (02/27/23): Homework 6 discussion 
 * References : Textbook Section 3.4
 * Notes: [homeework6disccusion](/homework6discussion.pdf)

Wednesday (03/01/23): Midterm Q&A
 * Notes: [Midterm Q&A](/midtermQA.pdf)

Monday/Wednesday (03/06/23, 03/09/23): Midterm and Midterm discussion
* Notes: [Midterm discussion](/midterm_discussion.pdf)
* Content:
 * Euler Formula
 * $Z_{pq}^*$ where $p$ and $q$ are odd primes, can't be cyclic. 
 * Integers which are squares can't be a generator. 

Monday, Wednesday (03/13/23, 03/16/23): RSA
* References : Textbook Section 3.2
* Notes: [Lecture 10](/lec10.pdf)
* Homework: [homeework7](/homework7.pdf)
* Content:
 * An overview of RSA cryptosystem. 
 * If factoring of integers is easy, then RSA is insecure. The reverse is not known. 
 * RSA in practice: 
  * Using CHR for encryption and decryption. 
  * Selecting the encryption and decryption exponenet. 
  * Textbook/plain RSA vs Padded RSA. 

