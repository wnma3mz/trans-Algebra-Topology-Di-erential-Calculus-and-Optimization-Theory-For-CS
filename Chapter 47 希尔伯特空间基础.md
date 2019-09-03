第四十七章

# 希尔伯特空间基础

第48章中证明的关于实值函数极小值存在的大多数“深层”结果依赖于希尔伯特空间理论的两个基本结果：

(1)    投影引理是希尔伯特空间v的非空闭凸子集的结果。

(2)    Riesz表示定理，它允许我们用V中的向量和V上的内积来表示希尔伯特空间V上的连续线性形式。

在拉格朗日对偶中出现的卡鲁什-库恩-塔克条件的正确性来自于一个版本的farkas–minkowski命题，也来自投影引理。

因此，我们认为回顾希尔伯特空间理论的一些基本结果是必不可少的，尽管在这里讨论的大多数应用中，希尔伯特空间是有限维的。然而，在优化理论中，有许多问题，我们寻求一个函数来最小化某种类型的能量泛函（通常由双线性形式给出），在这种情况下，我们要处理无限维希尔伯特空间，因此有必要开发工具来处理更通用的无限维希尔伯特空间的情形。

## 47.1投影引理，对偶性

假设Hermitian空间定义为kuk=phe，_（u，ui，我们在第13.1节中显示函数），是e上的范数。因此，e是赋范向量空间。ifk k k:e→er也是完整的，这是一个非常有趣的空间。

还记得完整性与柯西序列的收敛性有关。赋范向量空间He，Ukk Ki（关于赋范向量空间和度量的定义，见第36章），是度量D下的度量空间，定义如下：

d（u，v）=kv−space，或lang[108，109]或dixmier[52]）。给定一个度量空间e和度量d，一个序列

一千五百零五

（a n）n≥1的元素an∈e是一个柯西序列iff，对于每>0，有一些n≥1这样

对于所有m，n≥n。

我们说e是完全的，如果每个柯西序列收敛到一个极限（这是唯一的，因为度量空间是hausdorff）。

R或C上的每个有限维向量空间都是完整的。例如，可以通过归纳法证明，给定e的任何基（e1，…，en），线性映射h:cn→e定义为h（（z1，…，zn））=z1e1+······+znen

是同态（使用cn上的sup-norm）。我们还可以利用这样一个事实，即R或C上有限维向量空间上的任何两个范数都是等效的（见第8章，或lang[109]、Dixmier[52]、Schwartz[146]）。

但是，如果e有无穷大的维数，它可能不完整。当厄米空间完成时，有限维厄米空间的一些性质也适用于无限维空间。例如，任何封闭子空间都有一个正交补，特别是有限维子空间有一个正交补。在分析中，完备的埃尔米特空间也起着重要作用。由于希尔伯特首先研究了它们，所以它们被称为希尔伯特空间。

定义47.1.一个（复杂）厄米空间He，i是由_引起的范数k k k下的完全范数向量空间，称为希尔伯特空间。一个真正的欧几里得空间He，i，在由_诱导的k k范数下完成，称为真正的希尔伯特空间。

本节中的所有结果适用于复杂的希尔伯特空间以及真实的希尔伯特空间。我们只陈述复杂案例的所有结果，因为它们也适用于真实案例，而且复杂案例中的证明需要更多的关注。

例47.1。所有可数无穷序列的空间L2，复数的x=（Xi）i~（n），即希尔伯特空间。稍后将显示，图_：l2×l2→c定义如下：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

定义得很好，并且l2是_下的希尔伯特空间。事实上，我们将证明一个更普遍的结果（提案A.3）。

例47.2。光滑函数f[a，b]→c的集合c∞[a，b]是厄米形式下的厄米空间。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

但它不是希尔伯特空间，因为它不完整。可以构造它的完备l2（[a，b]），它是上勒贝格可积函数的空间。

[a，b]。

定理36.63给出了一个事实的快速证明，即任何厄米空间e（带有厄米积H−、−I）都可以嵌入到希尔伯特空间e h中。

