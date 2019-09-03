第二十七章

# Isometries of Hermitian Spaces  埃尔米特空间等距图

## 27.1     The Cartan–Dieudonn´e Theorem, Hermitian Case  27.1卡坦-迪乌登定理，赫米提亚案例

The Cartan-Dieudonn´e theorem can be generalized (Theorem 27.2), but this requires allowing new types of hyperplane reflections that we call Hermitian reflections. After doing so, every isometry in U(n) can always be written as a composition of at most n Hermitian reflections (for n ≥ 2). Better yet, every rotation in SU(n) can be expressed as the composition of at most 2n − 2 (standard) hyperplane reflections! This implies that every unitary transformation in U(n) is the composition of at most 2n−1 isometries, with at most one Hermitian reflection, the other isometries being (standard) hyperplane reflections. The crucial Proposition 12.2 is false as is, and needs to be amended. The QR-decomposition of arbitrary complex matrices in terms of Householder matrices can also be generalized, using a trick.
 卡坦-迪乌顿定理可以推广（定理27.2），但这需要允许新类型的超平面反射，我们称之为厄米特反射。这样做之后，u（n）中的每个等距线都可以写成至多n个厄米特反射（n≥2）的组合。更好的是，su（n）中的每个旋转可以表示为最多2n-2（标准）超平面反射的组成！这意味着u（n）中的每一个单位变换都是至多2n-1等距线的组成，其中至多一个厄米特反射，其他等距线是（标准）超平面反射。关键的12.2号提案是错误的，需要修改。利用一个技巧，也可以推广任意复杂矩阵在户主矩阵方面的二维分解。

In order to generalize the Cartan–Dieudonn´e theorem and the QR-decomposition in terms of Householder transformations, we need to introduce new kinds of hyperplane reflections. This is not really surprising, since in the Hermitian case, there are improper isometries whose determinant can be any unit complex number. Hyperplane reflections are generalized as follows.
 为了从户主变换的角度推广卡坦-迪乌顿定理和二维分解，需要引入新的超平面反射。这并不令人惊讶，因为在厄米提亚的例子中，有不适当的等距线，其行列式可以是任何单位复数。超平面反射一般如下。

Definition 27.1. Let E be a Hermitian space of finite dimension. For any hyperplane H, for any nonnull vector w orthogonal to H, so that E = H ⊕G, where G = Cw, a Hermitian reflection about H of angle θ is a linear map of the form ρH,θ : E → E, defined such that
 定义27.1.设e为有限维的厄米空间。对于任何超平面h，对于正交于h的任何非零矢量w，因此e=h_g，其中g=cw，关于θ角h的厄米反射是形式为ρh，θ：e→e的线性映射，其定义如下：

ρH,θ(u) = pH(u) + eiθpG(u),
 ρh，θ（u）=ph（u）+eiθpg（u），

for any unit complex number eiθ = 1 (6 i.e. θ =6 k2π). For any nonzero vector w ∈ E, we denote by ρw,θ the Hermitian reflection given by ρH,θ, where H is the hyperplane orthogonal to w.
 对于任何单位复数e iθ=1（6即θ=6 k2π）。对于任何非零矢量w∈e，我们用ρw，θ表示由ρh，θ给出的厄米反射，其中h是与w正交的超平面。

885
 八百八十五

Since u = pH(u) + pG(u), the Hermitian reflection ρw,θ is also expressed as
 由于u=ph（u）+pg（u），厄米反射ρw，θ也表示为

or as                                                                      
 或作为

Note that the case of a standard hyperplane reflection is obtained when eiθ = −1, i.e., θ = π.
 注意，标准超平面反射的情况是在e iθ=−1，即θ=π时得到的。

We leave as an easy exercise to check that ρw,θ is indeed an isometry, and that the inverse of ρw,θ is ρw,−θ. If we pick an orthonormal basis (e1,...,en) such that (e1,...,en−1) is an orthonormal basis of H, the matrix of ρw,θ is
 作为一个简单的练习，我们将检查ρw，θ确实是一个等距测量，并且ρw，θ的倒数是ρw，−θ。如果我们选取一个正交基（e1，…，en），使得（e1，…，en-1）是h的正交基，那么ρw，θ的矩阵是

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

We now come to the main surprise. Given any two distinct vectors u and v such that kusing two Hermitian reflections!uk = kvk, there isn’t always a hyperplane reflection mapping u to v, but this can be done
 我们现在主要的惊喜是。给任何两个截然不同的向量u和v，使kusing两个厄米提反射！Uk=kvk，不总是有一个超平面反射映射u到v，但这可以做到。

Proposition 27.1. Let E be any nontrivial Hermitian space.
 提案27.1.让我们成为任何非平凡的隐士空间。

*(1)*     thatthe (usual) reflectionFor any two vectorss(u) = eiθv. u,vs about the hyperplane orthogonal to the vector∈ E such that u =6      v and kuk = kvk, if u · vv=−eiθe−|uiθu· vis such|, then
 任意两个向量（u）=eiθv.u，vs关于与向量正交的超平面的（通常）反射∈e，使得u=6v，kuk=kvk，如果u·vv=−eiθe−uiθu·vis，那么

*(2)*     For any nonnull vector v ∈ E, for any unit complex number eiθ 6= 1, there is a Hermitian reflection ρv,θ such that
 对于任何非零向量v∈e，对于任何单位复数eiθ6=1，存在厄米反射ρv，θ，这样

ρv,θ(v) = eiθv.
 ρv，θ（v）=eiθv。

As a consequence, for u and v as in (1), we have ρv,−θ ◦ s(u) = v.
 因此，对于（1）中的u和v，我们有ρv，−θs（u）=v。

Proof. (1) Consider the (usual) reflection about the hyperplane orthogonal to w = v−e−iθu. We have
 证据。（1）考虑与w=v−e−iθu正交的超平面的（通常）反射。

.
 .

We need to compute
 我们需要计算

​                                    −2u · (v − e−iθu)    and    (v − e−iθu) · (v − e−iθu).
 −2u·（v−e−iθu）和（v−e−iθu）·（v−e−iθu）。

Since u · v = eiθ|u · v|, we have
 既然u·v=eiθu·v，我们有

​                                            e−iθu · v = |u · v|    and    eiθv · u = |u · v|.
 e−iθu·v=u·v和eiθv·u=u·v。

Using the above and the fact that kuk = kvk, we get
 利用上述和kuk=kvk的事实，我们得到

−2u · (v − e−iθu) = 2eiθiθ(kkuukk22−−2|uu ·· v,v|),
 −2u·（v−e−iθu）=2eiθiθ（kkukk22−2 uu··v，v），

