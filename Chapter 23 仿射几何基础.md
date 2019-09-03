第二十三章
Basics of Affine Geometry
仿射几何基础
L’alg`ebre n’est qu’une g´eom´etrie ´ecrite; la g´eom´etrie n’est qu’une alg`ebre figur´ee.
l'alg'ebre n'est qu'une g'eom'etrie'ecrite；la g'eom'etrie n'est qu'une alg'ebre figur ee'ee。
—Sophie Germain
-索菲日尔曼
23.1	Affine Spaces
23.1仿射空间
Geometrically, curves and surfaces are usually considered to be sets of points with some special properties, living in a space consisting of “points.” Typically, one is also interested in geometric properties invariant under certain transformations, for example, translations, rotations, projections, etc. One could model the space of points as a vector space, but this is not very satisfactory for a number of reasons. One reason is that the point corresponding to the zero vector (0), called the origin, plays a special role, when there is really no reason to have a privileged origin. Another reason is that certain notions, such as parallelism, are handled in an awkward manner. But the deeper reason is that vector spaces and affine spaces really have different geometries. The geometric properties of a vector space are invariant under the group of bijective linear maps, whereas the geometric properties of an affine space are invariant under the group of bijective affine maps, and these two groups are not isomorphic. Roughly speaking, there are more affine maps than linear maps.
在几何上，曲线和曲面通常被认为是一组具有某些特殊性质的点，它们生活在一个由“点”组成的空间中。通常，人们也对在某些变换下不变的几何性质感兴趣，例如，平移、旋转、投影离子等。人们可以将点的空间建模为矢量空间，但由于许多原因，这并不十分令人满意。一个原因是与零向量（0）相对应的点（称为原点）在没有理由拥有特权原点的情况下起着特殊的作用。另一个原因是某些概念，如并行性，处理起来很尴尬。但深层次的原因是向量空间和仿射空间的几何性质是不同的。向量空间的几何性质在双射线性映射群下是不变的，而仿射空间的几何性质在双射仿射映射群下是不变的，这两个群不是同构的。大致来说，仿射映射比线性映射多。
Affine spaces provide a better framework for doing geometry. In particular, it is possible to deal with points, curves, surfaces, etc., in an intrinsic manner, that is, independently of any specific choice of a coordinate system. As in physics, this is highly desirable to really understand what is going on. Of course, coordinate systems have to be chosen to finally carry out computations, but one should learn to resist the temptation to resort to coordinate systems until it is really necessary.
仿射空间为几何提供了一个更好的框架。特别是，可以以一种内在的方式处理点、曲线、曲面等，即独立于坐标系的任何特定选择。在物理学中，真正理解正在发生的事情是非常需要的。当然，为了最终进行计算，必须选择坐标系，但在真正必要之前，人们应该学会抵制使用坐标系的诱惑。
Affine spaces are the right framework for dealing with motions, trajectories, and physical forces, among other things. Thus, affine geometry is crucial to a clean presentation of kinematics, dynamics, and other parts of physics (for example, elasticity). After all, a rigid motion is an affine map, but not a linear map in general. Also, given an m × n matrix A
仿射空间是处理运动、轨迹和物理力等问题的正确框架。因此，仿射几何对于运动学、动力学和其他物理部分（例如弹性）的清晰呈现至关重要。毕竟，刚性运动是仿射映射，而不是一般的线性映射。另外，给定m×n矩阵a
695
六百九十五
and a vector b ∈ Rm, the set U = {x ∈ Rn | Ax = b} of solutions of the system Ax = b is an affine space, but not a vector space (linear space) in general.
而向量b∈rm，系统解a x=b的集u=x∈rn ax=b是仿射空间，但一般不是向量空间（线性空间）。
Use coordinate systems only when needed!
仅在需要时使用坐标系！
This chapter proceeds as follows. We take advantage of the fact that almost every affine concept is the counterpart of some concept in linear algebra. We begin by defining affine spaces, stressing the physical interpretation of the definition in terms of points (particles) and vectors (forces). Corresponding to linear combinations of vectors, we define affine combinations of points (barycenters), realizing that we are forced to restrict our attention to families of scalars adding up to 1. Corresponding to linear subspaces, we introduce affine subspaces as subsets closed under affine combinations. Then, we characterize affine subspaces in terms of certain vector spaces called their directions. This allows us to define a clean notion of parallelism. Next, corresponding to linear independence and bases, we define affine independence and affine frames. We also define convexity. Corresponding to linear maps, we define affine maps as maps preserving affine combinations. We show that every affine map is completely defined by the image of one point and a linear map. Then, we investigate briefly some simple affine maps, the translations and the central dilatations. At this point, we give a glimpse of affine geometry. We prove the theorems of Thales, Pappus, and Desargues. After this, the definition of affine hyperplanes in terms of affine forms is reviewed. The section ends with a closer look at the intersection of affine subspaces.
本章内容如下。我们利用了这样一个事实：几乎每一个仿射概念都是线性代数中某些概念的对应物。我们首先定义仿射空间，强调用点（粒子）和向量（力）来解释定义。对应于向量的线性组合，我们定义了点的仿射组合（重心），意识到我们被迫将注意力限制在最多1个标量的族上。针对线性子空间，引入仿射子空间作为仿射组合下的闭子集。然后，我们用称为方向的向量空间来描述仿射子空间。这允许我们定义一个清晰的并行性概念。其次，对应于线性独立和基，定义了仿射独立和仿射框架。我们也定义了凸性。对应于线性映射，我们将仿射映射定义为保留仿射组合的映射。我们证明了每一个仿射映射都完全由一个点的图像和一个线性映射定义。然后，我们简单地研究了一些简单的仿射映射、翻译和中心扩张。在这一点上，我们给出了仿射几何的一瞥。我们证明了泰雷兹、帕普斯和德沙格的定理。在此基础上，回顾了仿射超平面在仿射形式上的定义。该部分以更仔细的观察仿射子空间的交叉点结束。
Our presentation of affine geometry is far from being comprehensive, and it is biased toward the algorithmic geometry of curves and surfaces. For more details, the reader is referred to Pedoe [132], Snapper and Troyer [157], Berger [11, 12], Coxeter [44], Samuel [138], Tisseron [170], Fresnel [66], Vienne [179], and Hilbert and Cohn-Vossen [90].
我们对仿射几何的描述还远远不够全面，它偏向于曲线和曲面的算法几何。关于更多细节，读者可以参考Pedoe[132]、Snapper和Troyer[157]、Berger[11，12]、Coxeter[44]、Samuel[138]、Tisseron[170]、Fresnel[66]、Vienne[179]和Hilbert和Cohn Vossen[90]。
Suppose we have a particle moving in 3D space and that we want to describe the trajectory of this particle. If one looks up a good textbook on dynamics, such as Greenwood [82], one finds out that the particle is modeled as a point, and that the position of this point x is determined with respect to a “frame” in R3 by a vector. Curiously, the notion of a frame is rarely defined precisely, but it is easy to infer that a frame is a pair (O,(e1,e2,e3)) consisting of an origin O (which is a point) together with a basis of three vectors (e1,e2,e3). For example, the standard frame in R3 has origin O = (0,0,0) and the basis of three vectors e1 = (1,0,0), e2 = (0,1,0), and e3 = (0,0,1). The position of a point x is then defined by the “unique vector” from O to x.
假设有一个粒子在三维空间中运动，我们想描述这个粒子的轨迹。如果你查阅了一本很好的动力学教科书，比如Greenwood[82]，你会发现粒子被建模为一个点，这个点x的位置是由一个向量相对于r3中的“帧”来确定的。奇怪的是，帧的概念很少被精确定义，但很容易推断出帧是一对（o，（e1，e2，e3）），由原点o（即点）和三个矢量（e1，e2，e3）的基组成。例如，r3中的标准帧具有原点o=（0,0,0）和三个向量e1=（1,0,0）、e2=（0,1,0）和e3=（0,0,1）。点X的位置由从O到X的“唯一向量”定义。
But wait a minute, this definition seems to be defining frames and the position of a point without defining what a point is! Well, let us identify points with elements of R3. If so, given any two points a = (a1,a2,a3) and b = (b1,b2,b3), there is a unique free vector, denoted by →−ab, from a to b, the vector →−ab = (b1 − a1,b2 − a2,b3 − a3). Note that
但是等一下，这个定义似乎定义了框架和点的位置，而没有定义点是什么！好吧，让我们用r3的元素来确定点。如果是这样，在任意两点a=（a1、a2、a3）和b=（b1、b2、b3）下，有一个唯一的自由矢量，用→−ab表示，从a到b，矢量→−ab=（b1−a1、b2−a2、b3−a3）。注意
b = a + →−ab,
B=A+→AB，

Figure 23.1: Points and free vectors.
图23.1：点和自由矢量。
addition being understood as addition in R3. Then, in the standard frame, given a point x = (x1,x2,x3), the position of x is the vector Ox−→ = (x1,x2,x3), which coincides with the point itself. In the standard frame, points and vectors are identified. Points and free vectors are illustrated in Figure 23.1.
加成被理解为r3中的加成。然后，在标准帧中，给定一个点x=（x1，x2，x3），x的位置是向量ox−→=（x1，x2，x3），它与点本身重合。在标准框架中，识别点和向量。点和自由矢量如图23.1所示。
What if we pick a frame with a different origin, say Ω = (ω1,ω2,ω3), but the same basis vectors (e1,e2,e3)? This time, the point x = (x1,x2,x3) is defined by two position vectors:
如果我们选取一个原点不同的帧，比如Ω=（ω1，ω2，ω3），但基向量相同（e1，e2，e3），会怎么样？这一次，点x=（x1，x2，x3）由两个位置矢量定义：
Ox−→ = (x1,x2,x3)
Ox−→=（x1，x2，x3）
in the frame (O,(e1,e2,e3)) and
在帧（o，（e1，e2，e3））和
Ω−→x = (x1 − ω1,x2 − ω2,x3 − ω3)
Ω−→x=（x1−ω1，x2−ω2，x3−ω3）
in the frame (Ω,(e1,e2,e3)). See Figure 23.2.
在框架中（Ω，（e1，e2，e3））。见图23.2。
This is because  and O−→Ω = (ω1,ω2,ω3).
这是因为和O−→Ω=（ω1，ω2，ω3）。
We note that in the second frame (Ω,(e1,e2,e3)), points and position vectors are no longer identified. This gives us evidence that points are not vectors. It may be computationally convenient to deal with points using position vectors, but such a treatment is not frame invariant, which has undesirable effects.
我们注意到，在第二帧（Ω，（e1，e2，e3））中，不再识别点和位置矢量。这给了我们证据，证明点不是向量。使用位置向量处理点可能在计算上很方便，但这种处理不是帧不变的，这会产生不良的效果。
Inspired by physics, we deem it important to define points and properties of points that are frame invariant. An undesirable side effect of the present approach shows up if we attempt to define linear combinations of points. First, let us review the notion of linear combination of vectors. Given two vectors u and v of coordinates (u1,u2,u3) and (v1,v2,v3) with respect
受物理学的启发，我们认为定义帧不变的点和点的性质很重要。如果我们试图定义点的线性组合，则会出现当前方法的不良副作用。首先，让我们回顾向量线性组合的概念。给定坐标（U1、U2、U3）和（V1、V2、V3）的两个向量u和v

