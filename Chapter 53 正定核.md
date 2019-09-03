第五十三章

# 正定核

## 53.1正定核的基本性质

设x为非空集。如果集合x代表一组高度非线性的数据，使用一个称为特征图的函数，将x映射到一个更高维度的空间h，这可能是有利的。这一观点是，将x中的对象描述“展开”，以使其线性化。空间h通常是一个向量空间，它有一个内积h−−i。如果h是无限维，那么我们假设它是希尔伯特空间。

许多分析或分类数据的算法都使用了内积h_（x），（y）i，其中x，y∈x。因此，自然会做出以下定义。

定义53.1.设x为非空集，设h为（复杂）希尔伯特空间，设_：x→h为称为特征图的函数。函数k:x×x→c由

κ（x，y）=h（x），（y）i，x，y∈x，

称为内核函数。

备注：一个特征映射通常被称为特征嵌入，但是这个术语有点误导，因为它表明这样的映射是可注入的，这不一定是如此。不幸的是，大多数人都使用这个术语。

例53.1。假设我们有两个特征图，分别是：_:x→rn1和_:x→rn2，让κ1（x，y）=h_（x），_（y）i和κ2（x，y）=h_（x），_（y）i是对应的核函数1（其中h−，−i是rn上的标准内积）。定义特征图_：x→rn+n2 by_（x）=（_1（x），_2（x）），

（n1+n2）元组。我们有h_（x），_（y）i=h（_1（x），_（x）），（_（y），_（y））i=h_（x），_（y）i+h_（x），_（y）i

=κ1（x，y）+κ2（x，y），

一千七百七十一


 

它显示了由

K（x，y）=K 1（x，y）+K 2（x，y）

是对应于特征映射的核心函数，即：x→rn1+n2。

例53.2。设x为r2的一个子集，设_:x→r3为下式给出的图

.

观察特征空间h=r3中的线性关系对应于（数据）输入空间中的二次关系。我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

其中hx，yi是r2上常见的内积。因此函数

κ（x，y）=hx，yi2

是与功能空间r3关联的内核函数。如果我们现在考虑图_:x→r4，由

，

我们马上检查

h_2（x），_2（y）i=κ（x，z）=hx，yi2，

这表明相同的内核可以从不同的映射中产生到不同的特征空间。

例53.3。实例53.2可概括如下。假设我们有一个特征图_:x→rn，让κ1（x，y）=h_（x），_（y）i是相应的核函数（其中h−，−i是rn上的标准内积）。通过其N2组分（x）（i，j）=（_（x））i（_（x））j，1≤i，j≤n，定义特征图_：x→rn×rn。

内积在Rn×Rn上，由

.

然后我们有了

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

因此，由κ（x，y）=（κ1（x，y））2给出的mapκ是一个与特征图_：x→rn×rn相关联的核映射。特征图a是实例53.2中特征图_的直接概括。

2.上面的论点立即被改编以表明，如果_:X→RN1和_:X→RN是两个特征映射，并且如果κ1（x，y）=h_（x），_（y）i和κ2（x，y）=h_（x），_（y）i是对应的核函数，那么由定义的映射

k（x，y）=k 1（x，y）k 2（x，y）

是一个核心函数，用于特征空间RN1×RN2和特征映射

⑨（x）（i，j）=（_（x））i（_（x））j，1≤i≤n1，1≤j≤n2.

例53.4。注意，特征图_：x→rn×rn不是很经济的，因为如果i=6 j，那么部件_（i，j）（x）和_（j，i）（x）都等于（_1（x））i（_1（x））j。

因此，我们可以定义由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

其中1≤i≤j≤n的对（i，j）按字典顺序排列。特征图a是实例53.2中特征图_的直接概括。

请注意，也可以用以下方式定义_，这样更容易得出任何幂的泛化：

，

其中n-元组（i1，…，in）按字典顺序排列。回想一下，对于任意m≥1和任意（i1，…，in）∈nm，这样i1+i2+······+in=m，我们有

.

