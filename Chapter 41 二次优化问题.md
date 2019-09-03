第四十一章

# 二次优化问题

## 41.1二次优化：正定情况

在本章中，我们考虑了工程和计算机科学（尤其是计算机视觉）中经常出现的两类二次优化问题：

\1.    最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

在所有x∈rn上，或受线性或仿射约束。

\2.    最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

在单位范围内。

在这两种情况下，a都是对称矩阵。我们还寻求F具有全局最小值的必要和充分条件。

物理和工程中的许多问题可以说是某种能量函数的最小化，有或没有约束。事实上，自然的作用是使能量最小化，这是力学的一个基本原理。此外，如果物理系统处于稳定平衡状态，那么处于该状态的能量应该是最小的。例如，放置在球体顶部的小球处于不稳定的平衡位置。一个小动作使球滚下来。另一方面，由于势能很小，放置在球体内部和底部的球处于稳定的平衡位置。

最简单的能量函数是二次函数。这样的函数可以方便地在表单中定义

q（x）=x>ax−x>b，

一千三百八十三

其中a是对称n×n矩阵，x，b是rn中的向量，视为列向量。实际上，由于很快就会明白的原因，最好在二次项前面加一个因子，这样

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

问题是，在什么条件下（a）q（x）具有全局最小值，最好是唯一值？

我们分两个阶段完整回答上述问题：

\1.    在这一节中，我们证明，如果a是对称正定的，那么q（x）在

ax=b。

\2.    在第41.2节中，我们给出了一般情况下关于a的伪逆的必要和充分条件。

我们从定义20.2的矩阵版本（第一卷）开始。

定义41.1.对称正定矩阵是特征值严格为正的矩阵，对称正定半矩阵是特征值非负的矩阵。

等价标准在下面的命题中给出。

提案41.1.考虑到尺寸n的任何欧几里得空间e，下列性质成立：

*(1)*     每个自伴线性映射f:e→e为正定iff

Hf（x），Xi＞0

对于所有x∈e，x=06。

*(2)*     每一个自伴线性映射f:e→e都是半正定iff。

Hf（x），Xi超0

对于所有x∈e。

证据。（1）首先，假设f是正定的。回想一下，每个自伴线性映射都有一个特征向量的正交基（e1，…，en），并让λ1，…，λn作为相应的特征值。关于这个基础，每x=x1e1+····+xnen=06，我们有

，

这是严格正的，因为对于某些i，λi>0表示i=1，…，n，和x2i>0，因为x 6=0。

相反，假设HF（x），Xi＞0。

所有x=06。那么对于x=ei，我们得到

hf（ei），eii=hλiei，eii=λi，

因此，对于所有i=1，…，n，λi>0。

（2）如（1）所述，我们已经

，

由于λi超过0，对于i＝1，…，n，因为f是半正定的，我们有HF（x），Xi超过0，如所要求的。相反，如（1）所示，除了hf（ei），eii≥0，我们只得到λi≥0。

一些特殊的符号（特别是在凸优化领域）通常表示对称矩阵是正定或半正定的。

定义41.2.对于任意n×n对称矩阵，我们写的是半正定的，我们写的是正定的。

应该注意的是，我们可以定义这种关系

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)

在任意两个n×n矩阵（对称与否）之间，iff a−b是对称半正定的。很容易确认这种关系实际上是矩阵上的一个偏序，称为半正定锥序；有关详细信息，请参阅Boyd和Vandenberghe[29]第2.4节。

如果a是对称正定的，很容易检查−1也是对称正定的。另外，如果c是对称正定m×m矩阵，a是秩n的m×n矩阵（因此m≥n，且映射x 7→ax被投影到rm上），则a>ca是对称正定的。

我们现在可以证明

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

当a是对称正定时具有全局最小值。提案41.2.给定二次函数

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

如果a是对称正定的，则q（x）对于线性系统的解ax=b具有唯一的全局最小值。q（x）的最小值为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

