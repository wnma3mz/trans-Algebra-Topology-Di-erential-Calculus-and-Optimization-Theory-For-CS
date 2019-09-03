第十九章

# Spectral Graph Drawing  光谱图绘制

## 19.1           Graph Drawing and Energy Minimization  19.1图形绘制和能量最小化

Let G = (V,E) be some undirected graph. It is often desirable to draw a graph, usually in the plane but possibly in 3D, and it turns out that the graph Laplacian can be used to design surprisingly good methods. Say |V | = m. The idea is to assign a point ρ(vi) in Rn to the vertex vi ∈ V , for every vi ∈ V , and to draw a line segment between the points ρ(vi) and ρ(vj) iff there is an edge {vi,vj}.
 设g=（v，e）为无向图。通常需要绘制一个图形，通常是在平面上，但可能是在三维中，结果证明，拉普拉斯图可以用来设计出奇的好方法。假设v=m，其思想是将RN中的点ρ（vi）赋给顶点vi∈v，对于每个vi∈v，并在点ρ（vi）和ρ（vj）之间画一条直线段，如果有边vi，vj。

Definition 19.1. Let G = (V,E) be some undirected graph with m vertices. A graph drawing is a function ρ: V → Rn, for some n ≥ 1. The matrix of a graph drawing ρ (in Rn) is a m × n matrix R whose ith row consists of the row vector ρ(vi) corresponding to the point representing vi in Rn.
 定义19.1.设g=（v，e）为具有m个顶点的无向图。图形绘制是函数ρ：v→rn，对于某些n≥1。图的矩阵ρ（在r n中）是m×n矩阵r，其第i行由行向量ρ（vi）组成，与在rn中表示vi的点相对应。

For a graph drawing to be useful we want n ≤ m; in fact n should be much smaller than m, typically n = 2 or n = 3.
 为了使图形绘图有用，我们希望n≤m；实际上n应该比m小得多，通常n=2或n=3。

Definition 19.2. A graph drawing is balanced iff the sum of the entries of every column of the matrix of the graph drawing is zero, that is,
 定义19.2.图的绘制是平衡的，如果图的矩阵的每一列的条目之和为零，也就是说，

1>R = 0.
 1>r=0。

If a graph drawing is not balanced, it can be made balanced by a suitable translation. We may also assume that the columns of R are linearly independent, since any basis of the column space also determines the drawing. Thus, from now on, we may assume that n ≤ m.
 如果图的绘制不平衡，可以通过适当的翻译使其平衡。我们也可以假设r的列是线性独立的，因为列空间的任何基础也决定了绘图。因此，从现在开始，我们可以假定n≤m。

Remark: A graph drawing ρ: V → Rn is not required to be injective, which may result in degenerate drawings where distinct vertices are drawn as the same point. For this reason, we prefer not to use the terminology graph embedding, which is often used in the literature. This is because in differential geometry, an embedding always refers to an injective map. The term graph immersion would be more appropriate.
 注：图的ρ：v→rn不需要求内射，这可能导致退化图，其中不同的顶点绘制为同一点。因此，我们不喜欢使用文献中经常使用的术语图嵌入。这是因为在微分几何中，嵌入总是指一个内射映射。术语图浸入更合适。

603
 六百零三

As explained in Godsil and Royle [77], we can imagine building a physical model of G by connecting adjacent vertices (in Rn) by identical springs. Then it is natural to consider a representation to be better if it requires the springs to be less extended. We can formalize this by defining the energy of a drawing R by
 如Godsil和Royle[77]所述，我们可以想象通过相同的弹簧连接相邻顶点（RN）来建立G的物理模型。那么，如果要求弹簧的延伸度较小，那么考虑更好的表示是很自然的。我们可以通过定义绘图r的能量

 ,
 ，

where ρ(vi) is the ith row of R and kρ(vi) − ρ(vj)k2 is the square of the Euclidean length of the line segment joining ρ(vi) and ρ(vj).
 其中，ρ（vi）是r的第i行，kρ（vi）−ρ（vj）k2是连接ρ（vi）和ρ（vj）的线段欧几里得长度的平方。