希尔伯特空间定理47.1.（e h，给出了赫米特空间h−、−i）和线性映射（e，ω：h−e，→−ie）h（，因此相应地。欧几里得空间），有一个

H

h u，vi=h_（u），（v）ih

对于所有的u，v∈e，和（e）在eh中是稠密的。此外，eh在同构方面是独一无二的。

证据。设（e，b k k eb）为Banach空间，Letp瓒：e→eb为线性等距，给定

根据定理36.63。让kuk=hu、ui和e−hi=可以用normeb表示。如果e是一个实向量空间，我们知道

根据第11.1节，极性方程得出的内积h−

，

如果e是一个复杂的向量空间，我们从13.1节知道，我们有极性方程。

.

根据柯西-施瓦兹不等式，−i:e×e→r）是连续的。但是，它不是均匀连续的，但是我们可以hu，vi≤kukkkvk，地图H−，−i:e×e→c（resp.

h-通过使用极性方程将问题扩展到一个连续的映射来解决这个问题。

由一个正定埃尔米特内积（resp.欧几里得内积）通过连续性，极性方程也包含油墨keb i eh，这表明h−、−i−在eh h−上延伸到h。

延伸H−，−。

备注：我们按照Schwartz[145]中的方法（第二十三章第42节）。定理2）。其他方法见Munkres[127]（第7章第43节）和Bourbaki[27]。

有限维厄米特（和欧几里得）空间最重要的事实之一是它们有正交基。这意味着，在同构之前，每个有限维厄米空间都同构于cn（对于某些n∈n），并且内积由

.

此外，每个子空间w都有一个正交补码w，并且内积

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

归纳出e和e（实际上，e和e）之间的自然对偶性，其中e是e上线性形式的空间。

当e是希尔伯特空间时，e可能是无限维，通常是不可数维。因此，我们不能期望E总是有一个正交基。但是，如果我们修改基的概念，使“希尔伯特基”是一个在e中也很密集的正交族，也就是说，每个v∈e都是希尔伯特基向量的有限组合序列的极限，那么我们就可以恢复有限维的大部分“好”性质。艾尔·赫米特的同事空间。例如，如果（ck=hv，uki/kuukk）k k∈，那么k是希尔伯特基，因为everyv是其傅立叶级数v∈e的“和”，我们可以定义fourierpk∈k ckuk。然而，索引集k的基数可能非常大，因此有必要定义由k索引的一系列向量的可和性意味着什么。我们将在A.1节中进行此操作。结果表明，每个希尔伯特空间都同构于形式为l2（k）的空间，其中l2（k）是示例47.1空间的推广（见定理A.8，通常称为Riesz-Fischer定理）。

我们的第一个目标是证明希尔伯特空间的闭子空间具有正交补。我们还表明，如果我们将e的对偶e0重新定义为e上连续线性映射的空间，则对偶性是成立的。我们的演示与Bourbaki[27]密切相关。我们也受到了鲁丁[136]、朗[108，109]、施瓦茨[146，145]和迪克斯米尔[52]的启发。事实上，我们强烈推荐Dixmier[52]作为一个关于拓扑和分析基础的清晰而简单的文本。我们首先证明了所谓的投影引理。

回想一下，在度量空间e中，e的子集x对于每个收敛序列都是闭的iff

（xn）点xn∈x的极限x=limn→∞xn也属于x。x的闭包x是点xn∈x的收敛序列（xn）的所有极限的集合。显然，x x。我们

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

假设e的子集x在e iff e=x中是稠密的，x的闭包，这意味着每一个a∈e都是点xn∈x的某些序列（xn）的极限，凸集将再次起到至关重要的作用。

首先，我们陈述下面简单的“平行四边形不等式”，其证明留作练习。

提案47.2.如果e是厄米空间，对于任意两个向量u，v∈e，我们有

ku+vk2+ku−vk2=2（kuk2+kvk2）。

从上面我们得到了以下建议：

提案47.3.如果e是厄米空间，给定任意d，δ∈r，使0≤δ<d，设

b=u∈e kuk<d和c=u∈e kuk≤d+δ。