更一般地，对于任何m≥2，利用多项式定理，我们可以定义一个特征嵌入，定义由κ（x，y）=（κ1（x，y））m给出的核函数κ，其中

，

其中n-元组（i1，…，in）按字典顺序排列。

例53.5。对于任何正实常数r>0，常数函数k（x，y）=r为

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

一个对应于特征图的核函数，由_（x，y）=√r给出。

根据定义，给出的函数是一个核函数。

（特征图是从RN到自身的标识图）。我们刚刚看到，对于任何正实常数r>0，该常数都是一个核函数。例53.1中，函数）是一个核函数，对于任何整数d≥1，by

例53.3，函数k d由

，

是RN上的内核函数。根据二项式，

.

通过示例53.1，该内核函数的特征映射是d+1内核映射rd−mhx、yim的特征的串联。通过示例53.3，内核映射rd−mhx，yim的特征映射的组件是函数的重加权。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

用（I1，…，in）∈nn。因此，核函数κd的特征图的组成部分是函数的重加权。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

用（I1，…，in）∈nn。很容易看出这个特征空间的尺寸是。

多项式核κD有许多变化；所有嵌入核的子集、方差分析核；见Shawe–Taylor和Christianini[154]，第三章。

在下一个示例中，集合X不是向量空间。

例53.6。设d为有限集，x=2d为其幂集。如果d_=n，设h=rx～r2n。我们假设以某种方式枚举d的子集，使r2n的每个坐标对应于其中一个子集。例如，如果d=1,2,3,4，则让

U1=∅U2=1 U3=2 U4=3

U5=4 U6=1,2 U7=1,3 U8=1,4

U9=2,3 U10=2,4 U11=3,4 U12=1,2,3

U13=1,2,4 U14=1,3,4 U15=2,3,4 U16=1,2,3,4。

设_：x→h为特征图，定义如下：对于任意子集a，u∈x，

（

1如果U A

⑨（a）U=

否则为0。

例如，如果a1=1,2,3，我们得到向量

（1,2,3）=（1,1,1,1,0,1,0,1,0,0,1,0,0,0,0,0,0,0,0），

如果a2=2,3,4，我们得到矢量

（2,3,4）=（1,0,1,1,1,1,0,0,0,1,1,0,0,0,1,0）。

对于D的任意两个子集A1和A2，很容易检查

h_（a1），（a2）i=2 a1 a2，

a1和a2的公共子集的数目。例如，A1 A2=2,3，和

h_（a1），_（a2）i=4.

因此，函数k:x×x→r由

κ（a1，a2）=2 a1 a2，a1，a2 d

是一个内核函数。

内核函数具有以下重要特性。

提案53.1.设x为任意非空集，设h为任意（复杂）希尔伯特空间，设_：x→h为任意函数，设k:x×x→c为核，由

κ（x，y）=h（x），（y）i，x，y∈x.

对于x的任何有限子集s=x1，…，x p，如果ks是p×p矩阵

KS＝（κ（Xj，Xi））1，i，j，ω＝p＝（H*（Xj），（Xi）i）1，i，j，ωp，

然后我们得到u ks u≥0，对于所有u cp。

证据。我们有

，

如要求。

命题53.1提出了对内核函数的第二种方法，该方法不假定提供了特征空间和特征映射。我们将在第53.2节中看到这两种方法是等效的。第二种方法在实践中很有用，因为通常很难以简单的方式定义特征空间和特征映射。

定义53.2.设x为非空集。对于x的每个有限子集s=x1，…，x p，如果ks是p×p矩阵，那么函数k:x×x→c是一个正定核。

KS＝（κ（Xj，Xi））1，i，j，ωp

我们称之为克矩阵

，对于所有u∈cp。

注意，如果u=06，定义53.2不要求u ks u>0，因此术语正定有点滥用，使用术语正半定更合适。然而，似乎习惯上使用“正定核”，甚至是“正定核”。

提案53.2.设k:x×x→c为正定核。然后，对于所有x∈x，k（x，x）≥0，对于x的任何有限子集s=x1，…，x p，p×p矩阵k由

KS＝（κ（Xj，Xi））1，i，j，ωp