Then, “good drawings” are drawings that minimize the energy function E. Of course, the trivial representation corresponding to the zero matrix is optimum, so we need to impose extra constraints to rule out the trivial solution.
 那么，“好的图”就是把能量函数e最小化的图，当然，对应于零矩阵的平凡表示是最优的，所以我们需要施加额外的约束来排除平凡解。

We can consider the more general situation where the springs are not necessarily identical. This can be modeled by a symmetric weight (or stiffness) matrix W = (wij), with wij ≥ 0. Then our energy function becomes
 我们可以考虑弹簧不一定相同的更一般的情况。这可以通过对称重量（或刚度）矩阵w=（wij）来建模，wij≥0。然后我们的能量函数变成

 .
 .

It turns out that this function can be expressed in terms of the Laplacian L = D − W. The following proposition is shown in Godsil and Royle [77]. We give a slightly more direct proof.
 结果表明，该函数可以用拉普拉斯L=d−w表示。以下命题在Godsil和Royle[77]中给出。我们提供了一个更直接的证据。

Proposition 19.1. Let G = (V,W) be a weighted graph, with |V | = m and W an m × m symmetric matrix, and let R be the matrix of a graph drawing ρ of G in Rn (a m×n matrix).
 提案19.1。设g=（v，w）为加权图，其中v=m，w为m×m对称矩阵，r为Rn中g的图ρ的矩阵（m×n矩阵）。

If L = D − W is the unnormalized Laplacian matrix associated with W, then
 如果l=d−w是与w相关的非正规拉普拉斯矩阵，那么

E(R) = tr(R>LR).
 e（r）=tr（r>lr）。

Proof. Since ρ(vi) is the ith row of R (and ρ(vj) is the jth row of R), if we denote the kth column of R by Rk, using Proposition 18.4, we have
 证据。因为ρ（vi）是r的第i行（而ρ（vj）是r的第j行），如果我们用Rk表示r的第k列，用18.4号命题，我们得到

,
 ，

as claimed.                                                                                                                                         
 如要求。

### 19.1. GRAPH DRAWING AND ENERGY MINIMIZATION  19.1。图形绘制与能量最小化

Since the matrix R>LR is symmetric, it has real eigenvalues. Actually, since L is positive semidefinite, so is R>LR. Then the trace of R>LR is equal to the sum of its positive eigenvalues, and this is the energy E(R) of the graph drawing.
 由于矩阵r>lr是对称的，所以它具有实特征值。实际上，因为l是正半定的，所以r>lr也是。那么r>lr的迹线等于它的正特征值之和，这就是图的能量e（r）。

If R is the matrix of a graph drawing in Rn, then for any n×n invertible matrix M, the map that assigns ρ(vi)M to vi is another graph drawing of G, and these two drawings convey the same amount of information. From this point of view, a graph drawing is determined by the column space of R. Therefore, it is reasonable to assume that the columns of R are pairwise orthogonal and that they have unit length. Such a matrix satisfies the equation
 如果r是RN图的矩阵，那么对于任意n×n可逆矩阵m，将ρ（vi）m赋给vi的映射是g的另一个图，这两个图传递的信息量相同。从这个角度来看，图的绘制是由R的列空间决定的，因此，可以合理地假设R的列是成对正交的，并且它们有单位长度。这样的矩阵满足方程

R>R = I.
 r>r=i。

Definition 19.3. If the matrix R of a graph drawing satisfies the equation R>R = I, then the corresponding drawing is called an orthogonal graph drawing.
 定义19.3.如果图的矩阵r满足方程r>r=i，则相应的图称为正交图。

This above condition also rules out trivial drawings. The following result tells us how to find minimum energy orthogonal balanced graph drawings, provided the graph is connected. Recall that
 上述条件也排除了一些琐碎的绘图。下面的结果告诉我们如何找到最小能量正交平衡图，只要图是连接的。回想一下

L1 = 0,
 l1=0，

as we already observed.
 正如我们已经观察到的。

