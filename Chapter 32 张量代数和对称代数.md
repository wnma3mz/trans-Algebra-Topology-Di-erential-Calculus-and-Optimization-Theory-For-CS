第三十二章

# Tensor Algebras and Symmetric Algebras  张量代数和对称代数

Tensors are creatures that we would prefer did not exist but keep showing up whenever multilinearity manifests itself.
 张量是我们希望不存在的生物，但当多能性显现出来时，张量就会不断出现。

One of the goals of differential geometry is to be able to generalize “calculus on Rn” to spaces more general than Rn, namely manifolds. We would like to differentiate functions f : M → R defined on a manifold, optimize functions (find their minima or maxima), but also to integrate such functions, as well as compute areas and volumes of subspaces of our manifold.
 微分几何的目标之一是能够将“RN上的微积分”推广到比RN更普遍的空间，即流形。我们要区分在流形上定义的函数f:m→r，优化函数（找到它们的最小值或最大值），还要集成这些函数，以及计算流形子空间的面积和体积。

The suitable notion of differentiation is the notion of tangent map, a linear notion. One of the main discoveries made at the beginning of the twentieth century by Poincar´e and Elie´ Cartan, is that the “right” approach to integration is to integrate differential forms, and not functions. To integrate a function f, we integrate the form fω, where ω is a volume form on the manifold M. The formalism of differential forms takes care of the process of the change of variables quite automatically, and allows for a very clean statement of Stokes’ formula.
 微分的适当概念是切线映射的概念，一个线性概念。Poincar'e和Elie'Cartan在二十世纪初的主要发现之一是，整合的“正确”方法是整合微分形式，而不是功能。为了积分函数f，我们将形式fω积分，其中ω是流形m上的体积形式。微分形式的形式主义完全自动地处理变量的变化过程，并允许斯托克斯公式的一个非常清晰的陈述。

Differential forms can be combined using a notion of product called the wedge product, but what really gives power to the formalism of differential forms is the magical operation d of exterior differentiation. Given a form ω, we obtain another form dω, and remarkably, the following equation holds
 微分形式可以用一个称为楔积的积的概念来组合，但真正赋予微分形式形式形式主义力量的是外部微分的神奇运算d。给定形式ω，我们得到另一个形式dω，值得注意的是，下列方程成立

ddω = 0.
 ddω=0.

As silly as it looks, the above equation lies at the core of the notion of cohomology, a powerful algebraic tool to understand the topology of manifolds, and more generally of topological spaces.
 尽管看起来很愚蠢，但上述方程是上同调概念的核心，是理解流形拓扑的强大代数工具，更普遍的是拓扑空间。

Elie Cartan had many of the intuitions that lead to the cohomology of differential forms,´ but it was George de Rham who defined it rigorously and proved some important theorems about it. It turns out that the notion of Laplacian can also be defined on differential forms using a device due to Hodge, and some important theorems can be obtained: the Hodge
 Elie Cartan有许多直觉导致了微分形式的上同调，但正是乔治·德·雷姆对其进行了严格的定义，并证明了一些重要的定理。结果表明，由于霍奇的存在，拉普拉斯的概念也可以用一个装置在微分形式上定义，并且可以得到一些重要的定理：霍奇

1045
 一千零四十五

decomposition theorem, and Hodge’s theorem about the isomorphism between the de Rham cohomology groups and the spaces of harmonic forms.
 分解定理，和霍奇关于德拉姆上同调群与调和形式空间同构的定理。

To understand all this, one needs to learn about differential forms, which turn out to be certain kinds of skew-symmetric (also called alternating) tensors.
 要理解这一切，我们需要学习微分形式，它是某种斜对称（也称为交替）张量。

If one’s only goal is to define differential forms, then it is possible to take some short cuts and to avoid introducing the general notion of a tensor. However, tensors that are not necessarily skew-symmetric arise naturally, such as the curvature tensor, and in the theory of vector bundles, general tensor products are needed.
 如果一个人的唯一目标是定义微分形式，那么有可能采取一些捷径，避免引入张量的一般概念。然而，不一定是斜对称的张量自然产生，如曲率张量，在向量束理论中，一般张量积是必要的。

Consequently, we made the (perhaps painful) decision to provide a fairly detailed exposition of tensors, starting with arbitrary tensors, and then specializing to symmetric and alternating tensors. In particular, we explain rather carefully the process of taking the dual of a tensor (of all three flavors).
 因此，我们做出了（也许是痛苦的）决定，提供了一个相当详细的张量说明，从任意张量开始，然后专门讨论对称张量和交替张量。特别是，我们非常仔细地解释了取张量（三种口味中的）的对偶的过程。

We refrained from following the approach in which a tensor is defined as a multilinear map defined on a product of dual spaces, because it seems very artificial and confusing (certainly to us). This approach relies on duality results that only hold in finite dimension, and consequently unecessarily restricts the theory of tensors to finite dimensional spaces. We also feel that it is important to begin with a coordinate-free approach. Bases can be chosen for computations, but tensor algebra should not be reduced to raising or lowering indices.
 我们避免采用张量被定义为在对偶空间乘积上定义的多行映射的方法，因为它看起来非常人为和混乱（当然对我们来说）。这种方法依赖于仅在有限维中存在的对偶结果，因此不必要地将张量理论限制在有限维空间中。我们还认为，从无坐标方法开始是很重要的。可以选择基进行计算，但张量代数不应减少到提高或降低指数。

Readers who feel that they are familiar with tensors should probably skip this chapter and the next. They can come back to them “by need.”
 那些认为自己熟悉张量的读者可能会跳过这一章和下一章。他们可以“根据需要”回到他们身边。

We begin by defining tensor products of vector spaces over a field and then we investigate some basic properties of these tensors, in particular the existence of bases and duality. After this we investigate special kinds of tensors, namely symmetric tensors and skew-symmetric tensors. Tensor products of modules over a commutative ring with identity will be discussed very briefly. They show up naturally when we consider the space of sections of a tensor product of vector bundles.
 我们首先定义场上向量空间的张量积，然后研究这些张量的一些基本性质，特别是基和对偶的存在性。在此基础上，我们研究了特殊类型的张量，即对称张量和斜对称张量。讨论了具有恒等式的交换环上模的张量积。当我们考虑向量束张量积各部分的空间时，它们自然会出现。

Given a linear map f : E → F (where E and F are two vector spaces over a field K), fwe know that if we have a basis ((ui) on the basis vectors. For a multilinear mapui)i∈I for E, thenf :fEis completely determined by its valuesn → F, we don’t know if there is such a nice property but it would certainly be very useful.
 给定一个线性映射f:e→f（其中e和f是K域上的两个向量空间），我们知道如果我们有基向量的基（（ui）。对于多行mapui）i∈i表示e，那么f:f e is完全由其值n→f决定，我们不知道是否有这样一个好的属性，但它肯定是非常有用的。

In many respects tensor products allow us to define multilinear maps in terms of their action on a suitable basis. The crucial idea is to linearize, that is, to create a new vector space
 在许多方面，张量积允许我们在适当的基础上根据它们的作用定义多行映射。关键的思想是线性化，即创建一个新的向量空间

E⊗n such that the multilinear map f : En → F is turned into a linear map f⊗ : E⊗n → F which is equivalent to f in a strong sense. If in addition, f is symmetric, then we can define a symmetric tensor power Symn(E), and every symmetric multilinear map f : En → F is turned into a linear map  which is equivalent to f in a strong sense.
 e n使得多行映射f:en→f变成线性映射f：e n→f，在强意义上等价于f。另外，如果f是对称的，那么我们可以定义一个对称张量幂次对称（e），每个对称的多行映射f:en→f都变成一个强意义上等价于f的线性映射。

Similarly, if f is alternating, then we can define a skew-symmetric tensor power Vn(E), and every alternating multilinear map is turned into a linear map f∧ : Vn(E) → F which is equivalent to f in a strong sense.
 同样，如果f是交变的，那么我们可以定义一个斜对称张量幂vn（e），每个交变多线性映射都变成一个线性映射f：vn（e）→f，在强意义上等价于f。


 

Tensor products can be defined in various ways, some more abstract than others. We try to stay down to earth, without excess.
 张量积可以用不同的方式定义，有些比其他更抽象。我们尽量不过度地呆在地上。

Before proceeding any further, we review some facts about dual spaces and pairings. Pairings will be used to deal with dual spaces of tensors.
 在进一步讨论之前，我们回顾了一些关于双空间和配对的事实。配对将用于处理张量的对偶空间。

## 32.1     Linear Algebra Preliminaries: Dual Spaces and Pairings  32.1线性代数预备：对偶空间和对

We assume that we are dealing with vector spaces over a field K. As usual the dual space E∗ of a vector space E is defined by E∗ = Hom(E,K). The dual space E∗ is the vector space consisting of all linear maps ω: E → K with values in the field K.
 我们假设我们处理的是场k上的向量空间。通常，向量空间e的对偶空间e_由e=hom（e，k）定义。对偶空间e是由所有线性映射构成的向量空间，ω：e→k与字段k中的值。

A problem that comes up often is to decide when a space E is isomorphic to the dual F ∗ of some other space F (possibly equal to E). The notion of pairing due to Pontrjagin provides a very clean criterion.
 一个经常出现的问题是决定空间e何时同构于其他空间f（可能等于e）的对偶f_。Pontrjagin提出的配对概念提供了一个非常清晰的标准。

Definition 32.1. Given two vector spaces E and F over a field K, a map h−,−i: E×F → K is a nondegenerate pairing iff it is bilinear and iff hu,vi = 0 for all v ∈ F implies u = 0, and ϕhu,v: Ei = 0F ∗for alland ψu: F∈ →E Eimplies∗ defined such that for all for allv = 0. A nondegenerate pairing induces two linear mapsu ∈ E and all v ∈ F, ϕ(u) is the
 定义32.1.在一个K域上给定两个向量空间e和f，映射h−，−i:e×f→k是一个非退化的对，如果它是双线性的，并且iff h u，vi=0表示所有v∈f表示u=0，而_hu，v:ei=0f表示all andψu:f∈→e e implies定义为all表示allv=0。非退化配对诱导两个线性mapsu∈e，且所有v∈f，ω（u）是

→
 渐次

linear form in F ∗ and ψ(v) is the linear form in E∗ given by
 f和ψ（v）中的线性形式是e中的线性形式，由

ϕ(u)(y) =     hu,yi      for all y ∈ F ψ(v)(x)  =     hx,vi       for all x ∈ E.
 ⑨（u）（y）=hu，yi表示所有y∈fψ（v）（x）=hx，vi表示所有x∈e。

Schematically, ϕ(u) = hu,−i and ψ(v) = h−,vi.
 式中，（u）=hu、−i和ψ（v）=h−，vi。

ϕProposition 32.1.: E → F ∗ and ψϕ::For every nondegenerate pairingFE →E∗ are linear and injective. Furthermore, ifh−,−i: E ×F → KE, the induced mapsand F are finite dimensional, then → F ∗ and ψ: F → E∗ are bijective.
 第32.1条建议：e→f和_：：对于每一个非简并配对fe→e都是线性的和内射的。此外，如果H−、−i:e×f→ke，诱导映射和f是有限维的，那么→f和ψ:f→e是双射的。

Proof. The maps ϕ: E → F ∗ and ψ: F → E∗ are linear because u,v → h7              u,vi is bilinear.
 证据。由于u，v→h7 u，vi是双线性的，因此图_：e→f和ψ：f→e_是线性的。

Assume that ϕ(u) = 0. This means that ϕ(u)(y) = hu,yψ iis injective. If= 0 for all yE∈andF, and as ourF are finite pairing is nondegenerate, we must have u = 0. Similarly, dimensional, then dim(E) = dim(E∗) and dim(F) = dim(F ∗). However, the injectivity of ϕ and ψ implies that that dim(E) ≤ dim(F(E∗)) =and dimdim(F(F). Therefore, dim) ≤ dim(E∗). Consequently dim(E) = dim(F ∗) (andE) ≤ϕ dim(F) and dim(F) ≤ dim(E), so dim is bijective (and similarly dim(F) = dim(E∗) and ψ is bijective). 
 假设_（u）=0。也就是说，ψ（u）（y）=hu，yψ是注射剂。如果所有的ye∈andf都为0，并且我们的f是有限对，所以我们必须有u=0。同样，尺寸，然后dim（e）=dim（e）和dim（f）=dim（f）。然而，ω和ψ的注入率意味着dim（e）≤dim（f（e））=和dimdim（f（f）。因此，dim）≤dim（e）。因此，dim（e）=dim（f）（ande）≤dim（f）和dim（f）≤dim（e），所以dim是双射的（类似地，dim（f）=dim（e），ψ是双射的）。

Proposition 32.1 shows that when E and F are finite dimensional, a nondegenerate pairing induces canonical isomorphims ϕ: E → F ∗ and ψ: F → E∗; that is, isomorphisms that do not depend on the choice of bases. An important special case is the case where E = F and we have an inner product (a symmetric, positive definite bilinear form) on E.
 命题32.1表明，当e和f是有限维时，非简并配对产生标准同构，即不依赖于基的选择的同构。一个重要的特殊情况是E=F的情况，我们在E上有一个内积（对称的，正定双线性形式）。

Remark: When we use the term “canonical isomorphism,” we mean that such an isomorphism is defined independently of any choice of bases. For example, if E is a finite dimensional vector space and (e1,...,en) is any basis of E, we have the dual basis (
 注：当我们使用“规范同构”这个术语时，我们的意思是这样的同构是独立于任何碱基的选择而定义的。例如，如果e是一个有限维向量空间，而（e1，…，en）是e的任何基，我们就有了对偶基。（

E∗ (where,), and thus the map is an isomorphism between E and E∗.
 E（其中，），因此地图是E和E之间的同构。

This isomorphism is not canonical.
 这种同构不是典型的。

On the other hand, if h−,−i is an inner product on E, then Proposition 32.1 shows that the nondegenerate pairing h−,−i on E ×E induces a canonical isomorphism between E and E∗. This isomorphism is often denoted [: E → E∗, and we usually write u[ for [(u), with u ∈ E. Schematically, u[ = hu,−i. The inverse of [ is denoted ]: E∗ → E, and given any linear form ω ∈ E∗, we usually write ω] for ](ω). Schematically, ω = hω],−i.
 另一方面，如果h−、−i是e上的内积，那么命题32.1表明，非简并配对h−、−i在e×e上诱导e和e之间的规范同构。这种同构常被表示为[：e→e，我们通常用u[表示为[（u），用u e。用图式表示，u[=hu，−i。[表示为]：e→e的倒数，并且给定任何线性形式ωe，我们通常用ω]表示（ω）。简图上，ω=hω]，−i。

Given any basis, (e1,...,en) of E (not necessarily orthonormal), let (gij) be the n × nmatrix given by gij = hei,eji (the Gram matrix of the inner product). Recall that the dual basis  consists of the coordinate forms e∗i ∈ E∗, which are characterized by the following properties: e∗i (ej) = δij, 1 ≤ i,j ≤ n.
 给定e的任何基（e1，…，e n）（不一定是正交），设（gij）为gij=hei，eji（内积的g矩阵）给出的n×n matrix。该对偶基由坐标形式e i∈e组成，其特征是：e i（e j）=δij，1≤i，j≤n。

The inverse of the Gram matrix (gij) is often denoted by (gij) (by raising the indices).
 革兰矩阵（gij）的逆矩阵通常用（gij）（通过提高指数）表示。

The tradition of raising and lowering indices is pervasive in the literature on tensors. It is indeed useful to have some notational convention to distinguish between vectors and linear forms (also called one-forms or covectors). The usual convention is that coordinates of vectors are written using superscripts, as in , and coordinates of one-forms are written using subscripts, as in. Actually, since vectors are indexed with subscripts, one-forms are indexed with superscripts, so should be written as ei.
 提高和降低指数的传统在张量文献中普遍存在。有一些符号约定来区分向量和线性形式（也称为单形或双形）确实很有用。通常的惯例是向量的坐标是用上标写的，如中所示，而一种形式的坐标是用下标写的，如中所示。实际上，因为向量是用下标索引的，所以一种形式是用上标索引的，所以应该写为ei。

The motivation is that summation signs can then be omitted, according to the Einstein summation convention. According to this convention, whenever a summation variable (such as i) appears both as a subscript and a superscript in an expression, it is assumed that it is involved in a summation. For example the sum is abbreviated as
 根据爱因斯坦的求和约定，其动机是求和符号可以省略。根据这一惯例，当求和变量（如i）在表达式中同时显示为下标和上标时，假定它与求和有关。例如，总和缩写为

uiei,
 尤伊

and the sum is abbreviated as
 和缩写为

ωiei.
 ωIEI。

In this text we will not use the Einstein summation convention, which we find somewhat confusing, and we will also write instead of ei.
 在本文中，我们将不使用爱因斯坦求和约定，我们发现这有点令人困惑，我们也将写而不是EI。

The maps [ and ] can be described explicitly in terms of the Gram matrix of the inner product and its inverse.
 图[和]可以用内积的克矩阵及其逆矩阵来明确地描述。

Proposition 32.2. For any vector space E, given a basis (e1,...,en) for E and its dual basis , for any inner product h−,−i on E, if (gij) is its Gram matrix, with gij = hei,eji, and (gij) is its inverse, then for every vector and every one-form, we have
 提案32.2.对于任何向量空间e，给定e及其对偶基的基（e1，…，en），对于任何内积h−，−i on e，如果（gij）是它的g矩阵，其中gij=hei，eji，and（gij）是它的逆矩阵，那么对于每个向量和每个形式，我们都有

​                                                         ,                with               ,
 ，带有，

and
 和

​                                                       ,                  with                  .
 ，使用。

Proof. For every, since u[(v) = hu,vi for all v ∈ E, we have
 证据。对于每一个，因为u[（v）=hu，vi对于所有v∈e，我们有

,
 ，

so we get
 所以我们得到

​                                                         ,                             with .
 ，使用。

If we write and, since
 如果我们写信，从那以后

​                                                                ,                                        1 ≤ i ≤ n,
 ，1≤i≤n，

we get
 我们得到

,
 ，

where (gij) is the inverse of the matrix (gij).                                                                                  
 其中（gij）是矩阵（gij）的倒数。

The map [ has the effect of lowering (flattening!) indices, and the map ] has the effect of raising (sharpening!) indices.
 地图[具有降低效果（平展！）索引和地图]具有提升效果（锐化！）指数。

Here is an explicit example of Proposition 32.2. Let (e1,e2) be a basis of E such that
 这是32.2提案的一个明确例子。设（e1，e2）为e的基础，这样

he1,e1i = 1,    he1,e2i = 2,  he2,e2i = 5. Then
 he1，e1i=1，he1，e2i=2，he2，e2i=5。然后

 .
 .

Set u = u1e1 + u2e2 and observe that u[(e1) = hu1e1 + u2e2,e1i = he1,e1iu1 + he2,e1iu2 = g11u1 + g12u2 = u1 + 2u2 u[(e2) = hu1e1 + u2e2,e2i = he1,e2iu1 + he2,e2iu2 = g21u1 + g22u2 = 2u1 + 5u2,
 设置u=u1 e1+u2e2，观察u[（e1）=hu1e1+u2e2，e1i=he1，e1i u1+he2，e1iu2=g1u1+g12u2=u1+2u2 u[（e2）=hu1e1+u2e2，e2i=he1，e2iu1+he2，e2iu2=g21u1+g2u2=2u1+5u2，

which in turn implies that
 这反过来意味着

.
 .

Given, we calculate ω] = (ω])1e1 + (ω])2e2 from the following two linear equalities:
 给定，我们根据以下两个线性等式计算ω]=（ω]）1e1+（ω]）2e2：

ω1 = ω(e1) = hω],e1i = h(ω])1e1 + (ω])2e2,e1i
 ω1=ω（e1=hω），e1i=h（ω]）1e1+（ω]）2e2，e1i

= he1,e1i(ω])1 + he2,e1i(ω])2 = (ω])1 + 2(ω])2 = g11(ω])1 + g12(ω])2 ω2 = ω(e2) = hω],e2i = h(ω])1e1 + (ω])2e2,e2i
 =he1，e1i（ω）]1+h e2，e1i（ω）]2=（ω）]1+2（ω）]2=g11（ω）]1+g12（ω）]2ω2=ω（e2=hω），e2i=h（ω）]1e1+（ω）]2e2，e2i

= he1,e2i(ω])1 + he2,e2i(ω])2 = 2(ω])1 + 5(ω])2 = g21(ω])1 + g22(ω])2.
 =he1，e2i（ω）]1+he2，e2i（ω）]2=2（ω）]1+5（ω）]2=g21（ω）]1+g22（ω）]2.

These equalities are concisely written as
 这些等式简明地写为

 .
 .

Then
 然后

,
 ，

which in turn implies
 这反过来意味着

(ω])1 = 5ω1 − 2ω2,  (ω])2 = −2ω1 + ω2, i.e.
 （ω）1=5ω1−2ω2，（ω）2=−2ω1+ω2，即

ω] = (5ω1 − 2ω2)e1 + (−2ω1 + ω2)e2.
 ω]=（5ω1−2ω2）e1+（−2ω1+ω2）e2。

The inner product h−,−i on E induces an inner product on E∗ denoted h−,−iE∗, and given by
 内积H−、−I on E在E∮上诱导内积，表示为H−、−IE∮，并由下式给出

​                                                           ,                       for all ω1,ω2 ∈ E∗.
 ，对于所有ω1，ω2∈e。

Then we have
 然后我们有了

  for all    u,v ∈ E. If (e1,...,en) is a basis of E and gij = hei,eji, as
 对于所有u，v∈e，如果（e1，…，en）是e的基础，且gij=hei，eji，as

,
 ，

an easy computation shows that
 一个简单的计算表明

;
 ；

that is, in the basis (), the inner product on E∗ is represented by the matrix (gij), the inverse of the matrix (gij).
 也就是说，在基（）中，e上的内积由矩阵（gij）表示，即矩阵（gij）的倒数。

