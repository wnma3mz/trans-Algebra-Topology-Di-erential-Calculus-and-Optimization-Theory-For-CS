第十七章

# 边值问题的变分近似；有限元法简介

## 17.1一维问题：梁弯曲

如图所示，考虑在0和1端部支撑的单位长度梁，在力P的作用下沿其轴拉伸，并承受每个构件dx的横向荷载f（x）dx。

17.1。

0 DX 1

-P P P

f（x）dx

图17.1：梁的垂直偏转

摘要x处的弯矩u（x）是形式的边界问题（bp）的解。

−u00（x）+c（x）u（x）=f（x），0<x<1 u（0）=αu（1）=β，

五百五十七

式中，c（x）=p/（e i（x）），其中e是制造光束的材料的杨氏模量，i（x）是光束横截面在abcissa x处的主惯性矩，α=β=0。对于这个问题，我们可以假设c（x）≥0代表所有x∈[0,1]。

注：梁的垂向挠度w（x）和弯矩u（x）由以下公式得出：

.

如果我们寻求一个解u∈c2（[0,1]），也就是说，一个函数的第一和第二导数存在且是连续的，那么可以证明这个问题有一个唯一的解（假设c和f是[0,1]上的连续函数）。

除极少数情况外，这个问题没有封闭形式的解，所以我们只能求解的近似值。

一种方法是使用有限差分法，在这里我们离散问题并用差分代替导数。另一种方法是使用变分法。在这种方法中，我们遵循一条有些令人惊讶的路径，通过使用基于部分集成的技巧，我们想出了问题的所谓“弱公式”！

首先，让我们观察一下，我们总是可以假设α=β=0，通过寻找形式U（x）-（α（1−x）+βx的溶液。当我们按部件进行集成时，这是至关重要的。有很多微妙的数学细节，使遵循严格，但在这里，我们将采取“放松”的方法。

首先，我们需要指定“弱解”的空间，这是连续函数f在[0,1]上的向量空间v，其中f（0）=f（1）=0，并且在[0,1]上是分段连续可微的。这意味着X0，…，Xn＋1的X0＝0和Xn＋1＝1的有限数目的点，使得F0（Xi）对于i＝1，…，n是未定义的，但在每个区间（Xi，Xi＋1）上定义或连续地为i＝0，…，N.，空间V变成A。

内积下的欧氏向量空间

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

对于所有f，g∈v。相关规范是

.

假设u是原始边界问题（bp）的解，那么

−U00（X）+C（X）U（X）=F（X），0<X<1 U（0）=0 U（1）=0。


 

将微分方程乘以任意检验函数v∈v，得到

−U00（X）V（X）+C（X）U（X）V（X）=F（X）V（X），（）

积分这个方程！我们得到

Z 1 Z 1 Z 1

−U00（X）V（X）Dx+C（X）U（X）V（X）Dx=F（X）V（X）Dx。（†）

0 0 0

现在，技巧是在第一个术语中使用部分集成。回想一下

（U0V）0=U00V+U0V0，

要注意不连续，写

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

我们使用分部集成

ZXI + 1 ZXI + 1 ZXI + 1

u00（x）v（x）dx=（u0（x）v（x））0dx−u0（x）v0（x）dx

奚溪

ZXI＋1

=[u0（x）v（x）]xx==xxii+1 u0（x）v0（x）dx

奚

ZXI＋1

= U0（X+ 1）V（Xi＋1）U0（Xi）V（Xi）U0（x）V0（x）dx。

奚

接下来是

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

然而，测试函数v满足边界条件v（0）=v（1）=0（回想v∈v），因此我们得到

z 1 z 1 u00（x）v（x）dx=−u0（x）v0（x）dx.

0 0

因此，方程式（†）变为

Z 1 Z 1 Z 1

u0（x）v0（x）dx+c（x）u（x）v（x）dx=f（x）v（x）dx，

0 0 0

或

Z 1 Z 1

| 网络错误 | 网络错误 |
| -------- | -------- |
|          |          |

对于所有u，v∈v，

线性形式由

对于所有的v∈v。

然后，）变成a（u，v）=fe（v），对于所有v∈v。

我们还介绍了能量函数j，由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

| 网络错误   网络错误   网络错误 |          |
| ------------------------------ | -------- |
| 网络错误   网络错误            | 网络错误 |

对于所有u，v∈v，

和

对于所有的v∈v。

（2）如果c（x）≥0对于所有x∈[0,1]，那么函数u∈v是（wf）iff u的解。

最小化j（v），即j（u）=inf j（v），

VⅤ

具有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

此外，u是独一无二的。

证据。我们已经证明了（1）。

为了证明（2），首先我们证明

kvk2v≤2a（v，v），对于所有v∈v，对于这个，它足以证明

对于所有的v∈v，然而，对于函数，对于每一个x∈[0,1]，我们有

如此

