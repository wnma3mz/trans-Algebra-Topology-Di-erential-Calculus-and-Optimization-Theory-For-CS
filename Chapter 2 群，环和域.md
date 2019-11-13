# 第二章 群，环和域

在接下来的四章中，我们回顾基本的代数结构（群，环，域，向量空间），主要强调向量空间。线性代数的基本概念，如向量空间，子空间，线性组合，线性无关，基数，商空间，线性映射，矩阵，基数的变化，直和，线性形式，双空间，超平面，线性映射的转置，作为回顾。

## 2. 群，子群，陪集

实数的集合 $\mathbb{R}$ 具有两个运算 $+$：$\mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}$（加法）和 $*$：$\mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}$（乘法），其满足使 $\mathbb{R}$ 成为 $+$ 下的阿贝尔群的性质，并且 $\mathbb{R}  - \{0\} = \mathbb{R}^*$ 进入 $*$ 下的阿贝尔群。回想一下群的定义。

**定义2.1.A** *群*是一个具有二元运算·：$G \times G \rightarrow G$ 的集合 $G$，它将元素 $a\cdot b\in G$ 与每对元素 $a\cdot b \in G$ 相关联，并具有以下性质：$\cdot$ 是关联意义，具有一个标识元素 $e\in G$，并且 $G$ 中每个元素都是可逆的（w.r.t. $\cdot$ ）。更明确地，这意味着以下所有等式适用于 $a, b, c \in G$

（G1）$a \cdot(b \cdot c)=(a \cdot b) \cdot c$（结合性）；

（G2）$a \cdot e=e \cdot a=a$（一致性）；

（G3）对于每个 $a \in G$，有一些 $a^{-1} \in G$，这样 $a \cdot a^{-1}=a^{-1} \cdot a=e$.（可逆性）。

群 $G$ 是*阿贝尔*（或*交换的*），如果

$a\cdot b=b\cdot a$，对于所有 $a,b\in G$

集合 $M$ 的一个操作：$M \times M\rightarrow M$ 和满足条件（G1）和（G2）的元素 $e$ 被称为*单体*。例如，自然数的集合$\mathbb{N} =\{0,1,...,n...\}$ 是加法下的（交换）单体。然而，它不是一个群。

下面给出了一些组的例子。

**例2.1**

1. 整数的集合 $\mathbb{Z}=\{\ldots,-n, \ldots,-1,0,1, \ldots, n, \ldots\}$ 是加法下的阿贝尔群，具有单位元素0。然而，$\mathbb{Z}^{*}=\mathbb{Z}-\{0\}$ 不是乘法群。

2. 有理数（$p, q \in \mathbb{Z}$ 和 $q\neq0$ 的分数 $p/q$ ）的集合 $\mathbb{Q}$ 是一个加上的阿贝尔群，单位元素为0。集合 $\mathbb{Q}^{*}=\mathbb{Q}-\{0\}$ 也是一个单位元素未1的乘法下的阿贝尔群。

3. 对于任何非空集合 $S$，$f : S \rightarrow S$ 的双射集合，也称为 $S$ 的*排列*，是函数组合下的一个群（即 $f$ 和 $g$ 的乘法是组合 $g \circ f$ ），同一元素是同一函数 $\rm id_S$。只要 $S$ 有两个以上的元素，这个群就不是阿贝尔群。集合 $S=\{1, \ldots, n\}$ 的置换群通常表示为 $\mathfrak{S}_{n}$，称为 $n$ 元素上的*对称*群。

4. 对于任意正整数 $p \in \mathbb{N}$，在 $\mathbb{Z}$ 上定义一个关系，表示为 $m \equiv n$（mod p），如下所示：

$$m \equiv n \quad(\bmod p) \quad \text { iff } \quad m-n=k p \quad \text { for some } k \in \mathbb{Z}$$