The inner product on a finite vector space also yields a canonical isomorphism between the space Hom(E,E;K) of bilinear forms on E, and the space Hom(E,E) of linear maps from E to itself. Using this isomorphism, we can define the trace of a bilinear form in an intrinsic manner. This technique is used in differential geometry, for example, to define the divergence of a differential one-form.
 有限向量空间上的内积也在e上双线性形式的空间hom（e，e；k）和e到其自身的线性映射的空间hom（e，e）之间产生一个规范的同构。利用这种同构，我们可以用一种内在的方式定义双线性形式的轨迹。例如，这种技术在微分几何中被用来定义微分一形式的散度。

Proposition 32.3. If h−,−i is an inner product on a finite vector space E (over a field, K), then for every bilinear form f : E × E → K, there is a unique linear map f\ : E → E
 提案32.3.如果h−，−i是有限向量空间e（在字段上，k）上的内积，那么对于每一个双线性形式f:e×e→k，都有一个唯一的线性映射f \：e→e

such that f(u,v) = hf\(u),vi, for all u,v ∈ E.
 这样f（u，v）=hf \（u），vi，对于所有u，v∈e。

The map f 7→ f\ is a linear isomorphism between Hom(E,E;K) and Hom(E,E). Proof. For every g ∈ Hom(E,E), the map given by
 图F7→F是hom（e，e；k）和hom（e，e）之间的线性同构。证据。对于每个g∈hom（e，e），由

​                                                       f(u,v) = hg(u),vi,        u,v ∈ E,
 f（u，v）=hg（u），vi，u，v∈e，

is clearly bilinear. It is also clear that the above defines a linear map from Hom(E,E) to Hom(E,E;K). This map is injective, because if f(u,v) = 0 for all u,v ∈ E, as h−,−i is an inner product, we get g(u) = 0 for all u ∈ E. Furthermore, both spaces Hom(E,E) and Hom(E,E;K) have the same dimension, so our linear map is an isomorphism. 
 显然是双线性的。很明显，上面定义了从hom（e，e）到hom（e，e；k）的线性映射。这个映射是内射的，因为如果f（u，v）=0表示所有u，v∈e，因为h−，−i是一个内积，我们得到g（u）=0表示所有u∈e。此外，两个空间hom（e，e）和hom（e，e；k）都有相同的维数，所以我们的线性映射是同构的。

If (e1,...,en) is an orthonormal basis of E, then we check immediately that the trace of a linear map g (which is independent of the choice of a basis) is given by
 如果（e1，…，en）是e的正交基，那么我们立即检查线性映射g的迹线（与基的选择无关）是由

n
 n

tr(g) = Xhg(ei),eii,
 tr（g）=xhg（ei），eii，

i=1
 i＝1

where n = dim(E).
 其中n=尺寸（e）。

Definition 32.2. We define the trace of the bilinear form f by
 定义32.2.我们定义双线性形式f的迹线

tr(f) = tr(f\).
 Tr（f）=Tr（f\）。

From Proposition 32.3, tr(f) is given by
 根据提案32.3，Tr（f）由

n
 n

tr(f) = Xf(ei,ei),
 tr（f）=xf（ei，ei），即

i=1
 i＝1

for any orthonormal basis (e1,...,en) of E. We can also check directly that the above expression is independent of the choice of an orthonormal basis.
 对于e的任何正交基（e1，…，en），我们也可以直接检查上述表达式是否独立于正交基的选择。

We demonstrate how to calculate tr(f) where f : R2 ×R2 → R with f((x1,y1),(x2,y2)) = x1x2+2x2y1+3x1y2−y1y2. Under the standard basis for R2, the bilinear form f is represented as
 我们演示了如何计算Tr（f），其中f:r2×r2→r，其中f（（x1，y1），（x2，y2））=x1x2+2x2y1+3x1y2−y1y2。在r2的标准基础上，双线性形式f表示为

 .
 .

This matrix representation shows that
 这个矩阵表示表明

 ,
 ，

and hence
 因此

tr(.
 T.

We will also need the following proposition to show that various families are linearly independent.
 我们还需要以下的命题来证明各种族是线性独立的。

Proposition 32.4. Let E and F be two nontrivial vector spaces and let (ui)i∈I be any family of vectors ui ∈ E. The family (ui)i∈I is linearly independent iff for every family (vi)i∈I of vectors vi ∈ F, there is some linear map f : E → F so that f(ui) = vi for all i ∈ I.
 提案32.4.设e和f为两个非平凡向量空间，设（ui）i∈i为任意向量族ui∈e，向量族（ui）i∈i为每个向量族（vi）i∈i的线性独立iff，有一些线性映射f:e→f，使f（ui）=vi为所有i∈i。

Proof. Left as an exercise.                                                                                                                 
 证据。留作练习。

## 32.2       Tensors Products  32.2张量积

First we define tensor products, and then we prove their existence and uniqueness up to isomorphism.
 首先定义张量积，然后证明它们的存在性和唯一性，直至同构。

Definition 32.3. Let K be a given field, and let E1,...,En be n ≥ 2 given vector spaces. For any vector space F, a map f : E1 × ··· × En → F is multilinear iff it is linear in each of its argument; that is,
 定义32.3.设k为给定域，设e1，…，en为n≥2给定向量空间。对于任何向量空间f，映射f:e1×·······×en→f是多行的，如果它在每个参数中都是线性的，也就是说，

​                          f(u1,...ui1,v + w,ui+1,...,un)         =         f(u1,...ui1,v,ui+1,...,un)
 f（u1，…ui1，v+w，ui+1，…，un）=f（u1，…ui1，v，ui+1，…，un）

\+ f(u1,...ui1,w,ui+1,...,un)
 +f（u1，…ui1，w，ui+1，…，un）

​                               f(u1,...ui1,λv,ui+1,...,un)         =         λf(u1,...ui1,v,ui+1,...,un),
 f（u1，…ui1，λv，ui+1，…，un）=λf（u1，…ui1，v，ui+1，…，un）

for all uj ∈ Ej (j =6          i), all v,w ∈ Ei and all λ ∈ K, for i = 1...,n.
 对于所有的uj∈ej（j=6i），所有的v，w∈ei和所有的λ∈k，对于i=1…，n。

The set of multilinear maps as above forms a vector space denoted L(E1,...,En;F) or Hom(E1,...,En;F). When n = 1, we have the vector space of linear maps L(E,F) (also denoted Hom(E,F)). (To be very precise, we write HomK(E1,...,En;F) and HomK(E,F).)
 如上所述的多行映射集形成了表示l（e1，…，en；f）或hom（e1，…，en；f）的向量空间。当n=1时，我们得到线性映射的向量空间l（e，f）（也表示hom（e，f））。（准确地说，我们写homk（e1，…，en；f）和homk（e，f）。）


 

Definition 32.4. A tensor product of n ≥ 2 vector spaces E1,...,En is a vector space T together with a multilinear map ϕ: E1 × ··· × En → T, such that for every vector space F and for every multilinear map f : E1×···×En → F, there is a unique linear map f⊗ : T → F with f(u1,...,un) = f⊗(ϕ(u1,...,un)),
 定义32.4.n≥2个向量空间e1，…，en的张量积是向量空间t加上一个多行映射：e1×······························································，…，un）），

for all u1 ∈ E1,...,un ∈ En, or for short
 对于所有u1∈e1，…，un∈en，或简称

f = f⊗ ◦ ϕ.
 F=F _。

Equivalently, there is a unique linear map f⊗ such that the following diagram commutes.
 同样地，有一个独特的线性图f，这样下图就可以通勤了。

ϕ
 γ

​                                                            E1 × ··· × En          / T
 e1×····×en/t

NNNNNf⊗ f N& F
 nnnnn F F N&F公司

The above property is called the universal mapping property of the tensor product (T,ϕ).
 上述性质称为张量积（t，_）的普适映射性质。

We show that any two tensor products (T1,ϕ1) and (T2,ϕ2) for E1,...,En, are isomorphic.
 我们证明e1，…，en的任何两个张量积（T1，_）和（T2，_）是同构的。

Proposition 32.5. Given any two tensor products (T1,ϕ1) and (T2,ϕ2) for E1,...,En, there is an isomorphism h: T1 → T2 such that
 提案32.5。对于e1，…，en，给定任意两个张量积（t1，_）和（t2，_），存在同构h:t1→t2，这样

ϕ2 = h ◦ ϕ1.
 _2=H_1.

Proof. Focusing on (T1,ϕ1), we have a multilinear map ϕ2 : E1 × ··· × En → T2, and thus there is a unique linear map (ϕ2)⊗ : T1 → T2 with
 证据。针对（T1，_），我们有一个多行图_:e1×······×en→t2，因此有一个独特的线性图（_）：T1→t2

ϕ2 = (ϕ2)⊗ ◦ ϕ1
 _=（_）_

as illustrated by the following commutative diagram.
 如下图所示。

ϕ1
 1

​                                                         E1 × ··· × En          / T1
 e1×····×en/t1

MMMMMM(ϕ2)⊗ ϕ2
 mmmmmm（_2）_2

​                                                                                     M& 
 M & &

T2
 T2

Similarly, focusing now on on (T2,ϕ2), we have a multilinear map ϕ1 : E1 × ··· × En → T1, and thus there is a unique linear map (ϕ1)⊗ : T2 → T1 with
 同样，现在重点放在（t2，_）上，我们有一个多行图_:e1×······×en→t1，因此有一个唯一的线性图（_）：t2→t1

ϕ1 = (ϕ1)⊗ ◦ ϕ2
 _=（_）_

as illustrated by the following commutative diagram.
 如下图所示。

ϕ2
 2

​                                                         E1 × ··· × En          / T2
 e1×····×en/t2

MMMMMM(ϕ1)⊗ ϕ1
 mmmmmm（_1）_1

​                                                                                     M& 
 M & &

T1
 t1

Putting these diagrams together, we obtain the commutative diagrams
 把这些图放在一起，就得到了交换图。

8 T1
 8 T1

ϕ1q qqqq(ϕ2)⊗
 q QQQ（_）

q q
 问Q

qqqq ϕ2
 QQQ_号

​                                                         E1 × ··· × En      / T2
 e1×····×en/t2

MMMMϕMMMMMMMM(ϕ1)⊗
 _mmmm mmmm（_1）

​                                                                               1      & T 1
 1&T 1


 

and
 和

### 8 T2  8 T2

ϕ2ppppp(ϕ1)⊗
 pppp（_）

pp
 聚丙烯

pppp ϕ1 p
 pppp_1p

​                                                         E1 × ··· × En           /T1
 e1×····×en/t1

NNNNϕN2NNNNNN&(ϕ2)⊗
 nnnn_n2nnnnnn&（_2）


 

T2,
 T2，

which means that
 也就是说

​                          ϕ1 = (ϕ1)⊗ ◦ (ϕ2)⊗ ◦ ϕ1 and ϕ2 = (ϕ2)⊗ ◦ (ϕ1)⊗ ◦ ϕ2.
 _=（_）（_）_1和_=（_）（_）_2.

On the other hand, focusing on (T1,ϕ1), we have a multilinear map ϕ1 : E1 ×···×En → T1, but the unique linear map h: T1 → T1 with
 另一方面，聚焦于（T1，Ф1），我们有一个多行图，其中的第1行图为：e1×·································

ϕ1 = h ◦ ϕ1
 _1=H_1

is h = id, as illustrated by the following commutative diagram
 是h=id，如下图所示

ϕ1
 1

​                                                            E1 × ··· × En           / T1
 e1×····×en/t1

​                                                                        NNNNN          id
 nnnnn标识

1                 & 
 &

T1,
 T1

and since (ϕ1)⊗ ◦ (ϕ2)⊗ is linear as a composition of linear maps, we must have
 由于（_）（_）作为线性地图的组成部分是线性的，我们必须

(ϕ1)⊗ ◦ (ϕ2)⊗ = id.
 （_1）（_2）=ID.

Similarly, we have the commutative diagram
 同样，我们有交换图

ϕ2
 2

​                                                      E1 × ··· ×NNENNnN   / T2id
 e1×····×nnnn/t2id

2                 & 
 &

T2,
 T2

and we must have
 我们必须有

(ϕ2)⊗ ◦ (ϕ1)⊗ = id.
 （_2）（_1）=ID.

This shows that (isomorphism betweenϕ1)⊗T1and (andϕT22).⊗ are inverse linear maps, and thus, (ϕ2)⊗ : T1 → T2 is an
 这表明（_1）t1和（和_t22）之间的同构）是反线性映射，因此，（_2）：t1→t2是

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

Now that we have shown that tensor products are unique up to isomorphism, we give a construction that produces them. Tensor products are obtained from free vector spaces by a quotient process, so let us begin by describing the construction of the free vector space generated by a set.
 现在我们已经证明张量积在同构上是唯一的，我们给出了产生它们的构造。张量积是通过商过程从自由向量空间中得到的，所以让我们首先描述由集合生成的自由向量空间的构造。

For simplicity assume that our set I is finite, say
 为了简单起见，假设我们的集合i是有限的，比如

I = {♥,♦,♠,♣}.
 我=，♦，，。

The construction works for any field K (and in fact for any commutative ring A, in which case we obtain the free A-module generated by I). Assume that K = R. The free vector space generated by I is the set of all formal linear combinations of the form
 该结构适用于任意场k（实际上也适用于任意交换环a，在这种情况下，我们得到由i生成的自由a-模）。假设k=r，由i生成的自由向量空间是形式的所有形式线性组合的集合。

a♥ + b♦ + c♠ + d♣,
 A+B♦+C+D，

with a,b,c,d ∈ R. It is assumed that the order of the terms does not matter. For example,
 对于a，b，c，d∈r，假设条件的次序不重要。例如，

2♥ − 5♦ + 3♠ = −5♦ + 2♥ + 3♠.
 2−5♦+3=−5♦+2+3。

Addition and multiplication by a scalar are are defined as follows:
 标量的加法和乘法定义如下：

(a1♥ + b1♦ + c1♠ + d1♣) + (a2♥ + b2♦ + c2♠ + d2♣)
 （A1+B1♦+C1+D1）+（A2+B2♦+C2+D2）

= (a1 + a2)♥ + (b1 + b2)♦ + (c1 + c2)♠ + (d1 + d2)♣,
 =（a1+a2）+（b1+b2）♦+（c1+c2）+（d1+d2），

and
 和

α · (a♥ + b♦ + c♠ + d♣) = αa♥ + αb♦ + αc♠ + αd♣,
 α·（a+b♦+c+d）=αa+αb♦+αc+αd，

for all a,b,c,d,α ∈ RR. With these operations, it is immediately verified that we obtain a(I). The set I can be viewed as embedded in R(I) by the injection ι vector space denoted given by
 对于所有a，b，c，d，α∈rr。通过这些操作，我们立即证实我们获得了（i）。通过表示的注入_矢量空间，可以将集合i视为嵌入到r（i）中

​                                   ι(♥) = 1♥,       ι(♦) = 1♦,       ι(♠) = 1♠,        ι(♣) = 1♣.
 （）=1，（♦）=1♦，（）=1，（）=1。

Thus,case, RR(I()I)is isomorophic tocan be viewed as the vector space with the special basisR4.       I = {♥,♦,♠,♣}. In our The exact same construction works for any field K, and we obtain a vector space denoted by K(I) and an injection ι: I → K(I).
 因此，案例，rr（i（）i）是同构的，视为具有特殊基础的向量空间4.i=，♦，，。在我们对任意场k的完全相同的构造中，我们得到了一个用k（i）表示的向量空间和一个注入_：i→k（i）。

The main reason why the free vector space K(I) over a set I is interesting is that it satisfies a universal mapping property. This means that for every vector space F (over the field K), any function h: I → F, where F is considered just a set, has a unique linear
 集i上的自由向量空间k（i）有趣的主要原因是它满足一个普遍映射属性。这意味着对于每个向量空间f（在k域上），任何函数h:i→f，其中f仅被视为一个集合，具有唯一的线性。

extension h: K(I) → F. By extension, we mean that h(i) = h(i) for all i ∈ I, or more
 推广h:k（i）→f.通过推广，我们的意思是h（i）=h（i）对于所有i∈i，或更多

rigorously that h = h ◦ ι.
 严格地说，h=h。

For example, if I = {♥,♦,♠,♣}, K = R, and F = R3, the function h given by h(♥) = (1,1,1), h(♦) = (1,1,0), h(♠) = (1,0,0), h(♣) = (0,0 − 1)
 例如，如果i=，♦，，，k=r，f=r3，则h（）=（1,1,1），h（♦）=（1,1,0），h（）=（1,0,0），h（）=（0,0−1）给出的函数h。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

has a unique linear extension h: R(I) → R3 to the free vector space R(I), given by
 对自由向量空间r（i）具有唯一的线性扩展h:r（i）→r3，由下式给出

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

To generalize the construction of a free vector space to infinite sets I, we observe that the formal linear combination a♥ + b♦ + c♠ + d♣ can be viewed as the function f : I → R given by
 为了将自由向量空间的构造推广到无穷集i，我们发现形式线性组合a+b♦+c+d可以看作是由

​                                        f(♥) = a,        f(♦) = b,        f(♠) = c,        f(♣) = d,
 F（）=A，F（♦）=B，F（）=C，F（）=D，

where a,b,c,d ∈ R. More generally, we can replace R by any field K. If I is finite, then the set of all such functions is a vector space under pointwise addition and pointwise scalar multiplication. If I is infinite, since addition and scalar multiplication only makes sense for finite vectors, we require that our functions f : I → K take the value 0 except for possibly finitely many arguments. We can think of such functions as an infinite sequences (fi)i∈I of elements fi of K indexed by I, with only finitely many nonzero fi. The formalization of this construction goes as follows.
 其中a，b，c，d∈r，一般来说，我们可以用任意的k域代替r，如果i是有限的，那么所有这些函数的集合都是点加法和点标量乘法下的向量空间。如果我是无限的，因为加法和标量乘法只对有限向量有意义，我们要求函数f:i→k取0，除了可能有限的许多参数。我们可以把这些函数看作是一个无限序列（fi）i∈i，它是由i索引的k元素fi的i，只有有限多个非零fi。这项建设的形式化如下。

Given any set I viewed as an index set, let K(I) be the set of all functions f : I → K such that f(i) = 06 only for finitely many i ∈ I. As usual, denote such a function by (fi)i∈I; it is a family of finite support. We make K(I) into a vector space by defining addition and scalar multiplication by
 对于任何我视为索引集的集合，让k（i）是所有函数f:i→k的集合，这样f（i）=06只适用于有限多个i∈i。与通常一样，用（fi）i∈i表示该函数；它是一个有限支持族。通过定义加法和标量乘法，我们将k（i）转化为矢量空间。

(fi) + (gi) = (fi + gi) λ(fi) = (λfi).
 （fi）+（gi）=（fi+gi）λ（fi）=（λfi）。

the vector spaceThe family (ei)i∈IKis defined such that ((I), so that every w ∈ei)Kj (= 0I) can be uniquely written as a finite linearif j =6 i and (ei)i = 1. It is a basis of combination of the ei. There is also an injection ι: I → K(I) such that ι(i) = ei for every i ∈ I. Furthermore, it is easy to show that for any vector space F, and for any function h: I → F, there is a unique linear map h: K(I) → F such that h = h ◦ ι, as in the following diagram.
 向量空间家族（ei）i∈ik的定义是（（i），这样每个w∈ei）kj（=0i）都可以唯一地写为一个有限线性，如果j=6i和（ei）i=1。它是EI组合的基础。也有一个注入：i→k（i），使得（i）=ei对于每一个i∈i。此外，对于任何向量空间f，以及对于任何函数h:i→f，都有一个唯一的线性映射h:k（i）→f，这样h=h，如下图所示。

​                                                            I CCChCιCCCC/ CK!      (hI)
 我是CCCHC CCCC/CK！（嗨）

F
 f

Definition 32.5. The vector space (K(I),ι) constructed as above from a set I is called the free vector space generated by I (or over I). The commutativity of the above diagram is called the universal mapping property of the free vector space (K(I),ι) over I.
 定义32.5.由集合i如上构造的向量空间（k（i），称为i（或i）生成的自由向量空间。上图的交换性称为自由向量空间（k（i），）在i上的普遍映射性。

Using the proof technique of Proposition 32.5, it is not hard to prove that any two vector spaces satisfying the above universal mapping property are isomorphic.
 利用32.5命题的证明技术，不难证明满足上述普适映射性质的任意两个向量空间是同构的。

We can now return to the construction of tensor products. For simplicity consider two vector spaces E1 and E2. Whatever E1 ⊗ E2 and ϕ: E1 × E2 → E1 ⊗ E2 are, since ϕ is supposed to be bilinear, we must have
 现在我们可以回到张量积的构造。为了简单起见，考虑两个向量空间e1和e2。无论e1 e2和_：e1×e2→e1 e2是什么，既然_应该是双线性的，我们必须

ϕ(u1 + u2,v1) = ϕ(u1,v1) + ϕ(u2,v1) ϕ(u1,v1 + v2) = ϕ(u1,v1) + ϕ(u1,v2) ϕ(λu1,v1) = λϕ(u1,v1) ϕ(u1,µv1) = µϕ(u1,v1)
 ⑨（u1+u2，v1）＝（u1，v1）＋（u2，v1）⑨（u1，v1+v2）＝（u1，v1）＋（u1，v2）⑨（λu1，v1）＝（u1，v1）（u1，_v1）＝_（u1，v1）

for all u1,u2 ∈ E1, all v1,v2 ∈ E2, and all λ,µ ∈ K. Since E1 ⊗E2 must satisfy the universal mapping property of Definition 32.4, we may want to define1 2  E1 ⊗E2 as the free vector space1 2 K(E ×E ) generated by I = E1 ×E2 and let ϕ be the injection of E1 ×E2 into K(E ×E ). The problem is that in K(E1×E2), vectors such that
 对于所有的u1，u2∈e1，所有的v1，v2∈e2，和所有的λ，μ∈k，由于e1 e2必须满足定义32.4的普适映射性质，我们可以将1 2 e1 e2定义为i=e1×e2生成的自由矢量空间1 2 k（e×e），并让_为e1×e2注入k（e×e）。问题是，在k（e1×e2）中，向量

​                                              (u1 + u2,v1)    and    (u1,v1) + (u2,v2)
 （u1+u2，v1）和（u1，v1）+（u2，v2）

are different, when they should really be the same, since ϕ is bilinear. Since K(E1×E2) is free, there are no relations among the generators and this vector space is too big for our purpose.
 是不同的，当它们真的应该是相同的时候，因为_是双线性的。因为k（e1×e2）是自由的，所以发电机之间没有关系，这个矢量空间对于我们来说太大了。

The remedy is simple: take the quotient of the free vector space K(E1×E2) by the subspace
 补救方法很简单：用子空间取自由向量空间k（e1×e2）的商

N generated by the vectors of the form
 n由形式的向量生成

(u1 + u2,v1) − (u1,v1) − (u2,v1)
 （u1+u2，v1）−（u1，v1）−（u2，v1）

(u1,v1 + v2) − (u1,v1) − (u1,v2)
 （U1，V1+V2）−（U1，V1）−（U1，V2）

(λu1,v1) − λ(u1,v1) (u1,µv1) − µ(u1,v1).
 （λu1，v1）−λ（u1，v1）（u1，μv1）−μ（u1，v1）。

Then, if we let E1 ⊗ E2 be the quotient space K1(E12×E2)/N and let ϕ be the quotient map, this forces ϕ to be bilinear. Checking that (K(E ×E )/N,ϕ) satisfies the universal mapping property is straightforward. Here is the detailed construction.
 那么，如果我们让e1 e2为商空间k1（e12×e2）/n，并让e2为商映射，这将强制_为双线性。检查（k（e×e）/n，_）是否满足通用映射属性很简单。这是详细的结构。

Theorem 32.6. Given n ≥ 2 vector spaces E1,...,En, a tensor product (E1 ⊗ ··· ⊗ En,ϕ) for E1,...,En can be constructed. Furthermore, denoting ϕ(u1,...,un) as u1 ⊗···⊗un, the tensor product E1 ⊗ ··· ⊗ En is generated by the vectors u1 ⊗ ··· ⊗ un, where u1 ∈ E1,...,un ∈ En, and for every multilinear map f : E1 × ··· × En → F, the unique linear map f⊗ : E1 ⊗ ··· ⊗ En → F such that f = f⊗ ◦ ϕ is defined by
 定理32.6。给定n≥2个向量空间e1，…，en，可构造e1，…，en的张量积（e1···en，a）。此外，将_（u1，…，un）表示为u1················································································f=f _定义为

f⊗(u1 ⊗ ··· ⊗ un) = f(u1,...,un)
 f（u1····un）=f（u1，…，un）

on the generators u1 ⊗ ··· ⊗ un of E1 ⊗ ··· ⊗ En.
 在发电机上，e1··················en的U1······un

Proof. First we apply the construction of a free vector space to the cartesian product I = E1×···×En, obtaining the free vector space M = K(I) on I = E1×···×En. Since every basis generator ei ∈ M is uniquely associated with some n-tuple i = (u1,...,un) ∈ E1 ×···×En, we denote ei by (u1,...,un).
 证据。首先将自由向量空间的构造应用于笛卡尔积i=e1×·········×en，得到i=e1×·······×en上的自由向量空间m=k（i）。由于每一个基生成器ei∈m都与某个n元组i（u1，…，un）∈e1×·······×en唯一相关，因此我们用（u1，…，un）来表示ei。

Next let N be the subspace of M generated by the vectors of the following type:
 接下来，n是由以下类型的向量生成的m的子空间：

(u1,...,ui + vi,...,un) − (u1,...,ui,...,un) − (u1,...,vi,...,un), (u1,...,λui,...,un) − λ(u1,...,ui,...,un).
 （u1，…，ui+vi，…，un）-（u1，…，ui，…，un）-（u1，…，vi，…，un），（u1，…，λui，…，un）-λ（u1，…，ui，…，un）。

We let E1 ⊗···⊗En be the quotient M/N of the free vector space M by N, π: M → M/N be the quotient map, and set
 我们让e1····en是自由向量空间m的商m/n乘以n，π：m→m/n是商映射，并设置

ϕ = π ◦ ι.
 ⑨=π_。

By construction, ϕ is multilinear, and since π is surjective and the ι(i) = ei generate M, the fact that each i is of the form i = (u1,...,un) ∈ E1 × ··· × En implies that ϕ(u1,...,un) generate M/N. Thus, if we denote ϕ(u1,...,un) as u1 ⊗ ··· ⊗ un, the space E1 ⊗ ··· ⊗ En is generated by the vectors u1 ⊗ ··· ⊗ un, with ui ∈ Ei.
 通过构造，_是多行的，由于π是主观性的，且（i）=ei生成m，每个i的形式为i=（u1，…，un）∈e1×·····················································en由向量u1·····un生成，其中ui∈ei。

It remains to show that (E1 ⊗ ··· ⊗ En,ϕ) satisfies the universal mapping property. To1 n this end, we begin by proving there is a map h such that f = h ◦ ϕ1 . Sincen M = K(E ×···×E )
 仍需证明（e1····en，a）满足通用映射属性。为此，我们首先证明存在一个地图h，这样f=h_1。sincen m=k（e×····×e）

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

is free on I = E1 × ··· × En, there is a unique linear map f : K(E ×···×E ) → F, such that
 i=e1×e1······×en上是自由的，有一个独特的线性图f:k（e×e）·······×e）→f，这样

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

f = f ◦ ι,
 F=F_，

as in the diagram below.
 如下图所示。

​                                                E1 × ··· × En      ι  / K(E1×···×En) = M
 e1×····×en/k（e1×····×en）=m

SSSSSSSSSfSSSSSSSSS) 
 sssssssss）fssssssss）

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

