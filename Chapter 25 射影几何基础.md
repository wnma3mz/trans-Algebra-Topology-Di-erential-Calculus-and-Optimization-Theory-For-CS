第二十五章
Basics of Projective Geometry
射影几何基础
Think geometrically, prove algebraically.
几何地思考，代数地证明。
—John Tate
-约翰·泰特
25.1	Why Projective Spaces?
25.1为什么是投影空间？
For a novice, projective geometry usually appears to be a bit odd, and it is not obvious to motivate why its introduction is inevitable and in fact fruitful. One of the main motivations arises from algebraic geometry.
对于一个初学者来说，射影几何通常显得有点奇怪，并且不明显地激发了为什么它的引入是不可避免的，实际上是富有成效的。其中一个主要的动机来自代数几何。
The main goal of algebraic geometry is to study the properties of geometric objects, such as curves and surfaces, defined implicitly in terms of algebraic equations. For instance, the equation
代数几何的主要目标是研究几何对象的性质，如曲线和曲面，这些对象是通过代数方程隐式定义的。例如，方程式
x2 + y2 − 1 = 0
x2+y2−1=0
defines a circle in R2. More generally, we can consider the curves defined by general equations
在r2中定义一个圆。一般来说，我们可以考虑由一般方程定义的曲线
ax2 + by2 + cxy + dx + ey + f = 0
ax2+by2+cxy+dx+ey+f=0
of degree 2, known as conics. It is then natural to ask whether it is possible to classify these curves according to their generic geometric shape. This is indeed possible. Except for so-called singular cases, we get ellipses, parabolas, and hyperbolas. The same question can be asked for surfaces defined by quadratic equations, known as quadrics, and again, a classification is possible. However, these classifications are a bit artificial. For example, an ellipse and a hyperbola differ by the fact that a hyperbola has points at infinity, and yet, their geometric properties are identical, provided that points at infinity are handled properly.
二度的，称为二次曲线的。然后自然会问，是否可以根据这些曲线的一般几何形状对它们进行分类。这确实是可能的。除了所谓的奇异情况，我们得到椭圆、抛物线和双曲线。同样的问题也可以问到由二次方程定义的曲面，即所谓的四次曲面，同样，分类也是可能的。然而，这些分类有点人为。例如，椭圆和双曲线的区别在于双曲线在无穷远处有点，但如果正确处理无穷远处的点，则它们的几何性质是相同的。
Another important problem is the study of intersection of geometric objects (defined algebraically). For example, given two curves C1 and C2 of degree m and n, respectively, what is the number of intersection points of C1 and C2? (by degree of the curve we mean the total degree of the defining polynomial).
另一个重要问题是研究几何对象的交集（代数定义）。例如，给定m阶和n阶的两条曲线c1和c2，c1和c2的交点数是多少？（曲线的度数是指定义多项式的总度数）。
759
七百五十九

Well, it depends! Even in the case of lines (when m = n = 1), there are three possibilities: either the lines coincide, or they are parallel, or there is a single intersection point. In general, we expect mn intersection points, but some of these points may be missing because they are at infinity, because they coincide, or because they are imaginary.
好吧，看情况而定！即使在直线的情况下（当m=n=1时），也有三种可能：要么直线重合，要么它们平行，要么只有一个交叉点。一般来说，我们期望有mn交点，但其中一些可能会丢失，因为它们是无穷大的，因为它们是重合的，或者因为它们是虚构的。
What begins to transpire is that “points at infinity” cause trouble. They cause exceptions that invalidate geometric theorems (for example, consider the more general versions of the theorems of Pappus and Desargues), and make it difficult to classify geometric objects. Projective geometry is designed to deal with “points at infinity” and regular points in a uniform way, without making a distinction. Points at infinity are now just ordinary points, and many things become simpler. For example, the classification of conics and quadrics becomes simpler, and intersection theory becomes cleaner (although, to be honest, we need to consider complex projective spaces).
开始出现的是“指向无限”会引起麻烦。它们会导致使几何定理失效的异常（例如，考虑pappus和desargues定理的更通用版本），并使几何对象的分类变得困难。射影几何是设计用来处理“无限点”和规则点的统一方式，而不作区分。无穷远处的点现在只是普通的点，许多事情变得简单了。例如，二次曲线和四次曲线的分类变得更简单，交集理论变得更清晰（老实说，我们需要考虑复杂的射影空间）。
Technically, projective geometry can be defined axiomatically, or by building upon linear algebra. Historically, the axiomatic approach came first (see Veblen and Young [177, 178], Emil Artin [6], and Coxeter [45, 46, 43, 44]). Although very beautiful and elegant, we believe that it is a harder approach than the linear algebraic approach. In the linear algebraic approach, all notions are considered up to a scalar. For example, a projective point is really a line through the origin. In terms of coordinates, this corresponds to “homogenizing.” For example, the homogeneous equation of a conic is
从技术上讲，射影几何可以用公理定义，也可以建立在线性代数的基础上。历史上，公理化的方法首先出现（见Veblen and Young[177，178]、Emil Artin[6]和Coxeter[45，46，43，44]）。虽然非常漂亮和优雅，我们相信这是一个比线性代数方法更困难的方法。在线性代数方法中，所有的概念都被认为是一个标量。例如，投影点实际上是一条穿过原点的线。在坐标方面，这相当于“均匀化”，例如，二次曲线的齐次方程是
ax2 + by2 + cxy + dxz + eyz + fz2 = 0.
ax2+by2+cxy+dxz+eyz+fz2=0。
Now, regular points are points of coordinates (x,y,z) with z = 06 , and points at infinity are points of coordinates (x,y,0) (with x, y, z not all null, and up to a scalar). There is a useful model (interpretation) of plane projective geometry in terms of the central projection in R3 from the origin onto the plane z = 1. Another useful model is the spherical (or the half-spherical) model. In the spherical model, a projective point corresponds to a pair of antipodal points on the sphere.
现在，规则点是z=06的坐标点（x，y，z），无穷远处的点是坐标点（x，y，0）（x，y，z不都是空的，并且达到一个标量）。根据r3中从原点到平面z=1的中心投影，有一个有用的平面投影几何模型（解释）。另一个有用的模型是球形（或半球形）模型。在球面模型中，一个投影点对应于球面上的一对反极点。
As affine geometry is the study of properties invariant under affine bijections, projective geometry is the study of properties invariant under bijective projective maps. Roughly speaking, projective maps are linear maps up to a scalar. In analogy with our presentation of affine geometry, we will define projective spaces, projective subspaces, projective frames, and projective maps. The analogy will fade away when we define the projective completion of an affine space, and when we define duality.
由于仿射几何是研究仿射双射下不变性质的，射影几何是研究双射射影映射下不变性质的。大致来说，射影映射是一个标量的线性映射。与我们对仿射几何的描述类似，我们将定义射影空间、射影子空间、射影框架和射影映射。当我们定义仿射空间的射影完备和定义对偶性时，这个类比就会消失。
One of the virtues of projective geometry is that it yields a very clean presentation of rational curves and rational surfaces. The general idea is that a plane rational curve is the projection of a simpler curve in a larger space, a polynomial curve in R3, onto the plane z = 1, as we now explain.
射影几何的一个优点是它能产生非常清晰的有理曲线和有理曲面的表示。一般的观点是平面有理曲线是一条更简单曲线在更大的空间中的投影，一条r3中的多项式曲线，在平面z=1上，正如我们现在所解释的。
Polynomial curves are curves defined parametrically in terms of polynomials. More specifically, if E is an affine space of finite dimension n ≥ 2 and (a0,(e1,...,en)) is an affine frame
多项式曲线是根据多项式参数定义的曲线。更具体地说，如果e是有限维n≥2的仿射空间，（a0，（e1，…，en））是仿射框架
25.1. WHY PROJECTIVE SPACES?
25.1。为什么是投影空间？
for E, a polynomial curve of degree m is a map F : A → E such that
对于e，m次多项式曲线是f:a→e的映射，因此
F(t) = a0 + F1(t)e1 + ··· + Fn(t)en,
f（t）=a0+f1（t）e1+····+fn（t）en，
for all t ∈ A, where F1(t),...,Fn(t) are polynomials of degree at most m.
对于所有t∈a，其中f1（t），…，fn（t）最多为m的次数多项式。
Although many curves can be defined, it is somewhat embarassing that a circle cannot be defined in such a way. In fact, many interesting curves cannot be defined this way, for example, ellipses and hyperbolas. A rather simple way to extend the class of curves defined parametrically is to allow rational functions instead of polynomials. A parametric rational curve of degree m is a function F : A → E such that
虽然可以定义许多曲线，但不能这样定义圆，这有点令人尴尬。事实上，许多有趣的曲线不能这样定义，例如椭圆和双曲线。扩展参数化定义的曲线类的一个相当简单的方法是允许有理函数而不是多项式。m阶的参数有理曲线是f:a→e的函数，因此
,
，
for all t ∈ A, where F1(t),...,Fn(t),Fn+1(t) are polynomials of degree at most m. For example, a circle in A2 can be defined by the rational map
对于所有t∈a，其中f1（t）、…、fn（t）、fn+1（t）是最多m的度多项式，例如a2中的圆可以用有理映射来定义。
.
.
In terms of coordinates, the above curve is given by
在坐标方面，上述曲线由
,
，
and it is easily checked that x2 +y2 = 1. Note that the point (−1,0) is not achieved for any finite value of t, but it is for t = ∞.
可以很容易地看出，x2+y2=1。注意，对于t的任何有限值（−1,0）都不能达到该点，但对于t=∞。
In the above example, the denominator F3(t) = 1 + t2 never takes the value 0 when t ranges over A, but consider the following curve in A2:
在上述示例中，当t的范围超过a时，分母f3（t）=1+t2从不取0，但考虑a2中的以下曲线：
.
.
Observe that G(0) is undefined. In terms of coordinates, the above curve is given by
注意G（0）未定义。在坐标方面，上述曲线由

so we have y = 1/x. The curve defined above is a hyperbola, and for t close to 0, the point on the curve goes toward infinity in one of the two asymptotic directions.
所以我们有y=1/x。上面定义的曲线是一条双曲线，对于t接近0，曲线上的点在两个渐近方向中的一个朝无穷大。
A clean way to handle the situation in which the denominator vanishes is to work in a projective space. Intuitively, this means viewing a rational curve in An as some appropriate projection of a polynomial curve in An+1, back onto An.
处理分母消失的一种干净方法是在投影空间中工作。直观地说，这意味着在+1中的多项式曲线的适当投影中查看有理曲线，然后返回到。
Given an affine space E, for any hyperplane H in E and any point a0 not in H, the central projection (or conic projection, or perspective projection) of center a0 onto H, is the partial map p defined as follows: For every point x not in the hyperplane passing through a0 and parallel to H, we define p(x) as the intersection of the line defined by a0 and x with the hyperplane H; see Figure 25.1.
给定一个仿射空间e，对于e中的任何超平面h和不在h中的任何点a0，中心a0到h的中心投影（或圆锥投影或透视投影）是部分映射p，定义如下：对于不在通过a0和平行于h的超平面中的每个点x，我们定义p（x）是由a0和x定义的线与超平面h的交点；见图25.1。

Figure 25.1: A central projection in A3 through a0 onto the yellow hyperplane H. This central projection is not defined for any points in the peach hyperplane.
图25.1:a3到a0中的中心投影到黄色超平面h上。此中心投影没有为桃超平面中的任何点定义。
For example, we can view G as a rational curve in A3 given by
例如，我们可以将g看作a3中的有理曲线，由
G1(t) = a0 + t2e1 + e2 + te3.
g1（t）=a0+t2e1+e2+te3。
If we project this curve G1 (in fact, a parabola in A3) using the central projection (perspective projection) of center a0 onto the plane of equation x3 = 1, we get the previous hyperbola; see Figure 25.2. For t = 0, the point G1(0) = a0 +e2 in A3 is in the plane of equation x3 = 0, and its projection is undefined. We can consider that G1(0) = a0 + e2 in A3 is projected to infinity in the direction of e2 in the plane x3 = 0. In the setting of projective spaces, this direction corresponds rigorously to a point at infinity; see Figure 25.2.
如果我们使用中心a0的中心投影（透视投影）将曲线g1（实际上是a3中的抛物线）投影到方程x3=1的平面上，我们得到先前的双曲线；见图25.2。对于t=0，a3中的点g1（0）=a0+e2在式x3=0的平面上，其投影未定义。我们可以认为，在平面x3=0中，a3中的g1（0）=a0+e2沿e2的方向投影到无穷大。在射影空间的设置中，这个方向严格对应于无穷远处的一个点；见图25.2。
Let us verify that the central projection used in the previous example has the desired effect. Let us assume that E has dimension n + 1 and that (a0,(e1,...,en+1)) is an affine
让我们验证前面示例中使用的中心投影是否具有所需的效果。假设e的维数为n+1，（a0，（e1，…，en+1））是仿射
25.1. WHY PROJECTIVE SPACES?
25.1。为什么是投影空间？

Figure 25.2: A central projection in A3 through a0 of the parabola G1(t) onto the hyperplane x3 = 1.
图25.2：抛物线g1（t）在a3到a0中的中心投影到超平面x3=1上。
frame for E. We want to determine the coordinates of the central projection p(x) of a point x ∈ E onto the hyperplane H of equation xn+1 = 1 (the center of projection being a0). If
设为E的框架，我们要确定X点的中心投影P（X）∈E在方程Xn+1=1（投影中心为a0）的超平面H上的坐标。如果
x = a0 + x1e1 + ··· + xnen + xn+1en+1,
x=a0+x1e1+·····+xnen+xn+1en+1，
assuming that xn+1 = 06 ; a point on the line passing through a0 and x has coordinates of the form (λx1,...,λxn+1); and p(x), the central projection of x onto the hyperplane H of equation xn+1 = 1, is the intersection of the line from a0 to x and this hyperplane H. Thus we must have λxn+1 = 1, and the coordinates of p(x) are
假设xn+1=06；穿过a0和x的直线上的一点具有形式的坐标（λx 1，…，λxn+1）；和p（x），x在方程xn+1=1的超平面h上的中心投影是a0到x的直线与该超平面h的交点。因此，我们必须得到λxn+1=1，and p（x）的坐标为
.
.
Note that p(x) is undefined when xn+1 = 0. In projective spaces, we can make sense of such points.
注意，当xn+1=0时，p（x）是未定义的。在射影空间中，我们可以理解这些点。
The above calculation confirms that G(t) is a central projection of G1(t). Similarly, if we define the curve F1 in A3 by
上述计算证实G（t）是g1（t）的中心投影。同样地，如果我们将a3中的曲线f1定义为
F1(t) = a0 + (1 − t2)e1 + 2te2 + (1 + t2)e3,
f1（t）=a0+（1−t2）e1+2te2+（1+t2）e3，
the central projection of the polynomial curve F1 (again, a parabola in A3) onto the plane of equation x3 = 1 is the circle F.
多项式曲线f1（同样是a3中的抛物线）在方程x3=1平面上的中心投影是圆f。
What we just sketched is a general method to deal with rational curves. We can use our “hat construction” to embed an affine space E into a vector space Eb having one more dimension, then construct the projective space P Eb. This turns out to be the “projective completion” of the affine space E. Then we can define a rational curve in P , basically as the central projection of a polynomial curve in Ebback onto P . The same approach can be used to deal with rational surfaces. Due to the lack of space, such a presentation is omitted. However, it can be found on the web; see http://www.cis.upenn.edu/ jean/gbooks/geom2.html.
我们刚才画的是处理有理曲线的一般方法。我们可以利用我们的“帽构造”将仿射空间e嵌入到一个多维度的向量空间eb中，然后构造投影空间peb。这就是仿射空间e的“投影完成”，然后我们可以定义p中的有理曲线，基本上是ebback中多项式曲线对p的中心投影。同样的方法也可以用来处理有理曲面。由于缺乏空间，这种陈述被省略了。但是，可以在网上找到；请参阅http://www.cis.upenn.edu/jean/gbooks/geom2.html。
e
e
More generally, the projective completion of an affine space is a very convenient tool to handle “points at infinity” in a clean fashion.
更一般地说，仿射空间的投影完成是一个非常方便的工具，可以以干净的方式处理“无限点”。
This chapter contains a brief presentation of concepts of projective geometry. The following concepts are presented: projective spaces, projective frames, homogeneous coordinates, projective maps, projective hyperplanes, multiprojective maps, affine patches. The projective completion of an affine space is presented using the “hat construction.” The theorems of Pappus and Desargues are proved, using the method in which points are “sent to infinity.” We also discuss the cross-ratio and duality. The chapter ends with a very brief explanation of the use of the complexification of a projective space in order to define the notion of angle and orthogonality in a projective setting. We also include a short section on applications of projective geometry, notably to computer vision (camera calibration), efficient communication, and error-correcting codes.
本章简要介绍射影几何的概念。给出了以下概念：射影空间、射影框架、齐次坐标、射影映射、射影超平面、多射影映射、仿射面片。利用“hat构造”给出了仿射空间的射影完备，利用点“送至无穷远”的方法，证明了pappus和desargues的定理，并讨论了交叉比和对偶性。本章最后对射影空间的复杂性的使用作了非常简短的解释，以便在射影环境中定义角度和正交性的概念。我们还简要介绍了射影几何的应用，特别是计算机视觉（相机校准）、有效通信和纠错代码。
25.2	Projective Spaces
25.2投影空间
As in the case of affine geometry, our presentation of projective geometry is rather sketchy. For a systematic treatment of projective geometry, we recommend Berger [11, 12], Samuel [138], Pedoe [132], Coxeter [45, 46, 43, 44], Beutelspacher and Rosenbaum [22], Fresnel [66], Sidler [156], Tisseron [170], Lehmann and Bkouche [112], Vienne [179], and the classical treatise by Veblen and Young [177, 178], which, although slightly old-fashioned, is definitely worth reading. Emil Artin’s famous book [6] contains, among other things, an axiomatic presentation of projective geometry, and a wealth of geometric material presented from an algebraic point of view. Other “oldies but goodies” include the beautiful books by Darboux [48] and Klein [101]. For a development of projective geometry addressing the delicate problem of orientation, see Stolfi [162], and for an approach geared towards computer graphics, see Penna and Patterson [133].
在仿射几何中，我们对射影几何的描述相当粗略。对于射影几何的系统治疗，我们推荐Berger[11，12]、Samuel[138]、Pedoe[132]、Coxeter[45，46，43，44]、Beutelspacher和Rosenbaum[22]、Fresnel[66]、Sidler[156]、Tisseron[170]、Lehmann和Bkouche[112]、Vienne[179]和Veblen和Young的经典论文。[177178]虽然有些过时，但绝对值得一读。埃米尔·阿廷的著名著作[6]包括射影几何的公理化表述，以及从代数角度呈现的大量几何材料。其他的“古老而美好”包括达布克斯[48]和克莱恩[101]的美丽书籍。关于射影几何学的发展，解决了方向的微妙问题，见Stolfi[162]，关于面向计算机图形的方法，见Penna和Patterson[133]。
First, we define projective spaces, allowing the field K to be arbitrary (which does no harm, and is needed to allow finite and complex projective spaces). Roughly speaking, every projective concept is a linear–algebraic concept “up to a scalar.” For spaces, this is made precise as follows.
首先，我们定义了射影空间，允许场k是任意的（这不会造成伤害，并且需要允许有限和复杂的射影空间）。粗略地说，每一个射影概念都是一个线性代数概念，“达到一个标量”。对于空间来说，精确到如下。
Definition 25.1. Given a vector space E over a field K, the projective space P(E) induced by E is the set (E − {0})/ ∼ of equivalence classes of nonzero vectors in E under the
定义25.1.给定场k上的向量空间e，e引起的射影空间p（e）是e中非零向量在
25.2. PROJECTIVE SPACES equivalence relation ∼ defined such that for all u,v ∈ E − {0},
25.2。射影空间等价关系～定义如下：对于所有u，v∈e−0，
	u ∼ v	iff	v = λu, for some λ ∈ K − {0}.
u～v iff v=λu，对于某些λ∈k−0。
The canonical projection p: (E − {0}) → P(E) is the function associating the equivalence class [u]∼ modulo ∼ to u = 06 . The dimension dim(P(E)) of P(E) is defined as follows: If E is of infinite dimension, then dim(P(E)) = dim(E), and if E has finite dimension, dim(E) = n ≥ 1 then dim(P(E)) = n − 1.
规范投影p：（e−0）→p（e）是将等价类[u]模～u=06关联起来的函数。p（e）的维数dim（p（e））定义如下：如果e是无限维，那么dim（p（e））=dim（e），如果e是有限维，dim（e）=n≥1，那么dim（p（e））=n−1。
Mathematically, a projective space P(E) is a set of equivalence classes of vectors in E. The spirit of projective geometry is to view an equivalence class p(u) = [u]∼ as an “atomic” object, forgetting the internal structure of the equivalence class. For this reason, it is customary to call an equivalence class a = [u]∼ a point (the entire equivalence class [u]∼ is collapsed into a single object viewed as a point).
在数学上，射影空间p（e）是e中向量的一组等价类。射影几何的精神是将等价类p（u）=[u]视为“原子”对象，忽略等价类的内部结构。出于这个原因，通常调用等价类A=[U]一个点（整个等价类[U]折叠成一个被视为点的单个对象）。
Remarks:
评论：
(1) If we view E as an affine space, then for any nonnull vector u ∈ E, since
（1）如果我们把e看作仿射空间，那么对于任何非零向量u∈e，因为
	[u]∼ = {λu | λ ∈ K, λ = 06	},
[u]λuλ∈k，λ=06，
letting
出租
Ku = {λu | λ ∈ K}
ku=λuλ∈k
denote the subspace of dimension 1 spanned by u, the map
表示用u表示的维度1的子空间，即地图
[u]∼ 7→ Ku
[u]7→ku
from P(E) to the set of one-dimensional subspaces of E is clearly a bijection, and since subspaces of dimension 1 correspond to lines through the origin in E, we can view P(E) as the set of lines in E passing through the origin. So, the projective space P(E) can be viewed as the set obtained from E when lines through the origin are treated as points.
从p（e）到e的一维子空间集显然是一个双射，由于维1的子空间对应于e中穿过原点的线，我们可以将p（e）视为e中穿过原点的线集。因此，射影空间p（e）可以看作是通过原点的直线被视为点时从e得到的集合。
However, this is a somewhat deceptive view. Indeed, depending on the structure of the vector space E, a line (through the origin) in E may be a fairly complex object, and treating a line just as a point is really a mental game. For example, E may be the vector space of real homogeneous polynomials P(x,y,z) of degree 2 in three variables x,y,z (plus the null polynomial), and a “line” (through the origin) in E corresponds to an algebraic curve of degree 2. Lots of details need to be filled in, but roughly speaking, the curve defined by P is the “zero locus of P,” i.e., the set of points (x,y,z) ∈ P(R3) (or perhaps in P(C3)) for which P(x,y,z) = 0. We will come back to this point in Section 25.4 after having introduced homogeneous coordinates.
然而，这是一种有点欺骗性的观点。实际上，根据向量空间e的结构，e中的一条线（通过原点）可能是一个相当复杂的对象，将一条线当作一个点来处理实际上是一种心理游戏。例如，e可以是二次实齐次多项式p（x，y，z）在三个变量x，y，z（加上零多项式）中的向量空间，e中的“线”（通过原点）对应二次代数曲线。需要填写很多细节，但粗略地说，由p定义的曲线是“p的零轨迹”，即点集（x，y，z）∈p（r3）（或可能在p（c3）），其中p（x，y，z）=0。在引入齐次坐标后，我们将在第25.4节中回到这一点。
More generally, E may be a vector space of homogeneous polynomials of degree m in 3 or more variables (plus the null polynomial), and the lines in E correspond to such objects as algebraic curves, algebraic surfaces, and algebraic varieties. The point of view where a complex object such as a curve or a surface is treated as a point in a (projective) space is actually very fruitful and is one of the themes of algebraic geometry (see Fulton [67] or Harris [86]).
更一般地说，e可以是3个或更多变量（加上零多项式）中m次齐次多项式的向量空间，e中的线对应于代数曲线、代数曲面和代数变种等对象。把复杂物体（如曲线或曲面）视为（投影）空间中的一个点的观点实际上非常有效，是代数几何的主题之一（见Fulton[67]或Harris[86]）。
(2) When dim(E) = 1, we have dim(P(E)) = 0. When E = {0}, we have P(E) = ∅. By convention, we give it the dimension −1.
（2）当dim（e）=1时，我们得到dim（p（e））=0。当e=0时，我们得到p（e）=∅。按照惯例，我们给它一个维度-1。
We denote the projective space P(Kn+1) by PnK. When K = R, we also denote PnR by RPn, and when K = C, we denote PnC by CPn. The projective space P0K is a (projective) point. The projective space P1K is called a projective line. The projective space P2K is called a projective plane.
我们用pnk表示射影空间p（kn+1）。当k=r时，我们也用rpn表示pnr，当k=c时，我们用cpn表示pnc。投影空间p0k是一个（投影）点。投影空间p1k称为投影线。射影空间p2k称为射影平面。
The projective space P(E) can be visualized in the following way. For simplicity, assume that E = Rn+1, and thus P(E) = RPn (the same reasoning applies to E = Kn+1, where K is any field).
射影空间p（e）可以用以下方式可视化。为了简单起见，假设e=rn+1，因此p（e）=rpn（同样的推理也适用于e=kn+1，其中k是任何字段）。
Let H be the affine hyperplane consisting of all points (x1,...,xn+1) such that xn+1 = 1. Every nonzero vector u in E determines a line D passing through the origin, and this line intersects the hyperplane H in a unique point a, unless D is parallel to H. When D is parallel to H, the line corresponding to the equivalence class of u can be thought of as a point at infinity, often denoted by u∞. Thus, the projective space P(E) can be viewed as the set of points in the hyperplane H, together with points at infinity associated with lines in the hyperplane H∞ of equation xn+1 = 0. We will come back to this point of view when we consider the projective completion of an affine space. Figure 25.3 illustrates the above representation of the projective space for E = R2 and E = R3.
设h为由所有点（x1，…，xn+1）组成的仿射超平面，这样xn+1=1。e中的每一个非零向量u决定了一条穿过原点的线d，并且这条线与唯一点a中的超平面h相交，除非d与h平行。当d与h平行时，与u的等价类相对应的线可以被认为是无穷远的点，通常表示为通过u∞。因此，投影空间p（e）可以看作是超平面h中的一组点，以及方程xn+1=0的超平面h∞中与直线相关的无穷远点。当我们考虑仿射空间的射影完备时，我们将回到这个观点。图25.3说明了e=r2和e=r3的射影空间的上述表示。

(ii.)
（二）
Figure 25.3: The hyperplane model representations of RP1 and RP2.
图25.3:RP1和RP2的超平面模型表示。
25.2. PROJECTIVE SPACES
25.2。射影空间
We refer to the above model of P(E) as the hyperplane model. In this model some hyperplane H∞ (through the origin) in Rn+1 is singled out, and the points of P(E) arising from the hyperplane H∞ are declared to be “points at infinity.” The purpose of the affine hyperplane H parallel to H∞ and distinct from H∞ is to get images for the other points in P(E) (i.e., those that arise from lines not contained in H∞). It should be noted that the choice of which points should be considered as infinite is relative to the choice of H∞. Viewing certain points of P(E) as points at infinity is convenient for getting a mental picture of P(E), but there is nothing intrinsic about that. Points of P(E) are all equal, and unless some additional structure in introduced in P(E) (such as a hyperplane), a point in P(E) doesn’t know whether it is infinite! The notion of point at infinity is really an affine notion. This point will be made precise in Section 25.8.
我们将上述P（E）模型称为超平面模型。在这个模型中，我们选取了Rn+1中的一些超平面H∞（通过原点），并将由超平面H∞产生的p（e）点声明为“无穷远点”，仿射超平面H与H∞平行，与H∞不同，其目的是为了得到其它点的图像。n p（e）（即由H∞中未包含的线产生的线）。值得注意的是，选择哪些点应被视为无穷大，与选择H∞有关。把p（e）的某些点看作无穷远处的点，可以方便地从精神上了解p（e），但这并不是什么内在的东西。p（e）的点都是相等的，除非p（e）中引入了一些附加的结构（例如超平面），p（e）中的点不知道它是否无穷大！无穷远点的概念实际上是仿射概念。这一点将在第25.8节中精确说明。
Again, for RPn = P(Rn+1), instead of considering the hyperplane H, we can consider the n-sphere Sn of center 0 and radius 1, i.e., the set of points (x1,...,xn+1) such that
同样，对于rpn=p（rn+1），不考虑超平面h，我们可以考虑圆心0和半径1的n球sn，即点集（x1，…，xn+1），这样
.
.
In this case, every line D through the center of the sphere intersects the sphere Sn in two antipodal pointsn by identifying antipodal pointsa+ and a−. The projective spacea+ RPandn ais the quotient space obtained from−. It is hard to visualize such an the sphere S object! We call this model of P(E) the spherical model. See Figure 25.4.
在这种情况下，通过球体中心的每一条线d都会通过识别反极点sa+和a-，与两个反极点sn中的球体sn相交。投影空间a+rpandn是从−得到的商空间。很难想象这样一个球体的物体！我们称这个P（E）模型为球形模型。见图25.4。

(ii.)
（二）
Figure 25.4: The spherical model representations of RP1 and RP2.
图25.4:rp1和rp2的球形模型表示。
A more subtle construction consists in considering the (upper) half-sphere instead of the sphere, where the upper half-sphere is set of points on the sphere Sn such that xn+1 ≥ 0. This time, every line through the center intersects the (upper) half-sphere in a single point, except on the boundary of the half-sphere, where it intersects in two antipodal points a+ and a−. Thus, the projective space RPn is the quotient space obtained from the (upper) half-sphere by identifying antipodal points a+ and a− on the boundary of the half-sphere. We call this model of P(E) the half-spherical model; see Figure 25.5.
更微妙的结构是考虑（上）半球体而不是球体，其中上半球体是球体sn上的一组点，因此xn+1≥0。这一次，穿过中心的每一条线与（上）半球体在一个点上相交，除了在半球体的边界上，在那里它与两个反极点A+和A-相交。因此，射影空间Rpn是通过识别半球体边界上的对极点A+和A-从（上）半球体获得的商空间。我们称这个P（E）模型为半球面模型；见图25.5。

Figure 25.5: The half-spherical model representations of RP1 and RP2.
图25.5:rp1和rp2的半球面模型表示。
When n = 2, we get a circle. When n = 3, the upper half-sphere is homeomorphic to a closed disk (say, by orthogonal projection onto the xy-plane), and RP2 is in bijection with a closed disk in which antipodal points on its boundary (a unit circle) have been identified. This is hard to visualize! In this model of the real projective space, projective lines are great semicircles on the upper half-sphere, with antipodal points on the boundary identified. Boundary points correspond to points at infinity. By orthogonal projection, these great semicircles correspond to semiellipses, with antipodal points on the boundary identified. Traveling along such a projective “line,” when we reach a boundary point, we “wrap around”! In general, the upper half-sphere  is homeomorphic to the closed unit ball in Rn, whose boundary is the (nSn−1. For example, the projective space RP3 is in bijection with the closed unit ball in , with antipodal points on its boundary (the sphere S2) identified!
当n=2时，我们得到一个圆。当n=3时，上半球体同构于一个封闭圆盘（例如，通过在xy平面上的正交投影），并且rp2与一个封闭圆盘处于双射状态，在该封闭圆盘中，其边界上的反极点（单位圆）已被识别。这很难想象！在实射影空间的模型中，射影线是上半球面上的大半圆，边界上的反极点是确定的。边界点对应于无穷远处的点。通过正交投影，这些大半圆对应于半椭圆，并在边界上识别出对极点。沿着这样一条投射的“线”行进，当我们到达一个边界点时，我们就“环绕”！一般来说，上半球体与RN中的闭合单元球同胚，其边界为（nsn-1）。例如，投影空间rp3是双射的，封闭的单位球在里面，在它的边界（球体s2）上识别出了反极点！
Remarks:
评论：
(1)	A projective space P(E) has been defined as a set without any topological structure. When the field K is either the field R of reals or the field C of complex numbers, the vector space E is a topological space. Thus, the projection map p: (E −{0}) → P(E) induces a topology on the projective space P(E), namely the quotient topology. This means that a subset V of P(E) is open iff p−1(V ) is an open set in E. Then, for example, it turns out that the real projective space RPn is homeomorphic to the space
射影空间p（e）被定义为一个没有任何拓扑结构的集合。当K域是实数的R域或复数的C域时，向量空间E是拓扑空间。因此，投影图p:（e−0）→p（e）在投影空间p（e）上诱导拓扑，即商拓扑。这意味着p（e）的一个子集v是开的，如果p−1（v）是e中的一个开集，那么，举例来说，实际的射影空间rpn与空间同构。
25.3. PROJECTIVE SUBSPACES
25.3。射影子空间
obtained by taking the quotient of the (upper) half-sphere , by the equivalence
通过取（上）半球体的商，通过等价
Another interesting fact is that the complex projective linerelation identifying antipodal points a+ and a− on the boundary of the half-sphere.CP1 = P(C2) is homeomorphic to the (real) 2-sphere S2, and that the real projective space RP3 is homeomorphic to the group of rotations SO(3) of R3.
另一个有趣的事实是，在半球体的边界上识别反极点A+和A−的复杂射影线性关系。cp1=p（c2）与（实数）2球体s2同胚，而实数射影空间rp3与旋转群so（3）同胚。
(2)	If H is a hyperplane in E, recall from Proposition 10.4 that there is some nonnull linear form f ∈ E∗ such that H = Kerf. Also, given any nonnull linear form f ∈ E∗, its kernel H = Kerf = f−1(0) is a hyperplane, and if Kerf = Kerg = H, then g = λf for some λ = 06 . These facts can be concisely stated by saying that the map
如果h是e中的超平面，从命题10.4中回忆，有一些非零线性形式f∈e，这样h=kerf。另外，对于任何非空线性形式f∈e，其核h=kerf=f−1（0）是一个超平面，如果kerf=kerg=h，那么对于一些λ=06，g=λf。这些事实可以通过说
[f]∼ 7→ Kerf
[f]7→切口
mapping the equivalence class [f]∼ = {λf | λ = 06 } of a nonnull linear form f ∈ E∗ to the hyperplane H = Kerf in E is a bijection between the projective space P(E∗) and the set of hyperplanes in E. When E is of finite dimension, this bijection yields a useful duality, which will be investigated in Section 25.12.
将非零线性形式f∈e的等价类[f]λfλ=06映射到e中的超平面h=kerf是投影空间p（e）与e中的超平面集之间的双射。当e是有限维时，该双射产生一个有用的对偶性，将被转化为第25.12节中的TIG。
We now define projective subspaces.
我们现在定义射影子空间。
25.3	Projective Subspaces
25.3投影子空间
Projective subspaces of a projective space P(E) are induced by subspaces of the vector space E.
投影空间p（e）的投影子空间由向量空间e的子空间诱导而成。
Definition 25.2. Given a nontrivial vector space E, a projective subspace (or linear projective variety) of P(E) is any subset W of P(E) such that there is some subspace V =6 {0} of E with W = p(V − {0}). The dimension dim(W) of W is defined as follows: If V is of infinite dimension, then dim(W) = dim(V ), and if dim(V ) = p ≥ 1, then dim(W) = p − 1. We say that a family (ai)i∈I of points of P(E) is projectively independent if there is a linearly independent family (ui)i∈I in E such that ai = p(ui) for every i ∈ I.
定义25.2.对于非平凡向量空间e，p（e）的射影子空间（或线性射影变体）是p（e）的任何子空间w，因此存在一些子空间v=6 0 e，w=p（v−0）。W的尺寸dim（w）定义如下：如果v是无限尺寸，那么dim（w）=dim（v），如果dim（v）=p≥1，那么dim（w）=p−1。我们假设p（e）点的族（a i）i∈i是投影独立的，如果在e中有一个线性独立的族（ui）i∈i，那么ai=p（ui）对于每个i∈i。
Remark: If we allow the empty subset to be a projective subspace, then if assign the empty subset to the trivial subspace {0}, we obtain a bijection between the subspaces of E and the projective subspaces of P(E). If P(V ) is the projective space induced by the vector space V , we also denote p(V − {0}) by P(V ), or even by p(V ), even though p(0) is undefined.
注：如果我们允许空子集是投影子空间，那么如果将空子集赋给平凡子空间0，我们得到e的子空间与p（e）的投影子空间之间的双射。如果p（v）是向量空间v诱导的投影空间，我们也用p（v）表示p（v−0），甚至用p（v），即使p（0）未定义。
A projective subspace of dimension 0 is a called a (projective) point. A projective subspace of dimension 1 is called a (projective) line, and a projective subspace of dimension 2 is called a (projective) plane. If H is a hyperplane in E, then P(H) is called a projective hyperplane. It is easily verified that any arbitrary intersection of projective subspaces is a projective subspace.
维度0的投影子空间称为（投影）点。维数1的射影子空间称为（射影）线，维数2的射影子空间称为（射影）平面。如果h是e中的超平面，则p（h）称为投影超平面。很容易证明射影子空间的任意交集都是射影子空间。
A single point is projectively independent. Two points a,b are projectively independent if a =6 b. Two distinct points define a (unique) projective line. Three points a,b,c are projectively independent if they are distinct, and neither belongs to the projective line defined by the other two. Three projectively independent points define a (unique) projective plane.
单点是投影独立的。如果a=6b，两点a，b是投影独立的。两个不同的点定义了一条（唯一的）投影线。三个点A、B、C如果是不同的，则它们是投影独立的，并且都不属于其他两点定义的投影线。三个投影独立的点定义了一个（唯一的）投影平面。
A closer look at projective subspaces will show some of the advantages of projective geometry: In considering intersection properties, there are no exceptions due to parallelism, as in affine spaces.
仔细观察射影子空间将显示射影几何的一些优点：在考虑交集性质时，不存在由于平行性而产生的例外情况，如仿射空间。
Let E be a nontrivial vector space. Given any nontrivial subset S of E, the subset S defines a subset U = p(S − {0}) of the projective space P(E), and if hSi denotes the subspace of E spanned by S, it is immediately verified that P(hSi) is the intersection of all projective subspaces containing U, and this projective subspace is denoted by hUi. Then n ≥ 2 point a1,...,an ∈ P(E) are projectively independent iff for all i = 1,...,n the point ai does not belong to the projective subspace ha1,...,ai−1,ai+1,...,ani spanned by {a1,...,ai−1,ai+1,...,an}.
设e为非平凡向量空间。对于e的任何非平凡子集，子集s定义了射影空间p（e）的子集u=p（s−0），如果hsi表示e的子空间，则立即验证p（hsi）是包含u的所有射影子空间的交集，并且该射影子空间是由辉指出。那么n≥2点a1，…，an∈p（e）对所有i=1，…，都是投影独立的iff，n点aI不属于投影子空间ha1，…，ai−1，ai+1，…，ani，其范围为a1，…，ai−1，ai+1，…，an。
Given any subspaces M and N of E, recall from Proposition 23.15 that we have the
考虑到e的m和n的任何子空间，从23.15号提案中回忆起，我们有
Grassmann relation
格拉斯曼关系
dim(M) + dim(N) = dim(M + N) + dim(M ∩ N).
尺寸（m）+尺寸（n）=dim（m+n）+尺寸（m n）。
Then the following proposition is easily shown.
那么下面的命题就很容易地显示出来了。
Proposition 25.1. Given a projective space P(E), for any two projective subspaces U,V of
提案25.1.给定射影空间p（e），对于任意两个射影子空间u，v
P(E), we have dim(U) + dim(V ) = dim(hU ∪ V i) + dim(U ∩ V ).
p（e），我们有dim（u）+dim（v）=dim（hu v i）+dim（u v）。
Furthermore, if dim(U)+dim(V ) ≥ dim(P(E)), then U∩V is nonempty and if dim(P(E)) = n, then:
此外，如果dim（u）+dim（v）≥dim（p（e）），则u v为非空，如果dim（p（e））=n，则：
(i)	The intersection of any n hyperplanes is nonempty.
任何n个超平面的交集都是非空的。
(ii)	For every hyperplane H and every point a /∈ H, every line D containing a intersects H in a unique point.
对于每一个超平面h和每一个点a/∈h，每一条包含一个相交点h的线d。
(iii)	In a projective plane, every two distinct lines intersect in a unique point.
在射影平面中，每两条不同的线在一个唯一的点上相交。
As a corollary, in 3D projective space (dim(P(E)) = 3), for every plane H, every line not contained in H intersects H in a unique point.
作为推论，在三维投影空间（dim（p（e））=3）中，对于每个平面h，h中不包含的每一条线与h在一个唯一点相交。
It is often useful to deal with projective hyperplanes in terms of nonnull linear forms and equations. Recall that the map
用非零线性形式和方程来处理射影超平面通常是有用的。回想一下地图
[f]∼ 7→ Kerf
[f]7→切口
25.3. PROJECTIVE SUBSPACES
25.3。射影子空间
is a bijection between P(E∗) and the set of hyperplanes in E, mapping the equivalence class [f]∼ = {λf | λ = 06 } of a nonnull linear form f ∈ E∗ to the hyperplane H = Kerf. Furthermore, if u ∼ v, which means that u = λv for some λ = 06 , we have
是p（e）和e中超平面集之间的双射，将非零线性形式f e的等价类[f]λfλ=06映射到超平面h=kerf。此外，如果u～v，也就是说，对于某些λ=06，u=λv，我们有
	f(u) = 0	iff	f(v) = 0,
f（u）=0 iff（v）=0，
since f(v) = λf(u) and λ = 06	. Thus, there is a bijection
因为f（v）=λf（u）和λ=06。因此，有一个双射
	{λf | λ = 06	} 7→ P(Kerf)
λfλ=06_7→p（切口）
mapping points in P(E∗) to hyperplanes in P(E). Any nonnull linear form f associated with some hyperplane P(H) in the above bijection (i.e., H = Kerf) is called an equation of the projective hyperplane P(H). We also say that f = 0 is the equation of the hyperplane P(H).
将p（e）中的点映射到p（e）中的超平面。任何与上述双射（即H=kerf）中某些超平面P（H）相关的非零线性形式F称为投影超平面P（H）的方程。我们还说f=0是超平面p（h）的方程。
Before ending this section, we give an example of a projective space where lines have a nontrivial geometric interpretation, namely as “pencils of lines.” If E = R3, recall that the dual space E∗ is the set of all linear maps f : R3 → R. As we have just explained, there is a bijection p(f) 7→ P(Kerf)
在结束这一节之前，我们给出一个投影空间的例子，其中线条有一个非平凡的几何解释，即“线条的铅笔”。如果e=r3，回想一下双空间e是所有线性映射的集合f:r3→r。正如我们刚才解释的，有一个双射p（f）。7→P（切口）
between P(E∗) and the set of lines in P(E), mapping every point a∗ = p(f) to the line Da∗ = P(Kerf).
在p（e）和p（e）中的一组线之间，将每个点a=p（f）映射到线da=p（切口）。
Is there a way to give a geometric interpretation in P(E) of a line ∆ in P(E∗)? Well, a line ∆ in P(E∗) is defined by two distinct points a∗ = p(f) and b∗ = p(g), where f,g ∈ E∗ are two linearly independent linear forms. But f and g define two distinct planes H1 = Kerf and H2 = Kerg through the origin (in E = R3), and H1 and H2 define two distinct lines
有没有办法用p（e）来解释∆in p（e）线的几何意义？那么，p（e）中的线∆由两个不同的点a=p（f）和b=p（g）定义，其中f，g e是两个线性无关的线性形式。但是f和g定义了两个不同的平面h1=kerf和h2=kerg通过原点（e=r3），h1和h2定义了两条不同的线
D1 = p(H1) and D2 = p(H2) in P(E). The line ∆ in P(E∗) is of the form ∆ = p(V ), where
d1=p（h1），d2=p（h2）in p（e）。p（e）中的线∆的形式为∆=p（v），其中
V = {λf + µg | λ,µ ∈ R}
V=λf+_gλ，_
is the plane in E∗ spanned by f,g. Every nonnull linear form λf + µg ∈ V defines a plane H = Ker(λf + µg) in E, and since H1 and H2 (in E) are distinct, they intersect in a line L that is also contained in every plane H as above. Thus, the set of planes in E associated with nonnull linear forms in V is just the set of all planes containing the line L. Passing to P(E) using the projection p, the line L in E corresponds to the point c = p(L) in P(E), which is just the intersection of the lines D1 and D2. Thus, every point of the line ∆ in P(E∗) corresponds to a line in P(E) passing through c (the intersection of the lines D1 and D2), and this correspondence is bijective.
是e中被f，g所跨越的平面。每一个非零线性形式λf+μg∈v定义了e中的平面h=ker（λf+μg），并且由于h1和h2（e中）是不同的，它们相交于L线，也包含在上述每个平面h中。因此，与v中的非零线性形式相关联的e中的一组平面只是包含线l的所有平面的集合。通过投影p传递到p（e），e中的线l对应于p（e）中的点c=p（l），即线d1和d2的交点。因此，直线∆in p（e）的每一点对应于通过c（直线d1和d2的交点）的P（e）中的一条直线，并且这种对应是双射的。
In summary, a line ∆ in P(E∗) corresponds to the set of all lines in P(E) through some given point. Such sets of lines are called pencils of lines and are illustrated in Figure 25.6.
总之，p（e）中的一行∆对应于p（e）中通过某个给定点的所有行的集合。这组线条称为铅笔线条，如图25.6所示。
The above discussion can be generalized to higher dimensions and is discussed quite extensively in Section 25.12. In brief, letting E = Rn+1, there is a bijection mapping points in P(E∗) to hyperplanes in P(E). A line in P(E∗) corresponds to a pencil of hyperplanes in
上述讨论可概括为更高的维度，并在第25.12节中进行了广泛讨论。简而言之，假设e=rn+1，在p（e）中有一个双射映射点到p（e）中的超平面。p（e）中的一条线对应于

Figure 25.6: A pencil of lines through c in the hyperplane model of RP2
图25.6:rp2超平面模型中穿过c的一束线
P(E), i.e., the set of all hyperplanes containing some given projective subspace W = p(V ) of dimension n − 2. For n = 3, a pencil of planes in RP3 = P(R4) is the set of all planes (in RP3) containing some given line W. Other examples of unusual projective spaces and pencils will be given in Section 25.4.
p（e），即包含一些给定投影子空间的所有超平面的集合，w=p（v），尺寸n-2。对于n=3，rp3=p（r4）中的平面铅笔是包含一些给定的线w的所有平面的集合（在rp3中）。第25.4节将给出其他不寻常投影空间和铅笔的示例。
Next, we define the projective analogues of bases (or frames) and linear maps.
接下来，我们定义基（或帧）和线性映射的投影类似物。
25.4	Projective Frames
25.4投影框架
As all good notions in projective geometry, the concept of a projective frame turns out to be uniquely defined up to a scalar.
正如射影几何中所有好的概念一样，射影框架的概念被唯一地定义为一个标量。
Definition 25.3. Given a nontrivial vector space E of dimension n+1, a family (ai)1≤i≤n+2 of n + 2 points of the projective space P(E) is a projective frame (or basis) of P(E) if there exists some basis (e1,...,en+1) of E such that ai = p(ei) for 1 ≤ i ≤ n + 1, and an+2 = p(e1 + ··· + en+1). Any basis with the above property is said to be associated with the projective frame (ai)1≤i≤n+2.
定义25.3.给定一个维数n+1的非平凡向量空间e，射影空间p（e）的n+2点的族（a i）1≤i≤n+2是p（e）的射影框架（或基），如果e存在一些基（e1，…，en+1），使得ai=p（ei）对于1≤i≤n+1，an+2=p（e1+·····+en+1）。具有上述性质的任何基被称为与射影框架（ai）1≤i≤n+2相关。
The justification of Definition 25.3 is given by the following proposition.
定义25.3的理由由以下命题给出。
Proposition 25.2. If (ai)1≤i≤n+2 is a projective frame of P(E), for any two bases (u1,..., un+1), (v1,...,vn+1) of E such that ai = p(ui) = p(vi) for 1 ≤ i ≤ n + 1, and an+2 = p(u1 + ··· + un+1) = p(v1 + ··· + vn+1), there is a nonzero scalar λ ∈ K such that vi = λui, for all i, 1 ≤ i ≤ n + 1.
提案25.2.如果（a i）1≤i≤n+2是p（e）的投影框架，对于e的任意两个基（u1，…，un+1），（v1，…，vn+1），使得ai=p（ui）=p（vi）对于1≤i≤n+1，and an+2=p（u1+·············+un+1）=p（v1+············+vn+1），存在一个非零的标量λ∈k，使得vi=λui，对于所有i，1≤i≤n
Proof. Since p(ui) = p(vi) for 1 ≤ i ≤ n + 1, there exist some nonzero scalars λi ∈ K such that vi = λiui for all i, 1 ≤ i ≤ n + 1. Since we must have
证据。由于p（ui）=p（vi）对于1≤i≤n+1，存在一些非零标度λi∈k，因此对于所有i，1≤i≤n+1，vi=λiui。因为我们必须
p(u1 + ··· + un+1) = p(v1 + ··· + vn+1),
p（u1+·····+un+1）=p（v1+····+vn+1）

there is some λ = 06	such that
有一些λ=06这样
λ(u1 + ··· + un+1) = v1 + ··· + vn+1 = λ1u1 + ··· + λn+1un+1,
λ（u1+····+un+1）=v1+····+vn+1=λ1u1+···+λn+1un+1，
and thus we have
因此我们有
(λ − λ1)u1 + ··· + (λ − λn+1)un+1 = 0,
（λ−λ1）u1+····+（λ−λn+1）un+1=0，
and since (u1,...,un+1) is a basis, we have λi = λ for all i, 1 ≤ i ≤ n + 1, which implies λ1 = ··· = λn+1 = λ.	
因为（u1，…，un+1）是一个基础，我们得到所有i的λi=λ，1≤i≤n+1，这意味着λ1=····=λn+1=λ。
Proposition 25.2 shows that a projective frame determines a unique basis of E, up to a (nonzero) scalar. This would not necessarily be the case if we did not have a point an+2 such that an+2 = p(u1 + ··· + un+1).
命题25.2表明，射影框架决定了e的唯一基础，达到（非零）标量。如果我们没有一个点An+2，这样an+2=p（u1+·····+un+1），情况就不一定是这样了。
When n = 0, the projective space consists of a single point a, and there is only one projective frame, the pair (a,a). When n = 1, the projective space is a line, and a projective frame consists of any three pairwise distinct points a,b,c on this line. When n = 2, the projective space is a plane, and a projective frame consists of any four distinct points a,b,c,d such that a,b,c are the vertices of a nondegenerate triangle and d is not on any of the lines determined by the sides of this triangle. These examples of projective frames are illustrated in Figure 25.7. The reader can easily generalize to higher dimensions.
当n=0时，射影空间由单点A组成，只有一个射影帧，即对（A，A）。当n=1时，射影空间是一条直线，射影框架由这条直线上任意三对不同的点A、B、C组成。当n=2时，射影空间是一个平面，射影框架由四个不同的点a、b、c、d组成，这样a、b、c是非退化三角形的顶点，d不在由三角形边确定的任何直线上。这些投影帧的例子如图25.7所示。读者可以很容易地归纳出更高的维度。
Given a projective frame (ai)1≤i≤n+2 of P(E), let (u1,...,un+1) be a basis of E associated with (ai)1≤i≤n+2. For every a ∈ P(E), there is some u ∈ E − {0} such that
给定P（e）的投影帧（a i）1≤i≤n+2，设（u1，…，un+1）为与（ai）1≤i≤n+2相关的e的基础。对于每一个a∈p（e），有一些u∈e−0这样
a = [u]∼ = {λu | λ ∈ K − {0}},
a=[u]λuλ∈k−0，
the equivalence class of u, and the set
u的等价类和集合
{(x1,...,xn+1) ∈ Kn+1 | v = x1u1 + ··· + xn+1un+1, v ∈ [u]∼ = a}
（x1，…
of coordinates of all the vectors in the equivalence class [u]∼ is called the set of homogeneous coordinates of a over the basis (u1,...,un+1).
等价类[u]中所有向量的坐标称为A超基齐次坐标集（u1，…，un+1）。
Note that for each homogeneous coordinate (x1,...,xn+1) we must have xi = 06 for some i, 1 ≤ i ≤ n + 1, and any two homogeneous coordinates (x1,...,xn+1) and (y1,...,yn+1) for a differ by a nonzero scalar, i.e., there is some λ = 06 such that yi = λxi, 1 ≤ i ≤ n + 1. Homogeneous coordinates (x1,...,xn+1) are sometimes denoted by (x1 : ··· : xn+1), for instance in algebraic geometry.
请注意，对于每个齐次坐标（x1，…，xn+1），对于某些i，1±i＝n＋1，以及任何两个齐次坐标（x1，…，xn+1）和（y1，…，yn+1），都必须有一个非零标量，也就是说，有一些α＝06，所以i＝1，1，i＝n+1。齐次坐标（x1，…，xn+1）有时用（x1：···：xn+1）表示，例如在代数几何中。
By Proposition 25.2, any other basis (v1,...,vn+1) associated with the projective frame
根据25.2号提案，与投影框架相关的任何其他基础（v1，…，vn+1）
(ai)1≤i≤n+2 differs from (u1,...,un+1) by a nonzero scalar, which implies that the set of homogeneous coordinates of a ∈ P(E) over the basis (v1,...,vn+1) is identical to the set of homogeneous coordinates of a ∈ P(E) over the basis (u1,...,un+1). Consequently, we can associate a unique set of homogeneous coordinates to every point a ∈ P(E) with respect to the projective frame (ai)1≤i≤n+2. With respect to this projective frame, note that an+2 has homogeneous coordinates (1,...,1), and that ai has homogeneous coordinates (0,...,1,...,0), where the 1 is in the ith position, where 1 ≤ i ≤ n + 1. We summarize the above discussion in the following definition.
（a i）1≤i≤n+2不同于（u1，…，un+1）的非零标量，这意味着在基（v1，…，vn+1）上a∈p（e）的齐次坐标集与在基（u1，…，un+1）上a∈p（e）的齐次坐标集相同。因此，我们可以将一组唯一的齐次坐标与射影框架（a i）1≤i≤n+2的每一点a∈p（e）关联起来。关于这个射影框架，注意+2有齐次坐标（1，…，1），而ai有齐次坐标（0，…，1，…，0），其中1在第i个位置，其中1≤i≤n+1。我们将上述讨论概括为以下定义。

P0
P0
	K	a
K A

Figure 25.7: The projective frames for projective spaces of dimension 1, 2, and 3.
图25.7：尺寸1、2和3的投影空间的投影框架。
Definition 25.4. Given a nontrivial vector space E of dimension n + 1, for any projective frame (ai)1≤i≤n+2 of P(E) and for any point a ∈ P(E), the set of homogeneous coordinates of a with respect to (ai)1≤i≤n+2 is the set of (n + 1)-tuples
定义25.4.给定一个维数为n+1的非平凡向量空间e，对于p（e）的任何投影框（a i）1≤i≤n+2，对于任意点a∈p（e），a相对于（ai）1≤i≤n+2的齐次坐标集是（n+1）-元组集。
{(λx1,...,λxn+1) ∈ Kn+1 | xi = 06 for some i, λ = 06 , a = p(x1u1 + ··· + xn+1un+1)}, where (u1,...,un+1) is any basis of E associated with (ai)1≤i≤n+2.
{（S1x1，…，Lax xn+ 1）kn+1＝1＝06，对于一些i，s＝06，a= p（x1u1+···+xn+1un+1）}，其中（u1，…，un+1）是与（ai）1 i i＝n+2相关联的E的任何基础。
Given a projective frame (ai)1≤i≤n+2 for P(E), if (x1,...,xn+1) are homogeneous coordinates of a point a ∈ P(E), we write a = (x1,...,xn+1), and with a slight abuse of language, we may even talk about a point (x1,...,xn+1) in P(E) and write (x1,...,xn+1) ∈ P(E).
对于p（e），如果（x1，…，xn+1）是点A∈p（e）的齐次坐标，我们可以在p（e）中写a=（x1，…，xn+1），并且稍微滥用语言，我们甚至可以在p（e）中谈论点（x1，…，xn+1）并写（x1，…，xn+1）∈p（e）。
The special case of the projective line P1K is worth examining. The projective line P1K consists of all equivalence classes [x,y] of pairs (x,y) ∈ K2 such that (x,y) = (06 ,0), under the equivalence relation ∼ defined such that
投影线p1k的特殊情况值得研究。投影线p1k由对（x，y）的所有等价类[x，y]组成，因此（x，y）=（06，0），在等价关系下定义如下：
	(x1,y1) ∼ (x2,y2)	iff	x2 = λx1	and	y2 = λy1,
（x1，y1）（x2，y2）iff x2=λx1和y2=λy1，
for some λ ∈ K−{0}. When y = 06 , the equivalence class of (x,y) contains the representative (xy−1,1), and when y = 0, the equivalence class of (x,0) contains the representative (1,0).
对于某些λ∈k−0。当y=06时，（x，y）的等价类包含代表（xy−1,1），当y=0时，（x，0）的等价类包含代表（1,0）。
Thus, there is a bijection between K and the set of equivalence classes containing some representative of the form (x,1), and we denote the class [x,1] by x. The equivalence class [1,0] is denoted by ∞ and it is called the point at infinity. Thus, the projective line P1K is in bijection with K ∪ {∞}. The three points ∞ = [1,0], 0 = [0,1], and 1 = [1,1], form a projective frame for P1K. The projective frame (∞,0,1) is often called the canonical frame of P1K.
因此，在k和包含形式（x，1）的一些代表性的等价类集合之间有一个双射，我们用x表示类[x，1]。等价类[1,0]用∞表示，它被称为无穷远处的点。因此，投影线p1k是K∞的双射。三个点∞=[1,0]、0=[0,1]和1=[1,1]构成p1k的投影帧。投影帧（∞，0,1）通常称为p1k的规范帧。
Homogeneous coordinates are also very useful to handle hyperplanes in terms of equations. If (ai)1≤i≤n+2 is a projective frame for P(E) associated with a basis (u1,...,un+1) for E, a nonnull linear form f is determined by n + 1 scalars α1,...,αn+1 (not all null), and a point x ∈ P(E) of homogeneous coordinates (x1,...,xn+1) belongs to the projective hyperplane P(H) of equation f iff
齐次坐标对于处理方程中的超平面也非常有用。如果（a i）1≤i≤n+2是与e的基（u1，…，un+1）相关联的p（e）的投影框架，则非零线性形式f由n+1标量α1，…，αn+1（并非全部为零）确定，且齐次坐标（x1，…，xn+1）的点x∈p（e）属于方程f的投影超平面p（h）敌我识别
α1x1 + ··· + αn+1xn+1 = 0.
α1X1+····+αN+1XN+1=0.
In particular, if P(E) is a projective plane, a line is defined by an equation of the form αx + βy + γz = 0. If P(E) is a projective space, a plane is defined by an equation of the form αx + βy + γz + δw = 0.
特别地，如果p（e）是一个投影平面，直线由αx+βy+γz=0形式的方程定义。如果p（e）是投影空间，平面由αx+βy+γz+δw=0形式的方程定义。
As an application, let us find the coordinates of the intersection point of two distinct lines in a projective plane P(E) (with respect to some projective frame (a1,a2,a3,a4)). If D and D0 are two lines of equations
作为一个应用，让我们找出投影平面p（e）中两条不同直线的交点坐标（相对于某个投影框架（a1、a2、a3、a4））。如果d和d0是两行方程
	αx + βy + γz = 0	and	α0x + β0y + γ0z = 0,	(∗)
αx+βy+γz=0和αx+β0y+γ0z=0，（）
then D and D0 are distinct lines iff the matrix
然后d和d0是矩阵上的不同线

has rank 2. We claim that the intersection Q of the lines D and D0 has homogeneous coordinates
排名2。我们认为d和d0线的交点q具有齐次坐标。
	(βγ0 − β0γ: γα0 − γ0α: αβ0 − α0β);	(†)
（βγ0−β0γ：γα0−γ0α：αβ0−α0β）；（†）
in other words, it is the projective point corresponding to the cross-product
换句话说，它是与叉积相对应的投影点。
 ,
，
as illustrated in Figure 25.8.
如图25.8所示。
Indeed, the homogeneous coordinates of the intersection Q of D and D0 must satisfy simultaneously the two equations (∗), and since the two determinants
实际上，d和d0交点q的齐次坐标必须同时满足这两个方程（），因为这两个行列式
		and	
和


Figure 25.8: The intersection of two projective lines in the projective plane P(E) is the cross product of the normals for the two corresponding planes in R3.
图25.8：投影平面p（e）中两条投影线的交点是r3中两个对应平面的法线的交叉积。
are zero because they have two equal rows, and since by expanding these determinants with respect to their first row using the Laplace expansion formula we get
是零，因为它们有两个相等的行，并且通过使用拉普拉斯展开式对这些行列式的第一行展开，我们得到

and
和
,
，
which confirms that the point
这证实了这一点
Q = (βγ0 − β0γ: γα0 − γ0α: αβ0 − α0β)
Q=（βγ0−β0γ：γα0−γ0α：αβ0−α0β）
satisfies both equations in (∗), and thus belongs to both lines D and D0. Since the matrix
满足（）中的两个方程，因此属于第d行和第d0行。因为矩阵

has rank 2, at least one of the coordinates of Q is nonzero, so Q is indeed a point in the projective plane, and it is the intersection of the lines D and D0.
有秩2，q的坐标中至少有一个是非零的，所以q确实是射影平面中的一个点，它是d和d0线的交点。
The result that we just proved yields the following criterion for three lines D,D0,D00 in a projective plane to pass through a common point (to be concurrent). In a projective plane, three lines D,D0,D00 of equations
我们刚刚证明的结果给出了射影平面上三条线d，d0，d00通过一个公共点（要同时）的下列准则。在射影平面上，方程的三行d、d0、d00
αx + βy + γz = 0 α0x + β0y + γ0z = 0 α00x + β00y + γ00z = 0
αx+βy+γz=0αx+β0y+γ0z=0α00x+β00y+γ00z=0
are concurrent iff
是同时的iff
.
.
We can also find the equation of the unique line D = hP,P 0i passing through two distinct points P = (u: v: w) and P 0 = (u0 : v0 : w0) of a projective plane. This line is given by the equation
我们还可以找到唯一线d=hp，p 0i通过投影平面的两个不同点p=（u:v:w）和p 0=（u0:v0:w0）的方程。这条线由公式给出
	,	(††)
，（††）
and since
从那以后
has rank 2 because P =6 P 0, at least one of the coordinates of the equation (††) is nonzero. Observe that the coefficients of the equation (††) correspond to the cross-product
排名为2，因为p=6 p 0，方程式（††）的至少一个坐标为非零。请注意，方程式（††）的系数与叉积相对应。
 .
.
The equation of the line D = hP,P 0i must be satisfied by the homogeneous coordinates of the points P and P 0. Equation (††) can be written as
线d=hp，p 0i的方程必须由点p和p 0的齐次坐标来满足。方程式（††）可写为
,
，
and a reasoning as in the case of the intersection of lines shows that the equation of the line passing through P and P 0 is given by equation (††).
在直线交叉的情况下的推理表明，通过P和P 0的直线方程由方程（††）给出。
Then, in a projective plane, three points P = (u: v: w), P 0 = (u0 : v0 : w0) and P 00 = (u00 : v00 : w00) belong to a common line (are collinear) iff
然后，在投影平面中，三个点p=（u:v:w），p 0=（u0:v0:w0）和p 00=（u00:v00:w00）属于公共线（共线）。
.
.
More generally, in a projective space P(E) of dimension n ≥ 2, if n points P1,...,Pn are projectively independent and if Pi has homogeneous coordinates ( ) (with respect to some projective frame (a1,...,an+2)), then the equation of the unique hyperplane
一般来说，在尺寸n≥2的射影空间p（e）中，如果n点p1，…，pn是射影独立的，如果pi有齐次坐标（）（相对于某些射影框架（a1，…，an+2）），那么唯一超平面的方程
H containing P1,...,Pn is given by the equation
含p1，…，pn的h由公式给出。
.
.
We also have the following proposition giving another characterization of projective frames.
我们也有下面的命题，给出了射影框架的另一个特征。
Proposition 25.3. A family (ai)1≤i≤n+2 of n+2 points is a projective frame of P(E) iff for every i, 1 ≤ i ≤ n + 2, the subfamily (aj)j6=i is projectively independent.
提案25.3.n+2点的族（a i）1≤i≤n+2是p（e）iff的投影框架，对于每个i，1≤i≤n+2，子族（aj）j6=i是投影独立的。
Proof. We leave as an (easy) exercise the fact that if (ai)1≤i≤n+2 is a projective frame, then each subfamily (aj)j=6 i is projectively independent. Conversely, pick some ui ∈ E −{0} such that ai = p(ui), 1 ≤ i ≤ n + 2. Since (aj)j6=n+2 is projectively independent, (u1,...,un+1) is a basis of E. Thus, we must have
证据。作为一个简单的练习，如果（a i）1≤i≤n+2是一个投影帧，那么每个子族（a j）j=6i都是投影独立的。相反，选择一些ui∈e−0这样ai=p（ui），1≤i≤n+2。因为（aj）j6=n+2是投影独立的，（u1，…，un+1）是e的基础，所以我们必须
un+2 = λ1u1 + ··· + λn+1un+1,
un+2=λ1u1+····+λn+1un+1，
for some λi ∈ K. However, since for every i, 1 ≤ i ≤ n+1, the family (aj)j=6i is projectively independent, we must have λi = 06 , and thus (λ1u1,...,λn+1un+1) is also a basis of E, and since
对于某些λi∈k，但是，由于对于每个i，1≤i≤n+1，族（a j）j=6i是投影独立的，我们必须有λi=06，因此（λ1u1，…，λn+1un+1）也是e的基础，并且
un+2 = λ1u1 + ··· + λn+1un+1,
un+2=λ1u1+····+λn+1un+1，
it induces the projective frame (ai)1≤i≤n+2.	
它诱导投影框（ai）1≤i≤n+2。
Figure 25.9 shows a projective frame (a,b,c,d) in a projective plane. With respect to this projective frame, the points a,b,c,d have homogeneous coordinates (1,0,0), (0,1,0), (0,0,1), and (1,1,1). Let a0 be the intersection of hd,ai and hb,ci, b0 be the intersection of hd,bi and ha,ci, and c0 be the intersection of hd,ci and ha,bi. Then the points a0,b0,c0 have homogeneous coordinates (0,1,1), (1,0,1), and (1,1,0). The diagram formed by the line segments ha,c0i, ha,b0i, hb,b0i, hc,c0i, ha,di, and hb,ci is sometimes called a M¨obius net; see Hilbert and Cohn-Vossen [90] (Chapter III, §15, page 96).
图25.9显示了射影平面中的射影框架（A、B、C、D）。关于这个射影框架，点A、B、C、D具有齐次坐标（1,0,0）、（0,1,0）、（0,0,1）和（1,1,1）。设a0为hd、ai和hb的交点，ci、b0为hd、bi和ha、ci和c0的交点，hd、ci和ha、bi的交点。然后点a0，b0，c0具有齐次坐标（0,1,1），（1,0,1）和（1,1,0）。由线段ha、c0i、ha、b0i、hb、b0i、hc、c0i、ha、di和hb、ci组成的图有时称为m-obius网；见Hilbert和Cohn Vossen[90]（第三章，第15节，第96页）。
Recall that the equation of a line (a hyperplane in a projective plane) in terms of homogeneous coordinates with respect to the projective frame (a,b,c,d) is given by a homogeneous equation of the form
回想一下，关于射影框架（a，b，c，d），直线（射影平面中的超平面）的齐次坐标方程由形式的齐次方程给出。
αx + βy + γz = 0,
αx+βy+γz=0，
where α,β,γ are not all zero. It is easily verified that the equations of the lines ha,bi, ha,ci, hb,ci, are z = 0, y = 0, and x = 0, and the equations of the lines ha,di, hb,di, and hc,di,
其中α，β，γ不都是零。可以很容易地证明线Ha、Bi、Ha、Ci、Hb、Ci的方程为z=0、y=0和x=0，线Ha、Di、Hb、Di和hc、Di的方程为：

Figure 25.9: A projective frame (a,b,c,d).
图25.9：投影框架（A、B、C、D）。
are y = z, x = z, and x = y. The equations of the lines ha0,b0i, ha0,c0i, hb0,c0i are z = x + y, y = x + z, and x = y + z.
是y=z，x=z，x=y。线的方程式ha0，b0i，ha0，c0i，hb0，c0i是z=x+y，y=x+z，x=y+z。
If we let e be the intersection of hb,ci and hb0,c0i, f be the intersection of ha,ci and ha0,c0i,
如果e是hb，ci和hb0的交点，c0i，f是ha，ci和ha0，c0i的交点，
−	− h
-小时
handcoordinates (0which correspond to the homogeneous coordinates (0b,cigisbe the intersection ofx = 0,and the equation of the line1,1), (1,0,ha,b1)i, andand h(a−0,b1,0i1, then it easily seen that,0)b0,c. For example, since the equation of the line0i is ,x−=1,y1)+forz, fore. e,f,gx = 0have homogeneous, we get z = −y,
手坐标（0对应于齐次坐标（0b，cigisbe，x=0的交点，1,1），（1,0，h a，b1）i，and h（a−0，b1,0i 1，那么很容易看出，0）b0，c。例如，由于0的线方程是，x−=1，y1）+forz，fore。e，f，gx=0具有同质性，我们得到z=−y，
The coordinates of the points e,f,g satisfy the equation x+y +z = 0, which shows that they are collinear.
点E、F、G的坐标满足方程x+y+z=0，表明它们共线。
As pointed out in Coxeter [45] (Proposition 2.41), this is a special case of the projective version of Desargues’s theorem (Proposition 25.7) applied to the triangles (a,b,c) and
如coxeter[45]中所指出的（命题2.41），这是德沙格定理（命题25.7）的射影版本应用于三角形（a，b，c）和
(pointa0,b0,cd0. The line containing the points). Indeed, by construction, the linese,f,gha,ais called the0i, hb,b0i, andpolar line (or fundamental line)hc,c0i intersect in the common of d with respect to the triangle (a,b,c) (see Pedoe [132]). The diagram also shows the intersection g of ha,bi and ha0,b0i.
（点a0，b0，cd0.包含点的线）。实际上，通过构造，线se、f、gha、ais称为0i、hb、b0i和极线（或基本线）hc、c0i与三角形（a、b、c）在d的公共部分相交（见pedoe[132]）。图中还显示了ha、bi和ha0、b0i的交叉点g。
The projective space of circles provides a nice illustration of homogeneous coordinates.
圆的射影空间为均匀坐标提供了一个很好的说明。
Let E be the vector space (over R) consisting of all homogeneous polynomials of degree 2 in x,y,z of the form
设e为向量空间（在r上），由x，y，z形式中2次的所有齐次多项式组成。
ax2 + ay2 + bxz + cyz + dz2
轴2+AY2+BXZ+CyZ+DZ2
(plus the null polynomial). The projective space P(E) consists of all equivalence classes
（加上零多项式）。射影空间p（e）由所有等价类组成。
	[P]∼ = {λP | λ = 06	},
[p]λpλ=06，
where P(x,y,z) is a nonnull homogeneous polynomial in E. We want to give a geometric interpretation of the points of the projective space P(E). In order to do so, pick some projective frame (a1,a2,a3,a4) for the projective plane RP2, and associate to every [P] ∈ P(E) the subset of RP2 known as its its zero locus (or zero set, or variety) V ([P]), and defined such that
其中p（x，y，z）是e中的一个非零齐次多项式，我们想给出射影空间p（e）点的几何解释。为此，选取射影平面rp2的一些射影帧（a1，a2，a3，a4），并将rp2的子集（称为其零轨迹（或零集或变种）v（[p]）与每个[p]∈p（e）相关联，并定义如下：
V ([P]) = {a ∈ RP2 | P(x,y,z) = 0},
v（[p]）=a∈rp2 p（x，y，z）=0，
where (x,y,z) are homogeneous coordinates for a.
其中（x，y，z）是a的齐次坐标。
As explained earlier, we also use the simpler notation
如前所述，我们还使用更简单的符号
V ([P]) = {(x,y,z) ∈ RP2 | P(x,y,z) = 0}.
v（[p]）=（x，y，z）∈rp2 p（x，y，z）=0。
Actually, in order for V ([P]) to make sense, we have to check that V ([P]) does not depend on the representative chosen in the equivalence class [P] = {λP | λ = 06 }. This is because
实际上，为了使v（[p]）有意义，我们必须检查v（[p]）不依赖于在等价类[p]=λpλ=06中选择的代表。这是因为
	P(x,y,z) = 0	iff	λP(x,y,z) = 0	when λ = 06	.
当λ=06时，p（x，y，z）=0 iffλp（x，y，z）=0。
For simplicity of notation, we also denote V ([P]) by V (P). We also have to check that if
为了简化表示法，我们还用v（p）表示v（[p]）。我们还要检查一下如果
(λx,λy,λz) are other homogeneous coordinates for a ∈ RP2, where λ = 06	, then
（λx，λy，λz）是a∈rp2的其他齐次坐标，其中λ=06，则
	P(x,y,z) = 0	iff	P(λx,λy,λz) = 0.
p（x，y，z）=0 iff p（λx，λy，λz）=0。
However, since P(x,y,z) is homogeneous of degree 2, we have
然而，由于p（x，y，z）是2级的齐次，我们有
P(λx,λy,λz) = λ2P(x,y,z),
p（λx，λy，λz）=λ2p（x，y，z）
and since λ = 06	,
既然λ=06，
	P(x,y,z) = 0	iff	λ2P(x,y,z) = 0.
p（x，y，z）=0 iffλ2p（x，y，z）=0。
The above argument applies to any homogeneous polynomial P(x1,...,xn) in n variables of any degree m, since
上述论点适用于任意m阶n变量中的任何齐次多项式p（x1，…，xn），因为
P(λx1,...,λxn) = λmP(x1,...,xn).
p（λx1，…，λxn）=λmp（x1，…，xn）。
Thus, we can associate to every [P] ∈ P(E) the curve V (P) in RP2. One might wonder why we are considering only homogeneous polynomials of degree 2, and not arbitrary polynomials of degree 2? The first reason is that the polynomials in x,y,z of degree 2 do not form a vector space. For example, if P = x2 + x and Q = −x2 + y, the polynomial P + Q = x + y is not of degree 2. We could consider the set of polynomials of degree ≤ 2, which is a vector space, but now the problem is that V (P) is not necessarily well defined!.
因此，我们可以将rp2中的曲线v（p）与每一个[p]∈p（e）联系起来。我们为什么只考虑2阶的齐次多项式，而不考虑2阶的任意多项式？第一个原因是2阶的x，y，z多项式不形成向量空间。例如，如果p=x2+x且q=−x2+y，则多项式p+q=x+y不属于2阶。我们可以考虑次数≤2的多项式集，这是一个向量空间，但现在的问题是v（p）不一定定义得很好！.
For example, if P(x,y,z) = −x2 + 1, we have
例如，如果p（x，y，z）=-x2+1，我们有
	P(1,0,0) = 0	and	P(2,0,0) = −3,
P（1,0,0）=0和P（2,0,0）=3，
and yet (2,0,0) = 2(1,0,0), so that P(x,y,z) takes different values depending on the representative chosen in the equivalence class [1,0,0]. Thus, we are led to restrict ourselves to homogeneous polynomials. Actually, this is usually an advantage more than a disadvantage, because homogeneous polynomials tend to be well behaved.
然而（2,0,0）=2（1,0,0），因此p（x，y，z）根据在等价类[1,0,0]中选择的代表性取不同的值。因此，我们只能局限于齐次多项式。实际上，这通常是一个优点而不是缺点，因为齐次多项式往往表现得很好。
What are the curves V (P)? One way to “see” such curves is to go back to the hyperplane model of RP2 in terms of the plane H of equation z = 1 in R3. Then the trace of V (P) on H is the circle of equation
什么是曲线v（p）？“看到”这些曲线的一种方法是根据r3中方程式z=1的平面h回到rp2的超平面模型。那么h上v（p）的迹线就是方程的圆。
ax2 + ay2 + bx + cy + d = 0.
ax2+ay2+bx+cy+d=0.
Thus, we may think of P(E) as a projective space of circles. However, there are some problems. For example, V (P) may be empty! This happens, for instance, for P(x,y,z) = x2 + y2 + z2, since the equation
因此，我们可以把p（e）看作是圆的投影空间。但也存在一些问题。例如，v（p）可能是空的！例如，当p（x，y，z）=x2+y2+z2时，就会出现这种情况，因为方程
x2 + y2 + z2 = 0
x2+y2+z2=0
has only the trivial solution (0,0,0), which does not correspond to any point in RP2. Indeed, only nonnull vectors in R3 yield points in RP2. It is also possible that V (P) is reduced to a single point, for instance when P(x,y,z) = x2 + y2, since the only homogeneous solution of
只有平凡解（0,0,0），它与rp2中的任何点都不对应。实际上，在r3中只有非空向量在rp2中产生点。也有可能将v（p）简化为一个点，例如当p（x，y，z）=x2+y2时，因为
x2 + y2 = 0
x2+y2=0
is (0,0,1). Also, note that the map
是（0,0,1）。另外，注意地图
[P] 7→ V (P)
[P]7→V（P）
is not injective. For instance, P = x2 + y2 and Q = x2 + 2y2 define the same degenerate circle reduced to the point (0,0,1). We also accept as circles the union of two lines, as in the case
不是注射剂。例如，p=x2+y2和q=x2+2y2定义了同一退化圆，并将其简化为点（0,0,1）。我们也接受两条线的并线作为圆，就像在这个例子中那样。
(bx + cy + dz)z = 0,
（bx+cy+dz）z=0，
where a = 0, and even a double line, as in the case
其中a=0，甚至是双行，例如
z2 = 0,
z2=0，
where a = b = c = 0.
其中a=b=c=0。
A clean way to resolve most of these problems is to switch to homogeneous polynomials over the complex field C and to consider curves in CP2. This is what is done in algebraic geometry (see Fulton [67] or Harris [86]). If P(x,y,z) is a homogeneous polynomial over C of degree 2 (plus the null polynomial), it is easy to show that V (P) is always nonempty, and in fact infinite. It can also be shown that V (P) = V (Q) implies that Q = λP for some λ ∈ C, with λ = 0 (6 see Samuel [138], Section 1.6, Theorem 10). Another advantage of switching to the complex field C is that the theory of intersection is cleaner. Thus, any two circles that do not contain a common line always intersect in four points, some of which might be multiple points (as in the case of tangent circles). This may seem surprising, since in the real plane, two circles intersect in at most two points. Where are the other two points? They turn out to be the points (1,i,0) and (1,−i,0), as one can immediately verify. We can think of them as complex points at infinity! Not only are they at infinity, but they are not real. No wonder we cannot see them! We will come back to these points, called the circular points, in Section 25.14.
解决这些问题的一个干净方法是在复场C上切换到齐次多项式，并考虑CP2中的曲线。这就是在代数几何中所做的（见Fulton[67]或Harris[86]）。如果p（x，y，z）是2次C上的齐次多项式（加上零多项式），很容易证明v（p）总是非空的，实际上是无穷大的。也可以证明，v（p）=v（q）意味着对于某些λ∈c，q=λp，其中λ=0（6见Samuel[138]，第1.6节，定理10）。切换到复场C的另一个优点是交集理论更清晰。因此，任何不包含公共线的两个圆总是在四个点上相交，其中一些点可能是多个点（如切线圆）。这可能看起来很奇怪，因为在实际平面上，两个圆最多相交两个点。其他两点在哪里？它们被证明是点（1，i，0）和（1，−i，0），正如人们可以立即验证的那样。我们可以把它们看作无穷远处的复杂点！它们不仅是无穷大的，而且不是真实的。难怪我们看不见他们！我们将在第25.14节中回到这些点，即圆形点。
Going back to the vector space E of circles over R, it is worth saying that it can be shown that if V (P) = V (Q) contains at least two points (in which case, V (P) is actually infinite), then Q = λP for some λ ∈ R with λ = 0 (6 see Tisseron [170], Theorem 3.6.1 and Theorem 4.7). Thus, even over R, the mapping
回到r上的圆的向量空间e，值得说明的是，如果v（p）=v（q）至少包含两个点（在这种情况下，v（p）实际上是无限的），那么对于某些λ∈r，q=λp，其中λ=0（6见Tisseron[170]、定理3.6.1和定理4.7）。因此，即使在R上，映射
[P] 7→ V (P)
[P]7→V（P）
is injective whenever V (P) is neither empty nor reduced to a single point. Note that the projective space P(E) of circles has dimension 3. In fact, it is easy to show that three distinct points that are not collinear determine a unique circle (see Samuel [138], Section 1.6).
当v（p）既不是空的，也不是减少到一个点时，是注射的。注意圆的射影空间p（e）有维3。事实上，很容易证明三个不共线的不同点决定了一个唯一的圆（见塞缪尔[138]第1.6节）。
In a similar vein, we can define the projective space of conics P(E) where E is the vector space (over R) consisting of all homogeneous polynomials of degree 2 in x,y,z,
在类似的纹理中，我们可以定义二次曲线p（e）的投影空间，其中e是向量空间（在r上），它由x、y、z中2阶的所有齐次多项式组成。
ax2 + by2 + cxy + dxz + eyz + fz2
ax2+by2+cxy+dxz+eyz+fz2
(plus the null polynomial). The curves V (P) are indeed conics, perhaps degenerate. To see this, we can use the hyperplane model of RP2. The trace of V (P) on the plane of equation z = 1 is the conic of equation
（加上零多项式）。曲线v（p）确实是二次曲线，可能是退化的。为了看到这一点，我们可以使用RP2的超平面模型。方程z=1平面上v（p）的迹线是方程的二次曲线。
ax2 + by2 + cxy + dx + ey + f = 0.
ax2+by2+cxy+dx+ey+f=0.
Another way to see that V (P) is a conic is to observe that in R3,
另一种观察v（p）是二次曲线的方法是观察r3中，
ax2 + by2 + cxy + dxz + eyz + fz2 = 0
ax2+by2+cxy+dxz+eyz+fz2=0
defines a cone with vertex (0,0,0), and since its section by the plane z = 1 is a conic, all of its sections by planes are conics. See Figure 25.10 for schematic illustration of a projective conic embedded in RP2.
定义一个顶点为（0,0,0）的圆锥体，由于其平面截面z=1是一个圆锥体，因此其所有平面截面都是圆锥体。有关嵌入在RP2中的投影圆锥图的示意图，请参见图25.10。
The mapping
地图
[P] 7→ V (P)
[P]7→V（P）
is still injective when E is defined over the ground field C (Samuel [138], Section 1.6, Theorem 10), or if V (P) has at least two points when E is defined over R (Tisseron [170], Theorem 3.6.1 and Theorem 4.7). Note that the projective space P(E) of conics has dimension 5. In fact, it can be shown that five distinct points, no four of which are collinear, determine a
当e在地磁场c上定义时（塞缪尔[138]，第1.6节，定理10），或者当e在r上定义时，如果v（p）至少有两个点（Tisseron[170]，定理3.6.1和定理4.7），则仍然是内射的。注意二次曲线的射影空间p（e）的尺寸为5。事实上，可以证明五个不同的点，其中没有四个共线，决定了

Figure 25.10: A three step process for constructing V (P) where P is the homogenous conic xy = z. In Step 2, we convert to homogenous coordinates via the transformation x → x/z, y → y/z.
图25.10：构建v（p）的三步过程，其中p是均匀二次曲线x y=z。在步骤2中，我们通过变换x→x/z，y→y/z转换为均匀坐标。
unique conic (among many sources, see Samuel [138], Section 1.7, Theorem 17, or Coxeter [45], Theorem 6.56, where a geometric construction is given in Section 6.6).
唯一二次曲线（在许多来源中，见Samuel[138]，第1.7节，定理17，或Coxeter[45]，定理6.56，其中几何结构在第6.6节中给出）。
In fact, if we pick a projective frame (a1,a2,a3,a4) in CP2 (or RP2), and if the five points p1,p2,p3,p4,p5 have homogeneous coordinates pi = (xi,yi,zi) for i = 1,...,5 and (x,y,z) are variables, then it is an easy exercise to show that the equation of the unique conic C passing through the points p1,p2,p3,p4,p5 is given by
事实上，如果我们在CP2（或RP2）中选择一个射影帧（A1，A2，A3，A4），并且如果五点P1、P2、P3、P4、P5具有I＝1、…、5和（x，y，z）的齐次坐标PI=（Xi，Yi，Zi）是变量，那么这是一个简单的练习来证明唯一的圆锥曲线通过这些点的方程。p1，p2，p3，p4，p5由下式给出
.
.
The polynomial obtained by expanding the above determinant according to the first row is a homogeneous polynomial of degree 2 in the variables x,y,z, and it is not the zero polynomial because the 5×6 matrix obtained by deleting the first row in the matrix of the determinant has rank 5. Indeed, this is the matrix of the linear system determining the six coefficients of the conic passign through p1,p2,p3,p4,p5 (up to a scalar), and since this conic is unique, this matrix must have rank 5.
根据第一行展开上述行列式得到的多项式是变量x、y、z中二次齐次多项式，且不是零多项式，因为通过删除行列式矩阵中第一行得到的5×6矩阵具有秩5。实际上，这是线性系统的矩阵，通过p1、p2、p3、p4、p5（最高为一个标量）确定二次曲线通过的六个系数，由于这个二次曲线是唯一的，所以这个矩阵必须具有秩5。
It is also interesting to see what are lines in the space of circles or in the space of conics. In both cases we get pencils (of circles and conics, respectively). For more details, see Samuel [138], Sidler [156], Tisseron [170], Lehmann and Bkouche [112], Pedoe [132], Coxeter [45, 46], and Veblen and Young [177, 178].
同样有趣的是，在圆的空间或圆锥曲线的空间中，线条是什么。在这两种情况下，我们都会得到铅笔（分别是圆和圆锥曲线）。有关详细信息，请参阅Samuel[138]、Sidler[156]、Tisseron[170]、Lehmann和Bkouche[112]、Pedoe[132]、Coxeter[45、46]和Veblen and Young[177、178]。
The generalization of the space of projective conics is the space of projective quadrics P(E), where E is the vector space (over a field K, typically K = R or K = C) consisting of all homogeneous polynomials P(x1,...,xN+1) of degree 2 in the variables x1,...,xN+1, with N ≥ 3 (plus the null polynomial). The zero locus V (P) of P is defined just as before as
射影二次曲线的空间的推广是射影四次曲线的空间p（e），其中e是向量空间（在场k上，通常k=r或k=c），由变量x1，…，xn+1中2阶的所有齐次多项式p（x1，…，xn+1）组成，n≥3（加上零多项式MIAL）。p的零轨迹v（p）的定义与之前一样
V (P) = {(x1 : ··· : xN+1) ∈ PNK | P(x1,...,xN+1) = 0}.
v（p）=（x1：···：xn+1）∈pnk p（x1，…，xn+1）=0。
If the field K is algebraically closed, in particular if K = C, then V (P) = V (Q) implies that there is some nonzero λ ∈ K such that Q = λP; see Berger [12] (Chapter 14, Theorem
如果场k是代数闭合的，特别是如果k=c，那么v（p）=v（q）意味着存在一些非零的λ∈k，这样q=λp；参见Berger[12]（第14章，定理
14.1.6.2).
14.1.6.2条）。
Another situation where the map [P] 7→ V (P) is injective involves the notion of simple (or regular) point of a quadric. For any a = (a1 : ··· : aN+1) ∈ PNK, let Pxi(a) be the partial derivative of P at a given by
图[p]7→v（p）是内射的另一种情况涉及二次曲面的简单（或规则）点的概念。对于任意a=（a1：····：an+1）∈pnk，让pxi（a）是p在给定
.
.
Strictly speaking, Pxi(a) depends on the representative (a1,...,aN+1) ∈ KN+1 chosen for the point a, but since P is homogeneous of degree 2, for any nonzero λ ∈ K,
严格地说，pxi（a）依赖于a点所选的代表（a1，…，an+1）∈kn+1，但由于p是2阶的齐次，对于任何非零的λ∈k，
.
.
Thus Pxi(a) is defined up to a nonzero scalar. In particular, whether or not Pxi(a) = 0 depends only the point a = (a1 : ··· : aN+1) ∈ PNK. Then the point a ∈ V (P) is said to be simple (or regular) if
因此，pxi（a）被定义为非零标量。特别是，PxI（a）=0是否仅取决于点A=（a1：····：an+1）∈PNK。那么点a∈v（p）被称为简单（或规则）如果
	Pxi(a) = 06	for some i, 1 ≤ i ≤ N + 1.
pxi（a）=06，对于某些i，1≤i≤n+1。
Otherwise, if Px1(a) = ··· = PxN+1(a) = 0, we say that a ∈ V (P) is a singular point. If a ∈ V (P) is a regular point, then the tangent hyperplane TaV (P) to V (P) at a is the hyperplane given by the equation
否则，如果Px1（a）=······=Pxn+1（a）=0，我们就说a∈v（p）是一个奇异点。如果a∈v（p）是一个正则点，那么a处的切线超平面tav（p）到v（p）是由方程给出的超平面。
Px1(a)x1 + ··· + PxN+1(a)xN+1 = 0.
px1（a）x1+·····+pxn+1（a）xn+1=0。
It can be shown that if the field K is not the field F2 = {0,1} and if the quadric V (P) contains some regular point, then V (P) = V (Q) implies that there is some nonzero λ ∈ K such that Q = λP; see Samuel [138] (Chapter 3, Theorem 46).
可以证明，如果场k不是场f2=0,1，如果二次v（p）包含一些正则点，那么v（p）=v（q）意味着存在一些非零的λ∈k，这样q=λp；参见Samuel[138]（第3章，定理46）。
Quadrics, projective, affine, and Euclidean, have been thoroughly investigated. Among many sources, the reader is referred to Berger [11], Samuel [138], Tisseron [170], Fresnel [66], and Vienne [179].
四次方、射影、仿射和欧几里德已经被彻底研究过。在许多资料中，读者被称为伯杰[11]、塞缪尔[138]、蒂塞隆[170]、菲涅尔[66]和维也纳[179]。
We could also investigate algebraic plane curves of any degree m, by letting E be the vector space of homogeneous polynomials of degree m in x,y,z (plus the null polynomial). The zero locus V (P) of P is defined just as before as
我们也可以研究任意m阶的代数平面曲线，方法是让e是m阶在x，y，z（加上零多项式）中的齐次多项式的向量空间。p的零轨迹v（p）的定义与之前一样
V (P) = {(x: y: z) ∈ RP2 | P(x,y,z) = 0}.
v（p）=（x:y:z）∈rp2 p（x，y，z）=0。
Observe that when m = 1, since homogeneous polynomials of degree 1 are linear forms, we are back to the case where E = (R3)∗, the dual space of R3, and P(E) can be identified with the set of lines in RP2. But when m ≥ 3, things are even worse regarding the injectivity of the map [P] 7→ V (P). For instance, both P = xy2 and Q = x2y define the same union of two lines. It is necessary to consider irreducible curves, i.e., curves that are defined by irreducible polynomials, and to work over the field C of complex numbers (recall that a polynomial P is irreducible if it cannot be written as the product P = Q1Q2 of two polynomials Q1,Q2 of degree ≥ 1). We refer the reader to Fischer’s book for a beautiful (and very clear) introduction to algebraic curves [63]. The next step is Fulton [67].
观察到当m=1时，由于阶1的齐次多项式是线性形式，我们回到E=（r3）的情形，r3和p（e）的对偶空间可以用rp2中的一组线来标识。但当m≥3时，关于图的注入率[p]7→v（p），情况更糟。例如，p=xy2和q=x2y都定义了两条线的同一个联合。有必要考虑不可约曲线，即由不可约多项式定义的曲线，并对复数的域C进行研究（如果不能将多项式p写成两个多项式q1，q2的乘积p=q1q2，则多项式p是不可约的）。我们请读者参考费舍尔的书，了解代数曲线的美丽（非常清晰）介绍[63]。下一步是富尔顿[67]。
We can also investigate algebraic surfaces in RP3 (or CP3), by letting E be the vector space of homogeneous polynomials of degree m in four variables x,y,z,t (plus the null polynomial). We can also consider the zero locus of a set of equations
我们也可以研究rp3（或cp3）中的代数曲面，让e是四个变量x、y、z、t（加上零多项式）中m次齐次多项式的向量空间。我们也可以考虑一组方程的零轨迹。
E = {P1 = 0, P2 = 0, ..., Pn = 0},
E=p1=0，p2=0，…，pn=0，
where P1,...,Pn are homogeneous polynomials of degree m in x,y,z,t, defined as
式中，p1，…，pn是x，y，z，t中m阶的齐次多项式，定义为
V (E) = {(x: y: z: t) ∈ RP3 | Pi(x,y,z,t) = 0, 1 ≤ i ≤ n}.
v（e）=（x:y:z:t）∈rp3 pi（x，y，z，t）=0，1≤i≤n。
This way, we can also deal with space curves.
这样，我们也可以处理空间曲线。
Finally, we can consider homogeneous polynomials P(x1,...,xN+1) in N + 1 variables and of degree m (plus the null polynomial), and study the subsets of RPN or CPN (or more generally of PNK, for an arbitrary field K), defined as the zero locus of a set of equations
最后，我们可以考虑n+1变量中的齐次多项式p（x1，…，xn+1）和m阶的齐次多项式（加上零多项式），并研究rpn或cpn的子集（或更一般的p n k，对于任意场k），定义为一组方程的零轨迹。
E = {P1 = 0, P2 = 0, ..., Pn = 0},
E=p1=0，p2=0，…，pn=0，
where P1,...,Pn are homogeneous polynomials of degree m in the variables x1, ..., xN+1. For example, it turns out that the set of lines in RP3 forms a surface of degree 2 in RP5 (the Klein quadric). However, all this would really take us too far into algebraic geometry, and we simply refer the interested reader to Hulek [94], Fulton [67], and Harris [86].
式中，p1，…，pn是变量x1，…，xn+1中m阶的齐次多项式。例如，结果表明，rp3中的一组线在rp5（klein二次曲面）中形成一个2度曲面。然而，所有这一切真的会把我们带到代数几何中去太远，我们只是把感兴趣的读者引向Hulek[94]、Fulton[67]和Harris[86]。
We now consider projective maps.
我们现在考虑投影地图。
25.5	Projective Maps
25.5投影图
Given two nontrivial vector spaces E and F and a linear map f : E → F, observe that for every u,v ∈ (E − Kerf), if v = λu for some λ ∈ K − {0}, then f(v) = λf(u), and thus f restricted to (E −Kerf) induces a function P(f): (P(E)−P(Kerf)) → P(F) defined such that
给定两个非平凡向量空间e和f和一个线性映射f:e→f，观察每个u，v∈（e−kerf），如果v=λu对于一些λ∈k−0，那么f（v）=λf（u），因此f限制为（e−kerf）诱导一个函数p（f）：（p（e）−p（kerf））→p（f）定义如下：
P(f)([u]∼) = [f(u)]∼,
p（f）（[u]）=[f（u）]，
as in the following commutative diagram:
如下图所示：
f
f
	E − Kerf	/ F − {0}
E−切口/F−0
	p 	p
磷脂酶P

	P(E)P(Kerf)	/ P(F)
P（E）P（切口）/P（F）
P(f)
P（F）
When f is injective, i.e., when Kerf = {0}, then P(f): P(E) → P(F) is indeed a welldefined function. The above discussion motivates the following definition.
当f是注射剂时，即当kerf=0，那么p（f）：p（e）→p（f）确实是一个定义良好的函数。上述讨论激发了以下定义。
Definition 25.5. Given two nontrivial vector spaces E and F, any linear map f : E → F induces a partial map P(f): P(E) → P(F) called a projective map, such that if Kerf = {u ∈ E | f(u) = 0} is the kernel of f, then P(f): (P(E)−P(Kerf)) → P(F) is a total map defined such that
定义25.5.给定两个非平凡向量空间e和f，任何线性映射f:e→f都会产生一个称为投影映射的偏映射p（f）：p（e）→p（f），如果kerf=u∈e f（u）=0是f的核，那么p（f）：（p（e）−p（kerf））→p（f）是一个定义为
P(f)([u]∼) = [f(u)]∼,
p（f）（[u]）=[f（u）]，
as in the following commutative diagram:
如下图所示：
f
f
	E − Kerf	/ F − {0}
E−切口/F−0
	p 	p
磷脂酶P

	P(E)P(Kerf)	/ P(F)
P（E）P（切口）/P（F）
P(f)
P（F）
If f is injective, i.e., when Kerf = {0}, then P(f): P(E) → P(F) is a total function called
如果f是内射的，即当kerf=0时，那么p（f）：p（e）→p（f）是一个称为
a projective transformation, and when f is bijective, we call P(f) a projectivity, or projective isomorphism, or homography. The set of projectivities P(f): P(E) → P(E) is a group called the projective (linear) group, and is denoted by PGL(E).
一个射影变换，当f是双射影时，我们称p（f）为射影性，或射影同构，或同形。射影率p（f）：p（e）→p（e）是一个称为射影（线性）群的群，用pgl（e）表示。
 One should realize that if a linear map f : E → F is not injective, then the projective map P(f): P(E) → P(F) is only a partial map, i.e., it is undefined on P(Kerf). In particular, if f : E → F is the null map (i.e., Kerf = E), the domain of P(f) is empty and P(f) is the partial function undefined everywhere. We might want to require in Definition 25.5 that f not be the null map to avoid this degenerate case. Projective maps are often defined only when they are induced by bijective linear maps.
我们应该认识到，如果线性映射f:e→f不是内射的，那么投影映射p（f）：p（e）→p（f）只是局部映射，即p（kerf）上没有定义。特别是，如果f:e→f是空映射（即kerf=e），则p（f）的域为空，p（f）是处处未定义的部分函数。我们可能希望在定义25.5中要求f不是空映射以避免这种退化情况。射影映射通常只有在由双射影线性映射诱导时才被定义。

We take a closer look at the projectivities of the projective line P1K, since they play a role in the “change of parameters” for projective curves. A projectivity f : P1K → P1K is induced by some bijective linear map g: K2 → K2 given by some invertible matrix
我们更仔细地看一下投影线p1k的投影率，因为它们在投影曲线的“参数变化”中起着作用。由一些可逆矩阵给出的双射线性映射g:k2→k2，得到了f:p1k→p1k的投影性。

with ad−bc = 06 . Since the projective line P1K is isomorphic to K ∪{∞}, it is easily verified that f is defined as follows:
当ad−bc=06时。由于投影线p1k与k∞同构，很容易证明f的定义如下：
,
，
,
，
;
；
From Section 25.4, we know that the points not at infinity are repesented by vectors of the form (z,1) where z ∈ K and that ∞ is represented by (1,0). First, assume c = 06 . Since
从第25.4节中，我们知道不在无穷远处的点由形式（z，1）的向量表示，其中z∈k和∞由（1,0）表示。首先，假设c=06。自从
 ,
，
if cz + d = 06	, that is, z =6	−d/c, then
如果c z+d=06，即z=6−d/c，则
 ,
，
so z is is mapped to (az + d)/cz + d). If cz + d = 0, then
所以z映射到（az+d）/cz+d。如果cz+d=0，则
(az + d,0) ∼ (1,0) = ∞,
（az+d，0）（1,0）=∞，
so −d/c is mapped to ∞. We also have
因此−d/c映射到∞。我们也有
,
，
and since c = 06	we have
从C=06开始
(a,c) ∼ (a/c,1),
（a，c）（a/c，1）、
so ∞ is mapped to a/c. The case where c = 0 is handled similarly.
因此∞映射到A/C。C=0的情况处理类似。
If K = R or K = C, note that a/c is the limit of (az + b)/(cz + d), as z approaches infinity, and the limit of (az + b)/(cz + d) as z approaches −d/c is ∞ (when c 6= 0). Projections between hyperplanes form an important example of projectivities.
如果k=r或k=c，注意a/c是（a z+b）/（cz+d）的极限，当z接近无穷大时，（az+b）/（cz+d）的极限是∞（当c 6=0时）。超平面之间的投影是投影的一个重要例子。
Definition 25.6. Given a projective space P(E), for any two distinct hyperplanes P(H) and P(H0), for any point c ∈ P(E) neither in P(H) nor in P(H0), the projection (or perspectivity) of center c between P(H) and P(H0) is the map f : P(H) → P(H0) defined such that for every a ∈ P(H), the point f(a) is the intersection of the line hc,ai through c and a with P(H0).
定义25.6.给定一个投影空间p（e），对于任意两个不同的超平面p（h）和p（h0），对于任何点c∈p（e），无论是在p（h）还是在p（h0）中，中心c在p（h）和p（h0）之间的投影（或透视性）是映射f:p（h）→p（h0），定义为对于每一个a∈p（h），点f（a）是int。Hc、Ai至C和A线与P（H0）的截面。
Let us verify that f is well–defined and a bijective projective transformation. Since the hyperplanes P(H) and P(H0) are distinct, the hyperplanes H and H0 in E are distinct, and since c is neither in P(H) nor in P(H0), letting c = p(u) for some nonnull vector u ∈ E, then u /∈ H and u /∈ H0, and thus E = H ⊕Ku = H0 ⊕Ku. If π: E → H0 is the linear map
让我们验证f是定义良好的，并且是一个双射射影变换。由于超平面p（h）和p（h0）是不同的，所以e中的超平面h和h0是不同的，并且c既不在p（h）中也不在p（h0）中，因此对于一些非空向量u∈e，让c=p（u），那么u/∈h和u/∈h0，因此e=h ku=h0 ku。如果π：e→h0是线性映射
(projection onto H0 parallel to u) defined such that
（投影到与u平行的h0上）定义为
π(w + λu) = w,
π（w+λu）=w，
for all w ∈ H0 and all λ ∈ K, since E = H ⊕ Ku = H0 ⊕ Ku, the restriction g: H → H0 of π: E → H0 to H is a linear bijection between H and H0, and clearly f = P(g), which shows that f is a projectivity.
对于所有w∈h0和所有λ∈k，由于e=h ku=h0 ku，π：e→h0到h的约束g:h→h0是h和h0之间的线性双射，显然f=p（g），这表明f是一个投影性。
Remark: Going back to the linear map π: E → H0 (projection onto H0 parallel to u), note that P(π): P(E) → P(H0) is also a projective map, but it is not injective, and thus only a partial map. More generally, given a direct sum E = V ⊕W, the projection π: E → V onto V parallel to W induces a projective map P(π): P(E) → P(V ), and given another direct sum E = U ⊕ W, the restriction of π to U induces a perspectivity f between P(U) and P(V ). Geometrically, f is defined as follows: Given any point a ∈ P(U), if hP(W),ai is the smallest projective subspace containing P(W) and a, the point f(a) is the intersection of hP(W),ai with P(V ).
注：回到线性映射π：e→h0（投影到平行于u的h0上），注意p（π）：p（e）→p（h0）也是一个投影映射，但它不是内射的，因此只是一个局部映射。更一般地说，给定一个直和e=v_w，投影π：e→v与w平行，在v上产生一个投影图p（π）：p（e）→p（v），再给定另一个直和e=u_w，π对u的限制，在p（u）和p（v）之间产生一个透视f。几何上，F的定义如下：给定任意点a∈p（u），如果hp（w），ai是包含p（w）和a的最小投影子空间，点f（a）是hp（w），ai与p（v）的交集。
Figure 25.11 illustrates a projection f of center c between two projective lines ∆ and ∆0 (in the real projective plane).
图25.11说明了中心C在两条投影线∆和∆0之间的投影F（在实际投影平面中）。
If we consider three distinct points d1,d2,d3 on ∆ and their images on ∆0 under the projection f, then ratios are not preserved, that is,
如果我们考虑∆上的三个不同点d1、d2、d3及其在投影f下的∆0上的图像，那么比率就不会被保留，也就是说，
.
.
However, if we consider four distinct points d1,d2,d3,d4 on ∆ and their images on ∆0 under the projection f, we will show later that we have the following preservation of the so-called “cross-ratio”
但是，如果我们考虑∆上的四个不同点d1、d2、d3、d4，以及它们在投影f下的∆0上的图像，我们稍后将证明我们保留了所谓的“交叉比”。
.
.
Cross-ratios and projections play an important role in geometry (for some very elegant illustrations of this fact, see Sidler [156]).
交叉比和投影在几何学中起着重要作用（有关这一事实的一些非常优雅的说明，请参见Sidler[156]）。

Figure 25.11: A projection of center c between two lines ∆ and ∆0.
图25.11：中心C在两条直线∆和∆0之间的投影。
We now turn to the issue of determining when two linear maps f,g determine the same projective map, i.e., when P(f) = P(g). The following proposition gives us a complete answer.
我们现在讨论的问题是确定两个线性映射f，g何时确定同一投影映射，即p（f）=p（g）。下面的建议给了我们一个完整的答案。
Proposition 25.4. Given two nontrivial vector spaces E and F, for any two linear maps f : E → F and g: E → F, we have P(f) = P(g) iff there is some scalar λ ∈ K − {0} such that g = λf.
提案25.4.给定两个非平凡向量空间e和f，对于任意两个线性映射f:e→f和g:e→f，我们得到p（f）=p（g），如果有一些标量λ∈k−0，那么g=λf。
Proof. If g = λf, it is clear that P(f) = P(g). Conversely, in order to have P(f) = P(g), we must have Kerf = Kerg. If Kerf = Kerg = E, then f and g are both the null map, and this case is trivial. If E−Kerf =6 ∅, by taking a basis of Imf and some inverse image of this basis, we obtain a basis B of a subspace G of E such that E = Kerf ⊕G. If dim(G) = 1, the restriction of any linear map f : E → F to G is determined by some nonzero vector u ∈ E and some scalar λ ∈ K, and the proposition is obvious. Thus, assume that dim(G) ≥ 2. For any two distinct basis vectors u,v ∈ B, since P(f) = P(g), there must be some nonzero scalars λ(u), λ(v), and λ(u + v) such that
证据。如果g=λf，很明显p（f）=p（g）。相反，为了使p（f）=p（g），我们必须有切口=切口。如果kerf=kerg=e，那么f和g都是空映射，这种情况很简单。当e−kerf=6∅时，利用imf的基和该基的一些逆映象，得到e的子空间g的基b，使e=kerf g，当dim（g）=1时，任何线性映射f:e→f到g的约束由一些非零向量u∈e和一些标量λ∈k确定，并给出了相应的证明。位置很明显。因此，假设dim（g）≥2。对于任意两个不同的基向量u，v∈b，因为p（f）=p（g），必须有一些非零标度λ（u），λ（v）和λ（u+v），以便
	g(u) = λ(u)f(u),	g(v) = λ(v)f(v),	g(u + v) = λ(u + v)f(u + v).
g（u）=λ（u）f（u），g（v）=λ（v）f（v），g（u+v）=λ（u+v）f（u+v）。
Since f and g are linear, we get
因为f和g是线性的，我们得到
g(u) + g(v) = λ(u)f(u) + λ(v)f(v) = λ(u + v)(f(u) + f(v)),
g（u）+g（v）=λ（u）f（u）+λ（v）f（v）=λ（u+v）（f（u）+f（v）），
that is,
也就是说，
(λ(u + v) − λ(u))f(u) + (λ(u + v) − λ(v))f(v) = 0.
（λ（u+v）-λ（u））f（u）+（λ（u+v）-λ（v））f（v）=0.
Since f is injective on G and u,v ∈ B ⊆ G are linearly independent, f(u) and f(v) are also linearly independent, and thus we have
由于f在g和u上是内射的，v∈b g是线性无关的，f（u）和f（v）也是线性无关的，因此我们得到
λ(u + v) = λ(u) = λ(v).
λ（u+v）=λ（u）=λ（v）。
Now we have shown that λ(u) = λ(v), for any two distinct basis vectors in B, which proves that λ(u) is independent of u ∈ G, and proves that g = λf.	
现在我们证明了对于B中任意两个不同的基向量，λ（u）=λ（v），证明了λ（u）独立于u∈g，并证明了g=λf。
Proposition 25.4 shows that the projective linear group PGL(E) is isomorphic to the quotient group of the linear group GL(E) modulo the subgroup K∗idE (where K∗ = K − {0}). Using projective frames, we prove the following useful result.
命题25.4表明射影线性群pgl（e）同构于子群k ide（其中k=k−0）的线性群gl（e）模的商群。利用射影框架，我们证明了以下有用的结果。
Proposition 25.5. Given two nontrivial vector spaces E and F of the same dimension n + 1, for any two projective frames (ai)1≤i≤n+2 for P(E) and (bi)1≤i≤n+2 for P(F), there is a unique projectivity h: P(E) → P(F) such that h(ai) = bi for 1 ≤ i ≤ n + 2.
提案25.5.给定两个非平凡向量空间e和f，对于任意两个投影帧（a i）1≤i≤n+2，对于p（e）和（bi）1≤i≤n+2，对于p（f），有一个唯一的投影度h:p（e）→p（f），使得h（ai）=bi，对于1≤i≤n+2。
Proof. Let (u1,...,un+1) be a basis of E associated with the projective frame (ai)1≤i≤n+2, and let (v1,...,vn+1) be a basis of F associated with the projective frame (bi)1≤i≤n+2. Since (u1,...,un+1) is a basis, there is a unique linear bijection g: E → F such that g(ui) = vi, for 1 ≤ i ≤ n+1. Clearly, h = P(g) is a projectivity such that h(ai) = bi, for 1 ≤ i ≤ n+2. Let h0 : P(E) → P(F) be any projectivity such that h0(ai) = bi, for 1 ≤ i ≤ n + 2. By definition, there is a linear isomorphism f : E → F such that h0 = P(f). Since h0(ai) = bi, for 1 ≤ i ≤ n + 2, we must have f(ui) = λivi, for some λi ∈ K − {0}, where 1 ≤ i ≤ n + 1, and f(u1 + ··· + un+1) = λ(v1 + ··· + vn+1),
证据。设（u1，…，un+1）为与射影帧（a i）1≤i≤n+2相关联的e的基础，设（v1，…，vn+1）为与射影帧（bi）1≤i≤n+2相关联的f的基础。因为（u1，…，un+1）是一个基础，所以有一个唯一的线性双射g:e→f，这样g（ui）=vi，对于1≤i≤n+1。显然，h=p（g）是一个投射性，使得h（a i）=bi，对于1≤i≤n+2。设h0:p（e）→p（f）为任何投影性，使得h0（ai）=bi，对于1≤i≤n+2。根据定义，有一个线性同构f:e→f，这样h0=p（f）。由于h0（ai）=bi，对于1≤i≤n+2，我们必须有f（ui）=λivi，对于一些λi∈k−0，其中1≤i≤n+1，和f（u1+·······+un+1）=λ（v1+······+vn+1），
for some λ ∈ K − {0}. By linearity of f, we have
对于某些λ∈k−0。根据f的线性，我们得到
λ1v1 + ··· + λn+1vn+1 = λv1 + ··· + λvn+1,
λ1v1+····+λn+1vn+1=λv1+···+λvn+1，
and since (v1,...,vn+1) is a basis of F, we must have
既然（v1，…，vn+1）是f的基础，我们必须
λ1 = ··· = λn+1 = λ.
λ1=····=λn+1=λ。
This shows that f = λg, and thus that
这表明f=λg，因此
h0 = P(f) = P(g) = h,
h0=p（f）=p（g）=h，
and h is uniquely determined.	
H是唯一确定的。
 The above proposition and Proposition 25.4 are false if K is a skew field. Also, Proposition 25.5 fails if (bi)1≤i≤n+2 is not a projective frame, or if an+2 is dropped.
如果k是斜场，则上述命题和25.4都是假的。另外，如果（bi）1≤i≤n+2不是投影帧，或者如果一个+2被丢弃，则命题25.5失败。
As a corollary of Proposition 25.5, given a projective space P(E), two distinct projective lines D and D0 in P(E), three distinct points a,b,c on D, and any three distinct points a0,b0,c0 on D0, there is a unique projectivity from D to D0, mapping a to a0, b to b0, and c to c0. This is because, as we mentioned earlier, any three distinct points on a line form a projective frame.
作为25.5命题的一个推论，给定一个射影空间p（e），p（e）中的两条不同的射影线d和d0，d上的三个不同点a、b、c和d0上的任何三个不同点a0、b0、c0，有一个从d到d0的独特射影性，映射a到a0、b到b0和c到c0。这是因为，正如我们前面提到的，直线上的任何三个不同的点都形成了一个投影框架。
Remark: As in the affine case, there is “fundamental theorem of projective geometry.” For simplicity, we state this theorem assuming that vector spaces are over the field K = R. Given any two projective spaces P(E) and P(F) of the same dimension n ≥ 2, for any bijectivea,b,c to collinear functionpoints f(fa):,fP((bE),f) →(c)P, then(F), iff is a projectivity. For more general fields,f maps any three distinct collinear pointsf = P(g) for some
注：在仿射的情况下，有“射影几何的基本定理”。为了简单起见，我们假设向量空间在k=r的域上。给定任意两个射影空间p（e）和p（f），同维n≥2，任意双射影a、b、c到共线func点F（f a）：，f p（（be），f）→（c）p，然后（f），iff是一个投射性。对于更一般的字段，f映射任意三个不同的共线点sf=p（g）
“semilinear” bijectiondistinct points) is often called ag: E → Fcollineation. A map such as. For Kf =(preserving collinearity of any threeR, collineations and projectivities coincide. For more details, see Samuel [138].
“半线性”双射离散点）通常称为ag:e→f线性。像这样的地图。对于kf=（保持任意三者的共线性，共线性和射影率是一致的。有关更多详细信息，请参见Samuel[138]。
Before closing this section, we illustrate the power of Proposition 25.5 by proving two interesting results. We begin by characterizing perspectivities between lines.
在结束本节之前，我们通过证明两个有趣的结果来说明25.5号提案的威力。我们首先描述线条之间的透视性。
Proposition 25.6. Given any two distinct lines D and D0 in the real projective plane RP2, a projectivity f : D → D0 is a perspectivity iff f(O) = O, where O is the intersection of D and D0.
提案25.6.在实射影平面rp2中任意两条不同的线d和d0，射影率f:d→d0是透视率iff（o）=o，其中o是d和d0的交集。
Proof. If f : D → D0 is a perspectivity, then by the very definition of f, we have f(O) = O. Conversely, let f : D → D0 be a projectivity such that f(O) = O. Let a,b be any two distinct points on D also distinct from O, and let a0 = f(a) and b0 = f(b) on D0. Since f is a bijection and since a,b,O are pairwise distinct, a0 6= b0. Let c be the intersection of the lines ha,a0i and hb,b0i, which by the assumptions on a,b,O, cannot be on D or D0. Then we can define the perspectivity g: D → D0 of center c, and by the definition of c, we have
证据。如果f:d→d0是一个透视性，那么根据f的定义，我们有f（o）=o。相反，让f:d→d0是一个投影性，这样f（o）=o。让a，b是d上的任意两个不同点，也不同于o，让a0=f（a）和b0=f（b）在d0上。因为f是双射，而a，b，o是成对的，所以a0 6=b0。假设c是线ha、a0i和hb、b0i的交点，根据a、b、o的假设，这些线不能在d或d0上。然后我们可以定义中心c的透视率g:d→d0，根据c的定义，我们得到
	g(a) = a0,	g(b) = b0,	g(O) = O.
g（a）=a0，g（b）=b0，g（o）=o。
See Figure 25.12. However, f agrees with g on O,a,b, and since (O,a,b) is a projective frame for D, by Proposition 25.5, we must have f = g. 
见图25.12。然而，f在o，a，b上与g一致，由于（o，a，b）是d的投影框架，根据命题25.5，我们必须有f=g。
Using Proposition 25.6, we can give an elegant proof of a version of Desargues’s theorem (in the plane).
利用25.6号命题，我们可以很好地证明（在平面上）德沙格定理的一个版本。
Proposition 25.7. (Desargues) Given two triangles (a,b,c) and (a0,b0,c0) in RP2, where the
提案25.7.（desargues）在rp2中给出两个三角形（a，b，c）和（a0，b0，c0），其中
Apoints0 = hba,b,c,a0,c0i, B0,b0 =0, ch0a0are pairwise distinct and the lines,c0i, C0 = ha0,b0i are pairwise distinct, if the linesA = hb,ci, B = hha,aa,c0ii,, Chb,b=0ih, anda,bi,
apoints0=hba，b，c，a0，c0i，b0，b0=0，ch0a0是成对的不同，而线，c0i，c0=ha0，b0i是成对的不同，如果线a=hb，ci，b=hha，aa，c0ii，chb，b=0ih，anda，bi，
hc,c0i intersect in a common point d distinct from a,b,c, a0,b0,c0, then the intersection points p = hb,ci∩hb0,c0i, q = ha,ci∩ha0,c0i, and r = ha,bi∩ha0,b0i belong to a common line distinct from A,B,C, A0,B0,C0.
hc，c0i相交于与a，b，c，a0，b0，c0不同的公共点d，然后相交点p=hb，ci hb0，c0i，q=ha，ci ha0，c0i和r=ha，bi ha0，b0i属于与a，b，c，a0，b0，c0不同的公共线。
Proof.Ahc,c0,B0i0,CIn view of the assumptions on0. Let f : ha,a0i → hp. Letb,b0i hbe the perspectivity of center= ga,b,c◦f. Since both, a0,b0,c0, andf(dd, the point) = d and gr(dis on neither) = h0ia,anor0i, northe perspectivity of centerhb,b. It is also immediately shown that the line0i, the point p is on neither hb,b0i nor hc,c0i, and the pointhp,qi is distinct from the linesr andq is on neitherg: hb,bd0, we also havei → hha,aA,B,Cc,c0i be
证明：AHC、C0、B0I0、CIN对假设0的看法。让f:ha，a0i→hp。Letb，b0i hbe中心的透视率=ga，b，c f。由于a0，b0，c0，and f（d d，该点）=d和gr（d is-on-neither）=h0ia，anor0i，center hb，b的北透视率。也立即显示线条0i，该点p既不在hb，b0i也不在hc，c0i上，并且该点hp，qi与m线路sr和q在附近：hb，bd0，我们也有i→hha，aa，b，cc，c0i


Figure 25.12: An illustration of the perspectivity construction of Proposition 25.6.
图25.12：25.6提案的透视结构示意图。
h(d) = d. Thus by Proposition 25.6, the projectivity h: ha,a0i → hc,c0i is a perspectivity. Since
H（d）=D。因此，根据命题25.6，投影性H:h a，a0i→hc，c0i是一个透视性。自从
h(a)	=	g(f(a)) = g(b) = c, h(a0)	=	g(f(a0)) = g(b0) = c0,
h（a）=g（f（a））=g（b）=c，h（a0）=g（f（a0））=g（b0）=c0，
the intersection q of ha,ci and ha0,c0i is the center of the perspectivity h. Also note that the point m = ha,a0i∩hp,ri and its image h(m) are both on the line hp,ri, since r is the center of f and p is the center of g. Since h is a perspectivity of center q, the line hm,h(m)i = hp,ri passes through q, which proves the proposition.
h a、ci和ha0、c0i的交叉点q是透视性h的中心。还要注意，点m=ha、a0i h p、r i及其图像h（m）都在线hp、ri上，因为r是f的中心，p是g的中心。因为h是中心q的透视性，所以线hm、h（m）i=hp，ri通过啊，这证明了这个命题。
Desargues’s theorem is illustrated in Figure 25.13. It can also be shown that every projectivity between two distinct lines is the composition of two perspectivities (not in a unique way). An elegant proof of Pappus’s theorem can also be given using perspectivities.
德沙格定理如图25.13所示。也可以证明，两条不同线条之间的每一个投影都是两个透视图的组成部分（不是以独特的方式）。帕普斯定理的一个很好的证明也可以用透视法给出。
25.6	Finding a Homography Between Two Projective Frames
25.6在两个投影帧之间找到一个同形
In this section we present a method for finding the matrix (up to a scalar) of the unique homography (bijective projective transformation) mapping one projective frame to an other projective frame. This problem arises notably in computer vision in the context of image morphing.
在本节中，我们提出了一种求唯一同形矩阵（双射射影变换）的方法，将一个射影帧映射到另一个射影帧。这一问题在图像变形背景下的计算机视觉中尤为突出。
We begin with the simple case of two nondegenerate quadrilatrerals ([p1],[p2],[p3],[p4]) and [(q1],[q2],[q3],[q4]) in RP2, that is, two projective frames, which means that (p1,p2,p3)
我们从RP2中的两个非简并四分体（[p1]、[p2]、[p3]、[p4]）和[（q1]、[q2]、[q3]、[q4]）的简单情况开始，即两个投影帧，这意味着（p1、p2、p3）


Figure 25.13: Desargues’s theorem (projective version in the plane).
图25.13：德沙格定理（平面中的投影形式）。
and (q1,q2,q3) are linearly independent, and that if we write
和（q1，q2，q3）是线性无关的，如果我们写
p4 = α1p1 + α2p2 + α3p3
P4=α1p1+α2p2+α3p3
and q4 = λ1q1 + λ2q2 + λ3q3,
q4=λ1q1+λ2q2+λ3q3，
for some unique scalars α1,α2,α3 and λ1,λ2,λ3, then αi = 06 and λi = 06 for i = 1,2,3. The problem is to find the 3 × 3 matrix (up to a scalar) representing the unique homography h mapping [pi] to [qi] for i = 1,2,3,4.
对于一些独特的量表α1、α2、α3和λ1、λ2、λ3，则αi=06和λi=06表示i=1、2、3。问题是找到3×3矩阵（达到一个标量），它表示i=1,2,3,4的唯一同形H映射[pi]到[qi]。
We will use the canonical basis E = (e1,e2,e3) of R3, with e1 = (1,0,0), e2 = (0,1,0), e3 = (0,0,1), and the bases P = (p1,p2,p3) and Q = (q1,q2,q3) of R3.
我们将使用r3的规范基e=（e1，e2，e3），e1=（1，0，0），e2=（0，1，0），e3=（0，0，1），以及r3的基p=（p1，p2，p3）和q=（q1，q2，q3）。
As a first step, it is convenient to express (q1,q2,q3,q4) over the basis P = (p1,p2,p3), with q1 = (x1,y1,z1), q2 = (x2,y2,z2), q3 = (x3,y3,z3), q4 = (x4,y4,z4). Over the canonical basis
作为第一步，可以方便地表示（q1、q2、q3、q4）基P=（p1、p2、p3），其中q1=（x1、y1、z1），q2=（x2、y2、z2），q3=（x3、y3、z3），q4=（x4、y4、z4）。超越规范基础
E, the points (p1,p2,p3,p4) are given by the coordinates),
e，点（p1，p2，p3，p4）由坐标给出，
), and similarly, the points (q1,q2,q3,q4) are given by the
，同样，点（q1、q2、q3、q4）由
coordinates
协调
Proposition 25.8. 2With respect to the basis P = (p1,p2,p3), the matrix AP of the unique homography h of RP mapping the projective frame ([p1],[p2],[p3],[p4]) to the projective frame [(q1],[q2],[q3],[q4]) is given by
提案25.8.2关于基P=（p1，p2，p3），将投影帧（[p1]、[p2]、[p3]、[p4]）映射到投影帧[（q1]、[q2]、[q3]、[q4]）的RP的唯一同形H的矩阵ap由下式给出。
 .
.
Proof. Let u1 = α1p1, u2 = α2p2, u3 = α3p3, and let v1 = λ1q1, v2 = λ2q2, v3 = λ3q3, so that
证据。设u1=α1p1，u2=α2p2，u3=α3p3，v1=λ1q1，v2=λ2q2，v3=λ3q3，这样
p4 = u1 + u2 + u3
P4=U1+U2+U3
and q4 = v1 + v2 + v3.
q4=v1+v2+v3。
Because p1,p2,p3 are linearly independent and since αi = 06 for i = 1,2,3, the vectors (u1,u2,u2) are also linearly independent, so there is a unique linear map f : R3 → R3, such that
因为p1，p2，p3是线性无关的，而且由于αi=06，i=1,2,3，向量（u1，u2，u2）也是线性无关的，所以有一个唯一的线性映射f:r3→r3，这样
	f(ui) = vi	i = 1,...,3,
f（ui）=vi i=1，…，3，
and by linearity
以及线性
f(p4) = f(u1 + u2 + u3) = f(u1) + f(u2) + f(u3) = v1 + v2 + v3 = q4.
f（p4）=f（u1+u2+u3）=f（u1）+f（u2）+f（u3）=v1+v2+v3=q4。
With respect to the basis P = (p1,p2,p3), we have
关于基础p=（p1，p2，p3），我们有
,
，
so with respect to the basis P, the matrix of f is
所以对于基P，f的矩阵是
 ,
，
as claimed.	
如要求。
If we assume that we pick the coordinates of (p1,p2,p3,p4) and (q1,q2,q3,q4) with respect to the canonical basis E, then the coordinates α1,α2,α3 and λ1,λ2,λ3 are solutions of the systems
假设我们选取（p1，p2，p3，p4）和（q1，q2，q3，q4）相对于标准基e的坐标，那么坐标α1，α2，α3和λ1，λ2，λ3是系统的解。

and
和
 ,
，
and the matrix AE of our linear map f with respect to the canonical basis is determined as follows.
关于正则基的线性映射f的矩阵ae确定如下。
Proposition 25.9. With respect to the canonical basis2 E = (e1,e2,e3), the matrix AE of the unique homography h of RP mapping the projective frame ([p1],[p2],[p3],[p4]) to the projective frame [(q1],[q2],[q3],[q4]) is given by
提案25.9.对于标准基2 e=（e1，e2，e3），将射影帧（[p1]、[p2]、[p3]、[p4]）映射到射影帧[（q1]、[q2]、[q3]、[q4]）的RP唯一同形H的矩阵ae由下式给出。
 .
.
Proof. Since f : R3 → R3 is the unique linear map given by
证据。因为f:r3→r3是由
	f(ui) = vi,	i = 1,...,3,
f（ui）=vi，i=1，…，3，
the map f : R3 → R3 is equal to the composition
图f:r3→r3等于组成
f = fQ ◦ g,
F=FQ G，
where g: R3 → R3 is the unique linear map given by
其中，g:r3→r3是由
	g(ui) = ei,	i = 1,...,3,
g（ui）=ei，i=1，…，3，
and fQ : R3 → R3 is the unique linear map given by
而fq:r3→r3是由
	fQ(ei) = vi,	i = 1,...,3.
fq（ei）=vi，i=1，…，3.
However, g: R3 → R3 is the inverse of the unique linear map fP : R3 → R3 given by
然而，g:r3→r3是唯一线性映射fp:r3→r3的倒数，由
	fP(ei) = ui,	i = 1,...,3,
fp（ei）=ui，i=1，…，3，
so f = fQ ◦ fP−1.
所以f=fq fp−1。
The matrix BP representing fP over the canonical basis E is
在标准基e上表示fp的矩阵bp是
 ,
，
and similarly the matrix BQ representing fQ over E is
同样的，表示FQ的Bq矩阵是
 ,
，
and we have
我们有
AE = BQBP−1.
ae=BQBP−1。
Therefore, we have
因此，我们有
 ,
，
as claimed	
如声明
	The above method generalizes immediately to any dimension (and any field K).	If
上述方法立即推广到任何维度（和任何字段k）。
([p1],...,[pn+1],[pn+2]) and [(q1],...,[qn+1],[qn+2]) are any two projective frames in a projective space P(E) where E is a K-vector space of dimension n + 1, then (p1,...,pn+1) is a basis of E denoted by P and (q1,...,qn+1) is a basis of E denoted Q, and we can write
（[p1]、…、[p n+1]、[pn+2]）和[（q1]、…、[qn+1]、[qn+2]）是投影空间p（e）中任意两个投影帧，其中e是尺寸n+1的k矢量空间，则（p1，…，pn+1）是表示p的e的基，（q1，…，qn+1）是表示q的e的基，我们可以写
pn+2 = α1p1 + ··· + αn+1pn+1
Pn+2=α1p1+····+αn+1pn+1
qn+2 = λ1q1 + ··· + λn+1qn+1
qn+2=λ1q1+····+λn+1qn+1
for some unique αi,λi ∈ K such that αi = 06 and λi = 06 for i = 1,...,n + 1. If we assume that E = Kn+1, then the canonical basis is E = (e1,...,en+1). If we express the coordinates of the qj over the basis P by
对于一些独特的αi，λi∈k，使得αi=06和λi=06，对于i=1，…，n+1。如果我们假设e=kn+1，那么规范基础是e=（e1，…，en+1）。如果我们把qj在p基上的坐标表示为
,
，
then we have the following proposition.
然后我们有下面的建议。
Proposition 25.10. With respect to the basis P = (p1,...,pn+1), the matrix AP of the unique homography h of P(E) where E is a K-vector space of dimension n + 1, mapping the projective frame ([p1],...,[pn+1],[pn+2]) to the projective frame [(q1],...,[qn+1],[qn+2]) is given by
提案25.10。对于基P=（p1，…，p n+1），p（e）的唯一同形H的矩阵ap，其中e是尺寸n+1的k向量空间，将投影帧（[p1]、…，[pn+1]、[pn+2]）映射到投影帧[（q1]、…，[qn+1]、[qn+2]），由下式给出。
 .
.
If we express the coordinates of the vectors pi and qi over the canonical basis as pi = (p1i ,...,pni ,pni +1), qi = (qi1,...,qin,qin+1), i = 1,...,n + 2,
如果我们把规范基上向量Pi和Qi的坐标表示为Pi=（p1i，…，pni，pni+1），Qi=（qi1，…，qi n，qin+1），i=1，…，n+2，
then we have the following result.
然后我们得到以下结果。
Proposition 25.11. With respect to the canonical basis E = (e1,...,en+1), the matrix AE of the unique homography h of P(E) where E is a K-vector space of dimension n+1, mapping the projective frame ([p1],...,[pn+1],[pn+2]) to the projective frame [(q1],...,[qn+1],[qn+2]) is given by
提案25.11.关于规范基e=（e1，…，e n+1），p（e）的唯一同形h的矩阵ae，其中e是尺寸n+1的k向量空间，将投影帧（[p1]、…，[pn+1]、[pn+2]）映射到投影帧[（q1]、…，[qn+1]、[qn+2]），由下式给出。
 ,
，
where (α1,...,αn+1) and (λ1,...,λn+1) are the solutions of the systems
其中（α1，…，αn+1）和（λ1，…，λn+1）是系统的解。
and
和	 1 p1
1个P1
.
.
 ..
…

γ
 pn1
PN1

γ
pn1+1
pN1+ 1	... ...
……
...
…
...
…	p1n
P1N
...
…
pnn pnn+1
PNN PNN+1	 
	 1 q1
1季度
.
.
 ..
…

γ
 q1n
问题1

γ
q1n+1
Q1N+ 1	... ...
……
...
…
...
…	qn1
QN1
...
…
qnn qnn+1
Qnn Qnn+1	 .
.
We now consider the special case where the points ([p1],[p2],[p3],[p4]) belong to the affine patch of RP2 corresponding to the plane H of equation z = 1. In this case, we may identify [pi] with pi, which has coordinates ( 1) with respect to the canonical basis (the pis are not points at infinity; points at infinity are of of form (x,y,0)). Then, the barycentric coordinates α1,α2,α3 of p4 are solutions of the systems
我们现在考虑一个特殊情况，即点（[p1]、[p2]、[p3]、[p4]）属于方程z=1的平面h对应的rp2的仿射面片。在这种情况下，我们可以用π来标识[Pi]，它有关于规范基的坐标（Pi不是无穷大的点，无穷大的点是形式（x，y，0））。然后，P4的重心坐标α1，α2，α3是系统的解。
 .
.
By Proposition 25.9, we obtain the following result.
根据25.9号提案，我们得出以下结果。
Proposition 25.12. With respect to the canonical basis E = (e1,e2,e3), the matrix AE of
提案25.12.关于规范基e=（e1，e2，e3），矩阵ae
2 the unique homography h of RP mapping (p1,p2,p4,p4), points of the affine plane z = 1, to
2.RP映射的唯一同形H（p1，p2，p4，p4），仿射平面的点z=1，to
[(q1],[q2],[q3], [q4]) is given by
[（q1]、[q2]、[q3]、[q4]）由下式给出
 .
.
Observe that the above homography may map some of the affine points p1,p2,p3,p4 (which are not “points at infinity”) to arbitrary points in RP2, which may be points at infinity (in which case qiz = 0). The generalization to any dimension n ≥ 2 is immediate.
观察上述同形图可以将仿射点p1、p2、p3、p4（不是“无穷远点”）映射到rp2中的任意点，该点可能是无穷远点（在这种情况下，qiz=0）。对任意维n≥2的推广是直接的。
	We define the basis), with	1), and
我们定义了基础），用1）和
call it the affine canonical basis (of R2). We also define
称之为仿射正则基（r2）。我们还定义
In the special case where (p1,p2,p3,p4) is the canonical square (), since
在特殊情况下（p1，p2，p3，p4）是标准正方形（），因为
,
，
we have α1 = 1,α2 = 1, and α3 = −1, so
α1=1，α2=1，α3=-1，所以

where P is the change of basis matrix from the canonical basis E = (e1,e2,e3) to the affine
式中，p是基矩阵从规范基e=（e1，e2，e3）到仿射的变化。
basis). We have
基础）。我们有
and its inverse is
它的反方向是	 	 ,
，
In this case,
在这种情况下，	 	 .
.
 ,
，
	 	0	0 −1	1	0	0 
0 0−1 1 0 0
		 	,
，
we obtain
我们得到	 	 	 ,
，
and since that is,
既然是这样，
	q1x	q2x	q3xλ1	0	0 
q1x q2x q3xλ10 0_
	AE = qq11yz	qq22yz	qq33yz 00	λ02	λ03.
ae=qq11yz qq22yz qq33yz 00λ02λ03。
The generalization to any dimension n ≥ 2 is immediate.
对任意维n≥2的推广是直接的。
Finally, we consider the special case where the points ([p1],[p2],[p3],[p4]) and the points [(q1],[q2],[q3],[q4]) belong to the affine patch of RP2 corresponding to the plane H of equation z = 1. In this case, we may also identify [qi] with qi, which has coordinates ( 1) with respect to the canonical basis. Then, the barycentric coordinates λ1,λ2,λ3 of q4 are solutions of the systems
最后，我们考虑点（[p1]、[p2]、[p3]、[p4]）和点[（q1]、[q2]、[q3]、[q4]）属于方程z=1的平面h对应的rp2的仿射面片的特殊情况。在这种情况下，我们也可以用qi来标识[qi]，qi具有相对于规范基础的坐标（1）。然后，Q4的重心坐标λ1、λ2、λ3是系统的解。
 .
.
By Proposition 25.12 we obtain the following result.
根据25.12号提案，我们得出以下结果。
Proposition 25.13. With respect to the canonical basis2 E = (e1,e2,e3), the matrix AE of the unique homography h of RP mapping (p1,p2,p4,p4) to (q1,q2,q3,q4), all points of the affine plane z = 1, is given by
提案25.13.对于规范基2 e=（e1，e2，e3），RP映射（p1，p2，p4，p4）到（q1，q2，q3，q4）的唯一同形H的矩阵ae，仿射平面z=1的所有点由下式给出：
 .
.
If
如果
 ,
，
the transformed point of a point (x,y,1) in the affine plane z = 1,
仿射平面z=1中点（x，y，1）的变换点，
 ,
，
is not a point at infinity iff a31x + a32y + a33 = 06	, in which case it corresponds to the point in the affine plane z = 1 of coordinates
不是无穷大的点iff a31x+a32y+a33=06，在这种情况下，它对应于坐标的仿射平面z=1中的点
 .
.
The generalization to any dimension n ≥ 2 is immediate.
对任意维n≥2的推广是直接的。
Let us go back to the situation where the the points (p1,p2,p3,p4) and (q1,q2,q3,q4) are in the affine patch z = 1, and where the matrix of our linear map is expressed with respect to the basis P = (p1,p2,p3) and the coordinates of (q1,q2,q3,q4) are also expressed with respect to the basis P = (p1,p2,p3). In practical situations, for example in computer vision, it is important to find necessary and sufficient conditions for the unique projective transformation mapping (p1,p2,p3,p4) to (q1,q2,q3,q4) to be defined on the convex hull of the points p1,p2,p3,p4.
让我们回到点（p1，p2，p3，p4）和（q1，q2，q3，q4）在仿射面片z=1中的情况，我们的线性映射的矩阵表示为基P=（p1，p2，p3），并且（q1，q2，q3，q4）的坐标也表示为基P=（p1，第2页，第3页）。在实际情况下，例如在计算机视觉中，重要的是要找到在点p1、p2、p3、p4的凸包上定义到（q1、q2、q3、q4）的唯一投影变换映射（p1、p2、p3、p4）的必要和充分条件。
Proposition 25.14. The unique projective transformation mapping (p1,p2,p3,p4) to (q1,q2, q3,q4) (all points in the affine plane H of equation z = 1) is defined on the convex hull of the points p1,p2,p3,p4 iff the scalars in each of the pairs (α1,λ1), (α2,λ2) and (α3,λ3), have the same sign.
提案25.14.唯一射影变换映射（p1，p2，p3，p4）到（q1，q2，q3，q4）（方程式z=1的仿射平面h中的所有点）定义在点p1，p2，p3，p4的凸壳上，如果每个对（α1，λ1），（α2，λ2）和（α3，λ3）中的标量具有相同的符号。
Proof. With respect to the basis P, the equation of the plane H is
证据。关于基P，平面h的方程是
x + y + z = 1,
x+y+z=1，
so the image of p = (x,y,1 − x − y) under our linear map is
所以我们的线性图下的p=（x，y，1−x−y）的图像是
 .
.
The above point is a point at infinity iff
上面的点是无穷远处的点。
	.	(∗)
.（）
The unique projective transformation mapping (p1,p2,p3,p4) to (q1,q2,q3,q4) is defined on the convex hull of the points p1,p2,p3,p4 iff all four points p1,p2,p3,p4 are strictly contained in one of the two open half spaces determined by the line of equation (∗), which means that the affine form in (∗) must have the same sign on these four points.
唯一射影变换映射（p1，p2，p3，p4）到（q1，q2，q3，q4）是在点p1，p2，p3，p4的凸壳上定义的。如果所有四个点p1，p2，p3，p4都严格包含在方程（）所确定的两个半空间中的一个中，这意味着（）这四点上必须有相同的符号。
When we evaluate the affine form in (∗) on the four points p1,p2,p3,p4 using coordinates
当我们用坐标对四个点p1，p2，p3，p4上（）的仿射形式进行评估时
(x,y,1 − x − y), w.r.t. the basis P = (p1,p2,p3),
（x，y，1−x−y），w.r.t.基P=（p1，p2，p3）
1.	for p1 = (1,0,0) we get λ1/α1,
对于p1=（1,0,0），我们得到λ1/α1，
2.	for p2 = (0,1,0) we get λ2/α2,
对于p2=（0,1,0），我们得到λ2/α2，
3.	for p3 = (0,0,1) we get λ3/α3,
对于p3=（0,0,1），我们得到λ3/α3，
4.	and for p4 = (α1,α2,α3) we get
对于p4=（α1，α2，α3），我们得到

The fourth case shows that the sign of the affine form in (∗) is positive, and thus λ1/α1, λ2/α2,λ3/α3 > 0, which implies that the scalars in each of the pairs (α1,λ1), (α2,λ2) and (α3,λ3), must have the same sign.	
第四种情况表明（）中的仿射形式的符号为正，因此λ1/α1，λ2/α2，λ3/α3>0，这意味着每对（α1，λ1），（α2，λ2）和（α3，λ3）中的标量必须具有相同的符号。
The generalization to any dimension n ≥ 2 is immediate: the scalars in each pair (αi,λi) must have the same sign for i = 1,...,n + 2.
对任何维数n≥2的推广是直接的：每对（αi，λi）中的标量对于i=1，…，n+2必须有相同的符号。
In dimension 2, since α3 = 1 − α1 − α2 and λ3 = 1 − λ1 − λ2, there are four cases to consider:
在维度2中，由于α3=1−α1−α2和λ3=1−λ1−λ2，有四种情况需要考虑：
(1)	α1,λ1,α2,λ2 < 0. In this case, α3,λ3 > 1 so α3,λ3 also have the same sign.
α1，λ1，α2，λ2<0.在这种情况下，α3，λ3>1，因此α3，λ3也有相同的符号。
(2)	α1,λ1 < 0 and α2,λ2 > 0. In this case, since α3 = 1 − α1 − α2 and λ3 = 1 − λ1 − λ2, we must have either both α1 + α2 < 1 and λ1 + λ2 < 1, or both α1 + α2 > 1 and λ1 + λ2 > 1, in order for α3 and λ3 to have the same sign.
α1，λ1<0和α2，λ2>0。在这种情况下，由于α3=1-α1-α2和λ3=1-λ1-λ2，我们必须同时具有α1+α2<1和λ1+λ2<1，或者同时具有α1+α2>1和λ1+λ2>1，以便α3和λ3具有相同的符号。
(3)	α1,λ1 > 0 and α2,λ2 < 0. As in the previous case, since α3 = 1 − α1 − α2 and λ3 = 1 − λ1 − λ2, we must have either both α1 + α2 < 1 and λ1 + λ2 < 1, or both α1 + α2 > 1 and λ1 + λ2 > 1, in order for α3 and λ3 to have the same sign.
α1，λ1>0，α2，λ2<0.与前一种情况一样，由于α3=1-α1-α2和λ3=1-λ1-λ2，我们必须同时具有α1+α2<1和λ1+λ2<1，或者同时具有α1+α2>1和λ1+λ2>1，以便α3和λ3具有相同的符号。
(4)	α1,λ1,α2,λ2 > 0. As in the previous case, since α3 = 1−α1 −α2 and λ3 = 1−λ1 −λ2, we must have either both α1 + α2 < 1 and λ1 + λ2 < 1, or both α1 + α2 > 1 and λ1 + λ2 > 1, in order for α3 and λ3 to have the same sign.
α1，λ1，α2，λ2>0.在前面的例子中，由于α3=1−α1−α2和λ3=1−λ1−λ2，我们必须同时拥有α1+α2<1和λ1+λ2<1，或者同时拥有α1+α2>1和λ1+λ2>1，以便α3和λ3具有相同的符号。
Since α3 = 1 − α1 − α2 and λ3 = 1 − λ1 − λ2, we can write
由于α3=1−α1−α2和λ3=1−λ1−λ2，我们可以写

In the affine frame (p3,(p1 − p3,p2 − p3)), points have coordinates (α1,α2), and in the affine frame (q3,(q1 − q3,q2 − q3)), points have coordinates (λ1,λ2). In the first affine frame, the line hp1,p2i is given by the equation α1 + α2 = 1, and in the second affine frame, the line hq1,q2i is given by the equation λ1 +λ2 = 1. The open half plane containing p3 and bounded by the line hp1,p2i corresponds to the points of coordinates (α1,α2) satisfying α1 + α2 < 1, and the other open half plane not containing p3 corresponds to the points of coordinates (α1,α2) satisfying α1 +α2 > 1. Similarly, the open half plane containing q3 and bounded by the line hq1,q2i corresponds to the points of coordinates (λ1,λ2) satisfying λ1 + λ2 < 1, and the other open half plane not containing q3 corresponds to the points of coordinates (λ1,λ2) satisfying λ1 + λ2 > 1.
在仿射框架（p3，（p1−p3，p2−p3））中，点具有坐标（α1，α2），在仿射框架（q3，（q1−q3，q2−q3））中，点具有坐标（λ1，λ2）。在第一个仿射框中，线hp1，p2i由公式α1+α2=1给出，在第二个仿射框中，线hq1，q2i由公式λ1+λ2=1给出。含有p3且以线hp1、p2i为界的开半平面对应于满足α1+α2<1的坐标点（α1，α2），另一个不含p3的开半平面对应于满足α1+α2>1的坐标点（α1，α2）。同样，含有q3且以线hq1、q2i为界的开半平面对应于满足λ1+λ2<1的坐标点（λ1、λ2），另一个不包含q3的开半平面对应于满足λ1+λ2>1的坐标点（λ1、λ2）。
Then, the above conditions have the following interpretation in terms of regions in the affine plane z = 1:
那么，上述条件对于仿射平面z=1中的区域有如下解释：
(1)	When α1 < 0 and α2 < 0, the point p4 lies in quadrant III (with respect to the affine frames (p3,(p1 − p3,p2 − p3))). Under the mapping f, the point q4 is also mapped to quadrant III (with respect to the affine frame (q3,(q1 −q3,q2 −q3))); see Figure 25.14.
当α1<0和α2<0时，点P4位于象限III（相对于仿射帧（p3，（p1-p3，p2-p3））。在映射F下，点Q4也映射到象限III（相对于仿射帧（q3，（q1-q3，q2-q3））；参见图25.14。


Figure 25.14: Case (1)
图25.14：案例（1）
(2)	When α1,λ1 < 0 and α2,λ2 > 0, the points p4 and q4 belongs to quadrant II (with respect to the affine frames (p3,(p1 − p3,p2 − p3)) and (q3,(q1 − q3,q2 − q3))). Two possibilities occur. Either p4 belong to the open half space containing p3 and bounded by the line hp1,p2i and q4 belong to the open half space containing q3 and bounded by the line hq1,q2i, or p4 belong to the open half space not containing p3 and bounded by the line hp1,p2i and q4 belong to the open half space not containing q3 and bounded by the line hq1,q2i. The first possibility is illustrated by the top of Figure 25.15, while the second is illustrated by the bottom of Figure 25.15.
当α1、λ1<0和α2、λ2>0时，点p4和q4属于象限II（相对于仿射帧（p3，（p1−p3，p2−p3））和（q3，（q1−q3，q2−q3））。有两种可能性。p4属于包含p3的开放半空间，以hp1、p2i和q4线为界，属于包含q3的开放半空间，以hq1、q2i或p4线为界，属于不包含p3的开放半空间，以hp1、p2i和q4线为界，属于不包含co的开放半空间。第三行，以Hq1，q2i线为界。第一种可能性由图25.15的顶部说明，第二种可能性由图25.15的底部说明。
(3)	When α1,λ1 > 0 and α2,λ2 < 0, the points p4 and q4 belongs to quadrant IV (with respect to the affine frames (p3,(p1 − p3,p2 − p3)) and (q3,(q1 − q3,q2 − q3))). Two possibilities occur exactlty as in Case (2) depending on the position of p4 with respect to the line hp1,p2i and on the position of q4 with respect to the line hq1,q2i. The first possibility is illustrated by the top of Figure 25.16, while the second is illustrated by the bottom of Figure 25.16.
当α1，λ1>0和α2，λ2<0时，点P4和Q4属于象限IV（相对于仿射帧（P3，（P1−P3，P2−P3））和（Q3，（Q1−Q3，Q2−Q3））。两种可能性发生得很准确，如情况（2）所示，这取决于P4相对于线hp1，p2i得位置以及q4相对于线hq1，q2i得位置.图25.16顶部说明了第一种可能性，图25.16底部说明了第二种可能性.
(4)	When α1,λ1,α2,λ > 0 and α2,λ2 < 0, the points p4 and q4 belongs to quadrant I
当α1、λ1、α2、λ>0和α2、λ2<0时，点P4和Q4属于象限I。


Figure 25.15: Case (2)
图25.15：案例（2）
(with respect to the affine frames (p3,(p1 − p3,p2 − p3)) and (q3,(q1 − q3,q2 − q3))). Two possibilities occur exactlty as in Cases (2) and (3) depending on the position of p4 with respect to the line hp1,p2i and on the position of q4 with respect to the line hq1,q2i. The first possibility is illustrated by the top of Figure 25.17, while the second is illustrated by the bottom of Figure 25.17.
（关于仿射帧（p3，（p1−p3，p2−p3））和（q3，（q1−q3，q2−q3））。根据p4相对于线hp1、p2i的位置和q4相对于线hq1、q2i的位置，有两种可能发生，如案例（2）和（3）所示。第一种可能出现在图25.17的顶部，第二种可能出现在图的底部。第25.17条。
Thus, if both (p1,p2,p3,p4) and (q1,q2,q3,q4) satisfy the conditions listed above, there is no point at infinity inside of the convex hull of the quadrangle (p1,p2,p3,p4).
因此，如果（p1，p2，p3，p4）和（q1，q2，q3，q4）都满足上述条件，则四边形（p1，p2，p3，p4）的凸壳内部没有无穷大的点。
It remains to prove that the image of the convex hull of (p1,p2,p3,p4) is the convex hull of (q1,q2,q3,q4).
还有待证明（p1，p2，p3，p4）的凸壳图像是（q1，q2，q3，q4）的凸壳图像。
Proposition 25.15. If both (p1,p2,p3,p4) and (q1,q2,q3,q4) satisfy the conditions of Proposition 25.14, then the image of the convex hull of (p1,p2,p3,p4) under the unique projective map mapping (p1,p2,p3,p4) to (q1,q2,q3,q4) is the convex hull of (q1,q2,q3,q4)
提案25.15。如果（p1，p2，p3，p4）和（q1，q2，q3，q4）都满足命题25.14的条件，那么（p1，p2，p3，p4）在唯一投影映射（p1，p2，p3，p4）到（q1，q2，q3，q4）下的凸壳图像就是（q1，q2，q3，q4）的凸壳。
Proof. It suffices to show that the restriction of our projective transformation maps a line segment to the convex hull of the images of the endpoints of this segment. Thus, the problem
证据。证明了射影变换的限制条件将直线段映射到该段端点图像的凸包。因此，问题是


Figure 25.16: Case (3)
图25.16：案例（3）
reduces to proving that if a projective transformation given by an invertible matrix
减少到证明如果由可逆矩阵给出的射影变换

does not have points at infinity on the line segment in R2 corresponding to the points of coordinates (x,1) with 0 ≤ x ≤ 1, then the image of the line segment [(0,1),(1,1)] is the line segment [(b/d,1),((a + b)/(c + d),1)] (or [((a + b)/(c + d),1),(b/d,1)]).
在r2的直线段上没有与0≤x≤1的坐标点（x，1）对应的无穷远点，则直线段的图像[（0,1），（1,1）]是直线段[（b/d，1），（（a+b）/（c+d），1）]（或[（（a+b）/（c+d），1），（b/d，1）]。
We have
我们有

and
和


25.7. AFFINE PATCHES
25.7。仿射补丁


Figure 25.17: Case (4)
图25.17：案例（4）
In order for our map to be defined for 0 ≤ x ≤ 1, cx + d must have a constant sign for
为了使我们的地图定义为0≤x≤1，cx+d必须有一个常量符号
0 ≤ x ≤ 1, which means that d and c + d have the same sign. Then,
0≤x≤1，表示d与c+d符号相同。然后，

and
和

have opposite signs when 0 < x < 1, which means that the image of [0,1] is the interval [b/d,(a + b)/(c + d)] (or [(a + b)/(c + d),b/d]). 
当0<x<1时有相反的符号，这意味着[0,1]的图像是间隔[b/d，（a+b）/（c+d）]（或[（a+b）/（c+d），b/d]）。
We now consider the projective completion of an affine space. First, we introduce the notion of affine patch.
我们现在考虑仿射空间的射影完备。首先，我们介绍仿射补丁的概念。
25.7	Affine Patches
25.7仿射补丁
Given an affine space E with associated vector space →−E, we can form the vector space Eb, the homogenized version of E, and then, the projective space P  induced by Eb. This projective space, also denoted by Ee, has some very interesting properties. In fact, it satisfies a universal property, but before we can say what it is, we have to take a closer look at Ee.
给定一个具有相关向量空间→−e的仿射空间e，我们可以形成向量空间eb，e的均匀化版本，然后由eb诱导的射影空间p。这个射影空间，也用ee表示，有一些非常有趣的性质。事实上，它满足一个普遍的属性，但在我们说出它是什么之前，我们必须仔细看看EE。
Since the vector space Eb is the disjoint union of elements of the form ha,λi, where a ∈ E and λ ∈ K − {0}, and elements of the form u ∈ →−E, observe that if ∼ is the equivalence relation on Eb used to define the projective space P , then the equivalence class [ha,λi]∼ of a weighted point contains the special representative a = ha,1i, and the equivalence class [u]∼ of a nonzero vector is just a point of the projective space P . Thus, there is a bijection
由于向量空间eb是形式ha，λi的元素的不相交并，其中a∈e和λ∈k−0，以及形式u∈→−e的元素，观察如果是用于定义射影空间p的eb上的等价关系，那么一个权重的等价类[ha，λi]Ted点包含特殊的代表a=ha，1i，非零向量的等价类[u]只是射影空间p的点。因此，有一个双射
P 
磷
between P  and the disjoint union , which allows us to view E as being embedded in P . The points of P E in P E will be called points at infinity, and the projective hyperplane P is called the hyperplane at infinity. We will also denote the point [u]∼ of P  (where u = 0)6 by u∞.
在P和不相交的联合之间，这允许我们将E视为嵌入在P中。p e中的点称为无穷远处的点，投影超平面p称为无穷远处的超平面。我们还将用u∞表示点[u]p（其中u=0）6。
Thus, we can think of  as the projective completion of the affine space E obtained by adding points at infinity forming the hyperplane P . As we commented in Section 25.2 when we presented the hyperplane model of P(E), the notion of point at infinity is really an affine notion. But even if a vector space E doesn’t arise from the completion of an affine space, there is an affine structure on the complement of any hyperplane P(H) in the projective space P(E). In the case of Ee, the complement E of the projective hyperplane P  is indeed an affine space. This is a general property that is needed in order to figure out the universal property of Ee.
因此，我们可以把仿射空间e看作是在无穷远处加上点形成超平面p而得到的射影完备。正如我们在25.2节中所评论的，当我们提出p（e）的超平面模型时，无穷远点的概念实际上是一个仿射概念。但是，即使向量空间e不是仿射空间的完备形式，在射影空间p（e）中任何超平面p（h）的补上都存在仿射结构。在e e的情况下，射影超平面p的补e实际上是一个仿射空间。这是计算EE的通用属性所需的通用属性。
Proposition 25.16. Given a vector space E and a hyperplane H in E, the complement EH = P(E) − P(H) of the projective hyperplane P(H) in the projective space P(E) can be given an affine structure such that the associated vector space of EH is H. The affine structure on EH depends only on H, and under this affine structure, EH is isomorphic to an affine hyperplane in E.
提案25.16。给定一个向量空间e和e中的超平面h，射影空间p（e）中射影超平面p（h）的补码e h=p（e）−p（h）可以给出一个仿射结构，使得e h的相关向量空间为h。e h上的仿射结构仅依赖于h，并且在这个仿射结构下。结构，eh同构于e中的仿射超平面。
Proof. Since H is a hyperplane in E, there is some w ∈ E−H such that E = Kw⊕H. Thus, every vector u in E−H can be written in a unique way as λw+h, where λ = 06 and h ∈ H. As a consequence, for every point [u] in EH, the equivalence class [u] contains a representative of the form w + λ−1h, with λ = 06 . Then we see that the map ϕ: (w + H) → EH, defined such that
证据。由于h是e中的超平面，因此存在一些w∈e−h，e=kw h。因此，e−h中的每个向量u都可以用独特的方式写成λw+h，其中，λ=06和h∈h。因此，对于eh中的每个点[u]，等价类[u]都包含形式w+λ−1h，w的代表。ithλ=06.然后我们看到地图_：（w+h）→eh，定义如下：
ϕ(w + h) = [w + h],
⑨（w+h）=[w+h]，
is a bijection. In order to define an affine structure on EH, we define +: EH × H → EH as follows: For every point [w + h1] ∈ EH and every h2 ∈ H, we let
是一个双射。为了在eh上定义一个仿射结构，我们定义了+：eh×h→eh如下：对于每一点[w+h1]∈eh和每一个h2∈h，我们让
[w + h1] + h2 = [w + h1 + h2].
[w+h1]+h2=[w+h1+h2]。
The axioms of an affine space are immediately verified. Now, w + H is an affine hyperplane is E, and under the affine structure just given to EH, the map ϕ: (w+H) → EH is an affine
仿射空间的公理立即得到验证。现在，w+h是仿射超平面，e是仿射结构，在刚刚给eh的仿射结构下，图（w+h）→eh是仿射
25.7. AFFINE PATCHES
25.7。仿射补丁
map that is bijective. Thus, EH is isomorphic to the affine hyperplane w + H. If we had chosen a different vector w0 ∈ E −H such that E = Kw0 ⊕H, then EH would be isomorphic to the affine hyperplane w0 + H parallel to w + H. But these two hyperplanes are clearly isomorphic by translation, and thus the affine structure on EH depends only on H. 
双目标地图。因此，e h与仿射超平面w+h是同构的，如果我们选择一个不同的向量w0∈e−h，使e=kw0 h，那么eh将与平行于w+h的仿射超平面w0+h同构，但这两个超平面通过平移显然是同构的，因此仿射结构你对eh的依赖仅仅在于h。
An affine space of the form EH is called an affine patch on P(E). Proposition 25.16 allows us to view a projective space P(E) as the result of gluing some affine spaces together, at least when E is of finite dimension. For example, when E is of dimension 2, a hyperplane in E is just a line, and the complement of a point in the projective line P(E) can be viewed as an affine line. Thus, we can view P(E) as being covered by two affine lines glued together as illustrated by When K = R, this shows that topologically, the projective line RP1 is equivalent to a circle. See Figure 25.18. When E is of dimension 3, a hyperplane in E is
形式eh的仿射空间称为p（e）上的仿射补丁。命题25.16允许我们看到投影空间p（e），至少当e是有限维的时候，是把一些仿射空间粘合在一起的结果。例如，当e是维数2时，e中的超平面只是一条线，投影线p（e）中点的补部可以看作是仿射线。因此，我们可以把p（e）看作是由两条粘在一起的仿射线所覆盖，如当k=r时所示，这表明在拓扑上，射影线rp1等于一个圆。见图25.18。当e为尺寸3时，e中的超平面为

Figure 25.18: The covering of RP1 by the affine lines y = 0 and y = 1.
图25.18：用仿射线y=0和y=1覆盖rp1。
just a plane, and the complement of a projective line in the projective plane P(E) can be viewed as an affine plane. Thus, we can view P(E) as being covered by three affine planes glued together as illustrated by Figure 25.19.
只要一个平面，射影平面p（e）中射影线的补部就可以看作是仿射平面。因此，我们可以将p（e）视为由三个粘合在一起的仿射平面覆盖，如图25.19所示。
However, even when K = R, it is much more difficult to come up with a geometric embedding of the projective plane RP2 in A3, and in fact, this is impossible! Nevertheless, there are some fascinating immersions of the projective space RP2 as 3D surfaces with selfintersection, one of which is known as the Boy surface. We urge our readers to consult the remarkable book by Hilbert and Cohn-Vossen [90] for drawings of the Boy surface, and more. One should also consult Fischer’s books [62, 61], where many beautiful models of surfaces are displayed, and the commentaries in Chapter 6 of [61] regarding models of RP2. More generally, when E is of dimension n+1, the projective space P(E) is covered by n+1 affine patches (hyperplanes) glued together. This idea is very fruitful, since it allows the treatment of projective spaces as manifolds, and it is essential in algebraic geometry.
然而，即使当k=r时，要想在a3中嵌入射影平面rp2也要困难得多，事实上，这是不可能的！尽管如此，投影空间rp2还是有一些令人着迷的沉浸感，即自相交的三维表面，其中一个被称为“男孩表面”。我们敦促读者参考希尔伯特和科恩·沃森的这本非凡的书[90]来获取男孩表面的绘画，等等。我们还应该参考费舍尔的书[62，61]，其中展示了许多美丽的表面模型，以及[61]第6章中关于RP2模型的评论。通常，当e的尺寸为n+1时，投影空间p（e）被粘在一起的n+1仿射片（超平面）覆盖。这个想法是非常有成效的，因为它允许把射影空间作为流形来处理，并且它在代数几何中是必不可少的。
We can now go back to the projective completion Ee of an affine space E.
我们现在可以回到仿射空间e的射影完备ee。

Figure 25.19: The covering of RP2 by the affine planes z = 1, x = 1, and y = 1. The plane z = 1 covers everything but the circle x2 + y2 = 1 in the xy-plane. The plane y = 1 covers that circle modulo the point (1,0,0), which is then covered by the plane x = 1.
图25.19：仿射平面z=1、x=1和y=1覆盖了rp2。平面z=1覆盖了除xy平面中的圆x2+y2=1之外的所有内容。平面y=1覆盖该圆的模点（1,0,0），然后被平面x=1覆盖。
25.8	Projective Completion of an Affine Space
25.8仿射空间的射影完备
We begin by spelling out the universal property characterizing the projective completion of an affine space (E,→−E). Then, we prove thatwhere is the projective space obtained associated with the vector space E obtained from E by the hat construction from Chapter 24 is indeed a projective completion of (E,→−E).
我们首先阐述了一个仿射空间（e，→−e）的射影完备的普遍性质。然后，我们证明，从第24章的hat构造得到的与从e得到的向量空间e相关的射影空间在哪里，实际上是（e，→−e）的射影完成。
Definition 25.7. Given any affine space E with associated vector space →−E, a projective completion of the affine space E with hyperplane at infinity P(H) is a triple hP(E),P(H),ii, where E is a vector space, H is a hyperplane in E, i: E → P(E) is an injective map such projective spacethat i(E) = EH andP(Fi) (is affine (wherewhere F is some vector space), every hyperplaneEH = P(E) − P(H) is an affine patch), and for everyH in F, and every map f : E → P(F) such that f(E) ⊆ FH and f is affine (where FH = P(F) − P(H) is an
定义25.7.给定任意具有相关向量空间→−e的仿射空间e，在无穷大p（h）上具有超平面的仿射空间e的射影完备为三重hp（e），p（h），i i，其中e是向量空间，h是e中的超平面，即：e→p（e）是射影映射，即i（e）=eh和p（fi）（是仿射（其中f是一些向量空间），每个超平面=p（e）−p（h）是仿射补丁，对于f中的每一个平面，以及每个映射f:e→p（f），使得f（e）fh和f是仿射（其中fh=p（f）−p（h）是一个
25.8. PROJECTIVE COMPLETION OF AN AFFINE SPACE affine patch), there is a unique projective map) such that
25.8。仿射空间仿射面片的射影完成），有一个独特的射影图）这样
	f = fe◦ i	and	P 
F=铁I和P
(where →−i : →−E → H and →−f : →−E → H are the linear maps associated with the affine maps i: E → P(E) and f : E → P(F)), as in the following diagram:
（其中→−i：→−e→h和→−f：→−e→h是与仿射图i:e→p（e）和f:e→p（f）相关联的线性图，如下图所示：
r
R
E IIIIIiIIIIfI/IIEIHIII⊆IIIPI$ (E )fe⊇ryrPrrr(rHrr)rPro rrPr(r−→rir) rrP
E IIIII IIIIIFI/I IIEIHIII IIIPI$（E）Fe Ryrprr（rhrr）Rpro rrp r（r−→Rir）rrp

FH ⊆ P(F) ⊇ P(H)
f h p（f）p（h）
The points of P(E) in P(H) are called points at infinity, and the projective hyperplane P(H) is called the hyperplane at infinity. We will also denote the point [u]∼ of P(H) (where u = 0)6 by u∞. As usual, objects defined by a universal property are unique up to isomorphism. We leave the proof as an exercise.
p（h）中p（e）的点称为无穷远点，投影超平面p（h）称为无穷远点。我们还将用u∞来表示p（h）（其中u=0）6的点[u]。通常，由一个普遍属性定义的对象在同构上是唯一的。我们把证据留作练习。
The importance of the notion of projective completion stems from the fact that every affine map f : E → F extends in a unique way to a projective map fe: P(E) → P(F), where hP(E),P(HE),iEi is a projective completion ofis a projective completion of F, provided that the restriction of f to P E agrees with P f , as illustrated in the following commutative diagram:
射影完成概念的重要性源于每个仿射映射f:e→f都以独特的方式延伸到射影映射fe:p（e）→p（f），其中hp（e）、p（he）、iei是f的射影完成的射影完成，前提是f对p e ag的限制带有p f的Rees，如下图所示：
f
f
E	/ F iEiF
E/F IEIF公司

	P(E)	e / P(F).
P（E）E/P（F）。
f
f
We will now show that is the projective completion of E, where i: E → Ee is the injection of E into . For example, if E = A1K is an affine line, its projective completion Af1K is isomorphic to the projective line P(K2), and they both can be identified with A1K ∪ {∞}, the result of adding a point at infinity (∞) to A1K. In general, the projective completion AfmK of the affine space AmK is isomorphic to P(Km+1). Thus, is isomorphic to RPm, andis isomorphic to CPm.
现在我们将证明这是e的投影完成，其中i:e→ee是e的注入。例如，如果e=a1k是仿射线，其射影完备af1k与射影线p（k2）是同构的，两者都可以用a1k∞来标识，即在无穷大（∞）处加一个点到a1k的结果。一般来说，仿射空间amk的射影完备afmk是isom。奥菲奇到P（km+1）。因此，与RPM同构，与CPM同构。
First, let us observe that if E is a vector space and H is a hyperplane in E, then the homogenization of the affine patch EH (the complement of the projective hyperplane P(H) in P(E)) is isomorphic to E. The proof is rather simple and uses the fact that there is an affine bijection between EH and the affine hyperplane w + H in E, where w ∈ E − H is any fixed vector. Choosing w as an origin in EH, we know that EcH = H +b Kw, and since E = H ⊕ Kw, it is obvious how to define a linear bijection between EcH = H +b Kw and E = H ⊕ Kw. As a consequence the projective spaces EfH and P(E) are isomorphic, i.e., there is a projectivity between them.
首先，让我们观察一下，如果e是向量空间，h是e中的超平面，那么仿射面片eh（p（e）中投影超平面p（h）的补码）的同构化就是e的同构化，证明相当简单，并且使用了eh和t之间存在仿射双射的事实。他在e中仿射超平面w+h，其中w∈e−h是任何固定向量。选择w作为e h的原点，我们知道ech=h+b kw，由于e=h_kw，如何定义ech=h+b kw和e=h_kw之间的线性双射关系是显而易见的。因此，射影空间efh和p（e）是同构的，即它们之间存在射影性。
Proposition 25.17. Given any affine space E,, for every projective space P(F) (where F is some vector space), every hyperplane H in F, and every map f : E → P(F) such that f(E) ⊆ FH and f is affine (FH being viewed as an affine patch), there is a unique projective map fe: Ee → P(F) such that
提案25.17。给定任意仿射空间e，，对于每个射影空间p（f）（其中f是一些向量空间），f中的每个超平面h，以及每个映射f:e→p（f），使得f（e）fh和f是仿射（fh被视为仿射补丁），有一个独特的射影映射fe:ee→p（f），这样
	f = fe◦ i	and	P ,
f=fe i和p，
(where →−i : →−E → →−E and →−f : →−E → H are the linear maps associated with the affine maps i: E → Ee and f : E → P(F)), as in the following diagram:
（其中→−i：→−e→→−e和→−f：→−e→h是与仿射图i:e→ee和f:e→p（f）相关联的线性图，如下图所示：

E IIIIIiIIIIfI/IIEIHIII⊆IIIPI$ (E )fe⊇ryrPrrr(rHrr)rPro rrPr(r−→rir)rrrP
E IIIII IIIIIFI/I IIEIHIII IIIPI$（E）Fe Ryrprr（rhrr）Rpro Rpr（r−→Rir）Rrrp

FH ⊆ P(F) ⊇ P(H)
f h p（f）p（h）
Proof. The existence of feis a consequence of Proposition 24.6, where we observe thatis isomorphic to F. Just take the projective map P), where is the unique linear map extending f. It remains to prove its uniqueness.
证据。fei的存在是24.6命题的一个结果，在这里我们观察到它与f同构。只要取射影映射p），这里是唯一的线性映射延伸f，它仍然是证明其唯一性的。
As explained in the proof of Proposition 25.16, the affine patch FH is affinely isomorphic to some affine hyperplane of the form w + H for some w ∈ F − H. If we pick any a ∈ E, since by hypothesis f(a⊕) ∈ FH, we may assume that→ w ∈ F −H is chosen so that∈ f(a∈) = [→− w], and we have F = Kw H. Since f : E FH is affine, for any a E and any u E, we have
如命题25.16的证明所解释的那样，对于某些w∈f−h，仿射面片fh与形式为w+h的某些仿射超平面是仿射同构的。如果我们选取任何a∈e，因为根据假设f（a）∈fh，我们可以假定选择→w∈f−h，这样∈f（a∈）=[→−w]，一个d我们有f=kw h。因为f:e fh是仿射的，对于任何a e和任何u e，我们有
f(a + u) = f(a) + →−f (u) = w + →−f (u),
F（A+U）=F（A）+→−F（U）=W+→−F（U）、
whereis a linear map, and where f(a) is viewed as the vector w.
其中是线性图，其中f（a）被视为向量w。
Assume that) exists with the desired property. Then there is some linear map∈ g: Eb → F such that fe = P(g). Our goal is to prove that→− for some nonzero µ K. First, we prove that g vanishes on Ker f .
假设）具有所需属性。然后有一些线性映射∈g:eb→f，这样fe=p（g）。我们的目标是证明→−对于一些非零μK。首先，我们证明G在Ker F上消失。
	Since	, we must have f(a) = [w] = [g(a)], and thus g(a) = µw, for some µ = 0.6
因为，对于一些μ=0.6，我们必须有f（a）=[w]=[g（a）]，因此g（a）=μw。
Also, for every u ∈ E,
而且，对于每一个u∈e，

25.8. PROJECTIVE COMPLETION OF AN AFFINE SPACE
25.8。仿射空间的射影完备
and thus we must have
因此我们必须
	λ(u)w + λ(u)→−f (u) = µw + g(u),	(∗1)
λ（u）w+λ（u）→−f（u）=w+g（u），（1）
for some λ(u) 6= 0.
对于某些λ（u）6=0。
If Ker→−f = →−E, the linear map is the null map, and since we are requiring that the restriction of fe to P →−E be equal to P f , the linear map g must also be the null map on →−E. Thus, fe is unique, and the restriction of fe to P  is the partial map undefined everywhere.
如果ker→−f=→−e，则线性映射为零映射，由于我们要求fe对p→−e的限制等于p f，因此线性映射g也必须是→−e上的零映射，因此fe是唯一的，fe对p的限制是到处未定义的部分映射。
If →−E − Ker→−f 6= ∅, by taking a basis of Im→−f →−Eand some inverse image of this basis, we= Ker→−f ⊕ →−G. Since →−E = Ker→−f where dimobtain a basis of a subspace1, for any x ∈ Ker f and any nonnull vectorsuch that y ∈ →−G, we have ⊕ →−G
如果→−E−KER→−F 6=∅，通过取im→−F→−E的基和该基的一些逆像，我们=KER→−F→−G。因为→−E=KER→−F，其中dim获得子空间1的基，对于任何x∈KER F和任何非空矢量，例如y∈→−G，我们有→−G
λ(x)w
λ（x）w	=
=	µw + g(x),
礹w+g（x）、
λ(y)w + λ(y)→−f (y)
λ（y）w+λ（y）→−f（y）	=
=	µw + g(y),
礹w+g（y）、
and
和
λ(x + y)w + λ(x + y)→−f (x + y) = µw + g(x + y),
λ（x+y）w+λ（x+y）→−f（x+y）＝μw+g（x+y），
which by linearity yields
通过线性关系得出
(λ(x + y) − λ(x) − λ(y) + µ)w + (λ(x + y) − λ(y))→−f (y) = 0.
（λ（x+y）−λ（x）−λ（y）+μ）w+（λ（x+y）−λ（y））→−f（y）=0.
Since F = Kw ⊕ H and →−f : →−E → H, we must have λ(x + y) = λ(y) and λ(x) = µ. Then the equation
由于f=kw h和→−f：→−e→h，我们必须得到λ（x+y）=λ（y）和λ（x）=µ。那么方程
λ(x)w = µw + g(x)
λ（x）w=μw+g（x）
yields µw = µw + g(x), shows that g vanishes on Ker→−f . If dim	= 1 then by (∗1), for any y ∈ →−G we have
得到μw=μw+g（x），表明g在Ker→−f上消失。如果dim=1，那么（1），对于任何y∈→−g，我们有
λ(y)w + λ(y)→−f (y) = µw + g(y),
λ（y）w+λ（y）→−f（y）=μw+g（y），
and for any ν 6= 0 we have
对于任何v 6=0，我们有
λ(νy)w + λ(νy)→−f (νy) = µw + g(νy),
λ（νy）w+λ（νy）→−f（νy）=μw+g（νy），
which by linearity yields
通过线性关系得出
(λ(νy) − νλ(y) − µ + νµ)w + (νλ(νy) − νλ(y))→−f (y) = 0.
（λ（νy）−νλ（y）−祄+ν祄）w+（νλ（νy）−νλ（y））→−f（y）=0.
Since F = Kw ⊕ µH)(1, →−f−:ν→−E) = 0.→ H, and ν = 06 , we must have λ(νy) = λ(y). Then we must also have (λ(y) −
由于f=kw祫h）（1，→−f−：ν→−e）=0.→h，且ν=06，我们必须有λ（νy）=λ（y）。那么我们还必须有（λ（y）−
If K = {0,1}, since the only nonzero scalar is 1, it is immediate that6 ∈ →− g(y) = →−f (y), and we are done. Otherwise, for ν = 0,1, we get λ(y) = µ for all y G. Then equation
如果k=0,1，因为唯一的非零标量是1，那么6∈→−g（y）=→−f（y）是直接的，我们就完成了。否则，对于ν=0,1，我们得到所有y g的λ（y）=μ，然后方程
λ(y)w + λ(y)→−f (y) = µw + g(y)
λ（y）w+λ（y）→−f（y）=μw+g（y）
yields g = µ→−f on G, and since g vanishes on Ker→−f we get g = µ→−f on →−E and the restriction of →− is equal to P. But now, by Proposition 24.6 and since  is isomorphic to F, the linear map fbis completely determined by
在g上产生g=μ→−f，由于g在ker→−f上消失，我们在→−e上得到g=μ→−f，并且→−的限制等于p。但是现在，根据命题24.6，由于与f同构，线性图fbi完全由
,
，
and g is completely determined by
G完全由
.
.
Thus, we have.
因此，我们有。
Otherwise, if dim 2, then for any two distinct basis vectors u and v in B,
否则，如果dim 2，那么对于b中任意两个不同的基向量u和v，
λ(u)w + λ(u)→−f (u)
λ（u）w+λ（u）→−f（u）	=
=	µw + g(u),
礹w+g（u）、
λ(v)w + λ(v)→−f (v)
λ（v）w+λ（v）→−f（v）	=
=	µw + g(v),
礹w+g（v）、
and
和
λ(u + v)w + λ(u + v)→−f (u + v) = µw + g(u + v),
λ（u+v）w+λ（u+v）→−f（u+v）=礹w+g（u+v），
and by linearity, we get
通过线性，我们得到
(λ(u + v) − λ(u) − λ(v) + µ)w + (λ(u + v) − λ(u))→−f (u) + (λ(u + v) − λ(v))→−f (v) = 0.
（λ（u+v）-λ（u）-λ（v）+μw+（λ（u+v）-λ（u））→f（u）+（λ（u+v）-λ（v））→f（v）=0.
Since F = Kw ⊕H, →−f : →−E → H, and →−f (u) and →−f (v) are linearly independent (because →−f in injective on →−G), we must have
由于f=kw h，→−f：→−e→h和→−f（u）和→−f（v）是线性独立的（因为→−f在→−g上的注入中），我们必须
λ(u + v) = λ(u) = λ(v) = µ,
λ（u+v）=λ（u）=λ（v）=μ，
which implies that g = µ→−f on →−E, and the restriction of fe = P(g) to P  is equal to P . As in the previous case, g is completely determined by
这意味着在→−e上g=祆→−f，并且fe=p（g）到p的限制等于p。与前一种情况一样，G完全由
.
.
Again, we have g = µfb, and thus feis unique.	
同样，我们有g=μfb，因此feis是唯一的。
25.9. MAKING GOOD USE OF HYPERPLANES AT INFINITY
25.9。充分利用无限远超平面
 The requirement that the restriction of fe = P(g) to P  be equal to P  is necessary for the uniqueness of fe. The problem comes up when f is a constant map. Indeed, if f is the constant map defined such that f(a) = [w] for some fixed vector w ∈ F, it can be shown that any linear map g: Eb → F defined such that→− → g(a) = µw and g(u) =◦ ϕ(u)w for all u ∈ →−E, for some µ = 06 , and some linear form ϕ: E F satisfies f = P(g) i.
为了使铁的唯一性，必须限制铁=P（g）到P等于P。当f是一个常数映射时，问题就出现了。事实上，如果f是定义为f（a）=[w]的常数映射，对于某些固定向量w∈f，可以证明任何线性映射g:eb→f都定义为→−→g（a）=μw和g（u）=（u）w，对于所有u∈→−e，对于某些μ=06，和一些线性形式：e f满足f=p（g）i。
Proposition 25.17 shows that is the projective completion of the affine space E.
命题25.17表明，这是仿射空间e的射影完备。
The projective completion Ee of an affine space E is a very handy place in which to do geometry in, mainly because the following facts can be easily established.
仿射空间e的射影完备ee是一个非常方便的几何处理的地方，主要是因为下列事实可以很容易地建立起来。
There is a bijection between affine subspaces of E and projective subspaces of Ee not contained in P . Two affine subspaces of E are parallel iff the corresponding projective subspaces of Ee have the same intersection with the hyperplane at infinity P. There is also a bijection between affine maps from E to F and projective maps from Ee to Fe mapping the hyperplane at infinity P into the hyperplane at infinity P →−F . In the projective plane, two distinct lines intersect in a single point (possibly at infinity, when the lines are parallel). In the projective space, two distinct planes intersect in a single line (possibly at infinity, when the planes are parallel). In the projective space, a plane and a line not contained in that plane intersect in a single point (possibly at infinity, when the plane and the line are parallel).
e的仿射子空间与p中不包含的ee的投影子空间之间存在双射。e的两个仿射子空间是平行的，如果e的相应投影子空间在无穷大p处与超平面有相同的交集，则e到f的仿射映射与e到fe的投影映射之间也存在双射，将无穷大p处的超平面映射到超平面。在无穷大P→−F。在射影平面中，两条不同的直线相交于一个点（当直线平行时，可能在无穷远处）。在射影空间中，两个不同的平面在一条直线上相交（当平面平行时，可能在无穷远处）。在射影空间中，一个平面和一条不包含在该平面中的线相交于一个点（当平面和线平行时，可能在无穷远处）。
25.9	Making Good Use of Hyperplanes at Infinity
25.9充分利用无限远超平面
Given a vector space E and a hyperplane H in E, we have already observed that the projective spacesand P(E) are isomorphic. Thus, P(H) can be viewed as the hyperplane at infinity in P(E), and the considerations applying to the projective completion of an affine space apply to the affine patch EH on P(E). This fact yields a powerful and elegant method for proving theorems in projective geometry. The general schema is to choose some projective hyperplane P(H) in P(E), view it as the “hyperplane at infinity,” then prove an affine version of the desired result in the affine patch EH (the complement of P(H) in P(E), which has an affine structure), and then transfer this result back to the projective space P(E). This technique is often called “sending objects to infinity.” We refer the reader to geometry textbooks for a comprehensive development of these ideas (for example, Berger [11, 12], Samuel [138], Sidler [156], Tisseron [170], or Pedoe [132]), but we cannot resist presenting the projective versions of the theorems of Pappus and Desargues. Indeed, the method of sending points to infinity provides some strikingly elegant proofs. We begin with Pappus’s theorem, illustrated in Figure 25.20.
给定一个向量空间e和e中的超平面h，我们已经观察到射影空间和p（e）是同构的。因此，p（h）在p（e）中可视为无穷远的超平面，应用于仿射空间射影完备的考虑也适用于p（e）上的仿射面片eh。这一事实为证明射影几何中的定理提供了一种强大而优雅的方法。一般的模式是在p（e）中选择一些投影超平面p（h），将其视为“无穷远的超平面”，然后在仿射补丁eh（p（e）中p（h）的补码，它具有仿射结构）中证明所需结果的仿射版本，然后将该结果转移回射影空间P（E）。这种技术通常被称为“将物体发送到无限远的地方”。我们把读者引向几何教科书来全面发展这些思想（例如，伯杰[11，12]、塞缪尔[138]、西德勒[156]、蒂塞隆[170]或皮多[132]），但我们不能拒绝呈现投射的诗句。关于帕普斯定理和德沙格定理。实际上，将点发送到无穷大的方法提供了一些引人注目的优雅证明。我们从Pappus定理开始，如图25.20所示。
Proposition 25.18. (Pappus) Given any projective plane P(E) and any two distinct lines D and D0, for any distinct points a,b,c,a0,b0,c0, with a,b,c on D and a0,b0,c0 on D0, if
提案25.18。（pappus）给定任何投影平面p（e）和任何两条不同的线d和d0，对于任何不同的点a、b、c、a0、b0、c0，其中a、b、c在d上，a0、b0、c0在d0上，如果

Figure 25.20: Pappus’s theorem (projective version).
图25.20:Pappus定理（投影版本）。
a,b,c,a0,b0,c0 are distinct from the intersection of D and D0, then the intersection points p = hb,c0i ∩ hb0,ci, q = ha,c0i ∩ ha0,ci, and r = ha,b0i ∩ ha0,bi are collinear.
a、b、c、a0、b0、c0与d和d0的交点不同，那么交点p=hb、c0i hb0、ci、q=ha、c0i ha0、ci和r=ha、b0i ha0、bi是共线的。
Proof. First, since any two lines in a projective plane intersect in a single point, the points
证据。首先，由于射影平面上的任意两条直线相交于一个点，因此
hp,q,rXa0,b=iPare well defined. Choose ∆ =are parallel, and similarly(E) − ∆. Since ha,b0i andhb,chap,r0,bii intersect at a point at infinityas the line at infinity, and consider the affine planeb0,ci are parallel. Thus, by the affine version ofr on ∆, ha,b0i and h 0i and h
hp，q，rxa0，b=i定义良好。选择∆=平行，同样选择（e）−∆。由于ha、b0i和hb、chap、r0、bii在无穷远处与直线相交，因此认为仿射平面b0、ci是平行的。因此，通过∆、ha、b0i和h 0i和h上的r的仿射形式
Pappus’s theorem (Proposition 23.12), the lines ha,c0i andp,rhai, which means that0,ci are parallel, which meansp,q,r are that their intersection q is on the line at infinity ∆ = h collinear.	
Pappus定理（命题23.12），线ha，c0i和p，rhai，这意味着0，ci是平行的，这意味着sp，q，r是它们的交叉点q在无穷大的直线上∆=h共线。
By working in the projective completion of an affine plane, we can obtain an improved version of Pappus’s theorem for affine planes. The reader will have to figure out how to deal with the special cases where some of p,q,r go to infinity.
通过研究仿射平面的射影完备，我们可以得到仿射平面的帕普斯定理的一个改进版本。读者将不得不弄清楚如何处理一些特殊情况，其中p，q，r中的一些是无穷大的。
Now, we prove a projective version of Desargues’s theorem slightly more general than that given in Proposition 25.7. It is interesting that the proof is radically different, depending on the dimension of the projective space P(E). This is not surprising. In axiomatic presentations of projective plane geometry, Desargues’s theorem is independent of the other axioms. Desargues’s theorem is illustrated in Figure 25.21.
现在，我们证明了德沙格定理的一个射影形式，比25.7命题中给出的稍微更普遍一些。有趣的是，根据投影空间p（e）的尺寸，证明是完全不同的。这并不奇怪。在射影平面几何的公理表示中，德沙格定理独立于其他公理。德沙格定理如图25.21所示。
Proposition 25.19. (Desargues) Let P(E) be a projective space. Given two triangles (a,b,c) and (a0,b0,c0), where the points a,b,c,a0,b0,c0 are pairwise distinct and the lines A = hb,ci, B = ha,ci, C = ha,bi, A0 = hb0,c0i, B0 = ha0,c0i, C0 = ha0,b0i are pairwise distinct, if the
提案25.19。（德沙格）让p（e）是一个投影空间。给定两个三角形（a，b，c）和（a0，b0，c0），其中点a，b，c，a0，b0，c0是成对不同的，线a=hb，ci，b=ha，ci，c=ha，bi，a0=hb0，c0i，b0=ha0，c0i，c0=ha0，b0i是成对不同的，如果
25.9. MAKING GOOD USE OF HYPERPLANES AT INFINITY
25.9。充分利用无限远超平面
lines ha,a0i, hb,b0i, and hc,c0i intersect in a common point d distinct from a,b,c, a0,b0,c0, then the intersection points p = hb,ci ∩ hb0,c0i, q = ha,ci ∩ ha0,c0i, and r = ha,bi ∩ ha0,b0i belong to a common line distinct from A,B,C, A0,B0,C0.
线ha、a0i、hb、b0i和hc、c0i相交于与a、b、c、a0、b0、c0不同的公共点d，然后交点p=hb、ci hb0、c0i、q=ha、ci ha0、c0i和r=ha、bi ha0、b0i属于与a、b、c、a0、b0、c0不同的公共线。
Proof.A0,B0,CFirst, it is immediately shown that the line0. Let us assume that P(E) has dimension nh≥p,q3. If the seven pointsi is distinct from the linesd,a,b,c,aA,B,C0,b0,c,0 generate a projective subspace of dimension 3, then by Proposition 25.1, the intersection of the two planes ha,b,ci and ha0,b0,c0i is a line, and thus p,q,r are collinear.
证明.a0，b0，cfirst，它立即显示第0行。假设p（e）的维数nh≥p，q3。如果七个点si不同于线sd，a，b，c，aa，b，c0，b0，c，0生成一个维度3的投影子空间，那么根据命题25.1，两个平面ha，b，ci和ha0，b0，c0i的交点是一条线，因此p，q，r是共线的。
If P(E) has dimension n = 2 or the seven points d,a,b,c,a0,b0,c0 generate a projective subspace of dimension 2, we use the following argument. In the projective plane X generated by the seven points d,a,b,c,a0,b0,c0, choose the projective line ∆ = hp,ri as the line at infinity. Then in the affine plane Y = X −∆, the linesa,a0i, hhb,bb,c0ii, andand hhbc,c0,c00ii are either parallel orare parallel, and the lines ha,bi and ha0,b0i are parallel, and the lines h concurrent. Then by the converse of the affine version of Desargues’s theorem (Proposition
如果p（e）的维数n=2，或者七点d、a、b、c、a0、b0、c0生成维数2的投影子空间，我们使用以下参数。在由七个点d、a、b、c、a0、b0、c0生成的投影平面x中，选择投影线∆=hp，ri作为无穷大处的线。然后在仿射平面y=x−∆中，直线a、a0i、hhb、bb、c0ii和hhbc、c0、c0ii是平行的或是平行的，直线ha、bi和ha0、b0i是平行的，直线h是平行的。然后通过德沙格定理（命题）的仿射形式的逆
23.13)to the line at infinity ∆ =, the lines ha,ci and hhp,ra0,ci0, and thus thati are parallel, which means that their intersectionp,q,r are collinear.	q belongs
23.13）对于无穷大∆处的线，线ha、ci和hhp、ra0、ci0，因此i是平行的，这意味着它们的相交p、q、r是共线的。q属于


Figure 25.21: Desargues’s theorem (projective version).
图25.21：德沙格定理（射影版）。
The converse of Desargues’s theorem also holds. Using the projective completion of an affine space, it is easy to state an improved affine version of Desargues’s theorem. The reader will have to figure out how to deal with the case where some of the points p,q,r go to infinity. It can also be shown that Pappus’s theorem implies Desargues’s theorem. Many results of projective or affine geometry can be obtained using the method of “sending points to infinity.”
德沙格定理的逆命题也成立。利用仿射空间的射影完备，可以很容易地描述一个改进的德沙格定理的仿射形式。读者必须弄清楚如何处理点P，Q，R到无穷大的情况。也可以证明Pappus定理隐含了Desargues定理。射影几何或仿射几何的许多结果可以用“发送点到无穷大”的方法得到。
We now discuss briefly the notion of cross-ratio, since it is a major concept of projective geometry.
我们现在简单地讨论交叉比的概念，因为它是射影几何的一个主要概念。
25.10	The Cross-Ratio
25.10交叉比
Recall that affine maps preserve the ratio of three collinear points. In general, projective maps do not preserve the ratio of three collinear points. However, bijective projective maps preserve the “ratio of ratios” of any four collinear points (three of which are distinct). Such ratios are called cross-ratios (in French, “birapport”). There are several ways of introducing cross-ratios, but since we already have Proposition 25.5 at our disposal, we can circumvent some of the tedious calculations needed if other approaches are chosen.
回想一下，仿射映射保持三个共线点的比率。一般来说，投影图不保留三个共线点的比例。然而，双射射影映射保留了任何四个共线点（其中三个点是不同的）的“比率”。这种比率称为交叉比率（法语称为“birapport”）。有几种引入交叉比的方法，但是由于我们已经有了25.5号提案，如果选择了其他方法，我们可以绕过一些繁琐的计算。
Given a field K, say K = R, recall that the projective line P1K consists of all equivalence classes [x,y] of pairs (x,y) ∈ K2 such that (x,y) = (06 ,0), under the equivalence relation ∼ defined such that
给定一个场k，假设k=r，回想一下，射影线p1k由对（x，y）的所有等价类[x，y]组成∈k2，这样（x，y）=（06，0），在等价关系下定义如下：
	(x1,y1) ∼ (x2,y2)	iff	x2 = λx1	and	y2 = λy1,
（x1，y1）（x2，y2）iff x2=λx1和y2=λy1，
for some λ ∈ K−{0}. Letting ∞ = [1,0], the projective line P1K is in bijection with K∪{∞}. Furthermore, letting 0 = [0,1] and 1 = [1,1], the triple (∞,0,1) forms a projective frame for P1K. Using this projective frame and Proposition 25.5, we define the cross-ratio of four collinear points as follows.
对于某些λ∈k−0。设∞=[1,0]，投影线p1k为双射，k∞。另外，假设0=[0,1]和1=[1,1]，三重（∞，0,1）构成了p1k的投影框架，利用这个投影框架和命题25.5，我们定义了四个共线点的交叉比如下。
Definition 25.8. Given a projective line ∆ = P(D) over a field K, for any sequence (a,b,c,d) of four points in ∆, where a,b,c are distinct (i.e., (a,b,c) is a projective frame), the cross-ratio [a,b,c,d] is defined as the element h(d) ∈ P1K, where h: ∆ → P1K is the unique projectivity such that h(a) = ∞, h(b) = 0, and h(c) = 1 (which exists by Proposition 25.5, since (a,b,c) is a projective frame for ∆ and (∞,0,1) is a projective frame for P1K). For any projective space P(E) (of dimension ≥ 2) over a field K and any sequence (a,b,c,d) of four collinear points in P(E), where a,b,c are distinct, the cross-ratio [a,b,c,d] is defined using the projective line ∆ that the points a,b,c,d define. For any affine space E and any sequence (a,b,c,d) of four collinear points in E, where a,b,c are distinct, the cross-ratio [a,b,c,d] is defined by considering E as embedded in Ee.
定义25.8.给定一条在k域上的投影线∆=p（d），对于∆中四个点的任意序列（a、b、c、d），其中a、b、c是不同的（即（a、b、c）是投影帧），交叉比[a、b、c、d]定义为元素h（d）∈p1k，其中h：∆→p1k是唯一的投影性，因此h（a）=∞，h（b）=0，h（c）=1（通过命题25.5存在），因为（a，b，c）是∆的投影框，而（∞，0,1）是p1k的投影框。对于场k上的任何投影空间p（e）（尺寸≥2）和p（e）中四个共线点的任何序列（a、b、c、d），其中a、b、c是不同的，利用点a、b、c、d定义的投影线∆定义交叉比[a、b、c、d]。对于任意仿射空间e和e中四个共线点的任何序列（a，b，c，d），其中a，b，c是不同的，交叉比[a，b，c，d]是通过考虑e嵌入ee来定义的。
It should be noted that the definition of the cross-ratio [a,b,c,d] depends on the order of the points. Thus, there could be 24 = 4! different possible values depending on the permutation of {a,b,c,d}. In fact, there are at most 6 distinct values. Also, note that [a,b,c,d] = ∞ iff d = a, [a,b,c,d] = 0 iff d = b, and [a,b,c,d] = 1 iff d = c. Thus, [a,b,c,d] ∈ K − {0,1} iff d /∈ {a,b,c}.
应注意的是，交叉比[A、B、C、D]的定义取决于各点的顺序。因此，可能有24=4！不同的可能值取决于a、b、c、d的排列。实际上，最多有6个不同的值。另外，请注意，[a，b，c，d]=∞iff d=a，[a，b，c，d]=0 iff d=b，and[a，b，c，d]=1 iff d=c。因此，[a，b，c，d]∈k−0,1 iff d/∈a，b，c。
25.10. THE CROSS-RATIO
25.10条。交叉比
The following proposition is almost obvious, but very important. It shows that projectivities between projective lines are characterized by the preservation of the cross-ratio of any four points (three of which are distinct).
下面的命题几乎是显而易见的，但非常重要。结果表明，射影线之间的射影性具有保持任意四个点（其中三个点是不同的）的交叉比的特征。
Proposition 25.20. Given any two projective lines ∆ and ∆0, for any sequence (a,b,c,d) of points in ∆ and any sequence (a0,b0,c0,d0) of points in ∆0, if a,b,c are distinct and a0,b0,c0 are distinct, there is a unique projectivity f : ∆ → ∆0 such that f(a) = a0, f(b) = b0, f(c) = c0, and f(d) = d0 iff [a,b,c,d] = [a0,b0,c0,d0].
提案25.20。给定任意两条射影线∆和∆0，对于∆0点的任意序列（a，b，c，d）和∆0点的任意序列（a0，b0，c0，d0），如果a，b，c是不同的，a0，b0，c0是不同的，则有一个唯一的射影率f：∆→∆0，这样f（a）=a0，f（b）=b0，f（c）=c0，f（d）=d0 iff[a，b，c，d]=[a0，b0，c0，d0]。
Proof. First, assume that f : ∆ → ∆0 is a projectivity such that f(a) = a0, f(b) = b0, f(c) = c0, and f(d) = d0. Let h: ∆ → P1K be the unique projectivity such that h(a) = ∞, h(b) = 0, and h(c) = 1, and let h0 : ∆0 → PK1 be the unique projectivity such that h0(a0) = ∞, h0(b0) = 0, and h0(c0) = 1. By definition, [a,b,c,d] = h(d) and [a0,b0,c0,d0] = h0(d0). However, h0 ◦f : ∆ → P1K is a projectivity such that (h0 ◦f)(a) = ∞, (h0 ◦f)(b) = 0, and (h0 ◦f)(c) = 1, and by the uniqueness of h, we get h = h0 ◦ f. But then, [a,b,c,d] = h(d) = h0(f(d)) = h0(d0) = [a0,b0,c0,d0].
证据。首先，假设f：∆→∆0是一个投影性，这样f（a）=a0，f（b）=b0，f（c）=c0，f（d）=d0。设h：∆→p1k为唯一射影率，使h（a）=∞，h（b）=0，h（c）=1，设h0：∆0→pk1为唯一射影率，使h0（a0）=∞，h0（b0）=0，h0（c0）=1。根据定义，[a，b，c，d]=h（d）和[a0，b0，c0，d0]=h0（d0）。然而，h0 f：∆→p1k是一个投影性，因此（h0 f）（a）=∞，（h0 f）（b）=0和（h0 f）（c）=1，并且通过h的唯一性，我们得到h=h0 f。但是，然后，[a，b，c，d]=h（d）=h0（f（d））=h0（d0）=[a0，b0，c0，d0]。
Conversely, assume that [a,b,c,d] = [a0,b0,c0,d0]. Since (a,b,c) and (a0, b0, c0) are projective frames, by Proposition 25.5, there is a unique projectivity g: ∆ → ∆0 such that g(a) = a0, g(b) = b0, and g(c) = c0. Now, h0 ◦ g: ∆ → P1K is a projectivity such that (h0 ◦ g)(a) = ∞, (h0 ◦ g)(b) = 0, and (h0 ◦ g)(c) = 1, and thus, h = h0 ◦ g. However, h0(d0) = [a0,b0,c0,d0] = [a,b,c,d] = h(d) = h0(g(d)), and since h0 is injective, we get d0 = g(d).	
相反，假设[a，b，c，d]=[a0，b0，c0，d0]。由于（a，b，c）和（a0，b0，c0）是射影帧，根据命题25.5，有一个唯一的射影度g：∆→∆0，这样g（a）=a0，g（b）=b0，g（c）=c0。现在，h0 g：∆→p1k是一个投影性，这样（h0 g）（a）=∞，（h0 g）（b）=0，和（h0 g）（c）=1，因此，h=h0 g。然而，h0（d0）=[a0，b0，c0，d0]=[a，b，c，d]=h（d）=h0（g（d）），由于h0是注射剂，我们得到d0=g（d）。
As a corollary of Proposition 25.20, given any three distinct points a,b,c on a projective line ∆, for every λ ∈ P1K there is a unique point d ∈ ∆ such that [a,b,c,d] = λ.
作为命题25.20的一个推论，给定射影线∆上任意三个不同的点a、b、c，对于每一个λ∈p1k，都有一个唯一的点d∈∆使得[a、b、c、d]=λ。
In order to compute explicitly the cross-ratio, we show the following easy proposition.
为了明确计算交叉比，我们给出了以下简单的命题。
Proposition 25.21. Given any projective line ∆ = P(D), for any three distinct points a,b,c in ∆, if a = p(u), b = p(v), and c = p(u + v), where (u,v) is a basis of D, and for any
提案25.21。给定任何投影线∆=p（d），对于∆中的任何三个不同点a、b、c，如果a=p（u），b=p（v）和c=p（u+v），其中（u，v）是d的基，并且对于任何
[λ,µ]∼ ∈ P1K and any point d ∈ ∆, we have
[λ，μ]p1k和任意点d∆，我们有
	d = p(λu + µv)	iff	[a,b,c,d] = [λ,µ]∼.
d=p（λu+μv）iff[a，b，c，d]=[λ，μ]。
Proof. If (e1,e2) is the basis of K2 such that e1 = (1,0) and e2 = (0,1), it is obvious that p(e1) = ∞, p(e2) = 0, and p(e1 + e2) = 1. Let f : D → K2 be the bijective linear map such that f(u) = e1 and f(v) = e2. Then f(u + v) = e1 + e2, and thus f induces the unique projectivity P(f): P(D) → P1K such that P(f)(a) = ∞, P(f)(b) = 0, and P(f)(c) = 1.
证据。如果（e1，e2）是k2的基础，使得e1=（1,0）和e2=（0,1），很明显p（e1）=∞，p（e2）=0，和p（e1+e2）=1。设f:d→k2为双射线性映射，使f（u）=e1，f（v）=e2。然后f（u+v）=e1+e2，因此f诱导独特的投射性p（f）：p（d）→p1k，使p（f）（a）=∞，p（f）（b）=0和p（f）（c）=1。
Then
然后
P(f)(p(λu + µv)) = [f(λu + µv)]∼ = [λe1 + µe2]∼ = [λ,µ]∼,
p（f）（p（λu+μv））=[f（λu+μv）]至=[λe1+μe2]至=[λ，μ]至，
that is,
也就是说，
	d = p(λu + µv)	iff	[a,b,c,d] = [λ,µ]∼,
d=p（λu+μv）iff[a，b，c，d]=[λ，μ]，
as claimed.	
如要求。
We can now compute the cross-ratio explicitly for any given basis (u,v) of D. Assume that a,b,c,d have homogeneous coordinates [λ1,µ1], [λ2,µ2], [λ3,µ3], and [λ4,µ4] over the projective frame induced by (u,v). Letting wi = λiu + µiv, we have a = p(w1), b = p(w2), c = p(w3), and d = p(w4). Since a and b are distinct, w1 and w2 are linearly independent, and we can write w3 = αw1 + βw2 and w4 = γw1 + δw2, which can also be written as
我们现在可以显式计算d的任何给定基（u，v）的交叉比。假设a、b、c、d在（u，v）诱导的投影帧上具有均匀坐标[λ1，μ1]、[λ2，μ2]、[λ3，μ3]和[λ4，μ4]。假设wi=λiu+μiv，我们得到a=p（w1），b=p（w2），c=p（w3），d=p（w4）。由于a和b是不同的，w1和w2是线性无关的，我们可以写w3=αw1+βw2和w4=γw1+δw2，也可以写为
,
，
and by Proposition 25.21, [. However, since w1 and w2 are linearly independent, it is possible to solve for α,β,γ,δ in terms of the homogeneous coordinates, obtaining expressions involving determinants:
根据25.21号提案，[然而，由于w1和w2是线性无关的，因此可以用齐次坐标解α、β、γ、δ，得到涉及行列式的表达式：
,
，
and thus, assuming that d =6	a, we get
因此，假设d=6a，我们得到
.
.
When d = a, we have [a,b,c,d] = ∞. In particular, if ∆ is the projective completion of an affine line D, then µi = 1, and we get
当d=a时，我们得到[a，b，c，d]=∞。特别地，如果∆是仿射线d的投影完成，那么μi=1，我们得到
.
.
When d = ∞, we get
当d=∞时，我们得到
,
，
which is just the usual ratio (although we defined it earlier as −ratio(a,c,b)).
这只是通常的比率（尽管我们之前将其定义为−比率（a，c，b））。
We briefly mention some of the properties of the cross-ratio. For example, the crossratio [a,b,c,d] is invariant if any two elements and the complementary two elements are transposed, and letting 0−1 = ∞ and ∞−1 = 0, we have
我们简单地提到了交叉比的一些性质。例如，如果任意两个元素和互补的两个元素被转置，那么交叉比[a，b，c，d]是不变的，并且让0−1=∞和∞−1=0，我们得到
[a,b,c,d] = [b,a,c,d]−1 = [a,b,d,c]−1
[A，B，C，D]=[B，A，C，D]-1=[A，B，D，C]-1
and
和
[a,b,c,d] = 1 − [a,c,b,d].
【A、B、C、D】=1−【A、C、B、D】。
25.10. THE CROSS-RATIO
25.10条。交叉比
Since the permutations of {a,b,c,d} are generated by the above transpositions, the cross-λ = [a,b,c,d], if λ ∈ {∞,0,1}, then any permutation ratio takes at most six values. Letting of {a,b,c,d} yields a cross-ratio in {∞,0,1}, and if λ /∈ {∞,0,1}, then there are at most the six values λ,	.
由于a、b、c、d的置换是由上述置换产生的，因此交叉λ=[a、b、c、d]，如果λ∈∞，0,1，则任何置换比最多取6个值。放开a，b，c，d得出∞，0,1中的交叉比，如果λ/∞，0,1，则最多有六个值。
It can be shown that the function
可以看出，函数

takes a constant value on the six values listed above.
对上面列出的六个值取一个常量值。
We also define when four points form a harmonic division. For this, we need to assume that K is not of characteristic 2.
我们还定义了当四个点形成一个调和除法。为此，我们需要假设k不是特征2。
Definition 25.9. Given a projective line ∆, we say that a sequence of four collinear points
定义25.9.给定一条射影线∆，我们称为四个共线点的序列
([a,b,c,da,b,c,d] =) in ∆ (where−1, we also say thata,b,c are distinct) forms ac and d are harmonic conjugatesharmonic divisionofif [aa,b,c,dand b.] = −1. When
（[a，b，c，da，b，c，d]=）在∆中（其中−1，我们也说a，b，c是不同的）形式ac和d是谐波共轭的sharmonic分型of[aa，b，c，d and b.]=−1。什么时候？
If a,b,c are distinct collinear points in some affine space, from
如果a，b，c是某些仿射空间中不同的共线点，从
,
，
we note that c is the midpoint of (a,b) iff [a,b,c,∞] = −1a,b,c,d, that is, if) on the real line, where(a,b,c,∞) forms a harmonic division. Figure 25.22 shows a harmonic division ( the coordinates of (a,b,c,d) are (−2,2,1,4).
我们注意到，c是（a，b）iff[a，b，c，∞]=-1a，b，c，d的中点，也就是说，如果）在实线上，其中（a，b，c，∞）形成一个调和除法。图25.22显示了谐波划分（a、b、c、d）的坐标为（−2、2、1、4）。
	a	c	b	d
A C B D

Figure 25.22: Four points forming a harmonic division.
图25.22：构成谐波分区的四个点。
If ∆ = P1K and a,b,c,d are all distinct from ∞, then we see immediately from the formula
如果∆=p1k和a、b、c、d都与∞不同，那么我们可以立即从公式中看到
that [a,b,c,d] = −1 iff	.
即[a，b，c，d]=-1 iff。
We also check immediately that [a,b,c,∞] = −1 iff
我们还立即检查[a，b，c，∞]=−1 iff
a + b = 2c.
A+B=2c。
There is a nice geometric interpretation of harmonic divisions in terms of quadrangles (or complete quadrilaterals). Consider the quadrangle (projective frame) (a,b,c,d) in a hprojective plane, and letd,bi and ha,ci, and c0 be the intersection ofa0 be the intersection ofhd,cihandd,aiha,bandi. If we lethb,ci, b0 be the intersection ofg be the intersection
有一个很好的几何解释谐波划分的四角（或完全四边形）。在hprojective平面中考虑四边形（投影框）（a、b、c、d），Letd、bi和ha、ci和c0是hd、cihandd、aiha、bandi的交点。如果我们遗忘了，ci，b0是g的交集，是g的交集。
of ha,bi and ha0,b0i, then it is an interesting exercise to show that (a,c,b,d) as a projective frame and to computea,b,g,c0) is a harmonic division. One way to prove this is to pick (
关于ha，bi和ha0，b0i，那么证明（a，c，b，d）作为一个投影框架和计算，b，g，c0）是一个调和除法是一个有趣的练习。证明这一点的一种方法是（
the coordinates of,b,g,c0], which is computed using the above formula. Another way is to send some wella0,b0,c0, and g. Then because ha,ci is the line at infinity, [a,b,g,c0] =
b，g，c0]的坐标，用上述公式计算。另一种方法是发送一些wella0、b0、c0和g。然后，因为ha、ci是无穷远的直线，[a、b、g、c0]。=
[chosen points to infinity; see Berger [11] (Chapter 6, Section 6.4).∞
[选择的点指向无穷大；见Berger[11]（第6章，第6.4节）。∞

Figure 25.23: A quadrangle, and harmonic divisions.
图25.23：四边形和谐波分区。
In fact, it can be shown that the following quadruples of lines induce harmonic divihsions: (ha,dc,aii,,hhba00,a,b00ii,)hond,bhic,d,hbi0,c; see Figure 25.23. For more on harmonic divisions, the inter-0i) on ha,bi, (hb,ai,hc0,a0i, hd,ci,hc0,b0i) on ha,ci, and (hb,ci, a0,c0i,h
事实上，可以看出，下列四重线引起谐波分裂：（ha，d c，aii，，hhba00，a，b00ii，）hond，bhic，d，hbi0，c；见图25.23。关于谐波划分的更多信息，Ha、Bi（hb、ai、hc0、a0i、hd、ci、hc0、b0i）和Ha、ci和（hb、ci、a0、c0i、h）上的inter-0i
ested reader should consult any text on projective geometry (for example, Berger [11, 12], Samuel [138], Sidler [156], Tisseron [170], or Pedoe [132]).
尊敬的读者应该参考任何有关射影几何的文本（例如，Berger[11，12]、Samuel[138]、Sidler[156]、Tisseron[170]或Pedoe[132]）。
25.11 Fixed Points of Homographies and Homologies; Homographies of RP1 and RP2
25.11同系物和同系物的固定点；RP1和RP2的同系物
PLet(EP)(be homography (or projectivity) ofE) be a projective space where E is a vector space over some fieldP(E) where h is given by the linear isomorphismK, and let h: P(E) → f : E → E so that h = P(f). Observe that if u ∈ E is an eigenvector of f for some eigenvalue
Plet（e p）（e的同构（或射影性）是一个射影空间，其中e是某个场p（e）上的向量空间，其中h由线性同构mk给出，并让h:p（e）→f:e→e使h=p（f）。观察，如果u∈e是某个特征值f的特征向量

λ ∈ K, then h([u]) = [f(u)] = [λu] = [u]
λ∈k，则h（[u]）=[f（u）]=[λu]=[u]
since λ = 06 because f is an isomorphism, which means that the point [u] ∈ P(E) is a fixed pointh of h. In other words, eigenvectors of f induce fixed points of h = P(f).
因为λ=06，因为f是同构的，这意味着点[u]∈p（e）是h的不动点，换句话说，f的特征向量诱导h=p（f）的不动点。
Consequently, it makes sense to try to classify homographies in terms of their fixed points. Of course this depends on the field K. If K is algebraically closed, for instance K = C, then all the eigenvalues of f belong to K, and we can use the Jordan form of a matrix representing f. If K = R, which is of particular interest to us, then we can use the real Jordan form, and we can obtain a compete classification for E = R2 and E = R3. We will also see that special kinds of homographies that leave every point of some projective hyperplane P(H) fixed, called homologies, play a special role.
因此，试着根据不动点对同素词进行分类是有意义的。当然，这取决于场k。如果k是代数闭合的，例如k=c，那么f的所有特征值都属于k，我们可以使用表示f的矩阵的乔丹形式。如果k=r，这对我们特别有意义，那么我们可以使用真实的乔丹形式，我们可以得到c。e=r2和e=r3的综合分类。我们还将看到，使某些投影超平面p（h）的每个点保持不变的特殊类同构，称为同构，起着特殊的作用。
We begin with the classification of the homographies of the real projective line RP1. Since a homography h of RP1 is represented by a real invertible 2 × 2 matrix
我们从实射影线rp1的同构图分类开始。因为Rp1的同构式h由一个实可逆的2×2矩阵表示。
 ,
，
and since A either 0, 1, or 2, real eigenvalues, the homography h has 0, 1, or 2 fixed points.
因为0，1，或2，实特征值，所以同形H有0，1，或2个不动点。
Definition 25.10. A homography of the real projective line RP1 not equal to the identity is elliptic if is has no fixed point, parabolic if it has a single fixed point, or hyperbolic if it has two fixed points.
定义25.10.不等于恒等式的实射影线rp1的同形是椭圆的，如果没有不动点，则是抛物线；如果有单不动点，则是双曲的，如果有两个不动点。
(1)	Elliptic homographies. In this case, (a + d)2 − 4(ad − bc) < 0, so A has two distinct complex conjugate eigenvalues α ± iβ, and in C2, they correspond to two complex eigenvectors w1 = u + iv and w2 = u − iv, with u,v ∈ R2. Since
椭圆同形。在这种情况下，（a+d）2−4（ad−bc）<0，因此a有两个不同的复共轭特征值α±iβ，在c2中，它们对应于两个复特征向量w1=u+i v和w2=u−iv，其中u，v∈r2。自从
f(w1) = (α − iβ)w1
F（w1）=（α−iβ）w1
we obtain
我们得到
f(u) + if(v) = αu + βv + i(−βu + αv),
F（u）+如果（v）=αu+βv+i（−βu+αv），
which shows that in the basis (u,v), the homography h is represented by the matrix
这表明在基（u，v）中，用矩阵表示同形H。
 .
.
If we let θ ∈ (0,2π) be the angle given by
如果我们让θ∈（0,2π）为

and write then	
然后写
which corresponds to a similarity. Observe that h is an involution, that is, h2 = id iff θ = π/2.
相当于相似性。观察h为对合，即h2=id iffθ=π/2。
(2)	Parabolic homographies. In this case, we must have (a + d)2 − 4(ad − bc) = 0. The matrix A is not diagonalizable and it has a Jordan form of the form
抛物线均形。在这种情况下，我们必须（a+d）2−4（ad−bc）=0。矩阵A不可对角化，它具有形式的约旦形式
.
.
In the affine line y = 1, a parabolic homography behaves like the translation by 1/λ.
在仿射线y=1中，抛物线同形表示为1/λ的平移。
(3)	Hyperbolic homographies. In this case, (a+d)2 −4(ad−bc) > 0, so A has two distinct nonzero reals eigenvalues λ and µ, and in a basis of eigenvectors it is represented by the diagonal matrix
双曲同形。在这种情况下，（a+d）2−4（ad−bc）>0，因此a有两个不同的非零实特征值λ和礹，在特征向量的基础上，它由对角矩阵表示。
.
.
If P and Q are the distinct fixed points of the the homography h, it is not hard to show that for every M ∈ RP1 such that M =6 P,Q, we have
如果p和q是同形H的不同不动点，则不难证明对于每一个m∈rp1，m=6p，q，我们有
[P,Q,M,h(M)] = k
[P，Q，M，H（M）]=K
where k = λ/µ. For example, see Sidler [156] (Chapter 3, Proposition 3.3.1), and Berger [11] (Lemma 6.6.3). It can also be shown that h is an involution (h2 = id) with two distinct fixed points P and Q iff a + d = 0 iff k = −1 in the above equation; see Sidler [156] (Chapter 3, Proposition 3.3.2), and Samuel [138] (Section 2.4).
其中k=λ/μ。例如，参见Sidler[156]（第3章，提案3.3.1）和Berger[11]（Lemma 6.6.3）。也可以证明，h是一个对合（h2=id），在上述方程中有两个不同的不动点p和q iff a+d=0 iff k=−1；见Sidler[156]（第3章，命题3.3.2）和Samuel[138]（第2.4节）。
We now classify the homographies of RP2. Since the characteristic polynomial of a 3×3 real matrix A has degree 3 and since every real polynomial of degree 3 has at least one real zero, A has some real eigenvalue. Since C is algebraically closed, every complex polynomial of degree 3 has three zeros (counted with multiplicity), in which case, all three eigenvalues of a 3 × 3 complex matrix A belong to C. Thus we have the following useful fact.
我们现在对rp2的同构图进行分类。因为3×3实矩阵A的特征多项式有3次，而且3次的每一实多项式至少有一个实零，所以A有一些实特征值。因为C是代数闭的，所以三次的每一个复多项式都有三个零（用重数计数），在这种情况下，一个3×3复矩阵A的三个特征值都属于C，因此我们有以下有用的事实。
Proposition 25.22. Every homography of the real projective plane RP2 or of the complex projective plane CP2 has at least one fixed point.
提案25.22.实射影平面rp2或复射影平面cp2的每一个同形都至少有一个固定点。
Here is the classification of the homographies of RP2 based on the real Jordan form of a 3×3 matrix. Most details are left as exercises. We denote by Γ the 3×3 matrix representing the real Jordan form of the matrix of the linear map representing the homography h.
这里是基于3×3矩阵的实约但形式的RP2同构图的分类。大部分细节留作练习。我们用_表示3×3矩阵，表示表示表示同形H的线性映射矩阵的实乔丹形式。
(I)	Three real eigenvalues α,β,γ. The matrix Γ has the form
三个实特征值α，β，γ。矩阵_的形式
 ,
，
with α,β,γ ∈ R nonzero and all distinct. As illustrated in Figure 25.24, the homography h has three fixed points P,Q,R, forming a triangle. The sides (lines) of this triangle are invariant under h. The restriction of h to each of these sides is hyperbolic.
α、β、γ∈R非零且全部不同。如图25.24所示，同形H有三个固定点P、Q、R，形成三角形。这个三角形的边（线）在h下是不变的。h对这些边的限制是双曲线的。

Figure 25.24: Case (I): The left figure is the hyperplane representation of RP2 and a homography with fixed points P,Q,R. The purple (linear) hyperplane maps to itself in a manner which is not the identity.
图25.24：案例（i）：左边的图是rp2的超平面表示和不动点p、q、r的同形图。紫色（线性）超平面以非同一性的方式映射到自身。
(II)	One real eigenvalue α and two complex conjugate eigenvalues. Then Γ has the form
一个实特征值α和两个复共轭特征值。那么_有表格了
 ,
，
with α,γ ∈ R nonzero. The homography h, which is illustrated in Figure 25.25, has one fixed point P, and a line ∆ invariant under h and not containing P. The restriction of h to ∆ is elliptic.
α，γ∈R非零。图25.25所示的同形图h有一个不动点p，h下有一条不含p的直线∆不变量。h对∆的限制是椭圆的。

Figure 25.25: Case (II): The left figure is the hyperplane representation of RP2 and a homography with fixed point P and invariant line ∆. The purple (linear) hyperplane maps to itself under a rotation and rescaling.
图25.25：情况（ii）：左图是rp2的超平面表示和具有固定点p和不变线∆的同形图。紫色（线性）超平面在旋转和重新缩放下映射到自身。
(III)	Two real eigenvalues α,β. The matrix Γ has the form
两个实特征值α，β。矩阵_的形式
 ,
，
with α,β ∈ R nonzero and distinct. The homography h, as illustrated in Figure 25.26, has one fixed point P, and a line ∆ invariant under h and not containing P. The restriction of h to ∆ is the identity. Every line through P is invariant under h and the restriction of h to this line is hyperbolic.
α，β∈R非零且不同。如图25.26所示，同形图h有一个不动点p，h下的直线∆不变，不含p。h对∆的限制是恒等式。通过p的每一条线在h下都是不变的，h对这条线的限制是双曲线的。
(IV)	One real eigenvalue α. The matrix Γ has the form
一个实特征值α。矩阵_的形式
 ,
，
with α ∈ R nonzero. As illustrated by Figure 25.27, the homography h has one fixed point P, and a line ∆ invariant under h containing P. The restriction of h to ∆ is the identity. Every line through P is invariant under h and the restriction of h to this line is parabolic.
α∈R非零。如图25.27所示，同形图H有一个不动点P，H下的直线∆不变，包含P。H对∆的限制是同一性。通过p的每一条线在h下都是不变的，h对这条线的约束是抛物线的。

Figure 25.26: Case (III): The left figure is the hyperplane representation of RP2 and a homography with fixed point P and invariant line ∆. The purple (linear) hyperplane maps to itself under rescaling; as such the restriction of the homography to ∆ is the identity. The green (linear) hyperplane also is invariant under the homography, but the invariance is not given by the identity map.
图25.26：情况（iii）：左图是rp2的超平面表示和具有固定点p和不变线∆的同形图。紫色（线性）超平面在重新缩放下映射到自身；因此，同形性对∆的限制是同一性。绿色（线性）超平面在同形下也是不变的，但其不变性不是由同一映射给出的。

Figure 25.27: Case (IV): The left figure is the hyperplane representation of RP2 and a homography with fixed point P and invariant line ∆ containing P. The purple (linear) hyperplane maps to itself under rescaling; as such the restriction of the homography to ∆ is the identity. The green (linear) hyperplane also is invariant under the homography, but the invariance is not given by the identity map.
图25.27：案例（iv）：左边的图是rp2的超平面表示和一个具有固定点p和含有p的不变线∆的同形图。紫色（线性）超平面在重新缩放下映射到自身；因此，同形图对∆的限制是同一性。绿色（线性）超平面在同形下也是不变的，但其不变性不是由同一映射给出的。
(V)	Two real eigenvalues α,β. The matrix Γ has the form
两个实特征值α，β。矩阵_的形式
 ,
，
with α,β ∈ R nonzero and distinct. The homography h, which is illustrated in Figure 25.28, has two fixed points P and Q. The line hP,Qi is invariant under h, and there is is another line ∆ through Q invariant under h. The restriction of h to ∆ is parabolic, and the restriction of h to hP,Qi is hyperbolic.
α，β∈R非零且不同。图25.28所示的同形图h有两个不动点p和q。线hp，qi在h下不变，还有一条线∆到q在h下不变。h对∆的限制是抛物线的，h对hp，qi的限制是双曲线的。

Figure 25.28: Case (V): The left figure is the hyperplane representation of RP2 and a homography with fixed points P,Q and invariant line ∆. Both the purple and green (linear) hyperplanes are invariant under the homography, but the invariance is not given by the identity map.
图25.28：情况（v）：左图是rp2的超平面表示和具有固定点p、q和不变线∆的同形图。紫色和绿色（线性）超平面在同形下都是不变的，但其不变性不是由同一映射给出的。
(VI)	One real eigenvalue α. The matrix Γ has the form
一个实特征值α。矩阵_的形式
 ,
，
with α ∈ R nonzero. The homography h, which is illustrated in Figure 25.29, has one fixed point P, and a line ∆ invariant under h containing P. The restriction of h to ∆ is parabolic.
α∈R非零。图25.29所示的同形图H有一个固定点P，在H下有一条直线∆不变量，其中包含P。H对∆的限制是抛物线的。
For the classification of the homographies of CP2, Case (II) becomes Case (I).
对于CP2的同形图分类，案例（i i）变为案例（i）。

Figure 25.29: Case (VI): The left figure is the hyperplane representation of RP2 and a homography with fixed point P and invariant line ∆. The purple (linear) hyperplane maps to itself in a manner which is not the identity.
图25.29：案例（vi）：左图是rp2的超平面表示和具有固定点p和不变线∆的同形图。紫色（线性）超平面以非同一性的方式映射到自身。
Observe that in Cases (III) and (IV), the homography h has a line ∆ of fixed points, as well as a fixed point P. In Case (III), P /∈P ∆, and in Case (IV),is called the center and the line ∆ is calledP ∈ ∆. This kind of homography is called a homology. The point the axis (or base). Some authors only use the term homology when P /∈ ∆, and when P ∈ ∆, they use the term elation. When P ∈ ∆, other authors use the termO (instead of P). projective transvection, which we prefer. The center is usually denoted by
观察在情况（iii）和（iv）中，同形图h有一条不动点∆线和一条不动点p。在情况（iii）中，p/∈p∆，在情况（iv）中，称为中心，而线∆称为dp∈∆。这种同形被称为同源。轴（或基准）的点。有些作者只在p/∈∆时使用术语同调，而当p∈∆时使用术语关联。当p∈∆时，其他作者使用termo（而不是p）。投影变换，我们更喜欢。中心通常用
One of the nice features of homologies (and projective transvections) is that there is a nice geometric construction of the image h(M) of a point M in terms of the center O, the axis ∆, and any pair (A,A0) where A0 = h(A), A 6= O, and A /∈ ∆.
同系物（和射影变换）的一个很好的特征是，一个点m的图像h（m）有一个很好的几何结构，关于中心o，轴∆，以及任何一对（a，a0），其中a0=h（a），a 6=o，和a/∈∆。
throughThis construction is possible because for any pointO. This can be proved using Desargues’ Theorem; for example, see Silder [156]M =6	O, the line hM,h(M)i passes
通过这个构造是可能的，因为对于任何点。这可以用Desargues定理来证明；例如，参见Silder[156]m=6 o，线hm，h（m）i通过
(Chapter 4, Section 4.2). We will prove this property for a generalization of homologies to any projective space P(E), where E is a vector space of any finite dimension.
（第4章第4.2节）。我们将证明这一性质，以推广到射影空间p（e）的同系物，其中e是任何有限维的向量空间。
linelineFor the construction, first assume thathhA,Mi intersects ∆ in some point I. SinceM =6	OI is not on the line∈ ∆, it is fixed byA,Ii, its imagehA,Ah, so the image of the0iM. In this case, the0 = h(M) is on
线条对于施工，首先假设hha，mi与∆相交于某一点i。sincem=6 oi不在∈∆线上，它由a，ii，它的图像ha，ah固定，因此图像为0im。在这种情况下，0=h（m）开启
A,Ii is the line hA0,Ii, and since M is on the line h the line hA0,Ii. But M0 = h(M) is also on the line hO,Mi, which implies that M0 = h(M) is the intersection point of the lines hA0,Ii and hO,Mi; see Figure 25.30.
A，II是线HA0，II，因为M在H线上，所以是线HA0，II。但m0=h（m）也在ho，mi线上，这意味着m0=h（m）是ha0，ii和ho，mi线的交点；见图25.30。
If M 6= O is on the line hA,A0i, then we use the construction of the image B0 of some pointintersectionB 6= OJand not onof hM,Bi and ∆, and thenhA,A0i as before, and then repeat the construction by finding theM0 = h(M) is the intersection point of hB0,Ji and hA,A0i; see Figure 25.31.
如果m 6=o在ha，a0i线上，那么我们使用一些点相交b 6=oj的图像b0的构造，而不是hm，bi和∆，然后像以前一样使用ha，a0i，然后重复构造，找到them0=h（m）是hb0，ji和ha，a0i的交点；见图25.31。

Figure 25.30: The three step process for determining the homology point h(M) = M0 when
图25.30：确定同源点h（m）=m0的三步过程
M is not on the line hA,A0i. Step 1 finds the intersection between the extension ofA0,Ii. Step 3 extends hO,M0i and determines its intersectionhA,Mi and ∆. Step 2 forms the line h with hA0,Ii. The intersection point is M0.
m不在ha，a0i线上。步骤1找到0，ii延伸段之间的交点。步骤3扩展ho、m0i并确定其相交ha、mi和∆。第2步用HA0、II组成H线。交叉点是m0。

Figure 25.31: The five step process for determining the homology point h(M) = M0 when intersection betweenM is on the line hA,AhM,B0i. Steps 1 through 3 determine the linei and ∆, namely J. Step 5 forms the linehB,BhJ,B0i. Step 4 finds the0i and intersects it with hA,A0i. The intersection point is M0.
图25.31：当直线ha、ahm、b0i相交时，确定同源点h（m）=m0的五步过程。步骤1至3确定直线i和∆，即j。步骤5形成直线hb、bhj、b0i。步骤4找到0i并与ha、a0i相交。交叉点iS M0。
The above construction also works if O ∈ ∆; see Figures 25.32 and 25.33.
如果o∈∆，上述结构也可以工作；见图25.32和25.33。

Figure 25.32: The three step process for determining the elation point h(M) = M0 when M is not on the line hA,A0i. Step 1 finds the intersection between the extension of hA,Mi and ∆. Step 2 forms the line hA0,Ii. Step 3 extends hA0Ii and determines its intersection with hO,Mi. The intersection point is M0.
图25.32：当m不在ha，a0i线上时，确定相关点h（m）=m0的三步过程。步骤1找到ha，mi和∆的延伸段之间的交叉点。步骤2形成线HA0，II。步骤3扩展HA0II并确定其与HO、MI的交叉点。交叉点是m0。
Another useful property of homologies (here, O /∈ ∆) is that for any line d passing through the center O, if I is the intersection point of the line d and ∆, then for any M ∈ d distinct from O and not on ∆ and its image M0, the cross-ratio [O,I,M,M0] is independent of d. If [O,I,M,M0] = −1 for all M =6 O, we say that h is a harmonic homology. It can be shown that a homography h is a harmonic homology iff h is an involution (h2 = id); see Silder [156] (Chapter 4, Section 4.4). It can also be shown that any homography of RP2 can be expressed as the composition of two homologies; see Silder [156] (Chapter 4, Section 4.5).
同系物的另一个有用性质（这里，o/∈∆）是对于任何通过圆心o的d线，如果i是d线和∆线的交点，那么对于任何与o不同的m∈d，而不是在∆及其图像m0上，交叉比[o，i，m，m0]与d无关。如果[o，i，m，m0]。=-1对于所有m=6o，我们说h是调和同调。可以证明，同形H是调和同调，如果H是对合（h2=id）；见Silder[156]（第4章，第4.4节）。也可以证明，rp2的任何同形性可以表示为两个同源性的组成；见silder[156]（第4章，第4.5节）。
We now consider the generalization of the notion of homology (and projective transvection) to any projective space P(E), where E is a vector space of any finite dimension over a field K. We need to review a few concepts from Section 7.15.
我们现在考虑同调概念（和射影变换）到任何射影空间p（e）的推广，其中e是K域上任何有限维的向量空间。我们需要回顾7.15节中的一些概念。
Let E be a vector space and let H be a hyperplane in E. Recall from Definition 7.6 that for any nonzero vector u ∈ E such that u 6∈ H, and any scalar α = 06 ,1, a linear map f : E → E such that f(x) = x for all x ∈ H and f(x) = αx for every x ∈ D = Ku is called a dilatation of hyperplane H, direction D, and scale factor α. See Figure 25.34.
设e为向量空间，设h为e中的超平面。从定义7.6中回忆，对于任何非零向量u∈e，使u 6∈h，以及任何标量α=06，1，线性映射f:e→e，使f（x）=x代表所有x∈h和f（x）=αx代表每个x∈d=ku，称为超平面的扩张。e h、方向d和比例因子α。见图25.34。
From Definition 7.7, for any nonzero nonlinear form ϕ ∈ E∗ defining H (which means that H = Ker(ϕ)) and any nonzero vector u ∈ H, the linear map τϕ,u given by
根据定义7.7，对于任意非零非线性形式，定义h（即h=ker（_））和任意非零向量u h，线性映射τ_，u由下式给出
	τϕ,u(x) = x + ϕ(x)u,	ϕ(u) = 0,
τ，u（x）=x+（x）u，（u）=0，
for all x ∈ E is called a transvection of hyperplane H and direction u. See Figure 25.35.
对于所有x∈e，称为超平面h和方向u的矢量变换。见图25.35。

 

Figure 25.33: The five step process for determining elation point h(M) = M0 when M is on
图25.33：M开启时确定关联点h（m）=m0的五步过程
The intersection point isthe linebetweenhhA,AM,B0ii. Steps 1 through 3 determine the lineand ∆, namelyM0.	J. Step 5 forms the linehB,BhJ,B00ii. Step 4 finds the intersectionand intersects it with hA,A0i.
交叉点是NHHA、AM、B0II之间的直线。步骤1到3确定直线和∆，名称lYm0.j。步骤5形成直线hb，bhj，b00ii。步骤4找到交叉点并将其与ha，a0i交叉。

Figure 25.34: A dilation f of the xy-plane in direction u = (1,1,1). Every vector v not in the xy-plane determines a rose-colored plane through u, and the image f(v) is an element of this rose hyperplane since it is stretched in the u direction.
图25.34:u方向上xy平面的膨胀f=（1,1,1）。不在xy平面中的每个向量v都通过u确定一个玫瑰色平面，而图像f（v）是这个玫瑰色超平面的一个元素，因为它是在u方向拉伸的。

Figure 25.35: A transvection τϕ,u of the xy-plane in direction u = (0,1,0), where ϕ(x,y,z) = z. Every vector x not in the xy-plane determines a light-blue plane through x and u. The image f(x) stays in the light-blue hyperplane since it is ”stretched“ in the u direction by a factor of ϕ(x,y,z).
图25.35：x y平面在u=（0,1,0）方向上的矢量τ，u，式中，（x，y，z）=z。不在xy平面上的每个矢量x通过x和u确定浅蓝色平面。图像f（x）保持在浅蓝色超平面中，因为它在u方向上被“拉伸”了一个因数_（x，y，z）。
Proposition 25.23, which we repeat here for the convenience of the reader, characterizes the linear isomorphisms f =6 id that leave every point in the hyperplane H fixed.
为了方便读者，我们在这里重复这个命题25.23，它描述了线性同构f=6 id，使超平面h中的每个点保持不变。
Proposition 25.23. Let f : E → E be a bijective linear map of a finite-dimensional vector space E and assume that f =6 id and that f(x) = x for all x ∈ H, where H is some hyperplane in E. If det(f) = 1, then f is a transvection of hyperplane H; otherwise, f is a dilatation of hyperplane H. In either case, the vector u is uniquely defined up to a nonzero scalar.
提案25.23。设f:e→e为有限维向量空间e的双射线性映射，假设f=6 id，且f（x）=x表示所有x∈h，其中h是e中的某个超平面。如果det（f）=1，则f是超平面h的一个超矢量化；否则，f是超平面h的一个扩张。在任何情况下，vecTor U是唯一定义为非零标量的。
Proof. Only the last part was not proved in Proposition 7.23, Since f is bijective and the identity on H, the linear map f − id has kernel exactly H. Since H is a hyperplane in E, the image of f −id has dimension 1, and since u belong to this image, it is uniquely defined up to a nonzero scalar.	
证据。只有最后一部分没有在命题7.23中得到证明，因为f是双射的，而h上的恒等式，线性映射f−id的核正好是h。由于h是e中的超平面，f−id的图像有维数1，并且由于u属于这个图像，所以它被唯一地定义为非零标量。
The proof of Proposition 7.23 shows that if dim(E) = n + 1 and if f is a dilatation of hyperplane H, direction D = Ku, and scale α, then 1 is an eigenvalue of f with multiplicity n and α = 06 ,1 is an eigenvalue of f with multiplicity 1; the vector u is an eigenvector for α, and f is diagonalizable. If f is a transvection of hyperplane H and direction u, then 1 is the only eigenvalue of f, and it has multiplicity n; the vector u is an eigenvector for 1, and f is not diagonalizable.
命题7.23的证明表明，如果dim（e）=n+1，如果f是超平面h的扩张，方向d=ku，尺度α，那么1是f的特征值，具有多重性n和α=06，1是f的特征值，具有多重性1；向量u是α的特征向量，f是对角的。竹叶提取物。如果f是超平面h和方向u的矢量，那么1是f的唯一特征值，它具有多重性n；向量u是1的特征向量，f不可对角化。
A homology is the projective version of the type of maps involved in Proposition 25.23.
同调是25.23号命题所涉及的映射类型的投影版本。
Definition 25.11. For any vector space E and any hyperplane H in E, a homography h: P(E) → P(E) is a homology of axis (or base) P(H) if h(P) = P for all P ∈ P(H). In other words, the restriction of h to P(H) is the identity. More explicitly, if h = P(f) for some linear isomorphism f : E → E, we have P(f)(P) = P for all points P = [u] ∈ P(H).
定义25.11.对于任意向量空间e和e中的任何超平面h，如果h（p）=p，则同构h:p（e）→p（e）是轴（或基）p（h）的同构，如果h（p）=p表示所有p∈p（h）。换句话说，H到P（H）的限制就是身份。更明确地说，如果对于某些线性同构f:e→e，h=p（f），我们得到p（f）（p）=p，表示所有点p=[u]∈p（h）。
Using Proposition 25.23 we obtain the following characterization of homologies. Write dim(E) = n + 1.
利用命题25.23，我们得到了以下同系物的特征。写下dim（e）=n+1。
Proposition 25.24. If h: P(E) → P(E) is a homology of axis P(H) and if h =6 id, then for any linear isomorphism f : E → E such that h = P(f), the following properties hold:
提案25.24.如果h:p（e）→p（e）是p（h）轴的同系物，如果h=6 id，那么对于任何线性同构f:e→e，如果h=p（f），以下属性保持不变：
(1)	Either f is a dilatation of hyperplane H and of direction u for some nonzero u ∈ E−H uniquely defined up to a scalar;
f是超平面h的扩张，对于某个非零u∈e−h，它的方向u是唯一定义为一个标量的；
(2)	Or f is a transvection of hyperplane H and direction u for some nonzero u ∈ H uniquely defined up to a scalar.
或f是超平面h和方向u的矢量化，对于某个非零u∈h，其唯一定义为一个标量。
In both cases, O = [u] ∈ P(E) is a fixed point of h, and h has no other fixed points besides O and points in P(H). In Case (1), O /∈ P(H), whereas in Case (2), O ∈ P(H). Furthermore, for any point M ∈ P(E), if M =6 O and if M /∈ P(H), then the line hM,h(M)i passes through O. If dim(E) ≥ 3, the point O is the only point satisfying the above property.
在这两种情况下，O=[U]∈P（E）是H的不动点，H除了O和P（H）中的点外，没有其他不动点。在情况（1）中，o/∈p（h），而在情况（2）中，o∈p（h）。另外，对于任意点m∈p（e），如果m=6o，如果m/∈p（h），则线hm，h（m）i通过o，如果dim（e）≥3，则点o是满足上述性质的唯一点。
Proof. Since the restriction of h = P(f) to P(H) is the identity, and since P(f) = P(idH), by Proposition 25.4 we have f = λidH on H for some nonzero scalar λ ∈ K. Then g = λ−1f is the identity on H, so by Proposition 25.23 we obtain (1) and (2).
证据。由于h=p（f）对p（h）的约束是恒等式，并且p（f）=p（idh），根据命题25.4，对于一些非零标量λ∈k，我们在h上有f=λidh，那么g=λ−1f是h上的恒等式，因此根据命题25.23，我们得到（1）和（2）。
In Case (1), we have g(u) = αu, so P(g)([u]) = P(f)([u]) = [u]. In Case (2), g(u) = u, so again P(g)([u]) = P(f)([u]) = [u]. Therefore, O = [u] is a fixed point of P(f). In Case (1), the eigenvalues of f are 1 with multiplicity n and α with multiplicity 1. If Q = [v] =6 O was a fixed point of h not in P(H), then v would be an eigenvector corresponding to a nonzero eigenvalue λ of f with λ = 16 ,α, and then f would have n + 2 eigenvalues (counted with multiplicty), which is absurd. In Case (2), the only eigenvalue of f is 1, with multiplicity n, so f not diagonalizable, and as above, a vector v such that Q = [v] is a fixed point of h not in P(H) would be an eigenvector corresponding to a nonzero eigenvalue λ = 16 of f, so f would be diagonalizable, a contradiction.
在例（1）中，我们有g（u）=αu，所以p（g）（[u]）=p（f）（[u]）=u。在第（2）种情况下，g（u）=u，因此p（g）（[u]）=p（f）（[u]）=u。因此，o=[u]是p（f）的固定点。在例（1）中，f的特征值为1，具有多重性n，α具有多重性1。如果q=[v]=6o是h的不动点，而不是p（h），那么v是与f的非零特征值λ相对应的特征向量，其中λ=16，α，那么f将具有n+2特征值（用乘法计数），这是荒谬的。在第（2）种情况下，f的唯一特征值是1，具有多重性n，因此f不可对角化，如上所述，q=[v]是h的固定点而不在p（h）中的向量v将是对应于f的非零特征值λ=16的特征向量，因此f将是可对角化的，这是一个矛盾。
Since in Case (1), for any x =6 u and x /∈ H we have x = λu + h for some unique h ∈ H and some unique λ = 06 , so g(x) = g(λu) + g(h) = λαu + h = λu + h + (λα − λ)u = x + λ(α − 1)u,
因为在案例（1）中，对于任何x=6 u和x/∈h，对于一些唯一的h∈h和一些唯一的λ=06，我们有x=λu+h，因此g（x）=g（λu）+g（h）=λαu+h=λu+h+（λα−λ）u=x+λ（α−1）u，
which shows that O,[x] and P(g)([x]) = P(f)([x]) are collinear. In Case (2), for any x =6 u and x /∈ H we have
这表明O、[X]和P（G）（[X]）=P（F）（[X]）是共线的。在案例（2）中，对于任何x=6u和x/∈h，我们有
g(x) = x + ϕ(x)u,
g（x）=x+（x）u，
which also shows that O,[x] and P(g)([x]) = P(f)([x]) are collinear. The last property is left as an exercise (see Vienne [179], Chapter 4, Proposition 7). 
这也表明O、[X]和P（G）（[X]）=P（F）（[X]）是共线的。最后一项财产留作练习（见维也纳[179]，第4章，提案7）。
Proposition 25.24 suggests the following definition.
提案25.24提出了以下定义。
Definition 25.12. Let h: P(E) → P(E) be a homology of axis P(H) with h =6 id, where h = P(f) for some linear isomorphism f : E → E. The fixed point O = [u] associated with the vector u involved in the definition of f, which is unique up to a scalar, is called the center of h. If O ∈ P(H), then h is called a projective transvection (or elation).
定义25.12.设h:p（e）→p（e）是p（h）轴与h=6 id的同系物，其中h=p（f）是某些线性同构f:e→e的同系物。与f定义中涉及的向量u相关的不动点o=[u]被称为h的中心。如果o∈p（h），则h被称为pr。目标转移（或兴高采烈）。
The same geometric construction that we used in the case of the projective plane shows that a homology is determined by its center O, its axis P(H), and a pair of points A and A0 = h(A), with A =6 O and A /∈ P(H). As a kind of converse, we have the following proposition which is easily shown; see Vienne [179] (Chapter IV, Proposition 8).
我们在射影平面的情况下使用的相同几何结构表明，同调是由它的中心o、轴p（h）和一对点a和a0=h（a）确定的，a=6o和a/∈p（h）。作为一种反义词，我们有以下易于展示的命题；见维也纳[179]（第四章，命题8）。
Proposition 25.25. Let P(H) be a hyperplane of P(E) and let O ∈ P(E) be a point. For any pair of distinct points (A,A0) such that O,A,A0 are collinear and A,A0 ∈/ P(H)∪{O}, there is a unique homology h: P(E) → P(E) of centrer O and axis P(H) such that h(A) = A0.
提案25.25。设p（h）为p（e）的超平面，设o∈p（e）为点。对于任何一对不同的点（a，a0），如o，a，a0是共线，a，a0∈/p（h）o，中心的h:p（e）→p（e）和轴p（h）有一个唯一的同源性h（a）=a0。
Remark: From the proof of Proposition 7.23, since every dilatation can be represented by a matrix of the form 	 α	0 ···	0
注：从命题7.23的证明来看，由于每一次扩张都可以用α0····0形式的矩阵表示。
	0	1	0
0 1 0_
	...	...	...,
………………，

γ
	0	0	···	1
0 0···1
we see that by choosing the hyperplane at infinity to be x1 = 0, on the affine hyperplane x1 = 1, a homology becomes a central magnification by α−1. Similarly, since every transvection
我们看到，通过选择无限远的超平面为x1=0，在仿射超平面x1=1上，同源性通过α-1变成中心放大。同样地，因为每一次交通
can be represented by a matrix of the form
可以用形式的矩阵表示		

γ
	1	0
1 0
	α	1
α1
...
…

γ

γ
	0	0
0 0	···
·········
... ···
…·········	0
0℃
0
0℃
...,
……
1
一
we see that by choosing the hyperplane at infinity to be x1 = 0, on the affine hyperplane x1 = 1, an elation becomes a translation.
我们看到，通过选择无限远的超平面为x1=0，在仿射超平面x1=1上，一种兴奋变成了一种翻译。
Theorem 7.26 immediately yields the following result showing that the group of homographies PGL(E) is generated by the homologies.
定理7.26立即得出以下结果，表明同素异形群pgl（e）是由同系物生成的。
Theorem 25.26. Let E be any finite-dimensional vector space over a field K of characteristic not equal to 2. Then, the group of homographies PGL(E) is generated by the homologies.
定理25.26。设e为特征不等于2的场k上的任何有限维向量空间。然后，由同系物生成一组同系物pgl（e）。
When E = R3, we saw earlier that the involutions of RP2 have a nice structure. In particular, if an involution has two fixed points, then it is a harmonic homology.
当e=r3时，我们在前面看到rp2的对合有一个很好的结构。特别是，如果一个对合有两个不动点，那么它就是一个调和同调。
If dim(E) ≥ 4, it is harder to characterize the involutions of P(E), but it is possible. The case where the linear isomorphism f : E → E defining the involutive homography h = P(f) has no eigenvalue in the field K is quite different from the case where f has some eigenvalue in K. In the first case, h has no fixed point. It turns out that this implies that dim(E) is even and there is a simple description of the matrices representing an involution. If h has some fixed point, then f is an involution of E, so it has the eigenvalues +1 and −1, and E is the direct sum of the corresponding eigenspaces E1 and E−1. Then h can be described in terms of P(E1) and P(E−1). For details, we refer the reader to Vienne [179] (Chapter IV, Propositions 11 and 12).
如果dim（e）≥4，则很难描述p（e）的对合，但这是可能的。线性同构f:e→e定义对合同构h=p（f）在k域中没有特征值的情况与f在k域中有一些特征值的情况有很大不同，在第一种情况下，h没有固定点。结果表明，这意味着dim（e）是偶数，并且有一个表示对合的矩阵的简单描述。如果h有一个不动点，那么f是e的对合，因此它有特征值+1和−1，e是相应特征值e1和e−1的直接和。然后h可以用p（e1）和p（e-1）来描述。有关详细信息，我们请读者参考维也纳[179]（第四章，命题11和12）。
25.12	Duality in Projective Geometry
25.12射影几何中的对偶性
We now consider duality in projective geometry. Given a vector space E of finite dimension nE+1∗ is isomorphic to, recall that itsEdual space. We also have a canonical isomorphism betweenE∗ is the vector space of all linear formsEfand its bidual: E → K and thatE∗∗, which allows us to identify E and E∗∗.
我们现在考虑射影几何中的对偶性。给定一个有限维ne+1的向量空间e是同构的，回想一下它的程序空间。我们也有一个典型的同构，在之间是所有线性形式的向量空间，它的双：e→k和e，这使得我们能够识别e和e。
Let H(E) denote the set of hyperplanes in P(E). In Section 25.3 we observed that the map
设h（e）表示p（e）中的超平面集。在第25.3节中，我们观察到地图
p(f) 7→ P(Kerf)
P（F）7→P（切口）
is a bijection between P(E∗) and H(E), in which the equivalence classP(Kerfp)(. Using the abovef) = {λf | λ = 06 } bijection betweenof a nonnull linear formP(E∗)fand∈ EH∗(Eis mapped to the hyperplane), a projective subspace(E), namely the familyP(U) of P(E∗) (where U is a
是p（e）和h（e）之间的双射，其中等价类p（kerfp）（。使用上述f）=λfλ=06非空线性形式p（e）fand∈eh（e is映射到超平面）之间的双射，一个投影子空间（e），即p（e）的族yp（u）（其中u是a
subspace of E∗) can be identified with a subset of H
e）的子空间可以用h的子集来标识。
{P(H) | H = Kerf, f ∈ U − {0}}
_p（h）h=切口，f∈u−0
Uconsisting of the projective hyperplanes in. Such subsets of H(E) are called linear systems (of hyperplanes)H(E) corresponding to nonnull linear forms in.
u射影超平面的存在。这种H（E）的子集称为线性系统（超平面）H（E），对应于中的非零线性形式。
and linear systems as projective subspaces ofThe bijection between P(E∗) and H(E) allows us to viewH(E). In the projective spaceH(E) as a projective space,H(E), a point is a hyperplane in P(E)! The duality between subspaces of E and subspaces of E∗ (reviewed below) and the fact that there is a bijection betweenduality between the set of projective subspaces of P(EP)(Eand the set of linear systems in∗) and H(E) yields a powerful
线性系统作为p（e）和h（e）之间双射的投影子空间，使我们可以看到h（e）。在投影空间h（e）中，作为投影空间h（e），点是p（e）中的超平面！e的子空间与e的子空间之间的对偶性（见下文），以及p（ep）（和中的线性系统集）和h（e）的射影子空间集之间存在一个双射影的事实，产生了一个强大的
H(E) (or equivalently, the set of projective subspaces of P(E∗)).
h（e）（或相当于p（e）的射影子空间集）。
The idea of duality in projective geometry goes back to Gergonne and Poncelet, in the early nineteenth century. However, Poncelet had a more restricted type of duality in mind (polarity with respect to a conic or a quadric), whereas Gergonne had the more general idea of the duality between points and lines (or points and planes). This more general duality arises from a specific pairing between E and E∗ (a nonsingular bilinear form). Here we consider the pairing h−,−i: E∗ × E → K, defined such that
射影几何学中的对偶概念可以追溯到19世纪初的格冈涅和庞塞莱。然而，Poncelet在头脑中有一种更为有限的二元性（关于二次曲线或二次曲线的极性），而Gergonne对点和线（或点和平面）之间的二元性有更一般的概念。这种更普遍的二元性来自e和e（一种非奇异双线性形式）之间的特定配对。这里我们考虑配对h−，−i:e×e→k，定义如下：
hf,vi = f(v),
hf，vi=f（v）

25.12. DUALITY IN PROJECTIVE GEOMETRY
12月25日。射影几何中的对偶性
for all f ∈ E∗ and all v ∈ E. Recall that given a subset V of E (respectively a subset U of
对于所有f e和所有v e，回想一下给定的e的子集v（分别是
E∗), the orthogonal V 0 of V is the subspace of E∗ defined such that
e），v的正交v 0是e的子空间，定义如下：
V 0 = {f ∈ E∗ | hf,vi = 0, for every v ∈ V },
v 0=f∈e hf，vi=0，对于每个v∈v，
and that the orthogonal U0 of U is the subspace of E defined such that
u的正交u0是e的子空间，定义为
U0 = {v ∈ E | hf,vi = 0, for every
u0=v∈e hf，vi=0，每
Then, by Theorem 10.1 (since E and E∗ have the same finite dimension n + 1), U = U00,
然后，根据定理10.1（因为e和e具有相同的有限维n+1），u=u00，
V = V 00, and the maps
V=V 00，地图
	V 7→ V 0	and	U 7→ U0
V 7→V 0和U 7→U0
are inverse bijections, where V is a subspace of E, and U is a subspace of E∗.
是反双射，其中v是e的子空间，u是e的子空间。
These maps set up a duality between subspaces of E and subspaces of E∗. Furthermore, we know that U has dimension k iff U0 has dimension n+1−k, and similarly for V and V 0.
这些地图在e的子空间和e的子空间之间建立了一个对偶性。此外，我们知道u的维数是k，如果u0的维数是n+1−k，同样的，v和v 0的维数也是。
Since a linear system P = P(U) of hyperplanes in H(E) corresponds to a subspace U of E∗, and since
因为H（e）中超平面的线性系统p=p（u）对应于e的子空间u，并且

is the intersection of all the hyperplanes defined by nonnull linear forms in U, we can view a linear system P = P(U) = P(U00) in H(E) as the family of hyperplanes in P(E) containing P(U0).
是由u中的非空线性形式定义的所有超平面的交集，我们可以将h（e）中的线性系统p=p（u）=p（u00）视为p（e）中包含p（u0）的超平面族。
In view of the identification of P(E∗) with the set H(E) of hyperplanes in P(E), by passing to projective spaces, the above bijection between the set of subspaces of E and the set of subspaces of E∗ yields a bijection between the set of projective subspaces of P(E) and the set of linear systems in H(E) (or equivalently, the set of projective subspaces of P(E∗)) called duality. Recall that a point of H(E) is a hyperplane in P(E).
鉴于p（e）中超平面集h（e）对p（e）的识别，通过传递到射影空间，e的子空间集与e的子空间集之间的上述双射产生p（e）的射影子空间集与线性系统集之间的双射。在h（e）中（或等价地，p（e）的射影子空间集称为对偶。回想一下H（e）点是P（e）中的超平面。
More specifically, assuming that E has dimension n + 1, so that P(E) has dimension n, if Q = P(V ) is any projective subspace of P(E) (where V is any subspace of E) and if P = P(U) is any linear system in H(E) (where U is any subspace of E∗), we get a subspace
更具体地说，假设e的维数为n+1，那么p（e）的维数为n，如果q=p（v）是p（e）的任何投影子空间（其中v是e的任何子空间），如果p=p（u）是h（e）中的任何线性系统（其中u是e的任何子空间），我们得到一个子空间。
Q0 of H(E) defined by
h（e）的q0由定义
Q0 = {P(H) | Q ⊆ P(H), P(H) a hyperplane in H(E)},
q0=p（h）q p（h），p（h）h（e）中的超平面，
and a subspace P0 of P(E) defined by
p（e）的子空间p0定义为
P0 = \{P(H) | P(H) ∈ P, P(H) a hyperplane in H(E)}.
p0=p（h）p（h）∈p，p（h）H（e）中的超平面。
We have P = P00 and Q = Q00. Since Q0 is determined by P(V 0), if Q = P(V ) has dimension k (i.e., if V has dimension k + 1), then Q0 has dimension n − k − 1 (since V has dimension k+1 and dim(E) = n+1, then V 0 has dimension n+1−(k+1) = n−k). Thus,
我们有p=p00和q=q00。因为q0由p（v 0）决定，如果q=p（v）的尺寸为k（即v的尺寸为k+1），则q0的尺寸为n−k−1（因为v的尺寸为k+1，dim（e）=n+1，则v 0的尺寸为n+1−（k+1）=n−k）。因此，
dim(Q) + dim(Q0) = n − 1,
尺寸（Q）+尺寸（Q0）=N-1，
and similarly, dim(P) + dim(P0) = n − 1.
同样，dim（p）+dim（p0）=n-1。
A linear system P = P(U) of hyperplanes in H(E) is called a pencil of hyperplanes if it corresponds to a projective line in P(E∗), which means that U is a subspace of dimension 2 of E∗. From dim(P) + dim(P0) = n − 1, a pencil of hyperplanes P is the family of hyperplanes in H(E) containing some projective subspace P(V ) of dimension n − 2 (where P(V ) is a projective subspace of P(E), and P(E) has dimension n). When n = 2, a pencil of hyperplanes in H(E), also called a pencil of lines, is the family of lines passing through a given point. When n = 3, a pencil of hyperplanes in H(E), also called a pencil of planes, is the family of planes passing through a given line.
H（e）中超平面的线性系统p=p（u）如果对应于p（e）中的投影线，则称为超平面的铅笔，这意味着u是e的维2的子空间。从dim（p）+dim（p0）=n−1开始，超平面p的一支铅笔是h（e）中的超平面族，包含维度n−2的一些投影子空间p（v）（其中p（v）是p（e）的投影子空间，p（e）具有维度n）。当n=2时，h（e）中的超平面铅笔，也称为线笔，是穿过给定点的线族。当n=3时，h（e）中的超平面铅笔，也称为平面铅笔，是通过给定直线的平面族。
When n = 2, the above duality takes a rather simple form. In this case (of a projective plane P(E)), the duality is a bijection between points in P(E) and lines in P(E∗), represented by pencils of lines in H(E), with the following properties:
当n=2时，上面的对偶形式相当简单。在这种情况下（投影平面p（e）），对偶是p（e）中点和p（e）中线之间的双射，用h（e）中线的铅笔表示，具有以下特性：
•	A point a in P(E) maps to the line Da in P(E∗) represented by the pencil of lines in H(E) containing a, also denoted by a∗. See Figure 25.36.
p（e）中的点a映射到p（e）中的线da，由h（e）中的线笔表示，其中包含a，也用a表示。见图25.36。
•	A line D in P(E) maps to the point pD in P(E∗) represented by the line D in H(E). See Figure 25.37.
p（e）中的线d映射到p（e）中的点pd，该点由h（e）中的线d表示。见图25.37。
•	Two points a,b in P(E) map to lines Da,Db in P(E∗) represented by pencils of lines through a and b, and the intersection of Da and Db is the point pha,bi in P(E∗) corresponding to the line ha,bi belonging to both pencils. The point pha,bi is the image of the line ha,bi via duality. See Figure 25.38
p（e）中的两个点a、b映射到线da，db映射到线p（e），用铅笔通过a和b表示，da和db的交点是与线ha、bi对应的点pha、bi in p（e），bi属于这两个铅笔。点pha，bi是线ha，bi通过对偶的形象。见图25.38
•	A line D in P(E) containing two points a,b maps to the intersection pD of the lines Da and Db in P(E∗) which are the images of a and b under duality. This is because a,b map to lines Da,Db in P(E∗) represented by pencils of lines through a and b, and the intersection of Da and Db is the point pD in P(E∗) corresponding to the line D = ha,bi belonging to both pencils. The point pD is the image of the line D = ha,bi under duality. Once again, see Figure 25.38.
p（e）中包含两个点a，b的线d映射到p（e）中da和db线的交点pd，这是二元性下a和b的图像。这是因为A，B映射到P（E）中的线d a，d b，用穿过A和B的线的铅笔表示，并且da和db的交点是P（E）中的点p d，对应于D=ha，bi，属于这两支铅笔。点pd是二重性下d=ha，bi线的图像。再次参见图25.38。
•	If a ∈ D, where a is a point and D is a line in P(E), then pD ∈ Da in P(E∗). This is because under duality, a is mapped to the line Da in P(E∗) represented by the pencil of lines containing a, and D is mapped to the point pD ∈ P(E∗) represented by the line D through a in this pencil, so pD ∈ Da.
如果a d，其中a是点，d是p（e）中的线，那么pd da在p（e）中。这是因为在对偶性下，a被映射到p（e）中的线da，用含有a的线的铅笔表示，d被映射到点pd p（e），用该铅笔中的线d通过a表示，所以pd da。
The reader will discover that the dual of Desargues’s theorem is its converse. This is a nice way of getting the converse for free! We will not spoil the reader’s fun and let him discover the dual of Pappus’s theorem.
读者会发现德沙格定理的对偶是它的逆命题。这是一个免费获得谈话的好方法！我们不会破坏读者的乐趣，让他发现帕普斯定理的对偶性。
In general, when n ≥ 2, the above duality is a bijection between points in P(E) and hyperplanes in P(E∗), which are represented by linear systems of dimension n − 1 in H(E), with the following properties:
一般来说，当n≥2时，上述对偶是p（e）中点与p（e）中超平面之间的双射，用h（e）中n−1的线性系统表示，具有以下性质：
25.12. DUALITY IN PROJECTIVE GEOMETRY
12月25日。射影几何中的对偶性

 

Figure 25.36: The duality between a point in P(E) and a line in P(E∗). The line in P(E∗) is also represented by the pencil of lines through a in H(E).
图25.36：p（e）中的点与p（e）中的线之间的对偶性。p（e）中的线也由h（e）中的线笔表示。
•	A point a in P(E) maps to the hyperplane Ha in P(E∗) (the linear system of hyperplanes in H(E) containing a, also denoted by a∗).
p（e）中的点a映射到p（e）中的超平面ha（h（e）中包含a的超平面线性系统，也用a表示）。
•	A hyperplane H in P(E) maps to the point pH in P(E∗) (represented by the hyperplane H in H(E)).
p（e）中的超平面h映射到p（e）中的点ph（由h（e）中的超平面h表示）。
To conclude our quick tour of projective geometry, we establish a connection between the cross-ratio of hyperplanes in a pencil of hyperplanes with the cross-ratio of the intersection points of any line not contained in any hyperplane in this pencil with four hyperplanes in this pencil.
为了结束我们对射影几何的快速浏览，我们建立了超平面铅笔中超平面的交叉比与铅笔中任何超平面中不包含的线的交叉点的交叉比与铅笔中四个超平面的交叉比之间的联系。


Figure 25.37: The duality between a line in P(E) and point in P(E∗). The point in P(E∗) is also represented by Line D in H(E).
图25.37：p（e）中的一条线和p（e）中的点之间的对偶性。p（e）中的点也由h（e）中的d行表示。
25.13	Cross-Ratios of Hyperplanes
25.13超平面的交叉比
Given a pencil P = P(U) of hyperplanes in H(E), for any sequence (H1, H2, H3, H4) of hyperplanes in this pencil, if H1,H2,H3 are distinct, we define the cross-ratio [H1,H2,H3,H4] as the cross-ratio of the hyperplanes Hi considered as points on the projective line P in P(E∗). In particular, in a projective plane P(E), given any four concurrent lines D1, D2, D3, D4, where D1, D2, D3 are distinct, for any two distinct lines ∆ and ∆0 not passing through the common intersection c of the lines Di, letting di = ∆ ∩ Di, and d0i = ∆0 ∩ Di, note that the projection of center c from ∆ to ∆0 maps each di to d0i.
给定H（e）中超平面的铅笔p=p（u），对于铅笔中任何超平面序列（h1、h2、h3、h4），如果h1、h2、h3是不同的，我们将交叉比[h1、h2、h3、h4]定义为被视为P（e）中投影线p上点的超平面的交叉比。特别是，在投影平面p（e）中，给定任意四条平行线d1、d2、d3、d4，其中d1、d2、d3是不同的，对于任何两条不通过直线di的公共交叉点c的不同直线∆和∆0，让di=∆di和d0i=∆0 di，注意投影从∆到∆0的F中心C将每个di映射到d0i。
Since such a projection is a projectivity, and since projectivities between lines preserve cross-ratios, we have
因为这样的投影是投影，而且线之间的投影保持交叉比，所以我们有
,
，
25.13. CROSS-RATIOS OF HYPERPLANES
25.13条。超平面的交叉比

 

Figure 25.38: The duality between a line through two points in P(E) and a point incident to two lines in P(E∗).
图25.38：穿过p（e）中两点的线与入射到p（e）中两点的点之间的对偶性。
which means that the cross-ratio of the di is independent of the line ∆ (see Figure 25.39). In fact, this cross-ratio is equal to [D1,D2,D3,D4], as shown in the next proposition.
这意味着di的交叉比与直线∆无关（见图25.39）。事实上，这个交叉比等于[d1，d2，d3，d4]，如下一个命题所示。
Proposition 25.27. Let P = P(U) be a pencil of hyperplanes in H(E), and let ∆ = P(D) be any projective line such that ∆ ∈/ H for all H ∈ P. The map h: P → ∆ defined such that h(H) = H ∩ ∆ for every hyperplane H ∈ P is a projectivity. Furthermore, for any sequence (H1,H2,H3,H4) of hyperplanes in the pencil P, if H1,H2,H3 are distinct and di = ∆ ∩ Hi, then [d1,d2,d3,d4] = [H1,H2,H3,H4].
提案25.27。设p=p（u）为h（e）中超平面的一支铅笔，设∆=p（d）为任意一条射影线，使∆∈/h表示所有h∈p。图h:p→∆定义为每个超平面h∈p的h（h）=h∆为射影性。此外，对于铅笔p中的任何超平面序列（h1、h2、h3、h4），如果h1、h2、h3是不同的且di=∆hi，则[d1、d2、d3、d4]=[h1、h2、h3、h4]。
Proof. First, the map h: P → ∆ is well–defined, since in a projective space, every line ∆ = P(D) not contained in a hyperplane intersects this hyperplane in exactly one point. Since P = P(U) is a pencil of hyperplanes in H(E), U has dimension 2, and let ϕ and ψ be two nonnull linear forms in E∗ that constitute a basis of U, and let F = ϕ−1(0) and
证据。首先，映射h:p→∆定义得很好，因为在投影空间中，不包含在超平面中的每一条线∆=p（d）都与该超平面在一个点上相交。由于p=p（u）是h（e）中超平面的一支铅笔，u的尺寸为2，并且让_和ψ是e中构成u基础的两个非零线性形式，并且让f=_−1（0）和

Figure 25.39: A pencil of lines and its cross-ratio with intersecting lines.
图25.39：一支铅笔及其与相交线的交叉比。
G = ψ−1(0). Let a = P(F) ∩ ∆ and b = P(G) ∩ ∆. There are some vectors u,v ∈ D such that a = p(u) and b = p(v), and since ϕ and ψ are linearly independent, we have a =6 b, and we can choose ϕ and ψ such that ϕ(v) = −1 and ψ(u) = 1. Also, (u,v) is a basis of D.
G=ψ−1（0）。设a=p（f）∆和b=p（g）∆。有一些向量u，v∈d，这样a=p（u）和b=p（v），并且由于ψ和ψ是线性独立的，所以我们有a=6b，我们可以选择ψ和ψ，从而使（v）=-1和ψ（u）=1。另外，（u，v）是d的基础。
Then a point p(αu+βv) on ∆ belongs to the hyperplane H = p(γϕ+δψ) of the pencil P iff
那么∆上的点p（αu+βv）属于铅笔p iff的超平面h=p（γ_+δψ）。
(γϕ + δψ)(αu + βv) = 0,
（銄+δψ）（αu+βv）=0，
which, since ϕ(u) = 0, ψ(v) = 0, ϕ(v) = −1, and ψ(u) = 1, yields γβ = δα, which is equivalent to [α,β] = [γ,δ] in P(K2). But then the map h: P → ∆ is a projectivity. Letting di = ∆ ∩ Hi, since by Proposition 25.20 a projectivity of lines preserves the cross-ratio, we get [d1,d2,d3,d4] = [H1,H2,H3,H4].	
其中，由于_（u）=0，ψ（v）=0，（v）=-1和ψ（u）=1，产生γβ=δα，相当于p（k2）中的[α，β]=[γ，δ]。但是图h:p→∆是一个投影。假设di=∆hi，因为根据命题25.20，线的投影保持了交叉比，我们得到[d1，d2，d3，d4]=[h1，h2，h3，h4]。
25.14	Complexification of a Real Projective Space
25.14真实投影空间的复杂性
Notions such as orthogonality, angles, and distance between points are not projective concepts. In order to define such notions, one needs an inner product on the underlying vector space. We say that such notions belong to Euclidean geometry. At first glance, the fact that some important Euclidean concepts are not covered by projective geometry seems a major drawback of projective geometry. Fortunately, geometers of the nineteenth century (including Laguerre, Monge, Poncelet, Chasles, von Staudt, Cayley, and Klein) found an astute way of recovering certain Euclidean notions such as angles and orthogonality (also circles) by embedding real projective spaces into complex projective spaces. In the next two sections we will give a brief account of this method. More details can be found in Berger [11, 12], Pedoe [132], Samuel [138], Coxeter [43, 44], Sidler [156], Tisseron [170], Lehmann and Bkouche [112], and, of course, Volume II of Veblen and Young [178].
正交性、角度和点之间的距离等概念不是射影概念。为了定义这些概念，需要在底层向量空间上有一个内积。我们说这些概念属于欧几里得几何。乍一看，射影几何并没有涵盖一些重要的欧几里德概念，这似乎是射影几何的一个主要缺点。幸运的是，十九世纪的几何学家（包括拉盖尔、蒙格、庞塞莱、查理斯、冯·斯泰德、凯莱和克莱恩）发现了一种巧妙的方法，通过将真实的射影空间嵌入复杂的射影空间来恢复某些欧几里德概念，如角度和正交性（也包括圆）。锿。在接下来的两个部分中，我们将简要介绍这种方法。更多细节见Berger[11，12]、Pedoe[132]、Samuel[138]、Coxeter[43，44]、Sidler[156]、Tisseron[170]、Lehmann和Bkouche[112]，当然还有Veblen和Young的第二卷[178]。
25.14. COMPLEXIFICATION OF A REAL PROJECTIVE SPACE
25.14条。实射影空间的复杂性
The first step is to embed a real vector space E into a complex vector space EC. A quick but somewhat bewildering way to do so is to define the complexification of E as the tensor product C ⊗ E. A more tangible way is to define the following structure.
第一步是将实向量空间E嵌入到复向量空间EC中。一种快速但有些令人困惑的方法是将e的复杂性定义为张量积c e。一种更具体的方法是定义以下结构。
Definition 25.13. Given a real vector space E, let EC be the structure E × E under the addition operation
定义25.13.给定一个实向量空间e，让ec为加法运算下的结构e×e。
(u1, u2) + (v1, v2) = (u1 + v1, u2 + v2),
（u1，u2）+（v1，v2）=（u1+v1，u2+v2）
and let multiplication by a complex scalar z = x + iy be defined such that
并定义乘以复数标量z=x+iy
(x + iy) · (u, v) = (xu − yv, yu + xv).
（x+iy）·（u，v）=（xu−yv，yu+xv）。
It is easily shown that the structure EC is a complex vector space. It is also immediate that
结果表明，结构EC是一个复杂的矢量空间。也很快
(0, v) = i(v, 0),
（0，v）=i（v，0），
and thus, identifying E with the subspace of EC consisting of all vectors of the form (u, 0), we can write
因此，用包含形式（u，0）所有向量的EC子空间来识别e，我们可以写
(u, v) = u + iv.
（u，v）=u+iv。
Given a vector w = u + iv, its conjugate w is the vector w = u − iv. Then conjugation is a map from EC to itself that is an involution. If (e1,...,en) is any basis of E, then ((e1,0),...,(en,0)) is a basis of EC. We call such a basis a real basis.
给定一个向量w=u+iv，它的共轭w是向量w=u−iv。那么共轭是从ec到自身的映射，这是一个对合。如果（e1，…，en）是e的任何基础，那么（（e1，0），…，（en，0））是ec的基础。我们称这种基础为真正的基础。
Given a linear map f : E → E, the map f can be extended to a linear map fC: EC → EC defined such that fC(u + iv) = f(u) + if(v).
给定线性映射f:e→e，映射f可扩展为线性映射fc:ec→ec，定义为fc（u+iv）=f（u）+if（v）。
We define the complexification of P(E) as P). If E, is a real affine space, we define the complexified projective completion of E, E as P) and denote it by EeC. Then Ee is naturally embedded in EeC, and it is called the set of real points of EeC.
我们将p（e）的复杂性定义为p）。如果e是一个实仿射空间，我们将e，e的复射影完备定义为p），并用eec表示。然后EE自然地嵌入到EEC中，被称为EEC的实数点集。
If E has dimension n+1 and (e1,...,en+1) is a basis of E, given any homogeneous polynomial P(x1,...,xn+1) over C of total degree m, because P is homogeneous, it is immediately verified that
如果e的维数为n+1，且（e1，…，en+1）是e的基础，给定总度数m的c上的任何齐次多项式p（x1，…，xn+1），因为p是齐次的，立即验证
P(x1,...,xn+1) = 0
P（x1，…，xn+1）=0
iff
敌我识别
P(λx1,...,λxn+1) = 0,
p（λx1，…，λxn+1）=0，
for any λ = 06 . Thus, we can define the hypersurface V (P) of equation P(x1,...,xn+1) = 0 as the subset of EeC consisting of all points of homogeneous coordinates (x1,...,xn+1) such that P(x1,...,xn+1) = 0. We say that the hypersurface V (P) of equation P(x1,...,xn+1) = 0 is real whenever P(x1,...,xn+1) = 0 implies that P(x1,...,xn+1) = 0.
对于任何λ=06。因此，我们可以将方程p（x1，…，xn+1）=0的超曲面v（p）定义为由齐次坐标（x1，…，xn+1）的所有点组成的EEC的子集，这样p（x1，…，xn+1）=0。我们认为当p（x1，…，xn+1）=0表示p（x1，…，xn+1）=0时，方程p（x1，…，xn+1）=0的超曲面v（p）是实的。
 Note that a real hypersurface may have points other than real points, or no real points at all. For example,
注意，真实的超曲面可能有实点以外的点，或者根本没有实点。例如，
x2 + y2 − z2 = 0
x2+y2−z2=0
contains real and complex points such as (1,i,0) and (1,−i,0), and
包含实点和复杂点，如（1、i、0）和（1、−i、0），以及
x2 + y2 + z2 = 0
x2+y2+z2=0
contains only complex points. When m = 2 (where m is the total degree of P), a hypersurface is called a quadric, and when m = 2 and n = 2, a conic. When m = 1, a hypersurface is just a hyperplane.
只包含复杂点。当m=2（其中m是p的总度数）时，超曲面称为二次曲面；当m=2和n=2时，称为二次曲面。当m=1时，超曲面只是一个超平面。
Given any homogeneous polynomial P(x1,...,xn+1) over R of total degree m, since  viewed as a homogeneous polynomial over C defines a hypersurface V (P)C in EC, and also a hypersurface V (P) in P(E). It is clear that V (P) is naturally embedded in V (P)C, and V (P)C is called the complexification of V (P).
给定总次数m的r上的任何齐次多项式p（x1，…，xn+1），因为被视为c上的齐次多项式，所以在ec中定义了超曲面v（p）c，在p（e）中定义了超曲面v（p）。很明显V（P）是自然嵌入V（P）C中的，V（P）C被称为V（P）的复杂性。
We now show how certain real quadrics without real points can be used to define orthogonality and angles.
我们现在展示了如何使用没有实点的实数四次曲面来定义正交性和角度。
25.15	Similarity Structures on a Projective Space
25.15射影空间上的相似结构
We begin with a real Euclidean plane E,. We will show that the angle of two lines D1 and D2 can be expressed as a certain cross-ratio involving the lines D1, D2 and also two lines DI and DJ joining the intersection point D1 ∩D2 of D1 and D2 to two complex points at infinity I and J called the circular points. However, there is a slight problem, which is that we haven’t yet defined the angle of two lines! Recall that we define the (oriented) angle  of two unit vectors u1, u2 as the equivalence class of pairs of unit vectors under the equivalence relation defined such that
我们从一个真正的欧几里得平面E开始。我们将证明，两条直线d1和d2的夹角可以表示为一个特定的交叉比，涉及到直线d1、d2，以及两条直线di和dj，将d1和d2的交点d1 d2连接到无穷大i和j处的两个复点，称为圆点。但是，还有一个小问题，就是我们还没有定义两条线的角度！回想一下，我们把两个单位向量u1，u2的（定向）角定义为在等价关系下单位向量对的等价类，这样
hu1,u2i ≡ hu3,u4i
hu1、u2i hu3、u4i
iff there is some rotation r such that r(u1) = u3 and r(u2) = u4. The set of (oriented) angles of vectors is a group isomorphic to the group SO(2) of plane rotations. If the Euclidean plane is oriented, the measure of the angle of two vectors is defined up to 2kπ (k ∈ Z). The angle of two vectors has a measure that is either θ or 2π − θ, where θ ∈ [0,2π[ , depending on the orientation of the plane. The problem with lines is that they are not oriented: A line is defined by a point a and a vector u, but also by a and −u. Given any two lines D1 and D2, if r is a rotation of angle θ such that r(D1) = D2, note that the rotation −r of angle θ +π also maps D1 onto D2. Thus, in order to define the (oriented) angle D\1D2 of two lines D1, D2, we define an equivalence relation on pairs of lines as follows:
如果有旋转R，R（u1）=u3，R（u2）=u4。向量的（定向）角集是一个与平面旋转的SO（2）群同构的群。如果欧几里得平面是定向的，那么两个向量的角度的测量被定义为最高2 kπ（k∈z）。两个矢量的角度有一个θ或2π−θ的度量，其中θ∈[0,2π[，取决于平面的方向。线的问题在于它们没有定向：线由点A和向量U定义，也由A和−U定义。给定任意两条线d1和d2，如果r是角θ的旋转，因此r（d1）=d2，注意角θ+π的旋转−r也将d1映射到d2。因此，为了定义两条直线d1，d2的（定向）角d\1d2，我们定义了一个直线对上的等价关系，如下所示：
hD1,D2i ≡ hD3,D4i
hd1、d2i hd3、d4i

if there is some rotation r such that r(D1) = D2 and r(D3) = D4.
如果存在旋转R，使得R（d1）=d2和R（d3）=d4。
It can be verified that the set of (oriented) angles of lines is a group isomorphic to the quotient group SO(2)/{id,−id}, also denoted by PSO(2). In order to define the measure of the angle of two lines, the Euclidean plane E must be oriented. The measure of the angle D\1D2 of two lines is defined up to kπ (k ∈ Z). The angle of two lines has a measure that is either θ or π − θ, where θ ∈ [0,π[ , depending on the orientation of the plane. We now go back to the circular points.
可以证明线的一组（定向）角是与商群so（2）/id、−id同构的群，也由pso（2）表示。为了定义两条直线的角度测量，欧几里得平面E必须定向。两条直线的角d \1d2的测量定义为Kπ（K∈Z）。两条直线的角度有一个θ或π−θ的度量，其中θ∈[0，π[，取决于平面的方向。我们现在回到圆点。
Let (a0,a1,a2,a3) be any projective frame for EeC such that (a0,a1) arises from an orthonormal basis (u1,u2) of →−E and the line at infinity H corresponds to z = 0 (where (x,y,z) are the homogeneous coordinates of a point w.r.t. (a0,a1,a2,a3)). Consider the points belonging to the intersection of the real conic Σ of equation
设（a0，a1，a2，a3）为EEC的任何投影帧，使（a0，a1）从→−e的正交基（u1，u2）产生，无穷大h处的线对应于z=0（其中（x，y，z）是点W.R.T.（a0，a1，a2，a3）的齐次坐标）。考虑方程实二次曲线∑的交点
x2 + y2 − z2 = 0
x2+y2−z2=0
with the line at infinity z = 0. For such points, x2 + y2 = 0 and z = 0, and since
直线在无穷大z=0。对于这些点，x2+y2=0，z=0，并且
x2 + y2 = (y − ix)(y + ix),
x2+y2=（y−ix）（y+ix）
we get exactly two points I and J of homogeneous coordinates (1,−i,0) and (1,i,0). The points I and J are called the circular points, or the absolute points, of EeC. They are complex points at infinity. Any line containing either I or J is called an isotropic line.
我们得到两个齐次坐标点i和j（1、−i，0）和（1，i，0）。I点和J点被称为EEC的圆点或绝对点。它们是无穷远的复点。任何含有i或j的线都称为各向同性线。
What is remarkable about I and J is that they allow the definition of the angle of two lines in terms of a certain cross-ratio. Indeed, consider two distinct real lines D1 and D2 in E, and let DI and DJ be the isotropic lines joining D1 ∩D2 to I and J. We will compute the cross-ratio [D1,D2,DI,DJ]. For this, we simply have to compute the cross-ratio of the four points obtained by intersecting D1,D2,DI,DJ with any line not passing through D1 ∩ D2. By changing frame if necessary, so that D1 ∩ D2 = a0, we can assume that the equations of the lines D1,D2,DI,DJ are of the form
关于i和j，值得注意的是，它们允许以一定的交叉比定义两条直线的角度。实际上，考虑e中两条不同的实线d1和d2，让di和dj是连接d1 d2到i和j的各向同性线。我们将计算交叉比[d1，d2，di，dj]。为此，我们只需计算d1、d2、di、dj与任何不通过d1 d2的线相交所得到的四个点的交叉比。如有必要，通过改变帧，使d1 d2=a0，我们可以假定线d1、d2、di、dj的方程为
y
Y	=
=	m1x,
M1X，
y
Y	=
=	m2x,
小精灵，
y y
Y	=
=
=
=	 
leaving the cases m1 = ∞ and m2 = ∞ as a simple exercise. If we choose z = 0 as the intersecting line, we need to compute the cross-ratio of the points (D1)∞ = (1,m1,0),
将案例m1=∞和m2=∞留作简单练习。如果我们选择z=0作为相交线，我们需要计算点的交叉比（d1）∞=（1，m1，0），
(D2)∞ = (1,m2,0), I = (1,−i,0), and J = (1,i,0), and we get
（d2）∞=（1，m2,0），i=（1，−i，0）和j=（1，i，0），我们得到
,
，
that is,
也就是说，
.
.
However, since m1 and m2 are the slopes of the lines D1 and D2, it is well known that if θ is the (oriented) angle between D1 and D2, then
然而，由于m1和m2是直线d1和d2的斜率，众所周知，如果θ是d1和d2之间的（定向）角，那么
.
.
Thus, we have
因此，我们
,
，
that is,
也就是说，
One can check that the formula still holds when m1 = ∞ or m2 = ∞, and also when
我们可以检查当m1=∞或m2=∞时公式是否仍然有效，以及当
D1 = D2. The formula
d1=d2。公式
[D1,D2,DI,DJ] = ei2θ
[d1，d2，di，dj]=ei2θ
is known as Laguerre’s formula.
被称为拉盖尔公式。
If U denotes the group {eiθ | −π ≤ θ ≤ π} of complex numbers of modulus 1, recall that the map Λ: R → U defined such that
如果u表示模1复数的eiθ−π≤θ≤π组，则回想图∧：r→u定义如下：
Λ(t) = eit
∧（t）=eit
is a group homomorphism such that Λ−1(1) = 2kπ, where k ∈ Z. The restriction
是一个群同态，使得∧−1（1）=2kπ，其中k∈z。限制
Λ: ] − π, π[ → (U − {−1})
∧：−π，π[→（U−−1）
of Λ to ] − π, π[ is a bijection, and its inverse will be denoted by
其中∧到]−π，π[是双射，其逆时针表示为
logU : (U − {−1}) → ] − π, π[ .
对数单位：（U−−1）→]−π，π[。
For stating Proposition 25.28 more conveniently, we extend logU to U by letting logU(−1) = π, even though the resulting function is not continuous at −1!. Then we can write
为了更方便地说明命题25.28，我们通过让logu（−1）=π将logu扩展到u，即使结果函数在−1处不是连续的！然后我们可以写
.
.
If the orientation of the plane E is reversed, θ becomes π − θ, and since
如果平面e的方向相反，θ变为π−θ，并且
ei2(π−θ) = e2iπ−i2θ = e−i2θ,
e i2（π−θ）=e2iπ−i2θ=e−i2θ，
logU(ei2(π−θ)) = −logU(ei2θ), and
logu（ei2（π−θ））=−logu（ei2θ），和
.
.
In all cases, we have
在所有情况下，我们
,
，
a formula due to Cayley. We summarize the above in the following proposition.
凯莱的公式。我们将在下面的命题中总结上述内容。
Proposition 25.28. Given any two lines D1,D2 in a real Euclidean plane	E,, letting
提案25.28。给定任意两条线d1，d2在一个真正的欧几里得平面e中，让
DI and DJ be the isotropic lines in joining the intersection point D1 ∩ D2 of D1 and D2 to the circular points I and J, if θ is the angle of the two lines D1, D2, we have
di和dj是将d1和d2的交点d1 d2连接到圆点i和j的各向同性线，如果θ是两条线d1和d2的夹角，我们得到
[D1,D2,DI,DJ] = ei2θ,
[d1，d2，di，dj]=ei2θ，
known as Laguerre’s formula, and independently of the orientation of the plane, we have
被称为拉盖尔公式，独立于平面的方向，我们有
,
，
known as Cayley’s formula.
被称为凯莱公式。
In particular, note that θ = π/2 iff [D1,D2,DI,DJ] = −1, that is, if (D1,D2,DI, DJ) forms a harmonic division. Thus, two lines D1 and D2 are orthogonal iff they form a harmonic division with DI and DJ.
特别注意，θ=π/2 iff[d1，d2，di，dj]=−1，也就是说，如果（d1，d2，di，dj）形成一个谐波除法。因此，两条线d1和d2是正交的iff，它们与di和dj形成一个谐波分区。
The above considerations show that it is not necessary to assume that E, is a real Euclidean plane to define the angle of two lines and orthogonality. Instead, it is enough to assume that two complex conjugate points I,J on the line H at infinity are given. We say that hI,Ji provides a similarity structure on EeC. Note in passing that a circle can be defined as a conic in EeC that contains the circular points I,J. Indeed, the equation of a conic is of the form
上述考虑表明，不必假定e是一个真正的欧几里得平面来定义两条直线的夹角和正交性。相反，假设在无穷远的H线上有两个复共轭点i，j就足够了。我们说，hi，ji在eec上提供了一个相似的结构。请注意，在包含圆点i，j的EEC中，圆可以定义为圆锥曲线。实际上，圆锥曲线方程的形式是
ax2 + by2 + cxy + dxz + eyz + fz2 = 0.
ax2+by2+cxy+dxz+eyz+fz2=0。
If this conic contains the circular points I = (1,−i,0) and J = (1,i,0), we get the two equations
如果这个圆锥曲线包含圆点i=（1，−i，0）和j=（1，i，0），我们得到两个方程
,
，
from which we get 2ic = 0 and a = b, that is, c = 0 and a = b. The resulting equation
从中我们得到2ic=0和a=b，即c=0和a=b。所得方程
ax2 + ay2 + dxz + eyz + fz2 = 0
ax2+ay2+dxz+eyz+fz2=0
is indeed that of a circle.
确实是一个圆。
Instead of using the function logU : (U − {−1}) → ] − π, π[ as logarithm, one may use the complex logarithm function log: C∗ → B, where C∗ = C − {0} and
不用函数log u:（u−−1）→]−π，π[作为对数，可以使用复数对数函数log c:c→b，其中c=c−0和
B = {x + iy | x,y ∈ R, −π < y ≤ π}.
b=x+iy x，y∈r，−π<y≤π。
Indeed, the restriction of the complex exponential function z 7→ ez to B is bijective, and thus, log is well-defined on C∗ (note that log is a homeomorphism from C − {x | x ∈ R, x ≤ 0} onto {x + iy | x,y ∈ R, −π < y < π}, the interior of B). Then Cayley’s formula reads as
实际上，复指数函数z 7→ez对b的约束是双射的，因此，对数在c上定义得很好（注意，对数是从c−x x∈r，x≤0到x+iy x，y∈r，−π<y<π，b的内部的同态）。凯莱的公式是
,
，
with a ± in front when the plane is nonoriented. Observe that this formula allows the definition of the angle of two complex lines (possibly a complex number) and the notion of orthogonality of complex lines. In this case, note that the isotropic lines are orthogonal to themselves!
当平面没有定向时，前面有一个？.注意，这个公式允许定义两条复杂线（可能是复数）的角度和复杂线的正交性概念。在这种情况下，请注意各向同性线与其自身是正交的！
The definition of orthogonality of two lines D1,D2 in terms of (D1,D2, DI,DJ) forming a harmonic division can be used to give elegant proofs of various results. Cayley’s formula can even be used in computer vision to explain modeling and calibrating cameras! (see Faugeras [60]). As an illustration, consider a triangle (a,b,c), and recall that the line a0 passing through a and orthogonal to (b,c) is called the altitude of a, and similarly for b and c. It is well known that the altitudes a0,b0,c0 intersect in a common point called the orthocenter of the triangle (a,b,c). This can be shown in a number of ways using the circular points. Indeed, letting , and  denote the points at infinity of the
用（d1，d2，di，dj）来定义两条直线d1，d2的正交性，形成一个调和除法，可以很好地证明各种结果。凯莱的公式甚至可以用于计算机视觉解释建模和校准相机！（见Faugeras[60]）。作为一个例子，考虑一个三角形（A，B，C），并回想一下，穿过A并与（B，C）正交的线a0被称为A的高度，同样地，对于B和C也是如此。众所周知，高度a0，b0，c0在一个称为三角形正交中心（A，B，C）的公共点相交。这可以通过使用圆点的多种方式来显示。实际上，让并表示
lines hb,ci,ha,bi, ha,ci, a0,b0, and c0, we have
行HB、CI、HA、BI、HA、CI、A0、B0和C0，我们有
,
，
and it is easy to show that there is an involution σ of the line at infinity such that
很容易证明在无穷远处有一条线的对合σ，这样
σ(I)
西格玛（I）	=
=	J,
J
σ(J)
（j）	=
=	I,
我，
σ(bc∞) σ(ab∞) σ(ac∞)
σ（bc∞）σ（ab∞）σ（ac∞）	=
=
=
=
=
=	a0 ,
A0
∞
无穷大
c0 ,
C0
∞
无穷大
b0 .
B0。
∞
无穷大
Then, it can be shown that the lines a0,b0,c0 are concurrent. For more details and other results, notably on the conics, see Sidler [156], Berger [12], and Samuel [138].
然后，可以看出，行a0、b0、c0是并发的。有关更多细节和其他结果，尤其是圆锥曲线，请参见Sidler[156]、Berger[12]和Samuel[138]。
The generalization of what we just did to real Euclidean spaces E, of dimension n is simple. Let (a0,...,an+1) be any projective frame for such that (a0,...,an−1) arises from an orthonormal basis (u1,...,un) of →−E and the hyperplane at infinity H corresponds to xn+1 = 0 (where (x1,...,xn+1) are the homogeneous coordinates of a point with respect to (a0,...,an+1)). Consider the points belonging to the intersection of the real quadric Σ of equation
我们刚才对实欧几里得空间e，即维n所做的推广很简单。设（a0，…，an+1）为任意投影框架，使（a0，…，an-1）由→−e的正交基（u1，…，un）产生，无穷大h处的超平面对应于xn+1=0（其中（x1，…，xn+1）是点相对于（a0，…，an+1）的齐次坐标）。考虑方程实二次∑的交点

with the hyperplane at infinity xn+1 = 0. For such points,
超平面在无穷大xn+1=0。对于这些问题，
	= 0	and	xn+1 = 0.
=0和xn+1=0。
Such points belong to a quadric called the absolute quadric of EeC, and denoted by Ω. Any line containing any point on the absolute quadric is called an isotropic line. Then, given any two coplanar lines D1 and D2 in E, these lines intersect the hyperplane at infinity H in two points (D1)∞ and (D2)∞, and the line ∆ joining (D1)∞ and (D2)∞ intersects the absolute quadric Ω in two conjugate points I∆ and J∆ (also called circular points). It can be shown that the angle θ between D1 and D2 is defined by Laguerre’s formula:
这些点属于称为EEC绝对二次曲线的二次曲线，并用Ω表示。任何在绝对二次曲面上包含任何点的线称为各向同性线。然后，在e中任意两条共面线d1和d2，这些线在无穷大h处的两点（d1）∞和（d2）∞与超平面相交，而线∆连接（d1）∞和（d2）∞与绝对二次方Ω在两个共轭点i∆和j∆（也称为圆点）相交。可以看出，d1和d2之间的角度θ由拉盖尔公式定义：
[(D1)∞,(D2)∞,I∆,J∆] = [D1,D2,DI∆,DJ∆] = ei2θ,
[（d1）∞，（d2）∞，i∆，j∆]=[d1，d2，di∆，dj∆]=ei2θ，
where DI∆ and DJ∆ are the lines joining the intersection D1∩D2 of D1 and D2 to the circular points I∆ and J∆.
式中，di∆和dj∆是将d1和d2的交点d1 d2连接到圆点i∆和j∆的直线。
As in the case of a plane, the above considerations show that it is not necessary to assume that E, is a real Euclidean space to define the angle of two lines and orthogonality. Instead, it is enough to assume that a nondegenerate real quadric Ω in the hyperplane at infinity H and without real points is given. In particular, when n = 3, the absolute quadric Ω is a nondegenerate real conic consisting of complex points at infinity. We say that Ω provides a similarity structure on EeC.
对于平面，上述考虑表明，不必假设e是一个真正的欧几里得空间来定义两条直线的角度和正交性。相反，假设超平面上无穷大H且不带实点的非退化实二次曲面Ω就足够了。特别地，当n=3时，绝对二次方Ω是由无穷远的复点组成的非退化实二次曲线。我们说，Ω在EEC上提供了一个相似的结构。
It is also possible to show that the real projectivities of EeC that leave both the hyperplane H at infinity and the absolute quadric Ω (globally) invariant form a group which is none other than the group of affine similarities; see Lehmann and Bkouche [112] (Chapter 10, page 321), and Berger [11] (Chapter 8, Proposition 8.8.6.4).
也可以证明，将超平面h保持在无穷远处的欧共体的实射影率和绝对二次欧（全局）不变的欧共体形成一个除了仿射相似性组以外的组；见Lehmann和Bkouche[112]（第10章，第321页）和Berger[11]（第8章，提案8.8.6.4）。
Definition 25.14. Let (→−E,→−E,h−,−i) be a Euclidean affine space of finite dimension. An∈ →− affine similarity of (E, E) is an invertible affine map f GA(E) such that if f is the linear map associated with f, then there is some positive real ρ > 0 satisfying the condition
定义25.14.设（→−e、→−e、h−、−i）为有限维欧几里德仿射空间。（e，e）的∈→−仿射相似性是可逆仿射映射f ga（e），如果f是与f相关的线性映射，则存在满足条件的正实ρ>0。
 for all u ∈ →−E. The number ρ is called the ratio of the affine similarity f.
对于所有u∈→−e，数ρ称为仿射相似性f的比值。
If f ∈ GA(E) is an affine similarity of ratio ρ, let →−g = ρ−1→−f . Since ρ > 0, we have
如果f∈ga（e）是比率ρ的仿射相似度，则让→−g=ρ−1→−f。既然ρ>0，我们有

for all u ∈ →−E, and by Proposition 11.12, the map →−g = ρ−1→−f is an isometry; that is, →−g ∈ O(E).
对于所有u∈→−e，根据命题11.12，图→−g=ρ−1→−f是一个等距测量；即→−g∈o（e）。
Consequently, every affine similarity f of E can be written as the composition of an isometry (a member of O(E)), a central dilatation, and a translation. For example, when n = 2, a similarity is a transformation of the form
因此，e的每一个仿射相似性f都可以写成等距线（o（e）的一个成员）、中心扩张和翻译的组成部分。例如，当n=2时，相似度是形式的转换。
,
，
with. We have the following result showing that the affine similarities of the plane can be viewed as special kinds of projectivities of CP2.
用。结果表明，平面的仿射相似性可以看作是CP2的特殊射影性质。
Proposition 25.29. If a projectivity h of CP2 leaves the set of circular points {I,J} fixed and maps the affine space R2 into itself (where R2 is viewed as the subspace of all points (x,y,1) with x,y ∈ R), then h is an affine similarity.
提案25.29。如果cp2的射影度h离开一组圆点i，j固定，并将仿射空间r2映射到自身（其中r2被视为所有点（x，y，1）的子空间，其中x，y∈r），则h是仿射相似性。
Proof. The fact that h leaves the set of circular points {I,J} fixed means that either h(I) = I and h(J) = J or h(I) = J and h(J) = I. If we define I0 and J0 by
证据。H离开圆点集i，j固定的事实意味着h（i）=i和h（j）=j或h（i）=j和h（j）=i。如果我们定义i0和j0
	0)	and	
0）和
where 1, then the fact that h leaves the set of circular points {I,J} fixed is equivalent to
式中1，则h离开圆点集i，j固定的事实等于
	h(I) = I0	and	h(J) = J0.
h（i）=i0和h（j）=j0。
Assume that h is represented by the invertible matrix
假设h由可逆矩阵表示
 .
.
Then h(I) = I0 and h(J) = J0 means that there is some nonzero scalars λ,µ ∈ C such
那么h（i）=i0和h（j）=j0意味着存在一些非零的标量λ，μ∈c这样
		and	 .
而且。
We obtain the following equations:
我们得到以下方程：
		.
.
By adding the two equations on the first row we obtain
通过在第一行添加两个方程，我们得到
λ + µ = 2a,
λ+μ=2a，
by subtracting the first equation from the second on the second row we obtain
通过从第二行的第二个方程中减去第一个方程，我们得到
,
，
so we get
所以我们得到

By subtracting the first equation from the second on the first row we obtain
从第一行的第二个方程中减去第一个方程，我们得到
µ − λ = 2ia0,
礹−λ=2IA0，
and by adding the equations on the second row we obtain
把第二行的方程相加，我们得到

and since	1, we have	= 1, so we get
从1开始，我们有=1，所以我们得到

By adding and subtracting the equations on the third row we obtain
通过对第三行的方程进行加减，我们得到
c = c0 = 0.
c=c0=0。
Sinceassume thatA is invertible,c00 = 1, and we conclude thatc00 = 06	, and since A is determined up to a nonzero scalar we may
假设a是可逆的，c00=1，我们得出结论，that00=06，由于a被确定为非零标量，我们可以
.
.
If h maps R2 into itself, then
如果h将r2映射到自身中，则
must be real for all x,y ∈ R, which implies that a,b,a00,b00 ∈ R.	
必须是所有x，y∈r的实数，这意味着a，b，a00，b00∈r。
The following proposition from Berger [11] (Chapter 8, Proposition 8.8.5.1) gives a convenient characterization of the affine similarities.
Berger[11]提出的以下命题（第8章，命题8.8.5.1）方便地描述了仿射相似性。
Proposition 25.30. Let (E,→−E,h−,−i) be a Euclidean affine space of finite dimension n ≥
提案25.30。设（e，→−e，h−，−i）为有限维n≥的欧几里德仿射空间
2. An affine map  is an affine similarity iff preserves orthogonality; that is, for any two vectors u,v ∈ E, if hu,vi = 0, then h f (u), f (v)i = 0.
2。仿射映射是保持正交性的仿射相似性，即对于任意两个向量u，v∈e，如果hu，v i=0，则h f（u），f（v）i=0。
Proof.hu,vi = 0Assume that, then h→−f (uf),∈→−fGA(v)i(E= 0) is an affine map such that for any two vectors. Fix any nonzero u ∈ →−E and consider the linear formu,v ∈ →−E, ifϕu
证明：hu，v i=0假设，那么h→−f（uf），yger→−fga（v）i（e=0）是一个仿射映射，对于任意两个向量。固定任意非零u∈→−e，并考虑线性形式u，v∈→−e，如果
given by ϕu(v) = h→−f (u),→−f (v)i, v ∈ →−E.
由u（v）=h→−f（u），→−f（v）i，v∈→−e给出。
Since →−f is invertible, ϕu(u) 6= 0. For any v ∈ →−E such that hu,vi = 0, we have
因为→−f是可逆的，所以u（u）6=0。对于任何v∈→−e，如hu，vi=0，我们有
ϕu(v) = h→−f (u),→−f (v)i = 0,
⑨u（v）=h→−f（u），→−f（v）i=0，
thus ϕu is a nonzero linear form vanishing on the hyperplane H orthogonal to u, which is the kernel of the linear form v → h7 u,vi. Therefore, there is some nonzero scalar ρ(u) ∈ R such that ϕu(v) = ρ(u)hu,vi for all v ∈ →−E.
因此，在与u正交的超平面h上，是一个非零线性形式消失，它是线性形式v→h7 u，vi的核心。因此，有一些非零的标量ρ（u）∈r，这样，所有v∈¨u（v）=ρ（u）hu，vi都是。
Evaluating ϕu at u, we see that ρ(u) > 0. If we can show that ρ(u) is a constant ρ > 0 independent of u, we will have shown that
在u处评估u，我们发现ρ（u）>0。如果我们能证明ρ（u）是一个独立于u的常数ρ>0，我们将证明

	h→−f (u),→−f (v)i = ρhu,vi	for all u,v ∈ →−E,
h→−f（u），→−f（v）i=ρhu，vi表示所有u，v∈→−e，
and we will be done.
我们就完了。
independent, and let us evaluateSince dim(E) ≥ 2, pick v to be any nonzero vector inh→−f (u + v),→−f (w)i for any→−E such that. We haveu and v are linearly
独立，并让我们评估，因为dim（e）≥2，选择v为任意非零矢量inh→−f（u+v），对于任意→−e，选择→−f（w）i。我们有u和v是线性的。
h→−f (u + v),→−f (w)i = ϕu+v(w)
H→−F（U+V），→−F（W）I=_U+V（W）
= ρ(u + v)hu + v,wi
=ρ（u+v）hu+v，wi
= ρ(u + v)hu,wi + ρ(u + v)hv,wi
=ρ（u+v）hu，wi+ρ（u+v）hv，wi
and
和
h→−f (u + v),→−f (w)i = h→−f (u) + →−f (v),→−f (w)i
H→−F（U+V），→−F（W）I=H→−F（U）+→−F（V），→−F（W）I
= h→−f (u),→−f (w)i + h→−f (v),→−f (w)i = ρ(u)hu,wi + ρ(v)hv,wi,
=h→−f（u），→−f（w）i+h→−f（v），→−f（w）i=ρ（u）hu，wi+ρ（v）hv，wi，
so we get
所以我们得到
	h(ρ(u + v) − ρ(u))u + (ρ(u + v) − ρ(v))v,wi = 0	for all w ∈ →−E,
h（ρ（u+v）−ρ（u））u+（ρ（u+v）−ρ（v））v，wi=0，对于所有w∈→−e，
which implies that
这意味着
(ρ(u + v) − ρ(u))u + (ρ(u + v) − ρ(v))v = 0.
（ρ（u+v）-ρ（u））u+（ρ（u+v）-ρ（v））v=0.
Since u and v are linearly independent, we must have
既然u和v是线性无关的，我们必须
ρ(u + v) = ρ(u) = ρ(v).
ρ（u+v）=ρ（u）=ρ（v）。
This proves that ρ(u) is a constant ρ independent of u, as claimed.
这证明了ρ（u）是一个与u无关的常数。
	The converse is trivial.	
相反，这是微不足道的。
→−Remark:f ∈ O(E)Letdoes not admit the eigenvalue 1, thenf ∈ GA(E) be an affine similarity of ratiof has a unique fixed point.ρ. If either ρ = 16	or ρ = 1 and
→−备注：f∈o（e）Let不承认特征值1，那么f∈ga（e）是一个仿射相似度的比率有一个唯一的不动点。ρ。如果ρ=16或ρ=1和
any originIndeed, we havea ∈ E, the point→−f = ρ→−ag +for someu is a fixed point ofρ > 0 and some linear isometryf iff	→−g ∈ O(E), so for
任何一个原点，我们都有一个∈e，点→−f=ρ→−a g+对于someu是一个ρ>0的固定点和一些线性等距iff→−g∈o（e），因此
f(a + u) = a + u
F（A+U）=A+U
iff f(a) + →−f (u) = a + u
iff f（a）+→−f（u）=a+u
iff	
敌我识别
iff
敌我识别
(→−g − ρ−1id)(
（→−G−ρ−1id）（

The linear map →−g −ρ−1id is singular iff6 ρ−1 →−is an eigenvalue or →−g , and since→− →−g ∈→−O−(E) its eigenvalues have modulus 1, so if ρ = 1 or if ρ = 1 is not an eigenvalue of g , then g ρ−1id is invertible, and then there is a unique u ∈ E such that
线性映射→−g−ρ−1id是奇异的，如果6ρ−1→−是一个特征值或→−g，并且由于→−→−g∈→−o−（e）其特征值具有模1，因此如果ρ=1或如果ρ=1不是G的特征值，则Gρ−1id是可逆的，然后有一个唯一的u∈e，这样
(→−g − ρ−1id)(
（→−G−ρ−1id）（
For more details on the use of absolute quadrics to obtain some very sophisticated results, the reader should consult Berger [11, 12], Pedoe [132], Samuel [138], Coxeter [43], Sidler [156], Tisseron [170], Lehmann and Bkouche [112], and, of course, Volume II of Veblen and Young [178], which also explains how some non-Euclidean geometries are obtained by chosing the absolute quadric in an appropriate fashion (after Cayley and Klein).
关于使用绝对四次曲面获得一些非常复杂的结果的更多细节，读者应咨询Berger[11，12]、Pedoe[132]、Samuel[138]、Coxeter[43]、Sidler[156]、Tisseron[170]、Lehmann和Bkouche[112]，当然，还应咨询Veblen和Young[178]的第二卷，其中还包括平素一些非欧几里得几何是如何通过以适当的方式选择绝对二次曲面获得的（在凯莱和克莱因之后）。

## 25.16          Some Applications of Projective Geometry  25.16射影几何的一些应用

Projective geometry is definitely a jewel of pure mathematics and one of the major mathematical achievements of the nineteenth century. It turns out to be a prerequisite for algebraic geometry, but to our surprise (and pleasure), it also turns out to have applications in engineering. In this short section we summarize some of these applications.
 射影几何无疑是纯数学的瑰宝，是十九世纪数学的主要成就之一。结果证明这是代数几何的先决条件，但令我们惊讶（和高兴）的是，它也被证明在工程中有应用。在这一小段中，我们将总结其中的一些应用程序。

We first discuss applications of projective geometry to camera calibration, a crucial problem in computer vision. Our brief presentation follows quite closely Trucco and Verri [172] (Chapter 2 and Chapter 6). One should also consult Faugeras [60], or Jain, Katsuri, and Schunck [97].
 我们首先讨论了射影几何在摄像机标定中的应用，摄像机标定是计算机视觉中的一个关键问题。我们的简短介绍与Trucco和Verri[172]非常接近（第2章和第6章）。还应咨询Faugeras[60]或Jain、Katsuri和Schunck[97]。

The pinhole (or perspective) model of a camera is a typical example from computer vision that can be explained very simply in terms of projective transformations. A pinhole camera consists of a point O called the center or focus of projection, and a plane π (not containing O) called the image plane. The distance f from the image plane π to the center O is called the focal length. The line through O and perpendicular to π is called the optical axis, and the point o, intersection of the optical axis with the image plane is called the principal point or image center. The way the camera works is that a point P in 3D space is projected onto the image plane (the film) to a point p via the central projection of center O.
 相机的针孔（或透视）模型是计算机视觉的一个典型例子，可以很简单地用投影变换来解释。针孔相机由一个称为投影中心或焦点的点O和一个称为图像平面的平面π（不包含O）组成。从图像平面π到中心O的距离f称为焦距。穿过O并垂直于π的线称为光轴，光轴与像平面的交点称为主点或像中心。相机的工作方式是通过中心O的中心投影将三维空间中的点P投影到图像平面（胶片）上的点P。

It is assumed that an orthonormal frame Fc is attached to the camera, with its origin at O and its z-axis parallel to the optical axis. Such a frame is called the camera reference frame. With respect to the camera reference frame, it is very easy to write the equations relating the coordinates (x,y) (omitting z = f) of the image p (in the image plane π) of a point P of coordinates (X,Y,Z):
 假设一个正交帧fc连接到相机，其原点在o，Z轴平行于光轴。这种帧称为相机参考帧。对于摄像机参考帧，很容易写出关于坐标点p（x，y，z）的图像p（在图像平面π中）的坐标（x，y）（省略z=f）的方程：

.
 .

Typically, points in 3D space are defined by their coordinates not with respect to the camera reference frame, but with respect to another frame Fw, called the world reference frame.
 通常，三维空间中的点是由它们的坐标定义的，而不是相对于相机参考帧，而是相对于另一帧fw，称为世界参考帧。

However, for most computer vision algorithms, it is necessary to know the coordinates of a point in 3D space with respect to the camera reference frame. Thus, it is necessary to know the position and orientation of the camera with respect to the frame Fw. The position and orientation of the camera are given by some affine transformation (R,T) mapping the frame Fw to the frame Fc, where R is a rotation matrix and T is a translation vector. Furthermore, the coordinates of an image point are typically known in terms of pixel coordinates, and it is also necessary to transform the coordinates of an image point with respect to the camera reference frame to pixel coordinates. In summary, it is necessary to know the transformation that maps a point P in world coordinates (w.r.t. Fw) to pixel coordinates.
 然而，对于大多数计算机视觉算法来说，有必要知道三维空间中一点相对于相机参考帧的坐标。因此，有必要知道相机相对于帧FW的位置和方向。摄像机的位置和方向由一些仿射变换（r，t）给出，将帧fw映射到帧fc，其中r是旋转矩阵，t是平移向量。此外，图像点的坐标通常以像素坐标的形式已知，并且还需要将图像点相对于相机参考帧的坐标转换为像素坐标。总之，有必要知道将世界坐标（W.R.T.FW）中的点P映射到像素坐标的转换。

This transformation of world coordinates to pixel coordinates turns out to be a projective transformation that depends on the extrinsic and the intrinsic parameters of the camera. The extrinsic parameters of a camera are the location and orientation of the camera with respect to the world reference frame Fw. It is given by an affine map (in fact, a rigid motion, see Chapter 12, Section 26.2). The intrinsic parameters of a camera are the parameters needed to link the pixel coordinates of an image point to the corresponding coordinates in the camera reference frame. If Pw = (Xw,Yw,Zw) and Pc = (Xc,Yc,Zc) are the coordinates of the 3D point P with respect to the frames Fw and Fc, respectively, we can write
 世界坐标到像素坐标的转换是一种投影变换，它依赖于相机的外在和内在参数。相机的外部参数是相机相对于世界参考帧fw的位置和方向。它由仿射图给出（事实上，刚性运动，见第12章第26.2节）。相机的内部参数是将图像点的像素坐标链接到相机参考帧中相应坐标所需的参数。如果pw=（xw，yw，zw）和pc=（xc，yc，zc）分别是三维点p相对于帧fw和fc的坐标，我们可以写

Pc = R(Pw − T).
 pc=r（pw−t）。

| is   given by    由给出 |        |                                     |
| ----------------------- | ------ | ----------------------------------- |
| x    X                  | =    = | −(xim − ox)sx,    −（XIM−OX）SX，   |
| y    Y                  | =    = | −(yim − oy)sy,    −（Yim−Oy）系统， |

Neglecting distorsions possibly introduced by the optics, the correspondence between the coordinates (x,y) of the image point with respect to Fc and the pixel coordinates (xim,yim)
 忽略光学可能引入的畸变，图像点相对于fc的坐标（x，y）与像素坐标（xim，yim）之间的对应关系。

where (ox,oy) are the pixel coordinates the principal point o and sx,sy are scaling parameters.
 其中（ox，oy）是像素坐标，主点o和sx，sy是缩放参数。

After some simple calculations, the upshot of all this is that the transformation between the homogeneous coordinates (Xw,Yw,Zw,1) of a 3D point and its homogeneous pixel coordinates (x1,x2,x3) is given by
 经过一些简单的计算，得出的结论是，三维点的齐次坐标（xw，yw，zw，1）与其齐次像素坐标（x1，x2，x3）之间的转换由下式得出：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

where the matrix M, known as the projection matrix, is a 3 × 4 matrix depending on R, T, ox,oy, f (the focal length), and sx,sy (for the derivation of this equation, see Trucco and Verri [172], Chapter 2).
 其中，矩阵m（称为投影矩阵）是一个3×4的矩阵，取决于r、t、ox、oy、f（焦距）和sx、sy（关于该方程的推导，见Trucco和Verri[172]，第2章）。

The problem of estimating the extrinsic and the instrinsic parameters of a camera is known as the camera calibration problem. It is an important problem in computer vision.
 摄像机的外参数和内参数估计问题称为摄像机标定问题。这是计算机视觉中的一个重要问题。

Now, using the equations
 现在，使用这些方程

| x    X | =    = | −(xim − ox)sx,    −（XIM−OX）SX，   |
| ------ | ------ | ----------------------------------- |
| y    Y | =    = | −(yim − oy)sy,    −（Yim−Oy）系统， |

we get
 我们得到

,
 ，

relating the coordinates w.r.t. the camera reference frame to the pixel coordinates. This suggests using the parameters fx = f/sx and fy = f/sy instead of the parameters f,sx,sy. In fact, all we need are the parameters fx = f/sx and α = sy/sx, called the aspect ratio. Without loss of generality, it can also be assumed that (ox,oy) are known. Then we have a total of eight parameters.
 将相机参考帧的坐标W.R.T.与像素坐标相关联。这建议使用参数fx=f/sx和fy=f/sy，而不是参数f、sx、sy。实际上，我们需要的只是参数fx=f/sx和α=sy/sx，称为展弦比。在不丧失一般性的情况下，也可以假定（Ox，Oy）是已知的。然后我们一共有八个参数。

One way of solving the calibration problem is to try estimating fx,α, the rotation matrix R, and the translation vector T from N image points (xi,yi), projections of N suitably chosen world points (Xi,Yi,Zi), using the system of equations obtained from the projection matrix. It turns out that if N ≥ 7 and the points are not coplanar, the rank of the system is 7, and the system has a nontrivial solution (up to a scalar) that can be found using SVD methods (see Chapter 20, Trucco and Verri [172], or Jain, Katsuri, and Schunck [97]).
 解决校准问题的一种方法是尝试从N个图像点（XI，YI）估计FX、α、旋转矩阵R和平移向量T，使用从投影矩阵获得的方程系统，N个适当选择的世界点（XI，Yi，ZI）的投影。结果表明，如果n≥7且点不是共面的，则系统的秩为7，并且系统有一个非平凡解（达到一个标量），可以使用SVD方法找到该解（见第20章，Trucco和Verri[172]或Jain、Katsuri和Schunck[97]）。

Another method consists in estimating the whole projection matrix M, which depends on 11 parameters, and then extracting extrinsic and intrinsic parameters. Again, SVD methods are used (see Trucco and Verri [172], and Faugeras [60]).
 另一种方法是估计整个投影矩阵M，它依赖于11个参数，然后提取外部和内部参数。同样，使用SVD方法（见Trucco和Verri[172]和Faugeras[60]）。

Cayley’s formula can also be used to solve the calibration cameras, as explained in Faugeras [60]. Other problems in computer vision can be reduced to problems in projective geometry (see Faugeras [60]).
 如Faugeras[60]所述，Cayley的公式也可用于解决校准摄像头问题。计算机视觉中的其他问题可以简化为射影几何中的问题（见Faugeras[60]）。

In computer graphics, it is also necessary to convert the 3D world coordinates of a point to a two-dimensional representation on a view plane. This is achieved by a so-called viewing system using a projective transformation. For details on viewing systems see Watt [183] or Foley, van Dam, Feiner, and Hughes [64].
 在计算机图形学中，还需要将点的三维世界坐标转换为视图平面上的二维表示。这是通过使用投影变换的所谓观察系统实现的。有关查看系统的详细信息，请参见瓦特[183]或福利、范达姆、费纳和休斯[64]。

Projective spaces are also the right framework to deal with rational curves and rational surfaces. Indeed, in the projective framework it is easy to deal with vanishing denominators and with “infinite” values of the parameter(s).
 射影空间也是处理有理曲线和有理曲面的合适框架。实际上，在射影框架中，很容易处理消失分母和参数的“无限”值。

It is much less obvious that projective geometry has applications to efficient communication, error-correcting codes, and cryptography, as very nicely explained by Beutelspacher and Rosenbaum [22]. We sketch these applications very briefly, referring our readers to [22] for details. We begin with efficient communication. Suppose that eight students would like to exchange information to do their homework economically. The idea is that each student solves part of the exercises and copies the rest from the others (which we do not recommend, of course!). It is assumed that each student solves his part of the homework at home, and that the solutions are communicated by phone. The problem is to minimize the number of phone calls. An obvious but expensive method is for each student to call each of the other seven students. A much better method is to imagine that the eight students are the vertices of a cube, say with coordinates from {0,1}3. There are three types of edges:
 正如Beutelspacher和Rosenbaum[22]很好地解释的那样，射影几何在有效通信、纠错码和密码学方面的应用就不那么明显了。我们非常简单地概述了这些应用程序，详细信息请参阅[22]。我们从有效的沟通开始。假设有八个学生愿意交换信息以经济地完成家庭作业。这个想法是每个学生解决部分练习，并从其他人那里复制其余的（当然，我们不推荐！）.假设每个学生在家里完成自己的家庭作业，并通过电话沟通解决方案。问题是尽量减少通话次数。一个明显但昂贵的方法是让每个学生给另外七个学生打电话。一个更好的方法是假设八个学生是一个立方体的顶点，比如坐标为0,1 3。边缘有三种类型：

\1. Those parallel to the z-axis, called type 1; 2. Those parallel to the y-axis, called type 2;
 1。那些平行于z轴的，称为1型；2型。平行于y轴的，称为2型；

\3. Those parallel to the x-axis, called type 3.
 三。那些平行于x轴的，称为3型。

The communication can proceed in three rounds as follows: All nodes connected by type 1 edges exchange solutions; all nodes connected by type 2 edges exchange solutions; and finally all nodes connected by type 3 edges exchange solutions.
 通信可以分三轮进行：所有节点通过类型1边缘交换解决方案连接；所有节点通过类型2边缘交换解决方案连接；最后所有节点通过类型3边缘交换解决方案连接。

It is easy to see that everybody has all the answers at the end of the three rounds. Furthermore, each student is involved only in three calls (making a call or receiving it), and the total number of calls is twelve.
 很容易看出，在三轮比赛结束时，每个人都有所有的答案。此外，每个学生只参与三个电话（打一个电话或接一个电话），总的电话数是12个。

In the general case, N nodes would like to exchange information in such a way that eventually every node has all the information. A good way to to this is to construct certain finite projective spaces, as explained in Beutelspacher and Rosenbaum [22]. We pick q to be an integer (for instance, a prime number) such that there is a finite projective space of any dimension over the finite field of order q. Then, we pick d such that
 在一般情况下，n个节点希望以这样的方式交换信息，最终每个节点都拥有所有的信息。一个很好的方法是构造某些有限射影空间，如Beutelspacher和Rosenbaum[22]所述。我们把q选为一个整数（例如质数），这样在q阶的有限域上任何维都有一个有限的射影空间，然后，我们把d选为

qd−1 < N ≤ qd.
 qd−1<n≤qd。

Since q is prime, there is a projective space P(Kd+1) of dimension d over the finite field K of order q, and letting H be the hyperplane at infinity in P(Kd+1), we pick a frame P1,...,Pd in H. It turns out that the affine space A = P(Kd+1) − H has qd points. Then the communication nodes can be identified with points in the affine space A. Assuming for simplicity that N = qd, the algorithm proceeds in d rounds. During round i, each node Q ∈ A sends the information it has received to all nodes in A on the line QPi.
 由于q是素数，在q阶的有限域k上有一个维数d的投影空间p（kd+1），在p（kd+1）中设h为无穷远的超平面，我们选取一帧p1，…，pd in h，结果表明仿射空间a=p（kd+1）−h有qd点。然后利用仿射空间A中的点来识别通信节点，为了简单起见，假设n=qd，算法进行D轮运算。在第一轮中，每个节点q∈a将其接收到的信息发送到在线qpi中的所有节点。

It can be shown that at the end of the d rounds, each node has the total information, and that the total number of transactions is at most
 可以看出，在D轮结束时，每个节点都有总的信息，并且事务的总数最多是

(q − 1)logq(N)N.
 （q−1）logq（n）n.

Other applications of projective spaces to communication systems with switches are described in Chapter 2, Section 8, of Beutelspacher and Rosenbaum [22]. Applications to error-correcting codes are described in Chapter 5 of the same book. Introducing even the most elementary notions of coding theory would take too much space. Let us simply say that the existence of certain types of good codes called linear [n,n−r]-codes with minimum distance d is equivalent to the existence of certain sets of points called (n,d − 1)-sets in the finite projective space P({0,1}r). For the sake of completeness, a set of n points in a projective space is an (n,s)-set if s is the largest integer such that every subset of s points is projectively independent. For example, an (n,3)-set is a set of n points no three of which are collinear, but at least four of them are coplanar.
 射影空间在具有开关的通信系统中的其他应用，如Beutelspacher和Rosenbaum[22]第2章第8节所述。纠错码的应用在同一本书的第5章中进行了描述。即使引入编码理论的最基本概念也会占用太多的空间。让我们简单地说，具有最小距离d的某些类型的称为线性[n，n-r]的好代码的存在等价于有限射影空间p（0,1 r）中称为（n，d-1）-集的某些点集的存在。为了完备性，如果s是最大整数，则射影空间中n个点的集合是（n，s）-集，这样s点的每个子集都是射影独立的。例如，（n，3）-集是一组n点，其中没有三个是共线的，但至少有四个是共面的。

Other applications of projective geometry to cryptography are given in Chapter 6 of Beutelspacher and Rosenbaum [22].
 射影几何在密码学中的其他应用在Beutelspacher和Rosenbaum[22]的第6章中给出。


 

856                                                                 CHAPTER 25. BASICS OF PROJECTIVE GEOMETRY
 
 856第25章。射影几何基础

Part III
 第三部分

The Geometry of Bilinear Forms
 双线性形式的几何