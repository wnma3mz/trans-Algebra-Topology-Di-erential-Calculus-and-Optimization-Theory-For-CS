第五十二章

# 岭回归和套索回归

## 52.1岭回归

解一个超定或欠定线性系统ax=y的问题，是一个“学习问题”，在这个问题中，我们观察一系列数据（（a1，y1），…，（am，ym）），其中ai∈rn和yi∈r，被看作是我们试图推断的未知函数f的输入输出对。最简单的函数是一个线性函数f（x）=x>w，其中w∈rn是一个系数向量，通常称为权向量。由于这个问题是超定的，而且我们的观测可能会有误差，我们不能精确地解W，因为系统的解aw=y，所以我们只能解最小平方问题。

.

在第21.1节（第一卷）中，我们证明了这个问题可以用伪逆法来解决。我们知道极小值w是正态方程a>aw=a>y的解，但是当a>a不可逆时，这种解是不唯一的，因此必须用一些准则在这些解中进行选择。

一种解决方案是选择最小欧几里得范数kw+k2的唯一向量w+，使其最小化。解w+由w+=a+b给出，其中a+是a的伪逆矩阵。矩阵a+由a的SVD得到，即a=v∑u>。也就是说，a+=u∑+v>，其中∑+是用σi−1替换∑中的每一个非零奇异值σi得到的矩阵，保留所有零的位置，然后转置。这种方法的困难在于，它需要知道奇异值是零还是非常小但非零。一个非常小的非零奇异值σin∑会产生一个非常大的值σ−1 in∑+但σ=0在∑中保持为0。

这种不连续现象是不可取的，另一种方法是通过在kaw−yk2中添加一个正则化项来控制w的大小，自然的候选项是kwk2。还可以将矩阵A的每一行视为输入向量Xi

一千七百五十三

将m×n矩阵x定义为

，

其中行向量x> i是x的行，因此Xi→rn是列向量。我们的优化问题称为岭回归，即问题（rr1）：

最小化KY−XWK2+K KWK2，

通过引入新变量ξ=y−xw，可以重写为（rr2）：

最小化ξ>ξ+kw>w取决于

y−xw=ξ，

其中k>0是确定正则化项w>w影响的常数。

我们的最小化问题的第一版的目标函数可以表示为

j（w）=ky−xwk2+k kwk2

=（y−x w）>（y−xw）+kw>w=y>y−2w>x>y+w>x>xw+kw>w=w>（x>x+kin）w−2w>x>y+y>y。

矩阵x>x为对称半正定，k>0，因此矩阵x>x+kin为正定。接下来是

j（w）=w>（x>x+kin）w−2w>x>y+y>y

是严格凸的，所以它有一个独特的最小iff jw=0。自从

jw=2（x>x+kin）w−2x>y，

我们推断

W=（x>x+kin）−1X>y.（wp）

有趣的是，当k>0变为零时，矩阵（x>x+kin）−1X>的极限是x的伪逆x+。为了证明这一点，让x=v∑u>是x的SVD。

然后

（x>x+kin）=u∑>v>v∑u>+kin=u（∑>∑+kin）u>，

所以

（x>x+kin）−1X>=u（∑>kin）−1U>u∑>v>=u（∑>kin）−1∑>v>。矩阵中的对角项（∑>∑+kin）−1∑>是

，如果σi>0，

如果σi=0，则为零。所有非术语项均为零。当σi>0和k>0变为0时，

，

所以

lim（∑>∑+kin）−1∑>=∑+，

K7～0

这意味着

lim（x>x+kin）−1x>=x+。

K7～0

我们问题的第一个公式的对偶函数是一个常数函数（其值最小为j），因此它是无效的，但是我们问题的第二个公式产生了一个有趣的对偶问题。拉格朗日是

L（ξ，w，λ）=ξ>ξ+kw>w+（y−xw−ξ）>λ

=ξ>ξ+kw>w−w>x>λ−ξ>λ+λ>y。

用λ，ξ，y∈rm。

为了推导对偶函数g（λ），我们将l（ξ，w，λ）对ξ和w最小化，为此我们将梯度lξ，w设为零。自从

，

我们得到

.

上面建议定义变量α，使ξ=kα，因此我们得到λ=2kα和w=x>α。然后用拉格朗日方程中的ξ、λ和w的上述值代入α的函数，得到了α的对偶函数。

g（α）=k2α>α+kα>xx>α−2kα>xx>α−2k2α>α+2kα>y=−kα>（xx>+kim）α+2kα>y。

这是一个严格的凹函数，因此它的最大值达到iff gα=0，即，

2k（xx>+kim）α=2ky，

会产生

α=（xx>+kim）−1y.

把我们所获得的一切结合起来

α=（xx>+kim）−1y

