《高等数学A》第十二次习题课

> Author ZhenLiu
>
> 2022/11/22



#### 12.1 函数凹凸性

- 定义：凸性定义
  如果对于区间 $I$ 中任意两点 $x_1, x_2$ 和任何 $t \in(0,1)$, 都有

$$
f\left((1-t) x_1+t x_2\right) \geq(\leq)(1-t) f\left(x_1\right)+t f\left(x_2\right),
$$

则 $f(x)$ 是 $I$ 上的上(下) 凸函数. 如果上式中的不等号为 $>(<)$, 则称 $f(x)$ 为严格上(下) 凸函 数.

- 性质：
  - 性质1：如果 $f(x)$ 是某区间 $(a, b)$ 上的下凸函数, 则 $f(x)$ 在 $(a, b)$ 内连续, 且处处存在左、右导数.
  - 性质 2：如果 $f(x)$ 是某区间 $(a, b)$ 上的下凸函数, 则
    (i) 对任意的 $x \in(a, b)$ 均有 $f_{-}^{\prime}(x) \leq f_{+}^{\prime}(x)$;
    (ii) 对满足 $a<x_1<x_2<b$ 的任意 $x_1, x_2$, 均有 $f_{+}^{\prime}\left(x_1\right) \leq f_{-}^{\prime}\left(x_2\right)$.
- 判定1：设 $f(x)$ 在 $[a, b]$ 上连续, 在 $(a, b)$ 内可导, 则下列命题等价:
  (i) $f(x)$ 是 $[a, b]$ 上的下凸函数;
  (ii) $f^{\prime}(x)$ 在 $(a, b)$ 中递增;
  (iii) 对任何 $x_0 \in(a, b)$, 曲线 $y=f(x)$ 在点 $\left(x_0, f\left(x_0\right)\right)$ 的切线位于曲线的下方, 即

$$
f(x) \geq f\left(x_0\right)+f^{\prime}\left(x_0\right)\left(x-x_0\right), \quad \forall x \in[a, b] .
$$

- 判定2：设 $f(x)$ 在 $[a, b]$ 上连续, 在 $(a, b)$ 内两次可导. 则 $f(x)$ 在 $[a, b]$ 上为下凸函数的充分必要条件是: 对一切 $x \in(a, b)$, 都有 $f^{\prime \prime}(x) \geq 0$.

- 若 $f(x)$ 在 $I$ 上有定义, 则以下三条件等价:
  i) $f(x)$ 在 $I$ 上为凸函数;
  ii) $\forall q_1 \geqslant 0: q_1+q_2+\cdots+q_n=1, \forall x_1, x_2, \cdots, x_n \in I$, 有 $f\left(q_1 x_1+q_2 x_2+\cdots+q_n x_n\right) \leqslant q_1 f\left(x_1\right)+q_2 f\left(x_2\right)+\cdots+q_n f\left(x_n\right)$;
  iii) $\forall p_i \geqslant 0(i=1,2, \cdots, n)$ 不全为零, $\forall x_1, x_2, \cdots, x_n \in I$ 有 $f\left(\frac{p_1 x_1+p_2 x_2+\cdots+p_n x_n}{p_1+p_2+\cdots+p_n}\right) \leqslant \frac{p_1 f\left(x_1\right)+p_2 f\left(x_2\right)+\cdots+p_n f\left(x_n\right)}{p_1+p_2+\cdots+p_n}$.

- 【例题：利用凸函数证明不等式】已知 $a>0, b>0, a^3+b^3 \leqslant 2$. 求证: $a+b \leqslant 2$. 

  证 因为 $y=x^3$ 是凹函数, 所以曲线在弦下方. 有
  $$
  \left(\frac{a+b}{2}\right)^3<\frac{a^3+b^3}{2} \leqslant 1 \Longrightarrow(a+b)^3 \leqslant 8 \Longrightarrow a+b \leqslant 2
  $$

