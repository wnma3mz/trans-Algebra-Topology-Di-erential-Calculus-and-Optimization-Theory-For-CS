第二十八章

# The Geometry of Bilinear Forms; Witt’s Theorem; The Cartan–Dieudonn´e Theorem  双线性形式的几何；维特定理；卡坦-迪乌登定理

## 28.1       Bilinear Forms  28.1双线性形式

In this chapter, we study the structure of a K-vector space E endowed with a nondegenerate
 在本章中，我们研究了具有非退化性的k向量空间e的结构。

inner product. Unlike the case of an inner product, there may be nonzero vectorsbilinear formthat ϕ(u,u) = 0ϕ: Eso the map×E → Ku(for any field7→ ϕ(u,u) can no longer be interpreted as a notion of squareK), which can be viewed as a kind of generalizedu ∈ E such
 内部产品。与内积的情况不同，可能存在非零向量双线性形式，即，图×e→ku（对于任何场7→（u，u）不再被解释为平方的概念），这可以被看作是一种推广∈e，例如

length (also, ϕ(u,u) may not be real and positive!). However, the notion of orthogonality survives: we say that u,v ∈ E are orthogonal iff ϕ(u,v) = 0. Under some additional conditions on ϕ, it is then possible to split E into orthogonal subspaces having some special properties. It turns out that the special cases where ϕ is symmetric (or Hermitian) or skewsymmetric (or skew-Hermitian) can be handled uniformly using a deep theorem due to Witt (the Witt decomposition theorem (1936)).
 长度（也可以是，_（u，u）可能不是真的和正的！）然而，正交性的概念仍然存在：我们说u，v∈e是正交的iff_（u，v）=0。在一些附加条件下，可以将e分解成具有一些特殊性质的正交子空间。结果表明，当_为对称（或厄米提亚）或偏对称（或斜厄米提亚）时，由于witt（witt分解定理（1936）），可以使用深层定理统一处理。

We begin with the very general situation of a bilinear form ϕ: E×F → K, where K is an arbitrary field, possibly of characteristric 2. Actually, even though at first glance this may appear to be an uncessary abstraction, it turns out that this situation arises in attempting to prove properties of a bilinear map ϕ: E ×E → K, because it may be necessary to restrict ϕ to different subspaces U and V of E. This general approach was pioneered by Chevalley [37], E. Artin [6], and Bourbaki [24]. The third source was a major source of inspiration, and many proofs are taken from it. Other useful references include Snapper and Troyer [157], Berger [12], Jacobson [96], Grove [83], Taylor [169], and Berndt [14].
 我们从双线性形式的一般情况开始，其中k是一个任意场，可能具有特征2。事实上，尽管乍一看这似乎是一个不确定的抽象，但事实证明，这种情况是在试图证明双线性映射的性质时出现的，因为可能有必要将π限制到e的不同子空间u和v。这种一般方法是由Chevalley[37]、E.Artin[6]和Bourbaki[24]开创的。第三个来源是一个主要的灵感来源，许多证据都是从中获得的。其他有用的参考文献包括Snapper和Troyer[157]、Berger[12]、Jacobson[96]、Grove[83]、Taylor[169]和Berndt[14]。

is aDefinition 28.1.bilinear form iff the following conditions hold: For allGiven two vector spaces E and F over a fieldu,u ,uK∈, a mapE, all v,vϕ: E,v×∈FF→, forK
 是定义28.1.双线性形式iff的以下条件成立：对于所有给定的两个向量空间e和f，在一个域u，u，uk∈，a mape，all v，v_：e，v×∈ff→，fork上

​                                                                                                          1   2                     1   2
 1 2 1 2

899
 八百九十九

all λ,µ ∈ K, we have
 所有的λ，μ∈k，我们有

ϕ(u1 + u2,v) = ϕ(u1,v) + ϕ(u2,v)
 ⑨（u1+u2，v）=⑨（u1，v）+_（u2，v）

ϕ(u,v1 + v2) = ϕ(u,v1) + ϕ(u,v2) ϕ(λu,v) = λϕ(u,v) ϕ(u,µv) = µϕ(u,v).
 ⑨（u，v1+v2）＝（u，v1）＋（u，v2）（λu，v）＝（u，v）（u，μv）＝_（u，v）。

A bilinear form as in Definition 28.1 is sometimes called a pairing. The first two conditions imply that ϕ(0,v) = ϕ(u,0) = 0 for all u ∈ E and all v ∈ F.
 定义28.1中的双线性形式有时称为配对。前两个条件意味着，所有u∈e和所有v∈f的_（0，v）=（u，0）=0。

If E = F, observe that
 如果e=f，观察

ϕ(λu + µv,λu + µv) = λϕ(u,λu + µv) + µϕ(v,λu + µv)
 _（λu+μv，λu+μv）=λ（u，λu+μv）+_（v，λu+μv）

= λ2ϕ(u,u) + λµϕ(u,v) + λµϕ(v,u) + µ2ϕ(v,v).
 =λ2_（u，u）+λ_（u，v）+λ_（v，u）+_2（v，v）。

If we let λ = µ = 1, we get
 如果我们让λ=μ=1，我们得到

ϕ(u + v,u + v) = ϕ(u,u) + ϕ(u,v) + ϕ(v,u) + ϕ(v,v).
 ⑨（u+v，u+v）=⑨（u，u）+（u，v）+（v，u）+（v，v）。

If ϕ is symmetric, which means that
 如果φ是对称的，这意味着

​                                                  ϕ(u,v) = ϕ(v,u)       for all u,v ∈ E,
 所有u，v∈e，的（u，v）=（v，u）

then
 然后

​                                           2ϕ(u,v) = ϕ(u + v,u + v) − ϕ(u,u) − ϕ(v,v).                                      (∗)
 2_（u，v）=_（u+v，u+v）-（u，u）-（v，v）。（）

The function Φ defined such that
 函数Φ定义如下：

​                                                           Φ(u) = ϕ(u,u)      u ∈ E,
 Φ（u）＝（u，u）u∈e，

is called the quadratic form associated with ϕ. If the field K is not of characteristic 2, then ϕ is completely determined by its quadratic form Φ. The symmetric bilinear form ϕ is called the polar form of Φ. This suggests the following definition.
 被称为二次型。如果场k不属于特征2，那么，根据其二次型Φ完全确定。对称双线性形式，称为Φ的极性形式。这表明了以下定义。

Definition 28.2. A function Φ: E → K is a quadratic form on E if the following conditions hold:
 定义28.2.如果满足以下条件，函数Φ：e→k是e上的二次型：

(1)    We have Φ(λu) = λ2Φ(u), for all u ∈ E and all λ ∈ E.
 我们有Φ（λu）=λ2Φ（u），对于所有的u∈e和所有的λ∈e。

(2)    The map ϕ0 given by ϕ0(u,v) = Φ(u+v)−Φ(u)−Φ(v) is bilinear. Obviously, the map ϕ0 is symmetric.
 由_（u，v）=Φ（u+v）−Φ（u）−Φ（v）给出的图_为双线性。显然，图_是对称的。

Since Φ(x + x) = Φ(2x) = 4Φ(x), we have
 因为Φ（x+x）=Φ（2x）=4Φ（x），我们有

​                                                         ϕ0(u,u) = 2Φ(u)     u ∈ E.
 ⑨0（u，u）=2Φ（u）u∈e.


 

If the field K is not of characteristic 2, then is the unique symmetric bilinear form such that that ϕ(u,u) = Φ(u) for all u ∈ E. The bilinear form is called the polar form of Φ. In this case, there is a bijection between the set of bilinear forms on E and the set of quadratic forms on E.
 如果场k不属于特征2，则为唯一对称双线性形式，使得所有u∈e的（u，u）=Φ（u）。双线性形式称为Φ的极性形式。在这种情况下，E上的双线性形式集和E上的二次形式集之间存在双射。

If K is a field of characteristic 2, then ϕ0 is alternating, which means that
 如果k是特征2的场，那么_是交替的，这意味着

​                                                       ϕ0(u,u) = 0      for all u ∈ E.
 ⑨0（u，u）=0表示所有u∈e。

Thus if K is a field of characteristic 2, then Φ cannot be recovered from the symmetric bilinear form ϕ0.
 因此，如果k是特征2的场，那么Φ就不能从对称双线性形式_中恢复。

If (e1,...,en) is a basis of E, it is easy to show that
 如果（e1，…，en）是e的基础，很容易证明

.
 .

This shows that the quadratic form Φ is completely determined by the scalars Φ(ei) and ϕ0(ei,ej) (i =6 j). Furthermore, given any bilinear form ψ: E × E → K (not necessarily symmetric) we can define a quadratic form Φ by setting Φ(x) = ψ(x,x), and we immediately check that the symmetric bilinear form ϕ0 associated with Φ is given by ϕ0(u,v) = ψ(u,v)+ ψ(v,u). Using the above facts, it is not hard to prove that given any quadratic form Φ, there is some (nonsymmetric) bilinear form ψ such that Φ(u) = ψ(u,u) for all u ∈ E (see Bourbaki [24], Section §3.4, Proposition 2). Thus, quadratic forms are more general than symmetric bilinear forms (except in characteristic = 2).6
 由此可见，二次型Φ完全由量角器Φ（ei）和磴0（ei，ej）（i=6 j）决定。此外，对于任意双线性形式ψ：e×e→k（不一定是对称的），我们可以通过设置Φ（x）=ψ（x，x）来定义二次型Φ，并立即检查与Φ相关的对称双线性形式_0是否由痻0（u，v）=ψ（u，v）+ψ（v，u）给出。利用上述事实，不难证明给定任何二次型Φ，存在一些（非对称）双线性型ψ，使得所有u∈e的Φ（u）=ψ（u，u）（见Bourbaki[24]第3.4节，命题2）。因此，二次型比对称双线性型更为普遍（特征值为2的情况除外）。

Definition 28.3. Given any bilinear form ϕ: E ×E → K where K is a field of any characteristic, we say that ϕ is alternating if
 定义28.3.给定双线性形式，其中k是任何特征的场，我们认为，如果

​                                                        ϕ(u,u) = 0      for all u ∈ E,
 ⑨（u，u）=0表示所有u∈e，

and skew-symmetric if
 和斜对称if

​                                                 ϕ(v,u) = −ϕ(u,v)        for all u,v ∈ E.
 ⑨（v，u）=−⑨（u，v）表示所有u，v∈e。

If K is a field of any characteristic, the identity
 如果k是一个有任何特征的场，那么

ϕ(u + v,u + v) = ϕ(u,u) + ϕ(u,v) + ϕ(v,u) + ϕ(v,v)
 ⑨（U+V，U+V）=⑨（U，U）+（U，V）+（V，U）+（V，V）

shows that if ϕ is alternating, then
 表明如果_是交替的，那么

​                                                 ϕ(v,u) = −ϕ(u,v)        for all u,v ∈ E,
 所有u，v∈e，的（v，u）=−（u，v）

that is, ϕ is skew-symmetric. Conversely, if the field K is not of characteristic 2, then a skew-symmetric bilinear map is alternating, since ϕ(u,u) = −ϕ(u,u) implies ϕ(u,u) = 0.
 也就是说，η是斜对称的。相反，如果场k不属于特征2，则斜对称双线性映射是交替的，因为_（u，u）=-（u，u）表示（u，u）=0。

An important consequence of bilinearity is that a pairing yields a linear map from E into F ∗ and a linear map from F into E∗ (where E∗ = HomK(E,K), the dual of E, is the set of linear maps from E to K, called linear forms).
 双线性的一个重要结果是，配对产生一个从E到F的线性映射，和一个从F到E的线性映射（其中e=homk（e，k），e的对偶，是一组从E到K的线性映射，称为线性形式）。

Definition 28.4. Given a bilinear map ϕ: E × F → K, for every u ∈ E, let lϕ(u) be the linear form in F ∗ given by
 定义28.4.给定双线性映射，对于每一个u e，设l_（u）为f中的线性形式，由

​                                                  lϕ(u)(y) = ϕ(u,y)      for all y ∈ F,
 l_（u）（y）=（u，y）表示所有y∈f，

and for every v ∈ F, let rϕ(v) be the linear form in E∗ given by
 对于每一个v∈f，设r（v）为e中的线性形式，由

​                                                  rϕ(v)(x) = ϕ(x,v)      for all x ∈ E.
 对于所有x∈e，r_（v）（x）=（x，v）。

Because ϕ is bilinear, the maps lϕ : E → F ∗ and rϕ : F → E∗ are linear.
 因为_是双线性的，所以图l_：e→f和r_：f→e_是线性的。

Definition 28.5. A bilinear map ϕ: E×F → K is said to be nondegenerate iff the following conditions hold:
 定义28.5.双线性图_：e×f→k称为非简并iff，条件如下：

(1)    For every u ∈ E, if ϕ(u,v) = 0 for all v ∈ F, then u = 0, and
 对于每一个u∈e，如果所有v∈f的（u，v）=0，则u=0，并且

(2)    For every v ∈ F, if ϕ(u,v) = 0 for all u ∈ E, then v = 0.
 对于每一个v∈f，如果所有u∈e的（u，v）=0，则v=0。

The following proposition shows the importance of lϕ and rϕ.
 下面的命题说明了“l”和“r”的重要性。

Proposition 28.1. Given a bilinear map ϕ: E × F → K, the following properties hold:
 提案28.1.给定双线性映射，其中：e×f→k，以下属性保持不变：

*(a)*    The map lϕ is injective iff Property (1) of Definition 28.5 holds.
 图l_是定义28.5中的注射iff属性（1）。

*(b)*    The map rϕ is injective iff Property (2) of Definition 28.5 holds.
 图r_是定义28.5的注射iff属性（2）。

*(c)*     The bilinear form ϕ is nondegenerate and iff lϕ and rϕ are injective.
 双线性形式_是非退化的，如果l_和r_是注射剂。

*(d)*    If the bilinear form ϕ is nondegenerate and if E and F have finite dimensions, then dim(E) = dim(F), and lϕ : E → F ∗ and rϕ : F → E∗ are linear isomorphisms.
 如果双线性形式_是非退化的，并且如果e和f有有限的尺寸，那么dim（e）=dim（f），l_：e→f和r_：f→e是线性同构。

Proof. (a) Assume that (1) of Definition 28.5 holds. If lϕ(u) = 0, then lϕ(u) is the linear form whose value is 0 for all y; that is,
 证据。（a）假设（1）定义28.5成立。如果l_（u）=0，则l（u）是线性形式，其值为0，表示所有y；即，

​                                               lϕ(u)(y) = ϕ(u,y) = 0       for all y ∈ F,
 对于所有y∈f，l_（u）（y）=（u，y）=0，

and by (1) of Definition 28.5, we must have u = 0. Therefore, lϕ is injective. Conversely, if lϕ is injective, and if
 根据定义28.5的（1），我们必须得到u=0。因此，L_为注射型。相反，如果l_是注射的，并且如果

​                                               lϕ(u)(y) = ϕ(u,y) = 0       for all y ∈ F,
 对于所有y∈f，l_（u）（y）=（u，y）=0，

then lϕ(u) is the zero form, and by injectivity of lϕ, we get u = 0; that is, (1) of Definition 28.5 holds.
 那么l_（u）是零形式，通过l_的注入率，我们得到u=0；也就是说，定义28.5的（1）成立。

(b)        The proof is obtained by swapping the arguments of ϕ.
 证据是通过交换_的论点获得的。

(c)         This follows from (a) and (b).
 这源于（a）和（b）。

(d)        If E and F are finite dimensional, then dim(E) = dim(E∗) and dim(F) = dim(F ∗). Since ϕ is nondegenerate, lϕ : E → F ∗ and rϕ : F → E∗ are injective, so dim(E) ≤ dim(F ∗) = dim(F) and dim(F) ≤ dim(E∗) = dim(E), which implies that
 如果e和f是有限维，那么dim（e）=dim（e）和dim（f）=dim（f）。由于_是非退化的，l_：e→f和r_：f→e是注射剂，因此dim（e）≤dim（f）=dim（f）和dim（f）≤dim（e）=dim（e），这意味着

dim(E) = dim(F),
 dim（e）=dim（f）

and thus, lϕ : E → F ∗ and rϕ : F → E∗ are bijective.                                                                       
 因此，L_：E→F和R_：F→E_是双射的。

As a corollary of Proposition 28.1, we have the following characterization of a nondegenerate bilinear map. The proof is left as an exercise.
 作为命题28.1的一个推论，我们有一个非退化双线性映射的以下特征。证据留作练习。

Proposition 28.2. Given a bilinear map ϕ: E × F → K, if E and F have the same finite dimension, then the following properties are equivalent:
 提案28.2.给定双线性映射，如果e和f具有相同的有限维，则下列属性等效：

*(1)*     The map lϕ is injective.
 图l_是注射剂。

*(2)*     The map lϕ is surjective.
 地图“L”是推测性的。

*(3)*     The map rϕ is injective.
 地图R_是注射剂。

*(4)*     The map rϕ is surjective.
 地图“R”是推测性的。

*(5)*     The bilinear form ϕ is nondegenerate.
 双线性形式为非退化形式。

Observe that in terms of the canonical pairing between E∗ and E given by
 观察e和e之间的规范配对

​                                                      hf,ui = f(u),         f ∈ E∗,u ∈ E,
 hf，ui=f（u），f e，u e，

(and the canonical pairing between F ∗ and F), we have
 （和f和f之间的规范配对），我们有

​                                        ϕ(u,v) = hlϕ(u),vi = hrϕ(v),ui       u ∈ E,v ∈ F.
 ⑨（u，v）=hl（u），vi=hr（v），ui u∈e，v∈f.

Proposition 28.3. Given a bilinear map ϕ: E × F → K, if ϕ is nondegenerate and E and F are finite-dimensional, then dim(E) = dim(F) = n, and for every basis (e1,...,en) of E, there is a basis (f1,...,fn) of F such that ϕ(ei,fj) = δij, for all i,j = 1,...,n.
 提案28.3.给定双线性映射，如果_为非退化映射，且e和f为有限维，则dim（e）=dim（f）=n，对于e的每个基（e1，…，en），f都有一个基（f1，…，fn），因此，对于所有i，j=1，…，n，（ei，fj）=δij。

Proof. Since ϕ is nondegenerate, by Proposition 28.1 we have dim(E) = dim(F) = n, and by Proposition 28.2, the linear map rϕ is bijective. Then, if () is the dual basis (in E∗) of the basis (e1,...,en), the vectors (f1,...,fn) given by fi = rϕ−1(e∗i ) form a basis of F, and we have
 证据。由于_是非退化的，根据命题28.1，我们有dim（e）=dim（f）=n，根据命题28.2，线性映射r_是双射的。那么，如果（）是基（e1，…，en）的对偶基（e），由f i=r_−1（e i）给出的向量（f1，…，fn）构成f的基，我们有

,
 ，

as claimed.                                                                                                                                         
 如要求。

If E = F and ϕ is symmetric, then we have the following interesting result.
 如果e=f和_是对称的，那么我们得到了以下有趣的结果。

Theorem 28.4. Given any bilinear form ϕ: E×E → K with dim(E) = n, if ϕ is symmetric (possibly degenerate) and K does not have characteristic 2, then there is a basis (e1,...,en) of E such that ϕ(ei,ej) = 0, for all i =6 j.
 定理28.4.给定任何双线性形式，其中，dim（e）=n，如果_对称（可能退化），且k不具有特征2，则e有一个基（e1，…，en），使得所有i=6 j，_（ei，ej）=0。

Proof. We proceed by induction on n ≥ 0, following a proof due to Chevalley. The base case n = 0 is trivial. For the induction step, assume that n ≥ 1 and that the induction hypothesis holds for all vector spaces of dimension n−1. If ϕ(u,v) = 0 for all u,v ∈ E, then the statement holds trivially. Otherwise, since K does not have characteristic 2, equation
 证据。我们通过n≥0的诱导进行，根据Chevalley的证明。基本情况n=0无关紧要。对于归纳步骤，假设n≥1，并且归纳假设适用于维度n-1的所有向量空间。如果所有的u，v∈e的_（u，v）=0，那么该语句就无关紧要了。否则，因为k没有特征2，方程

​                                           2ϕ(u,v) = ϕ(u + v,u + v) − ϕ(u,u) − ϕ(v,v)                                      (∗)
 2_（u，v）=（u+v，u+v）−（u，u）−（v，v）（）

show that there is some nonzero vector e1 ∈ E such that ϕ(e1,e1) = 06 since otherwise ϕ would vanish for all u,v ∈ E. We claim that the set
 证明有一些非零向量e1∈e，这样，因为如果没有，那么，对于所有u，v∈e，θ（e1，e1）=06将消失。我们声称

H = {v ∈ E | ϕ(e1,v) = 0}
 h=v∈e _（e1，v）=0

has dimension n − 1, and that e1 ∈/ H.
 具有尺寸n-1，并且e1∈/h。

This is because
 这是因为

H = Ker(lϕ(e1)),
 H=Ker（l_（e1）），

where lϕ(e1) is the linear form in E∗ determined by e1. Since ϕ(e1,e1) = 06 , we have e1 ∈/ H, the linear form lϕ(e1) is not the zero form, and thus its kernel is a hyperplane H (a subspace of dimension n − 1). Since dim(H) = n − 1 and e1 ∈/ H, we have the direct sum
 式中，L_（e1）是e中由e1确定的线性形式。既然ω（e1，e1）=06，我们得到了e1∈/h，线性形式lω（e1）不是零形式，因此它的核是一个超平面h（维度n-1的子空间）。由于dim（h）=n−1和e1∈/h，我们得到了直接和

E = H ⊕ Ke1.
 e=h ke1。

By the induction hypothesis applied to H, we get a basis (e2,...,en) of vectors in H such that ϕ(ei,ej) = 0, for all i =6 j with 2 ≤ i,j ≤ n. Since ϕ(e1,v) = 0 for all v ∈ H and since ϕ is symmetric, we also have ϕ(v,e1) = 0 for all v ∈ H, so we obtain a basis (e1,...,en) of E such that ϕ(ei,ej) = 0, for all i =6 j.   
 通过应用于h的归纳假设，我们得到h中向量的一个基（e2，…，e n），使得所有i=6 j，其中2≤i，j≤n，因此，对于所有v∈h，由于（e1，v）=0，并且由于_是对称的，因此，对于所有v∈h，我们也有_（v，e1）=0，因此我们得到e的一个基（e1，…，en），以便⑨（ei，ej）=0，对于所有i=6 J。

If E and F are finite-dimensional vector spaces and if (e1,...,em) is a basis of E and (f1,...,fn) is a basis of F then the bilinearity of ϕ yields
 如果e和f是有限维向量空间，如果（e1，…，em）是e的基础，并且（f1，…，fn）是f的基础，那么_的双线性度产生

.
 .

This shows that ϕ is completely determined by the n × m matrix M = (mij) with mij = ϕ(ej,fi), and in matrix form, we have
 这表明，_完全由n×m矩阵m=（mij）确定，其中mij=_（ej，fi），在矩阵形式中，我们有

ϕ(x,y) = x>M>y = y>Mx,
 ⑨（x，y）=x>m>y=y>mx，

where x and y are the column vectors associated with (x1,...,xm) ∈ Km and (y1,...,yn) ∈ Kn. As in Section 11.1, we are committing the slight abuse of notation of letting x denote both the vector  and the column vector associated with (x1,...,xn) (and similarly for y).
 其中x和y是与（x1，…，xm）∈km和（y1，…，yn）∈kn相关的列向量。如第11.1节所述，我们犯了一个小错误，即x表示与（x1，…，xn）相关的向量和列向量（与y类似）。

Definition 28.6. If (e1,...,em) is a basis of E and (f1,...,fn) is a basis of F, for any bilinear form ϕ: E × F → K, the n × m matrix M = (mij) given by mij = ϕ(ej,fi) for i = 1,...,n and j = 1,...,m is called the matrix of ϕ with respect to the bases (e1,...,em) and (f1,...,fn).
 定义28.6.如果（e1，…，e m）是e的基，而（f1，…，f n）是f的基，对于任何双线性形式，如果（f1，…，fn）是f的基，那么对于i=1，…，n和j=1，…，m的n×m矩阵m=（mij）由mij=_（ej，fi）给出，则m被称为关于基（e1，…，em）和（f1，…，fn）的_矩阵。

The following fact is easily proved.
 以下事实很容易证明。

Proposition 28.5. If m = dim(E) = dim(F) = n, then ϕ is nondegenerate iff the matrix M is invertible iff det(M) = 06 .
 提案28.5。如果m=dim（e）=dim（f）=n，那么，如果矩阵m是可逆的，那么，如果矩阵m是非退化的，那么，iff det（m）=06。

As we will see later, most bilinear forms that we will encounter are equivalent to one whose matrix is of the following form:
 正如我们稍后将看到的，我们将遇到的大多数双线性形式等价于其矩阵为以下形式的形式：

\1.    In, −In.
 在−在。

\2.    If p + q = n, with p,q ≥ 1,
 如果p+q=n，其中p，q≥1，

\3.    If n = 2m,   
 如果n=2米，

\4.    If n = 2m,
 如果n=2米，

.
 .

If we make changes of bases given by matrices P and Q, so that x = Px0 and y = Qy0, then the new matrix expressing ϕ is P >MQ. In particular, if E = F and the same basis is used, then the new matrix is P >MP. This shows that if ϕ is nondegenerate, then the determinant of ϕ is determined up to a square element.
 如果我们改变矩阵p和q给出的碱基，使x=px0和y=qy0，那么新的矩阵式_是p>mq。特别是，如果e=f并且使用相同的基，那么新的矩阵是p>mp。这表明，如果_是非退化的，那么_的行列式被确定为一个平方元素。

Observe that if ϕ is a symmetric bilinear form (E = F) and if K does not have characteristic 2, then by Theorem 28.4, there is a basis of E with respect to which the matrix M representing ϕ is a diagonal matrix. If K = R or K = C, this allows us to classify completely the symmetric bilinear forms. Recall that Φ(u) = ϕ(u,u) for all u ∈ E.
 注意，如果_是对称双线性形式（e=f），并且k没有特征2，那么根据定理28.4，有一个e的基础，代表_的矩阵m是对角矩阵。如果k=r或k=c，这允许我们完全分类对称双线性形式。回想一下，所有u∈e的Φ（u）=（u，u）。

Proposition 28.6. Given any bilinear form ϕ: E × E → K with dim(E) = n, if ϕ is symmetric and K does not have characteristic 2, then there is a basis (e1,...,en) of E such that
 提案28.6.给定任何双线性形式，直径（e）=n，如果直径（e）=n，且k不具有特征2，则e有一个基（e1，…，en），以便

,
 ，

for some λi ∈ K − {0} and with r ≤ n.                         Furthermore, if K = C, then there is a basis
 对于某些λi∈k−0且r≤n.此外，如果k=c，则有一个基

(e1,...,en) of E such that
 （e1，…，en）的

,
 ，

and if K = R, then there is a basis (e1,...,en) of E such that
 如果k=r，那么e有一个基（e1，…，en），这样

,
 ，

with 0 ≤ p,q and p + q ≤ n.
 0≤P，Q和P+Q≤N。

Proof. The first statement is a direct consequence of Theorem 28.4. If K = C, then every λi has a square root µi, and if replace ei by ei/µi, we obtained the desired form.
 证据。第一个陈述是定理28.4的直接结果。如果k=c，那么每个λi都有一个平方根μi，如果用ei/μi替换ei，我们就得到了所需的形式。