Because f is multilinear, note that we must have f(w) = 0 for every w ∈ N; for example, on the generator
 因为f是多行的，请注意，对于每个w∈n，我们必须有f（w）=0；例如，在生成器上

(u1,...,ui + vi,...,un) − (u1,...,ui,...,un) − (u1,...,vi,...,un)
 （u1，…，ui+vi，…，un）-（u1，…，ui，…，un）-（u1，…，vi，…，un）

we have
 我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

But then, f : M → F factors through M/N, which means that there is a unique linear map
 然后，通过m/n得到f:m→f因子，这意味着存在一个唯一的线性映射。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

h: M/N → F such that f = h ◦ π making the following diagram commute
 h:m/n→f，使f=hπ作下表通勤

​                                                           M EEEπEEEE/EEM/N"  h
 m eeeπeeee/eem/n“H

f
 f

F,
 f

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

by defining h([z]) = f(z) for every z ∈ M, where [z] denotes the equivalence class in M/N
 通过定义h（[z]）=f（z），每个z∈m，其中[z]表示m/n中的等价类

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

of z ∈ M. Indeed, the fact that f vanishes on N insures that h is well defined on M/N, and
 实际上，f在n上消失的事实确保了h在m/n上定义良好，并且

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

it is clearly linear by definition. Since f = f ◦ ι, from the equation f = h ◦ π, by composing on the right with ι, we obtain
 根据定义，它显然是线性的。由于f=f_，从方程式f=h_π，通过在右边用_组合，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

f = f ◦ ι = h ◦ π ◦ ι = h ◦ ϕ,
 f=f_=h_π_=h_

as in the following commutative diagram.
 如下图所示。