Figure 23.2: The two position vectors for the point x.
图23.2:X点的两个位置矢量。
to the basis (e1,e2,e3), for any two scalars λ,µ, we can define the linear combination λu+µv as the vector of coordinates
对于基（e1，e2，e3），对于任意两个标量λ，μ，我们可以定义线性组合λu+μv作为坐标矢量。
(λu1 + µv1,λu2 + µv2,λu3 + µv3).
（λu1+μv1，λu2+μv2，λu3+μv3）。
If we choose a different basis () and if the matrix P expressing the vectors ( over the basis (e1,e2,e3) is
如果我们选择一个不同的基（），并且表示向量的矩阵p（相对于基（e1，e2，e3）是
 ,
，
which means that the columns of P are the coordinates of the e0j over the basis (e1,e2,e3), since
这意味着p列是e0j在基上的坐标（e1，e2，e3），因为

and
和
,
，
it is easy to see that the coordinates (u1,u2,u3) and (v1,v2,v3) of u and v with respect to the basis (e1,e2,e3) are given in terms of the coordinates () and (and v with respect to the basis () by the matrix equations
很容易看出，u和v相对于基（e1，e2，e3）的坐标（u1，u2，u3）和（v1，v2，v3）由矩阵方程给出，相对于基（e1，e2，e3）的坐标（）和（和v相对于基（）。
		and	 .
而且。
From the above, we get
从上面我们可以看到
		and	 ,
而且，
and by linearity, the coordinates
通过线性，坐标

of λu + µv with respect to the basis () are given by
关于基础（）的λu+μv的公式如下：
 .
.
Everything worked out because the change of basis does not involve a change of origin. On the other hand, if we consider the change of frame from the frame (O,(e1,e2,e3)) to the frame (Ω,(e1,e2,e3)), where O−→Ω = (ω1,ω2,ω3), given two points a, b of coordinates (a1,a2,a3) and (b1,b2,b3) with respect to the frame (O,(e1,e2,e3)) and of coordinates (
一切都是因为基础的改变并不涉及到原产地的改变。另一方面，如果我们考虑从帧（o，（e1，e2，e3））到帧（Ω，（e1，e2，e3））的变化，其中o−→（
) with respect to the frame (Ω,(e1,e2,e3)), since
）关于框架（Ω，（e1，e2，e3）），因为
(a01,a02,a03) = (a1 − ω1,a2 − ω2,a3 − ω3)
（a01，a02，a03）=（a1−ω1，a2−ω2，a3−ω3）
and
和
(b01,b02,b03) = (b1 − ω1,b2 − ω2,b3 − ω3),
（b01、b02、b03）=（b1−ω1、b2−ω2、b3−ω3）
the coordinates of λa + µb with respect to the frame (O,(e1,e2,e3)) are
λa+μb相对于框架（o，（e1，e2，e3））的坐标为
(λa1 + µb1,λa2 + µb2,λa3 + µb3),
（λa1+μb1，λa2+μb2，λa3+μb3）、
but the coordinates of λa + µb with respect to the frame (Ω,(e1,e2,e3)) are
但是，λa+μb相对于框架的坐标（Ω，（e1，e2，e3））是
(λa1 + µb1 − (λ + µ)ω1,λa2 + µb2 − (λ + µ)ω2,λa3 + µb3 − (λ + µ)ω3),
（λa1+μb1−（λ+μ）ω1，λa2+μb2−（λ+μ）ω2，λa3+μb3−（λ+μ）ω3）
which are different from
有什么不同
(λa1 + µb1 − ω1,λa2 + µb2 − ω2,λa3 + µb3 − ω3),
（λa1+μb1-ω1，λa2+μb2-ω2，λa3+μb3-ω3）
unless λ + µ = 1. See Figure 23.3.
除非λ+μ=1。见图23.3。
Thus, we have discovered a major difference between vectors and points: The notion of linear combination of vectors is basis independent, but the notion of linear combination of points is frame dependent. In order to salvage the notion of linear combination of points, some restriction is needed: The scalar coefficients must add up to 1.
因此，我们发现了向量和点之间的一个主要区别：向量的线性组合的概念与基无关，但点的线性组合的概念与帧相关。为了恢复点的线性组合的概念，需要一些限制：标量系数必须加起来为1。


Figure 23.3: The top figure shows the location of the “point” sum a + b with respect to the frame (O,(e1,e2,e3)), while the bottom figure shows the location of the “point” sum a + b with respect to the frame (Ω,(e1,e2,e3)).
图23.3：上图显示了“点”和A+B相对于帧（o，（e1，e2，e3））的位置，而下图显示了“点”和A+B相对于帧（Ω，（e1，e2，e3））的位置。
A clean way to handle the problem of frame invariance and to deal with points in a more intrinsic manner is to make a clearer distinction between points and vectors. We duplicate R3 into two copies, the first copy corresponding to points, where we forget the vector space structure, and the second copy corresponding to free vectors, where the vector space structure is important. Furthermore, we make explicit the important fact that the vector space R3 acts on the set of points R3 : Given any point a = (a1,a2,a3) and any vector v = (v1,v2,v3), we obtain the point
处理帧不变性问题和处理更内在的点的一个干净方法是对点和向量进行更清晰的区分。我们将r3复制成两个副本，第一个副本对应于点，忽略了向量空间结构，第二个副本对应于自由向量，其中向量空间结构很重要。此外，我们明确了向量空间r3作用于点r3集合的重要事实：给定任意点a=（a1，a2，a3）和任意向量v=（v1，v2，v3），我们得到该点。
a + v = (a1 + v1,a2 + v2,a3 + v3),
A+V=（A1+V1，A2+V2，A3+V3）
which can be thought of as the result of translating a to b using the vector v. We can imagine that v is placed such that its origin coincides with a and that its tip coincides with b. This action +: R3 × R3 → R3 satisfies some crucial properties. For example,
这可以被认为是用向量v将a转换为b的结果。我们可以想象，v的位置使其原点与a重合，其尖端与b重合。这个作用+：r3×r3→r3满足一些关键特性。例如，
	a + 0	=	a,
A+0=A，
	(a + u) + v	=	a + (u + v),
（A+U）+V=A+（U+V）
and for any two points a,b, there is a unique free vector →−ab such that
对于任意两点a，b，有一个独特的自由矢量→−ab，这样
b = a + →−ab.
B=A+→AB。
It turns out that the above properties, although trivial in the case of R3, are all that is needed to define the abstract notion of affine space (or affine structure). The basic idea is to consider two (distinct) sets E and →−E, where E is a set of points (with no structure) and →−E is a vector space (of free vectors) acting on the set E.
结果表明，上述属性虽然在R3的情况下微不足道，但却是定义仿射空间（或仿射结构）抽象概念所需的全部属性。基本思想是考虑两个不同的集合e和→−e，其中e是一组点（没有结构），而→−e是作用于集合e的向量空间（自由向量）。
Did you say “A fine space”?
你说“好地方”了吗？
Intuitively, we can think of the elements of →−E as forces moving the points in E, considered as physical particles. The effect of applying a force (free vector) u ∈ →−E to a point a ∈ E is a translation. By this, we mean that for every force u ∈ →−E, the action of the force u is to “move” every point a ∈ E to the point a+u ∈ E obtained by the translation corresponding→− to u viewed as a vector. Since translations can be composed, it is natural that E is a vector space.
直观地说，我们可以把→−e的元素看作是移动e中点的力，被认为是物理粒子。将力（自由矢量）u∈→−e施加到点a∈e上的效果是平移。由此，我们的意思是，对于每一个力u∈→−e，力u的作用是“移动”每一个点a∈e到点a+u∈e，这是由对应的→−到u的平移得到的，被视为一个向量。因为翻译可以组合，所以e是向量空间是很自然的。
For simplicity, it is assumed that all vector spaces under consideration are defined over the field R of real numbers. Most of the definitions and results also hold for an arbitrary field K, although some care is needed when dealing with fields of characteristic different from zero. It is also assumed that all families (λi)i∈I of scalars have finite support. Recall that a family (λi)i∈I of scalars has finite support if λi = 0 for all i ∈ I −J, where J is a finite subset of I. Obviously, finite families of scalars have finite support, and for simplicity, the reader may assume that all families of scalars are finite. The formal definition of an affine space is as follows.
为了简单起见，假设所有考虑的向量空间都是在实数的r域上定义的。大多数定义和结果也适用于任意场k，尽管在处理与零不同的特征场时需要注意一些。并假定所有的标量族（λi）i∈i都有有限的支持。回想一个标量的族（λi）i∈i具有有限的支持，如果λi=0表示所有i∈i−j，其中j是i的有限子集。显然，标量的有限族具有有限的支持，为了简单起见，读者可以假定所有标量的族都是有限的。仿射空间的形式定义如下。
Definition 23.1. An affine space is either the degenerate space reduced to the empty set, or a triple consisting of a nonempty set (of points), a vector space →−E (of translations, or free vectors), and an action +: E × E → E, satisfying the following conditions.
定义23.1.仿射空间可以是退化空间降为空集，也可以是由非空集（点）、向量空间→−e（平移或自由向量）和操作+：e×e→e组成的三重空间，满足以下条件。
(A1) a + 0 = a, for every a ∈ E.
（a1）a+0=a，每a∈e。
(A2) (a + u) + v = a + (u + v), for every a ∈ E, and every u,v ∈ →−E.
（a2）（a+u）+v=a+（u+v），对于每一个a∈e，以及每一个u，v∈→−e。
(A3) For any two points a,b ∈ E, there is a uniquesuch that a + u = b.
（a3）对于任意两点a，b∈e，存在一个唯一性，使得a+u=b。
The unique vector u ∈ →−E such that a + u = b is denoted by →−ab, or sometimes by ab, or even by b − a. Thus, we also write	→−
唯一向量u∈→−e，这样a+u=b用→−ab表示，有时用ab表示，甚至用b−a表示。因此，我们也写→−
b = a + ab
B=A+AB
(or b = a + ab, or even b = a + (b − a)). →−	→−
（或b=a+ab，甚至b=a+（b−a））。→–→–
The dimension of the affine space is the dimension dim(E) of the vector space →−E. For simplicity, it is denoted by dim(E).
仿射空间的维数是向量空间的维数dim（e）--e。为了简单起见，它用dim（e）表示。

Figure 23.4: Intuitive picture of an affine space.
图23.4：仿射空间的直观图片。
Conditions (A1) and (A2) say that the (abelian) group →−E acts on E, and Condition (A3) says that →−E acts transitively and faithfully on E. Note that
条件（a1）和（a2）表示（abelian）组→−e对e起作用，条件（a3）表示→−e对e起过渡和忠实的作用。注意：

for all a ∈ E and all v ∈ →−E, since	) is the unique vector such that
对于所有a∈e和所有v∈→−e，因为）是唯一的向量，这样
Thus, b = a + v is equivalent to ab = v. Figure 23.4 gives an intuitive picture of an affine space. It is natural to think of all vectors as having the same origin, the null vector.
因此，b=a+v等于ab=v。图23.4给出了仿射空间的直观图像。很自然地，所有向量都有相同的原点，即零向量。
The axioms defining an affine space  can be interpreted intuitively as saying that E and →−E are two different ways of looking at the same object, but wearing different sets of glasses, the second set of glasses depending on the choice of an “origin” in E. Indeed, we can choose to look at the points in E, forgetting that every pair (a,b) of points defines a unique vector →−ab in →−E, or we can choose to look at the vectors u in →−E, forgetting the points in E. Furthermore, if we also pick any point a in E, a point that can be viewed as an origin in E, then we can recover all the points in E as the translated points a + u for all u ∈ →−E. This can be formalized by defining two maps between E and →−E.
定义仿射空间的公理可以直观地解释为，e和→−e是观察同一物体的两种不同方式，但戴着不同的眼镜，第二组眼镜取决于e中“原点”的选择。实际上，我们可以选择观察t。他指向e，忘记了每对（a，b）点定义了一个唯一的向量→–––––––––––––––––––––––––––––––––––––––––––––––––––––––––e中的所有点作为所有u∈→−e的转换点a+u。这可以通过定义e和→−e之间的两个映射形式化。
For every a ∈ E, consider the mapping from →−E to E given by
对于每一个a∈e，考虑由
u 7→ a + u,
U 7→A+U，
where u ∈ →−E, and consider the mapping from E to →−E given by
式中u∈→−e，并考虑e到→−e的映射，由

where b ∈ E. The composition of the first mapping with the second is
式中b∈e。第一个映射与第二个映射的组合是
,
，
which, in view of (A3), yields u. The composition of the second with the first mapping is b 7→ →−ab 7→ a + →−ab,
根据（a3），得出u。第二个具有第一个映射的组合是b 7→→−ab7→a+→−a b，
which, in view of (A3), yields b. Thus, these compositions are the identity from →−E to →−E and the identity from E to E, and the mappings are both bijections.
从（a3）的角度来看，生成b。因此，这些组成是从→−e到→−e的同一性和从e到e的同一性，并且映射都是双射。
When we identify E with →−E via the mapping b →7	→−ab, we say that we consider E as the vector space obtained by taking a as the origin in E, and we denote it by Ea. Because Ea is a vector space, to be consistent with our notational conventions we should use the notation  (using an arrow), instead of Ea. However, for simplicity, we stick to the notation Ea.
当我们通过映射b→7→ab将e与→−e标识时，我们认为e是以a作为e的原点得到的向量空间，并用ea表示。因为ea是一个向量空间，为了符合我们的符号约定，我们应该使用符号（使用箭头），而不是ea。然而，为了简单起见，我们坚持使用符号ea。
Thus, an affine space →− is a way of defining a vector space structure on a set of points E, without making a commitment to a fixed origin in E. Nevertheless, as soon as we commit to an origin a in E, we can view E as the vector space Ea. However, we urge the reader to think of E as a physical set of points and of →−E as a set of forces acting on E, rather than reducing E to some isomorphic copy of Rn. After all, points are points, and not vectors! For notational simplicity, we will often denote an affine space), or even by E. The vector space →−E is called the vector space associated with E.
因此，仿射空间→−是在一组点E上定义向量空间结构的一种方法，而不承诺在E中有固定的原点。然而，只要我们承诺在E中有原点A，我们就可以将E视为向量空间EA。然而，我们敦促读者把E看作一个物理点集，把→−E看作作用于E的一组力，而不是把E简化成RN的一些同构副本。毕竟，点是点，而不是向量！为了便于记法，我们通常表示仿射空间），甚至用e表示。向量空间→−e被称为与e关联的向量空间。
 One should be careful about the overloading of the addition symbol +. Addition is well-defined on vectors, as in u + v; the translate a + u of a point a ∈ E by a vector  is also well-defined, but addition of points a + b does not make sense. In this respect, the notation b − a for the unique vector u such that b = a + u is somewhat confusing, since it suggests that points can be subtracted (but not added!).
注意加法符号+的过载。加在向量上定义得很好，如在u+v中；A点∈e的平移a+u也定义得很好，但是加a+b点没有意义。在这方面，唯一向量u的符号b−a使得b=a+u有些混乱，因为它表明可以减去点（但不能相加！）.
Any vector space →−E has an affine space structure specified by choosing , and letting + be addition in the vector space →−E. We will refer to the affine structure on a vector space →−E as the canonical (or natural) affine structure on →−E. In particular, the vector space Rn can be viewed as the affine space , denoted by An. In general, if K is any field, the affine space  is denoted by AnK. In order to distinguish between the double role played by members of Rn, points and vectors, we will denote points by row vectors, and vectors by column vectors. Thus, the action of the vector space Rn over the set Rn simply viewed as a set of points is given by
任何向量空间→−e都有一个通过选择指定的仿射空间结构，并让+在向量空间→−e中相加。我们将向量空间→−e上的仿射结构称为→−e上的规范（或自然）仿射结构。特别是，向量空间rn可以是视为仿射空间，用表示。一般来说，如果k是任何字段，仿射空间用ank表示。为了区分RN成员、点和向量所扮演的双重角色，我们将用行向量表示点，用列向量表示向量。因此，向量空间Rn在仅视为一组点的集合Rn上的作用由下式给出：
.
.
We will also use the convention that if x = (x1,...,xn) ∈ Rn, then the column vector associated with x is denoted by x (in boldface notation). Abusing the notation slightly, if a ∈ Rn is a point, we also write a ∈ An. The affine space An is called the real affine space of dimension n. In most cases, we will consider n = 1,2,3.
我们还将使用惯例，如果x=（x1，…，xn）∈rn，那么与x相关的列向量用x表示（粗体符号）。稍微滥用符号，如果a∈rn是一个点，我们也写a∈an。仿射空间an被称为维n的实仿射空间。在大多数情况下，我们将考虑n=1,2,3。

Figure 23.5: An affine space: the line of equation x + y − 1 = 0.
图23.5：仿射空间：方程x+y−1=0的直线。
23.2	Examples of Affine Spaces
23.2仿射空间示例
Let us now give an example of an affine space that is not given as a vector space (at least, not in an obvious fashion). Consider the subset L of A2 consisting of all points (x,y) satisfying the equation
现在让我们给出一个仿射空间的例子，它不是作为向量空间给出的（至少，不是以明显的方式）。考虑a2的子集l，由满足方程式的所有点（x，y）组成。
x + y − 1 = 0.
X+Y−1=0。
The set L is the line of slope −1 passing through the points (1,0) and (0,1) shown in Figure
设置L是穿过图中所示点（1,0）和（0,1）的坡度线−1。
23.5.
23.5。
The line L can be made into an official affine space by defining the action +: L×R → L of R on L defined such that for every point (x,1 − x) on L and any u ∈ R,
L线可以通过定义L上r的作用+：l×r→l而成为正式的仿射空间，定义为L上的每一点（x，1−x）和任何u∈r，
(x,1 − x) + u = (x + u,1 − x − u).
（X，1−X）+U=（X+U，1−X−U）。
It is immediately verified that this action makes L into an affine space. For example, for any two points a = (a1,1 − a1) and b = (b1,1 − b1) on L, the unique (vector) u ∈ R such that b = a + u is u = b1 − a1. Note that the vector space R is isomorphic to the line of equation x + y = 0 passing through the origin.
立即证实这个动作使L变成仿射空间。例如，对于L上的任意两点a=（a1,1−a1）和b=（b1,1−b1），唯一（向量）u∈r使得b=a+u是u=b1−a1。注意，向量空间r与通过原点的方程x+y=0的直线同构。
Similarly, consider the subset H of A3 consisting of all points (x,y,z) satisfying the equation
同样，考虑a3的子集h，由满足方程的所有点（x，y，z）组成。
x + y + z − 1 = 0.
X+Y+Z−1=0。
The set H is the plane passing through the points (1,0,0), (0,1,0), and (0,0,1). The plane H can be made into an official affine space by defining the action +: H × R2 → H of R2 on
设置h是穿过点（1,0,0）、（0,1,0）和（0,0,1）的平面。平面h可以通过定义上r2的作用+：h×r2→h而成为正式的仿射空间。

23.3. CHASLES’S IDENTITY
23.3。查理斯的身份

Figure 23.6: An affine space: the plane x + y + z − 1 = 0.
图23.6：仿射空间：平面x+y+z−1=0。
H defined such that for every point (x,y,1 − x − y) on H and any ,
h的定义是，对于h和任意点（x，y，1−x−y）的每个点，
.
.
For a slightly wilder example, consider the subset P of A3 consisting of all points (x,y,z) satisfying the equation
对于一个稍微疯狂的例子，考虑a3的子集p，它由满足方程的所有点（x，y，z）组成。
x2 + y2 − z = 0.
x2+y2−z=0.
The set P is a paraboloid of revolution, with axis Oz. The surface P can be made into an official affine space by defining the action +: P × R2 → P of R2 on P defined such that for every point (x,y,x2 + y2) on P and any ,
集合P是一个旋转的抛物面，轴为oz。曲面P可以通过定义p上r2的作用+：p×r2→p而变成一个正式的仿射空间，定义为p和an y上的每一点（x，y，x2+y2）。
.
.
See Figure 23.7.
见图23.7。
This should dispel any idea that affine spaces are dull. Affine spaces not already equipped with an obvious vector space structure arise in projective geometry.
这应该可以消除仿射空间单调的想法。射影几何中出现的仿射空间尚未配备明显的矢量空间结构。
23.3	Chasles’s Identity
23.3 Challes的身份
Given any three points a,b,c ∈ E, since c = a + →−ac, b = a + →−ab, and c = b + →−bc, we get
任意三点a，b，c∈e，因为c=a+→−ac，b=a+→−ab，c=b+→−bc，我们得到
c = b + →−bc = (a + →−ab) + →−bc = a + (→−ab + →−bc)
C=B+？-BC=（A+？-AB）+？-BC=A+（？-AB+？-BC）