是赫米提安，也就是说，ks=ks。

证据。第一个属性通过选择s=x很明显。我们有

（u+v）ks（u+v）=u ksu+u ksv+v ksu+v ksv，

| 由于（u+v）ks（u+v），u ksu，v ksv≥0，我们推断     |       |
| -------------------------------------------------- | ----- |
| 2a=u ksv+v ksu   一定是真的。用IU代替U，我们看到了 | （1） |
| 2b=−iu ksv+iv ksu                                  | （2） |

也必须是实数，通过将方程（2）乘以i并将其加到方程（1）中，我们得到

u ksv=a+ib.（3）

从式（1）中减去式（3），我们得到

然后

\-

对于所有u，v∈c，这意味着ks=ks。

如果mapκ：x×x→r是实数，那么我们有如下的标准，即κ是一个只涉及实数向量的正定核。

提案53.3.如果k:x×x→r，那么对于任何有限子集s x1，…，x p of x，p×p实矩阵k，由下式给出

ks=（k（xk，xj））1≤j，k≤p

是对称的，即，和

，对于所有u∈rp。

证据。如果κ是实值正定核，那么这个命题就是53.2命题的一个微不足道的结果。

相反，假设κ是对称的，并且它满足命题的第二个条件。我们需要证明，对于复向量，κ是一个正定核。如果我们写UK=AK+IBK，那么

.

因此，u ksu是真实的，iff ks是对称的。

因此，我们做出以下定义。

定义53.3.如果k（letx，y）=x是一个非空集，则确定核。一个函数k（y，x）对于所有x，y∈x，对于每个有限子集，k:x×x→r是x的（real）正x1，…，x p，如果ks是p×p实对称矩阵

KS＝（κ（Xi，Xj））1，i，j，ωp，

然后我们有了

，对于所有u∈rp。

除其他外，下一个命题表明一个正定核满足柯西-施瓦兹不等式。

提案53.4.厄米提亚2×2矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.gif)

当且仅当a≥0、d≥0和ad−b 2≥0时为正半定。

设k:x×x→c为正定核。对于所有x，y∈x，我们有κ（x，y）2≤κ（x，x）κ（y，y）。

证据。对于所有的x，y∈c，我们有

.

如果a是半正定的，那么我们已经知道a≥0和d≥0。如果a=0，则

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)

我们必须使b=0，否则我们可以使bxy+bxy，它是bxy的两倍实部，如我们想要的那样为负。在这种情况下，ad−b 2=0。

如果a>0，则

.

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.gif)

因此，如果ad−b 2<ad0−，我们可以选择b 2≥0。相反，y 6=0，x=−（by）/a，所以上面的表达式是负数。

如果x=y，则κ（x，y）2≤κ（x，x）κ（y，y）的不等式是微不足道的。如果x 6=y，则不等式通过将正半定准则应用于矩阵而得到。

，

如要求。

由舒尔（1911）提出的以下性质表明，两个正定核的点积也是正定核。

提案53.5。（I.Schur）如果k 1:x×x→c和k 2:x×x→c是两个正定核，那么由k（x，y）=k 1（x，y）k 2（x，y）给出的函数k:x×x→c对于所有x，y∈x也是一个正定核。

证据。证明了如果a=（ajk）和b=（bjk）是两个厄米半正定p×p矩阵，那么它们的点积c=a b=（ajkbjk）（也称为hadamard或schur积）。回想一下，厄米特半正定矩阵a可以对角化为a=u∧u，其中∧是一个带非负项的对角矩阵，u是一个单位矩阵。让∧1/2是由∧中对角线项的正平方根组成的对角线矩阵。然后我们有了

A=U∧U=U∧1/2∧1/2U=U∧1/2（U∧1/2）。

因此，如果我们设置r=u∧1/2，我们有

A=RR，

也就是说

.

那么对于任何u∈cp，我们有

.

既然b是半正定的，对于每个固定的h，我们有

，

如我们所见，让z=（u1r1h，…，uprph）

相反，两个对称半正定矩阵A和B的常积AB可能不是对称半正定的；示例见第7.9节。

