第二十四章
Embedding an Affine Space in a Vector Space
在向量空间中嵌入仿射空间
24.1	The “Hat Construction,” or Homogenizing
24.1“帽结构”或均质化
For all practical purposes, most geometric objects, including curves and surfaces, live in affine spaces. A disadvantage of the affine world is that points and vectors live in disjoint universes. It is often more convenient, at least mathematically, to deal with linear objects (vector spaces, linear combinations, linear maps), rather than affine objects (affine spaces, affine combinations, affine maps). Actually, it would also be advantageous if we could manipulate points and vectors as if they lived in a common universe, using perhaps an extra bit of information to distinguish between them if necessary.
在所有实际应用中，大多数几何对象，包括曲线和曲面，都生活在仿射空间中。仿射世界的一个缺点是点和向量生活在不相交的宇宙中。至少在数学上，处理线性对象（向量空间、线性组合、线性映射）比处理仿射对象（仿射空间、仿射组合、仿射映射）更方便。事实上，如果我们能像生活在一个共同的宇宙中一样操纵点和向量，在必要的时候使用额外的信息来区分它们，这也是有利的。
Such a “homogenization” (or “hat construction”) can be achieved. As a matter of fact, such a homogenization of an affine space and its associated vector space will be very useful to define and manipulate rational curves and surfaces. Indeed, the hat construction yields a canonical construction of the projective completion of an affine space. It also leads to a very elegant method for obtaining the various formulae giving the derivatives of a polynomial curve, or the directional derivatives of polynomial surfaces. However, these formulae are not needed here. Thus we omit this topic, referring the readers to Gallier [71].
这样的“同质化”（或“帽子结构”）可以实现。实际上，仿射空间及其相关向量空间的这种均匀化对于定义和操纵有理曲线和曲面是非常有用的。实际上，hat构造生成仿射空间射影完备的规范构造。它还引出了一种非常优雅的方法，用于获得给出多项式曲线导数或多项式曲面方向导数的各种公式。然而，这里不需要这些公式。因此，我们省略了这一主题，将读者引向Gallier[71]。
This chapter proceeds as follows. First, the construction of a vector space Eb in which both E and →−E are embedded as (affine) hyperplanes is described. It is shown how affine frames in E become bases in Eb. It turns out that Eb is characterized by a universality property: Affine maps to vector spaces extend uniquely to linear maps. As a consequence, affine maps between affine spaces E and F extend to linear maps between Eb and Fb.
本章内容如下。首先，描述了向量空间eb的构造，其中e和→−e都嵌入（仿射）超平面。它显示了e中的仿射帧如何成为eb中的基。结果表明，电子束具有普适性特征：矢量空间的仿射映射唯一地扩展到线性映射。因此，仿射空间e和f之间的仿射映射扩展到eb和fb之间的线性映射。
Let us first explain how to distinguish between points and vectors practically, using what amounts to a “hacking trick.” Then, we will show that such a procedure can be put on firm mathematical grounds.
让我们先解释一下如何在实际中区分点和向量，使用相当于“黑客把戏”的方法。然后，我们将展示这样一个过程可以建立在坚实的数学基础上。
Assume that we consider the real affine space E of dimension 3, and that we have some
假设我们考虑维3的实仿射空间e，我们有一些
741
七百四十一
affine frame (a0,(v1,v2,v2)). With respect to this affine frame, every point x ∈ E is repre-→− sented by its coordinates (x1,x2,x3), where a = a0 + x1v1 + x2v2 + x3v3. A vector u ∈ E is also represented by its coordinates (u1,u2,u3) over the basis (v1,v2,v2). One way to distinguish between points and vectors is to add a fourth coordinate, and to agree that points are represented by (row) vectors (x1,x2,x3,1) whose fourth coordinate is 1, and that vectors are represented by (row) vectors (v1,v2,v3,0) whose fourth coordinate is 0. This “programming trick” actually works very well. Of course, we are opening the door for strange elements such as (x1,x2,x3,5), where the fourth coordinate is neither 1 nor 0.
仿射帧（a0，（v1，v2，v2））。对于这个仿射框架，每个点x∈e由其坐标（x1，x2，x3）表示，其中a=a0+x1v1+x2v2+x3v3。矢量u∈e也由其在基（v1，v2，v2）上的坐标（u1，u2，u3）表示。区分点和矢量的一种方法是添加第四个坐标，并同意点由第四个坐标为1的（行）矢量（x1，x2，x3,1）表示，矢量由第四个坐标为0的（行）矢量（v1，v2，v3,0）表示。这个“编程技巧”实际上非常有效。当然，我们打开了一些奇怪元素的门，比如（x1，x2，x3，5），其中第四个坐标既不是1也不是0。
The question is, can we make sense of such elements, and of such a construction? The answer is yes. We will present a construction in which an affine space E, is embedded in a vector space Eb, in which →−E is embedded as a hyperplane passing through the origin, and E itself is embedded as an affine hyperplane, defined as ω−1(1), for some linear form ω: Eb → R. In the case of an affine space→− E of dimension 2, we can think of Eb as the vector space R3 of dimension 3 in which E corresponds to the xy-plane, and E corresponds to the plane of equation z = 1, parallel to the xy-plane and passing through the point on the z-axis of coordinates (0,0,1). The construction of the vector space Eb is presented in some detail in Berger [11]. Berger explains the construction in terms of vector fields. We prefer a more geometric and simpler description in terms of simple geometric transformations, translations, and dilatations.
问题是，我们能理解这样的元素和这样的结构吗？答案是肯定的。我们将提出一种构造，其中仿射空间e嵌入到向量空间eb中，其中→−e嵌入为穿过原点的超平面，e本身嵌入为仿射超平面，定义为ω−1（1），对于某种线性形式ω：eb→r。对于仿射空间，则定义为ω−1（1）。速度→−e在尺寸2中，我们可以把eb看作是尺寸3的向量空间r3，其中e对应于xy平面，e对应于方程z=1的平面，平行于xy平面，并通过坐标z轴上的点（0,0,1）。向量空间eb的构造在Berger[11]中有详细介绍。Berger解释了矢量场的构造。我们更喜欢用简单的几何变换、翻译和扩张来描述更为几何和简单的描述。
Remark: Readers with a good knowledge of geometry will recognize the first step in embedding an affine space into a projective space. We will also show that the homogenization Eb of an affine space E,, satisfies a universal property with respect to the extension of affine maps to linear maps. As a consequence, the vector space Eb is unique up to isomorphism, and its actual construction is not so important. However, it is quite useful to visualize the space Eb, in order to understand well rational curves and rational surfaces.
注：具有良好几何知识的读者将认识到在射影空间中嵌入仿射空间的第一步。我们还将证明仿射空间e，，的均匀化eb满足仿射映射到线性映射扩展的一个普遍性质。因此，矢量空间eb具有独特的同构性，其实际构造并不重要。然而，为了更好地理解有理曲线和有理曲面，可视化空间eb是非常有用的。
As usual, for simplicity, it is assumed that all vector spaces are defined over the field R of real numbers, and that all families of scalars (points and vectors) are finite. The extension to arbitrary fields and to families of finite support is immediate. We begin by defining two very simple kinds of geometric (affine) transformations. Given an affine space E,, every u ∈ →−E induces a mapping tu : E → E, called a translation, and defined such that for every a ∈ E. Clearly, the set of translations is a vector space isomorphic to
通常，为了简单起见，假设所有向量空间都定义在实数的r域上，并且所有标量族（点和向量）都是有限的。对任意域和有限支撑族的扩展是直接的。我们首先定义两种非常简单的几何（仿射）变换。给定一个仿射空间e，每一个u∈→−e诱导一个映射tu:e→e，称为翻译，并定义为每一个a∈e。显然，翻译集是一个向量空间同构于
E. Thus, we will use the same notation u for both the vector u and the translation tu. Given any point a and any scalar λ ∈ R, we define the mapping Ha,λ : E → E, called dilatation (or central dilatation, or homothety) of center a and ratio λ, and defined such that
e.因此，我们将对向量u和平移tu使用相同的符号u。给定任何点a和任何标量λ∈r，我们定义映射ha，λ：e→e，称为中心a和比率λ的扩张（或中心扩张，或同构），并定义如下：
Ha,λ(x) = a + λax,−→
ha，λ（x）=a+λax，−→
for every x ∈ E. We have Ha,λ(a) = a, and when−→λ = 06 and x 6= a, Ha,λ(x) is on the line defined by a and x, and is obtained by “scaling” ax by λ. The effect is a uniform dilatation (or contraction, if λ < 1). When λ = 0, Ha,0(x) = a for all x ∈ E, and Ha,0 is the constant affine map sending every point to a. If we assume λ = 16 , note that Ha,λ is never the identity, and since a is a fixed point, Ha,λ is never a translation.
对于每一个x∈e，我们有ha，λ（a）=a，当−→λ=06和x 6=a，ha，λ（x）在a和x定义的线上时，由λ“缩放”ax得到。效果是均匀的扩张（或收缩，如果λ<1）。当λ=0，ha，0（x）=a时，对于所有x∈e，ha，0是将每个点发送到a的常数仿射映射。如果假设λ=16，请注意，ha，λ绝不是同一性，并且由于a是固定点，ha，λ绝不是翻译。
We now consider the set Eb of geometric transformations from E to E, consisting of the union of the (disjoint) sets of translations and dilatations of ratio λ = 16 . We would like→− to give this set the structure of a vector space, in such a way that both E and E can be naturally embedded into Eb. In fact, it will turn out that barycenters show up quite naturally too!
我们现在考虑从e到e的几何变换集eb，它由（不相交的）平移集的并集和比率λ=16的扩张组成。我们希望→−给这个集合一个向量空间的结构，这样E和E都可以自然地嵌入到eb中。事实上，重心也会很自然地出现！
In order to “add” two dilatations Ha1,λ1 and Ha2,λ2, it turns out that it is more convenient to consider dilatations of the form Ha,1−λ, where λ = 06 . To see this, let us see the effect of such a dilatation on a point x ∈ E: We have
为了“加上”两个展开式Ha1，λ1和Ha2，λ2，结果表明考虑形式Ha，1−λ的展开更为方便，其中λ=06。为了看到这一点，让我们看看这种扩张对点x∈e的影响：我们有
Ha,1−λ(x) = a + (1 − λ)ax−→ = a + −ax→ − λ−ax→ = x + λxa.−→
ha，1−λ（x）=a+（1−λ）ax−→=a+−ax→−λ−ax→=x+λxa.−→
For simplicity of notation, let us denote Ha,1−λ by ha,λi. Then, we have
为了简化记法，让我们用ha，λi表示ha，1−λ。然后，我们得到
ha,λi(x) = x + λxa.−→
ha，λi（x）=x+λxa.−→
Remarks:
评论：
(1)	Note that Ha,1−λ(x) = Hx,λ(a).
注意，ha，1−λ（x）=hx，λ（a）。
(2)	Berger defines a map h: E → →−E as a vector field. Thus, each ha,λi can be viewed as the vector field x 7→ λxa−→. Similarly, a translation u can be viewed as the constant vector field x 7→ u. Thus, we could define Eb as the (disjoint) union of these two vector fields. We prefer our view in terms of geometric transformations. Then, since
Berger将地图h:e→→−e定义为矢量场。因此，可以将每个ha，λi视为向量场x 7→λxa−→。同样，一个平移u可以被看作是一个常数向量场x 7→u。因此，我们可以将eb定义为这两个向量场的（不相交）并集。我们更喜欢几何变换的观点。那么，自从
		and	,
