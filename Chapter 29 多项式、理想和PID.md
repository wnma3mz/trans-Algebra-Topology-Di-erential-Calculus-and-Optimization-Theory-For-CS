第二十九章

# Polynomials, Ideals and PID’s  多项式、理想和PID

##       29.1      Multisets  29.1多集

This chapter contains a review of polynomials and their basic properties. First, multisets are defined. Polynomials in one variable are defined next. The notion of a polynomial function in one argument is defined. Polynomials in several variable are defined, and so is the notion of a polynomial function in several arguments. The Euclidean division algorithm is presented, and the main consequences of its existence are derived. Ideals are defined, and the characterization of greatest common divisors of polynomials in one variables (gcd’s) in terms of ideals is shown. We also prove the Bezout identity. Next, we consider the factorization of polynomials in one variables into irreducible factors. The unique factorization of polynomials in one variable into irreducible factors is shown. Roots of polynomials and their multiplicity are defined. It is shown that a nonnull polynomial in one variable and of degree m over an integral domain has at most m roots. The chapter ends with a brief treatment of polynomial interpolation: Lagrange, Newton, and Hermite interpolants are introduced.
 本章回顾了多项式及其基本性质。首先，定义多集。接下来定义一个变量的多项式。定义了一个参数中多项式函数的概念。定义了几个变量的多项式，以及几个参数中多项式函数的概念。提出了欧几里得分割算法，并推导了其存在的主要后果。定义了理想，并给出了一个变量（GCD）中多项式最大公约数的理想特征。我们也证明了贝佐特的身份。接下来，我们考虑将一个变量中的多项式因式分解为不可约因子。证明了多项式在一个变量中的唯一因式分解为不可约因子。定义了多项式的根及其多重性。结果表明，一个变量的非零多项式和一个积分域上的m次多项式最多有m个根。最后简要介绍了多项式插值的方法：拉格朗日插值法、牛顿插值法和埃尔米特插值法。

In this chapter, it is assumed that all rings considered are commutative. Recall that a (commutative) ring A is an integral domain (or an entire ring) if 1 = 06 , and if ab = 0, then either a = 0 or b = 0, for all a,b ∈ A. This second condition is equivalent to saying that if a = 06 and b = 06 , then ab = 06 . Also, recall that a = 06 is not a zero divisor if ab 6= 0 whenever b = 06 . Observe that a field is an integral domain.
 在本章中，假设所有考虑的环都是交换的。回想一下，（交换）环A是一个积分域（或一个整环），如果1=06，并且如果a b=0，那么a=0或b=0，对于所有a，b∈a。第二个条件等价于说，如果a=06和b=06，那么ab=06。另外，如果a b 6=0，当b=06时，a=06不是零除数。观察一个场是一个积分域。

Our goal is to define polynomials in one or more indeterminates (or variables) X1,...,Xn, with coefficients in a ring A. This can be done in several ways, and we choose a definition that has the advantage of extending immediately from one to several variables. First, we need to review the notion of a (finite) multiset.
 我们的目标是在一个或多个不确定项（或变量）x1，…，xn中定义多项式，其中系数在环A中。这可以通过多种方式实现，并且我们选择的定义具有立即从一个变量扩展到多个变量的优点。首先，我们需要回顾一下（有限）多重集的概念。

Definition 29.1. Given a set I, a (finite) multiset over I is any function M : I → N such that M(i) = 06 for finitely many i ∈ I. The multiset M such that M(i) = 0 for all i ∈ I is the empty multiset, and it is denoted by 0. If M(i) = k = 06 , we say that i is a member of M of multiplicity k. The union M1 + M2 of two multisets M1 and M2 is defined such that
 定义29.1.给定一个集合i，i上的（有限）多集是任意函数m:i→n，这样m（i）=06表示有限多i∈i。多集m使得m（i）=0表示所有i∈i为空多集，并用0表示。如果m（i）=k=06，我们说i是多重性k的m的成员。两个多集m1和m2的联合m1+m2的定义如下：

(M1 +M2)(i) = M1(i)+M2(i), for every i ∈ I. If I is finite, say I = {1,...,n}, the multiset
 （m1+m2）（i）=m1（i）+m2（i），对于每一个i∈i，如果i是有限的，那么说i=1，…，n，多集

955
 九百五十五

M such that M(i) = ki for every i, 1 ≤ i ≤ n, is denoted by k1 · 1 + ··· + kn · n, or more simply, by (k1,...,kn), and deg(k1 · 1 + ··· + kn · n) = k1 + ··· + kn is the size or degree of M. The set of all multisets over I is denoted by N(I), and when I = {1,...,n}, by N(n).
 m使得m（i）=ki，对于每一个i，1≤i≤n，用k1·1+·················+kn·n表示，或者更简单地说，用（k1，…，kn）表示，deg（k1·1+·················+kn·n）=k1+·············+kn

Intuitively, the order of the elements of a multiset is irrelevant, but the multiplicity of each element is relevant, contrary to sets. Every i ∈ I is identified with the multiset Mi such that Mi(i) = 1 and Mi(j) = 0 for j =6 i. When I = {1}, the set N(1) of multisets k ·1 can be identified with N and {1}∗. We will denote k · 1 simply by k.
 直观地说，多集元素的顺序是不相关的，但是每个元素的多重性是相关的，与集相反。每一个i∈i都用多集mi来标识，使得mi（i）=1，mi（j）=0（j=6i），当i=1时，多集k·1的n（1）可以用n和1来标识。我们将简单地用k来表示k·1。

 However, beware that when n ≥ 2, the set N(n) of multisets cannot be identified with the set of strings in {1,...,n}∗, because multiset union is commutative, but concatenation of strings in {1,...,n}∗ is not commutative when n ≥ 2. This is because in a multiset k1 · 1 + ··· + kn · n, the order is irrelevant, whereas in a string, the order is relevant. For example, 2 · 1 + 3 · 2 = 3 · 2 + 2 · 1, but 11222 = 222116 , as strings over {1,2}.
 但是，要注意，当n≥2时，多集的集合n（n）不能用1，…，n中的字符串集来标识，因为多集并集是交换的，而1，…，n中的字符串的连接在n≥2时不是交换的。这是因为在多集k1·1+·····+kn·n中，顺序是不相关的，而在字符串中，顺序是相关的。例如，2·1+3·2=3·2+2·1，但11222=222116，作为1,2上的字符串。

Nevertherless, N(n) and the set Nn of ordered n-tuples under component-wise addition are isomorphic under the map
 然而，在映射下，按分量加法的有序n-元组的n（n）和集合nn是同构的。

k1 · 1 + ··· + kn · n 7→ (k1,...,kn).
 k1·1+·····+kn·n 7→（k1，…，kn）。

Thus, since the notation (k1,...,kn) is less cumbersome that k1 · 1 + ··· + kn · n, it will be preferred. We just have to remember that the order of the ki is really irrelevant.
 因此，由于符号（k1，…，kn）比k1·1+········+kn·n更为繁琐，因此最好使用它。我们只需要记住，ki的顺序确实是不相关的。

 But when I is infinite, beware that N(I) and the set NI of ordered I-tuples are not isomorphic.
 但当我无穷大时，要注意有序i-元组的n（i）和集ni不是同构的。

We are now ready to define polynomials.
 我们现在准备定义多项式。

##       29.2      Polynomials  29.2多项式

We begin with polynomials in one variable.
 我们从一个变量的多项式开始。

Definition 29.2. Given a ring A, we define the set PA(1) of polynomials over A in one variable as the set of functions P : N → A such that P(k) = 06 for finitely many k ∈ N. The polynomial such that P(k) = 0 for all k ∈ N is the null (or zero) polynomial and it is denoted by 0. We define addition of polynomials, multiplication by a scalar, and multiplication of polynomials, as follows: Given any three polynomials P,Q,R ∈ PA(1), letting ak = P(k), bk = Q(k), and ck = R(k), for every k ∈ N, we define R = P + Q such that
 定义29.2.对于一个环A，我们将一个变量上多项式的集合PA（1）定义为函数集P:N→A，这样对于有限多个k∈n，p（k）=06。对于所有k∈n，p（k）=0的多项式是零（或零）多项式，用0表示。我们定义了多项式的加法、标量乘法和多项式的乘法，如下：给定任意三个多项式p、q、r∈p a（1），让a k=p（k）、bk=q（k）和ck=r（k），对于每一个k∈n，我们定义r=p+q，使

ck = ak + bk,
 ck=ak+bk，

R = λP such that ck = λak,
 r=λp，因此ck=λak，

where λ ∈ A,
 式中，λ∈a，

and R = PQ such that
 R=PQ，因此

ck = X aibj.
 ck=x aibj.

i+j=k
 I+J＝K

We define the polynomial ek such that ek(k) = 1 and ek(i) = 0 for i =6 k. We also denote e0 by 1 when k = 0. Given a polynomial P, the ak = P(k) ∈ A are called the coefficients of P. If P is not the null polynomial, there is a greatest n ≥ 0 such that an = 0 (6 and thus, ak = 0 for all k > n) called the degree of P and denoted by deg(P). Then, P is written uniquely as
 我们定义多项式Ek，使Ek（k）=1，Ek（i）=0代表i=6 k。当k=0时，我们也用1表示e0。对于一个多项式p，a k=p（k）∈a被称为p的系数。如果p不是零多项式，则有一个最大的n≥0，使得a=0（6，因此，k>n的所有k=0）被称为p的度数，并用deg（p）表示。然后，p被唯一地写为

P = a0e0 + a1e1 + ··· + anen.
 P=a0e0+a1e1+····+anen。

When P is the null polynomial, we let deg(P) = −∞.
 当p是零多项式时，我们让deg（p）=-∞。

There is an injection of A into PA(1) given by the map a 7→ a1 (recall that 1 denotes e0). There is also an injection of N into PA(1) given by the map k →7 ek. Observe that
 在图A 7→A1给出的PA（1）中注入了A（记住1表示e0）。图K→7EK给出的PA（1）中也注入了N。注意

(with = 1). In order to alleviate the notation, we often denote e1 by X, and we call X a variable (or indeterminate). Then,  is denoted by Xk. Adopting this notation, given a nonnull polynomial P of degree n, if P(k) = ak, P is denoted by
 （与=1）。为了减少符号，我们通常用x表示e1，我们称x为变量（或不确定）。然后，用xk表示。采用这个符号，给出n次的非零多项式p，如果p（k）=ak，p表示为

P = a0 + a1X + ··· + anXn,
 P=a0+a1x+····+anxn，

or by
 或通过

P = anXn + an−1Xn−1 + ··· + a0,
 P=anxn+an−1Xn−1+····+a0，

if this is more convenient (the order of the terms does not matter anyway). Sometimes, it will also be convenient to write a polynomial as
 如果这样更方便（条款的顺序无论如何都不重要）。有时，将多项式写成

P = a0Xn + a1Xn−1 + ··· + an.
 P=a0xn+a1xn−1+····+an。

The set PA(1) is also denoted by A[X] and a polynomial P may be denoted by P(X). In denoting polynomials, we will use both upper-case and lower-case letters, usually, P,Q, R,S, p,q,r,s, but also f,g,h, etc., if needed (as long as no ambiguities arise).
 集合p a（1）也用[x]表示，多项式p可用p（x）表示。在表示多项式时，我们将同时使用大写和小写字母，通常是P、Q、R、S、P、Q、R、S，如果需要，也可以使用F、G、H等（只要不出现歧义）。

Given a nonnull polynomial P of degree n, the nonnull coefficient an is called the leading coefficient of P. The coefficient a0 is called the constant term of P. A polynomial of the form akXk is called a monomial. We say that akXk occurs in P if ak = 06 . A nonzero polynomial P of degree n is called a monic polynomial (or unitary polynomial, or monic) if an = 1, where an is its leading coefficient, and such a polynomial can be written as
 给定n次的非零多项式p，非零系数an称为p的前导系数。系数a0称为p的常数项。形式为akxk的多项式称为单项式。如果ak=06，则akxk出现在p中。n次的非零多项式p称为monic多项式（或一元多项式，或monic），如果an=1，其中an是其导系数，这样的多项式可以写为

​                           P = Xn + an−1Xn−1 + ··· + a0          or           P = Xn + a1Xn−1 + ··· + an.
 P=xn+an−1Xn−1+·····+a0或P=xn+a1xn−1+····+an。

 The choice of the variable X to denote e1 is standard practice, but there is nothing special about X. We could have chosen Y , Z, or any other symbol, as long as no ambiguities arise.
 变量x表示e1的选择是标准做法，但x没有什么特别之处，只要没有歧义，我们可以选择y、z或任何其他符号。

Formally, the definition of PA(1) has nothing to do with X. The reason for using X is simply convenience. Indeed, it is more convenient to write a polynomial as P = a0 + a1X + ··· + anXn rather than as P = a0e0 + a1e1 + ··· + anen.
 从形式上讲，pa（1）的定义与x无关，使用x的原因很简单。实际上，将多项式写成p=a0+a1x+·····+anxn比写成p=a0e0+a1e1+····+anen更方便。

We have the following simple but crucial proposition.
 我们有以下简单但关键的命题。

Proposition 29.1. Given two nonnull polynomials P(X) = a0+a1X+···+amXm of degree m and Q(X) = b0 + b1X + ··· + bnXn of degree n, if either am or bn is not a zero divisor, then ambn = 06 , and thus, PQ = 06 and
 提案29.1.给出了两个非零多项式p（x）=a0+a1x+······················································

deg(PQ) = deg(P) + deg(Q).
 度（PQ）=deg（P）+deg（Q）。

In particular, if A is an integral domain, then A[X] is an integral domain.
 特别地，如果a是一个积分域，那么[x]是一个积分域。

Proof. Since the coefficient of Xm+n in PQ is ambn, and since we assumed that either am or an is not a zero divisor, we have ambn = 06 , and thus, PQ = 06 and
 证据。由于pq中xm+n的系数是ambn，并且由于我们假设am或an不是零除数，我们得到ambn=06，因此pq=06和

deg(PQ) = deg(P) + deg(Q).
 度（PQ）=deg（P）+deg（Q）。

​          Then, it is obvious that A[X] is an integral domain.                                                                     
 很明显，a[x]是一个积分域。

It is easily verified that A[X] is a commutative ring, with multiplicative identity 1X0 = 1. It is also easily verified that A[X] satisfies all the conditions of Definition 3.1, but A[X] is not a vector space, since A is not necessarily a field.
 很容易证明[X]是一个交换环，其乘法恒等式为1X0=1。也很容易证明[X]满足定义3.1的所有条件，但[X]不是向量空间，因为A不一定是场。

A structure satisfying the axioms of Definition 3.1 when K is a ring (and not necessarily a field) is called a module. Modules fail to have some of the nice properties that vector spaces have, and thus, they are harder to study. For example, there are modules that do not have a basis. We postpone the study of modules until Chapter 34.
 当k是环（不一定是场）时，满足定义3.1公理的结构称为模块。模件没有向量空间所具有的一些好的性质，因此很难研究。例如，有些模块没有基础。我们将模块的研究推迟到第34章。

However, when the ring A is a field, A[X] is a vector space. But even when A is just a be written in a unique way asring, the family of polynomials (PX(Xk)) =k∈Nais a basis of0 + a1X + ···A[X+]a, since every polynomialnXn (with P(X) = 0 whenP(XP)(canX) is the null polynomial). Thus, A[X] is a free module.
 然而，当环A是一个场时，[X]是一个向量空间。但即使a只是以一种独特的方式写成，多项式族（p x（x k））=k∈nai也是0+a1x+·················································因此，一个[X]是一个自由模块。

Next, we want to define the notion of evaluating a polynomial P(X) at some α ∈ A. For this, we need a proposition.
 接下来，我们要定义在某个α∈a处计算多项式p（x）的概念，为此，我们需要一个命题。

Proposition 29.2. Let A,B be two rings and let h: A → B be a ring homomorphism. For any β ∈ B, there is a unique ring homomorphism ϕ: A[X] → B extending h such that ϕ(X) = β, as in the following diagram (where we denote by h+β the map h+β: A∪{X} → B such that (h + β)(a) = h(a) for all a ∈ A and (h + β)(X) = β):
 提案29.2.让a，b是两个环，让h:a→b是一个环同态。对于任何β∈b，都有一个唯一的环同态：a[x]→b延伸h，使得（x）=β，如下图所示（其中我们用h+β表示图h+β：a x→b，这样（h+β）（a）=h（a）表示所有a∈a和（h+β）（x）=β）：

​                                                                      A ∪ {X}      ι   / A[X]
 A X/A[X]

LLLLLLLLLL%       ϕ h+β
 llllllllll%h+β

B
 乙

Proof. Let ϕ(0) = 0, and for every nonull polynomial P(X) = a0 + a1X + ··· + anXn, let
 证据。设_（0）=0，对于每个非满多项式p（x）=a0+a1x+····+anxn，设

ϕ(P(X)) = h(a0) + h(a1)β + ··· + h(an)βn.
 ⑨（P（x））=H（a0）+H（a1）β+·····+H（an）βn.

It is easily verified that ϕ is the unique homomorphism ϕ: A[X] → B extending h such that ϕ(X) = β.       
 很容易证实，_是唯一的同态_：a[x]→b延伸h，使得_（x）=β。

Taking A = B in Proposition 29.2 and h: A → A the identity, for every β ∈ A, there is a unique homomorphism ϕβ : A[X] → A such that ϕβ(X) = β, and for every polynomial P(X), we write ϕβ(P(X)) as P(β) and we call P(β) the value of P(X) at X = β. Thus, we can define a function PA : A → A such that PA(β) = P(β), for all β ∈ A. This function is called the polynomial function induced by P.
 以29.2和h:a→a的恒等式中的a=b为例，对于每一个β∈a，都有一个唯一的同态，即，对于每一个多项式p（x），我们把_β（p（x））写为p（β），我们把p（β）称为p（x）在x=β时的值。因此，我们可以定义一个函数p a:a→a，使得pa（β）=p（β），对于所有的β∈a，这个函数称为p诱导的多项式函数。

More generally, PB can be defined for any (commutative) ring B such that A ⊆ B. In general, it is possible that PA = QA for distinct polynomials P,Q. We will see shortly conditions for which the map P 7→ PA is injective. In particular, this is true for A = R (in general, any infinite integral domain). We now define polynomials in n variables.
 更一般地说，p b可以定义为任何（交换）环b，这样a b。一般来说，对于不同的多项式p，q，pa=qa是可能的。我们将很快看到map p 7→pa是内射的条件。特别是，对于a=r（一般来说，任何无穷大的积分域），这是正确的。我们现在定义n个变量的多项式。