以下是从旧核中获得新的正定核的其他方法。

提案53.6.设k 1:x×x→c和k 2:x×x→c为两个正定核，f:x→c为函数，ψ：x→rn为函数，k 3:rn×rn→c为正定核，a∈r为任意正实。那么下面的函数就是正定核：

.

（5）如果b是一个对称的半正定n×n矩阵，那么mapκ：rn×rn→r由

κ（x，y）=x>

是一个正定核。

证据。（1）对于x的每个有限子集s=x1，…，x p，如果k1是p×p矩阵

k1=（k 1（xk，xj））1≤j，k≤p

如果k2是p×p矩阵

k2=（κ2（xk，xj））1≤j，k≤p，

那么对于任何u∈cp，我们有

u（k1+k2）u=u k1u+u k2u≥0，

因为u k1u≥0和u k2u≥0，因为κ2和κ2是阳性的定核，这意味着k1和k2是阳性的半定核。

(2)   我们有u（ak1）u=au k1u≥0，

因为a>0且u k1u≥0。

(3)   对于x的每个有限子集s=x1，…，x p，如果k是p×p矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image016.gif)

K=（K（XK，XJ））1≤J，K≤P=（F（XK）F（XJ））1≤J，K≤P

然后我们有了

.

(4)   对于x的每个有限子集s=x1，…，x p，p×p矩阵k由

k=（k（xk，xj））1≤j，k≤p=（k 3（ψ（xk），ψ（xj）））1≤j，k≤p

是对称的半正定的，因为κ3是一个正定核。

(5)   在53.5号提案的证明中（与实际情况相适应），有一个矩阵r

B=RR>，

所以κ（x，y）=x>by=x>r r>y=（r>x）>r>y=hr>x，r>yi，

因此，κ是由特征映射（x）=r>x从rn到自身给出的核函数，根据命题53.1，它是一个对称的正定核。

提案53.7.设k 1:x×x→c为正定核，p（z）为非负系数多项式。然后下面定义的函数k也是正定核。

*(1)*     κ（x，y）=p（κ1（x，y））。

*(2)*     κ（x，y）=eκ1（x，y）。

*(3)*     如果x是带内积h−、−ix和相应的范数k kx的实希尔伯特空间，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image018.gif)

对于任何σ>0。

证据。（1）如果p（z）=amzm+····+a1z+a0，则

p（k 1（x，y））=am k 1（x，y）m+······+a1 k 1（x，y）+a0。

由于k=0，…，m的ak≥0，根据命题53.5和命题53.6（2），1≤k≤m的每个函数akκ√i（x，y）k是一个正定核，根据命题53.6（3），f（x）=a0，常数函数a0是一个正定核，根据命题53.6（1），p（k 1（x，y））是一个正定核。有组织的定核。

(2)              我们有

.

（1）部分和

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image020.gif)

是正定核，由于eκ1（x，y）是正定核的（均匀）点限，所以也是正定核。

(3)              根据命题53.6（2），由于map（x，y）7→hx，yix显然是一个正定核（特征映射是一个恒等式），并且由于σ=06，函数（x，y）7→hx，yix/σ2是一个正定核，因此由（2）可知，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image022.gif)

是一个正定核。设f:x→r为

.

然后根据第53.6（3）号提案，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image024.gif)

是一个正定核。根据命题53.5，功能κ1κ2是一个正定核，即

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image026.gif)

是一个正定核。

正定核

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image028.gif)

称为高斯核。这个内核需要一个无限维空间中的特征映射，因为它是不同内核的无穷和。

注：如果κ1是一个正定核，则命题53.7（3）的证明立即适用于证明

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image030.gif)

是一个正定核。

其次，我们证明了每一个正定核都来自希尔伯特空间中的一个特征映射，它是一个函数空间。

## 53.2正定核的希尔伯特空间表示

下面的结果展示了如何从一个正定核构造一个所谓的复制核希尔伯特空间，简称Rkhs。


 

53.2。正核的希尔伯特空间表示