​	读者将很容易地验证这是一个等价关系，而且它与加法和乘法兼容，这意味着如果 $m_1\equiv n_1$（mod p）和 $m_2 \equiv n_2$（mod p），那么 $m_{1}+m_{2} \equiv n_{1}+n_{2}$（mod p）和 $m_{1} m_{2} \equiv n_{1} n_{2}$。因此，我们可以定义等价类集（mod p）的加法运算和乘法运算：

$[m]+[n]=[m+n]$

和

$[m]\cdot[n]=[mn]$

​	读者将很容易地验证加上余项（mod p）是否得到一个 $[0]$ 为零的阿贝尔群结构。该组表示 $\mathbb{Z} / p \mathbb{Z}$。

5. 具有实（复）系数的 $n\times n$ 可逆矩阵 $A$ 的集合使得 $\rm det(A) = 1$ 是矩阵乘法下的一个群，其单位元素为单位矩阵 $I_n$。这个群称为*一般线性群*，通常用 $\mathbf{G L}(n, \mathbb{R}) $ （或 $\mathbf{G} \mathbf{L}(n, \mathbb{C})$ ）表示。

6. 具有实（复）系数的 $n\times n$ 可逆矩阵 $A$ 的集合使得 $\rm det(A) = 1$ 是矩阵乘法下的一个群，其单位元素是单位矩阵 $I_n$。这个群称为*特殊线性群*，通常用  $\mathbf{SL}(n, \mathbb{R})$ （或 $\mathbf{SL}(n, \mathbb{C})$）表示。

7. 具有实数系数的 $n \times n$ 矩阵 $Q$ 的集合，这样

$Q Q^{\top}=Q^{\top} Q=I_{n}$

​	是矩阵乘法下的一个群，其中的单位元素是单位矩阵 $I_n$；我们有 $Q^{-1}=Q^{\top}$。这个群称为*正交群*，通常用 $\mathbf{O}(n)$ 表示。

8. 具有实数系数的 $n \times n$ 可逆矩阵 $Q$ 的集合，使得

$Q Q^{\top}=Q^{\top} Q=I_{n} \quad \text { and } \quad \operatorname{det}(Q)=1$

​	是矩阵乘法下的一个群，其中的单位元素是单位矩阵 $I_n$ ；如（6）所示，我们得到 $Q^{-1}=Q^{\top}$ 。这个群称为*特殊正交群*或*旋转群*，通常用 $\mathbf{SO}(n)$ 表示。

（5）–（8）中的群是 $n \geq 2$ 的非阿贝尔群，但作为阿贝尔群（但 $\mathbf{O}(2)$ 不是阿贝尔群）的 $\mathbf{SO}(2)$ 除外。

通常用 $+$ 表示阿贝尔群 $G$ 的运算，在这种情况下，元素 $a\in G$ 的逆 $a^{-1}$ 用 $-a$ 表示。

群的单位元素是*唯一*的。事实上，我们可以证明一个更一般的事实：

**命题2.1** *如果一个二元运算：$M \times M \rightarrow M$ 是关联的，如果 $e^{\prime} \in M$ 是左恒等式，$e^{\prime \prime} \in M$ 是右恒等式，这意味着*

$e^{\prime} \cdot a=a \quad \text { for all } \quad a \in M$ （G2l）

和 $a \cdot e^{\prime \prime}=a \quad \text { for all } \quad a \in M$ （G2r）

得到，$e^{\prime}=e^{\prime \prime}$

*证明*  如果方程（G2l）中 $a=e^{\prime \prime}$，我们得到 $e^{\prime} \cdot e^{\prime \prime}=e^{\prime \prime}$，

如果我们在方程（G2r）中让 $a=e^{\prime}$，我们得到 $e^{\prime} \cdot e^{\prime \prime}=e^{\prime}$

因此，$e^{\prime}=e^{\prime} \cdot e^{\prime \prime}=e^{\prime \prime}$，就像声明的那样。

命题2.1意味着独异点的同一元素是唯一的，并且由于每个群都是一个独异点，所以一个群的同一元素是唯一的。此外，一个群中的每个元素都有一个*唯一的逆*矩阵。这是一个更普遍的事实的结果：