Definition 29.3. Given n ≥ 1 and a ring A, the set PA(n) of polynomials over A in n variables is the set of functions P : N(n) → A such that P(k1,...,kn) = 06 for finitely many (k1,...,kn) ∈ N(n). The polynomial such that P(k1,...,kn) = 0 for all (k1,...,kn) is the null (or zero) polynomial and it is denoted by 0. We define addition of polynomials, multiplication by a scalar, and multiplication of polynomials, as follows: Given any three polynomials P,Q,R ∈ PA(n), letting a(k1,...,kn) = P(k1,...,kn), b(k1,...,kn) = Q(k1,...,kn), c(k1,...,kn) = R(k1,...,kn), for every (k1,...,kn) ∈ N(n), we define R = P + Q such that
 定义29.3.给定n≥1和环a，n个变量上多项式的集合pa（n）是函数p:n（n）→a这样，p（k1，…，kn）=06表示有限多（k1，…，kn）∈n（n）。所有（k1，…，kn）的p（k1，…，kn）=0的多项式是零（或零）多项式，用0表示。我们定义了多项式的加法、标量乘法和多项式的乘法，如下：给定任意三个多项式p，q，r∈p a（n），让a（k1，…，kn）=p（k1，…，kn），b（k1，…，kn）=q（k1，…，kn），c（k1，…，kn）=r（k1，…，kn），对于每（k1，…，kn）∈n（n），我们定义r=p。+问题是这样的

c(k1,...,kn) = a(k1,...,kn) + b(k1,...,kn),
 c（k1，…，kn）=a（k1，…，kn）+b（k1，…，kn）

R = λP, where λ ∈ A, such that
 r=λp，其中λ∈a，这样

c(k1,...,kn) = λa(k1,...,kn),
 c（k1，…，kn）=λa（k1，…，kn）

and R = PQ, such that
 R=PQ，这样

​                                         c(k1,...,kn) =                  X                 a(i1,...,in)b(j1,...,jn).
 c（k1，…，kn）=x a（i1，…，in）b（j1，…，jn）。

(i1,...,in)+(j1,...,jn)=(k1,...,kn)
 （i1，…，in）+（j1，…，jn）=（k1，…，kn）

For every (k1,...,kn) ∈ N(n), we let e(k1,...,kn) be the polynomial such that
 对于每一（k1，…，kn）∈n（n），我们让e（k1，…，kn）是多项式，这样

​                                      e(k1,...,kn)(k1,...,kn) = 1    and     e(k1,...,kn)(h1,...,hn) = 0,
 e（k1，…，kn）（k1，…，kn）=1，e（k1，…，kn）（h1，…，hn）=0，

for (h1,...,hn) = (6 k1,...,kn). We also denote e(0,...,0) by 1. Given a polynomial P, the a(k1,...,kn) = P(k1,...,kn) ∈ A, are called the coefficients of P. If P is not the null polynomial, there is a greatest d ≥ 0 such that a(k1,...,kn) = 06 for some (k1,...,kn) ∈ N(n), with d = k1 + ··· + kn, called the total degree of P and denoted by deg(P). Then, P is written uniquely as
 对于（h1，…，hn）=（6 k1，…，kn）。我们也用1表示e（0，…，0）。给定一个多项式p，a（k1，…，kn）=p（k1，…，kn）∈a，称为p的系数，如果p不是零多项式，则有一个最大d≥0，使得a（k1，…，kn）=06对于某些（k1，…，kn）∈n（n），d=k1+········+kn，称为p的总次数，用deg（p）表示。然后，p被唯一地写为

P = X a(k1,...,kn)e(k1,...,kn).
 P=x a（k1，…，kn）e（k1，…，kn）。

(k1,...,kn)∈N(n)
 （k1，…，kn）∈n（n）

When P is the null polynomial, we let deg(P) = −∞.
 当p是零多项式时，我们让deg（p）=-∞。

There is an injection of A into PA(n) given by the map a 7→ a1 (where 1 denotes e(0,...,0)). There is also an injection of N(n) into PA(n) given by the map (h1,...,hn) 7→ e(h1,...,hn). Note that e(h1,...,hn)e(k1,...,kn) = e(h1+k1,...,hn+kn). In order to alleviate the notation, let X1,...,Xn be n distinct variables and denote e(0,...,0,1,0...,0), where 1 occurs in the position i, by Xi (where 1 ≤ i ≤ n). With this convention, in view of e(h1,...,hn)e(k1,...,kn) = e(h1+k1,...,hn+kn), the polynomial e(k1,...,kn) is denoted by (with = 1) and it is called
 图A 7→A1（其中1表示e（0，…，0））给出了a注入到pa（n）中。图（h1，…，hn）7→e（h1，…，hn）给出的PA（n）中也注入了n（n）。注意e（h1，…，hn）e（k1，…，kn）=e（h1+k1，…，hn+kn）。为了减轻符号，让X1，…，Xn是n个不同的变量，并表示E（0，…，0，1,0…，0），其中1出现在位置I，由Xi（其中1个i i小于n）。根据这个惯例，考虑到e（h1，…，hn）e（k1，…，kn）=e（h1+k1，…，hn+kn），多项式e（k1，…，kn）用（with=1）表示，称为

a primitive monomial. Then, P is also written as
 原始的单项式。那么，p也写为

.
 .

We also denote PA(n) by A[X1,...,Xn]. A polynomial P ∈ A[X1,...,Xn] is also denoted by P(X1,...,Xn).
 我们也用[x1，…，xn]表示pa（n）。多项式p∈a[x1，…，xn]也用p（x1，…，xn）表示。

As in the case n = 1, there is nothing special about the choice of X1,...,Xn as variables (or indeterminates). It is just a convenience. After all, the construction of PA(n) has nothing to do with X1,...,Xn.
 在n=1的情况下，选择x1，…，xn作为变量（或不确定）没有什么特别的。这只是一种方便。毕竟，PA（n）的构造与x1，…，xn无关。

Given a nonnull polynomial P of degree d, the nonnull coefficients a(k1,...,kn) = 06 such that d = k1 + ··· + kn are called the leading coefficients of P. A polynomial of the form
 给定d次的非零多项式p，非零系数a（k1，…，kn）=06，使d=k1+·····+kn称为p的前导系数。该形式的多项式

is called a monomial. Note that deg(.
 称为单项式。注意度数（.

Given a polynomial
 给定多项式

P = X a(k1,...,kn)X1k1 ···Xnkn,
 P=x a（k1，…，kn）x1k1···xnkn，

(k1,...,kn)∈N(n)
 （k1，…，kn）∈n（n）

a monomial occurs in the polynomial P if a(k1,...,kn) = 0.6
 如果a（k1，…，kn）=0.6，多项式p中会出现一个单项式。

A polynomial
 多项式

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

is homogeneous of degree d if deg(
 D度均匀度（

for every monomialoccurring in P. If P is a polynomial of total degree d, it is clear that P can be written uniquely as
 对于p中的每一个单项式，如果p是总次数d的多项式，很明显p可以唯一地写成

P = P(0) + P(1) + ··· + P(d),
 P=P（0）+P（1）+····+P（d）、

where P(i) is the sum of all monomials of degree i occurring in P, where 0 ≤ i ≤ d.
 式中，p（i）是p中出现的所有i级单项式的总和，其中0≤i≤d。

It is easily verified that A[X1,...,Xn] is a commutative ring, with multiplicative identity
 很容易证明[x1，…，xn]是一个交换环，具有乘法恒等式。

= 1. It is also easily verified that A[X] is a module. When A is a field, A[X] is
 = 1。也很容易验证[X]是一个模块。当a是一个字段时，a[x]是

a vector space.
 向量空间。

Even when A is just a ring, the family of polynomials
 即使a只是一个环，多项式家族

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

is a basis of A[X1,...,Xn], since every polynomial P(X1,...,Xn) can be written in a unique way as
 是一个[x1，…，xn]的基础，因为每个多项式p（x1，…，xn）都可以用一种独特的方式写为

.
 .

Thus, A[X1,...,Xn] is a free module.
 因此，[x1，…，xn]是一个自由模块。

Remark: The construction of Definition 29.3 can be immediately extended to an arbitrary set I, and not just I = {1,...,n}. It can also be applied to monoids more general that N(I). Proposition 29.2 is generalized as follows.
 注：定义29.3的构造可以立即扩展到任意集i，而不仅仅是i=1，…，n。它也可以应用于比n（i）更一般的单倍体。命题29.2概括如下。

Proposition 29.3. Let A,B be two rings and let h: A → B be a ring homomorphism. For any β = (β1,...,βn) ∈ Bn, there is a unique ring homomorphism ϕ: A[X1,...,Xn] → B extending h such that ϕ(Xi) = βi, 1 ≤ i ≤ n, as in the following diagram (where we denote by h + β the map h + β: A ∪ {X1,...,Xn} → B such that (h + β)(a) = h(a) for all a ∈ A and (h + β)(Xi) = βi, 1 ≤ i ≤ n):
 提案29.3.让a，b是两个环，让h:a→b是一个环同态。对于任何β=（β1，…，βn）BN，存在一个唯一的环同态，即：[x1，…，Xn ] -b扩展h，使得（Xi）＝βi，1±i，n，如下面的图（其中H+β表示图H+β：α{x1，…，xn}）b，使得（a +）（h）＝h（a），对于所有αa和（H+β）（x）（x）i）=βi，1≤i≤n）：

​                                                         A ∪ {X1,...,Xn}        ι      / A[X1,...,Xn]
 a x1，…，xn/a[x1，…，xn]

TTTTTTTTTTTTTTTTT) Bϕ h+β
 ttttttttttttttttt）b_h+β

Proof. Let ϕ(0) = 0, and for every nonull polynomial
 证据。设_（0）=0，对于每个非满多项式

,
 ，

let
 让

.
 .

It is easily verified that ϕ is the unique homomorphism ϕ: A[X1,...,Xn] → B extending h such that ϕ(Xi) = βi.       
 很容易证明，Xn是唯一的同态：A[x1，…，Xn ] -B扩展H，使得（Xi）＝βI。

Taking A = B in Proposition 29.3 and h: A → A the identity, for every β1,...,βn ∈ A, there is a unique homomorphism ϕ: A[X1,...,Xn] → A such that ϕ(Xi) = βi, and for every polynomial P(X1,...,Xn), we write ϕ(P(X1,...,Xn)) as P(β1,...,βn) and we call P(β1,...,βn) the value of P(X1,...,Xn) at X1 = β1,...,Xn = βn. Thus, we can define a function PA : An → A such that PA(β1,...,βn) = P(β1,...,βn), for all β1,...,βn ∈ A. This function is called the polynomial function induced by P.
 取命题29.3中的a= b和h：a，a，β，n，β，n，有一个唯一的同态，即[x1，…，Xn ]：a，（x），βi，对于每个多项式p（x1，…，xn），我们将p（x1，…，Xn）写为p（β1，…，βn），我们称p（β1，…，βn）p（x1，…）的值。，xn）在x1=β1，…，xn=βn。因此，我们可以定义一个函数p a:an→a，使得pa（β1，…，βn）=p（β1，…，βn），对于所有β1，…，βn∈a。这个函数称为p诱导的多项式函数。

More generally, PB can be defined for any (commutative) ring B such that A ⊆ B. As in the case of a single variable, it is possible that PA = QA for distinct polynomials P,Q. We will see shortly that the map P →7 PA is injective when A = R (in general, any infinite integral domain).
 更一般地说，p b可以定义为任何（交换）环b，这样a b。在单变量的情况下，对于不同的多项式p，q，pa=qa是可能的。我们很快就会看到，当a=r时，map p→7pa是内射的（一般来说，任何无限积分域）。

Given any nonnull polynomial  in
 给定任意非空多项式

A[X1,...,Xn], where n ≥ 2, P(X1,...,Xn) can be uniquely written as
 a[x1，…，xn]，其中n≥2，p（x1，…，xn）可以唯一地写为

,
 ，

where each polynomial Qkn(X1,...,Xn−1) is in A[X1,...,Xn−1]. Even if A is a field, A[X1,...,Xn−1] is not a field, which confirms that it is useful (and necessary!) to consider polynomials over rings that are not necessarily fields.
 其中，每个多项式qkn（x1，…，xn−1）位于[x1，…，xn−1]中。即使a是一个字段，a[x1，…，xn−1]也不是一个字段，这证实了它是有用的（也是必要的！）考虑不一定是场的环上的多项式。

It is not difficult to show that A[X1,...,Xn] and A[X1,...,Xn−1][Xn] are isomorphic rings. This way, it is often possible to prove properties of polynomials in several variables X1,...,Xn, by induction on the number n of variables. For example, given two nonnull polynomials P(X1,...,Xn) of total degree p and Q(X1,...,Xn) of total degree q, since we assumed that A is an integral domain, we can prove that
 不难证明[x1，…，xn]和[x1，…，xn−1][xn]是同构环。这样，通过对变量数n的归纳，通常可以证明多个变量x1，…，xn中多项式的性质。例如，假设总度数p的两个非空多项式p（x1，…，xn）和总度数q的q（x1，…，xn），因为我们假设a是一个积分域，我们可以证明

deg(PQ) = deg(P) + deg(Q),
 度（PQ）=deg（P）+deg（Q）

and that A[X1,...,Xn] is an integral domain.
 而[x1，…，xn]是一个积分域。

Next, we will consider the division of polynomials (in one variable).
 接下来，我们将考虑多项式的除法（在一个变量中）。

##       29.3         Euclidean Division of Polynomials  29.3欧氏多项式划分

We know that every natural number n ≥ 2 can be written uniquely as a product of powers of prime numbers and that prime numbers play a very important role in arithmetic. It would be nice if every polynomial could be expressed (uniquely) as a product of “irreducible” factors. This is indeed the case for polynomials over a field. The fact that there is a division algorithm for the natural numbers is essential for obtaining many of the arithmetical properties of the natural numbers. As we shall see next, there is also a division algorithm for polynomials in A[X], when A is a field.
 我们知道每一个自然数n≥2都可以作为素数幂的乘积唯一地写，素数在算术中起着非常重要的作用。如果每一个多项式都可以（唯一地）表示为“不可约”因子的乘积，那就太好了。这确实是一个领域的多项式的情况。自然数有一个除法，这一事实对于获得自然数的许多算术性质是至关重要的。正如我们接下来将看到的，当a是一个场时，a[x]中还有一个多项式的除法。

Proposition 29.4. Let A be a ring, let f(X),g(X) ∈ A[X] be two polynomials of degree m = deg(f) and n = deg(g) with f(X) 6= 0 , and assume that the leading coefficient am of f(X) is invertible. Then, there exist unique polynomials q(X) and r(X) in A[X] such that
 提案29.4.设a为环，设f（x），g（x）∈a[x]为m=deg（f）和n=deg（g）的两个多项式，f（x）6=0，并假定f（x）的导系数am是可逆的。然后，在a[x]中存在唯一的多项式q（x）和r（x），这样

​                                                    g = fq + r     and      deg(r) < deg(f) = m.
 G=FQ+R和deg（R）<deg（F）=m。

Proof. We first prove the existence of q and r. Let
 证据。我们首先证明q和r的存在。

f = amXm + am−1Xm−1 + ··· + a0,
 f=amxm+am−1xm−1+····+a0，

and g = bnXn + bn−1Xn−1 + ··· + b0.
 g=bnxn+bn−1xn−1+····+b0。

If n < m, then let q = 0 and r = g. Since deg(g) < deg(f) and r = g, we have deg(r) < deg(f).
 如果n<m，则q=0，r=g。由于deg（g）<deg（f）和r=g，我们得到deg（r）<deg（f）。


 

29.3. EUCLIDEAN DIVISION OF POLYNOMIALS
 29.3。欧氏多项式划分

If n ≥ m, we proceed by induction on n. If n = 0, then g = b0, m = 0, f = a0 6= 0 , and we let q = a−0 1b0 and r = 0. Since deg(r) = deg(0) = −∞ and deg(f) = deg(a0) = 0 because a0 = 06 , we have deg(r) < deg(f).
 如果n≥m，我们在n上进行诱导。如果n=0，那么g=b0，m=0，f=a0 6=0，我们让q=a−0 1b0和r=0。因为deg（r）=deg（0）=-∞和deg（f）=deg（a0）=0，因为a0=06，我们得到deg（r）<deg（f）。

If n ≥ 1, since n ≥ m, note that
 如果n≥1，因为n≥m，注意

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

is a polynomial of degree deg(g1) < n, since the terms bnXn and bnam−1Xn−mamXm of degree n cancel out. Now, since deg(g1) < n, by the induction hypothesis, we can find q1 and r such that g1 = fq1 + r and deg(r) < deg(f) = m,
 是degree deg（g1）<n的多项式，因为degree n的术语bnxn和bnam−1xn−mamxm取消。现在，由于deg（g1）<n，根据诱导假设，我们可以找到q1和r，使得g1=fq1+r和deg（r）<deg（f）=m，

and thus,
 因此，

g1(X) = g(X) − bna−m1Xn−mf(X) = f(X)q1(X) + r(X),
 g1（x）=g（x）−bna−m1xn−mf（x）=f（x）q1（x）+r（x），

from which, letting ), we get
 我们从中得到

​                                                    g = fq + r     and      deg(r) < m = deg(f).
 G=FQ+R和deg（R）<M=deg（F）。

We now prove uniqueness. If
 我们现在证明了它的独特性。如果

g = fq1 + r1 = fq2 + r2,
 g=fq1+r1=fq2+r2，

with deg(r1) < deg(f) and deg(r2) < deg(f), we get
 当deg（r1）<deg（f）和deg（r2）<deg（f）时，我们得到

f(q1 − q2) = r2 − r1.
 F（q1−q2）=r2−r1。

​       If q2 −q1 = 06 , since the leading coefficient am of f is invertible, by Proposition 29.1, we have
 如果q2−q1=06，因为f的超前系数am是可逆的，根据命题29.1，我们得到

deg(r2 − r1) = deg(f(q1 − q2)) = deg(f) + deg(q2 − q1),
 度（r2−r1）=deg（f（q1−q2））=deg（f）+deg（q2−q1），

