第二十二章

# Computing Eigenvalues and Eigenvectors  计算特征值和特征向量

After the problem of solving a linear system, the problem of computing the eigenvalues and the eigenvectors of a real or complex matrix is one of most important problems of numerical linear algebra. Several methods exist, among which we mention Jacobi, Givens–Householder, divide-and-conquer, QR iteration, and Rayleigh–Ritz; see Demmel [49], Trefethen and Bau [171], Meyer [122], Serre [151], Golub and Van Loan [80], and Ciarlet [41]. Typically, better performing methods exist for special kinds of matrices, such as symmetric matrices.
 在求解线性系统问题之后，计算实矩阵或复矩阵的特征值和特征向量的问题是数值线性代数中最重要的问题之一。存在几种方法，其中我们提到Jacobi、Givens——户主、分而治之、QR迭代和Rayleigh——Ritz；见Demmel[49]、Trefetten和Bau[171]、Meyer[122]、Serre[151]、Golub和van Loan[80]和Ciarlet[41]。通常，对于特殊类型的矩阵（如对称矩阵），存在性能更好的方法。

In theory, given an n×n complex matrix A, if we could compute a Schur form A = UTU∗, where T is upper triangular and U is unitary, we would obtain the eigenvalues of A, since they are the diagonal entries in T. However, this would require finding the roots of a polynomial, but methods for doing this are known to be numerically very unstable, so this is not a practical method.
 在理论上，给定一个n×n复矩阵a，如果我们可以计算一个Schur形式a=u t u，其中t是上三角，u是单位的，我们就可以得到a的特征值，因为它们是t中的对角项。然而，这需要求多项式的根，但要求出方法这是众所周知的数值非常不稳定，所以这不是一个实际的方法。

A common paradigm is to construct a sequence (Pk) of matrices such that Ak = Pk−1APk converges, in some sense, to a matrix whose eigenvalues are easily determined. For example, Ak = Pk−1APk could become upper triangular in the limit. Furthermore, Pk is typically a product of “nice” matrices, for example, orthogonal matrices.
 一个常见的范例是构造一个矩阵序列（pk），使得ak=pk−1apk在某种意义上收敛到一个特征值容易确定的矩阵。例如，ak=pk−1apk可能在极限处变成上三角形。此外，pk通常是“nice”矩阵的乘积，例如正交矩阵。

For general matrices, that is, matrices that are not symmetric, the QR iteration algorithm, due to Rutishauser, Francis, and Kublanovskaya in the early 1960s, is one of the most efficient algorithms for computing eigenvalues. A fascinating account of the history of the QR algorithm is given in Golub and Uhlig [79]. The QR algorithm constructs a sequence of matrices (Ak), where Ak+1 is obtained from Ak by performing a QR-decomposition Ak = QkRk of Ak and then setting Ak+1 = RkQk, the result of swapping Qk and Rk. It is immediately verified that Ak+1 = Q∗kAkQk, so Ak and Ak+1 have the same eigenvalues, which are the eigenvalues of A.
 对于一般的矩阵，即非对称矩阵，20世纪60年代初由于Rutishauser、Francis和Kublanovskaya的影响，QR迭代算法是计算特征值最有效的算法之一。Golub和Uhlig[79]中给出了QR算法历史的精彩描述。QR算法构造了一个矩阵序列（AK），其中AK+1是通过对AK执行QR分解AK=QKRK，然后设置AK+1=RKQK，交换QK和RK的结果从AK获得的。立即证实，ak+1=q kakqk，因此ak和ak+1具有相同的特征值，即a的特征值。

The basic version of this algorithm runs into difficulties with matrices that have several eigenvalues with the same modulus (it may loop or not “converge” to an upper triangular matrix). There are ways of dealing with some of these problems, but for ease of exposition,
 该算法的基本版本在具有多个具有相同模的特征值的矩阵中遇到困难（它可能循环或不“收敛”到上三角矩阵）。有一些方法可以解决这些问题，但为了便于解释，

663
 六百六十三

we first present a simplified version of the QR algorithm which we call basic QR algorithm. We prove a convergence theorem for the basic QR algorithm, under the rather restrictive hypothesis that the input matrix A is diagonalizable and that its eigenvalues are nonzero and have distinct moduli. The proof shows that the part of Ak strictly below the diagonal converges to zero and that the diagonal entries of Ak converge to the eigenvalues of A.
 我们首先提出了一个简化版的二维码算法，我们称之为基本二维码算法。在输入矩阵A可对角化且特征值不为零且具有明显模性的限制性假设下，证明了基本QR算法的收敛定理。证明了严格低于对角的AK部分收敛到零，AK的对角项收敛到A的特征值。

Since the convergence of the QR method depends crucially only on the fact that the part of Ak below the diagonal goes to zero, it would be highly desirable if we could replace A by a similar matrix U∗AU easily computable from A and having lots of zero strictly below the diagonal. It turns out that there is a way to construct a matrix H = U∗AU which is almost triangular, except that it may have an extra nonzero diagonal below the main diagonal. Such matrices called, Hessenberg matrices, are discussed in Section 22.2. An n×n diagonalizable Hessenberg matrix H having the property that hi+1i = 06 for i = 1,...,n − 1 (such a matrix is called unreduced) has the nice property that its eigenvalues are all distinct. Since every Hessenberg matrix is a block diagonal matrix of unreduced Hessenberg blocks, it suffices to compute the eigenvalues of unreduced Hessenberg matrices. There is a special case of particular interest: symmetric (or Hermitian) positive definite tridiagonal matrices. Such matrices must have real positive distinct eigenvalues, so the QR algorithm converges to a diagonal matrix.
 由于qr方法的收敛性主要取决于一个事实，即对角线下的ak部分变为零，因此，如果我们可以用一个类似的矩阵u au替换a，该矩阵u au很容易从a计算出来，并且在对角线下有大量的零，这将是非常可取的。事实证明，有一种方法可以构造一个几乎是三角形的矩阵h=u au，除了它在主对角线下面可能有一个额外的非零对角线。在第22.2节中讨论了这种称为Hessenberg矩阵的矩阵。一个n×n的可对角化Hessenberg矩阵h，其性质为i=1，…，n−1（这种矩阵称为无约矩阵）具有其特征值都不同的优良性质。由于每一个海森堡矩阵都是一个由海森堡块组成的块对角矩阵，所以计算海森堡矩阵的特征值就足够了。有一个特别有趣的例子：对称（或厄米特）正定三对角矩阵。这样的矩阵必须具有实正的特征值，因此QR算法收敛到一个对角矩阵。

In Section 22.3, we consider techniques for making the basic QR method practical and more efficient. The first step is to convert the original input matrix A to a similar matrix H in Hessenberg form, and to apply the QR algorithm to H (actually, to the unreduced blocks of H). The second and crucial ingredient to speed up convergence is to add shifts.
 在第22.3节中，我们考虑了使基本QR方法更实用、更有效的技术。第一步是将原始输入矩阵A转换为类似的Hessenberg形式的矩阵H，并将QR算法应用于H（实际上，应用于H的未减少块）。加速收敛的第二个关键因素是增加移位。

A shift is the following step: pick some σk, hopefully close to some eigenvalue of A (in general, λn), QR-factor Ak − σkI as
 移动是以下步骤：选择一些σk，希望接近a（一般来说，λn）的特征值，qr因子ak-σki as

Ak − σkI = QkRk,
 AK−σki=qkrk，

and then form
 然后形成

Ak+1 = RkQk + σkI.
 AK+1=RKQK+σki。

It is easy to see that we still have Ak+1 = Q∗kAkQk. A judicious choice of σk can speed up convergence considerably. If H is real and has pairs of complex conjugate eigenvalues, we can perform a double shift, and it can be arranged that we work in real arithmetic.
 很容易看出我们仍然有ak+1=q kakqk。明智地选择σk可以大大加快收敛速度。如果h是实的，并且有一对复共轭特征值，我们可以执行双移位，并且可以安排我们在实算术中工作。

The last step for improving efficiency is to compute Ak+1 = Q∗kAkQk without even performing a QR-factorization of Ak −σkI. This can be done when Ak is unreduced Hessenberg. Such a method is called QR iteration with implicit shifts. There is also a version of QR iteration with implicit double shifts.
 提高效率的最后一步是计算ak+1=q kakqk，甚至不执行ak−σki的qr因子分解。这可以在AK是非公爵海森堡时完成。这种方法称为隐式移位的QR迭代。还有一个带有隐式双移位的QR迭代版本。

If the dimension of the matrix A is very large, we can find approximations of some of the eigenvalues of A by using a truncated version of the reduction to Hessenberg form due to Arnoldi in general and to Lanczos in the symmetric (or Hermitian) tridiagonal case. Arnoldi iteration is discussed in Section 22.4. If A is an m × m matrix, for much smaller than m) the idea is to generate the n × n Hessenberg submatrix Hn of the full Hessenberg matrix H (such that A = UHU∗) consisting of its first n rows and n columns; the matrix Un consisting of the first n columns of U is also produced. The Rayleigh–Ritz method consists in computing the eigenvalues of Hn using the QR- method with shifts. These eigenvalues, called Ritz values, are approximations of the eigenvalues of A. Typically, extreme eigenvalues are found first.
 如果矩阵A的维数非常大，我们可以通过使用截断形式的约简来找到A的一些特征值的近似值，这种约简形式通常是由于阿诺迪和兰佐斯在对称（或厄米提亚）三对角情况下的约简。第22.4节讨论了Arnoldi迭代。如果a是m×m矩阵，对于比m小得多的矩阵，其思想是生成完整的Hessenberg矩阵h（这样a=u h u）的n×n Hessenberg子矩阵hn，该子矩阵由其前n行和n列组成；也生成不由u的前n列组成的矩阵。瑞利-瑞兹方法是利用位移的QR-方法计算hn的特征值。这些特征值称为Ritz值，是A特征值的近似值。通常首先找到极端特征值。

Arnoldi iteration can also be viewed as a way of computing an orthonormal basis of a Krylov subspace, namely the subspace Kn(A,b) spanned by (b,Ab,...,Anb). We can also use Arnoldi iteration to find an approximate solution of a linear equation Ax = b by minimizing kb − Axnk2 for all xn is the Krylov space Kn(A,b). This method named GMRES is discussed in Section 22.5.
 Arnoldi迭代也可以看作是计算krylov子空间的正态基的一种方法，即（b，ab，…，anb）所跨越的子空间kn（a，b）。我们也可以使用Arnoldi迭代，通过最小化所有xn的kb−axnk2，找到线性方程ax=b的近似解，即krylov空间kn（a，b）。第22.5节讨论了名为gmres的方法。

The special case where H is a symmetric (or Hermitian) tridiagonal matrix is discussed in Section 22.6. In this case, Arnoldi’s algorithm becomes Lanczos’ algorithm. It is much more efficient than Arnoldi iteration.
 在第22.6节中讨论了H是对称（或厄米特）三对角矩阵的特殊情况。在这种情况下，Arnoldi的算法变成了Lanczos的算法。它比Arnoldi迭代更有效。

We close this chapter by discussing two classical methods for computing a single eigenvector and a single eigenvalue: power iteration and inverse (power) iteration; see Section
 我们通过讨论计算单个特征向量和单个特征值的两种经典方法来结束本章：功率迭代和逆（功率）迭代；参见第节

22.7.
 22.7。

## 22.1         The Basic QR Algorithm  22.1基本QR算法

Let A be an n × n matrix which is assumed to be diagonalizable and invertible. The basic QR algorithm makes use of two very simple steps. Starting with A1 = A, we construct sequences of matrices (Ak), (Qk) (Rk) and (Pk) as follows:
 假设a是一个n×n矩阵，它假定是对角化的和可逆的。基本的QR算法使用两个非常简单的步骤。从a1=a开始，我们构造矩阵（ak）、（qk）（rk）和（pk）的序列，如下所示：

​                                                 Factor                             A1 = Q1R1
 系数a1=q1r1

​                                                 Set                                  A2 = R1Q1
 设置a2=r1q1

​                                                 Factor                             A2 = Q2R2
 系数a2=q2r2

​                                                 Set                                  A3 = R2Q2
 设置a3=r2q2

...
 …

​                                                 Factor                             Ak = QkRk
 系数ak=qkrk

​                                                 Set                              Ak+1 = RkQk
 设置AK+1=RKQK

...
 …

Thus, Ak+1 is obtained from a QR-factorization Ak = QkRk of Ak by swapping Qk and
 因此，通过交换qk和

Rk. Define Pk by
 RK。定义pk的依据

Pk = Q1Q2 ···Qk.
 pk=q1q2···qk。

Since Ak = QkRk, we have , and since Ak+1 = RkQk, we obtain
 因为ak=qkrk，我们有，并且因为ak+1=rkqk，我们得到

​                                                                             .                                                                       (∗1)
 .（1）

An obvious induction shows that
 一个明显的归纳显示

,
 ，

that is
 那就是

​                                                                             .                                                                       (∗2)
 .（2）

Therefore, Ak+1 and A are similar, so they have the same eigenvalues.
 因此，AK+1和A是相似的，所以它们具有相同的特征值。

The basic QR iteration method consists in computing the sequence of matrices Ak, and in the ideal situation, to expect that Ak “converges” to an upper triangular matrix, more precisely that the part of Ak below the main diagonal goes to zero, and the diagonal entries converge to the eigenvalues of A.
 基本的QR迭代方法包括计算矩阵的序列AK，在理想情况下，期望AK“收敛”到上三角矩阵，更精确地说，主对角线下的AK部分变为零，对角线条目收敛到特征值。a.