，

自从

接下来，很容易检查

，对于所有u，v∈v。

那么，如果u是（wf）的解，我们可以推导出

0表示所有v∈v。

因为a（u，v）−fe（v）=0对于所有v∈v。因此，J达到了U的最小值。

）对于所有θ∈r，

因此，如果j满足u的最小值，那么a（u，v）=f（v），这意味着u是（wf）的解。

最后，假设c（x）≥0，我们认为如果v∈v和v 6=0，那么a（v，v）>0。这是因为如果a（v，v）=0，因为

kvk2v≤2a（v，v），对于所有v∈v，

kvkv=0，即v=0。那么，如果v 6=0，从

）对于所有v∈v

我们看到j（u+v）>j（u），所以最小u是唯一定理17.1表明边界问题（bp）的每一个解u都是方程（wf）的一个解（实际上是唯一的）。

该方程被称为弱形式或与边界问题有关的变分方程。推导这些方程的想法是由里兹和伽辽金提出的。

现在，自然的问题是变分方程（wf）是否有一个解，如果存在这个解，它是否也是边界问题的解（它必须属于c2（[0,1]），这是不明显的）。那么，（bp）和（wf）是等效的。

一些奇特的分析工具可以用来证明这些断言。第一个困难是向量空间v不是正确的解空间，因为为了使变分问题有一个解，它必须是完整的。所以，我们必须构造一个向量空间v的完备。这可以做到，我们得到了索波列夫空间1）。然后，也可以解决“弱解”的规律性问题。

我们不会担心这一切的。相反，让我们找到问题（WF）的近似值。我们不使用无限维向量空间v，而是考虑v的有限维子空间v a（与dim（va）=n），并考虑离散问题：找到一个函数u（a）∈va，这样

a（u（a），v）=fe（v），对于所有v∈va（dwf）

由于va是有限维的（n维的），让我们选取va中的函数（w1，…，wn）的基，这样每个函数u∈va都可以写成

u=u1w1+·····+unwn。

然后，方程（dwf）保持iff

a（u，wj）=fe（wj），j=1，…，n，

通过对u1w1+···································

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

因为双线性形式A是对称正定的，因此矩阵（A（wi，wj））是对称正定的，因此是可逆的。因此，（dwf）有一个线性系统给出的解！

从实际的角度来看，我们必须计算积分

和

但是，如果基函数足够简单，可以“手工”完成，否则必须使用数值积分方法，但也有一些好的方法。

我们还可以注意到定理17.1的证明也表明（dwf）的唯一解是j在v a中所有函数上的唯一极小值，也可以将近似解u（a）∈va与精确解u∈v进行比较。

定理17.2。假设c（x）≥0，所有x∈[0,1]。对于v的每个有限维子空间va（dim（va）=n），对于va的每个基（w1，…，wn），以下属性适用：

*(1)*     有一个唯一的函数u（a）∈va，这样

a（u（a），v）=fe（v），对于所有v∈va，（dwf）

如果u（a）=u1w1+·····+unwn，那么u=（u1，…，un）是线性系统的解。

au=b，（）

当a=（a i j）=（a（wi，wj））和bj=fe（wj），1≤i，j≤n时，矩阵a=（aij）是对称正定的。

*(2)*     （dwf）的唯一解u（a）∈va是j在va上的唯一极小值，即j（u（a））=inf j（v），

VA VA

*(3)*     有一个独立于v a和（wf）的唯一解u∈v的常数c，这样

.

我们证明了（1）和（2），但我们将省略（3）的证明，可以在Ciarlet中找到。

〔41〕。

现在让我们来举例说明在实践中使用的子空间va。它们通常由分段多项式函数组成。

选择一个整数n为1，并将[0,1]细分成n＋1区间[Xi，Xi＋1 ]，其中

.

我们将利用以下事实：每一个2 m+1（m≥0）的多项式p（x）完全由其值以及它在两个不同点α，β∈r上的第一个m导数的值决定。

有多种方法可以证明这一点。一种方法是使用伯恩斯坦基，因为多项式的kth导数是由一个公式根据其控制点给出的。例如，对于m=1，每个三次多项式都可以写成

P（x）=（1−x）3 b0+3（1−x）2xb1+3（1−x）x2 b2+x3 b3，

用b0，b1，b2，b3∈r表示

.

给定p（0）和p（1），我们确定b0和b3，从p 0（0）和p0（1），我们确定b1和b2。

一般来说，对于m次多项式，写为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

在伯恩斯坦基础上（））与

，

可以证明，p在零点的kth导数由下式给出：

，

对于p（k）（1），有一个类似的公式。

实际上，我们需要使用多项式的伯恩斯坦基bkm[r，s]，其中

，

当r<s时，在这种情况下

，

与p（k）（1）的公式相似。在我们的例子中，我们设置r = XI，s = XI + 1。现在，如果2M+2值