对于任何凸集，如a c−b，我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

Kv−Uk≤√12dδ，

对于所有u，v∈a（见图47.1）。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

图47.1：命题47.3的不等式

证据。因为a是凸的，所以…从形式上写的平行四边形不等式

，

因为δ<d，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

从哪来的

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

Kv−Uk≤√12dδ。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

如果x是度量空间（e，d）的非空子集，对于任何a∈e，回想一下，我们将a到x的距离d（a，x）定义为

d（a，x）=inf d（a，b）。BX

此外，x的直径δ（x）定义为

δ（x）=sup d（a，b）a，b∈x。

可能δ（x）=∞。我们将以下标准的两个事实作为练习（见Dixmier[52]）：

**Proposition 47.4.** *Let E be a metric space.*

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

*(1)*     *For every subset X* ⊆ *E, δ*(*X*) = *δ*(*X*)*.*

*(2)*     *If E is a complete metric space, for every sequence* (*Fn*) *of closed nonempty subsets of E such that Fn*+1 ⊆ *Fn, if* lim*n*→∞ *δ*(*Fn*) = 0*, then* ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif) *consists of a single point.*

We are now ready to prove the crucial projection lemma.

**Proposition 47.5.** *(Projection lemma) Let E be a Hilbert space.*

*(1)*     *vectorFor any nonempty convex and closed subsetpX*(*u*) ∈ *X such that  X* ⊆ *E, for any u* ∈ *E, there is a unique*

k*u* − *pX*(*u*)k = *v*inf∈*X* k*u* − *v*k = *d*(*u,X*)*.*

*See Figure 47.2.*

*(2)*     *The vector pX*(*u*) *is the unique vector w* ∈ *E satisfying the following property (see Figure 47.3):*

​                                                     *w* ∈ *X     and*       <h*u* − *w,z* − *w*i ≤ 0        *for all z* ∈ *X.*                          (∗)

*(3)*     *If X is a nonempty closed subspace of E then the vector pX*(*u*) *is the unique vector w* ∈ *E satisfying the following property:*

​                                                            *w* ∈ *X     and*      h*u* − *w,z*i = 0       *for all z* ∈ *X.*                             (∗∗)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

Figure 47.2: Let *X* be the solid pink ellipsoid. The projection of the purple point *u* onto *X* is the magenta point *pX*(*u*).

*Proof.*follows: for every(1) Let *d* =*n*inf≥ 1*v*∈,*X* k*u* − *v*k = *d*(*u,X*). We define a sequence *Xn* of subsets of *X* as

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image019.gif)*.*

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image020.gif)

Figure 47.3: Inequality of Proposition 47.5

It is immediately verified that each *Xn* is nonempty (by definition of *d*), convex, and that *Xn*+1 ⊆ *Xn*. Also, by Proposition 47.3, we have

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image021.gif)sup{k*w* − *v*k | *v,w* ∈ *Xn*} ≤ p12*d/n,*

and thus, T*n*≥1 *Xn* contains at most one point. We will prove that T*n*≥1 *Xn* contains exactly one point, namely, *pX*(*u*). For this, define a sequence (*wn*)*n*≥1 by picking some *wn* ∈ *Xn* for every *n* ≥ 1. We claim that (*wn*)*n*≥1 is a Cauchy sequence. Given any  *>* 0, if we pick *N* such that

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image023.gif)*,*

since (*Xn*)*n*≥1 is a monotonic decreasing sequence, which means that *Xn*+1 ⊆ *Xn* for all *n* ≥ 1, for all *m,n* ≥ *N*, we have

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image025.gif)

as desired. Since *E* is complete, the sequence (*wn*)*n*≥1 has a limit *w*, and since *wn* ∈ *X* and *X* is closed, we must have *w* ∈ *X*. Also observe that

k*u* − *w*k ≤ k*u* − *w**n*k + k*w**n* − *w*k*,*

and since *w* is the limit of (*wn*)*n*≥1 and

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image027.gif)*,*

given any  *>* 0, there is some *n* large enough so that

​                                                                       ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image029.gif)    and    ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image031.gif)*,*