If K = R, then there are two cases:
 如果k=r，则有两种情况：

\1.    If λi > 0, let µi be a positive square root of λi and replace ei by ei/µi.
 如果λi>0，则将μi设为λi的正平方根，并将ei替换为ei/μi。

\2.    If λi < 0, et µi be a positive square root of −λi and replace ei by ei/µi.
 如果λi<0，则etμi为−λi的正平方根，并将ei替换为ei/μi。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

In the nondegenerate case, the matrices corresponding to the complex and the real case are, In,−In, and Ip,q. Observe that the second statement of Proposition 28.6 holds in any field in which every element has a square root. In the case K = R, we can show that(p,q) only depends on ϕ.
 在非退化情况下，对应于复数和实数的矩阵是，in、−in和ip，q。注意，命题28.6的第二个陈述存在于每个元素都有平方根的任何域中。在k=r的情况下，我们可以证明（p，q）仅取决于_。

Definition 28.7. Let ϕ: E×E → R be any symmetric real bilinear form. For any subspace U of E, we say that ϕ is positive definite on U iff ϕ(u,u) > 0 for all nonzero u ∈ U, and we say that ϕ is negative definite on U iff ϕ(u,u) < 0 for all nonzero u ∈ U. Then, let
 定义28.7.设a:e×e→r为任意对称实双线性形式。对于e的任何子空间u，我们说，对于所有非零u∈u，在u iff（u，u）>0上，_是正定的，并且我们说，在u iff（u，u）<0，对于所有非零u∈u，_是负定的。那么，让

r = max{dim(U) | U ⊆ E, ϕ is positive definite on U}
 r=max dim（u）u e，ω在u上为正定

and let s = max{dim(U) | U ⊆ E, ϕ is negative definite on U}
 设s=max dim（u）u e，_在u上为负定

Proposition 28.7. (Sylvester’s inertia law) Given any symmetric bilinear form ϕ: E×E → R with dim(E) = n, for any basis (e1,...,en) of E such that
 提案28.7.（西尔维斯特惯量定律）给定任意对称双线性形式，ω：e×e→r，dim（e）=n，对于e的任何基（e1，…，en），这样

,
 ，

with 0 ≤ p,q and p + q ≤ n, the integers p,q depend only on ϕ; in fact, p = r and q = s, with r and s as defined above.
 当0≤p，q和p+q≤n时，整数p，q仅取决于_；事实上，p=r和q=s，其中r和s如上文所定义。

Proof. If we let U be the subspace spanned by (e1,...,ep), then ϕ is positive definite on U, so r ≥ p. Similarly, if we let V be the subspace spanned by (ep+1,...,ep+q), then ϕ is negative definite on V , so s ≥ q.
 证据。如果我们将u设为（e1，…，ep）所跨越的子空间，那么，在u上，ω是正定的，所以r≥p。同样，如果我们将v设为（ep+1，…，ep+q）所跨越的子空间，那么，在v上，ω是负定的，所以s≥q。

Next, if W1 is any subspace of maximum dimension such that ϕ is positive definite on
 下一步，如果w1是最大尺寸的任何子空间，那么，在

W1, and if we let V 0 be the subspace spanned by (ep+1,...,en), then ϕ(u,u) ≤ 0 on V 0, so W1 ∩ V 0 = (0), which implies that dim(W1) + dim(V 0) ≤ n, and thus, r + n − p ≤ n; that is, r ≤ p. Similarly, if W2 is any subspace of maximum dimension such that ϕ is negative definite on W2, and if we let U0 be the subspace spanned by (e1,...,ep,ep+q+1,...,en), then ϕ(u,u) ≥ 0 on U0, so W2 ∩ U0 = (0), which implies that s + n − q ≤ n; that is, s ≤ q. Therefore, p = r and q = s, as claimed       
 w1，如果我们让v 0为（ep+1，…，en）所跨越的子空间，那么v 0上的瓒（u，u）≤0，那么w1 v 0=（0），这意味着dim（w1）+dim（v 0）≤n，因此，r+n−p≤n；也就是说，r≤p。同样，如果w2是最大尺寸的任何子空间，使得瓒在w2上为负定，如果我们让u0是（e1，…，ep，ep+q+1，…，en）所跨越的子空间，那么，在u0上，那么，ω（u，u）≥0，那么，w2 u0=（0），这意味着s+n−q≤n；也就是说，s≤q。因此，p=r，q=s，正如所声称的那样。

These last two results can be generalized to ordered fields. For example, see Snapper and Troyer [157], Artin [6], and Bourbaki [24].
 最后两个结果可以推广到有序域。例如，参见Snapper和Troyer[157]、Artin[6]和Bourbaki[24]。


 

28.2. SESQUILINEAR FORMS
 28.2。倍线性形式

## 28.2       Sesquilinear Forms  28.2倍线性形式

In order to accomodate Hermitian forms, we assume that some involutive automorphism,
 为了适应赫米特形式，我们假设一些对合自同构，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

λ 7→ λ, of the field K is given. This automorphism of K satisfies the following properties:
 给出了K场的λ7→λ。k的自同构满足以下性质：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

Since any field automorphism maps the multiplicative unit 1 to itself, we have 1 = 1.
 因为任何场的自同构都将乘法单位1映射到自身，所以我们有1=1。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

If the automorphism λ 7→ λ is the identity, then we are in the standard situation of a bilinear form. When K = C (the complex numbers), then we usually pick the automorphism of C to be conjugation; namely, the map
 如果自同构λ7→λ是恒等式，则我们处于双线性形式的标准情形。当k=c（复数）时，我们通常选择c的自同构作为共轭，即映射

a + ib 7→ a − ib.
 A+Ib 7→A−Ib。

Definition 28.8. Given two vector spaces E and F over a field K with an involutive au-
 定义28.8.给定具有对合Au的K场上的两个向量空间e和f-

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

tomorphism λ 7→ λ, a mapu,u1ϕ,u:E∈×EF, all→v,vK1is a (right),v2 ∈ F, for allsesquilinear formλ,µ ∈ K, we haveiff the following conditions hold: For all
 tomorphismλ7→λ，a mapu，u1_，u:e∈×e f，all→v，vk1为a（右），v2∈f，对于所有二次线性形式λ，_∈k，我们有以下条件保持：对于所有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

Again, ϕ(0,v) = ϕ(u,0) = 0. If E = F, then we have
 再说一遍，_（0，v）=（u，0）=0。如果e=f，那么我们有

.
 .

If we let λ = µ = 1 and then λ = 1,µ = −1, we get
 如果我们让λ=μ=1，然后λ=1，μ=−1，我们得到

ϕ(u + v,u + v) = ϕ(u,u) + ϕ(u,v) + ϕ(v,u) + ϕ(v,v) ϕ(u − v,u − v) = ϕ(u,u) − ϕ(u,v) − ϕ(v,u) + ϕ(v,v),
 ⑨（u+v，u+v）=（u，u）+（u，v）+（v，u）+（v，v）（u−v，u−v）=（u，u）−（u，v）−（v，u）+（v，v）

so by subtraction, we get
 所以通过减法，我们得到

​                       2(ϕ(u,v) + ϕ(v,u)) = ϕ(u + v,u + v) − ϕ(u − v,u − v)          for u,v ∈ E.
 2（_（u，v）+_（v，u））=_（u+v，u+v）−（u−v，u−v）表示u，v∈e。

If we replace v by λv (with λ 6= 0), we get
 如果用λv代替v（用λ6=0），我们得到

and by combining the above two equations, we get
 把这两个方程结合起来，我们得到

​                                                                              .                                                                         (∗)
 .（）

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

If the automorphism λ 7→ λ is not the identity, then there is some λ ∈ K such thatϕ is completelyλ−λ 6= 0, and if K is not of characteristic 2, then we see that the sesquilinear form determined by its restriction to the diagonal (that is, the set of valuesIn the special case where K = C, we can pick λ = i, and we get {ϕ(u,u) | u ∈ E}).
 如果自同构式λ7→λ不是恒等式，则存在一些λ∈k，使得_完全是λ−λ6=0，如果k不属于特征2，则我们看到由其对对角线的限制所确定的倍线性形式（即，在特殊情况下，k=c的值集，我们可以选择λ=i，得到（u，u）u∈e）。

4ϕ(u,v) = ϕ(u + v,u + v) − ϕ(u − v,u − v) + iϕ(u + λv,u + λv) − iϕ(u − λv,u − λv).
 4_（u，v）=（u+v，u+v）-（u-v，u-v）+i_（u+λv，u+λv）-i（u-λv，u-λv）。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

Remark: If the automorphism λ 7→ϕλis symmetric.is the identity, then in general ϕ is not determined by its value on the diagonal, unless
 注：如果自同构式λ7→λ是对称的。是恒等式，那么一般来说，_不是由对角线上的值决定的，除非

In the sesquilinear setting, it turns out that the following two cases are of interest:
 在倍线性设置中，发现以下两种情况是有意义的：

\1.    We have
 我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

​                                                      ϕ(v,u) = ϕ(u,v),        for all u,v ∈ E,
 ⑨（v，u）=⑨（u，v），对于所有u，v∈e，

in which case we say that ϕ is Hermitian. In the special case where K = C and the involutive automorphism is conjugation, we see that ϕ(u,u) ∈ R, for u ∈ E.
 在这种情况下，我们称之为_为赫米特。在k=c的特殊情况下，对合自同构是共轭的，我们可以看到，对于u∈e，ω（u，u）∈r。

\2.    We have
 我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

​                                                     ϕ(v,u) = −ϕ(u,v),         for all u,v ∈ E,
 ⑨（v，u）=−⑨（u，v），对于所有u，v∈e，

in which case we say that ϕ is skew-Hermitian.
 在这种情况下，我们称之为倾斜赫米特。

We observed that in characteristic different from 2, a sesquilinear form is determined by its restriction to the diagonal. For Hermitian and skew-Hermitian forms, we have the following kind of converse.
 我们观察到，在不同于2的特征中，倍线性形式是由它对对角线的限制决定的。对于厄米提亚和歪厄米提亚形式，我们有以下几种相反的形式。

Proposition 28.8. If ϕ is a nonzero Hermitian or skew-Hermitian form and if ϕ(u,u) = 0
 提案28.8.如果η是非零厄米式或斜厄米式，并且如果η（u，u）=0

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

for all u ∈ E, then K is of characteristic 2 and the automorphism λ 7→ λ is the identity.
 对于所有u∈e，则k为特征2，自同构性λ7→λ为同一性。

Proof. We give the proof in the Hermitian case, the skew-Hermitian case being left as an exercise. Assume that ϕ is alternating. From the identity
 证据。我们在赫米特的案例中给出了证明，歪斜的赫米特案例作为练习被留下。假设_是交替的。从身份上

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

ϕ(u + v,u + v) = ϕ(u,u) + ϕ(u,v) + ϕ(u,v) + ϕ(v,v),
 ⑨（U+V，U+V）=⑨（U，U）+（U，V）+（U，V）+（V，V）、

we get
 我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

​                                                 ϕ(u,v) = −ϕ(u,v)        for all u,v ∈ E.
 ⑨（u，v）=-全部u，v∈e。

SinceFor anyϕ is not the zero form, there exist some nonzero vectorsλ ∈ K, we have u,v ∈ E such that ϕ(u,v) = 1.
 既然任何瓒不是零形式，存在一些非零向量λ∈k，我们有u，v∈e，因此瓒（u，v）=1。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

λϕ(u,v) = ϕ(λu,v) = −ϕ(λu,v) = −λϕ(u,v),
 哿（u，v）=哿（λu，v）=哿（λu，v）=哿（u，v）

28.2. SESQUILINEAR FORMS
 28.2。倍线性形式

and since ϕ(u,v) = 1, we get
 既然_（u，v）=1，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image016.gif)

​                                                            λ = −λ       for all λ ∈ K.
 λ=所有λ的−λ∈k。

For λ = 1, we get 1 = −1, which means that K has characterictic 2. But then
 对于λ=1，我们得到1=−1，这意味着k具有特征2。但是那时

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

​                                                         λ = −λ = λ        for all λ ∈ K,
 λ=−λ=所有λ的λ∈k，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

so the automorphism λ 7→ λ is the identity.                                                                                   
 所以自同构式λ7→λ是同一性。

The definition of the linear maps lϕ and rϕ requires a small twist due to the automorphism
 线性映射的定义l_和r_由于自同构需要一个小的扭曲。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

λ 7→ λ.
 λ7→λ。

Definition 28.9. Given a vector space E over a field K with an involutive automorphism
 定义28.9.给出了具有对合自同构的K域上的向量空间E

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image018.gif)

λ 7→ λ, we define the K-vector space E as E with its abelian group structure, but with scalar multiplication given by
 λ7→λ，我们用它的阿贝尔群结构将k向量空间e定义为e，但用下式给出的标量乘法

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

(λ,u) 7→ λu.
 （λ，u）7→λu。

Given two K-vector spaces E and F, a semilinear map f : E → F is a function, such that for all u,v ∈ E, for all λ ∈ K, we have
 给定两个k向量空间e和f，一个半线性映射f:e→f是一个函数，这样对于所有u，v∈e，对于所有λ∈k，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image020.gif)

Because λ = λ, observe that a function f : E → F is semilinear iff it is a linear map
 因为λ=λ，观察函数f:e→f是半线性的，如果它是线性映射

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image021.gif)

f : E → F. The K-vector spaces E and E are isomorphic, since any basis (ei)i∈I of E is also a basis of E.
 f:e→f。k向量空间e和e是同构的，因为e的任何基（e i）i∈i也是e的基。

The maps lϕ and rϕ are defined as follows:
 图L_和R_定义如下：

For every u ∈ E, let lϕ(u) be the linear form in F ∗ defined so that
 对于每一个u e，设l_（u）为f中定义的线性形式，以便

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

​                                                  lϕ(u)(y) = ϕ(u,y)      for all y ∈ F,
 l_（u）（y）=（u，y）表示所有y∈f，

and for every v ∈ F, let rϕ(v) be the linear form in E∗ defined so that
 对于每一个v∈f，设r（v）为e中的线性形式，因此

​                                                  rϕ(v)(x) = ϕ(x,v)      for all x ∈ E.
 对于所有x∈e，r_（v）（x）=（x，v）。

The reader should check that because we used ϕ(u,y) in the definition of lϕ(u)(y), the function lϕ(u) is indeed a linear form in F ∗. It is also easy to check that lϕ is a linear
 读者应检查，因为我们在l_（u）（y）的定义中使用了_（u，y），函数l_（u）实际上是f_中的线性形式。也可以很容易地检查l_是线性的

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image022.gif)

map lϕ : E → F ∗, and that rϕ is a linear map rϕ : F → E∗ (equivalently, lϕ : E → F ∗ and rϕ : F → E∗ are semilinear).
 图l_：e→f_，而r_是线性图r_：f→e（相当于，l_：e→f_和r_：f→e是半线性的）。

The notion of a nondegenerate sesquilinear form is identical to the notion for bilinear forms. For the convenience of the reader, we repeat the definition.
 非退化倍线性形式的概念与双线性形式的概念相同。为了方便读者阅读，我们重复定义。

Definition 28.10. A sesquilinear map ϕ: E × F → K is said to be nondegenerate iff the following conditions hold:
 定义28.10.当满足以下条件时，称倍线性映射为非退化的iff:e×f→k：

(1)    For every u ∈ E, if ϕ(u,v) = 0 for all v ∈ F, then u = 0, and
 对于每一个u∈e，如果所有v∈f的（u，v）=0，则u=0，并且

(2)    For every v ∈ F, if ϕ(u,v) = 0 for all u ∈ E, then v = 0.
 对于每一个v∈f，如果所有u∈e的（u，v）=0，则v=0。

Proposition 28.1 translates into the following proposition. The proof is left as an exercise. Proposition 28.9. Given a sesquilinear map ϕ: E ×F → K, the following properties hold:
 28.1号提案转化为以下提案。证据留作练习。提案28.9.给定一个倍线性映射，其中：e×f→k，以下属性保持不变：

*(a)*    The map lϕ is injective iff Property (1) of Definition 28.10 holds.
 图l_是定义28.10的注射iff属性（1）。

*(b)*    The map rϕ is injective iff Property (2) of Definition 28.10 holds.
 图R_是定义28.10的注射iff属性（2）。

*(c)*     The sesquilinear form ϕ is nondegenerate and iff lϕ and rϕ are injective.
 倍线性形式_是非退化的，如果l_和r_是注射剂。

*(d)*    If the sesquillinear form ϕ is nondegenerate and if E and F have finite dimensions,
 如果倍半线性形式_是非退化的，并且如果e和f有有限的尺寸，

then dim(E) = dim(F), and lϕ : E → F ∗ and rϕ : F → E∗ are linear isomorphisms.
 那么dim（e）=dim（f），l_：e→f和r_：f→e是线性同构。

Propositions 28.2 and 28.3 also generalize to sesquilinear forms. We also have the following version of Theorem 28.4, whose proof is left as an exercise.
 命题28.2和28.3也归纳为倍线性形式。我们还有下面的定理28.4版本，它的证明留作练习。

Theorem 28.10. Given any sesquilinear form ϕ: E × E → K with dim(E) = n, if ϕ is Hermitian and K does not have characteristic 2, then there is a basis (e1,...,en) of E such that ϕ(ei,ej) = 0, for all i =6 j.
 定理28.10。给定任意倍线性形式，其中，dim（e）=n，如果_为Hermitian且k不具有特征2，则e有一个基（e1，…，en），因此，所有i=6 j，_（ei，ej）=0。

As in Section 28.1, if E and F are finite-dimensional vector spaces and if (e1,...,em) is a basis of E and (f1,...,fn) is a basis of F then the sesquilinearity of ϕ yields
 如第28.1节所述，如果e和f是有限维向量空间，并且如果（e1，…，em）是e的基础，并且（f1，…，fn）是f的基础，那么，θ的倍线性产生

.
 .

This shows that ϕ is completely determined by the n × m matrix M = (mij) with mij = ϕ(ej,fi), and in matrix form, we have
 这表明，_完全由n×m矩阵m=（mij）确定，其中mij=_（ej，fi），在矩阵形式中，我们有

ϕ(x,y) = x>M>y = y∗Mx,
 ⑨（x，y）=x>m>y=y mx，

where x and y are the column vectors associated with (x1,...,xm) ∈ Km and (y1,...,yn) ∈ Kn, and y∗ = y>. As earlier, we are committing the slight abuse of notation of letting x denote both the vector  and the column vector associated with (x1,...,xn)
 其中x和y是与（x1，…，xm）km和（y1，…，yn）kn和y=y>相关的列向量。如前所述，我们犯了一个小小的错误，即x表示与（x1，…，xn）相关联的向量和列向量。

(and similarly for y).
 （与Y类似）。

Definition 28.11. If (e1,...,em) is a basis of E and (f1,...,fn) is a basis of F, for any sesquilinear form ϕ: E × F → K, the n × m matrix M = (mij) given by mij = ϕ(ej,fi) for i = 1,...,n and j = 1,...,m is called the matrix of ϕ with respect to the bases (e1,...,em) and (f1,...,fn).
 定义28.11.如果（e1，…，e m）是e的基，（f1，…，f n）是f的基，对于任何倍线性形式，_：e×f→k，对于i=1，…，n和j=1，…，m的n×m矩阵m=（mij）由mij=_（ej，fi）给出，m被称为关于基（e1，…，em）和（f1，…，fn）的_矩阵。


 

Proposition 28.5 also holds for sesquilinear forms and their matrix representations.
 命题28.5也适用于倍线性形式及其矩阵表示。

Observe that if ϕ is a Hermitian form (E = F) and if K does not have characteristic 2, then by Theorem 28.10, there is a basis of E with respect to which the matrix M representing ϕ is a diagonal matrix. If K = C, then these entries are real, and this allows us to classify completely the Hermitian forms.
 注意，如果_是厄米形式（e=f），并且k没有特征2，那么根据定理28.10，有一个e的基础，表示_的矩阵m是对角矩阵。如果k=c，那么这些条目是真实的，这允许我们完全分类赫米特形式。

Proposition 28.11. Given any Hermitian form ϕ: E × E → C with dim(E) = n, there is a basis (e1,...,en) of E such that
 提案28.11.给定任何厄米特式_：e×e→c，dim（e）=n，e有一个基（e1，…，en），这样

,
 ，

with 0 ≤ p,q and p + q ≤ n.
 0≤P，Q和P+Q≤N。

The proof of Proposition 28.11 is the same as the real case of Proposition 28.6. Sylvester’s inertia law (Proposition 28.7) also holds for Hermitian forms: p and q only depend on ϕ.
 第28.11号提案的证明与第28.6号提案的真实情况相同。西尔维斯特惯性定律（命题28.7）也适用于赫米特形式：p和q仅取决于_。

## 28.3       Orthogonality  28.3正交性

In this section we assume that we are dealing with a sesquilinear form ϕ: E × F → K. We
 在本节中，我们假设我们处理的是一个双方程形式，即：e×f→k。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

allow the automorphism λ →7 λ to be the identity, in which case ϕ is a bilinear form. This way, we can deal with properties shared by bilinear forms and sesquilinear forms in a uniform fashion. Orthogonality is such a property.
 允许自同构λ→7λ为恒等式，在这种情况下，Ⅷ为双线性形式。这样，我们就可以以统一的方式处理双线性形式和倍线性形式共享的属性。正交性就是这样一种性质。

Definition 28.12. Given a sesquilinear form ϕ: E×F → K, we say that two vectors u ∈ E and v ∈ F are orthogonal (or conjugate) if ϕ(u,v) = 0. Two subsets E0 ⊆ E and F 0 ⊆ F are orthogonal if ϕ(u,v) = 0 for all u ∈ E0 and all v ∈ F 0. Given a subspace U of E, the right orthogonal space of U, denoted U⊥, is the subspace of F given by
 定义28.12.给出了一个二次线性形式，即：e×f→k，我们认为两个向量u∈e和v∈f是正交的（或共轭的），前提是（u，v）=0。两个子集e0 e和f 0 f是正交的，如果所有u∈e0和所有v∈f 0的ω（u，v）=0。给定e的子空间u，u的右正交空间，表示u，是f的子空间，由

​                                            U⊥ = {v ∈ F | ϕ(u,v) = 0        for all u ∈ U},
 u=v∈f（u，v）=0表示所有u∈u，

and given a subspace V of F, the left orthogonal space of V , denoted V ⊥, is the subspace of E given by
 给定f的子空间v，v的左正交空间，表示为v，是e的子空间，由

​                                            V ⊥ = {u ∈ E | ϕ(u,v) = 0       for all v ∈ V }.
 V=U∈E（U，V）=0表示所有V∈V。

When E and F are distinct, there is little chance of confusing the right orthogonal subspace U⊥ of a subspace U of E and the left orthogonal subspace V ⊥ of a subspace V of F. However, if E = F, then ϕ(u,v) = 0 does not necessarily imply that ϕ(v,u) = 0, that is, orthogonality is not necessarily symmetric. Thus, if both U and V are subsets of E, there is a notational ambiguity if U = V . In this case, we may write U⊥r for the right orthogonal and U⊥l for the left orthogonal.
 当e和f不同时，几乎不可能混淆e的子空间u的右正交子空间u和f的子空间v的左正交子空间v。然而，如果e=f，则_（u，v）=0并不一定意味着（v，u）=0，也就是说，正交性不必要。对称。因此，如果u和v都是e的子集，那么如果u=v，就有一个符号模糊性。在这种情况下，我们可以为右正交写u_r，为左正交写u_l。

The above discussion brings up the following point: When is orthogonality symmetric?
 以上讨论提出了以下几点：正交对称是什么时候？

If ϕ is bilinear, it is shown in E. Artin [6] (and in Jacobson [96]) that orthogonality is symmetric iff either ϕ is symmetric or ϕ is alternating (ϕ(u,u) = 0 for all u ∈ E).
 如果ω是双线性的，则在e.artin[6]和jacobson[96]中表明，正交性是对称的iff，其中，ω是对称的，或者，ω是交替的（对于所有u∈e，u=0）。

If ϕ is sesquilinear, the answer is more complicated. In addition to the previous two cases, there is a third possibility:
 如果π是倍线性的，答案就更复杂了。除前两种情况外，还有第三种可能性：

​                                                              )                    for all u,v ∈ E,
 ）对于所有u，v∈e，

where  is some nonzero element in K. We say that-Hermitian. Observe that
 K中的非零元素在哪里，我们称之为厄米提安。注意

,
 ，

so if ϕ is not alternating, then ϕ(u,u) = 06      for some u, and we must have     = 1. The most common cases are
 因此，如果_不是交替的，那么_（u，u）=06对于一些u，我们必须有=1。最常见的情况是

\1.     = 1, in which case ϕ is Hermitian, and
 =1，在这种情况下，η为Hermitian，并且

\2.    1, in which case ϕ is skew-Hermitian.
 1，在这种情况下，η是歪厄米提安。

If ϕ is alternating and K is not of characteristic 2, then equation (∗) from Section 28.2
 如果φ是交替的，k不属于特征2，则第28.2节中的方程式（）

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image023.gif)

implies that the automorphism λ 7→ λ must be the identity if ϕ is nonzero. If so, ϕ is skew-symmetric, so
 意味着自同构λ7→λ必须是单位，如果_为非零。如果是的话，_是斜对称的，所以

In summary, if ϕ is either symmetric, alternating, or -Hermitian, then orthogonality is symmetric, and it makes sense to talk about the orthogonal subspace U⊥ of U. Observe that if-Hermitian, then
 综上所述，如果ω是对称的、交替的或-hermitian，那么正交性是对称的，讨论u的正交子空间u是有意义的。观察如果hermitian，那么

.
 .

This is because
 这是因为

,
 ，

so.
 所以。

If E and F are finite-dimensional with bases (e1,...,em) and (f1,...,fn), and if ϕ is represented by the n × m matrix M, then-Hermitian iff
 如果e和f是有限维的，有基（e1，…，e m）和（f1，…，f n），并且如果ρ由n×m矩阵m表示，那么Hermitian iff

,
 ，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image024.gif)

where M∗ = (M)> (as usual). This captures the following kinds of familiar matrices:
 式中m=（m）>（通常）。这捕获了以下类型的熟悉矩阵：