P（0），P（1）（0），…，P（m）（0），P（1），P（1）（1），…，P（m）（1）

给出了唯一确定2 m+2控制点b0，…，b2 m+1的三角形系统。

回想一下，cm（[0,1]）表示[0,1]上的cm函数集f，这意味着f，f（1），…，f（m）存在于[0,1]上是连续的。

我们将向量空间vnm定义为包含所有函数f的cm（[0,1]）的子空间，这样

\1.    F（0）=F（1）=0。

\2.    F对[Xi，Xi＋1 ]的限制是一个2m＋1的多项式，对于i＝0，…，N.

观察vn0中的函数是分段仿射函数f，f（0）=f（1）=0；图17.2显示了一个例子。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

图17.2：分段仿射函数

这个空间具有维数n，并且基由“帽子函数”Wi组成，其中Wi图的两个非平坦部分是从（Xi，1，0）到（XI，1）的线段，并且从（XI，1）到（XI+1，0），对于i＝1，…，n，见图17.3。

基函数wi的支持度很小，这是很好的，因为在计算给出（wi，wj）的积分时，我们发现我们得到了一个三对角矩阵。它们还具有每个函数v∈vn0在基（wi）上都有以下表达式的优良性质：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)*.*

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image018.gif)

Figure 17.3: A basis “hat function”

In general, it it not hard to see that *VNm* has dimension *mN* + 2(*m* − 1).

Going back to our problem (the bending of a beam), assuming that *c* and *f* are constant functions, it is not hard to show that the linear system (∗) becomes

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image020.gif) *.*

We can also find a basis of 2*N* + 2 cubic functions for *VN*1 consisting of functions with small support. This basis consists of the *N* functions *wi*0 and of the *N* + 2 functions *wi*1 uniquely determined by the following conditions:

​                                                         *wi*0(*xj*) = *δij,*          1 ≤ *j* ≤ *N,* 1 ≤ *i* ≤ *N*

(*wi*0)0(*xj*) = 0*,*    0 ≤ *j* ≤ *N* + 1*,* 1 ≤ *i* ≤ *N wi*1(*xj*) = 0*,*  1 ≤ *j* ≤ *N,* 0 ≤ *i* ≤ *N* + 1

​                                                   (*wi*1)0(*xj*) = *δij,*          0 ≤ *j* ≤ *N* + 1*,* 0 ≤ *i* ≤ *N* + 1

with *δij* = 1 iff *i* = *j* and *δij* = 0 if *i* =6                *j*. Some of these functions are displayed in Figure

17.4. The function *wi*0 is given explicitly by

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image022.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image024.gif)

for *i* = 1*,...,N*. The function *wj*1 is given explicitly by

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image026.gif)

and

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image028.gif)

for *j* = 0*,...,N* + 1. Furthermore, for every function *v* ∈ *VN*1, we have

*N N*+1 *v*(*x*) = X*v*(*ih*)*wi*0(*x*) + X *v*0*jih*)*wj*1(*x*)*,       x* ∈ [0*,*1]*.*

​                                                              *i*=1                                                    *j*=0

If we order these basis functions as

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image030.gif)*,*

we find that if *c* = 0, the matrix *A* of the system (∗) is tridiagonal by blocks, where the blocks are 2 × 2, 2 × 1, or 1 × 2 matrices, and with single entries in the top left and bottom right corner. A different order of the basis vectors would mess up the tridiagonal block structure of *A*. We leave the details as an exercise.

Let us now take a quick look at a two-dimensional problem, the bending of an elastic membrane.

w
 W

Figure 17.4: The basis functions wi0 and wj1
 图17.4：基础函数wi0和wj1

# 17.2 A Two-Dimensional Problem: An Elastic Membrane  17.2二维问题：弹性膜

Consider an elastic membrane attached to a round contour whose projection on the (x1,x2)plane is the boundary Γ of an open, connected, bounded region Ω in the (x1,x2)-plane, as illustrated in Figure 17.5. In other words, we view the membrane as a surface consisting of the set of points (x,z) given by an equation of the form
 假设一个弹性膜附着在一个圆形轮廓上，其在（x1，x2）平面上的投影是（x1，x2）平面中开放、连接、有界区域Ω的边界_，如图17.5所示。换句话说，我们把膜看作是一个表面，由一个形式方程给出的一组点（x，z）组成。

z = u(x),
 Z=U（X）、

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

with x = (x1,x2) ∈ Ω, where u: Ω → R is some sufficiently regular function, and we think of u(x) as the vertical displacement of this membrane.
 对于x=（x1，x2）∈Ω，其中u:Ω→r是一些足够规则的函数，我们认为u（x）是膜的垂直位移。

We assume that this membrane is under the action of a vertical force τf(x)dx per surface element in the horizontal plane (where τ is the tension of the membrane). The problem is
 我们假设该膜在水平面上每个表面单元的垂直力τf（x）dx的作用下（其中τ是膜的张力）。问题是