而且，
if we want to define ha1,λ1i+b ha2,λ2i, we see that we have to distinguish between two cases:
如果我们要定义ha1，λ1i+b ha2，λ2i，我们必须区分两种情况：
(1)	λ1 + λ2 = 0. In this case, since
λ1+λ2=0.在这种情况下，因为
λ1xa−→1 + λ2xa−→2 = λ1xa−→1 − λ1xa−→2 = λ1a−−2→a1,
λ1xa−→1+λ2xa−→2=λ1xa−→1-λ1xa−→2=λ1a−2→a1，
we let
我们让
ha1,λ1i +b ha2,λ2i = λ1a−−2→a1,
ha1，λ1i+b ha2，λ2i=λ1a−2→a1，
where denotes the translation associated with the vector.
其中表示与向量关联的转换。
(2)	λ1 +λ2 = 06 . In this case, the points a1 and a2 assigned the weights λ1/(λ1 +λ2) and λ2/(λ1 + λ2) have a barycenter
λ1+λ2=06.在这种情况下，分配给权重λ1/（λ1+λ2）和λ2/（λ1+λ2）的点a1和a2具有重心。
,
，
such that
这样的话
Since	
自从
we let
我们让
,
，
the dilatation associated with the point b and the scalar λ1 + λ2.
与点B和标量λ1+λ2相关的膨胀。
	Given a translation defined by u and a dilatation ha,λi, since λ = 06	, we have