w=x>α

ξ=kα，

会产生

w=x>（xx>+kim）−1y.（wd）

在早期（wp）我们发现

W=（X>X+K）−1X>Y，

而且很容易检查

（x>x+kin）−1X>=x>（xx>+kim）−1.

采用上述方法学习仿射函数f（w）=x>w+b，而不是线性函数f（w）=x>w，其中b∈r，我们有以下优化程序（rr3）：

最小化ξ>ξ+kw>w

从属于

y−xw−b1=ξ，

其中y，ξ，1∈Rm，w∈Rn。注意，在程序（rr3）中，最小化仅在ξ和w上执行，而不是在变量b上执行。与此程序相关的拉格朗日是

L（ξ，w，b，λ）=ξ>ξ+kw>w−w>x>λ−ξ>λ−b1>λ+λ>y。

通过将梯度lξ，b，w设置为零，我们得到

.

如前所述，如果我们设置ξ=kα，我们得到w=x>α和

g（α）=-kα>（xx>+kim）α+2kα>y。

由于k>0且λ=2kα，双岭回归为以下程序（drr3）：

最小化α>（xx>+kim）α−2α>y

1>α=0.

注意，在系数1/2之前，这个问题满足命题41.3的条件，a=（x x>+kim）−1，b=y，b=1m，f=0，x重命名为α。因此，它有一个独特的解α（注意，λ=2kα不是命题41.3中使用的λ，我们将其重命名为μ）。因为命题41.3给出的解是

µ=（b>ab）−1（b>ab−f），α=a（b−b）

我们得到μ=（1>（xx>+kim）−11>（xx>+kim）−1y，α=（xx>+kim）−1（y−1）。

注意，矩阵b>ab是标量1>（xx>+kim）−11。

一旦α，ξ=kα，w=x>α被确定，b由方程给出

b1=y−xw−ξ=y−xw−kα。

由于1>1=m和1>α=0，我们得到

，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

其中y是y的平均值，xj是x的jth列的平均值。因此，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image003.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image005.gif)

其中（x1···xn）是1×n行向量，其jth项为xj。因为w=x>α，我们可以

同时写

表达式

-。···

建议寻找上述形式的截距项b（也称为偏差），即程序（rr4）：

最小化ξ>ξ+kw>w

从属于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

同样，在程序（rr4）中，最小化只在ξ和w上进行，因为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

如果x=（x11···xn1）是m×n矩阵，其jth列为矢量xj1，则上述程序等于程序（rr5）：

最小化ξ>ξ+kw>w取决于

如果我们写y=y−y1和x=x−x，则上述程序变为（rr6）：

乙

根据Yb−xwb−bb1=ξ，最小化ξ>ξ+kw>w。

如果该程序的解决方案是wb，则bb由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)

bb=yb−（xb1···xbn）wb=0，

因为数据Yb和Xb居中。因此（rr6）相当于岭回归

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

没有适用于中心数据的截距项yb=y−y1和xb=x−x，程序（rr60）：

根据Yb−xwb=ξ，最小化ξ>ξ+kw>w。

如果w是由b给出的该程序的最优解

wb=xb>（xbxb>+kim）−1y，b

那么b是由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

B=Y−（x1···xn）W.

乙

备注：虽然这不是一个明显的先验，但程序（rr3）的最优解w等于程序（rr60）的最优解w。然而，实际上，自从

B求解对偶（drr3）比求解程序（rr60）困难，因为对偶程序具有额外的约束1>α=0，所以涉及中心数据的程序（rr60）是首选的。

如果我们在程序（rr3）中也将b最小化，自然会想知道会发生什么。让我们将术语KB2添加到目标函数中。然后我们得到程序

根据y−xw−b1=ξ，最小化ξ>ξ+kw>w+kb2。

这建议将b作为权重向量w的一个额外分量，通过将m×n+1矩阵[x 1]的列（维度m的列）添加到矩阵x中，得到程序（rr3b）：

最小化ξ>ξ+kw>w+kb2

从属于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image016.gif)

这个程序和程序（rr2）一样被解决，我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image018.gif)

因此b=1>α。

观察[x 1][x 1]>=xx>+11>。因为我们也有这个方程

y−xw−b1=ξ，

我们得到

所以

会产生

.

用任意常数c>0重新计算k的推导完全相同，我们得到

.

正如黑斯提、蒂比西拉尼和弗里德曼[87]所指出的那样（第3.4节），方法的一个缺陷是B的解在给每个值yi加上一个常数c时不是不变的。使用程序（RR60）的方法并非如此。

对偶（rr2）或（rr3）的一个有趣的方面是，它表明形式x>α的解w是一个线性组合。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image020.gif)

