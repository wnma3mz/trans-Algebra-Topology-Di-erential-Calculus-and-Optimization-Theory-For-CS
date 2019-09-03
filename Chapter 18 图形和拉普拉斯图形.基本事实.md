第十八章

# Graphs and Graph Laplacians; Basic Facts  图形和拉普拉斯图形.基本事实

In this chapter and the next we present some applications of linear algebra to graph theory. Graphs (undirected and directed) can be defined in terms of various matrices (incidence and adjacency matrices), and various connectivity properties of graphs are captured by properties of these matrices. Another very important matrix is associated with a (undirected) graph: the graph Laplacian. The graph Laplacian is symmetric positive definite, and its eigenvalues capture some of the properties of the underlying graph. This is a key fact that is exploited in graph clustering methods, the most powerful being the method of normalized cuts due to Shi and Malik [155]. This chapter and the next constitute an introduction to algebraic and spectral graph theory. We do not discuss normalized cuts, but we discuss graph drawings. Thorough presentations of algebraic graph theory can be found in Godsil and Royle [77] and Chung [39].
 在本章和下一章中，我们将介绍线性代数在图论中的一些应用。图（无向和有向）可以用各种矩阵（关联矩阵和邻接矩阵）来定义，图的各种连通性由这些矩阵的性质来捕获。另一个非常重要的矩阵与（无向）图有关：拉普拉斯图。拉普拉斯图是对称正定的，它的特征值捕获了底层图的一些性质。这是一个关键的事实，在图聚类方法中得到了充分利用，其中最强大的是由Shi和Malik[155]提出的归一化切割方法。本章和下一章将介绍代数和谱图理论。我们不讨论标准化切割，但讨论图形绘制。代数图论的详细介绍可在Godsil、Royle[77]和Chung[39]中找到。

We begin with a review of basic notions of graph theory. Even though the graph Laplacian is fundamentally associated with an undirected graph, we review the definition of both directed and undirected graphs. For both directed and undirected graphs, we define the degree matrix D, the incidence matrix B, and the adjacency matrix A. Then we define a weighted graph. This is a pair (V,W), where V is a finite set of nodes and W is a m × m symmetric matrix with nonnegative entries and zero diagonal entries (where m = |V |).
 我们首先回顾了图论的基本概念。尽管拉普拉斯图基本上与无向图有关，但我们回顾了有向图和无向图的定义。对于有向图和无向图，我们定义了度矩阵D、关联矩阵B和邻接矩阵A，然后定义了加权图。这是一对（v，w），其中v是一组有限的节点，w是一个m×m对称矩阵，具有非负项和零对角项（其中m=v）。

For every node vi ∈ V , the degree d(vi) (or di) of vi is the sum of the weights of the edges adjacent to vi:
 对于每个节点vi∈v，vi的阶数d（vi）（或di）是与vi相邻的边的权重之和：

.
 .

The degree matrix is the diagonal matrix
 度矩阵是对角矩阵

D = diag(d1,...,dm).
 d=诊断（d1，…，dm）。

The notion of degree is illustrated in Figure 18.1. Then we introduce the (unnormalized)
 度的概念如图18.1所示。然后我们介绍（非规范化的）

579
 五百七十九

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

Figure 18.1: Degree of a node.
 图18.1：节点的度数。

graph Laplacian L of a directed graph G in an “old-fashion” way, by showing that for any orientation of a graph G,
 有向图G的拉普拉斯L，用“旧的方式”表示，对于图G的任何方向，

BB> = D − A = L
 bb>=d−a=l

is an invariant. We also define the (unnormalized) graph Laplacian L of a weighted graph G = (V,W) as L = D−W. We show that the notion of incidence matrix can be generalized to weighted graphs in a simple way. For any graph Gσ obtained by orienting the underlying graph of a weighted graph G = (V,W), there is an incidence matrix Bσ such that
 是不变量。我们还将加权图g=（v，w）的（非规范化）拉普拉斯L定义为L=d−w。我们证明了关联矩阵的概念可以简单地推广到加权图。对于通过将加权图G=（V，W）的基础图定向而得到的任何图Gσ，存在一个关联矩阵Bσ，使得

Bσ(Bσ)> = D − W = L.
 bσ（bσ）>=d−w=l。

We also prove that
 我们也证明了

​                                                                                            for all x ∈ Rm.
 对于所有x∈rm。

Consequently, x>Lx does not depend on the diagonal entries in W, and if wij ≥ 0 for all i,j ∈ {1,...,m}, then L is positive semidefinite. Then if W consists of nonnegative entries, the eigenvalues 0 = λ1 ≤ λ2 ≤ ... ≤ λm of L are real and nonnegative, and there is an orthonormal basis of eigenvectors of L. We show that the number of connected components of the graph G = (V,W) is equal to the dimension of the kernel of L, which is also equal to the dimension of the kernel of the transpose (Bσ)> of any incidence matrix Bσ obtained by orienting the underlying graph of G.
 因此，x>lx不依赖于w中的对角线项，如果所有i，j∈1，…，m的wij≥0，则l为正半定。如果w由非负项组成，则特征值0=λ1≤λ2≤…L的λm是实的和非负的，L的特征向量有一个正交基，我们证明了图G的连通分量的个数（v，w）等于L的核的维数，也等于任意一个内点的转置（bσ）>的核的维数。通过确定G的下垫图的方向得到的Ence矩阵bσ。

We also define the normalized graph Laplacians Lsym and Lrw, given by
 我们还定义了标准化的拉普拉斯图lsym和lrw，由

Lsym = D−1/2LD−1/2 = I − D−1/2WD−1/2
 LSYM=D−1/2LD−1/2=I−D−1/2WD−1/2

Lrw = D−1L = I − D−1W,
 lrw=d−1l=i−d−1w，

and prove some simple properties relating the eigenvalues and the eigenvectors of L, Lsym and Lrw. These normalized graph Laplacians show up when dealing with normalized cuts.
 并证明了L、LSYM和LRW的特征值和特征向量的一些简单性质。这些归一化图形拉普拉斯出现在处理归一化切割。

Next, we turn to graph drawings (Chapter 19). Graph drawing is a very attractive application of so-called spectral techniques, which is a fancy way of saying that that eigenvalues and eigenvectors of the graph Laplacian are used. Furthermore, it turns out that graph clustering using normalized cuts can be cast as a certain type of graph drawing.
 接下来，我们来看看图表（第19章）。图的绘制是所谓的谱技术的一个非常有吸引力的应用，这是一种奇特的说法，即图的拉普拉斯特征值和特征向量被使用。此外，结果表明，使用归一化切割的图形聚类可以被转换为某种类型的图形绘制。

Given an undirected graph G = (V,E), with |V | = m, we would like to draw G in Rn for n (much) smaller than m. The idea is to assign a point ρ(vi) in Rn to the vertex vi ∈ V , for every vi ∈ V , and to draw a line segment between the points ρ(vi) and ρ(vj). Thus, a graph drawing is a function ρ: V → Rn.
 给出一个无向图G=（v，e），用v_=m，我们想在RN中画G，对于小于m的n（多），其思想是将RN中的点ρ（vi）赋给顶点vi∈v，对于每个vi∈v，并在点ρ（vi）和ρ（vj）之间画一条直线段。因此，图形绘制是函数ρ：v→rn。

We define the matrix of a graph drawing ρ (in Rn) as a m × n matrix R whose ith row consists of the row vector ρ(vi) corresponding to the point representing vi in Rn. Typically, we want n < m; in fact n should be much smaller than m.
 我们将图的矩阵ρ（在r n中）定义为m×n矩阵r，其中第i行由行向量ρ（vi）组成，该行向量与在rn中表示vi的点相对应。通常，我们需要n<m；实际上n应该比m小得多。

Since there are infinitely many graph drawings, it is desirable to have some criterion to decide which graph is better than another. Inspired by a physical model in which the edges are springs, it is natural to consider a representation to be better if it requires the springs to be less extended. We can formalize this by defining the energy of a drawing R by
 由于有无限多的图形绘制，因此需要有某种标准来决定哪个图形优于另一个图形。从一个边缘是弹簧的物理模型中得到启发，如果一个表示法要求弹簧的延伸度较小，那么它自然会考虑更好。我们可以通过定义绘图r的能量

 ,
 ，

where ρ(vi) is the ith row of R and kρ(vi) − ρ(vj)k2 is the square of the Euclidean length of the line segment joining ρ(vi) and ρ(vj).
 其中，ρ（vi）是r的第i行，kρ（vi）−ρ（vj）k2是连接ρ（vi）和ρ（vj）的线段欧几里得长度的平方。

Then “good drawings” are drawings that minimize the energy function E. Of course, the trivial representation corresponding to the zero matrix is optimum, so we need to impose extra constraints to rule out the trivial solution.
 那么“好的图”就是能量函数E最小化的图，当然，对应于零矩阵的平凡表示是最优的，所以我们需要施加额外的约束来排除平凡解。

We can consider the more general situation where the springs are not necessarily identical. This can be modeled by a symmetric weight (or stiffness) matrix W = (wij), with wij ≥ 0. In this case, our energy function becomes
 我们可以考虑弹簧不一定相同的更一般的情况。这可以通过对称重量（或刚度）矩阵w=（wij）来建模，wij≥0。在这种情况下，我们的能量函数变成

 .
 .