= 2e
 = 2e

and
 和

(v  e−iθu)  (v − e−iθu) = kvk2 + kuk2 − e−iθu · v − eiθv · u,
 （v e−iθu）（v−e−iθu）=kvk2+kuk2−e−iθu·v−eiθv·u，

2
 二

= 2(kuk − |u · v|),
 =2（kuk−u·v），

and thus,
 因此，

.
 .

But then,
 但是后来，

and s(u) = eiθv, as claimed.
 和s（u）=eiθv，如权利要求所述。

(2) This part is easier. Consider the Hermitian reflection
 （2）这部分比较容易。想想赫敏的倒影

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

We have
 我们有

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

Thus, ρv,θ(v) = eiθv. Since ρv,θ is linear, changing the argument v to eiθv, we get
 因此，ρv，θ（v）=eiθv。由于ρv，θ是线性的，将参数v改为eiθv，我们得到

ρv,−θ(eiθv) = v,
 ρv，−θ（eiθv）=v，

and thus, ρv,−θ ◦ s(u) = v.                                                                                                                
 因此，ρv，−θs（u）=v。

Remarks:
 评论：

(1)    If we use the vector v + e−iθu instead of v − e−iθu, we get s(u) = −eiθv.
 如果我们使用向量v+e−iθu而不是v−e−iθu，我们得到s（u）=−eiθv。

(2)    Certain authors, such as Kincaid and Cheney [100] and Ciarlet [41], use the vector instead of our vector v + e−iθu. The effect of this choice is that they also get
 某些作者，如Kincaid和Cheney[100]和Ciarlet[41]，使用矢量而不是我们的矢量v+e-iθu。这种选择的效果是，他们还可以

s(u) = −e v.
 S（U）=-E V.

(3)    If v = kuke1, where e1 is a basis vector, u · e1 = a1, where a1 is just the coefficient of u over the basis vector e1. Then, since u · e1 = eiθ|a1|, the choice of the plus sign in the vector kuke1 + e−iθu has the effect that the coefficient of this vector over e1 is kuk+|a1|, and no cancellations takes place, which is preferable for numerical stability (we need to divide by the square norm of this vector).
 如果v=kuke1，其中e1是基向量，u·e1=a1，其中a1只是基向量e1上u的系数。那么，由于u·e1=e iθa1，在矢量kuke1+e iθu中选择加号，会影响到该矢量在e1上的系数是kuk+a1，并且不会发生取消，这对于数值稳定性更可取（我们需要除以该矢量的平方范数）。

The last part of Proposition 27.1 shows that the Cartan–Dieudonn´e is salvaged, since we can send u to v by a sequence of two Hermitian reflections when u =6 v and kuk = kvk, and since the inverse of a Hermitian reflection is a Hermitian reflection. Actually, because we are over the complex field, a linear map always have (complex) eigenvalues, and we can get a slightly improved result.
 第27.1号提案的最后一部分表明，卡坦-迪乌登的E被挽救了，因为当u=6 v和kuk=kvk时，我们可以通过两个厄米特反射序列将u发送到v，并且由于厄米特反射的倒数是厄米特反射。实际上，由于我们在复场上，线性映射总是有（复）特征值，我们可以得到一个稍微改进的结果。

Theorem 27.2. Let E be a Hermitian space of dimension n ≥ 1. Every isometry f ∈ U(E) is the composition f = ρn ◦ ρn−1 ◦ ··· ◦ ρ1 of n isometries ρj, where each ρj is either the identity or a Hermitian reflection (possibly a standard hyperplane reflection). When n ≥ 2, the identity is the composition of any hyperplane reflection with itself.
 定理27.2。设e为尺寸n≥1的厄米空间。每一个等距f∈u（e）是n个等距ρj的组成f=ρnρn−1····ρ1，其中每个ρj是同一性或厄米特反射（可能是标准超平面反射）。当n≥2时，同一性是任何超平面反射本身的组成。

Proof. We prove by induction on n that there is an orthonormal basis of eigenvectors (u1,...,un) of f such that f(uj) = eiθjuj,
 证据。我们通过n的归纳证明了f的特征向量（u1，…，un）有一个正交基，这样f（uj）=eiθjuj，

where eiθj is an eigenvalue associated with uj, for all j, 1 ≤ j ≤ n.
 式中，eiθj是与uj相关的特征值，对于所有j，1≤j≤n。

When n = 1, every isometry f ∈ U(E) is either the identity or a Hermitian reflection ρθ, since for any nonnull vector u, we have f(u) = eiθu for some θ. We let u1 be any nonnull unit vector.
 当n=1时，每一个等距f∈u（e）要么是恒等式，要么是厄米反射ρθ，因为对于任何非零向量u，对于某些θ，我们有f（u）=eiθu。我们让u1是任何非空的单位向量。

Let us now consider the case where n ≥ 2. Since C is algebraically closed, the characteristic polynomial det(f − λid) of f has n complex roots which must be the form1 eiθ, since they have absolute value 1. Pick any such eigenvalue1 eiθ , and pick any eigenvector u1 = 06 of f for eiθ of unit length. If F = Cu1 is the subspace spanned by u1, we have f(F) = F, since f(u1) = eiθ1u1. Since f(F) = F and f is an isometry, it is easy to see that f(F ⊥) ⊆ F ⊥, and by Proposition 13.13, we have E = F ⊕ F ⊥. Furthermore, it is obvious that the restriction of f to F ⊥ is unitary. Since dim(F ⊥) = n − 1, we can apply the induction hypothesis to F ⊥, and we get an orthonormal basis of eigenvectors (u2,...,un) for F ⊥ such that
 现在让我们考虑n≥2的情况。因为c是代数闭的，所以f的特征多项式det（f-λid）有n个复数根，因为它们的绝对值为1，所以它们必须是形式1 eiθ。选取任意一个这样的特征值1 eiθ，对于单位长度的eiθ，选取任意一个f的特征向量u1=06。如果f=cu1是u1所跨越的子空间，我们得到f（f）=f，因为f（u1）=eiθ1u1。因为f（f）=f和f是一个等距，很容易看出f（f）f，根据命题13.13，我们得到e=f f。此外，F对F的限制是单一的。由于dim（f）=n-1，我们可以将诱导假设应用于f，我们得到f的特征向量（u2，…，un）的正态基，这样

f(uj) = eiθjuj,
 f（uj）=eiθjuj，

