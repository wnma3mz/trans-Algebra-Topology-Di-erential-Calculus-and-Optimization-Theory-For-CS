第三十章

# Annihilating Polynomials and the Primary Decomposition  湮灭多项式与一次分解

In this chapter all vector spaces are defined over an arbitrary field K.
 在本章中，所有的向量空间都是在一个任意的k域上定义的。

In Section 6.7 we explained that if f : E → E is a linear map on a K-vector space E, then for any polynomial p(X) = a0Xd + a1Xd−1 + ··· + ad with coefficients in the field K, we can define the linear map p(f): E → E by
 在第6.7节中，我们解释了如果f:e→e是k向量空间e上的线性映射，那么对于任何多项式p（x）=a0xd+a1xd−1+·········+ad以及字段k中的系数，我们可以通过以下方式定义线性映射p（f）：e→e：

p(f) = a0fd + a1fd−1 + ··· + adid,
 p（f）=a0fd+a1fd−1+····+adid，

where fk = f ◦ ··· ◦ f, the k-fold composition of f with itself. Note that
 式中，f k=f·····f，f与其自身的k-折叠组成。注意

p(f)(u) = a0fd(u) + a1fd−1(u) + ··· + adu,
 p（f）（u）=a0fd（u）+a1fd−1（u）+·····+adu，

for every vector u ∈ E. Then we showed that if E is finite-dimensional and if χf(X) = det(XI −f) is the characteristic polynomial of f, by the Cayley–Hamilton theorem, we have
 对于每个向量uε，我们证明了如果E是有限维的，并且如果χf（x）＝DET（Xi—f）是f的特征多项式，则通过Cayley -汉密尔顿定理，我们得到了。

χf(f) = 0.
 χf（f）=0。

This fact suggests looking at the set of all polynomials p(X) such that
 这一事实表明，研究所有多项式的集合p（x），这样

p(f) = 0.
 p（f）=0.

Such polynomials are called annihilating polynomials of f, the set of all these polynomials, denoted Ann(f), is called the annihilator of f, and the Cayley-Hamilton theorem shows that it is nontrivial since it contains a polynomial of positive degree. It turns out that Ann(f) contains a polynomial mf of smallest degree that generates Ann(f), and this polynomial divides the characteristic polynomial. Furthermore, the polynomial mf encapsulates a lot of information about f, in particular whether f can be diagonalized. One of the main reasons for this is that a scalar λ ∈ K is a zero of the minimal polynomial mf if and only if λ is an eigenvalue of f.
 这类多项式称为F的湮灭多项式，所有这些多项式的集合称为F的湮灭子，Cayley-Hamilton定理表明，它包含一个正度多项式，因此是不平凡的。结果表明，ann（f）包含一个生成ann（f）的最小阶多项式mf，该多项式对特征多项式进行了划分。此外，多项式mf还封装了许多关于f的信息，特别是f是否可以对角化。其主要原因之一是当且仅当λ是f的特征值时，标量λ∈k是最小多项式mf的零。

991
 九百九十一

The first main result is Theorem 30.6 which states that if f : E → E is a linear map on a finite-dimensional space E, then f is diagonalizable iff its minimal polynomial m is of the form
 第一个主要结果是定理30.6，它指出，如果f:e→e是有限维空间e上的线性映射，那么f是可对角化的，如果其最小多项式m是形式

m = (X − λ1)···(X − λk),
 m=（x−λ1）···（x−λk），

where λ1,...,λk are distinct elements of K.
 其中，λ1，…，λk是k的不同元素。

One of the technical tools used to prove this result is the notion of f-conductor; see Definition 30.2. As a corollary of Theorem 30.6 we obtain results about finite commuting families of diagonalizable or triangulable linear maps.
 证明这一结果的技术工具之一是F导体的概念；见定义30.2。作为定理30.6的推论，我们得到了对角化或三角化线性映射的有限交换族的结果。

If f : E → E is a linear map and λ ∈ K is an eigenvalue of f, recall that the eigenspace Eλ associated with λ is the kernel of the linear map λid − f. If all the eigenvalues λ1 ...,λk of f are in K and if f is diagonalizable, then
 如果f:e→e是一个线性映射，而λ∈k是f的特征值，回想一下，与λ相关联的特征空间eλ是线性映射的核心，即λid−f。如果所有特征值λ1…，则f的λk都是k，如果f是可对角化的，则

E = Eλ1 ⊕ ··· ⊕ Eλk,
 e=eλ1···eλk，

but in general there are not enough eigenvectors to span E. A remedy is to generalize the notion of eigenvector and look for (nonzero) vectors u (called generalized eigenvectors) such that
 但是，一般来说，没有足够的特征向量跨越e。一种补救方法是概括特征向量的概念，并寻找（非零）向量u（称为广义特征向量），以便

​                                                 (λid − f)r(u) = 0,       for some r ≥ 1.
 （λid−f）r（u）=0，对于某些r≥1。

Then, it turns out that if the minimal polynomial of f is of the form
 如果F的最小多项式是

m = (X − λ1)r1 ···(X − λk)rk,
 m=（x−λ1）r1···（x−λk）Rk，

then r = ri does the job for λi; that is, if we let
 那么r=ri为λi做这个工作；也就是说，如果我们允许

Wi = Ker(λiid − f)ri,
 wi=ker（λiid−f）ri，

then
 然后

E = W1 ⊕ ··· ⊕ Wk.
 E=w1····周。

The above facts are parts of the primary decomposition theorem (Theorem 30.11). It is a special case of a more general result involving the factorization of the minimal polynomial m into its irreducible monic factors; see Theorem 30.10.
 上述事实是主分解定理（定理30.11）的一部分。它是一个更一般的结果的特例，涉及极小多项式m因式分解为其不可约Monic因子；见定理30.10。

Theorem 30.11 implies that every linear map f that has all its eigenvalues in K can be written as f = D + N, where D is diagonalizable and N is nilpotent (which means that Nr = 0 for some positive integer r). Furthermore D and N commute and are unique. This is the Jordan decomposition, Theorem 30.12.
 定理30.11表明，每一个具有k中所有特征值的线性映射f都可以写成f=d+n，其中d是可对角化的，n是幂零的（对于某个正整数r，nr=0）。此外，D和N通勤和独特。这是乔丹分解，定理30.12。

The Jordan decomposition suggests taking a closer look at nilpotent maps. We prove that for any nilpotent linear map f : E → E on a finite-dimensional vector space E of dimension n over a field K, there is a basis of E such that the matrix N of f is of the form
 乔丹的分解意味着仔细观察幂零映射。我们证明了在有限维向量空间E上的任意幂零线性映射f:e→e在k域上存在一个e的基础，使得f的矩阵n的形式为

|     γ   0    零   0 N = ...    0 N=…       γ       γ   0    0       γ   0    零 | ν1    1伏   0    零   ...    …   0    零   0    零 | 0 ν2    0ω2   ...    …   0    零   0    零 | ···    ·········   ···...    ···…   ···    ·········   ···    ········· | 0    零   0    零   ...    …   0    零   0    零 | 0     0℃   0     0℃   ... ,    …，   νn    _n_   0    零 |
| ------------------------------------------------------------ | -------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                    |                                            |                                                              |                                                  |                                                              |


 

30.1. ANNIHILATING POLYNOMIALS AND THE MINIMAL POLYNOMIAL
 30.1。湮灭多项式与极小多项式

where νi = 1 or νi = 0; see Theorem 30.16. As a corollary we obtain the Jordan form; which involves matrices of the form
 式中，νi=1或νi=0；见定理30.16。作为推论，我们得到了乔丹形式；它涉及形式的矩阵。

| λ    γ-α   0    零       γ   . Jr(λ)   = ..    ②Jr（λ）=..       γ       γ   0    千分之一   0    零 | 1 λ    1兆   ...    …   0    零   0    零 | 0    零   1    一   ...    …   0    零   0    零 | ···    ·········   ···...    ···…   ... ···    …········· | 0    0℃   0    0℃   ...,    ……       γ   1 λ    1λ |
| ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------ | --------------------------------------------------------- | --------------------------------------------------------- |
|                                                              |                                           |                                                  |                                                           |                                                           |

called Jordan blocks; see Theorem 30.17.
 称为约旦块；见定理30.17。

## 30.1     Annihilating Polynomials and the Minimal Polynomial  30.1湮灭多项式和最小多项式

Given a linear map f : E → E, it is easy to check that the set Ann(f) of polynomials that annihilate f is an ideal. Furthermore, when E is finite-dimensional, the Cayley–Hamilton Theorem implies that Ann(f) is not the zero ideal. Therefore, by Proposition 29.10, there is a unique monic polynomial mf that generates Ann(f). Results from Chapter 29, especially about gcd’s of polynomials, will come handy.
 给出了一个线性映射f:e→e，很容易证明湮灭f的多项式的集合ann（f）是一个理想。此外，当e是有限维时，凯莱-汉密尔顿定理意味着ann（f）不是零理想。因此，根据命题29.10，有一个唯一的monic多项式mf生成ann（f）。第29章的结果，特别是关于多项式的GCD的结果，将非常有用。

Definition 30.1. If f : E → E is a linear map on a finite-dimensional vector space E, the unique monic polynomial mf(X) that generates the ideal Ann(f) of polynomials which annihilate f (the annihilator of f) is called the minimal polynomial of f.
 定义30.1.如果f:e→e是有限维向量空间e上的一个线性映射，那么产生湮灭f（f的湮灭子）的多项式的理想ann（f）的唯一Monic多项式mf（x）称为f的最小多项式。

The minimal polynomial mf of f is the monic polynomial of smallest degree that annihilates f. Thus, the minimal polynomial divides the characteristic polynomial χf, and deg(mf) ≥ 1. For simplicity of notation, we often write m instead of mf.
 F的最小多项式Mf是最小程度的Monic多项式，将F湮没，因此，最小多项式将特征多项式χf与deg（Mf）≥1相除。为了便于记法，我们经常写m而不是mf。

If A is any n × n matrix, the set Ann(A) of polynomials that annihilate A is the set of polynomials
 如果a是任意n×n矩阵，则湮灭a的多项式的集合ann（a）是多项式的集合。

p(X) = a0Xd + a1Xd−1 + ··· + ad−1X + ad
 P（x）=a0xd+a1xd−1+····+ad−1x+ad

such that
 这样的话

a0Ad + a1Ad−1 + ··· + ad−1A + adI = 0.
 a0ad+a1ad−1+····+ad−1a+adi=0.

It is clear that Ann(A) is a nonzero ideal and its unique monic generator is called the minimal polynomial of A. We check immediately that if Q is an invertible matrix, then A and Q−1AQ have the same minimal polynomial. Also, if A is the matrix of f with respect to some basis, then f and A have the same minimal polynomial.
 很明显，ann（a）是一个非零理想，其唯一的Monic发生器称为a的极小多项式。我们立即检查，如果q是可逆矩阵，那么a和q−1aq具有相同的极小多项式。另外，如果a是关于某个基的f的矩阵，那么f和a有相同的极小多项式。

The zeros (in K) of the minimal polynomial of f and the eigenvalues of f (in K) are intimately related.
 F的最小多项式的零点（k）和F的特征值（k）是密切相关的。

Proposition 30.1. Let f : E → E be a linear map on some finite-dimensional vector space
 提案30.1.设f:e→e为有限维向量空间上的线性映射