- 【例题：利用凸函数证明不等式】若 $a, b>0, p, q>0$, 使得 $\frac{1}{p}+\frac{1}{q}=1$. 求证:
  $$
  a b \leqslant \frac{a^p}{p}+\frac{b^q}{q}
  $$
  分析：将要证的不等式两边取对数, 并用对数性质改写成
  $$
  \frac{1}{p} \ln a^p+\frac{1}{q} \ln b^q \leqslant \ln \left(\frac{1}{p} a^p+\frac{1}{q} b^q\right) .
  $$
  证 因为 $y=\ln x$ 在 $(0, \infty)$ 上是凸函数. 故弦在曲线下方，即有
  $$
  \begin{array}{r}
  \ln a b \quad \ln \left(\frac{1}{p} a^p+\frac{1}{q} b^q\right) \\
  \| \\
  \ln a+\ln b=\frac{1}{p} \ln a^p+\frac{1}{q} \ln b^q
  \end{array}
  $$
  从此 $U$ 形等式知不等式串的两端成立, 又因为 $y=\ln x$ 在 $(0,+\infty)$ 上严格单调增加的, 故去掉对数即得
  $$
  a b \leqslant \frac{1}{p} a^p+\frac{1}{q} b^q
  $$

- 【例题：利用凸函数证明不等式】设 $f(x)$ 在 $(0,+\infty)$ 上是凹函数, 且 $\lim _{x \rightarrow 0+0} f(x)=0$. 求 证: $\frac{f(x)}{x}$ 在 $(0,+\infty)$ 上单调增加.
  分析：在 $(0,+\infty)$ 上任意指定 $x_1, x_2$, 不妨设 $x_1<x_2$. 要证$\frac{f\left(x_1\right)}{x_1} \leqslant \frac{f\left(x_2\right)}{x_2}$, 即要证 $f\left(x_1\right) \leqslant \frac{x_1}{x_2} f\left(x_2\right)$.
  证 为了用上条件 $\lim _{x \rightarrow 0+0} f(x)=0$, 引进一个动点 $x \in\left(0, x_1\right)$​, 并记 $\lambda=\frac{x_1-x}{x_2-x}$ (图 2.23), 则 $\frac{x_2-x_1}{x_2-x}=1-\lambda$. 因为 $f(x)$ 在 $(0,+\infty)$ 上 是凹函数, 所以
  $$
  f\left(x_1\right) \leqslant \lambda f\left(x_2\right)+(1-\lambda) f(x) .
  $$
  进一步，因为
  $$
  \lim _{x \rightarrow 0+0} \lambda=\frac{x_1}{x_2}, \quad \lim _{x \rightarrow 0+0} f(x)=0,
  $$
  所以由 $(1) \Longrightarrow f\left(x_1\right) \leqslant \frac{x_1}{x_2} f\left(x_2\right)$. 证毕.

- 【例题：关于凸函数等价性的应用】在锐角 $\triangle A B C$ 中, 求证: $\sin A+\sin B+\sin C>2$. 

  证 令 $f(x)=\sin x$, 则 $f^{\prime \prime}(x)=-\sin x<0, \forall x \in(0, \pi / 2)$. 由此可见, $f(x)$ 在 $(0, \pi / 2)$ 上是凸函数, 故弦 $y=2 x / \pi$ 在戭 方 (图 2.28), 即有 $\sin x>\frac{2 x}{\pi}, \forall x \in\left(0, \frac{\pi}{2}\right)$. 因此有
  $$
  \sin A>\frac{2 A}{\pi}, \quad \sin B>\frac{2 B}{\pi}, \quad \sin C>\frac{2 C}{\pi} .
  $$
  把以上三个不等式相加, 并注意到 $A+B+C=\pi$, 有
  $$
  \begin{array}{cc}
  \sin A+\sin B+\sin C & 2 \\
  \vee & \|
  \end{array}
  $$
  从此 $U$ 形等式-不等式串的两端即知
  $$
  \sin A+\sin B+\sin C>2
  $$