This ideal situation is only achieved in rather special cases. For one thing, if A is unitary (or orthogonal in the real case), since in the QR decomposition we have R = I, we get A2 = IQ = Q = A1, so the method does not make any progress. Also, if A is a real matrix, since the Ak are also real, if A has complex eigenvalues, then the part of Ak below the main diagonal can’t go to zero. Generally, the method runs into troubles whenever A has distinct eigenvalues with the same modulus.
 这种理想情况只有在相当特殊的情况下才能实现。首先，如果a是一元的（或在实际情况下是正交的），因为在q r分解中我们有r=i，我们得到a2=i q=q=a1，所以这个方法没有任何进展。另外，如果a是一个实矩阵，因为ak也是实的，如果a有复杂的特征值，那么主对角线下面的ak部分就不能归零。一般来说，当A的特征值不同且模相同时，该方法就会遇到麻烦。

The convergence of the sequence (Ak) is only known under some fairly restrictive hypotheses. Even under such hypotheses, this is not really genuine convergence. Indeed, it can be shown that the part of Ak below the main diagonal goes to zero, and the diagonal entries converge to the eigenvalues of A, but the part of Ak above the diagonal may not converge. However, for the purpose of finding the eigenvalues of A, this does not matter.
 序列的收敛性（ak）只有在一些相当严格的假设下才能知道。即使在这样的假设下，这也不是真正的趋同。事实上，可以证明主对角线下的ak部分为零，对角线条目收敛到a的特征值，但对角线上的ak部分可能不收敛。然而，为了求A的特征值，这并不重要。

The following convergence result is proven in Ciarlet [41] (Chapter 6, Theorem 6.3.10 and Serre [151] (Chapter 13, Theorem 13.2). It is rarely applicable in practice, except for symmetric (or Hermitian) positive definite matrices, as we will see shortly.
 以下收敛结果在Ciarlet[41]中得到证明（第6章，定理6.3.10和Serre[151]（第13章，定理13.2）。它在实践中很少适用，除了对称（或厄米特）正定矩阵，我们稍后将看到。

Theorem 22.1. Suppose the (complex) n×n matrix A is invertible, diagonalizable, and that its eigenvalues λ1,...,λn have different moduli, so that
 定理22.1。假设（复数）n×n矩阵a是可逆的、可对角化的，且其特征值λ1，…，λn具有不同的模，因此

|λ1| > |λ2| > ··· > |λn| > 0.
 |λ1>λ2>···>λn>0.

If A = PΛP −1, where Λ = diag(λ1,...,λn), and if P −1 has an LU-factorization, then the strictly lower-triangular part of Ak converges to zero, and the diagonal of Ak converges to Λ.
 如果a=p∧p−1，其中∧=diag（λ1，…，λn），并且如果p−1具有Lu因式分解，那么AK的严格下三角部分收敛到零，AK的对角线收敛到∧。

Proof. We reproduce the proof in Ciarlet [41] (Chapter 6, Theorem 6.3.10). The strategy is to study the asymptotic behavior of the matrices Pk = Q1Q2 ···Qk. For this, it turns out that we need to consider the powers Ak.
 证据。我们在Ciarlet[41]中复制了证明（第6章，定理6.3.10）。研究矩阵pk=q1q2···qk的渐近行为。为此，我们需要考虑权力AK。

Step 1. Let Rk = Rk ···R2R1. We claim that
 第1步。设Rk=Rk···r2r1。我们声称

​                                             Ak = (Q1Q2 ···Qk)(Rk ···R2R1) = PkRk.                                      (∗3)
 ak=（q1q2···qk）（rk···r2r1）=pkrk。（3）

We proceed by induction. The base case k = 1 is trivial. For the induction step, from
 我们采用归纳法。基本情况k=1无关紧要。对于感应步骤，从

(∗2), we have
 （2），我们有

PkAk+1 = APk.
 pkak+1=apk。

Since Ak+1 = RkQk = Qk+1Rk+1, we have
 由于AK+1=RKQK=QK+1RK+1，我们有

Pk+1Rk+1 = PkQk+1Rk+1Rk = PkAk+1Rk = APkRk = AAk = Ak+1
 pk+1rk+1=pkqk+1rk+1rk=pk ak+1rk=apkrk=aak=ak+1

establishing the induction step.
 建立诱导步骤。

Step 2. We will express the matrix Pk as Pk = QQekDk, in terms of a diagonal matrix Dk with unit entries, with Q and Qek unitary.
 第2步。我们将矩阵pk表示为pk=q qek dk，用带单位项的对角矩阵dk表示，q和qek为一元。

Let P = QR, a QR-factorization of P (with R an upper triangular matrix with positive diagonal entries), and P −1 = LU, an LU-factorization of P −1. Since A = PΛP −1, we have
 设p=qr，p的qr因子分解（r为上三角矩阵，带正对角项），p−1=lu，p−1的lu因子分解。既然a=p∧p−1，我们有

​                                         Ak = PΛkP −1 = QRΛkLU = QR(ΛkLΛ−k)ΛkU.                                  (∗4)
 ak=p∧kp−1=qr∧klu=qr（∧kl∧k）∧ku.（4）

Here, Λ−k is the diagonal matrix with entries λ−i k. The reason for introducing the matrix ΛkLΛ−k is that its asymptotic behavior is easy to determine. Indeed, we have
 这里，∧−k是条目为λ−i k的对角矩阵。引入矩阵∧kl∧−k的原因是其渐近行为易于确定。事实上，我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

​                                                   kLΛ−k)ij = 1        k           if i = j
 kl∧−k）i j=1 k，如果i=j

(Λ
 （b）

The hypothesis that |λ1| > |λ2| > ··· > |λn| > 0 implies that
 假设λ1>λ2>····>λn>0意味着

lim ΛkLΛ−k = I. (†) k7→∞
 lim∧kl∧−k=i.（†）k7→∞

Note that it is to obtain this limit that we made the hypothesis on the moduli of the eigenvalues. We can write
 注意，为了得到这个极限，我们假设了特征值的模。我们可以写信

​                                              ΛkLΛ−k = I + Fk,      with      lim Fk = 0,
 ∧kl∧−k=i+fk，其中lim fk=0，

k7→∞
 K7→∞

and consequently, since R(ΛkLΛ−k) = R(I + Fk) = R + RFkR−1R = (I + RFkR−1)R, we have
 因此，由于r（∧kl∧k）=r（i+fk）=r+rfkr−1r=（i+rfkr−1）r，我们得出

​                                                      R(ΛkLΛ−k) = (I + RFkR−1)R.                                               (∗5)
 R（∧kl∧k）=（I+Rfkr−1）R.（5）

By Proposition 8.11(1), since limk7→∞ Fk = 0, and thus limk7→∞ RFkR−1 = 0, the matrices I + RFkR−1 are invertible for k large enough. Consequently for k large enough, we have a QR-factorization
 根据命题8.11（1），由于limk7→∞fk=0，因此limk7→∞rfkr−1=0，矩阵i+rfkr−1对于k足够大是可逆的。因此，对于足够大的k，我们有一个qr因子分解。

​                                                            I + RFkR−1 = QekRek,                                                    (∗6)
 i+rfkr−1=qekrek，（6）

with (Rek)ii > 0 for i = 1,...,n. Since the matrices Qek are unitary, we have = 1, so the sequence (Qek) is bounded. It follows that it has a convergent subsequence (Qe`) that converges to some matrix Qe, which is also unitary. Since
 当（rek）i i>0时，i=1，…，n。因为矩阵qek是一元的，所以我们有=1，所以序列（qek）是有界的。因此，它有一个收敛子序列（qe`），它收敛到一个矩阵qe，这个矩阵qe也是一元的。自从

Re` = (Qe`)∗(I + RF`R−1),
 re`=（qe`）（i+rf`r−1），

we deduce that the subsequence (Re`) also converges to some matrix Re, which is also upper triangular with positive diagonal entries. By passing to the limit (using the subsequences), we get Re = (Qe)∗, that is,
 我们推导出子序列（re`）也收敛于某个矩阵re，该矩阵也是上三角形，具有正对角项。通过传递到极限（使用子序列），我们得到re=（qe），也就是说，

I = QeR.e
 i=qer.e

By the uniqueness of a QR-decomposition (when the diagonal entries of R are positive), we get
 通过qr分解的唯一性（当r的对角项为正时），我们得到

Qe = Re = I.
 qe=re=i。

Since the above reasoning applies to any subsequences of (Qek) and (Rek), by the uniqueness of limits, we conclude that the “full” sequences (Qek) and (Rek) converge:
 由于上述推理适用于（qek）和（rek）的任何子序列，根据极限的唯一性，我们得出结论，“全”序列（qek）和（rek）收敛：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

Since by (∗4),
 从（4）开始，

Ak = QR(ΛkLΛ−k)ΛkU,
 ak=qr（∧kl∧k）∧ku，

by (∗5),
 通过（5）

R(ΛkLΛ−k) = (I + RFkR−1)R,
 R（∧kl∧k）=（I+Rfkr−1）R，

and by (∗6)
 以及（6）

I + RFkR−1 = QekRek,
 i+rfkr−1=qekrek，

we proved that
 我们证明了

​                                                          Ak = (QQek)(RekRΛkU).                                                  (∗7)
 ak=（qqek）（rekr∧ku）。（7）

Observe that QQek is a unitary matrix, and RekRΛkU is an upper triangular matrix, as a product of upper triangular matrices. However, some entries in Λ may be negative, so we can’t claim that  has positive diagonal entries. Nevertheless, we have another QR-decomposition of Ak,
 观察到qqek是一个单位矩阵，rekr∧ku是一个上三角矩阵，作为上三角矩阵的乘积。然而，∧中的一些条目可能是负数，所以我们不能声称有正对角线条目。不过，我们还有另一个AK的QR分解，

Ak = (QQek)(RekRΛkU) = PkRk.
 ak=（qqek）（rekr∧ku）=pkrk.

It is easy to prove that there is diagonal matrix Dk with |(Dk)ii| = 1 for i = 1,...,n, such that
 很容易证明存在对角矩阵dk，其中i=1，…，n的（dk）ii=1，这样

​                                                                             .                                                                       (∗8)
 .（8）

The existence of Dk is consequence of the following fact: If an invertible matrix B has two QR factorizations B = Q1R1 = Q2R2, then there is a diagonal matrix D with unit entries such that Q2 = DQ1.
 dk的存在是以下事实的结果：如果可逆矩阵b有两个qr因式分解b=q1r1=q2r2，那么就有一个对角矩阵d，其单位项为q2=dq1。

The expression for Pk in (∗8) is that which we were seeking.
 （8）中pk的表达式是我们正在寻找的表达式。

Step 3. Asymptotic behavior of the matrices Ak+1 = Pk∗APk.
 第3步。矩阵ak+1=pk apk的渐近行为。

Since A = PΛP −1 = QRΛR−1Q−1 and by (∗8), Pk = QQekDk, we get
 由于a=p∧p−1=qr∧r−1q−1和by（8），pk=qqekdk，我们得到

​                                                                              .                                                                       (∗9)
 .（9）

Since limk7→∞ Qek = I, we deduce that
 由于limk7→∞qek=i，我们推断

| ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif) | 2    网络错误   0    网络错误 | ···...    网络错误   ···    网络错误 | ,    网络错误 |
| ------------------------------------------------------------ | ----------------------------- | ------------------------------------ | ------------- |
|                                                              |                               |                                      |               |

 λ1   ∗     ···
 λ1···

​                                                                                             0    λ
 0兆

an upper triangular matrix with the eigenvalues of A on the diagonal. Since R is upper triangular, the order of the eigenvalues is preserved. If we let
 在对角线上具有a特征值的上三角矩阵。由于R是上三角形，所以特征值的阶数保持不变。如果我们让

​                                                          Dk = (Qek)∗RΛR−1Qek,                                                 (∗10)
 dk=（qek）r∧r−1qek，（10）

then by (∗9) we have Ak+1 = Dk∗DkDk, and since the matrices Dk are diagonal matrices, we have
 然后通过（9），我们得到了ak+1=dk dkdk，由于dk矩阵是对角矩阵，我们得到了

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

(Ak+1)jj = (Dk∗DkDk)ij = (Dk)ii(Dk)jj(Dk)ij,
 （ak+1）jj=（dk dkdk）ij=（dk）ii（dk）jj（dk）ij，

which implies that
 这意味着

​                                                   (Ak+1)ii = (Dk)ii,        i = 1,...,n,                                            (∗11)
 （ak+1）i i=（dk）ii，i=1，…，n，（11）

since |(Dk)ii| = 1 for i = 1,...,n. Since limk→∞7 Dk = RΛR−1, we conclude that the strictly lower-triangular part of Ak+1 converges to zero, and the diagonal of Ak+1 converges to Λ. 
 由于（dk）i i=1，对于i=1，…，n.由于limk→∞7 dk=r∧r−1，我们得出的结论是，ak+1的严格下三角部分收敛到零，而ak+1的对角线收敛到∧。

Observe that if the matrix A is real, then the hypothesis that the eigenvalues have distinct moduli implies that the eigenvalues are all real and simple.
 如果矩阵A是实的，那么特征值具有不同模的假设意味着特征值都是实的和简单的。

The following Matlab program implements the basic QR-method using the function qrv4 from Section 11.8.
 下面的matlab程序使用第11.8节中的函数qrv4实现基本的qr方法。

function T = qreigen(A,m)
 函数t=qreigen（a，m）

T = A; for k = 1:m
 t=a；对于k=1:m

[Q R] = qrv4(T);
 [q r]=qrv4（t）；

T = R*Q;
 t=r*q；

end end
 结束

Example 22.1. If we run the function qreigen with 100 iterations on the 8×8 symmetric
 例22.1。如果我们在8×8对称上运行100次迭代的函数qreigen

| matrix    网络错误 |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |
| ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                    | ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif) | 1    网络错误   4    网络错误   1    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   1    网络错误   4    网络错误   1    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   1    网络错误   4    网络错误   1    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   1    网络错误   4    网络错误   1    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   0    网络错误   1    网络错误   4    网络错误   1    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   1    网络错误   4    网络错误   1    网络错误 | 0    网络错误   0    网络错误   0    网络错误   0 0,    网络错误   0    网络错误   1 4    网络错误 |

we find the matrix
 我们找到矩阵

 .
 .

The diagonal entries match the eigenvalues found by running the Matlab function eig(A).
 对角线条目与运行matlab函数eig（a）得到的特征值相匹配。

If several eigenvalues have the same modulus, then the proof breaks down, we can no longer claim (†), namely that
 如果几个特征值具有相同的模，那么证明就失效了，我们不能再声称（†），即

lim ΛkLΛ−k = I. k7→∞
 lim∧kl∧−k=i.k7→∞

If we assume that P −1 has a suitable “block LU-factorization,” it can be shown that the matrices Ak+1 converge to a block upper-triangular matrix, where each block corresponds to eigenvalues having the same modulus. For example, if A is a 9 × 9 matrix with eigenvalues λi such that |λ1| = |λ2| = |λ3| > |λ4| > |λ5| = |λ6| = |λ7| = |λ8| = |λ9|, then Ak converges to a block diagonal matrix (with three blocks, a 3 × 3 block, a 1 × 1 block, and a 5 × 5 block)
 如果我们假设P−1有一个合适的“块Lu因子分解”，可以证明矩阵AK+1收敛到块上三角矩阵，其中每个块对应具有相同模的特征值。例如，如果a是一个特征值为λi的9×9矩阵，使得 =124\ \\124;λ1 \\124;  \124\ \ λi的特征值为λi的9×9矩阵为\\ \\\\\\\\\\\124; \块）

| of the   form    网络错误                                    |                                                              |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| ?    网络错误   ? ?    网络错误       网络错误   0    网络错误       网络错误   0    网络错误       网络错误       网络错误   0    网络错误       网络错误   0    网络错误       网络错误   0    网络错误   0    网络错误 | ?    网络错误   ?    网络错误   ?    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | ?    网络错误   ?    网络错误   ?    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | ∗ ∗         ∗ ∗ ∗        ∗    网络错误   ∗ ∗  ∗ ∗ ∗      ∗     网络错误   ∗ ∗         ∗ ∗ ∗        ∗    网络错误   ?     ∗ ∗         ∗   ∗ ∗    网络错误   0     ?     ?     ?     ?       ?. 0   ?     ?       ?     ?     ?    网络错误   0   ?    ?    ?    ?   ?    网络错误   0     ?     ?     ?     ?       ? 0    ?     ?       ?     ?     ?    网络错误 |

See Ciarlet [41] (Chapter 6 Section 6.3) for more details.
 更多详情请参见CIARLET[41]（第6章第6.3节）。

Under the conditions of Theorem 22.1, in particular, if A is a symmetric (or Hermitian) positive definite matrix, the eigenvectors of A can be approximated. However, when A is not a symmetric matrix, since the upper triangular part of Ak does not necessarily converge, one has to be cautious that a rigorous justification is lacking.
 在定理22.1的条件下，特别是，如果a是对称（或厄米特）正定矩阵，则a的特征向量可以近似。然而，当a不是对称矩阵时，由于ak的上三角部分不一定收敛，因此必须注意缺乏严格的理由。

Suppose we apply the QR algorithm to a matrix A satisfying the hypotheses of Theorem Theorem 22.1. For k large enough,  is nearly upper triangular and the diagonal entries of Ak+1 are all distinct, so we can consider that they are the eigenvalues of Ak+1, and thus of A. To avoid too many subscripts, write T for the upper triangular matrix
 假设我们将QR算法应用于满足定理22.1假设的矩阵A。当k足够大时，是近上三角的，且ak+1的对角项都是不同的，因此我们可以认为它们是ak+1的特征值，因此是a的特征值。为了避免下标太多，请为上三角矩阵写t。


 

obtained by settting the entries of the part of Ak+1 below the diagonal to 0. Then we can find the corresponding eigenvectors by solving the linear system
 通过将对角线下的AK+1部分的条目设置为0获得。然后通过求解线性系统，求出相应的特征向量。

Tv = tiiv,
 tv=tiiv，

and since T is upper triangular, this can be done by bottom-up elimination. We leave it as an exercise to show that the following vectors ) are eigenvectors:
 因为T是上三角形，所以这可以通过自下而上的消除来实现。我们把它作为一个练习来证明以下向量）是特征向量：