给定u定义的平移和扩张ha，λi，因为λ=06，我们得到
λxa−→ + u = λ(xa−→ + λ−1u),
λxa−→+u=λ（xa−→+λ−1u）
and so, letting b = a + λ−1u, since →−ab = λ−1u, we have
因此，假设b=a+λ−1u，因为→−ab=λ−1u，我们有
λxa−→ + u = λ(xa−→ + λ−1u) = λ(−xa→ + →−ab) = λ→−xb,
λxa−→+u=λ（xa−→+λ−1u）=λ（−xa→+ab）=λ→−xb，
and we let ha,λi +b u = ha + λ−1u,λi,
我们让ha，λi+b u=ha+λ−1u，λi，
the dilatation of center a + λ−1u and ratio λ.
中心A+λ−1u和比率λ的扩张。
The sum of two translations u and v is of course defined as the translation u + v. It is also natural to define multiplication by a scalar as follows:
两个翻译u和v的和当然定义为翻译u+v。自然地，定义一个标量的乘法如下：
µ · ha,λi = ha,λµi,
礹·ha，λi=ha，λ礹i，
and
和
where λu is the product by a scalar in
式中，λu是中标量的乘积
We can now use the definition of the above operations to state the following proposition, showing that the “hat construction” described above has allowed us to achieve our goal of embedding both E and →−E in the vector space Eb.
我们现在可以使用上述操作的定义来陈述以下命题，表明上述“帽结构”允许我们实现将e和→−e嵌入向量空间eb的目标。
Proposition 24.1. The set Eb consisting of the disjoint union of the translations and the dilatations Ha,1−λ = ha,λi, λ ∈ R,λ = 06 , is a vector space under the following operations of addition and multiplication by a scalar: If λ1 + λ2 = 0, then
提案24.1.由平移与扩张的不相交并合ha，1−λ=ha，λi，λ∈r，λ=06组成的集合eb是一个在下列标量加乘运算下的向量空间：如果λ1+λ2=0，那么
;
；
if λ1 + λ2 = 06	, then
如果λ1+λ2=06，则
,
，
	u +b v	=	u + v;
U+B V=U+V；
if µ 6= 0, then
如果μ6=0，则
µ · ha,λi = ha,λµi, 0 · ha,λi =	0;
μ·ha，λi=ha，λμi，0·ha，λi=0；
and
和
λ · u = λu.
λ·u=λu。
Furthermore, the map ω: Eb → R defined such that
此外，图ω：eb→r定义如下：
ω(ha,λi)	=	λ, ω(u)	=	0,
ω（ha，λi）=λ，ω（u）=0，
is a linear form, ω−1(0) is a hyperplane isomorphic to →−E under the injective linear map  such that i(u) = tu (the translation associated with u), and ω−1(1) is an affine
是线性形式，ω−1（0）是在注入线性映射下与→−e同构的超平面，因此i（u）=tu（与u相关的平移），ω−1（1）是仿射
hyperplane isomorphic towhere j(a) = ha,1i for everyE with directiona ∈ E. Finally, for everyi(→−E), under the injective affine mapa ∈ E, we have	j: E → Eb,
超平面同构Towhere j（a）=ha，1i，对于方向为∈e的Everye，最后，对于Everyi（→−e），在注入仿射映射a∈e下，我们得到j:e→eb，
.
.
Proof. The verification that Eb is a vector space is straightforward. The linear map mapping a vector u to the translation defined by u is clearly an injection i: →−E → Eb embedding →−E as an hyperplane in Eb. It is also clear that ω is a linear form. Note that
证据。验证eb是一个向量空间是很简单的。将向量u映射到由u定义的平移的线性映射显然是注入i：→−e→eb嵌入→−e作为eb中的超平面。很明显，ω是一个线性形式。注意
j(a + u) = ha + u,1i = ha,1i +b u,
j（a+u）=ha+u，1i=ha，1i+b u，
where u stands for the translation associated with the vector u, and thus j is an affine injection with associated linear map i. Thus, ω−1(1) is indeed an affine hyperplane isomorphic to E with direction, under the map j: E → Eb. Finally, from the definition of +b , for every a ∈ E and every u ∈ →−E, since
式中，u代表与向量u相关的平移，因此j是具有相关线性映射i的仿射注入。因此，ω−1（1）确实是在映射j:e→eb下与e同构的仿射超平面。最后，从+b的定义来看，对于每一个a∈e和每一个u∈→−e，因为
i(u) +b λ · j(a) = u +b ha,λi = ha + λ−1u,λi,
i（u）+bλ·j（a）=u+b ha，λi=ha+λ−1u，λi，
whenarbitrary elementλ = 06	, we get any arbitraryhb,µi, µ 6= 0, by pickingv ∈ Ebλby picking= µ and uλ== 0µ→−ab. Thus,and u = v, and we get any
当双元素λ=06时，我们通过选择v∈ebλ通过选择=μ和uλ==0μ→−ab得到任意任意的hb，μi，μ6=0，因此，和u=v，我们得到
,
，
and since , we have
从那以后，我们
,
，
for every a ∈ E.	
对于每一个a∈e。