Following Godsil and Royle [77], we prove that
 根据Godsil和Royle[77]，我们证明

E(R) = tr(R>LR),
 e（r）=tr（r>lr）

where
 哪里

L = D − W,
 L=D-W，

is the familiar unnormalized Laplacian matrix associated with W, and where D is the degree matrix associated with W.
 是熟悉的与w有关的非正规拉普拉斯矩阵，其中d是与w有关的度矩阵。

It can be shown that there is no loss in generality in assuming that the columns of R are pairwise orthogonal and that they have unit length. Such a matrix satisfies the equation R>R = I and the corresponding drawing is called an orthogonal drawing. This condition also rules out trivial drawings.
 结果表明，假设R的列是成对正交的，并且它们具有单位长度，则不存在一般性的损失。这样的矩阵满足方程r>r=i，相应的图称为正交图。这种情况也排除了一些琐碎的绘图。

Then we prove the main theorem about graph drawings (Theorem 19.2), which essentially says that the matrix R of the desired graph drawing is constituted by the n eigenvectors of L associated with the smallest nonzero n eigenvalues of L. We give a number examples of graph drawings, many of which are borrowed or adapted from Spielman [158].
 然后，我们证明了关于图的主要定理（定理19.2），它实质上表示所需图的矩阵R是由L的n个特征向量与L的最小非零n个特征值构成的，我们给出了一些图的例子，其中许多是借用或改编自斯皮尔曼[158]。

## 18.1  Directed Graphs, Undirected Graphs, Incidence Matrices, Adjacency Matrices, Weighted Graphs  18.1有向图、无向图、关联矩阵、邻接矩阵、加权图

Definition 18.1. A directed graph is a pair G = (V,E), where V = {v1,...,vm} is a set of nodes or vertices, and E ⊆ V × V is a set of ordered pairs of distinct nodes (that is, pairs (u,v) ∈ V × V with u =6      v), called edges. Given any edge e = (u,v), we let s(e) = u be the source of e and t(e) = v be the target of e.
 定义18.1.有向图是一对g=（v，e），其中v=v1，…，vm是一组节点或顶点，e v×v是一组有序的不同节点对（即对（u，v）v×v和u=6v），称为边。给定任意边e=（u，v），我们让s（e）=u是e的源，t（e）=v是e的目标。

Remark: Since an edge is a pair (u,v) with u =6 v, self-loops are not allowed. Also, there is at most one edge from a node u to a node v. Such graphs are sometimes called simple graphs.
 注：由于边缘是U=6V的对（U，V），因此不允许出现自循环。此外，从节点U到节点V最多有一个边。这种图有时称为简单图。

An example of a directed graph is shown in Figure 18.2.
 有向图的示例如图18.2所示。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

Figure 18.2: Graph G1.
 图18.2：图G1。

Definition 18.2. For every node v ∈ V , the degree d(v) of v is the number of edges leaving or entering v:
 定义18.2.对于每个节点v∈v，v的阶数d（v）是离开或进入v的边数：

d(v) = |{u ∈ V | (v,u) ∈ E or (u,v) ∈ E}|.
 d（v）=u∈v（v，u）∈e或（u，v）∈e。

We abbreviate d(vi) as di. The degree matrix, D(G), is the diagonal matrix
 我们把d（vi）缩写为di。度矩阵d（g）是对角矩阵

D(G) = diag(d1,...,dm).
 d（g）=diag（d1，…，dm）。


 

For example, for graph G1, we have
 例如，对于图g1，我们有

​                                                                       2    0   0   0   0
 2 0 0 0 0_

​                                                                       0    4   0   0   0
 0 4 0 0 0_

​                                                      D(G1) = 0   0   3   0   0.
 D（g1）=0 0 3 0 0。

​                                                                                               
                                                                     

​                                                                       0    0   0   3   0
 0 0 3 0_

​                                                                          0   0   0   0   2
 0 0 0 0 2

Unless confusion arises, we write D instead of D(G).
 除非出现混淆，我们写D而不是D（G）。

Definition 18.3. Given a directed graph G = (V,E), for any two nodes u,v ∈ V , a path from u to v is a sequence of nodes (v0,v1,...,vk) such that v0 = u, vk = v, and (vi,vi+1) is an edge in E for all i with 0 ≤ i ≤ k − 1. The integer k is the length of the path. A path is closed if u = v. The graph G is strongly connected if for any two distinct nodes u,v ∈ V , there is a path from u to v and there is a path from v to u.
 定义18.3.给定有向图g=（v，e），对于任意两个节点u，v∈v，从u到v的路径是节点序列（v0，v1，…，v k），因此v0=u，vk=v，并且（v i，vi+1）是e中所有i的边，0≤i≤k−1。整数k是路径的长度。当u=v时，路径是封闭的，图G是强连通的，如果对于任意两个不同的节点u，v∈v，有一条从u到v的路径，有一条从v到u的路径。

Remark: The terminology walk is often used instead of path, the word path being reserved to the case where the nodes vi are all distinct, except that v0 = vk when the path is closed.
 备注：术语walk通常被用来代替path，单词path被保留到节点vi都是不同的情况下，除了路径关闭时v0=vk。

The binary relation on V ×V defined so that u and v are related iff there is a path from u to v and there is a path from v to u is an equivalence relation whose equivalence classes are called the strongly connected components of G.
 v×v上的二元关系定义为u和v是相关的，如果存在从u到v的路径，并且存在从v到u的路径，则为等价关系，其等价类称为g的强连通分量。

Definition 18.4. Given a directed graph G = (V,E), with V = {v1,...,vm}, if E = {e1,...,en}, then the incidence matrix B(G) of G is the m×n matrix whose entries bij are given by
 定义18.4.给定有向图g=（v，e），其中v=v1，…，v m，如果e=e1，…，e n，则g的关联矩阵b（g）是m×n矩阵，其条目bij由下式给出：


 γ

+1 if s(ej) = vi bij = −1 if t(ej) = vi 0 otherwise.
 +1，如果s（ej）=vi bij=-1，如果t（ej）=vi 0，否则。

Here is the incidence matrix of the graph G1:
 图g1的关联矩阵如下：

 .
 .

Observe that every column of an incidence matrix contains exactly two nonzero entries, +1 and −1. Again, unless confusion arises, we write B instead of B(G).
 注意，一个关联矩阵的每一列正好包含两个非零项，+1和−1。同样，除非出现混淆，我们写B而不是B（G）。

When a directed graph has m nodes v1,...,vm and n edges e1,...,en, a vector x ∈ Rm can be viewed as a function x: V → R assigning the value xi to the node vi. Under this interpretation, Rm is viewed as RV . Similarly, a vector y ∈ Rn can be viewed as a function
 当有向图有M个节点V1，…，VM和N边E1，…，EN时，向量X * RM可以被看作是函数X：V～R，将值XI赋值给节点VI。同样，向量y∈rn可以看作是一个函数。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image003.gif)

Figure 18.3: The undirected graph G2.
 图18.3：无向图g2。

in RE. This point of view is often useful. For example, the incidence matrix B can be interpreted as a linear map from RE to RV , the boundary map, and B> can be interpreted as a linear map from RV to RE, the coboundary map.
 在RE中。这种观点通常是有用的。例如，关联矩阵b可以解释为从re到rv的线性映射，边界映射，和b>可以解释为从rv到re的线性映射，共边界映射。

Remark: Some authors adopt the opposite convention of sign in defining the incidence matrix, which means that their incidence matrix is −B.
 注：有些作者在定义关联矩阵时采用了符号的相反约定，这意味着他们的关联矩阵是−b。

Undirected graphs are obtained from directed graphs by forgetting the orientation of the edges.
 无向图是通过忽略边的方向从有向图得到的。

Definition 18.5. A graph (or undirected graph) is a pair G = (V,E), where V = {v1,...,vm} is a set of nodes or vertices, and E is a set of two-element subsets of V (that is, subsets {u,v}, with u,v ∈ V and u =6 v), called edges.
 定义18.5.图（或无向图）是一对g=（v，e），其中v=v1，…，vm是一组节点或顶点，e是v的两个元素子集的集合（即子集u，v，具有u，v∈v和u=6v），称为边。

Remark: Since an edge is a set {u,v}, we have u =6 v, so self-loops are not allowed. Also, for every set of nodes {u,v}, there is at most one edge between u and v. As in the case of directed graphs, such graphs are sometimes called simple graphs.
 注：由于边是一组u，v，我们有u=6v，所以不允许自循环。而且，对于每一组节点u，v，u和v之间最多有一个边。在有向图的情况下，这种图有时称为简单图。

An example of a graph is shown in Figure 18.3.
 图18.3显示了一个图表的示例。

Definition 18.6. For every node v ∈ V , the degree d(v) of v is the number of edges incident to v:
 定义18.6.对于每个节点v∈v，v的阶数d（v）是v的边数：

d(v) = |{u ∈ V | {u,v} ∈ E}|.
 d（v）=u∈v u，v∈e。

The degree matrix D(G) (or simply, D) is defined as in Definition 18.2.
 度矩阵d（g）（或简单地说，d）的定义见定义18.2。