Figure 23.7: The paraboloid of revolution P viewed as a two-dimensional affine space.
图23.7：旋转p的抛物面被视为二维仿射空间。
by (A2), and thus, by (A3),
通过（a2），因此，通过（a3）
→−ab + →−bc = →−ac,
→−AB+→−BC=→−AC，
which is known as Chasles’s identity, and illustrated in Figure 23.8. Since a = a + −aa→ and by (A1) a = a + 0, by (A3) we get
这被称为Challes的身份，如图23.8所示。由于a=a+−aa→和（a1）a=a+0，由（a3）我们得到
−aa→ = 0.
−AA→=0。
Thus, letting a = c in Chasles’s identity, we get
因此，让A=C在Challes的身份中，我们得到
→−ba = −→−ab.
→−BA=−→−AB.
Given any four points a,b,c,d ∈ E, since by Chasles’s identity
给定任意四点a，b，c，d∈e，因为由Challes的同一性
→−ab + →−bc = −ad→ + →−dc = →−ac,
→−AB+→−BC=−AD→→−DC=→−AC，
we have the parallelogram law
我们有平行四边形定律
	→−ab = →−dc	iff	→−bc = −ad.→
→−AB=→−DC IFF→−BC=−AD.→
23.4	Affine Combinations, Barycenters
23.4仿射组合，重心
A fundamental concept in linear algebra is that of a linear combination. The corresponding concept in affine geometry is that of an affine combination, also called a barycenter. However, there is a problem with the naive approach involving a coordinate system, as we saw in Section 23.1. Since this problem is the reason for introducing affine combinations, at the
线性代数的一个基本概念是线性组合。仿射几何中相应的概念是仿射组合，也称为重心。但是，我们在23.1节中看到，涉及坐标系的幼稚方法存在问题。因为这个问题是引入仿射组合的原因，在
23.4. AFFINE COMBINATIONS, BARYCENTERS
23.4。仿射组合，重心

Figure 23.8: Points and corresponding vectors in affine geometry.
图23.8：仿射几何中的点和相应的向量。
risk of boring certain readers, we give another example showing what goes wrong if we are not careful in defining linear combinations of points.
如果我们不小心定义点的线性组合，我们会给出另一个例子，说明出了什么问题。
Consider R2 as an affine space, under its natural coordinate system with origin O = (0,0) and basis vectors  and . Given any two points a = (a1,a2) and b = (b1,b2), it is natural to define the affine combination λa + µb as the point of coordinates
把r2看作是仿射空间，在它的自然坐标系下，原点为o=（0,0），基向量为和。任意两点a=（a1，a2）和b=（b1，b2），将仿射组合λa+μb定义为坐标点是很自然的。
(λa1 + µb1,λa2 + µb2).
（λa1+μb1，λa2+μb2）。
Thus, when a = (−1,−1) and b = (2,2), the point a + b is the point c = (1,1).
因此，当a=−1、−1）和b=（2,2）时，点a+b是点c=（1,1）。
Let us now consider the new coordinate system with respect to the origin c = (1,1) (and the same basis vectors). This time, the coordinates of a are (−2,−2), the coordinates of b are (1,1), and the point a+b is the point d of coordinates (−1,−1). However, it is clear that the point d is identical to the origin O = (0,0) of the first coordinate system. This situation is illustrated in Figure 23.9.
现在让我们考虑新的坐标系关于原点c=（1,1）（和相同的基向量）。这一次，a的坐标是（−2、−2），b的坐标是（1,1），a+b是坐标的点d（−1、−1）。但是，很明显，点D与第一个坐标系的原点O=（0,0）相同。这种情况如图23.9所示。
Thus, a+b corresponds to two different points depending on which coordinate system is used for its computation!
因此，A+B对应于两个不同的点，这取决于用于计算的坐标系！
This shows that some extra condition is needed in order for affine combinations to make sense. It turns out that if the scalars sum up to 1, the definition is intrinsic, as the following proposition shows.
这表明为了使仿射组合有意义，需要一些额外的条件。事实证明，如果scalars加起来是1，那么这个定义是内在的，如下所示。
Proposition 23.1. Given an affine space E, let (ai)i∈I be a family of points in E, and let (λi)i∈I be a family of scalars. For any two points a,b ∈ E, the following properties hold:
提案23.1.给定仿射空间e，设（a i）i∈i为e中的点族，设（λi）i∈i为标量族。对于任意两点a，b∈e，下列性质成立：
(1)	If Pi∈I λi = 1, then
如果pi∈iλi=1，则
.
.

Figure 23.9: The example from the beginning of Section 23.4.
图23.9：第23.4节开头的示例。
(2)	If Pi∈I λi = 0, then	X	X −→ λiaa−→i =	λibai.
如果pi∈iλi=0，则x x−→λiaa−→i=λibai。
	i∈I	i∈I
I∈I I∈I
Proof. (1) By Chasles’s identity (see Section 23.3), we have
证据。（1）根据Challes的身份（见第23.3节），我们
		since Pi∈I λi = 1
因为pi∈iλi=1
	= b + Xλiba−→i	since b = a + →−ab.
=b+xλi b a−→i，因为b=a+→−ab。
i∈I
我爱我
An illustration of this calculation in A2 is provided by Figure 23.10.
图23.10给出了A2中该计算的图解。
(2) We also have
（2）我们也有

since Pi∈I λi = 0.	
因为π∈iλi=0。
23.4. AFFINE COMBINATIONS, BARYCENTERS
23.4。仿射组合，重心

	b	b
乙乙
Figure 23.10: Part (1) of Proposition 23.1.
图23.10：提案23.1的第（1）部分。
Thus, by Proposition 23.1, for any family of points (ai)i∈I in E, for any family (λi)i∈I of scalars such that Pi∈I λi = 1, the point
因此，通过命题23.1，对于任意点族（ai）i∈i in e，对于任意点族（λi）i∈i的标量，使得pi∈iλi=1，点

is independent of the choice of the origin a ∈ E. This property motivates the following definition.
独立于原点a∈e的选择，该性质激发了以下定义。
Definition 23.2.P λi = 1, and for anyFor any family of points (a ∈ E, the pointai)i∈I in E, for any family (λi)i∈I of scalars such that	i∈I
定义23.2.pλi=1，对于任意点族（a∈e，点ai）i∈i in e，对于任意点族（λi）i∈i of scalars，使i∈i
a + Xλiaa−→i
A+Xλi a a−→I
i∈I
我爱我
(which is independent of a ∈ E, by Proposition 23.1) is called the barycenter (or barycentric combination, or affine combination) of the points ai assigned the weights λi, and it is denoted by
（独立于a∈e，由23.1命题）被称为分配给权重λi的点ai的重心（或重心组合或仿射组合），并用表示
X
X
λiai.
LAI IAI。
i∈I
我爱我
In dealing with barycenters, it is convenient to introduce the notion of a weighted point, which is just a pair (a,λ), where a ∈ E is a point, and λ ∈ R is a scalar. Then, given a family of weighted points ((ai,λi))i∈I, where Pi∈I λi = 1, we also say that the point Pi∈I λiai is the barycenter of the family of weighted points ((ai,λi))i∈I.
在处理重心问题时，引入一个加权点的概念是很方便的，它只是一对（a，λ），其中a∈e是一个点，而λ∈r是一个标量。然后，给定一个加权点族（（a i，λi））i∈i，其中pi∈iλi=1，我们也可以说点pi∈iλiai是加权点族的重心（（ai，λi））i∈i。
Note that the barycenter x of the family of weighted points ((ai,λi))i∈I is the unique point such that
注意，加权点族的重心x（（ai，λi））i∈i是唯一的点，因此
 for every a ∈ E,
对于每一个a∈e，
and setting a = x, the point x is the unique point such that
设置a=x，点x是唯一的点，这样
Xλixa−→i = 0.
xλixa－→i=0.
i∈I
我爱我
In physical terms, the barycenter is the center of mass of the family of weighted points ((ai,λi))i∈I (where the masses have been normalized, so that Pi∈I λi = 1, and negative masses are allowed).
在物理术语中，重心是加权点族（（ai，λi））i∈i的质量中心（其中质量已经归一化，使得pi∈iλi=1，并且允许负质量）。
Remarks:
评论：
(1)	(Since the barycenter of a family ((λi)i∈I of scalars with finite support (and such thatai,λi))i∈I of weighted points is defined for familiesPi∈I λi = 1), we might as well assume that I is finite. Then, for all m ≥ 2, it is easy to prove that the barycenter of m weighted points can be obtained by repeated computations of barycenters of two weighted points.
（由于有有限支持的标量族（（λi）i∈i（并且这样ai，λi））i∈i的加权点是为族定义的，所以我们也可以假设i是有限的。然后，对于所有m≥2，通过对两个加权点的重心的重复计算，很容易证明m加权点的重心是可以得到的。
(2)	This result still holds, provided that the field K has at least three distinct elements, but the proof is trickier!
这个结果仍然成立，前提是K域至少有三个不同的元素，但是证明更难！
(3)	denote it byWhen Pi∈I λPi = 0i∈I λ, the vectoriai. This observation will be used to define a vector space in whichPi∈I λiaa−→i does not depend on the point a, and we may linear combinations of both points and vectors make sense, regardless of the value of Pi∈I λi.
当pi∈iλpi=0i∈iλ时，用向量表示。这个观察将被用来定义一个向量空间，其中pi∈iλi a a−→i不依赖于a点，我们可以使点和向量的线性组合有意义，不管pi∈iλi的值如何。
Figure 23.11 illustrates the geometric construction of the barycenters g1 and g2 of the weighted points a, , and c, , and (a,−1), (b,1), and (c,1).
图23.11说明了加权点A、C和（A、−1）、（B、1）和（C、1）的重心g1和g2的几何结构。
The point g1 can be constructed geometrically as the middle of the segment joining c to the middle of the segment (a,b), since
点g1可以几何构造为连接c到段（a，b）中间的段的中间，因为

The point g2 can be constructed geometrically as the point such that the middle  of the segment (b,c) is the middle of the segment (a,g2), since
点g2可以几何构造为点，使得段（b，c）的中间是段（a，g2）的中间，因为
.
.
Later on, we will see that a polynomial curve can be defined as a set of barycenters of a fixed number of points. For example, let (a,b,c,d) be a sequence of points in A2. Observe that
稍后，我们将看到一条多项式曲线可以定义为一组具有固定数量点的重心。例如，让（A、B、C、D）是A2中的点序列。注意
(1 − t)3 + 3t(1 − t)2 + 3t2(1 − t) + t3 = 1,
（1−t）3+3t（1−t）2+3t 2（1−t）+t3=1，


Figure 23.11: Barycenters,
图23.11：重心，
since the sum on the left-hand side is obtained by expanding (t + (1 − t))3 = 1 using the binomial formula. Thus,
因为左侧的和是通过使用二项式展开（t+（1-t））3=1得到的。因此，
(1 − t)3 a + 3t(1 − t)2 b + 3t2(1 − t)c + t3 d
（1−T）3 A+3T（1−T）2 B+3T2（1−T）C+T3 D
is a well-defined affine combination. Then, we can define the curve F : A → A2 such that
是定义明确的仿射组合。然后，我们可以定义曲线f:a→a2，这样
F(t) = (1 − t)3 a + 3t(1 − t)2 b + 3t2(1 − t)c + t3 d.
F（t）=（1−t）3 A+3T（1−t）2 B+3T2（1−t）C+T3 D。
Such a curve is called a B´ezier curve, and (a,b,c,d) are called its control points. Note that the curve passes through a and d, but generally not through b and c. It can be sbown that any point F(t) on the curve can be constructed using an algorithm performing affine interpolation steps (the de Casteljau algorithm).
这样的曲线称为B’ezier曲线，并且（A、B、C、D）称为其控制点。注意曲线通过A和D，但一般不通过B和C。曲线上的任何点F（T）都可以使用执行仿射插值步骤的算法（de casteljau算法）来构造。
23.5	Affine Subspaces
23.5仿射子空间
In linear algebra, a (linear) subspace can be characterized as a nonempty subset of a vector space closed under linear combinations. In affine spaces, the notion corresponding to the notion of (linear) subspace is the notion of affine subspace. It is natural to define an affine subspace as a subset of an affine space closed under affine combinations.
在线性代数中，（线性）子空间可以表示为在线性组合下闭合的向量空间的非空子集。在仿射空间中，与（线性）子空间概念相对应的概念是仿射子空间的概念。将仿射子空间定义为仿射组合下封闭的仿射空间的子集是很自然的。
Definition 23.3. Given an affine space, a subset V of E is an affine subspace (of
定义23.3.给定仿射空间，e的子集v是仿射子空间（of
) if for every family of weighted pointsP λiai belongs to V .	((ai,λi))i∈I in V such that Pi∈I λi = 1, the barycenter	i∈I
）如果每个加权点族的λi ai都属于v.（（ai，λi））i∈i在v中使得pi∈iλi=1，则重心i∈i
An affine subspace is also called a flat by some authors. According to Definition 23.3, the empty set is trivially an affine subspace, and every intersection of affine subspaces is an affine subspace.
仿射子空间也被一些作者称为平面。根据23.3的定义，空集通常是仿射子空间，仿射子空间的每个交叉点都是仿射子空间。
As an example, consider the subset U of R2 defined by
例如，考虑由
,
，
i.e., the set of solutions of the equation
即方程组的解
ax + by = c,
ax+by=c，
where it is assumed that a = 06 or b = 06 . Given any m points (xi,yi) ∈ U and any m scalars λi such that λ1 + ··· + λm = 1, we claim that
假设a=06或b=06。给定任何m点（十一，易）u和任何m个标量i i，使之等于，1 + +，+，m＝1，我们声称

Indeed, (xi,yi) ∈ U means that axi + byi = c,
实际上，（Xi，Yi）u表示AXI+BYI= C，
and if we multiply both sides of this equation by λi and add up the resulting m equations, we get
如果我们用这个方程的两边乘以λi，把得到的m方程加起来，我们得到

and since λ1 + ··· + λm = 1, we get
既然λ1+·····+λm=1，我们得到

which shows that
这表明

Thus, U is an affine subspace of A2. In fact, it is just a usual line in A2. It turns out that U is closely related to the subset of R2 defined by
因此，u是a2的仿射子空间。实际上，它只是A2中的一条普通线。结果表明，u与由
 ,
，
i.e., the set of solutions of the homogeneous equation
即齐次方程的一组解
ax + by = 0
ax+by=0

Figure 23.12: An affine line U and its direction.
图23.12：仿射线U及其方向。
obtained by setting the right-hand side of ax + by = c to zero. Indeed, for any m scalars λi, the same calculation as above yields that
通过将ax+的右侧x=c设置为零获得。事实上，对于任何m标量λi，与上面相同的计算得出：
m
米
	X	∈ →−
X∈→−
	λi(xi,yi)	U ,
（I，I）U，
i=1
i＝1
this time without any restriction on the	, since the right-hand side of the equation is null. Thus, →−U is a subspace of R2. In fact, U is one-dimensional, and it is just a usual line in R2. This line can be identified with a line passing through the origin of A2, a line that is parallel to the line U of equation ax + by = c, as illustrated in Figure 23.12. Now, if (x0,y0) is any point in U, we claim that
这一次对没有任何限制，因为方程的右边是空的。因此，→−u是r2的一个子空间。实际上，u是一维的，它只是r2中的一条普通线。这条线可以用穿过a2原点的线来标识，a2原点与方程ax+by=c的u线平行，如图23.12所示。现在，如果（X0，Y0）是U中的任何一个点，我们声称