v1 = e1,
 v1=e1，

and if i = 2,...,n, then
 如果i=2，…，n，那么

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

.
 .

Then the vectors (Pkv1,...,Pkvn) are a basis of (approximate) eigenvectors for A. In the special case where T is a diagonal matrix, then vi = ei for i = 1,...,n and the columns of Pk are an orthonormal basis of (approximate) eigenvectors for A.
 然后向量（pkv1，…，pkvn）是a的特征向量（近似）的基础，在t是对角矩阵的特殊情况下，i=1，…，n的vi=ei和pk的列是a的特征向量（近似）的正交基。

If A is a real matrix whose eigenvalues are not all real, then there is some complex pair of eigenvalues λ + iµ (with µ = 0)6 , and the QR-algorithm cannot converge to a matrix whose strictly lower-triangular part is zero. There is a way to deal with this situation using upper Hessenberg matrices which will be discussed in the next section.
 如果a是一个实矩阵，其特征值不都是实的，则存在一对复杂的特征值λ+i礹（具有礹=0）6，qr算法不能收敛到严格下三角部分为零的矩阵。有一种方法可以使用上赫森堡矩阵来处理这种情况，这将在下一节中讨论。

Since the convergence of the QR method depends crucially only on the fact that the part of Ak below the diagonal goes to zero, it would be highly desirable if we could replace A by a similar matrix U∗AU easily computable from A having lots of zero strictly below the diagonal. We can’t expect U∗AU to be a diagonal matrix (since this would mean that A was easily diagonalized), but it turns out that there is a way to construct a matrix H = U∗AU which is almost triangular, except that it may have an extra nonzero diagonal below the main diagonal. Such matrices called Hessenberg matrices are discussed in the next section.
 由于qr方法的收敛性主要取决于一个事实，即对角线下的ak部分变为零，因此，如果我们可以用一个类似的矩阵u au替换a，则很有必要从严格位于对角线下的具有大量零的矩阵u au进行计算。我们不能期望u au是一个对角矩阵（因为这意味着a很容易对角化），但事实证明有一种方法可以构造一个几乎是三角形的矩阵h=u au，除了它在主对角线下面可能有一个额外的非零对角线。下一节将讨论这种称为Hessenberg矩阵的矩阵。

## 22.2       Hessenberg Matrices  22.2 Hessenberg矩阵

Definition 22.1. An n × n matrix (real or complex) H is an (upper) Hessenberg matrix if it is almost triangular, except that it may have an extra nonzero diagonal below the main diagonal. Technically, hjk = 0 for all (j,k) such that j − k ≥ 2.
 定义22.1.n×n矩阵（实数或复数）h是（上）Hessenberg矩阵，如果它几乎是三角形的，除了在主对角线下面可能有一个额外的非零对角线。从技术上讲，所有（j，k）的hjk=0，因此j−k≥2。

The 5 × 5 matrix below is an example of a Hessenberg matrix.
 下面的5×5矩阵是Hessenberg矩阵的一个例子。

​                                                              ∗       ∗       ∗       ∗      ∗
  ∗                                                         ∗         ∗       ∗     ∗

​                                                            h21     ∗       ∗       ∗      ∗
 H21

​                                                    H =  0     h32    ∗       ∗     ∗.
 H=0 H32。

​                                                                                                  
                                                           

​                                                              0       0    h43    ∗      ∗
 0 0 h43__

​                                                                 0      0       0    h54   ∗
 0 0 0 h54_

The following result can be shown.
 可以显示以下结果。

Theorem 22.2. Every n × n complex or real matrix A is similar to an upper Hessenberg matrix H, that is, A = UHU∗ for some unitary matrix U. Furthermore, H can be constructed as a product of Householder matrices (the definition is the same as in Section 12.1, except that W is a complex vector, and that the inner product is the Hermitian inner product on Cn). If A is a real matrix, then H is an orthogonal matrix (and H is a real matrix).
 定理22.2.每一个n×n复数或实数矩阵a都类似于上赫森堡矩阵h，也就是说，对于某些单位矩阵u，a=uhu。此外，h可以被构造为户主矩阵的乘积（定义与第12.1节中的定义相同，只是w是一个复数向量，并且innER产品是中国大陆的赫敏内产品。如果a是实矩阵，那么h是正交矩阵（h是实矩阵）。

Theorem 22.2 and algorithms for converting a matrix to Hessenberg form are discussed in Trefethen and Bau [171] (Lecture 26), Demmel [49] (Section 4.4.6, in the real case), Serre [151] (Theorem 13.1), and Meyer [122] (Example 5.7.4, in the real case). The proof of correctness is not difficult and will be the object of a homework problem.
 定理22.2和将矩阵转换为Hessenberg形式的算法在Trefethen和Bau[171]（第26讲）、Demmel[49]（第4.4.6节，在实际情况下）、Serre[151]（定理13.1）和Meyer[122]（在实际情况下，示例5.7.4）中进行了讨论。正确性的证明并不难，而且将成为家庭作业问题的对象。

The following functions written in Matlab implement a function to compute a Hessenberg form of a matrix.
 以下用matlab编写的函数实现了一个计算矩阵Hessenberg形式的函数。

The function house constructs the normalized vector u defining the Householder reflection that zeros all but the first entries in a vector x.
 函数屋构造标准化向量u，定义了户主反射，它将向量x中除第一个条目之外的所有条目归零。

function [uu, u] = house(x) tol = 2*10^(-15);  % tolerance uu = x; p = size(x,1);
 函数[u u，u]=house（x）tol=2*10^（-15）；%公差uu=x；p=size（x，1）；

% computes l^1-norm of x(2:p,1) n1 = sum(abs(x(2:p,1))); if n1 <= tol
 %计算x的l^1-范数（2:p，1）n1=和（abs（x（2:p，1））；如果n1<=tol

u = zeros(p,1); uu = u;
 u=零（p，1）；uu=u；

else
 其他的

l = sqrt(x’*x); % l^2 norm of x uu(1) = x(1) + signe(x(1))*l; u = uu/sqrt(uu’*uu); end end
 l=sqrt（x'*x）；%l^2 x u u（1）=x（1）+signe（x（1））*l；u=uu/sqrt（uu'*uu）；结束

The function signe(z) returms −1 if z < 0, else +1.
 如果z<0，则函数signe（z）返回−1，否则返回+1。

The function buildhouse builds a Householder reflection from a vector uu.
 buildhouse函数从向量UU构建一个户主反射。

function P = buildhouse(v,i)
 功能P=建筑房屋（V，I）

% This function builds a Householder reflection
 %这个功能建立了一个户主的反映

%    [I 0 ] %  [0 PP]
 %[I 0]%[0页]

%          from a Householder reflection
 %从户主的反映

%        PP = I - 2uu*uu’
 %pp=i-2uu*uu'

%        where uu = v(i:n)
 %式中uu=v（i:n）

%           If uu = 0 then P - I
 %如果uu=0，则p-i

%
 %

n = size(v,1); if v(i:n) == zeros(n - i + 1,1)
 n=尺寸（v，1）；如果v（i:n）=0（n-i+1,1）

P = eye(n); else
 P=眼睛（N）；其他

PP = eye(n - i + 1) - 2*v(i:n)*v(i:n)’;
 pp=眼睛（n-i+1）-2*v（i:n）*v（i:n）'；

P = [eye(i-1) zeros(i-1, n - i + 1); zeros(n - i + 1, i - 1) PP]; end end
 P=[眼（i-1）零（i-1，n-i+1）；零（n-i+1，i-1）p p]；结束

The function Hessenberg1 computes an upper Hessenberg matrix H and an orthogonal matrix Q such that A = Q>HQ.
 函数Hessenberg1计算一个上Hessenberg矩阵h和一个正交矩阵q，使a=q>hq。

function [H, Q] = Hessenberg1(A)
 函数[h，q]=Hessenberg1（a）

%
 %

%           This function constructs an upper Hessenberg
 %此函数构造上Hessenberg

%            matrix H and an orthogonal matrix Q such that
 %矩阵H和正交矩阵Q

%       A = Q’ H Q
 %A=Q’H Q

n = size(A,1);
 n=尺寸（a，1）；

H = A;
 H＝a；

Q = eye(n); for i = 1:n-2
 Q=眼睛（n）；对于i=1:n-2

% H(i+1:n,i)
 %h（i+1:n，i）

[~,u] = house(H(i+1:n,i));
 [~，u]=房屋（h（i+1:n，i））；

% u
 %u

P     = buildhouse(u,1);
 =建筑用房（U，1）；

Q(i+1:n,i:n) = P*Q(i+1:n,i:n);
 q（i+1:n，i:n）=p*q（i+1:n，i:n）；

H(i+1:n,i:n) = H(i+1:n,i:n) - 2*u*(u’)*H(i+1:n,i:n);
 h（i+1:n，i:n）=h（i+1:n，i:n）-2*u*（u’）*h（i+1:n，i:n）；

H(1:n,i+1:n) = H(1:n,i+1:n) - 2*H(1:n,i+1:n)*u*(u’); end end
 H（1:N，I+1:N）=H（1:N，I+1:N）-2*H（1:N，I+1:N）*U*（U’）；端部

Example 22.2. If
 例22.2。如果

 ,
 ，