Definition 18.7. Given a (undirected) graph G = (V,E), for any two nodes u,v ∈ V , a path from u to v is a sequence of nodes (v0,v1,...,vk) such that v0 = u, vk = v, and {vi,vi+1} is an edge in E for all i with 0 ≤ i ≤ k − 1. The integer k is the length of the path. A path is closed if u = v. The graph G is connected if for any two distinct nodes u,v ∈ V , there is a path from u to v.
 定义18.7.给定（无向）图g=（v，e），对于任意两个节点u，v∈v，从u到v的路径是节点序列（v0，v1，…，v k），使得v0=u，vk=v，和v i，vi+1是e中0≤i≤k−1的所有i的边。整数k是路径的长度。当u=v时，路径是封闭的。图g是连通的，如果对于任意两个不同的节点u，v∈v，有一条从u到v的路径。

Remark: The terminology walk or chain is often used instead of path, the word path being reserved to the case where the nodes vi are all distinct, except that v0 = vk when the path is closed.
 备注：术语walk或chain通常被用来代替path，单词path被保留到节点vi都不同的情况下，除了v0=vk（路径关闭时）。

The binary relation on V ×V defined so that u and v are related iff there is a path from u to v is an equivalence relation whose equivalence classes are called the connected components of G.
 定义了V×V上的二元关系，使U和V是相关的，如果有一条从U到V的路径是一个等价关系，其等价类称为G的连通分量。

The notion of incidence matrix for an undirected graph is not as useful as in the case of directed graphs
 无向图的关联矩阵的概念不如有向图的概念有用。

Definition 18.8. Given a graph G = (V,E), with V = {v1,...,vm}, if E = {e1,...,en}, then the incidence matrix B(G) of G is the m × n matrix whose entries bij are given by
 定义18.8.给定一个图g=（v，e），其中v=v1，…，v m，如果e=e1，…，e n，则g的关联矩阵b（g）是m×n矩阵，其条目bij由下式给出：