where (x0,y0) + →−U =	(x0 + u1,y0 + u2) | (u1,u2) ∈ →−U	. n	o
其中（X0，Y0）+→−U=（X0+U1，Y0+U2）（U1，U2）∈→−U。氮氧化物
First, (x0,y0) + →−U ⊆ U, since ax0 + by0 = c and au1 + bu2 = 0 for all (u1,u2) ∈ →−U . Second, if (x,y) ∈ U, then ax + by = c, and since we also have ax0 + by0 = c, by subtraction, we get
首先，（X0，y0）+→−u u，因为ax0+by0=c，au1+bu2=0代表所有（u1，u2）∈→−u。其次，如果（x，y）∈u，那么ax+by=c，由于我们也有ax0+by0=c，通过减法，我们得到
a(x − x0) + b(y − y0) = 0,
A（X−X0）+B（Y−Y0）=0，
which shows that (→− x − x0,y −	, and thus (x,y) ∈ (x0,y0) + →−U . Hence, we also have U ⊆ (x0,y0) + U , and U = (x0,y0) + U .
这表明（→−X−X0，Y−，因此（X，Y）∈（X0，Y0）+→−U。因此，我们也有u（x0，y0）+u和u=（x0，y0）+u。
The above example shows that the affine line U defined by the equation
上面的例子表明，方程定义的仿射线u
ax + by = c
ax+by=c
is obtained by “translating” the parallel line →−U of equation
通过“平移”方程的平行线→−U得到
ax + by = 0
ax+by=0
passing through the origin. In fact, given any point (x0,y0) ∈ U,
穿过原点。实际上，给定任意点（X0，Y0）∈U，
U = (x0,y0) + →−U .
U=（X0，Y0）+→−U。
More generally, it is easy to prove the following fact. Given any m × n matrix A and any vector b ∈ Rm, the subset U of Rn defined by
一般来说，很容易证明以下事实。给定任意m×n矩阵a和任意向量b∈rm，由
U = {x ∈ Rn | Ax = b}
u=x∈rn ax=b
is an affine subspace of An.
是的仿射子空间。
Actually, observe that Ax = b should really be written as Ax> = b, to be consistent with our convention that points are represented by row vectors. We can also use the boldface notation for column vectors, in which case the equation is written as Ax = b. For the sake of minimizing the amount of notation, we stick to the simpler (yet incorrect) notation Ax = b.
实际上，注意ax=b应该写成ax>=b，以符合我们的惯例，即点由行向量表示。我们也可以对列向量使用黑体表示法，在这种情况下，方程写为ax=b。为了最小化表示法的数量，我们坚持使用更简单（但不正确）的表示法ax=b。
If we consider the corresponding homogeneous equation Ax = 0, the set
如果我们考虑相应的齐次方程ax=0，
→−U = {x ∈ Rn | Ax = 0}
→−u=x∈rn ax=0
is a subspace of Rn, and for any x0 ∈ U, we have
是Rn的子空间，对于任何X0∈U，我们有
U = x0 + →−U .
U=X0+→−U。
This is a general situation. Affine subspaces can be characterized in terms of subspaces of
这是一般情况。仿射子空间可以用
→−E. Let V be a nonempty subset of E. For every family (a1,...,an) in V , for any family (λ1,...,λn) of scalars, and for every point a ∈ V , observe that for every x ∈ E,
→−e.设v为e的非空子集，对于v中的每个族（a1，…，an），对于scalars的任何族（λ1，…，λn），对于每个点a∈v，观察每个x∈e，

is the barycenter of the family of weighted points
是加权点族的重心
,
，
since
自从
.
.
Given any point a ∈ E and any subset →−V of →−E, let a+→−V denote the following subset of E:
给定任意点a∈e和→−e的任何子集→−v，让a+→−v表示e的以下子集：
a + →−V = na + v | v ∈ →−V o.
A+→−V=NA+V V∈→−V O.
Figure 23.13: An affine subspace V and its direction →−V .
图23.13：仿射子空间V及其方向→−V。
Proposition 23.2. Let  be an affine space.
提案23.2.设为仿射空间。
(1)	A nonempty subset V of E is an affine subspace iff for every point a ∈ V , the set
e的一个非空子集v是每个点a∈v的仿射子空间iff，集合

is a subspace of →−E. Consequently, . Furthermore,
是→−e的子空间。因此，。此外，
is a subspace of E and Va = V for all a ∈ E. Thus,.
是所有a∈e的e和va=v的子空间，因此。
(2)	For any subspace →−V of →−E and for any a ∈ E, the set V = a+→−V is an affine subspace.
对于→−e的任意子空间→−v，对于任意a∈e，集合v=a+→−v是仿射子空间。
Proof. The proof is straightforward, and is omitted. It is also given in Gallier [71].	
证据。证据很直接，被省略了。加利尔文[71]也给出了这一点。
In particular, when E is the natural affine space associated with a vector space →−E, Proposition 23.2 shows that every affine subspace of E is of the form u + →−U , for a subspace →−U of →−E. The subspaces of →−E are the affine subspaces of E that contain 0.
特别地，当e是与向量空间→−e相关联的自然仿射空间时，命题23.2表明e的每个仿射子空间的形式为u+→−u，对于→−e的子空间→−u，→−e的子空间是包含0的e的仿射子空间。
The subspace →−V associated with an affine subspace is called the direction of V . It is also clear that the map +: V ×→−V → V induced by +: E × E → E confers to →− an affine structure. Figure 23.13 illustrates the notion of affine subspace.
与仿射子空间相关联的子空间→−v称为v的方向。还清楚地表明，由+：e×e→e诱导的map+：v×→−v→v赋予→−一个仿射结构。图23.13说明了仿射子空间的概念。
By the dimension of the subspace V , we mean the dimension of →−V .
通过子空间v的维数，我们是指→−v的维数。
An affine subspace of dimension 1 is called a line, and an affine subspace of dimension 2 is called a plane.
维1的仿射子空间称为直线，维2的仿射子空间称为平面。
An affine subspace of codimension 1 is called a hyperplane (recall that a subspace F of a vector space E has codimension 1 iff there is some subspace G of dimension 1 such that E = F ⊕ G, the direct sum of F and G, see Strang [165] or Lang [106]).
余维1的仿射子空间称为超平面（回想一下，向量空间e的子空间f具有余维1，如果存在维度1的某些子空间g，则e=f_g，f和g的直接和，参见strang[165]或lang[106]）。
We say that two affine subspaces U and V are parallel if their directions are identical. Equivalently, since →−U = →−V , we have U = a + →−U and V →−= b + →−U for any a ∈ U and any b ∈ V , and thus V is obtained from U by the translation ab.
我们说两个仿射子空间u和v方向相同时是平行的。等价地，由于→−u=→−v，我们有u=a+→−u和v→−=b+→−u表示任何a∈u和任何b∈v，因此v是通过翻译ab从u获得的。
In general, when we talk about n points a1,...,an, we mean the sequence (a1,...,an), and not the set {a1,...,an} (the ai’s need not be distinct). →−
一般来说，当我们讨论n点a1，…，an时，我们指的是序列（a1，…，an），而不是集合a1，…，an（ai不必是不同的）。δ
By Proposition 23.2, a line is specified by a point a ∈ E and a nonzero vector v ∈ E,
在23.2命题中，直线由点a∈e和非零向量v∈e指定，
i.e., a line is the set of all points of the form a + λv, for λ ∈ R→−.	→−
也就是说，一条直线是A+λv形式的所有点的集合，对于λ∈R→−。→−
We say that three points a,b,c are collinear if the vectors ab and ac are linearly dependent. If two of the points→− a,b,c are distinct, say a =6 b, then there is a unique λ ∈ R such that →−ac = λab, and we define the ratio .
如果向量AB和AC是线性相关的，我们就说三个点A，B，C是共线的。如果两个点→−a，b，c是不同的，假设a=6b，那么有一个唯一的λ∈r，这样→−a c=λa b，我们定义了比率。
A plane is specified by a point a ∈ E and two linearly independent vectors u,v ∈ →−E, i.e., a plane is the set of all points of the form a + λu + µv, for λ,µ ∈→−R.→−
平面由点a∈e和两个线性无关向量u，v∈→−e指定，即平面是形式a+λu+μv的所有点的集合，对于λ，μ∈→−r.→−
We say that four points a,b,c,d are coplanar if the vectors ab, ac, and are linearly dependent. Hyperplanes will be characterized a little later.
我们说，如果向量AB、AC和线性相关，那么四个点A、B、C、D是共面的。稍后将对超平面进行描述。
Proposition 23.3. Given an affine spaceP λiai (where Pi∈I λi , for any family= 1) is the smallest affine subspace(ai)i∈I of points in
提案23.3.给定一个仿射空间pλi ai（其中，对于任何族=1，pi∈iλi）是中点的最小仿射子空间（ai）i∈i。
E, the set V of barycenters i∈I containing (ai)i∈I.
e，重心i∈i的集合v包含（ai）i∈i。
Proof. If (ai)i∈I is empty, then V = ∅, because of the condition Pi∈I λi = 1. If (ai)i∈I is nonempty, then the smallest affine subspace containing (P λiai, and thus, it is enough to show that aVi)is closed under affine combina-i∈I must contain the set V of barycenters i∈I tions, which is immediately verified.	
证据。如果（ai）i∈i为空，则v=∅，因为条件pi∈iλi=1。如果（ai）i∈i是非空的，那么含有（pλiai，因此，足以证明avi）的最小仿射子空间在仿射组合a-i∈i下是封闭的，必须包含质心i∈i的集v，并立即得到验证。
Given a nonempty subset S of E, the smallest affine subspace of E generated by S is often denoted by hSi. For example, a line specified by two distinct points a and b is denoted by ha,bi, or even (a,b), and similarly for planes, etc.
给定e的非空子集s，s生成的e的最小仿射子空间通常用hsi表示。例如，由两个不同的点a和b指定的一条线用ha、bi或偶数（a、b）表示，同样，对于平面等。
Remarks:
评论：
(1)	Since it can be shown that the barycenter of n weighted points can be obtained by repeated computations of barycenters of two weighted points, a nonempty subset V of E is an affine subspace iff for every two points a,b ∈ V , the set V contains all barycentric combinations of a and b. If V contains at least two points, then V is an affine subspace iff for any two distinct points a,b ∈ V , the set V contains the line determined by a and b, that is, the set of all points (1 − λ)a + λb, λ ∈ R.
由于可以证明N个加权点的重心可以通过两个加权点的重心的重复计算得到，因此E的一个非空子集V是每两个点A，B∈V的仿射子空间iff，集合V包含A和B的所有重心组合。如果v包含S至少两点，则V是任意两点的仿射子空间iff，a，b∈v，集合V包含由a和b确定的直线，即所有点（1−λ）a+λb，λ∈r的集合。
(2)	This result still holds if the field K has at least three distinct elements, but the proof is trickier!
如果字段k至少有三个不同的元素，这个结果仍然有效，但是证明更难！

23.6	Affine Independence and Affine Frames
23.6仿射独立性和仿射框架
Corresponding to the notion of linear independence in vector spaces, we have the notion of affine independence. Given a family (ai)i∈I of points in an affine space E, we will reduce the notion of (affine) independence of these points to the (linear) independence of the families (a−−i→aj)j∈(I−{i}) of vectors obtained by choosing any ai as an origin. First, the following proposition shows that it is sufficient to consider only one of these families.
对应于向量空间中的线性独立概念，我们有仿射独立的概念。给定仿射空间E中点的族（a i）i∈i，我们将这些点的（仿射）独立性的概念简化为选择任意ai作为原点获得的向量族（a−i→a j）j∈（i−i）的（线性）独立性。首先，下面的命题表明，只考虑其中一个家庭是足够的。
Proposition 23.4. Given an affine space	→−	, let (ai)i∈I be a family of points in
提案23.4.给定仿射空间→−，让（a i）i∈i是
E. If the family (a−−i→aj)j∈(I−{i}) is linearly independent for some i ∈ I, then (a−−i→aj)j∈(I−{i}) is linearly independent for every i ∈ I.
e.如果家族（a−i→a j）j∈（i−i）对某些i∈i是线性独立的，那么（a−i→aj）j∈（i−i）对每个i∈i是线性独立的。
Proof. Assume that the family (a−−i→aj)j∈(I−{i}) is linearly independent for some specific i ∈ I.
证据。假设家族（a−i→a j）j∈（i−i）对于某些特定的i∈i是线性独立的。
Let k ∈ I with k =6	i, and assume that there are some scalars (λj)j∈(I−{k}) such that
设k∈i，k=6i，并假设有一些标度（λj）j∈（i−k），这样
X λja−−k→aj = 0.
xλja−k→aj=0.
j∈(I−{k})
J∈（I−K）
Since
自从
a−−k→aj = a−−k→ai + a−−i→aj,
A−K→AJ=A−K→Ai+A−I→AJ，
we have
我们有
,
，
and thus
因此
Since the family (− {	}	Pa−−i→aj)j∈(I−{λji}= 0) is linearly independent, we must have, which implies that λj = 0 for all j ∈ (λIj − {= 0k}for all).	j ∈
由于家族（−pa−−i→aj）j∈（i−λji=0）是线性独立的，因此我们必须有，这意味着所有j∈（λij−=0K）的λj=0。
(I	i,k ) and	j∈(I−{k})
（i i，k）和j∈（i−k）
We define affine independence as follows.
我们定义仿射独立性如下。
Definition 23.4. Given an affine space, a family (ai)i∈I of points in E is affinely independent if the family (a−−i→aj)j∈(I−{i}) is linearly independent for some i ∈ I.
定义23.4.给定一个仿射空间，如果（a−i→a j）j∈（i−i）对某些i∈i线性独立，则e中点的族（ai）i∈i是仿射独立的。

Figure 23.14: Affine independence and linear independence
图23.14：仿射独立和线性独立
Definition 23.4 is reasonable, because by Proposition 23.4, the independence of the family (a−−i→aj)j∈(I−{i}) does not depend on the choice of ai. A crucial property of linearly independent vectors (u1,...,um) is that if a vector v is a linear combination
定义23.4是合理的，因为根据命题23.4，家庭的独立性（a−i→a j）j∈（i−i）不依赖于人工智能的选择。线性无关向量（u1，…，um）的一个重要特性是，如果向量v是线性组合

of the ui, then the λi are unique. A similar result holds for affinely independent points.
对于ui，那么λi是唯一的。仿射独立点也有类似的结果。
Proposition 23.5. Given an affine space, let (a0,...,am) be a family of m + 1 points in E. Let x ∈ E, and assume that . Then, the family (λ0,...,λm) such that  is unique iff the family  is linearly independent.
提案23.5。给定仿射空间，设（a0，…，a m）为e中m+1点的族，设x∈e，并假定。然后，家族（λ0，…，λm）是唯一的，如果家族是线性独立的。
Proof. The proof is straightforward and is omitted. It is also given in Gallier [71].	
证据。证据很直接，被省略了。加利尔文[71]也给出了这一点。
Proposition 23.5 suggests the notion of affine frame. Affine frames are the affine analogues of bases in vector spaces. Let  be a nonempty affine space, and let (a0,...,am) be a family of + 1 points in E. The family (a0,...,am) determines the family of m vectors (. Conversely, given a point a0 in E and a family of m vectors
命题23.5提出了仿射框架的概念。仿射框架是向量空间中基的仿射类似物。设为非空仿射空间，设（a0，…，a m）为e中+1点的族。族（a0，…，am）决定m向量的族（。相反，给定e中的点a0和m向量族
(u1,...,um) in E, we obtain the family of m+1 points (a0,...,am) in E, where ai = a0 +ui,
（u1，…，um）在e中，我们得到e中m+1点（a0，…，am）的族，其中ai=a0+ui，
1 ≤ i ≤ m.
1≤i≤m。
Thus, for any m ≥ 1, it is equivalent to consider a family of→− m + 1 points (a0,...,am) in E, and a pair (a0,(u1,...,um)), where the ui are vectors in E. Figure 23.14 illustrates the notion of affine independence.
因此，对于任何m≥1，它等价于考虑e中的→−m+1点（a0，…，am）族和一对（a0，（u1，…，um）），其中ui是e中的向量。图23.14说明了仿射独立的概念。
Remark: The above observation also applies to infinite families (ai)i∈I of points in E and families (ui)i∈I−{0} of vectors in →−E, provided that the index set I contains 0.
注：上述观测也适用于E点的无限族（ai）i∈i和→−e中向量的族（ui）i∈i−0，前提是索引集i包含0。
When () is a basis of →−E then, for every x ∈ E, since , there is a unique family (x1,...,xm) of scalars such that
当（）是→−e的基础时，那么，对于每个x∈e，因为有一个唯一的标量族（x1，…，xm），这样
.
.
The scalars (x1,...,xm) may be considered as coordinates with respect to )). Since
scalars（x1，…，xm）可被视为相对于）的坐标。自从
 iff ,
