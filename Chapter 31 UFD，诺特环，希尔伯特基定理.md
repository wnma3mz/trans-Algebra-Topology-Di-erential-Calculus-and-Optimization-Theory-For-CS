第三十一章

# UFD’s, Noetherian Rings, Hilbert’s Basis Theorem  UFD，诺特环，希尔伯特基定理

## 31.1                 Unique Factorization Domains (Factorial Rings)  31.1唯一因子分解域（因子环）

We saw in Section 29.5 that if K is a field, then every nonnull polynomial in K[X] can be factored as a product of irreducible factors, and that such a factorization is essentially unique. The same property holds for the ring K[X1,...,Xn] where n ≥ 2, but a different proof is needed.
 我们在第29.5节中看到，如果k是一个字段，那么k[x]中的每个非空多项式都可以被分解为不可约因子的乘积，并且这种分解本质上是唯一的。同样的性质适用于环k[x1，…，xn]，其中n≥2，但需要不同的证明。

The reason why unique factorization holds for K[X1,...,Xn] is that if A is an integral domain for which unique factorization holds in some suitable sense, then the property of unique factorization lifts to the polynomial ring A[X]. Such rings are called factorial rings, or unique factorization domains. The first step if to define the notion of irreducible element in an integral domain, and then to define a factorial ring. If will turn out that in a factorial ring, any nonnull element a is irreducible (or prime) iff the principal ideal (a) is a prime ideal.
 唯一因式分解对k[x1，…，xn]成立的原因是，如果a是一个积分域，其中唯一因式分解在某种意义上成立，那么唯一因式分解的性质提升到多项式环a[x]。这样的环称为阶乘环，或唯一的阶乘域。第一步是在积分域中定义不可约元素的概念，然后定义阶乘环。如果在阶乘环中，任何非空元素a都是不可约的（或素数），只要主理想（a）是素数理想。

Recall that given a ring A, a unit is any invertible element (w.r.t. multiplication). The set of units of A is denoted by A∗. It is a multiplicative subgroup of A, with identity 1. Also, given a,b ∈ A, recall that a divides b if b = ac for some c ∈ A; equivalently, a divides b iff (b) ⊆ (a). Any nonzero a ∈ A is divisible by any unit u, since a = u(u−1a). The relation “a divides b,” often denoted by a | b, is reflexive and transitive, and thus, a preorder on A−{0}.
 回想一下，给定一个环A，一个单位是任何可逆元素（w.r.t.乘法）。a的一组单位用表示。它是a的乘法子群，具有标识1。另外，在给定a，b∈a的情况下，如果b=a c，则a对b进行除b，相当于a对b iff（b）（a）进行除b。任何非零a∈a可被任何单位u整除，因为a=u（u−1a）。关系“a divides b”，通常用a_b表示，是反身的和传递的，因此是a−0_的预订单。

Definition 31.1. Let A be an integral domain. Some element a ∈ A is irreducible if a = 06 , a /∈ A∗ (a is not a unit), and whenever a = bc, then either b or c is a unit (where b,c ∈ A).
 定义31.1.设A为积分域。如果a=06，a/∈a（a不是一个单位），某个元素a∈a是不可约的，当a=b c时，b或c是一个单位（其中b，c∈a）。

Equivalently, a ∈ A is reducible if a = 0, or a ∈ A∗ (a is a unit), or a = bc where b,c /∈ A∗
 等价地，如果a=0，或a∈a（a是一个单位）或a=b c，其中b，c/∈a a是可约的。

(a,b are both noninvertible) and b,c = 0.6
 （a，b都是不可逆的）和b，c=0.6

Observe that if a ∈ A is irreducible and u ∈ A is a unit, then ua is also irreducible. Generally, if a ∈ A, a = 06 , and u is a unit, then a and ua are said to be associated. This is the equivalence relation on nonnull elements of A induced by the divisibility preorder.
 如果a∈a是不可约的，而u∈a是一个单位，那么ua也是不可约的。一般来说，如果a∈a，a=06，u是一个单位，那么a和ua是相关联的。这是由可除性预序诱导的非空元素的等价关系。

1019
 一千零一十九


 

The following simple proposition gives a sufficient condition for an element a ∈ A to be irreducible.
 下面的简单命题给出了元素a∈a不可约的充分条件。

Proposition 31.1. Let A be an integral domain. For any a ∈ A with a = 06 , if the principal ideal (a) is a prime ideal, then a is irreducible.
 提案31.1.设A为积分域。对于任意a∈a且a=06，如果主理想（a）是素理想，则a是不可约的。

Proof. If (a) is prime, then (a) =6 A and a is not a unit. Assume that a = bc. Then, bc ∈ (a), and since (a) is prime, either b ∈ (a) or c ∈ (a). Consider the case where b ∈ (a), the other case being similar. Then, b = ax for some x ∈ A. As a consequence,
 证据。如果（a）是素数，那么（a）=6a，a不是一个单位。假设a=bc。那么，b c∈（a），由于（a）是素数，b∈（a）或c∈（a）。考虑b∈（a）的情况，另一个情况相似。那么，对于某些x∈a，b=ax。因此，

a = bc = axc,
 a=bc=axc，

​        and since A is an integral domain and a = 06 , we get
 因为a是一个积分域，a=06，我们得到

1 = xc,
 1=xc，

​         which proves that c = x−1 is a unit.                                                                                                
 这证明c=x−1是一个单位。

It should be noted that the converse of Proposition 31.1 is generally false. However, it holds for factorial rings, defined next.
 应当指出的是，31.1号提案的反面通常是错误的。然而，它适用于阶乘环，定义如下。

Definition 31.2. A factorial ring or unique factorization domain (UFD) (or unique factorization ring) is an integral domain A such that the following two properties hold:
 定义31.2.因式分解环或唯一因式分解域（UFD）（或唯一因式分解环）是一个积分域A，其具有以下两个性质：

(1)    For every nonnull a ∈ A, if a /∈ A∗ (a is not a unit), then a can be factored as a product
 对于每一个非空a∈a，如果a/∈a（a不是一个单位），则a可以被分解为一个积。

a = a1 ···am
 A=A1···AM

where each ai ∈ A is irreducible (m ≥ 1).
 其中，每个ai∈a都是不可约的（m≥1）。

(2)    For every nonnull a ∈ A, if a /∈ A∗ (a is not a unit) and if
 对于每一个非空a∈a，如果a/∈a（a不是一个单位），并且如果

a = a1 ···am = b1 ···bn
 a=a1···am=b1··bn

where ai ∈ A and bj ∈ A are irreducible, then m = n and there is a permutation σ of {1,...,m} and some units u1,...,um ∈ A∗ such that ai = uibσ(i) for all i, 1 ≤ i ≤ m.
 其中，a i∈a和bj∈a是不可约的，那么m=n，并且有一个1，…，m的置换σ和一些单位u1，…，um∈a，这样ai=uibσ（i）对于所有i，1≤i≤m。

Example 31.1. The ring Z of integers if a typical example of a UFD. Given a field K, the polynomial ring K[X] is a UFD. More generally, we will show later that every PID is a UFD (see Theorem 31.12). Thus, in particular, Z[X] is a UFD. However, we leave as an exercise to prove that the ideal (2X,X2) generated by 2X and X2 is not principal, and thus, Z[X] is not a PID.
 例31.1。整数的环Z，如果是一个典型的UFD例子。给定一个字段k，多项式环k[x]是一个ufd。更一般地说，我们稍后将展示每个PID都是一个UFD（见定理31.12）。因此，特别是z[x]是一个UFD。然而，我们作为一个练习来证明由2x和x2生成的理想（2x，x2）不是主体，因此z[x]不是PID。

First, we prove that condition (2) in Definition 31.2 is equivalent to the usual “Euclidean” condition.
 首先，我们证明了定义31.2中的条件（2）等价于通常的“欧几里德”条件。

 There are integral domains that are not UFD’s. For example, the subring√   ∈          Z[√−5] of C
 存在非UFD的积分域，例如c的子环√∈z[√−5]

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

consisting of the complex numbers of the form a + bi 5 where a,b Z is not a UFD. Indeed, we have
 由a+bi 5形式的复数组成，其中a、b、z不是ufd。事实上，我们有

9 = 3 · 3 = (2 + i√5)(2 − i√5),
 9=3·3=（2+i√5）（2−i√5）

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

and it can be shown that 3, 2+i√5, and 2√−−i√5 are irreducible, and that the units are ±1. The uniqueness condition (2) fails and Z[ 5] is not a UFD.
 可以看出，3、2+i√5和2√−−i√5是不可约的，单位为±1。唯一性条件（2）失败，Z[5]不是UFD。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image003.gif)

Remark: For d ∈ Z with d < 0, it is known that the ring of integers of Q(√d) is a UFD iff d is one of the nine primes, d = −1,−2,−3,−7,−11,−19,−43,−67 and −163. This is a hard theorem that was conjectured by Gauss but not proved until 1966, independently by Stark and Baker. Heegner had published a proof of this result in 1952 but there was some doubt about its validity. After finding his proof, Stark reexamined Heegner’s proof and concluded that it was essentially correct after all. In sharp contrast, when d is a positive integer, the
 备注：对于d∈z且d<0，已知q（√d）的整数环是一个ufd iff d是九个素数中的一个，d=−1、−2、−3、−7、−11、−19、−43、−67和−163。这是一个困难的定理，高斯猜想，但直到1966年才被证明，斯塔克和贝克独立。海格纳在1952年发表了这一结果的证明，但对其有效性存在一些怀疑。在找到证据后，斯塔克重新检查了希格纳的证据，并得出结论，这基本上是正确的。与此形成鲜明对比的是，当d是一个正整数时，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

problem of determining which of the rings of integers of Q(√d) are UFD’s, is still open. It
 确定q（√d）的整数环中哪一个是ufd的问题仍然是开放的。它

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

​       can also be shown that if√                  d < 0, then the ring Z[√d] is a UFD iff d = −1 or d = −2. If
 也可以证明，如果√d<0，则环Z[√d]是UFD iff d=−1或d=−2。如果

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

d ≡ 1(mod4), then Z[ d] is never a UFD. For more details about these remarkable results, see Stark [159] (Chapter 8).
 D 1（mod4），那么Z[D]永远不是UFD。有关这些显著结果的更多详细信息，请参阅Stark[159]（第8章）。

Proposition 31.2. Let A be an integral domain satisfying condition (1) in Definition 31.2. Then, condition (2) in Definition 31.2 is equivalent to the following condition:
 提案31.2.设A为满足定义31.2中条件（1）的积分域。那么，定义31.2中的条件（2）等于以下条件：

(20) If a ∈ A is irreducible and a divides the product bc, where b,c ∈ A and b,c = 06 , then either a divides b or a divides c.
 （20）如果a∈a是不可约的，a将积b c除，其中b，c∈a和b，c=06，则a将b除或a将c除。

​          Proof. First, assume that (2) holds. Let bc = ad, where d ∈ A, d = 06    . If b is a unit, then
 证据。首先，假设（2）成立。设bc=a d，其中d∈a，d=06。如果b是一个单位，那么

c = adb−1,
 C=adb−1，

and c is divisible by a. A similar argument applies to c. Thus, we may assume that b and c are not units. In view of (1), we can write
 C可以被A整除，类似的论点也适用于C，因此我们可以假设B和C不是单位。鉴于（1），我们可以写

​                                                     b = p1 ···pm    and    c = pm+1 ···qm+n,
 b=p1···pm，c=pm+1··qm+n，

where pi ∈ A is irreducible. Since bc = ad, a is irreducible, and b,c are not units, d cannot be a unit. In view of (1), we can write
 式中，π∈a是不可约的。因为b c=a d，a是不可约的，b，c不是单位，d不能是单位。鉴于（1），我们可以写

d = q1 ···qr,
 d=q1···qr，

where qi ∈ A is irreducible. Thus,
 其中qi∈a是不可约的。因此，

p1 ···pmpm+1 ···pm+n = aq1 ···qr,
 p1···pm pm+1···pm+n=aq1···qr，

where all the factors involved are irreducible. By (2), we must have
 所有涉及的因素都是不可约的。到（2）时，我们必须