- 【例题：关于凸函数等价性的应用】$\text { 在 } \triangle A B C \text { 中, 求证: } \sin A+\sin B+\sin C \leqslant \frac{3 \sqrt{3}}{2} \text {. }$

  证 因为 $y=\sin x$ 是凸函数, 取$3/\pi$处的切线，因为曲线在切线下方, 即有
  同理,
  $$
  \sin A \leqslant \frac{\sqrt{3}}{2}+\frac{1}{2}\left(A-\frac{\pi}{3}\right) .
  $$
  $$
  \begin{aligned}
  &\sin B \leqslant \frac{\sqrt{3}}{2}+\frac{1}{2}\left(B-\frac{\pi}{3}\right) \\
  &\sin C \leqslant \frac{\sqrt{3}}{2}+\frac{1}{2}\left(C-\frac{\pi}{3}\right)
  \end{aligned}
  $$
  $$
  \sin A+\sin B+\sin C \leqslant \frac{3 \sqrt{3}}{2}
  $$

  【拓展】对 $\forall \alpha, \beta, \gamma \in(a, b)$, 恒有
  $$
  \frac{f(\beta)-f(\alpha)}{\beta-\alpha} \leqslant \frac{f(\gamma)-f(\alpha)}{\gamma-\alpha} \leqslant \frac{f(\gamma)-f(\beta)}{\gamma-\beta} .
  $$
  上式的意义为: 如示意图 $2.15$ 所示, 在曲线 $y=f(x)$ 上自左至右任取三 点 $P, Q, R$, 则两两相连所得线段的斜率满足:
  $$
  K_{P Q} \leqslant K_{P R} \leqslant K_{Q R} .
  $$
  姑且称此为判定下凸函数的三斜准则.（由此得到的两个推论！）

- 【例题：三斜线准则的应用】设 $f(x)$ 是开区间 $(A, B)$ 上的下凸函数, 求证: 对任何 $[\alpha, \beta] \subset(A, B), f(x)$ 在 $[\alpha, \beta]$ 上满足 Lipschitz 条件.
  证明 对 $[\alpha, \beta] \subset(A, B)$, 选 $a, b, c, d \in(A, B)$, 使得
  $$
  a<b<\alpha<\beta<c<d \text {. }
  $$
  任取 $x_1, x_2 \in[\alpha, \beta]$, 且 $x_1<x_2$. 由下凸函数的充分必要条件 $($ 三斜准 则), 有
  $$
  \frac{f(b)-f(a)}{b-a} \leqslant \frac{f\left(x_2\right)-f\left(x_1\right)}{x_2-x_1} \leqslant \frac{f(d)-f(c)}{d-c} .
  $$
  令 $M=\max \left\{\left|\frac{f(b)-f(a)}{b-a}\right|,\left|\frac{f(d)-f(c)}{d-c}\right|\right\}$, 则有
  $$
  \left|\frac{f\left(x_2\right)-f\left(x_1\right)}{x_2-x_1}\right| \leqslant M, \quad \forall x_1, x_2 \in[\alpha, \beta] .
  $$
  因为 $M$ 与 $x_1, x_2$ 无关, 所以 $f(x)$ 在 $[\alpha, \beta]$ 上满足 Lipschitz 条件: $\exists M>$ 0, 使得
  $$
  \left|f\left(x_2\right)-f\left(x_1\right)\right| \leqslant M\left|x_2-x_1\right|, \quad \forall x_1, x_2 \in[\alpha, \beta] .
  $$
  评注：从本例还可得出: 开区间 $(A, B)$ 上的下凸函数必在 $(A, B)$ 的任一闭区间上连续, 因而该函数是 $(A, B)$ 内的连续函数.