where eiθj is an eigenvalue associated with uj, for all j, 2 ≤ j ≤ n Since E = F ⊕ F ⊥ and F = Cu1, the claim is proved. But then, if ρj is the Hermitian reflection about the hyperplane Hj orthogonal to uj and of angle θj, it is obvious that
 式中，eiθj是与uj相关的特征值，对于所有j，2≤j≤n，因为e=f_f和f=cu1，证明了该权利要求。但是，如果ρj是与uj正交的超平面hj和θj角的厄米反射，那么很明显

f = ρθn ◦ ··· ◦ ρθ1.
 f=ρθn···ρθ1.

When n ≥ 2, we have id = s ◦ s for every reflection s.                                                                    
 当n≥2时，每个反射s的id=s_s。

Remarks:
 评论：

(1)    Any isometry f ∈ U(n) can be express as f = ρθ◦g, where g ∈ SU(n) is a rotation, and ρθ is a Hermitian reflection. Indeed, by the above theorem, with respect to the basis (u1,...,un), det(f) = ei(θ1+···+θn), and letting θ = θ1 +···+θn and ρθ be the Hermitian reflection about the hyperplane orthogonal to u1 and of angle θ, since ρθ ◦ ρ−θ = id, we have
 任何等距f∈u（n）都可以表示为f=ρθ_g，其中g∈su（n）是一个旋转，而ρθ是一个厄米反射。实际上，根据上述定理，关于基（u1，…，un），Det（f）=ei（θ1+·····+θn），并让θ=θ1+······+θn和ρθ是关于与u1正交的超平面和角θ的厄米反射，因为ρθρ−θ=id，我们有

f = (ρθ ◦ ρ−θ) ◦ f = ρθ ◦ (ρ−θ ◦ f).
 f=（ρθρ−θ）f=ρθ（ρ−θf）。

LettingbetweengS=1 ×ρ−SUθ ◦f(, it is obvious that det(n) and U(n), where S1g) = 1is the unit circle (which corresponds to the. As a consequence, there is a bijection group of complex numbers eiθ of unit length). In fact, it is a homeomorphism.
 LettingBetweengs=1×ρ−suθf（，很明显，det（n）和u（n），其中s1g）=1是单位圆（对应于。因此，有一个复数的双射群，单位长度为eiθ）。事实上，它是同态的。

(2)    We abandoned the style of proof used in theorem 26.1, because in the Hermitian case, eigenvalues and eigenvectors always exist, and the proof is simpler that way (in the real case, an isometry may not have any real eigenvalues!). The sacrifice is that the theorem yields no information on the number of (standard) hyperplane reflections. We shall rectify this situation shortly.
 我们放弃了定理26.1中使用的证明方式，因为在厄米提亚情况下，特征值和特征向量总是存在的，而且这种证明方式更简单（在实际情况下，等距测量可能没有任何实际特征值！）.牺牲是，该定理不产生有关（标准）超平面反射数的信息。我们将很快纠正这种情况。

We will now reveal the beautiful trick (found in Mneimn´e and Testard [124]) that allows us to prove that every rotation in SU(n) is the composition of at most 2n − 2 (standard) hyperplane reflections. For what follows, it is more convenient to denote a standard reflection about the hyperplane H as hu (it is trivial that these do not depend on the choice of u in H⊥). Then, given any two distinct orthogonal vectors u,v such that kuk = kvk, consider the composition ρv,−θ ◦ρu,θ. The trick is that this composition can be expressed as two standard hyperplane reflections! This wonderful fact is proved in the next Proposition.
 我们现在将展示一个漂亮的技巧（在mneimn'e和testard[124]中发现），它允许我们证明su（n）中的每个旋转都是至多2n-2（标准）超平面反射的组成。对于以下内容，将超平面h的标准反射表示为h u更为方便（这些不依赖于h中u的选择，这是微不足道的）。然后，给任意两个不同的正交向量u，v，使kuk=kvk，考虑组成ρv，−θρu，θ。诀窍是这种合成可以表示为两个标准超平面反射！这个奇妙的事实在下一个命题中得到了证明。

Proposition 27.3. Let E be a nontrivial Hermitian space. For any two distinct orthogonal vectors u,v such that kuk = kvk, we have
 提案27.3.让我们成为一个非平凡的隐士空间。对于任意两个不同的正交向量u，v，如kuk=kvk，我们有

ρv,−θ ◦ ρu,θ = hv−u ◦ hv−e−iθu = hu+v ◦ hu+eiθv.
 ρv，−θρu，θ=hv−u hv−e−iθu=hu+v hu+eiθv.

Proof. Since u and v are orthogonal, each one is in the hyperplane orthogonal to the other, and thus,
 证据。因为u和v是正交的，所以每个都在与另一个正交的超平面中，因此，

ρu,θ(u) = eiθu, ρu,θ(v) = v,
 ρu，θ（u）=eiθu，ρu，θ（v）=v，

ρv,−θ(u) = u, ρv,−θ(v) = e−iθv, hv−u(u) = v, hv−u(v) = u,
 ρv，−θ（u）=u，ρv，−θ（v）=e−iθv，hv−u（u）=v，hv−u（v）=u，

hv−e−iθu(u) = eiθv,
 hv−e−iθu（u）=eiθv，

hv−e−iθu(v) = e−iθu.
 hv−e−iθu（v）=e−iθu。

Consequently, using linearity,
 因此，使用线性，

ρv,−θ ◦ ρu,θ(u) = eiθu, ρv,−θ ◦ ρu,θ(v) = e−iθv,
 ρv，−θρu，θ（u）=e iθu，ρv，−θρu，θ（v）=e-iθv，

hv−u ◦ hv−e−iθu(u) = eiθu, hv−u ◦ hv−e−iθu(v) = e−iθv, and since both ρv,−θ ◦ρu,θ and hv−u ◦hv−e−iθu are the identity on the orthogonal complement of {u,v}, they are equal. Since we also have
 hv−u hv−e−iθu（u）=eiθu，hv−u hv−e−iθu（v）=e−iθv，并且由于ρv、−θρu、θ和hv−u hv−e−iθu是u、v的正交补码上的恒等式，因此它们是相等的。因为我们也有

hu+v(u) = −v, hu+v(v) = −u,
 hu+v（u）=-v，hu+v（v）=-u，

hu+eiθv(u) = −eiθv,
 hu+eiθv（u）=−eiθv，

hu+eiθv(v) = −e−iθu,
 hu+e iθv（v）=−e−iθu，

it is immediately verified that
 立即证实

hv−u ◦ hv−e−iθu = hu+v ◦ hu+eiθv.
 hv−u hv−e−iθu=hu+v hu+eiθv.

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image007.gif)

We will use Proposition 27.3 as follows.
 我们将使用27.3号提案，如下所示。