and so, deg(r2−r1) ≥ deg(f), which contradicts the fact that deg(r1) < deg(f) and deg(r2) < deg(f). Thus, q1 = q2, and then also r1 = r2. 
 因此，deg（r2−r1）≥deg（f），这与deg（r1）<deg（f）和deg（r2）<deg（f）的事实相矛盾。因此，q1=q2，然后r1=r2。

It should be noted that the proof of Proposition 29.4 actually provides an algorithm for finding the quotient q and the remainder r of the division of g by f. This algorithm is called the Euclidean algorithm, or division algorithm. Note that the division of g by f is always possible when f is a monic polynomial, since 1 is invertible. Also, when A is a field, am = 06 is always invertible, and thus, the division can always be performed. We say that f divides g when r = 0 in the result of the division g = fq + r. We now draw some important consequences of the existence of the Euclidean algorithm.
 需要指出的是，29.4命题的证明实际上提供了一种求g除以f的商q和余数r的算法。这种算法被称为欧几里得算法或除法。注意，当f是Monic多项式时，g除以f总是可能的，因为1是可逆的。此外，当a是一个字段时，am=06总是可逆的，因此，可以始终执行除法。我们认为，当R=0时，F在G=FQ+R的除法结果中对G进行除法，得出了欧几里得算法存在的一些重要结果。

##       29.4           Ideals, PID’s, and Greatest Common Divisors  29.4理想、PID和最大公约数

First, we introduce the fundamental concept of an ideal.
 首先，我们介绍理想的基本概念。

Definition 29.4. Given a ring A, an ideal of A is any nonempty subset I of A satisfying the following two properties:
 定义29.4.给定环A，A的理想是满足以下两个性质的A的任何非空子集I：

(ID1) If a,b ∈ I, then b − a ∈ I.
 （id1）如果a，b∈i，则b−a∈i。

(ID2) If a ∈ I, then ax ∈ I for every x ∈ A.
 （id2）如果a∈i，则每x∈a的ax∈i。

An ideal I is a principal ideal if there is some a ∈ I, called a generator, such that
 一个理想i是一个主理想，如果有一个∈i，称为发生器，这样

I = {ax | x ∈ A}.
 i=a x x∈a。

​                      The equality I = {ax | x ∈ A} is also written as I = aA or as I = (a).                   The ideal
 等式i=a x x∈a也写为i=a a或i=（a）。

I = (0) = {0} is called the null ideal (or zero ideal).
 i=（0）=0称为零理想（或零理想）。

An idealEquivalently,In other words,An idealI is aIIis ais a prime ideal ifAprime ideal−maximal idealI is closed under multiplication and 1if I =6 Iif=6AIA=6and ifand ifA and for every idealaba,b∈ ∈I, thenA−I, thena∈∈AJI−ab =6orI.A∈b, ifA∈−III, for all⊆, for allJ, thena,ba,bJ∈∈=AAI...
 一个理想，换句话说，理想是一个基本理想，如果一个理想−最大理想在乘法下闭合，并且1if i=6 iif=6a i a=6和ifand ifa，对于每一个理想，b−i，thena∈aji−ab=6ori，a∈b，ifa−iii，对于所有，对于allj，thena，ba，bj∈∈=AAI…

Note that if I is an ideal, then I = A iff 1 ∈ I. Since by definition, an ideal I is nonempty, there is some a ∈ I, and by (ID1) we get 0 = a − a ∈ I. Then, for every a ∈ I, since 0 ∈ I, by (ID1) we get −a ∈ I. Thus, an ideal is an additive subgroup of A. Because of (ID2), an ideal is also a subring.
 注意，如果我是一个理想，那么i=a iff 1∈i。因为根据定义，一个理想i是非空的，有一些a∈i，通过（id1）我们得到0=a−a∈i。然后，对于每一个a∈i，由于0∈i，通过（id1）我们得到−a∈i。因此，理想是a的加性子群。因为（id2），一个理想也是一个子环。

Observe that if A is a field, then A only has two ideals, namely, the trivial ideal (0) and A itself. Indeed, if I 6= (0), because every nonnull element has an inverse, then 1 ∈ I, and thus, I = A.
 如果A是一个场，那么A只有两个理想，即平凡理想（0）和A本身。实际上，如果i 6=（0），因为每个非空元素都有一个逆元素，那么1∈i，因此i=a。

Definition 29.5.of a and that a dividesGiven a ringb if b = acA, for any two elementsfor some c ∈ A; this is usually denoted bya,b ∈ A we say thatab|is a multipleb.
 a的定义29.5.如果b=aca，则a分格在a环b中，对于某些c∈a的任何两个元素，这通常表示为a，b∈a，我们称ab是一个倍数b。

Note that the principal ideal (a) is the set of all multiples of a, and that a divides b iff b is a multiple of a iff b ∈ (a) iff (b) ⊆ (a).
 注意，主理想（a）是a的所有倍数的集合，并且a除以b iff b是iff b∈（a）iff（b）（a）的倍数。

iff acNote that every= 0 for someac∈= 06 A . With this convention, 0 is a zero divisor unlessdivides 0. However, it is customary to say that a is aA zero divisor= {0} (the trivial ring), and A is an integral domain iff 0 is the only zero divisor in A.
 iff ac注意，someac的每=0∈=06a。按照这个约定，0是零除数，除非除数是0。然而，习惯上说a是aa零除数=0（平凡环），a是积分域，iff 0是a中唯一的零除数。

Given a,b ∈ A with a,b 6= 0, if (a) = (b) then there exist c,d ∈ A such that a = bc and is an integral domain, we getb = ad. From this, we get a =dcadc= 1andandb =cdbcd= 1, that is,, that is,a(1c is invertible with inverse−dc) = 0 and b(1−cd) = 0d. Thus,. If A when A is an integral domain, we have b = ad, with d invertible. The converse is obvious, if b = ad with d invertible, then (a) = (b).
 给定a，b∈a与a，b 6=0，如果（a）=（b），则存在c，d∈a，使a=bc且是一个积分域，我们得到b=ad。由此，我们得到a=dcadc=1 anddb=cdbcd=1，即a（1c是可逆的，逆−dc）=0，b（1−cd）=0d。因此，…如果A是一个积分域，我们有b=a d，d是可逆的。反之很明显，如果b=a d，d可逆，则（a）=（b）。

It is worth recording this fact as the following proposition.
 这一事实值得记录为以下命题。

Proposition 29.5. If A is an integral domain, for any a,b ∈ A with a,b = 06 , we have (a) = (b) iff there exists some invertible d ∈ A such that b = ad.
 提案29.5。如果a是一个积分域，对于任意a，b∈a，b=06，我们得到（a）=（b）如果存在一些可逆d∈a，那么b=ad。

An invertible element u ∈ A is also called a unit. Given two ideals I and J, their sum
 可逆元素u∈a也称为单位。给定两个理想i和j，它们的和

I + J = {a + b | a ∈ I, b ∈ J}
 i+j=a+b a∈i，b∈j

is clearly an ideal. Given any nonempty subset J of A, the set
 显然是个理想。给定a的任何非空子集j，集合

{a1x1 + ··· + anxn | x1,...,xn ∈ A, a1,...,an ∈ J, n ≥ 1}
 a1 x1+······+a n xn x1，…，xn∈a，a1，…，a n∈j，n≥1

is easily seen to be an ideal, and in fact, it is the smallest ideal containing J. It is usually denoted by (J).
 很容易被认为是理想，事实上，它是包含j的最小理想，通常用（j）表示。

Ideals play a very important role in the study of rings. They tend to show up everywhere. For example, they arise naturally from homomorphisms.
 理想在环的研究中起着非常重要的作用。他们经常出现在任何地方。例如，它们自然地产生于同态。

Proposition 29.6. Given any ring homomorphism h: A → B, the kernel Kerh = {a ∈ A | h(a) = 0} of h is an ideal.
 提案29.6.在任意环同态h:a→b下，h的核kerh=a∈a h（a）=0是一个理想。

Proof. Given a,b ∈ A, we have a,b ∈ Kerh iff h(a) = h(b) = 0, and since h is a homomorphism, we get
 证据。给定a，b∈a，我们有a，b∈kerh iff h（a）=h（b）=0，由于h是同态，我们得到

h(b − a) = h(b) − h(a) = 0,
 h（b−a）=h（b）−h（a）=0，

and h(ax) = h(a)h(x) = 0
 h（a x）=h（a）h（x）=0

​          for all x ∈ A, which shows that Kerh is an ideal.                                                                           
 对于所有的x∈a，这表明kerh是一个理想。

There is a sort of converse property. Given a ring A and an ideal I ⊆ A, we can define the quotient ring A/I, and there is a surjective homomorphism π: A → A/I whose kernel is precisely I.
 有一种逆向性质。给定一个环A和一个理想的I A，我们可以定义商环A/I，并且有一个同态π：A→A/I，它的核正好是I。

Proposition 29.7. Given any ring A and any ideal I ⊆ A, the equivalence relation ≡I defined by a ≡I b iff b − a ∈ I is a congruence, which means that if a1 ≡I b1 and a2 ≡I b2, then
 提案29.7。对于任何环A和任何理想i a，由a i b iff b−a∈i定义的等价关系i是一个同余，这意味着如果a1 i b1和a2 i b2，那么

*1.*    a1 + a2 ≡I b1 + b2, and
 A1+A2 I B1+B2，以及

*2.*    a1a2 ≡I b1b2.
 A1A2 I B1B2。

Then, the set A/I of equivalence classes modulo I is a ring under the operations
 那么，等价类模I的集合A/I就是操作下的一个环

​                                                                     [a] + [b]   =    [a + b]
 [A]+[B]=[A+B]

​                                                                          [a][b]   =   [ab].
 [A][B]=[AB]。

The map π: A → A/I such that π(a) = [a] is a surjective homomorphism whose kernel is precisely I.
 图π：a→a/i使得π（a）=[a]是一个主观性同态，它的核正好是i。

Proof. Everything is straightforward. For example, if a1 ≡I b1 and a2 ≡I b2, then b1 −a1 ∈ I and b2 − a2 ∈ I. Since I is an ideal, we get
 证据。一切都很简单。例如，如果a1 i b1和a2 i b2，那么b1 a1∈i和b2−a2∈i，因为i是一个理想，我们得到

(b1 − a1)b2 = b1b2 − a1b2 ∈ I
 （b1−a1）b2=b1b2−a1b2∈i

and
 和

(b2 − a2)a1 = a1b2 − a1a2 ∈ I.
 （b2−a2）a1=a1b2−a1a2∈i。

Since I is an ideal, and thus, an additive group, we get
 因为我是一个理想，因此是一个加性群，我们得到

b1b2 − a1a2 ∈ I,
 b1b2−a1a2∈i，

​          i.e., a1a2 ≡I b1b2. The equality Kerπ = I holds because I is an ideal.                                        
 即A1A2 I B1B2。等式kπ=我持有，因为我是一个理想。

Example 29.1.
 例29.1。

\1.    In the ring Z, for every p ∈ Z, the subroup pZ is an ideal, and Z/pZ is a ring, the ring of residues modulo p. This ring is a field iff p is a prime number.
 在环Z中，对于每一个p∈z，子上的pz是一个理想的，z/pz是一个环，剩余模的环p。这个环是一个域iff p是一个素数。

\2.    The quotient of the polynomial ring R[X] by a prime ideal I is an integral domain.
 素理想i对多项式环r[x]的商是一个积分域。

\3.    The quotient of the polynomial ring R[X] by a maximal ideal I is a field. For example, if I = (X2 + 1), the principal ideal generated by X2 + 1 (which is indeed a maximal ideal since X2 + 1 has no real roots), then R[X]/(X2 + 1) ∼= C.
 多项式环r[x]被最大理想i的商是一个场。例如，如果i=（x2+1），由x2+1生成的主理想（由于x2+1没有实根，因此实际上是最大理想），则r[x]/（x2+1）=c。

The following proposition yields a characterization of prime ideals and maximal ideals in terms of quotients.
 下面的命题用商来描述素理想和最大理想。

Proposition 29.8. Given a ring A, for any ideal I ⊆ A, the following properties hold.
 提案29.8。对于任何理想i a，给定一个环a，以下属性保持不变。

*(1)*    The ideal I is a prime ideal iff A/I is an integral domain.
 理想i是一个素理想，如果a/i是一个积分域。

*(2)*    The ideal I is a maximal ideal iff A/I is a field.
 理想i是最大理想iff a/i是一个场。

Proof. (1) Assume that I is a prime ideal. Since I is prime, I =6 A, and thus, A/I is not the trivial ring (0). If [a][b] = 0, since [a][b] = [ab], we have ab ∈ I, and since I is prime, then either a ∈ I or b ∈ I, so that either [a] = 0 or [b] = 0. Thus, A/I is an integral domain.
 证据。（1）假设我是一个基本理想。因为i是素数，i=6a，因此a/i不是平凡的环（0）。如果[a][b]=0，因为[a][b]=ab]，我们有ab∈i，并且因为i是素数，那么a∈i或b∈i，所以[a]=0或[b]=0。因此，A/I是一个积分域。

Conversely, assume that A/I is an integral domain. Since A/I is not the trivial ring, I =6 A. Assume that ab ∈ I. Then, we have
 相反，假设a/i是一个积分域。既然a/i不是平凡环，i=6a，假设ab∈i，那么

π(ab) = π(a)π(b) = 0,
 π（a b）=π（a）π（b）=0，

which implies that either π(a) = 0 or π(b) = 0, since A/I is an integral domain (where π: A → A/I is the quotient map). Thus, either a ∈ I or b ∈ I, and I is a prime ideal.
 这意味着π（a）=0或π（b）=0，因为a/i是一个积分域（其中π：a→a/i是商映射）。因此，无论是a∈i还是b∈i，我都是素理想。

(2) Assume that I is a maximal ideal. As in (1), A/I is not the trivial ring (0). Let [a] = 06 in A/I. We need to prove that [a] has a multiplicative inverse. Since [a] = 06 , we have a /∈ I. Let Ia be the ideal generated by I and a. We have
 （2）假设我是最大理想。如（1）所示，A/I不是普通环（0）。假设A/I中[A]=06，我们需要证明[A]有一个乘法逆。从[a]=06开始，我们有一个/∈i。让ia是i和a产生的理想。我们有

​                                                                    I ⊆ Ia       and I =6 Ia,
 i ia和i=6 ia，

since a /∈ I, and since I is maximal, this implies that
 既然a/∈i，既然i是极大的，这就意味着

Ia = A.
 IA=A。

However, we know that
 但是，我们知道

Ia = {ax + h | x ∈ A, h ∈ I},
 i a=a x+h x∈a，h∈i，

and thus, there is some x ∈ A so that
 因此，有一些x∈a，所以

ax + h = 1,
 ax+h=1，

which proves that [a][x] = [1], as desired.
 这证明了[a][x]=[1]，如所需。

Conversely, assume that A/I is a field. Again, since A/I is not the trivial ring, I =6 A. Let J be any proper ideal such that I ⊆ J, and assume that I =6 J. Thus, there is some j ∈ J − I, and since Kerπ = I, we have π(j) = 06 . Since A/I is a field and π is surjective, there is some k ∈ A so that π(j)π(k) = 1, which implies that
 相反，假设A/I是一个字段。再者，因为a/i不是平凡环，i=6a。让j是任何合适的理想，这样i j，假设i=6j。因此，有一些j∈j−i，由于kerπ=i，我们有π（j）=06。由于a/i是一个场，π是可射的，所以有一些k∈a，所以π（j）π（k）=1，这意味着

jk − 1 = i
 jk−1=i

for some i ∈ I, and since I ⊂ J and J is an ideal, it follows that 1 = jk − i ∈ J, showing that J = A, a contradiction. Therefore, I = J, and I is a maximal ideal. 
 对于某些i i，由于i j和j是一个理想，它遵循1=jk−i j，表明j=a是一个矛盾。因此，i=j，i是最大理想。

As a corollary, we obtain the following useful result. It emphasizes the importance of maximal ideals.
 作为推论，我们得到了以下有用的结果。它强调最大理想的重要性。

Corollary 29.9. Given any ring A, every maximal ideal I in A is a prime ideal.
 推论29.9。对于任何环A，A中的每个最大理想I都是素理想。

Proof. If I is a maximal ideal, then, by Proposition 29.8, the quotient ring A/I is a field. However, a field is an integral domain, and by Proposition 29.8 (again), I is a prime ideal. 
 证据。如果我是一个最大理想，那么，根据命题29.8，商环A/I是一个场。然而，场是一个积分域，根据命题29.8（再次），我是一个素理想。

Observe that a ring A is an integral domain iff (0) is a prime ideal. This is an example of a prime ideal which is not a maximal ideal, as immediately seen in A = Z, where (p) is a maximal ideal for every prime number p.
 观察环A是积分域iff（0）是素理想。这是素数理想的一个例子，它不是最大理想，如a=z所示，其中（p）是每个素数p的最大理想。

 A less obvious example of a prime ideal which is not a maximal ideal is the ideal (X) in the ring of polynomials Z[X]. Indeed, (X,2) is also a prime ideal, but (X) is properly contained in (X,2). The ideal (X) is the set of all polynomials of the form XQ(X) for any Q(X) ∈ Z[X], in other words the set of all polynomials in Z[X] with constant term equal to
 不是最大理想的素数理想的一个不太明显的例子是多项式Z[X]环中的理想（X）。实际上，（x，2）也是一个基本理想，但（x）正确地包含在（x，2）中。理想（x）是任何q（x）∈z[x]形式的所有多项式的集合，换句话说，z[x]形式的所有多项式的集合，常数项等于

0, and the ideal (X,2) is the set of all polynomials of the form
 理想（x，2）是形式的所有多项式的集合。

​                                                 XQ1(X) + 2Q2(X),         Q1(X),Q2(X) ∈ Z[X],
 x q1（x）+2q2（x），q1（x），q2（x）∈z[x]，

which is just the set of all polynomials in Z[X] whose constant term is of the form 2c for some c ∈ Z. The ideal (X) is indeed properly contained in the ideal (X,2). If P(X)Q(X) ∈ (X,2), let a be the constant term in P(X) and let b be the constant term in Q(X). Since P(X)Q(X) ∈ (X,2), we must have ab = 2c for some c ∈ Z, and since 2 is prime, either a is divisible by 2 or b is divisible by 2. It follows that either P(X) ∈ (X,2) or Q(X) ∈ (X,2), which shows that (X,2) is a prime ideal.
 它只是z[x]中所有多项式的集合，其常数项对于某些c∈z为2c形式。理想（x）确实正确地包含在理想（x，2）中。如果p（x）q（x）∈（x，2），设a为p（x）中的常数项，设b为q（x）中的常数项。由于p（x）q（x）∈（x，2），对于某些c∈z，我们必须有a b=2c，并且由于2是素数，a可以被2整除，或者b可以被2整除。由此得出p（x）∈（x，2）或q（x）∈（x，2），这表明（x，2）是一个素理想。

