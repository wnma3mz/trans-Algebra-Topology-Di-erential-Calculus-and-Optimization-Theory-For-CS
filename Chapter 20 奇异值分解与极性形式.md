第二十章

# Singular Value Decomposition and Polar Form  奇异值分解与极性形式

## 20.1        Properties of f∗ ◦f  20.1 f f的性质

In this section we assume that we are dealing with real Euclidean spaces. Let f : E → E be any linear map. In general, it may not be possible to diagonalize f. We show that every linear map can be diagonalized if we are willing to use two orthonormal bases. This is the celebrated singular value decomposition (SVD). A close cousin of the SVD is the polar form of a linear map, which shows how a linear map can be decomposed into its purely rotational component (perhaps with a flip) and its purely stretching part.
 在本节中，我们假设我们处理的是真正的欧几里得空间。设f:e→e为任意线性映射。一般来说，F不可能对角化。我们证明了如果我们愿意使用两个正交基，每个线性映射都可以对角化。这是著名的奇异值分解（SVD）。SVD的近亲是线性映射的极性形式，它显示了如何将线性映射分解为其纯旋转组件（可能带有翻转）和纯拉伸部分。

The key observation is that f∗ ◦ f is self-adjoint since
 关键的观察是f f自

h(f∗ ◦ f)(u),vi = hf(u),f(v)i = hu,(f∗ ◦ f)(v)i.
 h（f f）（u），v i=hf（u），f（v）i=hu，（f f）（v）i.

Similarly, f ◦ f∗ is self-adjoint.
 同样，f f是自伴的。

The fact that f∗ ◦ f and f ◦ f∗ are self-adjoint is very important, because by Theorem
 F F和F F是自伴的事实非常重要，因为根据定理

16.8In fact, these, it implies thateigenvalues are all nonnegativef∗ ◦f and f ◦f∗ can be diagonalized and that they have real eigenvalues.as shown in the following proposition.
 16.8事实上，这意味着特征值都是非负的f f和f f可以对角化，并且它们具有真正的特征值。如以下命题所示。

Proposition 20.1. The eigenvalues of f∗ ◦ f and f ◦ f∗ are nonnegative. Proof. If u is an eigenvector of f∗ ◦ f for the eigenvalue λ, then
 提案20.1.f f和f f的特征值为非负。证据。如果u是特征值λ的f f的特征向量，那么

h(f∗ ◦ f)(u),ui = hf(u),f(u)i
 h（f_f）（u），u i=hf（u），f（u）i

and h(f∗ ◦ f)(u),ui = λhu,ui,
 h（f_f）（u），ui=λhu，ui，

and thus λhu,ui = hf(u),f(u)i,
 因此，λhu，u i=hf（u），f（u）i，

which implies that λ ≥ 0, since h−,−i is positive definite. A similar proof applies to f ◦ f∗.      
 这意味着λ≥0，因为h−，−i是正定的。类似的证据也适用于F F。

613
 六百一十三

Thus, the eigenvalues of f∗ ◦f are of the formor 0, where σi > 0, and similarly for f ◦ f∗.
 因此，f f的特征值的形式为0，其中，σi>0，与f f类似。

The above considerations also apply to any linear map f : E → F between two Euclidean spaces (E,h−,−i1) and (F,h−,−i2). Recall that the adjoint f∗ : F → E of f is the unique linear map f∗ such that
 上述考虑也适用于两个欧几里得空间（e，h−、−i1）和（f，h−、−i2）之间的任何线性映射f:e→f。回想一下，f的伴随f：f→e是唯一的线性映射f，这样

​                                  hf(u),vi2 = hu,f∗(v)i1,         for all u ∈ E and all v ∈ F.
 hf（u），vi2=hu，f（v）i1，对于所有u∈e和所有v∈f。

Then f∗ ◦ f and f ◦ f∗ are self-adjoint (the proof is the same as in the previous case), and the eigenvalues of f∗ ◦ f and f ◦ f∗ are nonnegative.
 则f f和f f为自伴（证明与前一种情况相同），f f和f f的特征值为非负。

Proof. If λ is an eigenvalue of f∗ ◦ f and u (6= 0) is a corresponding eigenvector, we have
 证据。如果λ是f f的特征值，而u（6=0）是对应的特征向量，我们得到

h(f∗ ◦ f)(u),ui1 = hf(u),f(u)i2,
 h（f_f）（u），ui1=hf（u），f（u）i2，

and also h(f∗ ◦ f)(u),ui1 = λhu,ui1,
 以及h（f_f）（u），ui1=λhu，ui1，

so
 所以

λhu,ui1,= hf(u),f(u)i2,
 λhu，ui1，=hf（u），f（u）i2，

which implies that λ ≥ 0. A similar proof applies to f ◦ f∗.                                                            
 这意味着λ≥0。类似的证据也适用于F F。

The situation is even better, since we will show shortly that f∗ ◦ f and f ◦ f∗ have the same nonzero eigenvalues.
 这种情况甚至更好，因为我们很快就会发现f f和f f具有相同的非零特征值。

Remark: Given any two linear maps f : E → F and g: F → E, where dim(E) = n and dim(F) = m, it can be shown that
 注：任意两个线性映射f:e→f和g:f→e，其中dim（e）=n和dim（f）=m

λm det(λIn − g ◦ f) = λn det(λIm − f ◦ g),
 λm det（λin−g f）=λn det（λim−f g），

and thus g ◦ f and f ◦ g always have the same nonzero eigenvalues; see Problem 14.14.
 因此，g f和f g总是具有相同的非零特征值；参见问题14.14。

eigenvalues ofDefinition 20.1.f∗ ◦Given any linear mapf (and f ◦ f∗) are called thef : E →singular values ofF, the square rootsf. σi > 0 of the positive
 定义的特征值20.1.f给定任何线性mapf（和f f）被取消：e→奇异值关闭，平方根sf。σi>0为正

Definition 20.2. A self-adjoint linear map f : E →is also invertible,E whose eigenvalues are nonnegative isf is said to be positive called positive semidefinite (or positive), and if f definite. In the latter case, every eigenvalue of f is strictly positive.
 定义20.2.自伴线性映射f:e→也是可逆的，其特征值为非负的e称为正半定（或正），如果f定。在后一种情况下，f的每个特征值都是严格正的。

If f : E → F is any linear map, we just showed that f∗ ◦ f and f ◦ f∗ are positive semidefinite self-adjoint linear maps. This fact has the remarkable consequence that every linear map has two important decompositions:
 如果f:e→f是任意线性映射，我们只证明f f和f f是半正定自伴线性映射。这一事实的显著结果是，每个线性映射都有两个重要的分解：

\1. The polar form.
 1。极地形态。


 

### 20.1. PROPERTIES OF f∗ ◦ f  20.1。f f的性质

\2. The singular value decomposition (SVD).
 2。奇异值分解（SVD）。

The wonderful thing about the singular value decomposition is that there exist two orthonormal bases (u1,...,un) and (v1,...,vm) such that, with respect to these bases, f is a diagonal matrix consisting of the singular values of f or 0. Thus, in some sense, f can always be diagonalized with respect to two orthonormal bases. The SVD is also a useful tool for solving overdetermined linear systems in the least squares sense and for data analysis, as we show later on.
 奇异值分解的美妙之处在于，存在两个正交基（u1，…，un）和（v1，…，vm），因此，对于这些基，f是由奇异值f或0组成的对角矩阵。因此，在某种意义上，F总是可以相对于两个正交基对角化。SVD也是解决最小二乘意义上的超定线性系统和数据分析的一个有用工具，如我们稍后所示。