a = ui0pi0
 A=ui0pi0

for some unit ui0 ∈ A and some index i0, 1 ≤ i0 ≤ m + n. As a consequence, if 1 ≤ i0 ≤ m, then a divides b, and if m + 1 ≤ i0 ≤ m + n, then a divides c. This proves that (20) holds. Let us now assume that (20) holds. Assume that
 对于某些单位ui0∈a和一些指数i0，1≤i0≤m+n，因此，如果1≤i0≤m，则a除以b，如果m+1≤i0≤m+n，则a除以c。这证明（20）成立。现在让我们假设（20）成立。假设

a = a1 ···am = b1 ···bn,
 a=a1···am=b1··bn，

where ai ∈ A and bj ∈ A are irreducible. Without loss of generality, we may assume that m ≤ n. We proceed by induction on m. If m = 1,
 其中，ai∈a和bj∈a是不可约的。在不失去一般性的情况下，我们可以假定m≤n。我们通过对m的归纳来进行。如果m=1，

a1 = b1 ···bn,
 a1=b1···bn，

and since a1 is irreducible, u = b1 ···bi−1bi+1bn must be a unit for some i, 1 ≤ i ≤ n. Thus, (2) holds with n = 1 and a1 = biu. Assume that m > 1 and that the induction hypothesis holds for m − 1. Since a1a2 ···am = b1 ···bn,
 由于a1是不可约的，u=b1·············································假设m>1，且诱导假设适用于m-1。由于a1a2···am=b1··bn，

a1 divides b1 ···bn, and in view of (20), a1 divides some bj. Since a1 and bj are irreducible, we must have bj = uja1, where uj ∈ A is a unit. Since A is an integral domain,
 A1划分b1···bn，从（20）来看，A1划分了一些bj。因为a1和bj是不可约的，我们必须有bj=uja1，其中uj∈a是一个单位。因为A是一个积分域，

a1a2 ···am = b1 ···bj−1uja1bj+1 ···bn
 a1a2·····am=b1····bj········1uja1bj+1···bn

implies that
 意味着

a2 ···am = (ujb1)···bj−1bj+1 ···bn,
 a2······am=（ujb1）····bj····1bj+1···bn，

and by the induction hypothesis, m − 1 = n − 1 and ai = vibτ(i) for some units vi ∈ A and some bijection τ between {2,...,m} and {1,...,j −1,j +1,...,m}. However, the bijection τ extends to a permutation σ of {1,...,m} by letting σ(1) = j, and the result holds by letting v1 = u−j 1.    
 根据诱导假设，对于某些单元vi∈a和一些在2，…，m和1，…，j−1，j+1，…，m之间的双射τ，m−1=n−1和a i=vibτ（i）。然而，双射τ通过让σ（1）=j扩展到1，…，m的置换σ，结果通过让v1=u−j 1保持。

As a corollary of Proposition 31.2. we get the converse of Proposition 31.1.
 作为命题31.2的推论。我们得到了31.1号命题的逆命题。

Proposition 31.3. Let A be a factorial ring. For any a ∈ A with a = 06      , the principal ideal (a) is a prime ideal iff a is irreducible.
 提案31.3.设A为阶乘环。对于任意a∈a，当a=06时，主理想（a）是素理想，当a是不可约的。

Proof. In view of Proposition 31.1, we just have to prove that if a ∈ A is irreducible, then the principal ideal (a) is a prime ideal. Indeed, if bc ∈ (a), then a divides bc, and by Proposition 31.2, property (20) implies that either a divides b or a divides c, that is, either b ∈ (a) or c ∈ (a), which means that (a) is prime. 
 证据。对于31.1号命题，我们只需要证明，如果a∈a是不可约的，那么主理想（a）就是素理想。实际上，如果b c∈（a），那么a除以bc，并且根据命题31.2，性质（20）意味着a除以b或a除以c，即b∈（a）或c∈（a），这意味着（a）是素数。

Because Proposition 31.3 holds, in a UFD, an irreducible element is often called a prime.
 因为命题31.3认为，在UFD中，不可约元素通常被称为素数。

In a UFD A, every nonzero element a ∈ A that is not a unit can be expressed as a product a = a1 ···an of irreducible elements ai, and by property (2), the number n of factors only depends on a, that is, it is the same for all factorizations into irreducible factors. We agree that this number is 0 for a unit.
 在UFD A中，每一个非零元素a∈a都可以表示为不可约元素ai的乘积a=a1··············································我们同意这个数字对于一个单位是0。

Remark: If A is a UFD, we can state the factorization properties so that they also applies to units:
 备注：如果a是ufd，我们可以说明分解性质，以便它们也适用于单位：

(1) For every nonnull a ∈ A, a can be factored as a product
 （1）对于每一个非空a∈a，a都可以被分解为一个积。

a = ua1 ···am
 A=UA1···AM

where u ∈ A∗ (u is a unit) and each ai ∈ A is irreducible (m ≥ 0). (2) For every nonnull a ∈ A, if
 其中u∈a（u是一个单位），而每个ai∈a都是不可约的（m≥0）。（2）对于每一个非空a∈a，如果

a = ua1 ···am = vb1 ···bn
 A=UA1···AM=VB1···Bn

where u,v ∈ A∗ (u,v are units) and ai ∈ A and bj ∈ A are irreducible, then m = n, and if m = n = 0 then u = v, else if m ≥ 1, then there is a permutation σ of {1,...,m} and some units u1,...,um ∈ A∗ such that ai = uibσ(i) for all i, 1 ≤ i ≤ m.
 其中u，v∈a（u，v是单位），a i∈a和bj∈a是不可约的，则m=n，如果m=n=0，则u=v，否则，如果m≥1，则存在1，…，m的置换σ，并且一些单位u1，…，um∈a，这样ai=uibσ（i）对于所有i，1≤i≤m。

We are now ready to prove that if A is a UFD, then the polynomial ring A[X] is also a UFD.
 我们现在准备证明，如果a是一个ufd，那么多项式环a[x]也是一个ufd。

First, observe that the units of A[X] are just the units of A. The fact that nonnull and nonunit polynomials in A[X] factor as products of irreducible polynomials is easier to prove than uniqueness. We will show in the proof of Theorem 31.10 that we can proceed by induction on the pairs (m,n) where m is the degree of f(X) and n is either 0 if the coefficient fm of Xm in f(X) is a unit of n is fm is the product of n irreducible elements.
 首先，观察a[x]的单位只是a的单位。事实上，在a[x]因子中的非零和非单位多项式作为不可约多项式的乘积，比唯一性更容易证明。我们将在定理31.10的证明中证明，我们可以通过对（m，n）的归纳来进行，其中m是f（x）的度数，如果f（x）中xm的系数fm是n的单位，则n是n不可约元素的积，则n是0。

For the uniqueness of the factorization, by Proposition 31.2, it is enough to prove that condition (20) holds. This is a little more tricky. There are several proofs, but they all involve a pretty Lemma due to Gauss.
 对于因式分解的唯一性，由命题31.2，足以证明条件（20）成立。这有点棘手。有几种证明，但由于高斯的缘故，它们都涉及一个漂亮的引理。

First, note the following trivial fact. Given a ring A, for any a ∈ A, a = 06 , if a divides every coefficient of some nonnull polynomial f(X) ∈ A[X], then a divides f(X). If A is an integral domain, we get the following converse.
 首先，注意下面这个小事实。给定一个环a，对于任意a∈a，a=06，如果a除以某个非空多项式f（x）∈a[x]的每一个系数，则a除以f（x）。如果A是一个积分域，我们得到如下的逆。

Proposition 31.4. Let A be an integral domain. For any a ∈ A, a = 06 , if a divides a nonnull polynomial f(X) ∈ A[X], then a divides every coefficient of f(X).
 提案31.4.设A为积分域。对于任意a∈a，a=06，如果a除以非零多项式f（x）∈a[x]，则a除以f（x）的每一个系数。

Proof. Assume that f(X) = ag(X), for some g(X) ∈ A[X]. Since a = 06 and A is an integral ring, f(X) and g(X) have the same degree m, and since for every i (0 ≤ i ≤ m) the coefficient of Xi in f(X) is equal to the coefficient of Xi in ag(x), we have fi = agi, and whenever fi = 06 , we see that a divides fi.       
 证据。假设f（x）=a g（x），对于某些g（x）∈a[x]。由于a＝06和a是整环，f（x）和g（x）具有相同的度数m，并且因为对于每个i（0±i＝m），在f（x）中的Xi系数等于Ag（x）中的Xi系数，所以我们有Fi＝AGI，并且每当Fi＝06时，我们看到划分FI。

Lemma 31.5. (Gauss’s lemma) Let A be a UFD. For any a ∈ A, if a is irreducible and a divides the product f(X)g(X) of two polynomials f(X),g(X) ∈ A[X], then either a divides f(X) or a divides g(X).
 引理31.5。（高斯引理）让A成为UFD。对于任意a∈a，如果a是不可约的，a将两个多项式f（x），g（x）的积f（x）g（x）除，则a将f（x）除，或a将g（x）除。

Proof. Let f(X) = fmXm + ··· + fiXi + ··· + f0 and g(X) = gnXn + ··· + gjXj + ··· + g0. Assume that a divides neither f(X) nor g(X). By the (easy) converse of Proposition 31.4, there is some i (0 ≤ i ≤ m) such that a does not divide fi, and there is some j (0 ≤ j ≤ n) such that a does not divide gj. Pick i and j minimal such that a does not divide fi and a does not divide gj. The coefficient ci+j of Xi+j in f(X)g(X) is
 证据。设f（x）=fmxm+·····+fixi+····+f0和g（x）=gnxn+····+gjxj+····+g0。假设a既不除f（x）也不除g（x）。根据命题31.4的（简单）倒数，有一些i（0≤i≤m），这样a不除fi，有一些j（0≤j≤n），这样a不除gj。选择i和j最小值，这样a不划分fi，a不划分gj。f（x）g（x）中Xi+j的系数Ci+j

ci+j = f0gi+j + f1gi+j−1 + ··· + figj + ··· + fi+jg0
 ci+j=f0gi+j+f1gi+j−1+····+figj+···+fi+jg0

(letting fh = 0 if h > m and gk = 0 if k > n). From the choice of i and j, a cannot divide figj, since a being irreducible, by (20) of Proposition 31.2, a would divide fi or gj. However, by the choice of i and j, a divides every other nonnull term in the sum for ci+j, and since a is irreducible and divides f(X)g(X), by Proposition 31.4, a divides ci+j, which implies that a divides figj, a contradiction. Thus, either a divides f(X) or a divides g(X). 
 （h>m时fh=0，k>n时gk=0）。从i和j的选择来看，a不能将fi gj分开，因为a是不可约的，除以（20）31.2，a将把fi或gj分开。然而，通过i和j的选择，a将ci+j和中的其他非空项相除，由于a是不可约的，并将f（x）g（x）除以命题31.4，a将ci+j相除，这意味着a将figj相除，这是一个矛盾。因此，要么A除以F（x），要么A除以G（x）。

As a corollary, we get the following proposition.
 作为推论，我们得到以下命题。

Proposition 31.6. Let A be a UFD. For any a ∈ A, a = 06 , if a divides the product f(X)g(X) of two polynomials f(X),g(X) ∈ A[X] and f(X) is irreducible and of degree at least 1, then a divides g(X).
 提案31.6.让A成为UFD。对于任意a∈a，a=06，如果a将两个多项式f（x）的积f（x）g（x），g（x）∈a[x]和f（x）不可约且阶数至少为1，则a将g（x）除。

Proof. The Proposition is trivial is a is a unit. Otherwise, a = a1 ···am where ai ∈ A is irreducible. Using induction and applying Lemma 31.5, we conclude that a divides g(X). 
 证据。命题是平凡的是一个是一个单位。否则，a=a1·····am，其中ai∈a是不可约的。利用归纳法和引理31.5，我们得出A除以G（x）。

We now show that Lemma 31.5 also applies to the case where a is an irreducible polynomial. This requires a little excursion involving the fraction field F of A.
 我们现在证明引理31.5也适用于a是不可约多项式的情况。这需要对a的分数场f作一点偏移。