Definition 29.6. An integral domain in which every ideal is a principal ideal is called a principal ring or principal ideal domain, for short, a PID.
 定义29.6.每个理想都是主理想的积分域称为主环或主理想域，简称PID。

The ring Z is a PID. This is a consequence of the existence of a (Euclidean) division algorithm. As we shall see next, when K is a field, the ring K[X] is also a principal ring.
 Z环是PID。这是（欧几里得）除法存在的结果。接下来我们将看到，当k是一个场时，环k[x]也是一个主环。

 However, when n ≥ 2, the ring K[X1,...,Xn] is not principal. For example, in the ring
 但是，当n≥2时，环k[x1，…，xn]不是主体。例如，在环中

K[X,Y ], the ideal (X,Y ) generated by X and Y is not principal. First, since (X,Y ) is the set of all polynomials of the form Xq1 + Y q2, where q1,q2 ∈ K[X,Y ], except when Xq1 + Y q2 = 0, we have deg(Xq1 + Y q2) ≥ 1. Thus, 1 ∈/ (X,Y ). Now if there was some p ∈ K[X,Y ] such that (X,Y ) = (p), since 1 ∈/ (X,Y ), we must have deg(p) ≥ 1. But we would also have X = pq1 and Y = pq2, for some q1,q2 ∈ K[X,Y ]. Since deg(X) = deg(Y ) = 1, this is impossible.
 k[x，y]，x和y产生的理想（x，y）不是主体。首先，因为（x，y）是x q1+y q2形式的所有多项式的集合，其中q1，q2∈k[x，y]，除了xq1+y q2=0时，我们有deg（xq1+y q2）≥1。因此，1∈/（x，y）。如果有一些p∈k[x，y]这样（x，y）=（p），既然1∈/（x，y），我们必须有deg（p）≥1。但是我们也可以得到x=pq1和y=pq2，对于一些q1，q2∈k[x，y]。因为deg（x）=deg（y）=1，这是不可能的。

Even though K[X,Y ] is not a principal ring, a suitable version of unique factorization in terms of irreducible factors holds. The ring K[X,Y ] (and more generally K[X1,...,Xn]) is what is called a unique factorization domain, for short, UFD, or a factorial ring.
 即使k[x，y]不是主环，但不可约因子的唯一因式分解的一个合适版本仍然成立。环k[x，y]（通常是k[x1，…，xn]）被称为唯一的因式分解域，简称为ufd或因式分解环。

From this point until Definition 29.11, we consider polynomials in one variable over a field K.
 从这一点到29.11的定义，我们考虑一个变量在一个域k上的多项式。

Remark: Although we already proved part (1) of Proposition 29.10 in a more general situation above, we reprove it in the special case of polynomials. This may offend the purists, but most readers will probably not mind.
 注：虽然在上述更一般的情况下，我们已经证明了29.10命题的第（1）部分，但我们在多项式的特殊情况下对其进行了反驳。这可能会冒犯纯粹主义者，但大多数读者可能不会介意。

Proposition 29.10. Let K be a field. The following properties hold:
 提案29.10。让k成为一个场。以下属性保留：

*(1)*    For any two nonzero polynomials f,g ∈ K[X], (f) = (g) iff there is some λ = 06  in K such that g = λf.
 对于任意两个非零多项式f，g∈k[x]，（f）=（g）iff，k中有一些λ=06，使得g=λf。

*(2)*    For every nonnull ideal I in K[X], there is a unique monic polynomial f ∈ K[X] such that I = (f).
 对于k[x]中的每一个非零理想i，都有一个唯一的Monic多项式f∈k[x]，因此i=（f）。

Proof. (1) If (f) = (g), there are some nonzero polynomials q1,q2 ∈ K[X] such that g = fq1 and f = gq2. Thus, we have f = fq1q2, which implies f(1 − q1q2) = 0. Since K is a field, by Proposition 29.1, K[X] has no zero divisor, and since we assumed f = 06 , we must have q1q2 = 1. However, if either q1 or q2 is not a constant, by Proposition 29.1 again, deg(q1q2) = deg(q1) + deg(q2) ≥ 1, contradicting q1q2 = 1, since deg(1) = 0. Thus, both q1,q2 ∈ K −{0}, and (1) holds with λ = q1. In the other direction, it is obvious that g = λf implies that (f) = (g).
 证据。（1）如果（f）=（g），则存在一些非零多项式q1，q2∈k[x]，使得g=fq1，f=gq2。因此，我们有f=f q1q2，这意味着f（1−q1q2）=0。因为k是一个场，根据29.1，k[x]没有零除数，而且既然我们假设f=06，我们必须得到q1q2=1。然而，如果q1或q2不是一个常数，根据命题29.1，deg（q1q2）=deg（q1）+deg（q2）≥1，与q1q2=1矛盾，因为deg（1）=0。因此，q1，q2∈k−0，和（1）都与λ=q1保持一致。在另一个方向上，显然g=λf意味着（f）=（g）。

(2) Since we are assuming that I is not the null ideal, there is some polynomial of smallest degree in I, and since K is a field, by suitable multiplication by a scalar, we can make sure that this polynomial is monic. Thus, let f be a monic polynomial of smallest degree in I. By (ID2), it is clear that (f) ⊆ I. Now, let g ∈ I. Using the Euclidean algorithm, there exist unique q,r ∈ K[X] such that
 （2）因为我们假设i不是零理想，所以i中有一个最小度数的多项式，因为k是一个域，通过适当的乘一个标量，我们可以确定这个多项式是Monic。因此，设f为i中最小阶的Monic多项式，由（id2），很明显（f）i。现在，设g∈i。使用欧几里得算法，存在唯一的q，r∈k[x]，这样

​                                                         g = qf + r      and     deg(r) < deg(f).
 g=qf+r和deg（r）<deg（f）。

​        If r = 06  , there is some λ = 06             in K such that λr is a monic polynomial, and since λr =
 如果r=06，k中有一些λ=06，因此λr是Monic多项式，因为λr=

, with f,g ∈ I, by (ID1) and (ID2), we have λr ∈ I, where deg(λr) < deg(f) and is a monic polynomial, contradicting the minimality of the degree of f. Thus, r = 0, and
 ，对于f，g∈i，通过（id1）和（id2），我们得到了λr∈i，其中deg（λr）<deg（f），是一个Monic多项式，与f阶的极小性相矛盾。因此，r=0，和

​          g ∈ (f). The uniqueness of the monic polynomial f follows from (1).                                         
 G∈（F）。Monic多项式f的唯一性来自（1）。

Proposition 29.10 shows that K[X] is a principal ring when K is a field.
 命题29.10表明，当k是一个场时，k[x]是一个主环。

We now investigate the existence of a greatest common divisor (gcd) for two nonzero polynomials. Given any two nonzero polynomials f,g ∈ K[X], recall that f divides g if g = fq for some q ∈ K[X].
 我们现在研究两个非零多项式的最大公约数的存在性。对于任意两个非零多项式f，g∈k[x]，回想一下，如果g=f q，f对某些q∈k[x]除以g。

Definition 29.7. Given any two nonzero polynomials f,g ∈ K[X], a polynomial d ∈ K[X] is a greatest common divisor of f and g (for short, a gcd of f and g) if d divides f and g and whenever h ∈ K[X] divides f and g, then h divides d. We say that f and g are relatively prime if 1 is a gcd of f and g.
 定义29.7.对于任意两个非零多项式f，g∈k[x]，一个多项式d∈k[x]是f和g的最大公因数（简而言之，f和g的gcd），如果d除以f和g，当h∈k[x]除以f和g，则h除以d。如果1是f和g的gcd，则f和g是相对素数。

Note that f and g are relatively prime iff all of their gcd’s are constants (scalars in K), or equivalently, if f,g have no divisor q of degree deg(q) ≥ 1.
 注意，f和g是相对素数iff，它们的gcd都是常数（K中的标量），或者等价的，如果f，g没有deg（q）≥1的除数q。

 In particular, note that f and g are relatively prime when f is a nonzero constant polynomial (a scalar λ = 06 in K) and g is any nonzero polynomial.
 特别要注意，当f是非零常数多项式（k中的标量λ=06）且g是任何非零多项式时，f和g是相对素数。

We can characterize gcd’s of polynomials as follows.
 我们可以用下面的方法来描述多项式的gcd。

Proposition 29.11. Let K be a field and let f,g ∈ K[X] be any two nonzero polynomials. For every polynomial d ∈ K[X], the following properties are equivalent:
 提案29.11.设k为场，设f，g∈k[x]为任意两个非零多项式。对于每一个多项式d∈k[x]，下列性质是等价的：

*(1)*    The polynomial d is a gcd of f and g.
 多项式d是f和g的gcd。

*(2)*    The polynomial d divides f and g and there exist u,v ∈ K[X] such that
 多项式d除以f和g，并存在u，v∈k[x]，这样

*d*         = uf + vg.
 =uf+vg。

*(3)*    The ideals (f),(g), and (d) satisfy the equation
 理想（f）、（g）和（d）满足方程

*d*         = (f) + (g).
 =（f）+（g）。

​             In addition, d = 06  , and d is unique up to multiplication by a nonzero scalar in K.
 此外，d=06，d是唯一的，直到K中的非零标量相乘。

Proof. Given any two nonzero polynomials u,v ∈ K[X], observe that u divides v iff (v) ⊆ (u). Now, (2) can be restated as (f) ⊆ (d), (g) ⊆ (d), and d ∈ (f) + (g), which is equivalent to (d) = (f) + (g), namely (3).
 证据。给定任意两个非零多项式u，v∈k[x]，观察u除以v iff（v）（u）。现在，（2）可以重述为（f）（d）、（g）（d）和d∈（f）+（g），相当于（d）=（f）+（g），即（3）。

If (2) holds, since d = uf + vg, whenever h ∈ K[X] divides f and g, then h divides d, and d is a gcd of f and g.
 如果（2）成立，因为d=uf+vg，当h∈k[x]除以f和g时，h除以d，d是f和g的gcd。

Assume that d is a gcd of f and g. Then, since d divides f and d divides g, we have (f) ⊆ (d) and (g) ⊆ (d), and thus (f) + (g) ⊆ (d), and (f) + (g) is nonempty since f and g are nonzero. By Proposition 29.10, there exists a monic polynomial d1 ∈ K[X] such that (d1) = (f) + (g). Then, d1 divides both f and g, and since d is a gcd of f and g, then d1 divides d, which shows that (d) ⊆ (d1) = (f) + (g). Consequently, (f) + (g) = (d), and (3) holds.
 假设d是f和g的gcd，因为d除以f和d除以g，我们得到（f）（d）和（g）（d），因此（f）+（g）（d）和（f）+（g）是非空的，因为f和g是非零的。根据29.10，存在一个Monic多项式d1∈k[x]，使得（d1）=（f）+（g）。然后，d1将f和g分开，因为d是f和g的gcd，所以d1将d分开，这表明（d）（d1）=（f）+（g）。因此，（f）+（g）=（d）和（3）成立。

Since (d) = (f) + (g) and f and g are nonzero, the last part of the proposition is obvious.  
 因为（d）=（f）+（g）和f和g是非零的，所以命题的最后一部分是显而易见的。

As a consequence of Proposition 29.11, two nonzero polynomials f,g ∈ K[X] are relatively prime iff there exist u,v ∈ K[X] such that
 由于29.11命题的结果，两个非零多项式f，g∈k[x]是相对素数，如果存在u，v∈k[x]，那么

uf + vg = 1.
 uf+vg=1.

The identity
 身份

d = uf + vg
 D=uf+vg

of part (2) of Proposition 29.11 is often called the Bezout identity.
 在第29.11号提案的第（2）部分中，常被称为贝佐特身份。

We derive more useful consequences of Proposition 29.11.
 我们得出29.11号提案更有用的结果。

Proposition 29.12. Let K be a field and let f,g ∈ K[X] be any two nonzero polynomials. For every gcd d ∈ K[X] of f and g, the following properties hold:
 提案29.12。设k为场，设f，g∈k[x]为任意两个非零多项式。对于f和g的每一个gcd d∈k[x]，下列性质成立：

*(1)*    For every nonzero polynomial q ∈ K[X], the polynomial dq is a gcd of fq and gq.
 对于每个非零多项式q∈k[x]，多项式dq是fq和gq的gcd。

*(2)*    For every nonzero polynomial q ∈ K[X], if q divides f and g, then d/q is a gcd of f/q and g/q.
 对于每一个非零多项式q∈k[x]，如果q除以f和g，则d/q是f/q和g/q的gcd。

Proof. (1) By Proposition 29.11 (2), d divides f and g, and there exist u,v ∈ K[X], such that
 证据。（1）根据29.11（2）号命题，d将f和g分开，并存在u，v∈k[x]，这样

d = uf + vg.
 d=uf+vg。

Then, dq divides fq and gq, and
 然后，dq将fq和gq分开，并且

dq = ufq + vgq.
 dq=ufq+vgq。

​          By Proposition 29.11 (2), dq is a gcd of fq and gq. The proof of (2) is similar.                         
 根据29.11（2）号提案，DQ是FQ和GQ的GCD。（2）的证明类似。

The following proposition is used often.
 通常使用以下命题。

Proposition 29.13. (Euclid’s proposition) Let K be a field and let f,g,h ∈ K[X] be any nonzero polynomials. If f divides gh and f is relatively prime to g, then f divides h.
 提案29.13。（欧几里得命题）设k为场，设f，g，h∈k[x]为任意非零多项式。如果F除以GH，F相对地是G的素数，那么F除以H。

Proof. From Proposition 29.11, f and g are relatively prime iff there exist some polynomials u,v ∈ K[X] such that
 证据。从29.11命题来看，f和g是相对素数iff，存在一些多项式u，v∈k[x]，这样

uf + vg = 1.
 uf+vg=1.

Then, we have
 那么，我们有了

ufh + vgh = h,
 ufh+vgh=h，

​            and since f divides gh, it divides both ufh and vgh, and so, f divides h.                                    
 因为F划分了GH，所以它同时划分了UFH和VGH，所以，F划分了H。

Proposition 29.14. Let K be a field and let f,g1,...,gm ∈ K[X] be some nonzero polynomials. If f and gi are relatively prime for all i, 1 ≤ i ≤ m, then f and g1 ···gm are relatively prime.
 提案29.14。设k为场，设f，g1，…，gm∈k[x]为非零多项式。如果f和gi对所有i都是相对素数，1≤i≤m，那么f和g1···gm是相对素数。

Proof. We proceed by induction on m. The case m = 1 is trivial. Let h = g2 ···gm. By the induction hypothesis, f and h are relatively prime. Let d be a gcd of f and g1h. We claim that d is relatively prime to g1. Otherwise, d and g1 would have some nonconstant gcd d1 which would divide both f and g1, contradicting the fact that f and g1 are relatively prime. Now, by Proposition 29.13, since d divides g1h and d and g1 are relatively prime, d divides h = g2 ···gm. But then, d is a divisor of f and h, and since f and h are relatively prime, d must be a constant, and f and g1 ···gm are relatively prime. 
 证据。我们对m进行归纳，m=1的情况是微不足道的。假设h=g2···gm，根据诱导假设，f和h是相对质数。假设d是f和g1h的gcd，我们认为d是g1的相对素数。否则，d和g1会有一些不稳定的gcd d1，将f和g1分开，这与f和g1相对质数的事实相矛盾。现在，根据命题29.13，由于d除以g1 h和d，g1是相对素数，d除以h=g2····gm，但d是f和h的除数，由于f和h是相对素数，d必须是常数，f和g1···gm是相对素数。

Definition 29.7 is generalized to any finite number of polynomials as follows.
 定义29.7推广到任何有限数量的多项式，如下所示。

Definition 29.8. Given any nonzero polynomials f1,...,fn ∈ K[X], where n ≥ 2, a polynomial d ∈ K[X] is a greatest common divisor of f1,...,fn (for short, a gcd of f1,...,fn) if d divides each fi and whenever h ∈ K[X] divides each fi, then h divides d. We say that f1,...,fn are relatively prime if 1 is a gcd of f1,...,fn.
 定义29.8.给定任意非零多项式f1，…，fn∈k[x]，其中n≥2，多项式d∈k[x]是f1，…，fn的最大公因数（简而言之，f1，…，fn的gcd），如果d对每个fi进行除，当h∈k[x]对每个fi进行除时，h对d进行除。我们说f1，…，fn是相对素数，如果1是gcd，fn是相对素数。一层，…，二层。

It is easily shown that Proposition 29.11 can be generalized to any finite number of polynomials, and similarly for its relevant corollaries. The details are left as an exercise.
 很容易证明29.11命题可以推广到任何有限个多项式，同样也可以推广到它的相关推论。细节留作练习。

Proposition 29.15. Let K be a field and let f1,...,fn ∈ K[X] be any n ≥ 2 nonzero polynomials. For every polynomial d ∈ K[X], the following properties are equivalent:
 提案29.15。设k为场，设f1，…，fn∈k[x]为任意n≥2个非零多项式。对于每一个多项式d∈k[x]，下列性质是等价的：

*(1)*    The polynomial d is a gcd of f1,...,fn.
 多项式d是f1，…，fn的gcd。

*(2)*    The polynomial d divides each fi and there exist u1,...,un ∈ K[X] such that
 多项式d将每一个fi分开，并且存在u1，…，un∈k[x]，这样

*d*         = u1f1 + ··· + unfn.
 =U1F1+·····+UNFN。

*(3)*    The ideals (fi), and (d) satisfy the equation
 理想（fi）和（d）满足方程

*d*         = (f1) + ··· + (fn).
 =（F1）+·····+（FN）。

​             In addition, d = 06  , and d is unique up to multiplication by a nonzero scalar in K.
 此外，d=06，d是唯一的，直到K中的非零标量相乘。

As a consequence of Proposition 29.15, some polynomials f1,...,fn ∈ K[X] are relatively prime iff there exist u1,...,un ∈ K[X] such that
 由于29.15命题的结果，一些多项式f1，…，fn∈k[x]是相对素数iff存在u1，…，un∈k[x]这样

u1f1 + ··· + unfn = 1.
 U1F1+·····+UNFN=1.