and thus

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image033.gif)

Since the above holds for everyT  *>* 0, we have k*zu*∈− *Xw*ksuch that= *d*. Thus,k*uww*−, which we denote as∈*z*k*X**n*=for all*d*(*u,Xn*) =≥ 1*d*, which proves that *n*≥1 *X**n* = {*w*}*z*. Now, any= *w*, proving the uniqueness of also belongs to every *X**n*, and thus *pX*(*u*). See Figure 47.4.

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image036.gif)

Figure 47.4: Let *X* be the solid pink ellipsoid with *pX*(*u*) = *w* at its apex. Each *Xn* is the intersection of *X* and a solid sphere centered at *u* with radius *d* + 1*/n*. These intersections are the colored “caps” of Figure ii. The Cauchy sequence (*wn*)*n*≥1 is obtained by selecting a point in each colored *Xn*.

(2) Let *z* ∈ *X*. Since *X* is convex, *w* = (1 − *λ*)*p**X*(*u*) + *λz* ∈ *X* for every *λ*, 0 ≤ *λ* ≤ 1. Then, we have

k*u* − *w*k ≥ k*u* − *p**X*(*u*)k

for all *λ*, 0 ≤ *λ* ≤ 1, and since

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image038.gif)*,*

for all *λ*, 0 *< λ* ≤ 1, we get

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image040.gif)*,*

and since this holds for every *λ*, 0 *< λ* ≤ 1 and

k*u* − *w*k ≥ k*u* − *p**X*(*u*)k*,*

we have

<h*u* − *pX*(*u*)*,z* − *pX*(*u*)i ≤ 0*.*

相反，假设w∈x满足条件

<hu−w，z−wi≤0

对于所有z∈x，对于所有z∈x，我们有ku−zk2=ku−wk2+kz−wk2−2<hu−w，z−wi≥ku−wk2，

这意味着ku-wk=d（u，x）=d，从（1）开始，w=px（u）。

（3）如果x是e和w∈x的子空间，当z的范围超过x时，向量z−w也在x的整个范围内，那么条件（）等于

对于所有z∈x.（1），w∈x and<hu−w，zi≤0

因为x是一个子空间，如果z∈x，那么−z∈x，这意味着（1）等于

对于所有z∈x.（2），w∈x and<hu−w，zi=0

最后，因为x是一个子空间，如果z∈x，那么iz∈x，这意味着

0=<hu−w，i zi=-i=hu−w，zi，

所以=hu−w，zi=0，但是由于我们也有<hu−w，zi=0，我们看到（2）等于

W∈X和Hu−W，Z=0代表所有Z∈X，（）

如要求。

矢量px（u）被称为u对x的投影，地图px:e→x被称为e对x的投影。在真实希尔伯特空间中，有一个直观的几何解释。

hu-px（u），z-px（u）i≤0

对于所有z∈x，如果我们将条件重述为

hu−px（u），px（u）−zi≥0

对于所有z∈xpx，这表示（u）和之间的角度测量的绝对值至多为π/2。见图47.5。这是有意义的，因为向量u−必须在与x的“切线空间”相反的一侧。

x是凸的，点在px（u）中，与u-px（u）正交。当然，这只是一个直观的描述，因为切线空间的概念还没有被定义！

正交Toif x是x的一个封闭子空间，在e的意义上，那么条件（u−px）表示向量z∈ux−。Px（u）是

（u）与每个向量正交，图px:e→x是连续的，如下所示。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

图47.5：假设x是蓝色的固体冰淇淋锥。黑色向量u−px（u）和紫色向量px（u）−z之间的锐角小于π/2。

提案47.6.让我们成为希尔伯特空间。对于任何非空凸和闭子集x e，映射px:e→x是连续的。实际上，px满足lipschitz条件

k px（v）−px（u）k≤kv−uk表示所有u，v∈e。

证据。对于任意两个向量u，v∈e，设x=px（u）−u，y=px（v）−px（u），z=v−px（v）。

很明显，（如图47.6所示）

V−U=X+Y+Z，