Proposition 27.4. Let E be a nontrivial Hermitian space, and let (u1,...,un) be some orthonormal basis for E. For any θ1,...,θn such that θ1 + ··· + θn = 0, if f ∈ U(n) is the isometry defined such that
 提案27.4.设e为非平凡厄米空间，设（u1，…，u n）为e的一些正交基，对于任何θ1，…，θn，使θ1+·····+θn=0，如果f∈u（n）是等距线，定义如下：

f(uj) = eiθjuj,
 f（uj）=eiθjuj，

for all j, 1 ≤ j ≤ n, then f is a rotation (f ∈ SU(n)), and
 对于所有j，1≤j≤n，那么f是一个旋转（f∈su（n）），并且

f = ρun,θn ◦ ··· ◦ ρu1,θ1
 f=ρun，θn····ρu1，θ1

= ρun,−(θ1+···+θn−1) ◦ ρun−1,θ1+···+θn−1 ◦ ··· ◦ ρu2,−θ1 ◦ ρu1,θ1
 =ρun，−（θ1+···+θn−1）ρun−1，θ1+····+θn−1··································

= hun−un−1 ◦ hun−e−i(θ1+···+θn−1)un−1 ◦ ··· ◦ hu2−u1 ◦ hu2−e−iθ1u1 = hun−1+un ◦ hun−1+ei(θ1+···+θn−1)un ◦ ··· ◦ hu1+u2 ◦ hu1+eiθ1u2.
 =hun−un−1 hun−e−i（θ1+·····+θn−1）un−1·································································

Proof. It is obvious from the definitions that
 证据。从定义上看，很明显

f = ρun,θn ◦ ··· ◦ ρu1,θ1,
 f=ρun，θn····ρu1，θ1，

and since the determinant of f is
 既然f的行列式是

D(f) = eiθ1 ···eiθn = ei(θ1+···+θn)
 d（f）=eiθ1···eiθn=ei（θ1+···+θn）

and θ1 + ··· + θn = 0, we have D(f) = e0 = 1, and f is a rotation. Letting
 θ1+·····+θn=0，我们得到d（f）=e0=1，f是一个旋转。出租

fk = ρuk,−(θ1+···+θk−1) ◦ ρuk−1,θ1+···+θk−1 ◦ ··· ◦ ρu3,−(θ1+θ2) ◦ ρu2,θ1+θ2 ◦ ρu2,−θ1 ◦ ρu1,θ1,
 fk=ρuk，−（θ1+···+θk−1）ρuk−1，θ1+····+θk−1····················································

| we prove   by induction on k, 2 ≤ k ≤ n, that    通过对k，2≤k≤n的诱导，我们证明 |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
|  iθjuj e    iθjuj e       γ                                           fk(uj)   = e−i(θ1+···+θk−1)uk    fk（uj）=e−i（θ1+····+θk−1）英国   uj    UJ | if 1 ≤ j ≤ k − 1, if j = k, and if k + 1 ≤ j ≤ n.    如果1≤j≤k−1，如果j=k，如果k+1≤j≤n。 |

The base case was treated in Proposition 27.3. Now, the proof of Proposition 27.3 also showed that
 基本情况在提案27.3中进行了处理。现在，27.3号提案的证明也表明

ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk(uk) = ei(θ1+···+θk)uk, ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk(uk+1) = e−i(θ1+···+θk)uk+1,
 ρuk+1，−（θ1+····+θk）ρuk，θ1+····+θk（uk）=e i（θ1+·····+θk）uk，ρuk+1，−（θ1+·····+θk）ρuk，θ1+·······+θk（uk+1）=e−i（θ1+····+θk）uk+1，

and thus, using the induction hypothesis for k (2 ≤ k ≤ n − 1), we have
 因此，利用k（2≤k≤n-1）的诱导假设，我们得出

fk+1(uj) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk ◦ fk(uj) = eiθjuj, 1 ≤ j ≤ k − 1, fk+1(uk) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk ◦ fk(uk) = ei(θ1+···+θk)e−i(θ1+···+θk−1)uk = eiθkuk, fk+1(uk+1) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk ◦ fk(uk+1) = e−i(θ1+···+θk)uk+1, fk+1(uj) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk ◦ fk(uj) = uj, k + 1 ≤ j ≤ n, which proves the induction step.
 fk+1(uj) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk ◦ fk(uj) = eiθjuj, 1 ≤ j ≤ k − 1, fk+1(uk) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk ◦ fk(uk) = ei(θ1+···+θk)e−i(θ1+···+θk−1)uk = eiθkuk, fk+1(uk+1) = ρuk+1,−(θ1+···+θk) ◦ ρuk,θ1+···+θk fk（uk+1）=e−i（θ1+····+θk）uk+1，fk+1（uj）=ρuk+1，−（θ1+······+θk）ρuk，θ1+······+θk fk（uj）=uj，k+1≤j≤n，证明了诱导步骤。

As a summary, we proved that
 总之，我们证明了