running Hessenberg1 we find
 运行Hessenberg1我们发现

|  1.0000    网络错误   H = −−50..38520000    网络错误       网络错误   0    网络错误   1.0000    网络错误 | −155..20693852    网络错误   −10..68930000    网络错误   −    网络错误   0    网络错误 | 0    网络错误   −10..68932069    网络错误   −0.0000    网络错误   0    网络错误 | 0     网络错误   −0.0000    网络错误   −0.0000    网络错误   0.0000    网络错误   0     网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |

Q   =  00      −00.8339.3714 −00.1516.5571 −−00..74285307.
 =00−00.8339.3714−00.1516.5571−00..74285307。


 γ

​                                                      0         0.4082    −0.8165    0.4082
 0 0.4082−0.8165 0.4082

An important property of (upper) Hessenberg matrices is that if some subdiagonal entry Hp+1p = 0, then H is of the form
 Hessenberg矩阵（上）的一个重要性质是，如果某个次极性项hp+1p=0，则h的形式为

 ,
 ，

where both H11 and H22 are upper Hessenberg matrices (with H11 a p×p matrix and H22 a (n − p) × (n − p) matrix), and the eigenvalues of H are the eigenvalues of H11 and H22. For
 其中h11和h22都是上Hessenberg矩阵（具有h11 a p×p矩阵和h22 a（n-p）×n-p矩阵），h的特征值是h11和h22的特征值。为了

| example,   in the matrix    网络错误                         |                                                              |                                                              |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|  ∗    网络错误   h21    网络错误   H =  0    网络错误       网络错误    0    网络错误   0    网络错误   if h43 = 0, then we have the block matrix    网络错误 | ∗    网络错误   ∗    网络错误   h32    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   h∗43    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   ∗    网络错误   ∗ h54    网络错误 | ∗ ∗    网络错误   ∗,    网络错误   ∗    网络错误   ∗    网络错误 |
|  ∗    网络错误   h21    网络错误   H =  0    网络错误       网络错误    0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   h32    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   ∗0    网络错误   0    网络错误 | ∗    网络错误   ∗ ∗    网络错误   ∗ h54    网络错误          | ∗ ∗    网络错误   ∗.    网络错误   ∗    网络错误   ∗    网络错误 |

Then the list of eigenvalues of H is the concatenation of the list of eigenvalues of H11 and the list of the eigenvalues of H22. This is easily seen by induction on the dimension of the block H11.
 h的特征值列表是h11的特征值列表和h22的特征值列表的串联。通过对H11块尺寸的归纳，很容易看出这一点。

More generally, every upper Hessenberg matrix can be written in such a way that it has diagonal blocks that are Hessenberg blocks whose subdiagonal is not zero.
 更一般地说，每一个上海森堡矩阵都可以用这样的方式来写：它有对角块，这是海森堡块，其次对角块不是零。

Definition 22.2. An upper Hessenberg n × n matrix H is unreduced if hi+1i = 06 for i = 1,...,n − 1. A Hessenberg matrix which is not unreduced is said to be reduced.
 定义22.2.如果i=1，…，n−1的hi+1i=06，则上Hessenberg n×n矩阵h是未减少的。一个没有被约化的海森堡矩阵被称为约化矩阵。

The following is an example of an 8 × 8 matrix consisting of three diagonal unreduced Hessenberg blocks:
 以下是一个8×8矩阵的示例，该矩阵由三个对角未缩减的Hessenberg块组成：

| ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif) | ?    网络错误   ?    网络错误   h32    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | ? ? ?    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   ∗?    网络错误   h54    网络错误   0    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗ ∗?    网络错误   ?    网络错误   h65    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗ ∗?    网络错误   ?    网络错误   ? 0 0    网络错误 | ∗    网络错误   ∗    网络错误   ∗    网络错误   ∗    网络错误   ∗    网络错误   ∗?    网络错误   h87    网络错误 | ∗    网络错误   ∗    网络错误    ∗    网络错误       网络错误   ∗.    网络错误       网络错误   ∗    网络错误       网络错误   ∗    网络错误   ? ?    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |

An interesting and important property of unreduced Hessenberg matrices is the following.
 下面是一个有趣的和重要的性质的未减少的海森堡矩阵。

Proposition 22.3. Let H be an n × n complex or real unreduced Hessenberg matrix. Then every eigenvalue of H is geometrically simple, that is, dim(Eλ) = 1 for every eigenvalue λ, where Eλ is the eigenspace associated with λ. Furthermore, if H is diagonalizable, then every eigenvalue is simple, that is, H has n distinct eigenvalues.
 提案22.3.设h为n×n复形或实无约Hessenberg矩阵。那么h的每个特征值在几何上都是简单的，即对于每个特征值λ，dim（eλ）=1，其中eλ是与λ相关的特征空间。此外，如果h是对角化的，那么每个特征值都是简单的，即h有n个不同的特征值。

Proof. We follow Serre’s proof [151] (Proposition 3.26). Let λ be any eigenvalue of H, let
 证据。我们遵循塞尔证明[151]（提案3.26）。设λ为h的任何特征值，设

M = λIn − H, and let N be the (1) matrix obtained from M by deleting its first row and its last column. Since is upper Hessenberg, N is a diagonal matrix with entries −hi+1i = 06 , i = 1,...,n − 1. Thus N is invertible and has rank n − 1. But a matrix has rank greater than or equal to the rank of any of its submatrices, so rank(M) = n − 1, since M is singular. By the rank-nullity theorem, rank(KerN) = 1, that is, dim(Eλ) = 1, as claimed.
 m=λin−h，n是从m中删除第一行和最后一列得到的（1）矩阵。由于是上赫森堡，n是一个对角线矩阵，条目−hi+1i=06，i=1，…，n−1。因此，n是可逆的，具有n-1的秩。但矩阵的秩大于或等于其任何子矩阵的秩，因此秩（m）=n-1，因为m是奇异的。根据秩零定理，秩（kern）=1，即dim（eλ）=1，如权利要求所述。

If H is diagonalizable, then the sum of the dimensions of the eigenspaces is equal to n, which implies that the eigenvalues of H are distinct. 
 如果h是对角化的，那么特征空间的维数之和等于n，这意味着h的特征值是不同的。

As we said earlier, a case where Theorem 22.1 applies is the case where A is a symmetric (or Hermitian) positive definite matrix. This follows from two facts.
 如前所述，定理22.1适用的情况是，a是对称（或厄米特）正定矩阵的情况。这源于两个事实。

The first fact is that if A is Hermitian (or symmetric in the real case), then it is easy to show that the Hessenberg matrix similar to A is a Hermitian (or symmetric in real case) tridiagonal matrix. The conversion method is also more efficient. Here is an example of a symmetric tridiagonal matrix consisting of three unreduced blocks:
 第一个事实是，如果a是厄米特矩阵（或在实际情况下是对称的），那么很容易证明类似a的Hessenberg矩阵是厄米特矩阵（或在实际情况下是对称的）三对角矩阵。转换方法也更有效。下面是一个由三个未减少的块组成的对称三对角矩阵的示例：

| ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif) | β1    网络错误   α2 β2    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0 β2    网络错误   α3    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0 α4 β4    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0 β4    网络错误   α5 β5    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   0 β5    网络错误   α6    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   0    网络错误   0    网络错误   0 α7 β7    网络错误 | 0     网络错误   0     网络错误   0     网络错误   0  0 .    网络错误   0     网络错误   β7 α8    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |

Thus the problem of finding the eigenvalues of a symmetric (or Hermitian) matrix reduces to the problem of finding the eigenvalues of a symmetric (resp. Hermitian) tridiagonal matrix, and this can be done much more efficiently.
 因此，求对称（或厄米特）矩阵的特征值的问题可归结为求对称（或厄米特）矩阵的特征值的问题。赫密特）三对角矩阵，这可以更有效地完成。

The second fact is that if H is an upper Hessenberg matrix and if it is diagonalizable, then there is an invertible matrix P such that H = PΛP −1 with Λ a diagonal matrix consisting of the eigenvalues of H, such that P −1 has an LU-decomposition; see Serre [151] (Theorem
 第二个事实是，如果h是一个上海森堡矩阵，如果它是对角化的，那么就有一个可逆矩阵p，使得h=p∧p−1带有∧一个由h的特征值组成的对角矩阵，这样p−1有一个lu分解；见serre[151]（定理

13.3).
 13.3）。

As a consequence, since any symmetric (or Hermitian) tridiagonal matrix is a block diagonal matrix of unreduced symmetric (resp. Hermitian) tridiagonal matrices, by Proposition 22.3, we see that the QR algorithm applied to a tridiagonal matrix which is symmetric (or Hermitian) positive definite converges to a diagonal matrix consisting of its eigenvalues. Let us record this important fact.
 因此，由于任何对称（或厄米提亚）三对角矩阵都是非降阶对称（resp）的块对角矩阵。Hermitian）三对角矩阵，通过22.3，我们看到应用于对称（或Hermitian）正定的三对角矩阵的QR算法收敛到由其特征值组成的对角矩阵。让我们记录下这一重要事实。

Theorem 22.4. Let H be a symmetric (or Hermitian) positive definite tridiagonal matrix. If H is unreduced, then the QR algorithm converges to a diagonal matrix consisting of the eigenvalues of H.
 定理22.4.设h为对称（或厄米特）正定三对角矩阵。如果h不被约化，则qr算法收敛到由h的特征值组成的对角矩阵。

Since every symmetric (or Hermitian) positive definite matrix is similar to tridiagonal symmetric (resp. Hermitian) positive definite matrix, we deduce that we have a method for finding the eigenvalues of a symmetric (resp. Hermitian) positive definite matrix (more accurately, to find approximations as good as we want for these eigenvalues).
 因为每一个对称（或厄米特）正定矩阵都与三对角对称（resp）相似。厄米特）正定矩阵，我们推导出一种求对称（resp）特征值的方法。正定矩阵（更准确地说，为了找到这些特征值的近似值）。

If A is a symmetric (or Hermitian) matrix, since its eigenvalues are real, for some µ > 0 large enough (pick µ > ρ(A)), A + µI is symmetric (resp. Hermitan) positive definite, so we can apply the QR algorithm to an upper Hessenberg matrix similar to A+µI to find its eigenvalues, and then the eigenvalues of A are obtained by subtracting µ.
 如果a是对称（或厄米特）矩阵，由于其特征值是实的，对于一些足够大的μ>0（pickμ>ρ（a）），a+μi是对称的（resp.Hermitan）正定的，因此我们可以将qr算法应用到一个类似于a+μi的上Hessenberg矩阵中，找到它的特征值，然后通过减去μ得到a的特征值。

The problem of finding the eigenvalues of a symmetric matrix is discussed extensively in Parlett [131], one of the best references on this topic.
 关于对称矩阵的特征值的求法问题，帕莱特[131]对此作了广泛的讨论，这是本课题的最佳参考文献之一。

The upper Hessenberg form also yields a way to handle singular matrices. First, checking the proof of Proposition 13.21 that an n × n complex matrix A (possibly singular) can be factored as A = QR where Q is a unitary matrix which is a product of Householder reflections and R is upper triangular, it is easy to see that if A is upper Hessenberg, then Q is also upper Hessenberg. If H is an unreduced upper Hessenberg matrix, since Q is upper Hessenberg and R is upper triangular, we have hi+1i = qi+1irii for i = 1...,n−1, and since H is unreduced, rii = 06 for i = 1,...,n−1. Consequently H is singular iff rnn = 0. Then the matrix RQ is a matrix whose last row consists of zero’s thus we can deflate the problem by considering the (n − 1) × (n − 1) unreduced Hessenberg matrix obtained by deleting the last row and the last column. After finitely many steps (not larger that the multiplicity of the eigenvalue 0), there remains an invertible unreduced Hessenberg matrix. As an alternative, see Serre [151] (Chapter 13, Section 13.3.2).
 上海森堡形式也产生了一种处理奇异矩阵的方法。首先，检查命题13.21的证明，一个n×n的复数矩阵a（可能是奇异的）可以被分解为a=q r，其中q是户主反射的乘积，r是上三角形，很容易看出，如果a是上Hessenberg，那么q也是上Hes森伯格。如果h是一个未减少的上Hessenberg矩阵，因为q是上Hessenberg矩阵，r是上三角形，我们有h i+1i=qi+1i rii表示i=1…，n-1，并且由于h是未减少的，rii=06表示i=1，…，n-1。因此，h是单数iff rnn=0。那么矩阵rq是最后一行由零组成的矩阵，因此我们可以通过考虑删除最后一行和最后一列得到的（n-1）×（n-1）未减少的Hessenberg矩阵来消除问题。在有限多个步骤之后（不大于特征值0的多重性），仍然存在一个可逆的不可约Hessenberg矩阵。作为替代方案，见SERRE[151]（第13章，第13.3.2节）。

As is, the QR algorithm, although very simple, is quite inefficient for several reasons. In the next section, we indicate how to make the method more efficient. This involves a lot of work and we only discuss the main ideas at a high level.
 事实上，QR算法虽然很简单，但由于几个原因效率很低。在下一节中，我们将说明如何提高方法的效率。这涉及到很多工作，我们只在高层讨论主要想法。


 

## 22.3     Making the QR Method More Efficient Using Shifts  22.3提高使用轮班的QR方法的效率

To improve efficiency and cope with pairs of complex conjugate eigenvalues in the case of real matrices, the following steps are taken:
 为了提高效率，并应对实矩阵中的复共轭特征值对，采取以下步骤：