Figure 24.1: Embedding an affine space E, into a vector space Eb.
图24.1：在向量空间eb中嵌入仿射空间e。
Figure 24.1 illustrates the embedding of the affine space E into the vector space Eb, when E is an affine plane.
图24.1说明了当e是仿射平面时，仿射空间e嵌入向量空间eb。
Note that Eb is isomorphic to →−E ∪ (E × R∗). Intuitively, we can think of Eb as a stack of parallel hyperplanes, one for each λ, a little bit like an infinite stack of very thin pancakes! There are two privileged pancakes: one corresponding to E, for λ = 1, and one corresponding to →−E, for λ = 0.
请注意，eb与→−e（e×r）同构。直观地说，我们可以把eb看作一堆平行超平面，每一个λ一个，有点像一堆无限薄的薄煎饼！有两个特权煎饼：一个对应于e，对于λ=1，另一个对应于→−e，对于λ=0。
From now on, we will identify j(E) and E, and  and →−E. We will also write λa instead of ha,λi, which we will call a weighted point, and write 1a just as a. When we want to be more precise, we may also write ha,1i as a. In particular, when we consider the homogenized version Ab of the affine space A associated with the field R considered as an
从现在开始，我们将识别j（e）和e，以及→−e。我们还将写出λa而不是ha，λi，我们称之为加权点，并将1a写成a。当我们想要更精确的时候，我们也可以把ha，1i写成a。特别是当我们考虑仿射的同质化版本ab时与字段r关联的空间a被视为
affine space, we write λ for hλ,1i, when viewing λ as a point in both A and Ab, and simply λ, when viewing λ as a vector in R and in Ab. As an example, the expression 2 + 3 denotes the real number 5, in A, (2 + 3)/2 denotes the midpoint of the segment , which can be denoted by 2.5, and 2+3 does not make sense in A, since it is not a barycentric combination. However, in Ab, the expression 2 + 3 makes sense: It is the weighted point. Then, in view of the fact that
在仿射空间中，当把λ视为a和ab中的一个点时，我们为hλ，1i写出λ，当把λ视为r和ab中的一个矢量时，我们只写出λ。例如，表达式2+3表示实数5，在a中，（2+3）/2表示段的中点，可以用2.5和2+3表示。在A中没有意义，因为它不是重心组合。然而，在ab中，表达式2+3是有意义的：它是加权点。那么，鉴于
ha + u,1i = ha,1i +b u,
ha+u，1i=ha，1i+b u，
and since we are identifying a + u with ha + u,1i (under the injection j), in the simplified notation the above reads as a + u = a +b u. Thus, we go one step further, and denote a +b u by a + u. However, since ha,λi +b u = ha + λ−1u,λi,
由于我们将a+u与ha+u，1i（在注入j下）进行识别，在简化的符号中，上述内容读作a+u=a+b u。因此，我们更进一步，用a+u表示a+b u。但是，由于ha，λi+b u=ha+λ−1u，λi，
we will refrain from writing λa +b u as λa + u, because we find it too confusing. From Proposition 24.1, for every a ∈ E, every element of Eb can be written uniquely as u +b λa. We also denote λa + (b −µ)b
我们将避免将λa+b u写成λa+u，因为我们发现它太令人困惑了。从命题24.1可以看出，对于每一个a∈e，e b的每一个元素都可以唯一地写成u+bλa。我们也表示λa+（b−μ）b。
by λa −b µb.
通过λa−bμb。
We can now justify rigorously the programming trick of the introduction of an extra coordinate to distinguish between points and vectors. First, we make a few observations. Given any family (ai)i∈I of points in E, and any family (λi)i∈I of scalars in R, it is easily shown by induction on the size of I that the following holds:
我们现在可以严格证明引入额外坐标来区分点和向量的编程技巧。首先，我们做了一些观察。给定e中点的任一族（ai）i∈i，r中标量的任一族（λi）i∈i，通过对i大小的归纳，可以很容易地表示如下：
(1) If Pi∈I λi = 0, then
（1）如果pi∈iλi=0，则
,
，
where
哪里
X−−−−−→ X −→ λiai = λibai
x−−−→x−→λiai=λibai
	i∈I	i∈I
I∈I I∈I
for any b ∈ E, which, by Proposition 23.1, is a vector independent of b, or (2) If Pi∈I λi = 06	, then
对于任何b∈e，根据23.1，它是独立于b的向量，或者（2）如果pi∈iλi=06，那么
.
.
Thus, we see how barycenters reenter the scene quite naturally, and that in Eb, we can make sense ofh	i Pi∈Ihai,λii, regardless of the value of−1(1), and thus it is a point. WhenPi∈I λi. When Pi∈I λi = 1P, the elementi∈I λi = 0,
因此，我们可以很自然地看到重心是如何重新进入场景的，而在eb中，我们可以理解h i pi∈ihai，λii，而不考虑−1（1）的值，因此它是一个点。when pi∈iλi.当pi∈iλi=1p时，元素i∈iλi=0，
P ai,λi belongs to the hyperplane ω
p ai，λi属于超平面ω
the linear combination of pointsi∈I	Pi∈ λiai is a vector, and when I = {1,...,n}, we allow
点si∈i pi∈λiai的线性组合是一个向量，当i=1，…，n时，我们允许
I
我
ourselves to write
我们自己写
λ1a1 +b ··· +b λnan,
λ1a1+b····+bλnan，
where some of the occurrences of + can be replaced by	, as
其中一些出现的+可以替换为，例如
λ1a1 + ··· + λnan,
λ1a1+····+λnan，
where the occurrences of −b (if any) are replaced by −.
其中−b（如果有）的出现被−替换。
In fact, we have the following slightly more general property, which is left as an exercise.
事实上，我们有以下稍微更一般的属性，作为练习。
Proposition 24.2. Given any affine space E,, for any family (ai)i∈I of points in E, any family (λi)i∈I of scalars in R, and any family (vj)j∈J of vectors in →−E, with I ∩ J = ∅, the following properties hold:
提案24.2.给定任意仿射空间e，，对于任意族（ai）i∈i中的点，任意族（λi）i∈i中的标度r，任意族（vj）j∈j中的向量→−e，具有i j∅的性质如下：
(1)	If Pi∈I λi = 0, then
如果pi∈iλi=0，则
,
，
where
哪里
X−−−−−→ X −→ λiai = λibai
x−−−→x−→λiai=λibai
	i∈I	i∈I