​                                                       (eiθjuj                         if 1 ≤ j ≤ n − 1,
 （eiθjuj，如果1≤j≤n-1，

​                                        fn(uj) =  e−i(θ1+···+θn−1)un  when j = n,
 当j=n时，fn（uj）=e−i（θ1+····+θn−1）un，

but since θ1 +···+θn = 0, we have θn = −(θ1 +···+θn−1), and the last expression is in fact
 但由于θ1+····+θn=0，我们得到了θn=−（θ1+····+θn-1），最后一个表达式实际上是

fn(un) = eiθnun. Therefore, we proved that
 fn（un）=eiθnun。因此，我们证明

f = ρun,θn ◦ ··· ◦ ρu1,θ1 = ρun,−(θ1+···+θn−1) ◦ ρun−1,θ1+···+θn−1 ◦ ··· ◦ ρu2,−θ1 ◦ ρu1,θ1,
 f=ρun，θn··········································································

and using Proposition 27.3, we also have
 利用27.3号提案，我们也有

f = ρun,−(θ1+···+θn−1) ◦ ρun−1,θ1+···+θn−1 ◦ ··· ◦ ρu2,−θ1 ◦ ρu1,θ1
 F=ρun，−（θ1+···+θn−1）ρun−1，θ1+·····+θn−1·································

= hun−un−1 ◦ hun−e−i(θ1+···+θn−1)un−1 ◦ ··· ◦ hu2−u1 ◦ hu2−e−iθ1u1
 =hun−un−1 hun−e−i（θ1+······+θn−1）un−1····hu2 hu2−e−iθ1U1

= hun−1+un ◦ hun−1+ei(θ1+···+θn−1)un ◦ ··· ◦ hu1+u2 ◦ hu1+eiθ1u2,
 =hun−1+un hun−1+ei（θ1+····+θn−1）un····hu1+u2 hu1+eiθ1u2，

which completes the proof.                                                                                                              
 这就完成了证明。

We finally get our improved version of the Cartan–Dieudonn´e theorem.
 我们最后得到了改进版的卡坦-迪乌顿定理。

Theorem 27.5. Let E be a Hermitian space of dimension n ≥ 1. Every rotation f ∈ SU(E) different from the identity is the composition of at most 2n−2 standard hyperplane reflections. Every isometry f ∈ U(E) different from the identity is the composition of at most 2n − 1 isometries, all standard hyperplane reflections, except for possibly one Hermitian reflection.
 定理27.5。设e为尺寸n≥1的厄米空间。每一个不同于同一性的旋转f∈su（e）是2n-2标准超平面反射的组成。每一个与同一性不同的等距f∈u（e），最多是2n-1等距的组成，所有标准超平面反射，除了可能的一个厄米特反射。

When n ≥ 2, the identity is the composition of any reflection with itself.
 当n≥2时，同一性是任何反射本身的组成。

Proof. By Theorem 27.2, f ∈ SU(n) can be written as a composition
 证据。根据定理27.2，f∈su（n）可以写成一个组合

ρun,θn ◦ ··· ◦ ρu1,θ1,
 ρun，θn····ρu1，θ1，

where (u1,...,un) is an orthonormal basis of eigenvectors. Since f is a rotation, det(f) = 1, and this implies that θ1 + ··· + θn = 0. By Proposition 27.4,
 其中（u1，…，un）是特征向量的正交基。因为f是一个旋转，Det（f）=1，这意味着θ1+····+θn=0。根据27.4号提案，

f = hun−un−1 ◦ hun−e−i(θ1+···+θn−1)un−1 ◦ ··· ◦ hu2−u1 ◦ hu2−e−iθ1u1,
 F=hun−un−1 hun−e−i（θ1+······+θn−1）un−1·····························

a composition of 2n − 2 hyperplane reflections. In general, if f ∈ U(n), by the remark after Theorem 27.2, f can be written as f = ρθ ◦ g, where g ∈ SU(n) is a rotation, and ρθ is a Hermitian reflection. We conclude by applying what we just proved to g. 
 2n-2超平面反射的组成。一般来说，如果f∈u（n），通过定理27.2后的注释，f可以写成f=ρθg，其中g∈su（n）是一个旋转，而ρθ是一个厄米反射。最后，我们将刚才证明的应用于G。

As a corollary of Theorem 27.5, the following interesting result can be shown (this is not hard, do it!). First, recall that a linear map f : E → E is self-adjoint (or Hermitian) iff f = f∗. Then, the subgroup of U(n) generated by the Hermitian isometries is equal to the group
 作为定理27.5的推论，可以得出以下有趣的结果（这并不难，做吧！）首先，回想一下线性映射f:e→e是自伴（或厄米提安）iff=f。然后，由厄米提亚等距线生成的u（n）子群等于该群

SU(n)± = {f ∈ U(n) | det(f) = ±1}.
 su（n）±=f∈u（n）det（f）=±1。

Equivalently, SU(n)± is equal to the subgroup of U(n) generated by the hyperplane reflections.
 同样地，su（n）±等于由超平面反射产生的u（n）的子群。

This problem had been left open by Dieudonn´e in [50]. Evidently, it was settled since the publication of the third edition of the book [50].
 Dieudonn'e在[50]年公开了这个问题。显然，这本书自第三版出版以来就已得到解决。

Inspection of the proof of Proposition 26.4 reveals that this Proposition also holds for Hermitian spaces. Thus, when n ≥ 3, the composition of any two hyperplane reflections is equal to the composition of two flips. As a consequence, a version of Theorem 26.5 holds for rotations in a Hermitian space of dimension at least 3.
 对26.4号命题的证明的检验表明，这个命题也适用于赫敏空间。因此，当n≥3时，任意两个超平面反射的合成等于两个翻转的合成。因此，定理26.5的一个版本适用于至少3维的厄米空间中的旋转。

Theorem 27.6. Let E be a Hermitan space of dimension n ≥ 3. Every rotation f ∈ SU(E) is the composition of an even number of flips f = f2k ◦···◦f1, where k ≤ n−1. Furthermore, if u = 06 is invariant under f (i.e. u ∈ Ker(f − id)), we can pick the last flip f2k such that , where F2k is the subspace of dimension n − 2 determining f2k.
 定理27.6。设e为尺寸n≥3的埃尔米坦空间。每个旋转f∈su（e）是偶数个翻转f=f2k·····f1的组合，其中k≤n−1。此外，如果u=06在f（即u∈ker（f−id））下是不变的，我们可以选取最后一个翻转f2k，其中f2k是确定f2k的n−2维的子空间。

Proof. It is identical to that of Theorem 26.5, except that it uses Theorem 27.5 instead of Theorem 26.1. The second part of the Proposition also holds, because if u = 06 is an eigenvector of f for 1, then u is one of the vectors in the orthonormal basis of eigenvectors used in 27.2. The details are left as an exercise. 
 证据。它与定理26.5相同，只是它使用了定理27.5而不是定理26.1。命题的第二部分也成立，因为如果u=06是f的1的特征向量，那么u是27.2中使用的特征向量的正交基中的向量之一。细节留作练习。

We now show that the QR-decomposition in terms of (complex) Householder matrices holds for complex matrices. We need the version of Proposition 27.1 and a trick at the end of the argument, but the proof is basically unchanged.
 我们现在证明，用（复杂）户主矩阵进行的QR分解适用于复杂矩阵。我们需要27.1号提案的版本和在辩论结束时的技巧，但是证据基本上是不变的。

Proposition 27.7. Let E be a nontrivial Hermitian space of dimension n. Given any orthonormal basis (e1,...,en), for any n-tuple of vectors (v1,...,vn), there is a sequence of n − 1 isometries h1,...,hn−1, such that hi is a hyperplane reflection or the identity, and if (r1,...,rn) are the vectors given by
 提案27.7.设e为维数n的非平凡厄米空间。给定任意正交基（e1，…，en），对于向量（v1，…，vn）的任意n元组，有一个n-1等距线h1，…，hn-1的序列，使得hi是超平面反射或恒等式，如果（r1，…，rn）是

​                                           rj = hn−1 ◦ ··· ◦ h2 ◦ h1(vj)    1 ≤ j ≤ n,
 rj=hn−1·····h2 h1（vj）1≤j≤n，

then every rj is a linear combination of the vectors (e1,...,ej), (1 ≤ j ≤ n). Equivalently, the matrix R whose columns are the components of the rj over the basis (e1,...,en) is an upper triangular matrix. Furthermore, if we allow one more isometry hn of the form
 然后，每个RJ是向量（e1，…，ej），（1≤j≤n）的线性组合。等价地，其列是基上RJ的分量的矩阵r（e1，…，en）是上三角矩阵。此外，如果我们允许形式的另一个等值线hn

hn = ρen,ϕn ◦ ··· ◦ ρe1,ϕ1
 hn=ρen，n···ρe1，_

after h1,...,hn−1, we can ensure that the diagonal entries of R are nonnegative.
 在h1，…，hn−1之后，我们可以确保r的对角线项是非负的。

Proof. The proof is very similar to the proof of Proposition 12.3, but it needs to be modified a little bit since Proposition 27.1 is weaker than Proposition 12.2. We explain how to modify the induction step, leaving the base case and the rest of the proof as an exercise.
 证据。证明与12.3号提案的证明非常相似，但由于27.1号提案弱于12.2号提案，因此需要对其稍作修改。我们将解释如何修改归纳步骤，将基本情况和其他证明作为练习。

As in the proof of Proposition 12.3, the vectors (e1,...,ek) form a basis for the subspace denoted as Uk0, the vectors (ek+1,...,en) form a basis for the subspace denoted as Uk00, the subspaces  and  are orthogonal, and . Let
 在命题12.3的证明中，向量（e1，…，ek）构成表示为UK0的子空间的基础，向量（ek+1，…，en）构成表示为UK00的子空间的基础，子空间和是正交的，以及。让

uk+1 = hk ◦ ··· ◦ h2 ◦ h1(vk+1).
 UK+1=hk····h2 h1（vk+1）。

We can write
 我们可以写信

,
 ，

where u0k+1 ∈ Uk0 and. Let
 其中U0K+1∈UK0和。让

​                                            ,                     and                              .
 ，和。

If, we let hk+1 = id. Otherwise, by Proposition 27.1, there is a
 如果，我们让hk+1=id。否则，根据27.1号提案，有一个

unique hyperplane reflection hk+1 such that
 独特的超平面反射hk+1

hk+1(u00k+1) = eiθk+1rk+1,k+1 ek+1,
 hk+1（u00k+1）=eiθk+1rk+1，k+1 ek+1，

where hk+1 is the reflection about the hyperplane Hk+1 orthogonal to the vector
 其中，hk+1是垂直于向量的超平面hk+1的反射。

.
 .

At the end of the induction, we have a triangular matrix R, but the diagonal entries eiθjrj,j of R may be complex. Letting
 在归纳的最后，我们得到了一个三角形的矩阵r，但是r的对角线项eiθj r j，j可能是复杂的。出租

hn+1 = ρen,−θn ◦ ··· ◦ ρe1,−θ1,
 hn+1=ρen，−θn····ρe1，−θ1，

we observe that the diagonal entries of the matrix of vectors
 我们观察到向量矩阵的对角项

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image009.gif)