证据。因为a是正定的，所以它是可逆的，因为它的特征值都是严格正的。

设x=a−1b，并计算任意y∈rn的q（y）−q（x）。因为ax=b，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image016.gif)

因为a是正定的，所以最后一个表达式是非负的，因此

q（y）≥q（x）

对于所有y∈rn，证明x=a−1b是q（x）的全局最小值。简单的计算得出

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image018.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image019.gif)

评论：

(1)    二次函数q（x）也由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image021.gif)

但是，使用x>b的定义对于41.2号提案的证明更为方便。

(2)    如果q（x）包含一个常数项c∈r，那么

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image023.gif)

命题41.2的证明仍然表明，对于x=a−1b，q（x）具有唯一的全局最小值，但最小值为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image025.gif)

因此，当系统的能量函数q（x）由二次函数给出时

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image027.gif)

如果a是对称正定的，求q（x）的全局最小值等于解线性系统ax=b。有时，将线性问题ax=b重设为变分问题（求某个能量函数的最小值）是有用的。然而，通常情况下，最小化问题会带有额外的约束，必须满足所有可接受的解决方案。例如，我们可能想最小化二次函数

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image029.gif)

受约束的

2x1−x2=5.

q（x1，x2）最小的溶液不再是（x1，x2）=（0,0），而是（x1，x2）=（2，−1），如下文所示。

几何上，r3中z=q（x1，x2）定义的函数图是旋转轴oz的p的抛物面。约束

2x1−x2=5

与平行于Z轴的垂直平面H相对应，并且在xy平面中包含公式2x1−x2=5的线。因此，q的约束最小值位于抛物面上，即抛物面p与平面h的交点。

解决上述约束最小化问题的一个好方法是使用第39.1节中讨论的拉格朗日乘子方法。但首先，让我们精确地定义我们打算解决的最小化问题。

定义41.3.二次约束最小化问题包括二次函数的最小化。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image031.gif)

受线性约束

b>x=f，

其中a−1是m×m对称正定矩阵，b是n阶m×n矩阵（使m≥n），其中b，x∈rm（视为列向量），f∈rn（视为列向量）。

使用−1而不是a的原因是约束最小化问题被解释为一组平衡方程，其中自然产生的矩阵是a（见Strang[164]）。由于a和a−1都是对称正定的，所以这没有任何区别，但最好还是坚持strang的表示法。

如第39.1节所述，拉格朗日乘数的方法包括将n个约束b>x=f合并到二次函数q（x）中，通过引入称为拉格朗日乘数的额外变量λ=（λ1，…，λn），每个约束一个。我们组成拉格朗日

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image033.gif)

从定理39.3可知，约束优化问题有解的一个必要条件是l（x，λ）=0。自从

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image035.gif)

我们得到了线性方程组。

A−1X+Bλ=B，

b>x=f，

可以用矩阵形式写为

.

我们将在下面的命题41.3中证明，我们的约束极小化问题有一个由上述系统实际给出的唯一解。

注意这个系统的矩阵是对称的。我们的解决方法如下。从第一个方程中减去x

A−1X+Bλ=B，

我们得到

x=a（b−bλ），

代入第二个方程，我们得到

b>a（b−bλ）=f，

也就是说，

b>abλ=b>ab−f。

然而，根据前面的注释，由于a是对称正定的，b的列是线性无关的，b>ab是对称正定的，因此是可逆的。因此我们得到了解决方案

λ=（b>ab）−1（b>ab−f），x=a（b−bλ）。

注意，这种解决系统的方法需要先解决拉格朗日乘数。

假设e=b−bλ，我们还注意到系统

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image037.gif)

相当于系统

e=b−bλ，

x=ae，b>x=f。

后一个系统被Strang[164]称为平衡方程。事实上，Strang证明了许多物理系统的平衡方程可以用上述形式表示。这包括弹簧质量系统、电网和桁架，它们是由弹性杆建造的结构。在每种情况下，x、e、b、a、λ、f和k=b>ab都有物理解释。矩阵k=b>ab通常称为刚度矩阵。同样，读者也被称为Strang[164]。