**命题2.2** *在具有单位元 $e$ 的独异点 $M$ 中*，如果某个元素 $a \in M$ 有左逆 $a^{\prime} \in M$ 和右逆 $a^{\prime \prime} \in M$，这意味着 $a^{\prime} \cdot a=e$ （G3l） 与 $a \cdot a^{\prime \prime}=e$ （G3r）得到，$a^{\prime}=a^{\prime \prime}$

*证明*  利用（G3l）和 $e$ 是一个单元元素，我们有 $\left(a^{\prime} \cdot a\right) \cdot a^{\prime \prime}=e \cdot a^{\prime \prime}=a^{\prime \prime}$

同样的，使用（G3r）和 $e$ 是一个单位元素，我们有 $a^{\prime} \cdot\left(a \cdot a^{\prime \prime}\right)=a^{\prime} \cdot e=a^{\prime}$

然而，由于 $M$ 是独异点，运算 $ \cdot$ 是关联的，所以

$a^{\prime}=a^{\prime} \cdot\left(a \cdot a^{\prime \prime}\right)=\left(a^{\prime} \cdot a\right) \cdot a^{\prime \prime}=a^{\prime \prime}$

如要求。

**注**：公理（G2）和（G3）可以通过只要求（G2r）（正确身份的存在）和（G3r）（每个元素都存在一个正确的反义词）（或（G2l）和（G3l））而稍微减弱。证明群公理（G2）和（G3）遵循（G2r）和（G3r）是一个很好的练习。

**定义2.2.** 如果一个 $G$ 组有有限个 $n$ 个元素，我们就说 $G$ 是一个 $n$ *阶*的群。如果 $G$ 是无限的，我们就说 $G$ 有*无限阶*。群的阶通常用 $|G|$ 表示（如果 $G$ 是有限的）。

对于群 $G$，对于任意两个子集 $R, S \subseteq G$，令 $R S=\{r \cdot s | r \in R, s \in S\}$

特别地，对于任何 $g \in G$，如果 $R=\{g\}$，写成 $g S=\{g \cdot s | s \in S\}$

同样地，如果 $S= \{g\}$，写成 $R g=\{r \cdot g | r \in R\}$

从现在开始，我们将拿掉乘号，并将 $g_1g_2$ 写为 $g_1\cdot g_2$。

**定义2.3.** 令 $G$ 为一个群。对于任意 $g\in G$，设 $L_g$，通过 $g$ *左移得到*，得 $L_g(a)=ga$ ，并且所有 $a\in G$，和 $R_g$，由 $g$ *右移得到*，由 $R_g(a)=ag$ ，并且所有 $a\in G$。

​	通常使用以下简单的事实。

**命题2.3.** *给定群 $G$* ，$L_g$ 和 $R_g$ 称为双射。

*证明* 我们证明了 $L_g$ ，那么证明 $R_g$ G是相似的。

​	如果有 $L_g(a)=L_g(b)$，那么 $ga=gb$，在左边乘以 $g^{−1}$，我们得到 $a=b$，所以 $L_g$注入。对于任何$b\in G$，我们有 $L_g(g^{-1}b)=gg^{-1}b$，所以 $L_g$ 是满射的。因此，$L_g$ 是双射。

**定义2.4.** *给定群 $G$*，$G$ 的子集 $H$ 是 $G$ iff的*子群*。

(1)   $G$ 的单位元 $e$ 也属于 $H$（ $e\in H$ ）；

(2)   对于所有的 $h_1，h_2\in H$，我们有 $h_1h_2\in H$；

(3)   对于所有的 $h\in H$，我们有 $h^{−1}\in H$。

​	下列命题的证明留作练习。

**命题2.4.** *给定群 $G$*，子集 $H \subseteq G$ 是 $G$ 的一个*子群*，当 $h_1h_2\in H$，则 $h_1h_2^{-1}\in H$。

​	如果群 $G$ 是有限的，那么可以使用以下标准。

**命题2.5.** *给定有限群 $G$*，子集 $H \subseteq G$ 是 $G$ iff 的子群