The identity
 身份

u1f1 + ··· + unfn = 1
 U1F1+·····+UNFN=1

of part (2) of Proposition 29.15 is also called the Bezout identity.
 第29.15号提案第（2）部分也被称为贝索特身份。

We now consider the factorization of polynomials of a single variable into irreducible factors.
 我们现在考虑将单个变量的多项式因式分解为不可约因子。

##       29.5          Factorization and Irreducible Factors in K[X]  29.5因子分解和K[X]中的不可约因子

Definition 29.9. Given a field K, a polynomial p ∈ K[X] is irreducible or indecomposable or prime if deg(p) ≥ 1 and if p is not divisible by any polynomial q ∈ K[X] such that 1 ≤ deg(q) < deg(p). Equivalently, p is irreducible if deg(p) ≥ 1 and if p = q1q2, then either q1 ∈ K or q2 ∈ K (and of course, q1 = 06 , q2 = 0).6
 定义29.9.给定一个域k，如果deg（p）≥1，多项式p∈k[x]是不可约或不可分解的或素数，如果p不可被任何多项式q∈k[x]除，则1≤deg（q）<deg（p）。等价地，如果deg（p）≥1，p是不可约的，如果p=q1 q2，则q1∈k或q2∈k（当然，q1=06，q2=0）。6

Example 29.2. Every polynomial aX + b of degree 1 is irreducible. Over the field R, the polynomial X2 + 1 is irreducible (why?), but X3 + 1 is not irreducible, since
 例29.2。1次的每个多项式ax+b都是不可约的。在r域上，多项式x2+1是不可约的（为什么？），但x3+1不是不可约的，因为

X3 + 1 = (X + 1)(X2 − X + 1).
 x3+1=（x+1）（x2−x+1）。

The polynomial X2 − X + 1 is irreducible over R (why?). It would seem that X4 + 1 is irreducible over R, but in fact,
 多项式x2-x+1在r上是不可约的（为什么？）.似乎x4+1在r上是不可约的，但实际上，

X4 + 1 = (X2 − √2X + 1)(X2 + √2X + 1).
 x4+1=（x2−√2x+1）（x2+√2x+1）。

However, in view of the above factorization, X4 + 1 is irreducible over Q.
 然而，考虑到上述因子分解，x4+1在q上是不可约的。

It can be shown that the irreducible polynomials over R are the polynomials of degree 1, or the polynomials of degree 2 of the form aX2 + bX + c, for which b2 − 4ac < 0 (i.e., those having no real roots). This is not easy to prove! Over the complex numbers C, the only irreducible polynomials are those of degree 1. This is a version of a fact often referred to as the “Fundamental theorem of Algebra”, or, as the French sometimes say, as “d’Alembert’s theorem”!
 可以看出，R上的不可约多项式是阶1的多项式，或者是ax2+bx+c形式的阶2的多项式，其中b2−4ac<0（即那些没有实根的）。这不容易证明！在复数c上，唯一不可约多项式是阶1的多项式。这是一个事实的版本，通常被称为“代数的基本定理”，或者，正如法国人有时说的，被称为“达朗伯定理”！

We already observed that for any two nonzero polynomials f,g ∈ K[X], f divides g iff (g) ⊆ (f). In view of the definition of a maximal ideal given in Definition 29.4, we now prove that a polynomial p ∈ K[X] is irreducible iff (p) is a maximal ideal in K[X].
 我们已经观察到，对于任意两个非零多项式f，g∈k[x]，f除以g iff（g）（f）。鉴于定义29.4中给出的最大理想的定义，我们现在证明多项式p∈k[x]是不可约的，iff（p）是k[x]中的最大理想。

Proposition 29.16. A polynomial p ∈ K[X] is irreducible iff (p) is a maximal ideal in K[X].
 提案29.16。多项式p∈k[x]是不可约的，iff（p）是k[x]中的最大理想。


 

29.5. FACTORIZATION AND IRREDUCIBLE FACTORS IN K[X]
 29.5。K[X]中的因式分解和不可约因子

Proof. Since K[X] is an integral domain, for all nonzero polynomials p,q ∈ K[X], deg(pq) = deg(p) + deg(q), and thus, (p) =6 K[X] iff deg(p) ≥ 1. Assume that p ∈ K[X] is irreducible. Since every ideal in K[X] is a principal ideal, every ideal in K[X] is of the form (q), for some q ∈ K[X]. If (p) ⊆ (q), with deg(q) ≥ 1, then q divides p, and since p ∈ K[X] is irreducible, this implies that p = λq for some λ = 06 in K, and so, (p) = (q). Thus, (p) is a maximal ideal. Conversely, assume that (p) is a maximal ideal. Then, as we showed above, deg(p) ≥ 1, and if q divides p, with deg(q) ≥ 1, then (p) ⊆ (q), and since (p) is a maximal ideal, this implies that (p) = (q), which means that p = λq for some λ = 06 in K, and so, p is irreducible.   
 证据。由于k[x]是一个积分域，对于所有非零多项式p，q∈k[x]，deg（pq）=deg（p）+deg（q），因此，（p）=6 k[x]iff deg（p）≥1。假设p∈k[x]是不可约的。因为k[x]中的每一个理想都是主理想，所以k[x]中的每一个理想都是形式（q），对于某些q∈k[x]。如果（p）（q），且deg（q）≥1，则q除以p，由于p∈k[x]是不可约的，这意味着对于一些λ=06的k，p=λq，因此，（p）=（q）。因此，（p）是最大理想。相反，假设（p）是最大理想。然后，如我们上面所示，deg（p）≥1，如果q除以p，deg（q）≥1，那么（p）（q），由于（p）是最大理想，这意味着（p）=（q），这意味着对于k中的一些λ=06，p=λq，因此p是不可约的。

Let p ∈ K[X] be irreducible. Then, for every nonzero polynomial g ∈ K[X], either p and g are relatively prime, or p divides g. Indeed, if d is any gcd of p and g, if d is a constant, then p and g are relatively prime, and if not, because p is irreducible, we have d = λp for some λ = 06 in K, and thus, p divides g. As a consequence, if p,q ∈ K[X] are both irreducible, then either p and q are relatively prime, or p = λq for some λ = 06 in K. In particular, if p,q ∈ K[X] are both irreducible monic polynomials and p =6 q, then p and q are relatively prime.
 设p∈k[x]不可约。那么，对于每一个非零多项式g∈k[x]，要么p和g是相对素数，要么p除以g。实际上，如果d是p和g的任何gcd，如果d是常数，那么p和g是相对素数，如果不是，因为p是不可约的，我们对k中的一些λ=06有d=λp，因此p除以g。作为一个常数。序列，如果p，q∈k[x]都是不可约的，那么p和q都是相对素数，或者对于k中的一些λ=06，p=λq。特别是，如果p，q∈k[x]都是不可约Monic多项式，p=6q，那么p和q都是相对素数。

We now prove the (unique) factorization of polynomials into irreducible factors. Theorem 29.17. Given any field K, for every nonzero polynomial
 我们现在证明多项式的（唯一）因式分解为不可约因子。定理29.17。对于每一个非零多项式，给定任意字段k

f = adXd + ad−1Xd−1 + ··· + a0
 f=adxd+ad−1xd−1+····+a0

of degree d = deg(f) ≥ 1 in K[X], there exists a unique set {hp1,k1i,...,hpm,kmi} such that
 当d=deg（f）≥1 in k[x]时，存在一个独特的集合hp1，k1i，…，hpm，kmi

,
 ，

where the pi ∈ K[X] are distinct irreducible monic polynomials, the ki are (not necessarily distinct) integers, and m ≥ 1, ki ≥ 1.
 当pi∈k[x]是不同的不可约Monic多项式时，ki是（不一定是不同的）整数，m≥1，ki≥1。

Proof. First, we prove the existence of such a factorization by induction on d = deg(f). Clearly, it is enough to prove the result for monic polynomials f of degree d = deg(f) ≥ 1. If d = 1, then f = X + a0, which is an irreducible monic polynomial.
 证据。首先，我们通过D=deg（f）上的归纳证明了这种因子分解的存在性。显然，这足以证明D=deg（f）≥1的Monic多项式f的结果。如果d=1，则f=x+a0，这是一个不可约Monic多项式。

Assume d ≥ 2, and assume the induction hypothesis for all monic polynomials of degree < d. Consider the set S of all monic polynomials g such that deg(g) ≥ 1 and g divides f. Since f ∈ S, the set S is nonempty, and thus, S contains some monic polynomial p1 of minimal degree. Since deg(p1) ≥ 1, the monic polynomial p1 must be irreducible. Otherwise we would have p1 = g1g2, for some monic polynomials g1,g2 such that deg(p1) > deg(g1) ≥ 1 and deg(p1) > deg(g2) ≥ 1, and since p1 divide f, then g1 would divide f, contradicting the minimality of the degree of p1. Thus, we have f = p1q, for some irreducible monic polynomial p1, with q also monic. Since deg(p1) ≥ 1, we have deg(q) < deg(f), and we can apply the induction hypothesis to q. Thus, we obtain a factorization of the desired form.
 假设d≥2，并假设所有次数<d的Monic多项式的归纳假设。考虑所有Monic多项式g的集合s，使deg（g）≥1和g除以f。由于f∈s，集合s是非空的，因此s包含一些最小次数的Monic多项式p1。由于deg（p1）≥1，monic多项式p1必须是不可约的。否则我们将得到p1=g1 g2，对于一些Monic多项式g1，g2，这样deg（p1）>deg（g1）≥1和deg（p1）>deg（g2）≥1，并且由于p1除以f，那么g1将除以f，这与p1的最小程度相矛盾。因此，对于一些不可约Monic多项式p1，我们有f=p1 q，其中q也是monic。由于deg（p1）≥1，因此deg（q）<deg（f），我们可以将诱导假设应用于q，从而获得所需形式的因式分解。

We now prove uniqueness. Assume that
 我们现在证明了它的独特性。假设

,
 ，

and
 和

.
 .

Thus, we have
 因此，我们

.
 .

We prove that m = n, pi = qi and hi = ki, for all i, with 1 ≤ i ≤ n.
 我们证明m=n，pi=qi，hi=ki，对于所有i，1≤i≤n。

The proof proceeds by induction on h1 + ··· + hn.
 通过对h1+·····+hn的归纳，证明了这一点。

If h1 + ··· + hn = 1, then n = 1 and h1 = 1. Then, since K[X] is an integral domain, we have
 如果h1+·····+hn=1，则n=1，h1=1。那么，既然k[x]是一个积分域，我们有

,
 ，

and since q1 and the pi are irreducible monic, we must have m = 1 and p1 = q1.
 既然q1和π是不可约的Monic，我们必须有m=1和p1=q1。

If h1 + ··· + hn ≥ 2, since K[X] is an integral domain and since h1 ≥ 1, we have
 如果h1+·····+hn≥2，因为k[x]是一个积分域，并且h1≥1，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

with
 具有

q = q1h1−1 ···qnhn,
 Q=Q1H1−1···QNHN，

where (h1 − 1) + ··· + hn ≥ 1 (and q1h1−1 = 1 if h1 = 1). Now, if q1 is not equal to any of the pi, by a previous remark, q1 and pi are relatively prime, and by Proposition 29.14, q1 and are relatively prime. But this contradicts the fact that q1 divides. Thus, q1 is equal to one of the pi. Without loss of generality, we can assume that q1 = p1. Then, since K[X] is an integral domain, we have
 式中（h1−1）+·····+hn≥1（如果h1=1，q1h1−1=1）。现在，如果q1不等于π中的任何一个，由前面的注释可知，q1和π是相对素数，由命题29.14可知，q1是相对素数。但这与q1分裂的事实相矛盾。因此，q1等于π之一。在不失去一般性的情况下，我们可以假设q1=p1。那么，既然k[x]是一个积分域，我们有

,
 ，

where = 1, and = 1. Now, (h1 −1)+···+hn < h1 +···+hn, and we can apply the induction hypothesis to conclude that m = n, pi = qi and hi = ki, with 1 ≤ i ≤ n. 
 其中=1和=1。现在，（h1−1）+·······+hn<h1······+hn），我们可以应用诱导假设得出m=n，pi=qi，hi=ki，1≤i≤n。

The above considerations about unique factorization into irreducible factors can be extended almost without changes to more general rings known as Euclidean domains. In such rings, some abstract version of the division theorem is assumed to hold.
 上述关于独特因子分解为不可约因子的考虑几乎可以扩展到更一般的环，即欧几里得域。在这样的环中，假设存在一些抽象形式的除法定理。

Definition 29.10. A Euclidean domain (or Euclidean ring) is an integral domain A such that there exists a function ϕ: A → N with the following property: For all a,b ∈ A with b = 06 , there are some q,r ∈ A such that
 定义29.10.欧几里得域（或欧几里得环）是一个积分域A，这样就存在一个具有以下性质的函数：对于所有a，b∈a和b=06，有一些q，r∈a这样

​                                                            a = bq + r     and    ϕ(r) < ϕ(b).
 A=Bq+R和_（R）<（B）。

29.5. FACTORIZATION AND IRREDUCIBLE FACTORS IN K[X]
 29.5。K[X]中的因式分解和不可约因子

Note that the pair (q,r) is not necessarily unique.
 注意，这对（q，r）不一定是唯一的。

Actually, unique factorization holds in principal ideal domains (PID’s), see Theorem 31.12. As shown below, every Euclidean domain is a PID, and thus, unique factorization holds for Euclidean domains.
 实际上，唯一因式分解存在于主理想域（PID），见定理31.12。如下图所示，每个欧几里德域都是一个PID，因此，欧几里德域具有唯一的因子分解。

Proposition 29.18. Every Euclidean domain A is a PID. Proof. Let I be a nonnull ideal in A. Then, the set
 提案29.18。每个欧几里得域A都是一个PID。证据。让我成为A中的一个非空理想。

{ϕ(a) | a ∈ I}
 （a）a∈i

is nonempty, and thus, has a smallest element m. Let b be any (nonnull) element of I such that m = ϕ(b). We claim that I = (b). Given any a ∈ I, we can write
 是非空的，因此有一个最小的元素m。让b是i的任何（非空）元素，这样m=_（b）。我们声称我=（B）。给任何a∈i，我们可以写

a = bq + r
 A=Bq+R

for some q,r ∈ A, with ϕ(r) < ϕ(b). Since b ∈ I and I is an ideal, we also have bq ∈ I, and since a,bq ∈ I and I is an ideal, then r ∈ I with ϕ(r) < ϕ(b) = m, contradicting the minimality of m. Thus, r = 0 and a ∈ (b). But then,
 对于某些q，r∈a，其中（r）<（b）。既然b∈i和i是一个理想，我们也有bq∈i，既然a，bq∈i和i是一个理想，那么r∈i与（r）<（b）=m，与m的极小性相矛盾。因此，r=0和a∈（b）。但是后来，

I ⊆ (b),
 我（b）

and since b ∈ I, we get
 既然b∈i，我们得到

I = (b),
 我=（B）

​         and A is a PID.                                                                                                                                  
 A是PID。

As a corollary of Proposition 29.18, the ring Z is a Euclidean domain (using the function ϕ(a) = |a|) and thus, a PID. If K is a field, the function ϕ on K[X] defined such that
 作为命题29.18的一个推论，环Z是一个欧几里得域（使用函数（a）=a），因此是一个PID。如果k是一个场，k[x]上的函数_定义如下：

​                                                                            0                     if f = 0,
 如果f=0，则为0，

f
 f

= 0,
 ＝0，

shows that K[X] is a Euclidean domain.
 表明k[x]是欧几里得域。

Example 29.3. A more interesting example of a Euclidean domain is the ring Z[i] of Gaussian integers, i.e., the subring of C consisting of all complex numbers of the form a + ib, where a,b ∈ Z. Using the function ϕ defined such that
 例29.3。欧几里得域的一个更有趣的例子是高斯整数的环Z[i]，即C的子环，由A+Ib形式的所有复数组成，其中a，b∈z。使用函数，定义如下：

ϕ(a + ib) = a2 + b2,
 ⑨（a+ib）=a2+b2，

we leave it as an interesting exercise to prove that Z[i] is a Euclidean domain.
 我们把它作为一个有趣的练习来证明z[i]是一个欧几里得域。

 Not every PID is a Euclidean ring.
 不是每个PID都是欧几里得环。

Remark: Given any integer d ∈ Z such thatQ(√d) is the field consisting of all complex numbersd 6= 0,1 and d does not have any square factor
 注：给定任意整数d∈z，则q（√d）是由所有复数组成的域，d 6=0,1，d不具有任何平方因子。

greater than one, the quadratic field
 大于1的二次场

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

 is denoted byof the formwith a,b ∈ Qa. The subring of+Z[ib√√d]−. We define thed if d < 0Q, and of all the real numbers of the form(√d)ring of integersconsisting of all elements as above for whichof the field Q(√                                                      a + b√d ifa,bd >∈ 0Z,
 用a，b∈qa表示。+Z[ib√√d]−的子框。我们定义了d<0q，和所有实数的形式（√d）环的积分，所有元素的存在，如上文所述，其中，字段q（√a+b√d ifa，bd>的∈0z，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

d) as the subring of Q(√d) consisting of the following elements:
 d）作为q（√d）的子框，由以下元素组成：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

(1)    If d ≡ 2 (mod 4) or d ≡ 3 (mod 4), then all elements of the forma + b√d (if d > 0), with a,b ∈ Z; a + ib√−d (if d < 0) or all elements of the form
 如果d 2（mod 4）或d 3（mod 4），那么形式的所有元素+b√d（如果d>0），带有a，b∈z；a+ib√−d（如果d<0）或形式的所有元素

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