为了证明我们的约束极小化问题有一个唯一的解，我们继续证明了受b>x=f约束的q（x）的约束极小化等价于另一个函数−g（λ）的无约束最大化。我们通过最小化拉格朗日L（x，λ）得到g（λ），该拉格朗日L（x，λ）仅被视为x的函数。函数−g（λ）是拉格朗日L（x，λ）的对偶函数。在这里，我们遇到了第49.7节中定义的对偶函数概念的一个特殊情况。

因为a−1是对称正定的，并且

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image039.gif)

根据命题41.2，得到L（x，λ）的解x的全局最小值（关于x）。

A−1X=B−Bλ，

也就是说，当

x=a（b−bλ），

L（x，λ）的最小值为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image041.gif)

出租

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image043.gif)

我们将在命题41.3中证明，受b>x=f约束的q（x）的约束极小化解等于−g（λ）的无约束最大化。这是第49.7节讨论的对偶性的一个特殊情况。

当然，因为我们最小化了l（x，λ）对x的影响，我们有

L（x，λ）≥−g（λ）

所有x和所有λ。但是，当约束b>x=f成立时，l（x，λ）=q（x），因此对于任何容许的x，也就是说b>x=f，我们有

最小值（x）≥最大值−g（λ）。

x·s

为了证明受b>x=f约束问题q（x）的唯一最小值是−g（λ）的唯一最大值，我们计算q（x）+g（λ）。

提案41.3.定义41.3的二次约束最小化问题具有由系统给出的唯一解（x，λ）。

.

此外，上述溶液的组分λ是−g（λ）最大的唯一值。

证据。如前所述，假设约束条件

b>x=f保持。去掉f，因为b>x=x>b和λ>b>x=x>bλ，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image045.gif)

因为a是正定的，所以最后一个表达式是非负的。实际上，它是空的iff

A−1X+Bλ−B=0，

也就是说，

A−1X+Bλ=B。

但是，当b>x=f和a−1x+bλ=b时，q（x）的唯一约束最小值b>x=f等于−g（λ）的唯一最大值，这证明了这个命题。

我们可以确认−g（λ）的最大值，或等于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image047.gif)

对应于通过解系统得到的λ值

事实上，自从

而b>ab是对称正定的，通过命题41.2，当

b>abλ−b>ab+f=0，

也就是说，如我们之前发现的，λ=（b>ab）−1（b>ab−f）。

评论：

(1)    在这种情况下，存在着一种二元性的形式。受b>x=f约束的q（x）的约束极小化称为原问题，而−g（λ）的无约束最大化称为对偶问题。二元性是指事实稍微松散地表述为

最小值（x）=max−g（λ）。x·s

第49.7节给出了约束最小化问题对偶性的一般处理。

回顾e=b−bλ，因为

我们也可以写

这个表达式通常表示系统的总势能。同样，最佳解是使势能最小（从而使−g（λ）最大）的解。

(2)    立即证明了命题41.3的方程等价于拉格朗日L（x，λ）的偏导数为空的方程：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image049.gif)

因此，受b>x=f约束的q（x）的最小值是拉格朗日L（x，λ）的极值。如我们在命题41.3中所示，这个极值对应于同时使L（x，λ）对X最小化和使L（x，λ）对λ最大化。几何上，这一点是l（x，λ）的鞍点。第49.7节讨论了鞍点。

(3)    拉格朗日乘数有时具有自然的物理意义。例如，在弹簧质量系统中，它们对应于节点位移。在一般意义上，拉格朗日乘数是满足平衡方程所需的修正项，也是满足约束条件的代价。有关更多详细信息，请参见Strang[164]。

回到约束最小化）

2x1−x2=5，

拉格朗日是

，

证明拉格朗日有鞍点的方程是

x1+2λ=0，x2−λ=0，2x1−x2−5=0。