First we show some useful relationships between the kernels and the images of f, f∗, f∗ ◦ f, and f ◦ f∗. Recall that if f : E → F is a linear map, the image Imf of f is the subspace f(E) of F, and the rank of f is the dimension dim(Imf) of its image. Also recall that (Theorem 5.11) dim(Kerf) + dim(Imf) = dim(E),
 首先，我们展示了内核与f、f_、f_和f_f_图像之间的一些有用关系。回想一下，如果f:e→f是一个线性映射，f的图像imf是f的子空间f（e），f的秩是其图像的维数dim（imf）。还记得（定理5.11）dim（切口）+dim（imf）=dim（e），

and that (Propositions 11.11 and 13.13) for every subspace W of E,
 对于e的每个子空间w（命题11.11和13.13），则

dim(W) + dim(W ⊥) = dim(E).
 dim（w）+dim（w）=dim（e）。

Proposition 20.2. Given any two Euclidean spaces E and F, where E has dimension n and F has dimension m, for any linear map f : E → F, we have
 提案20.2.给定任意两个欧几里得空间e和f，其中e有维数n，f有维数m，对于任何线性映射f:e→f，我们有

Kerf = Ker(f∗ ◦ f),
 切口=KER（F F）

Kerf∗ = Ker(f ◦ f∗),
 切口=KER（F F）

Kerf = (Imf∗)⊥,
 切口=（imf），

Kerf∗ = (Imf)⊥, dim(Imf) = dim(Imf∗),
 kerf=（imf），dim（imf）=dim（imf），

and f, f∗, f∗ ◦ f, and f ◦ f∗ have the same rank.
 F、F、F F和F F具有相同的等级。

Proof. To simplify the notation, we will denote the inner products on E and F by the same symbol h−,−i (to avoid subscripts). If f(u) = 0, then (f∗ ◦ f)(u) = f∗(f(u)) = f∗(0) = 0, and so Kerf ⊆ Ker(f∗ ◦ f). By definition of f∗, we have
 证据。为了简化表示法，我们将用相同的符号H−、−I（避免下标）来表示e和f上的内积。如果f（u）=0，那么（f（f）（u）=f（f（u））=f（0）=0，那么切口ker（f f）。根据F的定义，我们有

hf(u),f(u)i = h(f∗ ◦ f)(u),ui
 h f（u），f（u）i=h（f f）（u），用户界面

for all u ∈ E. If (f∗ ◦ f)(u) = 0, since h−,−i is positive definite, we must have f(u) = 0, and so Ker(f∗ ◦ f) ⊆ Kerf. Therefore,
 对于所有的u∈e，如果（f f）（u）=0，因为h−−i是正定的，我们必须有f（u）=0，所以ker（f f）kerf。因此，

Kerf = Ker(f∗ ◦ f).
 切口=KER（F F）。

The proof that Kerf∗ = Ker(f ◦ f∗) is similar.
 切口=KER（F F）的证据相似。

By definition of f∗, we have
 根据F的定义，我们有

​                                     hf(u),vi = hu,f∗(v)i         for all u ∈ E and all v ∈ F.                                 (∗)
 hf（u），v i=hu，f（v）i表示所有u e和所有v f.（）

This immediately implies that
 这立刻意味着

​                                            Kerf = (Imf∗)⊥      and      Kerf∗ = (Imf)⊥.
 切口=（imf）和切口=（imf）。

Let us explain why Kerf = (Imf∗)⊥, the proof of the other equation being similar. Because the inner product is positive definite, for every u ∈ E, we have
 让我们解释一下为什么kerf=（imf），这是另一个等式相似的证明。因为内积是正定的，对于每一个u∈e，我们有

•     u ∈ Kerf
 u∈切口

•     iff f(u) = 0
 iff f（u）=0

•     iff hf(u),vi = 0 for all v, • by (∗) iff hu,f∗(v)i = 0 for all v,
 i f f hf（u），v i=0代表所有v，•by（）iff hu，f（v）i=0代表所有v，

•     iff u ∈ (Imf∗)⊥.
 iff u∈（imf）。

Since
 自从

dim(Imf) = n − dim(Kerf)
 dim（imf）=n−dim（切口）

and dim(Imf∗) = n − dim((Imf∗)⊥),
 和dim（imf）=n（imf），

from
 从

Kerf = (Imf∗)⊥
 切口=（imf）

we also have dim(Kerf) = dim((Imf∗)⊥),
 我们还有dim（kerf）=dim（imf），

from which we obtain
 我们从中获得

dim(Imf) = dim(Imf∗).
 dim（imf）=dim（imf）。

Since dim(Ker(f∗ ◦ f)) + dim(Im(f∗ ◦ f)) = dim(E),
 因为dim（ker（f f））+dim（im（f f））=dim（e），

Ker(f∗ ◦ f) = Kerf and Kerf = (Imf∗)⊥, we get
 ker（f f）=kerf和kerf=（imf），我们得到

dim((Imf∗)⊥) + dim(Im(f∗ ◦ f)) = dim(E).
 dim（（im f））+dim（im（f f））=dim（e）。

Since dim((Imf∗)⊥) + dim(Imf∗) = dim(E),
 因为dim（（imf））+dim（imf）=dim（e），

we deduce that dim(Imf∗) = dim(Im(f∗ ◦ f)).
 我们推导出dim（im f）=dim（im（f f））。

A similar proof shows that
 类似的证据表明

dim(Imf) = dim(Im(f ◦ f∗)).
 dim（im f）=dim（im（f_f）。

Consequently, f, f∗, f∗ ◦ f, and f ◦ f∗ have the same rank.                                                             
 因此，F、F、F F和F F具有相同的等级。

20.2. SINGULAR VALUE DECOMPOSITION FOR SQUARE MATRICES
 20.2。方阵的奇异值分解

## 20.2     Singular Value Decomposition for Square Matrices  20.2平方矩阵的奇异值分解

We will now prove that every square matrix has an SVD. Stronger results can be obtained if we first consider the polar form and then derive the SVD from it (there are uniqueness properties of the polar decomposition). For our purposes, uniqueness results are not as important so we content ourselves with existence results, whose proofs are simpler. Readers interested in a more general treatment are referred to Gallier [73].
 现在我们将证明每个平方矩阵都有一个SVD。如果我们先考虑极性形式，然后从中导出SVD（极性分解具有唯一性），则可以得到更强有力的结果。就我们的目的而言，唯一性结果并没有那么重要，所以我们满足于存在结果，其证明更简单。读者对更普遍的治疗感兴趣，请参考加利尔[73]。

The early history of the singular value decomposition is described in a fascinating paper by Stewart [160]. The SVD is due to Beltrami and Camille Jordan independently (1873, 1874). Gauss is the grandfather of all this, for his work on least squares (1809, 1823) (but Legendre also published a paper on least squares!). Then come Sylvester, Schmidt, and Hermann Weyl. Sylvester’s work was apparently “opaque.” He gave a computational method to find an SVD. Schmidt’s work really has to do with integral equations and symmetric and asymmetric kernels (1907). Weyl’s work has to do with perturbation theory (1912). Autonne came up with the polar decomposition (1902, 1915). Eckart and Young extended SVD to rectangular matrices (1936, 1939).
 史都华[160]在一篇引人入胜的论文中描述了奇异值分解的早期历史。SVD独立于贝尔特拉米和卡米尔·乔丹（18731874）。高斯是所有这些的祖父，因为他在最小二乘（18091823）上的工作（但勒让德也发表了一篇关于最小二乘的论文！）然后是西尔维斯特、施密特和赫尔曼·韦尔。西尔维斯特的工作显然是“不透明的”，他给出了一种计算方法来寻找SVD。施密特的工作实际上与积分方程和对称和不对称内核有关（1907年）。韦尔的工作与微扰理论（1912）有关。Autonne提出了极地分解（19021915）。Eckart和Young将SVD扩展到了矩形矩阵（1936、1939）。

Theorem 20.3. (Singular value decomposition) For every real n×n matrix A there are two orthogonal matrices U and V and a diagonal matrix D such that A = V DU>, where D is of
 定理20.3。（奇异值分解）对于每个实n×n矩阵a，有两个正交矩阵u和v和一个对角矩阵d，其中a=v du>，其中d是