在数据点Xi中，系数αi对应于对偶函数的双变量La2= 2kα，以及

α=（xx>+kim）−1y.

如果m小于n，则求解α更为有利。但真正让双重意义有趣的是，我们对x的定义是

，

矩阵x x>由内部积x>i xj组成，同样，函数学习f（x）=w>x可以表示为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image022.gif)

即w和f（x）都是根据内积x>i xj和x>i x给出的。

这一事实是岭回归推广的关键，在岭回归中，输入空间rn嵌入到更大（可能是无限维）的欧几里得空间f（内积h−、−i）中，通常使用函数称为特征空间。

⑨：Rn→F.

问题变成（核岭回归）（krr2）：

最小化ξ>ξ+khw，wi

以Y-HW为例，（i）i＝ZeI i，i＝1，…，m。

注意w∈f。这个问题在Shawe–Taylor和Christianini[154]中讨论（第

7.3）。

我们将在下面说明解决方案完全相同：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image024.gif)

核矩阵，其中G是给定的GM矩阵，并且通常用GOJJ＝H*（Xi）G，，（XJ）I表示。

K

在这个框架中，我们在使用梯度时必须小心谨慎，因为涉及到内积h−、−i on f，而f可以是无限维的，但这不会造成任何问题，因为我们可以使用导数，并且根据命题38.5，我们已经

dh−、−i（u，v）（x，y）=hx，vi+hu，yi。

这意味着地图u 7→hu，ui的导数是

dh−、−iu（x）=2hx，ui。

由于地图u 7→hu，vi（v固定）是线性的，其导数为

dh−，viu（x）=hx，vi.拉格朗日的导数

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image026.gif)

关于ξ和w是

.

我们有=0表示全部，如果

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image028.gif)

我们再次定义了ξ=kα，所以我们得到了λ=2kα，并且

.

回到拉格朗日

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image030.gif)

如果G是由Gij= H*（Xi），（xJ）i给出的矩阵，那么我们得到

G（α）=-Kα>（G+Kim）α+2Kα>Y。

函数g是严格凹形的，其最大值为

α=（g+kim）−1y，

如前所述。

在岭回归的标准情况下，如果f=rn（但内积h−、−i是任意的），我们可以利用上述方法学习仿射函数f（w）=x>w+b，而不是线性函数f（w）=x>w，其中b∈r。这次我们假设b是形式

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image031.gif)

b=y−hw，（x1···xn）i，

其中x j是m×n矩阵x的j列，其第i行是

列向量ε（Xi），其中（x1·…·xn）被视为列向量。我们有最小化问题（krr60）：

最小化ξ>ξ+khw，wi

从属于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image033.gif)

其中）是n维向量

根据矩阵G给出的解由

，

和以前一样。我们得到α=（gb+kim）−1y，b

根据前面的计算，b由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image035.gif)


 

我们将在第53.3节中解释如何从矩阵G计算矩阵gb。

由于特征空间F的维数可能非常大，人们可能担心计算内积H（Xi），（xJ）i可能非常昂贵。这就是内核函数的救星。嵌入的一个核函数κ：rn→f是一个mapκ：rn×rn→r，其性质是

κ（u，v）=h（u），（v）i表示所有u，v∈rn。

如果可以以相当便宜的方式计算κ（u，v），并且如果（u）可以便宜地计算，那么可以很便宜地计算内积H*（Xi）、（xJ）i（和h（x））、（x）i。幸运的是，有好的内核函数。关于内核方法的两个非常好的来源是scho–lkopf和smola[141]以及shawe–taylor和Christianini[154]。我们将在第53章中研究内核。

## 52.2套索回归（`1-正则化回归）

岭回归的主要缺点是估计权向量w通常具有许多非零系数。因此，岭回归不能很好地扩大。实际上，我们需要能够处理数百万个或更多参数的方法。一种鼓励向量w稀疏的方法是用惩罚函数k kwk1替换二次惩罚函数，用“1-范数”替换“2-范数”。

这种方法最初是由Tibshirani arround于1996年提出的，其名称为lasso，代表“最小绝对选择和收缩运算符”。这种方法也被称为“1-正则回归”，但它不如主要使用的“lasso”那么可爱。

给定一组训练数据{（x1，y1），…，（xm，ym）}，用xi rn和yir r，如果x是m×n矩阵

，

其中，行向量x>i是x的行，如果出现以下优化问题（lasso1），则lasso回归：

最小化

y−xw=ξ，

其中k>0是确定正则化项kwk1影响的常数。

规则化术语kwk1=w1+··················wn的困难在于，对于所有w，映射w 7→kwk1都是不可微的。这种困难可以通过使用子梯度来克服，但也可以通过使用我们已经掌握的技巧，以基本的方式获得上述程序的对偶。使用，即如果x∈r，则