iff ,
x ∈ E can also be expressed uniquely as
x∈e也可以唯一地表示为

with = 1, and where, and λi = xi for 1 ≤ i ≤ m. The scalars (λ0,...,λm) are also certain kinds of coordinates with respect to (a0,...,am). All this is summarized in the following definition.
当＝1时，在1和±m＝m的情况下，以及（i，0，…，αm）也是相对于（a0，…，AM）的某种坐标。所有这些在下面的定义中进行了总结。
Definition 23.5. Given an affine space, an affine frame with origin a0 is a family (a0,...,am) of m + 1 points in E such that the list of vectors () is a basis of
定义23.5.给定仿射空间，原点为a0的仿射帧是e中m+1点的族（a0，…，am），因此矢量列表（）是
→−E. The pair (a0,(a−−0→a1,...,a−−0a→m)) is also called an affine frame with origin a0. Then, every x ∈ E can be expressed as
→e.这对（a0，（a−0→a1，…，a−0a→m））也被称为原点为a0的仿射帧。那么，每个x∈e可以表示为

for a unique family (x1,...,xm) of scalars, called the coordinates of x w.r.t. the affine frame )). Furthermore, every x ∈ E can be written as
对于标量的唯一族（x1，…，xm），称为x w.r.t.仿射帧的坐标）。此外，每个x∈e可以写成
x = λ0a0 + ··· + λmam
x=λ0a0+····+λmam
for some unique family (λ0,...,λm) of scalars such that λ0+···+λm = 1 called the barycentric coordinates of x with respect to the affine frame (a0,...,am). See Figure 23.15.
对于某些特殊的标度族（λ0，…，λm），如λ0+·····+λm=1，就仿射框架（a0，…，am）而言，称为x的重心坐标。见图23.15。
The coordinates (x1,...,xm) and the barycentric coordinates (λ0,..., λm) are related by the equations  and λi = xi, for 1 ≤ i ≤ m. An affine frame is called an affine basis by some authors. A family (ai)i∈I of points in E is affinely dependent if it is not affinely independent. We can also characterize affinely dependent families as follows.
坐标（x1，…，xm）和重心坐标（α0，…，αm）与方程和Li i＝Xi有关，对于1个i i＝m。仿射框架被一些作者称为仿射基。如果e中点的族（a i）i∈i不是仿射独立的，则它是仿射依赖的。我们还可以将仿射相依族定义为如下。

Figure 23.15: The affine frame (a0,a1,a2,a3) for A3. The coordinates for x = (−1,0,2)
图23.15:a3的仿射框（a0、a1、a2、a3）。X的坐标=（-1,0,2）
= 1, while the barycentric coordinates for x are λ0 = 3,
=1，而x的重心坐标为λ0=3，
1 = −
1=-
Proposition 23.6. Given an affine space , let (ai)i∈I be a family of points in E. jThe family∈ I, i∈ (ai)i∈I is affinely dependent iff there is a familyP λixa−→i = 0 for every x ∈ E. (λi)i∈I such that λj = 06 for some
提案23.6.给定一个仿射空间，让（a i）i∈i是e中的点族，j该族∈i，i∈（ai）i∈i是仿射相依的，如果存在一个家族，则每个x∈e有一个家族，即λi x a−→i=0。（λi）i∈i，这样对于某些人来说，λj=06
P λi = 0, and	i∈I I
pλi=0，i∈i i
Proof. By Proposition 23.5, the family (ai)i∈I is affinely dependent iff the family of vectors (a−−i→aj)j∈(I−{i}) is linearly dependent for some i ∈ I. For any i ∈ I, the family (a−−i→aj)j∈(I−{i}) is linearly dependent iff there is a family (λj)j∈(I−{i}) such that λj = 06 for some j, and such that
证据。根据23.5，家族（a i）i∈i是仿射依赖的，如果向量家族（a−i→a j）j∈（i−i）对某些i∈i是线性依赖的，对于任何i∈i，家族（a−i→aj）j∈（i−i）是线性依赖的，如果存在家族（λj）j∈（i−i），那么λj=06 f或者一些J，这样
X λja−−i→aj = 0.
xλja−i→aj=0.
j∈(I−{i})
J∈（I−I）
Then, for any x ∈ E, we have
那么，对于任何x∈e，我们有
,
，
and letting, we get Pi∈I λixa−→i = 0, with Pi∈I λi = 0 and λj = 06 for some j ∈ I. The converse is obvious by setting x = ai for some i such that λi = 06 , since Pi∈I λi = 0 implies that λj = 06 , for some j =6 i. 
假设，我们得到了π∈iλixa−→i=0，对于一些j∈i，用π∈i=0和λj=06。通过为一些i设置x=ai，使得λi=06明显相反，因为π∈iλi=0意味着对于一些j=6i，用π∈iλi=06。
a2
A2
	a0	
A0
	a0a1	
A0A1
Figure 23.16: Examples of affine frames and their convex hulls.
图23.16：仿射框架及其凸面外壳的示例。
Even though Proposition 23.6 is rather dull, it is one of the key ingredients in the proof of beautiful and deep theorems about convex sets, such as Carath´eodory’s theorem, Radon’s theorem, and Helly’s theorem.
尽管23.6命题相当单调，但它是证明凸集美丽而深刻定理的关键要素之一，如Carath'Eodory定理、Radon定理和Helly定理。
A family of two points (a,b) in E is affinely independent iff →−ab = 06 , iff a =6 b. If a =6 b, the affine subspace generated by a and b is the set of all points (1−λ)a+λb, which is the unique line passing through a and b. A family of three points (a,b,c) in E is affinely independent iff →−ab and →−ac are linearly independent, which means that a, b, and c are not on the same line (they are not collinear). In this case, the affine subspace generated by (a,b,c) is the set of all points (1 − λ − µ)a + λb + µc, which is the unique plane containing→− →− −→ a, b, and c. A family of four points (a,b,c,d) in E is affinely independent iff ab, ac, and ad are linearly independent, which means that a, b, c, and d are not in the same plane (they are not coplanar). In this case, a, b, c, and d are the vertices of a tetrahedron. Figure 23.16 shows affine frames and their convex hulls for |I| = 0,1,2,3.
e中的两点族（a，b）是仿射独立的iff→−ab=06，iff a=6b，如果a=6b，a和b生成的仿射子空间是所有点（1−λ）a+λb的集合，是通过a和b的唯一线，e中的三点族（a，b，c）是仿射独立的iff。→−AB和→−AC是线性独立的，这意味着A、B和C不在同一条线上（它们不是共线）。在这种情况下，由（a，b，c）生成的仿射子空间是所有点（1−λ−μ）a+λb+μc的集合，这是包含→−→→−−a，b和c的唯一平面。e中的四个点（a，b，c，d）的族是非仿射独立的iff ab，ac和ad是线性独立的，而mea是线性独立的。n表示a、b、c和d不在同一平面上（它们不是共面的）。在这种情况下，a、b、c和d是四面体的顶点。图23.16显示了i=0,1,2,3的仿射框架及其凸壳。
Given n+1 affinely independent points (a0,...,an) in E, we can consider the set of points λ0a0 +···+λnan, where λ0 +···+λn = 1 and λi ≥ 0 (λi ∈ R). Such affine combinations are called convex combinations. This set is called the convex hull of (a0,...,an) (or n-simplex spanned by (a0,...,an)). When n = 1, we get the segment between a0 and a1, including a0 and a1. When n = 2, we get the interior of the triangle whose vertices are a0,a1,a2, including boundary points (the edges). When n = 3, we get the interior of the tetrahedron whose vertices are a0,a1,a2,a3, including boundary points (faces and edges). The set
给定e中的n+1仿射独立点（a0，…，an），我们可以考虑一组点λ0a0+·····+λnan，其中λ0+·····+λn=1且λi≥0（λi∈r）。这种仿射组合称为凸组合。这个集合被称为（a0，…，an）（或N-单纯形的（a0，…，an））的凸壳。当n=1时，我们得到a0和a1之间的段，包括a0和a1。当n=2时，我们得到顶点为a0，a1，a2的三角形的内部，包括边界点（边）。当n=3时，我们得到顶点为a0、a1、a2、a3的四面体内部，包括边界点（面和边）。布景
where 0 ≤ λi ≤ 1 (λi ∈ R)}
其中0≤λi≤1（λi∈r）
is called the parallelotope spanned by (a0,...,an). When E has dimension 2, a parallelotope is also called a parallelogram, and when E has dimension 3, a parallelepiped. Figure 23.17 shows the convex hulls and associated parallelotopes for |I| = 0,1,2,3.
被称为（a0，…，an）所跨越的Parallelotope。当e的维数为2时，平行切开体也称为平行四边形；当e的维数为3时，平行六面体称为平行四边形。图23.17显示了i=0,1,2,3的凸壳和相关的平行耳。


Figure 23.17: Examples of affine frames, convex hulls, and their associated parallelotopes.
图23.17：仿射框架、凸面外壳及其相关的平行耳。
More generally, we say that a subset V of E is convex if for any two points a,b ∈ V , we have c ∈ V for every point c = (1 − λ)a + λb, with 0 ≤ λ ≤ 1 (λ ∈ R).
一般来说，我们说e的一个子集v是凸的，如果对于任意两点a，b∈v，对于每一点c=（1−λ）a+λb，我们都有c∈v，其中0≤λ≤1（λ∈r）。
 Points are not vectors! The following example illustrates why treating points as vectors may cause problems. Let a,b,c be three affinely independent points in A3. Any point x in the plane (a,b,c) can be expressed as
点不是向量！以下示例说明了将点作为向量处理可能会导致问题的原因。让a，b，c是a3中的三个仿射独立点。平面（a，b，c）中的任何点x都可以表示为
x = λ0a + λ1b + λ2c,
x=λ0a+λ1b+λ2c，
where λ0 + λ1 + λ2 = 1. How can we compute λ0,λ1,λ2? Letting a = (a1,a2,a3), b = (b1,b2,b3), c = (c1,c2,c3), and x = (x1,x2,x3) be the coordinates of a,b,c,x in the standard frame of A3, it is tempting to solve the system of equations
式中，λ0+λ1+λ2=1。我们如何计算λ0，λ1，λ2？假设a=（a1，a2，a3），b=（b1，b2，b3），c=（c1，c2，c3），x=（x1，x2，x3）是a3标准框架中a，b，c，x的坐标，很容易解出方程组。

 .
.
However, there is a problem when the origin of the coordinate system belongs to the plane
然而，当坐标系的原点属于平面时，存在一个问题。
(a,b,c), since in this case, the matrix is not invertible! What we should really be doing is to solve the system
（a，b，c），因为在这种情况下，矩阵是不可逆的！我们真正应该做的是解决这个系统
λ0Oa−→ + λ1Ob−→ + λ2Oc−→ = Ox,−→
λ0oa−→+λ1ob−→+λ2oc−→=Ox，−→
where O is any point not in the plane (a,b,c). An alternative is to use certain well-chosen cross products.
其中o是平面以外的任何点（a，b，c）。另一种选择是使用某些精选的交叉产品。
It can be shown that barycentric coordinates correspond to various ratios of areas and volumes; see the problems.
可以看出，重心坐标对应于面积和体积的不同比例；见问题。
23.7	Affine Maps
23.7仿射图
Corresponding to linear maps we have the notion of an affine map. An affine map is defined as a map preserving affine combinations.
对应于线性映射，我们有仿射映射的概念。仿射映射定义为保留仿射组合的映射。
Definition 23.6. Given two affine spaces and , a function f : E → E0 is an affine map iff for every family ((ai,λi))i∈I of weighted points in E such that Pi∈I λi = 1, we have
定义23.6.在给定两个仿射空间的情况下，函数f:e→e0是每个族（（a i，λi））的仿射映射iff，e中加权点的i∈i，使得pi∈iλi=1
.
.
In other words, f preserves barycenters.
换句话说，F保存重心。
Affine maps can be obtained from linear maps as follows. For simplicity of notation, the same symbol + is used for both affine spaces (instead of using both + and +0).
仿射映射可以从线性映射中获得，如下所示。为了简化表示法，相同的符号+用于两个仿射空格（而不是同时使用+和+0）。
Proposition 23.7.−→	→Given any point a ∈ E, any point b ∈ E0, and any linear map h: →−E → E0, the map f : E	E0 defined such that
命题23.7。−→→给定任意点a∈e，任意点b∈e0，以及任意线性映射h：→−e→e0，映射f:e e0定义如下：
f(a + v) = b + h(v)
F（A+V）=B+H（V）
is an affine map.
是仿射映射。
Proof. Indeed, for any family (λi)i∈I of scalars with Pi∈I λi = 1 and any family (vi)i∈I, since
证据。事实上，对于任何具有pi∈iλi=1的标量（λi）i∈i和任何族（vi）i∈i，因为

and
和
,
，
we have
我们有
as claimed.	
如要求。
Note that the condition Pi∈I λi = 1 was implicitly used (in a hidden call to Proposition
注意，条件pi∈iλi=1是隐式使用的（在对命题的隐藏调用中）
23.1) in deriving that
23.1）在推导
	X	X
十倍
	λi(a + vi) = a +	λivi
λi（a+vi）=a+λivi
	i∈I	i∈I
I∈I I∈I
and
和
X	X λi(b + h(vi)) = b + λih(vi).
x xλi（b+h（vi））=b+λih（vi）。
	i∈I	i∈I
I∈I I∈I
As a more concrete example, the map
作为一个更具体的例子，地图

defines an affine map in A2. It is a “shear” followed by a translation. The effect of this shear on the square (a,b,c,d) is shown in Figure 23.18. The image of the square (a,b,c,d) is the parallelogram (a0,b0,c0,d0).
在A2中定义仿射映射。它是一个“剪切”，然后是一个翻译。这种剪切对正方形（a，b，c，d）的影响如图23.18所示。正方形（a，b，c，d）的图像是平行四边形（a0，b0，c0，d0）。
Let us consider one more example. The map
让我们再考虑一个例子。地图

is an affine map. Since we can write
是仿射映射。因为我们可以写
 ,
，
d = (5,2) c = (6,2)
D=（5,2）C=（6,2）
	d = (0,1)	c = (1,1)	
D=（0,1）C=（1,1）
		a = (3,1) b = (4,1)
A=（3,1）B=（4,1）
	a = (0,0)	b = (1,0)