| the form    网络错误                                         |                                  |                                             |                                                              |
| ------------------------------------------------------------ | -------------------------------- | ------------------------------------------- | ------------------------------------------------------------ |
|     网络错误   σ1    网络错误       网络错误   D =  ...    网络错误       网络错误       网络错误 | σ2    网络错误   ...    网络错误 | ...    网络错误   ... ...   ...    网络错误 |     网络错误       网络错误   ...   ,    网络错误   σn    网络错误 |

where σ1,...,σr are the singular values of f, i.e., the (positive) square roots of the nonzero eigenvalues of A>A and AA>, and σr+1 = ··· = σn = 0. The columns of U are eigenvectors of A>A, and the columns of V are eigenvectors of AA>.
 式中，σ1，…，σr是f的奇异值，即a>a和aa>的非零特征值的（正）平方根，以及σr+1=·····=σn=0。u列是a>a的特征向量，v列是aa>的特征向量。

Proof. Since A>A is a symmetric matrix, in fact, a positive semidefinite matrix, there exists an orthogonal matrix U such that
 证据。由于a>a是对称矩阵，实际上是半正定矩阵，因此存在一个正交矩阵u，使得

A>A = UD2U>,
 a>a=ud2u>，

with D = diag(σ1,...,σr,0,...,0), where are the nonzero eigenvalues of A>A, and where r is the rank of A; that is, σ1,...,σr are the singular values of A. It follows that
 d=diag（σ1，…，σr，0，…，0），其中a>a的非零特征值，其中r是a的秩；即，σ1，…，σr是a的奇异值，其结果如下：

U>A>AU = (AU)>AU = D2,
 u>a>au=（au）>au=d2，

and if we let fj be the jth column of AU for j = 1,...,n, then we have
 如果我们让fj是j=1，…，n的au的jth列，那么我们有

​                                                      hfi,fji = σi2δij,        1 ≤ i,j ≤ r
 hfi，fji=σi2δi j，1≤i，j≤r

and
 和

​                                                           fj = 0,        r + 1 ≤ j ≤ n.
 fj=0，r+1≤j≤n。

If we define (v1,...,vr) by
 如果我们定义（v1，…，vr）

​                                                          vj = σj−1fj,       1 ≤ j ≤ r,
 Vj=σj−1fj，1≤j≤r，

then we have
 然后我们有了

​                                                        hvi,vji = δij,         1 ≤ i,j ≤ r,
 hvi，vji=δi j，1≤i，j≤r，

so complete (v1,...,vr) into an orthonormal basis (v1,...,vr,vr+1,...,vn) (for example, using Gram–Schmidt). Now since fj = σjvj for j = 1...,r, we have
 因此，将（v1，…，vr）完全转换为正态基（v1，…，vr，vr+1，…，vn）（例如，使用gram-schmidt）。既然fj=σjvj，对于j=1…，r，我们有

​                                      hvi,fji = σjhvi,vji = σjδi,j,           1 ≤ i ≤ n, 1 ≤ j ≤ r
 hvi，fji=σj hvi，vji=σjδi，j，1≤i≤n，1≤j≤r

and since fj = 0 for j = r + 1,...,n,
 既然j=r+1时fj=0，…，n，

​                                               hvi,fji = 0          1 ≤ i ≤ n, r + 1 ≤ j ≤ n.
 hvi，fji=0 1≤i≤n，r+1≤j≤n。

If V is the matrix whose columns are v1,...,vn, then V is orthogonal and the above equations prove that
 如果v是列为v1，…，vn的矩阵，则v是正交的，上述方程证明

V >AU = D,
 v>au=d，

which yields A = V DU>, as required.
 根据需要，得出a=v du>。

The equation A = V DU> implies that
 方程式a=v du>意味着

​                                                  A>A = UD2U>,        AA> = V D2V >,
 a>a=ud2u>，aa>=v d2v>，

which shows that A>A and AA> have the same eigenvalues, that the columns of U are eigenvectors of A>A, and that the columns of V are eigenvectors of AA>. 
 这表明A>A和AA>具有相同的特征值，U列是A>A的特征向量，V列是AA>的特征向量。

Example 20.1. Here is a simple example of how to use the proof of Theorem 20.3 to obtain an SVD decomposition. Let . Then , and
 例20.1。下面是一个简单的例子，说明如何使用定理20.3的证明来获得SVD分解。让。然后，和

. A simple calculation shows that the eigenvalues of A>A are 2 and 0, and
 . 简单计算表明，a>a的特征值为2和0，以及

for the eigenvalue 2, a unit eigenvector is , while a unit eigenvector for the eigenvalue
 对于特征值2，单位特征向量为，而单位特征向量为

. Observe that the singular values are σ1 = √2 and σ2 = 0. Furthermore,
 . 观察奇异值为σ1=√2和σ2=0。此外，

. To determine V , the proof of Theorem 20.3 tells us to first
 . 为了确定v，定理20.3的证明告诉我们首先

calculate
 计算

and then set
 然后设置

.
 .

### 20.2. SINGULAR VALUE DECOMPOSITION FOR SQUARE MATRICES  20.2。方阵的奇异值分解

Once v1 is determined, since σ2 = 0, we have the freedom to choose v2 such that (v1,v2) forms an orthonormal basis for R2. Naturally, we chose  and set. Of course we could have found V by directly computing the eigenvalues and eigenvectors for AA>. We leave it to the reader to check that
 一旦确定了v1，因为σ2=0，我们就可以自由地选择v2，这样（v1，v2）就形成了r2的正交基。当然，我们选择和设置。当然，我们可以通过直接计算aa>的特征值和特征向量找到v。我们把它留给读者检查一下

.
 .

Theorem 20.3 suggests the following definition.
 定理20.3给出了以下定义。

Definition 20.3. A triple (U,D,V ) such that A = V D U>, where U and V are orthogonal and D is a diagonal matrix whose entries are nonnegative (it is positive semidefinite) is called a singular value decomposition (SVD) of A.
 定义20.3.一种三重矩阵（u，d，v），其中a=v d u>，其中u和v是正交的，d是一个项为非负（正半定）的对角矩阵，称为a的奇异值分解（svd）。

The Matlab command for computing an SVD A = V DU> of a matrix A is [V, D, U] = svd(A).
 用于计算矩阵A的svd a=v d u>的matlab命令是[v，d，u]=svd（a）。

The proof of Theorem 20.3 shows that there are two orthonormal bases (u1,...,un) and (v1,...,vn), where (u1,...,un) are eigenvectors of A>A and (v1,...,vn) are eigenvectors of AA>. Furthermore, (u1,...,ur) is an orthonormal basis of ImA>, (ur+1,...,un) is an orthonormal basis of KerA, (v1,...,vr) is an orthonormal basis of ImA, and (vr+1,...,vn) is an orthonormal basis of KerA>.
 定理20.3的证明表明，有两个正交基（u1，…，un）和（v1，…，vn），其中（u1，…，un）是a>a的特征向量，（v1，…，vn）是aa>的特征向量。此外，（u1，…，ur）是ima>的正态基础，（ur+1，…，un）是kera的正态基础，（v1，…，vr）是ima的正态基础，（vr+1，…，vn）是kera>的正态基础。

Using a remark made in Chapter 4, if we denote the columns of U by u1,...,un and the columns of V by v1,...,vn, then we can write
 用第四章的注释，如果我们用u1，…，un表示u的列，用v1，…，vn表示v的列，那么我们可以写

.
 .