\1.    Symmetric matrices (
 对称矩阵（

\2.    Skew-symmetric matrices (
 斜对称矩阵（

\3.    Hermitian matrices (
 厄米特矩阵（

\4.    Skew-Hermitian matrices (
 偏斜厄米特矩阵（

Going back to a sesquilinear form ϕ: E × F → K, for any subspace U of E, it is easy to check that
 回到倍线性形式，对于e的任何子空间u，很容易检查

*U*    ⊆ (U⊥)⊥,
 （u），

and that for any subspace V of F, we have
 对于f的任何子空间v，我们有

*V*    ⊆ (V ⊥)⊥.
 （V）。

For simplicity of notation, we write U⊥⊥ instead of (U⊥)⊥ (and V ⊥⊥ instead of (V ⊥)⊥).
 为了简化表示法，我们编写u而不是（u）（和v而不是（v））。

Given any two subspaces U1 and U2 of E, if U1 ⊆ U2, then . Indeed, if then ϕ(u2,v) = 0 for all u2 ∈ U2, and since U1 ⊆ U2 this implies that ϕ(u1,v) = 0 for all u1 ∈ U1, which shows that . Similarly for any two subspaces V1,V2 of F, if V1 ⊆ V2, then. As a consequence,
 给定e的任意两个子空间u1和u2，如果u1 u2，那么。实际上，如果所有的u2∈u2，那么，既然u1 u2，那么意味着所有的u1∈u1，v=0，这表明。同样，对于任意两个子空间v1，v2 of f，如果v1 v2，那么。因此，

​                                                       U⊥ = U⊥⊥⊥,     V ⊥ = V ⊥⊥⊥.
 U=U，V=V。

First, we have U⊥ ⊆ U⊥⊥⊥. Second, from U ⊆ U⊥⊥, we get U⊥⊥⊥ ⊆ U⊥, so U⊥ = U⊥⊥⊥.
 首先，我们有u_u__。其次，从u u，我们得到u u，所以u=u。

The other equation is proved is a similar way.
 另一个方程也被证明是类似的。

Observe that ϕ is nondegenerate iff E⊥ = {0} and F ⊥ = {0}. Furthermore, since
 观察到，如果e=0和f=0不退化。此外，因为

ϕ(u + x,v) = ϕ(u,v) ϕ(u,v + y) = ϕ(u,v)
 ⑨（u+x，v）=⑨（u，v）⑨（u，v+y）=⑨（u，v）

for any x ∈ F ⊥ and any y ∈ E⊥, we see that we obtain by passing to the quotient a sesquilinear form
 对于任何x f和任何y e，我们看到我们通过传递给商得到一个倍线性形式。

[ϕ]: (E/F ⊥) × (F/E⊥) → K
 [⑨]：（E/F）×（F/E）→K

which is nondegenerate.
 这是不退化的。

Proposition 28.12. For any sesquilinear form ϕ: E × F → K, the space E/F ⊥ is finitedimensional iff the space F/E⊥ is finite-dimensional; if so, dim(E/F ⊥) = dim(F/E⊥).
 提案28.12。对于任何倍线性形式：e×f→k，空间e/f是有限维的，如果空间f/e是有限维的，那么dim（e/f）=dim（f/e）。

Proof. Since the sesquilinear form [ϕ]: (E/F ⊥) × (F/E⊥) → K is nondegenerate, the maps
 证据。由于sesquilinear形式[]：（e/f）×（f/e）→k是非退化的，因此地图

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image025.gif)

l[ϕ] : (E/F ⊥) → (F/E⊥)∗ and r[ϕ] : (F/E⊥) → (E/F ⊥)∗ are injective. If dim(E/F ⊥) = m, then dim(E/F ⊥) = dim((E/F ⊥)∗), so by injectivity of r[ϕ], we have dim(F/E⊥) =
 L[]：（E/F）→（F/E）和R[]：（F/E）→（E/F）为注射型。如果dim（e/f）=m，那么dim（e/f）=dim（（e/f）），那么通过r[_]的注入率，我们得到dim（f/e）=

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image026.gif)

dim((F/E⊥)) ≤ m. A similar reasoning using the injectivity of l[ϕ] applies if dim(F/E⊥) = n,
 dim（（f/e）≤m。如果dim（f/e）=n，使用l[]的注入率的类似推理适用。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image027.gif)

and we get dim(E/F ⊥) = dim((E/F ⊥)) ≤ n. Therefore, dim(E/F ⊥) = m is finite iff dim(F/E⊥) = n is finite, in which case m = n by Proposition 28.1(d). 
 我们得到dim（e/f）=dim（（e/f）≤n。因此，dim（e/f）=m是有限的，iff dim（f/e）=n是有限的，在这种情况下，根据命题28.1（d），m=n。

If U is a subspace of a space E, recall that the codimension of U is the dimension of E/U, which is also equal to the dimension of any subspace V such that E is a direct sum of
 如果u是空间e的子空间，回想一下u的余维是e/u的维数，也等于任何子空间v的维数，这样e是

U and V (E = U ⊕ V ).
 u和v（e=u v）。

Proposition 28.12 implies the following useful fact.
 建议28.12暗示了以下有用的事实。

Proposition 28.13. Let ϕ: E×F → K be any nondegenerate sesquilinear form. A subspace U of E has finite dimension iff U⊥ has finite codimension in F. If dim(U) is finite, then codim(U⊥) = dim(U), and U⊥⊥ = U.
 提案28.13。设_：e×f→k为任何非退化倍线性形式。e的子空间u有有限维，如果u在f中有有限的余维。如果dim（u）是有限的，那么codim（u）=dim（u），u=u。

Proof. Since ϕ is nondegenerate E⊥ = {0} and F ⊥ = {0}, so Proposition 28.12 applied to the restriction of ϕ to U × F implies that a subspace U of E has finite dimension iff U⊥ has finite codimension in F, and that if dim(U) is finite, then codim(U⊥) = dim(U). Since U⊥ and U⊥⊥ are orthogonal, and since codim(U⊥) is finite, dim(U⊥⊥) is finite and we have dim( ) = codim(U⊥⊥⊥) = codim(U⊥) = dim(U). Since U ⊆ U⊥⊥, we must have
 证据。既然_是非退化的e=0和f=0，那么适用于_到u×f的限制的命题28.12意味着e的子空间u具有有限的维数iff u在f中具有有限的余维数，并且如果dim（u）是有限的，那么codim（u）=dim（u）。由于u和u是正交的，并且由于codim（u）是有限的，所以dim（u）是有限的，我们有dim（）=codim（u）=codim（u）=dim（u）。既然你你，我们必须

U = U       .                                                                                                                                           
 u=u。

Proposition 28.14. Let ϕ: E ×F → K be any sesquilinear form. Given any two subspaces U and V of E, we have
 提案28.14.设_：e×f→k为任意倍线性形式。对于任意两个子空间u和v of e，我们有

(U + V )⊥ = U⊥ ∩ V ⊥.
 （U+V）=U V。

Furthermore, if ϕ is nondegenerate and if U and V are finite-dimensional, then
 此外，如果_是非退化的，并且u和v是有限尺寸，那么

(U ∩ V )⊥ = U⊥ + V ⊥.
 （u v）=u+v。

Proof. If w ∈ (U + V )⊥, then ϕ(u + v,w) = 0 for all u ∈ U and all v ∈ V . In particular, with v = 0, we have ϕ(u,w) = 0 for all u ∈ U, and with u = 0, we have ϕ(v,w) = 0 for all v ∈ V , so w ∈ U⊥ ∩ V ⊥. Conversely, if w ∈ U⊥ ∩ V ⊥, then ϕ(u,w) = 0 for all u ∈ U and ϕ(v,w) = 0 for all v ∈ V . By bilinearity, ϕ(u + v,w) = ϕ(u,w) + ϕ(v,w) = 0, which shows that w ∈ (U + V )⊥. Therefore, the first identity holds.
 证据。如果w∈（u+v），那么对于所有u∈u和所有v∈v，w=0。特别是，当v=0时，所有u∈u都有（u，w）=0，当u=0时，所有v∈v都有（v，w）=0，因此w∈u v。相反，如果w∈u v，则所有u∈u和（v，w）=0，所有v∈v。根据双线性度，ω（u+v，w）＝（u，w）＋（v，w）=0，表示w∈（u+v）。因此，第一个身份是成立的。

Now, assume that ϕ is nondegenerate and that U and V are finite-dimensional, and let W = U⊥ + V ⊥. Using the equation that we just established and the fact that U and V are finite-dimensional, by Proposition 28.13, we get
 现在，假设_是非退化的，u和v是有限维，并假设w=u+v。利用我们刚刚建立的方程和u和v是有限维的事实，通过28.13号命题，我们得到

W ⊥ = U⊥⊥ ∩ V ⊥⊥ = U ∩ V.
 W=U=U V。

We can apply Proposition 28.12 to the restriction of ϕ to U × W (since U⊥ ⊆ W and
 我们可以将第28.12号提案应用于对_至u×w的限制（因为u w和

W ⊥ ⊆ U), and we get
 W U），我们得到

dim(U/W ⊥) = dim(U/(U ∩ V )) = dim(W/U⊥).
 dim（u/w）=dim（u/（u v））=dim（w/u）。

If T is a supplement of U⊥ in W so that W = U⊥ ⊕T and if S is a supplement of W in E so that E = W ⊕ S, then codim(W) = dim(S), dim(T) = dim(W/U⊥), and we have the direct sum
 如果t是w中u的一个补充，使w=u t，如果s是e中w的补充，使e=w s，那么codim（w）=dim（s），dim（t）=dim（w/u），我们得到了直接和

E = U⊥ ⊕ T ⊕ S
 E=U T S

which implies that
 这意味着

dim(T) = codim(U⊥) − dim(S) = codim(U⊥) − codim(W)
 dim（t）=codim（u）−dim（s）=codim（u）−codim（w）

so dim(U/(U ∩ V )) = dim(W/U⊥) = codim(U⊥) − codim(W),
 所以dim（u/（u v））=dim（w/u）=codim（u）−codim（w），

and since codim(U⊥) = dim(U), we deduce that
 由于codim（u）=dim（u），我们推断

dim(U ∩ V ) = codim(W).
 dim（u v）=codim（w）。

However, by Proposition 28.13, we have dim(U ∩ V ) = codim((U ∩ V )⊥), so codim(W) = codim((U ∩ V )⊥), and since W ⊆ W ⊥⊥ = (U ∩ V )⊥, we must have W = (U ∩ V )⊥, as claimed. 
 然而，根据第28.13号提案，我们有dim（u v）=codim（（u v）），因此codim（w）=codim（（u v）），既然w w w=（u v），我们必须有w=（u v），如所声称的。

In view of Proposition 28.12, we can make the following definition.
 根据28.12号提案，我们可以作出以下定义。

Definition 28.13. Let ϕ: E × F → K be any sesquilinear form. If E/F ⊥ and F/E⊥ are finite-dimensional, then their common dimension is called the rank of the form ϕ. If E/F ⊥ and F/E⊥ have infinite dimension, we say that ϕ has infinite rank.
 定义28.13.设_：e×f→k为任意倍线性形式。如果e/f和f/e是有限维，那么它们的共同维数称为形式的秩。如果e/f和f/e有无穷大的维数，我们称之为_有无穷大的秩。

Not surprisingly, the rank of ϕ is related to the ranks of lϕ and rϕ.
 不奇怪，_的等级与l_和r_的等级有关。

Proposition 28.15. Let ϕ: E × F → K be any sesquilinear form. If ϕ has finite rank r, then lϕ and rϕ have the same rank, which is equal to r.
 提案28.15。设_：e×f→k为任意倍线性形式。如果_具有有限等级R，则l_和r_具有相同等级，等于r。

Proof. Because for every u ∈ E,
 证据。因为对于每一个u∈e，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

​                                                  lϕ(u)(y) = ϕ(u,y)      for all y ∈ F,
 l_（u）（y）=（u，y）表示所有y∈f，

and for every v ∈ F, rϕ(v)(x) = ϕ(x,v) for all x ∈ E,
 对于所有x∈e，对于每个v∈f，r_（v）（x）=（x，v）

it is clear that the kernel of lϕ : E → F ∗ is equal to F ⊥ and that, the kernel of rϕ : F → E∗ is equal to E⊥. Therefore, rank(lϕ) = dim(Imlϕ) = dim(E/F ⊥) = r, and similarly rank(rϕ) = dim(F/E⊥) = r. 
 很明显，l_：e→f的核等于f_，r_：f→e_的核等于e_。因此，等级（L_）=dim（iml）=dim（e/f）=r，类似等级（r）=dim（f/e）=r。

Remark: If the sesquilinear form ϕ is represented by the matrix n × m matrix M with respect to the bases (e1,...,em) in E and (f1,...,fn) in F, it can be shown that the matrix representing lϕ with respect to the bases (e1,...,em) and (, and that the matrix representing rϕ with respect to the bases (f1,...,fn) and (. It follows that the rank of ϕ is equal to the rank of M.
 注：如果倍线性形式_由矩阵n×m表示，矩阵m关于e中的基（e1，…，em）和f中的（f1，…，fn），则可以证明矩阵代表l_关于基（e1，…，em）和（，矩阵代表r_关于baSES（F1，…，FN）和（.由此可知，_的等级等于m的等级。

## 28.4         Adjoint of a Linear Map  28.4线性图的伴随

Let E1 and E2 be two K-vector spaces, and let ϕ1 : E1×E1 → K be a sesquilinear form on E1 and ϕ2 : E2 ×E2 → K be a sesquilinear form on E2. It is also possible to deal with the more general situation where we have four vector spaces E1,F1,E2,F2 and two sesquilinear forms ϕ1 : E1 ×F1 → K and ϕ2 : E2 ×F2 → K, but we will leave this generalization as an exercise.
 设e1和e2为两个k向量空间，设_:e1×e1→k为e1上的倍线性形式，_:e2×e2→k为e2上的倍线性形式。也可以处理更一般的情况，即我们有四个向量空间e1、f1、e2、f2和两个倍线性形式_:e1×f1→k和_:e2×f2→k，但我们将把这个推广留作练习。

We also assume that lϕ1 and rϕ1 are bijective, which implies that that ϕ1 is nondegenerate. This is automatic if the space E1 is finite dimensional and ϕ1 is nondegenerate.
 我们还假设l_和r_是双射的，这意味着_是非退化的。如果空间e1为有限维，而_为非退化空间，则此操作为自动操作。

Given any linear map f : E1 → E2, for any fixed u ∈ E2, we can consider the linear form in given by x 7→ ϕ2(f(x),u),    x ∈ E1.
 给定任意一个线性映射f:e1→e2，对于任意一个固定的u∈e2，我们可以考虑x 7→_（f（x），u），x∈e1给出的线性形式。

Since is bijective, there is a unique y ∈ E1 (because the vector spaces E1 and
 由于是双目标的，所以有一个唯一的y∈e1（因为向量空间e1和

E1 only differ by scalar multiplication), so that
 e1只因标量乘法而不同），因此

​                                              ϕ2(f(x),u) = ϕ1(x,y),       for all x ∈ E1.
 _（f（x），u）=_（x，y），对于所有x∈e1。

If we denote this unique y ∈ E1 by f∗l(u), then we have
 如果我们用f l（u）表示这个唯一的y∈e1，那么我们有

​                             ϕ2(f(x),u) = ϕ1(x,f∗l(u)),         for all x ∈ E1, and all u ∈ E2.
 _（f（x），u）=_（x，f l（u）），对于所有x∈e1和所有u∈e2。

Thus, we get a function f∗l : E2 → E1. We claim that this function is a linear map. For any v1,v2 ∈ E2, we have
 因此，我们得到一个函数f l:e2→e1。我们声称这个函数是一个线性映射。对于任何v1，v2∈e2，我们有

ϕ2(f(x),v1 + v2) = ϕ2(f(x),v1) + ϕ2(f(x),v2)
 _（f（x），v1+v2）=_（f（x），v1）+_（f（x），v2）

= ϕ1(x,f∗l(v1)) + ϕ1(x,f∗l(v2))
 =_1（x，f_l（v1））+_1（x，f_l（v2））

= ϕ1(x,f∗l(v1) + f∗l(v2)) = ϕ1(x,f∗l(v1 + v2)),
 =_1（x，f l（v1）+f l（v2））=_1（x，f l（v1+v2）），

for all x ∈ E1. Since rϕ1 is injective, we conclude that
 对于所有x∈e1。既然R_1是注射剂，我们得出结论：

f∗l(v1 + v2) = f∗l(v1) + f∗l(v2).
 f l（v1+v2）=f l（v1）+f l（v2）。

For any λ ∈ K, we have
 对于任何λ∈k，我们有

,
 ，

for all x ∈ E1. Since rϕ1 is injective, we conclude that
 对于所有x∈e1。既然R_1是注射剂，我们得出结论：

f∗l(λv) = λf∗l(v).
 f l（λv）=λf l（v）。


 

28.4. ADJOINT OF A LINEAR MAP
 28.4。线性映射的伴随

Therefore, f∗l is linear. We call it the left adjoint of f.
 因此，f l是线性的。我们称之为f的左伴随。

Now, for any fixed u ∈ E2, we can consider the linear form in given by
 现在，对于任何固定的u∈e2，我们可以考虑下式中的线性形式。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image028.gif)

​                                                         x 7→ ϕ2(u,f(x))     x ∈ E1.
 x 7→_（u，f（x））x∈e1.

Since is bijective, there is a unique y ∈ E1 so that
 因为是双目标的，所以有一个唯一的y∈e1，所以

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image029.gif)

​                                               ϕ2(u,f(x)) = ϕ1(y,x),       for all x ∈ E1.
 _（u，f（x））=_（y，x），对于所有x∈e1。

If we denote this unique y ∈ E1 by f∗r(u), then we have
 如果我们用f r（u）表示这个唯一的y∈e1，那么我们有

​                             ϕ2(u,f(x)) = ϕ1(f∗r(u),x),         for all x ∈ E1, and all u ∈ E2.
 _（u，f（x））=_（f r（u），x），对于所有x∈e1和所有u∈e2。

Thus, we get a function f∗r : E2 → E1. As in the previous situation, it easy to check that f∗r is linear. We call it the right adjoint of f. In summary, we make the following definition.
 因此，我们得到一个函数f r:e2→e1。和前面的情况一样，很容易检查f r是线性的。我们称之为f的右伴随。总之，我们做出如下定义。

Definition 28.14. Let E1 and E2 be two K-vector spaces, and let ϕ1 : E1 × E1 → K and ϕ2 : E2 × E2 → K be two sesquilinear forms. Assume that lϕ1 and rϕ1 are bijective, so that ϕ1 is nondegnerate. For every linear map f : E1 → E2, there exist unique linear maps f∗l : E2 → E1 and f∗r : E2 → E1, such that
 定义28.14.设e1和e2为两个k向量空间，设_:e1×e1→k和_:e2×e2→k为两个倍线性形式。假设l_1和r_1是双射的，因此，_1是不偏袒的。对于每个线性映射f:e1→e2，都存在唯一的线性映射f l:e2→e1和f r:e2→e1，这样

ϕ2(f(x),u) = ϕ1(x,f∗l(u)), for all x ∈ E1, and all u ∈ E2 ϕ2(u,f(x)) = ϕ1(f∗r(u),x), for all x ∈ E1, and all u ∈ E2.
 _（f（x），u）=_（x，f l（u）），对于所有x∈e1，并且所有u∈e2（u，f（x））=_（f r（u），x），对于所有x∈e1，和所有u∈e2。

The map f∗l is called the left adjoint of f, and the map f∗r is called the right adjoint of f.
 图f_l称为f的左伴随，图f_r称为f的右伴随。

If E1 and E2 are finite-dimensional with bases (e1,...,em) and (f1,...,fn), then we can work out the matrices A∗l and A∗r corresponding to the left adjoint f∗l and the right adjoint f∗r of f. Assumine that f is represented by the n × m matrix A, ϕ1 is represented by the m × m matrix M1, and ϕ2 is represented by the n × n matrix M2. Since
 如果e1和e2是基（e1，…，em）和（f1，…，f n）的有限维，那么我们就可以算出对应于f的左伴f l和右伴f r的矩阵a l和a r。假设f由n×m矩阵a表示，那么，ω1由m×m矩阵m1表示，_用n×n矩阵m2表示。自从

ϕ1(x,f∗l(u)) = (A∗lu)∗M1x = u∗(A∗l)∗M1x
 ⑨1（x，f l（u））=（a lu）m1x=u（a l）m1x

ϕ2(f(x),u) = u∗M2Ax
 _（f（x），u）=u m2ax

we find that (A∗l)∗M1 = M2A, that is (A∗l)∗ = M2AM1−1, and similarly
 我们发现（a l）m1=m2a，即（a l）=m2am1−1，并且类似地

ϕ1(f∗r(u),x) = x∗M1A∗ru
 _1（f_r（u），x）=x m1a_ru

ϕ2(u,f(x)) = (Ax)∗M2u = x∗A∗M2u,
 _（u，f（x））=（ax）m2u=x a m2u，

we have M1A∗r = A∗M2, that is A∗r = (M1)−1A∗M2. Thus, we obtain
 我们有m1 a r=a m2，即a r=（m1）−1a m2。因此，我们得到

A∗l = (M1∗)−1A∗M2∗
 a l=（m1）−1a m2

A∗r = (M1)−1A∗M2.
 a r=（m1）−1a m2。

If ϕ1 and ϕ2 are symmetric bilinear forms, then f∗l = f∗r. This also holds if ϕ is -Hermitian. Indeed, since ϕ2(u,f(x)) = ϕ1(f∗r(u),x),
 如果_1和_2是对称双线性形式，则f l=f r。如果_是-厄米提安，这也适用。事实上，由于_（u，f（x））=_（f r（u），x），

we get
 我们得到

,
 ，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image030.gif)

and since λ 7→ λ is an involution, we get
 既然λ7→λ是对合的，我们得到

ϕ2(f(x),u) = ϕ1(x,f∗r(u)).
 _（f（x），u）=_（x，f r（u））。

Since we also have ϕ2(f(x),u) = ϕ1(x,f∗l(u)),
 因为我们还有_（f（x），u）=_（x，f l（u）），

we obtain ϕ1(x,f∗r(u)) = ϕ1(x,f∗l(u))       for all x ∈ E1, and all u ∈ E2,
 对于所有x∈e1和所有u∈e2，我们得到_（x，f r（u））=_（x，f l（u）），

and since ϕ1 is nondegenerate, we conclude that f∗l = f∗r. Whenever f∗l = f∗r, we use the simpler notation f∗.
 既然_1是非退化的，我们得出的结论是f l=f r。每当f l=f r时，我们使用更简单的符号f。

If f : E1 → E2 and g: E1 → E2 are two linear maps, we have the following properties:
 如果f:e1→e2和g:e1→e2是两个线性映射，则我们具有以下特性：

(f    + g)∗l = f∗l + g∗l id∗l = id
 +g）l=f l+g l id l=id

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image031.gif)

(λf)∗l = λf∗l,
 （λf）l=λf l，

and similarly for right adjoints. If E3 is another space, ϕ3 is a sesquilinear form on E3, and if lϕ2 and rϕ2 are bijective, then for any linear maps f : E1 → E2 and g: E2 → E3, we have
 同样地，对于正确的邻接。如果e3是另一个空间，那么，在e3上，_是一个双线性形式，如果l_和r_是双射的，那么对于任何线性映射f:e1→e2和g:e2→e3，我们有

(g   ◦ f)∗l = f∗l ◦ g∗l,
 _f）l=f l g l，

and similarly for right adjoints. Furthermore, if E1 = E2 = E andl                      ϕ: rE × E → K is
 同样地，对于正确的邻接。此外，如果e1=e2=e和l_：re×e→k为

-Hermitian, for any linear map f : E → E (recall that in this case f∗ = f∗ = f∗), we have
 -Hermitian，对于任何线性映射f:e→e（回想一下，在本例中f=f=f），我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image033.gif)

## 28.5         Isometries Associated with Sesquilinear Forms  28.5与倍线性形式相关的等轴测图

The notion of adjoint is a good tool to investigate the notion of isometry between spaces equipped with sesquilinear forms. First, we define metric maps and isometries.
 伴随概念是研究具有倍线性形式的空间之间等距概念的一个很好的工具。首先，我们定义度量图和等轴测图。

Definition 28.15. If (E1,ϕ1) and (E2,ϕ2) are two pairs of spaces and sesquilinear maps ϕ1 : E1 × E1 → K and ϕ2 : E2 × E2 → K, a metric map from (E1,ϕ1) to (E2,ϕ2) is a linear map f : E1 → E2 such that
 定义28.15.如果（e1，_）和（e2，_）是两对空间和双线性映射，那么（e1，_）到（e2，_）的公制映射是线性映射f:e1→e2，因此

​                                           ϕ1(u,v) = ϕ2(f(u),f(v))       for all u,v ∈ E1.
 所有u，v∈e1的_（u，v）=_（f（u），f（v））。

We say that ϕ1 and ϕ2 are equivalent iff there is a metric map f : E1 → E2 which is bijective.
 我们说，如果有一个公制图f:e1→e2是双射的，那么_和_是等效的。

Such a metric map is called an isometry.
 这样一个度量图被称为等距图。

28.5. ISOMETRIES ASSOCIATED WITH SESQUILINEAR FORMS
 28.5。与倍线性形式相关的等轴测图

The problem of classifying sesquilinear forms up to equivalence is an important but very difficult problem. Solving this problem depends intimately on properties of the field K, and a complete answer is only known in a few cases. The problem is easily solved for K = R, K = C. It is also solved for finite fields and for K = Q (the rationals), but the solution is surprisingly involved!
 将倍线性形式分类到等价形式是一个重要而困难的问题。解决这个问题与K场的性质密切相关，只有在少数情况下才知道完整的答案。对于k=r，k=c，这个问题很容易解决。对于有限域和k=q（有理数），这个问题也可以解决，但令人惊讶的是，这个问题涉及到了这个问题！

It is hard to say anything interesting if ϕ1 is degenerate and if the linear map f does not have adjoints. The next few propositions make use of natural conditions on ϕ1 that yield a useful criterion for being a metric map.
 很难说有什么有趣的东西，如果ω1退化，如果线性映射f没有邻接。接下来的几个命题利用了第5.1条的自然条件，得出了作为度量图的有用标准。

Proposition 28.16. With the same assumptions as in Definition 28.14 (which imply that ϕ1 is nondegenerate), if f : E1 → E2 is a bijective linear map, then we have
 提案28.16。如果F:e1→e2是一个双射线性映射，那么我们有

ϕ1(x,y) = ϕ2(f(x),f(y)) for all x,y ∈ E1 iff f−1 = f∗l = f∗r.
 所有x，y∈e1 iff−1=f l=f r时，_（x，y）=_（f（x），f（y））。

Proof. We have ϕ1(x,y) = ϕ2(f(x),f(y))
 证据。我们有_（x，y）=_（f（x），f（y））