Remark: If A is a UFD, it is possible to prove the uniqueness condition (2) for A[X] directly without using the fraction field of A, see Malliavin [116], Chapter 3.
 备注：如果a是ufd，则可以直接证明[x]的唯一性条件（2），而不使用a的分数字段，见Malliavin[116]，第3章。

Given an integral domain A, we can construct a field F such that every element of F is of the form a/b, where a,b ∈ A, b = 06 , using essentially the method for constructing the field Q of rational numbers from the ring Z of integers.
 给定一个积分域A，我们可以构造一个域F，使F的每一个元素都是A/B的形式，其中A，B∈A，B=06，本质上是用整数环Z构造有理数的域Q的方法。

Proposition 31.7. Let A be an integral domain.
 提案31.7.设A为积分域。

*(1)*     There is a field F and an injective ring homomorphism i: A → F such that every element of F is of the form i(a)i(b)−1, where a,b ∈ A, b = 06 .
 有一个场f和一个内射环同态i:a→f，这样f的每一个元素都是形式i（a）i（b）−1，其中a，b∈a，b=06。

*(2)*     For every field K and every injective ring homomorphism h: A → K, there is a (unique) field homomorphism bh: F → K such that
 对于每个场k和每个内射环同态h:a→k，都有一个（唯一的）场同态bh:f→k，这样

bh(i(a)i(b)−1) = h(a)h(b)−1
 b h（i（a）i（b）−1）=h（a）h（b）−1

​                  for all a,b ∈ A, b = 06 .
 对于所有a，b∈a，b=06。

*(3)*     The field F in (1) is unique up to isomorphism.
 （1）中的F场在同构上是唯一的。

Proof. (1) Consider the binary relation ' on A × (A − {0}) defined as follows:
 证据。（1）考虑a×（a−0）上的二进制关系，定义如下：

​                                                             (a,b) ' (a0,b0)    iff   ab0 = a0b.
 （a，b）'（a0，b0）iff ab0=a0b.

It is easily seen that ' is an equivalence relation. Note that the fact that A is an integral domain is used to prove transitivity. The equivalence class of (a,b) is denoted by a/b. Clearly, (0,b) ' (0,1) for all b ∈ A, and we denote the class of (0,1) also by 0. The equivalence class a/1 of (a,1) is also denoted by a. We define addition and multiplication on A × (A − {0}) as follows:
 很容易看出，'是一个等价关系。注意，a是一个积分域的事实被用来证明传递性。（a，b）的等价类用a/b表示，显然，（0，b）'（0，1）对于所有b∈a，我们也用0表示（0，1）的等价类。（a，1）的等价类a/1也用a表示。我们在a×（a−0）上定义了加法和乘法，如下所示：

(a,b) + (a0,b0) = (ab0 + a0b,bb0), (a,b) · (a0,b0) = (aa0,bb0).
 （a，b）+（a0，b0）=（ab0+a0b，bb0），（a，b）·（a0，b0）=（aa0，bb0）。

It is easily verified that ' is congruential w.r.t. + and ·, which means that + and · are well-defined on equivalence classes modulo '. When a,b = 06 , the inverse of a/b is b/a, and it is easily verified that F is a field. The map i: A → F defined such that i(a) = a/1 is an injection of A into F and clearly
 很容易证明“是同余的w.r.t.+和·”，这意味着+和·在等价类模上定义得很好。当a，b=06时，a/b的倒数为b/a，很容易证明f是一个场。图i:a→f定义为i（a）=a/1是a注入f的过程，并且很清楚

.
 .

(2)  Given an injective ring homomorphism h: A → K into a field K,
 给定一个内射环同态H:A→K进入一个场K，

​                                                                                  iff   ab0 = a0b,
 如果ab0=a0b，

which implies that
 这意味着

h(a)h(b0) = h(a0)h(b),
 h（a）h（b0）=h（a0）h（b）

​       and since h is injective and b,b0 = 06 , we get
 因为h是注射剂，b，b0=06，我们得到

h(a)h(b)−1 = h(a0)h(b0)−1.
 H（a）H（b）−1=H（a0）H（b0）−1.

Thus, there is a map bh: F → K such that
 因此，有一个图bh:f→k，这样

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

for all a,b ∈ A, b = 06 , and it is easily checked that h is a field homomorphism. The map bh is clearly unique.
 对于所有的a，b∈a，b=06，很容易证明h是场同态。地图BH显然是独一无二的。

(3)  The uniqueness of F up to isomorphism follows from (2), and is left as an exercise.   
 F到同构的唯一性从（2）开始，留作练习。

The field F given by Proposition 31.7 is called the fraction field of A, and it is denoted by Frac(A).
 命题31.7给出的F场称为a的分数场，用frac（a）表示。

In particular, given an integral domain A, since A[X1,...,Xn] is also an integral domain, we can form the fraction field of the polynomial ring A[X1,...,Xn], denoted by F(X1,...,Xn), where F = Frac(A) is the fraction field of A. It is also called the field of rational functions over F, although the terminology is a bit misleading, since elements of F(X1,...,Xn) only define functions when the dominator is nonnull.
 特别是，给定一个积分域a，由于a[x1，…，xn]也是一个积分域，我们可以形成多项式环a[x1，…，xn]的分数域，用f（x1，…，xn）表示，其中f=frac（a）是a的分数域。它也被称为f上的有理函数域，尽管术语有点误导人，因为f（x1，…，xn）的元素仅在主宰符非空时定义函数。

We now have the following crucial lemma which shows that if a polynomial f(X) is reducible over F[X] where F is the fraction field of A, then f(X) is already reducible over A[X].
 我们现在有下面的关键引理，它表明如果多项式f（x）在f[x]上是可约的，其中f是a的分数域，那么f（x）已经在a[x]上是可约的。

Lemma 31.8. Let A be a UFD and let F be the fraction field of A. For any nonnull polynomial f(X) ∈ A[X] of degree m, if f(X) is not the product of two polynomials of degree strictly smaller than m, then f(X) is irreducible in F[X].
 引理31.8。设a为ufd，设f为a的分数域，对于任意非零多项式f（x）∈m的a[x]，如果f（x）不是严格小于m的两个多项式的乘积，则f（x）在f[x]中是不可约的。

Proof. Assume that f(X) is reducible in F[X] and that f(X) is neither null nor a unit. Then, f(X) = G(X)H(X),
 证据。假设f（x）在f[x]中是可约的，f（x）既不是空的也不是单位。那么，f（x）=g（x）h（x），

where G(X),H(X) ∈ F[X] are polynomials of degree p,q ≥ 1. Let a be the product of the denominators of the coefficients of G(X), and b the product of the denominators of the coefficients of H(X). Then, a,b = 06 , g1(X) = aG(X) ∈ A[X] has degree p ≥ 1, h1(X) = bH(X) ∈ A[X] has degree q ≥ 1, and
 式中g（x），h（x）∈f[x]是p，q≥1的多项式。设a为g（x）系数分母的乘积，b为h（x）系数分母的乘积。那么，a，b=06，g1（x）=ag（x）∈a[x]的阶数p≥1，h1（x）=bh（x）∈a[x]的阶数q≥1，并且

abf(X) = g1(X)h1(X).
 abf（x）=g1（x）h1（x）。

Let c = ab. If c is a unit, then f(X) is also reducible in A[X]. Otherwise, c = c1 ···cn, where ci ∈ A is irreducible. We now use induction on n to prove that
 设c=ab。如果c是一个单位，那么f（x）也可在a[x]中约化。否则，c=c1····cn，其中，ci∈a是不可约的。我们现在用n的归纳法来证明

f(X) = g(X)h(X),
 f（x）=g（x）h（x）

for some polynomials g(X) ∈ A[X] of degree p ≥ 1 and h(X) ∈ A[X] of degree q ≥ 1.
 对于某些多项式，p≥1的g（x）∈a[x]和q≥1的h（x）∈a[x]。

If n = 1, since c = c1 is irreducible, by Lemma 31.5, either c divides g1(X) or c divides h1(X). Say that c divides g1(X), the other case being similar. Then, g1(X) = cg(X) for some g(X) ∈ A[X] of degree p ≥ 1, and since A[X] is an integral ring, we get
 如果n=1，因为c=c1是不可约的，用引理31.5，c除以g1（x）或c除以h1（x）。假设c除以g1（x），另一种情况类似。然后，对于某些p≥1的g（x）∈a[x]的g1（x）=cg（x），由于a[x]是一个积分环，我们得到

f(X) = g(X)h1(X),
 f（x）=g（x）h1（x）

showing that f(X) is reducible in A[X]. If n > 1, since
 表示f（x）在a[x]中是可约化的。如果n>1，因为

c1 ···cnf(X) = g1(X)h1(X),
 c1···cnf（x）=g1（x）h1（x）

c1 divides g1(X)h1(X), and as above, either c1 divides g1(X) or c divides h1(X). In either case, we get c2 ···cnf(X) = g2(X)h2(X)
 c1除以g1（x）h1（x），如上所述，c1除以g1（x）或c除以h1（x）。在这两种情况下，我们得到c2···cnf（x）=g2（x）h2（x）

for some polynomials g2(X) ∈ A[X] of degree p ≥ 1 and h2(X) ∈ A[X] of degree q ≥ 1. By the induction hypothesis, we get
 对于某些多项式，p≥1的g2（x）∈a[x]，q≥1的h2（x）∈a[x]。通过归纳假设，我们得到

f(X) = g(X)h(X),
 f（x）=g（x）h（x）

for some polynomials g(X) ∈ A[X] of degree p ≥ 1 and h(X) ∈ A[X] of degree q ≥ 1, showing that f(X) is reducible in A[X].     
 对于某些多项式，g（x）∈p≥1的a[x]和q≥1的h（x）∈a[x]，表明f（x）在a[x]中是可约的。

Finally, we can prove that (20) holds.
 最后，我们可以证明（20）成立。

Lemma 31.9. Let A be a UFD. Given any three nonnull polynomials f(X),g(X),h(X) ∈ A[X], if f(X) is irreducible and f(X) divides the product g(X)h(X), then either f(X) divides g(X) or f(X) divides h(X).
 引理31.9。让A成为UFD。给定任意三个非零多项式f（x），g（x），h（x）∈a[x]，如果f（x）是不可约的，f（x）将积g（x）h（x）除，则f（x）将g（x）或f（x）将h（x）除。

Proof. If f(X) has degree 0, then the result follows from Lemma 31.5. Thus, we may assume that the degree of f(X) is m ≥ 1. Let F be the fraction field of A. By Lemma 31.8, f(X) is also irreducible in F[X]. Since F[X] is a UFD (by Theorem 29.17), either f(X) divides g(X) or f(X) divides h(X), in F[X]. Assume that f(X) divides g(X), the other case being similar. Then, g(X) = f(X)G(X),
 证据。如果f（x）的阶数为0，那么结果来自引理31.5。因此，我们可以假设f（x）的阶数是m≥1。设f为a的分数域。由引理31.8，f（x）在f[x]中也是不可约的。因为f[x]是一个ufd（根据定理29.17），f（x）除以g（x）或f（x）除以h（x），在f[x]中。假设f（x）除以g（x），另一种情况类似。那么，g（x）=f（x）g（x），

for some G(X) ∈ F[X]. If a is the product the denominators of the coefficients of G, we have ag(X) = q1(X)f(X),
 对于某些g（x）∈f[x]。如果a是g系数分母的乘积，我们得到ag（x）=q1（x）f（x），

where q1(X) = aG(X) ∈ A[X]. If a is a unit, we see that f(X) divides g(X). Otherwise, a = a1 ···an, where ai ∈ A is irreducible. We prove by induction on n that
 式中q1（x）=ag（x）∈a[x]。如果a是一个单位，我们看到f（x）除以g（x）。否则，a=a1··································我们通过归纳法证明了

g(X) = q(X)f(X)
 g（x）=q（x）f（x）

for some q(X) ∈ A[X].
 对于某些q（x）∈a[x]。