is triangular with nonnegative entries.                                                                                           
 是带有非负项的三角形。

Remark: For numerical stability, it is preferable to use wk+1 = rk+1,k+1 ek+1 + e−iθk+1u00k+1 instead of wk+1 = rk+1,k+1 ek+1 − e−jiθk+1u00k+1. The effect of that choice is that the diagonalj entries in R will be of the form −eiθ rj,j = ei(θ +π)rj,j. Of course, we can make these entries nonegative by applying
 备注：对于数值稳定性，最好使用wk+1=rk+1，k+1ek+1+e−iθk+1U00k+1，而不是wk+1=rk+1，k+1ek+1−e−jiθk+1U00k+1。这种选择的效果是，r中的对角线j项的形式为−eiθrj，j=ei（θ+π）rj，j。当然，我们可以通过应用

hn+1 = ρen,π−θn ◦ ··· ◦ ρe1,π−θ1
 hn+1=ρen，π−θn···ρe1，π−θ1

after hn.
 在hn之后。

As in the Euclidean case, Proposition 27.7 immediately implies the QR-decomposition for arbitrary complex n×n-matrices, where Q is now unitary (see Kincaid and Cheney [100], Golub and Van Loan [80], Trefethen and Bau [171], or Ciarlet [41]).
 在欧几里得案例中，命题27.7立即暗示了任意复杂n×n矩阵的qr分解，其中q现在是一元的（见Kincaid和Cheney[100]、Golub和van Loan[80]、Trefethen和Bau[171]或Ciarlet[41]）。

Proposition 27.8. For every complex n × n-matrix A, there is a sequence H1,...,Hn−1 of matrices, where each Hi is either a Householder matrix or the identity, and an upper triangular matrix R, such that
 提案27.8.对于每个复杂的n×n矩阵a，有一个矩阵的序列h1，…，hn−1，其中每个hi都是一个户主矩阵或恒等式，以及一个上三角矩阵r，这样

R = Hn−1 ···H2H1A.
 R=hn−1···h2h1a。

As a corollary, there is a pair of matrices Q,R, where Q is unitary and R is upper triangular, such that A = QR (a QR-decomposition of A). Furthermore, R can be chosen so that its diagonal entries are nonnegative. This can be achieved by a diagonal matrix D with entries such that |dii| = 1 for i = 1,...,n, and we have A = QeRe with
 作为推论，有一对矩阵q，r，其中q是一元的，r是上三角的，因此a=qr（a的qr分解）。此外，可以选择r，使其对角线项为非负。这可以通过一个对角矩阵d来实现，其中的条目为d i i=1代表i=1，…，n，我们有a=qere

​                                                    Qe = H1 ···Hn−1D,      Re = D∗R,
 qe=h1···hn−1d，re=d r，

where Re is upper triangular and has nonnegative diagonal entries
 其中，re是上三角形，具有非负对角线条目

Proof. It is essentially identical to the proof of Proposition 12.4, and we leave the details as an exercise. For the last statement, observe that hn ◦ ··· ◦ h1 is also an isometry. 
 证据。这与12.4号提案的证明基本相同，我们将细节留作练习。对于最后一个陈述，观察hn·····h1也是一个等距测量。

As in the Euclidean case, the QR-decomposition has applications to least squares problems. It is also possible to convert any complex matrix to bidiagonal form.
 在欧几里得的例子中，QR分解应用于最小二乘问题。也可以将任何复杂的矩阵转换为双对角形式。

## 27.2         Affine Isometries (Rigid Motions)  27.2仿射等距图（刚性运动）

In this section, we study very briefly the affine isometries of a Hermitian space. Most results holding for Euclidean affine spaces generalize without any problems to Hermitian spaces.
 在这一部分中，我们非常简单地研究了厄米空间的仿射等距线。欧几里得仿射空间的大多数结果都推广到埃尔米特空间，没有任何问题。