E1 × ··· ×mmmnmmmmιmmmmK(E1×···×RERnRR)RRRπRRRRRKRR(( E1×···×En)/N mmm6
 e1×····················································

E
 e

RRRRRRRfRRRRRRRR( Ful lllllllhlllllll
 rrrrrrr frrrrrr（ful lllllll hlllll

We now prove the uniqueness of h. For any linear map f⊗ : E1 ⊗ ··· ⊗ En → F such that f = f⊗ ◦ ϕ, since the vectors u1 ⊗···⊗ un generate E1 ⊗···⊗ En and since ϕ(u1,...,un) = u1 ⊗ ··· ⊗ un, the map f⊗ is uniquely defined by
 我们现在证明H的唯一性。对于任何线性映射f：e1············································································

f⊗(u1 ⊗ ··· ⊗ un) = f(u1,...,un).
 f（u1····un）=f（u1，…，un）。

Since f = h ◦ ϕ, the map h is unique, and we let f⊗ = h.                                                               
 由于f=h_，地图h是唯一的，我们让f=h。

The map ϕ from E1 × ··· × En to E1 ⊗ ··· ⊗ En is often denoted by ι⊗, so that
 从e1×····×en到e1·····en的地图通常用表示，因此

ι⊗(u1,...,un) = u1 ⊗ ··· ⊗ un.
 （u1，…，un）=u1···un.

What is important about Theorem 32.6 is not so much the construction itself but the fact that it produces a tensor product with the universal mapping property with respect to multilinear maps. Indeed, Theorem 32.6 yields a canonical isomorphism
 关于定理32.6，重要的不是构造本身，而是它产生一个张量积，关于多行映射具有普遍映射性质。事实上，定理32.6给出了一个正则同构

L(E1 ⊗ ··· ⊗ En,F) ∼= L(E1,...,En;F)
 L（e1····en，f）=L（e1，…，en；f）

between the vector space of linear maps L(E1 ⊗ ··· ⊗ En,F), and the vector space of multilinear maps L(E1,...,En;F), via the linear map − ◦ ϕ defined by h 7→ h ◦ ϕ,
 在线性映射L（e1····en，f）的矢量空间和多行映射L（e1，…，en；f）的矢量空间之间，通过H 7→H _定义的线性映射−_，

where h ∈ L(E1 ⊗ ··· ⊗ En,F). Indeed, h ◦ ϕ is clearly multilinear, and since by Theorem 32.6, for every multilinear map f ∈ L(E1,...,En;F), there is a unique linear map f⊗ ∈ L(E1 ⊗ ··· ⊗ En,F) such that f = f⊗ ◦ ϕ, the map − ◦ ϕ is bijective. As a matter of fact, its inverse is the map
 式中h∈l（e1····en，f）。事实上，h是明显的多行的，并且根据定理32.6，对于每一个多行映射f∈l（e1，…，en；f），都有一个唯一的线性映射f∈l（e1···en，f），这样f=f，映射−是双目标的。事实上，它的反方向是地图

f 7→ f⊗.
 F 7→F。

We record this fact as the following proposition.
 我们将这一事实记录为以下命题。

Proposition 32.7. Given a tensor product (E1 ⊗ ··· ⊗ En,ϕ), the linear map h 7→ h ◦ ϕ is a canonical isomorphism
 提案32.7。给定张量积（e1·····en，η），线性映射h 7→h _是一个典型的同构。

L(E1 ⊗ ··· ⊗ En,F) ∼= L(E1,...,En;F)
 L（e1····en，f）=L（e1，…，en；f）

between the vector space of linear maps L(E1⊗···⊗En,F), and the vector space of multilinear maps L(E1,...,En;F).
 线性映射的向量空间L（e1·····en，f）与多行映射的向量空间L（e1，…，en；f）之间。

Using the “Hom” notation, the above canonical isomorphism is written
 使用“hom”表示法，写出上述规范同构。

Hom(E1 ⊗ ··· ⊗ En,F) ∼= Hom(E1,...,En;F).
 hom（e1····en，f）=hom（e1，…，en；f）。

Remarks:
 评论：

(1)    To be very precise, since the tensor product depends on the field K, we should subscript the symbol ⊗ with K and write
 更准确地说，由于张量积依赖于K域，我们应该在符号下加上K并写

E1 ⊗K ··· ⊗K En.
 e1 k····k en.

However, we often omit the subscript K unless confusion may arise.
 然而，我们经常省略下标k，除非出现混淆。

(2)    For F = K, the base field, Proposition 32.7 yields a canonical isomorphism between the vector space L(E1 ⊗ ··· ⊗ En,K), and the vector space of multilinear forms L(E1,...,En;K). However, L(E1 ⊗···⊗En,K) is the dual space (E1 ⊗···⊗En)∗, and thus the vector space of multilinear forms L(E1,...,En;K) is canonically isomorphic to (E1 ⊗ ··· ⊗ En)∗.
 对于f=k的基域，命题32.7给出了向量空间l（e1······en，k）与多行形式l（e1，…，en；k）的向量空间之间的规范同构。然而，L（e1···································································

Since this isomorphism is used often, we record it as the following proposition.
 由于这种同构常被使用，我们把它记为以下命题。

Proposition 32.8. Given a tensor product E1 ⊗···⊗En,, there is a canonical isomorphism
 提案32.8。给定张量积e1······en，存在一个正则同构。

L(E1,...,En;K) ∼= (E1 ⊗ ··· ⊗ En)∗
 L（e1，…，en；k）=（e1···en）

between the vector space of multilinear maps L(E1,...,En;K) and the dual (E1 ⊗···⊗En)∗ of the tensor product E1 ⊗ ··· ⊗ En.
 在多行映射的向量空间l（e1，…，en；k）和张量积e1············en的对偶空间之间。

The fact that the map ϕ: E1 × ··· × En → E1 ⊗ ··· ⊗ En is multilinear, can also be expressed as follows:
 图_：e1×·······················································

u1 ⊗ ··· ⊗ (vi + wi) ⊗ ··· ⊗ un = (u1 ⊗ ··· ⊗ vi ⊗ ··· ⊗ un) + (u1 ⊗ ··· ⊗ wi ⊗ ··· ⊗ un), u1 ⊗ ··· ⊗ (λui) ⊗ ··· ⊗ un = λ(u1 ⊗ ··· ⊗ ui ⊗ ··· ⊗ un).
 U1·····················································································；ui····un）。

Of course, this is just what we wanted!
 当然，这正是我们想要的！

Definition 32.6. Tensors in E1 ⊗ ··· ⊗ En are called n-tensors, and tensors of the form u1 ⊗···⊗un, where ui ∈ Ei are called simple (or decomposable) n-tensors. Those n-tensors that are not simple are often called compound n-tensors.
 定义32.6.e1····en中的张量称为n-张量，u1·······un形式的张量，其中ui∈ei称为简单（或可分解）n-张量。那些不简单的n-张量通常称为复合n-张量。

Not only do tensor products act on spaces, but they also act on linear maps (they are functors).
 张量积不仅作用于空间，而且作用于线性映射（它们是函子）。

Proposition 32.9. Given two linear maps f : E → E0 and g: F → F 0, there is a unique linear map
 提案32.9。给定两个线性映射f:e→e0和g:f→f 0，有一个唯一的线性映射

f ⊗ g: E ⊗ F → E0 ⊗ F 0
 F G:E F→e0 F 0

such that
 这样的话

(f ⊗ g)(u ⊗ v) = f(u) ⊗ g(v),
 （f g）（u v）=f（u）g（v）

for all u ∈ E and all v ∈ F.
 对于所有u∈e和所有v∈f。

Proof. We can define h: E × F → E0 ⊗ F 0 by
 证据。我们可以通过定义h:e×f→e0 f 0

h(u, v) = f(u) ⊗ g(v).
 h（u，v）=f（u）g（v）。

It is immediately verified that h is bilinear, and thus it induces a unique linear map
 立即证明H是双线性的，从而得到一个唯一的线性映射。

f ⊗ g: E ⊗ F → E0 ⊗ F 0
 F G:E F→e0 F 0

making the following diagram commutes
 使下图成为通勤路线

ι⊗
 γ

​                                                             E × F            / E ⊗ F
 E×F/E F

​                                                                LLLLhLLLLLL&  f⊗g
 llllhllll&f G

E0 ⊗ F 0,
 e0 f 0，

such that (f ⊗ g)(u ⊗ v) = f(u) ⊗ g(v), for all u ∈ E and all v ∈ F.                                                
 使（f g）（u v）=f（u）g（v），对于所有u∈e和所有v∈f。

Definition 32.7. The linear map f ⊗ g: E ⊗ F → E0 ⊗ F 0 given by Proposition 32.9 is called the tensor product of f : E → E0 and g: F → F 0.
 定义32.7.命题32.9给出的线性映射f g:e f→e0 f 0称为f:e→e0和g:f→f 0的张量积。

Another way to define f ⊗ g proceeds as follows. Given two linear maps f : E → E0 and g: F → F 0, the map f × g is the linear map from E × F to E0 × F 0 given by (f × g)(u,v) = (f(u),g(v)),  for all u ∈ E and all v ∈ F.
 定义f g的另一种方法如下。给定两个线性映射f:e→e0和g:f→f 0，映射f×g是由（f×g）（u，v）=（f（u），g（v））给出的从e×f到e0×f 0的线性映射，对于所有u∈e和所有v∈f。

Then the map h in the proof of Proposition 32.9 is given by h = ι0 ◦ (f × g), and f ⊗ g is ⊗
 则证明32.9的地图h由h=_0（f×g）给出，f g为

the unique linear map making the following diagram commute.
 唯一的线性地图，使以下图表通勤。

ι⊗
 γ

E × F / E ⊗ F f×gf⊗g
 E×F/E F×GF G

 

​                                                            E0 × F      0  / E ⊗ F 0
 e0×f 0/e f 0

ι⊗
 γ

Remark: The notation f⊗g is potentially ambiguous, because Hom(E,F) and Hom(E0,F 0) are vector spaces, so we can form the tensor product Hom(E,F)⊗Hom(E0,F 0) which contains elements also denoted f ⊗ g. To avoid confusion, the first kind of tensor product of linear maps defined in Proposition 32.9 (which yields a linear map in Hom(E ⊗F,E0 ⊗F 0)) can be denoted by T(f,g). If we denote the tensor product E ⊗F by T(E,F), this notation makes it clearer that T is a bifunctor. If E,E0 and F,F 0 are finite dimensional, by picking bases it is not hard to show that the map induced by f ⊗ g 7→ T(f,g) is an isomorphism Hom(E,F) ⊗ Hom(E0,F 0) ∼= Hom(E ⊗ F,E0 ⊗ F 0).
 注：符号f g可能不明确，因为hom（e，f）和hom（e0，f 0）是向量空间，所以我们可以形成张量积hom（e，f）hom（e0，f 0），其中包含也表示f g的元素。为了避免混淆，在命题中定义的线性映射的第一类张量积32.9（以hom（e f，e0 f 0）表示的线性图）可以用t（f，g）表示。如果我们用t（e，f）表示张量积e f，这个符号可以更清楚地表明t是双算符。如果e，e0和f，f 0是有限维的，通过选取基，不难证明f g 7→t（f，g）诱导的映射是同构hom（e，f）hom（e0，f 0）=hom（e f，e0 f 0）。

Proposition 32.10. Suppose we have linear maps f : E → E0, g: F → F 0, f0 : E0 → E00 and g0 : F 0 → F 00. Then the following identity holds:
 提案32.10。假设我们有线性映射f:e→e0，g:f→f 0，f0:e0→e00和g0:f 0→f 00。然后，以下身份保持不变：

​                                          (f0 ◦ f) ⊗ (g0 ◦ g) = (f0 ⊗ g0) ◦ (f ⊗ g).                                     (∗)
 （f0 f）（g0 g）=（f0 g0）（f g）.（）

| Proof.   We have the commutative diagram    证据。我们有交换图 |         |        |
| ------------------------------------------------------------ | ------- | ------ |
|                                                              | ι⊗    γ | /    / |

E × F E ⊗ F f×gf⊗g
 e×f e f×gf g

 

E0 × F / E0⊗F 0 f0×g0f0⊗g0
 e0×f/e0 f 0 f0×g0f0 g0

 

​                                                            E00F     00 / E00 ⊗ F 00,
 e00 f 00/e00 f 00，

ι⊗
 γ

| and   thus the commutative diagram.    因此是交换图。 |         |                  |
| ----------------------------------------------------- | ------- | ---------------- |
| E      F    EF                                        | ι⊗    γ | / E       F    f |

×⊗
 γ

(f0×g0)◦(f×g)(f0⊗g0)◦(f⊗g)
 （f0×g0）（f×g）（f0 g0）（f g）

 

​                                                            E00F       00 / E ⊗ F 00
 e00f 00/e f 00

ι⊗
 γ

We also have the commutative diagram.
 我们也有交换图。

ι⊗
 γ

​                                                             E × F              / E ⊗ F
 E×F/E F

(f0◦f)×(g0◦g)(f0◦f)⊗(g0◦g)
 （f0_f）×（g0 g）（f0_f）（g0 g）

 

​                                                          E00 × F  ι00⊗ / E ⊗ F 00.
 e00×f_00/e f 00.

Since we immediately verify that
 因为我们立即证实

(f0 ◦ f) × (g0 ◦ g) = (f0 × g0) ◦ (f × g),
 （f0 f）×（g0 g）=（f0×g0）（f×g）、

by uniqueness of the map between E ⊗ F and E00 ⊗ F 00 in the above diagram, we conclude that
 通过上图中E F和e00 F 00之间的映射的唯一性，我们得出：

(f0 ◦ f) ⊗ (g0 ◦ g) = (f0 ⊗ g0) ◦ (f ⊗ g),
 （f0 f）（g0 g）=（f0 g0）（f g）、

as claimed.                                                                                                                                         
 如要求。

The above formula (∗) yields the following useful fact.
 上述公式（）得出以下有用的事实。

Proposition 32.11.E0 ⊗ F 0 is also an isomorphism.If f : E → E0 and g: F → F 0 are isomorphims, then f ⊗ g: E ⊗ F →
 命题32.11.e0 f 0也是同构，如果f:e→e0和g:f→f 0是同构，那么f g:e f→

Proof. If f−1 : E0 →−1E⊗ is the inverse ofg−1 : E0 ⊗ F 0 → Ef⊗: EF →is the inverse ofE0 and g−1 : Ff 0⊗→g:FE is the inverse of⊗ F → E0 ⊗ F 0, g: F → F 0 , then f which is shown as follows:
 证据。如果f−1:e0→−1e是g−1:e0 f 0→ef：ef→是e0的倒数，g−1:ff 0→g:fe是f→e0 f 0，g:f→f 0的倒数，则f如下所示：

(f ⊗ g) ◦ (f−1 ⊗ g−1) = (f ◦ f−1) ⊗ (g ◦ g−1)
 （f g）（f−1 g−1）=（f f−1）（g g−1）

= idE0 ⊗ idF0 = idE0⊗F0,
 =ide0 idf0=ide0 f0，

and
 和

(f−1 ⊗ g−1) ◦ (f ⊗ g) = (f−1 ◦ f) ⊗ (g−1 ◦ g) = idE ⊗ idF = idE⊗F .
 （f−1 g−1）（f g）=（f−1 f）（g−1 g）=ide idf=ide f。

Therefore, f ⊗ g: E ⊗ F → E0 ⊗ F 0 is an isomorphism.                                                               
 因此，f g:e f→e0 f 0是同构的。

The generalization to the tensor product f1 ⊗ ··· ⊗ fn of n ≥ 3 linear maps fi : Ei → Fi is immediate, and left to the reader.
 n≥3线性映射fi:ei→fi的张量积f1······fn的推广是直接的，留给读者。

## 32.3        Bases of Tensor Products  32.3张量积的基

We showed that E1 ⊗···⊗En is generated by the vectors of the form u1 ⊗···⊗un. However, these vectors are not linearly independent. This situation can be fixed when considering bases.
 我们发现，e1·······en是由u1······un形式的向量生成的。然而，这些向量并不是线性无关的。这种情况可以在考虑基础时加以解决。

To explain the idea of the proof, consider the case when we have two spaces E and F both of dimension 3. Given a basis (e1,e2,e3) of E and a basis (f1,f2,f3) of F, we would like to prove that
 为了解释证明的概念，考虑当我们有两个空间e和f都是维3时的情况。给定e的基（e1，e2，e3）和f的基（f1，f2，f3），我们想证明

e1 ⊗ f1,     e1 ⊗ f2,   e1 ⊗ f3,   e2 ⊗ f1,   e2 ⊗ f2,   e2 ⊗ f3,   e3 ⊗ f1,   e3 ⊗ f2,     e3 ⊗ f3
 e1 f1，e1 f2，e1 f3，e2 f1，e2 f2，e2 f3，e3 f1，e3 f2，e3 f3

are linearly independent. To prove this, it suffices to show that for any vector space G, if w11,w12,w13,w21,w22,w23,w31,w32,w33 are any vectors in G, then there is a bilinear map h: E × F → G such that h(ei,ej) = wij, 1 ≤ i,j ≤ 3.
 线性无关。为了证明这一点，可以证明对于任何向量空间g，如果w11、w12、w13、w21、w22、w23、w31、w32、w33是g中的任何向量，则存在一个双线性映射h:e×f→g，使得h（e i，e j）=wij，1≤i，j≤3。

Because h yields a unique linear map h⊗ : E ⊗ F → G such that
 因为h产生一个独特的线性映射h：e f→g，这样

​                                                  h⊗(ei ⊗ ej) = wij,      1 ≤ i,j ≤ 3,
 h（ei ej）=wij，1≤i，j≤3，

and by Proposition 32.4, the vectors
 根据命题32.4，向量

e1 ⊗ f1,     e1 ⊗ f2,   e1 ⊗ f3,   e2 ⊗ f1,   e2 ⊗ f2,   e2 ⊗ f3,   e3 ⊗ f1,   e3 ⊗ f2,     e3 ⊗ f3
 e1 f1，e1 f2，e1 f3，e2 f1，e2 f2，e2 f3，e3 f1，e3 f2，e3 f3

are linearly independent. This suggests understanding how a bilinear function f : E×F → G is expressed in terms of its values f(ei,fj) on the basis vectors (e1,e2,e3) and (f1,f2,f3), and this can be done easily. Using bilinearity we obtain
 线性无关。这意味着要理解双线性函数f:e×f→g是如何在基向量（e1、e2、e3）和（f1、f2、f3）的基础上用其值f（ei、fj）表示的，并且这很容易做到。利用双线性我们得到

f(u1e1 + u2e2 + u3e3,v1f1 + v2f2 + v3f3) = u1v1f(e1,f1) + u1v2f(e1,f2) + u1v3f(e1,f3) + u2v1f(e2,f1) + u2v2f(e2,f2) + u2v3f(e2,f3)
 f（u1e1+u2e2+u3e3，v1f1+v2f2+v3f3）=u1v1f（e1，f1）+u1v2f（e1，f2）+u1v3f（e1，f3）+u2v1f（e2，f1）+u2v2f（e2，f2）+u2v3f（e2，f3）

\+ u3v1f(e3,f1) + u3v2f(e3,f2) + u3v3f(e3,f3). Therefore, given w11,w12,w13,w21,w22,w23,w31,w32,w33 ∈ G, the function h given by
 +U3V1F（E3，F1）+U3V2F（E3，F2）+U3V3F（E3，F3）。因此，给定w11、w12、w13、w21、w22、w23、w31、w32、w33∈g，由

h(u1e1 + u2e2 + u3e3,v1f1 + v2f2 + v3f3) = u1v1w11 + u1v2w12 + u1v3w13
 h（u1e1+u2e2+u3e3，v1f1+v2f2+v3f3）=u1v1w11+u1v2w12+u1v3w13

\+ u2v1w21 + u2v2w22 + u2v3w23
 +u2v1w21+u2v2w22+u2v3w23

\+ u3v1w31 + u3v2w33 + u3v3w33
 +U3V1W31+U3V2W33+U3V3W33

is clearly bilinear, and by construction h(ei,fj) = wij, so it does the job.
 很明显是双线性的，并且通过构造h（ei，fj）=wij，所以它完成了工作。

The generalization of this argument to any number of vector spaces of any dimension (even infinite) is straightforward.
 把这个论点推广到任何维（甚至无穷大）的任意数量的向量空间是很简单的。

Proposition 32.12. Given n ≥ 2 vector spaces  is a basis for Ek,
 提案32.12。如果n≥2个向量空间是Ek的基础，

1 ≤ k ≤ n, then the family of vectors
 1≤k≤n，则向量族

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

is a basis of the tensor product E1 ⊗ ··· ⊗ En.
 是张量积e1·····en的基础。


 

32.4. SOME USEFUL ISOMORPHISMS FOR TENSOR PRODUCTS
 32.4。张量积的一些有用同构

Proof. For each k, 1 ≤ k ≤ n, every vk ∈ Ek can be written uniquely as
 证据。对于每个k，1≤k≤n，每个vk∈ek可以唯一地写为

vk = Xvjkukj ,
 VK=XVJkukj，

j∈Ik
 杰克

for some family of scalars (vjk)j∈Ik. Let F be any nontrivial vector space. We show that for every family
 对于某些scalars家族（vjk）j∈ik。设f为任意非平凡向量空间。我们为每个家庭展示这一点

(wi1,...,in)(i1,...,in)∈I1×...×In,
 （wi1，…，in）（i1，…，in）∈i1×…×in，

of vectors in F, there is some linear map h: E1 ⊗ ··· ⊗ En → F such that
 在f中，有一些线性映射h:e1···en→f，这样

.
 .

Then by Proposition 32.4, it follows that
 然后，根据32.4号提案，它遵循了

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image016.gif)

is linearly independent. However, since ( is a basis for Ek, the  also generate E1 ⊗ ··· ⊗ En, and thus, they form a basis of E1 ⊗ ··· ⊗ En.
 是线性无关的。但是，由于（是EK的基础，也会生成e1······en，因此它们构成e1·····en的基础。

We define the function f : E1 × ··· × En → F as follows: For any n nonempty finite subsets J1,...,Jn such that Jk ⊆ Ik for k = 1,...,n,
 我们定义函数f:e1×································································································

.
 .

It is immediately verified that f is multilinear. By the universal mapping property of the tensor product, the linear map f⊗ : E1 ⊗ ··· ⊗ En → F such that f = f⊗ ◦ ϕ, is the desired map h.  
 立即证实f是多行的。根据张量积的普适映射性质，线性映射f：e1····en→f使得f=f _，是所需的映射h。

In particular, when each Ik is finite and of size mk = dim(Ek), we see that the dimension of the tensor product E1 ⊗ ··· ⊗ En is m1 ···mn. As a corollary of Proposition 32.12, if (uki )i∈Ik is a basis for Ek, 1 ≤ k ≤ n, then every tensor z ∈ E1 ⊗ ··· ⊗ En can be written in a unique way as
 特别是，当每个ik都是有限的，并且其尺寸为mk=dim（ek）时，我们可以看到张量积e1································作为32.12命题的推论，如果（uki）i∈i k是ek的基础，1≤k≤n，那么每个张量z∈e1····en都可以用一种独特的方式写成

​                                           z =              X         λi1,...,in u1i1 ⊗ ··· ⊗ unin,
 z=xλi1，…，单位：u1i1··uni，

(i1,...,in) ∈ I1×...×In
 （I1，…

for some unique family of scalars λi1,...,in ∈ K, all zero except for a finite number.
 对于某些唯一的标量族，在∈k中，除一个有限数外，其余均为零。

## 32.4                 Some Useful Isomorphisms for Tensor Products  32.4张量积的一些有用同构

Proposition 32.13. Given three vector spaces E,F,G, there exists unique canonical isomorphisms
 提案32.13。给定三个向量空间e，f，g，存在唯一的正则同构。

*(1)*     E ⊗ F ∼= F ⊗ E
 E F=F E

*(2)*     (E ⊗ F) ⊗ G ∼= E ⊗ (F ⊗ G) ∼= E ⊗ F ⊗ G
 （E F）G=E（F G）=E F G

*(3)*     (E ⊕ F) ⊗ G ∼= (E ⊗ G) ⊕ (F ⊗ G)
 （e_f）g～=（e g）（f g）

*(4)*     K ⊗ E ∼= E
 K E～E=E

such that respectively
 这样分别

*(a)*         u ⊗ v 7→ v ⊗ u
 U V 7→V U

*(b)*         (u ⊗ v) ⊗ w →7       u ⊗ (v ⊗ w) 7→       u ⊗ v ⊗ w
 （u v）w→7 u（v w）7→u v w

*(c)*          (u, v) ⊗ w →7 (u ⊗ w, v ⊗ w) (d) λ ⊗ u 7→ λu.
 （u，v）w→7（u w，v w）（d）λu 7→λu。

Proof. Except for (3), these isomorphisms are proved using the universal mapping property of tensor products.
 证据。除（3）外，利用张量积的普遍映射性质证明了这些同构。

(1)      The map from E × F to F ⊗ E given by (u,v) 7→ v ⊗ u is clearly bilinear, thus it induces a unique linear α: E ⊗ F → F ⊗ E making the following diagram commute
 由（u，v）7→v u给出的从e×f到f e的图显然是双线性的，因此它产生了一个独特的线性α：e f→f e，使下面的图表通勤

ι
 γ

*E*    × FLLLLL⊗LLLL/ LE%      ⊗ αF
 ×flllll llll/le%αf

*F*    ⊗ E,
 e，

such that
 这样的话

​                                     α(u ⊗ v) = v ⊗ u,       for all u ∈ E and all v ∈ F.
 α（u v）=v u，表示所有u∈e和所有v∈f。

Similarly, the map frominduces a unique linear βF: F× ⊗E Eto→E E⊗ ⊗F Fgiven by (making the following diagram commutev,u) 7→ u ⊗ v is clearly bilinear, thus it
 同样地，图中通过（制作下图commentv，u）7→u v明显是双线性的，从而产生了一个独特的线性βf:f×e to→e e e f fgiven，因此

ι
 γ

​                                                    F × ELLLLL⊗LLLL/ LF%   ⊗ βE
 F×elllll lll/lf%βe

E ⊗ F,
 E F，

such that
 这样的话

​                                      β(v ⊗ u) = u ⊗ v,       for all u ∈ E and all v ∈ F.
 β（v u）=u v，表示所有u∈e和所有v∈f。

It is immediately verified that
 立即证实

​                                (β ◦ α)(u ⊗ v) = u ⊗ v   and   (α ◦ β)(v ⊗ u) = v ⊗ u
 （βα）（u v）=u v和（αβ）（v u）=v u

for all u ∈ E and all v ∈ F. Since the tensors of the form u ⊗ v span E ⊗ F and similarly the tensors of the form v ⊗ u span F ⊗F E⊗, the mapE, so α andβ ◦βαare isomorphisms.is actually the identity on E ⊗ F, and similarly α ◦ β is the identity on
 对于所有u e和所有v f，由于形式u v SPAN e f的张量和形式v u SPAN f f e f的张量相似，因此，α和βα是同构的，实际上是e f上的恒等式，同样αβ是上的恒等式。

32.4. SOME USEFUL ISOMORPHISMS FOR TENSOR PRODUCTS
 32.4。张量积的一些有用同构

(2)      Fix some w ∈ G. The map
 固定一些w∈g.地图

(u, v) 7→ u ⊗ v ⊗ w
 （u，v）7→u v w

from E ×F to E ⊗F ⊗G is bilinear, and thus there is a linear map fw : E ⊗F → E ⊗F ⊗G making the following diagram commute
 从E×F到E F G是双线性的，因此有一个线性图fw:E F→E F G，使下面的图表成为通勤图

ι⊗
 γ

E × FOOOOOOOOOO/O'E ⊗ fwF
 e×foooooooo/o'e前

E ⊗ F ⊗ G,
 E F G，

with fw(u ⊗ v) = u ⊗ v ⊗ w.
 当fw（u v）=u v w时。

Next consider the map
 接下来看地图

(z, w) 7→ fw(z),
 （z，w）7→fw（z）

from (linear mapE ⊗ Ff : () ×EG⊗intoF) ⊗EG⊗→FE⊗⊗GF. It is easily seen to be bilinear, and thus it induces a⊗ G making the following diagram commute
 自（Linear Mape ff：（）×eg intof）eg→fe gf。很容易看出它是双线性的，因此它诱导a g，使下面的图表变为通勤

ι⊗
 γ

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

(E ⊗ F) ×RGRRRRRRRR/RR(RER( ⊗ Ff) ⊗ G
 （e f）×rgrrrrrrrr/rr（rr（ff）g

E ⊗ F ⊗ G,
 E F G，

with f((u ⊗ v) ⊗ w) = u ⊗ v ⊗ w.
 f（（u v）w）=u v w。

Also consider the map
 还要考虑地图

(u, v,w) 7→ (u ⊗ v) ⊗ w
 （u，v，w）7→（u v）w

fromE E×) ⊗FG×Gmaking the following diagram commuteto (E⊗F)⊗G. It is trilinear, and thus there is a linear map g: E⊗F ⊗G →
 frome e×）f g×gma在下图中绘制通勤（e f）g。它是三线的，因此有一个线性图g:e f g→

(    ⊗ F
 （F

ι⊗
 γ

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image018.gif)

E × F ×QGQQQQQQQQQQ/ QEQ( ⊗ F g⊗ G
 E×F×QGQQQQQQQ/QEQ（F G G

(E ⊗ F) ⊗ G,
 （E F）G，

with g(u ⊗ v ⊗ w) = (u ⊗ v) ⊗ w. Clearly, f ◦ g and g ◦ f are identity maps, and thus f and g are isomorphisms. The other case is similar.
 当g（u v w）=（u v）w时，显然，f g和g f是身份图，因此f和g是同构的。另一种情况类似。

(3)      Given a fixed vector space G, for any two vector spaces M and N and every linear map f : M → N, let τG(f) = f ⊗idG be the unique linear map making the following diagram commute.
 给定一个固定的向量空间g，对于任意两个向量空间m和n以及每一个线性映射f:m→n，让τg（f）=f idg成为唯一的线性映射，从而使下表通勤。

ιM⊗
 米尔

*M*    × G  / M ⊗ G
 ×g/m g

f×idGf⊗idG
 f×idgf idg

 

*N*     × G ιN⊗ / N ⊗ G
 ×g_n/n_g

The identity (∗) proved in Proposition 32.10 shows that if g: N → P is another linear map, then
 命题32.10中证明的恒等式（）表明，如果g:n→p是另一个线性映射，那么

τG(g) ◦ τG(f) = (g ⊗ idG) ◦ (f ⊗ idG) = (g ◦ f) ⊗ (idG ◦ idG) = (g ◦ f) ⊗ idG = τG(g ◦ f). Clearly, τG(0) = 0, and a direct computation on generators also shows that
 τg（g）τg（f）=（g idg）（f idg）=（g f）（idg idg）=（g f）idg=τg（g f）。显然，τg（0）=0，对发电机的直接计算也表明

τG(idM) = (idM ⊗ idG) = idM⊗G,
 τg（idm）=（idm idg）=idm g，

and that if f0 : M → N is another linear map, then
 如果f0:m→n是另一个线性映射，那么

τG(f + f0) = τG(f) + τG(f0).
 τg（f+f0）=τg（f）+τg（f0）。

In fancy terms, τG is a functor. Now, if E ⊕ F is a direct sum, it is a standard fact of linear algebra that if πE : E ⊕ F → E and πF : E ⊕ F → F are the projection maps, then
 用花哨的术语来说，τg是一个函数。现在，如果e f是一个直和，那么线性代数的标准事实是，如果πe:e f→e和πf:e f→f是投影图，那么

​       πE ◦ πE = πE      πF ◦ πF = πF       πE ◦ πF = 0      πF ◦ πE = 0       πE + πF = idE⊕F .
 πeπe=πeπfπf=πfπeπf=0πfπe=0πe+πf=ide f。

If we apply τG to these identites, we get
 如果我们把τg应用到这些标识上，我们得到

τG(πE) ◦ τG(πE) = τG(πE)      τG(πF ) ◦ τG(πF ) = τG(πF ) τG(πE) ◦ τG(πF ) = 0      τG(πF ) ◦ τG(πE) = 0      τG(πE) + τG(πF ) = id(E⊕F)⊗G.
 τg（πe）τg（πe）=τg（πe）τg（πf）τg（πf）=τg（πf）τg（πe）τg（πf）=0τg（πf）τg（πe）=0τg（πe）+τg（πf）=id（E f）g。

Observe that τG(πE) = πE ⊗idG is a map from (E ⊕F)⊗G onto E ⊗G and that τG(πF ) = πF ⊗idG is a map from (E ⊕F)⊗G onto F ⊗G, and by linear algebra, the above equations mean that we have a direct sum
 观察τg（πe）=πe idg是从（e f）g到e g的映射，τg（πf）=πf idg是从（e f）g到f g的映射，通过线性代数，上述方程意味着我们有一个直接和

(E ⊗ G) ⊕ (F ⊗ G) ∼= (E ⊕ F) ⊗ G.
 （e g）（f g）（e f）g.

(4) We have the linear mapgiven by
 （4）我们得到的线性映射由

​                                                                                  for all u ∈ E.
 对于所有的u∈e。

The map (λ,u) 7→ λu from K × E to E is bilinear, so it induces a unique linear map η: K ⊗ E → E making the following diagram commute
 从k×e到e的映射（λ，u）7→λu是双线性的，因此它归纳出一个唯一的线性映射η：k e→e，使下面的图表通勤

ι⊗
 γ

​                                                               K × E           / K ⊗ E
 K×E/K E

​                                                                LLLLLLLLLLL%       η
 lllllllll%η

E,
 E

such that η(λ ⊗ u) = λu, for all λ ∈ K and all u ∈ E. We have
 使得η（λu）=λu，对于所有的λ∈k和所有的u∈e，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image020.gif)

and
 和

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image022.gif)

which shows that both are the identity, soare isomorphisms.                                                      
 这说明两者都是同一性的，翱翔同构。


 

Remark: The isomorphism (3) can be generalized to finite and even arbitrary direct sums Li∈I Ei of vector spaces (where I is an arbitrary nonempty index set). We have an isomorphism
 注：同构（3）可推广到向量空间的有限甚至任意直和li∈i ei（其中i是任意非空索引集）。我们有同构

.
 .

This isomorphism (with isomorphism (1)) can be used to give another proof of Proposition 32.12 (see Bertin [15], Chapter 4, Section 1) or Lang [106], Chapter XVI, Section 2).
 这种同构（与同构（1））可用于证明命题32.12（见Bertin[15]，第4章，第1节）或Lang[106]，第十六章，第2节）。

Proposition 32.14. Given any three vector spaces E,F,G, we have the canonical isomorphism
 提案32.14。给定任意三个向量空间e，f，g，我们有正则同构

Hom(E,F;G) ∼= Hom(E,Hom(F,G)).
 hom（e，f；g）=hom（e，hom（f，g））。

Proof. Any bilinear map f : E × F → G gives the linear map ϕ(f) ∈ Hom(E,Hom(F,G)), where ϕ(f)(u) is the linear map in Hom(F,G) given by
 证据。任何双线性图f:e×f→g给出线性图（f）∈hom（e，hom（f，g）），其中（f）（u）是hom（f，g）中的线性图，由下式给出

ϕ(f)(u)(v) = f(u,v).
 ⑨（f）（u）（v）=f（u，v）。

Conversely, given a linear map g ∈ Hom(E,Hom(F,G)), we get the bilinear map ψ(g) given by ψ(g)(u,v) = g(u)(v),
 反之，给定线性映射g∈hom（e，hom（f，g）），得到由ψ（g）（u，v）=g（u）（v）给出的双线性映射ψ（g）。

and it is clear that ϕ and ψ and mutual inverses.                                                                           
 很明显，ψ和ψ和相互反比。

Since by Proposition 32.7 there is a canonical isomorphism
 因为在32.7命题中，有一个典型的同构

Hom(E ⊗ F,G) ∼= Hom(E,F;G),
 hom（e f，g）=hom（e，f；g），

together with the isomorphism
 以及同构