- 【例题：有界性+凸函数】设函数 $f(x)$ 在区间 $(a, b)$ 上为下凸函数, 且有界. 求怔: 极限 $\lim _{x \rightarrow a^{+}} f(x)$ 和 $\lim _{x \rightarrow b^{-}} f(x)$ 均存在.

  证明 设 $x \in(a, b)$, 由有界性假设知 $\exists M>0$, 有
  $$
  f(x) \leqslant M, \quad x \in(a, b) .
  $$
  又 $f(x)$ 在区间 $(a, b)$ 上为下凸函数, 所以斜率 $\frac{f(x)-f\left(x_0\right)}{x-x_0}$ 是严格 递增的, 且对 $\forall x_1 \in\left(x_0, x\right)$, 有
  $$
  \frac{f(x)-f\left(x_0\right)}{x-x_0} \leqslant \frac{M-f\left(x_0\right)}{x_1-x_0}
  $$
  由单调有界定理知 $\lim _{x \rightarrow b^{-}} \frac{f(x)-f\left(x_0\right)}{x-x_0}$ 存在, 设为 $A$, 则
  $$
  \lim _{x \rightarrow b^{-}} f(x)=\lim _{x \rightarrow b^{-}}\left[\left(x-x_0\right) \frac{f(x)-f\left(x_0\right)}{x-x_0}+f\left(x_0\right)\right]=A\left(b-x_0\right)+f\left(x_0\right) .
  $$
  同理, 因为 $f(x)$ 在区间 $(a, b)$ 上为下凸函数, 所以斜率 $\frac{f\left(x_0\right)-f(x)}{x_0-x}$ 是严格递减的, 且对 $\forall x_1<x<x_0$, 有
  $$
  \frac{f\left(x_0\right)-f(x)}{x_0-x} \geqslant \frac{f\left(x_0\right)-M}{x_0-x_1} .
  $$
  由单调有界定理知 $\lim _{x \rightarrow a^{+}} f(x)$ 存在, 设为 $B$, 则
  $$
  \lim _{x \rightarrow a^{+}} f(x)=\lim _{x \rightarrow a^{+}}\left[f\left(x_0\right)-\frac{f\left(x_0\right)-f(x)}{x_0-x}\left(x_0-x\right)\right]=f\left(x_0\right)+B\left(a-x_0\right) .
  $$

- 【例题：有界性+凸函数】设 $f(x)$ 在 $(-\infty,+\infty)$ 上是有上界的凹函数. 求证: $f(x)$ 在 $(-\infty,+\infty)$ 上是常数.
  证 用反证法. 假设要证的结论不成立, 那么 $\exists x_1<x_2$, 使得 $f\left(x_1\right) \neq f\left(x_2\right)$. 设 $f(x) \leqslant M, x \in(-\infty,+\infty)$.
  下面分两种情况考虑.
  第一种情况是 $f\left(x_1\right)<f\left(x_2\right)$, 这时 $A \stackrel{\text { def }}{=} f\left(x_2\right)-f\left(x_1\right)>0$. 任选 取 $x>x_2$, 如图 $2.35$ 所示, 因为 $f(x)$ 是凹函数, 所以连接 $\left(x_1, f\left(x_1\right)\right)$, $(x, f(x))$ 的弦在曲线上方, 即有
  $$
  f\left(x_2\right) \leqslant f\left(x_1\right)+\frac{f(x)-f\left(x_1\right)}{x-x_1}\left(x_2-x_1\right),
  $$
  两边同乘以 $x-x_1>0$, 并用 $f(x) \leqslant M, A=f\left(x_2\right)-f\left(x_1\right)>0$, 即得
  $$
  A\left(x-x_1\right) \leqslant\left(M-f\left(x_1\right)\right)\left(x_2-x_1\right),
  $$
  上式两边令 $x \rightarrow+\infty$, 即得 $+\infty \leqslant\left(M-f\left(x_1\right)\right)\left(x_2-x_1\right)$, 矛盾.



#### 12.2 函数性质作图