E. Then λ ∈ K is a zero of the minimal polynomial mf(X) of f iff λ is an eigenvalue of f iff λ is a zero of χf(X). Therefore, the minimal and the characteristic polynomials have the same zeros (in K), except for multiplicities.
 e.则F iff的最小多项式mf（x）的一个零点，λ是F iff的一个特征值，λ是χf（x）的一个零点。因此，除了多重性外，最小多项式和特征多项式都有相同的零（以k为单位）。

Proof. First assume that m(λ) = 0 (with λ ∈ K, and writing m instead of mf). If so, using polynomial division, m can be factored as
 证据。首先假设m（λ）=0（用λ∈k，写m而不是mf）。如果是这样，使用多项式除法，m可以被分解为

m = (X − λ)q,
 m=（x−λ）q，

with deg(q) < deg(m). Since m is the minimal polynomial, q(f) = 06      , so there is some nonzero vector v ∈ E such that u = q(f)(v) = 06    . But then, because m is the minimal polynomial,
 度（q）<度（m）。因为m是最小多项式，q（f）=06，所以有一些非零向量v∈e，这样u=q（f）（v）=06。但是，因为m是极小多项式，

0 = m(f)(v)
 0=m（f）（v）

= (f − λid)(q(f)(v)) = (f − λid)(u),
 =（f-λid）（q（f）（v））=（f-λid）（u），

which shows that λ is an eigenvalue of f.
 这表明λ是f的特征值。

Conversely, assume that λ ∈ K is an eigenvalue of f. This means that for some u = 06 , we have f(u) = λu. Now it is easy to show that
 相反，假设λ∈k是f的特征值，这意味着对于某些u=06，我们有f（u）=λu，现在很容易证明

m(f)(u) = m(λ)u,
 m（f）（u）=m（λ）u，

and since m is the minimal polynomial of f, we have m(f)(u) = 0, so m(λ)u = 0, and since u = 06 , we must have m(λ) = 0.    
 既然m是f的极小多项式，我们得到m（f）（u）=0，所以m（λ）u=0，既然u=06，我们必须得到m（λ）=0。

Proposition 30.2. Let f : E → E be a linear map on some finite-dimensional vector space E. If f diagonalizable, then its minimal polynomial is a product of distinct factors of degree
 提案30.2.设f:e→e为有限维向量空间e上的线性映射，如果f可对角化，则其最小多项式是各次因子的乘积。

1.
 1。

Proof. If we assume that f is diagonalizable, then its eigenvalues are all in K, and if λ1,...,λk are the distinct eigenvalues of f, and then by Proposition 30.1, the minimal polynomial m of f must be a product of powers of the polynomials (X − λi). Actually, we claim that
 证据。如果我们假设f是可对角化的，那么它的特征值都是k，如果λ1，…，λk是f的独特特征值，那么根据命题30.1，f的最小多项式m必须是多项式（x-λi）的幂的乘积。事实上，我们声称

m = (X − λ1)···(X − λk).
 m=（x−λ1）···（x−λk）。

For this we just have to show that m annihilates f. However, for any eigenvector u of f, one of the linear maps f − λiid sends u to 0, so
 为此，我们只需证明m会湮灭f。然而，对于f的任何特征向量u，其中一个线性映射f−λiid将u发送到0，所以

m(f)(u) = (f − λ1id) ◦ ··· ◦ (f − λkid)(u) = 0.
 m（f）（u）=（f-λ1id）······（f-λkid）（u）=0。

Since E is spanned by the eigenvectors of f, we conclude that
 由于e是由f的特征向量构成的，因此我们得出结论：

​                                                                       m(f) = 0.                                                                       
 m（f）=0.

It turns out that the converse of Proposition 30.2 is true, but this will take a little work to establish it.
 事实证明，30.2号提案的反面是正确的，但这需要一点工作来确定它。

30.2. MINIMAL POLYNOMIALS OF DIAGONALIZABLE LINEAR MAPS
 30.2。对角化线性映射的极小多项式

## 30.2     Minimal Polynomials of Diagonalizable Linear Maps  30.2对角化线性映射的最小多项式

In this section we prove that if the minimal polynomial mf of a linear map f is of the form
 在这一节中，我们证明了如果线性映射f的最小多项式mf是

mf = (X − λ1)···(X − λk)
 Mf=（x−λ1）···（x−λk）

for distinct scalars λ1,...,λk ∈ K, then f is diagonalizable. This is a powerful result that has a number of implications. But first we need of few properties of invariant subspaces.
 对于不同的标量λ1，…，λk∈k，则f是可对角化的。这是一个强有力的结果，有很多含义。但首先我们需要一些不变子空间的性质。

Given a linear map f : E → E, recall that a subspace W of E is invariant under f if f(u) ∈ W for all u ∈ W. For example, if f : R2 → R2 is f(x,y) = (−x,y), the y-axis is invariant under f.
 给出了一个线性映射f:e→e，假设e的子空间w在f下是不变的，如果f（u）对所有u∈w都是不变的，例如，如果f:r2→r2是f（x，y）=（-x，y），y轴在f下是不变的。

Proposition 30.3. Let W be a subspace of E invariant under the linear map f : E → E (where E is finite-dimensional). Then the minimal polynomial of the restriction f | W of f to W divides the minimal polynomial of f, and the characteristic polynomial of f | W divides the characteristic polynomial of f.
 提案30.3.设w为线性映射f:e→e（其中e为有限维）下e不变量的子空间。然后F W的约束F W的最小多项式除F的最小多项式，F W的特征多项式除F的特征多项式。

Sketch of proof. The key ingredient is that we can pick a basis (e1,...,en) of E in which (e1,...,ek) is a basis of W. The matrix of f over this basis is a block matrix of the form
 证明草图。关键因素是我们可以选择e的基（e1，…，en），其中（e1，…，ek）是w的基。在这个基上，f的矩阵是形式的块矩阵。

 ,
 ，

where B is a k × k matrix, D is an (n − k) × (n − k) matrix, and C is a k × (n − k) matrix. Then
 其中b是k×k矩阵，d是（n-k）×n-k矩阵，c是k×n-k矩阵。然后

det(XI − A) = det(XI − B)det(XI − D),
 行列式（XI）a =，

which implies the statement about the characteristic polynomials. Furthermore,
 这意味着关于特征多项式的陈述。此外，

,
 ，

for some k × (n − k) matrix Ci. It follows that any polynomial which annihilates A also annihilates B and D. So the minimal polynomial of B divides the minimal polynomial of A.     
 对于一些k×（n-k）矩阵Ci。由此可知，任何一个歼灭a的多项式也同时歼灭b和d，所以b的极小多项式除以a的极小多项式。

For the next step, there are at least two ways to proceed. We can use an old-fashion argument using Lagrange interpolants, or we can use a slight generalization of the notion of annihilator. We pick the second method because it illustrates nicely the power of principal ideals.
 对于下一步，至少有两种方法可以继续。我们可以用拉格朗日插值来使用一个老式的论点，或者我们可以稍微概括一下湮灭子的概念。我们选择第二种方法是因为它很好地说明了主理想的力量。

What we need is the notion of conductor (also called transporter).
 我们需要的是导体的概念（也称为运输器）。

Definition 30.2. Let f : E → E be a linear map on a finite-dimensional vector space E, let W be an invariant subspace of f, and let u be any vector in E. The set Sf(u,W) consisting of all polynomials q ∈ K[X] such that q(f)(u) ∈ W is called the f-conductor of u into W.
 定义30.2.设f:e→e为有限维向量空间e上的线性映射，设w为f的不变子空间，设u为e中的任意向量，由所有多项式q∈k[x]组成的集sf（u，w），使q（f）（u）∈w称为u到w的f导体。

Observe that the minimal polynomial mf of f always belongs to Sf(u,W), so this is a nontrivial set. Also, if W = (0), then Sf(u,(0)) is just the annihilator of f. The crucial property of Sf(u,W) is that it is an ideal.
 观察到f的最小多项式mf总是属于sf（u，w），所以这是一个非平凡集。另外，如果w=（0），那么sf（u，（0））只是f的湮灭子，sf（u，w）的关键性质是它是一个理想。

Proposition 30.4. If W is an invariant subspace for f, then for each u ∈ E, the f-conductor Sf(u,W) is an ideal in K[X].
 提案30.4.如果w是f的不变子空间，那么对于每个u∈e，f-导体sf（u，w）是k[x]中的理想。

We leave the proof as a simple exercise, using the fact that if W invariant under f, then W is invariant under every polynomial q(f) in Sf(u,W).
 我们将证明留作一个简单的练习，假设w在f下不变，那么w在sf（u，w）中的每个多项式q（f）下不变。

Since Sf(u,W) is an ideal, it is generated by a unique monic polynomial q of smallest degree, and because the minimal polynomial mf of f is in Sf(u,W), the polynomial q divides m.
 因为sf（u，w）是一个理想，它是由一个唯一的最小阶Monic多项式q生成的，并且由于f的最小多项式mf在sf（u，w）中，多项式q除以m。

Definition 30.3. The unique monic polynomial which generates Sf(u,W) is called the conductor of u into W.
 定义30.3.生成sf（u，w）的唯一Monic多项式称为u到w的导体。

Example 30.1. For example, suppose f : R2 → R2 where f(x,y) = (x,0). Observe that W = {(x,0) ∈ R2} is invariant under f. By representing, we see that mf(X) = χf(X) = X2 − X. Let u = (0,y). Then Sf(u,W) = (X) and we say X is the conductor of u into W.
 例30.1。例如，假设f:r2→r2，其中f（x，y）=（x，0）。观察w=（x，0）∈r2在f下是不变的。通过表示，我们看到mf（x）=χf（x）=x2−x。让u=（0，y）。那么sf（u，w）=（x），我们说x是u到w的导体。

Proposition 30.5. Let f : E → E be a linear map on a finite-dimensional space E and assume that the minimal polynomial m of f is of the form
 提案30.5。设f:e→e为有限维空间e上的线性映射，并假定f的最小多项式m的形式为

m = (X − λ1)r1 ···(X − λk)rk,
 m=（x−λ1）r1···（x−λk）Rk，

where the eigenvalues λ1,...,λk of f belong to K. If W is a proper subspace of E which is invariant under f, then there is a vector u ∈ E with the following properties:
 其中，f的特征值λ1，…，λk属于k。如果w是e的一个子空间，在f下不变，则有一个具有以下性质的向量u∈e：

*(a)*    u /∈ W;
 u/∈w；

*(b)*    (f − λid)(u) ∈ W, for some eigenvalue λ of f.
 （f-λid）（u）∈w，对于f的一些特征值λ。

Proof. Observe that (a) and (b) together assert that the conductor of u into W is a polynomial of the form X − λi. Pick any vector v ∈ E not in W, and let g be the conductor of v into W, i.e. g(f)(v) ∈ W. Since g divides m and v /∈ W, the polynomial g is not a constant, and thus it is of the form g = (X − λ1)s1 ···(X − λk)sk,
 证据。观察（a）和（b）一起断言u到w的导体是x-λi形式的多项式，选取任意向量v∈e不在w中，并假设g是v到w的导体，即g（f）（v）∈w，因为g分m和v/∈w，多项式g不是常数，因此它是形式。g=（x−λ1）s1···（x−λk）sk，

with at least some si > 0. Choose some index j such that sj > 0. Then X − λj is a factor of g, so we can write
 至少有一些Si>0。选择一些索引j，使sj>0。那么x-λj是g的一个因子，所以我们可以写

​                                                                    g = (X − λj)q.                                                               (*)
 G=（x−λj）Q.（*）

30.2. MINIMAL POLYNOMIALS OF DIAGONALIZABLE LINEAR MAPS
 30.2。对角化线性映射的极小多项式