Theorem 19.2. Let G = (V,W) be a weighted graph with |V | = m. If L = D − W is the (unnormalized) Laplacian of G, and if the eigenvalues of L are 0 = λ1 < λ2 ≤ λ3 ≤ ... ≤ λm, then the minimal energy of any balanced orthogonal graph drawing of G in Rn is equal to λ2+···+λn+1 (in particular, this implies that n < m). The m×n matrix R consisting of any unit eigenvectors u2,...,un+1 associated with λ2 ≤ ... ≤ λn+1 yields a balanced orthogonal graph drawing of minimal energy; it satisfies the condition R>R = I.
 定理19.2。设g=（v，w）为v=m的加权图。如果l=d−w是g的（未归一化）拉普拉斯函数，如果l的特征值为0=λ1<λ2≤λ3≤…≤λm，则Rn中g的任意平衡正交图的最小能量等于λ2+·····+λn+1（特别是这意味着n<m）。由任意单位特征向量u2，…，un+1组成的m×n矩阵r与λ2≤…≤λn+1得到最小能量的平衡正交图，满足r>r=i的条件。

Proof. We present the proof given in Godsil and Royle [77] (Section 13.4, Theorem 13.4.1). The key point is that the sum of the n smallest eigenvalues of L is a lower bound for tr(R>LR). This can be shown using a Rayleigh ratio argument; see Proposition 16.25 (the Poincar´e separation theorem). Then any n eigenvectors (u1,...,un) associated with λ1,...,λn achieve this bound. Because the first eigenvalue of L is λ1 = 0 and because we are assuming that λ2 > 0, we have u1 = 1/√m. Since the uj are pairwise orthogonal for i = 2,...,n and since ui is orthogonal to u1 = 1/√m, the entries in ui add up to 0. Consequently, for any ` with 2 ≤ ` ≤ n, by deleting u1 and using (u2,...,u`), we obtain a balanced orthogonal graph drawing in R`−1 with the same energy as the orthogonal graph drawing in R` using (u1,u2,...,u`). Conversely, from any balanced orthogonal drawing in R`−1 using (u2,...,u`), we obtain an orthogonal graph drawing in R` using (u1,u2,...,u`) with the same energy. Therefore, the minimum energy of a balanced orthogonal graph drawing in Rn is equal to the minimum energy of an orthogonal graph drawing in Rn+1, and this minimum is λ2 + ··· + λn+1.  
 证据。我们给出了Godsil和Royle[77]中给出的证明（第13.4节，定理13.4.1）。关键是L的n个最小特征值之和是tr（r>lr）的下界。这可以用瑞利比论证来证明；见命题16.25（Poincar'e分离定理）。然后，任何与λ1，…，λn相关的n个特征向量（u1，…，un）都达到这个界限。因为l的第一个特征值是λ1=0，并且因为我们假设λ2>0，所以我们得到了u1=1/√m。由于uj对i=2是正交的，…，n并且因为ui对u1=1/√m是正交的，所以ui中的项加起来是0。因此，对于2≤`≤n的任意‘图，通过删除u1并使用（u2，…，u`），我们得到了r`-1中与r`使用（u1，u2，…，u`）中正交图绘制能量相同的平衡正交图。相反，利用（u2，…，u`）在r`-1中绘制平衡正交图，我们得到了能量相同的r``中使用（u1，u2，…，u`）绘制的正交图。因此，Rn中平衡正交图的最小能量等于Rn+1中正交图的最小能量，此最小能量为λ2+····+λn+1。

Since 1 spans the nullspace of L, using u1 (which belongs to KerL) as one of the vectors in R would have the effect that all points representing vertices of G would have the same first coordinate. This would mean that the drawing lives in a hyperplane in Rn, which is undesirable, especially when n = 2, where all vertices would be collinear. This is why we omit the first eigenvector u1.
 因为1跨越了l的空空间，使用u1（属于kerl）作为r中的向量之一会产生这样的效果，即表示g顶点的所有点都具有相同的第一坐标。这将意味着绘图生活在RN的超平面中，这是不可取的，尤其是当n=2时，所有顶点都将共线。这就是为什么我们省略了第一个特征向量U1。