## w17.2. A TWO-DIMENSIONAL PROBLEM: AN ELASTIC MEMBRANE  图17.2。二维问题：弹性膜

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

Figure 17.5: An elastic membrane
 图17.5：弹性膜

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image003.gif)

to find the vertical displacement u as a function of x, for x ∈ Ω. It can be shown (under some assumptions on Ω, Γ, and f), that u(x) is given by a PDE with boundary condition, of the form
 求垂直位移u与x的函数关系，对于x∈Ω。可以证明（在一些关于Ω、_和f的假设下），u（x）由具有边界条件的PDE给出，形式为

| −∆u(x) =   f(x),    网络错误 | x ∈ Ω    网络错误  |
| ---------------------------- | ------------------ |
| u(x) = g(x),    网络错误     | x ∈ Γ,    网络错误 |

where g: Γ → R represents the height of the contour of the membrane. We are looking for
 其中g：_→r代表膜轮廓的高度。我们在找

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

a function u in C2(Ω) ∩ C1(Ω). The operator ∆ is the Laplacian, and it is given by
 C2（Ω）C1（Ω）中的功能U。算符∆是拉普拉斯函数，它由

.
 .

This is an example of a boundary problem, since the solution u of the PDE must satisfy the condition u(x) = g(x) on the boundary of the domain Ω. The above equation is known as Poisson’s equation, and when f = 0 as Laplace’s equation.
 这是一个边界问题的例子，因为PDE的解u必须满足域Ω边界上的条件u（x）=g（x）。上述方程称为泊松方程，当f=0时称为拉普拉斯方程。

It can be proved that if the data f,g and Γ are sufficiently smooth, then the problem has a unique solution.
 可以证明，如果数据f、g和_足够平滑，那么问题有一个独特的解决方案。

To get a weak formulation of the problem, first we have to make the boundary condition homogeneous, which means that g(x) = 0 on Γ. It turns out that g can be extended to the
 为了得到问题的弱表达式，首先要使边界条件均匀，即g（x）=0 on_。结果证明G可以扩展到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image003.gif)

whole of Ω as some sufficiently smooth function bh, so we can look for a solution of the form u − bh, but for simplicity, let us assume that the contour of Ω lies in a plane parallel to the
 整个Ω是一些足够平滑的函数bh，因此我们可以寻找形式u-bh的解，但为了简单起见，让我们假设Ω的轮廓位于一个平行于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

(x1,x2)- plane, so that g = 0. We let V be the subspace of C2(Ω) ∩ C1(Ω) consisting of functions v such that v = 0 on Γ.
 （x1，x2）-平面，因此g=0。我们将v设为c2（Ω）c1（Ω）的子空间，由函数v组成，这样v=0 on_。

As before, we multiply the PDE by a test function v ∈ V , getting
 如前所述，我们将pde乘以一个测试函数v∈v，得到

−∆u(x)v(x) = f(x)v(x),
 −∆U（x）V（x）=F（x）V（x）、

and we “integrate by parts.” In this case, this means that we use a version of Stokes formula known as Green’s first identity, which says that
 在这种情况下，这意味着我们使用了斯托克斯公式的一个版本，称为格林的第一个恒等式，也就是说

​                            Z                        Z                                          Z
 Z z

​                                   −∆uv dx =         (gradu) · (gradv)dx −       (gradu) · nvdσ
 −∆uv dx=（梯度u）·（梯度v）dx−（梯度u）·nvdσ

​                              Ω                        Ω                                         Γ
 欧姆

(where n denotes the outward pointing unit normal to the surface). Because v = 0 on Γ, the integral RΓ drops out, and we get an equation of the form
 （其中n表示垂直于表面的向外指向单位）。因为在_上v=0，所以积分r_就消失了，我们得到了形式的方程。

​                                                      a(u,v) = fe(v)      for all v ∈ V,
 a（u，v）=fe（v），对于所有v∈v，

where a is the bilinear form given by
 其中a是双线性形式

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

and feis the linear form given by Z
 并feis z给出的线性形式

​                                                                 fe(v) =       fvdx.
 铁（V）=fvdx。

Ω
 γ

We get the same equation as in section 17.2, but over a set of functions defined on a two-dimensional domain. As before, we can choose a finite-dimensional subspace Va of V and consider the discrete problem with respect to Va. Again, if we pick a basis (w1,...,wn) of Va, a vector u = u1w1 + ··· + unwn is a solution of the Weak Formulation of our problem iff u = (u1,...,un) is a solution of the linear system
 我们得到与第17.2节中相同的方程，但在二维域上定义的一组函数上。和以前一样，我们可以选择v的有限维子空间v a，并考虑与va有关的离散问题。同样，如果我们选择va的基（w1，…，wn），那么向量u=u1w1+········+unwn是我们问题弱公式的解，如果u=（u1，…，un）是线性系统的解。茎