By definition of g, the vector u = q(f)(v) cannot be in W, since otherwise g would not be of minimal degree. However, (∗) implies that
 根据g的定义，向量u=q（f）（v）不能在w中，否则g将不具有最小程度。然而，（）意味着

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

is in W, which concludes the proof.                                                                                                  
 在w中，这就是证明的结论。

We can now prove the main result of this section.
 我们现在可以证明这个部分的主要结果。

Theorem 30.6. Let f : E → E be a linear map on a finite-dimensional space E. Then f is diagonalizable iff its minimal polynomial m is of the form
 定理30.6。设f:e→e为有限维空间e上的线性映射，则f是可对角化的，只要其最小多项式m的形式为

m = (X − λ1)···(X − λk),
 m=（x−λ1）···（x−λk），

where λ1,...,λk are distinct elements of K.
 其中，λ1，…，λk是k的不同元素。

Proof. We already showed in Proposition 30.2 that if f is diagonalizable, then its minimal polynomial is of the above form (where λ1,...,λk are the distinct eigenvalues of f).
 证据。我们已经在命题30.2中证明，如果f是可对角化的，那么它的最小多项式就是上述形式（其中，λ1，…，λk是f的独特特征值）。

For the converse, let W be the subspace spanned by all the eigenvectors of f. If W =6 E, since W is invariant under f, by Proposition 30.5, there is some vector u /∈ W such that for some λj, we have
 相反，设w为f的所有特征向量所跨越的子空间。如果w=6e，由于w在f下不变，根据命题30.5，有一些向量u/∈w，因此对于一些λj，我们得到

(f − λjid)(u) ∈ W.
 （f−λjid）（u）∈w.

Let v = (f − λjid)(u) ∈ W. Since v ∈ W, we can write
 设v=（f−λjid）（u）∈w。既然v∈w，我们可以写

v = w1 + ··· + wk
 v=w1+·····+wk

where f(wi) = λiwi (either wi = 0 or wi is an eigenvector for λi), and so for every polynomial h, we have h(f)(v) = h(λ1)w1 + ··· + h(λk)wk,
 式中，f（wi）=λiwi（wi=0或wi是λi的特征向量），因此对于每个多项式h，我们有h（f）（v）=h（λ1）w1+·····+h（λk）wk，

which shows that h(f)(v) ∈ W for every polynomial h. We can write
 这表明，对于每一个多项式h，h（f）（v）∈w，我们可以写

m = (X − λj)q
 m=（x−λj）q

for some polynomial q, and also
 对于某些多项式q，以及

q − q(λj) = p(X − λj)
 q−q（λj）=p（x−λj）

for some polynomial p. We know that p(f)(v) ∈ W, and since m is the minimal polynomial of f, we have
 对于某些多项式p，我们知道p（f）（v）∈w，由于m是f的极小多项式，我们得到

0 = m(f)(u) = (f − λjid)(q(f)(u)),
 0=m（f）（u）=（f−λjid）（q（f）（u）），

which implies that q(f)(u) ∈ W (either q(f)(u) = 0, or it is an eigenvector associated with λj). However,
 这意味着q（f）（u）∈w（q（f）（u）=0，或者是与λj相关的特征向量）。然而，

q(f)(u) − q(λj)u = p(f)((f − λjid)(u)) = p(f)(v),
 q（f）（u）−q（λj）u=p（f）（（f−λjid）（u））=p（f）（v），

and since p(f)(v) ∈ W and q(f)(u) ∈ W, we conclude that q(λj)u ∈ W. But, u /∈ W, which implies that q(λj) = 0, so λj is a double root of m, a contradiction. Therefore, we must have
 由于p（f）（v）∈w和q（f）（u）∈w，我们得出q（λj）u∈w。但是，u/∈w，这意味着q（λj）=0，所以λj是m的一个矛盾的双根。因此，我们必须

W = E.                                                                                                                                                 
 W＝E。

Remark: Proposition 30.5 can be used to give a quick proof of Theorem 14.5.
 注：命题30.5可以用来快速证明定理14.5。

## 30.3 Commuting Families of Diagonalizable and Triangulable Maps  30.3可对角化和三角化地图的交换族

Using Theorem 30.6, we can give a short proof about commuting diagonalizable linear maps.
 利用定理30.6，我们可以给出关于交换对角化线性映射的一个简短证明。

Definition 30.4. If F is a family of linear maps on a vector space E, we say that F is a commuting family iff f ◦ g = g ◦ f for all f,g ∈ F.
 定义30.4.如果f是向量空间e上的线性映射族，我们就说f是所有f的交换族iff f g=g f，g∈f。

Proposition 30.7. Let F be a finite commuting family of diagonalizable linear maps on a vector space E. There exists a basis of E such that every linear map in F is represented in that basis by a diagonal matrix.
 提案30.7。设f为向量空间e上可对角化线性映射的有限交换族，存在e的基，使得f中的每一个线性映射都用一个对角矩阵表示。

Proof. We proceed by induction on n = dim(E). If n = 1, there is nothing to prove. If n > 1, there are two cases. If all linear maps in F are of the form λid for some λ ∈ K, then the proposition holds trivially. In the second case, let f ∈ F be some linear map in F which is not a scalar multiple of the identity. In this case, f has at least two distinct eigenvalues λ1,...,λk, and because f is diagonalizable, E is the direct sum of the corresponding eigenspaces Eλ1,...,Eλk. For every index i, the eigenspace Eλi is invariant under f and under every other linear map g in F, since for any g ∈ F and any u ∈ Eλi, because f and g commute, we have
 证据。我们在n=dim（e）上进行归纳。如果n=1，则无需证明。如果n>1，则有两种情况。如果f中的所有线性映射都是某些λ∈k的λid形式，则该命题成立。在第二种情况下，让f∈f是f中的一个线性映射，它不是恒等式的标量倍数。在这种情况下，f至少有两个不同的特征值λ1，…，λk，并且由于f是可对角化的，e是相应特征空间eλ1，…，eλk的直接和。对于每个指数i，特征空间eλi在f和f中的其他线性映射g下是不变的，因为对于任何g∈f和任何u∈eλi，因为f和g上下班，我们有

f(g(u)) = g(f(u)) = g(λiu) = λig(u)
 f（g（u））=g（f（u））=g（λiu）=λig（u）

so g(u) ∈ Eλi. Let Fi be the family obtained by restricting each f ∈ F to Eλi. By Proposition 30.3, the minimal polynomial of every linear map f | Eλi in Fi divides the minimal polynomial mf of f, and since f is diagonalizable, mf is a product of distinct linear factors, so the minimal polynomial of f | Eλi is also a product of distinct linear factors. By Theorem 30.6, the linear map f | Eλi is diagonalizable. Since k > 1, we have dim(Eλi) < dim(E) for i = 1,...,k, and by the induction hypothesis, for each i there is a basis of Eλi over which f | Eλi is represented by a diagonal matrix. Since the above argument holds for all i, by combining the bases of the Eλi, we obtain a basis of E such that the matrix of every linear map f ∈ F is represented by a diagonal matrix. 
 所以g（u）∈eλi.让fi是通过限制每一个f∈f到eλi而得到的族.通过命题30.3，fi中每一个线性映射f eλi的最小多项式分割了f的最小多项式mf，由于f是可对角化的，mf是不同线性因子的乘积，所以最小多项式f eλi的omial也是不同线性因子的乘积。根据定理30.6，线性映射f eλi是可对角化的。由于k>1，对于i=1，…，k，我们有dim（eλi）<dim（e），并且通过归纳假设，对于每个i，都有eλi的基础，其中f eλi由对角矩阵表示。由于上述论点适用于所有i，通过结合eλi的基，我们得到e的基，这样每个线性映射f∈f的矩阵都由对角矩阵表示。

Remark: Proposition 30.7 also holds for infinite commuting families F of diagonalizable linear maps, because E being finite dimensional, there is a finite subfamily of linearly independent linear maps in F spanning F.
 注：命题30.7也适用于可对角化线性映射的无限交换族f，因为e是有限维的，所以f的跨度f中存在一个线性无关线性映射的有限子族。

There is also an analogous result for commuting families of linear maps represented by upper triangular matrices. To prove this we need the following proposition.
 对于用上三角矩阵表示的线性映射族，也有类似的结果。为了证明这一点，我们需要以下建议。

Proposition 30.8. Let F be a nonempty finite commuting family of triangulable linear maps on a finite-dimensional vector space E. Let W be a proper subspace of E which is invariant under F. Then there exists a vector u ∈ E such that:
 提案30.8。设f为有限维向量空间e上可三角线性映射的一个非空有限交换族。设w为e的一个子空间，该子空间在f下是不变的。然后存在一个向量u∈e，这样：

30.3. COMMUTING FAMILIES OF LINEAR MAPS
 30.3。线性映射的交换族

*1.*     u /∈ W.
 u/∈w.

*2.*     For every f ∈ F, the vector f(u) belongs to the subspace W ⊕ Ku spanned by W and u.
 对于每一个f∈f，向量f（u）属于w和u所跨越的子空间w ku。

Proof. By renaming the elements of F if necessary, we may assume that (f1,...,fr) is a basis of the subspace of End(E) spanned by F. We prove by induction on r that there exists some vector u ∈ E such that
 证据。如果必要的话，通过对f的元素进行重命名，我们可以假定（f1，…，f r）是f所跨越的end（e）的子空间的基础，通过对r的归纳，我们证明存在一些向量u∈e，这样

\1.    u /∈ W.
 u/∈w.

\2.    (fi − αiid)(u) ∈ W for i = 1,...,r, for some scalars αi ∈ K.
 （fi−αiid）（u）∈w表示i=1，…，r表示某些标量αi∈k。

Consider the base case r = 1. Since f1 is triangulable, its eigenvalues all belong to K since they are the diagonal entries of the triangular matrix associated with f1 (this is the easy direction of Theorem 14.5), so the minimal polynomial of f1 is of the form
 考虑基本情况r=1。因为f1是三角形的，所以它的特征值都是k，因为它们是与f1相关的三角形矩阵的对角项（这是定理14.5的简单方向），所以f1的最小多项式的形式是

m = (X − λ1)r1 ···(X − λk)rk,
 m=（x−λ1）r1···（x−λk）Rk，

where the eigenvalues λ1,...,λk of f1 belong to K. We conclude by applying Proposition
 其中，f1的特征值λ1，…，λk属于k，我们通过应用命题得出结论。

30.5.
 30.5。

Next assume that r ≥ 2 and that the induction hypothesis holds for f1,...,fr−1. Thus, there is a vector ur−1 ∈ E such that
 接下来假设r≥2，诱导假设适用于f1，…，fr−1。因此，有一个向量ur−1∈e，这样

\1.    ur−1 ∈/ W.
 UR−1∈/W。

\2.    (fi − αiid)(ur−1) ∈ W for i = 1,...,r − 1, for some scalars αi ∈ K.
 （fi−αiid）（ur−1）∈w表示i=1，…，r−1表示某些标量αi∈k。

Let
 让

Vr−1 = {w ∈ E | (fi − αiid)(w) ∈ W, i = 1,...,r − 1}.
 vr−1=w∈e（fi−αiid）（w）∈w，i=1，…，r−1。

Clearly, W ⊆ Vr−1 and ur−1 ∈ Vr−1. We claim that Vr−1 is invariant under F. This is because, for any v ∈ Vr−1 and any f ∈ F, since f and fi commute, we have
 显然，w vr−1和ur−1∈vr−1。我们声称，在f下，vr−1是不变的，这是因为，对于任何v∈vr−1和任何f∈f，由于f和fi交换，我们有