Observe that for any orthogonal n × n matrix Q, since
 观察任何正交n×n矩阵q，因为

tr(R>LR) = tr(Q>R>LRQ),
 tr（r>lr）=tr（q>r>lrq）

the matrix RQ also yields a minimum orthogonal graph drawing. This amounts to applying the rigid motion Q> to the rows of R.
 矩阵RQ还生成最小正交图。这相当于将刚性运动q>应用于r行。

In summary, if λ2 > 0, an automatic method for drawing a graph in R2 is this:
 总之，如果λ2>0，在r2中绘制图形的自动方法是：

\1.    Compute the two smallest nonzero eigenvalues λ2 ≤ λ3 of the graph Laplacian L (it is possible that λ3 = λ2 if λ2 is a multiple eigenvalue);
 计算拉普拉斯L图的两个最小非零特征值λ2≤λ3（如果λ2是多特征值，则可能是λ3=λ2）；

\2.    Compute two unit eigenvectors u2,u3 associated with λ2 and λ3, and let R = [u2 u3] be the m × 2 matrix having u2 and u3 as columns.
 计算与λ2和λ3相关的两个单位特征向量u2、u3，并让r=[u2 u3]为m×2矩阵，其中u2和u3为列。

\3.    Place vertex vi at the point whose coordinates is the ith row of R, that is, (Ri1,Ri2).
 将顶点vi放在坐标为r的第i行的点上，即（ri1，ri2）。

This method generally gives pleasing results, but beware that there is no guarantee that distinct nodes are assigned distinct images since R can have identical rows. This does not seem to happen often in practice.
 这种方法通常会给出令人满意的结果，但是要注意，由于r可以有相同的行，所以不能保证为不同的节点分配不同的图像。这在实践中似乎并不经常发生。

## 19.2         Examples of Graph Drawings  19.2图表示例

We now give a number of examples using Matlab. Some of these are borrowed or adapted from Spielman [158].
 现在我们用matlab给出一些例子。其中一些是借用或改编自斯皮尔曼[158]。

Example 1. Consider the graph with four nodes whose adjacency matrix is
 例1。考虑具有四个节点的图，其邻接矩阵为

 .
 .

We use the following program to compute u2 and u3:
 我们使用以下程序计算u2和u3：

A = [0 1 1 0; 1 0 0 1; 1 0 0 1; 0 1 1 0];
 A=[0 1 1 0；1 0 0 1；1 0 0 1；0 1 1 0]；

D = diag(sum(A));
 d=diag（总和（a））；

L = D - A;
 L=D-A；

[v, e] = eigs(L); gplot(A, v(:,[3 2])) hold on; gplot(A, v(:,[3 2]),’o’)
 [V，E]=EIGS（L）；gplot（A，V（：，[3 2]）保持；gplot（A，V（：，[3 2]），'O'）

### 19.2. EXAMPLES OF GRAPH DRAWINGS  19.2。图形绘图示例

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.gif)

Figure 19.1: Drawing of the graph from Example 1.
 图19.1：示例1中的图形。

The graph of Example 1 is shown in Figure 19.1. The function eigs(L) computes the six largest eigenvalues of L in decreasing order, and corresponding eigenvectors. It turns out that λ2 = λ3 = 2 is a double eigenvalue.
 示例1的图表如图19.1所示。函数特征值（L）按降序计算L的六个最大特征值和相应的特征向量。结果表明，λ2=λ3=2是一个双特征值。

Example 2. Consider the graph G2 shown in Figure 18.3 given by the adjacency matrix
 例2。考虑图18.3所示的图g2，由邻接矩阵给出。

| 0    网络错误   1 A = 1    网络错误       网络错误   0    网络错误   0    网络错误 | 1    网络错误   0    网络错误   1    网络错误   1    网络错误   1    网络错误 | 1    网络错误   1    网络错误   0    网络错误   1    网络错误   0    网络错误 | 0    网络错误   1    网络错误   1    网络错误   0    网络错误   1    网络错误 | 0    网络错误   1    网络错误   0.    网络错误   1 0    网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |

We use the following program to compute u2 and u3:
 我们使用以下程序计算u2和u3：

A = [0 1 1 0 0; 1 0 1 1 1; 1 1 0 1 0; 0 1 1 0 1; 0 1 0 1 0];
 A=[0 1 1 0 0；1 0 1 1 1；1 1 0 1 0；0 1 0 1；0 1 0 1 0]；

D = diag(sum(A));
 d=diag（总和（a））；

L = D - A;
 L=D-A；

[v, e] = eig(L); gplot(A, v(:, [2 3])) hold on
 [V，E]=EIG（L）；gplot（A，V（：，[2 3]）保持

gplot(A, v(:, [2 3]),’o’)
 gplot（A，V（：，[2 3]），'O'）

The function eig(L) (with no s at the end) computes the eigenvalues of L in increasing order. The result of drawing the graph is shown in Figure 19.2. Note that node v2 is assigned to the point (0,0), so the difference between this drawing and the drawing in Figure 18.3 is that the drawing of Figure 19.2 is not convex.
 函数eig（l）（结尾没有s）按递增顺序计算l的特征值。绘制图表的结果如图19.2所示。请注意，节点v2被指定为点（0,0），因此此图与图18.3中的图之间的区别在于图19.2的图不是凸的。

Example 3. Consider the ring graph defined by the adjacency matrix A given in the Matlab program shown below:
 例3。考虑以下matlab程序中给出的邻接矩阵a定义的环图：

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

Figure 19.2: Drawing of the graph from Example 2.
 图19.2：示例2中的图表。

A = diag(ones(1, 11),1);
 A=diag（1，11，1）；

A = A + A’;
 A=A+A'；

A(1, 12) = 1; A(12, 1) = 1;
 A（1，12）=1；A（12，1）=1；

D = diag(sum(A));
 d=diag（总和（a））；

L = D - A;
 L=D-A；

[v, e] = eig(L); gplot(A, v(:, [2 3])) hold on
 [V，E]=EIG（L）；gplot（A，V（：，[2 3]）保持

gplot(A, v(:, [2 3]),’o’)
 gplot（A，V（：，[2 3]），'O'）

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

Figure 19.3: Drawing of the graph from Example 3.
 图19.3：示例3中的图形。

Observe that we get a very nice ring; see Figure 19.3. Again λ2 = 0.2679 is a double eigenvalue (and so are the next pairs of eigenvalues, except the last, λ12 = 4).
 观察我们得到了一个非常漂亮的戒指；见图19.3。同样，λ2=0.2679是一个双特征值（下一对特征值也是如此，除了最后一对，λ12=4）。

### 19.2. EXAMPLES OF GRAPH DRAWINGS  19.2。图形绘图示例

Example 4. In this example adapted from Spielman, we generate 20 randomly chosen points in the unit square, compute their Delaunay triangulation, then the adjacency matrix of the corresponding graph, and finally draw the graph using the second and third eigenvalues of the Laplacian.
 例4。在这个由Spielman改编的例子中，我们在单位平方中生成20个随机选择的点，计算它们的Delaunay三角剖分，然后计算相应图的邻接矩阵，最后利用拉普拉斯的第二和第三特征值绘制图。

A = zeros(20,20); xy = rand(20, 2); trigs = delaunay(xy(:,1), xy(:,2)); elemtrig = ones(3) - eye(3); for i = 1:length(trigs),
 A=零（20,20）；xy=rand（20,2）；trigs=delaunay（xy（：，1），xy（：，2））；elemtrig=一（3）-眼（3）；对于i=1：长度（trigs），

A(trigs(i,:),trigs(i,:)) = elemtrig; end
 a（trigs（i，：），trigs（i，：）=elemtrig；结束

A = double(A >0); gplot(A,xy) D = diag(sum(A));
 A=双（A>0）；gplot（A，xy）D=diag（sum（A））；

L = D - A;
 L=D-A；

[v, e] = eigs(L, 3, ’sm’); figure(2) gplot(A, v(:, [2 1])) hold on
 [V，E]=EIGS（L，3，'SM'）；图（2）gplot（A，V（：，[2 1]）保持