(2)    If d ≡ 1(mod4), then all elements of the forma+b√d)/2 (if d > 0), with a,b ∈ Z(aand with+ib√−d)a,b/2 (either both even or bothif d < 0) or all elements of the form ( odd.
 如果d 1（mod4），那么所有的form a+b√d）/2元素（如果d>0），其中a，b∈z（aand with+ib√−d）a，b/2（偶数或both if d<0）或形式的所有元素（奇数）。

ZObserve that when[√ d ≡ 2(mod4) or d ≡ 3(mod4), the ring of integers of Q(√d) is equal to d].
 zobserve当[√d 2（mod4）或d 3（mod4）时，q（√d）的整数环等于d]。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

It can be shown that the rings of integers of the fields Q(√−d) where d = 19, 43, 67, 163 are PID’s, but not Euclidean rings. The proof is hard and long. First, it can be shown that these rings are UFD’s (refer to Definition 31.2), see Stark [159] (Chapter 8, Theorems 8.21
 可以证明，字段q（√−d）中d=19、43、67、163的整数环是PID，但不是欧几里得环。证据很难，而且很长。首先，可以证明这些环是UFD（参考定义31.2），见Stark[159]（第8章，定理8.21

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

and 8.22). Then, we use the fact that the ring of integers of the field Q(√d) (with d 6= 0,1 any square-free integers) is a certain kind of integral domain called a Dedekind ring; see Atiyah-MacDonald [8] (Chapter 9, Theorem 9.5) or Samuel [139] (Chapter III, Section 3.4). Finally, we use the fact that if a Dedekind ring is a UFD then it is a PID, which follows from Proposition 31.13.
 和8.22）。然后，我们利用q（√d）（d 6=0,1任意平方自由整数）的整数环是一种称为Dedekind环的积分域的事实；见Atiyah MacDonald[8]（第9章，定理9.5）或Samuel[139]（第三章，第3.4节）。最后，我们利用这样一个事实：如果一个Dedekind环是一个UFD，那么它是一个PID，这是从命题31.13得出的。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

Actually, the rings of integers of Q(√d) that are Euclidean domains are completely determined but the proof is quite difficult. It turns out that there are twenty one such rings corresponding to the integers: −11,−7,−3,−2,−1, 2,3,5,6,7,11, 13,17,19,21, 29,33,37,41,57 and 73, see Stark [159] (Chapter 8). For more on quadratic fields and their rings of integers, see Stark [159] (Chapter 8) or Niven, Zuckerman and Montgomery [128] (Chapter 9).
 实际上，欧氏域q（√d）的整数环是完全确定的，但证明是相当困难的。结果发现，有21个这样的环对应于整数：−11、−7、−3、−2、−1、2、3、5、6、7、11、13、17、19、21、29、33、37、41、57和73，见Stark[159]（第8章）。有关二次域及其整数环的更多信息，请参阅stark[159]（第8章）或niven、zuckerman和montgomery[128]（第9章）。

It is possible to characterize a larger class of rings (in terms of ideals), factorial rings (or unique factorization domains), for which unique factorization holds (see Section 31.1). We now consider zeros (or roots) of polynomials.
 可以描述一类更大的环（根据理想），阶乘环（或唯一的阶乘域），对于这些环，唯一的阶乘成立（见第31.1节）。我们现在考虑多项式的零（或根）。

##       29.6       Roots of Polynomials  29.6多项式的根

We go back to the general case of an arbitrary ring for a little while.
 我们回到一般情况下的任意环一会儿。

Definition 29.11. Given a ring A and any polynomial f ∈ A[X], we say that somef ∈) = 0.A[X1,...,Xα ∈nA],
 定义29.11.给定一个环A和任意一个多项式f∈a[x]时，我们假设somef∈）=0.a[x1，…，xα∈na]，

is a zero of f, or a root of f, if f(α) = 0. Similarly, given a polynomial we say that (α1,...,αn) ∈ An is a a zero of f, or a root of f, if f(α1,...,αn
 如果f（α）=0，则为f的零或根。同样，对于一个多项式，我们说（α1，…，αn）∈an是f的零点，或f的根，如果f（α1，…，αn

When f ∈ A[X] is the null polynomial, every α ∈ A is trivially a zero of f. This case being trivial, we usually assume that we are considering zeros of nonnull polynomials.
 当f∈a[x]是零多项式时，每个α∈a都是f的零值，这种情况是平凡的，我们通常假定我们考虑的是非零多项式的零。


 

Example 29.4. Considering the polynomial f(X) = X2 − 1, both +1 and −1 are zeros of f(X). Over the field of reals, the polynomial g(X) = X2 + 1 has no zeros. Over the field C of complex numbers, g(X) = X2 + 1 has two roots i and −i, the square roots of −1, which are “imaginary numbers.”
 例29.4。考虑到多项式f（x）=x2−1，+1和−1都是f（x）的零。在实数域上，多项式g（x）=x2+1没有零。在复数域C上，g（x）=x2+1有两个根i和−i，即−1的平方根，即“虚数”。

We have the following basic proposition showing the relationship between polynomial division and roots.
 下面给出了多项式除法与根的关系的基本命题。

Proposition 29.19. Let f ∈ A[X] be any polynomial and α ∈ A any element of A. If the result of dividing f by X − α is f = (X − α)q + r, then r = 0 iff f(α) = 0, i.e., α is a root of f iff r = 0.
 提案29.19。设f∈a[x]为任意多项式，α∈a为a的任意元素，如果f除以x−α的结果为f=（x−α）q+r，则r=0 iff（α）=0，即α为f iff r=0的根。

Proof. We have f = (X − α)q + r, with deg(r) < 1 = deg(X − α). Thus, r is a constant in K, and since f(α) = (α − α)q(α) + r, we get f(α) = r, and the proposition is trivial. 
 证据。我们有f=（x−α）q+r，deg（r）<1=deg（x−α）。因此，r是k中的常数，因为f（α）=（α−α）q（α）+r，我们得到f（α）=r，这个命题是平凡的。

We now consider the issue of multiplicity of a root.
 我们现在考虑一个根的多重性问题。

Proposition 29.20. Let f ∈ A[X] be any nonnull polynomial and h ≥ 0 any integer. The following conditions are equivalent.
 提案29.20。设f∈a[x]为任意非零多项式，h≥0任意整数。以下条件是等效的。

*(1)*    f is divisible by (X − α)h but not by (X − α)h+1.
 F可被（x−α）h整除，但不能被（x−α）h+1整除。

*(2)*    There is some g ∈ A[X] such that f = (X − α)hg and g(α) = 06 .
 有一些g∈a[x]这样f=（x−α）hg和g（α）=06。

Proof. Assume (1). Then, we have f = (X − α)hg for some g ∈ A[X]. If we had g(α) = 0, by Proposition 29.19, g would be divisible by (X − α), and then f would be divisible by (X − α)h+1, contradicting (1).
 证据。假设（1）。然后，对于一些g∈a[x]，我们得到f=（x−α）hg。如果g（α）=0，根据命题29.19，g可以被（x−α）整除，那么f可以被（x−α）h+1整除，与（1）矛盾。

Assume (2), that is, f = (X − α)hg and g(α) = 06 . If f is divisible by (X − α)h+1, then we have f = (X − α)h+1g1, for some g1 ∈ A[X]. Then, we have
 假设（2），即f=（x−α）Hg和g（α）=06。如果f可被（x−α）h+1整除，那么对于某些g1∈a[x]，我们得到f=（x−α）h+1g1。那么，我们有了

(X − α)hg = (X − α)h+1g1,
 （x−α）Hg=（x−α）H+1g1，

and thus
 因此

(X − α)h(g − (X − α)g1) = 0,
 （x−α）h（g−（x−α）g1）=0，

and since the leading coefficient of (X − α)h is 1 (show this by induction), by Proposition 29.1, (X − α)h is not a zero divisor, and we get g − (X − α)g1 = 0, i.e., g = (X − α)g1, and so g(α) = 0, contrary to the hypothesis.  
 由于（x−α）h的前导系数是1（通过归纳法证明），根据命题29.1，（x−α）h不是零因子，我们得到g−（x−α）g1=0，即g=（x−α）g1，因此g（α）=0，与假设相反。

As a consequence of Proposition 29.20, for every nonnull polynomial f ∈ A[X] and every α ∈ A, there is a unique integer h ≥ 0 such that f is divisible by (X − α)h but not by (X − α)h+1. Indeed, since f is divisible by (X − α)h, we have h ≤ deg(f). When h = 0, α is not a root of f, i.e., f(α) = 06 . The interesting case is when α is a root of f.
 由于29.20命题的结果，对于每一个非零多项式f∈a[x]和每一个α∈a，存在一个唯一的整数h≥0，使得f可被（x−α）h整除，但不可被（x−α）h+1整除。事实上，因为f可以被（x−α）h整除，所以h≤deg（f）。当h=0时，α不是f的根，即f（α）=06。有趣的情况是α是f的根。

Definition 29.12. Given a ring A and any nonnull polynomial f ∈ A[X], given any α ∈ A, the unique h ≥ 0 such that f is divisible by (X − α)h but not by (X − α)h+1 is called the order, or multiplicity, of α. We have h = 0 iff α is not a root of f, and when α is a root of f, if h = 1, we call α a simple root, if h = 2, a double root, and generally, a root of multiplicity h ≥ 2 is called a multiple root.
 定义29.12.给定一个环A和任意一个非零多项式f∈a[x]，给定任意α∈a，其唯一h≥0使得f可被（x−α）h整除，但不被（x−α）h+1整除，称为α的阶次或多重性。如果α不是f的根，当α是f的根时，如果h=1，我们称α为简单根，如果h=2，我们称之为双根，通常，多重性h≥2的根称为多根。

Observe that Proposition 29.20 (2) implies that if A ⊆ B, where A and B are rings, for every nonnull polynomial f ∈ A[X], if α ∈ A is a root of f, then the multiplicity of α with respect to f ∈ A[X] and the multiplicity of α with respect to f considered as a polynomial in B[X], is the same.
 观察29.20（2）命题意味着，如果a b，其中a和b是环，对于每个非零多项式f∈a[x]，如果α∈a是f的根，那么α相对于f∈a[x]的多重性和α相对于f的多重性在b[x]中被视为多项式，则为sa我。

We now show that if the ring A is an integral domain, the number of roots of a nonzero polynomial is at most its degree.
 我们现在证明，如果环A是一个积分域，则非零多项式的根的数目最多是它的次数。

Proposition 29.21. Let f,g ∈ A[X] be nonnull polynomials, let α ∈ A, and let h ≥ 0 and k ≥ 0 be the multiplicities of α with respect to f and g. The following properties hold.
 提案29.21。设f，g∈a[x]为非零多项式，设α∈a，设h≥0，k≥0为α对f和g的重数，其性质如下：

*(1)*    If l is the multiplicity of α with respect to (f + g), then l ≥ min(h,k). If h =6 k, then l = min(h,k).
 如果L是α相对于（f+g）的重数，则L≥min（h，k）。如果h=6 k，则l=min（h，k）。

*(2)*    If m is the multiplicity of α with respect to fg, then m ≥ h + k. If A is an integral domain, then m = h + k.
 如果m是α相对于fg的重数，则m≥h+k。如果a是积分域，则m=h+k。

Proof. (1) We have f(X) = (X − α)hf1(X), g(X) = (X − α)kg1(X), with f1(α) = 06 and g1(α) = 06 . Clearly, l ≥ min(h,k). If h =6 k, assume h < k. Then, we have f(X) + g(X) = (X − α)hf1(X) + (X − α)kg1(X) = (X − α)h(f1(X) + (X − α)k−hg1(X)), and since (f1(X) + (X − α)k−hg1(X))(α) = f1(α)  = 06, we have l = h = min(h,k).
 证据。（1）我们有f（x）=（x−α）hf1（x），g（x）=（x−α）kg1（x），其中f1（α）=06和g1（α）=06。显然，l≥min（h，k）。如果h=6 k，假设h<k。那么，我们有f（x）+g（x）=（x−α）h f1（x）+（x−α）kg1（x）=（x−α）h（f1（x）+（x−α）k−hg1（x）），因为（f1（x）+（x−α）k−hg1（x））（α）=f1（α）=06，我们有l=h=min（h，k）。

(2) We have f(X)g(X) = (X − α)h+kf1(X)g1(X),
 （2）我们得到f（x）g（x）=（x−α）h+kf1（x）g1（x），

with f1(α) = 06 and g1(α) = 06 . Clearly, m ≥ h + k. If A is an integral domain, then f1(α)g1(α) = 06 , and so m = h + k.      
 f1（α）=06和g1（α）=06。显然，m≥h+k。如果a是一个积分域，那么f1（α）g1（α）=06，因此m=h+k。

Proposition 29.22. Let A be an integral domain. Let f be any nonnull polynomial f ∈ A[X] and let α1,...,αm ∈ A be m ≥ 1 distinct roots of f of respective multiplicities k1,...,km.
 提案29.22。设A为积分域。设f为任意非零多项式f∈a[x]且设α1，…，αm∈a为m≥1各自多重性k 1，…，km的f的不同根。

Then, we have f(X) = (X − α1)k1 ···(X − αm)kmg(X),
 然后，我们得到f（x）=（x−α1）k1···（x−αm）kmg（x），

​        where g ∈ A[X] and g(αi) = 06     for all i, 1 ≤ i ≤ m.
 式中，所有i的g∈a[x]和g（αi）=06，1≤i≤m。

Proof. We proceed by induction on m. The case m = 1 is obvious in view of Definition 29.12 (which itself, is justified by Proposition 29.20). If m ≥ 2, by the induction hypothesis, we have
 证据。我们对m进行归纳，从定义29.12（其本身由29.20号提案证明）来看，案例m=1是显而易见的。如果m≥2，根据归纳假设，我们有

f(X) = (X − α1)k1 ···(X − αm−1)km−1g1(X),
 f（x）=（x−α1）k1····（x−αm−1）km−1g1（x），

where g1 ∈ A[X] and g1(αi) = 06 , for 1 ≤ i ≤ m − 1. Since A is an integral domain and αi =6 αj for i =6 j, since αm is a root of f, we have
 式中，g1∈a[x]和g1（αi）=06，对于1≤i≤m−1。因为a是一个积分域，αi=6αj是i=6 j，因为αm是f的根，我们有

0 = (αm − α1)k1 ···(αm − αm−1)km−1g1(αm),
 0=（αm−α1）k1····（αm−αm−1）km−1g1（αm），

which implies that   ) = 0. Now, by Proposition 29.21 (2), since αm is not a root of the polynomial (X − α1) 1 ···(X − αm−1)km−1 and since A is an integral domain, αm must be a root of multiplicity km of g1, which means that
 这意味着=0。现在，根据命题29.21（2），由于αm不是多项式（x−α1）1···（x−αm−1）km−1的根，并且由于a是一个积分域，αm必须是g1的多重性km的根，这意味着

g1(X) = (X − αm)kmg(X),
 g1（x）=（x−αm）kmg（x）、

with g(αm) = 06 . Since g1(αi) = 06 for 1 ≤ i ≤ m − 1 and A is an integral domain, we must also have g(αi) = 06 , for 1 ≤ i ≤ m − 1. Thus, we have
 g（αm）=06。因为g1（αi）=06对于1≤i≤m−1和a是一个积分域，我们还必须有g（αi）=06，对于1≤i≤m−1。因此，我们

f(X) = (X − α1)k1 ···(X − αm)kmg(X),
 f（x）=（x−α1）k1···（x−αm）kmg（x）、

​        where g ∈ A[X], and g(αi) = 06    for 1 ≤ i ≤ m.                                                                               
 式中，对于1≤i≤m，g∈a[x]和g（αi）=06。

As a consequence of Proposition 29.22, we get the following important result.
 根据29.22号提案，我们得到了以下重要结果。

Theorem 29.23. Let A be an integral domain. For every nonnull polynomial f ∈ A[X], if the degree of f is n = deg(f) and k1,...,km are the multiplicities of all the distinct roots of f (where m ≥ 0), then k1 + ··· + km ≤ n.
 定理29.23。设A为积分域。对于每一个非零多项式f∈a[x]，如果f的阶数为n=deg（f）和k1，…，km是f的所有不同根的重数（其中m≥0），则k1+·······+km≤n。

​        Proof. Immediate from Proposition 29.22.                                                                                     
 证据。直接引自29.22号提案。

Since fields are integral domains, Theorem 29.23 holds for nonnull polynomials over fields and in particular, for R and C. An important consequence of Theorem 29.23 is the following.
 由于域是积分域，定理29.23适用于域上的非空多项式，尤其适用于r和c。定理29.23的一个重要结论如下。

Proposition 29.24. Let A be an integral domain. For any two polynomials f,g ∈ A[X], if deg(f) ≤ n, deg(g) ≤ n, and if there are n + 1 distinct elements α1,α2,...,αn+1 ∈ A (with αi =6 αj for i =6 j) such that f(αi) = g(αi) for all i, 1 ≤ i ≤ n + 1, then f = g.
 提案29.24。设A为积分域。对于任意两个多项式f，g∈a[x]，如果deg（f）≤n，deg（g）≤n，并且如果有n+1个不同元素α1，α2，…，αn+1∈a（αi=6αj，i=6 j），那么f（αi）=g（αi）对于所有i，1≤i≤n+1，那么f=g。

Proof. Assume f =6 g, then, (f−g) is nonnull, and since f(αi) = g(αi) for all i, 1 ≤ i ≤ n+1, the polynomial (f − g) has n + 1 distinct roots. Thus, (f − g) has n + 1 distinct roots and is of degree at most n, which contradicts Theorem 29.23. 
 证据。假设f=6g，那么，（f−g）不为空，因为f（αi）=g（αi）对于所有i，1≤i≤n+1，多项式（f−g）有n+1个不同的根。因此，（f−g）有n+1个不同的根，最多有n个度，这与定理29.23相矛盾。

Proposition 29.24 is often used to show that polynomials coincide. We will use it to show some interpolation formulae due to Lagrange and Hermite. But first, we characterize the multiplicity of a root of a polynomial. For this, we need the notion of derivative familiar in analysis. Actually, we can simply define this notion algebraically.
 命题29.24常被用来证明多项式是一致的。我们将用它来表示由于拉格朗日和厄米特的一些插值公式。但首先，我们描述了多项式根的多重性。为此，我们需要分析中熟悉的导数概念。实际上，我们可以简单地用代数的方法定义这个概念。

First, we need to rule out some undesirable behaviors. Given a field K, as we saw in Example 2.8, we can define a homomorphism χ: Z → K given by
 首先，我们需要排除一些不良行为。给定一个场k，如例2.8所示，我们可以定义一个同态，由

χ(n) = n · 1,
 χ（n）=n·1，

where 1 is the multiplicative identity of K. Recall that we define n · a by
 其中1是k的乘法恒等式。回想一下，我们用

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

if n ≥ 0 (with 0 · a = 0) and
 如果n≥0（0·a=0），且

n · a = −(−n) · a
 N·A=−（−N）·A

if n < 0. We say that the field K is of characteristic zero if the homomorphism χ is injective. Then, for any a ∈ K with a = 06 , we have n · a = 06 for all n = 06
 如果n<0.如果同态χ是内射的，则K场的特征值为零。那么，对于a=06的任意a∈k，n=06都有n·a=06。