​                                    (fi − αiid)(f(v)) = f((fi − αiid)(v)),          1 ≤ i ≤ r − 1.
 （f i−αiid）（f（v））=f（（fi−αiid）（v）），1≤i≤r−1。

Now (fi −αiid)(v) ∈ W because v ∈ Vr−1, and W is invariant under F, so f(fi −αiid)(v)) ∈ W, that is, (fi − αiid)(f(v)) ∈ W.
 现在（fi−αiid）（v）∈w是因为v∈vr−1，而w在f下是不变的，所以f（fi−αiid）（v））是∈w，即，（fi−αiid）（f（v））是∈w。

Consider the restriction gr of fr to Vr−1. The minimal polynomial of gr divides the minimal polynomial of fr, and since fr is triangulable, just as we saw for f1, the minimal polynomial of fr is of the form
 考虑fr对vr−1的限制gr。gr的极小多项式除以fr的极小多项式，由于fr是三角的，正如我们对f1所看到的，fr的极小多项式的形式是

m = (X − λ1)r1 ···(X − λk)rk,
 m=（x−λ1）r1···（x−λk）Rk，

where the eigenvalues λ1,...,λk of fr belong to K, so the minimal polynomial of gr is of the same form. By Proposition 30.5, there is some vector ur ∈ Vr−1 such that
 其中，fr的特征值λ1，…，λk属于k，因此gr的最小多项式形式相同。根据命题30.5，有一个向量ur∈vr−1，这样

\1.    ur ∈/ W.
 ur∈/w.

\2.    (gr − αrid)(ur) ∈ W for some scalars αr ∈ K.
 （gr−αrid）（ur）对于某些标量αr∈k∈w。

Now since ur ∈ Vr−1, we have (fi −αiid)(ur) ∈ W for i = 1,...,r−1, so (fi −αiid)(ur) ∈ W for i = 1,...,r (since gr is the restriction of fr), which concludes the proof of the induction step. Finally, since every f ∈ F is the linear combination of (f1,...,fr), Condition (2) of the inductive claim implies Condition (2) of the proposition. 
 既然Ur∈vr−1，我们有（fi−αiid）（ur）∈w代表i=1，…，r−1，所以（fi−αiid）（ur）∈w代表i=1，…，r（因为gr是fr的限制），这就结束了诱导步骤的证明。最后，由于每一个f∈f都是（f1，…，fr）的线性组合，归纳权利要求的条件（2）隐含了命题的条件（2）。

We can now prove the following result.
 我们现在可以证明以下结果。

Proposition 30.9. Let F be a nonempty finite commuting family of triangulable linear maps on a finite-dimensional vector space E. There exists a basis of E such that every linear map in F is represented in that basis by an upper triangular matrix.
 提案30.9.设f为有限维向量空间e上的可三角线性映射的非空有限交换族，存在e的基，使得f中的每一个线性映射都用上三角矩阵表示。

Proof. Let n = dim(E). We construct inductively a basis (u1,...,un) of E such that if Wi is the subspace spanned by (u1 ...,ui), then for every f ∈ F,
 证据。设n=尺寸（e）。我们归纳地构造e的基（u1，…，un），如果wi是（u1，…，ui）所跨越的子空间，那么对于每个f∈f，

,
 ，

for some afij ∈ K; that is, f(ui) belongs to the subspace Wi.
 对于某些afij∈k，即f（ui）属于子空间wi。

We begin by applying Proposition 30.8 to the subspace W0 = (0) to get u1 so that for all f ∈ F,
 我们首先将30.8命题应用于子空间w0=（0），得到u1，这样对于所有f∈f，

.
 .

For the induction step, since Wi invariant under F, we apply Proposition 30.8 to the subspace Wi, to get ui+1 ∈ E such that
 对于归纳步骤，由于wi在f下是不变的，我们将命题30.8应用于子空间wi，得到ui+1∈e，这样

\1.    ui+1 ∈/ Wi.
 ui+1∈/wi。

\2.    For every f ∈ F, the vector f(ui+1) belong to the subspace spanned by Wi and ui+1.
 对于每个f∈f，向量f（ui+1）属于wi和ui+1所跨越的子空间。

Condition (1) implies that (u1,...,ui,ui+1) is linearly independent, and Condition (2) means that for every f ∈ F,
 条件（1）表示（u1，…，ui，ui+1）是线性独立的，条件（2）表示对于每个f∈f，

,
 ，

for some, establishing the induction step. After n steps, each f ∈ F is represented by an upper triangular matrix.  
 对一些人来说，建立诱导步骤。经过n步，每个f∈f用上三角矩阵表示。

Observe that if F consists of a single linear map f and if the minimal polynomial of f is of the form
 如果f由一个线性映射f组成，并且f的最小多项式的形式为

m = (X − λ1)r1 ···(X − λk)rk,
 m=（x−λ1）r1···（x−λk）Rk，

with all λi ∈ K, using Proposition 30.5 instead of Proposition 30.8, the proof of Proposition 30.9 yields another proof of Theorem 14.5.
 对于所有的λi∈k，用命题30.5代替命题30.8，命题30.9的证明给出了定理14.5的另一个证明。


 

## 30.4         The Primary Decomposition Theorem  30.4主分解定理

If f : E → E is a linear map and λ ∈ K is an eigenvalue of f, recall that the eigenspace Eλ associated with λ is the kernel of the linear map λid − f. If all the eigenvalues λ1 ...,λk of f are in K, it may happen that
 如果f:e→e是一个线性映射，而λ∈k是f的特征值，回想一下，与λ相关联的特征空间eλ是线性映射的核心，λid−f。如果f的所有特征值λ1…，λk都是k，则可能发生这种情况。

E = Eλ1 ⊕ ··· ⊕ Eλk,
 e=eλ1···eλk，

but in general there are not enough eigenvectors to span E. What if we generalize the notion of eigenvector and look for (nonzero) vectors u such that
 但是一般来说，没有足够的特征向量来跨越e，如果我们推广特征向量的概念，寻找（非零）向量u，那么

​                                                 (λid − f)r(u) = 0,       for some r ≥ 1?
 （λid−f）r（u）=0，对于某些r≥1？

It turns out that if the minimal polynomial of f is of the form
 结果表明，如果f的极小多项式是

m = (X − λ1)r1 ···(X − λk)rk,
 m=（x−λ1）r1···（x−λk）Rk，

then r = ri does the job for λi; that is, if we let
 那么r=ri为λi做这个工作；也就是说，如果我们允许

Wi = Ker(λiid − f)ri,
 wi=ker（λiid−f）ri，

then
 然后

E = W1 ⊕ ··· ⊕ Wk.
 E=w1····周。

This result is very nice but seems to require that the eigenvalues of f all belong to K. Actually, it is a special case of a more general result involving the factorization of the minimal polynomial m into its irreducible monic factors (see Theorem 29.17),
 这个结果很好，但似乎要求f的特征值都属于k。实际上，这是一个更一般的结果的特殊情况，涉及将最小多项式m因式分解为其不可约Moni因子（见定理29.17）。

,
 ，

where the pi are distinct irreducible monic polynomials over K.
 其中π是K上的独特的不可约Monic多项式。

Theorem 30.10. (Primary Decomposition Theorem) Let f : E → E be a linear map on the finite-dimensional vector space E over the field K. Write the minimal polynomial m of f as
 定理30.10。（主分解定理）设f:e→e为k域上有限维向量空间e上的线性映射。将f的最小多项式m写成

,
 ，

where the pi are distinct irreducible monic polynomials over K, and the ri are positive integers. Let
 式中，π是K上的独特的不可约Monic多项式，ri是正整数。让

​                                                   Wi = Ker(prii(f)),         i = 1,...,k.
 wi=ker（prii（f）），i=1，…，k.

Then
 然后

*(a)*     E = W1 ⊕ ··· ⊕ Wk.
 E=w1····周。

*(b)*     Each Wi is invariant under f.
 每个wi在f下是不变的。

*(c)*     The minimal polynomial of the restriction .
 约束的最小多项式。

Proof. The trick is to construct projections πi using the polynomials so that the range of πi is equal to Wi. Let
 证据。诀窍是用多项式构造投影πi，使πi的范围等于wi。让

gi = m/prii = Yprjj.
 gi=m/prii=yprjj。

j6=i
 J6=

Note that
 注意

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

Since p1,...,pk are irreducible and distinct, they are relatively prime. Then using Proposition 29.14, it is easy to show that g1,...,gk are relatively prime. Otherwise, some irreducible polynomial p would divide all of g1,...,gk, so by Proposition 29.14 it would be equal to one of the irreducible factors pi. But that pi is missing from gi, a contradiction. Therefore, by Proposition 29.15, there exist some polynomials h1,...,hk such that
 由于p1，…，pk是不可约的和独特的，它们是相对素数。然后用29.14号命题，很容易证明g1，…，gk是相对质数。否则，一些不可约多项式p会将所有g1，…，gk除尽，所以用命题29.14，它等于不可约因子pi之一。但是π在gi中是缺失的，一个矛盾。因此，根据命题29.15，存在一些多项式h1，…，hk，使得

g1h1 + ··· + gkhk = 1.
 g1h1+····+gkhk=1.

Let qi = gihi and let πi = qi(f) = gi(f)hi(f). We have
 设qi=gi hi，设πi=qi（f）=gi（f）hi（f）。我们有

q1 + ··· + qk = 1,
 q1+····+qk=1，

and since m divides qiqj for i =6  j, we get
 因为m将qiqj除以i=6j，我们得到

π1 + ··· + πk = id πiπj = 0,      i =6 j.
 π1+·····+πk=idπiπj=0，i=6 J。

(We implicitly used the fact that if p,q are two polynomials, the linear maps p(f) ◦ q(f) and q(f) ◦ p(f) are the same since p(f) and q(f) are polynomials in the powers of f, which commute.) Composing the first equation with πi and using the second equation, we get
 （我们隐式地使用了这样一个事实，即如果p，q是两个多项式，那么线性映射p（f）q（f）和q（f）p（f）是相同的，因为p（f）和q（f）是f的幂的多项式，而f的幂是交换的。）用πi组成第一个方程，然后使用第二个方程，我们得到

πi2 = πi.
 πI2=πI。

Therefore, the πi are projections, and E is the direct sum of the images of the πi. Indeed, every u ∈ E can be expressed as
 因此，πi是投影，e是πi图像的直接和。实际上，每个u∈e都可以表示为

u = π1(u) + ··· + πk(u).
 u=π1（u）+····+πk（u）。

Also, if π1(u) + ··· + πk(u) = 0,
 另外，如果π1（u）+····+πk（u）=0，

then by applying πi we get
 然后通过应用πi我们得到

​                                                   0 = πi2(u) = πi(u),        i = 1,...k.
 0=πi2（u）=πi（u），i=1，…k。

To finish proving (a), we need to show that
 为了完成证明（a），我们需要证明