As a consequence, if r is a lot smaller than n (we write ), we see that A can be reconstructed from U and V using a much smaller number of elements. This idea will be used to provide “low-rank” approximations of a matrix. The idea is to keep only the k top singular values for some suitable for which σk+1,...σr are very small.
 因此，如果r比n小很多（我们写的），我们可以看到a可以用更少的元素从u和v重建。这个想法将被用来提供矩阵的“低阶”近似值。我们的想法是，对于一些σk+1，…σr非常小的情况，只保留k的顶部奇异值。

Remarks:
 评论：

(1)    In Strang [165] the matrices U,V,D are denoted by U = Q2, V = Q1, and D = Σ, and an SVD is written as. This has the advantage that Q1 comes before Q2 in
 在Strang[165]中，矩阵u、v、d用u=q2、v=q1和d=∑表示，SVD写为。这具有q1在q2之前的优势。

. This has the disadvantage that A maps the columns of Q2 (eigenvectors
 . 这有一个缺点，即A映射了q2列（特征向量

of A>A) to multiples of the columns of Q1 (eigenvectors of AA>).
 a>a）到q1列的倍数（aa>的特征向量）。

(2)    Algorithms for actually computing the SVD of a matrix are presented in Golub and Van Loan [80], Demmel [49], and Trefethen and Bau [171], where the SVD and its applications are also discussed quite extensively.
 实际计算矩阵SVD的算法在Golub和van Loan[80]、Demmel[49]和Trefethen和Bau[171]中给出，其中，SVD及其应用也得到了广泛讨论。

(3)    If A is a symmetric matrix, then in general, there is no SVD V ΣU> of A with V = U. However, if A is positive semidefinite, then the eigenvalues of A are nonnegative, and so the nonzero eigenvalues of A are equal to the singular values of A and SVDs of A are of the form
 如果A是一个对称矩阵，那么一般来说，在V=U的情况下，A的SVD V∑U>是不存在的，但是，如果A是半正定的，那么A的特征值是非负的，因此A的非零特征值等于A的奇异值，A的SVD的形式是

*A*    = V ΣV >.
 =V∑V>。

(4)    The SVD also applies to complex matrices. In this case, for every complex n×n matrix
 SVD也适用于复杂矩阵。在这种情况下，对于每个复杂的n×n矩阵

A, there are two unitary matrices U and V and a diagonal matrix D such that
 有两个单位矩阵u和v和一个对角矩阵d，这样

*A*    = V D U∗,
 =v d u，

where D is a diagonal matrix consisting of real entries σ1,...,σn, where σ1,...,σr are the singular values of A, i.e., the positive square roots of the nonzero eigenvalues of A∗A and AA∗, and σr+1 = ... = σn = 0.
 式中，d是由实数项σ1，…，σn组成的对角矩阵，其中，σ1，…，σr是a的奇异值，即a a和aa的非零特征值的正平方根，以及σr+1=。=σn=0。

## 20.3         Polar Form for Square Matrices  20.3方阵的极性形式

A notion closely related to the SVD is the polar form of a matrix.
 与SVD密切相关的概念是矩阵的极性形式。

Definition 20.4. A pair (R,S) such that A = RS with R orthogonal and S symmetric positive semidefinite is called a polar decomposition of A.
 定义20.4.具有r正交和s对称半正定的a=rs的对（r，s）称为a的极分解。

Theorem 20.3 implies that for every real n×n matrix A, there is some orthogonal matrix
 定理20.3表明，对于每个实n×n矩阵a，都有一些正交矩阵

R and some positive semidefinite symmetric matrix S such that
 r和一些半正定对称矩阵s，这样

A = RS.
 A=卢比。

This is easy to show and we will prove it below. Furthermore, R,S are unique if A is invertible, but this is harder to prove; see Problem 20.9.
 这很容易展示，我们将在下面证明。此外，如果a是可逆的，r，s是唯一的，但这很难证明；见问题20.9。

For example, the matrix
 例如，矩阵

​                                                                            −      −
 −−

is both orthogonal and symmetric, and A = RS with R = A and S = I, which implies that some of the eigenvalues of A are negative.
 是正交和对称的，A=r s，R=a和S=i，这意味着A的一些特征值是负的。

Remark: In the complex case, the polar decomposition states that for every complex n×n matrix A, there is some unitary matrix U and some positive semidefinite Hermitian matrix H such that
 注：在复杂情况下，极分解表明，对于每一个复杂的n×n矩阵a，都有一些幺正矩阵u和一些半正定厄米特矩阵h，这样

A = UH.
 A=呃。

### 20.3. POLAR FORM FOR SQUARE MATRICES  20.3。方阵的极性形式

It is easy to go from the polar form to the SVD, and conversely.
 从极性形式到SVD很容易，反之亦然。

Given an SVD decomposition A = V D U>, let R = V U> and S = UD U>. It is clear that R is orthogonal and that S is positive semidefinite symmetric, and
 给定SVD分解a=v d u>，设r=v u>和s=ud u>。很明显，r是正交的，s是半正定对称的，并且

RS = V U>UD U> = V D U> = A.
 rs=v u>u d u>=v d u>=a。

Example 20.2. Recall from Example 20.1 that A = V DU> where V = I2 and
 例20.2。从示例20.1中回忆，a=v du>其中v=i2和

 .
 .

Set R = V U> = U and
 设置r=v u>=u和

 .
 .

Since  has eigenvalues √2 and 0. We leave it to the reader to check that A = RS.
 因为有特征值√2和0。我们把它留给读者来检查a=rs。

Going the other way, given a polar decomposition A = R1S, where R1 is orthogonal and S is positive semidefinite symmetric, there is an orthogonal matrix R2 and a positive semidefinite diagonal matrix D such that, and thus
 另一方面，给定极分解a=r1 s，其中r1是正交的，s是半正定对称的，有一个正交矩阵r2和一个半正定对角矩阵d，因此

,
 ，

where V = R1R2 and U = R2 are orthogonal.
 其中v=R1r2和u=r2是正交的。

Example 20.3. Let and A = R1S, where and S =
 例20.3。Let和a=R1s，其中和s=

. This is the polar decomposition of Example 20.2. Observe that
 . 这是实施例20.2的极性分解。注意

.
 .

Set U = R2 and  to obtain the SVD decomposition of Example 20.1.
 设置u=r2并获得实施例20.1的SVD分解。

The eigenvalues and the singular values of a matrix are typically not related in any obvious way. For example, the n × n matrix
 矩阵的特征值和奇异值通常没有任何明显的联系。例如，n×n矩阵

|     网络错误   1    网络错误   0    网络错误       网络错误   0 A = ...    网络错误       网络错误       网络错误   0    网络错误       网络错误   0    网络错误       网络错误   0    网络错误 | 2    网络错误   1    网络错误   0    网络错误   ...    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   2    网络错误   1    网络错误   ...    网络错误   ...    网络错误   ...    网络错误   ...    网络错误 | 0    网络错误   0    网络错误   2    网络错误   ...    网络错误   0    网络错误   0    网络错误   0    网络错误 | ...    网络错误   ...    网络错误   ... ...    网络错误   1    网络错误   0    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   ...    网络错误   2    网络错误   1    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   ...    网络错误   0    网络错误   2 1    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |

has the eigenvalue 1 with multiplicity n, but its singular values, σ1 ≥ ··· ≥ σn, which are the positive square roots of the eigenvalues of the matrix B = A>A with
 具有多重性n的特征值1，但其奇异值，σ1≥········································

| have a   wide spread, since    网络错误 |     网络错误   1    网络错误   2    网络错误       网络错误   0 B = ...    网络错误       网络错误       网络错误   0    网络错误       网络错误   0    网络错误       网络错误   0    网络错误 | 2    网络错误   5    网络错误   2    网络错误   ...    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   2    网络错误   5    网络错误   ...    网络错误   ...    网络错误   ...    网络错误   ...    网络错误 | 0    网络错误   0    网络错误   2    网络错误   ...    网络错误   2    网络错误   0    网络错误   0    网络错误 | ...    网络错误   ...    网络错误   ... ...    网络错误   5    网络错误   2    网络错误   0    网络错误 | 0    网络错误   0    网络错误   0    网络错误   ...    网络错误   2    网络错误   5    网络错误   2    网络错误 | 0    网络错误   0    网络错误   0    网络错误   ...    网络错误   0    网络错误   2 5    网络错误 |
| --------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                         |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |

= cond2(A) ≥ 2n−1.
 =cond2（a）≥2n−1。

If A is a complex n × n matrix, the eigenvalues λ1,...,λn and the singular values σ1 ≥ σ2 ≥ ··· ≥ σn of A are not unrelated, since
 如果a是一个复n×n矩阵，a的特征值λ1，…，λn和奇异值σ1≥σ2≥·································

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

and
 和

|λ1|···|λn| = |det(A)|,
 |λ1···λn=Det（a），

so we have
 所以我们有

|λ1|···|λn| = σ1 ···σn.
 |λ1···λn=σ1····σn.

More generally, Hermann Weyl proved the following remarkable theorem:
 一般来说，赫尔曼·韦尔证明了以下显著定理：

Theorem 20.4. (Weyl’s inequalities, 1949) For any complex n×n matrix, A, if λ1,...,λn ∈ C are the eigenvalues of A and σ1,...,σn ∈ R+ are the singular values of A, listed so that
 定理20.4.（Weyl's不等式，1949）对于任何复杂的n×n矩阵，a，如果λ1，…，λn∈c是a的特征值和σ1，…，σn∈r+是a的奇异值，列出如下：

|λ1| ≥ ··· ≥ |λn| and σ1 ≥ ··· ≥ σn ≥ 0, then
 |λ1≥······≥λn和σ1≥········≥σn≥0，则

​                                        |λ1|···|λn| = σ1 ···σn      and
 |λ1···λn=σ1·····σn和

​                                        |λ1|···|λk| ≤ σ1 ···σk,      for       k = 1,...,n − 1.
 |λ1···λk≤σ1······σk，对于k=1，…，n−1。

A proof of Theorem 20.4 can be found in Horn and Johnson [93], Chapter 3, Section 3.3, where more inequalities relating the eigenvalues and the singular values of a matrix are given.
 定理20.4的证明可在Horn和Johnson[93]第3章第3.3节中找到，其中给出了更多关于矩阵特征值和奇异值的不等式。

Theorem 20.3 can be easily extended to rectangular m × n matrices, as we show in the next section. For various versions of the SVD for rectangular matrices, see Strang [165] Golub and Van Loan [80], Demmel [49], and Trefethen and Bau [171].
 定理20.3可以很容易地扩展到矩形m×n矩阵，如我们在下一节所示。有关矩形矩阵的SVD的各种版本，请参见Strang[165]Golub和van Loan[80]、Demmel[49]和Trefethen和Bau[171]。

20.4. SINGULAR VALUE DECOMPOSITION FOR RECTANGULAR MATRICES
 20.4。矩形矩阵的奇异值分解

## 20.4     Singular Value Decomposition for Rectangular Matrices  20.4矩形矩阵的奇异值分解

Here is the generalization of Theorem 20.3 to rectangular matrices.
 这是定理20.3对矩形矩阵的推广。

| two orthogonal matrices U (n×n) and   V (m×m) and a diagonal m×n matrix D such that    网络错误 |                                  |                                             |                                  |                                                              |                                                        |
| ------------------------------------------------------------ | -------------------------------- | ------------------------------------------- | -------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------ |
| A =   V D U>, where D is of the form    网络错误             |                                  |                                             |                                  |                                                              |                                                        |
| σ1                ...     网络错误                                       σ2            ...     网络错误                                   ...    ...     ...    ...                 σ1    网络错误       网络错误                                                                                  网络错误                              D =  .           ...       σn   or D =  ...    网络错误                                   0    ..      ...     0                    网络错误                                                                 网络错误                                    ...     ...     ...     ...     网络错误       网络错误                                     0     ...     ...      0     网络错误 | σ2    网络错误   ...    网络错误 | ...    网络错误   ...   ... ...    网络错误 | ...    网络错误   σm    网络错误 | 0         ...    网络错误   0         ...    网络错误   .    网络错误   0     ..    网络错误   0         ...    网络错误 | 0    网络错误   0 ,    网络错误   0 0    网络错误 |

Theorem 20.5. (Singular value decomposition) For every real m × n matrix A, there are
 定理20.5。（奇异值分解）对于每个实M×N矩阵A，有

where σ1,...,σr are the singular values of f, i.e. the (positive) square roots of the nonzero eigenvalues of A>A and AA>, and σr+1 = ... = σp = 0, where p = min(m,n). The columns of U are eigenvectors of A>A, and the columns of V are eigenvectors of AA>.
 其中，σ1，…，σr是f的奇异值，即a>a和aa>的非零特征值的（正）平方根，以及σr+1=。=σp=0，其中p=min（m，n）。u列是a>a的特征向量，v列是aa>的特征向量。

Proof. As in the proof of Theorem 20.3, since A>A is symmetric positive semidefinite, there exists an n × n orthogonal matrix U such that
 证据。在定理20.3的证明中，由于a>a是对称半正定的，所以存在一个n×n正交矩阵u，使得

A>A = UΣ2U>,
 A>A=U∑2U>，

with Σ = diag(σ1,...,σr,0,...,0), where  are the nonzero eigenvalues of A>A, and where r is the rank of A. Observe that r ≤ min{m,n}, and AU is an m × n matrix. It follows that
 当∑=diag（σ1，…，σr，0，…，0），其中是a>a的非零特征值，其中r是a的秩。观察r≤min m，n，au是m×n矩阵。接下来是

U>A>AU = (AU)>AU = Σ2,
 u>a>au=（au）>au=∑2，

and if we let fj ∈ Rm be the jth column of AU for j = 1,...,n, then we have
 如果我们让Fj∈Rm为j=1，…，n的au的jth列，那么我们得到

​                                                      hfi,fji = σi2δij,        1 ≤ i,j ≤ r
 hfi，fji=σi2δi j，1≤i，j≤r

and
 和

​                                                           fj = 0,        r + 1 ≤ j ≤ n.
 fj=0，r+1≤j≤n。

If we define (v1,...,vr) by
 如果我们定义（v1，…，vr）

​                                                          vj = σj−1fj,       1 ≤ j ≤ r,
 Vj=σj−1fj，1≤j≤r，

then we have
 然后我们有了

​                                                        hvi,vji = δij,         1 ≤ i,j ≤ r,
 hvi，vji=δi j，1≤i，j≤r，

so complete (v1,...,vr) into an orthonormal basis (v1,...,vr,vr+1,...,vm) (for example, using Gram–Schmidt).
 因此，将（v1，…，vr）完全转换为正态基（v1，…，vr，vr+1，…，vm）（例如，使用gram-schmidt）。

Now since fj = σjvj for j = 1...,r, we have
 既然fj=σjvj，对于j=1…，r，我们有

​                                      hvi,fji = σjhvi,vji = σjδi,j,           1 ≤ i ≤ m, 1 ≤ j ≤ r
 hvi，fji=σjhvi，vji=σjδi，j，1≤i≤m，1≤j≤r

and since fj = 0 for j = r + 1,...,n, we have
 既然j=r+1时fj=0，…，n，我们有

​                                              hvi,fji = 0          1 ≤ i ≤ m, r + 1 ≤ j ≤ n.
 hvi，fji=0 1≤i≤m，r+1≤j≤n。

If V is the matrix whose columns are v1,...,vm, then V is an m×m orthogonal matrix and if m ≥ n, we let
 如果v是列为v1，…，v m的矩阵，那么v是m×m正交矩阵，如果m≥n，我们将

 ,
 ，

else if n ≥ m, then we let
 否则，如果n≥m，那么我们让