我们得到溶液（x1，x2，λ）=（2、−1、−1）。

拉格朗日乘子在优化和变分问题中的应用在第49章中进行了广泛的讨论。

最小二乘法和拉格朗日乘数用于解决计算机图形和计算机视觉中的许多问题；见Trucco和Verri[172]、Metaxas[121]、Jain、Katsuri和Schunck[97]、Faugeras[60]和Foley、van Dam、Feiner和Hughes[64]。

## 41.2二次优化：一般情况

在本节中，我们完成了第41.1节中开始的研究，并给出了二次函数具有全局最小值的必要和充分条件。我们从以下简单的事实开始：

提案41.4.如果a是可逆对称矩阵，那么函数

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image051.gif)

具有一个最小值iff，在这种情况下，该最佳值是针对唯一值x（即x=a−1b）获得的，并且

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image053.gif)

证据。注意

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image055.gif)

因此，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image057.gif)


 

41.2。二次优化：一般情况

如果a有一些负特征值，比如−λ（λ>0），如果我们选取与λ相关的a的任何特征向量u，那么对于任何α∈r，α=06，如果我们让x=αu+a−1b，那么由于au=−λu，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image059.gif)

因为α可以任意大，λ>0，我们看到f没有最小值。因此，为了使f有一个最小值，我们必须有0，因为a是可逆的，它是肯定的，所以（x−a−1b）>a（x−a−1b）>0 iff x−a−1b=06，很明显，当x−a−1b=0，即x=a−1b时，f的最小值是达到的。

现在让我们考虑一个任意对称矩阵A的情况。

提案41.5。如果a是n×n对称矩阵，那么函数

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image061.gif)

最小值iff和（i−a a+）b=0，在这种情况下，最小值为

此外，如果a被诊断为正交的，则由形式的所有x∈rn得到最优值。

，

对于任何z∈rn−r，其中r是a的秩。

证据。A是可逆的情况由命题41.4处理，因此我们可以假定A是奇异的。如果a的秩r<n，那么我们可以将a对角化为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image063.gif)

其中u是正交矩阵，∑r是r×r对角可逆矩阵。然后我们有了

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image065.gif)

如果我们写信

而且，

用y，c∈r r和z，d∈rn−r，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image067.gif)

当y=0时，我们得到f（x）=-z>d，

因此，如果d=06，函数f没有最小值。因此，如果f最小，则d=0。但是，d=0意味着

，

我们从命题21.5（第一卷）知道b在a的范围内（这里，u是v>），相当于（i−aa+）b=0。如果d=0，则

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image069.gif)

由于∑r是可逆的，根据命题41.4，函数f有一个最小的iff∑0，相当于

因此，我们已经证明，如果f有一个最小值，那么（i−a a+）b=0，反之，如果（i−aa+）b=0和0，我们刚刚做的证明f有一个最小值。

当上述条件成立时，自

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image071.gif)

是正半定的，a的伪逆a+由下式给出

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image073.gif)

根据命题41.4，当y=∑−r 1c，z=0，d=0时，即x的最小值由

而且，

41.2。二次优化：一般情况

我们由此推断

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image075.gif)

f的最小值是

对于形式的任何x∈rn

，

对于任何z∈rn−r，我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image077.gif)

我们有

和

因为（i−aa+）b=0，也就是说，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image079.gif)

所以如果

，

然后d=0。因此，最小化函数的问题

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image081.gif)

如果我们加上形式c>x=0的线性约束或形式c>x=t的仿射约束（其中t∈rm和t=0），6如果c是n×m矩阵，可以用c的qr分解将其简化为不受约束的情况。让我们演示如何对f的线性约束执行此操作。ORM C>X=0。

如果我们使用c的qr分解，通过排列c的列来确保c的前r列是线性无关的（其中r=秩（c）），我们可以假设

，

其中q为n×n正交矩阵，r为r×r可逆上三角矩阵，s为r×m-r矩阵，_为置换矩阵（c为秩r）。那么如果我们让