Hom(E,F;G) ∼= Hom(E,Hom(F,G))
 hom（e，f；g）=hom（e，hom（f，g））

given by Proposition 32.14, we obtain the important corollary:
 由32.14号命题给出，我们得到了重要的推论：

Proposition 32.15. For any three vector spaces E,F,G, we have the canonical isomorphism
 提案32.15。对于任意三个向量空间e，f，g，我们都有正则同构。

Hom(E ⊗ F,G) ∼= Hom(E,Hom(F,G)).
 hom（e f，g）=hom（e，hom（f，g））。

## 32.5         Duality for Tensor Products  32.5张量积的对偶性

In this section all vector spaces are assumed to have finite dimension, unless specified otherwise. Let us now see how tensor products behave under duality. For this, we define a pairing between and E1⊗···⊗En as follows: For any fixed (, we have the multilinear map
 在本节中，除非另有规定，否则假设所有向量空间都有有限维。现在让我们看看张量积在二元性下的行为。为此，我们定义了和e1·····en之间的配对，如下所示：对于任何固定的（，我们都有多行映射

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image024.gif)

from E1 × ··· × En to K. The map extends uniquely to a linear map making the following diagram commute.
 从e1×······································

ι⊗
 γ

​                                                  E1 × ··· × En          / E1 ⊗ ··· ⊗ En
 e1×····×en/e1····en

SSSSSSSSSSSSSSSS) KLv1∗,...,vn∗
 ssssssssssss）klv1，…，vn

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image026.gif)

We also have the multilinear map
 我们还有多行地图

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image028.gif)

fromto Hom(E1 ⊗···⊗En,K), which extends to a unique linear map L from  to Hom(E1 ⊗ ··· ⊗ En,K) making the following diagram commute.
 From to Hom（e1·················································

/
 /

UUULUvU1∗U,...,vUUUUn∗UUUUUU* L
 Uuuluvu1 u，…，Vuuuuun Uuuuuu*l

Hom(E1 ⊗ ··· ⊗ En;K)
 hom（e1···en；k）

However, in view of the isomorphism
 然而，鉴于同构

Hom(U ⊗ V,W) ∼= Hom(U,Hom(V,W))
 hom（u v，w）=hom（u，hom（v，w））。

given by Proposition 32.15, with and W = K, we can view L as a linear map
 由命题32.15给出，当且w=k时，我们可以把l看作一个线性映射。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image030.gif)

which corresponds to a bilinear map
 对应双线性图

​                                                                                                                                                     (††)
 （††）

via the isomorphism (U ⊗ V )∗ ∼= Hom(U,V ;K) given by Proposition 32.8. This pairing is given explicitly on generators by
 通过32.8号命题给出的同构（u v）～=hom（u，v；k）。这种配对在发电机上是通过

.
 .

This pairing is nondegenerate, as proved below.
 如下文所述，这种配对是非退化的。

Proof. If () are bases for E1,...,En, then for every basis element
 证据。如果（）是e1，…，en的基，则表示每个基元素

, and any basis element,
 以及任何基本元素，

we have
 我们有

​                                                                            ···                                           ,
 ···我是说，

where δij is Kronecker delta, defined such that δij = 1 if i = j, and 0 otherwise. Given any , assume that hα,βi = 0 for all β ∈ E1 ⊗···⊗En. The vector α is a finite linear combination, for some unique λi1,...,in ∈ K. If we choose, then we get
 式中，δi j为Kronecker delta，定义如下：如果i=j，δij=1，否则为0。假设hα，βi=0代表所有β∈e1·····en。向量α是一个有限线性组合，对于一些唯一的λi1，…，在∈k中，如果我们选择，那么我们得到

0 = hα,e1i1 ⊗ ··· ⊗ enini = DXλi1,...,in(e1i1)∗ ⊗ ··· ⊗ (einn)∗,ei11 ⊗ ··· ⊗ einnE
 0=Hα，e1i1···enini=dxλi1，…，in（e1i1）···（einn），ei11···einne

= Xλi1,...,inh(e1i1)∗ ⊗ ··· ⊗ (einn)∗,e1i1 ⊗ ··· ⊗ enini
 =xλi1，…，inh（e1i1）·····（einn），e1i1····enini

= λi1,...,in.
 =λi1，…，英寸

Therefore, α = 0,
 因此α=0，

Conversely, given any β ∈ E1⊗···⊗En, assume that hα,βi = 0, for all. The vector β is a finite linear combination, for some unique λi1,...,in ∈ K. If we choose, then we get
 相反，假设任何β∈e1·····en，假设hα，βi=0。向量β是一个有限线性组合，对于一些唯一的λi1，…，在∈k中，如果我们选择，那么我们得到

0 = h(e1i1)∗ ⊗ ··· ⊗ (enin)∗,βi = D(ei11)∗ ⊗ ··· ⊗ (einn)∗,Xλi1,...,ine1i1 ⊗ ··· ⊗ eninE = Xλi1,...,inh(e1i1)∗ ⊗ ··· ⊗ (einn)∗,e1i1 ⊗ ··· ⊗ enini
 0=H（e1i1）·······（enin），βi=D（ei11）·········（einn），xλi1，…，ine1i1····················································

= λi1,...,in.
 =λi1，…，英寸

Therefore, β = 0.                                                                                                                                
 因此，β=0。

By Proposition 32.1, we have a canonical isomorphism
 根据命题32.1，我们有一个规范同构

.
 .

Here is our main proposition about duality of tensor products. Proposition 32.16. We have canonical isomorphisms
 这是我们关于张量积二元性的主要命题。提案32.16。我们有规范同构

,
 ，

and
 和

Hom(E1,...,En;K).
 hom（e1，…，en；k）。

Proof. The second isomorphism follows from the isomorphism ( together with the isomorphism Hom(E1,...,En;K) ∼= (E1 ⊗···⊗En)∗ given by Proposition
 证据。第二个同构来自同构（连同同构hom（e1，…，en；k）=（e1···en）由命题给出。

32.8.                                                                                                                                                    
 32.8。

Remarks:
 评论：

\1.    The isomorphism Hom(E1,...,En;K) can be described explicitly as the linear extension toof the map given by
 同构hom（e1，…，en；k）可以明确地描述为映射的线性延伸

.
 .

\2.    The canonical isomorphism of Proposition 32.16 holds under more general conditions. Namely, that K is a commutative ring with identity and that the Ei are finitelygenerated projective K-modules (see Definition 34.7). See Bourbaki, [25] (Chapter III, §11, Section 5, Proposition 7).
 命题32.16的规范同构在更一般的条件下成立。也就是说，k是一个具有同一性的交换环，ei是有限生成的射影k模（见定义34.7）。见Bourbaki，[25]（第三章，第11节，第5节，提案7）。

We prove another useful canonical isomorphism that allows us to treat linear maps as tensors.
 我们证明了另一个有用的正则同构，它允许我们把线性映射看作张量。

Let E and F be two vector spaces and let α: E∗ × F → Hom(E,F) be the map defined such that α(u∗,f)(x) = u∗(x)f,
 设e和f为两个向量空间，设α：e×f→hom（e，f）为定义的映射，α（u，f）（x）=u（x）f，

for all u∗ ∈ E∗, f ∈ F, and x ∈ E. This map is clearly bilinear, and thus it induces a linear map α⊗ : E∗ ⊗ F → Hom(E,F) making the following diagram commute
 对于所有u e，f f，和x e，该图显然是双线性的，因此它归纳出一个线性图α：e f→hom（e，f），使下面的图通勤

​                                                         E∗ × F      ι⊗   / E∗ ⊗ F
 E×F/E F

​                                                           OOOOOαOOOOOO'  α⊗
 OOOOOαOOOOOα_

Hom(E,F),
 霍姆（E，F）

such that α⊗(u∗ ⊗ f)(x) = u∗(x)f.
 这样α（u f）（x）=u（x）f.

Proposition 32.17. If E and F are vector spaces (not necessarily finite dimensional), then the following properties hold:
 提案32.17。如果e和f是向量空间（不一定是有限维），则以下属性成立：

*(1)*     The linear map α⊗ : E∗ ⊗ F → Hom(E,F) is injective.
 线性映射α：e f→hom（e，f）是内射的。

*(2)*     If E is finite-dimensional, then α⊗ : E∗ ⊗F → Hom(E,F) is a canonical isomorphism.
 如果e是有限维，那么α：e f→hom（e，f）是规范同构。

*(3)*     If F is finite-dimensional, then α⊗ : E∗ ⊗F → Hom(E,F) is a canonical isomorphism.
 如果f是有限维，那么α：e f→hom（e，f）是规范同构。

Proof. (1) Let (e∗i )i∈I be a basis of E∗ and let (fj)j∈J be a basis of F. Then we know that (e∗i ⊗fj)i∈I,j∈J is a basis of E∗ ⊗F. To prove that α⊗ is injective, let us show that its kernel is reduced to (0). For any vector
 证据。（1）让（e i）i i为e的基，让（f j）j j为f的基，则我们知道（e i fj）i i，j j是e f的基，为了证明α是内射的，让我们证明它的核是（0）的。对于任何向量

ω = X λij e∗i ⊗ fj
 ω=xλij e i fj

i∈I0,j∈J0
 i∈i0，j∈j0

in E∗ ⊗ F, with I0 and J0 some finite sets, assume that α⊗(ω) = 0. This means that for every x ∈ E, we have α⊗(ω)(x) = 0; that is,
 在e f中，对于i0和j0一些有限集，假设α（ω）=0。这意味着，对于每一个x∈e，我们有α（ω）（x）=0；也就是说，

.
 .

Since (fj)j∈J is a basis of F, for every j ∈ J0, we must have
 因为（f j）j∈j是f的基础，对于每一个j∈j0，我们必须

​                                                     Xλije∗i (x) = 0,        for all x ∈ E.
 xλije i（x）=0，对于所有x∈e。

i∈I0
 我喜欢

But then (e∗i )i∈I0 would be linearly dependent, contradicting the fact that (e∗i )i∈I is a basis of E∗, so we must have
 但是（e i）i i0是线性相关的，这与（e i）i i是e i的基础这一事实相矛盾，因此我们必须

​                                               λij = 0,       for all i ∈ I0 and all j ∈ J0,
 λi j=0，对于所有i∈i0和所有j∈j0，

which shows that ω = 0. Therefore, α⊗ is injective.
 这表明ω=0。因此，α是注射剂。

(2) Let (ej)1≤j≤n be a finite basis of E, and as usual, let e∗j ∈ E∗ be the linear form defined by
 （2）让（e j）1≤j≤n是e的有限基，通常，让e j∈e是由

e∗j(ek) = δj,k,
 e j（Ek）=δj，k，

where δj,k = 1 iff j = k and 0 otherwise. We know that (e∗j)1≤j≤n is a basis of E∗ (this is where we use the finite dimension of E). For any linear map f ∈ Hom(E,F), for every x = x1e1 + ··· + xnen ∈ E, we have
 式中，δj，k=1 iff j=k，否则为0。我们知道（e j）1≤j≤n是e的基础（这是我们使用e的有限维的地方）。对于任何线性映射f∈hom（e，f），对于每个x=x1e1+·····+xnen∈e，我们有

.
 .

Consequently, every linear map f ∈ Hom(E,F) can be expressed as
 因此，每个线性映射f∈hom（e，f）可以表示为

,
 ，

for some fi ∈ F. Furthermore, if we apply f to ei, we get f(ei) = fi, so the fi are unique. Observe that
 对于某些fi∈f，而且，如果将f应用于ei，我们得到f（ei）=fi，因此fi是唯一的。注意

.
 .

Thus, α⊗ is surjective, so α⊗ is a bijection.
 因此，α是可预测的，因此α是双射。

(3) Let (f1,...,fm) be a finite basis of F, and let () be its dual basis. Given any linear map h: E → F, for all u ∈ E, since
 （3）设（f1，…，fm）为f的有限基，设（）为其对偶基。给定任意线性映射h:e→f，对于所有u∈e，因为

.
 .

If
 如果

​                                                                                      for all u ∈ E                                              (∗)
 对于所有u∈e（）

for some linear forms (, then
 对于一些线性形式（，那么

​                                                                )                                   for all u ∈ E,
 ）对于所有u∈e，

which shows that vi∗ = fi∗ ◦ h for i = 1,...,m. This means that h has a unique expression in terms of linear forms as in (∗). Define the map α from (E∗)m to Hom(E,F) by
 这表明，对于i=1，…，m，vi=fi h。这意味着h在线性形式方面有一个独特的表达式，如（）所示。定义从（e）m到hom（e，f）的映射α

​                                                                                                for all u ∈ E.
 对于所有的u∈e。

This map is linear. For any h ∈ Hom(E,F), we showed earlier that the expression of h in (∗) is unique, thus α is an isomorphism. Similarly, E∗ ⊗ F is isomorphic to (E∗)m. Any tensor ω ∈ E∗ ⊗ F can be written as a linear combination
 这张地图是线性的。对于任何h∈hom（e，f），我们之前已经证明h在（）中的表达是唯一的，因此α是同构的。同样，e f同构于（e）m。任何张量ω∈e f都可以写成线性组合。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image032.gif)

for some and some yk ∈ F, and since (f1,...,fm) is a basis of F, each yk can be written as a linear combination of (f1,...,fm), so ω can be expressed as
 对于一些和一些yk∈f，由于（f1，…，fm）是f的基础，每个yk可以写成（f1，…，fm）的线性组合，因此ω可以表示为

​                                                                             ,                                                                         (†)
 ，（？）

for some linear forms which are linear combinations of the. If we pick a basis
 对于一些线性形式，它们是的线性组合。如果我们选择一个基础

(this implies that thewi∗)i∈I for E∗, then we know that the family (vi∗ in (†) are unique. Define the linear mapwi∗ ⊗ fj)i∈I,1≤j≤mβis a basis offrom (E∗)m toE∗E⊗∗ ⊗F, andF by
 （这意味着wi）i i代表e，那么我们知道家族（vi in（†）是独一无二的。定义线性映射wi f j）i∈i，1≤j≤mβ是（e）m toe e f的基

.
 .

Since every tensor ω ∈ E∗ ⊗ F can be written in a unique way as in (†), this map is an isomorphism.       
 由于每一张量ω∈e f都可以用与（†）中一样的独特方式书写，因此该图是同构的。

Note that in Proposition 32.17, we have an isomorphism if either E or F has finite dimension. The following proposition allows us to view a multilinear as a tensor product.
 注意，在命题32.17中，如果e或f有有限维，我们有同构。下面的命题允许我们将多行视为张量积。