|     网络错误   σ1    网络错误       网络错误   D =  ...    网络错误       网络错误       网络错误 | σ2    网络错误   ...    网络错误 | ...    网络错误   ... ...    网络错误   ...    网络错误 | ...    网络错误   σm    网络错误 | 0    网络错误   0    网络错误   0    网络错误   0    网络错误 | ...    网络错误   ...    网络错误   ...    网络错误   ...    网络错误 | .    网络错误 |
| ------------------------------------------------------------ | -------------------------------- | ------------------------------------------------------- | -------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------- |
|                                                              |                                  |                                                         |                                  |                                                              |                                                              |               |

In either case, the above equations prove that
 无论哪种情况，上述方程都证明了

V >AU = D,
 v>au=d，

which yields A = V DU>, as required. The equation A = V DU> implies that
 根据需要，得出a=v du>。方程式a=v du>意味着

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

n−r
 n r

and
 和

AA> = V DD>V > = V diag(,
 aa>=v dd>v>=v诊断（，

m−r
 对氨基苯甲酸

which shows that A>A and AA> have the same nonzero eigenvalues, that the columns of U are eigenvectors of A>A, and that the columns of V are eigenvectors of AA>. 
 这表明A>A和AA>具有相同的非零特征值，U列是A>A的特征向量，V列是AA>的特征向量。

A triple (U,D,V ) such that A = V D U> is called a singular value decomposition (SVD) of A.
 一种三重（u，d，v），使a=v，d，u>称为a的奇异值分解（svd）。

### 20.4. SINGULAR VALUE DECOMPOSITION FOR RECTANGULAR MATRICES  20.4。矩形矩阵的奇异值分解

Example 20.4. Let . Then, and AA> =
 例20.4。让。然后，和aa>。=

 .                                                         The reader should verify that A>A = UΣ2U> where Σ and
 .读者应确认a>a=u∑2u>其中∑和

. Since  ,
 . 从那以后，

and complete an orthonormal basis for R3 by assigning, and. Thus
 并通过赋值完成r3的正交基，和。因此

V = I3, and the reader should verify that A = V DU>, where.
 v=i3，读卡器应验证a=v du>，其中。

Even though the matrix D is an m×n rectangular matrix, since its only nonzero entries are on the descending diagonal, we still say that D is a diagonal matrix.
 尽管矩阵d是一个m×n的矩形矩阵，但由于它的唯一非零项是在降对角线上，所以我们仍然认为d是一个对角线矩阵。

The Matlab command for computing an SVD A = V DU> of a matrix A is also [V, D, U] = svd(A).
 用于计算矩阵A的svd a=v d u>的matlab命令也是[v，d，u]=svd（a）。

If we view A as the representation of a linear map f : E → F, where dim(E) = n and dim(F) = m, the proof of Theorem 20.5 shows that there are two orthonormal bases (u1,..., un) and (v1,...,vm) for E and F, respectively, where (u1,...,un) are eigenvectors of f∗ ◦ f and (v1,...,vm) are eigenvectors of f ◦f∗. Furthermore, (u1,...,ur) is an orthonormal basis of Imf∗, (ur+1,...,un) is an orthonormal basis of Kerf, (v1,...,vr) is an orthonormal basis of Imf, and (vr+1,...,vm) is an orthonormal basis of Kerf∗.
 如果我们把a看作线性映射f:e→f的表示，其中dim（e）=n和dim（f）=m，定理20.5的证明表明e和f分别有两个正交基（u1，…，un）和（v1，…，vm），其中（u1，…，un）是f f和（v1，…，vm）的特征向量是特征向量。F F的任务大纲。此外，（u1，…，ur）是imf的正态基，（ur+1，…，un）是kerf的正态基，（v1，…，vr）是imf的正态基，（vr+1，…，vm）是kerf的正态基。

The SVD of matrices can be used to define the pseudo-inverse of a rectangular matrix; we will do so in Chapter 21. The reader may also consult Strang [165], Demmel [49], Trefethen and Bau [171], and Golub and Van Loan [80].
 矩阵的SVD可用于定义矩形矩阵的伪逆矩阵；我们将在第21章中这样做。读者还可以咨询Strang[165]、Demmel[49]、Trefetten和Bau[171]以及Golub和van Loan[80]。

One of the spectral theorems states that a symmetric matrix can be diagonalized by an orthogonal matrix. There are several numerical methods to compute the eigenvalues of a symmetric matrix A. One method consists in tridiagonalizing A, which means that there exists some orthogonal matrix P and some symmetric tridiagonal matrix T such that A = PTP >. In fact, this can be done using Householder transformations; see Theorem 22.2. It is then possible to compute the eigenvalues of T using a bisection method based on Sturm sequences. One can also use Jacobi’s method. For details, see Golub and Van Loan [80], Chapter 8, Demmel [49], Trefethen and Bau [171], Lecture 26, Ciarlet [41], and Chapter 22. Computing the SVD of a matrix A is more involved. Most methods begin by finding orthogonal matrices U and V and a bidiagonal matrix B such that A = V BU>; see Problem 12.8 and Problem 20.3. This can also be done using Householder transformations. Observe that B>B is symmetric tridiagonal. Thus, in principle, the previous method to diagonalize a symmetric tridiagonal matrix can be applied. However, it is unwise to compute B>B explicitly, and more subtle methods are used for this last step; the matrix of Problem 20.1 can be used, and see Problem 20.3. Again, see Golub and Van Loan [80], Chapter 8, Demmel [49], and Trefethen and Bau [171], Lecture 31.
 谱定理之一指出对称矩阵可以由正交矩阵对角化。计算对称矩阵A特征值的数值方法有多种，其中一种方法是三对角化A，即存在一些正交矩阵P和一些对称的三对角矩阵T，从而a=p t p>。事实上，这可以通过户主转换来实现；参见定理22.2。然后可以使用基于sturm序列的二分法计算t的特征值。也可以使用雅可比方法。有关详细信息，请参见Golub和van Loan[80]、第8章、Demmel[49]、Trefethen和Bau[171]、第26讲、Ciarlet[41]和第22章。计算矩阵A的SVD更为复杂。大多数方法首先找到正交矩阵u和v以及双对角矩阵b，使a=v bu>；参见问题12.8和问题20.3。这也可以通过户主转换来实现。观察b>b为对称三对角。因此，原则上，可以应用先前的对称三对角矩阵对角化方法。但是，显式地计算b>b是不明智的，最后一步使用更精细的方法；可以使用问题20.1的矩阵，见问题20.3。同样，见Golub和van Loan[80]，第8章，Demmel[49]和Trefethen和Bau[171]，第31课。

The polar form has applications in continuum mechanics. Indeed, in any deformation it is important to separate stretching from rotation. This is exactly what QS achieves. The orthogonal part Q corresponds to rotation (perhaps with an additional reflection), and the symmetric matrix S to stretching (or compression). The real eigenvalues σ1,...,σr of S are the stretch factors (or compression factors) (see Marsden and Hughes [117]). The fact that S can be diagonalized by an orthogonal matrix corresponds to a natural choice of axes, the principal axes.
 极性形式在连续介质力学中有应用。实际上，在任何变形中，将拉伸与旋转分开都是很重要的。这正是QS所实现的。正交部分q对应于旋转（可能带有附加反射），对称矩阵s对应于拉伸（或压缩）。S的实际特征值σ1，…，σr是拉伸系数（或压缩系数）（见Marsden和Hughes[117]）。事实上，S可以由一个正交矩阵对角化对应于轴的自然选择，主轴。

The SVD has applications to data compression, for instance in image processing. The idea is to retain only singular values whose magnitudes are significant enough. The SVD can also be used to determine the rank of a matrix when other methods such as Gaussian elimination produce very small pivots. One of the main applications of the SVD is the computation of the pseudo-inverse. Pseudo-inverses are the key to the solution of various optimization problems, in particular the method of least squares. This topic is discussed in the next chapter (Chapter 21). Applications of the material of this chapter can be found in Strang [165, 164]; Ciarlet [41]; Golub and Van Loan [80], which contains many other references; Demmel [49]; and Trefethen and Bau [171].
 SVD应用于数据压缩，例如图像处理。其思想是只保留数量足够大的奇异值。当其他方法如高斯消去产生非常小的支点时，SVD也可以用来确定矩阵的秩。支持向量机的主要应用之一是伪逆的计算。伪逆是求解各种优化问题的关键，尤其是最小二乘法。本主题将在下一章（第21章）中讨论。本章材料的应用可在Strang[165164]、Ciarlet[41]、Golub和van Loan[80]中找到，其中包含许多其他参考文献；Demmel[49]、Trefethen和Bau[171]。

## 20.5           Ky Fan Norms and Schatten Norms  20.5 KY Fan规范和Schatten规范

The singular values of a matrix can be used to define various norms on matrices which have found recent applications in quantum information theory and in spectral graph theory. Following Horn and Johnson [93] (Section 3.4) we can make the following definitions:
 矩阵的奇异值可以用来定义矩阵上的各种范数，这些范数在量子信息理论和谱图理论中有着最新的应用。根据Horn和Johnson[93]（第3.4节），我们可以做出以下定义：

Definition 20.5. For any matrix A ∈ Mm,n(C), let q = min{m,n}, and if σ1 ≥ ··· ≥ σq are the singular values of A, for any k with 1 ≤ k ≤ q, let
 定义20.5.对于任意矩阵a∈m m，n（c），设q=min m，n，如果σ1≥······································

Nk(A) = σ1 + ··· + σk,
 nk（a）=σ1+·····+σk，

called the Ky Fan k-norm of A.
 称为A的KY范k-范数。

More generally, for any p ≥ 1 and any k with 1 ≤ k ≤ q, let
 更一般地说，对于任何p≥1和任何k（1≤k≤q），让

,
 ，

called the Ky Fan p-k-norm of A. When k = q, Nq;p is also called the Schatten p-norm.
 称为a的ky fan p-k-norm。当k=q，nq；p也称为schatten p-norm。

Observe that when k = 1, N1(A) = σ1, and the Ky Fan norm N1 is simply the spectral norm from Chapter 8, which is the subordinate matrix norm associated with the Euclidean norm. When k = q, the Ky Fan norm Nq is given by
 注意，当k=1时，n1（a）=σ1，而ky-fan范数n1只是第8章中的谱范数，它是与欧几里得范数相关联的次矩阵范数。当k=q时，Ky扇范数nq由下式给出：

Nq(A) = σ1 + ··· + σq = tr((A∗A)1/2)
 nq（a）=σ1+·····+σq=tr（（a a）1/2）

### 20.6. SUMMARY  20.6。总结

and is called the trace norm or nuclear norm. When p = 2 and k = q, the Ky Fan Nq;2 norm is given by
 称为痕迹规范或核规范。当p=2和k=q时，ky fan nq；2范数由下式给出

,
 ，

which is the Frobenius norm of A.
 这是A的Frobenius规范。

It can be shown that Nk and Nk;p are unitarily invariant norms, and that when m = n, they are matrix norms; see Horn and Johnson [93] (Section 3.4, Corollary 3.4.4 and Problem
 可以看出，nk和nk；p是统一不变范数，当m=n时，它们是矩阵范数；见Horn和Johnson[93]（第3.4节，推论3.4.4和问题

3).
 3）。

## 20.6      Summary  20.6总结

The main concepts and results of this chapter are listed below:
 本章的主要概念和结果如下：

•     For any linear map f : E → E on a Euclidean space E, the maps f∗ ◦f and f ◦f∗ are self-adjoint and positive semidefinite.
 对于欧几里得空间E上的任何线性映射f:e→e，该映射f f和f f是自伴半定的。

•     The singular values of a linear map.
 线性映射的奇异值。

•     Positive semidefinite and positive definite self-adjoint maps.
 正半定和正定自伴映射。

•     Relationships between Imf, Kerf, Imf∗, and Kerf∗.
 imf、kerf、imf和kerf之间的关系。

•     The singular value decomposition theorem for square matrices (Theorem 20.3).
 平方矩阵的奇异值分解定理（定理20.3）。

•     The SVD of matrix.
 矩阵的SVD。

•     The polar decomposition of a matrix.
 矩阵的极分解。

•     The Weyl inequalities.
 韦尔不等式。

•     The singular value decomposition theorem for m × n matrices (Theorem 20.5).
 m×n矩阵的奇异值分解定理（定理20.5）。

•     Ky Fan k-norms, Ky Fan p-k-norms, Schatten p-norms.
 KY-Fan k-规范，KY-Fan p-k-规范，Schatten p-规范。

## 20.7      Problems  20.7问题

Problem 20.1. (1) Let A be a real n×n matrix and consider the (2n)×(2n) real symmetric matrix
 问题20.1。（1）设a为实n×n矩阵，并考虑（2n）×（2n）实对称矩阵

 .
 .

Suppose that A has rank r. If A = V ΣU> is an SVD for A, with Σ = diag(σ1,...,σn) and σ1 ≥ ··· ≥ σr > 0, denoting the columns of U by uk and the columns of V by vk, prove that σk is an eigenvalue of S with corresponding eigenvector , and that −σk is an eigenvalue of S with corresponding eigenvector .
 假设a的秩为r，如果a=v∑u>是a的SVD，用∑=diag（σ1，…，σn）和σ1≥·······················································Nding特征向量。

Hint. We have Auk = σkvk for k = 1,...,n. Show that A>vk = σkuk for k = 1,...,r, and that A>vk = 0 for k = r + 1,...,n. Recall that Ker(A>) = Ker(AA>).
 暗示。对于k=1，…，n，我们有auk=σk vk。表明，对于k=1，…，r，a>vk=σkuk，而对于k=r+1，…，n，a>vk=0。回想一下，ker（a>）=ker（aa>）。

(2)      Prove that the 2n eigenvectors of S in (1) are pairwise orthogonal. Check that if A has rank r, then S has rank 2r.
 证明（1）中s的2n特征向量是成对正交的。检查A是否具有等级R，则S是否具有等级2R。

(3)      Now assume that A is a real m × n matrix and consider the (m + n) × (m + n) real symmetric matrix
 假设A是实M×N矩阵，考虑（M+N）×实对称矩阵

 .
 .

Suppose that A has rank r. If A = V ΣU> is an SVD for A, prove that σk is an eigenvalue of S with corresponding eigenvector , and that −σk is an eigenvalue of
 假设a有秩r，如果a=v∑u>是a的svd，证明σk是具有相应特征向量的s的特征值，而−σk是

S with corresponding eigenvector .
 与相应的特征向量。

Find the remaining m + n − 2r eigenvectors of S associated with the eigenvalue 0.
 找到与特征值0相关的s的剩余m+n−2r特征向量。

(4) Prove that these m + n eigenvectors of S are pairwise orthogonal.
 （4）证明了S的M+N特征向量是成对正交的。

Problem 20.2. Let A be a real m × n matrix of rank r and let q = min(m,n).
 问题20.2。设a为秩r的实m×n矩阵，设q=min（m，n）。

(1)  Consider the (m + n) × (m + n) real symmetric matrix
 考虑（m+n）×（m+n）实对称矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

and prove that
 并证明

 .
 .

Use the above equation to prove that
 用上述方程证明

det(zIm+n − S) = tn−m det(t2Im − AA>).
 det（zim+n−s）=tn−m det（t2im−aa>）。

(2)  Prove that the eigenvalues of S are ±σ1,...,±σq, with |m − n| additional zeros.
 证明了S的特征值是±σ1，…，±σq，加上m−n 0。

Problem 20.3. Let B be a real bidiagonal matrix of the form
 问题20.3。设b为形式的实双对角矩阵

| a1    网络错误    0    网络错误       网络错误   B =  ...    网络错误        网络错误    0    网络错误   0    网络错误 | b1    网络错误   a2    网络错误   ... ···    网络错误   0    网络错误 | 0    网络错误   b2    网络错误   ...    网络错误   0    网络错误   ···    网络错误 | ···    网络错误   ...    网络错误   ...    网络错误   an−1    网络错误   0    网络错误 | 0     网络错误   0     网络错误   ... .    网络错误   bn−1    网络错误   an    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |

### 20.7. PROBLEMS  20.7。问题

Let A be the (2n) × (2n) symmetric matrix
 设A为（2n）×（2n）对称矩阵

 ,
 ，

and let P be the permutation matrix given by P = [e1,en+1,e2,en+2,··· ,en,e2n].
 设p为p=[e1，en+1，e2，en+2，···，en，e2n]给出的置换矩阵。

| diagonal   of the form    网络错误                           |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|     网络错误   0    网络错误   a1    网络错误     0    网络错误       网络错误    0    网络错误   T =  ...    网络错误       网络错误     0   0    网络错误       网络错误   0    网络错误 | a1 0    网络错误   b1    网络错误   0    网络错误   ...    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0    网络错误   b1 0 a2    网络错误   ...    网络错误   0    网络错误   0    网络错误   0    网络错误 | 0 0 a2    网络错误   0    网络错误   ...    网络错误   ···    网络错误   ···    网络错误   ···    网络错误 | 0 0    网络错误   0    网络错误   b2    网络错误   ...    网络错误   an−1    网络错误   0    网络错误   0    网络错误 | 0 0    网络错误   0 0    网络错误   ...    网络错误   0    网络错误   bn−1    网络错误   0    网络错误 | ···    网络错误   ··· ···    网络错误   ···...    网络错误   bn−1 0 an    网络错误 | 0     网络错误   0     网络错误   0     网络错误   0     网络错误   ...   .    网络错误   0    an    网络错误   0    网络错误 |

(1)      Prove that T = P >AP is a symmetric tridiagonal (2n)×(2n) matrix with zero main
 证明t=p>a p是一个主零点的对称三对角（2n）×2n矩阵

(2)      Prove that if xi is a unit eigenvector for an eigenvalue λi of T, then λi = ±σi where σi is a singular value of B, and that
 证明了如果Xi是T的特征值Li i的单位特征向量，则Li I＝±Sigi I，其中Sigi I是B的奇异值，并且

,
 ，

where the ui are unit eigenvectors of B>B and the vi are unit eigenvectors of BB>. Problem 20.4. Find the SVD of the matrix
 其中，ui是b>b的单位特征向量，vi是bb>的单位特征向量。问题20.4。找到矩阵的SVD

 .
 .

Problem 20.5. Let u,v ∈ Rn be two nonzero vectors, and let A = uv> be the corresponding rank 1 matrix. Prove that the nonzero singular value of A is kuk2 kvk2.
 问题20.5。设u，v∈rn为两个非零向量，a=uv>为相应的秩1矩阵。证明了A的非零奇异值是kuk2 kvk2。

Problem 20.6. Let A be a n×n real matrix. Prove that if σ1,...,σn are the singular values of A, thenare the singular values of AA>A.
 问题20.6。设a为n×n实矩阵。证明如果σ1，…，σn是a的奇异值，那么aa>a的奇异值。

Problem 20.7. Let A be a real n × n matrix.
 问题20.7。设A为实n×n矩阵。

(1)   Prove that the largest singular value σ1 of A is given by
 证明a的最大奇异值σ1由下式给出

,
 ，

and that this supremum is achieved at x = u1, the first column in U in an SVD A = V ΣU>.
 这个上确界是在x=u1处得到的，在svd a=v∑u>中u的第一列。

(2)   Extend the above result to real m × n matrices.
 将上述结果扩展到实M×N矩阵。

Problem 20.8. Let A be a real m × n matrix. Prove that if B is any submatrix of A (by keeping M ≤ m rows and N ≤ n columns of A), then (σ1)B ≤ (σ1)A (where (σ1)A is the largest singular value of A and similarly for (σ1)B).
 问题20.8。设A为实M×N矩阵。证明如果b是a的任何子矩阵（通过保持m≤m行，n≤n列a），则（σ1）b≤（σ1）a（其中（σ1）a是a的最大奇异值，与（σ1）b相似）。

Problem 20.9. Let A be a real n × n matrix.
 问题20.9。设A为实n×n矩阵。

(1)      Assume A is invertible. Prove that if A = Q1S1 = Q2S2 are two polar decompositions of A, then Q1 = Q2 and S1 = S2.
 假设a是可逆的。证明如果a=q1 s1=q2 s2是a的两个极分解，那么q1=q2，s1=s2。

Hint. , with S1 and S2 symmetric positive definite. Then use Problem 16.7.
 暗示。，具有s1和s2对称正定。然后使用问题16.7。

(2)      Now assume that A is singular. Prove that if A = Q1S1 = Q2S2 are two polar decompositions of A, then S1 = S2, but Q1 may not be equal to Q2.
 现在假设a是单数。证明如果a=q1 s1=q2 s2是a的两个极分解，那么s1=s2，但q1可能不等于q2。

Problem 20.10. (1) Let A be any invertible (real) n × n matrix. Prove that for every SVD, A = V DU> of A, the product V U> is the same (i.e., if , then
 问题20.10。（1）设A为任意可逆（实）n×n矩阵。证明对于每个SVD，a=v du>a，产品v u>是相同的（即，如果，那么

). What does V U> have to do with the polar form of A?
 ）v u>与a的极性形式有什么关系？

(2) Given any invertible (real) n × n matrix, A, prove that there is a unique orthogonal matrix, Q ∈ O(n), such that kA − QkF is minimal (under the Frobenius norm). In fact, prove that Q = V U>, where A = V DU> is an SVD of A. Moreover, if det(A) > 0, show that Q ∈ SO(n).
 （2）给定任意可逆（实）n×n矩阵，a，证明存在唯一的正交矩阵q∈o（n），使得ka−qkf最小（在frobenius范数下）。事实上，证明了q=v u>，其中a=v du>是a的一个svd，并且，如果det（a）>0，则表明q∈so（n）。

What can you say if A is singular (i.e., non-invertible)?
 如果a是单数（即不可逆），你能说什么？

Problem 20.11. (1) Prove that for any n × n matrix A and any orthogonal matrix Q, we have max{tr(QA) | Q ∈ O(n)} = σ1 + ··· + σn,
 问题20.11。（1）证明对于任意n×n矩阵a和任意正交矩阵q，我们有max tr（qa）q∈o（n）=σ1+······+σn，

where σ1 ≥ ··· ≥ σn are the singular values of A. Furthermore, this maximum is achieved by Q = UV >, where A = V ΣU> is any SVD for A.
 其中，σ1≥··············································

(2) By applying the above result with A = Z>X and Q = R>, deduce the following result : For any two fixed n × k matrices X and Z, the minimum of the set
 （2）通过将上述结果与a=z>x和q=r>一起应用，推导出以下结果：对于任意两个固定的n×k矩阵x和z，集合的最小值

{kX − ZRkF | R ∈ O(k)}
 kx−zrkf r∈o（k）

is achieved by R = V U> for any SVD decomposition V ΣU> = Z>X of Z>X.
 对于任何SVD分解V∑U>=Z>X，通过R=V U>实现。

Remark: The problem of finding an orthogonal matrix R such that ZR comes as close as possible to X is called the orthogonal Procrustes problem; see Strang [166] (Section IV.9) for the history of this problem.
 

注：找到一个正交矩阵r，使zr尽可能接近x的问题称为正交procrustes问题；关于这个问题的历史，见strang[166]（第4.9节）。