，

其中y∈r r和z∈rn−r，则c>x=0变为

，

这意味着y=0，c>x=0的每一个解的形式都是

.

我们原来的问题变成了

减少

服从y=0，y∈r r，z∈rn−r。

因此，约束c>x=0被简化为y=0，如果我们写

，

其中，g11是r×r矩阵，g22是（n-r）×n-r矩阵，以及

，


 

我们的问题变成了

减少，

提案41.5解决了这个问题。

形式c>x=t（其中t=0）6的约束可以用类似的方式处理。在这种情况下，我们可以假定c是一个n×m矩阵，具有满秩（因此m≤n）和t∈rm。然后我们使用一个形式的QR分解

，

其中p是正交n×n矩阵，r是m×m可逆上三角矩阵。如果我们写信

，

式中y∈rm和z∈rn−m，方程c>x=t变成

（r>0）p>x=t，

也就是说，

会产生

由于r是可逆的，我们得到y=（r>）-1t，然后很容易看出，我们的原始问题根据矩阵p>ap减少到一个不受约束的问题；细节留作练习。

## 41.3在单位球面上最大化二次函数

在本节中，我们讨论了主要由计算机视觉（图像分割和轮廓分组）引起的各种二次优化问题。这些问题可归结为以下基本优化问题：给定一个n×n实对称矩阵a

最大化x>ax，以x>x=1，x∈rn为准。

根据命题21.10（第一卷），单位球面上x>ax的最大值等于矩阵A的最大特征值λ1，并且它是针对与λ1相关的任何单位特征向量U1实现的。

A      在计算机视觉中经常遇到的上述问题的变种，包括在椭球体上用公式给出的X>AX最小化。

x>bx=1，

其中b是对称正定矩阵。因为b是正定的，所以它可以对角化为

B      =qdq>，

其中q是正交矩阵，d是对角矩阵，

d=诊断（d1，…，dn）

当di>0时，对于i=1，…，n.如果我们通过定义矩阵b1/2和b−1/2

b1/2=qdiag

和

B−1/2=qdiag，

很明显，这些矩阵是对称的，b−1/2bb−1/2=i，b1/2和b−1/2是互逆的。那么，如果我们改变变量

X=B−1/2Y，

方程x>bx=1变为y>y=1，优化问题

| 网络错误            | 网络错误 |
| ------------------- | -------- |
| 网络错误   网络错误 | 网络错误 |
| 网络错误            | 网络错误 |
| 网络错误            | 网络错误 |

其中y=b1/2x，其中b−1/2ab−1/2是对称的。

复杂版本的基本优化问题，其中A是一个厄米矩阵也出现在计算机视觉。也就是说，给定一个n×n复厄米特矩阵A，

最大化x ax，以x x=1，x∈cn为准。

同样，根据命题21.10（第一卷），单位球面上x ax的最大值等于矩阵A的最大特征值λ1，并且它是针对与λ1相关的任何单位特征向量U1实现的。

注：值得指出的是，如果a是一个偏厄米矩阵，也就是说，如果a=−a，那么x ax是纯虚数或零。

实际上，因为z=x ax是一个标量，我们有z=z（z的共轭），所以我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image082.gif)

x ax=（x ax）=x a x=-x ax，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image083.gif)

所以x ax+x ax=2re（x ax）=0，这意味着x ax是纯虚数或零。特别是，如果a是实矩阵，如果a是斜对称的，那么

x>ax=0。

因此，对于任何实矩阵（对称与否），

x>ax=x>h（a）x，

其中h（a）=（a+a>）/2，a的对称部分。

| 网络错误 |          |
| -------- | -------- |
| 网络错误 | 网络错误 |
| 网络错误 | 网络错误 |

在某些情况下，有必要对球体上的二次函数最大化问题添加线性约束。Golub[78]（1973）完全解决了这个问题。问题如下：给定n×n实对称矩阵a