- 函数作图并不要求我们像计算机一样把函数图像的任何信息都做出来, 重要的是我 们把函数的主要信息表现出来。主要信息可以根据与 $f, f^{\prime}, f^{\prime \prime}$ 的相关性分为四类:
  - 零阶信息 指函数的定义域、连续性、间断点、零点、函数值的符号。
  - 一阶信息 指函数的单调性、极值点、稳定点。
  - 二阶信息 指函数的凹凸性、拐点。
  - 渐进信息 通过渐进线画出函数的大致位置。
- 若曲线 $C$ 上的动点 $M$ 沿曲线无限地远离原点时, 点 $M$ 与某固定直线 $L$ 的距离趋向于零, 则 称 $L$ 是曲线 $C$ 的渐近线.
  (i) 水平渐近线
  若 $\lim _{x \rightarrow+\infty} f(x)=C$, 或 $\lim _{x \rightarrow-\infty} f(x)=C$, 则曲线 $y=f(x)$ 有水平渐近线 $y=C$.
  (ii) 垂直渐近线
  若 $\lim _{x \rightarrow C^{+}} f(x)=\infty$, 或 $\lim _{x \rightarrow C^{-}} f(x)=\infty$, 则曲线 $y=f(x)$ 有垂直渐近线 $x=C$.
  (iii) 斜渐近线
  若 $\lim _{x \rightarrow+\infty} \frac{f(x)}{x}=a \neq 0, \lim _{x \rightarrow+\infty}(f(x)-a x)=b$, 则曲线当 $x \rightarrow+\infty$ 时有渐近线 $y=$ $a x+b$. 类似地可判断曲线当 $x \rightarrow-\infty$ 时是否有渐近线及渐近线方程.
- 求曲线 $y=1-x+\sqrt{\frac{x^3}{3+x}}$ 的渐近线.
  解: 函数的定义域是 $(-\infty,-3) \cup[0,+\infty)$.

1) 垂直渐近线
   由于$\lim _{x \rightarrow-3^{-}} f(x)=+\infty$,所以 $x=-3$ 是垂直渐近线.
2) 水平渐近线
   由于

$$
\begin{aligned}
\lim _{x \rightarrow+\infty} f(x) &=1+\lim _{x \rightarrow+\infty} \frac{x \sqrt{x}-x \sqrt{3+x}}{\sqrt{3+x}} \\
&=1-\lim _{x \rightarrow+\infty} \frac{3 x}{\sqrt{3+x}(\sqrt{x}+\sqrt{3+x})} \\
&=-\frac{1}{2},
\end{aligned}
$$

所以 $y=-\frac{1}{2}$ 是水平渐近线.

3) 斜渐近线
   由于

$$
\begin{aligned}
\lim _{x \rightarrow-\infty} \frac{f(x)}{x}=\lim _{x \rightarrow-\infty}\left(\frac{1}{x}-1-\sqrt{\frac{x}{3+x}}\right)=-2 \\
\lim _{x \rightarrow-\infty}(f(x)+2 x) &=1+\lim _{x \rightarrow-\infty}\left(x+\sqrt{\frac{x^3}{3+x}}\right) \\
&=1+\lim _{x \rightarrow-\infty} x\left(1-\sqrt{\frac{x}{3+x}}\right) \\
&=\frac{5}{2}
\end{aligned}
$$

所以 $y=-2 x+\frac{5}{2}$ 是斜渐近线.





#### 12.3 向量解析几何

- 本小节的部分题目取自北京大学教材《解析几何》尤承业；

- 【拓展：分解定理】不共线向量// 不共面向量  分解的唯一性