Proposition 32.18. If the E1,...En are finite-dimensional vector spaces and F is any vector space, then we have the canonical isomorphism Hom(
 提案32.18。如果e1，…（

Proof. In view of the canonical isomorphism
 证据。从规范同构看

Hom(E1,...,En;F) ∼= Hom(E1 ⊗ ··· ⊗ En,F)
 hom（e1，…，en；f）=hom（e1··en，f）

given by Proposition 32.7 and the canonical isomorphism (
 由32.7命题和正则同构给出（

given by Proposition 32.16, if the Ei’s are finite-dimensional, then Proposition 32.17 yields the canonical isomorphism
 由命题32.16给出，如果ei是有限维的，那么命题32.17产生正则同构。

Hom(
 霍姆

as claimed.                                                                                                                                         
 如要求。


 

## 32.6       Tensor Algebras  32.6张量代数

Our goal is to define a vector space T(V ) obtained by taking the direct sum of the tensor products
 我们的目标是定义一个向量空间t（v），该向量空间t（v）是通过取张量积的直接和得到的。

,
 ，

and to define a multiplication operation on T(V ) which makes T(V ) into an algebraic structure called an algebra. The algebra T(V ) satisfies a universal property stated in Proposition 32.19, which makes it the “free algebra” generated by the vector space V . Definition 32.8. The tensor product
 在t（v）上定义一个乘法运算，使t（v）成为称为代数的代数结构。代数t（v）满足命题32.19中所述的一个普适性，这使得它成为向量空间v生成的“自由代数”。定义32.8.张量积

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image034.gif)

is also denoted as
 也表示为

​                                                                      or        V ⊗m
 或V m

and is called the m-th tensor power of V (with V ⊗1 = V , and V ⊗0 = K).
 称为v的m次张量幂（v 1=v，v 0=k）。

We can pack all the tensor powers of V into the “big” vector space
 我们可以把V的张量幂压缩到“大”向量空间中。

T(V ) = M V ⊗m,
 t（v）=m v m，

m≥0
 m 0

denoted T •(V ) or NV to avoid confusion with the tangent bundle.
 表示t•（v）或nv，以避免与切线束混淆。

This is an interesting object because we can define a multiplication operation on it which makes it into an algebra.
 这是一个有趣的对象，因为我们可以在它上面定义一个乘法运算，使它成为一个代数。

When V is of finite dimension n, we can pick some basis (e1 ...,en) of V , and then every tensor ω ∈ T(V ) can be expressed as a linear combination of terms of the form ei1 ⊗···⊗eik, where (i1,...,ik) is any sequence of elements from the set {1,...,n}. We can think of the tensors ei1 ⊗···⊗eik as monomials in the noncommuting variables e1,...,en. Thus the space T(V ) corresponds to the algebra of polynomials with coefficients in K in n noncommuting variables.
 当v为有限维n时，我们可以选取v的一些基（e1…，en），然后每个张量ω∈t（v）可以表示为ei1·······eik形式的项的线性组合，其中（i1，…，ik）是集合1，…，n中的任何元素序列。我们可以把张量Ei1·····Eik看作非定变量e1，…，en中的单项式。因此，空间t（v）对应于n个非交换变量中系数为k的多项式代数。

Let us review the definition of an algebra over a field. Let K denote any (commutative) field, although for our purposes, we may assume that K = R (and occasionally, K = C). Since we will only be dealing with associative algebras with a multiplicative unit, we only define algebras of this kind.
 让我们回顾一个领域上代数的定义。让k表示任何（交换）场，尽管为了我们的目的，我们可以假设k=r（偶尔，k=c）。因为我们只处理带乘法单位的结合代数，所以我们只定义这种代数。

Definition 32.9. Given a field K, a K-algebra is a K-vector space A together with a bilinear operation ·: A × A → A, called multiplication, which makes A into a ring with unity 1 (or 1A, when we want to be very precise). This means that · is associative and that there is a multiplicative identity element 1 so that 1 · a = a · 1 = a, for all a ∈ A. Given two K-algebras A and B, a K-algebra homomorphism h: A → B is a linear map that is also a ring homomorphism, with h(1A) = 1B; that is,
 定义32.9.对于一个k域，k-代数是一个k-向量空间a加上一个双线性运算·：a×a→a，称为乘法，它使a变成一个单位为1的环（当我们想非常精确的时候，也可以称为1a）。这意味着·是关联的，并且有一个乘法恒等元1，因此1·a=a·1=a，对于所有a∈a。给定两个k-代数a和b，k-代数同态h:a→b是一个线性映射，也是一个环同态，h（1a）=1b；也就是说，

h(a1 · a2) = h(a1) · h(a2) for all a1,a2 ∈ A h(1A) = 1B.
 h（a1·a2）=h（a1）·h（a2）表示所有a1，a2∈a h（1a）=1b。

The set of K-algebra homomorphisms between A and B is denoted Homalg(A,B).
 在a和b之间的k-代数同态集合称为homalg（a，b）。

For example, the ring Mn(K) of all n × n matrices over a field K is a K-algebra.
 例如，域k上所有n×n矩阵的环mn（k）是k-代数。

There is an obvious notion of ideal of a K-algebra.
 有一个关于k-代数理想的明显概念。

Definition 32.10. Let A be a K-algebra. An ideal A ⊆ A is a linear subspace of A that is also a two-sided ideal with respect to multiplication in A; this means that for all a ∈ A and all α,β ∈ A, we have αaβ ∈ A.
 定义32.10。让a成为k-代数。理想a a是a的线性子空间，也是a中关于乘法的双面理想；这意味着对于所有a∈a和所有α，β∈a，我们都有αaβ∈a。

If the field K is understood, we usually simply say an algebra instead of a K-algebra.
 如果能理解k域，我们通常只说代数而不是k代数。

We would like to define a multiplication operation on T(V ) which makes it into a Kalgebra. As
 我们要在t（v）上定义一个乘法运算，使它成为一个Kalgebra。AS

T(V ) = M V ⊗i,
 t（v）=m v i，

i≥0
 我超过0岁

for every i ≥ 0, there is a natural injection ιn : V ⊗n → T(V ), and in particular, an injection ι0 : K → T(V ). The multiplicative unit 1 of T(V ) is the image ι0(1) in T(V ) of the unit 1 of the field K. Since every v ∈ T(V ) can be expressed as a finite sum
 对于每一个i≥0，有一个自然的注入n:v n→t（v），特别是注入0:k→t（v）。t（v）的乘性单位1是k场的单位1的t（v）中的图像_0（1）。因为每个v∈t（v）都可以表示为一个有限和。

v = ιn1(v1) + ··· + ιnk(vk),
 V=_n1（v1）+····+nk（vk）、

where vi ∈ V ⊗ni and the ni are natural numbers with ni =6   nj if i =6 j, to define multiplication in T(V ), using bilinearity, it is enough to define multiplication operations
 其中，v i∈v ni和ni是自然数，ni=6 nj，如果i=6 j，用t（v）定义乘法，用双线性定义乘法运算就足够了。

·: V ⊗m × V ⊗n −→ V ⊗(m+n), which, using the isomorphisms V ⊗n ∼= ιn(V ⊗n), yield multiplication operations ·: ιm(V ⊗m) × ιn(V ⊗n) −→ ιm+n(V ⊗(m+n)). First, for ω1 ∈ V ⊗m and ω2 ∈ V ⊗n, we let ω1 · ω2 = ω1 ⊗ ω2.
 ·：v m×v n−→v（m+n），使用同构v n=n（v n），产生乘法运算·：m（v m）×n（v n）−→m+n（v（m+n））。首先，对于ω1∈v m和ω2∈v n，我们假设ω1·ω2=ω1ω2。

This defines a bilinear map so it defines a multiplication V ⊗m × V ⊗n −→ V ⊗m ⊗ V ⊗n. This is not quite what we want, but there is a canonical isomorphism
 这定义了一个双线性映射，因此它定义了一个乘法v m×v n−→v m v n。这不是我们想要的，但有一个规范的同构

V ⊗m ⊗ V ⊗n ∼= V ⊗(m+n)
 V m V n=V（m+n）

which yields the desired multiplication ·: V ⊗m × V ⊗n −→ V ⊗(m+n).
 得到所需的乘法·：v m×v n−→v（m+n）。

The isomorphism V ⊗m ⊗ V ⊗n ∼= V ⊗(m+n) can be established by induction using the isomorphism (E ⊗ F) ⊗ G ∼= E ⊗ F ⊗ G. First we prove by induction on m ≥ 2 that
 同构v m v n=v（m+n）可通过使用同构（e f）g=e f g的诱导建立。首先，我们通过在m≥2上的诱导证明

V ⊗(m−1) ⊗ V ∼= V ⊗m,
 V（m-1）V=V m，

and then by induction on n ≥ 1 than
 然后在n≥1上感应

V ⊗m ⊗ V ⊗n ∼= V ⊗(m+n).
 v m v n=v（m+n）。

In summary the multiplication V ⊗m × V ⊗n −→ V ⊗(m+n) is defined so that
 总之，乘法v m×v n−→v（m+n）的定义是：

(v1 ⊗ ··· ⊗ vm) · (w1 ⊗ ··· ⊗ wn) = v1 ⊗ ··· ⊗ vm ⊗ w1 ⊗ ··· ⊗ wn.
 （v1····vm）·（w1·············································

(This has to be made rigorous by using isomorphisms involving the associativity of tensor products, for details, see Jacobson [95], Section 3.9, or Bertin [15], Chapter 4, Section 2.)
 （这必须通过使用涉及张量积关联性的同构来严格，有关详细信息，请参见Jacobson[95]，第3.9节或Bertin[15]，第4章，第2节。）

Definition 32.11. Given a K-vector space V (not necessarily finite dimensional), the vector space
 定义32.11.给定一个k向量空间v（不一定是有限维），向量空间

T(V ) = M V ⊗m
 t（v）=m v m

m≥0
 m 0

denoted T •(V ) or NV equipped with the multiplication operations V ⊗m×V ⊗n −→ V ⊗(m+n) defined above is called the tensor algebra of V .
 表示t•（v）或nv，配上上面定义的乘法运算v m×v n−→v（m+n），称为v的张量代数。

Remark: It is important to note that multiplication in T(V ) is not commutative. Also, in all rigor, the unit 1 of T(V ) is not equal to 1, the unit of the field K. However, in view of the injection ι0 : K → T(V ), for the sake of notational simplicity, we will denote 1 by 1. More generally, in view of the injections ιn : V ⊗n → T(V ), we identify elements of V ⊗n with their images in T(V ).
 注：重要的是要注意t（v）中的乘法不是交换的。同样，严格地说，t（v）的单位1不等于场k的单位1。然而，考虑到注入_0:k→t（v），为了便于记法，我们将用1表示1。一般来说，考虑到注入n:v n→t（v），我们用t（v）中的图像识别v n的元素。

The algebra T(V ) satisfies a universal mapping property which shows that it is unique up to isomorphism. For simplicity of notation, let i: V → T(V ) be the natural injection of V into T(V ).
 代数t（v）满足一个普适映射性质，表明它在同构方面是唯一的。为了便于记法，让i:v→t（v）是v自然地注入t（v）。

Proposition 32.19. Given any K-algebra A, for any linear map f : V → A, there is a
 提案32.19。对于任何k-代数a，对于任何线性映射f:v→a，有一个

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image035.gif)

unique K-algebra homomorphism f : T(V ) → A so that
 唯一的k-代数同态f:t（v）→a，因此

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

f = f ◦ i,
 f=f_i，

as in the diagram below.
 如下图所示。

V EEEfEEiEE/EET" (Vf )
 v eeefeeee/eet（VF）

A
 一

Proof. Left an an exercise (use Theorem 32.6). A proof can be found in Knapp [102] (Appendix A, Proposition A.14) or Bertin [15] (Chapter 4, Theorem 2.4). 
 证据。留下一个练习（使用定理32.6）。可在Knapp[102]中（附录A，提案A.14）或Bertin[15]中找到证据（第4章，定理2.4）。

Proposition 32.19 implies that there is a natural isomorphism
 命题32.19意味着存在一个自然同构

Homalg(T(V ),A) ∼= Hom(V,A),
 homalg（t（v），a）=hom（v，a），

where the algebra A on the right-hand side is viewed as a vector space. Proposition 32.19 also has the following corollary.
 右边的代数A被视为向量空间。命题32.19也有以下推论。

Proposition 32.20. Given a linear map h: V1 → V2 between two vectors spaces V1,V2 over a field K, there is a unique K-algebra homomorphism ⊗h: T(V1) → T(V2) making the following diagram commute.
 提案32.20。在两个向量空间v1，v2之间的线性映射h:v1→v2在一个域k上，有一个独特的k-代数同态h:t（v1）→t（v2），使得下面的图变为通勤图。

i1
 I1

​                                                                  V           / T(V1)
 V/T（v1）

h⊗h 
 H·H

​                                                                 V2        / T(V2).
 V2/T（V2）。

Most algebras of interest arise as well-chosen quotients of the tensor algebra T(V ). This is true for the exterior algebra V(V ) (also called Grassmann algebra), where we take the quotient of T(V ) modulo the ideal generated by all elements of the form v ⊗ v, where v ∈ V ,and for the symmetric algebra Sym(V ), where we take the quotient of T(V ) modulo the ideal generated by all elements of the form v ⊗ w − w ⊗ v, where v,w ∈ V .
 大多数感兴趣的代数都出现在张量代数t（v）的商中。对于外部代数v（v）（也称为格拉斯曼代数），我们取t（v）模的商为形式v v的所有元素生成的理想，其中v∈v；对于对称代数sym（v），我们取t（v）模的商为形式v v的理想。形式为v w w v的l元素，其中v，w∈v。

Algebras such as T(V ) are graded in the sense that there is a sequence of subspaces
 像t（v）这样的代数在存在一系列子空间的意义上是分级的。

V ⊗n ⊆ T(V ) such that
 v n t（v）使得

T(V ) = MV ⊗n,
 T（V）=mV N，

k≥0
 K＝0

and the multiplication ⊗ behaves well w.r.t. the grading, i.e., ⊗: V ⊗m × V ⊗n → V ⊗(m+n).
 乘法表现良好，即：v m×v n→v（m+n）。

Definition 32.12. A K-algebra E is said to be a graded algebra iff there is a sequence of subspaces En ⊆ E such that
 定义32.12.一个k-代数e被称为一个等级代数，如果有一个子空间序列en e，那么

E = MEn,
 E=男性，

k≥0
 K＝0

(with E0 = K) and the multiplication · respects the grading; that is, ·: Em × En → Em+n. Elements in En are called homogeneous elements of rank (or degree) n.
 （e0=k），乘法表示等级，即：em×en→em+n。en中的元素称为秩（或度）n的齐次元素。

In differential geometry and in physics it is necessary to consider slightly more general tensors.
 在微分几何和物理学中，有必要考虑稍微更一般的张量。

Definition 32.13. Given a vector space V , for any pair of nonnegative integers (r,s), the tensor space Tr,s(V ) of type (r,s) is the tensor product
 定义32.13.给定向量空间v，对于任意一对非负整数（r，s），（r，s）类型的张量空间tr，s（v）是张量积。

,
 ，

with T0,0(V ) = K. We also define the tensor algebra T •,•(V ) as the direct sum (coproduct)
 当t0,0（v）=k时，我们也将张量代数t•，•（v）定义为直接和（副积）

T •,•(V ) = M Tr,s(V ).
 t•，•（v）=m tr，s（v）。

r,s≥0
 r，s≥0

Tensors in Tr,s(V ) are called homogeneous of degree (r,s).
 在tr，s（v）中的张量称为度的齐次（r，s）。

Note that tensors in Tr,0(V ) are just our “old tensors” in V ⊗r. We make T •,•(V ) into an algebra by defining multiplication operations
 请注意，t r，0（v）中的张量只是v r中的“旧张量”。我们通过定义乘法运算将t•，•（v）转化为代数。

Tr1,s1(V ) × Tr2,s2(V ) −→ Tr1+r2,s1+s2(V )
 tr1，s1（v）×tr2，s2（v）−→tr1+r2，s1+s2（v）

in the usual way, namely: For and
 以通常的方式，即：对于和

, let
 让

.
 .

Denote by Hom() the vector space of all multilinear maps from V r × (V ∗)s to W. Then we have the universal mapping property which asserts that there is a canonical isomorphism
 用hom（）表示从v r×（v）s到w的所有多行映射的向量空间，然后我们得到一个普适映射性质，即存在一个规范同构。

Hom(Tr,s(V ),W) ∼= Hom(.
 hom（tr，s（v），w）=hom（.

In particular,
 特别地，

(Tr,s(V ))∗ ∼= Hom(.
 （tr，s（v））～=hom（.

For finite dimensional vector spaces, the duality of Section 32.5 is also easily extended to the tensor spaces Tr,s(V ). We define the pairing
 对于有限维向量空间，第32.5节的对偶性也很容易扩展到张量空间tr，s（v）。我们定义了配对

Tr,s(V ∗) × Tr,s(V ) −→ K
 Tr，S（V）×Tr，S（V）−→K

as follows: if
 如下：如果

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image037.gif)

and
 和

,
 ，

then
 然后

.
 .

This is a nondegenerate pairing, and thus we get a canonical isomorphism (Tr,s(V ))∗ ∼= Tr,s(V ∗).
 这是一个非退化配对，因此我们得到一个正则同构（tr，s（v））～=tr，s（v）。

Consequently, we get a canonical isomorphism
 因此，我们得到了一个正则同构。

Tr,s(V ∗) ∼= Hom(.
 tr，s（v）=hom（.

We summarize these results in the following proposition.
 我们将这些结果概括为以下命题。

Proposition 32.21. Let V be a vector space and let
 提案32.21。设V为向量空间，设

.
 .

We have the canonical isomorphisms
 我们有规范同构

(Tr,s(V ))∗ ∼= Tr,s(V ∗),
 （tr，s（v））～=tr，s（v），

and
 和

Tr,s(V ∗) ∼= Hom(.
 tr，s（v）=hom（.

Remark: The tensor spaces, Tr,s(V ) are also denoted ). A tensor α ∈ Tr,s(V ) is said to be contravariant in the first r arguments and covariant in the last s arguments.
 注：张量空间tr，s（v）也表示。张量α∈tr，s（v）在第一个r变元中是反变的，在最后一个s变元中是协变的。

This terminology refers to the way tensors behave under coordinate changes. Given a basis
 这个术语指的是张量在坐标变化下的行为方式。有根据的

) denotes the dual basis, then every tensor α ∈ Tr,s(V ) is given
 ）表示对偶基，然后给出每个张量α∈tr，s（v）

by an expression of the form
 通过形式的表达

α = X aij11,...,i,...,jrsei1 ⊗ ··· ⊗ eir ⊗ e∗j1 ⊗ ··· ⊗ e∗js.
 α=x aij11，…，i，…，jrsei1··············································

i1,...,ir j1,...,js
 I1，…，IR J1，…，JS

The tradition in classical tensor notation is to use lower indices on vectors and upper indices on linear forms and in accordance to Einstein summation convention (or Einstein notation) the position of the indices on the coefficients is reversed. Einstein summation convention (already encountered in Section 32.1) is to assume that a summation is performed for all values of every index that appears simultaneously once as an upper index and once as a lower index. According to this convention, the tensor α above is written
 经典张量记法的传统是在向量上使用低指数，在线性形式上使用高指数，并且根据爱因斯坦求和约定（或爱因斯坦记法），指数在系数上的位置是相反的。爱因斯坦求和约定（已在第32.1节中遇到）假设对同时出现一次作为上索引和一次作为下索引的每个索引的所有值进行求和。根据这个惯例，上面的张量α是写的

.
 .

An older view of tensors is that they are multidimensional arrays of coefficients,
 张量的一个古老观点是它们是系数的多维数组，

,
 ，

subject to the rules for changes of bases.
 以基地变更规则为准。

Another operation on general tensors, contraction, is useful in differential geometry.
 对一般张量收缩的另一个运算在微分几何中很有用。

Definition 32.14. For all r,s ≥ 1, the contraction ci,j : Tr,s(V ) → Tr−1,s−1(V ), with 1 ≤ i ≤ r and 1 ≤ j ≤ s, is the linear map defined on generators by
 定义32.14.对于所有r，s≥1，收缩ci，j:tr，s（v）→tr−1，s−1（v），其中1≤i≤r和1≤j≤s，是发电机上定义的线性映射

ci,j(u1 ⊗ ··· ⊗ ur ⊗ v1∗ ⊗ ··· ⊗ vs∗)
 Ci，J（U1·······v1···vs）

= vj∗(ui)u1 ⊗ ··· ⊗ ubi ⊗ ··· ⊗ ur ⊗ v1∗ ⊗ ··· ⊗ vbj∗ ⊗ ··· ⊗ vs∗,
 =vj（ui）u1······························································

where the hat over an argument means that it should be omitted.
 在一个论点上的帽子意味着它应该被省略。

Let us figure our what is c1,1 : T1,1(V ) → R, that is c1,1 : V ⊗ V ∗ → R. If (e1,...,en) is a basis of V and () is the dual basis, by Proposition 32.17 every h ∈ V ⊗ V ∗ ∼= Hom(V,V ) can be expressed as
 让我们来计算我们的c1,1:t1,1（v）→r，即c1,1:v v→r。如果（e1，…，en）是v的基，并且（）是对偶基，根据命题32.17，每个h∈v v=hom（v，v）可以表示为

.
 .

As
 AS

,
 ，

we get
 我们得到

,
 ，

where tr(h) is the trace of h, where h is viewed as the linear map given by the matrix, (aij). Actually, since c1,1 is defined independently of any basis, c1,1 provides an intrinsic definition of the trace of a linear map h ∈ Hom(V,V ).
 其中，tr（h）是h的迹线，其中h是矩阵（aij）给出的线性映射。实际上，由于c1,1是独立于任何基础定义的，c1,1提供了线性映射H∈hom（v，v）轨迹的内在定义。

Remark: Using the Einstein summation convention, if
 备注：如果

,
 ，

then
 然后

.
 .

If E and F are two K-algebras, we know that their tensor product E ⊗ F exists as a vector space. We can make E ⊗ F into an algebra as well. Indeed, we have the multilinear map
 如果e和f是两个k-代数，我们知道它们的张量积e f作为向量空间存在。我们也可以把e f变成代数。实际上，我们有多行地图

E × F × E × F −→ E ⊗ F
 E×F×E×F−→E F

given by (a,b,c,d) 7→F(. By the universal mapping property, we get a linear map,ac) ⊗ (bd), where ac is the product of a and c in E and bd is the
 由（a，b，c，d）7→f（.根据通用映射性质，我们得到一个线性映射，a c）（bd），其中ac是e中a和c的乘积，bd是

product of b and d in
 B和D的乘积

E ⊗ F ⊗ E ⊗ F −→ E ⊗ F.
 E F E F−→E F.

Using the isomorphism
 使用同构

E ⊗ F ⊗ E ⊗ F ∼= (E ⊗ F) ⊗ (E ⊗ F),
 E F E F～=（E F）（E F），

we get a linear map
 我们得到一张线性地图

(E ⊗ F) ⊗ (E ⊗ F) −→ E ⊗ F,
 （E F）（E F）−→E F，

and thus a bilinear map,
 因此双线性图，

(E ⊗ F) × (E ⊗ F) −→ E ⊗ F
 （E F）×E F−→E F

which is our multiplication operation in E ⊗ F. This multiplication is determined by
 这是我们在e f中的乘法运算。这个乘法是由

(a ⊗ b) · (c ⊗ d) = (ac) ⊗ (bd).
 （a b）·（c d）=（ac）（bd）。

In summary we have the following proposition.
 总之，我们有以下建议。

Proposition 32.22. Given two K-algebra E and F, the operation on E ⊗ F defined on generators by
 提案32.22。给定两个k-代数e和f，在e f上的运算由

(a ⊗ b) · (c ⊗ d) = (ac) ⊗ (bd)
 （a b）·（c d）=（ac）（bd）

makes E ⊗ F into a K-algebra.
 使e f变成k-代数。

We now turn to symmetric tensors.
 现在我们来讨论对称张量。

## 32.7        Symmetric Tensor Powers  32.7对称张量幂

Our goal is to come up with a notion of tensor product that will allow us to treat symmetric multilinear maps as linear maps. Note that we have to restrict ourselves to a single vector space E, rather then n vector spaces E1,...,En, so that symmetry makes sense. Definition 32.15. A multilinear map f : En → F is symmetric iff
 我们的目标是提出张量积的概念，使我们能够将对称多线性映射视为线性映射。注意，我们必须把自己限制在一个向量空间e，而不是n个向量空间e1，…，en，这样对称才有意义。定义32.15。多行映射f:en→f是对称iff

f(uσ(1),...,uσ(n)) = f(u1,...,un),
 f（uσ（1），…，uσ（n））=f（u1，…，un）

for all ui ∈ E and all permutations, σ: {1,...,n} → {1,...,n}. The group of permutations on {1,...,n} (the symmetric group) is denoted Sn. The vector space of all symmetric multilinear maps f : En → F is denoted by Symn(E;F) or Homsymlin(En,F). Note that Sym1(E;F) = Hom(E,F).
 对于所有ui∈e和所有置换，σ：1，…，n→1，…，n。在1，…，n（对称群）上的排列群表示sn。所有对称多行映射f:en→f的向量空间用symn（e；f）或homsymlin（en，f）表示。注意sym1（e；f）=hom（e，f）。

We could proceed directly as in Theorem 32.6 and construct symmetric tensor products from scratch. However, since we already have the notion of a tensor product, there is a more economical method. First we define symmetric tensor powers.
 我们可以像定理32.6那样直接进行，从头开始构造对称张量积。然而，由于我们已经有了张量积的概念，所以有一种更经济的方法。首先我们定义对称张量幂。

Definition 32.16. An n-th symmetric tensor power of a vector space E, where n ≥ 1, is a vector space S together with a symmetric multilinear map ϕ: En → S such that, for every vector space F and for every symmetric multilinear map f : En → F, there is a unique linear map, with
 定义32.16。向量空间e的第n次对称张量幂，其中n≥1，是向量空间s加上对称多行映射，因此，对于每个向量空间f和每个对称多行映射f:en→f，都有一个唯一的线性映射，其中

,
 ，

for all u1,...,un ∈ E, or for short
 对于所有的u1，…，un∈e，或简称

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image039.gif)

Equivalently, there is a unique linear map f such that the following diagram commutes.
 同样地，有一个独特的线性图f，如下图表通勤。

​                                                                    En    ϕ   / S
 _/s

CCCCCCCC!        ff
 中交委！FF

F
 f

The above property is called the universal mapping property of the symmetric tensor power (S,ϕ).
 上述性质称为对称张量幂（S，_）的普适映射性质。

We next show that any two symmetric n-th tensor powers (S1,ϕ1) and (S2,ϕ2) for E are isomorphic.
 接下来我们证明任意两个对称的n阶张量幂（s1，_）和（s2，_）对于e是同构的。

Proposition 32.23. Given any two symmetric n-th tensor powers (S1,ϕ1) and (S2,ϕ2) for E, there is an isomorphism h: S1 → S2 such that
 提案32.23。对于e，给定任意两个对称n阶张量幂（s1，_）和（s2，_），存在同构h:s1→s2，这样

ϕ2 = h ◦ ϕ1.
 _2=H_1.


 

32.7. SYMMETRIC TENSOR POWERS
 32.7。对称张量幂

Proof. Replace tensor product by n-th symmetric tensor power in the proof of Proposition
 证据。在命题证明中用n次对称张量幂代替张量积

32.5.                                                                                                                                                    
 32.5。

We now give a construction that produces a symmetric n-th tensor power of a vector space E.
 我们现在给出一个构造，它产生一个向量空间e的对称n次张量幂。

Theorem 32.24. Given a vector space E, a symmetric n-th tensor power (Sn(E),ϕ) for
 定理32.24。给定一个向量空间e，对称n阶张量幂（sn（e），a），用于

E can be constructed (n ≥ 1). Furthermore, denoting , the symmetric tensor power Sn(E) is generated by the vectors, where u1,...,un ∈ E, and for every symmetric multilinear map f : En → F, the unique linear map such that is defined by
 e可构造（n≥1）。此外，表示对称张量幂sn（e）是由向量生成的，其中，u1，…，un∈e，对于每个对称多行映射f:en→f，唯一的线性映射，其定义如下：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image041.gif)

on the generators of Sn(E).
 在sn（e）的发电机上。

Proof. The tensor power E⊗n is too big, and thus we define an appropriate quotient. Let C be the subspace of E⊗n generated by the vectors of the form
 证据。张量幂E n太大，因此我们定义了一个适当的商。设c为由形式向量生成的e n的子空间。

u1 ⊗ ··· ⊗ un − uσ(1) ⊗ ··· ⊗ uσ(n),
 U1···Un−Uσ（1）···Uσ（n）、

for all ui ∈ E, and all permutations σ: {1,...,n} → {1,...,n}. We claim that the quotient space (E⊗n)/C does the job.
 对于所有的ui∈e，和所有的置换σ：1，…，n→1，…，n。我们声称商空间（e n）/c起作用。

Let p: E⊗n → (E⊗n)/C be the quotient map, and let ϕ: En → (E⊗n)/C be the map given by
 设p:e n→（e n）/c为商映射，设a:en→（e n）/c为下式给出的映射