iff ϕ1(x,y) = ϕ2(f(x),f(y)) = ϕ1(x,f∗l(f(y))
 iff_1（x，y）=_（f（x），f（y））=_（x，f_l（f（y））

iff
 敌我识别

​                              ϕ1(x,(id − f∗l ◦ f)(y)) = 0       for all x ∈ E1 and all y ∈ E2.
 所有x e1和所有y e2中，1（x，（id−f l f）（y））=0。

Since ϕ1 is nondegenerate, we must have
 既然_是非退化的，我们必须

f∗l ◦ f = id,
 F L F=身份证，

which implies that f−1 = f∗l. Similarly,
 这意味着f−1=f l。类似地，

ϕ1(x,y) = ϕ2(f(x),f(y))
 _（x，y）=_（f（x），f（y））

iff ϕ1(x,y) = ϕ2(f(x),f(y)) = ϕ1(f∗r(f(x)),y)
 iff_1（x，y）=_（f（x），f（y））=_（f r（f（x）），y）

iff
 敌我识别

​                             ϕ1((id − f∗r ◦ f)(x),y) = 0       for all x ∈ E1 and all y ∈ E2.
 ⑨1（（id−f r f）（x），y）=0，表示所有x∈e1和所有y∈e2。

Since ϕ1 is nondegenerate, we must have
 既然_是非退化的，我们必须

f∗r ◦ f = id,
 F R F=ID，

which implies that f−1 = f∗r. Therefore, f−1 = f∗l = f∗r. For the converse, do the computations in reverse. 
 这意味着f−1=f r。因此，f−1=f l=f r。相反，进行反向计算。

As a corollary, we get the following important proposition.
 作为推论，我们得到以下重要命题。

Proposition 28.17. If ϕ: E ×E → K is a sesquilinear map, and if lϕ and rϕ are bijective, for every bijective linear map f : E → E, then we have
 提案28.17。如果ω：e×e→k是一个双线性映射，并且如果l瓒和r瓒是双线性映射，那么对于每个双线性映射f:e→e，我们有

ϕ(f(x),f(y)) = ϕ(x,y) for all x,y ∈ E iff f−1 = f∗l = f∗r.
 所有x，y∈e iff f−1=f l=f r时，（f（x），f（y））=（x，y）。

We also have the following facts.
 我们还有以下事实。

Proposition 28.18. (1) If ϕ: E × E → K is a sesquilinear map and if lϕ is injective, then for every linear map f : E → E, if
 提案28.18。（1）如果ω：e×e→k是一个双线性映射，如果lω是内射的，那么对于每个线性映射f:e→e，如果

​                                              ϕ(f(x),f(y)) = ϕ(x,y)         for all x,y ∈ E,                                        (∗)
 所有x，y∈e，（）

then f is injective.
 那么F是注射剂。

(2) If E is finite-dimensional and if ϕ is nondegenerate, then the linear maps f : E → E satisfying (∗) form a group. The inverse of f is given by f−1 = f∗.
 （2）如果e是有限维，如果_是非退化的，那么线性映射f:e→e满足（）形成一个群。f的倒数由f−1=f给出。

Proof. (1) If f(x) = 0, then
 证据。（1）如果f（x）=0，则

​                                   ϕ(x,y) = ϕ(f(x),f(y)) = ϕ(0,f(y)) = 0          for all y ∈ E.
 所有y∈e时，ω（x，y）＝（f（x），f（y））＝（0，f（y））=0。

Since lϕ is injective, we must have x = 0, and thus f is injective.
 既然l_是注射剂，我们必须有x=0，因此f是注射剂。

(2) If E is finite-dimensional, since a linear map satisfying (∗) is injective, it is a bijection.
 （2）如果e是有限维，因为满足（）的线性映射是内射的，它是双射的。

By Proposition 28.17, we have f−1 = f∗. We also have ϕ(f(x),f(y)) = ϕ((f∗ ◦ f)(x),y) = ϕ(x,y) = ϕ((f ◦ f∗)(x),y) = ϕ(f∗(x),f∗(y)),
 根据命题28.17，我们得到f−1=f。我们还有（f（x），f（y））=（f（f）（x），y）=（x，y）=（f f）（x），y）=（f（x），f（y）），

which shows that f∗ satisfies (∗). If ϕ(f(x),f(y)) = ϕ(x,y) for all x,y ∈ E and ϕ(g(x),g(y))
 这表明f满足（）。如果所有x，y∈e和（g（x），g（y））=_（x，y），则

= ϕ(x,y) for all x,y ∈ E, then we have
 =（x，y）对于所有x，y∈e，那么我们有

​                        ϕ((g ◦ f)(x),(g ◦ f)(y)) = ϕ(f(x),f(y)) = ϕ(x,y)         for all x,y ∈ E.
 所有x，y∈e的（（g f）（x），（g f）（y））=_（f（x），f（y））=（x，y）。

Obviously, the identity map idE satisfies (∗). Therefore, the set of linear maps satisfying (∗) is a group.
 显然，标识映射ide满足（）。因此，满足（）的线性映射集是一组。

The above considerations motivate the following definition.
 上述考虑激发了以下定义。

Definition 28.16. Let ϕ: E × E → K be a sesquilinear map, and assume that E is finitedimensional and that ϕ is nondegenerate. A linear map f : E → E is an isometry of E (with respect to ϕ) iff ϕ(f(x),f(y)) = ϕ(x,y) for all x,y ∈ E.
 定义28.16.设_：e×e→k为倍线性映射，假设e为有限维，_为非退化。线性图f:e→e是e（关于_）iff_（f（x），f（y））=_（x，y）的等距图，适用于所有x，y∈e。

The set of all isometries of E is a group denoted by Isom(ϕ).
 e的所有等轴测集是一组由isom（a）表示的组。

28.5. ISOMETRIES ASSOCIATED WITH SESQUILINEAR FORMS
 28.5。与倍线性形式相关的等轴测图

If ϕ is symmetric, then the group Isom(ϕ) is denoted O(ϕ) and called the orthogonal group of ϕ. If ϕ is alternating, then the group Isom(ϕ) is denoted Sp(ϕ) and called the symplectic group of -Hermitian, then the group Isom(ϕ) is denoted U) and called the -unitary group of ϕ. When  = 1, we drop  and just say unitary group.
 如果直径对称，则组isom（直径）表示为o（直径），称为直径的正交组。如果_是交替的，则组isom（_）表示为sp（_），称为-Hermitian的辛群，则组isom（_）表示为u）并称为_的-单一群。当=1时，我们放弃，只说一元群。

If (e1,...,en) is a basis of E, ϕ is the represented by thel r n × n matrix M, and f is represented by the n × n matrix A, since A−1 = A∗ = A∗ = M−1A∗M, then we find that f ∈ Isom(ϕ) iff
 如果（e1，…，e n）是e的一个基，那么_是由thel r n×n矩阵m表示的，而f是由n×n矩阵a表示的，因为a−1=a=a=m−1a m，那么我们发现f∈isom（）iff

A∗MA = M,
 a ma=m，

and A−1 is given by A−1 = M−1A∗M.
 a−1由a−1=m−1a m给出。

More specifically, we define the following groups, using the matrices Ip,q,Jm,m and Am,m defined at the end of Section 28.1.
 更具体地说，我们使用第28.1节末尾定义的矩阵ip、q、jm、m和am、m来定义以下组。

(1)    K = R. We have
 K=R，我们有

O(n) = {A ∈ Mn(R) | A>A = In}
 o（n）=a∈mn（r）a>a=in

O(p,q) = {A ∈ Mp+q(R) | A>Ip,qA = Ip,q}
 o（p，q）=a∈mp+q（r）a>ip，qa=ip，q

Sp(2n,R) = {A ∈ M2n(R) | A>Jn,nA = Jn,n}
 sp（2n，r）=a∈m2n（r）a>jn，na=jn，n

SO(n) = {A ∈ Mn(R) | A>A = In, det(A) = 1}
 所以（n）=a∈mn（r）a>a=in，det（a）=1

SO(p,q) = {A ∈ Mp+q(R) | A>Ip,qA = Ip,q, det(A) = 1}.
 所以（p，q）=a∈mp+q（r）a>ip，qa=ip，q，det（a）=1。

The group O(n) is the orthogonal group, Sp(2n,R) is the real symplectic group, and SO(n) is the special orthogonal group. We can define the group
 群O（n）是正交群，sp（2n，r）是实辛群，所以（n）是特殊正交群。我们可以定义这个组

{A ∈ M2n(R) | A>An,nA = An,n},
 a∈m2n（r）a>a n，na=an，n，

but it is isomorphic to O(n,n).
 但它与O（N，N）同构。

(2)    K = C. We have
 K=C，我们有

U(n) = {A ∈ Mn(C) | A∗A = In}
 u（n）=a∈mn（c）a a=in

U(p,q) = {A ∈ Mp+q(C) | A∗Ip,qA = Ip,q}
 u（p，q）=a∈mp+q（c）a ip，qa=ip，q

Sp(2n,C) = {A ∈ M2n(C) | A>Jn,nA = Jn,n}
 sp（2n，c）=a∈m2n（c）a>jn，na=jn，n

SU(n) = {A ∈ Mn(C) | A∗A = In, det(A) = 1}
 su（n）=a∈mn（c）a a=in，det（a）=1

SU(p,q) = {A ∈ Mp+q(C) | A∗Ip,qA = Ip,q, det(A) = 1}.
 su（p，q）=a∈mp+q（c）a ip，qa=ip，q，det（a）=1。

The group U(n) is the unitary group, Sp(2n,C) is the complex symplectic group, and SU(n) is the special unitary group.
 群U（n）是一元群，sp（2n，c）是复辛群，su（n）是特殊的一元群。

It can be shown that if A ∈ Sp(2n,R) or if A ∈ Sp(2n,C), then det(A) = 1.
 可以看出，如果a∈sp（2n，r）或a∈sp（2n，c），那么det（a）=1。

## 28.6        Totally Isotropic Subspaces  28.6完全各向同性子空间

In this section, we deal with -Hermitian forms, ϕ: E × E → K. In general, E may have subspaces U such that U ∩ U⊥ = (0)6 , or worse, such that U ⊆ U⊥ (that is, ϕ is zero on U). We will see that such subspaces play a crucial in the decomposition of E into orthogonal subspaces.
 在本节中，我们讨论了-厄米特形式，:e×e→k。一般来说，e可能有子空间u，使得u（0）6，或更糟，这样u u（即，_在u上为零）。我们将看到这些子空间在将e分解为正交子空间中起着关键作用。

Definition 28.17. Given an -Hermitian forms ϕ: E × E → K, a nonzero vector u ∈ E is said to be isotropic if ϕ(u,u) = 0. It is convenient to consider 0 to be isotropic. Given any subspace U of E, the subspace rad(U) = U ∩ U⊥ is called the radical of U. We say that
 定义28.17.给定一个-厄米式，如果_（u，u）=0，则非零矢量u∈e称为各向同性。将0考虑为各向同性是很方便的。对于e的任何子空间u，子空间rad（u）=u u称为u的根式。

(i)      U is degenerate if rad(U) = (0) (6 equivalently if there is some nonzero vector u ∈ U such that x ∈ U⊥). Otherwise, we say that U is nondegenerate.
 如果rad（u）=（0）（6等价，如果有一些非零向量u∈u，那么u是退化的，这样x∈u）。否则，我们就说u是非退化的。

(ii)    U is totally isotropic if U ⊆ U⊥ (equivalently if the restriction of ϕ to U is zero).
 如果u u，u是完全各向同性的（如果_到u的限制为零，则等于）。

By definition, the trivial subspace U = (0) (= {0}) is nondegenerate. Observe that a subspace U is nondegenerate iff the restriction of ϕ to U is nondegenerate. A degenerate subspace is sometimes called an isotropic subspace. Other authors say that a subspace U is isotropic if it contains some (nonzero) isotropic vector. A subspace which has no nonzero isotropic vector is often called anisotropic. The space of all isotropic vectors is a cone often called the light cone (a terminology coming from the theory of relativity). This is not to be confused with the cone of silence (from Get Smart)! It should also be noted that some authors (such as Serre) use the term isotropic instead of totally isotropic. The apparent lack of standard terminology is almost as bad as in graph theory!
 根据定义，平凡子空间u=（0）（=0）是非退化的。观察到子空间u是非简并的，而如果对u的限制是非简并的。退化子空间有时称为各向同性子空间。其他作者说，如果子空间U包含一些（非零）各向同性向量，则它是各向同性的。没有非零各向同性向量的子空间通常称为各向异性。所有各向同性向量的空间都是一个圆锥，通常称为光锥（一个术语来自相对论）。不要把这和沉默的锥体混淆（从聪明做起）！还应注意的是，有些作者（如SERRE）使用了“各向同性”一词，而不是“完全各向同性”。明显缺乏标准术语几乎和图论一样糟糕！

It is clear that any direct sum of pairwise orthogonal totally isotropic subspaces is totally isotropic. Thus, every totally isotropic subspace is contained in some maximal totally isotropic subspace. Here is another fact that we will use all the time: if V is a totally isotropic subspace and if U is a subspace of V , then U is totally isotropic.
 很明显，任何成对正交完全各向同性子空间的直接和都是完全各向同性的。因此，每个完全各向同性子空间都包含在一些最大的完全各向同性子空间中。还有一个事实，我们将一直使用：如果v是一个完全各向同性的子空间，如果u是v的子空间，那么u是完全各向同性的。

This is because by definition V is isotropic if V ⊆ V ⊥, and since U ⊆ V we get V ⊥ ⊆ U⊥, so U ⊆ V ⊆ V ⊥ ⊆ U⊥, which shows that U is totally isotropic.
 这是因为根据定义，如果v v，v是各向同性的，既然u，我们得到v u，那么u v u，这表明u是完全各向同性的。

First, let us show that in order to sudy an -Hermitian form on a space E, it suffices to restrict our attention to nondegenerate forms.
 首先，让我们证明，为了在空间E上苏迪安-赫米特形式，它足以限制我们对非退化形式的关注。

Proposition 28.19. Given an -Hermitian form ϕ: E × E → K on E, we have:
 提案28.19。给定一个-厄米提亚式，在e上：e×e→k，我们有：

*(a)*     If U and V are any two orthogonal subspaces of E, then
 如果u和v是e的任意两个正交子空间，那么

rad(U + V ) = rad(U) + rad(V ).
 rad（u+v）=rad（u）+rad（v）。

*(b)*     rad(rad(E)) = rad(E).
 rad（rad（e））=rad（e）。


 

*(c)*     If U is any subspace supplementary to rad(E), so that
 如果u是rad（e）的补充子空间，那么

E = rad(E) ⊕ U,
 e=rad（e）u，

then U is nondegenerate, and rad(E) and U are orthogonal.
 那么u是非退化的，rad（e）和u是正交的。

Proof. (a) If U and V are orthogonal, then U ⊆ V ⊥ and V ⊆ U⊥. We get
 证据。（a）如果u和v是正交的，则u v和v u。我们得到

rad(U + V ) = (U + V ) ∩ (U + V )⊥
 rad（u+v）=（u+v）（u+v）

= (U + V ) ∩ U⊥ ∩ V ⊥
 =（U+V）U V

= U ∩ U⊥ ∩ V ⊥ + V ∩ U⊥ ∩ V ⊥
 =U U V+V U V

= U ∩ U⊥ + V ∩ V ⊥
 =U U+V V

= rad(U) + rad(V ).
 =rad（u）+rad（v）。

(b)   By definition, rad(E) = E⊥, and obviously E = E⊥⊥, so we get
 根据定义，rad（e）=e，显然e=e，所以我们得到

rad(rad(E)) = E⊥ ∩ E⊥⊥ = E⊥ ∩ E = E⊥ = rad(E).
 rad（rad（e））=e=e=rad（e）。

(c)    If E = rad(E)⊕U, by definition of rad(E), the subspaces rad(E) and U are orthogonal. From (a) and (b), we get rad(E) = rad(E) + rad(U).
 如果e=rad（e）u，根据rad（e）的定义，子空间rad（e）和u是正交的。从（a）和（b），我们得到rad（e）=rad（e）+rad（u）。

Since rad(U) = U ∩ U⊥ ⊆ U and since rad(E) ⊕ U is a direct sum, we have a direct sum
 因为rad（u）=u u u和rad（e）u是一个直接和，所以我们有一个直接和

rad(E) = rad(E) ⊕ rad(U),
 rad（e）=rad（e）rad（u）、

which implies that rad(U) = (0); that is, U is nondegenerate.                                                       
 这意味着rad（u）=0；也就是说，u是非退化的。

Proposition 28.19(c) shows that the restriction of ϕ to any supplement U of rad(E) is nondegenerate and ϕ is zero on rad(U), so we may restrict our attention to nondegenerate forms.
 命题28.19（c）表明，对rad（e）的任何补充u的限制为非退化形式，而对rad（u）的限制为零，因此我们可以将注意力限制在非退化形式。

The following is also a key result.
 以下也是一个关键结果。

Proposition 28.20. Given an -Hermitian form ϕ: E × E → K on E, if U is a finitedimensional nondegenerate subspace of E, then E = U ⊕ U⊥.
 提案28.20。在e上给出了一个-厄米式，如果u是e的有限维非退化子空间，那么e=u u。

Proof. By hypothesis, the restriction ϕU of ϕ to U is nondegenerate, so the semilinear map rϕU : U → U∗ is injective. Since U is finite-dimensional, rϕU is actually bijective, so for every v ∈ E, if we consider the linear form in U∗ given by u 7→ ϕ(u,v) (u ∈ U), there is a unique v0 ∈ U such that ϕ(u,v0) = ϕ(u,v) for all u ∈ U;
 证据。根据假设，对u的限制是非退化的，所以半线性映射r_u:u→u_是内射的。由于u是有限维的，r_u实际上是双射的，所以对于每一个v∈e，如果我们考虑u中由u 7给出的线性形式（u，v）（u∈u），就有一个唯一的v0∈u，使得所有u∈u的_（u，v0）=（u，v）；

that is, ϕ(u,v − v0) = 0 for all u ∈ U, so v − v0 ∈ U⊥. It follows that v = v0 + v − v0, with v0 ∈ U and v0 −v ∈ U⊥, and since U is nondegenerate U ∩U⊥ = (0), and E = U ⊕U⊥. 
 也就是说，对于所有u∈u，那么v−v0∈u来说，（u，v−v0）=0。由此可知，v=v0+v−v0，其中v0∈u和v0−v∈u，由于u是非退化的u u=（0），并且e=u u。

As a corollary of Proposition 28.20, we get the following result.
 作为28.20号命题的推论，我们得到如下结果。

Proposition 28.21. Given an -Hermitian form ϕ: E×E → K on E, if ϕ is nondegenerate and if U is a finite-dimensional subspace of E, then rad(U) = rad(U⊥), and the following conditions are equivalent:
 提案28.21。给定-Hermitian形式，在e上：e×e→k，如果_是非退化的，并且如果u是e的有限维子空间，那么rad（u）=rad（u），并且下列条件是等效的：

*(i)*          U is nondegenerate.
 u是非退化的。

*(ii)*       U⊥ is nondegenerate.
 U是非退化的。

*(iii)*     E = U ⊕ U⊥.
 E=U U。

Proof. By definition, rad(U⊥) = U⊥ ∩ U⊥⊥, and since ϕ is nondegenerate and U is finitedimensional, U⊥⊥ = U, so rad(U⊥) = U⊥ ∩ U⊥⊥ = U ∩ U⊥ = rad(U).
 证据。根据定义，rad（u）=u u，由于_是非退化的，u是有限维，u=u，所以rad（u）=u=u=rad（u）。

By Proposition 28.20, (i) implies (iii). If E = U ⊕ U⊥, then rad(U) = U ∩ U⊥ = (0), so U is nondegenerate and (iii) implies (i). Since rad(U⊥) = rad(U), (iii) also implies (ii).
 根据28.20号提案，（i）暗示（iii）。如果e=u u，那么rad（u）=u u=（0），那么u是非退化的，并且（i i i）意味着（i）。因为rad（u）=rad（u），（iii）也意味着（ii）。

Now, if U⊥ is nondegenerate, we have U⊥ ∩ U⊥⊥ = (0), and since U ⊆ U⊥⊥, we get
 现在，如果u是非退化的，我们就得到u=（0），而且既然u u，我们得到

U ∩ U⊥ ⊆ U⊥⊥ ∩ U⊥ = (0),
 U U U=0，

which shows that U is nondegenerate, proving the implication (ii) =⇒ (i).                                
 这表明U是非简并的，证明其含义（i i）=⇒（i）。

If E is finite-dimensional, we have the following results.
 如果e是有限维的，我们得到以下结果。

Proposition 28.22. Given an -Hermitian form ϕ: E × E → K on a finite-dimensional space E, if ϕ is nondegenerate, then for every subspace U of E we have
 提案28.22。给定有限维空间e上的-Hermitian形式：e×e→k，如果该形式为非退化形式，则对于e的每个子空间u，我们都有

*(i)*       dim(U) + dim(U⊥) = dim(E).
 dim（u）+dim（u）=dim（e）。

*(ii)*     U⊥⊥ = U.
 U=U.

Proof. (i) Since ϕ is nondegenerate and E is finite-dimensional, the semilinear map lϕ : E →
 证据。（i）由于_是非退化的，e是有限维，半线性图l_：e→

E∗ is bijective. By transposition, the inclusion i: U → E yields a surjection r: E∗ → U∗
 E是双主题的。通过转位，包涵体i:u→e产生一个推测r:e→u

(with r(f) = f ◦ i for every f ∈ E∗; the map f ◦ i is the restriction of the linear form f to
 （其中r（f）=f i对于每一个f∈e映射f i是线性形式f对

U). It follows that the semilinear map r ◦ lϕ : E → U∗ given by
 U）。由此可知，半线性图r_l_：e→u由下式给出

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image034.gif)

​                                              (r ◦ lϕ)(x)(u) = ϕ(x,u)      x ∈ E,u ∈ U
 （r_l_）（x）（u）＝（x，u）x∈e，u∈u

is surjective, and its kernel is U⊥. Thus, we have
 是主观性的，它的核心是u。因此，我们

dim(U∗) + dim(U⊥) = dim(E),
 尺寸（U）+尺寸（U）=尺寸（E）

and since dim(U) = dim(U∗) because U is finite-dimensional, we get
 因为dim（u）=dim（u），因为u是有限维，我们得到

dim(U) + dim(U⊥) = dim(U∗) + dim(U⊥) = dim(E).
 dim（u）+dim（u）=dim（u）+dim（u）=dim（e）。

(ii) Applying the above formula to U⊥, we deduce that dim(U) = dim(U⊥⊥). Since U ⊆ U⊥⊥, we must have U⊥⊥ = U.    
 （ii）将上述公式应用于u，我们推导出dim（u）=dim（u）。因为u u，我们必须有u=u。

Remark: We already proved in Proposition 28.13 that if U is finite-dimensional, then codim(U⊥) = dim(U) and U⊥⊥ = U, but it doesn’t hurt to give another proof. Observe that (i) implies that dim(U) + dim(rad(U)) ≤ dim(E).
 注：我们已经在28.13号命题中证明了，如果u是有限维的，那么codim（u）=dim（u）和u=u，但给出另一个证明并不伤人。观察（i）表示dim（u）+dim（rad（u））≤dim（e）。

We can now proceed with the Witt decomposition, but before that, we quickly take care of the structure theorem for alternating bilinear forms (the case where ϕ(u,u) = 0 for all u ∈ E). For an alternating bilinear form, the space E is totally isotropic. For example in dimension 2, the matrix
 我们现在可以继续进行维特分解，但在这之前，我们很快地处理了交替双线性形式的结构定理（其中，所有的u∈e，都是ω（u，u）=0的情况）。对于交替双线性形式，空间E是完全各向同性的。例如，在维度2中，矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image036.gif)

defines the alternating form given by
 定义由给定的交替形式

ϕ((x1,y1),(x2,y2)) = x1y2 − x2y1.
 ⑨（（x1，y1），（x2，y2））=x1y2−x2y1。

This case is surprisingly general.
 这件事非常普遍。

Proposition 28.23. Let ϕ: E × E → K be an alternating bilinear form on E. If u,v ∈ E are two (nonzero) vectors such that ϕ(u,v) = λ = 06 , then u and v are linearly independent. If we let u1 = λ−1u and v1 = v, then ϕ(u1,v1) = 1, and the restriction of ϕ to the plane spanned by u1 and v1 is represented by the matrix
 提案28.23。设ω：e×e→k为e上的一个交替双线性形式，如果u，v∈e是两个（非零）向量，使得ω（u，v）=λ=06，则u和v是线性无关的。如果我们让u1=λ−1u和v1=v，那么（u1，v1）=1，并且_对u1和v1所跨越平面的限制由矩阵表示。

.
 .

Proof. If u and v were linearly dependent, as u,v = 06 , we could write v = µu for some µ = 06 , but then, since ϕ is alternating, we would have
 证据。如果u和v是线性相关的，如u，v=06，我们可以为一些礹=06写v=礹u，但是，由于礹是交替的，我们将

λ = ϕ(u,v) = ϕ(u,µu) = µϕ(u,u) = 0,
 λ=_（u，v）=（u，_u）=（u，u）=0，

contradicting the fact that λ = 06  . The rest is obvious.                                                                 
 与λ=06这一事实相矛盾。剩下的很明显。

Proposition 28.23 yields a plane spanned by two vectors u1,v1 such that ϕ(u1,u1) = ϕ(v1,v1) = 0 and ϕ(u1,v1) = 1. Such a plane is called a hyperbolic plane. If E is finitedimensional, we obtain the following theorem.
 命题28.23给出了一个由两个向量u1，v1所跨越的平面，使得（u1，u1）=（v1，v1）=0和（u1，v1）=1。这样的平面称为双曲面。如果e是有限维的，我们得到以下定理。

Theorem 28.24. Let ϕ: E × E → K be an alternating bilinear form on a space E of finite dimension n. Then, there is a direct sum decomposition of E into pairwise orthogonal subspaces
 定理28.24。设_：e×e→k为有限维n空间e上的交替双线性形式，然后将e直接和分解为成对正交子空间。

E = W1 ⊕ ··· ⊕ Wr ⊕ rad(E),
 e=w1···wr rad（e）

where each Wi is a hyperbolic plane and rad(E) = E⊥. Therefore, there is a basis of E of the form
 其中，每个wi是一个双曲面，rad（e）=e。因此，形式的e有一个基础

(u1,v1,...,ur,vr,w1,...,wn−2r),
 （u1，v1，…，ur，vr，w1，…，wn−2r）

with respect to which the matrix representing ϕ is a block diagonal matrix M of the form
 关于该矩阵，表示_的矩阵是形式的块对角矩阵m。

,
 ，

with
 具有

Proof. If ϕ = 0, then E = E⊥ and we are done. Otherwise, there are two nonzero vectors u,v ∈ E such that ϕ(u,v) = 06 , so by Proposition 28.23, we obtain a hyperbolic plane W2 spanned by two vectors u1,v1 such that ϕ(u1,v1) = 1. The subspace W1 is nondegenerate (for example, det(J) = −1), so by Proposition 28.21, we get a direct sum
 证据。如果直径=0，那么e=e我们就完成了。否则，有两个非零向量u，v∈e，因此，根据命题28.23，我们得到一个由两个向量u1，v1所跨越的双曲面w2，这样，a（u1，v1）=1。子空间w1是非退化的（例如，det（j）=-1），因此根据命题28.21，我们得到一个直接和

.
 .

By Proposition 28.14, we also have
 根据28.14号提案，我们也有

.
 .

By the induction hypothesis applied to , we obtain our theorem.                                                
 通过应用归纳假设，我们得到了我们的定理。

The following corollary follows immediately.
 下面的推论紧接着。

Proposition 28.25. Let ϕ: E × E → K be an alternating bilinear form on a space E of finite dimension n.
 提案28.25。设a:e×e→k为有限维n空间e上的交替双线性形式。

*(1)*     The rank of ϕ is even.
 _的等级是偶数。

*(2)*     If ϕ is nondegenerate, then dim(E) = n is even.
 如果直径不退化，则dim（e）=n为偶数。

*(3)*     Two alternating bilinear forms ϕ1 : E1 ×E1 → K and ϕ2 : E2 ×E2 → K are equivalent iff dim(E1) = dim(E2) and ϕ1 and ϕ2 have the same rank.
 两个交替双线性形式_:e1×e1→k和_:e2×e2→k是等效的iff dim（e1）=dim（e2）和_和_具有相同的等级。

The only part that requires a proof is part (3), which is left as an easy exercise.
 唯一需要证明的部分是第（3）部分，这是一个简单的练习。