gplot(A, v(:, [2 1]),’o’)
 gplot（A，V（：，[2 1]），'O'）

The Delaunay triangulation of the set of 20 points and the drawing of the corresponding graph are shown in Figure 19.4. The graph drawing on the right looks nicer than the graph on the left but is is no longer planar.
 图19.4显示了20个点集的Delaunay三角测量和相应图形的绘制。右边的图形看起来比左边的图形好，但不再是平面图形。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

​                00 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 1         −0.4−0.4  −0.3 −0.2 −0.1 0   0.1 0.2 0.3     0.4
 00 0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 1−0.4−0.4−0.3−0.2−0.1 0.1 0.2 0.3 0.4

Figure 19.4: Delaunay triangulation (left) and drawing of the graph from Example 4 (right).
 图19.4：Delaunay三角测量（左）和示例4（右）中图形的绘制。

Example 5. Our last example, also borrowed from Spielman [158], corresponds to the skeleton of the “Buckyball,” a geodesic dome invented by the architect Richard Buckminster Fuller (1895–1983). The Montr´eal Biosph`ere is an example of a geodesic dome designed by Buckminster Fuller.
 例5。我们的最后一个例子，也借用了斯皮尔曼（Spielman）的著作[158]，与建筑师理查德·巴克明斯特·富勒（Richard Buckminster Fuller，1895-1983）发明的测地穹顶“Buckyball”的骨架相对应。蒙特利尔生物圈是巴克明斯特富勒设计的测地穹顶的一个例子。

A = full(bucky);
 A=满（Bucky）；

D = diag(sum(A));
 d=diag（总和（a））；

L = D - A;
 L=D-A；

[v, e] = eig(L); gplot(A, v(:, [2 3])) hold on;
 [V，E]=EIG（L）；gplot（A，V（：，[2 3]）保持；

gplot(A,v(:, [2 3]), ’o’)
 gplot（A，V（：，[2 3]），‘O’）

Figure 19.5 shows a graph drawing of the Buckyball. This picture seems a bit squashed for two reasons. First, it is really a 3-dimensional graph; second, λ2 = 0.2434 is a triple eigenvalue. (Actually, the Laplacian of L has many multiple eigenvalues.) What we should really do is to plot this graph in R3 using three orthonormal eigenvectors associated with λ2.
 图19.5显示了Buckyball的图形。这张照片似乎有点压扁，有两个原因。首先，它实际上是一个三维图；其次，λ2=0.2434是一个三重特征值。（实际上，L的拉普拉斯有许多多重特征值。）我们真正应该做的是用三个与λ2相关的正交特征向量在r3中绘制这个图。

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

Figure 19.5: Drawing of the graph of the Buckyball.
 图19.5：七叶树图。

A 3D picture of the graph of the Buckyball is produced by the following Matlab program, and its image is shown in Figure 19.6. It looks better!
 下面的matlab程序生成了Buckyball图形的三维图像，其图像如图19.6所示。看起来好多了！

[x, y] = gplot(A, v(:, [2 3]));
 [X，Y]=gplot（A，V（：，[2 3]）；

[x, z] = gplot(A, v(:, [2 4])); plot3(x,y,z)
 [X，Z]=gplot（A，V（：，[2 4]）；plot3（X，Y，Z）

## 19.3      Summary  19.3总结

The main concepts and results of this chapter are listed below:
 本章的主要概念和结果如下：

• Graph drawing.
 •图形绘制。

### 19.3. SUMMARY  19.3。总结

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image011.gif)

Figure 19.6: Drawing of the graph of the Buckyball in R3.
 图19.6:R3中Buckyball的图形。

•     Matrix of a graph drawing.
 图的矩阵。

•     Balanced graph drawing.
 平衡图绘制。

•     Energy E(R) of a graph drawing.
 图的能量e（r）。

•     Orthogonal graph drawing.
 正交图绘制。

•     Delaunay triangulation.
 Delaunay三角测量。

•     Buckyball.
 巴基鲍尔。


 