定理53.8。设k:x×x→c为非空集x上的一个正定核，对于每个x∈x，设k x:x→c为

κx（y）=κ（x，y），y∈x。

设h0为函数族（κx）∈x所跨越的x到c函数的向量空间cx的子空间，设_：x→h0为（x）=κx给出的映射，h0上有一个厄米特内积H−、−i，这样

κ（x，y）=h（x），（y）i，对于所有x，y∈x。

h0的完成h是希尔伯特空间，图η：h→cx由

ε（f）（x）＝Hf，κXi，x x，

是线性的和内射的，所以h可以用cx的子空间来标识。我们也有

κ（x，y）=h（x），（y）i，对于所有x，y∈x。

对于所有f0 H0和x x，f，κXi= f（x），

被称为复制财产的财产。

证据。对于任意两个线性组合，用x j，yk∈x和αj，βk∈c，定义hf，gi

.（？）

乍一看，上述表达式似乎依赖于f和g的线性表达式。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image031.gif)

组合，但由于κ（xj，yk）=κ（yk，xj），观察

，（）

由于第一项和第三项对于表示f和g的所有线性组合都是相等的，因此我们得出结论（†）仅取决于f和g，而不取决于它们作为线性组合的表示。

很明显（†）定义了一种赫米特亮片形式。对于每一个f∈h0，我们有

，

因为κ是一个正定核。对于任何有限子集f1，…，h0的fn和任何z∈cn，

，

结果表明，从h0×h0到c的map（f，g）7→hf，gi是一个正定核。注意，对于所有f∈h0和所有x∈x，（†）意味着

，

被称为复制财产的财产。上面的意思是

Hκx，κyi=κ（x，y）。（）

通过对正定核（f，g）7→hf，gi的53.4号命题，我们得到

εHf，κXi 2，HF，FIHκX，κXI，

也就是说，

| f（x）2≤hf，fiκ（x，x）、

sinceso h f，f_（ix=0）=意味着κx，我们有f（x）=0，——因为alli是一个Hermitian内积onx∈x，这意味着h−，h−0i，by（定义为（）和†）是正定的。因此，H−

κ（x，y）=h（x），（y）i，对于所有x，y∈x。

设h为完成h0的希尔伯特空间，使h0在h中稠密。图η：h→cx由

ε（f）（x）＝Hf，κXi

显然是线性的，它是内射的，因为家庭（κx）x x x跨越H中稠密的H0，因此它在H中也是稠密的，因此如果Hf，κXi＝0，对于所有x x，则F＝0。

如果我们用函数η（f）来识别函数f∈h，那么我们就有了再生性质。

HF，κX= F（x），对于所有的fh h和x x x都是。

如果x是有限的，那么cx是有限维。如果x是一个可分离的拓扑空间，如果k是连续的，那么可以证明h是一个可分离的希尔伯特空间。

另外，如果k:x×x→r是实对称正定核，那么我们马上就能看到定理53.8适用于h0的实欧几里德空间和h的实希尔伯特空间。

53.2。正核的希尔伯特空间表示

注：如果x=g，其中g是局部紧群，那么函数p:g→c（不一定连续）是正半定的，如果对于所有s1，…，sn∈g和所有ξ1，…，ξn∈c，我们得到

.

因此，如果我们用

κ（s，t）=p（t-1s），

那么k是g上的一个正定核。如果p是连续的，那么我们就知道p是由希尔伯特空间h中G群的一元表示u:g→u（h）产生的，其内积为h−、−i（具有一定连续性的同态），从某种意义上说，这里有一些向量x0。使

p（s）=hu（s）（x0），x0i，对于所有s∈g。

由于美国是H上的单一运营商，

p（t−1s）=hu（t−1s）（x0），x0i=hu（t−1）（u（s）（x0）），x0i

=hu（t）（u（s）（x0）），x0 i=hu（s）（x0）），u（t）（x0）i，

这表明

κ（s，t）=hu（s）（x0）），u（t）（x0）i，

因此，图_：g→h由_（s）=u（s）（x0）给出。