I∈I I∈I
for any b ∈ E, which, by Proposition 23.1, is a vector independent of b, or
对于任何b∈e，根据23.1，它是独立于b的向量，或
(2)	If Pi∈I λi = 06	, then
如果pi∈iλi=06，则
.
.
Proof. By induction on the size of I and the size of J.	
证据。通过归纳I的大小和J的大小。
The above formulae show that we have some kind of extended barycentric calculus. Operations on weighted points and vectors were introduced by H. Grassmann, in his book published in 1844! This calculus will be helpful in dealing with rational curves.
上面的公式表明我们有某种扩展的重心微积分。在1844年出版的书中，H.Grassmann介绍了加权点和向量的运算。这种计算方法将有助于处理有理曲线。
24.2	Affine Frames of E and Bases of Eb
24.2 e的仿射框架和eb的基
There is also a nice relationship between affine frames in E, and bases of Eb, stated in the following proposition.
在e中的仿射框架和eb的基之间也有一个很好的关系，如下所述。
Proposition 24.3. Given any affine space	E,, for any affine frame ,  for E, the family  is a basis for Eb, and for any affine frame
提案24.3.对于任意仿射空间e，对于任意仿射框架，对于e，族是eb和任意仿射框架的基础。
(a0,...,am) for E, the family (a0,...,am) is a basis for Eb. Furthermore, given any element hx,λi ∈ Eb, if
（a0，…，am）对于e，家庭（a0，…，am）是eb的基础。此外，给定任何元素hx，λi∈eb，如果

over the affine frame , then the coordinates of hx,λi over the basis
在仿射框架上，然后是Hx的坐标，在基上的λi
 are
是
(λx1,...,λxm,λ).
（λx1，…，λxm，λ）。
For any vector v ∈ →−E, if
对于任何向量v∈→−e，如果


24.2. AFFINE FRAMES OF E AND BASES OF Eˆ
24.2。e的仿射框架和e_的基
over the basis , then over the basis , the coordinates of v are
在基础上，然后在基础上，v的坐标是
(v1,...,vm,0).
（v1，…，vm，0）。
For any element ha,λi, where λ = 06 , if the barycentric coordinates of a w.r.t. the affine basis (a0,...,am) in E are (λ0,...,λm) with λ0 +···+λm = 1, then the coordinates of ha,λi w.r.t. the basis (a0,...,am) in Eb are
对于任何元素ha，λi，其中，λ=06，如果w.r.t.的重心坐标，e中的仿射基（a0，…，am）是（λ0，…，λm）且λ0+···+λm=1，那么ha，λi w.r.t.eb中的基（a0，…，am）是
(λλ0,...,λλm).
（λ0，…，λm）。
If a vector v ∈ →−E is expressed as
如果向量v∈→−e表示为
,
，
with respect to the affine basis (a0,...,am) in E, then its coordinates w.r.t.	the basis
关于e中的仿射基（a0，…，am），则其坐标为w.r.t.基
(a0,...,am) in Eb are
（a0，…，am）在eb中是
(−(v1 + ··· + vm),v1,...,vm).
（−（v1+····+vm），v1，…，vm）。
Proof. We sketch parts of the proof, leaving the details as an exercise. Figure 24.2 shows the basis () corresponding to the affine frame (a0,a1,a2) in E.
证据。我们画出部分证据，把细节留作练习。图24.2显示了e中仿射帧（a0，a1，a2）对应的基（）。