If ϕ is nondegenerate, then n = 2r, and a basis of E as in Theorem 28.24 is called a symplectic basis. The space E is called a hyperbolic space (or symplectic space). Observe that if we reorder the vectors in the basis
 如果ω是非简并的，那么n=2r，定理28.24中e的基称为辛基。空间e称为双曲空间（或辛空间）。注意，如果我们重新排列基向量

(u1,v1,...,ur,vr,w1,...,wn−2r)
 （u1，v1，…，ur，vr，w1，…，wn-2r）

to obtain the basis
 获取基础

(u1,...,ur,v1,...vr,w1,...,wn−2r),
 （u1，…，ur，v1，…，vr，w1，…，wn−2r）

then the matrix representing ϕ becomes
 那么代表_的矩阵变成

 .
 .

This particularly simple matrix is often preferable, especially when dealing with the matrices (symplectic matrices) representing the isometries of ϕ (in which case n = 2r).
 这种特别简单的矩阵通常是可取的，尤其是在处理矩阵（辛矩阵）时，它代表了直径的等距（在这种情况下，n=2r）。

As a warm up for Proposition 28.29 of the next section, we prove an analog of Proposition
 作为下一节28.29号提案的热身，我们证明了一个类似的提案

28.23 in the case of a symmetric bilinear form.
 28.23对于对称双线性形式。

Proposition 28.26. Let ϕ: E×E → K be a nondegenerate symmetric bilinear form with K a field of characteristic different from 2. For any nonzero isotropic vector u, there is another nonzero isotropic vector v such that ϕ(u,v) = 2, and u and v are linearly independent. In the basis (u,v/2), the restriction of ϕ to the plane spanned by u and v/2 is of the form
 提案28.26。设_：e×e→k为非退化对称双线性形式，k为特征场，与2不同。对于任何非零各向同性向量u，还有另一个非零各向同性向量v，使得（u，v）=2，u和v是线性无关的。在基础（u，v/2）中，对u和v/2所跨越平面的直径限制为：

 .
 .

Proof. Since ϕ is nondegenerate, there is some nonzero vector z such that (rescaling z if necessary) ϕ(u,z) = 1. If v = 2z − ϕ(z,z)u,
 证据。由于_是非退化的，因此有一些非零矢量z（必要时重新缩放z）_（u，z）=1。如果v=2z（z，z）u，

then since ϕ(u,u) = 0 and ϕ(u,z) = 1, note that
 然后，由于_（u，u）=0和（u，z）=1，注意

ϕ(u,v) = ϕ(u,2z − ϕ(z,z)u) = 2ϕ(u,z) − ϕ(z,z)ϕ(u,u) = 2,
 ⑨（u，v）=⑨（u，2z（z，z）u）=2（u，z）−（z，z）（u，u）=2，

and
 和

ϕ(v,v) = ϕ(2z − ϕ(z,z)u,2z − ϕ(z,z)u) = 4ϕ(z,z) − 4ϕ(z,z)ϕ(u,z) + ϕ(z,z)2ϕ(u,u) = 4ϕ(z,z) − 4ϕ(z,z) = 0.
 ⑨（v，v）＝（2z（z，z）U，2z（z，z）U）=4（z，z）−4（z，z）（u，z）+（z，z）2（u，u）=4（z，z）−4（z，z）=0.

If u and z were linearly dependent, as u,z = 06 , we could write z = µu for some µ = 06 , but then, we would have ϕ(u,z) = ϕ(u,µu) = µϕ(u,u) = 0,
 如果u和z是线性相关的，当u，z=06时，我们可以为一些祆=06写z=祆u，但随后，我们将得到祆（u，z）=祆（u，祆u）=0，

contradicting the fact that ϕ(u,z) = 06 . Then u and v = 2z − ϕ(z,z)u are also linearly independent, since otherwise z could be expressed as a multiple of u. The rest is obvious. 
 与之相矛盾的是，_（u，z）=06。那么u和v=2z（z，z）u也是线性独立的，因为否则z可以表示为u的倍数。其余的很明显。

Proposition 28.26 yields a plane spanned by two vectors u1,v1 such that ϕ(u1,u1) = ϕ(v1,v1) = 0 and ϕ(u1,v1) = 1. Such a plane is called an Artinian plane. Proposition 28.26 also shows that nonzero isotropic vectors come in pair.
 命题28.26给出了一个由两个向量u1，v1所跨越的平面，从而使得_（u1，u1）=_（v1，v1）=0和_（u1，v1）=1。这样的一个平面称为Artian平面。命题28.26还表明非零各向同性向量是成对的。

Proposition 28.26 has the following corollary which has applications in number theory; see Serre [152], Chapter IV.
 命题28.26有以下推论，在数论中有应用；见Serre[152]，第四章。

Proposition 28.27. If Φ is any nondegenerate quadratic form (over a field of characteristic = 26 ) such that there is some nonzero vector x ∈ E with Φ(x) = 0, then for every α ∈ K, there is some y ∈ E such that Φ(y) = α.
 提案28.27。如果Φ是任何非退化二次型（在特征值为26的场上），那么有一些非零向量x∈e，其中Φ（x）=0，那么对于每个α∈k，有一些y∈e，这样Φ（y）=α。

Proof. Since by hypothesis there is some nonzero vector u ∈ E with Φ(u) = 0, by Proposition 28.26 there is another isotropic vector v such that u and v are linearly independent and such that (after rescaling) ϕ(u,v) = 1. Then for any α ∈ K, check that
 证据。由于假设存在一些非零向量u∈e，其中Φ（u）=0，根据命题28.26，存在另一个各向同性向量v，这样u和v是线性无关的，并且（重新缩放后）_（u，v）=1。那么对于任何α∈k，检查

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image038.gif)

as desired.                                                                                                                                          
 根据需要。

Remark: Some authors refer to the above plane as a hyperbolic plane. Berger (and others) point out that this terminology is undesirable because the notion of hyperbolic plane already exists in differential geometry and refers to a very different object.
 注：有些作者将上述平面称为双曲面。伯杰（和其他人）指出，这个术语是不可取的，因为双曲平面的概念已经存在于微分几何中，并且指的是一个非常不同的物体。

We leave it as an exercice to figure out that the group of isometries of the Artinian plane, the set of all 2 × 2 matrices A such that
 我们把它作为一个练习，来搞清楚亚第面的等轴测群，所有2×2矩阵的集合A，这样

 ,
 ，

consists of all matrices of the form
 由形式的所有矩阵组成

​                                                              or                            .
 或者。

In particular, if K = R, then this group denoted O(1,1) has four connected components.
 特别是，如果k=r，那么表示o（1，1）的这个组有四个相连的组件。

We now turn to the Witt decomposition.
 现在我们来谈谈维特分解。

## 28.7        Witt Decomposition  28.7维特分解

From now on, ϕ: E × E → K is an -Hermitian form. The following assumption will be needed:
 从现在开始，⑨：e×e→k是一个-赫敏形式。需要以下假设：

Property (T). For every u ∈ E, there is some α ∈ K such that.
 属性（t）。对于每一个u∈e，都有一些α∈k这样。

Property (T) is always satisfied if ϕ is alternating, or if K is of characteristic = 26 and 1, with 
 如果_为交替的，或如果k的特征值为26和1，则始终满足性能（t），且

The following (bizarre) technical lemma will be needed.
 需要以下（奇异的）技术引理。

Lemma 28.28. Let ϕ be an -Hermitian form on E and assume that ϕ satisfies property (T). For any totally isotropic subspace U = (0)6 of E, for every x ∈ E not orthogonal to U, and for every α ∈ K, there is some y ∈ U so that
 引理28.28。设a为e上的-厄米式形式，并假设a满足性质（t）。对于任意完全各向同性的子空间u=（0）6 of e，对于每一个不与u正交的x∈e，并且对于每一个α∈k，有一些y∈u，因此

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image040.gif)


 

Proof. By property (T), we have for some β ∈ K. For any y ∈ U, since ϕ is -Hermitian, ), and since U is totally isotropic ϕ(y,y) = 0, so we have
 证据。根据性质（t），我们有一些β∈k。对于任何y∈u，因为_是-厄米特式的，），并且因为u是完全各向同性的（y，y）=0，所以我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image042.gif)

Since x is not orthogonal to U, the function y 7→ ϕ(x,y) + β is not the constant function. Consequently, this function takes the value α for some y ∈ U, which proves the lemma. 
 由于x与u不正交，函数y 7→（x，y）+β不是常数函数。因此，这个函数取某个y∈u的α值，证明了引理。

Definition 28.18. Let ϕ be an -Hermitian form on E. A weak Witt decomposition of E is a triple (U,U0,W), such that (i) E = U ⊕ U0 ⊕ W (a direct sum).
 定义28.18.设_为e上的-厄米形式。e的弱维特分解是三重（u，u0，w），这样（i）e=u u0 w（直接和）。

(ii)      U and U0 are totally isotropic.
 u和u0是完全各向同性的。

(iii)    W is nondegenerate and orthogonal to U ⊕ U0.
 w是非简并与u_u0正交的。

We say that a weak Witt decomposition (U,U0,W) is nontrivial if U = (0)6 and U0 = (0).6 Furthermore, if E is finite-dimensional, then dim(U) = dim(U0) and in a suitable basis, the matrix representing ϕ is of the form
 我们说，弱维特分解（u，u0，w）是非平凡的，如果u=（0）6和u0=（0）。6此外，如果e是有限维的，那么dim（u）=dim（u0），在适当的基础上，表示_的矩阵是形式。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image044.gif)

We say that ϕ is a neutral form if it is nondegenerate, E is finite-dimensional, and if W = (0). In this case, the matrix B is missing.
 我们说，如果是非退化形式，那么_是中性形式，e是有限维，如果w=（0）。在这种情况下，矩阵B丢失。

A Witt decomposition for which W has no nonzero isotropic vectors (W is anisotropic) is called a Witt decomposition.
 对于w没有非零各向同性向量（w是各向异性的）的witt分解称为witt分解。

Observe that if Φ is nondegenerate, then we have the trivial weak Witt decomposition obtained by letting U = U0 = (0) and W = E. Thus a weak Witt decomposition is informative only if E is not anisotropic (there is some nonzero isotropic vector, i.e. some u = 06 such that Φ(u) = 0), in which case the most informative nontrivial weak Witt decompositions are those for which W is anisotropic and U and U0 are as big as possible.
 观察到，如果Φ是非退化的，那么我们得到了由u=u0=（0）和w=e得到的平凡的弱维特分解。因此，弱维特分解只有当e不是各向异性的（有一些非零的各向同性向量，即一些u=06，使得Φ（u）=0）时才是信息性的，在这种情况下最有用的非平凡弱维特分解是那些w是各向异性的，u和u0是尽可能大的。

Sometimes, we use the notation U1 ⊕⊥ U2 to indicate that in a direct sum U1 ⊕ U2, the subspaces U1 and U2 are orthogonal. Then, in Definition 28.18, we can write that E = (U ⊕ U0) ⊕⊥ W.
 有时，我们用符号u1 u2来表示在直接和u1 u2中，子空间u1和u2是正交的。然后，在定义28.18中，我们可以写出e=（u u0）w。

The first step in showing the existence of a Witt decomposition is this.
 证明维特分解存在的第一步就是这个。

Proposition 28.29. Let ϕ be an -Hermitian form on E, assume that ϕ is nondegenerate and satisfies property (T), and let U be any totally isotropic subspace of E of finite dimension dim(U) = r ≥ 1.
 提案28.29。设_为e上的-厄米形式，假设_是非退化的且满足性质（t），设u为有限维dim（u）=r≥1的e的任何完全各向同性子空间。

*(1)*     If U0 is any totally isotropic subspace of dimension r and if U0 ∩U⊥ = (0), then U ⊕U0 is nondegenerate, and for any basis (u1,...,ur) of U, there is a basis such that , for all i,j = 1,...,r.
 如果u0是维r的任何完全各向同性子空间，如果u0 u=（0），那么u u0是非退化的，对于u的任何基（u1，…，ur），都有这样一个基，对于所有i，j=1，…，r。

*(2)*     If W is any totally isotropic subspace of dimension at most r and if W ∩ U⊥ = (0), then there exists a totally isotropic subspace U0 with dim(U0) = r such that W ⊆ U0 and U0 ∩ U⊥ = (0).
 如果w至多是维的任何完全各向同性子空间r，如果w u=（0），则存在一个具有dim（u0）=r的完全各向同性子空间u0，使得w u0和u0 u=（0）。

Proof. (1) Let ϕ0 be the restriction of ϕ to U × U0. Since U0 ∩ U⊥ = (0), for any v ∈ U0, if ϕ(u,v) = 0 for all u ∈ U, then v = 0. Thus, ϕ0 is nondegenerate (we only have to check on the left since-Hermitian). Then, the assertion about bases follows from the version of Proposition 28.3 for sesquilinear forms. Since U is totally isotropic, U ⊆ U⊥, and since U0 ∩ U⊥ = (0), we must have U0 ∩ U = (0), which show that we have a direct sum U ⊕ U0. It remains to prove that U + U0 is nondegenerate. Observe that
 证据。（1）设瘳0为瘳对U×U0的限制。由于u0 u=（0），对于任何v u0，如果所有u u（u，v）=0，则v=0。因此，ω0是非退化的（我们只需检查左侧，因为赫米特）。然后，关于基的断言来自于28.3命题对于倍线性形式的版本。因为u是完全各向同性的，u u，并且由于u0 u=（0），我们必须有u0 u=（0），这表明我们有一个直接和u u0。它仍然需要证明U+U0是非简并的。注意

H = (U + U0) ∩ (U + U0)⊥ = (U + U0) ∩ U⊥ ∩ U0⊥.
 H=（U+U0）（U+U0）=（U+U0）U U0。

Since U is totally isotropic, U ⊆ U⊥, and since U0 ∩ U⊥ = (0), we have
 既然u是完全各向同性的，u u，既然u0 u=（0），我们有

(U + U0) ∩ U⊥ = (U ∩ U⊥) + (U0 ∩ U⊥) = U + (0) = U,
 （U+U0）U=（U U）＋（U0 U）=U+（0）=U，

thus H = U ∩ U0⊥. Since ϕ0 is nondegenerate, U ∩ U0⊥ = (0), so H = (0) and U + U0 is nondegenerate.
 因此，h=u u0。既然_是非退化的，u u0=（0），那么h=（0）和u+u0是非退化的。

(2) We proceed by descending induction on s = dim(W). The base case s = r is trivial. For the induction step, it suffices to prove that if s < r, then there is a totally isotropic subspace W 0 containing W such that dim(W 0) = s + 1 and W 0 ∩ U⊥ = (0).
 （2）我们在s=dim（w）上通过下降诱导进行。基本情况s=r是微不足道的。对于诱导步骤，它足以证明，如果s<r，那么有一个完全各向同性的子空间w 0包含w，从而dim（w 0）=s+1和w 0 u=（0）。

Since s = dim(W) < dim(U), the restriction of ϕ to U × W is degenerate. Since W ∩ U⊥ = (0), we must have U ∩ W ⊥ = (0)6 . We claim that
 由于s=dim（w）<dim（u），因此，对_至u×w的限制退化。既然w u=（0），我们必须有u w=（0）6。我们声称

W ⊥ 6⊆ W + U⊥.
 W 6 W+U。

If we had W ⊥ ⊆ W + U⊥,
 如果我们有W W+U，

then because U and W are finite-dimensional and ϕ is nondegenerate, by Proposition 28.13,
 那么，因为u和w是有限维的，并且，根据第28.13号命题，ω是非退化的，

U⊥⊥ = U and W ⊥⊥ = W, so by taking orthogonals, W ⊥ ⊆ W + U⊥ would yield
 u=u和w=w，所以通过取正字法，w w+u将产生

(W + U⊥)⊥ ⊆ W ⊥⊥,
 （W+U），

that is,
 也就是说，

W ⊥ ∩ U ⊆ W,
 W U W，

thus W ⊥ ∩ U ⊆ W ∩ U, and since U is totally isotropic, U ⊆ U⊥, which yields
 因此，w u w u，由于u是完全各向同性的，u u，它产生

W ⊥ ∩ U ⊆ W ∩ U ⊆ W ∩ U⊥ = (0),
 W U W U W=（0）、

contradicting the fact that U ∩ W ⊥ 6= (0).
 与U W 6=（0）这一事实相矛盾。

sinceany vectorTherefore, there is somez ∈ Uz⊥∈, thenW ⊥                                                     U     Uu⊥ ∈so thatW ⊥ such thatu+z ∈ Wu /⊥∈andW +uU+⊥Wz /. Since⊥∈∩WU+U= (0)6 U⊆⊥ U(if⊥is totally isotropic, we can add tou+z ∈ W +U⊥u,
 因此，在任何向量机中，都有一些z∈uz uz u u uu uw uu uu uu uw uu wz/。既然w u+u=（0）6u u（如果是完全各向同性的，我们可以加上tou+z w+u u，

∩u ∈ ⊆W + U⊥, a contradiction). Since
 u∈w+u，一个矛盾）。自从

Wandthat0 =u /ϕW(∈uW++z,uKx+ U+⊥is a totally isotropic subspace of dimensionz= () = 0W ⊥. See Figure 28.1. If we write∩ U)⊥, we can invoke Lemma 28.28 to find ax =su+ 1+ z. Furthermore, we claim, thenzx /∈∈WW⊥ ∩+UU⊥such, so
 wndthat0=u/_w（∈uw++z，ukx+u+）是一个完全各向同性的维数z=（）=0w子空间。见图28.1。如果我们写u），我们可以调用lemma 28.28来找到ax=su+1+z，而且我们声称，那么zx/∈ww+uu这样，所以

that W 0 ∩ U⊥ = 0.
 即w 0 u=0。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image045.gif)

E
 e

Figure 28.1: A schematic illustration of W and x = u + z
 图28.1:w和x=u+z的示意图

Otherwise, we would have y = w + λx ∈ U⊥, for some w ∈ W and some λ ∈ K, and then we would have λx = −w + y ∈yW∈ +U⊥Uand⊥. Ifwλ∈= 06 W, then, we havex ∈ yW∈+WU∩⊥, a contradiction.U⊥ = (0), which
 否则，我们会得到y=w+λx∈u，对于一些w∈w和一些λ∈k，然后我们会得到λx=−w+y∈yw∈+u u and。如果wλ∈=06w，那么我们有x∈yw∈+w u，一个矛盾，u=（0），其中

Therefore, λ = 0, y = w, and since means that y = 0. Therefore, W 0 is the required subspace and this completes the proof. 
 因此，λ=0，y=w，因为y=0。因此，w 0是所需的子空间，这就完成了证明。

Here are some consequences of Proposition 28.29. If we set W = (0) in Proposition 28.29(2), then we get the following theorem showing that if E is not anisotropic (there is some nonzero isotropic vector) then weak nontrivial Witt decompositions exist.
 这是28.29号提案的一些结果。如果我们在28.29（2）中设置w=（0），那么我们得到如下定理：如果e不是各向异性的（有一些非零各向同性向量），那么存在弱非平凡的witt分解。

Theorem 28.30. Let ϕ be an -Hermitian form on E which is nondegenerate and satisfies
 定理28.30。设_为e上非简并满足的-厄米形式。

nondegenerate. As a consequence, ifproperty (T). For any totally isotropic subspaceexists a totally isotropic subspace U0 Eof dimensionis not anisotropic, thenUrofsuch thatE of finite dimensionU ∩ U0 = (0) andr ≥U1⊕, thereU0 is  is a weak nontrivial Witt decomposition for E. Furthermore, by Proposition 28.29(1), the block A in the matrix of ϕ is the identity matrix.
 不退化。因此，ifproperty（t）。对于任何完全各向同性的子空间存在一个完全各向同性的子空间，u0 e of维数不是各向异性的，因此，如果有限维数u u0=（0）andr≥u1的e是一个弱的非平凡的witt分解，而且，根据命题28.29（1），矩阵中的a块⑨为单位矩阵。

Proposition 28.31. Any two -Hermitian neutral forms satisfying property (T) defined on spaces of the same dimension are equivalent.
 提案28.31。在同一维空间上定义的满足性质（t）的任何两个埃尔米特中性形式都是等价的。

The following proposition shows that every subspace U of E can be embedded into a nondegenerate subspace. It is needed to prove a version of the Witt extension theorem (Theorem 28.48).
 下面的命题表明，e的每个子空间u都可以嵌入到一个非退化子空间中。需要证明维特推广定理（定理28.48）的一个版本。

Proposition 28.32. Let ϕ be an -Hermitian form on E which is nondegenerate and satisfies property (T). For any subspace U of E of finite dimension, if we write
 提案28.32。设a为e上的一个-厄米形式，它是非退化的且满足属性（t）。对于有限维E的任何子空间u，如果我们写

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image047.gif)

for some orthogonal complement W of V = rad(U), and if we let r = dim(rad(U)), then there exists a totally isotropic subspace V 0 of dimension r such that V ∩ V 0 = (0), and
 对于一些v=rad（u）的正交补码w，如果我们让r=dim（rad（u）），那么存在一个完全各向同性的子空间v 0，即v v 0=（0），并且

 is nondegenerate.                                                       Furthermore, any isometry f from U into
 是不退化的。而且，从u到

another space (E0,ϕ0) where ϕ0 is an -Hermitian form satisfying the same assumptions as ϕ can be extended to an isometry on (V ⊕ V 0) ⊕⊥ W.
 另一个空间（e0，_），其中，_是符合与_相同假设的-厄米式形式，可延伸至（v v 0）w上的等距测量。

Proof. Since W is nondegenerate, W ⊥ is also nondegenerate, and V ⊆ W ⊥. Therefore, we can apply Theorem 28.30 to the restriction of ϕ to W ⊥ and to V to obtain the required V 0. We know that V ⊕ V 0 is nondegenerate and orthogonal to W, which is also nondegenerate, so (V ⊕ V 0) ⊕⊥ W = V 0 ⊕ U is nondegenerate.
 证据。由于w是非退化的，w也是非退化的，v w。因此，我们可以将定理28.30应用到_到w和v的限制，以获得所需的v 0。我们知道v v 0是非简并的，与w正交，w也是非简并的，所以（v v 0）w=v 0 u是非简并的。

We leave the second statement about extending f as an exercise (use the fact that f(U) =
 我们留下第二个关于扩展f的陈述作为练习（使用f（u）这个事实=

), where V1 = f(V ) is totally isotropic of dimension r, to find another totally isotropic susbpace  of dimension r such that     = (0) and is orthogonal to f(W)).  
 ，式中，v1=f（v）是尺寸r的完全各向同性，求出另一个尺寸r的完全各向同性的近似值，使之等于（0），并与f（w）正交。

The subspace (V ⊕ V 0) ⊕⊥ W = V 0 ⊕ U is often called a nondegenerate completion of U. The subspace V ⊕ V 0 is called an Artinian space. Proposition 28.29 show that V ⊕ V 0 has a basis (u1,v1,...,ur,vr) consisting of vectors ui ∈ V and vj ∈ V 0 such that ϕ(ui,uj) = δij. The subspace spanned by (ui,vi) is an Artinian plane, so V ⊕ V 0 is the orthogonal direct sum of r Artinian planes. Such a space is often denoted by Ar2r.
 子空间（v v 0）w=v 0 u通常被称为u的非退化完成。子空间v v 0被称为Artian空间。命题28.29表明，v v 0有一个基（u1，v1，…，ur，vr），由向量ui∈v和vj∈v 0组成，从而使得（ui，uj）=δij。（ui，vi）所跨越的子空间是一个Artian平面，因此v v 0是r Artian平面的正交直接和。这种空间通常用ar2r表示。

In order to obtain the stronger version of the Witt decomposition when ϕ has some nonzero isotropic vector and W is anisotropic we now sharpen Proposition 28.29
 为了获得更强大的维特分解形式，当_有一些非零各向同性向量且w是各向异性时，我们现在尖锐化了命题28.29。

Theorem 28.33. Let ϕ be an -Hermitian form on E which is nondegenerate and satisfies property (T). Let U1 and U2 be two totally isotropic maximal subspaces of E, with U1 or U2 of finite dimension ≥ 1. Write U = U1 ∩ U2, let S1 be a supplement of U in U1 and S2 be a supplement of U in U2 (so that U1 = U ⊕ S1, U2 = U ⊕ S2), and let S = S1 + S2. Then, there exist two subspaces W and D of E such that:
 定理28.33。设a为e上的一个-厄米形式，它是非退化的且满足属性（t）。设u1和u2为e的两个完全各向同性最大子空间，其中有限维的u1或u2≥1。写u=u1 u2，设s1为u1中u的补充，s2为u2中u的补充（使u1=u s1，u2=u s2），设s=s1+s2。然后，存在两个子空间w和d of e，这样：

*(a)*    The subspaces S, U + W, and D are nondegenerate and pairwise orthogonal.
 子空间s、u+w和d是非退化的，并且是成对正交的。

*(b)*    We have a direct sum.
 我们有一个直接的和。

*(c)*     The subspace D contains no nonzero isotropic vector (D is anisotropic).
 子空间d不包含非零各向同性向量（d是各向异性的）。

*(d)*    The subspace W is totally isotropic.
 子空间w是完全各向同性的。

Furthermore, U1 and U2 are both finite dimensional, and we have dim(U1) = dim(U2), dim(W) = dim(U), dim(S1) = dim(S2), and codim(D) = 2dim(F1).
 此外，u1和u2都是有限维的，我们有dim（u1）=dim（u2），dim（w）=dim（u），dim（s1）=dim（s2），codim（d）=2dim（f1）。

Proof. First observe that if X is a totally isotropic maximal subspace of E, then any isotropic vector x ∈ E orthogonal to X must belong to X, since otherwise, X + Kx would be a totally isotropic subspace strictly containing X, contradicting the maximality of X. As a consequence, if xi is any isotropic vector such that xi ∈ Ui⊥ (for i = 1,2), then xi ∈ Ui.
 证据。首先观察到，如果X是E的全迷向最大子空间，那么任何与X正交的各向同性向量X E必须属于X，否则，X+KX将是严格包含X的完全各向同性子空间，与X的最大性相矛盾，因此，如果XI是各向同性的，向量，如Xi uIi（i＝1，2），然后是Xi uUI。

We claim that
 我们声称

​                                                      = (0)            and                .
 =（0）和。

Assume that y ∈ S1 is orthogonal to S2. Since U1 = U ⊕ S1 and U1 is totally isotropic, y is orthogonal to U1, and thus orthogonal to U, so that y is orthogonal to U2 = U ⊕ S2. Since S1 ⊆ U1 and U1 is totally isotropic, y is an isotropic vector orthogonal to U2, which by a previous remark implies that y ∈ U2. Then, since S1 ⊆ U1 and U ⊕ S1 is a direct sum, we have
 假设y∈s1与s2正交。由于u1=u_s1和u1完全各向同性，y与u1正交，因此与u正交，因此y与u2=u_s2正交。由于s1 u1和u1是完全各向同性的，y是一个正交于u2的各向同性向量，前面的一句话暗示y∈u2。那么，既然s1 u1和u s1是一个直接和，我们有

y ∈ S1 ∩ U2 = S1 ∩ U1 ∩ U2 = S1 ∩ U = (0).
 y∈s1 u2=s1 u1 u2=s1 u=（0）。

Therefore                                                  = (0). A similar proof show that is finite-dimensional
 因此=（0）。一个类似的证明表明这是有限维的