If n = 1, since f(X) is irreducible and of degree m ≥ 1 and
 如果n=1，因为f（x）是不可约的，且m≥1，并且

a1g(X) = q1(X)f(X),
 a1g（x）=q1（x）f（x）

by Lemma 31.5, a1 divides q1(X). Thus, q1(X) = a1q(X) where q(X) ∈ A[X]. Since A[X] is an integral domain, we get g(X) = q(X)f(X),
 用引理31.5，a1除以q1（x）。因此，q1（x）=a1q（x），其中q（x）∈a[x]。因为a[x]是一个积分域，我们得到g（x）=q（x）f（x），

and f(X) divides g(X). If n > 1, from
 f（x）除以g（x）。如果n>1，从

a1 ···ang(X) = q1(X)f(X),
 a1···ang（x）=q1（x）f（x），

we note that a1 divides q1(X)f(X), and as in the previous case, a1 divides q1(X). Thus, q1(X) = a1q2(X) where q2(X) ∈ A[X], and we get
 我们注意到a1除以q1（x）f（x），和前面的例子一样，a1除以q1（x）。因此，q1（x）=a1q2（x），其中q2（x）=a[x]，我们得到

a2 ···ang(X) = q2(X)f(X).
 a2···ang（x）=q2（x）f（x）。

By the induction hypothesis, we get
 通过归纳假设，我们得到

g(X) = q(X)f(X)
 g（x）=q（x）f（x）

​           for some q(X) ∈ A[X], and f(X) divides g(X).                                                                               
 对于一些q（x）∈a[x]，f（x）除以g（x）。

We finally obtain the fact that A[X] is a UFD when A is.
 我们最终得出这样一个事实：当a是时，a[x]是一个UFD。

Theorem 31.10. If A is a UFD then the polynomial ring A[X] is also a UFD.
 定理31.10。如果a是ufd，那么多项式环a[x]也是ufd。

Proof. As we said earlier, the factorization property (1) is easier to prove than uniqueness. Assume that f(X) has degree m and let fm be the coefficient of Xm in f(X). Either fm is a unit or it is the product of n ≥ 1 irreducible elements. If fm is a unit we set n = 0. We proceed by induction on the pair (m,n), using the well-founded ordering on pairs, i.e.,
 证据。如前所述，因子分解属性（1）比唯一性更容易证明。假设f（x）的阶数为m，fm是f（x）中xm的系数。fm要么是一个单位，要么是n≥1个不可约元素的乘积。如果fm是一个单位，我们设置n=0。我们通过对（m，n）的归纳，利用对上的有根据的排序，即：

(m,n) ≤ (m0,n0)
 （m，n）≤（m0，n0）

iff either m < m0, or m = m0 and n < n0. If f(X) is a nonnull polynomial of degree 0 which is not a unit, then f(X) ∈ A, and f(X) = fm = a1 ···an for some irreducible ai ∈ A, since A is a UFD. This proves the base case.
 如果m<m0，或m=m0和n<n0。如果f（x）是0次的非零多项式，它不是一个单位，那么f（x）∈a，f（x）=fm=a1····································这证明了基本情况。

If f(X) has degree m > 0 and f(X) is reducible, then
 如果f（x）的度数m>0且f（x）是可约化的，则

f(X) = g(X)h(X),
 f（x）=g（x）h（x）

where g(X) and h(X) have degree p,q ≤ m and are not units. There are two cases.
 其中g（x）和h（x）具有p级，q≤m且不是单位。有两种情况。

(1)    fm is a unit (so n = 0).
 fm是一个单位（因此n=0）。

If so, since fm = gphq (where gp is the coefficient of Xp in g(X) and hq is the coefficient of Xq in h(X)), then gp and hq are both units. We claim that p,q ≥ 1. Otherwise, p = 0 or q = 0, but then either g(X) = g0 is a unit or h(X) = h0 is a unit, a contradiction.
 如果是这样，因为fm=gp hq（其中gp是xp的系数，单位为g（x），hq是xq的系数，单位为h（x）），那么gp和hq都是单位。我们声称p，q≥1。否则，p=0或q=0，但g（x）=g0是一个单位，或h（x）=h0是一个单位，一个矛盾。

Now, since m = p + q and p,q ≥ 1, we have p,q < m so (p,0) < (m,0) and (q,0) < (m,0), and by the induction hypothesis, both g(X) and h(X) can be written as products of irreducible factors, thus so can f(X).
 现在，由于m=p+q和p，q≥1，我们得到p，q<m so（p，0）<（m，0）和（q，0）<（m，0），根据诱导假设，g（x）和h（x）都可以写成不可约因子的乘积，因此f（x）也可以写成。

(2)    fm is not a unit, say fm = a1 ···an where a1,...,an are irreducible and n ≥ 1.
 fm不是一个单位，比如fm=a1··································

(a)     If p,q < m, then (p,n1) < (m,n) and (q,n2) < (m,n) where n1 is the number of irreducible factors of gp or n1 = 0 if gp is irreducible, and similarly n2 is the number of irreducible factors of hp or n2 = 0 if hp is irreducible (note that n1,n2 ≤ n and it is possible that n1 = n if hq is irreducible or n2 = n if gp is irreducible). By the induction hypothesis, g(X) and h(X) can be written as products of irreducible polynomials, thus so can f(X).
 如果p，q<m，则（p，n1）<（m，n）和（q，n2）<（m，n），其中n1是gp的不可约因子数，如果gp不可约，n1=0；同样，n2是hp的不可约因子数，如果hp不可约，n2=0（注意n1，n2≤n，如果hq不可约，n1=n是可能的如果gp不可约，e或n2=n）。根据归纳假设，G（x）和H（x）可以写成不可约多项式的乘积，F（x）也可以写成。

(b)    If p = 0 and q = m, then g(X) = gp and by hypothesis gp is not a unit. Since fm = a1 ···an = gphq and gp is not a unit, either hq is not a unit in which case, by the uniqueness of the number of irreducible elements in the decomposition of fm (since A is a UFD), hq is the product of n2 < n irreducible elements, or n2 = 0 if hq is irreducible. Since n ≥ 1, this implies that (m,n2) < (m,n), and by the induction hypothesis h(X) can be written as products of irreducible polynomials. Since gp ∈ A is not a unit, it can also be written as a product of irreducible elements, thus so can f(X).
 如果p=0，q=m，那么g（x）=gp，假设gp不是一个单位。由于fm=a1····a n=gp hq和gp不是一个单位，在这种情况下，根据fm分解中不可约元素数量的唯一性（因为a是一个ufd），hq是n2<n不可约元素的乘积，或n2=0（如果hq是不可约元素）。由于n≥1，这意味着（m，n2）<（m，n），并且通过归纳假设h（x）可以写成不可约多项式的乘积。由于gp∈a不是一个单位，它也可以写成不可约元素的乘积，因此f（x）也可以。

The case where p = m and q = 0 is similar to the previous case.
 其中p=m和q=0的情况与前一种情况类似。

​                Property (20) follows by Lemma 31.9. By Proposition 31.2, A[X] is a UFD.                        
 属性（20）后接引理31.9。根据提案31.2，a[x]是一个UFD。

As a corollary of Theorem 31.10 and using induction, we note that for any field K, the polynomial ring K[X1,...,Xn] is a UFD.
 作为定理31.10的推论，使用归纳法，我们注意到对于任何场k，多项式环k[x1，…，xn]都是一个ufd。

For the sake of completeness, we shall prove that every PID is a UFD. First, we review the notion of gcd and the characterization of gcd’s in a PID.
 为了完整起见，我们将证明每个PID都是一个UFD。首先，我们回顾了GCD的概念和PID中GCD的特征。

​                Given an integral domain A, for any two elements a,b ∈ A, a,b = 06      , we say that d ∈ A
 给定一个积分域a，对于任意两个元素a，b∈a，a，b=06，我们称d∈a

​       (d = 0)6 is a greatest common divisor (gcd) of a and b if
 （d=0）6是a和b的最大公约数（gcd），如果

(1)    d divides both a and b.
 D把A和B分开。

(2)    For any h ∈ A (h = 0)6  , if h divides both a and b, then h divides d.
 对于任意h∈a（h=0）6，如果h同时除以a和b，则h又除以d。

We also say that a and b are relatively prime if 1 is a gcd of a and b.
 如果1是a和b的gcd，我们也说a和b是相对质数。

Note that a and b are relatively prime iff every gcd of a and b is a unit. If A is a PID, then gcd’s are characterized as follows.
 注意，A和B是相对主要的iff，A和B的每个gcd都是一个单位。如果A是PID，则GCD的特征如下。

Proposition 31.11. Let A be a PID.
 提案31.11.让A成为PID。

*(1)*     For any a,b,d ∈ A (a,b,d = 0)6     , d is a gcd of a and b iff
 对于任何a，b，d∈a（a，b，d=0）6，d是a和b iff的gcd。

(d) = (a,b) = (a) + (b),
 （d）=（a，b）=（a）+（b），

i.e., d generates the principal ideal generated by a and b.
 即，D生成A和B生成的主理想。

*(2)*     (Bezout identity) Two nonnull elements a,b ∈ A are relatively prime iff there are some x,y ∈ A such that
 （Bezout恒等式）两个非零元素a，b∈a是相对质数iff有一些x，y∈a这样

ax + by = 1.
 ax+by=1.

Proof. (1) Recall that the ideal generated by a and b is the set
 证据。（1）回想A和B产生的理想是集合

(a) + (b) = aA + bA = {ax + by | x,y ∈ A}.
 （a）+（b）=aa+ba=a x+x，y∈a。

First, assume that d is a gcd of a and b. If so, a ∈ Ad, b ∈ Ad, and thus, (a) ⊆ (d) and (b) ⊆ (d), so that
 首先，假设d是a和b的gcd，如果是，a∈ad，b∈ad，因此，（a）（d）和（b）（d），这样

(a) + (b) ⊆ (d).
 （a）+（b）（d）。

​         Since A is a PID, there is some t ∈ A, t = 06   , such that
 因为a是pid，所以有一些t∈a，t=06，这样

(a) + (b) = (t),
 （a）+（b）=（t）

and thus, (a) ⊆ (t) and (b) ⊆ (t), which means that t divides both a and b. Since d is a gcd of a and b, t must divide d. But then,
 因此，（a）（t）和（b）（t），这意味着t将a和b分开。由于d是a和b的gcd，t必须将d分开。但是，

(d) ⊆ (t) = (a) + (b),
 （d）（t）=（a）+（b），

and thus, (d) = (a) + (b).
 因此，（d）=（a）+（b）。

Assume now that
 现在假设

(d) = (a) + (b) = (a,b).
 （d）=（a）+（b）=（a，b）。

Since (a) ⊆ (d) and (b) ⊆ (d), d divides both a and b. Assume that t divides both a and b, so that (a) ⊆ (t) and (b) ⊆ (t). Then,
 由于（a）（d）和（b）（d），d将a和b分开。假设t将a和b分开，这样（a）（t）和（b）（t）。然后，

(d) = (a) + (b) ⊆ (t),
 （d）=（a）+（b）（t）、

which means that t divides d, and d is indeed a gcd of a and b. (2) By (1), if a and b are relatively prime, then
 这意味着t除以d，d实际上是a和b的gcd（2）乘以（1），如果a和b是相对质数，那么

(1) = (a) + (b),
 （1）=（a）+（b），

which yields the result. Conversely, if
 结果就是这样。相反，如果

ax + by = 1,
 ax+by=1，

then
 然后

(1) = (a) + (b),
 （1）=（a）+（b），

​         and 1 is a gcd of a and b.                                                                                                                  
 1是A和B的GCD。

Given two nonnull elements a,b ∈ A, if a is an irreducible element and a does not divide b, then a and b are relatively prime. Indeed, if d is not a unit and d divides both a and b, then a = dp and b = dq where p must be a unit, so that
 给定两个非零元素a，b∈a，如果a是不可约元素，a不除b，则a和b是相对质数。实际上，如果d不是一个单位，d将a和b分开，那么a=d p和b=dq，其中p必须是一个单位，因此

b = ap−1q,
 B=AP-1Q，