（1）$e\in H$；

（2）$H$ *在乘法下闭合*。

*证明* 我们只需要证明定义2.4的条件（3）成立。对于任何 $a\in H$，由于左移 $L_a$ 是双射的，它对 $H$ 的限制是单射的，而由于 $H$ 是有限的，它也是双射的。由于 $e\in H$，存在唯一的 $b\in H$，因此 $L_a(b)=ab=e$。但是，如果 $a^{-1}$ 是 $G$ 中 $a$ 的倒数，我们也有 $L_a(a^{-1})=aa^{-1}=e$，并且由于 $L_a$的单射，我们得到 $a^{−1}=b\in H$。

**例2.2.**

1. 对于任意整数 $n\in \mathbb{Z}$，集合 $n \mathbb{Z}=\{n k | k \in \mathbb{Z}\}$ 是群 $\mathbb{Z}$ 的子群。
2. 矩阵集 $\mathrm{GL}^{+}(n, \mathbb{R})=\{A \in \mathrm{GL}(n, \mathbb{R}) | \operatorname{det}(A)>0\}$ 是群 $\mathrm{GL}(n, \mathbb{R})$ 的子群。
3.    群 $\mathrm{SL}(n, \mathbb{R})$ 是群 $\mathrm{GL}(n, \mathbb{R})$ 的一个子群。

4. 群 $\rm O(n)$ 是群 $\mathrm{GL}(n, \mathbb{R})$ 的一个子群。

5. 群 $\rm SO(n)$ 是群 $\rm O(n)$ 的一个子群，是群 $\mathrm{SL}(n, \mathbb{R})$ 的一个子群。

6. 不难证明每个2×2旋转矩阵 $R \in \mathrm{SO}(2)$ 都可以写成

   $R=\left(\begin{array}{cc}{\cos \theta} & {-\sin \theta} \\ {\sin \theta} & {\cos \theta}\end{array}\right), \quad \text { with } \quad 0 \leq \theta<2 \pi$

   然后，通过观察矩阵，可以将 $\mathrm{SO}(2)$ 视为 $\mathrm{SO}(3)$ 的一个子群。

   $R=\left(\begin{array}{cc}{\cos \theta} & {-\sin \theta} \\ {\sin \theta} & {\cos \theta}\end{array}\right)$

   作为矩阵

   $Q=\left(\begin{array}{ccc}{\cos \theta} & {-\sin \theta} & {0} \\ {\sin \theta} & {\cos \theta} & {0} \\ {0} & {0} & {1}\end{array}\right)$

7. 形如2×2上三角矩阵集

   $\left(\begin{array}{cc}{a} & {b} \\ {0} & {c}\end{array}\right) \quad a, b, c \in \mathbb{R}, a, c \neq 0$

   是群 $\mathrm{GL}(2, \mathbb{R})$ 的子群。

8. 由四个矩阵组成的集合 $V$

   $\left(\begin{array}{cc}{ \pm 1} & {0} \\ {0} & { \pm 1}\end{array}\right)$

   是群 $\mathrm{GL}(2, \mathbb{R})$ 的一个子群，称为 *Klein four-group*。

**定义2.5.** 如果 $H$ 是 $G$ 的一个子群，任意元素满足 $g\in G$ ，那么$gH$ 形式的集合称为 $G$ 中 $H$ 的*左模集*，$Hg$ 形式的集合称为 $G$ 中 $H$ 的*右模集*，左模集（分别，右模）引出一个等价关系～定义如下：对于所有 $g_{1}, g_{2} \in G$，$g_1～g_2$  iff $g_1H=g_2H$（同样，$g_1～g_2$  iff $Hg_1=Hg_2$）。显然，是一个等价关系。

​	现在，我们声明以下事实：

**命题2.6.** *给定群 $G$ 和 $G$ 的任意子群 $H$，我们得到 $g_{1} H=g_{2} H$ iff $g_{2}^{-1} g_{1} H=H \text { iff } g_{2}^{-1} g_{1} \in H$，对于所有 ,$g_{1}, g_{2} \in G$。*