ϕ = p ◦ ϕ0,
 _=P__0，

where ϕ0 : En → E⊗n is the injection given by ϕ0(u1,...,un) = u1 ⊗ ··· ⊗ un.
 式中，ω0:e n→e n为ω0（u1，…，un）=u1··un给出的注入量。

Let us denote. It is clear that ϕ is symmetric. Since the vectors u1 ⊗ ··· ⊗ un generate E⊗n, and p is surjective, the vectors generate (E⊗n)/C.
 让我们来说明一下。很明显，Ф是对称的。由于向量u1····un生成e n，而p是可预测的，因此向量生成（e n）/c。

It remains to show that ((E⊗n)/C,ϕ) satisfies the universal mapping property. To this end we begin by proving that there is a map h such that f = h ◦ ϕ. Given any symmetric multilinear map f : En → F, by Theorem 32.6 there is a linear map f⊗ : E⊗n → F such that f = f⊗ ◦ ϕ0, as in the diagram below.
 仍需证明（（e n）/c，η）满足通用映射属性。为此，我们首先证明有一个地图h，这样f=h_。根据定理32.6，对于任何对称多行映射f:e n→f，都有一个线性映射f：e n→f，这样f=f _0，如下图所示。

​                                                                   En   ϕ0 / E⊗n
 _0/e n

FFFFFFFFF#     f⊗ f
 fffffffff f f

F
 f

However, since f is symmetric, we haven)/C → F making the following diagram commute.f⊗(z) = 0 for every z ∈ C. Thus, we get an induced linear map h: (E⊗
 然而，由于f是对称的，所以我们得到了/c→f，使下面的图表通勤。f（z）=0，对于每个z∈c，我们得到了一个诱导线性映射h：（e

E<⊗nK yyϕy0yyyyyy⊗KKKKKpKKKK% n)/C
 E<NK YY_Y0YYYY KKKKK PKKKK%n）/C

EnEEEfEEEEEE"f yrrrrrrhrrr(rE⊗
 Eneefeeee“f yrrrrhrrr（re_

F
 f

If we define h([z]) = f⊗(z) for every z ∈ E⊗n, where [z] is the equivalence class in (E⊗n)/C of z ∈ E⊗n, the above diagram shows that f = h ◦ p ◦ ϕ0 = h ◦ ϕ. We now prove the uniqueness of h. For any linear map  such that , since
 如果我们定义h（[z]）=f（z）为每个z∈e n，其中[z]是z∈e n的（e n）/c中的等价类，上图显示f=h p _0=h _。我们现在证明了H.对于任何线性映射的唯一性，因为

and the vectors  generate (E⊗n)/C, the map f
 向量生成（e n）/c，图f

is uniquely defined by
 由唯一定义

.
 .

Since f = h ◦ ϕ, the map h is unique, and we let . Thus, Sn(E) = (E⊗n)/C and ϕ constitute a symmetric n-th tensor power of E. 
 由于f=h_，地图h是唯一的，我们让。因此，sn（e）=（e n）/c和ξ构成e的对称n阶张量幂。

The map ϕ from En to Sn(E) is often denoted ι, so that
 从en到sn（e）的图_通常表示为_，因此

.
 .

Again, the actual construction is not important. What is important is that the symmetric n-th power has the universal mapping property with respect to symmetric multilinear maps.
 同样，实际施工也不重要。重要的是对称n次幂对对称多行映射具有普遍的映射性质。

Remark: The notation  for the commutative multiplication of symmetric tensor powers is not standard. Another notation commonly used is ·. We often abbreviate “symmetric tensor power” as “symmetric power.” The symmetric power Sn(E) is also denoted SymnE but we prefer to use the notation Sym to denote spaces of symmetric multilinear maps. To be consistent with the use of , we could have used the notation Jn E. Clearly, S1(E) ∼= E and it is convenient to set S0(E) = K.
 注：对称张量幂的交换乘法符号不规范。另一个常用的符号是·。我们通常把“对称张量幂”简称为“对称幂”，对称幂sn（e）也表示为symne，但我们更喜欢用sym表示对称多线性映射的空间。为了与的用法一致，我们可以使用符号Jn e。很明显，s1（e）=e，并且设置S0（e）=k很方便。

The fact that the map ϕ: En → Sn(E) is symmetric and multilinear can also be expressed as follows:
 图_：en→sn（e）是对称的，多行也可以表示为：

,
 ，

for all permutations σ ∈ Sn.
 对于所有置换，σ∈sn。

The last identity shows that the “operation”  is commutative. This allows us to view the symmetric tensor as an object called a multiset.
 最后一个恒等式表明“运算”是交换的。这允许我们将对称张量看作一个称为多重集的对象。

32.7. SYMMETRIC TENSOR POWERS
 32.7。对称张量幂

Given a set A, a multiset with elements from A is a generalization of the concept of a set that allows multiple instances of elements from A to occur. For example, if A = {a,b,c,d}, the following are multisets:
 给定一个集合A，包含a元素的多集是集合概念的一个推广，该集合允许出现a元素的多个实例。例如，如果A=A、B、C、D，则以下是多集：

M1 = {a,a,b}, M2 = {a,a,b,b,c}, M3 = {a,a,b,b,c,d,d,d}.
 M1=A，A，B，M2=A，A，B，B，C，M3=A，A，B，B，C，D，D，D。

Here is another way to represent multisets as tables showing the multiplicities of the elements in the multiset:
 下面是另一种将多集表示为显示多集中元素多重性的表的方法：

 .
 .

The above are just graphs of functions from the set A = {a,b,c,d} to N. This suggests the following definition.
 以上只是从集合A=A、B、C、D到N的函数图。这表明了以下定义。

Definition 32.17. A finite multiset M over a set A is a function M : A → N such that M(a) = 06 for finitely many a ∈ A. The multiplicity of an element a ∈ A in M is M(a). The set of all multisets over A is denoted by N(A), and we let dom(M) = {a ∈ A | M(a) = 06 }, which is a finite set. The set dom(M) is the set of elements in A that actually occur in
 定义32.17。在集合A上的有限多集M是一个函数m:a→n，这样m（a）=06表示有限多a∈a。在m中，元素a∈a的多重性是m（a）。a上所有多集的集合用n（a）表示，我们让dom（m）=a∈a m（a）=06，这是一个有限集。set dom（m）是a中实际发生的元素集。

MmultisetP. For any multiseta∈dom(AA) Mand is called the(a), and domM ∈(MsizeN)(A)is finite; this sum is the total number of elements in the, note thatof M. Let |MP|a∈=APMa(∈aA)Mmakes sense, since(a).                                                                                                                        Pa∈A M(a) =
 多集。对于任意多集合∈dom（a a）m and称为（a），而dom∈（msizen）（a）是有限的；这个和是m中的元素总数，注意m的元素总数。让mp a∈=apma（∈aa）mmakes sense，因为（a）.pa∈a m（a）=

Going back to our symmetric tensors, we can view the tensors of the form as multisets of size n over the set E.
 回到对称张量，我们可以把形式的张量看作是集合e上大小为n的多集合。

Theorem 32.24 implies the following proposition.
 定理32.24包含以下命题。

Proposition 32.25. There is a canonical isomorphism
 提案32.25。有一个典型的同构

Hom(Sn(E),F) ∼= Symn(E;F),
 hom（sn（e），f）=symn（e；f），

between the vector space of linear maps Hom(Sn(E),F) and the vector space of symmetric multilinear maps Symn(E;F) given by the linear map − ◦ ϕ defined by h 7→ h ◦ ϕ, with h ∈ Hom(Sn(E),F).
 在线性映射的向量空间hom（sn（e），f）和对称多线性映射的向量空间symn（e；f）之间，由h 7→h_定义的线性映射−_给出，其中h∈hom（sn（e），f）。

Proof. The map h ◦ ϕ is clearly symmetric multilinear. By Theorem 32.24, for every symmetric multilinear map f ∈ Symn(E;F) there is a unique linear map Hom(Sn(E),F) such that, so the map − ◦ ϕ is bijective. Its inverse is the map. 
 证据。地图H_是清晰对称的多行。根据定理32.24，对于每一个对称多行映射f∈symn（e；f），都有一个唯一的线性映射hom（sn（e），f），因此该映射−是双射的。与之相反的是地图。

In particular, when F = K, we get the following important fact. Proposition 32.26. There is a canonical isomorphism
 特别是，当f=k时，我们得到以下重要事实。提案32.26。有一个典型的同构

(Sn(E))∗ ∼= Symn(E;K).
 （sn（e））～=symn（e；k）。

Definition 32.18. Symmetric tensors in Sn(E) are called symmetric n-tensors, and tensors of the form, where ui ∈ E, are called simple (or decomposable) symmetric ntensors. Those symmetric n-tensors that are not simple are often called compound symmetric n-tensors.
 定义32.18。sn（e）中的对称张量称为对称n张量，其中ui∈e形式的张量称为简单（或可分解）对称张量。那些不简单的对称n-张量通常称为复合对称n-张量。

Given two linear maps f : E → E0 and g: E → E0, since the map ) is bilinear and symmetric, there is a unique linear map  making the following diagram commute.
 给定两个线性映射f:e→e0和g:e→e0，由于该映射）是双线性和对称的，因此有一个唯一的线性映射使下面的图变为通勤图。

/
 /

​                                                               f×g                      
 F×G

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image042.gif)

/ S2(E0).
 /s2（e0）。

Observe thatis determined by
 观察这是由

.
 .

Proposition 32.27. Given any linear maps f : E → E0, g: E → E0, f0 : E0 → E00, and g0 : E0 → E00, we have
 提案32.27。对于任何线性映射f:e→e0，g:e→e0，f0:e0→e00和g0:e0→e00，我们有

.
 .

The generalization to the symmetric tensor product 3 linear maps fi : E → E0 is immediate, and left to the reader.
 对称张量积3线性映射fi:e→e0的推广是直接的，留给读者。

## 32.8        Bases of Symmetric Powers  32.8对称幂的基

The vectorswhere u1,...,um ∈ E generate Sm(E), but they are not linearly independent. We will prove a version of Proposition 32.12 for symmetric tensor powers using multisets.
 其中U1，…，Um∈e产生Sm（e），但它们不是线性无关的。我们将证明一个关于使用多重集的对称张量幂的32.12命题的版本。

Recall that a (finite) multiset over a set I is a function M : I → N, such that M(i) = 06 for finitely many i ∈ I. The set of all multisets over I is denoted as N(I) and we let dom(M) = {i ∈ I | M(i) = 06 }, the finite set of elements in I that actually occur in M. The size of the multiset M is |M| = Pa∈A M(a).
 回想一个集合i上的（有限）多集是一个函数m:i→n，这样m（i）=06表示有限多i∈i。i上所有多集的集合表示为n（i），我们让dom（m）=i∈i m（i）=06，i中实际出现的有限元素集m。多集m的大小是m=pa∈a m（a）。

To explain the idea of the proof, consider the case when m = 2 and E has dimension 3. Given a basis (e1,e2,e3) of E, we would like to prove that
 为了解释证明的概念，考虑当m=2和e的维数为3时的情况。考虑到e的基础（e1，e2，e3），我们想证明

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image044.gif)

are linearly independent. To prove this, it suffices to show that for any vector space F, if w11,w12,w13,w22,w23,w33 are any vectors in F, then there is a symmetric bilinear map h: E2 → F such that h(ei,ej) = wij, 1 ≤ i ≤ j ≤ 3.
 线性无关。为了证明这一点，可以证明对于任何向量空间f，如果w11、w12、w13、w22、w23、w33是f中的任何向量，则存在对称双线性映射h:e2→f，这样h（ei，ej）=wij，1≤i≤j≤3。

32.8. BASES OF SYMMETRIC POWERS
 32.8。对称幂的基

Because h yields a unique linear map such that
 因为H生成一个唯一的线性映射，这样

,
 ，

by Proposition 32.4, the vectors
 根据命题32.4，向量

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image046.gif)

are linearly independent. This suggests understanding how a symmetric bilinear function f : E2 → F is expressed in terms of its values f(ei,ej) on the basis vectors (e1,e2,e3), and this can be done easily. Using bilinearity and symmetry, we obtain
 线性无关。这表明理解对称双线性函数f:e2→f是如何在基向量（e1，e2，e3）上用其值f（ei，ej）表示的，这很容易做到。利用双线性和对称性，我们得到

f(u1e1 + u2e2 + u3e3,v1e1 + v2e2 + v3e3) = u1v1f(e1,e1) + (u1v2 + u2v1)f(e1,e2) + (u1v3 + u3v1)f(e1,e3) + u2v2f(e2,e2)
 f（u1e1+u2e2+u3e3，v1e1+v2e2+v3e3）=u1v1f（e1，e1）+（u1v2+u2v1）f（e1，e2）+（u1v3+u3v1）f（e1，e3）+u2v2f（e2，e2）

\+ (u2v3 + u3v2)f(e2,e3) + u3v3f(e3,e3). Therefore, given w11,w12,w13,w22,w23,w33 ∈ F, the function h given by
 +（u2v3+u3v2）f（e2，e3）+u3v3f（e3，e3）。因此，给定w11、w12、w13、w22、w23、w33∈f，函数h由

h(u1e1 + u2e2 + u3e3,v1e1 + v2e2 + v3e3) = u1v1w11 + (u1v2 + u2v1)w12
 h（u1e1+u2e2+u3e3，v1e1+v2e2+v3e3）=u1v1w11+（u1v2+u2v1）w12

\+ (u1v3 + u3v1)w13 + u2v2w22
 +（U1v3+U3v1）w13+u2v2w22

\+ (u2v3 + u3v2)w23 + u3v3w33
 +（u2v3+u3v2）w23+u3v3w33

is clearly bilinear symmetric, and by construction h(ei,ej) = wij, so it does the job.
 显然是双线性对称的，并且通过构造h（ei，ej）=wij，所以它完成了任务。

The generalization of this argument to any m ≥ 2 and to a space E of any dimension (even infinite) is conceptually clear, but notationally messy. If dim(E) = n and if (e1,...,en) is a basis of E, for any m vectors, for any symmetric multilinear map f : Em → F, we have
 这个论点对任何m≥2和任何维（甚至无穷大）的空间e的推广在概念上是清楚的，但在本质上是混乱的。如果dim（e）=n并且if（e1，…，en）是e的基础，对于任意m向量，对于任意对称多行映射f:em→f，我们有

.
 .

Definition 32.19. Given any set J of n ≥ 1 elements, say J = {j1,...,jn}, and given any m ≥ 2, for any sequence (k1 ...,kn) of natural numbers ki ∈ N such that k1 + ··· + kn = m, the multiset M of size m
 定义32.19。给定任意一组n≥1个元素的j，如j=j1，…，jn，并给定任意m≥2，对于任意自然数序列（k1…，kn），ki∈n，使得k1+······+kn=m，大小为m的多集m

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image048.gif)

is denoted by M(m,J,k1,...,kn). Note that M(ji) = ki, for i = 1,...,n. Given any k ≥ 1, and any u ∈ E, we denote.
 用m（m，j，k1，…，kn）表示。注意，m（ji）=k i，对于i=1，…，n.给定任意k≥1，且任意u∈e，我们表示。

We can now prove the following proposition.
 我们现在可以证明以下命题。

Proposition 32.28. Given a vector space E, if (ei)i∈I is a basis for E, then the family of
 提案32.28。给定一个向量空间e，如果（e i）i∈i是e的基础，那么

vectors
 向量

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image050.gif)

is a basis of the symmetric m-th tensor power Sm(E).
 是对称m-th张量幂sm（e）的基础。

Proof. The proof is very similar to that of Proposition 32.12. First assume that E has finite dimension n. In this case I = {1,...,n}, and any multiset M ∈ N(I) of size |M| = m is of the form M(m,{1,...,n},k1,...,kn), with ki = M(i) and k1 + ··· + kn = m. For any nontrivial vector space F, for any family of vectors
 证据。证据与32.12号提案的证据非常相似。首先假设e有有限维n，在这种情况下，i=1，…，n，任何尺寸为m=m的多集m∈n（i）的形式为m（m，1，…，n，k1，…，kn），其中ki=m（i）和k1+·····+kn=m。对于任何非平凡向量空间f，对于任何向量族

(wM)M∈N(I), |M|=m,
 （wm）m∈n（i），m=m，

we show the existence of a symmetric multilinear map h: Sm(E) → F, such that for every M ∈ N(I) with |M| = m, we have
 我们证明了对称多行映射h:sm（e）→f的存在性，这样对于每一个m∈n（i）和m=m，我们得到

,
 ，

where {i1,...,ik} = dom(M). We define the map f : Em → F as follows: for any m vectors
 其中i1，…，ik=dom（m）。我们将映射f:em→f定义为：对于任何m向量

v1,...,vm ∈ E we can writeand we set
 v1，…，vm∈e我们可以写，我们可以设置

f(v1,...,vm)
 F（v1，…，vm）

​                                                                                    !                          !!
 ！！！

​                     = X                          X                  Y u1,i1         ··· Y un,in         wM(m,{1,...,n},k1,...,kn).
 =x x y u1，i1···y un，单位为wm（m，1，…，n，k1，…，kn）。

​                  k1+···+kn=m IIi1∩∪···∪Ij=∅I, in=6={j,1|,...,mIj|=k}j    i1∈I1     in∈In
 k1+······························································

It is not difficult to verify that f is symmetric and multilinear. By the universal mapping property of the symmetric tensor product, the linear map such that
 不难证明f是对称的和多行的。由对称张量积的普遍映射性质，使线性映射

, is the desired map h. Then by Proposition 32.4, it follows that the family
 ，是所需的地图h。然后，根据32.4号提案，它遵循了家庭

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image052.gif)

is linearly independent. Using the commutativity of , we can also show that these vectors generate Sm(E), and thus, they form a basis for Sm(E).
 是线性无关的。利用的交换性，我们还可以证明这些向量产生sm（e），因此它们构成了sm（e）的基础。

If I is infinite dimensional, then for any m vectors v1,...,vm ∈ F there is a finite subset J of I such that vk = Pj∈J uj,kej for k = 1,...,m, and if we write n = |J|, then the formula for f(v1,...,vm) is obtained by replacing the set {1,...,n} by J. The details are left as an exercise.  
 如果i是无限维，那么对于任意m向量v1，…，vm∈f，i有一个有限的子集j，使得vk=pj∈j uj，kej为k=1，…，m，如果我们写n=j，那么用j替换集合1，…，n得到f（v1，…，vm）的公式。细节留作练习。

32.9. SOME USEFUL ISOMORPHISMS FOR SYMMETRIC POWERS
 32.9。对称幂的一些有用同构

As a consequence, when I is finite, say of size p = dim(E), the dimension of Sm(E) is the number of finite multisets (j1,...,jp), such that j1 + ··· + jp = m, jk ≥ 0. We leave as an exercise to show that this number is m , then the dimension of S. Compare with the dimension of E⊗m, which is pm. In particular, when p = 2, the dimension of Sm(E) is m + 1. This can also be seen directly.
 因此，当我是有限的时，比如说尺寸p=dim（e），sm（e）的维数是有限多集（j1，…，jp）的个数，因此j1+·····+jp=m，jk≥0。作为练习，我们将这个数字表示为m，然后是s的维数，与e m的维数（即pm）进行比较。特别是当p=2时，sm（e）的维数为m+1。这也可以直接看到。

Remark: The number  is also the number of homogeneous monomials
 注：该数也是齐次单项式的个数。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image054.gif)

of total degree m in p variables (we have j1 +···+jp = m). This is not a coincidence! Given a vector space E and a basis (ei)i∈I for E, Proposition 32.28 shows that every symmetric tensor z ∈ Sm(E) can be written in a unique way as
 在P变量中的总度数m（我们有j1+····+jp=m）。这不是巧合！在给定向量空间e和基（e i）i∈i for e的情况下，命题32.28表明，每一个对称张量z∈sm（e）都可以用一种独特的方式写成

,
 ，

for some unique family of scalars λM ∈ K, all zero except for a finite number.
 对于某些唯一的标量族，除有限数外，其余均为零。

This looks like a homogeneous polynomial of total degree m, where the monomials of total degree m are the symmetric tensors
 这看起来像是总次数m的齐次多项式，其中总次数m的单项式是对称张量。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image056.gif)

in the “indeterminates” ei, where i ∈ I (recall that M(i1) + ··· + M(ik) = m) and implies that polynomials can be defined in terms of symmetric tensors.
 在“不确定”ei中，其中i∈i（回想一下m（i1）+·····+m（ik）=m），并暗示多项式可以用对称张量来定义。

## 32.9            Some Useful Isomorphisms for Symmetric Powers  32.9对称幂的一些有用同构

We can show the following property of the symmetric tensor product, using the proof technique of Proposition 32.13 (3).
 利用命题32.13（3）的证明技术，我们可以证明对称张量积的以下性质。

Proposition 32.29. We have the following isomorphism:
 提案32.29。我们有以下同构：

n
 n

Sn(E ⊕ F) ∼= MSk(E) ⊗ Sn−k(F).
 sn（e_f）=msk（e）sn−k（f）。

k=0
 K＝0

## 32.10        Duality for Symmetric Powers  32.10对称功率的对偶性

In this section all vector spaces are assumed to have finite dimension over a field of characteristic zero. We define a nondegenerate pairing Sn(E∗)×Sn(E) −→ K as follows: Consider the multilinear map
 在本节中，假设所有向量空间在特征为零的场上都有有限维。我们定义了一个非退化配对sn（e）×sn（e）−→k如下：考虑多行映射

(E∗)n × En −→ K
 （e）n×en−→k

given by
 给出者

(v1∗,...,vn∗,u1,...,un) 7→ X vσ∗(1)(u1)···vσ∗(n)(un).
 （v1，…，v n，u1，…，un）7→x vσ（1）（u1）···vσ（n）（un）。

σ∈Sn
 σ∈sn