(1)    Initially reduce the matrix A to upper Hessenberg form, as A = UHU∗. Then apply the QR-algorithm to H (actually, to its unreduced Hessenberg blocks). It is easy to see that the matrices Hk produced by the QR algorithm remain upper Hessenberg.
 最初将矩阵A简化为上赫森堡形式，即A=uhu。然后将qr算法应用于h（实际上，应用于其未减少的hessenberg块）。很容易看出，由QR算法生成的矩阵hk仍保持在Hessenberg的上方。

(2)    To accelerate convergence, use shifts, and to deal with pairs of complex conjugate eigenvalues, use double shifts.
 为了加速收敛，使用移位，为了处理复共轭特征值对，使用双移位。

(3)    Instead of computing a QR-factorization explicitly while doing a shift, perform an implicit shift which computes  without having to compute a QRfactorization (of Ak − σkI), and similarly in the case of a double shift. This is the most intricate modification of the basic QR algorithm and we will not discuss it here. This method is usually referred as bulge chasing. Details about this technique for real matrices can be found in Demmel [49] (Section 4.4.8) and Golub and Van Loan [80] (Section 7.5). Watkins discusses the QR algorithm with shifts as a bulge chasing method in the more general case of complex matrices [181, 182].
 在进行移位时，不需要显式计算qr因子分解，而是执行隐式移位，该移位不需要计算qr factorization（ak-σki），同样，在进行双移位时也需要计算qrfactorization。这是对基本QR算法最复杂的修改，我们在这里不讨论它。这种方法通常被称为鼓包追逐。有关真实矩阵的这种技术的详细信息，请参见demmel[49]（第4.4.8节）和Golub和van Loan[80]（第7.5节）。在复杂矩阵的更一般情况下，Watkins讨论了将移位作为凸点追踪方法的QR算法[181182]。

Let us repeat an important remark made in the previous section. If we start with a matrix H in upper Hessenberg form, if at any stage of the QR algorithm we find that some subdiagonal entry (Hk)p+1p = 0 or is very small, then Hk is of the form
 让我们重复上一节中的一个重要评论。如果我们以Hessenberg上形式的矩阵h开始，如果在qr算法的任何阶段，我们发现某些次方向项（hk）p+1p=0或非常小，那么hk就是这种形式。

 ,
 ，

| a (n − p) × (n − p) matrix), and   the eigenvalues of Hk are the eigenvalues of H11 and H22.    网络错误 |                                                              |                                                              |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| For   example, in the matrix    网络错误                     |                                                              |                                                              |                                                              |                                                              |
|  ∗    网络错误   h21    网络错误   H =  0    网络错误       网络错误    0    网络错误   0    网络错误   if h43 = 0, then we have the block matrix    网络错误 | ∗    网络错误   ∗    网络错误   h32    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   h∗43    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   ∗    网络错误   ∗ h54    网络错误 | ∗ ∗    网络错误   ∗,    网络错误   ∗    网络错误   ∗    网络错误 |
|  ∗    网络错误   h21    网络错误   H =  0    网络错误       网络错误    0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   h32    网络错误   0    网络错误   0    网络错误 | ∗    网络错误   ∗    网络错误   ∗0    网络错误   0    网络错误 | ∗    网络错误   ∗ ∗    网络错误   ∗   h54    网络错误        | ∗ ∗    网络错误   ∗.    网络错误   ∗    网络错误   ∗    网络错误 |

where both H11 and H22 are upper Hessenberg matrices (with H11 a p × p matrix and H22 Then we can recursively apply the QR algorithm to H11 and H22.
 其中h11和h22都是上Hessenberg矩阵（h11是p×p矩阵和h22），那么我们可以递归地将qr算法应用于h11和h22。

In particular, if (Hk)nn−1 = 0 or is very small, then (Hk)nn is a good approximation of an eigenvalue, so we can delete the last row and the last column of Hk and apply the QR algorithm to this submatrix. This process is called deflation. If (Hk)n−1n−2 = 0 or is very small, then the 2 × 2 “corner block”
 特别是，如果（hk）nn−1=0或非常小，那么（hk）nn是特征值的良好近似值，因此我们可以删除hk的最后一行和最后一列，并将qr算法应用于该子矩阵。这个过程叫做通货紧缩。如果（hk）n−1n−2=0或非常小，则2×2“角块”

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

appears, and its eigenvalues can be computed immediately by solving a quadratic equation. Then we deflate Hk by deleting its last two rows and its last two columns and apply the QR algorithm to this submatrix.
 出现了，它的特征值可以通过解二次方程立即计算出来。然后，我们通过删除最后两行和最后两列来缩小hk，并将qr算法应用于该子矩阵。

Thus it would seem desirable to modify the basic QR algorithm so that the above situations arises, and this is what shifts are designed for. More precisely, under the hypotheses of Theorem 22.1, it can be shown (see Ciarlet [41], Section 6.3) that the entry (Ak)ij with i > j converges to 0 as |λi/λj|k converges to 0. Also, if we let ri be defined by
 因此，似乎需要修改基本的QR算法，以便出现上述情况，这就是移位的设计目的。更准确地说，在定理22.1的假设下，可以证明（见Ciarlet[41]第6.3节），i>j的入口（ak）ij收敛到0，因为λi/λj_k收敛到0。另外，如果我们让ri定义为

,
 ，

then there is a constant C (independent of k) such that
 然后有一个常数c（独立于k），这样

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image019.gif)

In particular, if H is upper Hessenberg, then the entry (Hk)i+1i converges to 0 as |λi+1/λi|k converges to 0. Thus if we pick σk close to λi, we expect that (Hk − σkI)i+1i converges to 0 as |(λi+1 −σk)/(λi −σk)|k converges to 0, and this ratio is much smaller than 1 as σk is closer to λi. Typically, we apply a shift to accelerate convergence to λn (so i = n − 1). In this case, both (Hk −σkI)nn−1 and |(Hk −σkI)nn −λn| converge to 0 as |(λn −σk)/(λn−1 −σk)|k converges to 0.
 特别是，如果h是上Hessenberg，则条目（h k）i+1i收敛到0，因为λi+1/λi_k收敛到0。因此，如果我们选取靠近λi的σk，我们期望（hk−σki）i+1i收敛到0，因为（λi+1−σk）/（λi−σk）k收敛到0，并且这个比率比1小得多，因为σk更接近λi。通常，我们应用移位来加速收敛到λn（因此i=n-1）。在这种情况下，（hk−σki）nn-1和（hk−σki）nn−λn收敛到0，因为（λn−σk）/（λn−1−σk）k收敛到0。

A shift is the following modified QR-steps (switching back to an arbitrary matrix A, since the shift technique applies in general). Pick some σk, hopefully close to some eigenvalue of A (in general, λn), and QR-factor Ak − σkI as
 移位是以下修改的QR步骤（切换回任意矩阵A，因为移位技术通常适用）。选择一些σk，希望接近a的特征值（一般来说，λn），以及qr因子ak-σki作为

Ak − σkI = QkRk,
 AK−σki=qkrk，

and then form
 然后形成

Ak+1 = RkQk + σkI.
 AK+1=RKQK+σki。

Since
 自从

Ak+1 = RkQk + σkI
 AK+1=RKQK+σki

= Q∗kQkRkQk + Q∗kQkσk
 =q kqkrkqk+q k q kσk

= Q∗k(QkRk + σkI)Qk
 =q k（qkrk+σki）qk

= Q∗kAkQk,
 =Q Kakqk，

Ak+1 is similar to Ak, as before. If Ak is upper Hessenberg, then it is easy to see that Ak+1 is also upper Hessenberg.
 AK+1与AK类似，如前所述。如果ak是上海森堡，那么很容易看出ak+1也是上海森堡。

If A is upper Hessenberg and if σi is exactly equal to an eigenvalue, then Ak − σkI is singular, and forming the QR-factorization will detect that Rk has some diagonal entry equal to 0. Assuming that the QR-algorithm returns (Rk)nn = 0 (if not, the argument is easily adapted), then the last row of RkQk is 0, so the last row of Ak+1 = RkQk + σkI ends with σk (all other entries being zero), so we are in the case where we can deflate Ak (and σk is indeed an eigenvalue).
 如果a是上Hessenberg，如果σi正好等于特征值，那么ak-σki是奇异的，形成qr因式分解将检测到Rk有一些等于0的对角线入口。假设qr算法返回（rk）nn=0（如果不是，参数很容易适应），那么RKQK的最后一行是0，所以AK+1=RKQK+σki的最后一行以σk结尾（所有其他项都为零），所以我们可以对ak进行放气（而σk实际上是一个特征值）。

The question remains, what is a good choice for the shift σk?
 问题是，对于移位σk，什么是一个好的选择？

Assuming again that H is in upper Hessenberg form, it turns out that when (Hk)nn−1 is small enough, then a good choice for σk is (Hk)nn. In fact, the rate of convergence is quadratic, which means roughly that the number of correct digits doubles at every iteration. The reason is that shifts are related to another method known as inverse iteration, and such a method converges very fast. For further explanations about this connection, see Demmel [49] (Section 4.4.4) and Trefethen and Bau [171] (Lecture 29).
 再次假设h为上Hessenberg形式，结果表明当（h k）nn-1足够小时，σk的一个好选择是（hk）nn。事实上，收敛速度是二次的，这意味着在每次迭代中，正确数字的数目大致都会加倍。原因是移位与另一种称为逆迭代的方法有关，这种方法收敛得很快。关于这种联系的进一步解释，见demmel[49]（第4.4.4节）和trefethen和bau[171]（第29课）。

One should still be cautious that the QR method with shifts does not necessarily converge, and that our convergence proof no longer applies, because instead of having the identity Ak = PkRk, we have
 我们仍然应该谨慎，带移位的qr方法不一定收敛，并且我们的收敛证明不再适用，因为我们没有拥有标识ak=pkrk，而是

(A − σkI)···(A − σ2I)(A − σ1I) = PkRk.
 （a−σki）···（a−σ2i）（a−σ1i）=pkrk。

Of course, the QR algorithm loops immediately when applied to an orthogonal matrix A. This is also the case when A is symmetric but not positive definite. For example, both the QR algorithm and the QR algorithm with shifts loop on the matrix
 当然，当应用于正交矩阵A时，QR算法会立即循环，当A是对称的但不是正定的时候也是如此。例如，QR算法和矩阵上带移位环的QR算法

 .
 .

In the case of symmetric matrices, Wilkinson invented a shift which helps the QR algorithm with shifts to make progress. Again, looking at the lower corner of Ak, say
 在对称矩阵的情况下，威尔金森发明了一种移位，这有助于QR算法的移位取得进展。再看看AK的下角，说

,
 ，

the Wilkinson shift picks the eigenvalue of B closer to an. If we let
 威尔金森位移选取的特征值B更接近A。如果我们让

δ = an−1 − an ,
 δ=an−1−an，

2
 二

it is easy to see that the eigenvalues of B are given by
 很容易看出，b的特征值由

.
 .

It follows that
 接下来是

q λ − an = δ ±   δ2 + b2n−1,
 qλ−an=δ±δ2+b2n−1，

and from this it is easy to see that the eigenvalue closer to an is given by
 从这个很容易看出，更接近a的特征值是由

.
 .

If δ = 0, then we pick arbitrarily one of the two eigenvalues. Observe that the Wilkinson shift applied to the matrix
 如果δ=0，那么我们可以任意选取两个特征值中的一个。观察应用于矩阵的威尔金森位移

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image021.gif)

is either +1 or −1, and in one step, deflation occurs and the algorithm terminates successfully.
 是+1或−1，在一个步骤中，会发生通缩，算法成功终止。

We now discuss double shifts, which are intended to deal with pairs of complex conjugate eigenvalues.
 我们现在讨论双移位，这是为了处理复共轭特征值对。

Let us assume that A is a real matrix. For any complex number σk with nonzero imaginary part, a double shift consists of the following steps:
 假设A是一个实矩阵。对于具有非零虚数部分的复数σk，双移位包括以下步骤：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image023.gif)

From the computation made for a single shift, we have Ak+1 = Q∗kAkQk and Ak+2 =
 根据对单个位移的计算，我们得到了ak+1=q kakqk和ak+2。=

Q∗k+1Ak+1Qk+1, so we obtain
 q k+1ak+1qk+1，因此我们得出

.
 .

The matrices Qk are complex, so we would expect that the Ak are also complex, but remarkably we can keep the products QkQk+1 real, and so the Ak also real. This is highly desirable to avoid complex arithmetic, which is more expensive. Observe that since
 矩阵qk是复杂的，所以我们希望ak也是复杂的，但很明显我们可以保持产品qkqk+1是真实的，所以ak也是真实的。这是非常理想的避免复杂的算术，这是更昂贵的。从那以后再观察

Qk+1Rk+1 = Ak+1 − σkI = RkQk + (σk − σk)I,
 qk+1rk+1=ak+1−σk i=rkqk+（σk−σk）i，

we have
 我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image025.gif)

If we assume by induction that matrix Ak is real (with k = 2`+1,` ≥ 0), then the matrix S = A2k − 2(<σk)Ak + |σk|2I is also real, and since QkQk+1 is unitary and Rk+1Rk is upper triangular, we see that
 如果我们通过归纳假设矩阵ak是实的（k=2`+1，`≥0），那么矩阵s=a2k−2（<σk）ak+σk 2i也是实的，因为qkqk+1是一元的，而rk+1rk是上三角的，我们可以看到

S = QkQk+1Rk+1Rk
 S=QKQK+1RK+1RK

is a QR-factorization of the real matrix S, thus QkQk+1 and Rk+1Rk can be chosen to be real matrices, in which case (QkQk+1)∗ is also real, and thus
 是实矩阵s的qr因子分解，因此qkqk+1和rk+1rk可以选择为实矩阵，在这种情况下（qkqk+1）也是实矩阵，因此

Ak+2 = Q∗k+1Q∗kAkQkQk+1 = (QkQk+1)∗AkQkQk+1
 ak+2=q k+1q kakqk+1=（qkqk+1）akqkqk+1