Au = b,
 au=b，

with A = (a(wi,wj)) and b = (fe(wj)). However, the integrals that give the entries in A and b are much more complicated.
 其中a=（a（wi，wj））和b=（fe（wj））。然而，给a和b中的项的积分要复杂得多。

An approach to deal with this problem is the method of finite elements. The idea is to also discretize the boundary curve Γ. If we assume that Γ is a polygonal line, then we can triangulate the domain Ω, and then we consider spaces of functions which are piecewise defined on the triangles of the triangulation of Ω. The simplest functions are piecewise affine and look like tents erected above groups of triangles. Again, we can define base functions with small support, so that the matrix A is tridiagonal by blocks.
 处理这个问题的方法是有限元法。其思想是对边界曲线_进行离散化。如果假设_是一条多边形线，那么我们可以对域Ω进行三角化，然后我们考虑在Ω三角化的三角形上分段定义的函数空间。最简单的函数是分段仿射函数，它看起来就像一组三角形上面的帐篷。同样，我们可以用小的支持来定义基函数，这样矩阵A就成了三对角的块。

The finite element method is a vast subject and it is presented in many books of various degrees of difficulty and obscurity. Let us simply state three important requirements of the finite element method:
 有限元法是一门庞大的学科，在许多不同难度和晦涩程度的书籍中都有介绍。让我们简单地说明有限元法的三个重要要求：


 

\1.    “Good” triangulations must be found. This in itself is a vast research topic. Delaunay triangulations are good candidates.
 必须找到“良好”的三角测量。这本身就是一个庞大的研究课题。Delaunay三角测量是很好的候选者。

\2.    “Good” spaces of functions must be found; typically piecewise polynomials and splines.
 必须找到“好”的函数空间；通常是分段多项式和样条曲线。

\3.    “Good” bases consisting of functions will small support must be found, so that integrals can be easily computed and sparse banded matrices arise.
 由函数组成的“好”基的支持度很小，因此积分很容易计算，并产生稀疏带状矩阵。

We now consider boundary problems where the solution varies with time.
 我们现在考虑边界问题，其中解随时间变化。

# 17.3 Time-Dependent Boundary Problems: The Wave Equation  17.3时变边界问题：波动方程

Consider a homogeneous string (or rope) of constant cross-section, of length L, and stretched (in a vertical plane) between its two ends which are assumed to be fixed and located along the x-axis at x = 0 and at x = L.
 考虑等截面、长度为l的均质绳索（或绳索），并在其两端之间拉伸（垂直平面），假定其固定并沿x轴位于x=0和x=l处。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

Figure 17.6: A vibrating string
 图17.6：振动弦

The string is subjected to a transverse force τf(x)dx per element of length dx (where τ is the tension of the string). We would like to investigate the small displacements of the string in the vertical plane, that is, how it vibrates.
 每根长度为dx（其中，τ是管柱的张力）的元件承受横向力τf（x）dx。我们想研究弦在垂直面上的小位移，也就是它是如何振动的。

Thus, we seek a function u(x,t) defined for t ≥ 0 and x ∈ [0,L], such that u(x,t) represents the vertical deformation of the string at the abscissa x and at time t.
 因此，我们寻求一个函数u（x，t），定义为t≥0和x∈[0，l]，这样u（x，t）代表弦在横坐标x和时间t处的垂直变形。

It can be shown that u must satisfy the following PDE
 可以看出，u必须满足以下pde

,
 ，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

with c = pτ/ρ, where ρ is the linear density of the string, known as the one-dimensional wave equation.
 c=pτ/ρ，其中，ρ是弦的线密度，称为一维波动方程。

Furthermore, the initial shape of the string is known at t = 0, as well as the distribution of the initial velocities along the string; in other words, there are two functions ui,0 and ui,1 such that
 此外，弦的初始形状已知为t=0，以及沿弦的初始速度分布；换句话说，有两个函数ui，0和ui，1，这样

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

For example, if the string is simply released from its given starting position, we have ui,1 = 0. Lastly, because the ends of the string are fixed, we must have
 例如，如果字符串只是从给定的起始位置释放，那么我们有ui，1=0。最后，因为字符串的两端是固定的，所以我们必须

​                                                        u(0,t) = u(L,t) = 0,        t ≥ 0.
 u（0，t）=u（l，t）=0，t≥0。

Consequently, we look for a function u: R+ × [0,L] → R satisfying the following conditions:
 因此，我们寻找一个满足以下条件的函数u:r+×0，l]→r：

,
 ，

u(0,t) = u(L,t) = 0,       t ≥ 0       (boundary condition), u(x,0) = ui,0(x),     0 ≤ x ≤ L   (intitial condition),
 u（0，t）=u（l，t）=0，t≥0（边界条件），u（x，0）=ui，0（x），0≤x≤l（初始条件），