and a divides b, a contradiction.
 A分B，矛盾。

Theorem 31.12. Let A be ring. If A is a PID, then A is a UFD.
 定理31.12。给我一个电话。如果a是pid，那么a是ufd。

Proof. First, we prove that every nonnull element that is a not a unit can be factored as a product of irreducible elements. Let S be the set of nontrivial principal ideals (a) such that a = 06 is not a unit and cannot be factored as a product of irreducible elements (in particular, a is not irreducible). Assume that S is nonempty. We claim that every ascending chain in
 证据。首先，我们证明了每一个非空元素都是不可约元素的乘积。让我们做一组非平凡主理想（a），这样a=06不是一个单位，不能作为不可约元素（特别是a不是不可约元素）的乘积来考虑。假设s不是空的。我们声称每一条上升链

S is finite. Otherwise, consider an infinite ascending chain
 S是有限的。否则，考虑一个无限的上升链。

(a1) ⊂ (a2) ⊂ ··· ⊂ (an) ⊂ ··· .
 （a1）（a2）······（an）····。

It is immediately verified that
 立即证实

[
 [

(an) n≥1
 （a）n≥1

is an ideal in A. Since A is a PID,
 是A中的理想。因为A是PID，

[
 [

(an) = (a)
 （a）=（a）

n≥1
 n＝1

for some a ∈ A. However, there must be some n such that a ∈ (an), and thus,
 但是，对于某些a∈a，必须有一些n，这样a∈（an），因此，

(an) ⊆ (a) ⊆ (an),
 （an）（a）（an）、

and the chain stabilizes at (an).
 链稳定在（a）。

As a consequence, there are maximal ideals in S. Let (a) be a maximal ideal in S. Then, for any ideal (d) such that
 因此，在S中有最大理想。让（a）在S中是最大理想。然后，对于任何理想（d），这样

​                                                               (a) ⊂ (d)    and    (a) = (6 d),
 （a）（d）和（a）=6 d，

we must have d /∈ S, since otherwise (a) would not be a maximal ideal in S. Observe that a is not irreducible, since (a) ∈ S, and thus,
 我们必须有d/∈s，否则（a）将不是s中的最大理想，观察a不是不可约的，因为（a）∈s，因此，

a = bc
 公元前

for some b,c ∈ A, where neither b nor c is a unit. Then,
 对于某些b，c∈a，其中b和c都不是一个单位。然后，

​                                                               (a) ⊆ (b)    and     (a) ⊆ (c).
 （a）（b）和（a）（c）。

If (a) = (b), then b = au for some u ∈ A, and then
 如果（a）=（b），那么对于某些u∈a，b=au，然后

a = auc,
 A=AUC，

so that
 以便

1 = uc,
 1=UC，

since A is an integral domain, and thus, c is a unit, a contradiction. Thus, (a) = (6 b), and similarly, (a) = (6 c). But then, by a previous observation b /∈ S and c /∈ S, and since a and b are not units, both b and c factor as products of irreducible elements and so does a = bc, a contradiction. This implies that S = ∅, so every nonnull element that is a not a unit can be factored as a product of irreducible elements
 因为A是一个积分域，所以C是一个单位，一个矛盾。因此，（a）=（6 b）和类似地，（a）=（6 c）。但是，根据前面的观察b/∈s和c/∈s，由于a和b不是单位，b和c因子都是不可约元素的产物，a=bc也是一个矛盾。这意味着S=∅，因此，非单位的每个非空元素都可以作为不可约元素的乘积进行分解。

To prove the uniqueness of factorizations, we use Proposition 31.2. Assume that a is irreducible and that a divides bc. If a does not divide b, by a previous remark, a and b are relatively prime, and by Proposition 31.11, there are some x,y ∈ A such that
 为了证明因式分解的唯一性，我们使用命题31.2。假设A是不可约的，而BC是分的。如果a不除以b，通过前面的一句话，a和b是相对质数，并且通过命题31.11，有一些x，y∈a这样

ax + by = 1.
 ax+by=1.

Thus,
 因此，

acx + bcy = c,
 acx+bcy=c，

​         and since a divides bc, we see that a must divide c, as desired.                                                   
 由于a除以bc，我们看到a必须按需要除以c。

Thus, we get another justification of the fact that Z is a UFD and that if K is a field, then K[X] is a UFD.
 因此，我们得到了另一个理由，证明Z是一个UFD，如果K是一个场，那么K[X]是一个UFD。

It should also be noted that in a UFD, gcd’s of nonnull elements always exist. Indeed, this is trivial if a or b is a unit, and otherwise, we can write
 还应该注意的是，在UFD中，总是存在非空元素的gcd。事实上，如果a或b是一个单位，这是微不足道的，否则，我们可以写

​                                                          a = p1 ···pm    and    b = q1 ···qn
 a=p1···pm，b=q1···qn

where pi,qj ∈ A are irreducible, and the product of the common factors of a and b is a gcd of a and b (it is 1 is there are no common factors).
 式中pi，qj∈a是不可约的，a和b的公因子的乘积是a和b的gcd（即1是没有公因子）。

We conclude this section on UFD’s by proving a proposition characterizing when a UFD is a PID. The proof is nontrivial and makes use of Zorn’s lemma (several times).
 我们通过证明当一个UFD是PID时的一个命题来结束这个关于UFD的章节。证明是不平凡的，并利用了佐恩的引理（多次）。

Proposition 31.13. Let A be a ring that is a UFD, and not a field. Then, A is a PID iff every nonzero prime ideal is maximal.
 提案31.13。让A成为一个UFD的环，而不是一个场。然后，a是PID iff，每个非零素数理想都是最大的。

Proof. Assume that A is a PID that is not a field. Consider any nonzero prime ideal, (p), and pick any proper ideal A in A such that
 证据。假设a是一个PID，而不是一个字段。考虑任何非零素数理想，（p），并在a中选择任何合适的理想a

(p) ⊆ A.
 （p）a.

Since A is a PID, the ideal A is a principal ideal, so A = (q), and since A is a proper nonzero ideal, q = 06 and q is not a unit. Since
 因为a是一个PID，理想a是一个主理想，所以a=（q），因为a是一个适当的非零理想，q=06，q不是一个单位。自从

(p) ⊆ (q),
 （p）（q）

q divides p, and we have p = qp1 for some p1 ∈ A. Now, by Proposition 31.1, since p = 06 and (p) is a prime ideal, p is irreducible. But then, since p = qp1 and p is irreducible, p1 must be a unit (since q is not a unit), which implies that
 q除以p，对于某些p1∈a，我们得到p=qp1。现在，根据命题31.1，由于p=06和（p）是素理想，p是不可约的。但是，既然p=q p1和p是不可约的，p1必须是一个单位（因为q不是一个单位），这意味着

(p) = (q);
 （p）=（q）；

that is, (p) is a maximal ideal.
 也就是说，（p）是最大理想。

Conversely, let us assume that every nonzero prime ideal is maximal. First, we prove that every prime ideal is principal. This is obvious for (0). If A is a nonzero prime ideal, then, by hypothesis, it is maximal. Since A = (0)6 , there is some nonzero element a ∈ A. Since A is maximal, a is not a unit, and since A is a UFD, there is a factorization a = a1 ···an of a into irreducible elements. Since A is prime, we have ai ∈ A for some i. Now, by Proposition 31.3, since ai is irreducible, the ideal (ai) is prime, and so, by hypothesis, (ai) is maximal. Since (ai) ⊆ A and (ai) is maximal, we get A = (ai).
 相反，假设每个非零素数理想都是最大的。首先，我们证明了每一个素理想都是主理想。这对于（0）是显而易见的。如果A是非零素数理想，那么根据假设，它是最大的。由于a=（0）6，有一些非零元素a∈a，由于a是极大的，a不是一个单位，由于a是一个ufd，所以a的因式分解a=a1·······························因为a是素数，我们有一些i的ai∈a。现在，根据命题31.3，由于ai是不可约的，理想（ai）是素数，因此，根据假设，（ai）是最大的。因为（ai）a和（ai）是最大的，所以我们得到a=（ai）。

Next, assume that A is not a PID. Define the set, F, by
 接下来，假设a不是PID。定义集合f

F = {A | A ⊆ A, A is not a principal ideal}.
 F=A A A不是主要理想。

Since A is not a PID, the set F is nonempty. Also, the reader will easily check that every chain in FSis bounded inAi is an ideal which is not principal, soF. Indeed, for any chain (ASi)ii∈∈II Aof ideals ini ∈ F. Then, by Zorn’s lemmaF it is not hard to verify that i∈I
 因为a不是PID，所以集合f是非空的。此外，读者还可以很容易地检查到fsis中的每个链都有界，inai是一个理想的，而不是主体，sof。实际上，对于任何链（asi）i i∈ii aof理想ini∈f，那么，通过zorn的lemmaf，不难证明i∈i

(Lemma B.1), the set F has some maximal element, A. Clearly, A = (0)6 is a proper ideal (since A = (1)), and A is not prime, since we just showed that prime ideals are principal. Then, by Theorem B.3, there is some maximal ideal, M, so that A ⊂ M. However, a maximal ideal is prime, and we have shown that a prime ideal is principal. Thus,
 （引理b.1），集合f有一些极大元素a。显然，a=（0）6是一个合适的理想（因为a=（1）），a不是素数，因为我们刚刚证明了素数理想是主的。然后，根据定理B.3，有一些极大理想m，因此a m。然而，极大理想是素数，我们证明了素数理想是主的。因此，

A ⊆ (p),
 A（P）、


 

for some p ∈ A that is not a unit. Moreover, by Proposition 31.1, the element p is irreducible. Define B = {a ∈ A | pa ∈ A}.
 对于某些p∈a，它不是一个单位。此外，根据命题31.1，元素P是不可约的。定义b=a∈a pa∈a。

Clearly, A = pB, B = (0)6 , A ⊆ B, and B is a proper ideal. We claim that A 6= B. Indeed, if A = B were true, then we would have A = pB = B, but this is impossible since p is irreducible, A is a UFD, and B = (0) (6 we get B = pmB for all m, and every element of B would be a multiple of pm for arbitrarily large m, contradicting the fact that A is a UFD). Thus, we have A ⊂ B, and since A is a maximal element of F, we must have B ∈ F/ . However, B ∈ F/ means that B is a principal ideal, and thus, A = pB is also a principal ideal, a contradiction.      
 显然，a=pb，b=（0）6，a b和b是一个合适的理想。我们声称a 6=b。事实上，如果a=b是真的，那么我们将得到a=pb=b，但这是不可能的，因为p是不可约的，a是一个ufd，b=（0）（6我们得到b=pmb对于所有m，b的每个元素对于任意大的m都是pm的倍数，这与a是一个ufd的事实相矛盾。因此，我们有a b，由于a是f的极大元素，我们必须有b∈f/。然而，b∈f/意味着b是一个主理想，因此，a=pb也是一个主理想，一个矛盾。

Observe that the above proof shows that Proposition 31.13 also holds under the assumption that every prime ideal is principal.
 观察到上述证明表明，命题31.13也在每一个素数理想都是主的假设下成立。

## 31.2         The Chinese Remainder Theorem  31.2中国余数定理

In this section, which is a bit of an interlude, we prove a basic result about quotients of commutative rings by products of ideals that are pairwise relatively prime. This result has applications in number theory and in the structure theorem for finitely generated modules over a PID, which will be presented later.
 在这一部分，这是一个有点插曲的部分，我们证明了一个关于交换环商的基本结果，它是理想的两个相对素数的乘积。这个结果在数论和PID上有限生成模块的结构定理中有应用，稍后将介绍。

Given two ideals a and b of a ring A, we define the ideal ab as the set of all finite sums of the form a1b1 + ··· + akbk, ai ∈ a, bi ∈ b.
 给出了A环的两个理想a和b，我们将理想ab定义为a1b1+······+akbk，ai∈a，bi∈b形式的所有有限和的集合。

The reader should check that ab is indeed an ideal. Observe that ab ⊆ a and ab ⊆ b, so that
 读者应该检查AB确实是一个理想。观察AB A和AB B，以便

ab ⊆ a ∩ b.
 AB A B.

In general equality does not hold. However if
 一般来说，平等不成立。但是，如果

a + b = A,
 A+B=A，

then we have
 然后我们有了

ab = a ∩ b.
 AB=A B.

This is because there is some a ∈ a and some b ∈ b such that
 这是因为有一些a∈a和一些b∈b这样

a + b = 1,
 A+B=1，

so for every x ∈ a ∩ b, we have x = xa + xb,
 所以对于每一个x∈a b，我们有x=xa+xb，

which shows that x ∈ ab. Ideals a and b of A that satisfy the condition a + b = A are sometimes said to be comaximal.
 这表明满足a+b=a条件的a的x∈ab理想a和b有时被称为共轴。

We define the homomorphism ϕ: A → A/a × A/b by
 我们定义同态，用

ϕ(x) = (xa,xb),
 ⑨（x）=（xa，xb）

where xa is the equivalence class of x modulo a (resp. xb is the equivalence class of x modulo b). Recall that the ideal a defines the equivalence relation ≡a on A given by
 其中x a是x模a（resp.x b是x模b的等价类）。回想一下，理想A定义了给定的

​                                                           x ≡a y    iff     x − y ∈ a,
 x a y如果x−y∈a，

and that A/a is the quotient ring of equivalence classes xa, where x ∈ A, and similarly for A/b. Sometimes, we also write x ≡ y (mod a) for x ≡a y.
 a/a是等价类xa的商环，其中x∈a，类似于a/b，有时我们也写x y（mod a）表示x a y。

Clearly, the kernel of the homomorphism ϕ is a ∩ b. If we assume that a + b = A, then Ker(ϕ) = a∩b = ab, and because ϕ has a constant value on the equivalence classes modulo ab, the map ϕ induces a quotient homomorphism
 显然，同态的核心是a b。如果我们假设a+b=a，那么ker（_）=a b=ab，并且由于_在等价类模ab上有一个常量值，映射_会产生商同态。

θ: A/ab → A/a × A/b.
 θ：A/AB→A/A×A/B。

Because Ker(ϕ) = ab, the homomorphism θ is injective. The Chinese Remainder Theorem says that θ is an isomorphism.
 因为Ker（η）=ab，同态θ是内射的。中国剩余定理认为θ是同构的。

Theorem 31.14. Given a commutative ring A, let a and b be any two ideals of A such that a + b = A. Then, the homomorphism θ: A/ab → A/a × A/b is an isomorphism.
 定理31.14。给定一个交换环a，让a和b是a的任意两个理想，这样a+b=a，那么同态θ：a/ab→a/a×a/b是同态。

Proof. We already showed that θ is injective, so we need to prove that θ is surjective. We need to prove that for any y,z ∈ A, there is some x ∈ A such that
 证据。我们已经证明θ是内射的，所以我们需要证明θ是射的。我们需要证明，对于任何y，z∈a，有一些x∈a，这样

x ≡ y     (mod a) x ≡ z     (mod b).
 X Y（A型）X Z（B型）。

Since a + b = A, there exist some a ∈ a and some b ∈ b such that
 由于a+b=a，存在一些a∈a和一些b∈b，因此

a + b = 1.
 A+B=1.

If we let
 如果我们让

x = az + by,
 x=az+x，

then we have x ≡a by ≡a (1 − a)y ≡a y − ay ≡a y,
 然后我们得到x a x a（1−a）y a y y a y，

and similarly x ≡b az ≡b (1 − b)z ≡b z − bz ≡b z,
 同样地，x b az b（1−b）z b z−bz b z，

which shows that x = az + by works.                                                                                               
 这表明x=az+是通过工程得出的。

Theorem 31.14 can be generalized to any (finite) number of ideals.
 定理31.14可以推广到任何（有限）个理想。

Theorem 31.15. (Chinese Remainder Theorem) Given a commutative ring A, let a1,...,an be any n ≥ 2 ideals of A such that ai + aj = A for all i =6 j. Then, the homomorphism θ: A/a1 ···an → A/a1 × ··· × A/an is an isomorphism.
 定理31.15。（中国剩余定理）给定交换环a，让a1，…，a是a的任意n≥2个理想，使得aI+a j=a，对于所有i=6j，同态θ：a/a1···························a/an是同态。

Proof. The map θ: A/a1 ∩ ··· ∩ an → A/a1 × ··· × A/an is induced by the homomorphism ϕ: A → A/a1 × ··· × A/an given by
 证据。图θ：a/a1····an→a/a1×··················a/an由下式给出

ϕ(x) = (xa1,...,xan).
 ⑨（x）=（xa1，…，xan）。

Clearly, Ker(ϕ) = a1 ∩ ··· ∩ an, so θ is well-defined and injective. We need to prove that
 很明显，Ker（η）=A1···，因此θ定义明确且具有内射性。我们需要证明

a1 ∩ ··· ∩ an = a1 ···an
 a1····an=a1····an

and that θ is surjective. We proceed by induction. The case n = 2 is Theorem 31.14. By induction, assume that a2 ∩ ··· ∩ an = a2 ···an.
 θ是主观的。我们采用归纳法。案例n=2是定理31.14。通过归纳，假设a2·····an=a2·························

We claim that a1 + a2 ···an = A.
 我们认为a1+a2···an=a。

Indeed, since a1 + ai = A for i = 2,...,n, there exist some ai ∈ a1 and some bi ∈ ai such that
 实际上，由于a1+a i=a，对于i=2，…，n，存在一些ai∈a1和一些bi∈ai，因此

​                                                         ai + bi = 1,         i = 2,...,n,
 ai+bi=1，i=2，…，n，

and by multiplying these equations, we get
 通过乘以这些方程，我们得到

a + b2 ···bn = 1,
 a+b2···bn=1，

where a is a sum of terms each containing some aj as a factor, so a ∈ a1 and b2 ···bn ∈ a2 ···an, which shows that a1 + a2 ···an = A,
 式中a是一个项的总和，每个项都包含一些aj作为因子，因此a∈a1和b2·····································

as claimed. It follows that
 如要求。接下来是

a1 ∩ a2 ∩ ··· ∩ an = a1 ∩ (a2 ···an) = a1a2 ···an.
 a1 a2·····an=a1（a2·····an）=a1a2·······an。

Let us now prove that θ is surjective by induction. The case n = 2 is Theorem 31.14. Let x1,...,xn be any n ≥ 3 elements of A. First, applying Theorem 31.14 to a1 and a2 ···an, we can find y1 ∈ A such that
 现在让我们用归纳法证明θ是主观的。案例n=2是定理31.14。假设x1，…，xn是a的任意n≥3个元素。首先，将定理31.14应用于a1和a2····an，我们可以找到y1∈a，这样

y1 ≡ 1 (mod a1) y1 ≡ 0 (mod a2 ···an).
 Y1 1（A1型）Y1 0（A2型···AN型）。

By the induction hypothesis, we can find y2,...,yn ∈ A such that for all i,j with 2 ≤ i,j ≤ n,
 通过归纳假设，我们可以找到y2，…，yn∈a，这样对于所有i，j，2≤i，j≤n，

yi ≡ 1    (mod ai) yi ≡ 0  (mod aj),      j =6   i.
 Yi 1（mod ai）Yi 0（mod aj），j=6 i。

We claim that
 我们声称

x = x1y1 + x2y2 + ··· + xnyn
 X=x1y1+x2y2+····+xnyn

works. Indeed, using the above congruences, for i = 2,...,n, we get
 作品。实际上，使用上面的一致性，对于i=2，…，n，我们得到

​                                                         x ≡ x1y1 + xi     (mod ai),                                                    (∗)
 xx1y1+Xi（mod ai），（*）

but since a2 ···an ⊆ ai for i = 2,...,n and y1 ≡ 0 (mod a2 ···an), we have
 但是，由于a2············································

​                                                 x1y1 ≡ 0    (mod ai),        i = 2,...,n
 x1y1 0（mod ai），i=2，…，N

and equation (∗) reduces to
 方程式（）减至

​                                                   x ≡ xi     (mod ai),        i = 2,...,n.
 Xi XI（mod ai），i＝2，…，n。

For i = 1, we get
 当i=1时，我们得到

​                                                               x ≡ x1    (mod a1),
 x x1（A1型）

therefore
 因此

​                                                   x ≡ xi     (mod ai),        i = 1,...,n.
 Xi XI（mod ai），i＝1，…，n。

proving surjectivity.                                                                                                                          
 证明主观臆断。

The classical version of the Chinese Remainder Theorem is the case where A = Z and where the ideals ai are defined by n pairwise relatively prime integers m1,...,mn. By the Bezout identity, since mi and mj are relatively prime whenever i =6 j, there exist some ui,uj ∈ Z such that uimi + ujmj = 1, and so miZ + mjZ = Z. In this case, we get an isomorphism
 中国剩余定理的经典版本是A=Z，理想ai由n对相对素数m1，…，mn定义的情况。根据Bezout恒等式，当i=6j时，由于mi和mj是相对素数，因此存在一些ui，uj∈z，使得uimi+ujmj=1，因此miz+mjz=z，在这种情况下，我们得到一个同构

.
 .

In particular, if m is an integer greater than 1 and
 特别是，如果m是大于1的整数，并且

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

is its factorization into prime factors, then
 那么它的因式分解成素因子吗？

Z/mZ ≈ YZ/priiZ.
 z/mz≈yz/priiz.

i
 我

In the previous situation where the integers m1,...,mn are pairwise relatively prime, if we write m = m1 ···mn and m0i = m/mi for i = 1...,n, then mi and m0i are relatively prime, and so  has an inverse modulo mi. If ti is such an inverse, so that
 在前面的情形中，整数m1，…，m n是成对的相对素数，如果我们写m=m1····mn和m0i=m/m i表示i=1…，n，那么mi和m0i是相对素数，因此有一个反模mi。如果ti是反的，那么

,
 ，

then it is not hard to show that for any a1,...,an ∈ Z,
 那么不难证明，对于任何a1，…，an∈z，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

satisfies the congruences
 满足一致性

​                                                  x ≡ ai     (mod mi),        i = 1,...,n.
 x ai（mod mi），i=1，…，n.

Theorem 31.15 can be used to characterize rings isomorphic to finite products of quotient rings. Such rings play a role in the structure theorem for torsion modules over a PID.
 定理31.15可用于描述与商环的有限积同构的环。这样的环在PID上扭转模块的结构定理中起作用。

Given n rings A1,...,An, recall that the product ring A = A1 × ··· × An is the ring in which addition and multiplication are defined componenwise. That is,
 对于n个环a1，…，an，回想一下，乘积环a=a1×··············×an是定义加法和乘法的环。也就是说，

(a1,...,an) + (b1,...,bn) = (a1 + b1,...,an + bn) (a1,...,an) · (b1,...,bn) = (a1b1,...,anbn).
 （a1，…，an）+（b1，…，bn）=（a1+b1，…，an+bn）（a1，…，an）·（b1，…，bn）=（a1b1，…，anbn）。

The additive identity is 0A = (0,...,0) and the multiplicative identity is 1A = (1,...,1). Then, for i = 1,...,n, we can define the element ei ∈ A as follows:
 加法恒等式为0a=（0，…，0），乘法恒等式为1a=（1，…，1）。然后，对于i=1，…，n，我们可以定义元素ei∈a如下：

ei = (0,...,0,1,0,...,0),
 ei=（0，…，0,1,0，…，0），

where the 1 occurs in position i. Observe that the following properties hold for all i,j = 1,...,n:
 当1出现在位置i时，观察以下属性适用于所有i，j=1，…，n：

e2i = ei
 E2i=Ei

eiej = 0, i =6 j e1 + ··· + en = 1A.
 eiej=0，i=6J e1+·····+en=1a。

Also, for any element a = (a1,...,an) ∈ A, we have
 另外，对于任何元素a=（a1，…，an）∈a，我们有

eia = (0,...,0,ai,0,...,0) = pri(a),
 EIA=（0，…，0，ai，0，…，0）=pri（a）

where pri is the projection of A onto Ai. As a consequence
 其中pri是a对ai的投影。因此

Ker(pri) = (1A − ei)A.
 ker（pri）=（1a−ei）a.

Definition 31.3. Given a commutative ring A, a direct decomposition of A is a sequence (b1,...,bn) of ideals in A such that there is an isomorphism A ≈ A/b1 × ··· × A/bn.
 定义31.3.对于交换环A，a的直接分解是a中理想的序列（b1，…，bn），因此存在一个同构a≈a/b1×····×a/bn。

The following theorem gives useful conditions characterizing direct decompositions of a ring.
 下面的定理给出了表征环的直接分解的有用条件。

Theorem 31.16. Let A be a commutative ring and let (b1,...,bn) be a sequence of ideals in A. The following conditions are equivalent:
 定理31.16。设a为交换环，设（b1，…，bn）为a中的理想序列。下列条件等效：

*(a)*    The sequence (b1,...,bn) is a direct decomposition of A.
 序列（b1，…，bn）是a的直接分解。

*(b)*    There exist some elements e1,...,en of A such that
 存在一些元素e1，…，en

e2i = ei
 E2i=Ei

eiej = 0, i =6 j e1 + ··· + en = 1A,
 eiej=0，i=6J e1+·····+en=1a，

and bi = (1A − ei)A, for i,j = 1,...,n.
 而bi=（1a−ei）a，对于i，j=1，…，n。

*(c)*     We have bi + bj = A for all i =6   j, and b1 ···bn = (0).
 对于所有i=6j，我们有bi+bj=a，b1···bn=（0）。

*(d)*    We have bi + bj = A for all i =6   j, and b1 ∩ ··· ∩ bn = (0).
 对于所有i=6j，我们有bi+bj=a，b1·bn=（0）。

Proof. Assume (a). Since we have an isomorphism A ≈ A/b1 ×···× A/bn, we may identify A with A/b1 × ··· × A/bn, and bi with Ker(pri). Then, e1,...,en are the elements defined just before Definition 31.3. As noted, bi = Ker(pri) = (1A − ei)A. This proves (b).
 证据。假设（a）。由于我们有一个同构a≈a/b1×····×a/bn，我们可以用a/b1×···×a/bn来标识a，用ker（pri）来标识bi。那么，e1，…，en是在定义31.3之前定义的元素。如前所述，bi=ker（pri）=（1a−ei）a。这证明（b）。

Assume (b). Since bi = (1A − ei)A and A is a ring with unit 1A, we have 1A − ei ∈ bi for i = 1,...,n. For all i =6 j, we also have ei(1A − ej) = ei − eiej = ei, so (because bj is an ideal), ei ∈ bj, and thus, 1A = 1A − ei + ei ∈ bi + bj, which shows that bi + bj = A for all i =6 j. Furthermore, for any xi ∈ A, with 1 ≤ i ≤ n, we have
 假设（b）。既然bi=（1a−ei）a和a是一个单位为1a的环，我们有1a−ei∈bi表示i=1，…，n。对于所有i=6 j，我们也有ei（1a−ej）=ei−eiej=ei，所以（因为bj是一个理想），ei ei∈bj，因此，1a=1a−ei+ei∈bi+bj，这表明bi+bj=a表示所有i=6 j。此外，对于任何一个具有1个i i的n，我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

which proves that b1 ···bn = (0). Thus, (c) holds.
 证明b1···bn=（0）。因此，（c）成立。

The equivalence of (c) and (d) follows from the proof of Theorem 31.15.
 （c）和（d）的等价性来源于定理31.15的证明。

​       The fact that (c) implies (a) is an immediate consequence of Theorem 31.15.                    
 （c）表示（a）的事实是定理31.15的直接结果。

Here is example of Theorem 31.16. Take the commutative ring of residue classes mod 30, namely
 这是定理31.16的例子。取剩余类mod 30的交换环，即

.
 .

Let
 让

b
 乙

b2 = 3Z/30Z := {3i}9i=0 b3 = 5Z/30Z := {5i}5i=0.
 b2=3z/30z:=3i 9i=0 b3=5z/30z:=5i 5i=0.


 

31.3. NOETHERIAN RINGS AND HILBERT’S BASIS THEOREM
 31.3。诺瑟尔环与希尔伯特基定理

Each bi is an ideal in Z/30Z. Furthermore
 每个BI都是z/30z的理想选择。

Z/30Z = (Z/30Z)/(2Z/30Z) × (Z/30Z)/(3Z/30Z) × (Z/30Z)/(5Z/30Z), where
 Z/30Z=（Z/30Z）/（2Z/30Z）×Z/30Z/（3Z/30Z）×Z/30Z/（5Z/30Z），其中

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

​                        e1 = (1,0,0) → 15,           e2 = (0,1,0) → 10,           e3 = (0,0,1) → 6,
 e1=（1,0,0）→15，e2=（0,1,0）→10，e3=（0,0,1）→6，

since
 自从

.
 .

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image016.gif)

Note that 15 corresponds to 1 ∈ (Z/30Z)/(2Z/30Z), 10 corresponds to
 注意15对应1∈（z/30z）/（2z/30z），10对应

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

1 ∈ (Z/30Z)/(3Z/30Z), while 6 corresponds to 1 ∈ (Z/30Z)/(5Z/30Z).
 1∈（z/30z）/（3z/30z），6对应1∈（z/30z）/（5z/30z）。

## 31.3           Noetherian Rings and Hilbert’s Basis Theorem  31.3诺特环和希尔伯特基定理

Given a (commutative) ring A (with unit element 1), an ideal A ⊆ A is said to be finitely generated if there exists a finite set {a1,...,an} of elements from A so that A = (a1,...,an) = {λ1a1 + ··· + λnan | λi ∈ A, 1 ≤ i ≤ n}.
 给定（交换）环A（具有单位元1），如果存在a的有限集a1，…，a中的一个元素，则称理想a a是有限生成的，因此a=（a1，…，a n）=λ1a1+····+λnanλi∈a，1≤i≤n。

If K is a field, it turns out that every polynomial ideal A in K[X1,...,Xm] is finitely generated. This fact due to Hilbert and known as Hilbert’s basis theorem, has very important consequences. For example, in algebraic geometry, one is interested in the zero locus of a set of polyomial equations, i.e., the set, V (P), of n-tuples (λ1,...,λn) ∈ Kn so that
 如果k是一个域，则证明k[x1，…，xm]中的每个多项式理想a都是有限生成的。这一事实由于希尔伯特而被称为希尔伯特基本定理，具有非常重要的后果。例如，在代数几何中，人们对一组多变量方程的零轨迹感兴趣，即n-元组（λ1，…，λn）∈kn的集合v（p），因此

Pi(λ1,...,λn) = 0
 Pi（λ1，…，λn）=0

for all polynomials Pi(X1,...,Xn) in some given family, P = (Pi)i∈I. However, it is clear that
 对于某些给定族中的所有多项式p i（x1，…，xn），p=（pi）i∈i。然而，很明显

V (P) = V (A),
 V（P）=V（A）

where A is the ideal generated by P. Then, Hilbert’s basis theorem says that V (A) is actually defined by a finite number of polynomials (any set of generators of A), even if P is infinite.
 当a是p产生的理想时，希尔伯特的基定理说v（a）实际上是由有限个多项式（a的任何一组生成元）定义的，即使p是无限的。

The property that every ideal in a ring is finitely generated is equivalent to other natural properties, one of which is the so-called ascending chain condition, abbreviated a.c.c. Before proving Hilbert’s basis theorem, we explore the equivalence of these conditions.
 一个环中的每一个理想都是有限生成的，这一性质等价于其他自然性质，其中一个是所谓的上升链条件，简称A.C.C。在证明希尔伯特基定理之前，我们先探讨这些条件的等价性。

Definition 31.4. Let A be a commutative ring with unit 1. We say that A satisfies the ascending chain condition, for short, the a.c.c, if for every ascending chain of ideals
 定义31.4.设A为单位为1的交换环。我们说，A满足上升链条件，简而言之，A.C.C，如果对于每一个理想的上升链

A1 ⊆ A2 ⊆ ··· ⊆ Ai ⊆ ··· ,
 A1 A2·········

there is some integer n ≥ 1 so that
 有一个整数n≥1，所以

​                                                       Ai = An     for all      i ≥ n + 1.
 ai=所有i的a≥n+1。

We say that A satisfies the maximum condition if every nonempty collection C of ideals in A has a maximal element, i.e., there is some ideal A ∈ C which is not contained in any other ideal in C.
 如果A中的每一个非空集合C都有一个极大元素，即在C中有一个不包含在任何其他理想中的理想A∈C，则A满足极大条件。

Proposition 31.17. A ring A satisfies the a.c.c if and only if it satisfies the maximum condition.
 提案31.17。如果且仅当A环满足最大条件时，A环满足交流。

Proof. Suppose that A does not satisfy the a.c.c. Then, there is an infinite strictly ascending sequence of ideals
 证据。假设a不满足a.c.c，那么有一个无限严格的理想上升序列。

A1 ⊂ A2 ⊂ ··· ⊂ Ai ⊂ ··· ,
 A1 A2········

and the collection C = {Ai} has no maximal element.
 集合c=ai没有最大元素。

Conversely, assume that A satisfies the a.c.c. Let C be a nonempty collection of ideals Since C is nonempty, we may pick some ideal A1 in C. If A1 is not maximal, then there is some ideal A2 in C so that
 相反，假设a满足a.c.c.假设c是理想的非空集合，因为c是非空的，我们可以在c中选择一些理想a1。如果a1不是最大的，那么在c中有一些理想a2，因此

A1 ⊂ A2.
 A1 A2.

Using this process, if C has no maximal element, we can define by induction an infinite strictly increasing sequence
 利用这个过程，如果c没有最大元素，我们可以通过归纳一个无限严格递增序列来定义。

A1 ⊂ A2 ⊂ ··· ⊂ Ai ⊂ ··· .
 A1 A2········

However, the a.c.c. implies that such a sequence cannot exist. Therefore, C has a maximal element.   
 然而，交流意味着这样的序列不可能存在。因此，c有一个极大的元素。

Having shown that the a.c.c. condition is equivalent to the maximal condition, we now prove that the a.c.c. condition is equivalent to the fact that every ideal is finitely generated. Proposition 31.18. A ring A satisfies the a.c.c if and only if every ideal is finitely generated.
 在证明了交流条件等价于最大条件之后，我们现在证明了交流条件等价于每个理想都是有限生成的。提案31.18。当且仅当每个理想都是有限生成的时，A环才满足交流。

Proof. Assume that every ideal is finitely generated. Consider an ascending sequence of ideals
 证据。假设每个理想都是有限生成的。考虑理想的升序

A1 ⊆ A2 ⊆ ··· ⊆ Ai ⊆ ··· .
 A1 A2········

Observe that A = Si Ai is also an ideal. By hypothesis, A has a finite generating set {a1,...,an}. By definition of A, each ai belongs to some Aji, and since the Ai form an ascending chain, there is some m so that ai ∈ Am for i = 1,...,n. But then,
 观察a=si-ai也是一个理想。根据假设，A有一个有限的生成集A1，…，一个。根据a的定义，每个a i都属于某个aji，由于ai形成了一条上升链，所以有一些m使得ai∈am代表i=1，…，n，但是，

Ai = Am
 ai=上午

for all i ≥ m + 1, and the a.c.c. holds.
 对于所有i≥m+1，并且交流保持不变。

Conversely, assume that the a.c.c. holds. Let A be any ideal in A and consider the family C of subideals of A that are finitely generated. The family C is nonempty, since (0) is a subideal of A. By Proposition 31.17, the family C has some maximal element, say B. For
 相反，假设交流电保持不变。让a是a中的任何理想，并考虑a的子理想的C族，这些子理想是有限生成的。C族是非空的，因为（0）是A的次理想。根据命题31.17，C族有一些极大的元素，比如b。

31.3. NOETHERIAN RINGS AND HILBERT’S BASIS THEOREM
 31.3。诺瑟尔环与希尔伯特基定理

any a ∈ A, the ideal B + (a) (where B + (a) = {b + λa | b ∈ B, λ ∈ A}) is also finitely generated (since B is finitely generated), and by maximality, we have
 任意a∈a，理想b+（a）（其中b+（a）=b+λa b∈b，λ∈a）也是有限生成的（因为b是有限生成的），并且通过极大性，我们得到

B = B + (a).
 B=B+（A）。

So, we get a ∈ B for all a ∈ A, and thus, A = B, and A is finitely generated.                                   
 因此，我们得到所有a∈a的a∈b，因此，a=b，a是有限生成的。

Definition 31.5. A commutative ring A (with unit 1) is called noetherian if it satisfies the a.c.c. condition. A noetherian domain is a noetherian ring that is also a domain.
 定义31.5.如果一个交换环A（带单位1）满足交流条件，它就称为非以太环。诺特域是一个诺特环，也是一个域。

By Proposition 31.17 and Proposition 31.18, a noetherian ring can also be defined as a ring that either satisfies the maximal property or such that every ideal is finitely generated. The proof of Hilbert’s basis theorem will make use the following lemma:
 通过命题31.17和命题31.18，一个诺厄特环也可以定义为一个满足最大性质或每个理想都是有限生成的环。希尔伯特基本定理的证明将使用以下引理：

Lemma 31.19. Let A be a (commutative) ring. For every ideal A in A[X], for every i ≥ 0, let Li(A) denote the set of elements of A consisting of 0 and of the coefficients of Xi in all the polynomials f(X) ∈ A which are of degree i. Then, the Li(A)’s form an ascending chain of ideals in A. Furthermore, if B is any ideal of A[X] so that A ⊆ B and if Li(A) = Li(B) for all i ≥ 0, then A = B.
 引理31.19。设A为（交换）环。对于[x]中的每个理想A，对于每i i 0，让李（a）表示由0个多项式组成的元素集合和所有i（i）x的多项式i的系数，然后，李（a）形成理想的上升链。此外，如果B是[x]的任何理想，那么Ab如果所有i≥0的li（a）=li（b），则a=b。

Proof. That Li(A) is an ideal and that Li(A) ⊆ Li+1(A) follows from the fact that if f(X) ∈ A and g(X) ∈ A, then f(X) + g(X), λf(X), and Xf(X) all belong to A. Now, let g(X) be any polynomial in B, and assume that g(X) has degree n. Since Ln(A) = Ln(B), there is some polynomial fn(X) in A, of degree n, so that g(X) − fn(X) is of degree at most n − 1. Now, since A ⊆ B, the polynomial g(X) − fn(X) belongs to B. Using this process, we can define by induction a sequence of polynomials fn+i(X) ∈ A, so that each fn+i(X) is either zero or has degree n − i, and
 证据。李（a）是一个理想，李（a）李+1（a）是从F（x）A和G（x）A出发的，那么F（x）+G（x）、λf（x）和Xf（x）都属于A，现在，假设G（x）是B中的任何多项式，假设G（x）具有n次方，因为ln（a）=ln（b），degre的a中有一些多项式fn（x）。e n，使g（x）−fn（x）至多为n−1。现在，由于a b，多项式g（x）−fn（x）属于b。利用这个过程，我们可以通过归纳定义多项式fn+i（x）∈a的序列，使每个fn+i（x）要么为零，要么为n−i，并且

g(X) − (fn(X) + fn+1(X) + ··· + fn+i(X))
 G（X）−（FN（X）+FN+1（X）+······+FN+I（X））

is of degree at most n − i − 1. Note that this last polynomial must be zero when i = n, and thus, g(X) ∈ A. 
 最多为n−i−1度。注意，当i=n时，最后一个多项式必须为零，因此，g（x）∈a。

We now prove Hilbert’s basis theorem. The proof is substantially Hilbert’s original proof. A slightly shorter proof can be given but it is not as transparent as Hilbert’s proof (see the remark just after the proof of Theorem 31.20, and Zariski and Samuel [188], Chapter IV, Section 1, Theorem 1).
 我们现在证明希尔伯特基本定理。证据实质上是希尔伯特的原始证据。可以给出一个稍短的证明，但它不如希尔伯特的证明那么透明（见定理31.20证明之后的注释，以及Zariski和Samuel[188]，第四章，第1节，定理1）。

Theorem 31.20. (Hilbert’s basis theorem) If A is a noetherian ring, then A[X] is also a noetherian ring.
 定理31.20。（希尔伯特基本定理）如果A是一个非以太环，那么[X]也是一个非以太环。

Proof. Let A be any ideal in A[X], and denote by L the set of elements of A consisting of 0 and of all the coefficients of the highest degree terms of all the polynomials in A. Observe that
 证据。设a为a[x]中的任何理想，并用l表示a中由0组成的元素集和a中所有多项式的最高次数项的所有系数。观察

.
 .

Thus, L is an ideal in A (this can also be proved directly). Since A is noetherian, L is finitely generated, and let {a1,...,an} be a set of generators of L. Let f1(X),...,fn(X) be polynomials in A having respectively a1,...,an as highest degree term coefficients. These polynomials generate an ideal B. Let q be the maximum of the degrees of the fi(X)’s. Now, pick any polynomial g(X) ∈ A of degree d ≥ q, and let aXd be its term of highest degree. Since a ∈ L, we have a = λ1a1 + ··· + λnan,
 因此，L是A中的理想（这也可以直接证明）。由于a是诺特良的，l是有限生成的，并且让a1，…，a是l的一组生成元。让f1（x），…，fn（x）是a中的多项式，分别具有a1，…，作为最高阶项系数。这些多项式产生一个理想的b，设q为fi（x）的最大度数，现在选取任意一个d≥q的多项式g（x）∈a，设axd为其最高度数项。由于a∈l，我们得到a=λ1a1+·····+λnan，

for some λi ∈ A. Consider the polynomial
 对于某些λi∈a.考虑多项式

,
 ，

where di is the degree of fi(X). Now, g(X) − g1(X) is a polynomial in A of degree at most d − 1. By repeating this procedure, we get a sequence of polynomials gi(X) in B, having strictly decreasing degrees, and such that the polynomial
 其中di是fi（x）的度数。现在，g（x）−g1（x）是一个次数最多为d−1的多项式。通过重复这一过程，我们得到了B中多项式gi（x）的序列，严格地具有递减的度数，这样多项式

g(X) − (g1(X) + ··· + gi(X))
 g（x）−（g1（x）+·····+gi（x））

is of degree at most d − i. This polynomial must be of degree at most q − 1 as soon as i = d − q + 1. Thus, we proved that every polynomial in A of degree d ≥ q belongs to B.
 至多为d−i的度数。只要i=d−q+1，此多项式至多为q−1的度数。由此证明了D≥Q阶A中的每一个多项式都属于B。

It remains to take care of the polynomials in A of degree at most q − 1. Since A is noetherian, each ideal Li(A) is finitely generated, and let {ai1,...,aini} be a set of generators for Li(A) (for i = 0,...,q − 1). Let fij(X) be a polynomial in A having aijXi as its highest degree term. Given any polynomial g(X) ∈ A of degree d ≤ q − 1, if we denote its term of highest degree by aXd, then, as in the previous argument, we can write
 它仍然要注意多项式的程度，最多为q-1。由于a是诺特良的，每个理想的li（a）都是有限生成的，并且让a i 1，…，aini成为li（a）的一组发生器（对于i=0，…，q−1）。让fij（x）是以aijxi为最高次数项的多项式。给定任意多项式g（x）∈a的d≤q−1，如果我们用a x d表示它的最高阶项，那么，就像前面的论点一样，我们可以写出

a = λ1ad1 + ··· + λndadnd,
 A=λ1ad1+····+λndadnd，

and we define
 我们定义

,
 ，

where di is the degree of fdi(X). Then, g(X)−g1(X) is a polynomial in A of degree at most d − 1, and by repeating this procedure at most q times, we get an element of A of degree 0, and the latter is a linear combination of the f0i’s. This proves that every polynomial in A of degree at most q − 1 is a combination of the polynomials fij(X), for 0 ≤ i ≤ q − 1 and 1 ≤ j ≤ ni. Therefore, A is generated by the fk(X)’s and the fij(X)’s, a finite number of polynomials.    
 式中，di是外国直接投资的程度（x）。那么，g（x）−g1（x）是至多d−1阶的多项式，通过至多q次重复这个过程，我们得到一个0阶的元素，后者是f0i的线性组合。这证明了至多q−1阶的每个多项式都是pol的组合。对于0≤i≤q−1和1≤j≤ni，ynomials fij（x）。因此，由fk（x）’和fij（x）’生成a，这是有限数量的多项式。

Remark: Only a small part of Lemma 31.19 was used in the above proof, namely, the fact that Li(A) is an ideal. A shorter proof of Theorem 31.21 making full use of Lemma 31.19 can be given as follows:
 注：上述证明中只使用了引理31.19的一小部分，即李（a）是一个理想的事实。充分利用引理31.19，定理31.21的较短证明如下：

31.4. FUTHER READINGS
 31.4。进一步阅读

Proof. (Second proof) Let (Ai)i≥1 be an ascending sequence of ideals in A[X]. Consider the doubly indexed family (Li(Aj)) of ideals in A. Since A is noetherian, by the maximal property, this family has a maximal element Lp(Aq). Since the Li(Aj)’s form an ascending sequence when either i or j is fixed, we have Li(Aj) = Lp(Aq) for all i and j with i ≥ p and j ≥ q, and thus, Li(Aq) = Li(Aj) for all i and j with i ≥ p and j ≥ q. On the other hand, for any fixed i, the a.c.c. shows that there exists some integer n(i) so that Li(Aj) = Li(An(i)) for all j ≥ n(i). Since Li(Aq) = Li(Aj) when i ≥ p and j ≥ q, we may take n(i) = q if i ≥ p. This shows that there is some n0 so that n(i) ≤ n0 for all i ≥ 0, and thus, we have Li(Aj) = Li(An(0)) for every i and for every j ≥ n(0). By Lemma 31.19, we get Aj = An(0) for every j ≥ n(0), establishing the fact that A[X] satisfies the a.c.c. 
 证据。（第二个证明）让（a i）i≥1是a[x]中理想的升序。考虑A中理想的双索引族（li（aj））。由于a是诺特良族，根据极大性，该族具有极大元素lp（aq）。由于当i或j固定时，li（aj）形成一个升序，所以对于i≥p和j≥q的所有i和j，我们都有li（aj）=lp（aq），因此，对于i≥p和j≥q的所有i和j，li（aq）=li（aj）。另一方面，对于任何固定i，a.c.c.表明存在一些整数n（i）。因此，对于所有j≥n（i），li（aj）=li（an（i））。由于当i≥p且j≥q时，li（aq）=li（aj），如果i≥p，我们可以取n（i）=q。这表明存在一些n0，因此对于所有i≥0，n（i）≤n0，因此，对于每个i和j≥n（0），我们都有li（aj）=li（an（0））。通过引理31.19，我们得到每j≥n（0）的aj=an（0），证明a[x]满足a.c.c。

Using induction, we immediately obtain the following important result.
 利用归纳法，我们立即得到以下重要结果。

Corollary 31.21. If A is a noetherian ring, then A[X1,...,Xn] is also a noetherian ring.
 推论31.21。如果A是一个非以太环，那么[x1，…，xn]也是一个非以太环。

Since a field K is obviously noetherian (since it has only two ideals, (0) and K), we also have:
 因为一个场k显然是非以太的（因为它只有两个理想，（0）和k），我们也有：

Corollary 31.22. If K is a field, then K[X1,...,Xn] is a noetherian ring.
 推论31.22。如果k是一个场，那么k[x1，…，xn]是一个非其他环。

## 31.4       Futher Readings  31.4进一步读数

The material of this Chapter is thoroughly covered in Lang [106], Artin [7], Mac Lane and Birkhoff [115], Bourbaki [25, 26], Malliavin [116], Zariski and Samuel [188], and Van Der Waerden [173].
 本章的材料在lang[106]、Artin[7]、Mac Lane和Birkhoff[115]、Bourbaki[25，26]、Malliavin[116]、Zariski和Samuel[188]以及van der Waerden[173]中有详细介绍。


 