是特征空间H中的一个特征映射。这个定理是由GelfandRaikov（1943）提出的。

定理53.8的证明与Godement关于正型函数与一元表示之间对应关系的上述结果的部分证明基本相同；见Helgason[89]，第四章，定理1.5。定理53.8更为一般，因为它不假定x是一个群，但当g是一个群时，特征映射是由一个统一表示产生的。

集合上的内核可以用度量来定义。

例53.7。设（d，a）为可测量空间，其中d为非空集，a为d上的σ-代数（可测量集）。设x为a的一个子集。如果μ是（d，a）上的正测量值，并且μ是有限的，这意味着μ（d）是有限的，那么我们可以定义图k 1:x×x→r，由

κ1（a1，a2）＝（a1 a2），a1，a2 x。

我们可以证明κ是一个核函数，如下所示。设h=l2μ（d，a，r）为可积函数的希尔伯特空间，其内积为

Z



f，g=f（s）g（s）d礹（s），

D

并设_：x→h为特征嵌入，由

⑨（a）=χa，a∈x，

A的特征函数，那么我们有

Z

κ1（a1，a2）＝（a1a2）＝χa1 a2（s）dµ（s）

D

Z

=χa1（s）χa2（s）dµ（s）=hχa1，χa2i

D

=h_（a1），_（a2）i.

上面的内核称为交集内核。如果我们假设μ是标准化的，那么μ（d）=1，那么我们也有联合补码内核：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image032.gif)

κ2（a1，a2）=（a1 a2）=1（a1 a2）。

核κ1和κ2的总和κ3是一致核：

κS（a1，a2）=1−（a1−a2）−（a2−a1）。

可以设计许多其他类型的内核，特别是图形内核。有关内核的全面介绍，请参阅sch–olkopf和smola[141]以及shawe–taylor和Christianini[154]。

## 53.3核PCA

作为核函数的一个应用，我们讨论了主成分分析方法（PCA）的推广。假设我们在一些输入空间x中有一组数据s=x1，…，xn，并假设我们在（真实）特征空间（f，h−，−i）中嵌入了x的：x→f，但我们只能访问内核函数κ（x，y）=h（x），（y）i。我们想对集合（s）=（x）进行PCA分析。1），…，_（xn）。

有两个障碍：

(1)    我们需要将数据中心化，并计算成对中心数据的内积。更准确地说，如果_（s）的质心是

，

然后我们需要计算内积h_（x）−_（y）−i。

53.3。核PCA

(2)    让我们假设F＝RD与标准欧几里得内积，并且数据点（XI）表示为N×D矩阵X的行向量Xi（因为它是Curm）。内积κ（Xi，XJ）＝h（Xi），（xJ）i由核矩阵k= xxx给出。请注意，用这种表示，（Xi）是D维列向量，并且（Xi）＝Xi＞。然而，主分量yk（视为n维列向量）的jth分量（yk）j是由xbj=xj−μ投影到方向uk（视为d维行向量）给出的，该方向是矩阵的单位特征向量（x−μ）>（x−）（其中xb=x−）。礹是第j行为）的矩阵，由内积给出。

hxj−μ，uki=（yk）j；

见定义21.2（第一卷）和定理21.11（第一卷）。问题是，我们知道矩阵（x−礿）（x−礿）>是从（1）得到的，因为它可以用k表示，但我们不知道（x−礿）>（x−礿）是什么，因为我们没有访问xb=x−礿的权限。

这两个困难都很容易克服。对于（1），我们有

.

对于（2），如果K是核矩阵k=（κ（Xi，xJ）），则对应于核函数κ的核矩阵KB由

Bκ（x，y）=h（x）−_，（y）−_i b

可以用k表示。设1为列向量（维度n），其条目均为1。则11>是n×n矩阵，其条目均为1。如果a是n×n矩阵，那么1>a是由a列和组成的行向量，a1是由a列和组成的列向量，1>a1是a中所有项的和，那么很容易看出核函数k对应的核矩阵是给定的。通过

乙

K11。

假设xb=x−礹具有秩r。要克服第二个问题，请注意，如果