​                                                                                                        (intitial condition).
 （初始条件）。

This is an example of a time-dependent boundary-value problem, with two initial conditions.
 这是一个时间相关边值问题的例子，有两个初始条件。

To simplify the problem, assume that f = 0, which amounts to neglecting the effect of gravity. In this case, our PDE becomes
 为了简化这个问题，假设f=0，这等于忽略了重力的影响。在这种情况下，我们的PDE变成

,
 ，

Let us try our trick of multiplying by a test function v depending only on x, C1 on [0,L], and such that v(0) = v(L) = 0, and integrate by parts. We get the equation
 让我们试着用一个只依赖于x，c1的测试函数v乘以[0，l]，这样v（0）=v（l）=0，并按部分积分。我们得到了方程

.
 .

For the first term, we get
 第一学期，我们

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

where hu,vi is the inner product in L2([0,L]). The fact that it is legitimate to move ∂2/∂t2 outside of the integral needs to be justified rigorously, but we won’t do it here.
 其中，hu，vi是l2（[0，l]）中的内积。把2/t2移出积分是合法的，这一事实需要严格证明，但我们不会在这里这样做。

For the second term, we get
 第二学期，我们

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

and because v ∈ V , we have v(0) = v(L) = 0, so we obtain
 因为v∈v，我们有v（0）=v（l）=0，所以我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

Our integrated equation becomes
 我们的积分方程变成

,   for all v ∈ V  and all t ≥ 0. It is natural to introduce the bilinear form a: V × V → R given by
 ，对于所有v∈v和所有t≥0。引入双线性形式a:v×v→r是自然的，由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image019.gif)

where, for every t ∈ R+, the functions u(x,t) and (v,t) belong to V . Actually, we have to replace V by the subspace of the Sobolev space) consisting of the functions such that v(0) = v(L) = 0. Then, the weak formulation (variational formulation) of our problem is this:
 其中，对于每一个t∈r+，函数u（x，t）和（v，t）都属于v。实际上，我们必须用Sobolev空间的子空间替换v），它由函数组成，这样v（0）=v（l）=0。那么，我们问题的弱公式（变分公式）是：

Find a function u ∈ V such that
 求一个函数u∈v，这样

​                                                                                                    and all t ≥ 0
 且所有t≥0

​                                             u(x,0) = ui,0(x),       0 ≤ x ≤ L      (intitial condition),
 u（x，0）=ui，0（x），0≤x≤l（初始条件）

​                                                                                                   (intitial condition).
 （初始条件）。

It can be shown that there is a positive constant α > 0 such that
 可以证明有一个正常数α>0，这样

​                                                                                     for all v ∈ V
 对于所有v∈v

(Poincar´e’s inequality), which shows that a is positive definite on V . The above method is known as the method of Rayleigh-Ritz.
 （Poincar'e不等式），表示a在v上是正定的。上述方法称为瑞利-里兹法。

A study of the above equation requires some sophisticated tools of analysis which go far beyond the scope of these notes. Let us just say that there is a countable sequence of solutions with separated variables of the form
 对上述方程的研究需要一些复杂的分析工具，这些工具远远超出了这些注释的范围。我们只要说，有一个可数的解序列，它的形式变量是分开的。

,
 ，

called modes (or normal modes). Complete solutions of the problem are series obtained by combining the normal modes, and they are of the form
 被称为模式（或正常模式）。该问题的完全解是由正规模式组合而成的级数，其形式为

,
 ，

where the coefficients Ak,Bk are determined from the Fourier series of ui,0 and ui,1.
 其中系数ak，bk由ui，0和ui，1的傅立叶级数确定。

We now consider discrete approximations of our problem. As before, consider a finite dimensional subspace Va of V and assume that we have approximations ua,0 and ua,1 of ui,0 and ui,1. If we pick a basis (w1,...,wn) of Va, then we can write our unknown function u(x,t) as u(x,t) = u1(t)w1 + ··· + un(t)wn,
 我们现在考虑问题的离散近似。如前所述，考虑V的有限维子空间v a，假设我们有近似值ua，0和ua，ui，0和ui，1。如果我们选取VA的基（w1，…，wn），那么我们可以把未知函数u（x，t）写成u（x，t）=u1（t）w1+······+un（t）wn，

where u1,...,un are functions of t. Then, if we write u = (u1,...,un), the discrete version of our problem is
 其中，u1，…，un是t的函数，那么，如果我们写u=（u1，…，un），我们问题的离散版本是

d2u
 D2U

​                                                A                       + Ku = 0,
 a+ku=0，

where A = (hwi,wji) and K = (a(wi,wj)) are two symmetric matrices, called the mass matrix and the stiffness matrix, respectively. In fact, because a and the inner product h−,−i are positive definite, these matrices are also positive definite.
 其中a=（hwi，wji）和k=（a（wi，wj））是两个对称矩阵，分别称为质量矩阵和刚度矩阵。事实上，因为a和内积h−，−i是正定的，所以这些矩阵也是正定的。