- 【例题：三向量共面】向量 $\alpha, \beta, \gamma$ 共面的充分必要条件是, 存在不全为 0 的实数 $\lambda, \mu, \nu$, 使得$\lambda \alpha+\mu \beta+\nu \gamma=0$
  证明 充分性：用反证法. 假如 $\alpha, \vec{\beta}, \gamma$ 不共面, 则根据分解定理，0向量对他们有唯一的分解即可。

  必要性：如果 $\alpha=0$,则
  $$
  1 \alpha+0 \beta+0 \gamma=0 \text {. }
  $$
  如果 $\alpha \neq 0$, 但是 $\boldsymbol{\alpha} / / \boldsymbol{\beta}$, 则存在 $\lambda$, 使得 $\beta=\lambda \alpha$. 则
  $$
  \lambda \alpha-\beta+ 0 \gamma =0 .
  $$
  如果 $\alpha, \beta$ 不平行, 由分解定理知道, $\gamma$ 对 $\alpha, \beta$ 可分解,
  $$
  \begin{gathered}
  \boldsymbol{\gamma}=\lambda \alpha+\mu \beta, \\
  \lambda \alpha+\mu \beta+(-1) \boldsymbol{\gamma}=0 .
  \end{gathered}
  $$

- 【例题：三点共面】设 $\left[O ; e_1, e_2\right]$ 是平面 $\pi$ 上的一个平面仿射坐标系, 上的三点 $A, B, C$ 的坐标分别为 $\left(a_1, a_2\right),\left(b_1, b_2\right),\left(c_1, c_2\right)$, 则
  $$
  A, B, C \text { 共线 } \Leftrightarrow\left|\begin{array}{lll}
  a_1 & a_2 & 1 \\
  b_1 & b_2 & 1 \\
  c_1 & c_2 & 1
  \end{array}\right|=0 .
  $$
  证明：根据行列式的性质,
  $$
  \begin{aligned}
  \left|\begin{array}{lll}
  a_1 & a_2 & 1 \\
  b_1 & b_2 & 1 \\
  c_1 & c_2 & 1
  \end{array}\right| &=0\\
  & \Leftrightarrow\left|\begin{array}{ll}
  a_1-c_1 & a_2-c_2 \\
  b_1-c_1 & b_2-c_2
  \end{array}\right|=0 \\
  & \Leftrightarrow \overrightarrow{C A} / / \overrightarrow{C B} \\
  & \Leftrightarrow A, B, C \text { 共线. }
  \end{aligned}
  $$

- 【例题：双重混合积】对任意向量 $\alpha, \beta, \gamma$, 有等式
   $(\alpha \times \beta) \times \boldsymbol{\gamma}=(\boldsymbol{\alpha} \cdot \boldsymbol{\gamma}) \beta-(\beta \cdot \gamma) \alpha$;

  $\alpha \times(\beta \times \gamma)=(\alpha \cdot \gamma) \beta-(\alpha \cdot \beta) \gamma$

- 【例题：lagrange恒等式】对任意四个向量 $\alpha, \beta, \gamma, \delta$, 证明：
  $$
  \alpha \times \beta \cdot \gamma \times \delta=\left|\begin{array}{ll}
  \alpha \cdot \gamma & \alpha \cdot \delta \\
  \beta \cdot \gamma & \beta \cdot \delta
  \end{array}\right| \text {. }
  $$
  证明 $\alpha \times \beta \cdot \gamma \times \delta=(\alpha \times \beta, \gamma, \delta)=(\alpha \times \beta) \times \gamma \cdot \delta$
  $$
  \begin{aligned}
  &=[(\alpha \cdot \gamma) \beta-(\beta \cdot \gamma) \alpha] \cdot \delta \\
  &=(\alpha \cdot \gamma)(\beta \cdot \delta)-(\beta \cdot \gamma)(\alpha \cdot \delta) \\
  &=\left|\begin{array}{ll}
  \alpha \cdot \gamma & \alpha \cdot \delta \\
  \beta \cdot \gamma & \beta \cdot \delta
  \end{array}\right| .
  \end{aligned}
  $$