Figure 24.2: The affine frame (a0,a1,a2) of E and the basis (.
图24.2:e的仿射框（a0，a1，a2）和基（.
If we assume that we have a nontrivial linear combination
假设我们有一个非平凡的线性组合
,
，
if µ = 06	, then we have
如果μ=06，那么我们有
,
，
which is never null, and thus, µ = 0, but since () is a basis of →−E, we must also have λi = 0 for all i,1 ≤ i ≤ m.
它从不为空，因此，μ=0，但由于（）是→−e的基础，因此我们也必须对所有i都有λi=0，1≤i≤m。
Given any element hx,λi ∈ Eb, if
给定任何元素hx，λi∈eb，如果

over the affine frame (, in view of the definition of +b , we have
在仿射框架上（，考虑到+b的定义，我们有
hx,λi = ha0 + x1a−−0→a1 + ··· + xma−−0a→m,λi
hx，λi=h0+x1a−0→a1+·····+xma−0a→m，λi
= ha0,λi +b λx1a−−0→a1 +b ··· +b λxm−−a0a→m,
=Ha0，λi+bλx1a−0→a1+b····+bλxm−a0a→m，
which shows that over the basis (, the coordinates of hx,λi are
这表明在基础上（，hx的坐标，λi是
(λx1,...,λxm,λ).
（λx1，…，λxm，λ）。

	If (x1,...,xm) are the coordinates of x w.r.t. the affine frame (	)) in
如果（x1，…，xm）是x w.r.t.中仿射帧（）的坐标
E, then (x1,...,xm,1) are the coordinates of x in Eb, i.e., the last coordinate is 1, and if u has coordinates (u1,...,um) with respect to the basis (, then u has coordinates (u1,...,um,0) in Eb, i.e., the last coordinate is 0. Figure 24.3 shows the affine frame (a0,a1,a2) in E viewed as a basis in Eb.
e，那么（x1，…，xm，1）是eb中x的坐标，也就是说，最后一个坐标是1，如果u有关于基的坐标（u1，…，um），那么u在eb中有坐标（u1，…，um，0），也就是说，最后一个坐标是0。图24.3显示了作为eb基础的e中的仿射帧（a0，a1，a2）。

Figure 24.3: The basis (a0,a1,a2) in Eb.
图24.3:eb中的基础（a0、a1、a2）。
24.3. ANOTHER CONSTRUCTION OF Eˆ
24.3。E_的另一个结构
Now that we have defined Eb and investigated the relationship between affine frames in E and bases in Eb, we can give another construction of a vector space F from E and →−E that will allow us to “visualize” in a much more intuitive fashion the structure of Eb and of its operations +b and ·.
既然我们已经定义了e b并研究了e中仿射帧与eb中碱基之间的关系，我们可以给出从e到→−e的向量空间f的另一种构造，它将使我们以更直观的方式“可视化”eb及其操作的结构+b和···。
24.3	Another Construction of Eb
24.3电子束的另一种结构
One would probably wish that we could start with this construction of F first, and then define Eb using the isomorphism defined below. Unfortunately, we first need the vector space structure on E to show that Ω is linear!
有人可能希望我们可以先从F的构造开始，然后使用下面定义的同构定义eb。不幸的是，我们首先需要E上的向量空间结构来显示Ω是线性的！
Definition 24.1. Given any affine space E,, we define the vector space F as the direct sum →−E ⊕R, where R denotes the fieldF →−R⊕considered as a vector space (over itself). Denoting∈ F the unit vector in by 1, since = E R, every vector v can be written as v = u+λ1, for some unique u ∈ E and some unique λ ∈ R. Then, for any choice of an origin Ω1 in E, we define the map Ω:b Eb → F, as follows:
定义24.1.对于任意仿射空间e，我们将向量空间f定义为直接和→−e r，其中r表示字段f→−r被视为向量空间（在其自身上）。用1表示单位向量∈f，由于=e r，每一个向量v都可以写成v=u+λ1，对于某些唯一的u∈e和一些唯一的λ∈r，那么，对于e中的原点Ω1的任何选择，我们定义了图Ω：b eb→f，如下：
		∈ E and λ = 06	;
∈e和λ=06；
.
.
The idea is that, once again, viewing	as an affine space under its canonical structure, E is embedded in F as the hyperplane H = 1 + E, with direction	, the hyperplane →−E in
我们的想法是，再一次把e看作是一个仿射空间，在它的正则结构下，e嵌入f中，作为超平面h=1+e，有方向，超平面→−e嵌入
F. Then, every point a ∈ E is in bijection with the point A = 1 + Ω1a, in the hyperplane H. If we denote the origin 0 of the canonical affine space F by Ω, the map Ω maps a pointb ha,λi ∈ E to a point inF F, as follows: ) is the point on the line passing through both→− the origin Ω of and the point A = 1 + Ω1a in the hyperplane H = 1 + E, such that
f.那么，在超平面h中，每个点a∈e都是双射的，点a=1+Ω1a。如果我们用Ω来表示正则仿射空间f的原点0，那么mapΩ将A点b ha，λi∈e映射到一个点inf f，如下所示：）是通过这两个点的直线上的点→−原点Ω。超平面h=1+e中的点a=1+Ω1a，这样
.
.
The following proposition shows that Ω is an isomorphism of vector spaces.
下面的命题表明，Ω是向量空间的同构。
Proposition 24.4. Given any affine space (E,→−E), for any choice Ω1 of an origin in E, the map Ω:b Eb → F is a linear isomorphism between Eb and the vector space F of Definition 24.1. The inverse of Ωb is given by
提案24.4.给定任意仿射空间（e，→−e），对于e中原点的Ω1的任何选择，mapΩ：b eb→f是eb与定义为24.1的向量空间f之间的线性同构。Ωb的倒数由下式得出：
; .
；
Proof. It is a straightforward verification. We check that Ω is invertible, leaving the verifi-b cation that it is linear as an exercise. We have
证据。这是一个简单的验证。我们检查了Ω是可逆的，剩下的校验B阳离子是线性的作为练习。我们有

and
和
,
，
and since Ω is the identity onb	→−E, we have shown that Ω ◦ Ω−1 = id, and	Ω = id. This shows that Ω is a bijection.b	
既然Ω是B→−E上的标识，我们已经证明了ΩΩ−1=ID，Ω=ID。这表明Ω是双射。b
Figure 24.4 illustrates the embedding of the affine space E into the vector space F, when E is an affine plane.
图24.4说明了当e是仿射平面时，仿射空间e嵌入向量空间f。

Figure 24.4: Embedding an affine space E, into a vector space F.
图24.4：在向量空间f中嵌入仿射空间e。
Proposition 24.4 gives a nice interpretation of the sum operation +b of Eb. Given two weighted points ha1,λ1i and ha2,λ2i, we have
提案24.4对电子商务的和运算+b给出了一个很好的解释。给定两个加权点ha1，λ1i和ha2，λ2i，我们得到
ha1,λ1i +b ha2,λ2i = Ωb−1(Ω(b ha1,λ1i) + Ω(b ha2,λ2i)).
Ha1，λ1i+b Ha2，λ2i=Ωb−1（Ω（b Ha1，λ1i）+Ω（b Ha2，λ2i））。
The operation) has a simple geometric interpretation. If λ1 +λ2 = 06 , then find the points M1 and M2 on the lines passing through the origin Ω of−−→ F→and the points−−→
操作）具有简单的几何解释。如果λ1+λ2=06，则在穿过−→F→原点Ω的直线上找到点M1和M2，然后找到点−→
) and A2 = Ω(b a2) in the hyperplane H, such that ΩM1 = λ1Ω−−A1 and ΩM2 = λ2ΩA2, add the vectors Ω−−M→1 and , getting a point N such that Ω−−→N = −−ΩM→1 + Ω−−M→2, and consider the intersection G of the line passing through Ω and N with the hyperplane H. Then, G is the barycenter of A1 and A2 assigned the weights λ1/(λ1 +λ2) and λ2/(λ1 +λ2), and if g = Ωb−1(Ω−→G), then Ωb−1(Ω−−→N) = hg,λ1 + λ2i. See Figure 24.5.
）在超平面H中，A2=Ω（b a2），这样，Ωm 1=λ1Ω−a1和Ωm 2=λ2Ωa2，加上矢量Ω−m→1，得到一个点n，使得Ω−→n=−Ωm→1+Ω−m→2，并考虑通过Ω和n的线与超平面的交点g。e h.那么，g是分配重量为λ1/（λ1+λ2）和λ2/（λ1+λ2）的a1和a2的重心，如果g=Ωb−1（Ω−→g），则Ωb−1（Ω−→n）=hg，λ1+λ2i。见图24.5。
Instead of adding the vectors  and , we can take the middle N0 of the segment M1M2, and G is the intersection of the line passing through Ω and N0 with the hyperplane H as illustrated in Figure 24.5.
不用加向量和，我们可以取段m1m2的中间n0，g是穿过Ω和n0的线与超平面h的交点，如图24.5所示。
24.3. ANOTHER CONSTRUCTION OF Eˆ
24.3。E_的另一个结构