(
 （

bij =      +1 if ej = {vi,vk} for some k 0      otherwise.
 如果ej=vi，则bij=+1，对于某些k 0，则为vk。

Unlike the case of directed graphs, the entries in the incidence matrix of a graph (undirected) are nonnegative. We usually write B instead of B(G).
 与有向图的情况不同，图（无向）的关联矩阵中的条目是非负的。我们通常写B而不是B（G）。

Definition 18.9. If G = (V,E) is a directed or an undirected graph, given a node u ∈ V , any node v ∈ V such that there is an edge (u,v) in the directed case or {u,v} in the undirected case is called adjacent to u, and we often use the notation
 定义18.9.如果g=（v，e）是有向图或无向图，给定一个节点u∈v，任意节点v∈v，使得有向情况下有一个边（u，v），或在无向情况下有一个边（u，v），我们通常使用符号“邻近u”来表示。

u ∼ v.
 U～V。

Observe that the binary relation ∼ is symmetric when G is an undirected graph, but in general it is not symmetric when G is a directed graph.
 注意，当g是无向图时，二进制关系～是对称的，但一般来说，当g是有向图时，它不是对称的。

The notion of adjacency matrix is basically the same for directed or undirected graphs.
 有向图和无向图的邻接矩阵的概念基本相同。

Definition 18.10. Given a directed or undirected graph G = (V,E), with V = {v1,...,vm}, the adjacency matrix A(G) of G is the symmetric m × m matrix (aij) such that
 定义18.10.给定有向或无向图g=（v，e），对于v=v1，…，v m，g的邻接矩阵a（g）是对称m×m矩阵（aij），这样

(1)    If G is directed, then
 如果G被指示，那么

(
 （

aij =      1   if there is some edge (vi,vj) ∈ E or some edge (vj,vi) ∈ E 0 otherwise.
 如果有边（vi，vj）∈e或某边（vj，vi）∈e 0，则aij=1。

(2)    Else if G is undirected, then
 否则，如果g是无向的，那么

(
 （

aij =      1   if there is some edge {vi,vj} ∈ E 0 otherwise.
 如果有边vi，则aij=1，否则vj∈e 0。

As usual, unless confusion arises, we write A instead of A(G). Here is the adjacency matrix of both graphs G1 and G2:
 像往常一样，除非出现混淆，否则我们写A而不是A（G）。这是图g1和g2的邻接矩阵：

​                                                                   0    1   1   0   0
 0 1 1 0_

​                                                                   1    0   1   1   1
 1 0 1 1 1_

​                                                          A = 1   1   0   1  0.
 A=1 1 0 1 0。

​                                                                                           
                                                                 

​                                                                   0    1   1   0   1
 0 1 1 0 1_

​                                                                      0   1   0   1   0
 0 1 0 1 0

If G = (V,E) is an undirected graph, the adjacency matrix A of G can be viewed as a linear map from RV to RV , such that for all x ∈ Rm, we have
 如果g=（v，e）是一个无向图，g的邻接矩阵a可以看作是从RV到RV的线性映射，这样对于所有x∈rm，我们得到

(Ax)i = Xxj;
 （ax）i=xxj；

j∼i
 J i

that is, the value of Ax at vi is the sum of the values of x at the nodes vj adjacent to vi. The adjacency matrix can be viewed as a diffusion operator. This observation yields a geometric interpretation of what it means for a vector x ∈ Rm to be an eigenvector of A associated with some eigenvalue λ; we must have
 也就是说，x在vi处的值是x在与vi相邻的节点vj处的值之和。邻接矩阵可视为扩散算子。这个观察给出了向量x∈rm是与某个特征值λ相关的a的特征向量的几何解释；我们必须

​                                                         λxi = Xxj,            i = 1,...,m,
 Xxj＝1，…，m，

j∼i
 J i

which means that the the sum of the values of x assigned to the nodes vj adjacent to vi is equal to λ times the value of x at vi.
 这意味着分配给邻近vi节点vj的x值之和等于λ乘以vi处x值。

Definition 18.11. Given any undirected graph G = (V,E), an orientation of G is a function σ: E → V × V assigning a source and a target to every edge in E, which means that for every edge {u,v} ∈ E, either σ({u,v}) = (u,v) or σ({u,v}) = (v,u). The oriented graph Gσ obtained from G by applying the orientation σ is the directed graph Gσ = (V,Eσ), with Eσ = σ(E).
 定义18.11.给定任意无向图g=（v，e），g的方向是一个函数σ：e→v×v，将一个源和一个目标赋给e中的每一条边，这意味着对于每一条边u，v∈e，要么是σ（u，v）=（u，v）或σ（u，v）=（v，u）。应用方向σ从g得到的定向图gσ是有向图gσ=（v，eσ），其中eσ=σ（e）。

The following result shows how the number of connected components of an undirected graph is related to the rank of the incidence matrix of any oriented graph obtained from G.
 下面的结果显示了无向图的连通分量的数目与从G得到的任何有向图的关联矩阵的秩是如何相关的。

Proposition 18.1. Let G = (V,E) be any undirected graph with m vertices, n edges, and c connected components. For any orientation σ of G, if B is the incidence matrix of the oriented graph Gσ, then c = dim(Ker(B>)), and B has rank m − c. Furthermore, the nullspace of B> has a basis consisting of indicator vectors of the connected components of G; that is, vectors (z1,...,zm) such that zj = 1 iff vj is in the ith component Ki of G, and zj = 0 otherwise.
 提案18.1.设g=（v，e）为任意具有m个顶点、n个边和c个连通分量的无向图。对于g的任何方向σ，如果b是有向图gσ的关联矩阵，则c=dim（ker（b>），b的秩为m−c。此外，b>的零空间有一个基，由g的连接分量的指示向量组成；也就是说，向量（z1，…，zm），使得zj=1 iff vj在g的第i个分量ki中，否则zj=0。

Proof. (After Godsil and Royle [77], Section 8.3). The fact that rank(B) = m − c will be proved last.
 证据。（在Godsil和Royle[77]之后，第8.3节）。排名（b）=m-c的事实将最后证明。

Let us prove that the kernel of B> has dimension c. A vector z ∈ Rm belongs to the kernel of B> iff B>z = 0 iff z>B = 0. In view of the definition of B, for every edge {vi,vj} of G, the column of B corresponding to the oriented edge σ({vi,vj}) has zero entries except for a +1 and a −1 in position i and position j or vice-versa, so we have
 让我们证明b>的核具有维数c，向量z∈rm属于b>iff b>z=0 iff z>b=0的核。根据b的定义，对于g的每一个边vi，vj，b的列对应于定向边σ（vi，vj），除了位置i和位置j中的a+1和a−1外，其余都是零项，因此我们有

zi = zj.
 zi=zj.

An easy induction on the length of the path shows that if there is a path from vi to vj in G (unoriented), then zi = zj. Therefore, z has a constant value on any connected component of
 对路径长度的一个简单归纳表明，如果在g中有一条从vi到vj的路径（无方向），那么zi=zj。因此，z在

G. It follows that every vector z ∈ Ker(B>) can be written uniquely as a linear combination
 g.由此可知，每个向量z∈ker（b>）都可以唯一地写成一个线性组合。

z = λ1z1 + ··· + λczc,
 Z=λ1z1+····+λczc，

where the vector zi corresponds to the ith connected component Ki of G and is defined such that
 其中，矢量zi对应于g的第i个连通分量ki，并且定义为

(
 （

​                                                             zji =     1     iff vj ∈ Ki
 zji=1 iff vj∈ki

​                                                                        0    otherwise.
 否则为0。

This shows that dim(Ker(B>)) = c, and that Ker(B>) has a basis consisting of indicator vectors.
 这表明dim（ker（b>）=c，而ker（b>）有一个由指示器向量组成的基。

Since B> is a n × m matrix, we have
 因为b>是一个n×m矩阵，我们有

m = dim(Ker(B>)) + rank(B>),
 m=dim（ker（b>）+等级（b>），

and since we just proved that dim(Ker(B>)) = c, we obtain rank(B>) = m − c. Since B and B> have the same rank, rank(B) = m − c, as claimed. 
 由于我们刚刚证明了dim（ker（b>）=c，我们得到了秩（b>）=m−c，因为b和b>具有相同的秩，如所述，秩（b）=m−c。

Definition 18.12. Following common practice, we denote by 1 the (column) vector (of dimension m) whose components are all equal to 1.
 定义18.12.按照惯例，我们用1表示（列）向量（维数m），其分量都等于1。

Since every column of B contains a single +1 and a single −1, the rows of B> sum to zero, which can be expressed as
 因为B的每一列都包含一个+1和一个-1，所以B>的行和为零，可以表示为

B>1 = 0.
 b>1=0。

According to Proposition 18.1, the graph G is connected iff B has rank m−1 iff the nullspace of B> is the one-dimensional space spanned by 1.
 根据命题18.1，图G是连通的，如果b的秩为m-1，如果b>的空空间是1的一维空间。

In many applications, the notion of graph needs to be generalized to capture the intuitive idea that two nodes u and v are linked with a degree of certainty (or strength). Thus, we assign a nonnegative weight wij to an edge {vi,vj}; the smaller wij is, the weaker is the link (or similarity) between vi and vj, and the greater wij is, the stronger is the link (or similarity) between vi and vj.
 在许多应用中，需要对图的概念进行广义化，以获取直观的观点，即两个节点u和v与一定程度的确定性（或强度）相关联。因此，我们将非负权重wij赋给边vi，vj；wij越小，vi和vj之间的链接（或相似性）越弱，wij越大，vi和vj之间的链接（或相似性）越强。

Definition 18.13. A weighted graph is a pair G = (V,W), where V = {v1,...,vm} is a set of nodes or vertices, and W is a symmetric matrix called the weight matrix, such that wij ≥ 0 for all i,j ∈ {1,...,m}, and wii = 0 for i = 1,...,m. We say that a set {vi,vj} is an edge iff wij > 0. The corresponding (undirected) graph (V,E) with E = {{vi,vj} | wij > 0}, is called the underlying graph of G.
 定义18.13.加权图是一对g=（v，w），其中v=v1，…，v m是一组节点或顶点，w是称为权矩阵的对称矩阵，这样w i j对于所有i，j 1，…，m，wii=0对于i=1，…，m都等于0。我们说，集vi，vj是边iff wij>0。对应的（无向）图（v，e），其中e=vi，vj wij>0，称为G的底层图。

Remark: Since wii = 0, these graphs have no self-loops. We can think of the matrix W as a generalized adjacency matrix. The case where wij ∈ {0,1} is equivalent to the notion of a graph as in Definition 18.5.
 注：由于wii=0，这些图没有自循环。我们可以把矩阵w看作一个广义邻接矩阵。wij 0,1等于定义18.5中的图的概念的情况。

We can think of the weight wij of an edge {vi,vj} as a degree of similarity (or affinity) in an image, or a cost in a network. An example of a weighted graph is shown in Figure 18.4. The thickness of an edge corresponds to the magnitude of its weight.
 我们可以将边vi、vj的权重wij视为图像中的相似度（或相似性），或网络中的成本。加权图的示例如图18.4所示。边缘的厚度与它的重量大小相对应。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

Figure 18.4: A weighted graph.
 图18.4：加权图。

Definition 18.14. Given a weighted graph G = (V,W), for every node vi ∈ V , the degree d(vi) of vi is the sum of the weights of the edges adjacent to vi:
 定义18.14.给定加权图g=（v，w），对于每个节点vi∈v，vi的阶数d（vi）是与vi相邻的边的权重之和：

.
 .

Note that in the above sum, only nodes vj such that there is an edge {vi,vj} have a nonzero contribution. Such nodes are said to be adjacent to vi, and we write vi ∼ vj. The degree matrix D(G) (or simply, D) is defined as before, namely by D(G) = diag(d(v1),...,d(vm)).
 请注意，在上述总和中，只有节点vj具有非零贡献，这样就有一个边vi，vj。这样的节点被称为与vi相邻，我们写vi～vj。度矩阵d（g）（或简单地说，d）定义为之前，即d（g）=diag（d（v1），…，d（vm））。

The weight matrix W can be viewed as a linear map from RV to itself. For all x ∈ Rm, we have
 重量矩阵w可以看作是从RV到自身的线性映射。对于所有x∈rm，我们有

(Wx)i = Xwijxj;
 （wx）i=xwijxj；

j∼i
 J i

that is, the value of Wx at vi is the weighted sum of the values of x at the nodes vj adjacent to vi.
 也就是说，wx在vi处的值是x在邻近vi的节点vj处的值的加权和。

Observe that W1 is the (column) vector (d(v1),...,d(vm)) consisting of the degrees of the nodes of the graph.
 观察w1是（列）向量（d（v1），…，d（vm）），由图中节点的度数组成。

We now define the most important concept of this chapter: the Laplacian matrix of a graph. Actually, as we will see, it comes in several flavors.
 我们现在定义本章最重要的概念：图的拉普拉斯矩阵。实际上，正如我们将看到的，它有几种口味。


 

18.2. LAPLACIAN MATRICES OF GRAPHS
 18.2。图的拉普拉斯矩阵

## 18.2         Laplacian Matrices of Graphs  18.2图的拉普拉斯矩阵

Let us begin with directed graphs, although as we will see, graph Laplacians are fundamentally associated with undirected graph. The key proposition below shows how given an undirected graph G, for any orientation σ of G, Bσ(Bσ)> relates to the adjacency matrix A (where Bσ is the incidence matrix of the directed graph Gσ). We reproduce the proof in Gallier [72] (see also Godsil and Royle [77]).
 让我们从有向图开始，尽管正如我们将看到的，图拉普拉斯人基本上与无向图联系在一起。下面的关键命题展示了给定的无向图g，对于g的任何方向，bσ（bσ）>如何与邻接矩阵a（其中bσ是有向图gσ的关联矩阵）相关。我们用Gallier[72]复制了证据（另见Godsil和Royle[77]）。

Proposition 18.2. Given any undirected graph G, for any orientation σ of G, if Bσis the incidence matrix of the directed graph Gσ, A is the adjacency matrix of Gσ, and D is the degree matrix such that Dii = d(vi), then
 提案18.2.给定任意无向图g，对于g的任何方向σ，如果bσ是有向图gσ的关联矩阵，a是gσ的邻接矩阵，d是度矩阵，因此dii=d（vi），那么

Bσ(Bσ)> = D − A.
 bσ（bσ）>=d−a。

Consequently, L = Bσ(Bσ)> is independent of the orientation σ of G, and D−A is symmetric and positive semidefinite; that is, the eigenvalues of D − A are real and nonnegative. Proof. The entry Bσ(Bσ)>ij is the inner product of the ith row bσi , and the jth row bσj of Bσ.
 因此，l=bσ（bσ）>与g的方向σ无关，d−a是对称的正半定的，即d−a的特征值是实的和非负的。证据。条目bσ（bσ）>i j是第i行bσi的内积，bσj的第j行bσj。

| If i = j,   then as    网络错误                              |                                                     |
| ------------------------------------------------------------ | --------------------------------------------------- |
|     网络错误   +1    网络错误       网络错误                                                           bσik   =       −1    网络错误   0    网络错误 | if s(ek) = vi if t(ek) =   vi otherwise    网络错误 |

we see that bσi · bσi = d(vi). If i =6 j, then bσi · bjσ = 06 iff there is some edge ek with s(ek) = vi and t(ek) = vj or vice-versa (which are mutually exclusive cases, since Gσ arises by orienting an undirected graph), in which case, bσi · bσj = −1. Therefore,
 我们看到bσi·bσi=d（vi）。如果i=6 J，那么bσi·b jσ=06如果有一些边Ek，s（Ek）=vi和t（Ek）=vj，反之亦然（这是互斥的情况，因为gσ是通过定向无向图产生的），在这种情况下，bσi·bσj=−1。因此，

Bσ(Bσ)> = D − A,
 bσ（bσ）>=d−a，

as claimed.
 如要求。

For every x ∈ Rm, we have
 对于每一个x∈rm，我们有

,
 ，

since the Euclidean norm k k2 is positive (definite). Therefore, L = Bσ(Bσ)> is positive semidefinite. It is well-known that a real symmetric matrix is positive semidefinite iff its eigenvalues are nonnegative.      
 因为欧几里得范数k k2是正的（确定的）。因此，l=bσ（bσ）>是半正定的。众所周知，实对称矩阵是半正定的，而其特征值是非负的。

Definition 18.15. The matrix L = Bσ(Bσ)> = D − A is called the (unnormalized) graph
 定义18.15.矩阵l=bσ（bσ）>=d−a称为（非正规化）图。

Laplacian of the graph Gσ. The (unnormalized) graph Laplacian of an undirected graph
 图Gσ的拉普拉斯函数。无向图的拉普拉斯图

G = (V,E) is defined by
 g=（v，e）的定义如下：

L = D − A.
 L=D−A。

For example, the graph Laplacian of graph G1 is
 例如，图g1的拉普拉斯图是

 .
 .

Observe that each row of L sums to zero (because (Bσ)>1 = 0). Consequently, the vector 1 is in the nullspace of L.
 观察每行L的总和为零（因为（bσ）>1=0）。因此，向量1在l的空空间中。

Remarks:
 评论：

\1.    With the unoriented version of the incidence matrix (see Definition 18.8), it can be shown that
 对于无定向版本的发病率矩阵（见定义18.8），可以证明：

BB> = D + A.
 bb>=d+a。

\2.    As pointed out by Evangelos Chatzipantazis, Proposition 18.2 in which the incidence matrix Bσ is replaced by the incidence matrix B of any arbitrary directed graph G does not hold. The problem is that such graphs may have both edges (vi,vj) and (vj,vi) between two distinct nodes vi and vj, and as a consequence, the inner product bi · bj = −2 instead of −1. A simple counterexample is given by the directed graph with three vertices and four edges whose incidence matrix is given by
 正如Evangelos Chatzipantazis所指出的那样，18.2命题中，任何任意有向图G的关联矩阵b代替了关联矩阵b。问题是这样的图可能在两个不同的节点vi和vj之间都有边（vi，vj）和（vj，vi），因此内部积bi·bj=-2而不是-1。给出了三顶点四边有向图的一个简单反例，其关联矩阵由

 .
 .

We have
 我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

The natural generalization of the notion of graph Laplacian to weighted graphs is this:
 图拉普拉斯的概念对加权图的自然概括是：

Definition 18.16. Given any weighted graph G = (V,W) with V = {v1,...,vm}, the (unnormalized) graph Laplacian L(G) of G is defined by
 定义18.16.给定任意加权图g=（v，w），其中v=v1，…，vm，g的（非正规化）图拉普拉斯L（g）定义为

L(G) = D(G) − W,
 L（g）=D（g）−W，

where D(G) = diag(d1,...,dm) is the degree matrix of G (a diagonal matrix), with
 其中d（g）=diag（d1，…，dm）是g（对角矩阵）的度数矩阵，其中

.
 .

As usual, unless confusion arises, we write D instead of D(G) and L instead of L(G).
 像往常一样，除非出现混淆，我们写D而不是D（G），L而不是L（G）。

### 18.2. LAPLACIAN MATRICES OF GRAPHS  18.2。图的拉普拉斯矩阵

The graph Laplacian can be interpreted as a linear map from RV to itself. For all x ∈ RV , we have
 拉普拉斯图可以解释为从RV到自身的线性映射。对于所有的x∈rv，我们有

.
 .

It is clear from the equation L = D − W that each row of L sums to 0, so the vector 1 is the nullspace of L, but it is less obvious that L is positive semidefinite. One way to prove it is to generalize slightly the notion of incidence matrix.
 从方程l=d−w可以清楚地看出，每行l的总和为0，因此向量1是l的空空间，但不太明显l是半定的。证明这一点的一种方法是稍微概括一下关联矩阵的概念。

Definition 18.17. Given a weighted graph G = (V,W), with V = {v1,...,vm}, if {e1,..., en} are the edges of the underlying graph of G (recall that {vi,vj} is an edge of this graph iff wij > 0), for any oriented graph Gσ obtained by giving an orientation to the underlying graph of G, the incidence matrix Bσ of Gσ is the m × n matrix whose entries bij are given by
 定义18.17.给定一个加权图g=（v，w），其中v=v1，…，vm，如果e1，…，en是g的下一个图的边（回想一下v i，vj是这个图的边iff wij>0），对于通过给g的下一个图一个方向而得到的任何定向图gσ，gσi的关联矩阵bσs m×n矩阵，其条目bij由下式给出。

.
 .

For example, given the weight matrix
 例如，给定权重矩阵

 ,
 ，

the incidence matrix B corresponding to the orientation of the underlying graph of W where an edge (i,j) is oriented positively iff i < j is
 当边缘（i，j）为正方向且i<j为正方向时，对应于基础图w方向的入射矩阵b

 .
 .

The reader should verify that BB> = D − W. This is true in general, see Proposition 18.3.
 读者应确认bb>=d−w。这通常是正确的，见第18.3条建议。

It is easy to see that Proposition 18.1 applies to the underlying graph of G. For any oriented graph Gσ obtained from the underlying graph of G, the rank of the incidence matrix Bσ is equal to m−c, where c is the number of connected components of the underlying graph of G, and we have (Bσ)>1 = 0. We also have the following version of Proposition 18.2 whose proof is immediately adapted.
 很容易看出，命题18.1适用于g的下垫图。对于从g的下垫图获得的任何定向图gσ，关联矩阵bσ的秩等于m−c，其中c是g下垫图的连通分量的数目，我们得到（bσ）>1=0。我们也有以下版本的18.2号提案，其证据立即被采纳。

Proposition 18.3. Given any weighted graph G = (V,W) with V = {v1,...,vm}, if Bσ is the incidence matrix of any oriented graph Gσ obtained from the underlying graph of G and D is the degree matrix of G, then
 提案18.3.给定任意加权图g=（v，w），其中v=v1，…，vm，如果bσ是从g的底层图中得到的任意定向图g的关联矩阵，d是g的度矩阵，那么

Bσ(Bσ)> = D − W = L.
 bσ（bσ）>=d−w=l。

Consequently, Bσ(Bσ)> is independent of the orientation of the underlying graph of G and L = D − W is symmetric and positive semidefinite; that is, the eigenvalues of L = D − W are real and nonnegative.
 因此，bσ（bσ）>与g的下垫图的方向无关，l=d−w是对称的正半定的，也就是说，l=d−w的特征值是实的和非负的。

Another way to prove that L is positive semidefinite is to evaluate the quadratic form x>Lx.
 证明l是半正定的另一种方法是求二次型x>lx。

Proposition 18.4. For any m × m symmetric matrix W = (wij), if we let L = D − W where D is the degree matrix associated with W (that is, ), then we have
 提案18.4.对于任何m×m对称矩阵w=（wij），如果我们让l=d−w，其中d是与w相关联的度数矩阵（即，），那么我们有

​                                                                                            for all x ∈ Rm.
 对于所有x∈rm。

Consequently, x>Lx does not depend on the diagonal entries in W, and if wij ≥ 0 for all i,j ∈ {1,...,m}, then L is positive semidefinite.
 因此，x>lx不依赖于w中的对角线项，如果所有i，j∈1，…，m的wij≥0，则l为正半定。

Proof. We have
 证据。我们有

!
 ！

Obviously, the quantity on the right-hand side does not depend on the diagonal entries in W, and if wij ≥ 0 for all i,j, then this quantity is nonnegative. 
 显然，右边的数量不依赖于w中的对角线项，如果w i j对于所有i，j都大于等于0，那么这个数量是非负的。

Proposition 18.4 immediately implies the following facts: For any weighted graph G = (V,W),
 命题18.4立即暗示了以下事实：对于任何加权图g=（v，w），

\1.    The eigenvalues 0 = λ1 ≤ λ2 ≤ ... ≤ λm of L are real and nonnegative, and there is an orthonormal basis of eigenvectors of L.
 特征值0=λ1≤λ2≤…L的λm是实的和非负的，并且L的特征向量有一个正交基。

\2.    The smallest eigenvalue λ1 of L is equal to 0, and 1 is a corresponding eigenvector.
 L的最小特征值λ1等于0，1是对应的特征向量。

It turns out that the dimension of the nullspace of L (the eigenspace of 0) is equal to the number of connected components of the underlying graph of G.
 结果表明，L的零空间维数（特征空间为0）等于G的底层图的连通分量的个数。

### 18.3. NORMALIZED LAPLACIAN MATRICES OF GRAPHS  18.3。图的正规拉普拉斯矩阵

Proposition 18.5. Let G = (V,W) be a weighted graph. The number c of connected components K1,...,Kc of the underlying graph of G is equal to the dimension of the nullspace of L, which is equal to the multiplicity of the eigenvalue 0. Furthermore, the nullspace of L has a basis consisting of indicator vectors of the connected components of G, that is, vectors (f1,...,fm) such that fj = 1 iff vj ∈ Ki and fj = 0 otherwise.
 提案18.5。设g=（v，w）为加权图。G下垫图的连通分量k1，…，kc的个数c等于L的零空间的维数，等于特征值0的重数。此外，L的零空间有一个基，由G的连通分量的指示向量构成，即向量（f1，…，fm），使fj=1 iff vj∈ki，否则fj=0。

Proof. Since L = BB> for the incidence matrix B associated with any oriented graph obtained from G, and since L and B> have the same nullspace, by Proposition 18.1, the dimension of the nullspace of L is equal to the number c of connected components of G and the indicator vectors of the connected components of G form a basis of Ker(L). 
 证据。由于l=b b>对于与从g得到的任何定向图相关联的关联矩阵b，并且l和b>具有相同的零空间，根据命题18.1，l的零空间的维数等于g的连接分量的C数和连接分量的指示向量。t的g构成了ker（l）的基础。

Proposition 18.5 implies that if the underlying graph of G is connected, then the second eigenvalue λ2 of L is strictly positive.
 命题18.5意味着，如果G的下垫图是连通的，那么L的第二特征值λ2是严格正的。

Remarkably, the eigenvalue λ2 contains a lot of information about the graph G (assuming that G = (V,E) is an undirected graph). This was first discovered by Fiedler in 1973, and for this reason, λ2 is often referred to as the Fiedler number. For more on the properties of the Fiedler number, see Godsil and Royle [77] (Chapter 13) and Chung [39]. More generally, the spectrum (0,λ2,...,λm) of L contains a lot of information about the combinatorial structure of the graph G. Leverage of this information is the object of spectral graph theory.
 值得注意的是，特征值λ2包含了大量关于图G的信息（假设g=（v，e）是无向图）。这是费德勒在1973年首次发现的，因此，λ2通常被称为费德勒数。关于费德勒数属性的更多信息，见Godsil和Royle[77]（第13章）和Chung[39]。一般来说，L的谱（0，λ2，…，λm）包含了大量关于图G组合结构的信息，利用这些信息是谱图理论的研究对象。

## 18.3          Normalized Laplacian Matrices of Graphs  18.3图的正规拉普拉斯矩阵

It turns out that normalized variants of the graph Laplacian are needed, especially in applications to graph clustering. These variants make sense only if G has no isolated vertices.
 结果表明，需要图形拉普拉斯的规范化变量，特别是在图形聚类的应用中。只有当g没有孤立的顶点时，这些变量才有意义。

Definition 18.18. Given a weighted graph G = (V,W), a vertex u ∈ V is isolated if it is not incident to any other vertex. This means that every row of W contains some strictly positive entry.
 定义18.18.给定一个加权图g=（v，w），如果一个顶点u∈v不与任何其他顶点相关联，则它是孤立的。这意味着W的每一行都包含一些严格的正数。

If G has no isolated vertices, then the degree matrix D contains positive entries, so it is invertible and D−1/2 makes sense; namely
 如果g没有孤立的顶点，那么度数矩阵d包含正项，因此它是可逆的，d−1/2是有意义的；即

D−1/2 = diag(,
 D−1/2=诊断（，

and similarly for any real exponent α.
 与任何实数指数α类似。

Definition 18.19. Given any weighted directed graph G = (V,W) with no isolated vertex and with V = {v1,...,vm}, the (normalized) graph Laplacians Lsym and Lrw of G are defined by
 定义18.19.给定任何无孤立顶点的加权有向图g=（v，w），以及v=v1，…，vm，（归一化）图g的拉普拉斯LSYM和lrw定义为

Lsym = D−1/2LD−1/2 = I − D−1/2WD−1/2 Lrw = D−1L = I − D−1W.
 LSYM=D−1/2LD−1/2=I−D−1/2WD−1/2 LRW=D−1L=I−D−1W。

Observe that the Laplacian Lsym = D−1/2LD−1/2 is a symmetric matrix (because L and
 观察拉普拉斯LSYM=d−1/2ld−1/2是一个对称矩阵（因为l和

D−1/2 are symmetric) and that
 d−1/2是对称的）和

Lrw = D−1/2LsymD1/2.
 lrw=d−1/2lsymd1/2。

The reason for the notation Lrw is that this matrix is closely related to a random walk on the graph G.
 符号lrw的原因是这个矩阵与图g上的随机游动密切相关。

Example 18.1. As an example, the matrices Lsym and Lrw associated with the graph G1
 例18.1。例如，与图g1相关的矩阵lsym和lrw

| are    网络错误 |                                                              |                                                              |                                                              |                                                              |                                                              |
| --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| and    网络错误 | ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif) | −10.0000.3536    网络错误   −00..28872887   −0.3536    网络错误   −    网络错误 | −00..40822887    网络错误   −1.0000    网络错误   −0.03333    网络错误 | 0    网络错误   −00..28873333    网络错误   −1.0000    网络错误   −0.4082    网络错误 | 0     网络错误   −0.3536    网络错误   0     网络错误   −0.4082    网络错误   1.0000    网络错误 |
|                 | ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif) | −10.0000.5000    网络错误   −00..33333333   −0.5000    网络错误   −    网络错误 | −00..50002500    网络错误   −1.0000    网络错误   −0.03333    网络错误 | 0    网络错误   −00..25003333    网络错误   −1.0000    网络错误   −0.5000    网络错误 | 0     网络错误   −0.2500    网络错误   0 .    网络错误   −0.3333    网络错误   1.0000    网络错误 |

Since the unnormalized Laplacian L can be written as L = BB>, where B is the incidence matrix of any oriented graph obtained from the underlying graph of G = (V,W), if we let
 由于非正规拉普拉斯L可以写成l=b b>，其中b是从基础图g=（v，w）得到的任何定向图的关联矩阵，如果我们

Bsym = D−1/2B,
 Bsym=d−1/2b，

we get
 我们得到

.
 .

In particular, for any singular decomposition Bsym = UΣV > of Bsym (with U an m × m orthogonal matrix, Σ a “diagonal” m×n matrix of singular values, and V an n×n orthogonal matrix), the eigenvalues of Lsym are the squares of the top m singular values of Bsym, and the vectors in U are orthonormal eigenvectors of Lsym with respect to these eigenvalues (the squares of the top m diagonal entries of Σ). Computing the SVD of Bsym generally yields more accurate results than diagonalizing Lsym, especially when Lsym has eigenvalues with high multiplicity.
 特别是对于任意一个bsym的奇异分解bsym=u∑v>（有u个m×m正交矩阵，∑一个“对角”m×n奇异值矩阵，v个n×n正交矩阵），lsym的特征值是bsym上m奇异值的平方，u中的向量是正交的。关于这些特征值的lsym的法向特征向量（∑的上m个对角线项的平方）。计算bsym的SVD通常比对角化lsym得到更精确的结果，特别是当lsym具有高重特征值时。

There are simple relationships between the eigenvalues and the eigenvectors of Lsym, and Lrw. There is also a simple relationship with the generalized eigenvalue problem Lx = λDx.
 LSYM和LRW的特征值与特征向量之间存在简单的关系。与广义特征值问题lx=λdx也有一个简单的关系。

Proposition 18.6. Let G = (V,W) be a weighted graph without isolated vertices. The graph Laplacians, L,Lsym, and Lrw satisfy the following properties:
 提案18.6.设g=（v，w）为无孤立顶点的加权图。拉普拉斯图、L、Lsym和Lrw满足以下特性：

### 18.3. NORMALIZED LAPLACIAN MATRICES OF GRAPHS  18.3。图的正规拉普拉斯矩阵

*(1)*         The matrix Lsym is symmetric and positive semidefinite. In fact,
 矩阵LSYM是对称的半正定矩阵。事实上，

​                                                                                                          for all x ∈ Rm.
 对于所有x∈rm。

*(2)*         The normalized graph Laplacians Lsym and Lrw have the same spectrum
 归一化图拉普拉斯函数lsym和lrw具有相同的谱。

(0 = ν1 ≤ ν2 ≤ ... ≤ νm), and a vector u 6 = 0is an eigenvector of Lrw for λ iff D/2u is an eigenvector of Lsym for λ.
 （0=霏1≤霏2≤…且向量u 6=0是λiff d/2u的lrw的特征向量是λ的lsym的特征向量。

*(3)*         The graph Laplacians L and Lsym are symmetric and positive semidefinite.
 图拉普拉斯l和lsym是对称的、半正定的。

*(4)*         A vector u = 06 is a solution of the generalized eigenvalue problem Lu = λDu iff D1/2u is an eigenvector of Lsym for the eigenvalue λ iff u is an eigenvector of Lrw for the eigenvalue λ.
 向量u=06是广义特征值问题lu=λdu iff d1/2u是特征值λ的LSYM特征向量，iff u是特征值λ的LRW特征向量。

*(5)*         The graph Laplacians, L and Lrw have the same nullspace. For any vector u, we have u ∈ Ker(L) iff D1/2u ∈ Ker(Lsym).
 图拉普拉斯，l和lrw有相同的空空间。对于任何向量u，我们都有u∈ker（l）iff d1/2u∈ker（lsym）。

*(6)*         The vector 1 is in the nullspace of Lrw, and D1/21 is in the nullspace of Lsym.
 矢量1在lrw的空空间中，d1/21在lsym的空空间中。

*(7)*         For every eigenvalue νi of the normalized graph Laplacian Lsym, we have 0 ≤ νi ≤ 2. Furthermore, νm = 2 iff the underlying graph of G contains a nontrivial connected bipartite component.
 对于归一化图拉普拉斯LSYM的每一个特征值，我们有0≤νi≤2。此外，如果g的下垫图包含一个非平凡的连接二部分量，则v m=2。

*(8)*         If m ≥ 2 and if the underlying graph of G is not a complete graph,1 then ν2 ≤ 1.
 如果m≥2，如果g的下垫图不是一个完整的图，1，则v 2≤1。

Furthermore the underlying graph of G is a complete graph iff.
 此外，G的底层图是一个完整的IFF图。

*(9)*         If m ≥ 2 and if the underlying graph of G is connected, then ν2 > 0.
 如果m≥2且G的下垫图连通，则v 2>0。

*(10)*    If m ≥ 2 and if the underlying graph of G has no isolated vertices, then .
 如果m≥2，并且g的基础图没有孤立的顶点，那么。

Proof. (1) We have Lsym = D−1/2LD−1/2, and D−1/2 is a symmetric invertible matrix (since it is an invertible diagonal matrix). It is a well-known fact of linear algebra that if B is an invertible matrix, then a matrix S is symmetric, positive semidefinite iff BSB> is symmetric, positive semidefinite. Since L is symmetric, positive semidefinite, so is Lsym = D−1/2LD−1/2. The formula
 证据。（1）我们有lsym=d−1/2ld−1/2，d−1/2是对称可逆矩阵（因为它是可逆对角矩阵）。线性代数的一个众所周知的事实是，如果b是可逆矩阵，那么矩阵s是对称的，半正定的iff bsb>是对称的，半正定的。因为l是对称的，半正定的，所以lsym=d−1/2ld−1/2也是。公式

​                                                                                                      for all x ∈ Rm
 对于所有x∈rm

follows immediately from Proposition 18.4 by replacing x by D−1/2x, and also shows that Lsym is positive semidefinite.
 紧随命题18.4，用d−1/2x替换x，还表明lsym是正半定的。

(2)   Since
 自从

Lrw = D−1/2LsymD1/2,
 lrw=d−1/2lsymd1/2，

the matrices Lsym and Lrw are similar, which implies that they have the same spectrum. In fact, since D1/2 is invertible,
 矩阵lsym和lrw相似，这意味着它们具有相同的光谱。实际上，由于d1/2是可逆的，

Lrwu = D−1Lu = λu
 LrWu=d−1lu=λu

iff
 敌我识别

D−1/2Lu = λD1/2u
 D−1/2lu=λd 1/2u

iff
 敌我识别

D−1/2LD−1/2D1/2u = LsymD1/2u = λD1/2u,
 d−1/2ld−1/2d 1/2u=lsymd1/2u=λd1/2u，

which shows that a vector u = 06 is an eigenvector of Lrw for λ iff D1/2u is an eigenvector of Lsym for λ.
 结果表明，对于λiff d1/2u，向量u=06是lrw的特征向量，对于λ，向量l=06是lsym的特征向量。

(3)   We already know that L and Lsym are positive semidefinite. (4) Since D−1/2 is invertible, we have
 我们已经知道l和lsym是正半定的。（4）由于d−1/2是可逆的，我们有

Lu = λDu
 Lu=λdu

iff
 敌我识别

D−1/2Lu = λD1/2u
 D−1/2lu=λd 1/2u

iff
 敌我识别

D−1/2LD−1/2D1/2u = LsymD1/2u = λD1/2u,
 d−1/2ld−1/2d 1/2u=lsymd1/2u=λd1/2u，

which shows that a vector u = 06 is a solution of the generalized eigenvalue problem Lu = λDu iff D1/2u is an eigenvector of Lsym for the eigenvalue λ. The second part of the statement follows from (2).
 结果表明，向量u=06是广义特征值问题lu=λdu iff d1/2u的解，是特征值λ的Lsym的特征向量。陈述的第二部分来自（2）。

(5)      Since D−1 is invertible, we have Lu = 0 iff D−1Lu = Lrwu = 0. Similarly, since D−1/2 is invertible, we have Lu = 0 iff D−1/2LD−1/2D1/2u = 0 iff D1/2u ∈ Ker(Lsym).
 因为d−1是可逆的，所以当d−1lu=lrwu=0时，我们得到lu=0。同样，由于d−1/2是可逆的，我们得到lu=0 iff d−1/2ld−1/2d1/2u=0 iff d1/2u∈ker（lsym）。

(6)      Since L1 = 0, we get Lrw1 = D−1L1 = 0. That D1/21 is in the nullspace of Lsym follows from (2). Properties (7)–(10) are proven in Chung [39] (Chapter 1). The eigenvalues the matrices Lsym and Lrw from Example 18.1 are
 因为l1=0，我们得到lrw1=d−1l1=0。d1/21在lsym的空白处，从（2）开始。性能（7）–（10）在Chung[39]中得到证明（第1章）。例18.1中矩阵lsym和lrw的特征值为

0, 7257, 1.1667, 1.5, 1.6076.
 0，7257，1.1667，1.5，1.6076。

On the other hand, the eigenvalues of the unormalized Laplacian for G1 are
 另一方面，非正规拉普拉斯的特征值为

0, 1.5858, 3, 4.4142, 5.
 0，1.5858，3，4.4142，5.

Remark: Observe that although the matrices Lsym and Lrw have the same spectrum, the matrix Lrw is generally not symmetric, whereas Lsym is symmetric.
 注：观察到尽管矩阵lsym和lrw具有相同的频谱，但矩阵lrw一般不对称，而lsym是对称的。

A version of Proposition 18.5 also holds for the graph Laplacians Lsym and Lrw. This follows easily from the fact that Proposition 18.1 applies to the underlying graph of a weighted graph. The proof is left as an exercise.
 命题18.5的一个版本也适用于拉普拉斯图lsym和lrw。这很容易从18.1命题适用于加权图的基础图这一事实得出。证据留作练习。

### 18.4. GRAPH CLUSTERING USING NORMALIZED CUTS  18.4。使用标准化切割的图形聚类

Proposition 18.7. Let G = (V,W) be a weighted graph. The number c of connected components K1,...,Kc of the underlying graph of G is equal to the dimension of the nullspace of both Lsym and Lrw, which is equal to the multiplicity of the eigenvalue 0. Furthermore, the nullspace of Lrw has a basis consisting of indicator vectors of the connected components of G, that is, vectors (f1,...,fm) such that fj = 1 iff vj ∈ Ki and fj = 0 otherwise. For Lsym, a basis of the nullpace is obtained by multiplying the above basis of the nullspace of Lrw by D1/2.
 提案18.7。设g=（v，w）为加权图。G下垫图的连通分量k1，…，kc的个数c等于Lsym和Lrw的空空间的维数，等于特征值0的重数。此外，LRW的零空间有一个由G的连通分量的指示向量构成的基，即向量（f1，…，fm），否则fj=1 iff vj∈ki，fj=0。对于lsym，空空间的基础是通过将lrw的空空间的上述基础乘以d1/2得到的。

A particularly interesting application of graph Laplacians is graph clustering.
 图拉普拉斯的一个特别有趣的应用是图聚类。

## 18.4           Graph Clustering Using Normalized Cuts  18.4使用标准化切割的图形聚类

In order to explain this problem we need some definitions.
 为了解释这个问题，我们需要一些定义。

Definition 18.20. Given any subset of nodes A ⊆ V , we define the volume vol(A) of A as the sum of the weights of all edges adjacent to nodes in A:
 定义18.20。给定节点a v的任何子集，我们将a的体积vol（a）定义为a中与节点相邻的所有边的权重之和：

m
 米

vol(A) = XXwij.
 体积（A）=xxwij。

vi∈A j=1
 vi∈a j=1

Given any two subsets A,B ⊆ V (not necessarily distinct), we define links(A,B) by
 对于任意两个子集a，b_v（不一定是不同的），我们定义链接（a，b）的方式是

links(A,B) = X wij.
 链接（a，b）=x wij。

vi∈A,vj∈B
 vi∈a，vj∈b

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

The quantity links(A,A) = links(A,A) (where A = V − A denotes the complement of A in V ) measures how many links escape from A (and A). We define the cut of A as
 数量链接（A，A）=Links（A，A）（其中A=V−A表示V中A的补码）测量从A（和A）中漏出的链接数。我们将a的切割定义为

cut(A) = links(A,A).
 剪切（A）=Links（A，A）。

The notion of volume is illustrated in Figure 18.5 and the notions of cut is illustrated in Figure 18.6.
 体积的概念如图18.5所示，切割的概念如图18.6所示。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image013.jpg)

Figure 18.5: Volume of a set of nodes.
 图18.5：一组节点的体积。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image015.jpg)

Figure 18.6: A cut involving the set of nodes in the center and the nodes on the perimeter.
 图18.6：包括中心节点集和周界节点的切口。

The above concepts play a crucial role in the theory of normalized cuts. This beautiful and deeply original method first published in Shi and Malik [155], has now come to be a “textbook chapter” of computer vision and machine learning. It was invented by Jianbo Shi and Jitendra Malik and was the main topic of Shi’s dissertation. This method was extended to K ≥ 3 clusters by Stella Yu in her dissertation [185] and is also the subject of Yu and Shi
 上述概念在标准化切割理论中起着至关重要的作用。这一优美而深刻的原创方法首次发表在Shi和Malik[155]上，现已成为计算机视觉和机器学习的“教科书章节”。它是石建波和马立克共同发明的，是石建波博士论文的主题。该方法在论文[185]中被Stella Yu推广到k≥3簇，也是Yu和Shi的研究课题。

[187].
 〔187〕。

Given a set of data, the goal of clustering is to partition the data into different groups according to their similarities. When the data is given in terms of a similarity graph G, where the weight wij between two nodes vi and vj is a measure of similarity of vi and vj, the problem can be stated as follows: Find a partition (A1,...,AK) of the set of nodes V into different groups such that the edges between different groups have very low weight (which indicates that the points in different clusters are dissimilar), and the edges within a group have high weight (which indicates that points within the same cluster are similar).
 给定一组数据，聚类的目的是根据数据的相似性将其划分为不同的组。当用相似度图G给出数据时，其中两个节点vi和vj之间的权重wij是vi和vj相似度的度量，问题可以表述为：将一组节点v的分区（a1，…，ak）分成不同的组，这样不同的组之间的边UPS的权重非常低（表示不同集群中的点不同），而一组中的边缘权重较高（表示同一集群中的点相似）。

The above graph clustering problem can be formalized as an optimization problem, using the notion of cut mentioned earlier. If we want to partition V into K clusters, we can do so by finding a partition (A1,...,AK) that minimizes the quantity
 利用前面提到的割的概念，上述图聚类问题可以形式化为一个优化问题。如果我们想把v划分成k簇，我们可以通过找到一个最小化数量的分区（a1，…，ak）来实现。

​                                                                      K                         K
 K-K

cut(links(Ai,Ai).
 剪切（链接（ai，ai）。

​                                                                     =1                       =1
 ＝1＝1

For K = 2, the mincut problem is a classical problem that can be solved efficiently, but in practice, it does not yield satisfactory partitions. Indeed, in many cases, the mincut solution separates one vertex from the rest of the graph. What we need is to design our cost function in such a way that it keeps the subsets Ai “reasonably large” (reasonably balanced).
 对于k=2，mincut问题是一个可以有效解决的经典问题，但在实际应用中，它不能产生令人满意的分区。实际上，在许多情况下，mincut解将一个顶点与图中的其他顶点分开。我们需要的是设计我们的成本函数，使子集合ai“相当大”（相当平衡）。

An example of a weighted graph and a partition of its nodes into two clusters is shown in Figure 18.7.
 图18.7显示了一个加权图及其节点划分为两个集群的示例。

### 18.5. SUMMARY  18.5。总结

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image017.gif)

Figure 18.7: A weighted graph and its partition into two clusters.
 图18.7：加权图及其划分成两个簇。

A way to get around this problem is to normalize the cuts by dividing by some measure of each subset Ai. A solution using the volume vol(Ai) of Ai (for K = 2) was proposed and investigated in a seminal paper of Shi and Malik [155]. Subsequently, Yu (in her dissertation [185]) and Yu and Shi [187] extended the method to K > 2 clusters. The idea is to minimize the cost function
 解决这个问题的一种方法是通过除以每个子集ai的某个度量来规范化切割。在Shi和Malik的一篇开创性论文[155]中，提出并研究了一种利用ai体积（k=2）的解决方案。随后，Yu（在她的论文[185]中）和Yu和Shi[187]将该方法扩展到k>2个簇。其思想是最小化成本函数

KK
 KK

Ncut(A1,...,AK) = X links(Ai,Ai) = X cut(Ai,Ai). i=1       vol(Ai)   i=1 vol(Ai)
 ncut（a1，…，ak）=x链接（ai，ai）=x剪切（ai，ai）。i=1卷（ai）i=1卷（ai）

The next step is to express our optimization problem in matrix form, and this can be done in terms of Rayleigh ratios involving the graph Laplacian in the numerators. This theory is very beautiful, but we do not have the space to present it here. The interested reader is referred to Gallier [70].
 下一步是用矩阵形式表示我们的优化问题，这可以用分子中含有拉普拉斯图的瑞利比来表示。这个理论很美，但是我们没有空间来展示它。感兴趣的读者可参考Gallier[70]。

## 18.5      Summary  18.5总结

The main concepts and results of this chapter are listed below:
 本章的主要概念和结果如下：

•     Directed graphs, undirected graphs.
 有向图，无向图。

•     Incidence matrices, adjacency matrices.
 关联矩阵，邻接矩阵。

•     Weighted graphs.
 加权图。

•     Degree matrix.
 度矩阵。

•     Graph Laplacian (unnormalized).
 拉普拉斯图（非标准化）。

•     Normalized graph Laplacian.
 规范化拉普拉斯图。

•     Spectral graph theory.
 光谱图理论。

•     Graph clustering using normalized cuts.
 使用标准化切割进行图形聚类。

## 18.6      Problems  18.6问题

Problem 18.1. Find the unnormalized Laplacian of the graph representing a triangle and of the graph representing a square.
 问题18.1。求表示三角形的图和表示正方形的图的非正规拉普拉斯。

Problem 18.2. Consider the complete graph Km on m ≥ 2 nodes.
 问题18.2。考虑m≥2个节点上的完整图km。

(1)   Prove that the normalized Laplacian Lsym of K is
 证明K的正规拉普拉斯LSYM是

|     网络错误   1    网络错误   −1/(m − 1) Lsym =  ...    网络错误       网络错误       网络错误   −1/(m − 1)    网络错误       网络错误   −1/(m − 1)    网络错误 | −1/(m1 − 1)    网络错误   ...    网络错误   −11//((mm −− 1)1)    网络错误   −    网络错误 | ...    网络错误   ... ...    网络错误   ...    网络错误   ...    网络错误 | −11//((.mm..−−   1)1)    网络错误   −    网络错误   1    网络错误   −1/(m − 1)    网络错误 | −1/(m −   1)    网络错误   −1/(m −   1)    网络错误              ...    .    网络错误   −1/(m − 1) 1    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |

(2)   Prove that the characteristic polynomial of Lsym is
 证明了LSYM的特征多项式是

 .
 .

Hint. First subtract the second column from the first, factor λ − m/(m − 1), and then add the first row to the second. Repeat this process. You will end up with the determinant
 暗示。首先从第一列中减去第二列，系数λ−m/（m−1），然后将第一行添加到第二行。重复此过程。你最终会得到行列式

.
 .

Problem 18.3. Consider the complete bipartite graph Km,n on m + n ≥ 3 nodes, with edges between each of the first m ≥ 1 nodes to each of the last n ≥ 1 nodes. Prove that the eigenvalues of the normalized Laplacian Lsym of Km,n are 0 with multiplicity m + n − 2 and 1 with multiplicity 2.
 问题18.3。考虑完整的二部图km，n在m+n≥3个节点上，第一个m≥1个节点与最后n≥1个节点之间的边。证明了m+n-2的归一化拉普拉斯LSYM的特征值为0，2的归一化拉普拉斯LSYM的特征值为1。

Problem 18.4. Let G be a graph with a set of nodes V with m ≥ 2 elements, without isolated nodes, and let Lsym = D−1/2LD−1/2 be its normalized Laplacian (with L its unnormalized Laplacian).
 问题18.4.设g为一组节点v的图，其中m≥2个元素，无孤立节点；设lsym=d−1/2ld−1/2为其归一化拉普拉斯函数（L为其非归一化拉普拉斯函数）。

### 18.6. PROBLEMS  18.6。问题

(1)   For any y ∈ RV , consider the Rayleigh ratio
 对于任意y∈rv，考虑瑞利比

.
 .

Prove that if x = D−1/2y, then
 证明如果x=d−1/2y，那么

.
 .

(2)   Prove that the second eigenvalue ν2 of Lsym is given by
 证明lsym的第二特征值v 2由下式给出

.
 .

(3)   Prove that the largest eigenvalue νm of Lsym is given by
 证明了lsym的最大特征值νm由下式给出

.
 .

Problem 18.5. Let G be a graph with a set of nodes V with m ≥ 2 elements, without isolated nodes. If 0 = ν1 ≤ ν1 ≤ ... ≤ νm are the eigenvalues of Lsym, prove the following properties:
 问题18.5。设g为一组节点v的图，其中m≥2个元素，没有孤立的节点。如果0=ν1≤ν1≤…≤νm是lsym的特征值，证明了以下性质：

(1)    We have ν1 + ν2 + ··· + νm = m.
 我们得到了，θ1+θ2+·········，θm=m。

(2)    We have ν2 ≤ m/(m−1), with equality holding iff G = Km, the complete graph on m nodes.
 我们得到了θ2≤m/（m-1），等式为iff g=km，m节点上的完整图。

(3)    We have νm ≥ m/(m − 1).
 我们有v m≥m/（m-1）。

(4)    If G is not a complete graph, then ν2 ≤ 1
 如果g不是一个完整的图，那么v 2≤1

Hint. If a and b are nonadjacent nodes, consider the function x given by
 暗示。如果a和b是非相邻节点，则考虑由

| ![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image019.gif) | if v = a if v = b    网络错误   if v =6          a,b,    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |

and use Problem 18.4(2).
 使用问题18.4（2）。

(5)    Prove that νm ≤ 2. Prove that νm = 2 iff the underlying graph of G contains a nontrivial connected bipartite component.
 证明νm≤2。证明了当g的底层图包含一个非平凡的连通二部分量时，νm=2。

Hint. Use Problem 18.4(3).
 暗示。使用问题18.4（3）。

(6)    Prove that if G is connected, then ν2 > 0.
 证明如果G连通，那么v 2>0。

Problem 18.6. Let G be a graph with a set of nodes V with m ≥ 2 elements, without isolated nodes. Let vol(G) = Pv∈V dv and let
 问题18.6.设g为一组节点v的图，其中m≥2个元素，没有孤立的节点。设vol（g）=pv∈v dv，设

.
 .

Prove that
 证明这一点

.
 .

Problem 18.7. Let G be a connected bipartite graph. Prove that if ν is an eigenvalue of Lsym, then 2 − ν is also an eigenvalue of Lsym.
 问题18.7。设G为连通二部图。证明如果nv是lsym的特征值，那么2−nv也是lsym的特征值。

Problem 18.8. Prove Proposition 18.7.
 问题18.8。证明18.7号提案。