We have made some progress since we now have a system of ODE’s, and we can solve it by analogy with the scalar case. So, we look for solutions of the form Ucosωt (or Usinωt), where U is an n-dimensional vector. We find that we should have
 我们已经取得了一些进展，因为我们现在有了一个ODE系统，并且我们可以通过与标量情况进行类比来解决它。因此，我们寻找形式为ucosωt（或usinωt）的解，其中u是一个n维向量。我们发现我们应该

(K − ω2A)Ucosωt = 0,
 （k−ω2a）ucosωt=0，

which implies that ω must be a solution of the equation
 这意味着ω必须是方程的解。

KU = ω2AU.
 ku=ω2au。

Thus, we have to find some λ such that
 因此，我们必须找到一些λ，以便

KU = λAU,
 ku=λau，

a problem known as a generalized eigenvalue problem, since the ordinary eigenvalue problem for K is
 由于k的一般特征值问题是

KU = λU.
 ku=λu.

Fortunately, because A is SPD, we can reduce this generalized eigenvalue problem to a standard eigenvalue problem. A good way to do so is to use a Cholesky decomposition of A as
 幸运的是，由于a是spd，我们可以将这个广义特征值问题简化为标准特征值问题。这样做的一个好方法是使用a的cholesky分解

A = LL>,
 A=ll>，

where L is a lower triangular matrix (see Theorem 7.10). Because A is SPD, it is invertible, so L is also invertible, and
 其中，L是下三角矩阵（见定理7.10）。因为a是spd，它是可逆的，所以l也是可逆的，并且

KU = λAU = λLL>U
 ku=λau=λll>u

yields
 产量

L−1KU = λL>U,
 L−1ku=λl>u，

which can also be written as
 也可以写为

L−1K(L>)−1L>U = λL>U. Then, if we make the change of variable
 L−1K（L>）−1L>U=λL>U。那么，如果我们改变变量

Y = L>U,
 Y=L>U，

using the fact (L>)−1 = (L−1)>, the above equation is equivalent to
 利用事实（l>）-1=（l−1）>，上述方程等于

L−1K(L−1)>Y = λY,
 L−1K（L−1）>Y=λY，

a standard eigenvalue problem for the matrix Kb = L−1K(L−1)>. Furthermore, we know from Section 7.8 that since K is SPD and L−1 is invertible, the matrix Kb = L−1K(L−1)> is also SPD.
 矩阵的标准特征值问题kb=l−1k（l−1）>。此外，我们从第7.8节了解到，由于k是spd，l−1是可逆的，因此矩阵kb=l−1k（l−1）>也是spd。

Consequently, Kb has positive real eigenvalues ( ) (not necessarily distinct) and it can be diagonalized with respect to an orthonormal basis of eigenvectors, say Y1,...,Yn.
 因此，kb具有正的实特征值（）（不一定是不同的），并且它可以相对于特征向量的正态基对角化，例如y1，…，yn。

Then, since Y = L>U, the vectors
 然后，因为y=l>u，向量

​                                                      Ui = (L>)−1Yi,          i = 1,...,n,
 ui=（l>）-1yi，i=1，…，n，

are linearly independent and are solutions of the generalized eigenvalue problem; that is,
 是线性独立的，是广义特征值问题的解；也就是说，

​                                                      KUi = ωi2AUi,         i = 1,...,n.
 kui=ωi2aui，i=1，…，n.

More is true. Because the vectors Y1,...,Yn are orthonormal, and because Yi = L>Ui, from
 更多是真的。因为向量y1，…，yn是正交的，并且因为yi=l>ui，来自

(Yi)>Yj = δij,
 （yi）>yj=δij，

we get
 我们得到

​                                                   (Ui)>LL>Uj = δij,         1 ≤ i,j ≤ n,
 （ui）>ll>uj=δi j，1≤i，j≤n，

and since A = LL>, this yields
 由于a=ll>，这就产生了

​                                                     (Ui)>AUj = δij,         1 ≤ i,j ≤ n.
 （ui）>auj=δi j，1≤i，j≤n。

This suggests defining the functions Ui ∈ Va by
 这建议通过定义函数ui∈va

.
 .

Then, it immediate to check that
 那么，马上检查一下

a(Ui,Uj) = (Ui)>AUj = δij,
 a（ui，uj）=（ui）>auj=δij，

which means that the functions (U1,...,Un) form an orthonormal basis of Va for the inner product a. The functions Ui ∈ Va are called modes (or modal vectors).
 这意味着函数（u1，…，un）为内积a形成了va的正交基，函数ui∈va称为模态（或模态向量）。