The fields Q, R, and C are of characteristic zero. In fact, it is easy to see that every field of characteristic zero contains a subfield isomorphic to Q. Thus, finite fields can’t be of characteristic zero.
 Q、R和C字段为特征零。事实上，很容易看出特征零点的每个场都包含一个与Q同构的子场，因此，有限场不能是特征零点。

Remark: If a field is not of characteristic zero, it is not hard to show that its characteristic, that is, the smallest n ≥ 2 such that n·1 = 0, is a prime number p. The characteristic p of K is the generator of the principal ideal pZ, the kernel of the homomorphism χ: Z → K. Thus, every finite field is of characteristic some prime p. Infinite fields of nonzero characteristic also exist.
 注：如果一个场不属于特征零点，则不难证明其特征，即n·1=0的最小n≥2是素数p，k的特征p是主理想p z的生成者，同态的核χ：z→k，因此，每一个定义Te场具有某些素数p的特征，也存在一些非零特征的无穷大的场。

Definition 29.13. Let A be a ring. The derivative f0, or Df, or D1f, of a polynomial f ∈ A[X] is defined inductively as follows:
 定义29.13.让A成为一个戒指。多项式f∈a[x]的导数f0或df或d1f归纳定义如下：

f0 = 0,    if f = 0, the null polynomial, f0 = 0,      if f = a, a = 06      , a ∈ A, f0 = nanXn if.
 f0=0，如果f=0，则为零多项式，f0=0，如果f=a，a=06，a∈a，f0=nanxn，如果。

If A = K is a field of characteristic zero, if deg(f) ≥ 1, the leading coefficient nan of f0 is nonzero, and thus, f0 is not the null polynomial. Thus, if A = K is a field of characteristic zero, when n = deg(f) ≥ 1, we have deg(f0) = n − 1.
 如果a=k是特征零点的一个字段，如果deg（f）≥1，f0的前导系数nan是非零的，因此f0不是零多项式。因此，如果a=k是特征零点的场，当n=deg（f）≥1时，我们得到deg（f0）=n-1。

 For rings or for fields of characteristic p ≥ 2, we could have f0 = 0, for a polynomial f of degree ≥ 1.
 对于环或特征p≥2的场，我们可以得到f0=0，对于次数≥1的多项式f。

The following standard properties of derivatives are recalled without proof (prove them as an exercise).
 以下衍生产品的标准属性被召回，但没有证据（作为练习证明）。

Given any two polynomials, f,g ∈ A[X], we have
 对于任意两个多项式，f，g∈a[x]，我们有

(f + g)0 = f0 + g0,
 （f+g）0=f0+g0，

(fg)0 = f0g + fg0.
 （fg）0=f0g+fg0。

For example, if f = (X − α)kg and k ≥ 1, we have
 例如，如果f=（x−α）kg和k≥1，我们有

f0 = k(X − α)k−1g + (X − α)kg0.
 f0=k（x−α）k−1g+（x−α）kg0。

We can now give a criterion for the existence of simple roots. The first proposition holds for any ring.
 我们现在可以给出简单根存在的标准。第一个命题适用于任何环。

Proposition 29.25. Let A be any ring. For every nonnull polynomial f ∈ A[X], α ∈ A is a simple root of f iff α is a root of f and α is not a root of f0.
 提案29.25。让A成为任何戒指。对于每一个非零多项式f∈a[x]，α∈a是f的简单根iffα是f的根，α不是f0的根。

Proof. Since α ∈ A is a root of f, we have f = (X − α)g for some g ∈ A[X]. Now, α is a simple root of f iff g(α) = 06 . However, we have f0 = g + (X − α)g0, and so f0(α) = g(α). Thus, α is a simple root of f iff f0(α) = 0.6   
 证据。因为α∈a是f的根，所以对于一些g∈a[x]，我们有f=（x−α）g。现在，α是f iff g（α）=06的简单根。然而，我们有f0=g+（x-α）g0，所以f0（α）=g（α）。因此，α是f iff f0（α）=0.6的简单根。

We can improve the previous proposition as follows.
 我们可以把前面的建议改进如下。

Proposition 29.26. Let A be any ring. For every nonnull polynomial f ∈ A[X], let α ∈ A be a root of multiplicity k ≥ 1 of f. Then, α is a root of multiplicity at least k − 1 of f0. If A is a field of characteristic zero, then α is a root of multiplicity k − 1 of f0.
 提案29.26。让A成为任何戒指。对于每一个非零多项式f∈a[x]，设α∈a为f的重数k≥1的根，则α为f0的重数k-1的根。如果a是特征零的场，那么α是f0的重数k−1的根。

Proof. Since α ∈ A is a root of multiplicity k of f, we have f = (X−α)kg for some g ∈ A[X] and g(α) = 06 . Since
 证据。由于α∈a是f的多重性k的根，对于某些g∈a[x]和g（α）=06，我们得到f=（x−α）kg。自从

f0 = k(X − α)k−1g + (X − α)kg0 = (X − α)k−1(kg + (X − α)g0),
 f0=k（x−α）k−1g+（x−α）k g0=（x−α）k−1（kg+（x−α）g0），

it is clear that the multiplicity of α w.r.t. f0 is at least k−1. Now, (kg+(X−α)g0)(α) = kg(α), and if A is of characteristic zero, since g(α) = 06 , then kg(α) = 06 . Thus, α is a root of multiplicity k − 1 of f0.       
 很明显，αw.r.t.f0的多重性至少为k-1。现在，（kg+（x−α）g0）（α）=kg（α），如果a为特征零，因为g（α）=06，那么kg（α）=06。因此，α是f0的重数k−1的根。

As a consequence, we obtain the following test for the existence of a root of multiplicity k for a polynomial f:
 因此，我们对多项式f的多重性k的根的存在性进行了以下测试：

Given a field K of characteristic zero, for any nonnull polynomial f ∈ K[X], any α ∈ K is a root of multiplicity k ≥ 1 of f iff α is a root of f,D1f,D2f,...,Dk−1f, but not a root of Dkf.
 给定特征零的K域，对于任意非零多项式f∈k[x]，任意α∈k是f的重数k≥1的根iffα是f，d1f，d2f，…，dk−1f的根，而不是dkf的根。

We can now return to polynomial functions and tie up some loose ends. Given a ring A, recall that every polynomial f ∈ A[X1,...,Xn] induces a function fA : An → A defined such that fA(α1,...,αn) = f(α1,...,αn), for every (α1,...,αn) ∈ An. We now give a sufficient condition for the mapping f 7→ fA to be injective.
 现在我们可以返回多项式函数，并绑定一些松散的端点。对于一个环A，回想一下，每个多项式f∈a[x1，…，xn]都会产生一个函数fa:a n→a，定义为fa（α1，…，αn）=f（α1，…，αn），对于每个（α1，…，αn）∈an。我们现在给出了映射f 7→f a是内射的充分条件。

Proposition 29.27. Let A be an integral domain. For every polynomial f ∈ A[X1,...,Xn], if A1,...,An are n infinite subsets of A such that f(α1,...,αn) = 0 for all (α1,...,αn) ∈ A1 ×···×An, then f = 0, i.e., f is the null polynomial. As a consequence, if A is an infinite integral domain, then the map f 7→ fA is injective.
 提案29.27。设A为积分域。对于每一个多项式f∈a[x1，…，xn]，如果a1，…，a n是a的n个无限子集，这样f（α1，…，αn）=0表示全部（α1，…，αn）∈a1×······×an，那么f=0，即f是零多项式。因此，如果a是一个无穷大的积分域，那么映射f 7→fa是内射的。

Proof. We proceed by induction on n. Assume n = 1. If f ∈ A[X1] is nonnull, let m = deg(f) be its degree. Since A1 is infinite and f(α1) = 0 for all α1 ∈ A1, then f has an infinite number of roots. But since f is of degree m, this contradicts Theorem 29.23. Thus, f = 0. If n ≥ 2, we can view f ∈ A[X1,...,Xn] as a polynomial
 证据。我们从n开始归纳，假设n=1。如果f∈a[x1]为非空，则m=deg（f）为其度。因为a1是无穷大的，而f（α1）=0对于所有α1∈a1，那么f有无穷多的根。但由于f是m级的，这与定理29.23相矛盾。因此，f=0。如果n≥2，我们可以把f∈a[x1，…，xn]看作一个多项式。

,
 ，

where the coefficients gi are polynomials in A[X1,...,Xn−1]. Now, for every (α1,...,αn−1) ∈ A1 ×···×An−1, f(α1,...,αn−1,Xn) determines a polynomial h(Xn) ∈ A[Xn], and since An is infinite and h(αn) = f(α1,...,αn−1,αn) = 0 for all αn ∈ An, by the induction hypothesis, we have gi(α1,...,αn−1) = 0. Now, since A1,...,An−1 are infinite, using the induction hypothesis again, we get gi = 0, which shows that f is the null polynomial. The second part of the proposition follows immediately from the first, by letting Ai = A. 
 其中，系数gi是a[x1，…，xn−1]中的多项式。现在，对于每一个（α1，…，αn-1）∈a1×·······································································现在，由于a1，…，a−1是无限的，再次使用归纳假设，我们得到gi=0，这表明f是零多项式。命题的第二部分紧接着从第一部分开始，让ai=a。

When A is an infinite integral domain, in particular an infinite field, since the map f 7→ fA is injective, we identify the polynomial f with the polynomial function fA, and we write fA simply as f.
 当a是一个无限积分域，特别是一个无限域时，由于图f 7→fa是内射的，我们用多项式函数fa来标识多项式f，并将fa简单地写为f。

The following proposition can be very useful to show polynomial identities.
 下面的命题对于证明多项式恒等式是非常有用的。

Proposition 29.28. Let A be an infinite integral domain and f,g1,...,gm ∈ A[X1,...,Xn] be polynomials. If the gi are nonnull polynomials and if
 提案29.28。设a为无穷积分域，f，g1，…，gm∈a[x1，…，xn]为多项式。如果gi是非空多项式，如果

​                                 f(α1,...,αn) = 0 whenever gi(α1,...,αn) 6= 0        for all i, 1 ≤ i ≤ m,
 当所有i的gi（α1，…，αn）6=0，1≤i≤m时，f（α1，…，αn）=0，

for every (α1,...,αn) ∈ An, then
 对于每个（α1，…，αn）∈an，那么

f = 0,
 f＝0，

i.e., f is the null polynomial.
 也就是说，F是零多项式。

Proof. If f is not the null polynomial, since the gi are nonnull and A is an integral domain, then the product fg1 ···gm is nonnull. By Proposition 29.27, only the null polynomial maps to the zero function, and thus there must be some (α1,...,αn) ∈ An, such that
 证据。如果f不是零多项式，因为gi是非零的，a是一个整型域，那么积fg1····gm是非零的。根据命题29.27，只有零多项式映射到零函数，因此必须有一些（α1，…，αn）∈an，这样

​                                                 f(α1,...,αn)g1(α1,...,αn)···gm(α1,...,αn) = 06       ,
 F（α1，…，αn）g1（α1，…，αn）···gm（α1，…，αn）=06，

​        but this contradicts the hypothesis.                                                                                                
 但这与假设相矛盾。

Proposition 29.28 is often called the principle of extension of algebraic identities. Another perhaps more illuminating way of stating this proposition is as follows: For any polynomial g ∈ A[X1,...,Xn], let
 命题29.28常被称为代数恒等式的推广原理。另一种可能更具启发性的表述这个命题的方法是：对于任何多项式g∈a[x1，…，xn]，让

V (g) = {(α1,...,αn) ∈ An | g(α1,...,αn) = 0},
 v（g）=（α1，…，αn）∈an g（α1，…，αn）=0，

the set of zeros of g. Note that V (g1)∪···∪V (gm) = V (g1 ···gm). Then, Proposition 29.28 can be stated as:
 G的零点集合。注意V（g1）·····································那么，29.28号提案可以表述为：

If f(α1,...,αn) = 0 for every (α1,...,αn) ∈ An − V (g1 ···gm), then f = 0.
 如果f（α1，…，αn）=0，对于每（α1，…，αn）∈an−v（g1···gm），则f=0。

In other words, if the algebraic identity f(α1,...,αn) = 0 holds on the complement of V (g1) ∪ ··· ∪ V (gm) = V (g1 ···gm), then f(α1,...,αn) = 0 holds everywhere in An. With this second formulation, we understand better the terminology “principle of extension of algebraic identities.”
 换句话说，如果代数恒等式f（α1，…，αn）=0保留V（g1）·············································通过第二个公式，我们更好地理解术语“代数恒等式的扩展原理”。


 

Remark: Letting U(g) = A−V (g), the identity V (g1)∪···∪V (gm) = V (g1 ···gm) translates to U(g1) ∩ ··· ∩ U(gm) = U(g1 ···gm). This suggests to define a topology on A whose basis of open sets consists of the sets U(g). In this topology (called the Zariski topology), the sets of the form V (g) are closed sets. Also, when g1,...,gm ∈ A[X1,...,Xn] and n ≥ 2, understanding the structure of the closed sets of the form V (g1)∩···∩V (gm) is quite difficult, and it is the object of algebraic geometry (at least, its classical part).
 备注：让u（g）=a−v（g），单位v（g1）···············································这就建议定义一个拓扑，在这个拓扑的基础上，开放集由集U（G）组成。在这个拓扑（称为zariski拓扑）中，V（G）形式的集合是闭集合。另外，当g1，…，gm∈a[x1，…，xn]和n≥2时，理解形式v（g1）·v（gm）闭集的结构是相当困难的，它是代数几何的对象（至少是它的经典部分）。

 When f ∈ A[X1,...,Xn] and n ≥ 2, one should not apply Proposition 29.27 abusively. For example, let
 当f∈a[x1，…，xn]且n≥2时，不应滥用29.27号命题。例如，让

f(X,Y ) = X2 + Y 2 − 1,
 F（x，y）=x2+y 2−1，

considered as a polynomial in R[X,Y ]. Since R is an infinite field and since
 在r[x，y]中被认为是多项式。因为r是一个无限的场

,
 ，

for every t ∈ R, it would be tempting to say that f = 0. But what’s wrong with the above reasoning is that there are no two infinite subsets R1,R2 of R such that f(α1,α2) = 0 for all (α1,α2) ∈ R2. For every α1 ∈ R, there are at most two α2 ∈ R such that f(α1,α2) = 0. What the example shows though, is that a nonnull polynomial f ∈ A[X1,...,Xn] where n ≥ 2 can have an infinite number of zeros. This is in contrast with nonnull polynomials in one variables over an infinite field (which have a number of roots bounded by their degree).
 对于每一个t∈r，我们都会倾向于说f=0。但上述推理的错误之处在于，R中没有两个无穷大的子集r1，r2，因此f（α1，α2）=0表示所有（α1，α2）∈r2。对于每个α1∈r，至多有两个α2∈r，使得f（α1，α2）=0。然而，示例显示，非空多项式f∈a[x1，…，xn]其中n≥2可以有无限个零。这与无限域上一个变量中的非空多项式形成对比（该变量的根数受其阶数的限制）。

We now look at polynomial interpolation.
 现在我们来看看多项式插值。

## 29.7     Polynomial Interpolation (Lagrange, Newton, Hermite)  29.7多项式插值（拉格朗日、牛顿、赫米特）

Let K be a field. First, we consider the following interpolation problem: Given a sequence
 让k成为一个场。首先，我们考虑以下插值问题：给定一个序列

(α1,...,αm+1) of pairwise distinct scalars in K and any sequence (β1,...,βm+1) of scalars in K, where the βj are not necessarily distinct, find a polynomial P(X) of degree ≤ m such that
 （α1，…，αm+1）k中的成对不定标度和k中的任何标度序列（β1，…，βm+1），其中βj不一定是不同的，求一个次数≤m的多项式p（x），这样

P(α1) = β1,...,P(αm+1) = βm+1.
 P（α1）=β1，…，P（αm+1）=βm+1。

First, observe that if such a polynomial exists, then it is unique. Indeed, this is a consequence of Proposition 29.24. Thus, we just have to find any polynomial of degree ≤ m. Consider the following so-called Lagrange polynomials:
 首先，观察这样一个多项式是否存在，那么它是唯一的。事实上，这是29.24号提案的结果。因此，我们只需要找到任何次数≤m的多项式。考虑以下所谓的拉格朗日多项式：

.
 .

​           Note that L(αi) = 1 and that L(αj) = 0, for all j =6      i. But then,
 注意，l（αi）=1，l（αj）=0，对于所有j=6 i，但是，

P(X) = β1L1 + ··· + βm+1Lm+1
 P（x）=β1l1+····+βm+1lm+1

is the unique desired polynomial, since clearly, P(αi) = βi. Such a polynomial is called a Lagrange interpolant. Also note that the polynomials (L1,...,Lm+1) form a basis of the vector space of all polynomials of degree ≤ m. Indeed, if we had
 是唯一的期望多项式，因为很明显，p（αi）=βi。这样的多项式称为拉格朗日插值。还需要注意的是，多项式（l1，…，lm+1）构成了度≤m的所有多项式的向量空间的基础。

λ1L1(X) + ··· + λm+1Lm+1(X) = 0,
 λ1l1（x）+·····+λm+1lm+1（x）=0，

setting X to αi, we would get λi = 0. Thus, the Li are linearly independent, and by the previous argument, they are a set of generators. We we call (L1,...,Lm+1) the Lagrange basis (of order m + 1).
 将x设为αi，我们得到λi=0。因此，li是线性独立的，根据前面的论证，它们是一组生成器。我们称（l1，…，lm+1）为拉格朗日基（m+1阶）。

It is known from numerical analysis that from a computational point of view, the Lagrange basis is not very good. Newton proposed another solution, the method of divided differences. Consider the polynomial P(X) of degree ≤ m, called the Newton interpolant,
 从数值分析可知，从计算的角度来看，拉格朗日基不是很好。牛顿提出了另一种解决方法，差分法。考虑次数≤m的多项式p（x），称为牛顿插值，

P(X) = λ0 + λ1(X − α1) + λ2(X − α1)(X − α2) + ··· + λm(X − α1)(X − α2)···(X − αm).
 p（x）=λ0+λ1（x-α1）+λ2（x-α1）（x-α2）+····+λm（x-α1）（x-α2）···（x-αm）。