Wi = Ker(.
 wi=ker（.

If v ∈ πi(E), then v = πi(u) for some u ∈ E, so
 如果v∈πi（e），那么对于某些u∈e，v=πi（u），那么

prii(f)(v) = prii(f)(πi(u))
 prii（f）（v）=prii（f）（πi（u））

= prii(f)gi(f)hi(f)(u)
 =prii（f）gi（f）hi（f）（u）

= hi(f)prii(f)gi(f)(u) = hi(f)m(f)(u) = 0,
 =hi（f）prii（f）gi（f）（u）=hi（f）m（f）（u）=0，

because m is the minimal polynomial of f. Therefore, v ∈ Wi.
 因为m是f的极小多项式，所以v∈wi。

Conversely, assume that v ∈ Wi = Ker(, then gjhj is divisible by, so
 相反，假设v∈wi=ker（，那么gjhj可以被除，所以

​                                                   gj(f)hj(f)(v) = πj(v) = 0,       j =6  i.
 gj（f）hj（f）（v）=πj（v）=0，j=6i。

Then since π1 + ··· + πk = id, we have v = πiv, which shows that v is in the range of πi. Therefore, Wi = Im(πi), and this finishes the proof of (a).
 既然π1+·····+πk=id，我们就得到了V=πiv，这表明V在πi的范围内，因此，wi=im（πi），这就完成了（a）的证明。

If prii(f)(u) = 0, then prii(f)(f(u)) = f(piri(f)(u)) = 0, so (b) holds.
 如果prii（f）（u）=0，那么prii（f）（f（u））=f（piri（f）（u））=0，那么（b）保持不变。

If we write fi = f | Wi, then prii(fi) = 0, because piri(f) = 0 on Wi (its kernel). Therefore, the minimal polynomial of fi divides. Conversely, let q be any polynomial such that q(fi) = 0 (on Wi). Since, the fact that m(f)(u) = 0 for all u ∈ E shows that
 如果我们写fi=f_wi，那么prii（fi）=0，因为piri（f）=0在wi（它的内核）上。因此，fi的极小多项式被除。相反，假设q是任何多项式，这样q（fi）=0（wi上）。因为，m（f）（u）=0表示所有u∈e的事实表明

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

and thus Im(gi(f)) ⊆ Ker(prii(f)) = Wi. Consequently, since q(f) is zero on Wi,
 因此im（gi（f））ker（prii（f））=wi。因此，既然q（f）在wi上为零，

​                                                       q(f)gi(f) = 0      for all u ∈ E.
 q（f）gi（f）=0表示所有u∈e。

But then qgi is divisible by the minimal polynomial, and since and gi are relatively prime, by Euclid’s proposition, must divide q. This finishes the proof that the minimal polynomial of fi is prii, which is (c). 
 但是q gi可以被极小多项式整除，由于和gi是相对素数，所以必须被欧几里得命题整除q，这就证明fi的极小多项式是prii，即（c）。

To best understand the projection constructions of Theorem 30.10, we provide the following two explicit examples of the primary decomposition theorem.
 为了更好地理解定理30.10的投影构造，我们提供了下面两个主分解定理的显式示例。

Example 30.2. First let f : R3 → R3 be defined as ). In terms of the standard basis f is represented by the 3 × 3 matrix. Then a simple
 例30.2。首先让f:r3→r3定义为）。根据标准基f，用3×3矩阵表示。然后一个简单的

calculation shows that mf(x) = χf(x) = (x2 +1)(x−1). Using the notation of the preceding proof set
 计算表明，mf（x）=χf（x）=（x2+1）（x−1）。使用前面证明集的符号

​                                         m = p1p2,         p1 = x2 + 1,          p2 = x − 1.
 m=p1 p2，p1=x2+1，p2=x−1。

Then
 然后

.
 .

We must find h1,h2 ∈ R[x] such that g1h1 + g2h2 = 1. In general this is the hard part of the projection construction. But since we are only working with two relatively prime polynomials g1,g2, we may apply the Euclidean algorithm to discover that
 我们必须找到h1，h2∈r[x]这样g1h1+g2h2=1。一般来说，这是投影结构的硬部分。但是由于我们只研究两个相对素数多项式g1，g2，我们可以应用欧几里得算法来发现

,
 ，

where while. By definition
 何时何地。按定义

 id) =  ,
 id）=，

and
 和

 .
 .

Then R3 = W1 ⊕ W2, where
 则r3=w1 w2，其中

W1 = π1(R3) = Ker(p1(Xf)) = Ker(Xf2 + id) = Ker ,
 w1=π1（r3）=ker（p1（xf））=ker（xf2+id）=ker，

W2 = π2(R3) = Ker(p2(Xf)) = Ker(Xf − id) = Ker .
 w2=π2（r3）=ker（p2（xf））=ker（xf−id）=ker。

Example 30.3. For our second example of the primary decomposition theorem let f : R3 →
 例30.3。对于第一分解定理的第二个例子，让f:r3→

R3 be defined as f(x,y,z) = (y,−x + z,−y), with standard matrix representation Xf =
 r3定义为f（x，y，z）=（y，−x+z，−y），标准矩阵表示为xf。=

0          1     0
 0 1 1

. A simple calculation shows that mf(x) = χf(x) = x(x2 + 2). Set
 . 简单计算表明，mf（x）=χf（x）=x（x2+2）。集合

.
 .

Since gcd(g1,g2) = 1, we use the Euclidean algorithm to find
 由于gcd（g1，g2）=1，我们使用欧几里得算法来查找

,
 ，

such that g1h1 + g2h2 = 1. Then
 使g1h1+g2h2=1。然后

 ,
 ，

while
 虽然

 .
 .

Although it is not entirely obvious, π1 and π2 are indeed projections since
 虽然并不十分明显，但π1和π2确实是投影，因为

,
 ，

and
 和

.
 .

Furthermore observe that π1 + π2 = id. The primary decomposition theorem implies that R3 = W1 ⊕ W2 where
 此外，观察π1+π2=ID。主分解定理表明r3=w1 w2，其中

​                                                                                        1    0   1
 10 1_

W1 = π1(R3) = Ker(p1(f)) = Ker(X2 + 2) = Ker 0            0            0 = span{(0,1,0),(1,0,−1)},
 w1=π1（r3）=ker（p1（f））=ker（x2+2）=ker 0 0 0=span（0,1,0），（1,0，−1），

​                                                                                           1   0   1
 1 0 1

W2 = π2(R3) = Ker(p2(f)) = Ker(X) = span{(1,0,1)}.
 w2=π2（r3）=ker（p2（f））=ker（x）=span（1,0,1）。

See Figure 30.1.
 见图30.1。

If all the eigenvalues of f belong to the field K, we obtain the following result.
 如果F的所有特征值都属于K域，则得到以下结果。

Theorem 30.11. (Primary Decomposition Theorem, Version 2) Let f : E → E be a linear map on the finite-dimensional vector space E over the field K. If all the eigenvalues λ1,...,λk of f belong to K, write
 定理30.11。（初等分解定理，第2版）让f:e→e是有限维向量空间e上k域上的线性映射。如果f的所有特征值λ1，…，则λk属于k，则写下

m = (X − λ1)r1 ···(X − λk)rk
 m=（x−λ1）r1···（x−λk）Rk

for the minimal polynomial of f,
 对于f的极小多项式，

χf = (X − λ1)n1 ···(X − λk)nk
 χf=（x-λ1）n1···（x-λk）nk

for the characteristic polynomial of f, with 1 ≤ ri ≤ ni, and let
 对于f的特征多项式，1≤ri≤ni，且let

​                                                 Wi = Ker(λiid − f)ri,          i = 1,...,k.
 wi=ker（λiid−f）ri，i=1，…，k.

Then
 然后

*(a)*    E = W1 ⊕ ··· ⊕ Wk.
 E=w1····周。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

Figure 30.1: The direct sum decomposition of R3 = W1 ⊕W2 where W1 is the plane x+z = 0 and W2 is line t(1,0,1). The spanning vectors of W1 are in blue.
 图30.1:r3=w1 w2的直接和分解，其中w1是平面x+z=0，w2是直线t（1,0,1）。w1的跨度矢量为蓝色。

*(b)*    Each Wi is invariant under f.
 每个wi在f下是不变的。

*(c)*     dim(Wi) = ni.
 尺寸（wi）=ni。

*(d)*    The minimal polynomial of the restriction f | Wi of f to Wi is (X − λi)ri.
 f对wi的限制f_wi的最小多项式是（x−λi）ri。

Proof. Parts (a), (b) and (d) have already been proven in Theorem 30.10, so it remains to prove (c). Since Wi is invariant under f, let fi be the restriction of f to Wi. The characteristic polynomial χfi of fi divides χ(f), and since χ(f) has all its roots in K, so does χi(f). By Theorem 14.5, there is a basis of Wi in which fi is represented by an upper triangular matrix, and since (λiid−f)ri = 0, the diagonal entries of this matrix are equal to λi. Consequently,
 证据。第（a）、（b）和（d）部分已经在定理30.10中得到证明，因此仍需证明（c）。既然wi在f下是不变的，那么就让fi成为f对wi的限制。fi的特征多项式χfi除χ（f），由于χ（f）的根都在k中，因此χi（f）也是。根据定理14.5，Wi有一个基础，其中fi由上三角矩阵表示，由于（λiid−f）ri=0，该矩阵的对角项等于λi。因此，

χfi = (X − λi)dim(Wi),
 χfi=（x−λi）dim（wi），

and since χfi divides χ(f), we conclude hat
 由于χfi除以χ（f），我们得出：

​                                                      dim(Wi) ≤ ni,         i = 1,...,k.
 尺寸（wi）≤ni，i=1，…，k.

Because E is the direct sum of the Wi, we have dim(W1) + ··· + dim(Wk) = n, and since n1 + ··· + nk = n, we must have
 因为e是wi的直接和，所以我们有dim（w1）+······+dim（wk）=n，既然n1+·····+nk=n，我们必须有

​                                                      dim(Wi) = ni,         i = 1,...,k,
 尺寸（wi）=ni，i=1，…，k，

proving (c).                                                                                                                                        
 证明（c）。


 

30.5. JORDAN DECOMPOSITION
 30.5。约旦分解

Definition 30.5. If λ ∈ K is an eigenvalue of f, we define a generalized eigenvector of f as a nonzero vector u ∈ E such that
 定义30.5.如果λ∈k是f的特征值，我们将f的广义特征向量定义为非零向量u∈e，这样

​                                                 (λid − f)r(u) = 0,       for some r ≥ 1.
 （λid−f）r（u）=0，对于某些r≥1。

The index of λ is defined as the smallest r ≥ 1 such that
 λ的指数定义为最小r≥1，因此

Ker(λid − f)r = Ker(λid − f)r+1.
 ker（λid−f）r=ker（λid−f）r+1。

It is clear that Ker(λid − f)i ⊆ Ker(λid − f)i+1 for all i ≥ 1. By Theorem 30.11(d), if λ = λi, the index of λi is equal to ri.
 很明显，对于所有i≥1，ker（λid−f）i ker（λid−f）i+1。根据定理30.11（d），如果λ=λi，则λi的指数等于ri。

## 30.5        Jordan Decomposition  30.5约旦分解

Recall that a linear map g: E → E is said to be nilpotent if there is some positive integer r such that gr = 0. Another important consequence of Theorem 30.11 is that f can be written as the sum of a diagonalizable and a nilpotent linear map (which commute). For example f : R2 → R2 be the R-linear map f(x,y) = (x,x + y) with standard matrix representation
 回想一下，如果有一个正整数r，比如gr=0，那么线性映射g:e→e就称为幂零。定理30.11的另一个重要结论是，f可以写成对角化和幂零线性映射（可交换）的和。例如：r2→r2是具有标准矩阵表示的r-线性映射f（x，y）=（x，x+y）

. A basic calculation shows that mf(x) = χf(x) = (x − 1)2. By Theorem 30.6
 . 基本计算表明，mf（x）=χf（x）=x−1）2。根据定理30.6