A=（0,0）B=（1,0）
Figure 23.18: The effect of a shear.
图23.18：剪切效应。
this affine map is the composition of a shear, followed by a rotation of angle π/4, followed by a magnification of ratio √2, followed by a translation. The effect of this map on the square (a,b,c,d) is shown in Figure 23.19. The image of the square (a,b,c,d) is the parallelogram
这个仿射图是剪切力的组成，然后旋转角度π/4，然后放大比例√2，然后平移。图23.19显示了这张地图对广场（A、B、C、D）的影响。正方形（a，b，c，d）的图像是平行四边形。
(a0,b0,c0,d0).
（a0、b0、c0、d0）。
c	= (5,4)
=（5,4）
d	= (0,1)	c = (1,1) 
=（0,1）c=（1,1）
	a = (0,0)	b = (1,0)	a = (3,0)
A=（0,0）B=（1,0）A=（3,0）
Figure 23.19: The effect of an affine map.
图23.19：仿射映射的效果。
The following proposition shows the converse of what we just showed. Every affine map is determined by the image of any point and a linear map.
下面的命题显示了我们刚才所展示的相反的情况。每个仿射映射都由任意点的图像和线性映射决定。
Proposition 23.8. Given an affine map f : E → E0, there is a unique linear map →−f : →−E →  such that f(a + v) = f(a) + →−f (v),
提案23.8。给定仿射映射f:e→e0，有一个唯一的线性映射→−f：→−e→这样f（a+v）=f（a）+→−f（v），
for every a ∈ E and every v ∈ →−E.
对于每一个a∈e和每一个v∈→−e。
Proof. Let a ∈ E be any point in E. We claim that the map defined such that
证据。假设a∈e是e中的任意点，我们声称地图定义如下：

for every v ∈ →−E is a linear map →−f : →−E → E−→0. Indeed, we can write
对于每一个v∈→−e是一个线性映射→−f：→−e→e−→0。事实上，我们可以写
a + λv = λ(a + v) + (1 − λ)a,
a+λv=λ（a+v）+（1-λ）a，
since, and also
因为，还有
a + u + v = (a + u) + (a + v) − a,
A+U+V=（A+U）+（A+V）−A，
since. Since f preserves barycenters, we get
从那以后。因为F保留了重心，我们得到
f(a + λv) = λf(a + v) + (1 − λ)f(a).
f（a+λv）=λf（a+v）+（1-λ）f（a）。
If we recall that x = Pi∈I λiai is the barycenter of a family ((ai,λi))i∈I of weighted points (with Pi∈I λi = 1) iff  for every b ∈ E,
如果我们记得x=pi∈iλi ai是一个家族的重心（（ai，λi））i∈i的加权点（pi∈iλi=1）iff对于每个b∈e，
we get
我们得到
,
，
showing that). We also have
显示出来）。我们也有
f(a + u + v) = f(a + u) + f(a + v) − f(a),
F（A+U+V）=F（A+U）+F（A+V）−F（A）、
from which we get
我们从中得到
,
，
showing that f is a linear map. For any other point b ∈ E, since
表示f是一个线性映射。对于任何其他点b∈e，因为

b + v = (a + v) − a + b, and since f preserves barycenters, we get
B+V=（A+V）−A+B，由于F保留了重心，我们得到
f(b + v) = f(a + v) − f(a) + f(b),
F（B+V）=F（A+V）−F（A）+F（B）
which implies that
这意味着
,
，
Thus, f(b)f(b + v) = f(a)f(a + v), which shows that the definition of does not depend on the choice of a ∈ E. The fact that f is unique is obvious: We must have →−f (v) = The unique linear map →−f : →−E → −E→0 given by Proposition 23.8 is called the linear map associated with the affine map f.
因此，f（b）f（b+v）=f（a）f（a+v），这表明f的定义不依赖于a∈e的选择，f是唯一的这一事实是显而易见的：我们必须有→−f（v）=唯一的线性映射→−f：→−e→−e→0，由23.8给出的，称为与仿射映射。
Note that the condition f(a + v) = f(a) + →−f (v),
注意，条件f（a+v）=f（a）+→−f（v），
for every a ∈ E and every v ∈ →−E, can be stated equivalently as
对于每一个a∈e和每一个v∈→−e，可以等价地表示为
	f(x) = f(a) + →−f (−ax→),	or ,
f（x）=f（a）+→−f（−ax→），或，
for all a,x ∈ E. Proposition 23.8 shows that for any affine map→−f : →−E → −E→0, such thatf : E → E0, there are points a ∈ E, b ∈ E0, and a unique linear map
对于所有a，x∈e，命题23.8表明，对于任意仿射映射→−f：→−e→−e→0，这样f:e→e0，有点a∈e，b∈e0，和一个唯一的线性映射
f(a + v) = b + →−f (v),
F（A+V）=B+→−F（V）
for all v ∈ →−E (just let b = f(a), for any ). Affine maps for which →−f is the identity map are called translations. Indeed, if f = id,
对于所有v∈→−e（只要让b=f（a），对于任何）。其中→−f是身份图的仿射映射称为翻译。实际上，如果f=id，
and so	
如此
which shows that f is the translation induced by the vector ) (which does not depend on a).
这表明f是矢量引起的翻译（不依赖a）。
Since an affine map preserves barycenters, and since an affine subspace V is closed under barycentric combinations, the image f(V ) of V is an affine subspace in E0. So, for example, the image of a line is a point or a line, and the image of a plane is either a point, a line, or a plane.
由于仿射映射保留重心，并且仿射子空间v在重心组合下闭合，因此v的图像f（v）是e0中的仿射子空间。例如，直线的图像是一个点或一条线，平面的图像是一个点、一条线或一个平面。
It is easily verified that the composition of two affine maps is an affine map. Also, given affine maps f : E → E0 and g: E0 → E00, we have
很容易证明两个仿射映射的组合是一个仿射映射。另外，给定仿射映射f:e→e0和g:e0→e0，我们得到
,
，

iffAn affine mapf : E → E0 is injective, and thatis constant iff. It is easy to show that an affine mapf :→−fE:→→−E E→0 is surjective iff−E→0 is the null (constant) linear map equal→−f : f→−E: E→→−E→0Eis surjective.0 is injective
iffan仿射mapf:e→e0是内射的，这是常数iff。可以很容易地看出，仿射映射f：→−f e：→−e→0是可射的iff−e→0是零（常数）线性映射等于→−f:f→−e:e→−e→0是可射的。0是可射的。