xb=v du>

是XB的SVD，那么

xb>=ud>v>

是xb>的一个svd，d>的r×r次矩阵由d>（和d）的第一行r和r列组成，是由xb的奇异值σ1≥·············································由V（1≤K≤R）的前r列v k组成

ur=xb>vr∑−r 1。

此外，是的非零特征值，并且vr的列是kb的相应的单位特征向量。从

ur=xb>vr∑−r 1

Ur的第k列Uk（是与特征值σk2相关的xb>xb的单位特征向量）由下式给出：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image034.gif)

因此，根据下式给出了[（x）到英国的投影

*n+

H[[（x），uCi]＝（x），x＝k＝1（vk）i〔（Xi）〕

i＝1

n

= x，k，k，1，（d），[（x）e（x）e＝x，k＝1，（i）。

I=1 I=1

因此，主分量YK在主方向UK的第j个分量由下式给出：

.

将核PCA推广到（实）特征空间（f，h−−i）中x的一般嵌入，其中核矩阵k由

Kij= H*（Xi），（XJ）I，

步骤如下。设r为kb的秩，其中

K11

设为kb的非零特征值，v1，…，vr为相应的单位特征向量。符号

αk=σk−1vk


 

通常使用，其中αk被称为双变量。列向量yk（1≤k≤r）由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image036.gif)

被称为数据集s=x1，…，xn在方向b（即使矩阵xb未知）的kth内核主成分（简称kth内核PCA）。

在下一节中，我们给出了在岭回归泛化中使用内核函数的另一个说明（参见第52.1节）。

## 53.4ν-sv回归

设{（x1，y1），…，（xm，ym）}是一组观测数据，通常称为训练数据集，用Xi→Rn和Yi-r r。我们的目标是学习F（x）＝w＞x－b的仿射函数F，它符合训练数据集，但不惩罚低于给定的0的误差。因此，我们尝试将一个具有半径的管与数据相匹配，但是我们也允许误差，在某种意义上，一些数据XI可以满足某些Zi＞0的相等，或者对于某些Zi0＞0的等式（f（Xi））。在这种情况下，XI位于管的半径之外。松弛变量ξi和ξi0的大小和大小之间的权衡是通过使用两个常数ν≥0和c>0来实现的。对于短的nv-sv回归，nv-支持向量回归的方法由以下最小化问题规定：nv-sv回归：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image038.gif)

最小化变量w、b、ξ和ξ0。约束是仿射的。

首先，观察方程

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image040.gif)

只有在以下情况下才能同时保持

，

也就是说，

，

因为0，只有当=0时才会发生这种情况，然后

西> B＝易。特别是，如果>0，则方程式

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image042.gif)

不能同时保持。此外，由于w＞X+B+Yi＝（w＞Xi，b，y），对于最优解，如果w＞Xi→B→Yi为0，则Zi0 i0＝0，因为不等式成立。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image044.gif)

基本满足（因为0），如果W*Xi，B，Yi小于0，则类似地，Zi＝0。因此，我们得到了方程

（ξξ0）

观察如果v>1，则上述程序的最佳解必须产生

实际上，如果大于0，我们可以减少一小部分δ>0，并增加以满足约束条件，但目标函数的变化量为−vδ+δ，这是负的，因为0不是最佳值。

驱动到零不是目标，因为通常数据不是噪声的，所以非常少的对（Xi，Yi）满足方程W＞X-B＝Yi，然后许多对（Xi，Yi）将对应于一个误差（Zi i＞0或ZiI0＞0）。因此，我们通常假设0<ν≤1。

为了构造拉格朗日，我们将拉格朗日乘子αi＞0分配到约束W*Xi，拉格朗日乘子αi0±0以上的约束条件，

拉格朗日乘数ηi≥0到约束ξi≥0，拉格朗日乘数

约束0，拉格朗日乘子β≥0到约束0。这个

拉格朗日是

，

拉格朗日也可以写成

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image046.gif)