we know that f is not diagonalizable over R. But since the eigenvalue λ1 = 1 of f does belong to R, we may use the projection construction inherent within Theorem 30.11 to write f = D + N, where D is a diagonalizable linear map and N is a nilpotent linear map. The proof of Theorem 30.10 implies that
 我们知道f在r上不可对角化，但由于f的特征值λ1=1属于r，我们可以用定理30.11中固有的投影构造写出f=d+n，其中d是可对角化线性映射，n是幂零线性映射。定理30.10的证明表明

.
 .

Then
 然后

​          D = λ1π1 = id,                   N = f − D = f(x,y) − id(x,y) = (x,x + y) − (x,y) = (0,y),
 D=λ1π1=ID，N=F−D=F（x，y）−ID（x，y）=（x，x+y）−（x，y）=（0，y），

which is equivalent to the matrix decomposition
 相当于矩阵分解

 .
 .

This example suggests that the diagonal summand of f is related to the projection constructions associated with the proof of the primary decomposition theorem. If we write
 这个例子表明f的对角和式与投影结构有关，而投影结构与主分解定理的证明有关。如果我们写信

D = λ1π1 + ··· + λkπk,
 D=λ1π1+····+λkπk，

where πi is the projection from E onto the subspace Wi defined in the proof of Theorem
 式中πi是从e到定理证明中定义的子空间wi的投影。

30.10, since
 30.10，自

π1 + ··· + πk = id,
 π1+····+πk=id，

we have f = fπ1 + ··· + fπk,
 我们有f=fπ1+····+fπk，

and so we get
 所以我们得到

N = f − D = (f − λ1id)π1 + ··· + (f − λkid)πk.
 n=f−d=（f−λ1id）π1+·····+（f−λkid）πk。

We claim that N = f − D is a nilpotent operator. Since by construction the πi are polynomials in f, they commute with f, using the properties of the πi, we get
 我们认为n=f−d是幂零算子。由于πi是f中的多项式，它们与f交换，利用πi的性质，我们得到

Nr = (f − λ1id)rπ1 + ··· + (f − λkid)rπk.
 nr=（f−λ1id）rπ1+····+（f−λkid）rπk。

Therefore, if r = max{ri}, we have (f − λkid)r = 0 for i = 1,...,k, which implies that
 因此，如果r=max r i，我们有（f−λkid）r=0，对于i=1，…，k，这意味着

Nr = 0.
 nr=0。

It remains to show that D is diagonalizable. Since N is a polynomial in f, it commutes with f, and thus with D. From
 它仍然表明d是可对角化的。因为n是f中的多项式，它与f相乘，因此与d相乘。

D = λ1π1 + ··· + λkπk,
 D=λ1π1+····+λkπk，

and
 和

π1 + ··· + πk = id,
 π1+····+πk=id，

we see that
 我们看到了

.
 .

Since the projections πj with j =6 i vanish on Wi, the above equation implies that D − λiid vanishes on Wi and that (D − λjid)(Wi) ⊆ Wi, and thus that the minimal polynomial of D is
 由于j=6i的投影πj在wi上消失，因此上述方程表明d-λiid在wi上消失，d-λjid（wi）wi也消失，因此d的最小多项式为

(X − λ1)···(X − λk).
 （x-λ1）···（x-λk）。

Since the λi are distinct, by Theorem 30.6, the linear map D is diagonalizable.
 由于λi是不同的，根据定理30.6，线性映射d是可对角化的。

In summary we have shown that when all the eigenvalues of f belong to K, there exist a diagonalizable linear map D and a nilpotent linear map N such that
 综上所述，当f的所有特征值都属于k时，存在一个对角化线性映射d和一个幂零线性映射n，从而

f = D + N DN = ND,
 f=d+n，dn=nd，

and N and D are polynomials in f.
 n和d是f中的多项式。

A decomposition of f as above is called a Jordan decomposition. In fact, we can prove more: the maps D and N are uniquely determined by f.
 如上所述，F的分解称为约旦分解。事实上，我们可以证明：图d和n是由f唯一确定的。

30.5. JORDAN DECOMPOSITION
 30.5。约旦分解

Theorem 30.12. (Jordan Decomposition) Let f : E → E be a linear map on the finitedimensional vector space E over the field K. If all the eigenvalues λ1,...,λk of f belong to
 定理30.12。（约当分解）设f:e→e为K域上有限维向量空间e上的线性映射。如果f的所有特征值λ1，…，则λk属于

K, then there exist a diagonalizable linear map D and a nilpotent linear map N such that
 k，那么存在一个对角化的线性映射d和一个幂零的线性映射n，这样

f = D + N DN = ND.
 f=d+n，dn=nd。

Furthermore, D and N are uniquely determined by the above equations and they are polynomials in f.
 此外，D和N是由上述方程唯一确定的，它们是F中的多项式。

Proof. We already proved the existence part. Suppose we also have f = D0 + N0, with D0N0 = N0D0, where D0 is diagonalizable, N0 is nilpotent, and both are polynomials in f. We need to prove that D = D0 and N = N0.
 证据。我们已经证明了存在的部分。假设我们也有f=d0+n0，其中d0是对角化的，n0是幂零的，两者都是f中的多项式，我们需要证明d=d0和n=n0。

Since D0 and N0 commute with one another and f = D0 + N0, we see that D0 and N0 commute with f. Then D0 and N0 commute with any polynomial in f; hence they commute with D and N. From
 因为d0和n0是相互通勤的，而f=d0+n0，我们看到，d0和n0是与f一起通勤的，然后，d0和n0是与f中的任何多项式一起通勤的；因此，它们是与d和n一起通勤的。

D + N = D0 + N0,
 d+n=d0+n0，

we get
 我们得到

D − D0 = N0 − N,
 d−d0=n0−n，

and D,D0,N,N0 commute with one another. Since D and D0 are both diagonalizable and commute, by Proposition 30.7, they are simultaneousy diagonalizable, so D − D0 is diagonalizable. Since N and N0 commute, by the binomial formula, for any r ≥ 1,
 D、D0、N、N0彼此通勤。由于d和d0都是可对角化的和通勤的，根据命题30.7，它们是同时可对角化的，所以d-d0是可对角化的。由于n和n0通勤，根据二项式，对于任何r≥1，

.
 .

Since both N and N0 are nilpotent, we have Nr1 = 0 and (N0)r2 = 0, for some r1,r2 > 0, so for r ≥ r1 +r2, the right-hand side of the above expression is zero, which shows that N0 −N is nilpotent. (In fact, it is easy that r1 = r2 = n works). It follows that D − D0 = N0 − N is both diagonalizable and nilpotent. Clearly, the minimal polynomial of a nilpotent linear map is of the form Xr for some r > 0 (and r ≤ dim(E)). But D − D0 is diagonalizable, so its minimal polynomial has simple roots, which means that r = 1. Therefore, the minimal polynomial of D − D0 is X, which says that D − D0 = 0, and then N = N0. 
 由于n和n0都是幂零的，我们得到n r1=0和（n0）r2=0，对于一些r1，r2>0，因此对于r≥r1+r2，上述表达式的右边是零，这表明n0−n是幂零的。（事实上，很容易r1=r2=n起作用）。由此可知，d−d0=n0−n既可对角化又可幂零。很明显，幂零线性映射的最小多项式的形式是xr，对于一些r>0（和r≤dim（e））。但是d-d0是对角化的，所以它的最小多项式有简单的根，这意味着r=1。因此，d-d0的最小多项式是x，表示d-d0=0，然后n=n0。

If K is an algebraically closed field, then Theorem 30.12 holds. This is the case when K = C. This theorem reduces the study of linear maps (from E to itself) to the study of nilpotent operators. There is a special normal form for such operators which is discussed in the next section.
 如果k是代数闭场，则定理30.12成立。当k=c时就是这样。这个定理将线性映射的研究（从e到自身）简化为幂零算子的研究。这类运算符有一种特殊的正规形式，将在下一节中讨论。

## 30.6           Nilpotent Linear Maps and Jordan Form  30.6幂零线性映射和约旦形式

This section is devoted to a normal form for nilpotent maps. We follow Godement’s exposition [76]. Let f : E → E be a nilpotent linear map on a finite-dimensional vector space over a field K, and assume that f is not the zero map. There is a smallest positive integer r ≥ 1 such fr = 06 and fr+1 = 0. Clearly, the polynomial Xr+1 annihilates f, and it is the minimal polynomial of f since fr = 06 . It follows that r + 1 ≤ n = dim(E). Let us define the subspaces Ni by
 本节讨论幂零映射的正规形式。我们遵循上帝的解释[76]。设f:e→e为k域上有限维向量空间上的幂零线性映射，并假定f不是零映射。有一个最小的正整数r≥1，fr=06，fr+1=0。显然，多项式xr+1会湮灭f，这是自fr=06以来f的最小多项式。由此可知，r+1≤n=dim（e）。让我们定义子空间ni

​                                                             Ni = Ker(fi),       i ≥ 0.
 ni=ker（fi），i≥0。

Note that N0 = (0), N1 = Ker(f), and Nr+1 = E. Also, it is obvious that
 注意n0=（0），n1=ker（f），nr+1=e。此外，很明显

​                                                              Ni ⊆ Ni+1,      i ≥ 0.
 ni ni+1，i≥0。

Proposition 30.13. Given a nilpotent linear map f with fr = 06 and fr+1 = 0 as above, the inclusions in the following sequence are strict:
 提案30.13。给出了一个幂零线性映射f，fr=06，fr+1=0，如下所列的包含严格：

(0) = N0 ⊂ N1 ⊂ ··· ⊂ Nr ⊂ Nr+1 = E.
 （0）=n0 n1···nr nr+1=e。

Proof. We proceed by contradiction. Assume that Ni = Ni+1 for some i with 0 ≤ i ≤ r.
 证据。我们自相矛盾。假设某些i的ni=ni+1，其中0≤i≤r。

Since fr+1 = 0, for every u ∈ E, we have
 因为fr+1=0，对于每个u∈e，我们有

0 = fr+1(u) = fi+1(fr−i(u)),
 0=fr+1（u）=fi+1（fr−i（u）），

which shows that fr−i(u) ∈ Ni+1. Since Ni = Ni+1, we get fr−i(u) ∈ Ni, and thus fr(u) = 0. Since this holds for all u ∈ E, we see that fr = 0, a contradiction. 
 即fr−i（u）∈ni+1。由于ni=ni+1，我们得到fr−i（u）∈ni，因此fr（u）=0。既然这适用于所有的u∈e，我们看到fr=0，一个矛盾。

Proposition 30.14. Given a nilpotent linear map f with fr = 06 and fr+1 = 0, for any integer i with 1 ≤ i ≤ r, for any subspace U of E, if U ∩ Ni = (0), then f(U) ∩ Ni−1 = (0), and the restriction of f to U is an isomorphism onto f(U).
 提案30.14。给定一个幂零线性映射f，f r=06，fr+1=0，对于1≤i≤r的任何整数i，对于e的任何子空间u，如果u ni=（0），那么f（u）ni−1=（0），f对u的限制是对f（u）的同构。

Proof. Pick vi(∈u) = 0f(U). Then∩ Ni−1. We haveu ∈ U ∩ Niv, so= fu(= 0u) for somesince U ∩u N∈iU= (0)and, andfi−1(vv) = 0= f(, whichu) = 0. means that f
 证据。选择vi（∈u）=0f（u）。然后ni−1。我们有u u niv，so=fu（=0u），因为u u n iu=（0），并且fi−1（vv）=0=f（，whichu）=0。意思是f