*证明* 如果我们把双射同时应用于g1h和g2h，我们得到

并且，既然1∈h，我们得到g2−1g1∈h，反之，如果g2−1g1∈h，既然h是一个群，那么左边的翻译是h的双射，所以g2−1g1h=h，因此，g2−1g1h=h iff g2−1g1∈h。

由此可知，元素G∈G的等价类是coset-gh（resp。汞）。因为lg是h和gh之间的双射，所以cosets gh的基数都相同。图lg-1_rg是左coset-gh和右coset-hg之间的双射，因此它们也具有相同的基数。由于不同的cosets-gh形成了g的一个划分，我们得到如下事实：

提案2.7.（拉格朗日）对于任何有限群G和G的任何子群H，H的阶H除以G的阶N。

定义2.6.给定有限群G和G的子群H，如果n=g和h=h，则比值n/h用（g:h）表示，称为g中h的指数。

指数（g:h）是g中h的左（右）陪集的个数。命题2.7可以表示为

| G=（G:H）H。

h在g中的左余割集（通常不是一个群）表示g/h。g/h的“点”是通过将coset中的所有元素“折叠”成单个元素来获得的。

例2.3.

\1.    设n为任意正整数，并考虑z的nz子群（在加法下）。0的陪集是0，任意非零整数m∈z的陪集是

m+nz=m+nk k∈z。

用m除以n，我们得到一些独特r的m=nq+r，这样0≤r≤n-1。但是我们看到r是coset m+nz中最小的正元素。这意味着在z的nz子群的陪集和残基集0,1，…，n−1模n之间存在双射，或者与z/nz相等的双射。

\2.    gl（n，r）中sl（n，r）的陪集是矩阵集。

a sl（n，r）=a b b∈sl（n，r），a∈gl（n，r）。

$\mathrm{GL}(2, \mathbb{R})$







$L_{g_{2}^{-1}}\left(g_{1} H\right)=g_{2}^{-1} g_{1} H$

$L_{g_{2}^{-1}}\left(g_{2} H\right)=H$

$g_{1} H=g_{2} H \text { iff } g_{2}^{-1} g_{1} H=H$

$g_{2}^{-1} g_{1} H=H$

$g_{2}^{-1} g_{1} \in H$

$g_{2}^{-1} g_{1} \in H$

$L_{g_{2}^{-1} g_{1}}$

$g_{2}^{-1} g_{1} H=H$

$g_{2}^{-1} g_{1} H=H \text { iff } g_{2}^{-1} g_{1} \in H$

$L_{g^{-1}} \circ R_{g}$

$|G|=(G : H)|H|$

$m+n \mathbb{Z}=\{m+n k | k \in \mathbb{Z}\}$

$0 \leq r \leq n-1$

$\{0,1, \ldots, n-1\}$

$A \mathbf{S L}(n, \mathbb{R})=\{A B | B \in \mathbf{S L}(n, \mathbb{R})\}, A \in \mathbf{G} \mathbf{L}(n, \mathbb{R})$

$\operatorname{det}(A) \neq 0$

$A=(\operatorname{det}(A))^{1 / n}\left((\operatorname{det}(A))^{-1 / n} A\right)$

$\operatorname{det}(A)>0$

$A=(-\operatorname{det}(A))^{1 / n}\left((-\operatorname{det}(A))^{-1 / n} A\right)$

$\operatorname{det}(A)<0$

$(\operatorname{det}(A))^{-1 / n} A \in \mathbf{S L}(n, \mathbb{R})$

$\operatorname{det}(A)>0$

$-(-\operatorname{det}(A))^{-1 / n} A \in \mathbf{S L}(n, \mathbb{R})$

$A \mathbf{S L}(n, \mathbb{R})$

$(\operatorname{det}(A))^{1 / n} I_{n} \text { if } \operatorname{det}(A)>0, \quad-(-\operatorname{det}(A))^{1 / n} I_{n} \quad \text { if } \quad \operatorname{det}(A)<0$