- 【例题：参考坐标系】如果 $\alpha, \beta, \gamma$ 不共面,则 $\beta \times \boldsymbol{\beta}, \boldsymbol{\gamma} \times \boldsymbol{\alpha}, \boldsymbol{\alpha} \times \beta$ 也不共面！
  证明 $(\beta \times \gamma, \gamma \times \alpha, \alpha \times \beta)=(\beta \times \gamma) \times(\gamma \times \alpha) \cdot \alpha \times \beta$

- 【拓展】线性方程组的求解和Grammer法则；

- 【定理】直线 $l$
  $\left\{\begin{array}{l}A_1 x+B_1 y+C_1 z+D_1=0 \\ A_2 x+B_2 y+C_2 z+D_2=0\end{array}\right.$
  在平面 $\pi$ 上的充分必要条件为: 存在不全为 0 的实数 $\lambda, \mu$, 使得 $\lambda\left(A_1 x+B_1 y+C_1 z+\dot{D}_1\right)+\mu\left(A_2 x+B_2 y+C_2 z+D_2\right)=0$ 是 $\pi$ 的一般方程.
  证明：充分性上面已经证明,下面证明必要性.
  $>$ 假设 $\pi$ 经过直线 $l$. 取在 $\pi$ 上, 但不在 $l$ 上的一点 $M_0\left(x_0, y_0\right.$,
  $\left.z_0\right)$. 设
  $$
  \begin{array}{r}
  \frac{\mu_0}{2} \\
  =A_1 x_0+B_1 y_0+C_1 z_0+D_1 \\
  =A_2 x_0+B_2 y_0+C_2 z_0+D_2,
  \end{array}
  $$
  则 $\lambda_0, \mu_0$ 不全为零(否则 $M_0$在 $l$ 上). 于是平面 $\lambda_0$ $\lambda_0\left(A_1 x+B_1 y+C_1 z+D_1\right) \quad \mu_0\left(A_2 x+B_2 y+C_2 z+D_2\right)=0$

- 【例题】求过三个已知点 $P_1(2,3,0), P_2(-2,-3,4)$ 和 $P_3(0,6,0)$ 所 确定的平面方程.
  解法 1 (平面束方法) 过 $P_1(2,3,0), P_2(-2,-3,4)$ 两点的直线 方程为
  $$
  \frac{x-2}{-4}=\frac{y-3}{-6}=\frac{z}{4},
  $$
  过这条直线的平面束方程为
  $$
  \left(\frac{x-2}{4}-\frac{y-3}{6}\right)+\lambda\left(\frac{y-3}{-6}-\frac{z}{4}\right)=0
  $$
  依题意, 所求平面还过 $P_3(0,6,0)$, 将此代入上述平面束方程, 得到
  $\left(\frac{0-2}{4}-\frac{6-3}{6}\right)+\lambda\left(\frac{6-3}{-6}-\frac{0}{4}\right)=0$.由此解得 $\lambda=-2$, 再将此代入上述平面束方程, 得到
  $$
  3 x+2 y+6 z-12=0,
  $$
  这就是所求的平面方程.
  解法 2 (待定系数法) 设所求的平面方程为 $A x+B y+C z+D=0$. 根据其过 $P_k(k=1,2,3)$ 点, 有
  $$
  \left\{\begin{array}{l}
  2 A+3 B+D=0 \\
  -2 A-3 B+4 C+D=0 \\
  6 B+D=0
  \end{array}\right.
  $$
  否则 $A=B=C=D=0$, 不合题意. 所求的平面方程为 $-\frac{1}{4} x-\frac{1}{6} y-\frac{1}{2} z+1=0$, 即 $3 x+2 y+6 z-12=0$.



#### 12.4 空间曲线的切线与弧长

- 本小节的部分题目取自北京大学教材《微分几何初步》陈维桓；
- 【拓展】空间曲线求弧长的公式与参数变换是无关的；
- 【例题】设 $\boldsymbol{a}(t)$ 是一个非零连续可微函数, 则
  (i) 函数 $\boldsymbol{a}(t)$ 的长度是常数, 当且仅当 $\boldsymbol{a}^{\prime}(t) \cdot \boldsymbol{a}(t) \equiv 0$;
  (ii) 函数 $\boldsymbol{a}(t)$ 的方向不变, 当且仅当 $\boldsymbol{a}^{\prime}(t) \times \boldsymbol{a}(t) \equiv 0$;
  (iii) 函数 $\boldsymbol{a}(t)$ 与一个确定的方向垂直, 当且仅当 $\left(\boldsymbol{a}(t), \boldsymbol{a}^{\prime}(t), \boldsymbol{a}^{\prime \prime}(t)\right) \equiv 0$

证明 (i) 因为 $\frac{\mathrm{d}}{\mathrm{d} t}|\boldsymbol{a}(t)|^2=2 \boldsymbol{a}^{\prime}(t) \cdot \boldsymbol{a}(t)$, 所以 $|\boldsymbol{a}(t)|^2=$常数当且仅当结论成立；
(ii) 若 $\boldsymbol{a}(t)$ 的方向不变, 则有单位常向量 $\boldsymbol{b}$, 使得 $\boldsymbol{a}(t)$ 为$\boldsymbol{a}(t)=f(t) \cdot \boldsymbol{b},$其中 $f(t)$ 是连续可微函数. 因此
$$
\begin{aligned}
&\boldsymbol{a}^{\prime}(t)=f^{\prime}(t) \cdot \boldsymbol{b}, \\
&\boldsymbol{a}^{\prime}(t) \times \boldsymbol{a}(t)=0 .
\end{aligned}
$$
反之, 设 $\boldsymbol{a}^{\prime}(t) \times \boldsymbol{a}(t)=0$, 命 $\boldsymbol{b}(t)=\boldsymbol{a}(t)/| \boldsymbol{a}(t) \mid$, 则 $|\boldsymbol{b}(t)|=1$由 (i) 可知 $\boldsymbol{b}^{\prime}(t) \cdot \boldsymbol{b}(t)=0$, 即 $\boldsymbol{b}^{\prime}(t) \cdot \boldsymbol{a}(t)=0$. 由定义可知 $\boldsymbol{a}(t)=f(t) \cdot b$，其中 $f(t)=|\boldsymbol{a}(t)|$, 则
 $\boldsymbol{a}^{\prime}(t)=f^{\prime}(t) \cdot \boldsymbol{b}(t)+f(t) \cdot \boldsymbol{b}^{\prime}(t)$,
$\boldsymbol{a}^{\prime}(t) \times \boldsymbol{a}(t)=f(t) \cdot \boldsymbol{b}^{\prime}(t) \times \boldsymbol{a}(t)=0$
因此 $\boldsymbol{b}^{\prime}(t) \| \boldsymbol{a}(t)$. 由于 $\boldsymbol{b}^{\prime}(t) \cdot \boldsymbol{a}(t)=0$, 故 $\boldsymbol{b}^{\prime}(t)=0$, 即 $\boldsymbol{b}(t)$ 是常向量, 即向量函数 $\boldsymbol{a}(t)$ 的方向不变.

- 【例题】平面曲线
  $$
  \boldsymbol{r}(t)=\left(t^3, t^2\right) .
  $$
  这是一条可微曲线, 但是 $r^{\prime}(0)=(0,0)$, 所以它不是正则曲线. 从图形上看,该曲线在 $t=0$ 处有一个尖点 由此可见, 可微的参数曲线与直观上光滑的曲线 (即切线连续变化的曲线) 是不一致的. 在尖点尽管有唯一确定的切线, 但是把切线看成有向直线时, 在通过尖点时,'切线要转动 $180^{\circ}$. 我们还很容易构造出 (可微参数曲线的例子 (比如锯齿状曲线), 它在非正则点没有确定的切线.) 对于正则曲线不会出现这种情形, 也就是正则参数曲线 和直观上光滑的曲线是很好的吻合的.

  