Therefore, f(U) ∩ Ni−1 = (0). The restriction of f to U is obviously surjective on f(U). Suppose that f(u) = 0 for some u ∈ U. Then u ∈ U ∩ N1 ⊆ U ∩ Ni = (0) (since i ≥ 1), so u = 0, which proves that f is also injective on U. 
 因此，f（u）ni−1=（0）。f对u的限制显然是对f（u）的限制。假设f（u）=0，对于一些u∈u，那么u∈u n1 u ni=（0）（因为i≥1），那么u=0，这证明f也是对u的内射。

Proposition 30.15. Given a nilpotent linear map f with fr = 06  and fr+1 = 0, there exists a sequence of subspace U1,...,Ur+1 of E with the following properties:
 提案30.15。对于fr=06且fr+1=0的幂零线性映射f，存在一个e的子空间u1，…，ur+1序列，其性质如下：

*(1)*     Ni = Ni−1 ⊕ Ui, for i = 1,...,r + 1.
 ni=ni−1 ui，对于i=1，…，r+1。

*(2)*     We have f(Ui) ⊆ Ui−1, and the restriction of f to Ui is an injection, for i = 2,...,r+1.
 我们有f（ui）ui−1，而f对ui的限制是注入，对于i=2，…，r+1。

See Figure 30.2.
 见图30.2。


 

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

Figure 30.2: A schematic illustration of Ni = Ni−1⊕Ui with f(Ui) ⊆ Ui−1 for i = r+1,r,r−1.
 图30.2:ni=ni−1 ui和f（ui）ui−1（i=r+1，r，r−1）的示意图。

Proof. We proceed inductively, by defining the sequence Ur+1,Ur,...,U1. We pick Ur+1 to be any supplement of Nr in Nr+1 = E, so that
 证据。我们通过定义序列uR+1，uR，…，u1进行归纳。我们选择ur+1作为nr+1=e中nr的任何补充，因此

E = Nr+1 = Nr ⊕ Ur+1.
 E=nr+1=nr ur+1。

Since fr+1 = 0 and Nr = Ker(fr), we have f(Ur+1) ⊆ Nr, and by Proposition 30.14, as Ur+1 ∩Nr = (0), we have f(Ur+1)∩Nr−1 = (0). As a consequence, we can pick a supplement Ur of Nr−1 in Nr so that f(Ur+1) ⊆ Ur. We have
 由于fr+1=0和nr=ker（fr），我们有f（ur+1）nr，根据命题30.14，作为ur+1 nr=（0），我们有f（ur+1）nr−1=（0）。因此，我们可以在nr中选择nr−1的补充uR，以便f（ur+1）uR。我们有

​                                              Nr = Nr−1 ⊕ Ur    and     f(Ur+1) ⊆ Ur.
 nr=nr−1 ur和f（ur+1）ur。

By Proposition 30.14, f is an injection from Ur+1 to Ur. Assume inductively that Ur+1,...,Ui have been defined for i ≥ 2 and that they satisfy (1) and (2). Since
 根据提案30.14，F是从UR+1到UR的注入。假设u+1，…，ui被定义为i≥2，并且满足（1）和（2）。自从

Ni = Ni−1 ⊕ Ui,
 ni=ni−1 ui，

we have Ui ⊆ Ni, so fi−1(f(Ui)) = fi(Ui) = (0), which implies that f(Ui) ⊆ Ni−1. Also, since Ui ∩Ni−1 = (0), by Proposition 30.14, we have f(Ui)∩Ni−2 = (0). It follows that there is a supplement Ui−1 of Ni−2 in Ni−1 that contains f(Ui). We have
 我们有ui ni，所以fi−1（f（ui））=fi（ui）=（0），这意味着f（ui）ni−1。此外，由于ui ni−1=（0），根据命题30.14，我们得到f（ui）ni−2=（0）。因此，在ni−1中有一个包含f（ui）的ni−2的补充ui−1。我们有

​                                          Ni−1 = Ni−2 ⊕ Ui−1   and     f(Ui) ⊆ Ui−1.
 ni−1=ni−2 ui−1和f（ui）ui−1。

The fact that f is an injection from Ui into Ui−1 follows from Proposition 30.14. Therefore, the induction step is proven. The construction stops when i = 1.       
 事实上，f是从ui注入到ui−1的注入，这一点源于命题30.14。因此，证明了诱导步骤。当i=1时，结构停止。

Because N0 = (0) and Nr+1 = E, we see that E is the direct sum of the Ui:
 因为n0=（0）和nr+1=e，我们看到e是ui的直接和：

E = U1 ⊕ ··· ⊕ Ur+1,
 E=U1···UR+1，

with f(Ui) ⊆ Ui−1, and f an injection from Ui to Ui−1, for i = r + 1,...,2. By a clever choice of bases in the Ui, we obtain the following nice theorem.
 对于f（ui）ui−1和f，从ui注入到ui−1，对于i=r+1，…，2。通过在用户界面中巧妙地选择基，我们得到了下面的好定理。

Theorem 30.16. For any nilpotent linear map f : E → E on a finite-dimensional vector space E of dimension n over a field K, there is a basis of E such that the matrix N of f is
 定理30.16。对于在有限维向量空间e上的任意幂零线性映射f:e→e，在k域上，有一个e的基础，使得f的矩阵n是

| of the   form    形式的                                      |                                                    |                                            |                                                              |                                                  |                                                              |
| ------------------------------------------------------------ | -------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------------------ |
|     γ   0    零   0    千分之一       γ   N = ...    N=……       γ   0    0       γ   0    零 | ν1    1伏   0    零   ...    …   0    零   0    零 | 0 ν2    0ω2   ...    …   0    零   0    零 | ···    ·········   ···...    ···…   ···    ·········   ···    ········· | 0    零   0    零   ...    …   0    零   0    零 | 0     0℃   0     0℃   ... ,    …，   νn    _n_   0    零 |

where νi = 1 or νi = 0.
 式中，νi=1或νi=0。

Proof. First apply Proposition 30.15 to obtain a direct sum. Then we define a basis of E inductively as follows. First we choose a basis
 证据。首先应用30.15号提案获得直接和。然后我们归纳地定义e的一个基，如下。首先我们选择一个基础

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

of Ur+1. Next, for i = r + 1,...,2, given the basis
 你的+1。接下来，对于i=r+1，…，2，给出了基础

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

of Ui, since f is injective on Ui and f(Ui) ⊆ Ui−1, the vectors) are linearly independent, so we define a basis of Ui−1 by completing) to a basis in Ui−1:
 对于ui，因为f在ui上是内射的，而f（ui）ui-1，向量）是线性独立的，所以我们通过完成定义ui-1的基础）到ui-1的基础：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

with
 具有

​                                                      eij−1 = f(eij),        j = 1...,ni.
 eij−1=f（eij），j=1…，ni.

Since U1 = N1 = Ker(f), we have
 因为u1=n1=ker（f），我们有

​                                                        f(e1j) = 0,        j = 1,...,n1.
 f（e1j）=0，j=1，…，n1.

These basis vectors can be arranged as the rows of the following matrix:
 这些基向量可以排列为以下矩阵的行：

​              er1+1   ··· ern+1r+1                                                                                        
 er1+1···ern+1r+1


 γ

​                 ...                   ...                                                                                              
 …

​                er1      ···   ernr+1 ernr+1+1 ···    ernr                                                         
 er1····ernr+1 ernr+1+1····ernr···


 γ

​                ...                 ...           ...                   ...                                                           
 ………………………

​              er−1   ··· ern−r+11 ern−r+11 +1   ···   ern−r 1 enr−r+11                            ···      ern−r−11    
 er−1···················································

 1
 1

 ...      ...     ...     ...     ...     ...       ...    ...     ...     ...     ...     ...     
 ………………………………………………………………………………………………

​                   e11    ···  e1nr+1 e1nr+1+1 ···    e1nr e1nr+1  ···  en1r−1  ···     ···   e1n1
 E11····E1nr+1 E1nr+1+1····E1nr E1nr+1·········E1n1

Finally, we define the basis (e1,...,en) by listing each column of the above matrix from the bottom-up, starting with column one, then column two, etc. This means that we list the vectors in the following order:
 最后，我们通过自下而上列出上述矩阵的每一列来定义基础（e1，…，en），从第一列开始，然后是第二列，等等。这意味着我们按照以下顺序列出向量：

For j = 1,...,nr+1, list;
 对于j=1，…，nr+1，列表；

In general, for i = r,...,1, for j = ni+1 + 1,...,ni, list e1j,...,eij.
 一般来说，对于i=r，…，1，对于j=ni+1+1，…，ni，列出e1j，…，eij。

Then because f(e1j) = 0 and eij−1 = f(eji) for i ≥ 2, either
 然后，因为f（e1j）=0和eij−1=f（eji），对于i≥2，或者

​                                                       f(ei) = 0     or     f(ei) = ei−1,
 f（ei）=0或f（ei）=ei-1，

which proves the theorem.                                                                                                               
 这证明了这个定理。

As an application of Theorem 30.16, we obtain the Jordan form of a linear map. Definition 30.6. A Jordan block is an r × r matrix Jr(λ), of the form
 作为定理30.16的一个应用，我们得到了线性映射的乔丹形式。定义30.6.约旦块是R×R矩阵Jr（λ），其形式为

| λ    γ-α   0    零       γ   . Jr(λ)   = ..    ②Jr（λ）=..       γ       γ   0    0   0    零 | 1 λ    1兆   ...    …   0    零   0    零 | 0    零   1    一   ...    …   0    零   0    零 | ···    ·········   ···...    ···…   ... ···    …········· | 0    0℃   0    0℃   ...,    ……       γ   1 λ    1λ |
| ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------ | --------------------------------------------------------- | --------------------------------------------------------- |
|                                                              |                                           |                                                  |                                                           |                                                           |

where λ ∈ K, with J1(λ) = (λ) if r = 1. A Jordan matrix, J, is an n × n block diagonal matrix of the form
 式中，如果r=1，则λ∈k，其中j1（λ）=（λ）。约旦矩阵j是形式的n×n块对角矩阵。

 ,
 ，

where each Jrk(λk) is a Jordan block associated with some λk ∈ K, and with r1+···+rm = n.
 其中，每个JRk（λk）是一个与一些λk∈k相关联的约旦块，并且与R1+····+Rm=n相关。

| To   simplify notation, we often write J(λ) for Jr(λ). Here is an example of a   Jordan    为了简化符号，我们通常为jr（λ）编写j（λ）。下面是一个约旦的例子 |                                                              |                                                              |                                                              |                                                              |                                                           |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | --------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| matrix   with four blocks:    四块矩阵：                     |                                                              |                                                              |                                                              |                                                              |                                                           |                                                              |                                                              |
| λ    γ-α   0    千分之一   0    0       γ   0 J = 0    0 J=0       γ       γ   0    0       γ   0    千分之一   0    零 | 1 λ    1兆   0    零   0    零   0    零   0    零   0    零   0    零 | 0    零   1 λ    1兆   0    零   0    零   0    零   0    零   0    零 | 0 0    0 0   0 λ    0兆   0    零   0    零   0    零   0    零 | 0    零   0    零   0    零   1 λ    1兆   0    零   0    零   0    零 | 0    零   0 0 0    0 0 0   0 λ    0兆   0    零   0    零 | 0 0 0    0 0 0   0    零   0    零   0 µ    千分之一   0    零 | 0    0℃   0    0℃   0    0_   0 0.    0 0。   0    0_   1 µ    1 _ |