The characterization of the set of fixed points of an affine map is unchanged. Similarly, every affine isometry f (of a Hermitian space) can be written uniquely as
 仿射映射不动点集的特征不变。类似地，每一个仿射等距f（厄米空间的）都可以唯一地写为

​                                                    f = t ◦ g,      with   t ◦ g = g ◦ t,
 f=t_g，其中t_g=g_t，

where g is an isometry having a fixed point, and t is a translation by a vector τ such that →−f (τ) = τ, and with some additional nice properties (see Proposition 27.13). A generalization
 其中，g是具有固定点的等距测量，t是矢量τ的平移，使得→−f（τ）=τ，并具有一些额外的优良性质（见命题27.13）。泛化


 

27.2. AFFINE ISOMETRIES (RIGID MOTIONS)
 27.2。仿射等距线（刚性运动）

of the Cartan–Dieudonn´e theorem can easily be shown: every affine isometry in Is(n,C) can be written as the composition of at most 2n − 1 isometries if it has a fixed point, or else as the composition of at most 2n+1 isometries, where all these isometries are affine hyperplane reflections except for possibly one affine Hermitian reflection. We also prove that every rigid motion in SE(n,C) is the composition of at most 2n − 2 flips (for n ≥ 3).
 关于卡坦-迪乌顿定理，可以很容易地证明：IS（n，c）中的每一个仿射等值线，如果有一个固定点，可以写成至多2n-1等距线的组合，或者写成至多2n+1等距线的组合，其中所有这些等距线都是仿射超平面反射，不包括可能有一个仿射厄米特反射。我们还证明了SE（n，c）中的每一个刚性运动都是至多2n−2翻转（n≥3）的组成。

Definition 27.2. Given any two nontrivial Hermitian affine spaces E and F of the same finite dimension n, a function f : E → F is an affine isometry (or rigid map) iff it is an affine map and
 定义27.2.给定任意两个具有相同有限维n的非平凡厄米仿射空间e和f，函数f:e→f是仿射等值线（或刚性映射），如果它是仿射映射，并且

,
 ，

for all a,b ∈ E. When E = F, an affine isometry f : E → E is also called a rigid motion.
 对于所有a，b∈e，当e=f时，仿射等距f:e→e也被称为刚性运动。

Thus, an affine isometry is an affine map that preserves the distance. This is a rather strong requirement, but unlike the Euclidean case, not strong enough to force f to be an affine map.
 因此，仿射等值线是保持距离的仿射图。这是一个相当强烈的要求，但与欧几里得的情况不同，它的强度不足以迫使f成为仿射映射。

The following simple Proposition is left as an exercise.
 下面的简单命题留作练习。

Proposition 27.9. Given any two nontrivial Hermitian affine spaces E and F of the same finite dimension , an affine map f : E → F is an affine isometry iff its associated linear map f : E → F is an isometry. An affine isometry is a bijection.
 提案27.9.给定任意两个具有相同有限维的非平凡厄米仿射空间e和f，仿射映射f:e→f是仿射等值线，而其相关线性映射f:e→f是等值线。仿射等值线是双射。

As in the Euclidean case, given an affine isometry→− f : E → E, if →−f is a rotation, we call f a proper (or direct) affine isometry, and if f is a an improper linear isometry, we call f a an improper (or skew) affine isometry. It is easily shown that the set of affine isometries f : E → E forms a group, and those for which →−f is a rotation is a subgroup. The group of affine isometries, or rigid motions, is a subgroup of the affine group GA(E,C) denoted as Is(E,C) (or Is(n,C) when E = Cn). The subgroup of Is(E,C) consisting of the direct rigid motions is also a subgroup of SA(E,C), and it is denoted as SE(E,C) (or SE(n,C), when E = Cn). The translations are the affine isometries f for which →−f = id, the identity map on →−E. The following Proposition is the counterpart of Proposition 13.14 for isometries between Hermitian vector spaces.
 在欧几里得例子中，给定一个仿射等值线→−f:e→e，如果→−f是一个旋转，我们称之为适当（或直接）仿射等值线，如果f是一个不适当的线性等值线，我们称之为不适当（或歪斜）仿射等值线。可以很容易地看出，仿射等距图f:e→e构成一个群，其中→−f是一个旋转的群是一个子群。仿射等轴测群或刚性运动群是仿射群ga（e，c）的一个子群，表示为is（e，c）（或e=c n时为（n，c）。由直接刚性运动组成的IS（E，C）子群也是SA（E，C）子群，当E=CN时，它表示为SE（E，C）（或SE（N，C）。翻译是仿射等距f，其中→−f=id，在→−e上的标识映射。下面的命题是13.14号命题的对应命题，用于Hermitian向量空间之间的等距。

Proposition 27.10. Given any two nontrivial Hermitian affine spaces E and F of the same finite dimension n, for every function f : E → F, the following properties are equivalent:
 提案27.10。给定任意两个具有相同有限维n的非平凡厄米仿射空间e和f，对于每一个函数f:e→f，下列性质是等价的：

(1) f is an affine map and , for all a,b ∈ E.
 （1）f是仿射映射，对于所有a，b∈e。

, and there is some Ω ∈ E such that
 ，还有一些Ω∈e，这样

,
 ，

for all a,b ∈ E.
 对于所有a，b∈e。

Proof. Obviously, (1) implies (2). The proof that that (2) implies (1) is similar to the proof of Proposition 26.7, but uses Proposition 13.14 instead of Proposition 11.12. The details are left as an exercise.      
 证据。显然，（1）意味着（2）。证明（2）暗示（1）类似于26.7号提案的证明，但使用13.14号提案而不是11.12号提案。细节留作练习。

Inspection of the proof shows immediately that Proposition 26.8 holds for Hermitian spaces. For the sake of completeness, we restate the Proposition in the complex case.
 对证据的检验立即表明26.8号提案适用于赫米特空间。为了完整起见，我们在复杂的情况下重述了这个命题。

Proposition 27.11. Let E be any complex affine space of finite dimension For every affine map f : E → E, let Fix(f) = {a ∈ E | f(a) = a} be the set of fixed points of f. The following properties hold:
 提案27.11.设e为每个仿射映射f:e→e的任意有限维仿射空间，设fix（f）=a∈e f（a）=a为f的不动点集，其性质如下：

*(1)*     If f has some fixed point a, so that Fix(f) =6  ∅, then Fix(f) is an affine subspace of
 如果f有固定点a，那么fix（f）=6∅，那么fix（f）是

E such that
 这样的话