$\mathrm{SL}(n, \mathbb{R})$

$\mathbf{G L}(n, \mathbb{R})$

$\mathbf{G} \mathbf{L}^{+}(n, \mathbb{R})$

$A \mathrm{SO}(n)=\{A Q | Q \in \mathrm{SO}(n)\}, A \in \mathrm{GL}^{+}(n, \mathbb{R})$

$\mathbf{G} \mathbf{L}^{+}(n, \mathbb{R})$

$Q \mathrm{SO}(2)=\{Q R | R \in \mathrm{SO}(2)\}, Q \in \mathrm{SO}(3)$

$x \mapsto Q x \quad \text { for any rotation } Q \in \mathrm{SO}(3)$

$S^{2}=\left\{(x, y, z) \in \mathbb{R}^{3} | x^{2}+y^{2}+z^{2}=1\right\}$

$N=(0,0,1)$

$Q N \in S^{2}$

$Q \in \mathrm{SO}(3)$

$\left(g_{1} H\right)\left(g_{2} H\right)=\left(g_{1} g_{2}\right) H$

$G \rightarrow G^{\prime}$

$\varphi\left(g_{1} g_{2}\right)=\varphi\left(g_{1}\right) \varphi\left(g_{2}\right), \quad \text { for all } g_{1}, g_{2} \in G$

$g_{1}=g_{2}=e(\text { in } G)$

$\varphi(e)=e^{\prime}$

$\varphi\left(g^{-1}\right)=(\varphi(g))^{-1}$









由于a是可逆的，所以det（a）=06，如果det（a）>0，我们可以写a=（det（a））1/n（（det（a））-1/na，如果det（a）<0，我们可以写a=（det（a））1/n（（-det（a））-1/na。但如果det（a）>0，我们有（det（a））-1/na∈sl（n，r），如果det（a）>0，我们有−（−det（a））-1/na∈sl（n，r），如果det（a）<

0，所以coset asl（n，r）包含矩阵

（det（a））1/nin，如果det（a）>0，则−（−det（a））1/nin，如果det（a）<0。

由此可知，gl（n，r）和r中sl（n，r）的陪集之间存在双射。

\3.    gl+（n，r）中so（n）的陪集是矩阵集。

a so（n）=a q q∈so（n），a∈gl+（n，r）。

可以证明（使用矩阵的极性形式）gl+（n，r）中so（n）的陪集与n×n对称、正、定矩阵的陪集之间存在一个双射，它们是特征值严格为正的对称矩阵。

\4.    so（3）中so（2）的陪集是矩阵集。

q so（2）=q r r∈so（2），q∈so（3）。

群so（3）在r3中移动球面s2上的点，即对于任何x∈s2，

x 7→qx表示任意旋转q∈so（3）。

在这里，

s2=（x，y，z）∈r3 x2+y2+z2=1。

设n=（0,0,1）为球面s2上的北极。那么，不难证明so（2）正是so（3）的子群，使n保持不变。因此，陪集qso（2）中的所有旋转qr都映射到同一点qn∈s2，并且可以证明so（3）中的so（2）陪集与s2上的点之间存在双射。该图的可拓性与so（3）在s2上的作用是可传递的这一事实有关，也就是说，对于任何点x∈s2，都有一些旋转q∈so（3），使得qn=x。

在左陪集（或右陪集）上通过设置

（g1h）（g2h）=（g1g2）h，

但这种运算一般没有很好的定义，除非H子群具有特殊的性质。在示例2.3中，可以在（1）中定义coset的乘法，但在（2）和（3）中不可能。

允许在左陪集上定义乘法运算的子群H的性质是群同态核的典型性质，因此我们得出以下定义。

定义2.7.给定任意两组g和g0，函数_：g→g0是同态iff

⑨（g1 g2）＝（g1）⑨（g2），对于所有g1、g2∈g。

取g1=g2=e（g），我们看到

⑨（e）=e0，

取g1=g和g2=g-1，我们可以看到

⑨（g−1）=（⑨（g））−1.