为了找到关于原始变量的双函数g（α，α0，η，η0，β），我们将其最小化。观察拉格朗日是凸的，由于（，一个凸的开集，根据定理39.11，拉格朗日有一个最小的iff=0，所以我们计算梯度。我们得到

，

哪里

，和。

因此，如果我们设为0，我们得到方程

，（W）

.

将上述方程代入拉格朗日方程的第二个表达式中，我们发现双函数g与变量β、η、η0无关，由下式得出：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image048.gif)

如果

，

以及−∞否则。

对偶程序是通过使g（α，α0）最大化或等效地通过最小化得到的。

-以下双程序：G（α，α0），结束。考虑到η，η0≥0和β≥0，我们得出

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image050.gif)

KKT条件（针对主要项目）是

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image052.gif)

如果>0，因为方程

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image054.gif)

不能同时保持，我们必须

（αα0）

从方程式中

，

我们得到方程

（三）

这些方程表明，如果ξi>0，那么，我们就有了活动约束。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image056.gif)

并且XI是一个错误，类似地，如果ZEII0> 0，那么，我们就有活动约束。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image058.gif)

XI是一个错误。

如果原始解具有w=06且>0的最优解，则通过（w）和自

）=0和αiαi0=0，

有一些i0，比如αi0>0，一些j0=6i0，比如0。在温和假设下，有一些i0，比如0，有一些j0，那么通过（），我们得到了ξi0=0，ξj0 0=0，我们得到了这两个方程。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image060.gif)

所以可以计算b和。特别地，

.

函数f（x）=w>x−b（通常称为回归估计）由以下公式给出：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image062.gif)

制约因素

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image064.gif)

这意味着数据中至多有一个分数。如果随后的结果是，如果>0和0<ν≤1，那么ν是误差分数的上界。

kkt条件意味着如果>0，那么β=0，在这种情况下

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image066.gif)

因为=0，并且由于支持向量对应于0，我们看到，ν是支持向量分数的下界。

因为w、b和f（x）的公式，

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image068.gif)

仅在数据点XI中涉及内积，并且由于对偶程序的目标函数g（α，α0）也只涉及数据点XI中的内积，所以我们可以对其进行回归。

与前面的部分一样，我们假设我们的数据点{x1，…，xM}属于一个集合x，我们假设我们具有特征空间（f，h，，i）和特征嵌入映射：x，f，但是我们只能访问核函数κ（Xi，xJ）＝h（x），（xJ）i。n数据集上的特征空间f（（x1），y1），…，（（xm），ym）。经过前面的计算，我们看到原始程序是由

核v-sv回归：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image070.gif)

最小化变量w、b、ξ和ξ0。拉格朗日由

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image072.gif)

将拉格朗日梯度设为零，也得到了方程组。

，（W）

.

利用上述方程，我们发现双函数g与变量β、η、η0无关，得到以下双程序：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image074.gif)

我们前面所说的一切也适用于核Vo-SV回归方法，除了Xi被（Xi）代替，并且必须使用内积h，，i，并且我们有公式。

！

只涉及κ的表达。

注：通过设置ν=0并保持不变，得到了一个关于ν-sv回归的变量。这种方法称为-SV回归或（线性）不敏感SV回归。相应的优化程序为-SV回归：

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image076.gif)

最小化变量w、b、ξ和ξ0。

很容易看出双程序是

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image078.gif)

约束条件

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image080.gif)

已经不存在了，但是额外的项）已经被添加到双重功能中，以防止αi和爆炸。

有一个明显的-sv回归的核心版本。可以很容易地看出，如果ν-sv回归成功并得到w，b，>0，那么具有相同c和相同值的-sv回归也成功并返回相同对（w，b）。有关这些方法的更多详细信息，请参阅sch–olkopf、smola、williamson和bartlett[143]。

注：线性惩罚函数）可以用二次惩罚函数来表示；见Shawe–Taylor和Christianini[154]（第7章）。

然而，v-sv回归的另一个变体是将该项添加到目标函数中。

新拉格朗日是

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image082.gif)

我们得到了新的方程

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image084.gif)

确定b，替换方程式

.

新的双重计划是

最小化

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image086.gif)


 