(the case where U2 is finite-dimensional is similar), then S1 is finite-dimensional, so by Proposition 28.13,has finite codimension. Since = (0), and since any supplement of  has finite dimension, we must have
 （u2是有限维的情况相似），那么s1是有限维，因此根据命题28.13，具有有限的余维。既然=（0），而且由于的任何补充都有有限维，我们必须

dim(S2) ≤ codim(.
 尺寸（s2）≤codim（.

By a similar argument, dim(S1) ≤ dim(S2), so we have
 通过一个类似的论点，dim（s1）≤dim（s2），所以我们有

dim(S1) = dim(S2).
 dim（s1）=dim（s2）。

By Proposition 28.29(1), we conclude that S = S1 + S2 is nondegenerate.
 通过28.29（1）号提案，我们得出S=s1+s2是非退化的。

By Proposition 28.21, the subspace N = S⊥ = (S1 + S2)⊥ is nondegenerate. Since U1 = U ⊕ S1, U2 = U ⊕ S2, and U1,U2 are totally isotropic, U is orthogonal to S1 and to S2, so U ⊆ N. Since U is totally isotropic, by Proposition 28.30 applied to N, there is a totally isotropic subspace W of N such that dim(W) = dim(U), U ∩ W = (0), and U + W is nondegenerate. Consequently, (d) is satisfied by W.
 根据命题28.21，子空间n=s=（s1+s2）是非退化的。由于u1=u_s1，u2=u_s2，和u1，u2是完全各向同性的，u与s1和s2正交，所以u_n。由于u是完全各向同性的，根据适用于n的28.30号命题，有一个完全各向同性的子空间w为n，因此dim（w）=dim（u），u_w=（0），u+w是非退化的。因此，（d）被w满足。

To satisfy (a) and (b), we pick D to be the orthogonal of U ⊕ W in N. Then, N =
 为了满足（a）和（b），我们选取d作为u_w在n中的正交，然后，n=

.
 .

As to (c), since D is orthogonal U ⊕ W, D is orthogonal to U, and since D ⊆ N and N is orthogonal to S1 +S2, D is orthogonal to S1, so D is orthogonal to U1 = U ⊕S1. If y ∈ D is any isotropic vector, since , by a previous remark, y ∈ U1, so y ∈ D ∩ U1. But, D ⊆ N with N ∩ (S1 + S2) = (0), and D ∩ (U + W) = (0), so D ∩ (U + S1) = D ∩ U1 = (0), which yields y = 0. The statements about dimensions are easily obtained. 
 至于（c），因为d是正交的u_w，d是正交的u，而且d_n和n是正交的s1+s2，d是正交的s1，所以d是正交的u1=u_s1。如果y∈d是任何各向同性向量，因为，根据前面的注释，y∈u1，所以y∈d u1。但是，d n，其中n（s1+s2）=（0），d（u+w）=（0），因此d（u+s1）=d u1=（0），得出y=0。关于尺寸的说明很容易获得。

Finally, Theorem 28.33 yields the strong form of the Witt decomposition in which W is anistropic. Given any matrix A ∈ Mn(K), we say that A is definite if x>Ax = 06 for all x ∈ Kn.
 最后，定理28.33给出了witt分解的强形式，其中w是各向异性的。对于任意矩阵a∈mn（k），我们认为a是确定的，如果x>ax=06对于所有x∈kn。

Theorem 28.34. Let ϕ be an -Hermitian form on E which is nondegenerate and satisfies property (T).
 定理28.34。设a为e上的一个-厄米形式，它是非退化的且满足属性（t）。

*(1)*     Any two totally isotropic maximal spaces of finite dimension have the same dimension.
 任意两个完全各向同性的有限维极大空间都有相同的维数。

*(2)*     For any totally isotropic maximal subspace U of finite dimension r ≥ 1, there is another totally isotropic maximal subspace U0 of dimension r such that U ∩ U0 = (0), and U ⊕ U0 is nondegenerate. Furthermore, if D = (U ⊕ U0)⊥, then (U,U0,D) is a
 对于有限维r≥1的完全各向同性最大子空间u，存在另一个完全各向同性最大子空间u0，使得u u0=（0），u u0是非退化的。此外，如果d=（u u0），（u，u0，d）是a

Witt decomposition of E; that is, there are no nonzero isotropic vectors in D (D is anisotropic).
 e的维特分解；也就是说，d中没有非零各向同性向量（d是各向异性的）。

*(3)*     If E has finite dimension n ≥ 1 and there is some nonzero isotropic vector for ϕ (E is not anisotropic), then E has a nontrivial Witt decomposition (U,U0,D) as in (2). There is a basis of E such that
 如果e的有限维数n≥1，且有一些非零各向同性向量用于_（e不是各向异性的），则e具有非平凡的witt分解（u，u0，d），如（2）中所示。有这样一个基础

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

*(a)*     if ϕ is alternating ( − and λ = λ for all λ ∈ K), then n = 2m and ϕ is represented by a matrix of the form
 如果ω是交替的（−和λ=λ代表所有的λ∈k），则n=2 m和ω由形式的矩阵表示。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image049.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

*(b)*     if ϕ is symmetric ( and λ = λ for all λ ∈ K), then ϕ is represented by a matrix of the form
 如果ω是对称的（且所有λ∈k的λ=λ），则用形式的矩阵表示。

 ,
 ，

where either n = 2r and P does not occur, or n > 2r and P is a definite symmetric matrix.
 其中n=2r和p没有出现，或者n>2r和p是一个确定的对称矩阵。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

-Hermitian (the involutive automorphism λ 7→ λ is not the identity), then ϕ is represented by a matrix of the form
 -厄米提安（对合自同构λ7→λ不是恒等式），则用形式的矩阵表示。

 ,
 ，

where either n = 2r and P does not occur, or n > 2r and P is a definite matrix such that .
 其中n=2r和p没有出现，或者n>2r和p是一个确定的矩阵，这样。

Proof. Part (1) follows from Theorem 28.33. By Proposition 28.30, we obtain a totally isotropic subspace U0 of dimension r such that U ∩ U0 = (0). By applying Theorem 28.33 to U1 = U and U2 = U0, we get U = W = (0), which proves (2). Part (3) is an immediate consequence of (2).     
 证据。第（1）部分来自定理28.33。通过命题28.30，我们得到了维R的完全各向同性子空间u0，这样u u0=（0）。将定理28.33应用于u1=u和u2=u0，得到u=w=（0），证明（2）。第（3）部分是第（2）部分的直接后果。

As a consequence of Theorem 28.34, we make the following definition.
 根据定理28.34，我们做出如下定义。

Definition 28.19. Let E be a vector space of finite dimension n, and let ϕ be an -Hermitian form on E which is nondegenerate and satisfies property (T). The index (or Witt index) ν of ϕ, is the common dimension of all totally isotropic maximal subspaces of E. We have 2ν ≤ n.
 定义28.19.设e为有限维数n的向量空间，且当e为非退化且满足性质（t）的-Hermitian形式时，则当e为非退化且满足性质（t）的-Hermitian形式。ω的指数（或维特指数）为e的所有全向各向同性最大子空间的公共维数。我们有2ν≤n。

Neutral forms only exist if n is even, in which case, ν = n/2. Forms of index ν = 0 have no nonzero isotropic vectors. When K = R, this is satisfied by positive definite or negative definite symmetric forms. When K = C, this is satisfied by positive definite or negative definite Hermitian forms. The vector space of a neutral Hermitian form ( = +1) is an Artinian space, and the vector space of a neutral alternating form is a hyperbolic space.
 中性形式只有当n为偶数时才存在，在这种情况下，ν=n/2。指数的形式v=0没有非零的各向同性向量。当k=r时，用正定或负定对称形式表示。当k=c时，这可由正定或负定厄米式来满足。中性厄米形式（+1）的矢量空间是一个Artian空间，中性交替形式的矢量空间是一个双曲空间。

If the field K is algebraically closed, we can describe all nondegenerate quadratic forms.
 如果K域是代数闭的，我们可以描述所有的非退化二次型。

Proposition 28.35. If K is algebraically closed and E has dimension n, then for every nondegenerate quadratic form Φ, there is a basis (e1,...,en) such that Φ is given by
 提案28.35。如果k是代数闭的，e有维数n，那么对于每一个非退化二次型Φ，都有一个基（e1，…，en），使得Φ由

if n = 2m      if n = 2m + 1.
 如果n=2米，如果n=2米+1。

Proof. We work with the polar form ϕ of Φ. Let U1 and U2 be some totally isotropic subspaces such that U1 ∩ U2 = (0) given by Theorem 28.34, and let q be their common dimension. Then, W = U = (0). Since we can pick bases (e1,...eq) in U1 and (eq+1,...,e2q) in U2 such that ϕ(ei,ei+q) = 0, for i,j = 1,...,q, it suffices to proves that dim(D) ≤ 1. If x,y ∈ D with x = 06 , from the identity
 证据。我们使用的极性形式是Φ。设u1和u2为一些完全各向同性的子空间，如定理28.34给出的u1 u2=（0），并设q为它们的公共维数。那么，w=u=（0）。由于我们可以选取U1中的碱基（e1，…eq）和U2中的碱基（eq+1，…，e2q），因此，对于i，j=1，…，q，它足以证明dim（d）≤1。如果x，y∈d，x=06，从恒等式

Φ(y − λx) = Φ(y) − λϕ(x,y) + λ2Φ(x)
 Φ（y−λx）=Φ（y）−λ（x，y）+λ2Φ（x）

and the fact that Φ(x) = 06    since x ∈ D and x = 06     , we see that the equation Φ(y − λy) = 0 has at least one solution. Since Φ(z) = 06     for every nonzero z ∈ D, we get y = λx, and thus dim(D) ≤ 1, as claimed.       
 从x∈d和x=06开始，Φ（x）=06，我们发现方程Φ（y-λy）=0至少有一个解。由于Φ（z）=06，对于每一个非零z∈d，我们得到y=λx，因此dim（d）≤1，如权利要求所述。

Proposition 28.35 shows that for every nondegenerate quadratic form Φ over an algebraically closed field, if dim(E) = 2m or dim(E) = 2m + 1 with m ≥ 1, then Φ has some nonzero isotropic vector.
 命题28.35表明，对于代数闭场上的每一个非退化二次型Φ，如果dim（e）=2 m或dim（e）=2 m+1且m≥1，则Φ具有一些非零各向同性向量。

## 28.8        Symplectic Groups  28.8辛群

In this section, we are dealing with a nondegenerate alternating form ϕ on a vector space E of dimension n. As we saw earlier, n must be even, say n = 2m. By Theorem 28.24, there is a direct sum decomposition of E into pairwise orthogonal subspaces
 在这一节中，我们要处理的是一个非退化的交替形式，在维n的向量空间e上。正如我们前面所看到的，n必须是偶数，即n=2米。根据定理28.24，e的直接和分解成成对的正交子空间。

​                                                            E = W1 ⊕ ···⊥ ⊕⊥ Wm,
 E=w1····wm，

where each Wi is a hyperbolic plane. Each Wi has a basis (ui,vi), with ϕ(ui,ui) = ϕ(vi,vi) = 0 and ϕ(ui,vi) = 1, for i = 1,...,m. In the basis
 其中每个wi都是一个双曲线平面。每个wi都有一个基（ui，vi），其中，当i=1，…，m时，其中，qian（ui，ui）=0和qian（ui，vi）=1。

(u1,...,um,v1,...,vm),
 （u1，…，um，v1，…，vm）

ϕ is represented by the matrix
 用矩阵表示

 .
 .

The symplectic group Sp(2m,K) is the group of isometries of ϕ. The maps in Sp(2m,K) are called symplectic maps. With respect to the above basis, Sp(2m,K) is the group of 2m × 2m matrices A such that
 辛群sp（2m，k）为_等轴测群。SP（2M，K）中的映射称为辛映射。就上述基础而言，sp（2m，k）是由2m×2m矩阵a组成的组，因此

A>Jm,mA = Jm,m.
 a>jm，ma=jm，m。

Matrices satisfying the above identity are called symplectic matrices. In this section, we show that Sp(2m,K) is a subgroup of SL(2m,K) (that is, det(A) = +1 for all A ∈ Sp(2m,K)), and we show that Sp(2m,K) is generated by special linear maps called symplectic transvections.
 满足上述恒等式的矩阵称为辛矩阵。在本节中，我们证明了sp（2 m，k）是sl（2 m，k）的一个子群（即，所有a∈sp（2 m，k）的det（a）=+1），并且我们证明sp（2 m，k）是由称为辛变换的特殊线性映射生成的。

First, we leave it as an easy exercise to show that Sp(2,K) = SL(2,K). The reader should also prove that Sp(2m,K) has a subgroup isomorphic to GL(m,K).
 首先，我们将它作为一个简单的练习来展示sp（2，k）=sl（2，k）。读者还应证明sp（2m，k）与gl（m，k）具有同构子群。

Next we characterize the symplectic maps f that leave fixed every vector in some given hyperplane H, that is,
 接下来，我们描述辛映射f，在给定的超平面h中保持不变的每个向量，也就是说，

​                                                           f(v) = v      for all v ∈ H.
 f（v）=v，表示所有v∈h。

Since ϕ is nondegenerate, by Proposition 28.22, the orthogonal H⊥ of H is a line (that is, dim(H⊥) = 1). For every u ∈ E and every v ∈ H, since f is an isometry and f(v) = v for all v ∈ H, we have
 因为根据命题28.22，_是非退化的，所以h的正交h是一条线（即，dim（h）=1）。对于每一个u∈e和每一个v∈h，因为f是一个等值线，而f（v）=v对于所有v∈h，我们有

ϕ(f(u) − u,v) = ϕ(f(u),v) − ϕ(u,v)
 Ⅷ（f（u）−u，v）=Ⅷ（f（u），v）−Ⅷ（u，v）

= ϕ(f(u),v) − ϕ(f(u),f(v))
 =_（f（u），v）-_（f（u），f（v））

= ϕ(f(u),v − f(v))) = ϕ(f(u),0) = 0,
 =_（f（u），v−f（v）））=（f（u），0）=0，

which shows that f(u) − u ∈ H⊥ for all u ∈ E. Therefore, f − id is a linear map from E into the line H⊥ whose kernel contains H, which means that there is some nonzero vector w ∈ H⊥ and some linear form ψ such that
 这表明f（u）−u∈h对于所有u∈e，因此f−id是从e到h线的线性映射，h线的内核包含h，这意味着存在一些非零向量w∈h和一些线性形式ψ，因此

​                                                        f(u) = u + ψ(u)w,       u ∈ E.
 f（u）=u+ψ（u）w，u∈e。


 

28.8. SYMPLECTIC GROUPS
 28.8。辛群

Since f is an isometry, we must have ϕ(f(u),f(v)) = ϕ(u,v) for all u,v ∈ E, which means that
 因为f是一个等距测量，所以我们必须对所有u，v∈e都取_（f（u），f（v））=_（u，v），这意味着

ϕ(u,v) = ϕ(f(u),f(v))
 ⑨（u，v）=⑨（f（u），f（v））

= ϕ(u + ψ(u)w,v + ψ(v)w)
 =ψ（u+ψ（u）w，v+ψ（v）w）

= ϕ(u,v) + ψ(u)ϕ(w,v) + ψ(v)ϕ(u,w) + ψ(u)ψ(v)ϕ(w,w)
 =_（u，v）+_（u）_（w，v）+_（v）_（u，w）+_（u）_（v）_（w，w）

= ϕ(u,v) + ψ(u)ϕ(w,v) − ψ(v)ϕ(w,u),
 =_（u，v）+ψ（u）_（w，v）−ψ（v）（w，u）、

which yields ψ(u)ϕ(w,v) = ψ(v)ϕ(w,u)    for all u,v ∈ E.
 其中，所有u，v∈e产生ψ（u）_（w，v）=ψ（v）（w，u）。

Since ϕ is nondegenerate, we can pick some v0 such that ϕ(w,v0) = 06      , and we get ψ(u)ϕ(w,v0) = ψ(v0)ϕ(w,u) for all u ∈ E; that is,
 既然_是非退化的，我们可以选择一些v0，这样，_（w，v0）=06，我们得到所有u∈e的ψ（u）_（w，v0）=ψ（v0）（w，u）；也就是说，

​                                                    ψ(u) = λϕ(w,u)      for all u ∈ E,
 ψ（u）＝_（w，u）表示所有u∈e，

for some λ ∈ K. Therefore, f is of the form
 对于某些λ∈k，因此，f是形式

​                                                f(u) = u + λϕ(w,u)w,        for all u ∈ E.
 f（u）=u+λ（w，u）w，表示所有u∈e。

It is also clear that every f of the above form is a symplectic map. If λ = 0, then f = id. Otherwise, if λ = 06 , then f(u) = u iff ϕ(w,u) = 0 iff u ∈ (Kw)⊥ = H, where H is a hyperplane. Thus, f fixes every vector in the hyperplane H. Note that since ϕ is alternating, ϕ(w,w) = 0, which means that w ∈ H.
 很明显，上述形式的每一个f都是一个辛映射。如果λ=0，则f=id。否则，如果λ=06，则f（u）=u iff（w，u）=0 iff u∈（kw）=h，其中h是超平面。因此，f固定了超平面h中的每一个向量。注意，由于_是交替的，因此_（w，w）=0，这意味着w∈h。

In summary, we have characterized all the symplectic maps that leave every vector in some hyperplane fixed, and we make the following definition.
 总之，我们已经描述了所有使某个超平面中的每个向量保持不变的辛映射，并且我们做出了以下定义。

Definition 28.20. Given a nondegenerate alternating form ϕ on a space E, a symplectic transvection (of direction w) is a linear map f of the form
 定义28.20。给定空间E上的非简并交替形式，辛矢量（方向W）是形式的线性映射f。

​                                                f(u) = u + λϕ(w,u)w,        for all u ∈ E,
 f（u）=u+λ（w，u）w，对于所有u∈e，

for some nonzero w ∈ E and some λ ∈ K. If λ = 06 , the subspace of vectors left fixed by f is the hyperplane H = (Kw)⊥. The map f is also denoted τw,λ.
 对于一些非零w∈e和一些λ∈k，如果λ=06，由f固定的向量的子空间是超平面h=（kw）。图f也表示为τw，λ。

Observe that
 注意

τw,λ ◦ τw,µ = τw,λ+µ
 τw，λτw，μ=τw，λ+μ

and τw,λ = id iff λ = 0. The above shows that det(τw,λ) = 1, since when λ = 06 , we have τw,λ = (τw,λ/2)2.
 τw，λ=id iffλ=0。上述结果表明，Det（τw，λ）=1，因为当λ=06时，我们得到τw，λ=（τw，λ/2）2。

Our next goal is to show that if u and v are any two nonzero vectors in E, then there is a simple symplectic map f such that f(u) = v.
 我们的下一个目标是证明，如果u和v是e中的任意两个非零向量，那么有一个简单的辛映射f，这样f（u）=v。

Proposition 28.36. Given any two nonzero vectors u,v ∈ E, there is a symplectic map f such that f(u) = v, and f is either a symplectic transvection, or the composition of two symplectic transvections.
 提案28.36。对于任意两个非零矢量u，v∈e，存在一个辛映射f，使得f（u）=v，f是一个辛变换，或者是两个辛变换的组合。

Proof. There are two cases.
 证据。有两种情况。

Case 1. ϕ(u,v) = 0.6
 案例1。⑨（u，v）=0.6

In this case, u =6 v, since ϕ(u,u) = 0. Let us look for a symplectic transvection of the form τv−u,λ. We want
 在这种情况下，U=6 V，因为_（U，U）=0。让我们来寻找形式τv−u，λ的辛变换。我们想要

v = u + λϕ(v − u,u)(v − u) = u + λϕ(v,u)(v − u),
 V=U+λ_（V−U，U）（V−U）=U+λ（V，U）（V−U）、

which yields
 会产生

(λϕ(v,u) − 1)(v − u) = 0.
 （λη（v，u）−1）（v−u）=0.

Since ϕ(u,v) = 06 and ϕ(v,u) = −ϕ(u,v), we can pick λ = ϕ(v,u)−1 and τv−u,λ maps u to v. Case 2. ϕ(u,v) = 0.
 既然_（u，v）=06和（v，u）=-（u，v），我们可以选择λ=_（v，u）−1和τv−u，λ将u映射到v。情况2。⑨（u，v）=0.

If u = v, use τu,0 = id. Now, assume u =6 v. We claim that it is possible to pick some w ∈ E such that ϕ(u,w) = 06 and ϕ(v,w) = 06 . Indeed, if (Ku)⊥ = (Kv)⊥, then pick any nonzero vector w not in the hyperplane (Ku)⊥. Othwerwise, (Ku)⊥ and (Kv)⊥ are two distinct hyperplanes, so neither is contained in the other (they have the same dimension), so pick any nonzero vector w1 such that w1 ∈ (Ku)⊥ and w1 ∈/ (Kv)⊥, and pick any nonzero vector w2 such that w2 ∈ (Kv)⊥ and w2 ∈/ (Ku)⊥. If we let w = w1 + w2, then ϕ(u,w) = ϕ(u,w2) = 06 , and ϕ(v,w) = ϕ(v,w1) = 06 . From case 1, we have some symplectic transvection τw−u,λ1 such that τw−u,λ1(u) = w, and some symplectic transvection τv−w,λ2 such that τv−w,λ2(w) = v, so the composition τv−w,λ2 ◦ τw−u,λ1 maps u to v. 
 如果u=v，则使用τu，0=id。现在，假设u=6v。我们声称可以选择一些w∈e，这样，（u，w）=06和（v，w）=06。实际上，如果（ku）=（kv），那么选取不在超平面（ku）中的任何非零矢量w。另外，（ku）和（kv）是两个不同的超平面，因此两者都不包含在另一个超平面中（它们具有相同的维数），因此选取任意非零矢量w1，使w1∈（ku）和w1∈/（kv），并选取任意非零矢量w2，使w2∈（kv）和w2∈/（ku）。如果我们让w=w1+w2，那么_（u，w）=（u，w2）=06，和（v，w）=（v，w1）=06。从情况1来看，我们有一些辛矢量τw−u，λ1，这样τw−u，λ1（u）=w，和一些辛矢量τv−w，λ2，这样τv−w，λ2（w）=v，所以组成τv−w，λ2τw−u，λ1将u映射到v。

Next, we would like to extend Proposition 28.36 to two hyperbolic planes W1 and W2.
 接下来，我们将28.36号命题扩展到两个双曲面w1和w2。

Proposition 28.37. Given any two hyperbolic planes W1 and W2 given by bases (u1,v1) and (u2,v2) (with ϕ(ui,ui) = ϕ(vi,vi) = 0 and ϕ(ui,vi) = 1, for i = 1,2), there is a symplectic map f such that f(u1) = u2, f(v1) = v2, and f is the composition of at most four symplectic transvections.
 提案28.37。给定任意两个由基（u1，v1）和（u2，v2）给出的双曲线平面w1和w2（其中，_（ui，ui）=（vi，vi）=0和（ui，vi）=1，对于i=1,2，有一个辛映射f，这样f（u1）=u2，f（v1）=v2，并且f至多是四个辛变换的组合。

Proof. From Proposition 28.36, we can map u1 to u2, using a map f which is the composition of at most two symplectic transvections. Say v3 = f(v1). We claim that there is a map g such that g(u2) = u2 and g(v3) = v2, and g is the composition of at most two symplectic transvections. If so, g ◦ f maps the pair (u1,v1) to the pair (u2,v2), and g ◦ f consists of at most four symplectic transvections. Thus, we need to prove the following claim:
 证据。从28.36号提案，我们可以用最多由两个辛变换组成的映射f来映射u1到u2。假设v3=f（v1）。我们认为存在一个图G，这样G（u2）=u2和G（v3）=v2，并且G是最多两个辛矢量的组合。如果是这样，g f将对（u1，v1）映射到对（u2，v2），并且g f最多包含四个辛变换。因此，我们需要证明以下声明：

Claim. If (u,v) and (u,v0) are hyperbolic bases determining two hyperbolic planes, then there is a symplectic map g such that g(u) = u, g(v) = v0, and g is the composition of at most two symplectic transvections. There are two case.
 索赔。如果（u，v）和（u，v0）是决定两个双曲线平面的双曲线基，那么有一个辛映射g，这样g（u）=u，g（v）=v0，g是至多两个辛变换的组合。有两种情况。

Case 1. ϕ(v,v0) = 0.6
 案例1。⑨（v，v0）=0.6

In this case, there is a symplectic transvection τv0−v,λ such that τv0−v,λ(v) = v0. We also have ϕ(u,v0 − v) = ϕ(u,v0) − ϕ(u,v) = 1 − 1 = 0.
 在这种情况下，有一个辛矢量τv0−v，λ，这样τv0−v，λ（v）=v0。我们也有_（u，v0−v）=（u，v0）−（u，v）=1−1=0。

28.8. SYMPLECTIC GROUPS
 28.8。辛群

Therefore, τv0−v,λ(u) = u, and g = τv0−v,λ does the job.
 因此，τv0−v，λ（u）=u，g=τv0−v，λ起作用。

Case 2. ϕ(v,v0) = 0.
 案例2。⑨（v，v0）=0.

First, check that (u,u + v) is a also hyperbolic basis. Furthermore,
 首先，检查（u，u+v）是否也是双曲线的基础。此外，

​                                       ϕ(v,u + v) = ϕ(v,u) + ϕ(v,v) = ϕ(v,u) = −1 = 06     .
 ⑨（V，U+V）=⑨（V，U）＋⑨（V，V）＝（V，U）=-1=06.

Thus, there is a symplectic transvection τv,λ1 such that τu,λ1(v) = u + v and τu,λ1(u) = u.
 因此，有一个辛矢量τv，λ1，使得τu，λ1（v）=u+v和τu，λ1（u）=u。

We also have
 我们也有

​                                    ϕ(u + v,v0) = ϕ(u,v0) + ϕ(v,v0) = ϕ(u,v0) = 1 = 06 ,
 ⑨（u+v，v0）=⑨（u，v0）+（v，v0）=（u，v0）=1=06，

so there is a symplectic transvection τv0−u−v,λ2 such that τv0−u−v,λ2(u + v) = v0. Since
 所以有一个辛矢量τv0−u−v，λ2，这样τv0−u−v，λ2（u+v）=v0。自从

ϕ(u,v0 − u − v) = ϕ(u,v0) − ϕ(u,u) − ϕ(u,v) = 1 − 0 − 1 = 0,
 ⑨（u，v0−u−v）=（u，v0）−（u，u）−（u，v）=1−0−1=0，

we have τv0−u−v,λ2(u) = u. Then, the composition g = τv0−u−v,λ2 ◦ τu,λ1 is such that g(u) = u and g(v) = v0.      
 我们有τv0−u−v，λ2（u）=u。那么，组成g=τv0−u−v，λ2τu，λ1是这样的g（u）=u和g（v）=v0。

We will use Proposition 28.37 in an inductive argument to prove that the symplectic transvections generate the symplectic group. First, make the following observation: If U is a nondegenerate subspace of E, so that
 我们将在归纳论点中使用命题28.37来证明辛变换产生辛群。首先，做如下观察：如果u是e的非退化子空间，那么

,
 ，

and if τ is a transvection of H⊥, then we can form the linear map idU ⊕⊥ τ whose restriction to U is the identity and whose restriction to U⊥ is τ, and idU ⊕⊥ τ is a transvection of E.
 如果τ是H的一个变换，那么我们可以形成一个线性映射iduτ，它对u的限制是同一性，对u的限制是τ，iduτ是e的一个变换。