is real. Consequently, if A1 = A is real, then A2`+1 is real for all ` ≥ 0.
 是真的。因此，如果a1=a是实的，那么a2`+1对所有的`≥0都是实的。

The strategy that consists in picking σk and σk as the complex conjugate eigenvalues of the corner block
 选择σk和σk作为角块复共轭特征值的策略

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image027.gif)

is called the Francis shift (here we are assuming that A has be reduced to upper Hessenberg form).
 被称为弗朗西斯位移（这里我们假设a已经被简化为上海森堡形式）。

It should be noted that there are matrices for which neither a shift by (Hk)nn nor the Francis shift works. For instance, the permutation matrix
 应该注意的是，有些矩阵的（hk）nn移位和Francis移位都不起作用。例如，置换矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image029.gif)

has eigenvalues ei2π/3,ei4π/3,+1, and neither of the above shifts apply to the matrix
 具有特征值ei2π/3，ei4π/3，+1，并且上述两种移位都不适用于矩阵

 .
 .

However, a shift by 1 does work. There are other kinds of matrices for which the QR algorithm does not converge. Demmel gives the example of matrices of the form
 但是，按1的移位确实有效。还有其他类型的矩阵，QR算法不收敛。demmel给出了形式矩阵的例子。

​                                                                0     1     0    0
 0 1 0 0_

​                                                                1     0     h    0
 10小时0_

​                                                                 0 −h    0  1
 0−H 0 1

​                                                                   0     0     1   0
 0 0 1 0

where h is small.
 其中h是小的。

Algorithms implementing the QR algorithm with shifts and double shifts perform “exceptional” shifts every 10 shifts. Despite the fact that the QR algorithm has been perfected since the 1960’s, it is still an open problem to find a shift strategy that ensures convergence of all matrices.
 采用移位和双移位的QR算法每10个移位执行一次“异常”移位。尽管自20世纪60年代以来QR算法得到了完善，但寻找一种确保所有矩阵收敛的移位策略仍然是一个开放性问题。

Implicit shifting is based on a result known as the implicit Q theorem. This theorem says that if A is reduced to upper Hessenberg form as A = UHU∗ and if H is unreduced (hi+1i = 06 for i = 1,...,n−1), then the columns of index 2,...,n of U are determined by the first column of U up to sign; see Demmel [49] (Theorem 4.9) and Golub and Van Loan [80] (Theorem 7.4.2) for the proof in the case of real matrices. Actually, the proof is not difficult and will be the object of a homework exercise. In the case of a single shift, an implicit shift generates Ak+1 = Q∗kAkQk without having to compute a QR-factorization of Ak − σkI. For real matrices, this is done by applying a sequence of Givens rotations which perform a bulge chasing process (a Givens rotation is an orthogonal block diagonal matrix consisting of a single block which is a 2D rotation, the other diagonal entries being equal to 1). Similarly, in the case of a double shift, Ak+2 = (QkQk+1)∗AkQkQk+1 is generated without having to compute the QR-factorizations of Ak − σkI and Ak+1 − σkI. Again, (QkQk+1)∗AkQkQk+1 is generated by applying some simple orthogonal matrices which perform a bulge chasing process. See Demmel [49] (Section 4.4.8) and Golub and Van Loan [80] (Section 7.5) for further explanations regarding implicit shifting involving bulge chasing in the case of real matrices. Watkins [181, 182] discusses bulge chasing in the more general case of complex matrices.
 隐式移位是基于一个被称为隐式Q定理的结果。这个定理表明，如果a被简化为a=u h u的上海森堡形式，而h未被简化（i=1，…，n−1，hi+1i=06），那么索引2，…，n的u列由u的第一列直到符号决定；见demmel[49]（定理4.9）和golub和van loan[80]（定理7.4.2）。对于实矩阵的证明。事实上，证明并不难，而且将是家庭作业练习的对象。在单个移位的情况下，隐式移位生成ak+1=q kakqk，而无需计算ak-σki的qr因子分解。对于实矩阵，这是通过应用一系列执行凸起追踪过程的givens旋转来完成的（givens旋转是一个正交的块对角矩阵，由一个二维旋转的单个块组成，其他对角线条目等于1）。同样，在双移位的情况下，AK+2=（QKQK+1）AKQKQK+1生成时不需要计算AK−σki和AK+1−σki的QR因子分解。同样地，（qkqk+1）akqkqk+1是通过应用一些简单的正交矩阵来生成的，这些矩阵执行一个凸起追踪过程。参见demmel[49]（第4.4.8节）和Golub和van Loan[80]（第7.5节），了解关于真实矩阵中涉及凸起追踪的隐式移位的进一步解释。Watkins[181182]讨论了复杂矩阵的更一般情况下的凸度追踪。

The Matlab function for finding the eigenvalues and the eigenvectors of a matrix A is eig and is called as [U, D] = eig(A). It is implemented using an optimized version of the QR-algorithm with implicit shifts.
 求矩阵A的特征值和特征向量的matlab函数是特征值，称为[u，d]=eig（a）。它是使用隐式移位的优化版QR算法实现的。

If the dimension of the matrix A is very large, we can find approximations of some of the eigenvalues of A by using a truncated version of the reduction to Hessenberg form due to Arnoldi in general and to Lanczos in the symmetric (or Hermitian) tridiagonal case.
 如果矩阵A的维数非常大，我们可以通过使用截断形式的约简来找到A的一些特征值的近似值，这种约简形式通常是由于阿诺迪和兰佐斯在对称（或厄米提亚）三对角情况下的约简。

## 22.4         Krylov Subspaces; Arnoldi Iteration  22.4 Krylov子空间；Arnoldi迭代

In this section, we denote the dimension of the square real or complex matrix A by m rather than n, to make it easier for the reader to follow Trefethen and Bau exposition [171], which is particularly lucid.
 在这一节中，我们用m而不是n来表示正方形实矩阵或复矩阵的维数，以便读者更容易遵循Trefetten和Bau论述[171]，这一点特别清晰。

| upper   left block    网络错误 |                                                              |                                                              |                                                             |                                                              |                                                              |
| ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                |     网络错误   h11    网络错误   h21    网络错误       网络错误    0    网络错误   Hen =    ...    网络错误     0    网络错误       网络错误   0    网络错误 | h12 h22 h32 ...    网络错误   ···    网络错误   ···    网络错误 | h13 h23 h33 ...    网络错误   0    网络错误   0    网络错误 | ··· ···    网络错误   ···...    网络错误   hnn−1    网络错误   0    网络错误 | h1n  h2n  h3n     网络错误   ...     网络错误   hnn    hn+1n    网络错误 |

Suppose that the m × m matrix A has been reduced to the upper Hessenberg form H, as A = UHU∗. For any n ≤ m (typically much smaller than m), consider the (n + 1) × n
 假设m×m矩阵a已简化为上赫森堡形式h，即a=uhu。对于任何n≤m（通常小于m），考虑（n+1）×n


 

22.4. KRYLOV SUBSPACES; ARNOLDI ITERATION of H, and the n × n upper Hessenberg matrix Hn obtained by deleting the last row of Hen,
 22.4。Krylov子空间；H的Arnoldi迭代，以及通过删除最后一行hen得到的n×n上Hessenberg矩阵hn，

 .
 .

If we denote by Un the m×n matrix consisting of the first n columns of U, denoted u1,...,un, then matrix consisting of the first n columns of the matrix UH = AU can be expressed as
 如果用u n表示由u的前n列组成的m×n矩阵，表示为u1，…，un，那么由矩阵的前n列组成的矩阵uh=au可以表示为

​                                                                AUn = Un+1Hen.                                                         (∗1)
 aun=un+1小时。（1）

It follows that the nth column of this matrix can be expressed as
 因此，该矩阵的第n列可以表示为

​                                            Aun = h1nu1 + ··· + hnnun + hn+1nun+1.                                    (∗2)
 aun=h1nu1+····+hnnun+hn+1nun+1。（2）

Since (u1,...,un) form an orthonormal basis, we deduce from (∗2) that
 由于（u1，…，un）形成了正态基，我们从（2）推导出

​                                             huj,Auni = u∗jAun = hjn,         j = 1,...,n.                                        (∗3)
 huj，auni=u_jaun=hjn，j=1，…，n.（3）

Equations (∗2) and (∗3) show that Un+1 and Hen can be computed iteratively using the following algorithm due to Arnoldi, known as Arnoldi iteration:
 方程（2）和（3）表明，由于Arnoldi（称为Arnoldi迭代），可以使用以下算法迭代计算un+1和hen：

Given an arbitrary nonzero vector b ∈ Cm, let u1 = b/kbk; for n = 1,2,3,... do z := Aun; for j = 1 to n do hjn := u∗jz;
 给定任意非零向量b∈cm，设u1=b/kbk；对于n=1,2,3，…do z：=aun；对于j=1至n do hjn：=u jz；

z := z − hjnuj
 Z：=Z−HJnuj

endfor hn+1n := kzk; if hn+1n = 0 quit un+1 = z/hn+1n
 endfor hn+1n：=kzk；如果hn+1n=0退出un+1=z/hn+1n

When hn+1n = 0, we say that we have a breakdown of the Arnoldi iteration.
 当hn+1n=0时，我们说Arnoldi迭代有一个分解。

Arnoldi iteration is an algorithm for producing the n×n Hessenberg submatrix Hn of the full Hessenberg matrix H consisting of its first n rows and n columns (the first n columns of U are also produced), not using Householder matrices.
 Arnoldi迭代是一种生成完整的Hessenberg矩阵h的n×n Hessenberg子矩阵hn的算法，该矩阵由其前n行和n列组成（U的前n列也是生成的），而不使用户主矩阵。

As long as hj+1j = 06 for j = 1,...,n, Equation (∗2) shows by an easy induction that un+1 belong to the span of (b,Ab,...,Anb), and obviously Aun belongs to the span of (u1,...,un+1), and thus the following spaces are identical:
 只要j=1，…，n的hj+1j=06，方程（2）通过一个简单的归纳表明，un+1属于（b，ab，…，anb）的跨度，而aun显然属于（u1，…，un+1）的跨度，因此以下空间是相同的：

Span(b,Ab,...,Anb) = Span(u1,...,un+1).
 span（b，ab，…，anb）=span（u1，…，un+1）。

The space Kn(A,b) = Span(b,Ab,...,An−1b) is called a Krylov subspace. We can view Arnoldi’s algorithm as the construction of an orthonormal basis for Kn(A,b). It is a sort of Gram–Schmidt procedure.
 空间kn（a，b）=span（b，ab，…，an−1b）称为krylov子空间。我们可以将Arnoldi算法看作是构造kn（a，b）的正交基。这是一种克-施密特程序。

Equation (∗2) shows that if Kn is the m × n matrix whose columns are the vectors (b,Ab,...,An−1b), then there is a n × n upper triangular matrix Rn such that
 方程（2）表明，如果kn是m×n矩阵，其列为向量（b，ab，…，an−1b），则存在n×n上三角矩阵rn，从而

​                                                                     Kn = UnRn.                                                             (∗4)
 kn=unrn.（4）

The above is called a reduced QR factorization of Kn.
 上面称为kn的简化qr因子分解。

Since (u1,...,un) is an orthonormal system, the matrix  is the +1) matrix consisting of the identity matrix In plus an extra column of 0’s, so  is
 因为（u1，…，un）是一个正交系统，矩阵是由单位矩阵加上一个0的额外列组成的+1）矩阵，所以

obtained by deleting the last row of Hen, namely Hn, and so
 通过删除母鸡的最后一行，即hn获得，依此类推。

​                                                                             .                                                                       (∗5)
 .（5）

We summarize the above facts in the following proposition.
 我们将上述事实概括为以下命题。

Proposition 22.5. If Arnoldi iteration run on an m × m matrix A starting with a nonzero vector b ∈ Cm does not have a breakdown at stage n ≤ m, then the following properties hold:
 提案22.5.如果Arnoldi迭代在m×m矩阵a上以非零向量b∈cm开始运行，在n≤m阶段没有崩溃，那么以下属性保持不变：

*(1)*     If Kn is the m × n Krylov matrix associated with the vectors (b,Ab,...,An−1b) and if Un is the m × n matrix of orthogonal vectors produced by Arnoldi iteration, then there is a QR-factorization
 如果kn是与向量（b，ab，…，a n−1b）相关联的m×n krylov矩阵，如果un是由Arnoldi迭代生成的正交向量的m×n矩阵，则存在qr因子分解。

Kn = UnRn,
 kn=unrn，

for some n × n upper triangular matrix Rn.
 对于一些n×n上三角矩阵rn。

*(2)*     The m×n upper Hessenberg matrices Hn produced by Arnoldi iteration are the projection of A onto the Krylov space Kn(A,b), that is,
 Arnoldi迭代产生的m×n上Hessenberg矩阵hn是a对krylov空间kn（a，b）的投影，也就是说，

.
 .

*(3)*     The successive iterates are related by the formula
 连续迭代与公式有关

.
 .

Remark: If Arnoldi iteration has a breakdown at stage n, that is, hn+1 = 0, then we found the first unreduced block of the Hessenberg matrix H. It can be shown that the eigenvalues of Hn are eigenvalues of A. So a breakdown is actually a good thing. In this case, we can pick some new nonzero vector un+1 orthogonal to the vectors (u1,...,un) as a new starting vector and run Arnoldi iteration again. Such a vector exists since the (n+1)th column of U works. So repeated application of Arnoldi yields a full Hessenberg reduction of A. However,
 注：如果Arnoldi迭代在n阶段有一个分解，即hn+1=0，那么我们就找到了Hessenberg矩阵h的第一个未简化块，可以证明hn的特征值是a的特征值，所以分解实际上是一件好事。在这种情况下，我们可以选择一些与向量（u1，…，un）正交的新的非零向量un+1作为新的起始向量，并再次运行arnoldi迭代。这种向量存在于u的第（n+1）列工作之后。因此，重复使用阿诺迪得到了一个完整的海森堡减少a。