Fix(f) = a + E(1,→−f ) = a + Ker(→−f − id),
 固定（F）=A+E（1，→−F）=A+KER（→−F−ID）

where E(1,→−f ) is the eigenspace of the linear map →−f for the eigenvalue 1.
 其中e（1，→−f）是线性映射的特征空间→−f是特征值1的特征空间。

*(2)*     The affine map f has a unique fixed point iff E(1,→−f ) = Ker(→−f − id) = {0}.
 仿射映射f有一个唯一的固定点iff e（1，→−f）=ker（→−f−id）=0。

Affine orthogonal symmetries are defined just as in the Euclidean case, and Proposition
 仿射正交对称的定义与欧几里得的情形一样，以及命题

26.9 also applies to complex affine spaces.
 26.9也适用于复杂仿射空间。

Proposition 27.12. Given any affine complex space E, if f : E → E and g: E → E are affine orthogonal symmetries about parallel affine subspaces→−→− F1 and F2, then g ◦ f is a translation defined by the vector 2ab, where ab is any vector perpendicular to the common direction →−F of F1 and F2 such that  is the distance between F1 and F2, with a ∈ F1 and b ∈ F2. Conversely, every translation by a vector τ is obtained as the composition of two affine orthogonal symmetries about parallel affine subspaces F1 and F2 whose common direction is orthogonal to→− τ = →−ab, for some a ∈ F1 and some b ∈ F2 such that the distance betwen F1 and.
 提案27.12。给定任意仿射复空间e，如果f:e→e和g:e→e是关于平行仿射子空间→→→−f1和f2的仿射正交对称性，则g f是向量2ab定义的平移，其中ab是垂直于f1和f2的公共方向→−f的任意向量，因此t是f1和f2之间的距离，a∈f1和b∈f2。相反，对于一些a∈f1和一些b∈f2，向量τ的每一个平移都是作为平行仿射子空间f1和f2的两个仿射正交对称的组成，其公共方向与→−τ→−ab正交，从而使得f1和f1之间的距离。

It is easy to check that the proof of Proposition 26.10 also holds in the Hermitian case.
 很容易证实26.10号命题的证明也适用于赫米特案。

Proposition 27.13. Let E be a Hermitian affine space of finite dimension n. For every affine isometry f : E →→−E, there is a unique affine isometry∈ →− − g: E → E and a unique{ ∈ translation t = tτ, with f (τ) = τ (i.e., τ Ker( f id)), such that the set Fix(g) = a
 提案27.13。设e为有限维n的厄米特仿射空间，对于每一个仿射同构f:e→→−e，都有一个唯一的仿射同构∈→−−g:e→e和一个唯一的∈翻译t=tτ，其中f（τ）=τ（即τker（f id）），使得集fix（g）=a

E, | g(a) = a} of fixed points of g is a nonempty affine subspace of E of direction
 E，G（A）=A G的不动点是方向E的非空仿射子空间

→−G = Ker(→−f − id) = E(1,→−f ),
 →−G=KER（→−F−ID）=E（1，→−F），

and such that
 这样的话

​                                                      f = t ◦ g    and    t ◦ g = g ◦ t.
 f=t_g和t_g=g_t。

Furthermore, we have the following additional properties:
 此外，我们还有以下附加属性：

27.2. AFFINE ISOMETRIES (RIGID MOTIONS)
 27.2。仿射等距线（刚性运动）

*(a)*    f = g and τ = 0 iff f has some fixed point, i.e., iff Fix(f) =6  ∅.
 f=g，τ=0，iff f有固定点，即iff fix（f）=6∅。

*(b)*    If f has no fixed points, i.e., Fix(f) = ∅, then dim(Ker(→−f − id)) ≥ 1.
 如果f没有固定点，即fix（f）=∅，则dim（ker（→−f−id））≥1。

The remarks made in the Euclidean case also apply to the Hermitian case. In particular, the fact that E has finite dimension is only used to prove (b).
 欧几里得案例中的评论也适用于赫米特案例。特别是，e有有限维这一事实仅用于证明（b）。

A version of the Cartan–Dieudonn´e also holds for affine isometries, but it may not be possible to get rid of Hermitian reflections entirely.
 卡坦-迪乌登的一个版本也适用于仿射等距线，但可能无法完全消除赫米特反射。

Theorem 27.14. Let E be an affine Hermitian space of dimension n ≥ 1. Every affine isometry in Is(n,C) can be written as the composition of at most 2n − 1 affine isometries if it has a fixed point, or else as the composition of at most 2n + 1 affine isometries, where all these isometries are affine hyperplane reflections except for possibly one affine Hermitian reflection. When n ≥ 2, the identity is the composition of any reflection with itself.
 定理27.14。设e为尺寸n≥1的仿射厄米空间。IS（n，c）中的每一个仿射等值线可以写成至多2n-1个仿射等距线的组成，如果它有一个固定点，或者写成至多2n+1个仿射等距线的组成，其中所有这些等距线都是仿射超平面反射，除了可能有一个仿射厄米提亚参考线。选择。当n≥2时，同一性是任何反射本身的组成。

Proof. The proof is very similar to the proof of Theorem 26.11, except that it uses Theorem 27.5 instead of Theorem 26.1. The details are left as an exercise. 
 证据。证明与定理26.11的证明非常相似，只是它使用了定理27.5而不是定理26.1。细节留作练习。

When n ≥ 3, as in the Euclidean case, we can characterize the affine isometries in SE(n,C) in terms of flips, and we can even bound the number of flips by 2n − 2.
 当n≥3时，如欧几里得案例中，我们可以用翻转来描述SE（n，c）中的仿射等距图，甚至可以用2n-2绑定翻转的数量。

Theorem 27.15. Let E be a Hermitian affine space of dimension n ≥ 3. Every rigid motion f ∈ SE(E,C) is the composition of an even number of affine flips f = f2k ◦ ··· ◦ f1, where k ≤ n − 1.
 定理27.15。设e为尺寸n≥3的厄米特仿射空间。每一个刚性运动f∈se（e，c）是偶数个仿射翻转f=f2k····f1的组成，其中k≤n−1。

Proof. It is very similar to the proof of theorem 26.12, but it uses Proposition 27.6 instead of Proposition 26.5. The details are left as an exercise. 
 证据。它与定理26.12的证明非常相似，但它使用了命题27.6而不是命题26.5。细节留作练习。

A more detailed study of the rigid motions of Hermitian spaces of dimension 2 and 3 would seem worthwhile, but we are not aware of any reference on this subject.
 对2维和3维厄米特空间的刚性运动进行更详细的研究似乎是值得的，但我们不知道这方面的任何参考。


 