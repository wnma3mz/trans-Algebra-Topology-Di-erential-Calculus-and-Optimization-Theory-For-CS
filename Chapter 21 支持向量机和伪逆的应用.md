第二十一章
Applications of SVD and Pseudo-Inverses
支持向量机和伪逆的应用
De tous les principes qu’on peut proposer pour cet objet, je pense qu’il n’en est pas de plus g´en´eral, de plus exact, ni d’une application plus facile, que celui dont nous avons fait usage dans les recherches pr´ec´edentes, et qui consiste `a rendre minimum la somme des carr´es des erreurs. Par ce moyen il s’´etablit entre les erreurs une sorte d’´equilibre qui, empˆechant les extrˆemes de pr´evaloir, est tr`es propre `as faire connaitre l’´etat du syst`eme le plus proche de la v´erit´e.
我们的原则是，我们的建议者必须保证所有的工作都能顺利完成，而且必须准确无误，申请程序简单易行，我们不知道如何使用这些资源，并考虑到至少要有一个完整的工作流程。瑞尔。《欧洲货币体系》中的“电子商务中心”未经分类的“公平报价”，《欧洲货币体系外部评估》，《欧洲货币体系》中的“公平竞争”部分。
—Legendre, 1805, Nouvelles M´ethodes pour la d´etermination des Orbites des Com`etes
-勒让德，1805年，《轨道测量的新方法》
21.1	Least Squares Problems and the Pseudo-Inverse
21.1最小二乘问题和伪逆问题
This chapter presents several applications of SVD. The first one is the pseudo-inverse, which plays a crucial role in solving linear systems by the method of least squares. The second application is data compression. The third application is principal component analysis (PCA), whose purpose is to identify patterns in data and understand the variance–covariance structure of the data. The fourth application is the best affine approximation of a set of data, a problem closely related to PCA.
本章介绍了SVD的几种应用。第一种是伪逆，它在最小二乘法求解线性系统中起着至关重要的作用。第二个应用程序是数据压缩。第三个应用是主成分分析（PCA），其目的是识别数据中的模式并了解数据的方差-协方差结构。第四个应用是一组数据的最佳仿射近似，这是一个与主成分分析密切相关的问题。
The method of least squares is a way of “solving” an overdetermined system of linear equations
最小二乘法是求解超定线性方程组的一种方法。
Ax = b,
ax=b，
i.e., a system in which A is a rectangular m×n matrix with more equations than unknowns (when m > n). Historically, the method of least squares was used by Gauss and Legendre to solve problems in astronomy and geodesy. The method was first published by Legendre in 1805 in a paper on methods for determining the orbits of comets. However, Gauss had already used the method of least squares as early as 1801 to determine the orbit of the asteroid
也就是说，其中a是一个矩形m×n矩阵，方程多于未知方程（当m>n时）。历史上，高斯和勒让德使用最小二乘法来解决天文学和大地测量学中的问题。勒让德于1805年在一篇关于彗星轨道确定方法的论文中首次发表了这一方法。然而，早在1801年，高斯就已经使用最小二乘法来确定小行星的轨道。
631
六百三十一
Ceres, and he published a paper about it in 1810 after the discovery of the asteroid Pallas. Incidentally, it is in that same paper that Gaussian elimination using pivots is introduced.
在发现小行星帕拉斯之后，他于1810年发表了一篇关于它的论文。顺便说一句，在同一篇文章中，介绍了利用支点进行高斯消元。
The reason why more equations than unknowns arise in such problems is that repeated measurements are taken to minimize errors. This produces an overdetermined and often inconsistent system of linear equations. For example, Gauss solved a system of eleven equations in six unknowns to determine the orbit of the asteroid Pallas.
在这些问题中，产生的方程多于未知数的原因是为了使误差最小化而重复测量。这就产生了一个超定的，经常不一致的线性方程组。例如，高斯在六个未知数中解出了一个由十一个方程组成的系统来确定小行星帕拉斯的轨道。
Example 21.1. As a concrete illustration, suppose that we observe the motion of a small object, assimilated to a point, in the plane. From our observations, we suspect that this point moves along a straight line, say of equation y = dx + c. Suppose that we observed the moving point at three different locations (x1,y1), (x2,y2), and (x3,y3). Then we should have
例21.1。作为一个具体的例子，假设我们观察一个小物体的运动，被同化到平面上的一个点上。根据我们的观察，我们怀疑这一点沿着直线移动，例如方程y=dx+c。假设我们在三个不同的位置（x1、y1）、（x2、y2）和（x3、y3）观察到移动点。那么我们应该
c + dx1 = y1, c + dx2 = y2, c + dx3 = y3.
C+dx1=y1，C+dx2=y2，C+dx3=y3。
If there were no errors in our measurements, these equations would be compatible, and c and d would be determined by only two of the equations. However, in the presence of errors, the system may be inconsistent. Yet we would like to find c and d!
如果在我们的测量中没有误差，这些方程将是兼容的，C和D将只由两个方程确定。但是，在出现错误时，系统可能不一致。但是我们想找到C和D！
The idea of the method of least squares is to determine (c,d) such that it minimizes the sum of the squares of the errors, namely,
最小二乘法的思想是确定（c，d），使误差平方和最小化，即，
(c + dx1 − y1)2 + (c + dx2 − y2)2 + (c + dx3 − y3)2.
（C+DX1−Y1）2+（C+DX2−Y2）2+（C+DX3−Y3）2.
See Figure 21.1.
见图21.1。

Figure 21.1: Given three points (x1,y1), (x2,y2), (x3,y3), we want to determine the line y = cx + d which minimizes the lengths of the dashed vertical lines.
图21.1：给定三个点（x1，y1），（x2，y2），（x3，y3），我们想确定一条线y=cx+d，它将虚线垂直线的长度最小化。
In general, for an overdetermined m × n system Ax = b, what Gauss and Legendre discovered is that there are solutions x minimizing
一般来说，对于一个超定的m×n系统ax=b，高斯和勒让德发现有解x最小化

(where, the square of the Euclidean norm of the vector u = (u1,...,un)), and that these solutions are given by the square n × n system
（式中，向量u的欧几里得范数的平方=（u1，…，u n）），这些解由平方n×n系统给出。
A>Ax = A>b,
a>ax=a>b，
called the normal equations. Furthermore, when the columns of A are linearly independent, it turns out that A>A is invertible, and so x is unique and given by
称为法方程。此外，当a的列是线性无关的时，结果表明a>a是可逆的，因此x是唯一的，由
x = (A>A)−1A>b.
x=（a>a）−1a>b.
Note that A>A is a symmetric matrix, one of the nice features of the normal equations of a least squares problem. For instance, since the above problem in matrix form is represented as
注意a>a是一个对称矩阵，是最小二乘法方程的一个很好的特征。例如，由于上述矩阵形式的问题表示为
 ,
，
the normal equations are
正态方程是
 .
.
In fact, given any real m × n matrix A, there is always a unique x+ of minimum norm that minimizes, even when the columns of A are linearly dependent. How do we prove this, and how do we find x+?
事实上，对于任何实M×N矩阵A，总是有一个唯一的最小范数x+，即使A的列是线性相关的，也会最小化。我们如何证明这一点，以及如何找到x+？
Theorem 21.1. Every linear system Ax = b, where A is an m × n matrix, has a unique least squares solution x+ of smallest norm.
定理21.1。每个线性系统a x=b，其中a是m×n矩阵，具有最小范数的唯一最小二乘解x+。
Proof. Geometry offers a nice proof of the existence and uniqueness of x+. Indeed, we can interpret b as a point in the Euclidean (affine) space Rm, and the image subspace of A (also called the column space of A) as a subspace U of Rm (passing through the origin). Then it is clear that
证据。几何为X+的存在和唯一性提供了很好的证明。实际上，我们可以把b解释为欧几里得空间rm中的一个点，把a的图像子空间（也称为a的列空间）解释为rm的子空间u（通过原点）。很明显
,
，
with U = ImA, and we claim that x minimizes kAx−, where p the orthogonal projection of b onto the subspace U.
当u=ima时，我们认为x使kax-最小化，其中p是b在子空间u上的正交投影。
Recall from Section 12.1 that the orthogonal projection pU : U ⊕ U⊥ → U is the linear map given by
从第12.1节回忆起，正交投影pu:u u→u是由
pU(u + v) = u,
pu（u+v）=u，
with u ∈ U and v ∈→−U⊥. If we let− ∈ p = pU(b) ∈ U, then for any point y ∈ U, the vectors py−→ = y − p ∈ U and bp = p b U⊥ are orthogonal, which implies that
带u∈u和v∈→−u。如果我们让−p=p u（b）∈u，那么对于任意点y∈u，向量py−→=y−p∈u和bp=p b u是正交的，这意味着
,
，
where →−by = y −b. Thus, p is indeed the unique point in U that minimizes the distance from b to any point in U. See Figure 21.2.
其中→−b y=y−b。因此，p确实是u中的唯一点，它将b到u中任何点的距离减至最小。见图21.2。

Figure 21.2: Given a 3 × 2 matrix A, U = ImA is the peach plane in R3 and p is the orthogonal projection of b onto U. Furthermore, given y ∈ U, the points b, y, and p are the vertices of a right triangle.
图21.2：给定3×2矩阵a，u=ima是r3中的桃平面，p是b在u上的正交投影。此外，给定y∈u，点b、y和p是直角三角形的顶点。
Thus the problem has been reduced to proving that there is a unique x+ of minimum norm such that Ax+ = p, with p = pU(b) ∈ U, the orthogonal projection of b onto U. We use the fact that
因此，该问题被简化为证明存在一个唯一的最小范数x+，使得ax+=p，其中p=p u（b）∈u，b对u的正交投影。
Rn = KerA ⊕ (KerA)⊥.
RN=KERA（KERA）。
Consequently, every x ∈ Rn can be written uniquely as x = u + v, where u ∈ KerA and v ∈ (KerA)⊥, and since u and v are orthogonal,
因此，每个x∈rn可以唯一地写成x=u+v，其中u∈kera和v∈（kera），并且由于u和v是正交的，
.
.
Furthermore, since u ∈ KerA, we have Au = 0, and thus Ax = p iff Av = p, which shows that the solutions of Ax = p for which x has minimum norm must belong to (KerA)⊥. However, the restriction of A to (KerA)⊥ is injective. This is because if Av1 = Av2, where v1,v2 ∈ (KerA)⊥, then A(v2 − v2) = 0, which implies v2 − v1 ∈ KerA, and since v1,v2 ∈ (KerA)⊥, we also have v2 − v1 ∈ (KerA)⊥, and consequently, v2 − v1 = 0. This shows that there is a unique x+ of minimum norm such that Ax+ = p, and that x+ must belong to
此外，由于u∈kera，我们得到了au=0，因此ax=p iff av=p，这表明x具有最小范数的ax=p的解必须属于（kera）。但是，A到（KERA）的限制是注射性的。这是因为如果a v1=a v2，其中v1，v2∈（kera），那么a（v2−v2）=0，这意味着v2−v1∈kera，并且由于v1，v2∈（kera），我们也有v2−v1∈（kera），因此，v2−v1=0。这表明有一个最小范数的唯一x+，这样ax+=p，x+必须属于
(KerA)⊥. By our previous reasoning, x+ is the unique vector of minimum norm minimizing
（喀拉邦）。根据前面的推理，x+是最小范数最小的唯一向量。
.	
.
The proof also shows that x minimizesis orthogonal to U, which can be expressed by saying that b−Ax is orthogonal to every column of A. However, this is equivalent to
证明还表明，x与u正交，可以用b-ax与a的每一列正交来表示。然而，这相当于
	A>(b − Ax) = 0,	i.e.,	A>Ax = A>b.
a>（b−ax）=0，即a>ax=a>b。
Finally, it turns out that the minimum norm least squares solution x+ can be found in terms of the pseudo-inverse A+ of A, which is itself obtained from any SVD of A.
最后，证明了最小范数最小二乘解x+可以用a的伪逆a+来表示，a的伪逆a+本身就是从a的任意svd得到的。
Definition 21.1. Given any nonzero m × n matrix A of rank r, if A = V DU> is an SVD of A such that
定义21.1.给定秩r的任何非零m×n矩阵a，如果a=v du>是a的svd，
 ,
，
with
具有
Λ = diag(λ1,...,λr)
∧=diag（λ1，…，λr）
an r ×r diagonal matrix consisting of the nonzero singular values of A, then if we let D+ be the n × m matrix
一个由a的非零奇异值组成的r×r对角矩阵，如果我们让d+是n×m矩阵
 ,
，
with
具有
Λ−1 = diag(1/λ1,...,1/λr),
∧−1=diag（1/λ1，…，1/λr），
the pseudo-inverse of A is defined by
a的伪逆定义为
A+ = UD+V >.
a+=ud+v>。
If A = 0m,n is the zero matrix, we set A+ = 0n,m. Observe that D+ is obtained from D by inverting the nonzero diagonal entries of D, leaving all zeros in place, and then transposing the matrix. For example, given the matrix
如果a=0 m，n是零矩阵，我们设置a+=0 n，m。观察d+是通过颠倒d的非零对角线项得到的，保留所有零，然后转置矩阵。例如，给定矩阵
,
，
its pseudo-inverse is
它的伪逆是
The pseudo-inverse of a matrix is also known as the Moore–Penrose pseudo-inverse.
矩阵的伪逆矩阵也称为摩尔-彭罗斯伪逆矩阵。
Actually, it seems that A+ depends on the specific choice of U and V in an SVD (U,D,V ) for A, but the next theorem shows that this is not so.
实际上，a+似乎取决于a的svd（u，d，v）中u和v的具体选择，但是下一个定理表明这不是这样的。
Theorem 21.2. The least squares solution of smallest norm of the linear system Ax = b, where A is an m × n matrix, is given by
定理21.2。线性系统最小范数的最小二乘解ax=b，其中a是m×n矩阵，由下式得出：
x+ = A+b = UD+V >b.
x+=a+b=ud+v>b。
Proof. First assume that A is a (rectangular) diagonal matrix D, as above. Then since x minimizesis the projection of b onto the image subspace F of D, it is fairly obvious that x+ = D+b. Otherwise, we can write
证据。首先假设a是（矩形）对角矩阵d，如上所述。然后，由于x最小化了b在d的图像子空间f上的投影，很明显x+=d+b。否则，我们可以写
A = V DU>,
a=v du>，
where U and V are orthogonal. However, since V is an isometry,
其中u和v是正交的。但是，既然v是等距测量，
kAx − bk2 = kV DU>x − bk2 = kDU>x − V >bk2.
kax−bk2=kv du>x−bk2=kdu>x−v>bk2。
Letting y = U>x, we have kxk2 = kyk2, since U is an isometry, and since U is surjective, kAx − bk2 is minimized iff kDy − V >bk2 is minimized, and we have shown that the least solution is
假设y=u>x，我们得到kxk2=kkk2，因为u是一个等值线，并且由于u是可预测的，所以当kdy−v>bk2最小化时，kax−bk2最小化，并且我们已经证明了最小解是
y+ = D+V >b.
Y+=D+V>B。
Since y = U>x, with kxk2 = kyk2, we get
因为y=u>x，kxk2=kkk2，我们得到
x+ = UD+V >b = A+b.
x+=ud+v>b=a+b。
Thus, the pseudo-inverse provides the optimal solution to the least squares problem.	
因此，伪逆为最小二乘问题提供了最优解。
By Theorem 21.2 and Theorem 21.1, A+b is uniquely defined by every b, and thus A+ depends only on A.
根据定理21.2和21.1，a+b由每个b唯一定义，因此a+仅依赖于a。
The Matlab command for computing the pseudo-inverse B of the matrix A is B = pinv(A).
用于计算矩阵A的伪逆B的matlab命令是b=pinv（a）。
Example 21.2. If A is the rank 2 matrix
例21.2。如果a是秩2矩阵

whose eigenvalues are −1.1652,0,0,17.1652, using Matlab we obtain the SVD A = V DU>
其特征值为−1.1652,0,0,17.1652，使用matlab，我们得到了SVD a=v du>

with
具有
−0.3147
网络错误
U	= −−00..42755402
网络错误

网络错误
−0.6530
网络错误
−0.3147
网络错误
V	= −−00..42755402
网络错误

网络错误
−0.6530
网络错误	0.7752
网络错误
0.3424
网络错误
−00..09035231
网络错误
−
网络错误
−00..77523424
网络错误
−0.0903
网络错误
0.5231
网络错误	0.2630
网络错误
0.0075
网络错误
−0.8039
网络错误
0.5334
网络错误
0.5452
网络错误
−0.7658
网络错误
−0.1042
网络错误
0.3247
网络错误	−0.4805
网络错误
0.8366 
网络错误
−0.2319,
网络错误
−0.1243
网络错误
0.0520 
网络错误
0.3371 
网络错误
−0.8301,
网络错误
0.4411
网络错误

	17.1652	0	0	0
17.1652 0 0_
	D =  00	1.16520	00	00.
D=00 1.16520 00 00。
	0	0	0	0
0 0 0 0 0
Then
然后
and
网络错误	 	0
网络错误
0.8583 0
网络错误
0
网络错误	0	0
网络错误
0	0,
网络错误
0	0
网络错误
0	0
网络错误	
	 	−00..22000900
网络错误
−0.0400
网络错误
0.1700
网络错误	0.0700 0.0400
网络错误
0.0100
网络错误
−0.0200
网络错误	0.3600 
网络错误
0.1700 , −0.0200
网络错误
−0.2100
网络错误
which is also the result obtained by calling pinv(A).
这也是通过调用pinv（a）获得的结果。
If A is an m × n matrix of rank n (and so m ≥ n), it is immediately shown that the
如果a是n阶的m×n矩阵（因此m≥n），则立即显示
QR-decomposition in terms of Householder transformations applies as follows:
就户主转换而言，QR分解应用如下：
There are n m × m matrices H1,...,Hn, Householder matrices or the identity, and an upper triangular m × n matrix R of rank n such that
有n个m×m矩阵h1，…，hn，户主矩阵或恒等式，以及一个上三角m×n矩阵r的秩n，这样
A = H1 ···HnR.
a=h1···hnr。
Then because each Hi is an isometry,
因为每个Hi都是一个等距线，
kAx − bk2 = kRx − Hn ···H1bk2,
kax−bk2=krx−hn···h1bk2，
and the least squares problem Ax = b is equivalent to the system
最小二乘问题ax=b等于系统
Rx = Hn ···H1b.
rx=hn···h1b.
Now the system
现在系统
	Rx = Hn	H b
Rx=Hn H b
is of the form
是这样的
,
，
where R1 is an invertible n×n matrix (since A has rank n), c ∈ Rn, and d ∈ Rm−n, and the least squares solution of smallest norm is
其中，R1是可逆n×n矩阵（因为a有秩n），c∈rn，d∈rm−n，最小范数的最小二乘解为
x+ = R1−1c.
X+=R1−1C。
Since R1 is a triangular matrix, it is very easy to invert R1.
因为R1是一个三角形矩阵，所以很容易将R1反转。
The method of least squares is one of the most effective tools of the mathematical sciences. There are entire books devoted to it. Readers are advised to consult Strang [165], Golub and Van Loan [80], Demmel [49], and Trefethen and Bau [171], where extensions and applications of least squares (such as weighted least squares and recursive least squares) are described. Golub and Van Loan [80] also contains a very extensive bibliography, including a list of books on least squares.
最小二乘法是数学科学中最有效的工具之一。有很多书都是专门为它写的。建议读者参考Strang[165]、Golub和van Loan[80]、Demmel[49]和Trefethen和Bau[171]，其中描述了最小二乘（如加权最小二乘和递归最小二乘）的扩展和应用。Golub和vanLoan[80]还包含了非常广泛的参考书目，包括关于最小二乘法的书籍列表。
21.2	Properties of the Pseudo-Inverse
21.2伪逆函数的性质
We begin this section with a proposition which provides a way to calculate the pseudo-inverse of an m × n matrix A without first determining an SVD factorization.
我们从一个命题开始，这个命题提供了一种计算m×n矩阵a的伪逆的方法，而不需要首先确定SVD分解。
Proposition 21.3. When A has full rank, the pseudo-inverse A+ can be expressed as A+ = (A>A)−1A> when m ≥ n, and as A+ = A>(AA>)−1 when n ≥ m. In the first case (m ≥ n), observe that A+A = I, so A+ is a left inverse of A; in the second case (n ≥ m), we have AA+ = I, so A+ is a right inverse of A.
提案21.3.当a具有满秩时，当m≥n时，伪逆a+可表示为a+=（a>a）−1a>，当n≥m时，伪逆a+可表示为a+=a>（aa>）−1。在第一种情况下（m≥n），观察a+a=i，因此a+是a的左逆；在第二种情况下（n≥m），我们有aa+=i，因此a+是a的右逆。
Proof. If m ≥ n and A has full rank n, we have
证据。如果m≥n且a具有满秩n，则我们有

with Λ an n × n diagonal invertible matrix (with positive entries), so
带有∧an n×n对角可逆矩阵（带正项），所以
We find that
我们发现了
,
，
which yields
会产生
.
.
Therefore, if m ≥ n and A has full rank n, then
因此，如果m≥n且a具有满秩n，则
A+ = (A>A)−1A>. If n ≥ m and A has full rank m, then
A+=（A>A）−1a>。如果n≥m且a具有满秩m，则

with Λ an m × m diagonal invertible matrix (with positive entries), so
带∧an m×m对角可逆矩阵（带正项），所以
We find that
我们发现了
,
，
which yields
会产生
.
.
Therefore, if n ≥ m and A has full rank m, then A+ = A>(AA>)−1.	
因此，如果n≥m且a具有满秩m，则a+=a>（aa>）-1。

21.2. PROPERTIES OF THE PSEUDO-INVERSE
21.2。伪逆的性质
For example, if, then A has rank 2 and since m ≥ n, A+ = (A>A)−1A>
例如，如果，那么a的等级为2，并且由于m≥n，a+=（a>a）−1a>
where
哪里
.
.
If, since A has rank 2 and n ≥ m, then A+ = A>(AA>)−1 where
如果，由于a的秩2和n≥m，则a+=a>（aa>）-1，其中
 .
.
Let A = V ΣU> be an SVD for any m × n matrix A. It is easy to check that both AA+ and A+A are symmetric matrices. In fact,
假设a=v∑u>是任意m×n矩阵a的SVD，很容易检查aa+和a+a都是对称矩阵。事实上，
and	
和
From the above expressions we immediately deduce that
从上面的表达式，我们立即推断
AA+A
网络错误	=
网络错误	A,
网络错误
A+AA+
网络错误
and that
网络错误	=
网络错误	A+,
网络错误
(AA+)2
网络错误	=
网络错误	AA+,
网络错误
(A+A)2
网络错误	=
网络错误	A+A,
网络错误
so both AA+ and A+A are orthogonal projections (since they are both symmetric).
所以a a+和a+都是正交投影（因为它们都是对称的）。
Proposition 21.4. The matrix AA+ is the orthogonal projection onto the range of A and A+A is the orthogonal projection onto Ker(A)⊥ = Im(A>), the range of A>.
提案21.4.矩阵a a+是a范围的正交投影，a+a是k（a）=im（a>）的正交投影，a>的范围。
Proof. Obviously, we have range(AA+) ⊆ range(A), and for any y = Ax ∈ range(A), since
证据。显然，我们有范围（a a+）范围（a），对于任何y=ax∈范围（a），因为
AA+A = A, we have
a a+a=a，我们有
AA+y = AA+Ax = Ax = y,
aa+y=aa+ax=ax=y，
so the image of AA+ is indeed the range of A. It is also clear that Ker(A) ⊆ Ker(A+A), and since AA+A = A, we also have Ker(A+A) ⊆ Ker(A), and so
所以a a+的图像实际上是a的范围，也很明显，ker（a）ker（a+a），由于aa+a=a，我们还有ker（a+a）ker（a），所以
Ker(A+A) = Ker(A).
ker（A+A）=ker（A）。
Since A+A is symmetric, range(A+A) = range((A+A)>) = Ker(A+A)⊥ = Ker(A)⊥, as claimed.	
由于a+a是对称的，范围（a+a）=range（（a+a）>）=ker（a+a）=ker（a），如权利要求所述。
Proposition 21.5. The set range(A) = range(AA+) consists of all vectors y ∈ Rm such that
提案21.5。集合范围（a）=range（aa+）由所有向量y∈rm组成，这样
 ,
，
with z ∈ Rr.
带z∈rr。
Proof. Indeed, if y = Ax, then
证据。实际上，如果y=ax，那么
 ,
，
where Σr is the r × r diagonal matrix diag(σ1,...,σr). Conversely, if ), then ), and
其中∑r是r×r对角矩阵diag（σ1，…，σr）。相反，如果），则），以及

which shows that y belongs to the range of A.	
这表明Y属于A的范围。
Similarly, we have the following result.
同样，我们得到了以下结果。
Proposition 21.6. The set range(A+A) = Ker(A)⊥ consists of all vectors y ∈ Rn such that
提案21.6.集合范围（a+a）=ker（a）由所有向量y∈rn组成，这样
,
，
with z ∈ Rr.
带z∈rr。
21.2. PROPERTIES OF THE PSEUDO-INVERSE
21.2。伪逆的性质
Proof. If y = A+Au, then
证据。如果y=a+au，那么
 ,
，
for some z ∈ Rr. Conversely, if), then), and so
对于某些z∈rr。相反，如果），则），依此类推。

which shows that y ∈ range(A+A).	
表示y∈范围（a+a）。
Analogous results hold for complex matrices, but in this case, V and U are unitary matrices and AA+ and A+A are Hermitian orthogonal projections.
类似的结果适用于复杂矩阵，但在这种情况下，v和u是一元矩阵，a a+和a+a是厄米特正交投影。
If A is a normal matrix, which means that AA> = A>A, then there is an intimate relationship between SVD’s of A and block diagonalizations of A. As a consequence, the pseudo-inverse of a normal matrix A can be obtained directly from a block diagonalization of A.
如果a是正态矩阵，即aa>=a>a，则a的svd与a的块对角化之间存在密切关系，因此，正态矩阵a的伪逆可以直接从a的块对角化得到。
If A is a (real) normal matrix, then we know from Theorem 16.18 that A can be block diagonalized with respect to an orthogonal matrix U as
如果a是（实数）正规矩阵，那么我们从定理16.18知道a可以对一个正交矩阵u进行分块对角化，作为
A = UΛU>,
A=U∧U>，
where Λ is the (real) block diagonal matrix
其中∧是（实数）块对角矩阵
Λ = diag(B1,...,Bn),
∧=diag（b1，…，bn）
consisting either of 2 × 2 blocks of the form
由2×2块模板组成

with µj = 06	, or of one-dimensional blocks Bk = (λk). Then we have the following proposition:
μj=06，或一维块bk=（λk）。然后我们有以下建议：
Proposition 21.7. For any (real) normal matrix A and any block diagonalization A = UΛU> of A as above, the pseudo-inverse of A is given by
提案21.7.对于任何（实）法向矩阵A和任何块对角化a=u∧u>如上所述，a的伪逆由下式给出：
A+ = UΛ+U>,
A+=U∧+U>，
where Λ+ is the pseudo-inverse of Λ. Furthermore, if
其中∧+是∧的伪逆。此外，如果
 ,
，
where Λr has rank r, then
式中，∧r的秩为r，则
 .
.
Proof. Assume that B1,...,Bp are 2×2 blocks and that λ2p+1,...,λn are the scalar entries. We know that the numbers λj ± iµj, and the λ2p+k are the eigenvalues of A. Let ρ2j−1 =
证据。假设b1，…，bp是2×2块，而λ2p+1，…，λn是标量项。我们知道，数字λj±iμj和λ2p+k是a的特征值，设为ρ2j−1。=

ρ2j = qλ2j + µj2 = pdet(Bi) for j = 1,...,p, ρj = |λj| for j = 2p + 1,...,r. Multiplying U by a suitable permutation matrix, we may assume that the blocks of Λ are ordered so that ρ1 ≥ ρ2 ≥ ··· ≥ ρr > 0. Then it is easy to see that
对于j=1，…，p，ρj=λj对于j=2p+1，…，r，？2j=qλ2j+μj2=pdet（bi）。将u乘以适当的置换矩阵，我们可以假定∧的块是有序的，因此，ρ1≥ρ2≥·····························那么很容易看出
AA> = A>A = UΛU>UΛ>U> = UΛΛ>U>,
a a>=a>a=u∧u>u∧>u>=u∧∧>u>，
with
具有
ΛΛ> = diag(,
∧∧>=诊断（，
so ρ1 ≥ ρ2 ≥ ··· ≥ ρr > 0 are the singular values σ1 ≥ σ2 ≥ ··· ≥ σr > 0 of A. Define the diagonal matrix
因此，ρ1≥ρ2≥············································
Σ = diag(σ1,...,σr,0,...,0),
∑=diag（σ1，…，σr，0，…，0）、
where r = rank(A), σ1 ≥ ··· ≥ σr > 0 and the block diagonal matrix Θ defined such that
式中，r=秩（a），σ1≥·································
the block Bi in Λ is replaced by the block σ−1Bi where σ = pdet(Bi), the nonzero scalar λj is replaced λj/|λj|, and a diagonal zero is replaced by 1. Observe that Θ is an orthogonal matrix and
将∧中的块bi替换为块σ−1bi，其中σ=pdet（bi），将非零标量λj替换为λj/λj，将对角零替换为1。观察到θ是一个正交矩阵
Λ = ΘΣ.
∧=完成∑。
But then we can write
但是我们可以写
A = UΛU> = UΘΣU>,
A=U∧U>=U完成∑U>，
and we if let V = UΘ, since U is orthogonal and Θ is also orthogonal, V is also orthogonal and A = V ΣU> is an SVD for A. Now we get
如果我们让v=u，因为u是正交的，而θ也是正交的，v也是正交的，a=v∑u>是a的svd，现在我们得到
A+ = UΣ+V > = UΣ+Θ>U>.
A+=U∑+V>=U∑+成人>U>。
However, since Θ is an orthogonal matrix, Θ> = Θ−1, and a simple calculation shows that
然而，由于θ是一个正交矩阵，所以θ>=θ-1，简单的计算表明
Σ+Θ> = Σ+Θ−1 = Λ+,
∑+完成>=∑+完成−1=∧+，
which yields the formula
得出公式
A+ = UΛ+U>.
A+=U∧+U>。
Also observe that Λr is invertible and
也注意到∧r是可逆的，并且
 .
.
Therefore, the pseudo-inverse of a normal matrix can be computed directly from any block diagonalization of A, as claimed.	
因此，正态矩阵的伪逆矩阵可以直接从A的任何块对角化中计算出来，如所述。
21.3. DATA COMPRESSION AND SVD
21.3。数据压缩和SVD
Example 21.3. Consider the following real diagonal form of the normal matrix
例21.3。考虑下正规矩阵的实对角形式
,
，
with
具有
 .
.
We obtain
我们得到
 ,
，
and the pseudo-inverse of A is
A的伪逆是
 ,
，
which agrees with pinv(A).
与PINv（a）一致。
The following properties, due to Penrose, characterize the pseudo-inverse of a matrix. We have already proved that the pseudo-inverse satisfies these equations. For a proof of the converse, see Kincaid and Cheney [100].
由于Penrose的原因，以下特性描述了矩阵的伪逆矩阵。我们已经证明了伪逆满足这些方程。关于相反的证明，见Kincaid和Cheney[100]。
Proposition 21.8. Given any m × n matrix A (real or complex), the pseudo-inverse A+ of A is the unique n × m matrix satisfying the following properties:
提案21.8。对于任意m×n矩阵a（实矩阵或复矩阵），a的伪逆a+是满足以下特性的唯一n×m矩阵：
AA+A = A,
a a+a=a，
A+AA+ = A+,
A+AA+=A+，
(AA+)> = AA+, (A+A)> = A+A.
（a a+）>=aa+，（a+a）>=a+a。
21.3	Data Compression and SVD
21.3数据压缩和SVD
Among the many applications of SVD, a very useful one is data compression, notably for images. In order to make precise the notion of closeness of matrices, we use the notion of matrix norm. This concept is defined in Chapter 8, and the reader may want to review it before reading any further.
在SVD的众多应用中，一个非常有用的应用是数据压缩，尤其是图像压缩。为了使矩阵的紧密性概念更加精确，我们使用了矩阵范数的概念。这一概念在第8章中有定义，读者可能想在进一步阅读之前回顾一下。
Given an m × n matrix of rank r, we would like to find a best approximation of A by a matrix B of rank k ≤ r (actually, k < r) such that kA − Bk2 (or kA − BkF ) is minimized. The following proposition is known as the Eckart–Young theorem.
给定秩r的m×n矩阵，我们希望通过秩k≤r的矩阵b（实际上，k<r）找到a的最佳近似值，从而使ka−bk2（或ka−bkf）最小化。下面的命题被称为Eckart-Young定理。
Proposition 21.9. Let A be an m × n matrix of rank r and let V DU> = A be an SVD for A. Write ui for the columns of U, vi for the columns of V , and σ1 ≥ σ2 ≥ ··· ≥ σp for the singular values of A (p = min(m,n)). Then a matrix of rank k < r closest to A (in the k k2 norm) is given by
提案21.9.设a为秩r的m×n矩阵，v du>=a为a的svd，写出u列的ui，v列的vi，σ1≥σ2≥·······································然后，最接近a（k k2范数）的秩k<r矩阵由下式得出：
diag(σ1,...,σk,0,...,0)U>
diag（σ1，…，σk，0，…，0）u>
and kA − Akk2 = σk+1.
kA−akk2=σk+1。
Proof. By construction, Ak has rank k, and we have
证据。根据结构，AK的等级是K，我们有
p diag(0.
P诊断（0.
= +1
= 1
It remains to show that kA − Bk2 ≥ σk+1 for all rank k matrices B. Let B be any rank k matrix, so its kernel has dimension n−k. The subspace Uk+1 spanned by (u1,...,uk+1) has dimension k + 1, and because the sum of the dimensions of the kernel of B and of Uk+1 is (n − k) + k + 1 = n + 1, these two subspaces must intersect in a subspace of dimension at least 1. Pick any unit vector h in Ker(B) ∩ Uk+1. Then since Bh = 0, and since U and V are isometries, we have
仍然需要证明所有秩k矩阵b的ka−bk2≥σk+1。假设b是任何秩k矩阵，那么它的核具有维数n−k。由（u1，…，uk+1）所跨越的子空间uk+1具有维数k+1，并且因为b和uk+1的核的维数之和是（n−k）+k+1=n+1，t这两个子空间必须在维度至少为1的子空间中相交。选取Ker（b）UK+1中的任何单位向量h。既然bh=0，既然u和v是等距的，我们有
,
，
which proves our claim.	
这证明了我们的主张。
Note that Ak can be stored using (m + n)k entries, as opposed to mn entries. When , this is a substantial gain.
请注意，AK可以使用（m+n）k项存储，而不是使用mn项。当，这是一个巨大的收益。
Example 21.4. Consider the badly conditioned symmetric matrix
例21.4。考虑坏条件对称矩阵

from Section 8.5. Since A is SPD, we have the SVD
来自第8.5节。既然A是SPD，我们有SVD
A = UDU>,
A=Udu>，

with
具有
 .
.
If we set σ3 = σ4 = 0, we obtain the best rank 2 approximation
如果我们将σ3=σ4=0，我们得到最佳秩2近似值。
 .
.
A nice example of the use of Proposition 21.9 in image compression is given in Demmel [49], Chapter 3, Section 3.2.3, pages 113–115; see the Matlab demo.
demmel[49]第3章第3.2.3节第113-115页给出了在图像压缩中使用21.9号提案的一个很好的例子；见matlab演示。
Proposition 21.9 also holds for the Frobenius norm; see Problem 21.4.
提案21.9也适用于弗罗贝尼乌斯规范；见问题21.4。
An interesting topic that we have not addressed is the actual computation of an SVD. This is a very interesting but tricky subject. Most methods reduce the computation of an SVD to the diagonalization of a well-chosen symmetric matrix which is not A>A; see Problem 20.1 and Problem 20.3. Interested readers should read Section 5.4 of Demmel’s excellent book [49], which contains an overview of most known methods and an extensive list of references.
一个有趣的话题我们还没有讨论，那就是SVD的实际计算。这是一个很有趣但很棘手的问题。大多数方法都将SVD的计算简化为选定的对称矩阵的对角化，该对称矩阵不是a>a；见问题20.1和问题20.3。感兴趣的读者应该阅读德梅尔优秀著作[49]的第5.4节，其中包括最著名的方法概述和大量参考文献。
21.4	Principal Components Analysis (PCA)
21.4主要成分分析（PCA）
Suppose we have a set of data consisting of n points X1,...,Xn, with each Xi ∈ Rd viewed as a row vector. Think of the Xi’s as persons, and if Xi = (xi1,...,xid), each xij is the value of some feature (or attribute) of that person.
假设我们有一组由N点X1，…，Xn组成的数据，每个Xi RD被看作行向量。把XI看成是人，如果X=（XI1，…，XID），每个XIJ都是那个人的某些特征（或属性）的值。
Example 21.5. For example, the Xi’s could be mathematicians, d = 2, and the first component, xi1, of Xi could be the year that Xi was born, and the second component, xi2, the length of the beard of Xi in centimeters. Here is a small data set:
例21.5。例如，XI可以是数学家，D＝2，XI的第一个组成部分XI1可以是XI出生的一年，第二个组成部分XI2是XI的胡须长度厘米。下面是一个小数据集：
Name
网络错误	year
网络错误	length
网络错误
Carl Friedrich Gauss
网络错误	1777
网络错误	0
网络错误
Camille Jordan
网络错误	1838
网络错误	12
网络错误
Adrien-Marie Legendre
网络错误	1752
网络错误	0
网络错误
Bernhard Riemann
网络错误	1826
网络错误	15
网络错误
David Hilbert
网络错误	1862
网络错误	2
网络错误
Henri Poincar´e
网络错误	1854
网络错误	5
网络错误
Emmy Noether
网络错误	1882
网络错误	0
网络错误
Karl Weierstrass
网络错误	1815
网络错误	0
网络错误
Eugenio Beltrami
网络错误	1835
网络错误	2
网络错误
Hermann Schwarz
网络错误	1843
网络错误	20
网络错误
We usually form the n × d matrix X whose ith row is Xi, with 1 ≤ i ≤ n. Then the jth column is denoted by Cj (1 ≤ j ≤ d). It is sometimes called a feature vector, but this terminology is far from being universally accepted. In fact, many people in computer vision call the data points Xi feature vectors!
我们通常形成n×d矩阵x，其行是Xi，1的i i小于n，然后用Cj（1×j j）表示JTH列。它有时被称为特征向量，但这个术语远未被普遍接受。其实很多人在计算机视觉上调用了数据点XI的特征向量！
The purpose of principal components analysis, for short PCA, is to identify patterns in data and understand the variance–covariance structure of the data. This is useful for the following tasks:
主成分分析（简称PCA）的目的是识别数据模式，了解数据的方差-协方差结构。这对以下任务很有用：
1.	Data reduction: Often much of the variabi lity of the data can be accounted for by a smaller number of principal components.
数据简化：通常，数据的许多变量都可以由较少的主成分来解释。
2.	Interpretation: PCA can show relationships that were not previously suspected.
解释：PCA可以显示以前没有被怀疑的关系。
Given a vector (a sample of measurements) x = (x1,...,xn) ∈ Rn, recall that the mean (or average) x of x is given by
给定一个向量（测量样本）x=（x1，…，xn）∈rn，回想一下x的平均值（或平均值）x由
.
.
We let x − x denote the centered data point
我们让x-x表示中心数据点。
x − x = (x1 − x,...,xn − x).
x−x=（x1−x，…，xn−x）。
In order to measure the spread of the xi’s around the mean, we define the sample variance (for short, variance) var(x) (or s2) of the sample x by
为了测量XI在平均值附近的传播，我们定义了样本X的样本方差（简称为方差）VaR（x）（或S2）。
	Example 21.6. If	2), and var(x) =
例21.6。如果2）和var（x）=
	1), and var(
1）和var（
2.
2。
There is a reason for using n − 1 instead of n. The above definition makes var(x) an unbiased estimator of the variance of the random variable being sampled. However, we don’t need to worry about this. Curious readers will find an explanation of these peculiar definitions in Epstein [58] (Chapter 14, Section 14.5) or in any decent statistics book.
使用n−1而不是n是有原因的。上述定义使var（x）成为被采样随机变量方差的无偏估计量。不过，我们不必为此担心。好奇的读者会在爱泼斯坦[58]中（第14章，第14.5节）或任何像样的统计书中找到对这些特殊定义的解释。
Given two vectors x = (x1,...,xn) and y = (y1,...,yn), the sample covariance (for short, covariance) of x and y is given by
给定两个向量x=（x1，…，xn）和y=（y1，…，yn），x和y的样本协方差（简称协方差）由下式给出：
cov(.
冠状病毒
Example 21.7. If we take x = (1,3,−1) and y = (0,2,−2), we know from Example 21.6 that x − x = (0,2,−2) and y − y = (−1,0,1). Thus, cov(x,y) = 0(−1)+2(0)+(2 −2)(1) = −1.
例21.7。如果我们取x=（1,3、-1）和y=（0,2、-2），我们从例21.6中知道x−x=（0,2、-2）和y−y=（-1,0,1）。因此，cov（x，y）=0（−1）+2（0）+（2−2）（1）=1。
The covariance of x and y measures how x and y vary from the mean with respect to each other. Obviously, cov(x,y) = cov(y,x) and cov(x,x) = var(x).
x和y的协方差度量x和y在平均值上的差异。显然，cov（x，y）=cov（y，x）和cov（x，x）=var（x）。
Note that
注意
cov(.
冠状病毒
We say that x and y are uncorrelated iff cov(x,y) = 0.
我们说x和y是不相关的，iff cov（x，y）=0。
Finally, given an n × d matrix X of n points Xi, for PCA to be meaningful, it will be necessary to translate the origin to the centroid (or center of gravity) µ of the Xi’s, defined by
最后，给定n点x的n×d矩阵x，对于PCA是有意义的，有必要将原点翻译成Xi的质心（或重心），由
.
.
Observe that if µ = (µ1,...,µd), then µj is the mean of the vector Cj (the jth column of X).
观察，如果μ=（μ1，…，μd），则μj是矢量Cj（x的jth列）的平均值。
We let X − µ denote the matrix whose ith row is the centered data point Xi − µ (1 ≤ i ≤ n). Then the sample covariance matrix (for short, covariance matrix) of X is the d × d symmetric matrix
我们以X为表示矩阵为Iz行为中心的数据点Xi（1）那么x的样本协方差矩阵（简称协方差矩阵）就是d×d对称矩阵。
.
.
Example 21.8. Let, the 3 × 2 matrix whose columns are the vector x and −
例21.8。设3×2矩阵，其列为矢量x和−
y of Example 21.6. Then
例21.6的y。然后
,
，
and
和
.
.
Remark: The factor is irrelevant for our purposes and can be ignored.
备注：该因素与我们的目的无关，可以忽略不计。
Example 21.9. Here is the matrix X −µ in the case of our bearded mathematicians: since
例21.9。下面是我们的胡须数学家的矩阵x−μ：因为
	µ1 = 1828.4,	µ2 = 5.6,
礹1=1828.4，礹2=5.6，
we get
我们得到
Name
	网络错误	year
	网络错误	length
网络错误
Carl Friedrich Gauss
	网络错误	−51.4
	网络错误	−5.6
网络错误
Camille Jordan
	网络错误	9.6
	网络错误	6.4
网络错误
Adrien-Marie Legendre
	网络错误	−76.4
	网络错误	−5.6
网络错误
Bernhard Riemann
	网络错误	−2.4
	网络错误	9.4
网络错误
David Hilbert
	网络错误	33.6
	网络错误	−3.6
网络错误
Henri Poincar´e
	网络错误	25.6
	网络错误	−0.6
网络错误
Emmy Noether
	网络错误	53.6
	网络错误	−5.6
网络错误
Karl Weierstrass
	网络错误	13.4
	网络错误	−5.6
网络错误
Eugenio Beltrami
	网络错误	6.6
	网络错误	−3.6
网络错误
Hermann Schwarz
	网络错误	14.6
	网络错误	14.4
网络错误
See Figure 21.3.
见图21.3。
We can think of the vector Cj as representing the features of X in the direction ej (the jth canonical basis vector in Rd, namely ej = (0,...,1,...0), with a 1 in the jth position).
我们可以把矢量Cj看作是表示x在ej方向上的特征（rd中的jth规范基矢量，即ej=（0，…，1，…，0），其中1在jth位置）。
If v ∈ Rd is a unit vector, we wish to consider the projection of the data points X1,...,Xn onto the line spanned by v. Recall from Euclidean geometry that if x ∈ Rd is any vector and v ∈ Rd is a unit vector, the projection of x onto the line spanned by v is hx,viv.
如果v∈rd是单位向量，我们希望考虑数据点x1，…，xn在v所跨越的直线上的投影。从欧几里德几何中回忆，如果x∈rd是任何向量，v∈rd是单位向量，x在v所跨越的直线上的投影是hx，viv。
Thus, with respect to the basis v, the projection of x has coordinate hx,vi. If x is represented by a row vector and v by a column vector, then
因此，对于基V，x的投影具有坐标hx，vi。如果x由行向量表示，v由列向量表示，那么
hx,vi = xv.
hx，vi=xv。

Figure 21.3: The centered data points of Example 21.9.
图21.3：示例21.9的中心数据点。
Therefore, the vector Y ∈ Rn consisting of the coordinates of the projections of X1,...,Xn onto the line spanned by v is given by Y = Xv, and this is the linear combination
因此，由x1，…，xn的投影坐标构成的向量y∈rn在V所跨越的线上，由y=xv给出，这是线性组合。
Xv = v1C1 + ··· + vdCd
xv=v1c1+·····+vdcd
of the columns of X (with v = (v1,...,vd)).
x列（v=（v1，…，vd））。
Observe that because µj is the mean of the vector Cj (the jth column of X), we get
观察到，由于μj是矢量cj（x的jth列）的平均值，我们得到
Y = Xv = v1µ1 + ··· + vdµd,
y=xv=v1祄1+····+vd祄d，
and so the centered point Y − Y is given by
因此中心点y−y由

Y − Y = v1(C1 − µ1) + ··· + vd(Cd − µd) = (X − µ)v.
Y−Y=v1（c1−μ1）+·····+v d（cd−μd）=（x−μ）V。
Furthermore, if Y = Xv and Z = Xw, then
此外，如果y=xv，z=xw，那么
cov(
冠状病毒

where Σ is the covariance matrix of X. Since Y − Y has zero mean, we have
其中∑是x的协方差矩阵。由于y−y的均值为零，我们得到

The above suggests that we should move the origin to the centroid µ of the Xi’s and consider the matrix X − µ of the centered data points Xi − µ.
这意味着我们应该把原点移动到Xi的质心上，并考虑中心数据点Xi的矩阵X。
From now on beware that we denote the columns of X − µ by C1,...,Cd and that Y denotes the centered point  is a unit vector.
从现在开始要注意，我们用c1，…，cd表示x-，y表示中心点是单位向量。
Basic idea of PCA: The principal components of X are uncorrelated projections Y of the data points X1, ..., Xn onto some directions v (where the v’s are unit vectors) such that var(Y ) is maximal.
主成分分析的基本思想：x的主要成分是数据点x1，…，xn的不相关投影y到一些方向v（其中v是单位向量），使得var（y）最大。
This suggests the following definition:
这表明了以下定义：
Definition 21.2. Given an n×d matrix X of data points X1,...,Xn, if µ is the centroid of the Xi’s, then a first principal component of X (first PC) is a centered point Y1 = (X−µ)v1, the projection of X1,...,Xn onto a direction v1 such that var(Y1) is maximized, where v1 is a unit vector (recall that Y1 = (X − µ)v1 is a linear combination of the Cj’s, the columns of X − µ).
定义21.2.给定数据点X1，…，Xn的N×D矩阵X，如果X是XI的质心，那么X（第一PC）的第一主分量是中心点Y1=（xω）V1，X1，…，Xn投影到方向V1，使得VAR（Y1）被最大化，其中V1是单位向量（回忆Y1＝（x）。-μ）v1是Cj的线性组合，x-μ的柱）。
More generally, if Y1,...,Yk are k principal components of X along some unit vectors v1,...,vk, where 1 ≤ k < d, a (k+1)th principal component of X ((k+1)th PC) is a centered point Yk+1 = (X − µ)vk+1, the projection of X1,...,Xn onto some direction vk+1 such that var(Yk+1) is maximized, subject to cov(Yh,Yk+1) = 0 for all h with 1 ≤ h ≤ k, and where vk+1 is a unit vector (recall that Yh = (X − µ)vh is a linear combination of the Cj’s). The vh are called principal directions.
更一般地说，如果y1，…，yk是x的k主分量，沿着一些单位向量v1，…，vk，其中1≤k<d，x的a（k+1）th主分量（（k+1）th pc）是一个中心点yk+1=（x-μ）vk+1，x1，…，xn在某个方向上的投影vk+1，这样var（yk+1）最大化，subject to cov（yh，yk+1）=0，对于1≤h≤k的所有h，其中vk+1是单位矢量（回想一下，yh=（x−µ）vh是cj的线性组合）。VH被称为主方向。
The following proposition is the key to the main result about PCA. This result was already proven in Proposition 16.23 except that the eigenvalues were listed in increasing order. For the reader’s convenience we prove it again.
下面的命题是主成分分析主要结果的关键。这一结果已经在命题16.23中得到证明，只是特征值是按递增顺序列出的。为了读者的方便，我们再次证明了这一点。
Proposition 21.10. If A is a symmetric d × d matrix with eigenvalues λ1 ≥ λ2 ≥ ··· ≥ λd and if (u1,...,ud) is any orthonormal basis of eigenvectors of A, where ui is a unit eigenvector associated with λi, then
提案21.10。如果a是特征值λ1≥λ2≥·····················································

(with the maximum attained for x = u1) and
（X=U1时达到最大值）和

(with the maximum attained for x = uk+1), where 1 ≤ k ≤ d − 1.
（X=UK+1时达到最大值），其中1≤K≤D−1。
Proof. First observe that
证据。首先要注意
,
，
and similarly,
同样地，
.
.
Since A is a symmetric matrix, its eigenvalues are real and it can be diagonalized with respect to an orthonormal basis of eigenvectors, so let (u1,...,ud) be such a basis. If we write
由于A是一个对称矩阵，其特征值是实的，它可以相对于特征向量的正态基对角化，因此（u1，…，ud）就是这样的基。如果我们写信
,
，
a simple computation shows that
简单的计算表明
d x>Ax = Xλix2i .
d x>ax=xλix2i。
i=1
i＝1
If x>x = 1, then	= 1, and since we assumed that λ1 ≥ λ2 ≥ ··· ≥ λd, we get
如果x>x=1，则=1，由于我们假设λ1≥λ2≥·································
.
.
Thus,
因此，
,
，
and since this maximum is achieved for e1 = (1,0,...,0), we conclude that
由于e1（1,0，…，0）达到了这个最大值，我们得出结论
.
.
Next observe that x ∈ {u1,...,uk}⊥ and x>x = 1 iff x1 = ··· = xk = 0 and
接下来观察x∈u1，…，uk和x>x=1 iff x1=····=xk=0和
Consequently, for such an x, we have
因此，对于这样一个x，我们有
.
.
Thus,
因此，
,
，
and since this maximum is achieved for ek+1 = (0,...,0,1,0,...,0) with a 1 in position k+1, we conclude that
由于Ek+1的最大值为（0，…，0,1,0，…，0），位置k+1为1，我们得出结论：
,
，
as claimed.	
如要求。
The quantity
数量

is known as the Rayleigh ratio or Rayleigh–Ritz ratio (see Section 16.6 ) and Proposition 21.10 is often known as part of the Rayleigh–Ritz theorem.
被称为瑞利比或瑞利-瑞兹比（见第16.6节），而21.10命题通常被称为瑞利-瑞兹定理的一部分。
Proposition 21.10 also holds if A is a Hermitian matrix and if we replace x>Ax by x∗Ax and x>x by x∗x. The proof is unchanged, since a Hermitian matrix has real eigenvalues and is diagonalized with respect to an orthonormal basis of eigenvectors (with respect to the Hermitian inner product).
命题21.10也适用于如果a是厄米特矩阵，并且如果我们用x ax替换x>ax，x>x替换x x，则证明是不变的，因为厄米特矩阵具有实际特征值，并且相对于特征向量的正交基（关于厄米特内积）对角化。
We then have the following fundamental result showing how the SVD of X yields the PCs:
然后，我们将得到以下基本结果，说明X的SVD如何生成PC：
Theorem 21.11. (SVD yields PCA) Let X be an n × d matrix of data points X1,...,Xn, and let µ be the centroid of the Xi’s. If X − µ = V DU> is an SVD decomposition of X − µ and if the main diagonal of D consists of the singular values σ1 ≥ σ2 ≥ ··· ≥ σd, then the centered points Y1,...,Yd, where
定理21.11。（SVD产生PCA），X为数据点X1，…，Xn的N×D矩阵，并设为Xi的质心。如果X＝＝V DU>是X×SVD的SVD分解，如果D的主对角线由奇异值α1×2以上的±·ω-δD组成，则中心点Y1，…，YD，WH。埃尔
Yk = (X − µ)uk = kth column of V D
yk=（x−μ）uk=v d的第k列
and uk is the kth column of U, are d principal components of X. Furthermore,
Uk是u的第k列，是x的d个主要成分。

and cov(Yh,Yk) = 0, whenever h =6	k and 1 ≤ k,h ≤ d.
而cov（yh，yk）=0，当h=6 k且1≤k时，h≤d。
Proof. Recall that for any unit vector v, the centered projection of the points X1,...,Xn onto the line of direction v is Y = (X − µ)v and that the variance of Y is given by
证据。回想一下，对于任何单位向量v，点x1，…，xn在方向v的直线上的中心投影是y=（x-μ）v，y的方差由下式得出：

Since X − µ = V DU>, we get
由于x−μ=v du>，我们得到

Similarly, if Y = (X − µ)v and Z = (X − µ)w, then the covariance of Y and Z is given by
同样，如果y=（x−μ）v和z=（x−μ）w，则y和z的协方差由下式得出：
cov(
冠状病毒
the columns ofObviously, U (n−1U1)Dform an orthonormal basis of unit eigenvectors.2U> is a symmetric matrix whose eigenvalues are , and
实际上，u（n−1u1）数据列构成单位特征向量的正态基。2u>是一个对称矩阵，其特征值为，和
We proceed by induction on k. For the base case, k = 1, maximizing var(Y ) is equivalent to maximizing
我们对k进行归纳。对于基本情况，k=1，最大化var（y）等于最大化

where v is a unit vector. By Proposition 21.10, the maximum of the above quantity is the largest eigenvalue of, namely, and it is achieved for u1, the first columnn of U. Now we get
其中v是单位向量。由命题21.10可知，上述数量的最大值是最大特征值，即，对于u的第一列u1，我们得到
Y1 = (X − µ)u1 = V DU>u1,
y1=（x−µ）u1=v du>u1，
and since the columns of U form an orthonormal basis, U>u1 = e1 = (1,0,...,0), and so Y1 is indeed the first column of V D.
由于u的列构成正交基，u>u1=e1=（1,0，…，0），所以y1确实是v d的第一列。
By the induction hypothesis, the centered points Y1,...,Yk, where Yh = (X − µ)uh and u1,...,uk are the first k columns of U, are k principal components of X. Because
根据诱导假设，中心点y1，…，yk，其中yh=（x−µ）uh和u1，…，u k是u的前k列，是x的k主要成分。因为
cov(
冠状病毒
where Y = (X − µ)v and Z = (X − µ)w, the condition cov(Yh,Z) = 0 for h = 1,...,k is equivalent to the fact that w belongs to the orthogonal complement of the subspace spanned by {u1,...,uk}, and maximizing var(Z) subject to cov(Yh,Z) = 0 for h = 1,...,k is equivalent to maximizing
式中，y=（x−μ）v和z=（x−μ）w，条件cov（y h，z）=0，对于h=1，…，k等于w属于由u1，…，uk所跨越的子空间的正交补集，并且服从cov（yh，z）=0，对于h=1，…，k等于最大化。

where w is a unit vector orthogonal to the subspace spanned by {u1,...,uk}. By Proposition
其中w是一个与子空间正交的单位向量，其范围为u1，…，uk。按命题
21.10, the maximum of the above quantity is the (k+1)th eigenvalue of, namely
21.10，上述数量的最大值为（k+1）的第（k+1）个特征值，即
, and it is achieved for uk+1, the (k + 1)th columnn of U. Now we get
它是为英国+1，美国的第（k+1）列而实现的。
Yk+1 = (X − µ)uk+1 = V DU>uk+1,
YK+1=（x−µ）UK+1=V du>UK+1，
and since the columns of U form an orthonormal basis, U>uk+1 = ek+1, and Yk+1 is indeed the (k + 1)th column of V D, which completes the proof of the induction step. 
由于u列构成正交基，u>u k+1=ek+1，yk+1确实是v d的（k+1）第（k+1）列，完成了诱导步骤的证明。
The d columns u1,...,ud of U are usually called the principal directions of X − µ (and X). We note that not only do we have cov(Yh,Yk) = 0 whenever h =6 k, but the directions u1,...,ud along which the data are projected are mutually orthogonal.
u的d列u1，…，ud通常称为x−礹（和x）的主方向。我们注意到，不仅当h=6K时，cov（yh，yk）=0，而且数据投影的方向u1，…，ud是相互正交的。
Example 21.10. For the centered data set of our bearded mathematicians (Example 21.9) we have X − µ = V ΣU>, where Σ has two nonzero singular values, σ1 = 116.9803,σ2 = 21.7812, and with
例21.10。对于胡须数学家的中心数据集（例21.9），我们有x−µ=v∑u>，其中∑有两个非零奇异值，σ1=116.9803，σ2=21.7812，以及
 ,
，
so the principal directions are u1 = (0.9995,0.0325) and u2 = (0.0325,−0.9995). Observe that u1 is almost the direction of the x-axis, and u2 is almost the opposite direction of the y-axis. We also find that the projections Y1 and Y2 along the principal directions are
所以主方向是U1=（0.9995,0.0325）和U2=（0.0325，−0.9995）。观察u1几乎是x轴的方向，u2几乎是y轴的相反方向。我们还发现沿着主方向的投影y1和y2是
−51.5550
网络错误
 9.8031 −76.5417
网络错误

网络错误
 −2.0929
网络错误

网络错误
 33.4651 V D =  25.5669
网络错误

网络错误

网络错误
 53.3894
网络错误

网络错误
 13.2107
网络错误

网络错误
 6.4794
网络错误
15.0607
网络错误	3.9249 
网络错误
−6.0843 
网络错误
3.1116 
网络错误
−9.4731 
网络错误
4.6912 ,
网络错误
1.4325  7.3408 
网络错误
6.0330 
网络错误
3.8128  −13.9174
网络错误	with
网络错误	−51.4000
网络错误
 9.6000 −76.4000
网络错误

网络错误
 −2.4000
网络错误

网络错误
 33.6000
网络错误
Xµ =  25.6000
网络错误

网络错误

网络错误
 53.6000
网络错误

网络错误
 13.4000
网络错误

网络错误
 6.6000
网络错误
14.6000
网络错误	−5.6000
网络错误
6.4000 
网络错误
−5.6000
网络错误
9.4000  −3.6000. −0.6000
网络错误
−5.6000
网络错误
−5.6000
网络错误
−3.6000
网络错误
14.4000
网络错误
See Figures 21.4, 21.5, and 21.6.
网络错误			

Figure 21.4: The centered data points of Example 21.9 and the two principal directions of Example 21.10.
图21.4：实施例21.9的中心数据点和实施例21.10的两个主要方向。
We know from our study of SVD that are the eigenvalues of the symmetric positive semidefinite matrix (X − µ)>(X − µ) and that u1,...,ud are corresponding eigenvectors. Numerically, it is preferable to use SVD on X −µ rather than to compute explicitly (Xµ) and then diagonalize it. Indeed, the explicit computation of A>A from a matrix can be numerically quite unstable, and good SVD algorithms avoid computing A>A explicitly.
我们从对SVD的研究中知道，对称半正定矩阵（x−礹）>（x−礹）的特征值和u1，…，ud是相应的特征向量。在数值上，最好在x−μ上使用SVD，而不是显式计算（xμ），然后对其进行对角线化。事实上，从矩阵中显式计算a>a可能在数值上相当不稳定，并且良好的SVD算法避免显式计算a>a。

Figure 21.5: The first principal components of Example 21.10, i.e. the projection of the centered data points onto the u1 line.
图21.5：实施例21.10的第一个主要组成部分，即中心数据点在U1线上的投影。

Figure 21.6: The second principal components of Example 21.10, i.e. the projection of the centered data points onto the u2 line.
图21.6：实施例21.10的第二个主要组成部分，即中心数据点在U2线上的投影。
In general, since an SVD of X is not unique, the principal directions u1,...,ud are not unique. This can happen when a data set has some rotational symmetries, and in such a case, PCA is not a very good method for analyzing the data set.
一般来说，由于x的svd不是唯一的，所以主方向u1，…，ud不是唯一的。当数据集具有某些旋转对称性时，就会发生这种情况，在这种情况下，PCA不是一种很好的数据集分析方法。
21.5	Best Affine Approximation
21.5最佳仿射近似
A problem very close to PCA (and based on least squares) is to best approximate a data set of n points X1,...,Xn, with Xi ∈ Rd, by a p-dimensional affine subspace A of Rd, with 1 ≤ p ≤ d − 1 (the terminology rank d − p is also used).
一个非常接近PCA的问题（和基于最小二乘法）是最好地逼近一个N点X1，…，Xn的数据集，用X-RD，用RD的p维仿射子空间A，用1个±p＝D 1（术语等级D P）也使用。
First consider p = d−1. Then A = A1 is an affine hyperplane (in Rd), and it is given by an equation of the form
首先考虑P=D-1。那么a=a1是仿射超平面（在rd中），它由形式方程给出。
a1x1 + ··· + adxd + c = 0.
A1x1+·····+ADxd+c=0.
By best approximation, we mean that (a1,...,ad,c) solves the homogeneous linear system
通过最佳逼近，我们的意思是（a1，…，ad，c）解齐次线性系统。

in the least squares sense, subject to the condition that a = (a1,...,ad) is a unit vector, that is, a>a = 1, where Xi = (xi1,··· ,xid). If we form the symmetric matrix
在最小二乘意义上，服从A=（A1，…，AD）是单位向量的条件，即A＞A＝1，其中X=（XI1，FAY·，XID）。如果我们形成对称矩阵
	x11	···	> x11	···	x1d	1
x11········································
	x1d	1
X1D 1
.
.
	 ..	...	...	...  ...	...	...	...
………………………………………………
	xn1	···	xnd	1	xn1	···	xnd	1
xn1···xnd 1 xn1···xnd 1
involved in the normal equations, we see that the bottom row (and last column) of that matrix is
在正规方程中，我们看到矩阵的最下面一行（和最后一列）是
	nµ1	···	nµd	n,
n礹1···n礹d n，
where times the mean of the column Cj of X.
其中乘以x的cj列的平均值。
Therefore, if (a1,...,ad,c) is a least squares solution, that is, a solution of the normal equations, we must have
因此，如果（a1，…，ad，c）是一个最小二乘解，也就是说，一个正态方程的解，我们必须
nµ1a1 + ··· + nµdad + nc = 0,
n礹a1+·····+n礹dad+nc=0，
that is, a1µ1 + ··· + adµd + c = 0,
也就是说，A1礹1+·····+AD礹d+C=0，
which means that the hyperplane A1 must pass through the centroid µ of the data points X1,...,Xn. Then we can rewrite the original system with respect to the centered data Xi − µ, find that the variable c drops out, get the system (X − µ)a = 0,
这意味着超平面A1必须通过数据点x1，…，xn的质心。然后，我们可以重写原始系统相对于中心数据Xi，发现变量C退出，得到系统（x＝*）A＝0，

21.5. BEST AFFINE APPROXIMATION
21.5。最佳仿射近似
where a = (a1,...,ad).
其中a=（a1，…，ad）。
Thus, we are looking for a unit vector a solving (X − µ)a = 0 in the least squares sense, that is, some a such that a>a = 1 minimizing
因此，我们在寻找一个单位向量a，在最小二乘意义上求解（x−μ）a=0，也就是说，一些a，使得a>a=1最小化
a>(X − µ)>(X − µ)a.
A>（X−礹）>（X−礹）A.
Compute some SVD V DU> of X −µ, where the main diagonal of D consists of the singular values σ1 ≥ σ2 ≥ ··· ≥ σd of X − µ arranged in descending order. Then
计算x−μ的一些svd v du>值，其中d的主对角线由x−μ的奇异值σ1≥σ2≥·······························然后
a>(X − µ)>(X − µ)a = a>UD2U>a,
a>（x−礹）>（x−礹）a=a>ud2u>a，
where D2 = diag() is a diagonal matrix, so pick a to be the last column in U
其中d2=diag（）是一个对角矩阵，所以选择a作为u中的最后一列
(corresponding to the smallest eigenvalue σd2 of (X − µ)>(X − µ)). This is a solution to our best fit problem.
（对应于（x−μ）>（x−μ）的最小特征值σd2）。这是我们最适合的问题的解决方案。
Therefore, if Ud−1 is the linear hyperplane defined by a, that is,
因此，如果ud−1是由a定义的线性超平面，也就是说，
Ud−1 = {u ∈ Rd | hu,ai = 0},
ud−1=u∈rd hu，ai=0，
where a is the last column in U for some SVD V DU> of X − µ, we have shown that the affine hyperplane A1 = µ + Ud−1 is a best approximation of the data set X1,...,Xn in the least squares sense.
其中a是x−μ的某些svd v du>的u中的最后一列，我们已经证明仿射超平面a1=μ+ud−1是最小平方意义上的数据集x1，…，xn的最佳近似值。
It is easy to show that this hyperplane A1 = µ + Ud−1 minimizes the sum of the square distances of each Xi to its orthogonal projection onto A1. Also, since Ud−1 is the orthogonal complement of a, the last column of U, we see that Ud−1 is spanned by the first d−1 columns of U, that is, the first d − 1 principal directions of X − µ.
很容易证明，超平面A1=ω+UD 1最小化了每个XI的平方距离与A1上的正交投影的平方之和。此外，由于u d−1是u的最后一列a的正交补码，我们发现ud−1由u的第一个d−1列（即x−µ的第一个d−1主方向）构成。
All this can be generalized to a best (d−k)-dimensional affine subspace Ak approximating X1,...,Xn in the least squares sense (1 ≤ k ≤ d−1). Such an affine subspace Ak is cut out by k independent hyperplanes Hi (with 1 ≤ i ≤ k), each given by some equation
所有这些都可以推广到一个最佳（d−k）维仿射子空间ak，在最小二乘意义上近似于x1，…，xn（1≤k≤d−1）。这样的仿射子空间ak由k独立超平面hi（1≤i≤k）切出，每个超平面由一些方程给出。
ai1x1 + ··· + aidxd + ci = 0.
ai1x1+·····+aidxd+ci=0.
If we write ai = (ai1,··· ,aid), to say that the Hi are independent means that a1,...,ak are linearly independent. In fact, we may assume that a1,...,ak form an orthonormal system.
如果我们写ai=（ai1，···，aid），表示hi是独立的，意味着a1，…，ak是线性独立的。事实上，我们可以假设a1，…，ak形成一个正态系统。
Then finding a best (d − k)-dimensional affine subspace Ak amounts to solving the homogeneous linear system
然后找到一个最佳的（d−k）维仿射子空间AK等于解齐次线性系统。
 ,
，
in the least squares sense, subject to the conditions a>i aj = δij, for all i,j with 1 ≤ i,j ≤ k, where the matrix of the system is a block diagonal matrix consisting of k diagonal blocks (X,1), where 1 denotes the column vector (1,...,1) ∈ Rn.
在最小二乘意义上，在a>i a j=δij的条件下，对于所有i，j，1≤i，j≤k，其中系统矩阵是由k个对角块（x，1）组成的块对角矩阵，其中1表示列向量（1，…，1）∈rn。
Again it is easy to see that each hyperplane Hi must pass through the centroid µ of X1,...,Xn, and by switching to the centered data Xi − µ we get the system 	  
很容易看出，每一个超平面Hi都必须通过x1，…，xn的质心，通过切换到中心数据Xi，我们得到了系统。
	X − µ	0 ···	0	a1	0
X−0···0 A1 0
	 ...	...	...	...  ...  = ...,
……………………=…，

γ
	0	0 ···	X − µ	ak	0
0 0·····X····AK 0
with a>i aj = δij for all i,j with 1 ≤ i,j ≤ k.
a>i a j=δij，对于所有i，j，1≤i，j≤k。
If V DU> = X−µ is an SVD decomposition, it is easy to see that a least squares solution of this system is given by the last k columns of U, assuming that the main diagonal of D consists of the singular values σ1 ≥ σ2 ≥ ··· ≥ σd of X−µ arranged in descending order. But now the (d−k)-dimensional subspace Ud−k cut out by the hyperplanes defined by a1,...,ak is simply the orthogonal complement of (a1,...,ak), which is the subspace spanned by the first d − k columns of U.
如果v d u>=x−µ是一个SVD分解，很容易看出这个系统的最小二乘解是由u的最后k列给出的，假设d的主对角线由x−µ的奇异值σ1≥σ2≥···································但是现在，由a1，…，ak定义的超平面切出的（d−k）维子空间ud−k只是（a1，…，ak）的正交补码，它是由u的第一个d−k列所跨越的子空间。
So the best (d−k)-dimensional affine subpsace Ak approximating X1,...,Xn in the least squares sense is
因此，在最小二乘意义上，最好的（d−k）维仿射子簇ak近似于x1，…，xn是
Ak = µ + Ud−k,
ak=μ+ud−k，
where Ud−k is the linear subspace spanned by the first d−k principal directions of X−µ, that is, the first d−k columns of U. Consequently, we get the following interesting interpretation of PCA (actually, principal directions):
其中，u d−k是由x−μ的第一个d−k主方向（即u的第一个d−k列）所跨越的线性子空间。因此，我们得到了以下有趣的PCA解释（实际上，主方向）：
Theorem 21.12. Let X be an n × d matrix of data points X1,...,Xn, and let µ be the centroid of the Xi’s. If X − µ = V DU> is an SVD decomposition of X − µ and if the main diagonal of D consists of the singular values σ1 ≥ σ2 ≥ ··· ≥ σd, then a best (d − k)dimensional affine approximation Ak of X1,...,Xn in the least squares sense is given by
定理21.12。设X是数据点X1、…、Xn的N×D矩阵，并设为Xi的质心。如果X＝＝V DU>是X×SVD的SVD分解，如果D的主对角线是由奇异值α1×2以上的ω-ω-ωd，则是一个最好的（d×k）维仿射逼近A。k的x1，…，xn在最小二乘意义上由下式给出
Ak = µ + Ud−k,
ak=μ+ud−k，
where Ud−k is the linear subspace spanned by the first d − k columns of U, the first d − k principal directions of X − µ (1 ≤ k ≤ d − 1).
其中，u d−k是由u的第一个d−k列跨越的线性子空间，x−（1≤k≤d−1）的第一个d−k主方向。
Example 21.11. Going back to Example 21.10, a best 1-dimensional affine approximation A1 is the affine line passing through (µ1,µ2) = (1824.4,5.6) of direction u1 = (0.9995,0.0325).
例21.11。回到实施例21.10，最好的一维仿射近似值a1是穿过U1=（0.9995,0.0325）方向（μ1，μ2）=（1824.4,5.6）的仿射线。
There are many applications of PCA to data compression, dimension reduction, and pattern analysis. The basic idea is that in many cases, given a data set X1,...,Xn, with Xi ∈ Rd, only a “small” subset of m < d of the features is needed to describe the data set accurately.
PCA在数据压缩、降维和模式分析中有许多应用。其基本思想是，在许多情况下，给定数据集X1，…，Xn，Xi，RD RD，只有一个“小”子集的特征的MD D需要准确地描述数据集。
21.6. SUMMARY
21.6。总结
If u1,...,ud are the principal directions of X −µ, then the first m projections of the data (the first m principal components, i.e., the first m columns of V D) onto the first m principal directions represent the data without much loss of information. Thus, instead of using the original data points X1,...,Xn, with Xi ∈ Rd, we can use their projections onto the first m principal directions Y1,...,Ym, where Yi ∈ Rm and m < d, obtaining a compressed version of the original data set.
如果U1，…，ud是x−祄的主方向，那么数据的第一个m投影（第一个m主分量，即v d的第一个m列）在第一个m主方向上表示数据，而不会丢失太多信息。因此，代替使用原始数据点X1，…，Xn，用Xi×RD，我们可以将它们的投影应用到第一M主方向Y1，…，YM，其中Yi-Rm和M< D，获得原始数据集的压缩版本。
For example, PCA is used in computer vision for face recognition. Sirovitch and Kirby (1987) seem to be the first to have had the idea of using PCA to compress facial images. They introduced the term eigenpicture to refer to the principal directions, ui. However, an explicit face recognition algorithm was given only later by Turk and Pentland (1991). They renamed eigenpictures as eigenfaces.
例如，PCA用于计算机视觉中的人脸识别。Sirovitch和Kirby（1987）似乎是第一个想到使用PCA压缩面部图像的人。他们引入了“本征图”这个术语来指代主方向，即用户界面。然而，只有在Turk和Pentland（1991）之后才给出了一种明确的人脸识别算法。他们把本征图片改名为本征面。
For details on the topic of eigenfaces, see Forsyth and Ponce [65] (Chapter 22, Section 22.3.2), where you will also find exact references to Turk and Pentland’s papers.
有关Eigenfaces主题的详细信息，请参阅Forsyth和Ponce[65]（第22章，第22.3.2节），在这里您还可以找到Turk和Pentland论文的确切参考。
Another interesting application of PCA is to the recognition of handwritten digits. Such an application is described in Hastie, Tibshirani, and Friedman, [87] (Chapter 14, Section
PCA的另一个有趣的应用是手写数字的识别。这种应用在黑斯提、提比西拉尼和弗里德曼[87]中有描述（第14章，第
14.5.1).
14.5.1条）。
21.6	Summary
21.6总结
The main concepts and results of this chapter are listed below:
本章的主要概念和结果如下：
•	Least squares problems.
最小二乘问题。
•	Existence of a least squares solution of smallest norm (Theorem 21.1).
最小范数最小二乘解的存在性（定理21.1）。
•	The pseudo-inverse A+ of a matrix A. • The least squares solution of smallest norm is given by the pseudo-inverse (Theorem
矩阵A的伪逆A+。•最小范数的最小二乘解由伪逆（定理）给出。
21.2)
21.2）
•	Projection properties of the pseudo-inverse.
伪逆的投影属性。
•	The pseudo-inverse of a normal matrix.
正态矩阵的伪逆矩阵。
•	The Penrose characterization of the pseudo-inverse.
伪逆的彭罗斯特征。
•	Data compression and SVD.
数据压缩和SVD。
•	Best approximation of rank < r of a matrix.
矩阵秩小于r的最佳近似。
•	Principal component analysis.
主成分分析。
•	Review of basic statistical concepts: mean, variance, covariance, covariance matrix.
回顾基本统计概念：均值、方差、协方差、协方差矩阵。
•	Centered data, centroid.
中心数据，质心。
•	The principal components (PCA).
主要成分（PCA）。
•	The Rayleigh–Ritz theorem (Theorem 21.10).
瑞利-里兹定理（定理21.10）。
•	The main theorem: SVD yields PCA (Theorem 21.11).
主定理：SVD产生PCA（定理21.11）。
•	Best affine approximation.
最佳仿射近似。
•	SVD yields a best affine approximation (Theorem 21.12).
SVD产生最佳仿射近似（定理21.12）。
•	Face recognition, eigenfaces.
人脸识别，特征面。
21.7	Problems
21.7问题
Problem 21.1. Consider the overdetermined system in the single variable x:
问题21.1。考虑单变量x中的超定系统：
a1x = b1,...,amx = bm.
a1x=b1，…，amx=bm。
Prove that the least squares solution of smallest norm is given by
证明了最小范数的最小二乘解由
.
.
Problem 21.2. Let X be an m × n real matrix. For any strictly positive constant K > 0, the matrix X>X +KIn is invertible. Prove that the limit of the matrix (X>X +KIn)−1X> when K goes to zero is equal to the pseudo-inverse X+ of X.
问题21.2。设x为m×n实矩阵。对于任何严格正常数k>0，矩阵x>x+kin是可逆的。证明当k为零时，矩阵（x>x+kin）−1X>的极限等于x的伪逆x+。
Problem 21.3. Use Matlab to find the pseudo-inverse of the 8 × 6 matrix
问题21.3。用matlab求8×6矩阵的伪逆
64
网络错误
 9
网络错误
17
网络错误

网络错误
40 A = 32
网络错误

网络错误

网络错误
41
网络错误

网络错误
49
网络错误
8
网络错误	2
网络错误
55
网络错误
47
网络错误
26
网络错误
34
网络错误
23
网络错误
15
网络错误
58
网络错误	3 54
网络错误
46
网络错误
27
网络错误
35
网络错误
22
网络错误
14
网络错误
59
网络错误	61
网络错误
12
网络错误
20
网络错误
37
网络错误
29
网络错误
44
网络错误
52
网络错误
5
网络错误	60
网络错误
13
网络错误
21
网络错误
36
网络错误
28
网络错误
45
网络错误
53
网络错误
4
网络错误	6 
网络错误
51
网络错误
43
网络错误
30 38.
网络错误
19
网络错误
11
网络错误
62
网络错误
Observe that the sums of the columns are all equal to to 256. Let b be the vector of dimension 6 whose coordinates are all equal to 256. Find the solution x+ of the system Ax = b.
观察各列的总和均等于256。设b为坐标均等于256的维度6的向量。找到系统的解决方案x+，ax=b。
Problem 21.4. The purpose of this problem is to show that Proposition 21.9 (the Eckart– Young theorem) also holds for the Frobenius norm. This problem is adapted from Strang
问题21.4。这个问题的目的是证明21.9命题（Eckart-Young定理）也适用于Frobenius规范。这个问题是根据Strang改编的
[166], Section I.9.
[166]，第I.9节。
21.7. PROBLEMS
21.7。问题
Suppose the m×n matrix B of rank at most k minimizes kA − BkF . Start with an SVD of B,
假设秩至多k的m×n矩阵b使ka−bkf最小化。从B的SVD开始，
,
，
where D is a diagonal k × k matrix. We can write
其中d是对角线k×k矩阵。我们可以写信
,
，
where L is strictly lower triangular in the first k rows, E is diagonal, and R is strictly upper triangular, and let
其中，在前k行中，l是严格的下三角形，e是对角的，r是严格的上三角形，并
,
，
which clearly has rank
很明显有排名
(1)	Prove that
证明这一点
.
.
Since kA − BkF is minimal, show that L = R = F = 0.
因为kA−bkf是最小的，所以表明l=r=f=0。
Similarly, show that G = 0.
同样，显示g=0。
(2)	We have
我们有
 ,
，
where E is diagonal, so deduce that
其中e是对角线，所以推断
1.	D = diag(σ1,...,σk).
d=diag（σ1，…，σk）。
2.	The singular values of H must be the smallest n − k singular values of A.
h的奇异值必须是a的最小n-k奇异值。
3.	The minimum of kA − BkF must be.
kA−bkf的最小值必须为。
Problem 21.5. Prove that the closest rank 1 approximation (in k k2) of the matrix
问题21.5。证明矩阵的最近秩1近似（k k2）
is
是
.
.
	1 matrixShow that the Eckart–Young theorem fails for the operator normB such that kA − Bk∞ < kA − A1k∞.	k k∞ by finding a rank Problem 21.6. Find a closest rank 1 approximation (in k k2) for the matrices
1矩阵：通过发现秩问题21.6，Eckart–Young定理对算符normb失败，从而使k a−bk∞<ka−a1k∞.k k k∞。求矩阵的最近秩1近似值（k k2）
 .
.
Problem 21.7. Find a closest rank 1 approximation (in k k2) for the matrix
问题21.7。求矩阵的最近秩1近似值（k k2）
.
.
Problem 21.8. Let S be a real symmetric positive definite matrix and let S = UΣU> be a diagonalization of S. Prove that the closest rank 1 matrix (in the L2-norm) to, where u1 is the first column of U.
问题21.8。设为实对称正定矩阵，设s=u∑u>为s的对角化，证明最接近的秩1矩阵（在l2范数中），其中u1是u的第一列。