### 22.4. KRYLOV SUBSPACES; ARNOLDI ITERATION  22.4。Krylov子空间；Arnoldi迭代

this is not what we are after, since m is very large an we are only interested in a “small” number of eigenvalues of A.
 这不是我们所追求的，因为m非常大，我们只对a的“少量”特征值感兴趣。

There is another aspect of Arnoldi iteration, which is that it solves an optimization problem involving polynomials of degree n. Let Pn denote the set of (complex) monic polynomials of degree n, that is, polynomials of the form
 Arnoldi迭代还有一个方面，它解决了一个涉及n次多项式的优化问题。让pn表示n次（复数）多项式的集合，即形式的多项式。

​                                      p(z) = zn + cn−1zn−1 + ··· + c1z + c0      (ci ∈ C).
 p（z）=zn+cn−1zn−1+····+c1z+c0（ci∈c）。

For any m × m matrix A, we write
 对于任何M×M矩阵A，我们写

p(A) = An + cn−1An−1 + ··· + c1A + c0I.
 p（a）=an+cn−1an−1+····+c1a+c0i。

The following result is proven in Trefethen and Bau [171] (Lecture 34, Theorem 34.1).
 以下结果在Trefethen和Bau[171]中得到了证明（第34课，定理34.1）。

Theorem 22.6. If Arnoldi iteration run on an m × m matrix A starting with a nonzero vector b does not have a breakdown at stage n ≤ m, then there is a unique polynomial p ∈ Pn such that kp(A)bk2 is minimum, namely the characteristic polynomial det(zI − Hn) of Hn.
 定理22.6。如果以非零向量b开始的m×m矩阵a上运行的Arnoldi迭代在n≤m阶段没有崩溃，则存在一个唯一的多项式p∈pn，使得kp（a）bk2最小，即hn的特征多项式det（zi-hn）。

Theorem 22.6 can be viewed as the “justification” for a method to find some of the eigenvalues of  of them). Intuitively, the closer the roots of the characteristic polynomials of Hn are to the eigenvalues of A, the smaller kp(A)bk2 should be, and conversely. In the extreme case where m = n, by the Cayley–Hamilton theorem, p(A) = 0 (where p is the characteristic polynomial of A), so this idea is plausible, but this is far from constituting a proof (also, b should have nonzero coordinates in all directions associated with the eigenvalues).
 定理22.6可被视为一种求其某些特征值的方法的“正当性”。直观地说，hn特征多项式的根越接近a的特征值，kp（a）bk2越小，反之亦然。在m=n的极端情况下，根据凯莱-汉密尔顿定理，p（a）=0（其中p是a的特征多项式），所以这个想法是合理的，但这远不能构成一个证明（同时，b在与特征值相关的所有方向上都应该有非零坐标）。

The method known as the Rayleigh–Ritz method is to run Arnoldi iteration on A and some b = 06 chosen at random for steps before or until a breakdown occurs. Then run the QR algorithm with shifts on Hn. The eigenvalues of the Hessenberg matrix Hn may then be considered as approximations of the eigenvalues of A. The eigenvalues of Hn are called Arnoldi estimates or Ritz values. One has to be cautious because Hn is a truncated version of the full Hessenberg matrix H, so not all of the Ritz values are necessary close to eigenvalues of A. It has been observed that the eigenvalues that are found first are the extreme eigenvalues of A, namely those close to the boundary of the spectrum of A plotted in C. So if A has real eigenvalues, the largest and the smallest eigenvalues appear first as Ritz values. In many problems where eigenvalues occur, the extreme eigenvalues are the one that need to be computed. Similarly, the eigenvectors of Hn may be considered as approximations of eigenvectors of A.
 称为瑞利-里兹方法的方法是在a和一些b=06上运行阿诺迪迭代，随机选择步骤，直到出现故障。然后在hn上运行移位的qr算法。然后，可以将Hessenberg矩阵hn的特征值视为a特征值的近似值。hn的特征值称为Arnoldi估计或Ritz值。我们必须谨慎，因为hn是完整的Hessenberg矩阵h的截尾形式，所以并非所有的Ritz值都必须接近a的特征值。据观察，首先找到的特征值是a的极端特征值，即那些接近a的边界的特征值。图中A的谱，如果A有实特征值，最大和最小的特征值首先作为Ritz值出现。在许多特征值出现的问题中，极值特征值是需要计算的。同样，可以将hn的特征向量视为a的特征向量的近似值。

The Matlab function eigs is based on the computation of Ritz values. It computes the six eigenvalues of largest magnitude of a matrix A, and the call is [V, D] = eigs(A). More generally, to get the top k eigenvalues, use [V, D] = eigs(A, k).
 Matlab函数的特征值是基于Ritz值的计算。它计算矩阵A的最大数量的六个特征值，调用为[v，d]=eigs（a）。更一般地说，要得到顶部的k特征值，使用[v，d]=特征值（a，k）。

In the absence of rigorous theorems about error estimates, it is hard to make the above statements more precise; see Trefethen and Bau [171] (Lecture 34) for more on this subject.
 在缺乏关于误差估计的严格定理的情况下，很难使上述陈述更加精确；关于这一主题的更多信息，请参阅Trefethen和Bau[171]（第34课）。

However, if A is a symmetric (or Hermitian) matrix, then Hn is a symmetric (resp. Hermitian) tridiagonal matrix and more precise results can be shown; see Demmel [49] (Chapter 7, especially Section 7.2). We will consider the symmetric (and Hermitan) case in the next section, but first we show how Arnoldi iteration can be used to find approximations for the solution of a linear system Ax = b where A is invertible but of very large dimension m.
 但是，如果a是对称（或厄米特）矩阵，那么hn是对称（resp）。Hermitian）三对角矩阵和更精确的结果可以显示出来；见demmel[49]（第7章，特别是第7.2节）。我们将在下一节中考虑对称（和厄米坦）情况，但首先我们将展示如何使用Arnoldi迭代来寻找线性系统ax=b的近似解，其中a是可逆的，但m的尺寸非常大。

## 22.5        GMRES  22.5克

Suppose A is an invertible m×m matrix and let b be a nonzero vector in Cm. Let x0 = A−1b, the unique solution of Ax = b. It is not hard to show that x0 ∈ Kn(A,b) for some n ≤ m. In fact, there is a unique monic polynomial p(z) of minimal degree s ≤ m such that p(A)b = 0, so x0 ∈ Ks(A,b). Thus it makes sense to search for a solution of Ax = b in Krylov spaces of dimension m ≤ s. The idea is to find an approximation xn ∈ Kn(A,b) of x0 such that rn = b − Axn is minimized, that is, krnk2 = kb − Axnk2 is minimized over xn ∈ Kn(A,b).
 假设A是可逆M×M矩阵，B是非零向量，单位为厘米。设X0=a−1b，ax=b的唯一解，不难证明X0∈kn（a，b）对于一些n≤m，实际上存在一个极小阶s≤m的唯一Monic多项式p（z），使得p（a）b=0，所以X0∈ks（a，b）。因此，在维数m≤s的krylov空间中寻找ax=b的解是有意义的，其思想是求X0的近似值xn∈kn（a，b），使rn=b−axn最小化，即krnk2=kb−axnk2在xn∈kn（a，b）上最小化。

This minimization problem can be stated as
 这个最小化问题可以表述为

​                                    minimize     krnk2 = kAxn − bk2 ,      xn ∈ Kn(A,b).
 最小化krnk2=kaxn−bk2，xn∈kn（a，b）。

This is a least-squares problem, and we know how to solve it (see Section 21.1). The quantity rn is known as the residual and the method which consists in minimizing krnk2 is known as GMRES, for generalized minimal residuals.
 这是一个最小二乘问题，我们知道如何解决它（见第21.1节）。量Rn被称为残差，对于广义最小残差，包含最小化krnk2的方法被称为gmres。

Now since (u1,...,un) is a basis of Kn(A,b) (since n ≤ s, no breakdown occurs, except for n = s), we may write xn = Uny, so our minimization problem is
 现在，因为（u1，…，un）是kn（a，b）的基础（因为n≤s，除了n=s，没有发生故障），我们可以写xn=uny，所以我们的最小化问题是

​                                                minimize    kAUny − bk2 ,     y ∈ Cn.
 最小化kauny−bk2，y∈cn。

Since by (∗1) of Section 22.4, we have AUn = Un+1Hen, minimizing kAUny − bk2 is equivalent to minimizing kUn+1Heny − bk2 over Cm. Since Un+1Heny and b belong to the column space of Un+1, minimizing kUn+1Heny − bk2 is equivalent to minimizing .
 由于在第22.4节（1）中，我们得出了aun=un+1hen，最小化kauny−bk2等于在cm上最小化kun+1heny−bk2。由于un+1heny和b属于un+1的列空间，因此最小化kun+1heny−bk2等于最小化。

However, by construction,
 但是，通过施工，

,
 ，

so our minimization problem can be stated as
 所以我们的最小化问题可以表述为

​                                             minimize  kHeny − kbk2e1k2,   y ∈ Cn.
 最小化kheny−kbk2e1k2，y∈cn。

The approximate solution of Ax = b is then
 ax=b的近似解是

xn = Uny.
 xn=uny。

Starting with u1 = b/kbk2 and with n = 1, the GMRES method runs n ≤ s Arnoldi iterations to find Un and Hen, and then runs a method to solve the least squares problem
 从u1=b/kbk2，n=1开始，GMRES方法进行n≤s阿诺尔底迭代，找到un和hen，然后运行一种求解最小二乘问题的方法。

​                                             minimize  kHeny − kbk2e1k2,   y ∈ Cn.
 最小化kheny−kbk2e1k2，y∈cn。

### 22.6. THE HERMITIAN CASE; LANCZOS ITERATION  22.6。赫米特案例；兰佐斯迭代

When krnk2 = kHeny−kbk2e1k2 is considered small enough, we stop and the approximate solution of Ax = b is then xn = Uny.
 当krnk2=kheny−kbk2e1k2足够小时，我们停止，ax=b的近似解为xn=uny。

There are ways of improving efficiency of the “naive” version of GMRES that we just presented; see Trefethen and Bau [171] (Lecture 35). We now consider the case where A is a Hermitian (or symmetric) matrix.
 我们刚刚介绍的GMRES“幼稚”版本有一些提高效率的方法；见Trefethen和Bau[171]（第35课）。我们现在考虑的情况是，a是一个厄米特（或对称）矩阵。

## 22.6          The Hermitian Case; Lanczos Iteration  22.6 Hermitian案例；Lanczos迭代

If A is an m×m symmetric or Hermitian matrix, then Arnoldi’s method is simpler and much more efficient. Indeed, in this case, it is easy to see that the upper Hessenberg matrices Hn are also symmetric (Hermitian respectively), and thus tridiagonal. Also, the eigenvalues of
 如果a是m×m对称矩阵或厄米特矩阵，那么阿诺迪方法简单而有效。事实上，在这种情况下，很容易看出上海森堡矩阵hn也是对称的（分别是赫米特矩阵），因此是三对角矩阵。另外，特征值

A and Hn are real. It is convenient to write
 a和hn是真的。写起来很方便

​                                                          α1   β1                              
 α1β1_

​                                                          β1    α2   β2                       
 β1α2β2_

​                                                   Hn =  β2      α3      ...             .
 hn=β2α3…。

​                                                                                                     
                                                         

 ... ... βn−1 βn−1 αn
 ……βn−1βn−1αn

The recurrence (∗2) of Section 22.4 becomes the three-term recurrence
 第22.4节的复发（2）成为三期复发。

​                                                Aun = βn−1un−1 + αnun + βnun+1.                                         (∗6)
 aun=βn−1un−1+αnun+βnun+1。（6）

We also have, so Arnoldi’s algorithm become the following algorithm known as Lanczos’ algorithm (or Lanczos iteration). The inner loop on j from 1 to n has been eliminated and replaced by a single assignment.
 我们也有，所以Arnoldi的算法变成了下面的算法，叫做Lanczos算法（或Lanczos迭代）。J上从1到n的内环已被消除，并被一个单独的赋值所取代。

Given an arbitrary nonzero vector b ∈ Cm, let u1 = b/kbk; for n = 1,2,3,... do
 给定任意非零向量b∈cm，设u1=b/kbk；对于n=1,2,3，…做

z := Aun;
 Z：=aun；

;
 ；

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image031.gif)

if βn = 0 quit un+1 = z/βn
 如果βn=0，退出un+1=z/βn

When βn = 0, we say that we have a breakdown of the Lanczos iteration.
 当βn=0时，我们说我们有兰佐斯迭代的分解。

Versions of Proposition 22.5 and Theorem 22.6 apply to Lanczos iteration.
 命题22.5和定理22.6的版本适用于Lanczos迭代。