to 0 for all v ∈ E.
对于所有v∈e为0。
If E is an affine space of dimension m and (a0,a1,...,am) is an affine frame for E, then for any other affine space F and for any sequence (b0,b1,...,bm) of m+1 points in F, there is a unique affine map f : E → F such that f(ai) = bi, for 0 ≤ i ≤ m. Indeed, f must be such that
如果e是维数m的仿射空间，（a0，a1，…，am）是e的仿射框架，那么对于任何其他仿射空间f和f中m+1点的任何序列（b0，b1，…，bm），都有一个唯一的仿射映射f:e→f，因此f（a i）=bi，对于0≤i≤m。实际上，f必须是这样的：
f(λ0a0 + ··· + λmam) = λ0b0 + ··· + λmbm,
f（λ0a0+····+λmam）=λ0b0+····+λmbm，
where λ0+···+λm = 1, and this defines a unique affine map on all of E, since (a0,a1,...,am) is an affine frame for E.
其中，λ0+····+λm=1，这定义了所有e上的唯一仿射映射，因为（a0，a1，…，am）是e的仿射帧。
Using affine frames, affine maps can be represented in terms of matrices. We explain how an affine map f : E → E is represented with respect to a frame (a0,...,an) in E, the more general case where an affine map f : E → F is represented with respect to two affine frames (a0,...,an) in E and (b0,...,bm) in F being analogous. Since
使用仿射框架，仿射映射可以用矩阵表示。我们解释了仿射映射f:e→e是如何相对于e中的帧（a0，…，an）表示的，更一般的情况是仿射映射f:e→f相对于e中的两个仿射帧（a0，…，an）表示，而f中的（b0，…，bm）是类似的。自从
f(a0 + x) = f(a0) + →−f (x)
F（a0+x）=F（a0）+→−F（x）
for all x ∈ →−E, we have
对于所有x∈→−e，我们有
.
.
Since x, a−−−−0f(a→0), and a−−−−−−−−0f(a0 +→x), can be expressed as
因为x，a−−−0f（a→0）和a−−−−−0f（a0+→x）可以表示为
x
网络错误
a−−−−0f(a→0)
网络错误
a−−−−−−−−0f(a0 +→x)
网络错误	=
网络错误
=
网络错误
=
网络错误	x1a−−0→a1 + ··· + xna−−0→an, b1a−−0→a1 + ··· + bna−−0→an, y1a−−0→a1 + ··· + yna−−0→an,
网络错误
if A = (aij) is the n×n matrix of the linear map →−f over the basis (, y, and b denote the column vectors of components (x1,...,xn), (y1,...,yn), and (b1,...,bn),
如果a=（aij）是线性映射的n×n矩阵→−f的基（，y和b表示分量（x1，…，xn），（y1，…，yn）和（b1，…，bn）的列向量，

is equivalent to
等于
y = Ax + b.
y=ax+b。
Note that b = 06 unless f(a0) = a0. Thus, f is generally not a linear transformation, unless it has a fixed point, i.e., there is a point a0 such that f(a0) = a0. The vector b is the “translation part” of the affine map. Affine maps do not always have a fixed point. Obviously, nonnull translations have no fixed point. A less trivial example is given by the affine map
注意b=06，除非f（a0）=a0。因此，f一般不是线性变换，除非它有一个固定点，即有一个点a0，这样f（a0）=a0。向量B是仿射映射的“翻译部分”。仿射映射并不总是有固定点。显然，非空翻译没有固定点。仿射映射给出了一个不那么简单的例子。
.
.
This map is a reflection about the x-axis followed by a translation along the x-axis. The affine map
这张地图是关于x轴的反射，然后是沿x轴的平移。仿射图

can also be written as
也可以写为

which shows that it is the composition of a rotation of angle π/3, followed by a stretch (by a factor of 2 along the x-axis, and by a factor of  along the y-axis), followed by a translation. It is easy to show that this affine map has a unique fixed point. On the other hand, the affine map
这表明它是角π/3旋转的组成，然后是拉伸（沿x轴乘以系数2，沿y轴乘以系数），然后是平移。很容易看出这个仿射映射有一个唯一的不动点。另一方面，仿射图

has no fixed point, even though
没有固定点，即使
 ,
，
and the second matrix is a rotation of angle θ such that cos and sin.
第二个矩阵是角θ的旋转，cos和sin。
There is a useful trick to convert the equation y = Ax + b into what looks like a linear equation. The trick is to consider an (n + 1) × (n + 1) matrix. We add 1 as the (n + 1)th component to the vectors x, y, and b, and form the (n + 1) × (n + 1) matrix
将方程y=ax+b转换成线性方程有一个很有用的技巧。技巧是考虑（n+1）×（n+1）矩阵。我们将1作为（n+1）th分量加到向量x、y和b上，形成（n+1）×n+1矩阵。

so that y = Ax + b is equivalent to
所以y=ax+b等于
 .
.
This trick is very useful in kinematics and dynamics, where A is a rotation matrix. Such affine maps are called rigid motions.
这个技巧在运动学和动力学中非常有用，其中a是旋转矩阵。这种仿射映射称为刚性运动。
If f : E → E0 is a bijective affine map, given any three collinear points a,b,c in E, with a =6 b, where, say, c = (1 − λ)a + λb, since f preserves barycenters, we have f(c) = (1−λ)f(a)+λf(b), which shows that f(a),f(b),f(c) are collinear in E0. There is a converse to this property, which is simpler to state when the ground field is K = R. The converse states that given any bijective function f : E → E0 between two real affine spaces of the same dimension n ≥ 2, if f maps any three collinear points to collinear points, then f is affine. The proof is rather long (see Berger [11] or Samuel [138]).
如果f:e→e0是双射仿射映射，给定任意三个共线点a，b，c在e中，a=6b，其中，比如，c=（1−λ）a+λb，因为f保留了重心，所以我们得到f（c）=（1−λ）f（a）+λf（b），这表明f（a）、f（b）、f（c）在e0中是共线的。有一个与这个性质相反的性质，当地面场为k=r时，它的状态更简单。在两个相同维n≥2的实仿射空间之间给出了任意双射函数f:e→e0，如果f将任意三个共线点映射到共线点，那么f是仿射的。证据相当长（见Berger[11]或Samuel[138]）。
Given three collinear points a,b,c, where a =6 c, we have b = (1 − β)a + βc for some unique β, and we define the ratio of the sequence a,b, c, as →−
给定三个共线点a，b，c，其中a=6c，我们得到一些独特β的b=（1−β）a+βc，我们将序列a，b，c的比值定义为→−
ratio(,
比率（，
provided that β = 16 , i.e., b =6 c. When b = c, we agree that ratio(a,b,c) = ∞. We warn our readers that other authors define the ratio of a,b,c as −ratio( −→. Since affine maps preserve barycenters, it is clear that affine maps preserve the ratio of three points.
假设β=16，即b=6 c，当b=c时，我们同意比值（a，b，c）=∞。我们警告读者，其他作者将A、B、C的比率定义为−比率（−→）。由于仿射映射保留重心，很明显仿射映射保留了三个点的比例。
23.8	Affine Groups
23.8仿射群
We now take a quick look at the bijective affine maps. Given an affine space E, the set of affine bijections f : E → E is clearly a group, called the affine group of , and denoted by GA(E). Recall that the group of bijective linear maps of the vector space E is denoted by GL(→−E). Then, the map f 7→ →−f defines a group homomorphism L: GA(E) → GL(→−E). The kernel of this map is the set of translations on E.
现在我们快速地看一下双目标仿射图。给定仿射空间e，f:e→e的仿射双射集合显然是一个群，称为仿射群，用ga（e）表示。回想一下，向量空间e的双射线性映射组用gl（→−e）表示。然后，图F7→→−F定义了一个组同态l:ga（e）→gl（→−e）。这个地图的核心是E上的一组翻译。
The subset of all linear maps of the form λid→−E , where λ ∈ R − {0}, is a subgroup of GL(→−E), and is denoted by R∗id→−E (where λid→−E (u) = λu, and R∗ = R − {0}). The subgroup DIL(E) = L−1(R∗id→−E ) of GA(E) is particularly interesting. It turns out that it is the disjoint union of the translations and of the dilatations of ratio λ = 16 . The elements of DIL(E) are called affine dilatations.
形式为λid→−e的所有线性映射的子集，其中，λ∈r−0，是gl（→−e）的一个子组，并由r id→−e表示（其中，λid→−e（u）=λu，r=r−0）。GA（e）的子组dil（e）=l−1（r id→−e）特别有趣。结果表明，它是平移与扩张之比λ=16的不相交的结合。dil（e）的元素称为仿射扩张。
Given any point a ∈ E, and any scalar λ ∈ R, a dilatation or central dilatation (or homothety) of center a and ratio λ is a map Ha,λ defined such that
给定任意点a∈e和任意标量λ∈r，中心a和比率λ的扩张或中心扩张（或同构）是映射ha，λ定义如下：
Ha,λ(x) = a + λax,−→
ha，λ（x）=a+λax，−→
for every x ∈ E.
每x∈e。
Remark: The terminology does not seem to be universally agreed upon. The terms affine dilatation and central dilatation are used by Pedoe [132]. Snapper and Troyer use the term dilation for an affine dilatation and magnification for a central dilatation [157]. Samuel uses homothety for a central dilatation, a direct translation of the French “homoth´etie” [138]. Since dilation is shorter than dilatation and somewhat easier to pronounce, perhaps we should use that!
备注：术语似乎没有得到普遍认同。pedoe使用了“仿射扩张”和“中心扩张”这两个术语[132]。Snapper和Troyer使用术语“扩张”表示仿射扩张，而“放大”表示中心扩张[157]。塞缪尔用谐音作为中心扩张词，直接翻译了法语“homoth'etie”[138]。因为扩张比扩张短，而且发音更容易，也许我们应该使用它！
Observe that Ha,λ(a) = a, and when λ = 06 and x =6 a, Ha,λ(x) is on the line defined by a and x, and is obtained by “scaling” ax−→ by λ.
观察Ha，λ（a）=a，当λ=06和x=6 a时，Ha，λ（x）在a和x定义的线上，并通过“缩放”a x－→由λ获得。
Figure 23.20 shows the effect of a central dilatation of center d. The triangle (a,b,c) is magnified to the triangle (a0,b0,c0). Note how every line is mapped to a parallel line.
图23.20显示了中心D的中心扩张效应。三角形（a，b，c）放大为三角形（a0，b0，c0）。注意每条线是如何映射到一条平行线的。
	When λ = 1, Ha,1 is the identity. Note that. When λ = 06	, it is clear that
当λ=1时，ha，1为同一性。请注意。当λ=06时，很明显
Ha,λ is an affine bijection. It is immediately verified that
ha，λ是仿射双射。立即证实
Ha,λ ◦ Ha,µ = Ha,λµ.
ha，λha，μ=ha，λμ。
We have the following useful result.
我们得到了以下有用的结果。

23.8. AFFINE GROUPS
23.8。仿射群

Figure 23.20: The effect of a central dilatation Hd,λ(x).
图23.20：中心扩张hd的影响，λ（x）。
Proposition 23.9. Given any affine space E, for any affine bijection f ∈ GA(E), if →−f = λid→−E , for some λ ∈ R∗ with λ = 16	, then there is a unique point c ∈ E such that f = Hc,λ.
提案23.9.给定任意仿射空间e，对于任意仿射双射f∈ga（e），如果→−f=λid→−e，对于某些λ∈r且λ=16，则存在一个唯一点c∈e，使得f=hc，λ。
Proof. The proof is straightforward, and is omitted. It is also given in Gallier [71].	
证据。证据很直接，被省略了。加利尔文[71]也给出了这一点。
Clearly, if →−f = id→−E , the affine map f is a translation. Thus, the group of affine dilatations DIL(E) is the disjoint union of the translations and of the dilatations of ratio λ = 06 ,1. Affine dilatations can be given a purely geometric characterization.
显然，如果→−f=id→−e，仿射映射f就是一个翻译。因此，仿射扩张群dil（e）是平移与比率λ=06，1扩张的不相交的结合。仿射扩张可以给出一个纯粹的几何特征。
Another point worth mentioning is that affine bijections preserve the ratio of volumes of parallelotopes. Indeed, given any basis B = (u1,...,um) of the vector space →−E associated with the affine space E, given any m + 1 affinely independent points (a0,...,am), we can compute the determinant det) w.r.t. the basis B. For any bijective affine map f : E → E, since
另一点值得一提的是仿射双射保留了平行耳的体积比。实际上，如果向量空间的任何基b=（u1，…，um）→e与仿射空间e相关联，给定任何m+1仿射独立点（a0，…，am），我们可以计算行列式det）w.r.t.对于任何双射仿射映射f:e→e，因为

and the determinant of a linear map is intrinsic (i.e., depends only on →−f , and not on the particular basis B), we conclude that the ratio
线性映射的行列式是内在的（即只取决于→−f，而不是特定的基础b），我们得出如下结论：

is independent of the basis) is the volume of the parallelotope spanned by (a0,...,am), where the parallelotope spanned by any point a and the vectors
不依赖于基）是由（a0，…，am）所跨越的平行头的体积，其中平行头由任意点a和向量所跨越。

Figure 23.21: The theorem of Thales.
图23.21：泰雷兹定理。
(u1,...,um) has unit volume (see Berger [11], Section 9.12), we see that affine bijections preserve the ratio of volumes of parallelotopes. In fact, this ratio is independent of the choice of the parallelotopes of unit volume. In particular, the affine bijections f ∈ GA(E) such that det = 1 preserve volumes. These affine maps form a subgroup SA(E) of GA(E) called the special affine group of E. We now take a glimpse at affine geometry.
（u1，…，um）有单位体积（见Berger[11]，第9.12节），我们发现仿射双射保留了平行耳的体积比。事实上，这一比例与单位体积的平行叶的选择无关。尤其是仿射双射f∈ga（e），使得det=1保留体积。这些仿射映射形成了GA（e）的一个子群sa（e），称为e的特殊仿射群。现在我们来看看仿射几何。
23.9	Affine Geometry: A Glimpse
23.9仿射几何：一瞥
In this section we state and prove three fundamental results of affine geometry. Roughly speaking, affine geometry is the study of properties invariant under affine bijections. We now prove one of the oldest and most basic results of affine geometry, the theorem of Thales.
在这一节中，我们陈述并证明了仿射几何的三个基本结果。一般来说，仿射几何是研究仿射双射下的不变量性质。我们现在证明了仿射几何最古老和最基本的结果之一，泰雷兹定理。
Proposition 23.10. Given any affine space E, if H1,H2,H3 are any three distinct parallel hyperplanes, and A and B are any two lines not parallel to Hi, letting ai = Hi ∩ A and bi = Hi ∩ B, then the following ratios are equal:
提案23.10。给定任意仿射空间e，如果h1、h2、h3是任意三个不同的平行超平面，而a和b是任意两条不平行于hi的线，让ai=hi a和bi=hi b，则下列比值相等：

Conversely, for any point d on the line, then d = a3.
相反，对于线上的任何点d，则d=a3。
Proof. Figure 23.21 illustrates the theorem of Thales. We sketch a proof, leaving the details as an exercise. Since H1,H2, H3 are parallel, they have the same direction →−H, a hyperplane
证据。图23.21说明了泰雷兹定理。我们画了一个证明，把细节留作练习。因为h1，h2，h3是平行的，它们有相同的方向→−h，一个超平面
23.9. AFFINE GEOMETRY: A GLIMPSE
23.9。仿射几何：一瞥
in →−E. Let be any nonnull vector such that A = a1+Ru. Since A is not parallel to H, we have E = H→−⊕Ru, and thus we can define the linear map p:→→−E → Ru, the projection on Ru parallel to H. This linear map induces an affine map f : E A, by defining f such that
在→−e.中，设为任意非零矢量，使a=a1+ru。由于a不平行于h，我们有e=h→−ru，因此我们可以定义线性映射p：→→−e→ru，即ru上平行于h的投影。该线性映射通过定义f来诱导仿射映射f:e a，从而
f(b1 + w) = a1 + p(w),
f（b1+w）=a1+p（w）
for all w ∈ →−E. Clearly, f(b1) = a1, and since H1,H2,H3 all have direction →−H, we also have f(b2) = a2 and f(b3) = a3. Since f is affine, it preserves ratios, and thus
对于所有w∈→−e，很明显，f（b1）=a1，由于h1、h2、h3都有方向→−h，我们也有f（b2）=a2和f（b3）=a3。因为f是仿射的，所以它保持比率，因此
.
.
The converse is immediate.	
反过来说是直接的。
We also have the following simple proposition, whose proof is left as an easy exercise.
我们也有以下简单的命题，它的证明是一个简单的练习。
Proposition 23.11. Given any affine space E, given any two distinct points a,b ∈ E, and for any affine dilatation f different from the identity, if a0 = f(a), D = ha,bi is the line passing through a and b, and D0 is the line parallel to D and passing through a0, the following are equivalent:
提案23.11.给定任意仿射空间e，给定任意两个不同点a，b∈e，并且对于任何不同于恒等式的仿射展开f，如果a0=f（a），d=ha，bi是通过a和b的线，而d0是平行于d并通过a0的线，则以下是等价的：
(i)	b0 = f(b);
b0=f（b）；
(ii)	If f is a translation, then b0 is the intersection of D0 with the line parallel to ha,a0i passing through b;
如果f是平移，则b0是d0与平行于ha，a0i通过b的线的交点；
If f is a dilatation of center c, then b0 = D0 ∩ hc,bi.
如果f是中心c的膨胀，则b0=d0 hc，bi。
The first case is the parallelogram law, and the second case follows easily from Thales’ theorem. For an illustration, see Figure 23.22.
第一种情况是平行四边形定律，第二种情况很容易从泰雷兹定理得出。有关说明，请参见图23.22。
We are now ready to prove two classical results of affine geometry, Pappus’s theorem and Desargues’s theorem. Actually, these results are theorems of projective geometry, and we are stating affine versions of these important results. There are stronger versions that are best proved using projective geometry.
我们现在准备证明仿射几何的两个经典结果，帕普斯定理和德沙格定理。实际上，这些结果是射影几何的定理，我们正在陈述这些重要结果的仿射形式。有更强大的版本，最好证明使用射影几何。
Proposition 23.12. Given any affine plane E, any two distinct lines D and D0, then for any distinct points a,b,c on D and a0,b0,c0 on D0, if a,b,c,a0, b0, c0 are distinct from the intersection of D and D0 (if D and D0 intersect) and if the lines ha,b0i and ha0,bi are parallel, and the lines hb,c0i and hb0,ci are parallel, then the lines ha,c0i and ha0,ci are parallel.
提案23.12。给定任意仿射平面e，任意两条不同的线d和d0，那么对于任意不同的点a，b，c，d和a0，b0，c0，d0，如果a，b，c，a0，b0，c0与d和d0的交点不同（如果d和d0相交），并且如果线ha，b0i和ha0，bi平行，并且线hb，c0i和hb0，ci是para那么线ha，c0i和ha0，ci是平行的。


Figure 23.22: An illustration of Proposition 23.11. The bottom left diagram illustrates a translation, while the bottom right illustrates a central dilation through c.
图23.22：提案23.11的说明。左下角的图表说明了平移，而右下角的图表说明了通过C的中心扩张。
Proof. Pappus’s theorem is illustrated in Figure 23.23. If D and D0 are not parallel, let d be their intersection. Let f be the dilatation of center d such that f(a) = b, and let g be the dilatation of center d such that g(b) = c. Since the lines ha,b0i anda0ha=0,bfi(bare parallel, and0) and b0 = g(c0).
证据。Pappus定理如图23.23所示。如果d和d0不平行，则d是它们的交点。设f为中心d的扩张，使f（a）=b，设g为中心d的扩张，使g（b）=c。由于线ha，b0i和0ha=0，bfi（裸平行，and0）和b0=g（c0）。
However, we observed that dilatations with the same center commute, and thusand thus, lettingthe lines hb,c0i andh =hb0g,c◦ifare parallel, by Proposition 23.11 we have, we get c =Dh(aand) andD0aare parallel, we use translations instead of0 = h(c0). Again, by Proposition 23.11, thef ◦g = g◦f, lines ha,c0i and ha0,ci are parallel. If dilatations.	
然而，我们观察到在相同的中心通勤条件下的扩张，因此，假设线hb，c0i和h=hb0g，c如果是平行的，根据23.11号命题，我们得到c=dh（aand）和d0aare平行，我们使用翻译而不是0=h（c0）。同样，根据23.11号提案，off g=g f，行ha，c0i和ha0，ci是平行的。如果膨胀。
There is a converse to Pappus’s theorem, which yields a fancier version of Pappus’s theorem, but it is easier to prove it using projective geometry. It should be noted that in axiomatic presentations of projective geometry, Pappus’s theorem is equivalent to the commutativity of the ground field K (in the present case, K = R). We now prove an affine version of Desargues’s theorem.
有一个与Pappus定理相反的定理，它产生了Pappus定理的更高级的版本，但使用射影几何更容易证明它。应该注意的是，在射影几何的公理化表示中，Pappus定理等价于基场k的交换性（在本例中，k=r）。我们现在证明了德沙格定理的仿射形式。
Proposition 23.13. Given any affine space E, and given any two triangles (a,b,c) and (a0,b0,c0), where a,b,c,a0,b0,c0 are all distinct, if ha,bi and ha0,b0i are parallel and hb,ci and hb0,c0i are parallel, then ha,ci and ha0,c0i are parallel iff the lines ha,a0i, hb,b0i, and hc,c0i are either parallel or concurrent (i.e., intersect in a common point).
提案23.13。给定任意仿射空间e，给定任意两个三角形（a，b，c）和（a0，b0，c0），其中a，b，c，a0，b0，c0都是不同的，如果ha，bi和ha0，b0i是平行的，hb，ci和hb0，c0i是平行的，那么ha，ci和ha0，c0i是平行的，如果ha，a0i，hb，b0i和hc，c0i是平行的或同时的。（也就是说，在一个公共点上相交）。
hProof. We prove half of the proposition, the direction in which it is assumed that haa,c0,bi0iandare
H车顶。我们证明了这个命题的一半，即假设haa，c0，bi0iandare的方向。
a0,c0i are parallel, leaving the converse as an exercise. Since the lines ha,bi and h
a0，c0i是平行的，把相反的留作练习。因为行哈，bi和h
23.9. AFFINE GEOMETRY: A GLIMPSE
23.9。仿射几何：一瞥

Figure 23.23: Pappus’s theorem (affine version).
图23.23:Pappus定理（仿射版本）。
parallel, the points a,b,a0,b0 are coplanar. Thus, either ha,a0i and hb,b0i are parallel, or they have some intersection d. We consider the second case where they intersect, leaving the other case as an easy exercise. Let f be the dilatation of center d such that f(a) = a0. By Proposition 23.11, we get f(b) = b0. If f(c) = c00, again by Proposition 23.11 twice, the
平行，点A，B，A0，B0是共面的。因此，要么ha，a0i和hb，b0i是平行的，要么它们有一些交点d。我们考虑它们相交的第二种情况，将另一种情况留作一个简单的练习。设f为中心d的膨胀，使f（a）=a0。根据23.11号提案，我们得到f（b）=b0。如果f（c）=c00，再根据23.11号提案，两次
hfollows thatlines0 0hb,care parallel. Thus, the linesi andc00 =hb0c,c0. Indeed, recall that00i are parallel, and the lineshb,ci andhha,cb0,ci0iandare identical, and similarly the linesare parallel, and similarlyha0,c00i are parallel. From this itha,ci and a ,c i	
沿着这条线走，注意平行。因此，线si和c00=hb0c，c0。事实上，记得00i是平行的，线SHb，ci和hha，cb0，ci0i是相同的，同样的线是平行的，同样的，hhha，c0i是平行的。从这一点上来说，伊莎，CI和A，C I
ha0,c00i and ha0,c0i are identical. Since a0c0 and b0c0 are linearly independent, these lines have a unique intersection, which must be c00 = c0.
HA0、C00i和HA0、C0i是相同的。由于a0c0和b0c0是线性无关的，所以这些线有一个唯一的交点，必须是c00=c0。
The direction where it is assumed that the lines ha,a0i, hb,b0i and hc,c0i, are either parallel or concurrent is left as an exercise (in fact, the proof is quite similar). 
假设线ha、a0i、hb、b0i和hc、c0i是平行的或同时存在的方向作为练习（事实上，证明是非常相似的）。
Desargues’s theorem is illustrated in Figure 23.24.
德沙格定理如图23.24所示。
There is a fancier version of Desargues’s theorem, but it is easier to prove it using projective geometry. It should be noted that in axiomatic presentations of projective geometry, Desargues’s theorem is related to the associativity of the ground field K (in the present case, K = R). Also, Desargues’s theorem yields a geometric characterization of the affine dilatations. An affine dilatation f on an affine space E is a bijection that maps every line D to a line f(D) parallel to D. We leave the proof as an exercise.
德沙格定理有一个更高级的版本，但是用射影几何来证明它更容易。应该注意的是，在射影几何的公理表示中，Desargues定理与地面场k的关联性有关（在本例中，k=r）。此外，德沙格定理给出了仿射扩张的几何特征。仿射空间e上的仿射展开式f是一个双射，它把每一条d线映射到平行于d的f（d）线上。我们把证明留作练习。

Figure 23.24: Desargues’s theorem (affine version).
图23.24：德沙格定理（仿射版）。
23.10	Affine Hyperplanes
23.10仿射超平面
We now consider affine forms and affine hyperplanes. In Section 23.5 we observed that the set L of solutions of an equation
我们现在考虑仿射形式和仿射超平面。在第23.5节中，我们观察到一个方程的解集l
ax + by = c
ax+by=c
is an affine subspace of A2 of dimension 1, in fact, a line (provided that a and b are not both null). It would be equally easy to show that the set P of solutions of an equation
是维度1的a2的仿射子空间，实际上是一行（前提是a和b都不是空的）。同样容易证明方程的解集p
ax + by + cz = d
ax+by+cz=d
is an affine subspace of A3 of dimension 2, in fact, a plane (provided that a,b,c are not all null). More generally, the set H of solutions of an equation
是维度2的a3的仿射子空间，实际上是一个平面（前提是a、b、c不是全部为空）。更一般地说，一个方程的解的集合h
λ1x1 + ··· + λmxm = µ
λ1x1+····+λmxm=μ
is an affine subspace of Am, and if λ1,...,λm are not all null, it turns out that it is a subspace of dimension m − 1 called a hyperplane. We can interpret the equation
是a m的仿射子空间，如果λ1，…，λm不都为空，则证明它是维度m-1的子空间，称为超平面。我们可以解释这个方程
λ1x1 + ··· + λmxm = µ
λ1x1+····+λmxm=μ
in terms of the map f : Rm → R defined such that
根据图f:rm→r，定义如下：
f(x1,...,xm) = λ1x1 + ··· + λmxm − µ
f（x1，…，xm）=λ1x1+····+λmxm−礹
for all (x1,...,xm) ∈ Rm. It is immediately verified that this map is affine, and the set H of solutions of the equation
对于所有（x1，…，xm）∈rm。立即证明该映射是仿射的，并且方程的解集h
λ1x1 + ··· + λmxm = µ
λ1x1+····+λmxm=μ
23.10. AFFINE HYPERPLANES is the null set, or kernel, of the affine map f : Am → R, in the sense that
第23.10条。仿射超平面是仿射映射f:am→r的空集或核，在这个意义上
H = f−1(0) = {x ∈ Am | f(x) = 0},
h=f−1（0）=x∈am f（x）=0，
where x = (x1,...,xm).
其中x=（x1，…，xm）。
Thus, it is interesting to consider affine forms, which are just affine maps f : E → R from an affine space to R. Unlike linear forms f∗, for which Kerf∗ is never empty (since it always contains the vector 0), it is possible that f−1(0) = ∅ for an affine form f. Given an affine map f : E → R, we also denote f−1(0) by Kerf, and we call it the kernel of f. Recall that an (affine) hyperplane is an affine subspace of codimension 1. The relationship between affine hyperplanes and affine forms is given by the following proposition.
因此，考虑仿射形式是很有趣的，它只是仿射空间到r的仿射映射f:e→r。与线性形式f不同，对于这种形式，切口从不为空（因为它总是包含向量0），对于仿射形式f，f−1（0）=→r，我们也用切口表示f−1（0），我们称之为f的核心。回想一下，（仿射）超平面是余维1的仿射子空间。仿射超平面与仿射形式之间的关系由以下命题给出。
Proposition 23.14. Let E be an affine space. The following properties hold:
提案23.14.设e为仿射空间。以下属性保留：
(a)	Given any nonconstant affine form f : E → R, its kernel H = Kerf is a hyperplane.
对于任何非常量仿射形式f:e→r，其核心h=kerf是超平面。
(b)	For any hyperplane H in E, there is a nonconstant affine form f : E → R such that H = Kerf. For any other affine form g: E → R such that H = Kerg, there is some λ ∈ R such that g = λf (with λ = 06 ).
对于e中的任何超平面h，都有一个非恒定的仿射形式f:e→r，这样h=kerf。对于任何其他的仿射形式g:e→r，例如h=kerg，有一些λ∈r，例如g=λf（带有λ=06）。
(c)	Given any hyperplane H in E and any (nonconstant) affine form f : E → R such that H = Kerf, every hyperplane H0 parallel to H is defined by a nonconstant affine form g such that g(a) = f(a) − λ, for all a ∈ E and some λ ∈ R.
给定e中的任意超平面h和任意（非常数）仿射形式f:e→r，使得h=kerf，每个平行于h的超平面h0都由非常数仿射形式g定义，这样g（a）=f（a）−λ，对于所有a∈e和一些λ∈r。
Proof. The proof is straightforward, and is omitted. It is also given in Gallier [71].	
证据。证据很直接，被省略了。加利尔文[71]也给出了这一点。
When E is of dimension n, given an affine frame (a0,(u1,...,un)) of E with origin a0, recall from Definition 23.5 that every point of E can be expressed uniquely as x = a0 +x1u1 +···+xnun, where (x1,...,xn) are the coordinates of x with respect to the affine frame (a0,(u1,...,un)).
当e为n维数时，给定e的原点为a0的仿射帧（a0，（u1，…，un）），从定义23.5中回忆，e的每个点可以唯一地表示为x=a0+x1u1+······+xnun，其中（x1，…，xn）是x相对于仿射帧的坐标（a0，（u1，…，un））。
Also recall that every linear form f∗ is such that f∗(x) = λ1x1 + ··· + λnxn, for every x = x1u1 +···+xnun and some→− λ1,...,λn ∈ R. Since an affine form f : E → R satisfies the property f(a0 +x) = f(a0)+ f (x), denoting f(a0 +x) by f(x1,...,xn), we see that we have
还记得，每一个线性形式f是这样的：f（x）=λ1x1+·····+λnxn，对于每一个x=x1u1+······+xnun和一些·−λ1，…，λn∈r。由于仿射形式f:e→r满足性质f（a0+x）=f（a0）+f（x），用f（x1，…，xn表示f（a0+x），我们看到我们已经
f(x1,...,xn) = λ1x1 + ··· + λnxn + µ,
f（x1，…，xn）=λ1x1+····+λnxn+μ，
where µ = f(a0) ∈ R and λ1,...,λn ∈ R. Thus, a hyperplane is the set of points whose coordinates (x1,...,xn) satisfy the (affine) equation
式中，μ=f（a0）∈r和λ1，…，λn∈r。因此，超平面是坐标（x1，…，xn）满足（仿射）方程的点集。
λ1x1 + ··· + λnxn + µ = 0.
λ1x1+····+λnxn+μ=0.
23.11	Intersection of Affine Spaces
23.11仿射空间的交集
In this section we take a closer look at the intersection of affine subspaces. This subsection can be omitted at first reading.
在本节中，我们将更详细地了解仿射子空间的交集。本小节可在第一次阅读时省略。
First, we need a result of linear algebra. Given a vector space E and any two subspaces M
首先，我们需要一个线性代数的结果。给定向量空间e和任意两个子空间m
	→	⊕N and in2 : N → M⊕N
→n和in2:n→m_n
map fromof the inclusion map fromand thus, injectionsMand+NN, there are several interesting linear maps. We have the canonical injectionsandMj:∩NN→tofM:N+MNwith∩, the canonical injectionsMN ∩in2. Then, we have the mapsM	N and g: M	inN1 : MM f M+ g: M ∩ N → M ⊕iN: M, and→,
包含图From的映射，因此，InjectionsMand+nn，有几个有趣的线性映射。我们有标准注射剂和mj：n n→tofm:n+mn和，标准注射剂mn in2。然后，我们有mapsm n和g:m inn1:mm f m+g:m n→m in:m，和→，
	→N to⊕M with in1, and∩	→g is the composition of the inclusion⊕N, where f is the composition
→n to m with in1，and→g is the composition of the inclusion n，其中f is the composition
i − j: M ⊕ N → M + N.
i−j:m n→m+n。
Proposition 23.15. Given a vector space E and any two subspaces M and N, with the definitions above,
提案23.15。给定一个向量空间e和任意两个子空间m和n，以及上面的定义，
0 −→ M ∩ N −f+→g M ⊕ N −i−→j M + N −→ 0
0−→M N−F+→G M N−I−→J M+N−→0
Im(is a short exact sequence, which means thatf + g) = Ker(i − j). As a consequence, we have the Grassmann relationf + g is injective, i − j is surjective, and that
im（是一个短的精确序列，这意味着f+g）=ker（i-j）。因此，我们得到格拉斯曼关系式+G是内射的，I−J是外射的，并且
dim(M) + dim(N) = dim(M + N) + dim(M ∩ N).
尺寸（m）+尺寸（n）=dim（m+n）+尺寸（m n）。
Proof. It is obvious that i −, andj is surjective and thatv ∈ Ni. Then,(u) = j(iv() =u) =wfj∈(+vj)M)g, and thus, by definition of, as desired. The second part ofis injective. Assume that (∩ N. By definition of f andi andi −g,
证据。很明显，i−和j是主观性的，v∈ni。然后，（u）=j（iv（）=u）=wfj∈（+vj）m）g，因此，根据定义，根据需要。第二部分是注射剂。假设（n.根据f和i和i-g的定义，
j)(u + v) = 0, where u ∈ MN, such that j, there is some w ∈g(Mw)∩, and thus Im(f + g) = Ker(i − u = f(w) and v =
j）（u+v）=0，其中u∈mn，这样j，有一些w∈g（mw），因此im（f+g）=ker（i−u=f（w）和v=
the proposition follows from standard results of linear algebra (see Artin [7], Strang [165], or Lang [106]).	
这个命题来自线性代数的标准结果（见Artin[7]、Strang[165]或Lang[106]）。
We now prove a simple proposition about the intersection of affine subspaces.
我们现在证明一个关于仿射子空间交集的简单命题。
Proposition 23.16. Given any affine space E, for any two nonempty affine subspaces M and N, the following facts hold:
提案23.16。对于任意两个非空的仿射子空间m和n，对于任意仿射空间e，以下事实成立：
(1)	M ∩ N 6= ∅ iff →−ab ∈ −M→ + →−N for some a ∈ M and some b ∈ N.
m n 6=∅iff→−a b∈−−m→＋→−n，对于某些a∈m和一些b∈n。
(2)	M ∩−→N∩consists of a single point iff→−N = {0}. →−ab ∈ M−→ + →−N for some a ∈ M and some b ∈ N, and M
M−→N由单点iff→−N=0组成。对于一些a∈m和一些b∈n，和m
(3)	If S is the least affine subspace containing M and N, then →−S = −M→ + →−N + K→−ab (the vector space →−E is defined over the field K).
如果s是包含m和n的最小仿射子空间，则→−s=−m→+→−n+k→−ab（矢量空间→−e在字段k上定义）。
23.11. INTERSECTION OF AFFINE SPACES
11月23日。仿射空间的交集
Proof.−→(1) Pick any a ∈ M and any→−	b→−∈ N, which is possible, since M and N are nonempty.we have
证明。−→（1）选择任意a∈m和任意→−b→−n，这是可能的，因为m和n是非空的。
→−	, withfor some→−ac ∈a M∈ Mandand somebc ∈ N, and thus,b ∈ N. Thenab ∈→−abM=+−ax→N+. Conversely, assume that→−by, for some x ∈ M and
→−，对于一些→−ac∈a m∈m and和一些bc∈n，因此，b∈n.thenab∈→−abm=+−ax→n+。相反，假设→−by，对于某些x∈m和
some y ∈ N. But we also have	→−ab = ax−→ + −xy→ + →−yb,
一些y∈n，但我们也有→−ab=ax−→+xy→+yb，
[x,y], and since −yx→ = 2
[x，y]，并且由于−yx→=2
and thus we get 0 =(y,−1). Thus x also belongs tox−xy→∈ M→−yb+,→−∩ybxN−= 2, and→−bybN, that is,−, sinceMy∩is the barycenter of the weighted points (N−xy→N6= = 2∅being an affine subspace, it is closed under. →−by. Thus, b is the middle of the segmentb,2) and
因此我们得到0=（Y，−1）。因此x也属于tox−xy→∈m→−yb+、→yb x n−2，和→−bybn，即−，sincemy是加权点的重心（n−xy→n6＝2∅是仿射子空间，它在下面闭合。→−通过。因此，b是节段b，2）和
barycenters. Thus,
重心。因此，
(2)	Note that in general, if M ∩ N 6= ∅, then
注意，一般情况下，如果m n 6=∅，则
−−−−M ∩→N = −M→ ∩ →−N,
−−−M→N=−M→→−N，
because
因为
−−−−M ∩→N = {→−ab | a,b ∈ M ∩ N} = {→−ab | a,b ∈ M} ∩ {→−ab | a,b ∈ N} = −M→ ∩ →−N.
−−−m→n=→−a b a，b∈m n→−ab a，b∈m→−ab a，b∈n=−m→→−n。
Since M ∩ N = c + −−−−M ∩→N for any c ∈ M ∩ N, we have
因为m n=c+−−−−m→n对于任何c∈m n，我们有
	M ∩ N = c + −M→ ∩ →−N	for any c ∈ M ∩ N.
m n=c+−m−n表示任意c m n。
This fact together with what we proved in (1) proves (2).From this it follows that if M∩N 6= ∅, then M∩N consists of a single point iff −M→∩→−N = {0}.
这一事实连同我们在（1）中证明的事实证明（2），由此得出，如果m n 6=∅，那么m n由单点iff−m n 0组成。
(3)	This is left as an easy exercise.	
这是一个简单的练习。
Remarks:
评论：
(1)	aThe proof of Proposition 23.16 shows that if∈ M and all b ∈ N.	M ∩ N =6	∅, then →−ab ∈ −M→ + →−N for all
A.命题23.16的证明表明，如果∈m和所有b∈n.m n=6∅，那么→−ab∈−m→＋→−n代表所有
(2)	Proposition 23.16 implies that for any two nonempty affine subspaces	, if
命题23.16意味着对于任意两个非空仿射子空间，如果
, then M ∩ N consists of a single point. Indeed, if E = M
，则m n由一个点组成。实际上，如果e=m
part (2) of the proposition.ab ∈ E for all a ∈ M and all b ∈ N, and since M−→ ∩ →−N = {0}, the result follows from⊕ N, then
命题的第（2）部分，a b∈e表示所有a∈m和所有b∈n，由于m−→→−n=0，其结果如下n，则
We can now state the following proposition.
我们现在可以陈述以下命题。
Proposition 23.17. Given an affine space E and any two nonempty affine subspaces M and N, if S is the least affine subspace containing M and N, then the following properties hold:
提案23.17。给定一个仿射空间e和任意两个非空仿射子空间m和n，如果s是包含m和n的最小仿射子空间，则以下属性成立：
(1)	If M ∩ N = ∅, then
如果m n=直径，则
dim(M) + dim(N) < dim(E) + dim(−M→ + →−N)
尺寸（m）+尺寸（n）<尺寸（e）+尺寸（m→+N）
and dim(S) = dim(M) + dim(N) + 1 − dim(−M→ ∩ →−N).
和dim（s）=dim（m）+dim（n）+1−dim（−m→→−n）。
(2)	If M ∩ N 6= ∅, then
如果m n 6=直径，则
dim(S) = dim(M) + dim(N) − dim(M ∩ N).
尺寸=尺寸（m）+尺寸（n）-尺寸（m n）。
Proof. The proof is not difficult, using Proposition 23.16 and Proposition 23.15, but we leave it as an exercise.	
证据。使用23.16号和23.15号提案，证明并不困难，但我们将其作为练习。