Theorem 28.38. The symplectic group Sp(2m,K) is generated by the symplectic transvections. For every transvection f ∈ Sp(2m,K), we have det(f) = 1.
 定理28.38。辛群sp（2 m，k）由辛向矢量产生。对于每一个f∈sp（2m，k），我们得到了Det（f）=1。

Proof. Let G be the subgroup of Sp(2m,K) generated by the transvections. We need to prove that G = Sp(2m,K). Let (u1,v1,...,um,vm) be a symplectic basis of E, and let f ∈ Sp(2m,K) be any symplectic map. Then, f maps (u1,v1,...,um,vm) to another symplectic basis (). If we prove that there is some g ∈ G such that g(ui) = u0i and , then f = g and G = Sp(2m,K).
 证据。设g为由变换生成的sp（2m，k）的子群。我们需要证明g=sp（2m，k）。设（u1，v1，…，um，vm）为e的辛基，设f∈sp（2m，k）为任意辛映射。然后，f将（u1，v1，…，um，vm）映射到另一个辛基（）。如果我们证明存在一些g∈g，使得g（ui）=u0i，那么f=g，g=sp（2m，k）。

We use induction on i to prove that there is some gi ∈ G so that gi maps (u1,v1,...,ui,vi) to (
 我们利用I上的归纳法来证明存在一些g i∈g，因此gi映射（u1，v1，…，ui，vi）到（

The base case i = 1 follows from Proposition 28.37.
 基本情况i=1从命题28.37开始。

For the induction step, assume that we have some gi ∈ G mapping (u1,v1,...,ui,vi) to (), and let () be the image of (ui+1,vi+1,...,um,vm) by gi. If U is the subspace spanned by (), then each hyperbolic plane  given by (u0i+k,vi0+k) and each hyperbolic plane given by () belongs to U⊥. Using the remark before the theorem and Proposition 28.37, we can find a transvection τ mapping  onto  and leaving every vector in U fixed. Then, τ ◦ gi maps
 对于归纳步骤，假设我们有一些gi∈g映射（u1，v1，…，ui，vi）到（），并让（）是（ui+1，vi+1，…，um，vm）的gi图像。如果u是用（）表示的子空间，则由（u0i+k，vi0+k）表示的每个双曲面和由（）表示的每个双曲面都属于u。利用定理和命题28.37之前的注释，我们可以找到一个关于u中每一个向量的转移τ映射。然后，τGI图

), establishing the induction step.
 ）建立诱导步骤。

For the second statement, since we already proved that every transvection has a determinant equal to +1, this also holds for any composition of transvections in G, and since G = Sp(2m,K), we are done.     
 对于第二个陈述，由于我们已经证明了每一个transvection都有一个等于+1的行列式，这也适用于g中transvections的任何组成，并且由于g=sp（2m，k），我们就这样做了。

It can also be shown that the center of Sp(2m,K) is reduced to the subgroup {id,−id}. The projective symplectic group PSp(2m,K) is the quotient group PSp(2m,K)/{id,−id}. All symplectic projective groups are simple, except PSp(2,F2),PSp(2,F3), and PSp(4,F2), see Grove [83].
 也可以证明，sp（2m，k）的中心被缩小到亚组id、−id。投影辛群psp（2 m，k）是商群psp（2 m，k）/id、−id。除psp（2，f2）、psp（2，f3）和psp（4，f2）外，所有辛射影群都很简单，见grove[83]。

The orders of the symplectic groups over finite fields can be determined. For details, see Artin [6], Jacobson [96] and Grove [83].
 有限域上辛群的阶可以确定。有关详细信息，请参见Artin[6]、Jacobson[96]和Grove[83]。

An interesting property of symplectic spaces is that the determinant of a skew-symmetric matrix B is the square of some polynomial Pf(B) called the Pfaffian; see Jacobson [96] and Artin [6]. We leave considerations of the Pfaffian to the exercises.
 辛空间的一个有趣的性质是，斜对称矩阵b的行列式是称为pfafian的多项式pf（b）的平方；见Jacobson[96]和Artin[6]。我们在练习中考虑了pfafian。

We now take a look at the orthogonal groups.
 现在我们来看看正交群。

## 28.9     Orthogonal Groups and the Cartan–Dieudonn´e Theorem  28.9正交群与卡坦-迪乌顿定理

In this section we are dealing with a nondegenerate symmetric bilinear from ϕ over a finitedimensional vector space E of dimension n over a field of characateristic not equal to 2. Recall that the orthogonal group O(ϕ) is the group of isometries of ϕ; that is, the group of linear maps f : E → E such that
 在这一节中，我们讨论的是一个非退化对称双线性，它是在一个不等于2的特征场上，由π在一个尺寸为n的有限维向量空间e上得到的。记住，正交组o（_）是_的等轴测图组；也就是说，线性映射组f:e→e这样

​                                              ϕ(f(u),f(v)) = ϕ(u,v)        for all u,v ∈ E.
 所有u，v∈e的（f（u），f（v））=（u，v）。

The elements of O(ϕ) are also called orthogonal transformations. If M is the matrix of ϕ in any basis, then a matrix A represents an orthogonal transformation iff
 O（_）的元素也被称为正交变换。如果m是任何基的矩阵，那么矩阵a表示正交变换iff

A>MA = M.
 a>ma=m。

Since ϕ is nondegenerate, M is invertible, so we see that det(A) = ±1. The subgroup
 因为_是非退化的，m是可逆的，所以我们看到Det（a）=±1。小组

SO(ϕ) = {f ∈ O(ϕ) | det(f) = 1}
 所以（_）=f∈o（_）det（f）=1

is called the special orthogonal group (of ϕ), and its members are called rotations (or proper orthogonal transformations). Isometries f ∈ O(ϕ) such that det(f) = −1 are called improper orthogonal transformations, or sometimes reversions.
 被称为特殊正交群（的），其成员被称为旋转（或适当的正交变换）。等距f∈o（），使得det（f）=-1被称为不适当的正交变换，或有时逆转。


 

If H is any nondegenerate hyperplane in E, then D = H⊥ is a nondegenerate line and we have
 如果h是e中的任何非简并超平面，那么d=h是一条非简并线，我们有

.
 .

For any nonzero vector u ∈ D = H⊥ Consider the map τu given by
 对于任何非零向量u∈d=h考虑由

​    for all v ∈ E. If we replace u by λu with λ = 06 , we have
 对于所有v∈e，如果我们用λu替换u，用λ=06，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image051.gif)

which shows that τu depends only on the line D, and thus only the hyperplane H. Therefore, denote by τH the linear map τu determined as above by any nonzero vector u ∈ H⊥. Note that if v ∈ H, then τH(v) = v,
 这表明τu仅依赖于线d，因此仅依赖于超平面h。因此，用τh表示由任何非零向量u∈h确定的线性图τu。注意，如果v∈h，那么τh（v）=v，

and if v ∈ D, then τH(v) = −v.
 如果v∈d，那么τh（v）=−v。

A simple computation shows that
 简单的计算表明

​                                          ϕ(τH(u),τH(v)) = ϕ(u,v)       for all u,v ∈ E,
 ⑨（τh（u），τh（v））=所有u，v∈e的Ⅷ（u，v）

so τH ∈ O(ϕ), and by picking a basis consisting of u and vectors in H, that det(τH) = −1. It is also clear that τH2 = id.
 因此，τh∈o（），通过选择由u和h中的向量组成的基，该det（τh）=-1。很明显，τh2=id。

Definition 28.21. If H is any nondegenerate hyperplane in E, for any nonzero vector u ∈ H⊥, the linear map τH given by
 定义28.21。如果h是e中的任何非退化超平面，对于任何非零向量u∈h，线性映射τh由

 for all v ∈ E
 对于所有v∈e

is an involutive isometry of E called the reflection through (or about) the hyperplane H.
 是E的对合等距线，称为通过（或关于）超平面H的反射。

Remarks:
 评论：

\1.    It can be shown that if f ∈ O(ϕ) leaves every vector in some hyperplane H fixed, then either f = id or f = τH; see Taylor [169] (Chapter 11). Thus, there is no analog to symplectic transvections in the orthogonal group.
 可以证明，如果f∈o（）使某个超平面h中的每一个向量保持不变，则f=id或f=τh；见Taylor[169]（第11章）。因此，在正交组中没有类似于辛矢量的变换。

\2.    If K = R and ϕ is the usual Euclidean inner product, the matrices corresponding to hyperplane reflections are called Householder matrices.
 如果k=r和_是通常的欧几里得内积，则对应于超平面反射的矩阵称为户主矩阵。

Our goal is to prove that O(ϕ) is generated by the hyperplane reflections. The following proposition is needed.
 我们的目标是证明O（a）是由超平面反射产生的。需要以下建议。

Proposition 28.39. Let ϕ be a nondegenerate symmetric bilinear form on a vector space E. For any two nonzero vectors u,v ∈ E, if ϕ(u,u) = ϕ(v,v) and v − u is nonisotropic, then the hyperplane reflection τH = τv−u maps u to v, with H = (K(v − u))⊥. Proof. Since v − u is not isotropic, ϕ(v − u,v − u) = 06 , and we have
 提案28.39。设a为向量空间e上的非退化对称双线性形式。对于任意两个非零向量u，v∈e，如果a（u，u）=a（v，v）和v−u是非各向同性的，则超平面反射τh=τv−u映射u到v，h=（k（v−u））。证据。由于v−u不是各向同性的，因此，ω（v−u，v−u）=06，我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image053.gif)

which proves the proposition.                                                                                                         
 这证明了这个命题。

We can now obtain a cheap version of the Cartan–Dieudonn´e theorem.
 我们现在可以得到卡坦-迪乌顿定理的廉价版本。

Theorem 28.40. (Cartan–Dieudonn´e, weak form) Let ϕ be a nondegenerate symmetric bilinear form on a K-vector space E of dimension n (char(K) = 26 ). Then, every isometry f ∈ O(ϕ) with f =6 id is the composition of at most 2n − 1 hyperplane reflections.
 定理28.40。（Cartan–Dieudonn'e，弱形式）假设a是尺寸n（char（k）=26）的k向量空间e上的非退化对称双线性形式。然后，每个f=6 id的等距f∈o（）是至多2n-1超平面反射的组成。

Proof. We proceed by induction on n. For n = 0, this is trivial (since O(ϕ) = {id}).
 证据。我们在n上进行归纳，对于n=0，这是微不足道的（因为o（）=id）。

Next, assume that n ≥ 1. Since ϕ is nondegenerate, we know that there is some nonisotropic vector u ∈ E. There are three cases.
 接下来，假设n≥1。由于_是非退化的，我们知道有一些非各向同性向量u∈e，有三种情况。

Case 1. f(u) = u.
 案例1。F（U）=U。

Since ϕ is nondegenrate and u is nonisotropic, the hyperplane H = (Ku)⊥ is nondegenerate, E = H ⊕⊥ Ku, and since f(u) = u, we must have f(H) = H. The restriction f0 of of f to H is an isometry of H. By the induction hypothesis, we can write
 既然π是非退化的，u是非各向同性的，超平面h=（ku）是非退化的，e=h ku，既然f（u）=u，我们必须有f（h）=h。f到h的限制f0是h的等距测量。通过归纳假设，我们可以写下

,
 ，

where τi is some hyperplane reflection about a hyperplane, with k ≤ 2n − 3. We can extend each τi0 to a reflection τi about the hyperplane Li ⊕ Ku so that τi(u) = u, and clearly,
 其中，τi是关于超平面的超平面反射，k≤2n-3。我们可以将每个τi0扩展到超平面li_ku的反射τi，这样τi（u）=u，并且很明显，

f = τk ◦ ··· ◦ τ1.
 F=τk···τ1.

Case 2. f(u) = −u.
 案例2。F（U）=-U。

If τ is the hyperplane reflection about the hyperplane H = (Ku)⊥, then g = τ ◦ f is an isometry of E such that g(u) = u, and we are back to Case (1). Since τ2 = 1 We obtain
 如果τ是关于超平面h=（ku）的超平面反射，那么g=τf是e的等距测量，这样g（u）=u，我们回到情况（1）。因为τ2=1，我们得到

f = τ ◦ τk ◦ ··· ◦ τ1
 f=ττk···τ1

where τ and the τi are hyperplane reflections, with k ≥ 2n − 3, and we get a total of 2n − 2 hyperplane reflections.
 其中，τ和τi是超平面反射，k≥2n−3，我们总共得到2n−2超平面反射。

​       Case 3. f(u) =6   u and f(u) =6  −u.
 案例3。F（U）=6 U，F（U）=6−U。

Note that f(u) − u and f(u) + u are orthogonal, since
 注意f（u）−u和f（u）+u是正交的，因为

ϕ(f(u) − u,f(u) + u) = ϕ(f(u),f(u)) + ϕ(f(u),u) − ϕ(u,f(u)) − ϕ(u,u) = ϕ(u,u) − ϕ(u,u) = 0. We also have
 Ⅷ（f（u）−u，f（u）+u）=Ⅷ（f（u），f（u））+Ⅷ（f（u），u）−Ⅷ（u，f（u））−Ⅷ（u，u）=Ⅷ（u，u）−Ⅷ（u，u）=0.我们也有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image055.gif)

so f(u) + u and f(u) − u cannot be both isotropic, since u is not isotropic. If f(u) − u is not isotropic, then the reflection τf(u)−u is such that
 所以f（u）+u和f（u）−u不能同时是各向同性的，因为u不是各向同性的。如果f（u）−u不是各向同性的，那么反射τf（u）−u是这样的：

τf(u)−u(u) = f(u),
 τf（u）−u（u）=f（u），

and since τf2(u)−u = id, if g = τf(u)−u ◦ f, then g(u) = u, and we are back to case (1). We obtain f = τf(u)−u ◦ τk ◦ ··· ◦ τ1
 既然τf2（u）−u=id，如果g=τf（u）−u f，那么g（u）=u，我们回到情况（1）。我们得到f=τf（u）−uτk···τ1

where τf(u)−u and the τi are hyperplane reflections, with k ≥ 2n − 3, and we get a total of 2n − 2 hyperplane reflections.
 其中，τf（u）−u和τi是超平面反射，k≥2n−3，我们得到了2n−2个超平面反射。

If f(u) + u is not isotropic, then the reflection τf(u)+u is such that
 如果f（u）+u不是各向同性的，那么反射τf（u）+u是这样的：

τf(u)+u(u) = −f(u),
 τf（u）+u（u）=-f（u），

and since τf2(u)+u = id, if g = τf(u)+u ◦ f, then g(u) = −u, and we are back to case (2). We obtain f = τf(u)−u ◦ τ ◦ τk ◦ ··· ◦ τ1
 既然τf 2（u）+u=id，如果g=τf（u）+u_f，那么g（u）=−u，我们回到情况（2）。我们得到f=τf（u）−uττk···τ1

where τ,τf(u)−u and the τi are hyperplane reflections, with k ≥ 2n−3, and we get a total of 2n − 1 hyperplane reflections. This proves the induction step. 
 其中，τ、τf（u）−u和τi是超平面反射，k≥2n−3，我们得到2n−1的超平面反射。这证明了归纳步骤。

The bound 2 1 is not optimal. The strong version of the Cartan–Dieudonn´e theorem says that at most      reflections are needed, but the proof is harder. Here is a neat proof due to E. Artin (see [6], Chapter III, Section 4).
 绑定2 1不是最佳的。卡坦-迪乌登定理的强大版本说，大多数情况下需要反思，但证明更难。这是一个整洁的证据，由于E.Artin（见[6]，第三章，第4节）。

Case 1 remains unchanged. Case 2 is slightly different: f(u) − u = 06 is not isotropic. Since ϕ(f(u) + u,f(u) − u) = 0, as in the first subcase of Case (3), g = τf(u)−u ◦ f is such that g(u) = u and we are back to Case 1. This only costs one more reflection.
 案例1保持不变。情况2略有不同：f（u）−u=06不是各向同性的。由于_（f（u）+u，f（u）−u）=0，如第（3）种情况的第一个亚基，g=τf（u）−u f是这样的，g（u）=u，我们回到了第1种情况。这只需要再考虑一次。

The new (bad) case is:
 新的（坏的）情况是：

Case 3’. f(u) − u is nonzero and isotropic for all nonisotropic u ∈ E. In this case, what saves us is that E must be an Artinian space of dimension n = 2m and that f must be a rotation (f ∈ SO(ϕ)).
 案例3”。f（u）−u是所有非各向同性u∈e的非零和各向同性。在这种情况下，我们省去的是，e必须是尺寸n=2米的Artian空间，f必须是一个旋转（f∈so（））。

If we acccept this fact proved in Proposition 28.43 then pick any hyperplane reflection τ. Then, since f is a rotation, g = τ ◦ f is not a rotation because det(g) = det(τ)det(f) = (−1)(+1) = −1, so g(u) − u is either 0 or not isotropic for some nonisotropic u ∈ E (otherwise, g would be a rotation), we are back to either Case 1 or Case 2, and using the induction hypothesis, we get τ ◦ f = τk ◦ ...,τ1,
 如果我们接受28.43号提案中证明的这个事实，那么选取任何超平面反射τ。那么，既然f是一个旋转，g=τf不是一个旋转，因为det（g）=det（τ）det（f）=（-1）（+1）=−1，所以g（u）−u是0或不是各向同性的，对于一些非各向同性的u∈e（否则，g将是一个旋转），我们返回到情况1或情况2，并且使用归纳假设，我们得到τf=τk…，τ1，

where each *τi* is a hyperplane reflection, and *k* ≤ 2*m*. Since *τ* ◦ *f* is not a rotation, actually *k* ≤ 2*m*−1, and then *f* = *τ* ◦*τk* ◦*...,τ*1, the composition of at most *k* +1 ≤ 2*m* hyperplane reflections.

Therefore, except for the fact that in Case 3’, *E* must be an Artinian space of dimension *n* = 2*m* and that *f* must be a rotation, which has not been proven yet, we proved the following theorem.

**Theorem 28.41.** *(Cartan–Dieudonn´e, strong form) Let ϕ be a nondegenerate symmetric bilinear form on a K-vector space E of dimension n (*char(*K*) = 26 *). Then, every isometry f* ∈ **O**(*ϕ*) *with f* =6 id *is the composition of at most n hyperplane reflections.*

To fill in the gap, we need two propositions.

**Proposition 28.42.** *Let* (*E,ϕ*) *be an Artinian space of dimension* 2*m, and let U be a totally isotropic subspace of dimension m. For any isometry f* ∈ **O**(*ϕ*)*, if f*(*U*) = *U, then* det(*f*) = 1 *(f is a rotation).*

*Proof.* We know that we can find a basis (*u*1*,...,um,v*1*,...,vm*) of *E* such (*u*1*,...,um*) is a basis of *U* and *ϕ* is represented by the matrix

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image057.gif) *.*

Since *f*(*U*) = *U*, the matrix representing *f* is of the form

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image059.gif) *.*

The condition *A*>*Am,mA* = *Am,m* translates as

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image061.gif)that is,

*,*

which implies that *B*>*D* = *I*, and so det(*A*) = det(*B*)det(*D*) = det(*B*>)det(*D*) = det(*B*>*D*) = det(*I*) = 1*,*

as claimed                                                                                                                                       ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image062.gif)

**Proposition 28.43.** *Let ϕ be a nondegenerate symmetric bilinear form on a space E of dimension n, and let f be any isometry f* ∈ **O**(*ϕ*) *such that f*(*u*)−*u is nonzero and isotropic for every nonisotropic vector u* ∈ *E. Then, E is an Artinian space of dimension n* = 2*m, and f is a rotation (f* ∈ **SO**(*ϕ*)*).*

*Proof.* We follow E. Artin’s proof (see [6], Chapter III, Section 4). First, consider the case *n* = 2. Since we are assuming that *E* has some nonzero isotropic vector, by Proposition 28.26, *E* is an Artinian plane and there is a basis in which *ϕ* is represented by the matrix

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image064.gif) *,*

we have *ϕ*((*x*1*,x*2)*,*(*x*1*,x*2)) = 2*x*1*x*2, and the matrices representing isometries are of the form ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image066.gif) or   ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image068.gif)*.*

In the second case,

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image070.gif) *,*

but *u* = (*λ,*1) is a nonisotropic vector such that *f*(*u*)−*u* = 0. Therefore, we must be in the first case, and det(*f*) = +1.

Let us now assume that *n* ≥ 3. We are going to prove that *f*(*y*) − *y* is isotropic for all nonzero isotropic vectors *y*. Let *y* be any nonzero isotropic vector. Since *n* ≥ 3, the orthogonal space (*Ky*)⊥ has dimension at least 2, and we know that rad(*Ky*) = rad((*Ky*)⊥), a space of dimension at most 1, which implies that (*Ky*)⊥ contains some nonisotropic vector, say *x*. We have      ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image072.gif)= 0, for ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image074.gif)1. Then, by hypothesis, the vectors *f*(*x*) − *x,f*(*x* + *y*) − (*x* + *y*) = *f*(*x*) − *x* + (*f*(*y*) − *y*), and *f*(*x*−*y*)−(*x*−*y*) = *f*(*x*)−*x*−(*f*(*y*)−*y*) are isotropic. The last two vectors can be written

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image076.gif)1, so we have

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image078.gif)*.*

If we write the two equations corresponding to  ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image080.gif)1, and then add them up, we get

*ϕ*(*f*(*y*) − *y,f*(*y*) − *y*) = 0*.*

这证明了f（y）−y对任何非零各向同性向量y都是各向同性的。由于假设f（u）−u对每个非各向同性向量u都是各向同性的，我们证明了f（u）−u对每个u∈e都是各向同性的。如果我们让w=im（f−id），那么w中的每个向量都是各向同性的，因此w是完全各向同性的。pic（回想一下，我们假设char（k）=26，因此，a由Φ决定）。对于任何u∈e和任何v∈w，由于w是完全各向同性的，我们有

ϕ(f(u) − u,f(v) − v) = 0,
 ⑨（f（u）−u，f（v）−v）=0，

and since f(u) − u ∈ W and v ∈ W ⊥, we have ϕ(f(u) − u,v) = 0, and so
 既然f（u）−u∈w和v∈w，我们就有（f（u）−u，v）=0，所以

0 = ϕ(f(u) − u,f(v) − v)
 0=_（f（u）−u，f（v）−v）

= ϕ(f(u),f(v)) − ϕ(u,f(v)) − ϕ(f(u) − u,v)
 =_（f（u），f（v））−_（u，f（v））−_（f（u）−u，v）

= ϕ(u,v) − ϕ(u,f(v))
 =_（u，v）-_（u，f（v））

= ϕ(u,v − f(v)),
 =⑨（u，v−f（v）），

for all u ∈ E. Since ϕ is nonsingular, this means that f(v) = v, for all v ∈ W ⊥. However, by hypothesis, no nonisotropic vector is left fixed, which implies that W ⊥ is also totally isotropic. In summary, we proved that W ⊆ W ⊥ and W ⊥ ⊆ W ⊥⊥ = W, that is,
 对于所有u e，由于_是非奇异的，这意味着f（v）=v，对于所有v w。然而，根据假设，没有非各向同性向量是固定的，这意味着w也是完全各向同性的。总之，我们证明了w w和w w=w，即，

W = W ⊥.
 W=W。

Since, dim(W) + dim(W ⊥) = n, we conclude that W is a totally isotropic subspace of E such that dim(W) = n/2.
 由于dim（w）+dim（w）=n，我们得出w是e的完全各向同性子空间，因此dim（w）=n/2。

By Proposition 28.29, the space E is an Artinian space of dimension n = 2m. Since W = W ⊥ and f(W) = W, by Proposition 28.42, the isometry f is a rotation. 
 根据命题28.29，空间E是一个尺寸为n=2米的Artian空间。由于w=w和f（w）=w，根据命题28.42，等距线f是一个旋转。

Remarks:
 评论：

\1.    Another way to finish the proof of Proposition 28.43 is to prove that if f is an isometry, then
 完成28.43号提案的证明的另一种方法是证明，如果f是等距线，那么

Ker(f − id) = (Im(f − id))⊥.
 ker（f−id）=（im（f−id））。

After having proved that W = Im(f − id) is totally isotropic, we get
 在证明w=im（f-id）是完全各向同性之后，我们得到

Ker(f − id) = Im(f − id),
 ker（f-id）=im（f-id）、

which implies that (f − id)2 = 0. From this, we deduce that det(f) = 1. For details, see Jacobson [96] (Chapter 6, Section 6).
 这意味着（f-id）2=0。由此，我们推导出Det（f）=1。有关详细信息，请参见Jacobson[96]（第6章第6节）。

\2.    If f = τHk ◦ ··· ◦ τH1, where the Hi are hyperplanes, then it can be shown that
 如果f=τhk····τh1，其中hi是超平面，则可以证明

dim(H1 ∩ H2 ∩ ··· ∩ Hs) ≥ n − s.
 尺寸（h1 h2··hs）≥N s。

Now, since each Hi is left fixed by τHi, we see that every vector in H1 ∩ ··· ∩ Hs is left fixed by f. In particular, if s < n, then f has some nonzero fixed point. As a consequence, an isometry without fixed points requires n hyperplane reflections.
 现在，由于每个hi都由τhi保持不变，我们看到h1··hs中的每个向量都由f保持不变。特别是，如果s<n，那么f有一些非零固定点。因此，没有固定点的等距测量需要n个超平面反射。

# 28.10 Witt’s Theorem  28.10维特定理

Witt’s theorem was referred to as a “scandal” by Emil Artin. What he meant by this is that one had to wait until 1936 (Witt [184]) to formulate and prove a theorem at once so simple in its statement and underlying concepts, and so useful in various domains (geometry, arithmetic of quadratic forms).
 维特定理被埃米尔·阿丁称为“丑闻”。他所指的是，一个人必须等到1936年（witt[184]）才能立刻制定和证明一个定理，它的表述和基本概念如此简单，在各个领域（几何、二次型算术）也如此有用。

Besides Witt’s original proof (Witt [184]), Chevalley’s proof [37] seems to be the “best” proof that applies to the symmetric as well as the skew-symmetric case. The proof in Bourbaki [24] is based on Chevalley’s proof, and so are a number of other proofs. This is the one we follow (slightly reorganized). In the symmetric case, Serre’s exposition is hard to beat (see Serre [152], Chapter IV).
 除了维特的原始证明（维特[184]），契瓦利的证明[37]似乎是适用于对称和斜对称情况的“最佳”证明。Bourbaki[24]中的证明基于Chevalley的证明，其他一些证明也是如此。这是我们所遵循的（稍微重组）。在对称的情况下，Serre的论述很难打破（见Serre[152]，第四章）。

The following observation is one of the key ingredients in the proof of Theorem 28.45.
 下面的观察是定理28.45证明的关键成分之一。

Proposition 28.44. Given a finite-dimensional space E equipped with an -Hermitan form ϕ, if U1 and U2 are two subspaces of E such that U1 ∩U2 = (0) and if we have metric linear maps f1 : U1 → E and f2 : U2 → E such that
 提案28.44。给定一个有限维空间e，如果u1和u2是e的两个子空间，那么u1 u2=（0），如果我们有公制线性映射f1:u1→e和f2:u2→e，那么