| X=最大X，−X。

利用这个技巧，通过引入一个非负变量的向量，我们可以重写lasso最小化，如下所示：lasso正则化（lasso2）：

最小化

，

其中y，ξ∈rm和。

约束和是等价的，对于一个最优解，我们必须有，也就是。

拉格朗日）由

，

与λ∈Rm和。由于目标函数是凸的，且约束L相对于原始函数具有最小值为仿射（因此是合格的），所以拉格朗日

变量，=0。因为梯度由

，

我们得到了方程

ξ=λ

α+α-α-β=x>λα+α-β=k1-β。

利用这些方程，给出了

.

由于β≥0，约束α+α−=k1−β等于

α+α−≤k1。

其中最大值为α+，α−≥。如果我们回想一下，对于任意i∈1，…，n zt（∈rn，α+）i−（α-）i的最小值是−k，并且

K

kzk∞=1最大值≤i≤n zi，

因此，约束条件

α+α−≤k1

x>λ=α+α−α−

相当于

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image037.gif)

以上相当于2n约束

−k≤（x>λ）i≤k，1≤i≤n。

因此，双套索程序由

最大化受试者

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image039.gif)

其中（因为是常数项）等于（dlasso2）：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image041.gif)

考虑到约束y−xw=ξ，并且对于最优解，我们必须有ξ=λ，必须满足以下条件：

（）还观察到，对于最优解，我们

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image043.gif)

由于目标函数是凸的，且常数是合格的，对偶间隙为零，因此对于初等和对偶的最优解，即

，

由此得出方程

w>x>（y−xw）=k kwk1.（）

以上是w和x>的内积（y−xw），所以当w i=06时，由于kwk1=w1+············································如果

S=I∈1，…，N Wi=06，

如果x表示由s索引的x列组成的矩阵，如果ws表示由w的非零分量组成的向量，那么我们有

.

我们也有

−∞

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image044.gif)

其中s是s的补码。第一个方程得出

xs>xs ws=xs>y-ksgn（ws）

因此，如果x>xs是可逆的（如果x的列是线性无关的，则是这种情况），我们得到ws=（xs>xs）−1（xs>y-ksgn（ws））。

理论上，如果我们知道w的支持和它的组件的符号，那么ws是确定的，但在实践中，这是无用的，因为问题是要找到支持和解决方案的符号。

求解套索回归的一种方法是用对偶程序求出λ=ξ，然后用线性规划方法求出W，通过保持ξ常数求解套索初值产生的线性规划。最好的方法是使用第51.7（5）节所述的ADMM。梯度下降也有许多变化；见黑斯提、提比西拉尼和温赖特。

〔88〕。

在前面的讨论中，我们假设我们试图学习一个线性函数f（x）=w>x。为了学习仿射函数f（x）=w>x+b，我们解决了以下优化问题（lasso3）：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image046.gif)

观察到，正如在岭回归的情况下，我们没有最小化超过b。

与这个优化问题有关的拉格朗日是

，

因此，通过将梯度设置为零，我们得到了方程

ξ=λ

α+α-α-β=x>λα+α-β=k1-β

1>λ=0，

利用这些方程，我们发现对偶函数也由

，

双套索程序由

最大化受试者

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image048.gif)

相当于（dlasso3）：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image050.gif)

一旦确定了λ=ξ和w，我们就用方程得到b。

b1=y−xw−ξ，

由于1>1=m和1>ξ=1>λ=0，上述结果

，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image051.gif)

其中y是y的平均值，xj是x的jth列的平均值。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image053.gif)

可用于，如岭回归（见第52.1节），证明程序（lasso3）等同于对中心应用无截距项的lasso回归（lasso2）。

数据，替换b。那么b是由

其中w是（lasso2）给出的溶液。这是黑斯迪，蒂比西拉尼描述的方法，

乙

和Wainwright[88]（第2.2节）。

找到b的另一种方法是将术语（c/2）b2添加到目标函数中，使某个正常数c获得程序（lasso4）。这次拉格朗日是

，

因此，通过将梯度设置为零，我们得到了方程

ξ=λ

α+α-α-β=x>λα+α-β=k1-β

cb=1>λ。


 

52.3。总结

因此B也被确定，并且双套索程序与第一套索双（dlasso2）相同，即

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image055.gif)

因为方程ξ=λ和

y−xw−b1=ξ

保持，从cb=1>λ我们得到

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image057.gif)

那就是

会产生

.

在岭回归的情况下，B也受到惩罚的方法的一个缺陷是，在每个值yi加上一个常数c时，B的解不是不变的。

## 52.3总结

本章的主要概念和结果如下：

•     岭回归。

•     核岭回归。

•     内核函数。

•     套索回归。