Figure 24.5: The geometric construction of Ω(b ha1,λ1i) + Ω(b ha2,λ2i) for λ1 + λ2 = 0.6
图24.5：λ1+λ2=0.6的Ω（b ha1，λ1i）+Ω（b ha2，λ2i）的几何结构
If λ1 + λ2 = 0, then ha1,λ1i +b ha2,λ2i is a vector determined as follows. Again, find the points M1 and M2 on the lines passing through the origin Ω of F and the points
如果λ1+λ2=0，则Ha1、λ1i+b Ha2、λ2i是如下确定的向量。同样，在穿过F原点Ω的直线上找到M1和M2点以及这些点
and A2 = Ω(b a2) in the hyperplane H, such that and, and add the vectors Ω−−M→1 and , getting a point N such that ΩN = ΩM1 + ΩM2. The desired vector is Ω−−→N, which is parallel to the line A1A2. Equivalently, let N0 be the middle of the segment M1M2, and the desired vector is 2Ω−−N→0. See Figure 24.6.
在超平面h中，a2=Ω（ba2），这样，and，并加上矢量Ω−m→1，得到点n，这样，Ωn=Ωm 1+Ωm2。所需的矢量为Ω−→N，与管线A1A2平行。等价地，让n0是段m1m2的中间，并且所需的向量是2Ω−n→0。见图24.6。
We can also give a geometric interpretation of ha,λi+u. Let) in the hyperplane H, let D be the line determined by A and u, let M1 be the point such that , and let M2 be the point such that Ω−−M→2 = u, that is, M2 = Ω+u. By construction, the line D is in the hyperplane H, and it is parallel to Ω−−M→2, so that D, M1, and M2 are coplanar. Then, add the vectors Ω−−M→1 and , getting a point N such that Ω−−→N = Ω−−M→1 + Ω−−M→2, and let G be the intersection of the line determined by Ω and N with the line D. If g = Ωb−1(Ω−→G), then,. Equivalently, if N0 is the middle of the segment M1M2, then G is the intersection of the line determined by Ω and N0, with the line D; see Figure 24.7.
我们还可以给出超平面h中h a，λi+u.let）的几何解释，设d为a和u确定的线，设m1为点，使m2为点，使Ω−−m→2=u，即m2=Ω+u。通过构造，d线在超平面h中，它是Parall。EL至Ω−m→2，使d、m1和m2共面。然后，加上矢量Ω−m→1，得到一个点n，使Ω−→n=Ω−m→1+Ω−m→2，并让g是由Ω和n确定的线与线d的交点。如果g=Ωb−1（Ω−→g），则，。同样，如果n0是段m1m2的中间，则g是由Ω和n0确定的线与线d的交点；见图24.7。
We now consider the universal property of Eb mentioned at the beginning of this section.
我们现在考虑本节开头提到的电子商务的普遍属性。

Figure 24.6: The geometric construction of Ω(b ha1,λ1i) + Ω(b ha2,λ2i) for λ1 + λ2 = 0.
图24.6：λ1+λ2=0时，Ω（b ha1，λ1i）+Ω（b ha2，λ2i）的几何结构。
24.4	Extending Affine Maps to Linear Maps
24.4将仿射映射扩展到线性映射
Roughly, the vector space Eb has the property that for any vector space →−F and any affine map f : E → →−F , there is a unique linear map  extending f : E → →−F . As a consequence, given two affine spaces E and F, every affine map f : E → F extends uniquely to a linear map fb: Eb → Fb. First, we define rigorously the notion of homogenization of an affine space.
大体上，向量空间eb具有以下性质：对于任何向量空间→−f和任何仿射映射f:e→→−f，都有一个唯一的线性映射扩展f:e→→−f。因此，在给定两个仿射空间e和f的情况下，每个仿射映射f:e→f唯一地扩展到一个线性映射fb:eb→fb。首先，我们严格定义了仿射空间的同质化概念。
Definition 24.2. Given any affine space	E,, a homogenization (or linearization) of
定义24.2.给定任意仿射空间e，，的均匀化（或线性化）
(E,→−E) is a triple hE,j,ωi, where E is a vector space,→− → E j:E →E → E→− is an injective affine map with associated injective linear map i: E , ω: R is a linear form such that ), and for every vector space F and every affine map f : E → F there is a unique linear map  extending f, i.e., f = fb◦ j, as in the following diagram:
（e，→−e）是一个三重He，j，ωi，其中e是一个向量空间，→–→e j:e→e→e→−是一个与之相关的内射线性映射的内射仿射映射i:e，ω：r是一个这样的线性形式），对于每个向量空间f和每个仿射映射f:e→f，都有一个唯一的线性映射扩展如下图所示：
j
J
E@@@@@@@@ / E fb
E@@@@@@@@@@/E FB
f
f
→−F
→−F
Thus, j(E) = ω−1(1) is an affine hyperplane with direction (0). Note that we could have defined a homogenization of an affine space (E, E), as a triple hE,j,Hi, where E is a vector space, H is an affine hyperplane in E, and j: E → E is an injective affine map such that j(E) = H, and such that the universal property stated above holds. However, Definition 24.2 is more convenient for our purposes, since it makes the notion of weight more evident.
因此，j（e）=ω−1（1）是一个方向为（0）的仿射超平面。注意，我们可以定义一个仿射空间（e，e）的同构，作为一个三重He，j，hi，其中e是一个向量空间，h是e中的仿射超平面，j:e→e是一个可注射的仿射映射，这样j（e）=h，并且上面所述的普遍性质成立。然而，定义24.2对于我们的目的来说更方便，因为它使重量的概念更加明显。
The obvious candidate for E is the vector space Eb that we just constructed. The next proposition will show that Eb indeed has the required extension property. As usual, objects
显然，e的候选者是我们刚刚构造的向量空间eb。下一个提议将表明电子商务确实具有所需的扩展属性。像往常一样，物体
24.4. EXTENDING AFFINE MAPS TO LINEAR MAPS