​                                  ϕ(f1(u1),f2(u2)) = ϕ(u1,u2)      for ui ∈ Ui (i = 1,2),                               (∗)
 ⑨（f1（u1），f2（u2））=⑨（u1，u2）代表ui∈ui（i=1,2），（）

then the linear map f : U1 ⊕ U2 → E given by f(u1 + u2) = f1(u1) + f2(u2) extends f1 and f2 and is metric. Furthermore, if f1 and f2 are injective, then so if f.
 然后，由f（u1+u2）=f1（u1）+f2（u2）给出的线性图f:u1 u2→e延伸f1和f2，为公制。此外，如果f1和f2是内射的，那么如果f。

Proof. Indeed, since f1 and f2 are metric and using (∗), we have
 证据。事实上，因为f1和f2是公制的，并且使用（），我们有

ϕ(f1(u1) + f2(u2),f1(v1) + f2(v2)) = ϕ(f1(u1),f1(v1)) + ϕ(f1(u1),f2(v2))
 Ⅷ（f1（u1）+f2（u2），f1（v1）+f2（v2））=Ⅷ（f1（u1），f1（v1））+Ⅷ（f1（u1），f2（v2））

\+ ϕ(f2(u2),f1(v1)) + ϕ(f2(u2),f2(v2)) = ϕ(u1,v1) + ϕ(u1,v2) + ϕ(u2,v1) + ϕ(u2,v2) = ϕ(u1 + u2,v2 + v2).
 +Ⅷ（F2（U2），F1（V1））+Ⅷ（F2（U2），F2（V2））=Ⅷ（U1，V1）+Ⅷ（U1，V2）+Ⅷ（U2，V1）+Ⅷ（U2，V2）=Ⅷ（U1+U2，V2+V2）。

Thus f is a metric map extending f1 and f2.                                                                                    
 因此，F是延伸f1和f2的度量图。

Theorem 28.45. (Witt, 1936) Let E and E0 be two finite-dimensional spaces respectively equipped with two nondegenerate -Hermitan forms ϕ and ϕ0 satisfying condition (T), and assume that there is an isometry between (E,ϕ) and (E0,ϕ0). For any subspace U of E, every injective metric linear map f from U into E0 extends to an isometry from E to E0.
 定理28.45。（witt，1936）让e和e0分别为两个有限维空间，分别配备两个满足条件（t）的非简并-厄米坦形式，并假设（e，_）和（e0，_0）之间存在一个等距线。对于e的任何子空间u，从u到e0的每个内射度量线性映射f延伸到从e到e0的等距线。

Proof. Since (E,ϕ) and (E0,ϕ0) are isometric, we may assume that E0 = E and ϕ0 = ϕ (if h: E → E0 is an isometry, then h−1 ◦f is an injective metric map from U into E. The details are left to the reader).
 证据。因为（e，_）和（e0，_）是等距的，我们可以假设e0=e和_0=_（如果h:e→e0是等距的，那么h-1 f是从u到e的一个注入式公制图。细节留给读者）。

We proceed by induction on the dimension r of U. Since the proof is quite intricate, we spell out the general plan of attack. For the induction step, we first show that we can reduce the situation to what we call Case (H), namely that the subspace of U left fixed by f is a hyperplane H in U. Then, the set D = {f(u) − u | u ∈ U} is a line in U and it turns out that D⊥ is a hyperplane in E. We now introduce Hypothesis (V), which says we can find a nontrivial subspace V of E orthogonal to D and such that V ∩ U = V ∩ f(U) = (0). We show that if Hypothesis (V) holds, then f can be extended to an isometry of U ⊕ V . It is then possible to further extend f to an isometry of E.
 我们对U的维R进行归纳，由于证明是相当复杂的，所以我们阐明了攻击的总体方案。对于诱导步骤，我们首先证明了我们可以将情形简化为（h），也就是说，由f左固定的u的子空间是u中的超平面h，然后，集合d=f（u）−u u∈u是u中的一条线，结果表明d是e中的超平面，现在我们引入假设。（v），也就是说我们可以找到一个与d正交的e的非平凡子空间v，这样v u=v f（u）=0。我们证明，如果假设（v）成立，那么f可以推广到u v的等距测量。然后可以进一步将f扩展到e的等值线。

To prove that Hypothesis (V) holds we consider two cases. In Case (a), we obtain some V such that E = U ⊕ V and we are done. In Case (b), we obtain some V such that D⊥ = U ⊕V . We are then reduced to the situation where U = D⊥ is a hyperplane in E and f is an isometry of U. To finish the proof we pick any v /∈ U, so that E = U ⊕ Kv, and we find some v1 ∈ E such that
 为了证明假设（v）成立，我们考虑了两个案例。在（a）种情况下，我们得到一些v，这样e=u_v，我们就完成了。在（b）种情况下，我们得到一些v，这样d=u v。然后，我们将其简化为u=d是e中的超平面，f是u的一个等距，为了完成这个证明，我们选取了任意v/∈u，使e=u_kv，我们发现了一些v1∈e，这样

​                                                 ϕ(f(u),v1) = ϕ(u,v)      for all u ∈ U
 所有u∈u的（f（u），v1）=（u，v）

ϕ(v1,v1) = ϕ(v,v).
 ⑨（v1，v1）=⑨（v，v）。

Then, by Proposition 28.44, we can extend f to a metric map g of U + Kv = E such that g(v) = v1. The argument used to find v1 makes use of (†) (see below) and is bit tricky. We also makes use of Property (T) in the form of Lemma 28.28.
 然后，根据命题28.44，我们可以把f扩展到u+kv=e的度量图g，这样g（v）=v1。用于查找v1的参数使用了（†）（见下文）并有点棘手。我们还使用了属性（t）的形式lemma 28.28。

We now go back to the proof. The case r = 0 is trivial. For the induction step, r ≥ 1 so U = (0)6 , and let H be any hyperplane in U. Let f : U → E be an injective metric linear map. By the induction hypothesis, the restriction f0 of f to H extends to an isometry g0 of E. If g0 extends f, we are done. Otherwise, H is the subspace of elements of U left fixed by g0−1 ◦f. If the theorem holds in this situation, namely the subspace of U left fixed by g0−1 ◦f is a hyperplane H in U, then we have an isometry g1 of E extending g0−1 ◦ f, and g0 ◦ g1 is an isometry of E extending f. Therefore, we are reduced to the following situation:
 我们现在回到证据上来。r=0的情况是微不足道的。对于诱导步骤，r≥1，所以u=（0）6，并且h是u中的任何超平面。让f:u→e是一个内射度量线性映射。根据诱导假设，F对H的限制性f0延伸到E的等值线g0，如果g0延伸到F，我们就完成了。否则，h是由g0−1 f固定的u元素的子空间。如果定理在这种情况下成立，即由g0−1 f固定的u元素的子空间是u中的超平面h，则我们有e延伸g0−1 f的等距g1，而g0 g1是e延伸f的等距。关于，我们将减少到以下情况：

Case (H). The subspace of U left fixed by f is a hyperplane H in U.
 案例（h）。F左固定的U的子空间是U中的超平面H。

In this case, the set D = {f(u) − u | u ∈ U} is a line in U (a one-dimensional subspace).
 在这种情况下，集合d=f（u）−u u∈u是u（一维子空间）中的一条线。

For all u,v ∈ U, we have ϕ(f(u),f(v) − v) = ϕ(f(u),f(v)) − ϕ(f(u),v) = ϕ(u,v) − ϕ(f(u),v) = ϕ(u − f(u),v),
 对于所有u，v∈u，我们都有_（f（u），f（v）−v）=（f（u），f（v））−_（f（u），v）=（u，v）−（f（u），v）=（u−f（u），v），

that is
 那就是

​                                     ϕ(f(u),f(v) − v) = ϕ(u − f(u),v)         for all u,v ∈ U,                            (∗∗)
 所有u，v∈u，（_）

and if u ∈ H, which means that f(u) = u, we get u ∈ D⊥. Therefore, H ⊆ D⊥. Since ϕ is nondegenerate, we have dim(D) + dim(D⊥) = dim(E), and since dim(D) = 1, the subspace D⊥ is a hyperplane in E.
 如果u∈h，这意味着f（u）=u，我们得到u∈d。因此，H D。由于ω是非退化的，所以我们有dim（d）+dim（d）=dim（e），由于dim（d）=1，子空间d是e中的超平面。

Hypothesis (V). We can find a nontrivial subspace V of E orthogonal to D and such that
 假设（v）。我们可以找到一个与d正交的e的非平凡子空间v，这样

V ∩ U = V ∩ f(U) = (0).
 V U=V F（U）=（0）。

Claim. Hypothesis (V) implies that f can be extended to an isometry of U ⊕ V .
 索赔。假设（v）意味着f可以扩展到u v的等距测量。

Proof of Claim. If Hypothesis (V) holds, then we have
 索赔证明。如果假设（v）成立，那么我们有

​                                      ϕ(f(u),v) = ϕ(u,v)       for all u ∈ U and all v ∈ V ,
 （f（u），v）=（u，v），对于所有u∈u和所有v∈v，

since ϕ(f(u),v) − ϕ(u,v) = ϕ(f(uf)1−=u,vf ) = 0and f, with2 the inclusion off(u) − u ∈ VD intoand Ev , we can extend∈ V orthogonal to D. By Proposition 28.44 with f{ to an injective metric map on U ⊕ V Dleaving all vectors in. V fixed. In this case, the set f(w) − w | w ∈ U ⊕ V } is still the line 
 既然_（f（u），v）−_（u，v）=（f（uf）1−u，vf）=0和f，在2不包含（u）−u∈v d intoand ev的情况下，我们可以通过命题28.44，用f扩展到u v上的一个内射度量图，而不保留所有的向量。V固定。在这种情况下，集合f（w）−w w∈u v仍然是线

We show below that the fact that f can be extended to U ⊕ V implies that f can be
 我们在下面表明，f可以扩展到u v这一事实意味着f可以

extended to the whole ofIn case (b), D⊥ = U ⊕ V Ewhere. There are two cases. In Case (a),D⊥fis a hyperplane incan be extended to an isometry ofE and fEis an isometry of= U ⊕VEand we are done..       D⊥. By a subtle argument, we will show that
 扩展到整个案例（b），d=u v e这里。有两种情况。在（a）种情况下，d fi是一个超平面inca，扩展到e和fei的等距，等距等于u vea，我们就完成了..d。通过微妙的争论，我们将展示

We are reduced to proving that a subspace V as above exists. We distinguish between two cases.
 我们可以证明上面的子空间V存在。我们区分两种情况。

​      Case (a). U ⊆6  D⊥.
 案例（a）。U 6 D。

Proof of Case (a). In this case, formula (∗∗) show that f(U) is not contained in D⊥ (check this!). Consequently,
 案件证明（a）。在这种情况下，公式（）表示f（u）不包含在d中（勾选此项！）因此，

U ∩ D⊥ = f(U) ∩ D⊥ = H.
 U D=F（U）D=H.

We can pickV ∩fU(U⊕) = (0)V 6=VDto be any supplement of. Since⊥ (sinceUU⊕is not contained inV contains the hyperplaneH in DD⊥, and the above formula shows that⊥ andDV⊥⊆(sinceD⊥), we must haveD⊥ = H V and HV ∩UU=), and     ⊕ E = U⊆⊕ V , and as we showed as a consequence of hypothesis (V), f can be extended to an isometry of
 我们可以选择v fu（u）=（0）v 6=vd作为任何补充。由于（since u u不包含，in v在dd中包含超平面，并且上述公式表明和dv（sinced），我们必须有d=h v和hv uu=）和e=u v，并且，正如我们在假设（v）的结果中所示，f可以扩展为

U ⊕ V = E.                                                                                                                                          
 u v=e.

Case (b). U ⊆ D⊥.
 案例（b）。U D。

sinceProof of Case (b).D = {f(u) − uIn this case, formula (| u ∈ U}, we have D∗∗⊆) Dshows that⊥; that is, the linef(U) ⊆ DD⊥ sois isotropic.U +f(U) ⊆ D⊥, and
 鉴于情况（b）.d=f（u）−ui，在这种情况下，公式（u∈u，我们有d）表示，即，线f（u）dd sois各向同性.u+f（u）d，和

We show that there exists a subspace V of D⊥, such that
 我们证明存在d的子空间v，这样

D⊥ = U ⊕ V = f(U) ⊕ V.
 D=U V=F（U）V.

Thus, case (b) shows that we are reduced to the situation where U = D⊥ and f is an isometry of U.
 因此，情况（b）表明，我们被简化到u=d和f是u的等距测量。

x /∈IfHU, and let= f(Uy)U∈we pick, we havef(U) withV to be a supplement ofy /∈ H. Since f(H) =UH in(pointwise),D⊥. Otherwise, letf is injective, andx ∈ U withH is a hyperplane in
 x/∈ifhu，且设=f（uy）u∈we pick，我们将f（u）与v作为y/∈h的补充，因为f（h）=uh in（pointwise），d。否则，Letf是内射的，x∈u和h是中的超平面。

​                                                   U = H ⊕ Kx,         f(U) = H ⊕ Ky.
 u=h kx，f（u）=h ky。

We claim that x + y /∈ U. Otherwise, since y = x + y − x, with x + y,x ∈ U and since y ∈ f(U), we would have y ∈ U ∩ f(U) = H, a contradiction. Similarly, x + y /∈ f(U). It follows that
 我们声称x+y/∈u，否则，因为y=x+y−x，有x+y，x∈u，既然y∈f（u），我们就有y∈u f（u）=h，一个矛盾。同样，x+y/∈f（u）。接下来是

*U*    + f(U) = U ⊕ K(x + y) = f(U) ⊕ K(x + y).
 +f（u）=u k（x+y）=f（u）k（x+y）。

Now, pick W to be any supplement of U + f(U) in D⊥ so that D⊥ = (U + f(U)) ⊕ W, and let
 现在，选择w作为d中u+f（u）的任何补充，使d=（u+f（u））w，并让

*V*    = K(x + y) + W.
 =K（x+y）+W。

Then, since x ∈ U,y ∈ f(U), W ⊆ D⊥, and U + f(U) ⊆ D⊥, we have V ⊆ D⊥. We also have
 然后，由于x∈u，y∈f（u），w d，和u+f（u）d，我们得到v d。我们也有

U ⊕ V = U ⊕ K(x + y) ⊕ W = (U + f(U)) ⊕ W = D⊥
 u v=u k（x+y）w=（u+f（u））w=d

and
 和

f(U) ⊕ V = f(U) ⊕ K(x + y) ⊕ W = (U + f(U)) ⊕ W = D⊥,
 F（U）V=F（U）K（X+Y）W=（U+F（U））W=D，

so as we showed as a consequence of hypothesis (V), f can be extended to an isometry of the hyperplane D⊥ = U ⊕ V , and D is still the line {f(w) − w | w ∈ U ⊕ V }. 
 因此，根据假设（v）的结果，f可以扩展到超平面d=u v的等距线，d仍然是线f（w）−w w∈u v。

The argument in the proof of Case (b) shows that we are reduced to the situation where U = D⊥ is a hyperplane in E and f is an isometry of U. If we pick any v /∈ U, then E = U ⊕ Kv, so suppose we can find some v1 ∈ E such that
 例（b）证明中的论点表明，我们简化到u=d是e中的超平面，f是u的一个等值线的情形，如果我们选取任何v/∈u，那么e=u kv，那么假设我们可以找到一些v1∈e，这样

​                                                 ϕ(f(u),v1) = ϕ(u,v)      for all u ∈ U
 所有u∈u的（f（u），v1）=（u，v）

ϕ(v1,v1) = ϕ(v,v).
 ⑨（v1，v1）=⑨（v，v）。

The first condition is condition (∗) of Proposition 28.44, and the second condition asserts that the map λv 7→ λv2 from the line Kv to the line Kv1 is a metric map. Then, by Proposition 28.44, we can extend f to a metric map g of U + Kv = E such that g(v) = v1. To find v1, let us prove that for every v ∈ E, there is some v0 ∈ E such that
 第一个条件是命题28.44的条件（），第二个条件断言从Kv线到Kv1线的映射λv 7→λv2是公制映射。然后，根据命题28.44，我们可以把f扩展到u+kv=e的度量图g，这样g（v）=v1。为了找到v1，让我们证明对于每一个v∈e，都有一些v0∈e，这样

​                                                 ϕ(f(u),v0) = ϕ(u,v)      for all u ∈ U.                                            (†)
 所有u∈u.（†）的（f（u），v0）=（u，v）

This is because the linear form u 7→ ϕ(f−1(u),v) (u ∈ U) is the restriction of a linear form ψ ∈ E∗, and since ϕ is nondegenerate, there is some (unique) v0 ∈ E, such that
 这是因为线性形式u 7→（f−1（u），v）（u∈u）是线性形式ψ∈e的限制，并且由于_是非退化的，所以有一些（唯一的）v0∈e，这样

​                                                     ψ(x) = ϕ(x,v0)      for all x ∈ E,
 ψ（x）＝（x，v0），对于所有x∈e，

which implies that ϕ(u,v0) = ϕ(f−1(u),v) for all u ∈ U,
 也就是说，对于所有u∈u，（u，v0）=（f−1（u），v）

and since f is an automorphism of U, that (†) holds. Furthermore, observe that formula (†) still holds if we add to v0 any vector y in D, since f(U) = U = D⊥. Therefore, for any v1 = v0 + y with y ∈ D, if we extend f to a linear map of E by setting g(v) = v1, then by (†) we have ϕ(g(u),g(v)) = ϕ(u,v) for all u ∈ U.
 因为f是u的自同构，所以（†）成立。此外，如果我们在v0中加上d中的任何向量y，则可以观察到公式（†）仍然成立，因为f（u）=u=d。因此，对于任何带有y∈d的v1=v0+y，如果我们通过设置g（v）=v1将f扩展到e的线性映射，那么通过（†）我们得到了所有u∈u的（g（u），g（v））=（u，v）。

We still need to pick y ∈ D so that v1 = v0 + y satisfies ϕ(v1,v1) = ϕ(v,v). However, since v /∈ U = D⊥, the vector v is not orthogonal D, and by Lemma 28.28, there is some y0 ∈ D such that ϕ(v0 + y0,v0 + y0) = ϕ(v,v).
 我们仍然需要选择y∈d，以便v1=v0+y满足_（v1，v1）=（v，v）。然而，由于v/∈u=d，向量v不是正交d，并且根据引理28.28，有一些y0∈d，这样使得饨（v0+y0，v0+y0）=（v，v）。

Then, if we let v1 = v0 + y0, by Proposition 28.44, we can extend f to a metric map g of U + Kv = E by setting g(v) = v1. Since ϕ is nondegenerate, g is an isometry. 
 然后，如果我们让v1=v0+y0，根据命题28.44，我们可以通过设置g（v）=v1，将f扩展到u+kv=e的公制图g。由于_是非简并的，g是等距测量。

The first corollary of Witt’s theorem is sometimes called the Witt’s cancellation theorem.
 维特定理的第一个推论有时被称为维特对消定理。

Theorem 28.46. (Witt Cancellation Theorem) Let (E1,ϕ1) and (E2,ϕ2) be two pairs of finite-dimensional spaces and nondegenerate -Hermitian forms satisfying condition (T), and assume that (E1,ϕ1) and (E2,ϕ2) are isometric. For any subspace U of E1 and any subspace V of E2, if there is an isometry f : U → V , then there is an isometry g: U⊥ → V ⊥.
 定理28.46。（维特相消定理）设（e1，_）和（e2，_）为满足条件（t）的两对有限维空间和非退化厄米特形式，并假定（e1，_）和（e2，_）是等距的。对于e1的任何子空间u和e2的任何子空间v，如果存在等距f:u→v，则存在等距g:u→v。

Proof. If f : U → V is an isometry between U and V , by Witt’s theorem (Theorem 28.46), the linear map f extends to an isometry g between E1 and E2. We claim that g maps U⊥ into V ⊥. This is because if v ∈ U⊥, we have ϕ1(u,v) = 0 for all u ∈ U, so
 证据。如果f:u→v是u和v之间的等值线，根据维特定理（定理28.46），线性映射f延伸到e1和e2之间的等值线g。我们声称G把u映射成v。这是因为如果v u，我们将所有u u都取_（u，v）=0，所以

​                                          ϕ2(g(u),g(v)) = ϕ1(u,v) = 0      for all u ∈ U,
 _（g（u），g（v））=_（u，v）=0，对于所有u∈u，

and since g is a bijection between U and V , we have g(U) = V , so we see that g(v) is orthogonal to V for every v ∈ U⊥; that is, g(U⊥) ⊆ V ⊥. Since g is a metric map and since ϕ1 is nondegenerate, the restriction of g to U⊥ is an isometry from U⊥ to V ⊥. 
 因为g是u和v之间的双射，所以我们得到了g（u）=v，所以我们看到g（v）对于每个v∈u是与v正交的，也就是说，g（u）v。由于g是一个公制地图，且由于_是非退化的，因此g对u的限制是从u到v的等距测量。

A pair (E,ϕ) where E is finite-dimensional and ϕ is a nondegenerate -Hermitian form is often called an -Hermitian space. When  = 1 and ϕ is symmetric, we use the term Euclidean space or quadratic space. When  is alternating, we use the term
 其中e是有限维的，而a是非简并的-厄米特形式的对（e，a），通常称为-厄米特空间。当=1和_对称时，我们使用欧几里得空间或二次空间。当是交替的，我们用这个词

symplectic space. When  = 1 and the automorphism λ 7→ λ is not the identity we use the term Hermitian space, and when 1, we use the term skew-Hermitian space.
 辛空间。当=1且自同构λ7→λ不是恒等式时，我们使用术语Hermitian空间；当1时，我们使用术语Skew Hermitian空间。

We also have the following result showing that the group of isometries of an -Hermitian space is transitive on totally isotropic subspaces of the same dimension.
 结果还表明，厄米空间的等轴测群在同一维的完全各向同性子空间上是可传递的。

Theorem 28.47. Let E be a finite-dimensional vector space and let ϕ be a nondegenerate -Hermitian form on E satisfying condition (T). Then for any two totally isotropic subspaces U and V of the same dimension, there is an isometry f ∈ Isom(ϕ) such that f(U) = V . Furthermore, every linear automorphism of U is induced by an isometry of E.
 定理28.47。设e为有限维向量空间，当e满足条件（t）时，设_为非退化厄米形式。那么对于任意两个完全各向同性的同维子空间u和v，有一个等距f∈isom（），这样f（u）=v。此外，u的每一个线性自同构都是由e的一个等距引起的。

Remark: Witt’s cancelation theorem can be used to define an equivalence relation on Hermitian spaces and to define a group structure on these equivalence classes. This way, we obtain the Witt group, but we will not discuss it here.
 注：维特的抵消定理可以用来定义厄米特空间上的等价关系，也可以用来定义这些等价类上的群结构。这样，我们就得到了维特集团，但我们不会在这里讨论它。

Witt’s Theorem can be sharpened to isometries in SO(ϕ), but some condition on U is needed.
 威特定理可以在so中锐化为等轴测，但需要在u上有一些条件。

Theorem 28.48. (Witt–Sharpened Version) Let E be a finite-dimensional space equipped with a nondegenerate symmetric bilinear forms ϕ. For any subspace U of E, every linear injective metric map f from U into E extends to an isometry g of E with a prescribed value
 定理28.48。（witt–锐化版本）让e是一个配备非退化对称双线性形式的有限维空间。对于e的任何子空间u，从u到e的每一个线性内射度量图f都扩展到具有规定值的e的等距g。

±1 of det(g) iff dim(U) + dim(rad(U)) < dim(E) = n.
 ±1 of det（g）iff dim（u）+dim（rad（u））<dim（e）=n.

If
 如果

dim(U) + dim(rad(U)) = dim(E) = n,
 dim（u）+dim（rad（u））=dim（e）=n，

and det(f) = −1, then there is no g ∈ SO(ϕ) extending f.
 且Det（f）=-1，则没有g∈so（）延伸f。

Proof. If g1 and g2 are two extensions of f such that det( 1, then h = g1−1 ◦g2 is an isometry such that det(h) = −1, and h leaves every vector of fixed. Conversely, if h is an isometry such that det(h) = −1, and h(u) = u for all u ∈ U, then for any extesnion g1 of f, the map g2 = h◦g1 is another extension of f such that det(g2) = −det(g1). Therefore, we need to show that a map h as above exists.
 证据。如果g1和g2是f的两个扩展，那么det（1，那么h=g1−1 g2是一个等距测量，这样det（h）=−1，h使每个向量保持固定。相反地，如果h是一个等距测量，使得所有u∈u的Det（h）=-1和h（u）=u，那么对于f的任何外轴g1，图g2=h g1是f的另一个延伸，这样Det（g2）=-Det（g1）。因此，我们需要证明上面的地图h是存在的。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

If dim(U)+dim(rad(U)) < dim(E), consider the nondegenerate completion U of U given
 如果dim（u）+dim（rad（u））<dim（e），考虑给定u的非退化完成u

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

by Proposition 28.32. We know that dim(U) = dim(U) + dim(rad(U)) < n, and since U is nondegenerate, we have
 根据第28.32号提案。我们知道dim（u）=dim（u）+dim（rad（u））<n，由于u是非退化的，我们有

,
 ，

with U⊥ = (0)6                . Pick any isometry τ of U⊥ such that det(τ) = −1, and extend it to an
 使用u=（0）6。选取u的任何等距τ，使det（τ）=1，并将其扩展到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image003.gif)

isometry h of E whose restriction to U is the identity.
 e的等距H，其对u的限制是同一性。

If dim(U) + dim(rad(U)) = dim(E) = n, then U = V ⊕⊥ W with V = rad(U) and since
 如果dim（u）+dim（rad（u））=dim（e）=n，则u=v w，其中v=rad（u），自

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

dim(U) = dim(U) + dim(rad(U)) = n, we have
 dim（u）=dim（u）+dim（rad（u））=n，我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

E = U = (V ⊕ V 0) ⊕⊥ W,
 E=U=（V V 0）W，

where V ⊕V 0 = Ar2r = W ⊥ is an Artinian space. Any isometry h of E which is the identity on U and with det(h) = −1 is the identity on W, and thus it must map W ⊥ = Ar2r = V ⊕V 0 into itself, and the restriction h0 of h to Ar2r has det(h0) = −1. However, h0 is the identity on V = rad(U), a totally isotropic subspace of Ar2r of dimension r, and by Proposition 28.42, we have det(h0) = +1, a contradiction.    
 其中v v 0=ar2r=w是一个Artian空间。e的任何等距H是u上的同一性，且具有det（h）=-1，则是w上的同一性，因此它必须将w=ar2r=v v 0映射到自身中，而h对ar2r的限制h0具有det（h0）=-1。然而，h0是v=rad（u）上的恒等式，是r维ar2r的一个完全各向同性子空间，根据命题28.42，我们得到了det（h0）=+1，这是一个矛盾。

It can be shown that the center of O(ϕ) is {id,−id}. For further properties of orthogonal groups, see Grove [83], Jacobson [96], Taylor [169], and Artin [6].
 可以看出，O（_）的中心是ID、−ID。关于正交群的进一步性质，请参见Grove[83]、Jacobson[96]、Taylor[169]和Artin[6]。


 

Part IV
 第四部分

Algebra: PID’s, UFD’s, Noetherian Rings, Tensors,
 代数：pid's，ufd's，noetherian环，张量，

Modules over a PID, Normal Forms
 PID上的模块，正常形式

