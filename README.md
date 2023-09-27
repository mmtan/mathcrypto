# Mathematics Foundation of Cryptography
Course [website](https://mmtan.github.io/mathcrypto/) for Math Foundation of Cryptography

**These documents are not to be sold, published, or distributed without the author's consent.**

---
Instructor:  Dr. Ming Ming Tan

Email:  mtan@augusta.edu

Course Description:
In this course, students will learn about basic number theory and abstract algebra necessary to understand the definitional details of modern number-theoretic encryption schemes. All of the mathematical developments in this course are directly motivated by cryptographic applications.

Suggested Reference Books:
- **Textbook** [An Introduction to Mathematical Cryptography by Jeffrey Hoffstein, Jill Pipher, Joseph H. Silverman] (https://www.math.brown.edu/johsilve/MathCryptoHome.html)
- [Cryptography: An Introduction (3rd Edition) by Nigel Smart](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwitr7vL9a78AhVltjEKHbdQAhYQFnoECBEQAQ&url=https%3A%2F%2Fwww.cs.umd.edu%2F~waa%2F414-F11%2FIntroToCrypto.pdf&usg=AOvVaw2p0Q3HMItj7KaorAn67GJL)
- Introduction to Modern Cryptography by Jonathan Katz and Yehuda Lindell

Syllabus: [spring 2023](/syllabus_spring_2023.md)

course website: https://mmtan.github.io/mathcrypto/

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
 * Notes: [Homework 5 Disccusion](/homework5discussion.pdf) 
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
 * Notes: [Homework 6 Disccusion](/homework6discussion.pdf)

Wednesday (03/01/23): Midterm Q&A
 * Notes: [Midterm Q&A](/midtermQA.pdf)

Monday/Wednesday (03/06/23, 03/09/23): Midterm and Midterm discussion
* Notes: [Midterm Discussion](/midterm_discussion.pdf)
* Content:
  * Euler Formula
  * $Z_{pq}^*$ where $p$ and $q$ are odd primes, can't be cyclic. 
  * Integers which are squares can't be a generator. 

Monday, Wednesday (03/13/23, 03/16/23): RSA
* References : Textbook Section 3.2
* Notes: [Lecture 10](/lec10.pdf)
* Homework: [Homework 7](/homework7.pdf)
* Content:
  * An overview of RSA cryptosystem. 
  * If factoring of integers is easy, then RSA is insecure. The reverse is not known. 
  * RSA in practice: 
    * Using Euler formula for encryption and decryption 
    * Using CHR for encryption and decryption. 
    * Selecting the encryption and decryption exponenet. 
      * small decryption exponent leads to brute force attack. 
      * small encryption eponent wil small message size leads to attack via solving $e$-th root of the ciphtertext over integers, without the modulo $N$. 
    * Textbook/plain RSA vs Padded RSA. 
      * Plain RSA is deterministic. This raises security concern. For example, if adversary just need to know if a message sent to Alice is $m$, he/she just need to compare the ciphertext intercepted with the ciphertext $m^e \bmod{N}$ where $(N,e)$ are public key of Alice. 
      * Padded RSA embed messages in random string before encryption. 

Monday (03/20/23): RSA
* References : Textbook Section 3.2
* Notes: [Homework 7 Discussion](/homework7discussion.pdf), [Working Example for Question 5](https://colab.research.google.com/drive/1xU_cEju6sAPyilRHolAWRcFUTkpU397S?usp=sharing)
* Content:
  * Explore the condition where $gcd(e,p-1)$ is not 1 to the solution to $x^{e}\equiv c \bmod{p}$: either the congruence has no solution or has more than one solution (in particular, $gcd(e,p-1)$ distinct solutions). 
  * Informally, we look at the notion of quadratic residues modulo odd prime $p$. The congruence $x^2 \equiv c \bmod{p}$ has no solution when $c$ is not a quadratic residue modulo $p$ and it has exactly $2$ solutions when $c$ is a quadratic residue modulo $p$. 
  * This means that the set of quadratic residue modulo $p$ has $\frac{p-1}{2}$ elements. 
  * An example of "misuse" of RSA: Use the same modulus N to send the same message. 
  * Explore the following variant of RSA: Double encryption RSA and Multiprime RSA
  * Complexity theoretic reductions from one problem to another:  
     *  RSA problem is no harder than Factoring. The reverse is not known. 
     *  Diffie-Hellman is no harder than Discrete Logarithm. The reverse is true for some groups. 
     *  (Next week) SquareRoot is no harder than Factoring. Factoring is no harder than SquareRoot. Hence, the Factoring and SquareRoot problems are polynomial-time equivalent. 

Wednesday (03/22/23): Quadratic Residues mod P
* References : Textbook Section 3.9
* Notes: [Lecture 11a](/lec11a.pdf)
* Homework: [Homework 8](/homework8.pdf)
* Content:
  * The definitions of quadratic residue (QR) and quadratic non-residue (QNR).
  * The set of quadratic residues form a subgroup of an abelian group. 
  * Quadratic residues modulo $p$ where $p$ is odd prime:
    *  Every quadratic residue mod $p$ has exactly two square roots.
    *  The set of quadratic residues $QR_p$ has the same size as the set of quadratic non-residues $QNR_p$. 
    *  An element $x$ is a quadratic residue modulo $p$ if and only if $x^{\frac{p-1}{2}} = 1 \bmod{p}$. 
    *  Define $J_p(x)$ to be 1 if $x$ is QR and -1 if $x$ is QNR. 
    *  We have $J_p(x) = x^{\frac{p-1}{2}}$. 
    *  $J_p$ is mulitplicative: $J_p(xy) = J_p(x)J_p(y)$. 
    *  Product of two quadratic non-residues is a quadratic residue. Product of two quadratic residues is a quadratic residue. Product of a quadratic residue and a quadratic non-residue is a quadratic non-residue. 
    *  Algorithm to find if $x$ is a quadratic residue mod $p$. 
    *  Algorithm to find if square root of a quadratic residue $x$ mod $p$: 
      - when p is congruent 3 mod 4: the square roots are $x^{\frac{p+1}{4}}, -x^{\frac{p+1}{4}}$. 
      - when p is congruent 1 mod 4: there is no known deterministic polynomial algorithm to find the square roots. 

Monday (03/27/23): Quadratic Residues mod N
* References : Textbook Section 3.9
* Notes: [Lecture 11b](/lec11b.pdf)
* Content:
  * Quadratic residues modulo $N$ where $N = pq$ for $p$ and $q$ are distinct primes.
    *  Every quadratic residue mod $N$ has exactly four square roots.
    *  The set of quadratic residues $QR_N$ is 1/4 of the size of $Z_N^*$. 
    *  An element $x$ is a quadratic residue modulo $N$ if and only if $x_p$ is a quadratic residue modulo $p$ and $x_q$ is a quadratic residue modulo $q$. ($x_p = x \bmod{p}$ and $x_q = x \bmod{q}$). 
    *  Algorithm to find if $x$ is a quadratic residue mod $N$. 
    *  Algorithm to find if square roots of a quadratic residue $x$ mod $N$: 
      - compute square roots of $x_p$ and square roots of $x_q$. 
      - There are two square roots of $x_p$, say $a_1, a_2$, two square roots of $x_q$, say $b_1, b_2$. 
      - The four square roots of $x$ is $(a_1,b_1), (a_2, b_1), (a_1, b_2), (a_2, b_2)$. These square roots are in $Z_p^* \times Z_q^*$. 
      - Use Chinese remainder theorem to compute the value of $x_i \in Z_N^*$ such that $x_i = a_i \bmod{p}$ and $x_i = b_i \bmod{q}$ for $i=1,2$. 
    * If factoring $N$ is easy, then it is easy to compute square roots modulo $N$. 
    * If computing square root modulo $N$ is easy, then it is easy to factor $N$.  
    
Wednesday (03/29/23): Rabin Encryption
* References : Textbook Section 3.10
* Notes: [Lecture 12](/lec12.pdf)
* Homework: [Homework 9](/homework9.pdf)
* Content:
  * Rabin Encryption. 
  * Rabin vs RSA. 
    * Encryption is faster in Rabin. 
    * Hardness assumption of Rabin is guaranteed with the hardness of factoring integer. 
    * On the other hand, if factoring is hard, it doesn't mean that RSA problem is hard. 
    * There are four square roots. Hence, extra information is required to find the original message. 
    * Just like RSA, Rabin is deterministic. Hence, an adversary that just need to distinguish two different messages can just compare the ciphertexts.
  * An integer $N$ is called a Blum integer when $N = pq$ where $p \equiv q \equiv 3 \bmod{4}$.  
  * Recall that it is easy to compute the square roots of $x$ modulo $N$ if $N$ is a Blum integer because it is easy to compute a square root of $x$ mod $p$ when $p \equiv 3 \bmod{4}$. 
  * Let $N$ be an Blum integer. Then exactly one of the four square roots of a quadratic residue is a quadratic residue. 
  * In other words, the function $f: QR_N -> QR_N$ where $f(x) = x^2$ is a one to one and onto mapping.
  * Application: Let $N$ be a Blum integer. If plaintext $m \in QR_N$, then one can recover plaintext from the ciphertext in Rabin encryption scheme
 by checking which of the four square roots is a quadratic residue.
 * However, note that if the plaintext $m$ is not a quadratic residues, then Rabin encryption scheme still gives four potential plaintexts even when $N$ is a Blum integer.
 * Other methods for ensuring one to one mapping between plaintext and ciphertext of Rabin: 
   *  Pad messages with $l$ bits of 1's.
   *  Ciphertext is $(c, J_N(m), half)$ where $c = m^2 \bmod{N}$, $J_N(m) = J_p(m)J_q(m)$ and half is 1 if $m<\frac{N}{2}$, 0 otherwise. 
 * Elgamal Encryption is a probabilistic public key cryptostem. The same message can be encrypted to two different ciphertexts. 
 * Elgamal gives 2 to 1 message expansion. That is two times the bits are required to represent the ciphertext than plaintext.
 * If DLP is easy, then we can break Elgamal. 
 * If DHP is easy, then we can break Elgamal. 
  
    
Monday, Wednesday (04/10/23, 04/12/23): Homework 9 Discussion and Digital Signature Scheme
* References : Textbook Section 4.2, 4.3
* Homework: [Homework 9 Discussion](/homework9discussion.pdf), [Working Example for Question 1](https://colab.research.google.com/drive/12V1vrB62BXeFLzj_VQS9cTf6mw_kicIK?usp=sharing)
* Homework: [Homework 10](/homework10.pdf), [working example for Question 3](https://colab.research.google.com/drive/1XQJqK6GZl8C_3IVle-mnKEvKAOaZOKo9?usp=sharing)
* Notes: [Lecture 13](/lec13.pdf)
* Content:
  * Man in the middle attack of Diffie-Hellman Exchange Scheme
  * Digital Signature Scheme (Oversimplified version)

Monday (04/17/23): 
* References : Textbook Section 5.4
* Notes: [Lecture 13](/lec13.pdf)
* Content:
  * Cryptographic hash function (Oversimplified version)
     * Properties: One way, collison resistance
  * Birthday Paradox
     * It is harder to construct a collision resistance hash function compared to a one way hash function.

Wednesday (04/19/23): 
* References : Textbook Section 6.5
* Homework: [Homework 11](/homework11.pdf), [working example for Question 3](https://colab.research.google.com/drive/1w6r4hEjx8_3w6HkZ11ugKeFVAX-6pnoM?usp=sharing)
* Notes: [Lecture 14](/lec14.pdf)
* Content: 
  * Pollard rho's collision algorithm to solve discrete logarithm problem 
  * Pollard rho's collison algorithm to factor $N = pq$ where $p$, $q$ are primes. 

Monday (04/24/23): 
* References : Textbook Section 2.10
* Notes: [Lecture 15](/lec15.pdf)
* Content: 
  * Ring and Field
  * Polynomial Ring
  * Finite Field
    * There exists finite field of prime power order. 
    * Every finite field is of prime power order. 
    * All finite fields of the same order are isomorphic. 
  * Construction of finite field of order $p^d$ by taking the set of polynomials, mod a prime p and mod an irreducible polynomial of degree $d$. 
  * If F is a finite field, $F\setminus \{0\}$ is cyclic multiplicative group. 

Wednesday (04/26/23): 
* References : Textbook Section 8.4
* Homework: [Homework 12](/homework12.pdf)
* Notes: [Lecture 16](/lec16.pdf)
* Content: 
  * Lagrange Interpolation 
  * Shamir secret sharing scheme. 
  
Monday (05/01/23): 
* Homework: [Homework 12 discussion](/homework12solution.pdf)
* Final Exam: [Final Exam](/finalexam.pdf)
  
 
 