Note that the expression on the right-hand side is “almost” the determinant det(vj∗(ui)), except that the sign sgn(σ) is missing (where sgn(σ) is the signature of the permutation σ; that is, the parity of the number of transpositions into which σ can be factored). Such an expression is called a permanent.
 注意，右边的表达式“几乎”是行列式det（vj（ui）），只是缺少符号sgn（σ）（其中sgn（σ）是置换σ的签名；也就是说，可以将σ分解成因子的转置数的奇偶性）。这样的表达式称为永久表达式。

It can be verified that this expression is symmetric w.r.t. the ui’s and also w.r.t. the vj∗.
 可以验证该表达式是对称的w.r.t.UI和w.r.t.vj。

For any fixed (, we get a symmetric multilinear map
 对于任何固定的（，我们得到一个对称的多行映射

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image058.gif)

from En to K. The map extends uniquely to a linear map making the following diagram commute:
 从en到k。地图独特地延伸到线性地图，使以下图表通勤：

/
 /

lv1∗,...,vGGGGn∗GGGGG#
 Lv1，…，vgggn ggg#

K. We also have the symmetric multilinear map
 k.我们还有对称多行图

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image060.gif)

from (E∗)n to Hom(Sn(E),K), which extends to a linear map L from Sn(E∗) to Hom(Sn(E),K) making the following diagram commute:
 从（e）n到hom（sn（e），k），这延伸到从sn（e）到hom（sn（e），k）的线性图l，使以下图表通勤：

/ Sn(E∗)
 /序号（E）

PPPPPPPPPPPP' L
 pppppppppppp'l

Hom(Sn(E),K).
 HOM（序列号（E），K）。

However, in view of the isomorphism
 然而，鉴于同构

Hom(U ⊗ V,W) ∼= Hom(U,Hom(V,W)),
 hom（u v，w）=hom（u，hom（v，w）），

with U = Sn(E∗), V = Sn(E) and W = K, we can view L as a linear map
 当u=sn（e）、v=sn（e）和w=k时，我们可以将l视为线性映射。

L: Sn(E∗) ⊗ Sn(E) −→ K,
 L:锡（E）锡（E）−→K，

which by Proposition 32.8 corresponds to a bilinear map
 根据命题32.8，它对应于双线性图。

​                                                       h−,−i: Sn(E∗) × Sn(E) −→ K.                                                  (∗)
 H−、−I:锡（E）×锡（E）−→K.（）

32.10. DUALITY FOR SYMMETRIC POWERS
 第32.10条。对称幂的对偶性

This pairing is given explicitly on generators by
 这种配对在发电机上是通过

.
 .

Now this pairing in nondegenerate. This can be shown using bases. If (e1,...,em) is a basis of E, then for every basis element (of Sn(E∗), with n1+···+nk = n, we have
 现在这个配对是非退化的。这可以用碱来表示。如果（e1，…，em）是e的基，那么对于每个基元（sn（e），对于n1+····+nk=n，我们有

,
 ，

and
 和

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image062.gif)

if (
 如果（

​                                 n1                   nk
 N1 NK

If the field K has characteristic zero, then n1!···nk! = 06 . We leave the details as an exercise to the reader. Therefore we get a canonical isomorphism
 如果场k的特征为零，则n1！···NK！=06。我们把细节留给读者作为练习。因此我们得到了一个正则同构

(Sn(E))∗ ∼= Sn(E∗).
 （sn（e））～=sn（e）。

The following proposition summarizes the duality properties of symmetric powers.
 下面的命题总结了对称幂的对偶性。

Proposition 32.30. Assume the field K has characteristic zero. We have the canonical isomorphisms
 提案32.30。假设场k的特征为零。我们有规范同构

(Sn(E))∗ ∼= Sn(E∗)
 （sn（e））～=sn（e）

and
 和

Sn(E∗) ∼= Symn(E;K) = Homsymlin(En,K),
 sn（e））=symn（e；k）=homsymlin（en，k）、

which allows us to interpret symmetric tensors over E∗ as symmetric multilinear maps.
 这使得我们可以将E上的对称张量解释为对称多线性映射。

Proof. The isomorphism µ: Sn(E∗) ∼= Symn(E;K)
 证据。同构：sn（e））=symn（e；k）

follows from the isomorphisms (Sn(E))∗ ∼= Sn(E∗) and (Sn(E))∗ ∼= Symn(E;K) given by Proposition 32.26.   
 从32.26号提案给出的同构（sn（e））～=sn（e）和（sn（e））～=symn（e；k）得出。

Remarks:
 评论：

\1.    The isomorphism µ: Sn(E∗) ∼= Symn(E;K) discussed above can be described explicitly as the linear extension of the map given by
 上述讨论的同构（e））=symn（e；k）可以明确地描述为图的线性延伸

.
 .

If (e1,...,em) is a basis of E, then for every basis element ( of
 如果（e1，…，em）是e的基，那么对于

Sn(E∗), with n1 + ··· + nk = n, we have
 sn（e），n1+·····+nk=n，我们有

,
 ，

If the field K has positive characteristic, then it is possible that n1!···nk! = 0, and this is why we required K to be of characteristic 0 in order for Proposition 32.30 to hold.
 如果场k具有正特性，则可能是n1！···NK！=0，这就是为什么我们要求k的特征为0，以保持命题32.30。

\2.    The canonical isomorphism of Proposition 32.30 holds under more general conditions. Namely, that K is a commutative algebra with identity over Q, and that the E is a finitely-generated projective K-module (see Definition 34.7). See Bourbaki, [25] (Chapter III, §11, Section 5, Proposition 8).
 在更一般的条件下，32.30命题的规范同构成立。也就是说，k是一个恒等式超过q的交换代数，e是一个有限生成的射影k模（见定义34.7）。见Bourbaki，[25]（第三章，第11节，第5节，提案8）。

The map from En to Sn(E) given by ( yields a surjection π: E⊗n → Sn(E). Because we are dealing with vector spaces, this map has some section; that is, there is some injection η: Sn(E) → E⊗n with π◦η = id. Since our field K has characteristic 0, there is a special section having a natural definition involving a symmetrization process defined as follows: For every permutation σ, we have the map rσ : En → E⊗n given by
 从e n到sn（e）的映射由（产生一个推测π：e n→sn（e）。因为我们处理的是向量空间，所以这张图有一个部分，也就是说，有一些注入η：sn（e）→e n，πη=id。由于我们的场k有特征0，所以有一个特殊的部分有一个自然定义，涉及一个对称化过程，定义如下：对于every排列σ，我们得到了图rσ：e n→e n，由

rσ(u1,...,un) = uσ(1) ⊗ ··· ⊗ uσ(n).
 rσ（u1，…，u n）=uσ（1）··uσ（n）。

As rσ is clearly multilinear, rσ extends to a linear map (rσ)⊗ : E⊗n → E⊗n making the following diagram commute
 由于rσ显然是多行的，rσ延伸到一个线性图（rσ）：e n→e n，使得下图中的通勤

EnFFrFσFιF⊗FFFF/ " E⊗ (rnσ)⊗
 Enfrfσf_f ffff/“e（rnσ）

E⊗n,
 埃恩，

and we get a map Sn × E⊗n −→ E⊗n, namely
 我们得到一个图sn×e n−→e n，即

σ · z = (rσ)⊗(z).
 σ·z=（rσ）（z）。

It is immediately checked that this is a left action of the symmetric group Sn on E⊗n, and the tensors z ∈ E⊗n such that
 立即检查这是对称群sn在e n上的左作用，张量z∈e n使得

​                                                        σ · z = z,      for all     σ ∈ Sn
 σ·z=z，对于所有的σ∈sn

are called symmetrized tensors.
 称为对称张量。

We define the map η: En → E⊗n by
 我们定义了图η：e n→e n

.
 .

32.11. SYMMETRIC ALGEBRAS
 32.11.对称代数

As the right hand side is clearly symmetric, we get a linear map making the following diagram commute.
 由于右手边是明显对称的，所以我们得到了一个线性地图，使下面的图表成为通勤路线。

/
 /

GGGηGGGGGG# η
 gggηgggggη

E⊗n
 埃恩

Clearly, )) is the set of symmetrized tensors in E⊗n. If we consider the map  where π is the surjection π: E⊗n → Sn(E), it is easy to check
 很明显，）是e n中对称张量的集合。如果我们考虑π是投影π：e n→sn（e）的映射，很容易检查

that S ◦ S = S. Therefore, S is a projection, and by linear algebra, we know that
 S S=S。因此，S是一个投影，根据线性代数，我们知道

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image064.gif)

It turns out that KerS = E⊗n ∩I = Ker π, where I is the two-sided ideal of T(E) generated by all tensors of the form u ⊗ v − v ⊗ u ∈ E⊗2 (for example, see Knapp [102], Appendix A).
 结果表明，Kers=e n i=Kerπ，其中i是由形式为u v v u e 2的所有张量产生的t（e）的双面理想（例如，见Knapp[102]，附录A）。

Therefore, η is injective,
 因此，η是注射剂，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image066.gif)

and the symmetric tensor power Sn(E) is naturally embedded into E⊗n.
 对称张量幂sn（e）自然嵌入e n中。

## 32.11       Symmetric Algebras  32.11对称代数

As in the case of tensors, we can pack together all the symmetric powers Sn(V ) into an algebra.
 在张量的情况下，我们可以将所有对称幂sn（v）组合成一个代数。

Definition 32.20. Given a vector space V , the space
 定义32.20。给定向量空间v，空间

S(V ) = M Sm(V ),
 s（v）=m sm（v）、

m≥0
 m 0

is called the symmetric tensor algebra of V .
 称为V的对称张量代数。

We could adapt what we did in Section 32.6 for general tensor powers to symmetric tensors but since we already have the algebra T(V ), we can proceed faster. If I is the two-sided ideal generated by all tensors of the form u ⊗ v − v ⊗ u ∈ V ⊗2, we set
 我们可以将第32.6节中关于一般张量幂的内容修改为对称张量，但是由于我们已经有了代数t（v），我们可以更快地进行。如果i是由u v v u∈v 2形式的所有张量产生的双面理想，我们将

S•(V ) = T(V )/I.
 S•（V）=T（V）/I。

Observe that since the ideal I is generated by elements in V ⊗2, every tensor in I is a linear combination of tensors of the form ω1 ⊗(u⊗v −v ⊗u)⊗ω2, with ω1 ∈ V ⊗n1 and ω2 ∈ V ⊗n2 for some n1,n2 ∈ N, which implies that
 观察到，由于理想i是由v 2中的元素生成的，i中的每个张量都是形式为ω1（u v u）ω2的张量的线性组合，其中ω1∈v n1和ω2∈v n2对于某些n1，n2∈n，这意味着

I = M (I ∩ V ⊗m).
 i=m（i v m）。

m≥0
 m 0

Then, S•(V ) automatically inherits a multiplication operation which is commutative, and since T(V ) is graded, that is
 然后，s•（v）自动继承一个可交换的乘法运算，因为t（v）是分级的，即

T(V ) = M V ⊗m,
 t（v）=m v m，

m≥0
 m 0

we have
 我们有

S•(V ) = M V ⊗m/(I ∩ V ⊗m).
 S•（V）=M V M/（I V M）。

m≥0
 m 0

However, it is easy to check that
 但是，很容易检查

Sm(V ) ∼= V ⊗m/(I ∩ V ⊗m),
 sm（v）=v m/（i v m）、

so
 所以

S•(V ) ∼= S(V ).
 S•（V）=S（V）。

When V is of finite dimension n, S(V ) corresponds to the algebra of polynomials with coefficients in K in n variables (this can be seen from Proposition 32.28). When V is of infinite dimension and (ui)i∈I is a basis of V , the algebra S(V ) corresponds to the algebra of polynomials in infinitely many variables in I. What’s nice about the symmetric tensor algebra S(V ) is that it provides an intrinsic definition of a polynomial algebra in any set of I variables.
 当v为有限维n时，s（v）对应于n个变量中系数为k的多项式代数（这可以从命题32.28中看出）。当v是无穷维且（ui）i∈i是v的基础时，代数s（v）对应于i中无穷多变量中的多项式代数。对称张量代数s（v）的优点在于它提供了任意i v集合中多项式代数的内在定义。咏叹调。

It is also easy to see that S(V ) satisfies the following universal mapping property.
 也很容易看出S（V）满足以下通用映射属性。

Proposition 32.31. Given any commutative K-algebra A, for any linear map f : V → A, there is a unique K-algebra homomorphism f : S(V ) → A so that
 提案32.31。对于任意一个交换的k-代数a，对于任何线性映射f:v→a，都有一个唯一的k-代数同态f:s（v）→a，因此

f = f ◦ i,
 f=f_i，

as in the diagram below.
 如下图所示。

V EEEfEEiEE/EES(" V f )
 电子设备/电子设备（“V F）

A
 一

Remark: If E is finite-dimensional, recall the isomorphism µ: Sn(E∗) −→ Symn(E;K) defined as the linear extension of the map given by
 备注：如果e为有限维，则回忆同构：sn（e）−→symn（e；k），定义为由

.
 .

Now we have also a multiplication operation Sm(E∗)×Sn(E∗) −→ Sm+n(E∗). The following question then arises:
 现在我们还有一个乘法运算sm（e）×sn（e）－→sm+n（e）。然后出现以下问题：

32.11. SYMMETRIC ALGEBRAS
 32.11.对称代数

Can we define a multiplication Symm(E;K) × Symn(E;K) −→ Symm+n(E;K) directly on symmetric multilinear forms, so that the following diagram commutes?
 我们可以直接在对称多行形式上定义一个乘法符号（e；k）×symn（e；k）－→sym+n（e；k），以便下面的图表转换吗？

​                                                                               S               /
 S/

​                                                           µm×µn                                 µm+n
 礹m×礹n礹m+n

​                                       Symm(E;K) × Symn(E;K)       ·   / Symm+n (E;K)
 symm（e；k）×symm（e；k）·/symm+n（e；k）

The answer is yes! The solution is to define this multiplication such that for f ∈ Symm(E;K) and g ∈ Symn(E;K),
 答案是肯定的！解决方法是定义这个乘法，这样对于f∈symm（e；k）和g∈symn（e；k），就

​                  (f · g)(u1,...,um+n) = X f(uσ(1),...,uσ(m))g(uσ(m+1),...,uσ(m+n)),                    (∗)
 （f·g）（u1，…，u m+n）=x f（uσ（1），…，uσ（m））g（uσ（m+1），…，uσ（m+n）），（）

σ∈shuffle(m,n)
 σ∈洗牌（m，n）

where shuffle(m,n) consists of all (m,n)-“shuffles;” that is, permutations σ of {1,...m+n} such that σ(1) < ··· < σ(m) and σ(m + 1) < ··· < σ(m + n). Observe that a (m,n)-shuffle is completely determined by the sequence σ(1) < ··· < σ(m).
 式中，shuffle（m，n）由所有（m，n）-“shuffles”组成；即，置换σof 1，…m+n，这样，σ（1）<······<σ（m）和σ（m+1）<······<σ（m+n）。观察到a（m，n）-洗牌完全由序列σ（1）<······<σ（m）决定。

For example, suppose m = 2 and n = 1. Given , the multiplication structure on S(E∗) implies that (). Furthermore, for u1,u2,u3,∈ E,
 例如，假设m=2，n=1。给定，s（e）上的乘法结构意味着（）。此外，对于U1，U2，U3，∈e，

.
 .

Now the (2,1)- shuffles of {1,2,3} are the following three permutations, namely
 现在1,2,3的（2,1）-洗牌是以下三种排列，即

​                                                 ,                          ,                           .
 、、。

If) and), then (∗) implies that
 如果）和），那么（）意味着

(f f(uσ(1),uσ(2))g(uσ(3))
 （f f（uσ（1），uσ（2））g（uσ（3））

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image068.gif)

We leave it as an exercise for the reader to verify Equation (∗) for arbitrary nonnegative integers m and n.
 我们把它作为一个练习，让读者验证任意非负整数m和n的方程（）。

Another useful canonical isomorphism (of K-algebras) is given below.
 另一个有用的正则同构（k-代数）如下。

Proposition 32.32. For any two vector spaces E and F, there is a canonical isomorphism
 提案32.32。对于任意两个向量空间e和f，都存在一个正则同构。

(of K-algebras)
 （关于k-代数）

S(E ⊕ F) ∼= S(E) ⊗ S(F).
 s（e_f）=s（e）s（f）。

## 32.12      Problems  32.12问题

Problem 32.1. Prove Proposition 32.4.
 问题32.1。证明32.4号提案。

Problem 32.2. Given two linear maps f : E → E0 and g: F → F 0, we defined the unique linear map
 问题32.2。给定两个线性映射f:e→e0和g:f→f 0，我们定义了唯一的线性映射

f ⊗ g: E ⊗ F → E0 ⊗ F 0
 F G:E F→e0 F 0

by
 通过

(f ⊗ g)(u ⊗ v) = f(u) ⊗ g(v),
 （f g）（u v）=f（u）g（v）

for all u ∈ E and all v ∈ F. See Proposition 32.9. Thus f ⊗ g ∈ Hom(E ⊗ F,E0 ⊗ F 0). If we denote the tensor product E ⊗ F by T(E,F), and we assume that E,E0 and F,F 0 are finite dimensional, pick bases and show that the map induced by f ⊗ g →7 T(f,g) is an isomorphism
 关于所有u∈e和所有v∈f，见命题32.9。因此f g∈hom（e f，e0 f 0）。如果我们用t（e，f）表示张量积e f，并且假定e，e0和f，f 0是有限维的，那么选取基并证明由f g→7t（f，g）引起的映射是同构的。

Hom(E,F) ⊗ Hom(E0,F 0) ∼= Hom(E ⊗ F,E0 ⊗ F 0).
 hom（e，f）hom（e0，f 0）=hom（e f，e0 f 0）。

Problem 32.3. Adjust the proof of Proposition 32.13 (2) to show that
 问题32.3。调整建议32.13（2）的证明，以证明

E ⊗ (F ⊗ G) ∼= E ⊗ F ⊗ G,
 E（F G）=E F G，

whenever E, F, and G are arbitrary vector spaces.
 当e、f和g是任意向量空间时。

Problem 32.4. Given a fixed vector space G, for any two vector spaces M and N and every linear map f : M → N, we defined τG(f) = f ⊗idG to be the unique linear map making the following diagram commute.
 问题32.4。给定一个固定的向量空间g，对于任意两个向量空间m和n以及每一个线性映射f:m→n，我们将τg（f）=f idg定义为唯一的线性映射，使下表通勤。

ιM⊗
 米尔

*M*    × G  / M ⊗ G
 ×g/m g

f×idGf⊗idG
 f×idgf idg

 

*N*     × G ιN⊗ / N ⊗ G
 ×g_n/n_g

See the proof of Proposition 32.13 (3). Show that
 见提案32.13（3）的证明。展示一下

(1)    τG(0) = 0,
 τg（0）=0，

(2)    τG(idM) = (idM ⊗ idG) = idM⊗G,
 τg（idm）=（idm idg）=idm g，

(3)    If f0 : M → N is another linear map, then τG(f + f0) = τG(f) + τG(f0).
 如果f0:m→n是另一个线性映射，则τg（f+f0）=τg（f）+τg（f0）。

32.12. PROBLEMS
 32.12条。问题

Problem 32.5. Induct on m ≥ 2 to prove the canonical isomorphism
 问题32.5。引入m≥2证明正则同构

V ⊗m ⊗ V ⊗n ∼= V ⊗(m+n).
 v m v n=v（m+n）。

Use this isomorphism to show that ·: V ⊗m × V ⊗n −→ V ⊗(m+n) defined as
 用这个同构表示·：v m×v n−→v（m+n）定义为

(v1 ⊗ ··· ⊗ vm) · (w1 ⊗ ··· ⊗ wn) = v1 ⊗ ··· ⊗ vm ⊗ w1 ⊗ ··· ⊗ wn.
 （v1····vm）·（w1·············································

induces a multiplication on T(V ).
 诱导t（v）上的乘法。

Hint. See Jacobson [95], Section 3.9, or Bertin [15], Chapter 4, Section 2.).
 暗示。见Jacobson[95]第3.9节或Bertin[15]第4章第2节。

Problem 32.6. Prove Proposition 32.19.
 问题32.6。证明32.19号提案。

Hint. See Knapp [102] (Appendix A, Proposition A.14) or Bertin [15] (Chapter 4, Theorem
 暗示。参见Knapp[102]（附录A，提案A.14）或Bertin[15]（第4章，定理

2.4).
 2.4）。

Problem 32.7. Given linear maps f0 : E0 → E00 and g0 : E0 → E00, show that
 问题32.7。给定线性映射f0:e0→e00和g0:e0→e00，显示

.
 .

Problem 32.8. Complete the proof of Proposition 32.28 for the case of an infinite dimensional vector space E.
 问题32.8。对于无穷维向量空间e，完成32.28命题的证明。

Problem 32.9. Let I be a finite index set of cardinality p. Let m be a nonnegative integer. Show that the number of multisets over I with cardinality.
 问题32.9。设为基数p的有限索引集，设m为非负整数。用基数显示多集在i上的数目。

Problem 32.10. Prove Proposition 32.29.
 问题32.10。证明32.29号提案。

Problem 32.11. Using bases, show that the bilinear map at (∗) in Section 32.10 produces a nondegenerate pairing.
 问题32.11。使用碱基，显示第32.10节中（）处的双线性映射产生非退化配对。

Problem 32.12. Let I be the two-sided ideal generated by all tensors of the form u ⊗ v − v ⊗ u ∈ V ⊗2. Prove that Sm(V ) ∼= V ⊗m/(I ∩ V ⊗m).
 问题32.12。我是由u v v u∈v 2形式的所有张量产生的双面理想。证明sm（v）=v m/（i v m）。

Problem 32.13. Verify Equation (∗) of Section 32.11 for arbitrary nonnegative integers m and n.
 问题32.13。验证第32.11节中任意非负整数m和n的方程（）。


 