Theorem 30.17. (Jordan form) Let E be a vector space of dimension n over a field K and let f : E → E be a linear map. The following properties are equivalent:
 定理30.17。（约旦形式）让e是一个向量空间的维度n在一个领域K和让f:e→e是一个线性地图。以下属性等效：

*(1)*     The eigenvalues of f all belong to K (i.e. the roots of the characteristic polynomial χf all belong to K).
 f的特征值都属于k（即特征多项式的根χf都属于k）。

*(2)*     There is a basis of E in which the matrix of f is a Jordan matrix.
 有一个e的基，其中f的矩阵是约旦矩阵。

Proof. Assume (1). First we apply Theorem 30.11, and we get a direct sum, such that the restriction of gi = f − λjid to Wi is nilpotent. By Theorem 30.16, there is a basis of Wi such that the matrix of the restriction of gi is of the form
 证据。假设（1）。首先，我们应用定理30.11，得到一个直接和，使得gi=f-λjid对wi的约束是幂零的。根据定理30.16，有一个wi的基础，使得gi的约束矩阵的形式

|     γ   0    零   0    千分之一       γ   Gi = ...    吉=…       γ   0    0       γ   0    零 | ν1    1伏   0    零   ...    …   0    零   0    零 | 0 ν2    0ω2   ...    …   0    零   0    零 | ···    ·········   ···...    ···…   ···    ·········   ···    ········· | 0    零   0    零   ...    …   0    零   0    零 | 0     0℃   0     0℃   ...   ,    …，   νni    νni_   0    零 |
| ------------------------------------------------------------ | -------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                    |                                            |                                                              |                                                  |                                                              |

where νi = 1 or νi = 0. Furthermore, over any basis, λiid is represented by the diagonal matrix Di with λi on the diagonal. Then it is clear that we can split Di + Gi into Jordan blocks by forming a Jordan block for every uninterrupted chain of 1s. By putting the bases of the Wi together, we obtain a matrix in Jordan form for f.
 式中，νi=1或νi=0。此外，在任何基础上，用对角矩阵di表示λiid，对角线上用λi表示。很明显，我们可以通过为每一个连续的1s链形成一个约旦块来将di+gi分解成约旦块，通过把wi的基部放在一起，我们得到了f的约旦形式的矩阵。

Now assume (2). If f can be represented by a Jordan matrix, it is obvious that the diagonal entries are the eigenvalues of f, so they all belong to K. 
 现在假设（2）。如果F可以用约当矩阵表示，那么很明显，对角项是F的特征值，所以它们都属于K。

Observe that Theorem 30.17 applies if K = C. It turns out that there are uniqueness properties of the Jordan blocks. There are also other fundamental normal forms for linear maps, such as the rational canonical form, but to prove these results, it is better to develop more powerful machinery about finitely generated modules over a PID. To accomplish this most effectively, we need some basic knowledge about tensor products.
 注意定理30.17适用于k=c的情况。结果表明，约旦块具有唯一性。线性映射也有其他基本的正规形式，例如有理正规形式，但是为了证明这些结果，最好在PID上开发关于有限生成模块的更强大的机制。为了最有效地实现这一点，我们需要一些关于张量积的基本知识。

If a complex n × n matrix A is expressed in terms of its Jordan decomposition as A = D + N, since D and N commute, by Proposition 8.21, the exponential of A is given by
 如果一个复n×n矩阵a用它的约当分解表示为a=d+n，因为d和n乘上命题8.21，a的指数由

eA = eDeN,
 ea=伊甸园，

and since N is an n × n nilpotent matrix, Nn−1 = 0, so we obtain
 由于n是n×n的幂零矩阵，n−1=0，因此我们得到

 .
 .

In particular, the above applies if A is a Jordan matrix. This fact can be used to solve (at least in theory) systems of first-order linear differential equations. Such systems are of the form
 特别是，如果a是jordan矩阵，则上述内容适用。这一事实可用于求解（至少在理论上）一阶线性微分方程组。这样的系统是这样的

​                                                                                                                                                       (∗)
 （三）

where A is an n × n matrix and X is an n-dimensional vector of functions of the parameter t.
 其中a是n×n矩阵，x是参数t函数的n维向量。

It can be shown that the columns of the matrix etA form a basis of the vector space of solutions of the system of linear differential equations (∗); see Artin [7] (Chapter 4). Furthermore, for any matrix B and any invertible matrix P, if A = PBP −1, then the system
 可以看出，矩阵eta的列构成了线性微分方程组（）解的向量空间的基础；见Artin[7]（第4章）。此外，对于任何矩阵b和任何可逆矩阵p，如果a=pbp−1，则系统

(∗) is equivalent to
 （）等于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

so if we make the change of variable Y = P −1X, we obtain the system
 因此，如果我们改变变量y=p−1X，我们得到系统

​                                                                                                                                                     (∗∗)
 （）

Consequently, if B is such that the exponential etB can be easily computed, we obtain an explicit solution Y of (∗∗) , and X = PY is an explicit solution of (∗). This is the case when B is a Jordan form of A. In this case, it suffices to consider the Jordan blocks of B. Then we have and the powers Nk are easily computed.
 因此，如果b可以很容易地计算出指数ETb，我们得到（）的显式解y，x=py是（）的显式解。当b是a的约旦形式时就是这样。在这种情况下，考虑b的约旦块就足够了。然后我们就有了，并且可以很容易地计算出k的幂。

For example, if
 例如，如果

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image019.gif)

we obtain
 我们得到

 .
 .

The columns of etB form a basis of the space of solutions of the system of linear differential equations
 ETB的列构成了线性微分方程组解空间的基础。

 .
 .

Solving systems of first-order linear differential equations is discussed in Artin [7] and more extensively in Hirsh and Smale [91].
 一阶线性微分方程组的求解在Artin[7]中进行了讨论，在Hirsh和Smale[91]中进行了更广泛的讨论。

## 30.7      Summary  30.7总结

The main concepts and results of this chapter are listed below:
 本章的主要概念和结果如下：

•     Ideals, principal ideals, greatest common divisors.
 理想，主理想，最大公约数。

•     Monic polynomial, irreducible polynomial, relatively prime polynomials.
 Monic多项式，不可约多项式，相对素多项式。

•     Annihilator of a linear map.
 线性地图的湮灭子。

•     Minimal polynomial of a linear map.
 线性映射的极小多项式。

•     Invariant subspace.
 不变子空间。

•     f-conductor of u into W; conductor of u into W.
 F—U到W的导体；U到W的导体。

•     Diagonalizable linear maps.
 可对角化线性映射。

•     Commuting families of linear maps.
 线性地图的交换族。

•     Primary decomposition.
 初级分解。

•     Generalized eigenvectors.
 广义特征向量。

•     Nilpotent linear map.
 幂零线性映射。

•     Normal form of a nilpotent linear map.
 幂零线性映射的正规形式。

•     Jordan decomposition.
 约旦分解。

•     Jordan block.
 约旦街区。


 

30.8. PROBLEMS
 30.8。问题

•     Jordan matrix.
 约旦矩阵。

•     Jordan normal form.
 约旦标准形状。

•     Systems of first-order linear differential equations.
 一阶线性微分方程组。

## 30.8      Problems  30.8问题

Problem 30.1. Given a linear map f : E → E, prove that the set Ann(f) of polynomials that annihilate f is an ideal.
 问题30.1。给出了一个线性映射f:e→e，证明了湮灭f的多项式的集合ann（f）是一个理想。

Problem 30.2. Provide the details of Proposition 30.3.
 问题30.2。提供提案30.3的细节。

Problem 30.3. Prove that the f-conductor Sf(u,W) is an ideal in K[X] (Proposition 30.4).
 问题30.3。证明f导体sf（u，w）是k[x]中的理想（命题30.4）。

Problem 30.4. Prove that the polynomials g1,...,gk used in the proof of Theorem 30.10 are relatively prime.
 问题30.4。证明定理30.10证明中使用的多项式g1，…，gk是相对素数。

Problem 30.5. Find the minimal polynomial of the matrix
 问题30.5。求矩阵的极小多项式

 .
 .

Problem 30.6. Find the Jordan decomposition of the matrix
 问题30.6。求矩阵的约当分解

 .
 .

Problem 30.7. Let f : E → E be a linear map on a finite-dimensional vector space. Prove that if f has rank 1, then either f is diagonalizable or f is nilpotent but not both. Problem 30.8. Find the Jordan form of the matrix
 问题30.7。设f:e→e为有限维向量空间上的线性映射。证明如果f有秩1，那么f要么是对角化的，要么f是幂零的，但不是两者都是。问题30.8。找到矩阵的约旦形式

 .
 .

Problem 30.9. Let N be a 3 × 3 nilpotent matrix over C. Prove that the matrix A = I + (1/2)N − (1/8)N2 satisfies the equation
 问题30.9。设n为c上的3×3幂零矩阵，证明矩阵a=i+（1/2）n−（1/8）n2满足方程

A2 = I + N.
 A2=I+N。

In other words, A is a square root of I + N.
 换句话说，a是i+n的平方根。

Generalize the above fact to any n × n nilpotent matrix N over C using the binomial series for (1 + t)1/2.
 利用（1+t）1/2的二项级数将上述事实推广到C上任意n×n的幂零矩阵n。

Problem 30.10. Let K be an algebraically closed field (for example, K = C). Prove that every 4 × 4 matrix is similar to a Jordan matrix of the following form:
 问题30.10。设k为代数闭场（例如，k=c）。证明每个4×4矩阵类似于以下形式的约旦矩阵：

​                λ1     0     0      0                   λ    1    0      0 
 λ1 0 0 0λ1 0 0

​                 0    λ2    0      0                   0    λ    0      0 
 0λ2 0 0 0λ0 0

​                0    0    λ3    0 ,              0   0   λ3                          0 ,,
 0λ3 0，0λ3 0，，

​                    0     0     0    λ4                        0    0    0    λ4
 0 0 0λ4 0 0 0λ4

| λ    γ-α   0    0   0    0       γ   0    零 | 1 λ    1兆   0    零   0    零 | 0    零   0 µ    0℃   0    零 | 0    0℃   0,    0℃，   1 µ    1 _ | λ    γ-α   0    0   0    0       γ   0    零 | 1 λ    1兆   0    零   0    零 | 0    零   1 λ    1兆   0    零 | 0 0.    0 0。   1 λ    1λ |
| ------------------------------------------------ | ------------------------------ | ----------------------------- | ------------------------------------- | ------------------------------------------------ | ------------------------------ | ------------------------------ | ----------------------------- |
|                                                  |                                |                               |                                       |                                                  |                                |                                |                               |

Problem 30.11. In this problem the field K is of characteristic 0. Consider an (r × r)
 问题30.11。在这个问题中，字段k的特征为0。考虑a（r×r）

| Jordan   block    约旦街区                                   |                                                              |                                           |                                                  |                                                           |                                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------ | --------------------------------------------------------- | --------------------------------------------------------- |
|                                                              | λ    小精灵   0    零       γ   . Jr(λ) = ..    ②Jr（λ）=..       γ       γ   0    千分之一   0    零 | 1 λ    1兆   ...    …   0    零   0    零 | 0    零   1    一   ...    …   0    零   0    零 | ···    ·········   ···...    ···…   ... ···    …········· | 0    0℃   0    0℃   ....    ……       γ   1 λ    1λ |
| Prove that for any polynomial f(X), we   have    证明对于任何多项式f（x），我们有 |                                                              |                                           |                                                  |                                                           |                                                           |

,
 ，

where
 哪里

and f(k)(X) is the kth derivative of f(X).
 f（k）（x）是f（x）的kth导数。