Besides being much more efficient than Arnoldi iteration, Lanczos iteration has the advantage that the Rayleigh–Ritz method for finding some of the eigenvalues of A as the eigenvalues of the symmetric (respectively Hermitian) tridiagonal matrix Hn applies, but there are more methods for finding the eigenvalues of symmetric (respectively Hermitian) tridiagonal matrices. Also theorems about error estimates exist. The version of Lanczos iteration given above may run into problems in floating point arithmetic. What happens is that the vectors uj may lose the property of being orthogonal, so it may be necessary to reorthogonalize them. For more on all this, see Demmel [49] (Chapter 7, in particular Section 7.2-7.4). The version of GMRES using Lanczos iteration is called MINRES.
 Lanczos迭代除了比Arnoldi迭代更有效外，还有一个优点，那就是瑞利-瑞兹方法用于寻找a的一些特征值，作为对称（分别是Hermitian）三对角矩阵hn的特征值，但是有更多的方法可以找到t。对称（分别是厄米特矩阵）三对角矩阵的特征值。还存在关于误差估计的定理。上面给出的Lanczos迭代版本可能在浮点运算中遇到问题。结果是，矢量UJ可能失去正交性，因此有必要对其进行重定位。有关更多信息，请参见demmel[49]（第7章，特别是第7.2-7.4节）。使用lanczos迭代的gmres版本称为minres。

We close our brief survey of methods for computing the eigenvalues and the eigenvectors of a matrix with a quick discussion of two methods known as power methods.
 我们结束了对计算矩阵特征值和特征向量的方法的简短调查，并对两种称为幂次法的方法进行了快速讨论。

## 22.7       Power Methods  22.7动力方法

Let A be an m × m complex or real matrix. There are two power methods, both of which yield one eigenvalue and one eigenvector associated with this vector:
 设A为m×m复矩阵或实矩阵。有两种功率方法，都会产生一个特征值和一个与此向量相关的特征向量：

(1)    Power iteration.
 动力迭代。

(2)    Inverse (power) iteration.
 逆（幂）迭代。

Power iteration only works if the matrix A has an eigenvalue λ of largest modulus, which means that if λ1,...,λm are the eigenvalues of A, then
 只有当矩阵A具有最大模的特征值λ时，方可进行幂次迭代，也就是说，如果λ1，…，λm是a的特征值，那么

|λ1| > |λ2| ≥ ··· ≥ |λm| ≥ 0.
 |λ1>λ2≥······≥λm≥0.

In particular, if A is a real matrix, then λ1 must be real (since otherwise there are two complex conjugate eigenvalues of the same largest modulus). If the above condition is satisfied, then power iteration yields λ1 and some eigenvector associated with it. The method is simple enough:
 特别是，如果a是一个实矩阵，那么λ1必须是实矩阵（否则有两个相同最大模的复共轭特征值）。如果满足上述条件，则功率迭代得到λ1及其相关的一些特征向量。方法非常简单：

Pick some initial unit vector x0 and compute the following sequence (xk), where
 选取一些初始单位向量X0并计算以下序列（XK），其中

.
 .

We would expect that (xk) converges to an eigenvector associated with λ1, but this is not quite correct. The following results are proven in Serre [151] (Section 13.5.1). First assume that λ1 = 0.6
 我们期望（xk）收敛到与λ1相关的特征向量，但这并不完全正确。以下结果在SERRE[151]中得到证实（第13.5.1节）。首先假设λ1=0.6

We have
 我们有

.
 .

If A is a complex matrix which has a unique complex eigenvalue λ1 of largest modulus, then
 如果A是一个具有最大模的唯一复特征值λ1的复矩阵，那么

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image033.gif)

### 22.7. POWER METHODS  22.7。功率法

is a unit eigenvector of A associated with λ1. If λ1 is real, then
 是与λ1相关联的a的单位特征向量。如果λ1为真，则

v = lim xk k7→∞
 V=lim xk k7→∞

is a unit eigenvector of A associated with λ1. Actually some condition on x0 is needed: x0 must have a nonzero component in the eigenspace E associated with λ1 (in any direct sum of Cm in which E is a summand).
 是与λ1相关联的a的单位特征向量。实际上，在X0上需要一些条件：X0必须在与λ1相关的特征空间e中有一个非零分量（在任何直接和cm中，e是和）。

The eigenvalue λ1 is found as follows. If λ1 is complex, and if vj = 06 is any nonzero coordinate of v, then
 特征值λ1如下所示。如果λ1是复数，并且vj=06是v的任何非零坐标，那么

.
 .

If λ1 is real, then we can define the sequence (λ(k)) by
 如果λ1是实的，那么我们可以通过以下方式定义序列（λ（k））：

​                                                  λ(k+1) = (xk+1)∗Axk+1,    k ≥ 0,
 λ（k+1）=（xk+1）axk+1，k≥0，

and we have
 我们有

λ1 = lim λ(k). k7→∞
 λ1=limλ（k）。K7→∞

Indeed, in this case, since v = limk7→∞ xk and v is a unit eigenvector for λ1, we have
 实际上，在这种情况下，由于v=limk7→∞xk和v是λ1的单位特征向量，我们得到

lim λ(k) = lim (xk+1)∗Axk+1 = v∗Av = λ1v∗v = λ1. k7→∞   k7→∞
 limλ（k）=lim（xk+1）axk+1=v av=λ1v v=λ1.K7→∞K7→∞

Note that since xk+1 is a unit vector, (xk+1)∗Axk+1 is a Rayleigh ratio.
 注意，由于xk+1是单位向量，（xk+1）axk+1是瑞利比。

If A is a Hermitian matrix, then the eigenvalues are real and we can say more about the rate of convergence, which is not great (only linear). For details, see Trefethen and Bau [171] (Lecture 27).
 如果a是一个厄米矩阵，那么特征值是真实的，我们可以说更多的收敛速度，这不是很大（只有线性）。有关详细信息，请参阅Trefetten和Bau[171]（第27课）。

If λ1 = 0, then there is some power ` < m such that Ax` = 0.
 如果λ1=0，则存在一些功率`<m，使得ax`=0。

The inverse iteration method is designed to find an eigenvector associated with an eigenvalue λ of A for which we know a good approximation µ.
 反迭代法的目的是找到一个特征向量与一个我们知道一个很好的近似值μ的特征值λ相关。

Pick some initial unit vector x0 and compute the following sequences (wk) and (xk), where wk+1 is the solution of the system
 选取一些初始单位向量X0，计算以下序列（wk）和（xk），其中wk+1是系统的解

​                      (A − µI)wk+1 = xk     equivalently    wk+1 = (A − µI)−1xk,      k ≥ 0,
 （a−μi）wk+1=xk等于wk+1=（a−μi）−1xk，k≥0，

and
 和

.
 .

The following result is proven in Ciarlet [41] (Theorem 6.4.1).
 以下结果在Ciarlet[41]中得到证明（定理6.4.1）。

Proposition 22.7. Let A be an m × m diagonalizable (complex or real) matrix with eigenvalues λ1,...,λm, and let λ = λ` be an arbitrary eigenvalue of A (not necessary simple).
 提案22.7.设a为特征值为λ1，…，λm的m×m可对角化（复或实）矩阵，并设λ=λ`为a的任意特征值（不必简单）。

For any µ such that
 对于任何这样的

​                                      µ =6 λ    and      |µ − λ| < |µ − λj|      for all j =6  `,
 μ=6λ和μ−λ<μ−λj对于所有j=6`，

if x0 does not belong to the subspace spanned by the eigenvectors associated with the eigenvalues λj with j =6 `, then
 如果X0不属于特征值λj（j=6`）相关特征向量所跨越的子空间，则

−
 \-

where v is an eigenvector associated with λ. Furthermore, if both λ and µ are real, we have
 其中v是与λ相关的特征向量。此外，如果λ和μ都是真的，我们有

| lim xk = v   k7→∞    网络错误   lim (−1)kxk = v    网络错误 | if µ < λ,    网络错误   if µ >   λ.    网络错误 |
| ----------------------------------------------------------- | ----------------------------------------------- |
|                                                             |                                                 |

k7→∞
 K7→∞

Also, if we define the sequence (λ(k)) by
 另外，如果我们用

λ(k+1) = (xk+1)∗Axk+1,
 λ（k+1）=（xk+1）axk+1，

then
 然后

lim λ(k+1) = λ.
 limλ（k+1）=λ。

k7→∞
 K7→∞

The condition of x0 may seem quite stringent, but in practice, a vector x0 chosen at random usually satisfies it.
 X0的条件可能看起来相当严格，但在实践中，随机选择的向量X0通常满足它。

If A is a Hermitian matrix, then we can say more. In particular, the inverse iteration algorithm can be modified to make use of the newly computed λ(k+1) instead of µ, and an even faster convergence is achieved. Such a method is called the Rayleigh quotient iteration. When it converges (which is for almost all x0), this method eventually achieves cubic convergence, which is remarkable. Essentially, this means that the number of correct digits is tripled at every iteration. For more details, see Trefethen and Bau [171] (Lecture 27) and Demmel [49] (Section 5.3.2).
 如果A是一个厄米矩阵，那么我们可以说更多。特别是，可以修改逆迭代算法，以利用新计算的λ（k+1）而不是μ，从而实现更快的收敛。这种方法叫做瑞利商迭代。当它收敛时（几乎是所有的X0），这种方法最终达到了三次收敛，这是显著的。从本质上来说，这意味着在每次迭代中正确数字的数量是三倍。有关更多详细信息，请参阅Trefetten和Bau[171]（第27讲）和Demmel[49]（第5.3.2节）。

## 22.8      Summary  22.8总结

The main concepts and results of this chapter are listed below:
 本章的主要概念和结果如下：

•     QR iteration, QR algorithm.
 二维码迭代，二维码算法。

•     Upper Hessenberg matrices.
 上海森堡矩阵。

•     Householder matrix.
 户主矩阵。

### 22.9. PROBLEMS  22.9。问题

•     Unreduced and reduced Hessenberg matrices.
 未简化和约化的Hessenberg矩阵。

•     Deflation.
 通货紧缩。

•     Shift.
 换档。

•     Wilkinson shift.
 威尔金森轮班。

•     Double shift.
 双班制。

•     Francis shift.
 弗朗西斯变换。

•     Implicit shifting.
 隐性转变。

•     Implicit Q-theorem.
 隐式Q定理。

•     Arnoldi iteration.
 阿诺迪迭代。

•     Breakdown of Arnoldi iteration.
 阿诺迪迭代的分解。

•     Krylov subspace.
 Krylov子空间。

•     Rayleigh–Ritz method.
 瑞利-里兹法。

•     Ritz values, Arnoldi estimates.
 里兹值，阿诺迪估计。

•     Residual.
 剩余。

•     GMRES
 GMRES

•     Lanczos iteration.
 Lanczos迭代。

•     Power iteration.
 动力迭代。

•     Inverse power iteration.
 逆功率迭代。

•     Rayleigh ratio.
 瑞利比。

## 22.9      Problems  22.9问题

Problem 22.1. Prove Theorem 22.2; see Problem 12.7.
 问题22.1。证明定理22.2；见问题12.7。

Problem 22.2. Prove that if a matrix A is Hermitian (or real symmetric), then any Hessenberg matrix H similar to A is Hermitian tridiagonal (real symmetric tridiagonal).
 问题22.2。证明了如果矩阵A是厄米特矩阵（或实对称），那么任何与A相似的海森堡矩阵H都是厄米特三对角矩阵（实对称三对角）。

Problem 22.3. For any matrix (real or complex) A, if A = QR is a QR-decomposition of A using Householder reflections, prove that if A is upper Hessenberg then so is Q.
 问题22.3。对于任何矩阵（实矩阵或复矩阵）a，如果a=qr是使用户主反射的qr分解，证明如果a是上赫斯伯格，那么q也是。

Problem 22.4. Prove that if A is upper Hessenberg, then the matrices Ak obtained by applying the QR-algorithm are also upper Hessenberg.
 问题22.4.证明如果a是上海森堡，那么应用qr算法得到的矩阵ak也是上海森堡。

Problem 22.5. Prove the implicit Q theorem. This theorem says that if A is reduced to upper Hessenberg form as A = UHU∗ and if H is unreduced (hi+1i = 06 for i = 1,...,n−1), then the columns of index 2,...,n of U are determined by the first column of U up to sign;
 问题22.5。证明隐式Q定理。这个定理表明，如果a被简化为上赫森伯格形式a=u h u，如果h不被简化（i=1，…，n−1时hi+1i=06），那么索引2，…，n的列由u的第一列到符号决定；

Problem 22.6. Read Section 7.5 of Golub and Van Loan [80] and implement their version of the QR-algorithm with shifts.
 问题22.6.阅读Golub和van Loan[80]的第7.5节，并通过移位实现他们的QR算法版本。

Problem 22.7. If an Arnoldi iteration has a breakdown at stage n, that is, hn+1 = 0, then we found the first unreduced block of the Hessenberg matrix H. Prove that the eigenvalues of Hn are eigenvalues of A.
 问题22.7。如果阿诺迪迭代在n阶段有一个分解，即hn+1=0，那么我们就找到了Hessenberg矩阵h的第一个不可约块，证明hn的特征值是a的特征值。

Problem 22.8. Prove Theorem 22.6.
 问题22.8。证明定理22.6。

Problem 22.9. Implement GRMES and test it on some linear systems.
 问题22.9.实现GRMES并在一些线性系统上进行测试。

Problem 22.10. State and prove versions of Proposition 22.5 and Theorem 22.6 for the Lanczos iteration.
 问题22.10。陈述并证明关于Lanczos迭代的22.5号命题和22.6号定理的版本。

Problem 22.11. Prove the results about the power iteration method stated in Section 22.7.
 问题22.11。证明第22.7节所述的功率迭代法的结果。

Problem 22.12. Prove the results about the inverse power iteration method stated in Section 22.7.
 问题22.12。证明第22.7节所述逆功率迭代法的结果。

Problem 22.13. Implement and test the power iteration method and the inverse power iteration method.
 问题22.13。实现并测试了功率迭代法和逆功率迭代法。

Problem 22.14. Read Lecture 27 in Trefethen and Bau [171] and implement and test the Rayleigh quotient iteration method.
 问题22.14。阅读Trefethen和Bau[171]中的第27讲，实现并测试瑞利商迭代法。


 