Then, the λi can be determined by successively setting X to, α1,α2,...,αm+1. More precisely, we define inductively the polynomials Q(X) and Q(α1,...,αi,X), for 1 ≤ i ≤ m, as follows:
 然后，通过依次将x设置为，α1，α2，…，αm+1来确定λi。更准确地说，我们归纳地定义了1≤i≤m的多项式q（x）和q（α1，…，αi，x），如下：

.
 .

By induction on i, 1 ≤ i ≤ m − 1, it is easily verified that
 通过对i的感应，1≤i≤m−1，很容易证实

Q(X) = P(X),
 Q（x）=P（x）

Q(α1,...,αi,X) = λi + λi+1(X − αi+1) + ··· + λm(X − αi+1)···(X − αm), Q(α1,...,αm,X) = λm.
 q（α1，…，αi，x）=λi+λi+1（x−αi+1）+······+λm（x−αi+1）··（x−αm），q（α1，…，αm，x）=λm。

From the above expressions, it is clear that
 从上面的表达式可以清楚地看出

λ0 = Q(α1), λi = Q(α1,...,αi,αi+1), λm = Q(α1,...,αm,αm+1).
 λ0=q（α1），λi=q（α1，…，αi，αi+1），λm=q（α1，…，αm，αm+1）。

The expression Q(α1,α2,...,αi+1) is called the i-th difference quotient. Then, we can compute the λi in terms of β1 = P(α1),...,βm+1 = P(αm+1), using the inductive formulae for the Q(α1,...,αi,X) given above, initializing the Q(αi) such that Q(αi) = βi.
 表达式q（α1，α2，…，αi+1）称为第i个差商。然后，我们可以根据β1=p（α1），…，βm+1=p（αm+1）计算λi，使用上面给出的q（α1，…，αi，x）的归纳公式，初始化q（αi），使q（αi）=βi。

The above method is called the method of divided differences and it is due to Newton.
 上述方法称为差分法，它是牛顿的结果。

An astute observation may be used to optimize the computation. Observe that if Pi(X) is the polynomial of degree ≤ i taking the values β1,...,βi+1 at the points α1,...,αi+1, then the coefficient of Xi in Pi(X) is Q(α1,α2,...,αi+1), which is the value of λi in the Newton interpolant
 一个敏锐的观察可以用来优化计算。若皮（x）是在α1、α、αi＋1点取β1、…、βi＋1的值的多项式，则Xi在pi（x）中的系数是q（α1，α2，…，αi+1），这是牛顿插值中λi的值。

Pi(X) = λ0 + λ1(X − α1) + λ2(X − α1)(X − α2) + ··· + λi(X − α1)(X − α2)···(X − αi).
 Pi（x）=λ0+λ1（x−α1）+λ2（x−α1）（x−α2）+····+λi（x−α1）（x−α2）···（x−αi）。

As a consequence, Q(α1,α2,...,αi+1) does not depend on the specific ordering of the αj and there are better ways of computing it. For example, Q(α1,α2,...,αi+1) can be computed using
 因此，q（α1，α2，…，αi+1）不依赖于αj的特定顺序，有更好的计算方法。例如，q（α1，α2，…，αi+1）可以用

.
 .

Then, the computation can be arranged into a triangular array reminiscent of Pascal’s triangle, as follows:
 然后，可以将计算安排成一个类似于帕斯卡三角形的三角形数组，如下所示：

Initially, Q(αj) = βj, 1 ≤ j ≤ m + 1, and
 最初，q（αj）=βj，1≤j≤m+1，以及

Q(α1)
 Q（α1）

Q(α1,α2)
 Q（α1，α2）

Q(α2) Q(α1,α2,α3) Q(α2,α3)   ...
 Q（α2）Q（α1，α2，α3）Q（α2，α3）……

Q(α3)    Q(α2,α3,α4) Q(α3,α4) ...
 Q（α3）Q（α2，α3，α4）Q（α3，α4）……

​                                                      Q(α4)          ...
 Q（α4）

...
 …

In this computation, each successive column is obtained by forming the difference quotients of the preceeding column according to the formula
 在该计算中，每个连续列都是通过根据公式形成前一列的差商得到的。

.
 .

The λi are the elements of the descending diagonal.
 λi是下对角线的元素。

Observe that if we performed the above computation starting with a polynomial Q(X) of degree m, we could extend it by considering new given points αm+2, αm+3, etc. Then, from what we saw above, the (m + 1)th column consists of λm in the expression of Q(X) as a Newton interpolant and the (m + 2)th column consists of zeros. Such divided differences are used in numerical analysis.
 观察到，如果我们从m次的多项式q（x）开始进行上述计算，我们可以通过考虑新的给定点αm+2、αm+3等来扩展它。然后，从我们上面看到的，（m+1）第列由q（x）表示为牛顿插值的λm和（m+2）t组成。H列由零组成。在数值分析中使用了这种分离的差异。

Newton’s method can be used to compute the value P(α) at some α of the interpolant
 牛顿方法可以用来计算插值函数中某些α处的p（α）

P(X) taking the values β1,...,βm+1 for the (distinct) arguments α1,...,αm+1. We also mention that inductive methods for computing P(α) without first computing the coefficients of the Newton interpolant exist, for example, Aitken’s method. For this method, the reader is referred to Farin [59].
 p（x）取β1，…，βm+1作为（不同的）参数α1，…，αm+1。我们还提到了在不首先计算牛顿插值系数的情况下计算p（α）的归纳法，例如艾特肯方法。对于这种方法，读者可以参考法林[59]。

It has been observed that Lagrange interpolants oscillate quite badly as their degree increases, and thus, this makes them undesirable as a stable method for interpolation. A standard example due to Runge, is the function
 据观察，拉格朗日插值函数随着其阶数的增加而振荡得很厉害，因此，这使得拉格朗日插值函数不适合作为一种稳定的插值方法。一个标准的例子，由于梯级，是函数

,
 ，

in the interval [−5, +5]. Assuming a uniform distribution of points on the curve in the interval [−5, +5], as the degree of the Lagrange interpolant increases, the interpolant shows wilder and wilder oscillations around the points x = −5 and x = +5. This phenomenon becomes quite noticeable beginning for degree 14, and gets worse and worse. For degree 22, things are quite bad! Equivalently, one may consider the function
 在区间[-5，+5]。假设曲线上点在区间[-5，+5]内的均匀分布，随着拉格朗日插值程度的增加，插值在点x=-5和x=+5周围显示出更狂野和更狂野的振荡。这种现象在14度开始时变得相当明显，并且越来越严重。对于22级，情况相当糟糕！等价地，我们可以考虑函数

,
 ，

in the interval [−1, +1].
 在区间[−1，+1]。

We now consider a more general interpolation problem which will lead to the Hermite polynomials.
 我们现在考虑一个更普遍的插值问题，它将导致厄米多项式。

We consider the following interpolation problem:
 我们考虑以下插值问题：

Given a sequence (α1,...,αm+1) of pairwise distinct scalars in K, integers n1,...,nm+1 where nj ≥ 0, and m + 1 sequences () of scalars in K, letting
 给定一个k中成对不同标量的序列（α1，…，αm+1），整数n1，…，nm+1，其中nj≥0，m+1，k中标量的序列（），让

n = n1 + ··· + nm+1 + m,
 n=n1+·····+n m+1+m，

find a polynomial P of degree ≤ n, such that
 求一个多项式p的次数≤n，这样

,
 ，

​                                              D1P(α1) = β11,      ...      D1P(αm+1) = βm1 +1,
 d1p（α1）=β11，…d1p（αm+1）=βm1+1，

...
 …

​                                                               D     ,       ...                       D,
 D，…D，，

...
 …

D.
 d.

Note that the above equations constitute n+1 constraints, and thus, we can expect that there is a unique polynomial of degree ≤ n satisfying the above problem. This is indeed the case and such a polynomial is called a Hermite polynomial. We call the above problem the Hermite interpolation problem.
 请注意，上述方程构成n+1约束，因此，我们可以期望有一个满足上述问题且次数≤n的唯一多项式。这确实是这样的情况，这样的多项式被称为埃尔米特多项式。我们将上述问题称为埃尔米特插值问题。

Proposition 29.29. The Hermite interpolation problem has a unique solution of degree ≤ n, where n = n1 + ··· + nm+1 + m.
 提案29.29。埃尔米特插值问题有一个唯一的解，即n=n1+·····+n m+1+m。

Proof. First, we prove that the Hermite interpolation problem has at most one solution. Assume that P and Q are two distinct solutions of degree ≤ n. Then, by Proposition 29.26 and the criterion following it, P −Q has among its roots α1 of multiplicity at least n1 +1,..., αm+1 of multiplicity at least nm+1 + 1. However, by Theorem 29.23, we should have
 证据。首先，我们证明了厄米插值问题至多只有一个解。假设p和q是两个不同的度≤n的解，那么，根据命题29.26及其后的标准，p−q在多重性的根α1中至少有n1+1，…，多重性的αm+1至少有nm+1+1。然而，根据定理29.23，我们应该

n1 + 1 + ··· + nm+1 + 1 = n1 + ··· + nm+1 + m + 1 ≤ n,
 n1+1+······+n m+1+1=n1+·····+nm+1+m+1≤n，

which is a contradiction, since n = n1 + ··· + nm+1 + m. Thus, P = Q. We are left with proving the existence of a Hermite interpolant. A quick way to do so is to use Proposition 6.13, which tells us that given a square matrix A over a field K, the following properties hold:
 这是一个矛盾，因为n=n1+·····+n m+1+m。因此，p=q。我们只剩下证明一个埃尔米特插值的存在。这样做的一个快速方法是使用命题6.13，它告诉我们，给定一个域k上的平方矩阵a，以下属性成立：

For every column vector B, there is a unique column vector X such that AX = B iff the only solution to AX = 0 is the trivial vector X = 0 iff D(A) = 0.6
 对于每个列向量b，都有一个唯一的列向量x，这样ax=b iff，ax=0的唯一解是平凡向量x=0 iff d（a）=0.6。

If we let P = y0 + y1X + ··· + ynXn, the Hermite interpolation problem yields a linear system of equations in the unknowns (y0,...,yn) with some associated (n+1)×(n+1) matrix A. Now, the system AY = 0 has a solution iff P has among its roots α1 of multiplicity at least n1 + 1,..., αm+1 of multiplicity at least nm+1 + 1. By the previous argument, since P has degree ≤ n, we must have P = 0, that is, Y = 0. This concludes the proof. 
 如果p=y0+y1x+·····+ynxn，厄米特插值问题在未知（y0，…，yn）中产生一个线性方程组，其中有一些相关（n+1）×n+1）矩阵a。现在，系统ay=0有一个解，如果p在其多重性的根α1中至少有n1+1，…，αm+1，mul滴度至少为nm+1+1。根据前面的论点，由于p的度数≤n，我们必须有p=0，即y=0。这就是证据的结论。

Proposition 29.29 shows the existence of unique polynomials Hji(X) of degree ≤ n such that D ) = 1 and D ) = 0, for k =6 i or l =6 j, 1 ≤ j,l ≤ m + 1, 0 ≤ i,k ≤ nj.
 命题29.29显示了度≤n的唯一多项式hji（x）的存在，使得d=1和d=0，对于k=6 i或l=6 j，1≤j，l≤m+1，0≤i，k≤nj。

The polynomials Hji are called Hermite basis polynomials.
 多项式hji称为Hermite基多项式。

One problem with Proposition 29.29 is that it does not give an explicit way of computing the Hermite basis polynomials. We first show that this can be done explicitly in the special cases n1 = ... = nm+1 = 1, and n1 = ... = nm+1 = 2, and then suggest a method using a generalized Newton interpolant.
 29.29号命题的一个问题是，它没有给出计算厄米特基多项式的明确方法。我们首先表明，这可以在特殊情况下显式地做到n1=……=nm+1=1，n1=……=nm+1=2，然后建议使用广义牛顿插值法。

​                   Assume that n1 = ... = nm+1 = 1.                     We try Hj0 = (a(X − αj) + b)L2j, and Hj1 =
 假设n1=…=nm+1=1。我们尝试hj0=（a（x−αj）+b）l2j和hj1=

(c(X − αj) + d)L2j, where Lj is the Lagrange interpolant determined earlier. Since
 （c（x−αj）+d）L2j，其中Lj是前面确定的拉格朗日插值。自从

DHj0 = aL2j + 2(a(X − αj) + b)LjDLj,
 dhj0=al2j+2（a（x−αj）+b）ljdlj，

requiring that Hj0(αj) = 1, Hj0(αk) = 0, DHj0(αj) = 0, and DHj0(αk) = 0, for k =6 j, implies b = 1 and a = −2DLj(αj). Similarly, from the requirements Hj1(αj) = 0, Hj1(αk) = 0, DHj1(αj) = 1, and DHj1(αk) = 0, k 6= j, we get c = 1 and d = 0.
 要求hj0（αj）=1，hj0（αk）=0，dhj0（αj）=0和dhj0（αk）=0，对于k=6 j，意味着b=1和a=-2dlj（αj）。同样，根据要求hj1（αj）=0，hj1（αk）=0，dhj1（αj）=1，dhj1（αk）=0，k 6=j，我们得到c=1，d=0。

Thus, we have the Hermite polynomials
 因此，我们有埃尔米特多项式

​                                       Hj0 = (1 − 2DLj(αj)(X − αj))Lj2,            Hj1 = (X − αj)L2j.
 hj0=（1−2dlj（αj）（x−αj））lj2，hj1=（x−αj）l2j。

In the special case where m = 1, α1 = 0, and α2 = 1, we leave as an exercise to show that the Hermite polynomials are
 在m=1，α1=0，α2=1的特殊情况下，我们将作为一个练习来证明厄米特多项式是

H00 = 2X3 − 3X2 + 1,
 h00=2x3−3x2+1，

H10 = −2X3 + 3X2, H01 = X3 − 2X2 + X, H11 = X3 − X2.
 h10=−2x3+3x2，h01=x3−2x2+x，h11=x3−x2。

As a consequence, the polynomial P of degree 3 such that P(0) = x0, P(1) = x1, P 0(0) = m0, and P 0(1) = m1, can be written as
 因此，阶数为3的多项式p，如p（0）=x0，p（1）=x1，p 0（0）=m0，p 0（1）=m1，可以写成

P(X) = x0(2X3 − 3X2 + 1) + m0(X3 − 2X2 + X) + m1(X3 − X2) + x1(−2X3 + 3X2).
 P（x）=X0（2x3−3x2+1）+m0（x3−2x2+x）+m1（x3−x2）+x1（−2x3+3x2）。

If we want the polynomial P of degree 3 such that P(a) = x0, P(b) = x1, P 0(a) = m0, and P 0(b) = m1, where b =6 a, then we have
 如果我们想要三次多项式p，这样p（a）=x0，p（b）=x1，p 0（a）=m0，p 0（b）=m1，其中b=6a，那么我们得到

P(X) = x0(2t3 − 3t2 + 1) + (b − a)m0(t3 − 2t2 + t) + (b − a)m1(t3 − t2) + x1(−2t3 + 3t2), where
 p（x）=x0（2t3−3t2+1）+（b−a）m0（t3−2t2+t）+（b−a）m1（t3−t2）+x1（−2t3+3t2），其中

.
 .

Observe the presence of the extra factor () in front of m0 and m1, the formula would be false otherwise!
 观察m0和m1前面的额外因子（）的存在，否则公式将为假！

We now consider the case where n1 = ... = nm+1 = 2. Let us try
 我们现在考虑一下n1=的情况。=nm+1=2。让我们试试看

Hji(X) = (ai(X − αj)2 + bi(X − αj) + ci)L3j,
 hji（x）=（ai（x−αj）2+bi（x−αj）+ci）l3j，

where 0 ≤ i ≤ 2. Sparing the readers some (tedious) computations, we find:
 其中0≤i≤2。除了读者的一些（繁琐）计算，我们发现：

,
 ，

Going back to the general problem, it seems to us that a kind of Newton interpolant will be more manageable. Let
 回到一般问题，在我们看来，一种牛顿插值法将更易于管理。让

P00(X) = 1,
 p00（x）=1，

Pj0(X) = (X − α1)n1+1 ···(X − αj)nj+1, 1 ≤ j ≤ m
 Pj0（x）=（x−α1）n1+1···（x−αj）nj+1，1≤j≤m

P0i(X) = (X − α1)i(X − α2)n2+1 ···(X − αm+1)nm+1+1, 1 ≤ i ≤ n1,
 p0i（x）=（x−α1）i（x−α2）n2+1····（x−αm+1）nm+1+1，1≤i≤n1，

Pji(X) = (X − α1)n1+1 ···(X − αj)nj+1(X − αj+1)i(X − αj+2)nj+2+1 ···(X − αm+1)nm+1+1,
 Pji（x）=（x−α1）n1+1···（x−αj）nj+1（x−αj+1）i（x−αj+2）nj+2+1···（x−αm+1）nm+1+1，

1 ≤ j ≤ m − 1, 1 ≤ i ≤ nj+1,
 1≤j≤m−1，1≤i≤nj+1，

Pmi (X) = (X − α1)n1+1 ···(X − αm)nm+1(X − αm+1)i, 1 ≤ i ≤ nm+1,
 pmi（x）=（x−α1）n1+1···（x−αm）nm+1（x−αm+1）i，1≤i≤nm+1，

and let
 让

j=m,i=nj+1
 j=m，i=nj+1

P(X) = X λijPji(X).
 p（x）=xλijpji（x）。

j=0,i=0
 j=0，i=0

We can think of P(X) as a generalized Newton interpolant. We can compute the derivatives D, for 1 ≤ k ≤ nj+1, and if we look for the Hermite basis polynomials ) such that DiHji(αj) = 1 and DkHji(αl) = 0, for k 6= i or l 6= j, 1 ≤ j,l ≤ m + 1, 0 ≤ i,k ≤ nj, we find that we have to solve triangular systems of linear equations. Thus, as in the simple case n1 = ... = nm+1 = 0, we can solve successively for the λij. Obviously, the computations are quite formidable and we leave such considerations for further study.
 我们可以把p（x）看作是广义牛顿插值。我们可以计算1≤k≤nj+1的导数d，如果我们寻找埃尔米特基多项式），那么dihji（αj）=1和dkhji（αl）=0，对于k 6=i或l 6=j，1≤j，l≤m+1，0≤i，k≤nj，我们发现我们必须解线性方程的三角系。因此，在简单情况下，n1=……=nm+1=0，我们可以依次求解λij。显然，这些计算是相当可怕的，我们将这些考虑留作进一步研究。


 