如第41.2节所示，Golub表明线性约束c>x=0可以消除如下：如果我们使用c的qr分解，通过排列列，我们可以假设

，

其中q是一个正交n×n矩阵，r是一个r×r可逆上三角矩阵，s是一个r×r（p-r）矩阵（假设c的秩为r）。那么如果我们让

，

其中y∈r r和z∈rn−r，则c>x=0变为

，

这意味着y=0，c>x=0的每一个解的形式都是

.

我们原来的问题变成了

最小化（

以z>z=1，z∈rn−r，y=0，y∈rr为准。

因此，约束c>x=0被简化为y=0，如果我们写

，

我们的问题变成了

最小化z>g22z，服从z>z=1，z∈rn−r，

标准特征值问题。

注：有一种求g22特征值的方法，它不需要c的qrfactorization。如果我们

然后

，

### 0 G22

如果我们设置

P=Q>JQ，

然后

pap=q>jqaq>jq。

现在q>jqaq>jq和jqaq>j具有相同的特征值，所以pap和jqaq>j也具有相同的特征值。结果表明，我们的优化问题的解在k=pap的特征值中，其中r至少为0。利用CC+是C范围的投影，其中C+是C的伪逆，也可以证明

P=I−CC+，

到c>内核的投影。因此p可以直接用c来计算，特别是当n≥p和c具有全秩（c的列是线性无关的），那么我们知道c+=（c>c）−1c>和

P=I−C（C>C）−1C>。

库尔和施[42]使用了这一事实，于和施[186]也含蓄地使用了这一事实。

在实践中也出现了增加n>x=t形式的仿射约束的问题，其中t=06。乍一看，这个问题似乎并不比t=0的线性问题更困难，但事实确实如此。Gander、Golub和von Matt[75]在一篇论文中对这个问题进行了广泛的研究（1989年）。

Gander、Golub和von Matt考虑了以下问题：给定（n+m）×（n+m）实对称矩阵a（n>0），一个（n+m）×m全秩矩阵n，以及一个非零向量t∈rm（其中（n>）+表示n>的伪逆矩阵），

最小化x>ax

以x>x=1，n>x=t，x∈rn+m为准。

条件1确保问题有一个解决方案，并且不是琐碎的。作者首先证明了仿射约束n>x=t是可以消除的。一种方法是使用n.if的qr分解。

，

其中p是一个正交（n+m）×n+m矩阵，r是一个m×m可逆上三角矩阵，如果我们观察到，如果我们写下

其中b为m×m对称矩阵，c为n×n对称矩阵，_为m×n矩阵，且

，

用y∈Rm和z∈Rn，得到

x>ax=y>by+2z>_y+z>cz，

r>y=t，y>y+z>z=1。

因此

y=（r>）-1t，

如果我们写

s2=1−y>y>0

和

B=_Y，

我们得到了简化的问题

最小化z>cz+2z>b，以z>z=s2，z∈rm为准。

不幸的是，如果b 6=0，21.10号提案（第一卷）不再适用。使用拉格朗日乘子仍然可以求出函数z>cz+2z>b的最小值，但这种解太过复杂，无法在此给出。感兴趣的读者将在Gander、Golub和von Matt[75]中找到一个深入的讨论。

## 41.4总结

本章的主要概念和结果如下：

•     二次优化问题；二次函数。

•     对称正定和半正定矩阵。

•     半正定锥序。

•     当a为对称正定时，存在全局极小值。

•     约束二次优化问题。

•     拉格朗日乘数；拉格朗日。

•     原始问题和双重问题。

•     二次优化问题：对称可逆矩阵A的情况。

•     二次优化问题：对称矩阵A的一般情况。

•     添加形式c>x=0的线性约束。

•     添加形式c>x=t的仿射约束，其中t 6=0。

•     在单位球面上最大化二次函数。

•     在椭球上最大化二次函数。

•     最大化埃尔米特二次型。

•     添加形式c>x=0的线性约束。

•     添加形式n>x=t的仿射约束，其中t 6=0。


 