Figure 24.7: The geometric construction of ha,λi + u.
defined by a universal property are unique up to isomorphism. This property is left as an exercise.
Proposition 24.5. Given any affine space E,  and any vector space →−F , for any affine map f : E → →−F , there is a unique linear map   extending f such that

for all a ∈ E, all u ∈ →−E, and all λ ∈ R, where →−f is the linear map associated with f. In particular, when λ = 06 , we have
 .
Proof. Assuming that fb exists, recall that from Proposition 24.1, for every a ∈ E, every element of Eb can be written uniquely as u+b λa. By linearity of fband since fbextends f, we have
 .
If λ = 1, since   and a + u are identified, and since fbextends f, we must have
 ,
and thus ) for all u ∈ →−E. Then we have

which proves the uniqueness of f. On the other hand, the map f defined as above is clearly a linear map extending f.
	When λ = 06	, we have
 .

Proposition 24.5 shows that  , is a homogenization of E, . As a corollary, we obtain the following proposition.
Proposition 24.6. Given two affine spaces E and F and an affine map f : E → F, there is a unique linear map extending f, as in the diagram below,
f
	E	/ F
jj

Eb / Fb
fb
such that
 ,
for all a ∈ E, all u ∈ →−E, and all λ ∈ R, where →−f is the linear map associated with f. In particular, when λ = 06 , we have
 .
Proof. Consider the vector space 	and the affine map j ◦ f : E → Fb. By Proposition 24.5, there is a unique linear map f : E → F extending j ◦ f, and thus extending f.	 
Note that fb: Eb → Fb has the property that . More generally, since
 ,
the linear map fb is weight-preserving. Also observe that we recover f from fb, by letting λ = 1 in fb(u +b λa) = λf(a + λ−1u), that is, we have
 .

24.4。将仿射映射扩展到线性映射757

From a practical point of view, Proposition 24.6 shows us how to homogenize an affine map to turn it into a linear map between the two homogenized spaces. Assume that E and F are of finite dimension, that (a0,(u1,...,un)) is an affine frame of E with origin a0, and (b0,(v1,...,vm)) is an affine frame of F with origin b0. Then, with respect to the two bases (u1,...,un,a0) in Eb and (v1,...,vm,b0) in Fb, a linear map h: Eb → Fb is given by an
 从实践的角度来看，命题24.6向我们展示了如何使仿射映射同质化，使其成为两个同质化空间之间的线性映射。假设e和f是有限维的，（a0，（u1，…，un））是e的仿射框架，原点为a0，（b0，（v1，…，vm））是f的仿射框架，原点为b0。然后，对于eb中的两个碱基（u1，…，un，a0）和fb中的（v1，…，vm，b0），线性映射h:eb→fb由

\+ 1) matrix A. Assume that this linear map h is equal to the homogenized
 +1）矩阵A。假设该线性映射H等于均匀化

version f of an affine map f. Since
 仿射映射f的版本f。自

,
 ，

and since over the basis (u1,...,un,a0) in Eb, points are represented by vectors whose last coordinate is 1 and vectors are represented by vectors whose last coordinate is 0, the following properties hold.
 由于在eb的基（u1，…，un，a0）上，点由最后一个坐标为1的向量表示，而向量由最后一个坐标为0的向量表示，因此以下属性保持不变。

\1.    The last row of the matrix A = M(fb) with respect to the given bases is
 矩阵A=m（fb）相对于给定基的最后一行是

(0,0,...,0,1)
 （0,0，…，0,1）

with n occurrences of 0.
 n次出现0。

\2.    The last column of A contains the coordinates
 A的最后一列包含坐标

(µ1,...,µm,1)
 （μ1，…，μm，1）

of f(a0) with respect to the basis (v1,...,vm,b0).
 f（a0）的基础（v1，…，vm，b0）。

\3.    The submatrix of A obtained by deleting the last row and the last column is the matrix of the linear map →−f with respect to the bases (u1,...,un) and (v1,...,vm),
 通过删除最后一行和最后一列得到的a的子矩阵是线性映射的矩阵→−f关于基（u1，…，un）和（v1，…，vm）。

Finally, since
 最后，因为

,
 ，

given any x ∈ E and y ∈ F with coordinates (x1,...,xn,1) and (y1,...,ym, 1), for X =
 对于x，给定坐标（x1，…，xn，1）和（y1，…，ym，1）的x∈e和y∈f。=

(x1,...,xn,1)> and Y = (y1,...,ym,1)>, we have y = f(x) iff
 （x1，…，xn，1）>和y=（y1，…，ym，1）>，我们有y=f（x）iff

Y = AX.
 Y=最大值。

For example, consider the following affine map f : A2 → A2 defined as follows:
 例如，考虑如下定义的仿射映射f:a2→a2：

| y1    Y1 | =    = | ax1 + bx2 + µ1,    ax1+bx2+祄1， |
| -------- | ------ | -------------------------------- |
| y2    Y2 | =    = | cx1 + dx2 + µ2.    cx1+dx2+μ2。  |

The matrix of fbis
 联邦调查局的矩阵

 ,
 ，

CHAPTER 24. EMBEDDING AN AFFINE SPACE IN A VECTOR SPACE
 第24章。在向量空间中嵌入仿射空间

and we have
 我们有

 .
 .

In Eb, we have
 在电子商务中，我们有

 ,
 ，

which means that the homogeneous map fbis is obtained from f by “adding the variable of
 也就是说，通过“加上

| homogeneity   x3:”    同质性x3：“ |        |                                      |
| --------------------------------- | ------ | ------------------------------------ |
| y1    Y1                          | =    = | ax1 + bx2 + µ1x3,    ax1+bx2+礹1x3， |
| y2    Y2                          | =    = | cx1 + dx2 + µ2x3,    cx1+dx2+礹2x3， |
| y3    Y3                          | =    = | x3.    X3。                          |


 

 