从第47.5（2）号提案，我们也有

<hx，yi≥0且<hz，yi≥0，

我们从中得到

kv−uk2==kkxxy++zy+2+zk2y=k2k+2x+<zh+x，y2y.ki2+2<hz，yi k

≥k k2=k px（v）−px（u）k

然而，k px（v）−px（u）k≤kv−uk显然意味着px是连续的。

我们现在可以证明下列重要命题。

提案47.7。让我们成为希尔伯特空间。

*(1)*     对于任何封闭子空间v e，我们有e=v v，并且图pv:e→v是线性和连续的。

*(2)*     对于任何u∈e，投影pv（u）是唯一的向量w∈e，因此

对于所有z∈v，w∈v和hu−w，zi=0。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

图47.6：设x为实心金椭球体。矢量v−u是三个绿色矢量的总和，每个绿色矢量由适当的投影确定。

证据。（1）首先，我们证明u−pvλ（u∈）c∈，并且sincev对于所有的uv∈都是凸的和非空的（自ite以来）。对于任何v∈v，因为v是一个子空间，z=pv（u）+λv∈v代表所有

是一个子空间），通过假设，通过命题47.5（2），我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

<（λhu−pv（u），vi）=<（hu−pv（u），λvi=<hu−pv（u），z−pv（u）i≤0表示所有的λ∈c。特别是，上述公式适用于λ=hu−pv（u），vi，得出

| hu−pv（u），vi≤0，

因此，hu−up=v（puv）（，vu）+i=0u−。见图47.7。因此，对于每一个v v=u 0e，我们有ee==uvv−+pvvv（u.在另一个上。）的pv（u）对于所有u e。因为−i是正定的，h and，因为h−

我们已经在命题47.6中证明了pv:e→v是连续的。另外，由于pv（λu+μv）-（λpv（u）+μpv（v））=pv（λu+μv）-（λu+μv）+λ（u-pv（u））+μ（v-pv（v）），

对于所有u，v∈e，由于左边项属于v，我们有v，从我们刚才所展示的，右边项属于

pv（λu+μv）-（λpv（u）+μpv（v））=0，

表明pv是线性的。

（2）这从（1）基本上是显而易见的。我们在（1）中证明了u−pv（u）∈v，这正是条件

hu−pv（u），zi=0

对于所有z∈v。相反，如果w∈v满足条件hu−w，zi=0

对于所有z∈v，由于w∈v，每个向量z∈v的形式是y−w，其中y=z+w∈v，因此，我们有

hu−w，y−wi=0

对于所有y∈v，这意味着命题47.5（2）的条件：

<hu−w，y−wi≤0

对于所有y∈v。根据命题47.5，w=pv（u）是u对v的投影。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

图47.7：假设v是粉色平面。向量u−pv（u）垂直于任意v∈v。

注：f-pv:e e的凸子集，那么→v是线性的，那么pv:e→v是线性的，iffv是v的子空间，是e的子空间。因此，ife.v是一个封闭的

让我们举例说明47.7号命题对以下“最小二乘”问题的威力。

给定一个实系统m×n-矩阵a和一些向量b∈rm，我们要求解线性

AX＝B

将欧几里得Normin最小化为最小二乘意义，这意味着我们希望找到误差ax−b的一些解kax−bk。实际上，不清楚x∈rn这个问题是否有解，但确实有解！问题可以重述如下：是否有

x∈rn，使kax−bk=yinf∈rn kay−bk，

或者等价地，是否有一些z∈im（a）这样

kz−bk=d（b，im（a）），

式中im（im（a）=ay∈rm ry m∈，由于我们是在有限维上，命题47.7 tellsrn，a.自

a）是我们的封闭子空间，存在一个唯一的z∈im（a），这样

kz−bk=yinf∈rn kay−bk，

因此，问题自x∈rn开始就一直有一个解，这样ax=z（由im（az）的定义）就∈。注意这样的anim（az），并且由于至少有一些∈im（a）是x的解不一定是

独一无二。此外，命题47.7也告诉我们

hz−b，wi=0，对于所有w∈im（a），