As a final step, let us look again for a solution of our discrete weak formulation of the problem, this time expressing the unknown solution u(x,t) over the modal basis (U1,...,Un), say
 作为最后一步，让我们再一次寻找问题的离散弱公式的解，这次用模态基（u1，…，un）表示未知解u（x，t），比如

,
 ，

where each uej is a function of t. Because
 其中，每个uej都是t的函数，因为

,
 ，

if we write u = (u1,...,un) with, we see that
 如果我们写u=（u1，…，un），我们会看到

u ,
 U

so using the fact that
 所以利用这个事实

​                                                      KUj = ωj2AUj,          j = 1,...,n,
 kuj=ωj2auj，j=1，…，n，

the equation
 方程式

d2u
 D2U

A dt2 + Ku = 0
 a dt2+ku=0

yields
 产量

.
 .

Since A is invertible and since (U1,...,Un) are linearly independent, the vectors (AU1,
 由于a是可逆的，并且（u1，…，un）是线性无关的，因此向量（au1，

...,AUn) are linearly independent, and consequently we get the system of n ODEs’
 …，aun）是线性独立的，因此我们得到了n odes的系统。

​                                                 (uej)00 + ωj2uej = 0,    1 ≤ j ≤ n.
 （uej）00+ωj2uej=0，1≤j≤n。

Each of these equation has a well-known solution of the form
 每个方程都有一个众所周知的形式解。

uej = Aj cosωjt + Bj sinωjt.
 uej=aj cosωjt+bj sinωjt。

Therefore, the solution of our approximation problem is given by
 因此，我们的近似问题的解由

,
 ，

and the constants Aj,Bj are obtained from the intial conditions
 从初始条件中得到常数aj，bj。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image021.gif)

by expressing ua,0 and ua,1 on the modal basis (U1,...,Un). Furthermore, the modal functions (U1,...,Un) form an orthonormal basis of Va for the inner product a.
 通过在模态基础上表达ua，0和ua，1（u1，…，un）。此外，模态函数（u1，…，un）为内积a形成了va的正交基。

If we use the vector space VN0 of piecewise affine functions, we find that the matrices A and K are familar! Indeed,
 如果我们使用分段仿射函数的向量空间vn0，我们会发现矩阵a和k是家族的！的确，

and                                                                       
 和

To conclude this section, let us discuss briefly the wave equation for an elastic membrane, as described in Section 17.2. This time, we look for a function u: R+ × Ω → R satisfying the following conditions:
 为了总结这一节，让我们简要讨论弹性膜的波动方程，如第17.2节所述。这次，我们寻找一个满足以下条件的函数u:r+×Ω→r：

,
 ，

u(x,t) = 0,       x ∈ Γ,     t ≥ 0       (boundary condition), u(x,0) = ui,0(x), x ∈ Ω     (intitial condition), Ω      (intitial condition).
 u（x，t）=0，x∈_，t≥0（边界条件），u（x，0）=ui，0（x），x∈Ω（初始条件），Ω（初始条件）。

Assuming that f = 0, we look for solutions in the subspace V of the Sobolev space consisting of functions v such that v = 0 on Γ. Multiplying by a test function v ∈ V and using Green’s first identity, we get the weak formulation of our problem:
 假设f=0，我们在Sobolev空间的子空间v中寻找由函数v组成的解，这样v=0 on_。用一个检验函数v∈v乘以格林的第一个恒等式，得到了问题的弱公式：

Find a function u ∈ V such that
 求一个函数u∈v，这样

​                                                                                                       and all t ≥ 0
 且所有t≥0

​                                                 u(x,0) = ui,0(x),      x ∈ Ω     (intitial condition),
 u（x，0）=ui，0（x），x∈Ω（初始条件）

​                                                                   Ω                          (intitial condition),
 Ω（初始状态）

where a: V × V → R is the bilinear form given by
 其中a:v×v→r为双线性形式，由

and                                                                        
 和

As usual, we find approximations of our problem by using finite dimensional subspaces Va of V . Picking some basis (w1,...,wn) of Va, and triangulating Ω, as before, we obtain the equation
 和往常一样，我们用有限维子空间v的va来近似我们的问题。选取Va的一些基（w1，…，wn），然后像以前一样进行三角处理，我们得到了方程。

d2u
 D2U

A dt2 + Ku = 0,
 dt2+ku=0，

,
 ，

where A = (hwi,wji) and K = (a(wi,wj)) are two symmetric positive definite matrices.
 其中a=（hwi，wji）和k=（a（wi，wj））是两个对称正定矩阵。

In principle, the problem is solved, but, it may be difficult to find good spaces Va, good triangulations of Ω, and good bases of Va, to be able to compute the matrices A and K, and to ensure that they are sparse.
 原则上解决了这个问题，但要计算矩阵a和k并确保它们是稀疏的，可能很难找到好的空间va、Ω的良好三角和va的良好基。