或者等价地，x∈rn是

Hax−b，Ayi=0表示所有y∈rn，

相当于

Ha>（ax−b），Yi=0表示所有y∈rn，

因此，由于内积是正定的，到a>（ax−b）=0，即，

a>ax=a>b。

所以，原始最小二乘问题的解就是所谓的正态方程的解。

a>ax=a>b，

由高斯和勒让德发现于1800年左右。我们还证明了正态方程总是有解的。

在计算上，最好不要直接求解正态方程，而是使用QR分解（应用于a）或SVD分解（以伪逆的形式）等方法。稍后我们将回到这一点。

C，零空间是47.7命题的另一个推论，对于任何连续的非零线性映射h:e→

h=kerh=u∈e h（u）=0=h−1（0）

是一个封闭超平面，这表明定义了H的对偶空间，因此，H是维度1的一个子空间，E是所有连续映射的集合H:ee=→hc.h。

备注：如果h:e→hc=是一个线性映射，iskerh在e中是稠密的！因此，如果不连续，则可以将超平面简化为

{ 0 }。这违背了我们对RN（或CN）中超平面是什么的直觉，并警告我们在处理无限维时不要太相信我们的“物理”直觉。作为一个

结果，mapv∈e）是连续的（内积是连续的[：e→e，在第13.2节中介绍（见定义47.2之后）。u 7→hu，vi（对于下面的一些固定矢量）不是可射的，因为形式的线性形式

我们现在证明，通过将希尔伯特空间的对偶空间重新定义为E上的连续线性形式集，我们恢复了定理13.6。

定义47.2.对于希尔伯特空间e，我们将e的对偶空间e0定义为所有连续线性形式算符、有界线性泛函或简单的算符或泛函的向量空间：e→c。e0中的映射也被称为。有界线性

如第13.2节所述，对于所有u，v∈e，我们定义的映射如下：

，

和

.

事实上，由于内积H−、−I是连续的，因此很明显，v代替了。是连续的和线性的，所以。为了简化符号，我们将定理13.6推广到希尔伯特空间，如下所示。

提案47.8。（Riesz表示定理）让e是希尔伯特空间。然后，地图

[：e→e0定义如下：

[（v）=_v，

是半线性的、连续的和双射的。此外，对于任何连续线性映射，如果u∈e是唯一的向量，那么

ψ（v）=hv，所有v∈e的ui，

那么我们有kψk=kuk，其中

.

证据。证明与定理13.6的证明基本相同，只是

对于h∈e0的任何非空线性算子子空间的可射性，需要参数，超平面[：he→是维1的子空间，因此e0，sincehe=可能不是有限维。kerh=h−1（0）是闭合的。

# 根据47.7号提案，

E=H H。然后，选取任意一个非零向量w∈h，观察h也是线性算子的核，其中

_w（u）=hu，wi，

因此，由于定义同一超平面的任何两个非零线性形式都必须成比例，所以有一些非零标度[：e→e0是可射的。λ∈c，使得h=λ_w.但是，h=_λw，证明

通过柯西-施瓦兹不平等

|ψ（v）=hv，ui≤kvkkuk，

所以根据kψk的定义，我们得到kψk≤kuk。

显然，如果u=0，那么假设u 6=0。我们有

kuk2=hu，ui=ψ（u）≤kψkkuk，

其产生kuk≤kψk，因此kψk=kuk，如权利要求所述。

命题47.8被称为Riesz表示定理或“小Riesz定理”，它表明希尔伯特空间上的内积引起了自然的半线性同构。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

在e和它的对偶e0之间（相当于e和e0之间的线性同构）。这种同构是一种同构（它保留了规范）。

注：许多有关量子力学的书籍都使用所谓的狄拉克符号来表示希尔伯特空间E中的物体，以及双空间e0中的算符。在狄拉克记号中，E的一个元素表示为Xi，E0的一个元素表示为HT。标量乘积表示为Ht*.Xi。这使用了e和e0之间的同构，只是假定内积在左边是半线性的，而不是在右边。

命题47.8允许我们定义一个线性映射的伴随，如赫米特案例（见命题13.8）。实际上，我们可以证明一个更一般的结果，这是在优化理论中使用的。

36.59如果立即适应于证明：e×e→c是赋范向量空间上的一个倍线性映射（如果存在一些常数k k，则_是连续的），则命题k≥0，以便

|⑨（u，v）≤k kukkkvk表示所有u，v∈e。

因此，我们根据第36.42条的定义定义k

k_k=sup（x，y）kxk≤1，kyk≤1，x，y∈e。

命题47.9.e→c，对于每一个连续的半线性映射，都有一个给定希尔伯特空间e的唯一的连续线性映射，因此，_:e×

⑨（u，v）=hu，f⑨（v）i表示所有u，v∈e。

我们也有k f_k=k_k。如果_是厄米提，那么f_是自伴的，即

hu，f_（v）i=hf_（u），vi表示所有u，v∈e。

证据。该证明改编自Rudin[137]（定理12.8）。为了定义函数f，我们进行如下操作。对于任何固定的v∈e，定义线性映射

所有u∈e的v（u）=a（u，v）。

由于_是连续的，所以根据命题47.8，在e中有一个唯一的向量，我们表示f_（v），这样

_v（u）=hu，f（v）i表示所有u∈e，

和kf_（v）k=k_vk。让我们检查地图v 7→f（v）是线性的。

我们有

⑨（u，v1+v2）＝（u，v1）＋（u，v2）为添加剂

=hu，f_（v1）i+hu，f（v2）i，根据f_的定义

=hu，f_（v1）+f（v2）i h−，−i是添加剂

对于所有u∈e，并且由于f_（v1+v2）是唯一的向量，因此，对于所有u∈e，我们必须具有（u，v1+v2）=hu，f（v1+v2）i。

f_（v1+v2）=f（v1）+f_（v2）。

对于任何λ∈c，我们有

⑨（u，λv）=λ（u，v）_为倍线性

=λhu，f_（v）i根据f_的定义

=hu，λf（v）i h−，−i为倍线性

对于所有u∈e，由于f（λv）是唯一的向量，因此，对于所有u∈e，我们必须有f（λv）=λf（v）。

因此f_是线性的。

那么根据k的定义，我们有

| v（u）=_（u，v）≤k_kkukkvk，

说明k_vk≤k_kkkvk。由于kf_（v）k=k_vk，我们有

Kf_（v）k≤k_kkkvk，

这表明f_是连续的，kf_k≤k_k。但是根据柯西-施瓦兹不等式，我们也有

|⑨（u，v）=hu，f（v）i≤kukkf_（v）k≤kukkff_kkkvk，

因此k_k≤kf_k，因此kf_k=k_k。

如果直径为Hermitian，直径（v，u）=直径（u，v），那么

hf_（u），v i=hv，f_（u）i=_（v，u）=（u，v）=hu，f（v）i，

这表明f_是自伴的。

提案47.10。给定希尔伯特空间e，对于每个连续线性映射f:e→e，都有一个唯一的连续线性映射f：e→e，这样

hf（u），v i=hu，f（v）i表示所有u，v∈e，

我们有kf k=kfk。地图f被称为f的伴随。

证据。证据改编自鲁丁[137]（第12.9节）。由柯西-施瓦兹不等式

| HX，Yi≤KXKKYK

我们看到E×E上的倍线性映射（x，y）7→hx，yi是连续的。设_：e×e→c为由下式给出的倍线性图。

⑨（u，v）=hf（u），vi表示所有u，v∈e。

因为f是连续的，而内积h−、−fi是连续的，所以这是一个连续的图。：e→e这样

根据命题47.9，有一个唯一的线性映射

hf（u），v i=_（u，v）=hu，f（v）i表示所有u，v∈e，

Kf k=k_k.

我们也可以证明k_k=kfk。首先，根据k的定义，我们有

k_k=sup _（x，y）kxk≤1，kyk≤1

=sup hf（x），yi kxk≤1，kyk≤1

≤SUP K（F（X）KKYK KXK≤1，KYK≤1

≤sup k（f（x）k kxk≤1=kfk。

在另一个方向

k f（x）k2=hf（x），f（x）i=_（x，f（x））≤k_kkkxkkff（x）k，

如果f（x）6=0fwe getk≤k_kkkf。因此我们有（x）k≤k_kkkxk。如果f（x）=0，这个不等式就无关紧要了，因此我们得出结论，k k_k=kfk，

如权利要求，因此kf k=k_k=kfk。

很容易证明伴随满足以下性质：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

也可以证明kf fk=kkk2（见Rudin[137]第12.9节）。

在Hermitian的例子中，给定两个Hilbert空间e和f，上面的结果可以用来证明对于任何线性映射f:e→f，都有一个唯一的线性映射f：f→e，这样

hf（u），vi2=hu，f（v）i1

对于所有u∈e和所有v∈f，线性映射f也被称为f的伴随。

## 47.2希尔伯特空间的Farkas–Minkowski Lemma

在这一节中，（v，h−，−i）被假定为一个真实的希尔伯特空间。投影引理可以用来在希尔伯特空间中展示一个有趣的farkas-minkowski引理。

给定一个有限向量序列（a1，…，am）的ai∈v，设c为多面体锥

C=锥形（.

对于任何向量b∈v，farkas-minkowski引理给出了检验b∈c是否成立的准则。

V，其中V是任何

向量空间可能是无限维的，因为重要的事实是数字是闭合的。对证明的仔细检验表明，它通过了IFIN命题43.2，我们证明了每一个具有ai∈rn的多面体锥（a1，…，aai∈m）。

这些向量中的m是有限的，而不是它们的维数。

希尔伯特空间定理47.11.对于任何有限向量序列（希尔伯特空间中的farkas–minkowski引理），让（a1，…，am）和（iv，h−v，−，ifi）实现

多面体控制因子u∈v这样的that=cone（a1，…，am），对于任何向量b∈v，我们都有b/∈c iff存在a

hai，ui≥0 i=1，…，m，hb，ui<0.

等价地，b∈c iff表示所有u∈v，

如果hai，ui≥0 i=1，…，m，则hb，ui≥0。


 

47.2。希尔伯特空间中的法卡斯-明可夫斯基引理

证据。我们遵循Ciarlet[41]（第9章，定理9.1.1）。我们已经在命题43.2中确定多面体锥c=锥（a1，…，am）是闭合的。接下来，我们声明如下：

向量这样的结论：如果c是希尔伯特空间b/∈c的一个非空的、闭的、凸的子集，那么就存在一些u∈v和无穷多个scalarsv，而bα∈vris则是这样的：

hv，ui>α，每v∈c

hb，ui<α。

一些唯一性使用投影引理（命题47.5），它表示sincec=pc（b）∈c，这样b/∈c存在

kb−ck=vinf∈c kb−vk>0 hb−c，v−ci≤0表示所有v∈c，

或同等

kb−ck=vinf∈c kb−vk>0 hv−c，c−bi≥0表示所有v∈c。

因此，我们有hv，c−bi≥hc，c−bi>hb，c−bi，

如果我们选择u=c−b和任何α，

hc，c−bi>α>hb，c−bi，

索赔已得到满足。

我们现在证明了法卡—明可夫斯基引理。A当b/∈c。由于c是非空的、凸的、封闭的，根据这个说法，有一些u∈v和一些α∈r这样

hv，ui>α，每v∈c

hb，ui<α。

但是c是一个多面体锥，包含0，所以我们必须有α<0。那么对于每一个v∈c，既然c是一个多面体锥，如果v∈c，那么λv∈c对于所有的λ>0，那么由上而定

对于每个λ>0，

这意味着hv，ui≥0。

由于i=1，…，m的ai∈c，我们证明了

hai，ui≥0 i=1，…，m和hb，ui<α<0，

这证明了法卡斯伦玛，1524，第47章。希尔伯特空间基础

观察在定理47.11的证明过程中所建立的断言，表明方程hv的仿射超平面hu，α，ui=α对于所有v∈v严格地分离c和b。