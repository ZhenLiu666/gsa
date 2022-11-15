《高等数学A》第十一次习题课

> Author ZhenLiu
>
> 2022/11/15



#### 11.1 函数极值

- 极值的几个性质：

  -  一阶必要条件：又称 Fermat定理 设 $f(x)$ 在 $(a, b)$ 可导, 如果 $x_0$ 是 $f$ 一个极值 点, 那么 $f^{\prime}\left(x_0\right)=0$ 
  - 二阶必要条件 设 $f(x)$ 在 $(a, b)$ 二阶可导, 如果 $x_0$ 是 $f$ 一个极大(小)值点, 那 么 $f^{\prime}\left(x_0\right)=0$, 并且 $f^{\prime \prime}\left(x_0\right) \leq(\geq) 0$ 。
  - 二阶充分条件：设 $f(x)$ 在 $(a, b)$ 二阶可导, 如果 $f^{\prime}\left(x_0\right)=0$, 并且 $f^{\prime \prime}\left(x_0\right)<(>$ ) 0 , 那么 $x_0$ 是 $f$ 个极大(小) 值点。

- 【例题】设 $f(x)$ 二阶连续可微, 且满足 $x f^{\prime \prime}(x)+3 x\left[f^{\prime}(x)\right]^2=1-\mathrm{e}^{-x}, x \in(-\infty,+\infty)$, 若 $x_0$ 是 $f(x)$ 的 极值点, 证明 $f\left(x_0\right)$ 是极小值.
  证明:当 $x_0 \neq 0$ 时, 由 $x_0 f^{\prime \prime}\left(x_0\right)+3 x_0\left[f^{\prime}\left(x_0\right)\right]^2=1-\mathrm{e}^{-x_0}$, 知 $f^{\prime \prime}\left(x_0\right)=\frac{1-\mathrm{e}^{-x_0}}{x_0}>0$, 故 $f\left(x_0\right)$ 是 极小值.当 $x_0=0$ 时, 取 $x \neq 0$, 有 $f^{\prime \prime}(x)=\frac{1-\mathrm{e}^{-x}}{x}-3\left[f^{\prime}(x)\right]^2$. 由L'H法则, 知 $\lim _{x \rightarrow 0} f^{\prime \prime}(x)=1$, 即 知 $f^{\prime \prime}(0)=1>0$, 因此 $f\left(x_0\right)$ 是极小值.

- 【例题】不可导的极 (最) 值点 (2020) 求出闭区间 $[-1,1]$ 上的一元函数 $f(x)=x^{2 / 3}-\left(x^2-1\right)^{1 / 3}$ 达 到最小值的所有点.
  解. 最值点要在极值点和端点中寻找, 极值点又要在稳定点和不可导点中寻找.
  首先, $f(x)$ 是连续函数, 因此在 $[-1,1]$ 上必可取到最小值.
  其次, $f(x)$ 在 $(-1,0)$ 和 $(0,1)$ 内是可导的. 当 $x \neq 0, \pm 1$ 时, 有$f^{\prime}(x)=\frac{2}{3 \sqrt[3]{x}}-\frac{2 x}{3 \sqrt[3]{\left(x^2-1\right)^2}} .$我们寻找稳定点, 让上式等于 0 , 即得$x^4=\left(x^2-1\right)^2,$从而 $x=\pm \frac{\sqrt{2}}{2}$.所以, 最小值点要在 $\left\{-1,1,0,-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right\}$ 中寻找. 容易计算
  $$
  \begin{aligned}
  f(-1) &=f(1)=f(0)=1, \\
  f\left(\frac{\sqrt{2}}{2}\right) &=f\left(-\frac{\sqrt{2}}{2}\right)=\sqrt[3]{4}>1,
  \end{aligned}
  $$
  因此最小值点为 0 和 $\pm 1$.注: 0 为不可导的极小值点.

- 【例题】隐函数的极值：设二阶可导的隐函数 $y(x)$ 由 $x^3+y^3-3 x y=3$ 确定. 试求 $y(x)$ 的极值并判断型.
  解. 我们首先求隐函数的导数. 上式两端同时对 $x$ 求导可得$3 x^2+3 y^2 y^{\prime}-3 x y^{\prime}-3 y=0,$

解得$y^{\prime}=\frac{x^2-y}{x-y^2} .$再求导可得
$$
y^{\prime \prime}=\frac{\left(2 x-y^{\prime}\right)\left(x-y^2\right)-\left(x^2-y\right)\left(1-2 y y^{\prime}\right)}{\left(x-y^2\right)^2}
$$
令 $y^{\prime}=0$, 可得 $y=x^2$. 代入条件可得$x^3+x^6-3 x^3=3,$解得 $x=-1$ 或 $x=\sqrt[3]{3}$.
利用 $y=x^2$ 和 $y^{\prime}=0$ 化简可得对于这两个点有
$$
y^{\prime \prime}=\frac{2 x}{x-y^2}=\frac{2}{1-x^3},
$$
分别有 $y^{\prime \prime}=1$ 和 $y^{\prime \prime}=-1$. 因此当 $x=-1$ 时取到极小值 1 , 当 $x=\sqrt[3]{3}$ 时取到极大值 $\sqrt[3]{9}$.

- 【例题】





#### 11.2 函数凹凸性

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
- 【例题】设 $f(x)$ 在区间 $I$ 的任一闭子区间上有上界并且满足

$$
f\left(\frac{x_1+x_2}{2}\right) \leq \frac{f\left(x_1\right)+f\left(x_2\right)}{2},
$$
则 $f(x)$ 是区间 $I$ 上的下凸函数。
证明: 反证法
假设结论不真, 则存在 $x_1 \in I, x_2 \in I, 0<t<1 / 2$, 使得
$$
f\left[t x_1+(1-t) x_2\right]-t f\left(x_1\right)-(1-t) f\left(x_2\right)=a>0,
$$
作函数$F(x)=f(x)-f\left(x_1\right)-\frac{f\left(x_2\right)-f\left(x_1\right)}{x_2-x_1}\left(x-x_1\right),$显然在 $I$ 的任一闭子区间中 $F(x)$ 与 $f(x)$ 同时有界或无界, 并可直接验证 $F(x)$ 与 $f(x)$ 具有相 同的凸性, 且满足$F\left(x_1\right)=F\left(x_2\right)=0, \quad F\left[t x_1+(1-t) x_2\right]=a>0,$

所以由(1)有
$$
\begin{aligned}
2 a &=2 F\left[t x_1+(1-t) x_2\right]=2 F\left(\frac{2 t x_1+(1-2 t) x_2+x_2}{2}\right) \\
& \leq F\left[2 t x_1+(1-2 t) x_2\right]+F\left(x_2\right)=F\left[2 t x_1+(1-2 t) x_2\right] .
\end{aligned}
$$
令 $t^{\prime}=2 t$, 所以$F\left[t^{\prime} x_1+\left(1-t^{\prime}\right) x_2\right] \geq 2 a>0,$若 $t^{\prime}<1 / 2$, 则重复上面手续; 若 $t^{\prime}>1 / 2$, 则令 $1-t^{\prime}=t_1^{\prime}, x_1=x_2^{\prime}, x_2=x_1^{\prime}$, 由 $(2)$ 得$F\left[t_1^{\prime} x_1^{\prime}+\left(1-t_1^{\prime}\right) x_2^{\prime}\right] \geq 2 a>0,$然后再重复前面手续. 因此, 存在 $t^{\prime \prime}, t^{\prime \prime \prime}, \cdots, t^{(n)}, \cdots$ 使得
$$
F\left[t^{(n)} x_1+\left(1-t^{(n)}\right) x_2\right] \geq 2^n a .
$$
由条件, $F(x)$ 应在 $x_1$ 及 $x_2$ 之间有界, 这与 (3)式矛盾. 故 $f(x)$ 是区间 $I$ 上的下凸函数.
注: 若将本题中有上界的条件改为在区间上连续, 其他条件不变, 也有相同的结果.

- 【例题】设函数 $f(x)$ 在区间 $I$ 为凸函数. 试证: $f(x)$ 在 $I$ 的任一闭子区间上有界. 
  证 设 $[a, b] \subset I$ 为任一闭子区间.
  $1^{\circ}$ (证明 $f(x)$ 在 $[a, b]$ 上有上界) $\forall x \in[a, b]$, 取 $\lambda=$ $\frac{x-a}{b-a} \in[0,1]$, 则 $x=\lambda b+(1-\lambda) a$. 因 $f$ 为凸函数, 所以
  $$
  \begin{aligned}
  f(x) &=f[\lambda b+(1-\lambda) a] \leqslant \lambda f(b)+(i-\lambda) f(a) \\
  & \leqslant \lambda M+(1-\lambda) M=M,
  \end{aligned}
  $$
  其中 $M=\max \{f(a), f(b)\}$. 即 $[a, b]$ 上有上界 $M$.
  $2^{\circ}$ (证明 $f(x)$ 在 $[a, b]$ 上有下界) 记 $c=\frac{a+b}{2}$ 为 $a, b$ 的中 点. 则 $\forall x \in[a, b]$ 有关于 $c$ 的对称点 $x^{\prime}$. 因 $f$ 为凸函数, 所以
  $$
  f(c) \leqslant \frac{f(x)+f\left(x^{\prime}\right)}{2} \leqslant \frac{1}{2} f(x)+\frac{1}{2} M .
  $$
  从而 $f(x) \geqslant 2 f(c)-M \stackrel{\text { 记 }}{\equiv} m$.即 $m$ 为 $f(x)$ 在 $[a, b]$ 上的下界.

- 【例题】设 $f(x)$ 为区间 $(a, b)$ 内的凸函数. 试证: $f(x)$ 在 $I$ 的任一内闭区间 $[\alpha, \beta] \subset(a, b)$ 上满足 Lipschitz 条件.
  证：要证明 $f(x)$ 在 $[\alpha, \beta]$ 上满足 Lipschitz 条件, 即要证明: $\exists L>0$, 使得 $\forall x_1, x_2 \in[\alpha, \beta]$ 有
  $$
  \left|f\left(x_1\right)-f\left(x_2\right)\right| \leqslant L\left|x_1-x_2\right| .
  $$
  因为 $[\alpha, \beta] \subset(a, b)$, 故可取 $h>0$ 充分小, 使得$[\alpha-h, \beta+h] \subset(a, b) .$于是 $\forall x_1, x_2 \in[\alpha, \beta]$, 若 $x_1<x_2$, 取 $x_3=x_2+h$. 根据 $f$ 的凸 性,
  $$
  \frac{f\left(x_2\right)-f\left(x_1\right)}{x_2-x_1} \leqslant \frac{f\left(x_3\right)-f\left(x_2\right)}{x_3-x_2} \leqslant \frac{M-m}{h}
  $$

(其中 $M, m$ 分别表示 $f(x)$ 在 $[\alpha-h, \beta+h]$ 上的上、下界), 从而
$$
f\left(x_2\right)-f\left(x_1\right) \leqslant \frac{M-m}{h}\left|x_2-x_1\right| .
$$
若 $x_2<x_1$, 可取 $x_3=x_2-h$, 由 $f$ 的凸性, 有
$$
\frac{f\left(x_2\right)-f\left(x_3\right)}{x_2-x_3} \leqslant \frac{f\left(x_1\right)-f\left(x_2\right)}{x_1-x_2} .
$$
从而$\frac{f\left(x_2\right)-f\left(x_1\right)}{x_1-x_2} \leqslant \frac{f\left(x_3\right)-f\left(x_2\right)}{x_2-x_3} \leqslant \frac{M-m}{h} .$由此亦可推得成立.

由本例可知: 若 $f(x)$ 在 $(a, b)$ 内为凸的, 则 $f(x)$ 在 $(a$, $b$ ) 内连续. 但注意端点的情况不一样: 即令 $f$ 在 $[a, b]$ 上为凸的, 不能保证 $a, b$ 处连续. 因端点处 $f(a), f(b)$ 改为更大的数不会改变凸性.

- 【例题】设 $f(x)$ 在 $[a, b]$ 上二次可微. 对 $[a, b]$ 中每个 $x, f(x)$ 与 $f^{\prime \prime}(x)$ 同号或同时为零, 又 $f(x)$ 在 $[a, b]$ 的任何子区 间内不恒为零. 试证: $f(x)=0$ 在 $(a, b)$ 内如果有根, 则必唯一.
  证 (反证法) 设 $f(x)=0$ 在 $(a, b)$ 内有二相异实根 $x_1, x_2$ $\in(a, b)$ (不妨设 $\left.x_1<x_2\right)$. 因为 $f(x)$ 在 $\left[x_1, x_2\right]$ 上连续, 在 $\left[x_1\right.$, $x_2$ ]上有最大、最小值, 而 $f\left(x_1\right)=f\left(x_2\right)=0$, 所以最大、最小值至 少有一个在内部达到 (否则 $f(x) \equiv 0$ 与已知条件矛盾). 例如在 $\xi$ $\in\left(x_1, x_2\right)$ 处有最大值 $f(\xi)>0$. 根据连续函数局部保号性, 必存 在 $\xi$ 的某个邻域 $U \equiv(\xi-\varepsilon, \xi+\varepsilon)$, 使得在 $U$ 上恒有 $f(x)>0$ (从而按已知条件, $U$ 上 $f^{\prime \prime}(x)>0, f$ 为凸函数), 又因 $f\left(x_1\right)=$ $f\left(x_2\right)=0$, 邻域 $U$ 可取得足够大, 以致在 $U$ 上 $f(x)$ 龵 $f(\xi)$, 于 是 $\exists \xi_1 \in U$ 使得$0<f\left(\xi_1\right)<f(\xi) .$记 $\xi_1$ 关于 $\xi$ 的对称点为 $\xi_2$, 则 $\xi_2 \in(\xi-\varepsilon, \xi+\varepsilon)$, 有$0<f\left(\xi_2\right) \leqslant f(\xi),$从而
  $$
  \frac{f\left(\xi_1\right)+f\left(\xi_2\right)}{2}<f(\xi)=f\left(\frac{\xi_1+\xi_2}{2}\right) .
  $$
  与凸性矛盾.





#### 11.3 函数性质作图

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





#### 补充：

- 【例题】证明如下不等式：$e^x-1-x>1-\cos x, \quad x>0$;
  证明:证法1) 利用函数单调性
  $$
  \text { 令 } f(x)=\mathrm{e}^x-x+\cos x-2, f^{\prime}(x)=\mathrm{e}^x-1-\sin x, f^{\prime \prime}(x)=\mathrm{e}^x-\cos x>0(x>0) \text {. }
  $$
  证法2) 利用Lagrange中值定理
  将不等式写成 $\mathrm{e}^x+\cos x-2>x$, 考察函数 $f(x)=\mathrm{e}^x+\cos x$, 则 $f(x)$ 在 $[0, x]$ 上连 续, 在 $(0, x)$ 内可导, 且 $f(0)=2$, 于是由Lagrange中值定理, 至少存在一点 $\xi \in(0, x)$, 使 $f(x)-f(0)=f^{\prime}(\xi) x$, 即 $\mathrm{e}^x+\cos x-2=\left(\mathrm{e}^{\xi}-\sin \xi\right) x ;$ 易证 $\xi>0$ 时, $\mathrm{e}^{\xi}-\sin \xi>1$, 从而证明了原不等式.
  证法3) 利用Taylor公式
  将不等式写成 $\mathrm{e}^x+\cos x>2+x$. 设 $f(x)=\mathrm{e}^x+\cos x$, 写出 $f(x)$ 的二阶麦克劳林公 式
  $$
  \begin{gathered}
  f(0)=2, f^{\prime}(0)=1, f^{\prime \prime}(0)=0, f^{\prime \prime \prime}(\xi)=\mathrm{e}^{\xi}+\sin \xi, \\
  \mathrm{e}^x+\cos x=2+x+0+\frac{1}{3 !}\left(\mathrm{e}^{\xi}+\sin \xi\right) x^3,(0<\xi<x)
  \end{gathered}
  $$
  由于 $\xi>0, \mathrm{e}^{\xi}+\sin \xi>0$, 故当 $x>0$ 时有 $\mathrm{e}^x+\cos x>2+x$.

- 【例题】计算 $y=\arctan x$ 带 Maclaurin余项的局部泰勒公式。
  证明： 我们知道 $y^{\prime}=\frac{1}{1+x^2}$, 根据前面的例题可以写出 $y^{\prime}$ 的局部泰勒公式:
  $$
  y^{\prime}=\frac{1}{1+x^2}=1-x^2+x^4-\cdots+(-1)^n x^{2 n}+o\left(x^{2 n+1}\right) .
  $$
  直观理解 对 Taylor公式(40)的左右两侧同时计算积分:
  $$
  y=\int \frac{\mathrm{d} x}{1+x^2}=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots \frac{(-1)^n x^{2 n+1}}{2 n+1}+o\left(x^{2 n+2}\right),
  $$
  这里我们还借助了无穷小量的形式积分运算 $\int o\left(x^{2 n+1}\right) \mathrm{d} x=o\left(x^{2 n+2}\right)$ 。从直观 上, $2 n+1$ 次的函数积分得到 $2 n+2$ 次的函数是直观的, 上述方法得到的泰勒公式 也是完全正确的, 但是上述方法理论有两个错误:
  1. 积分 $\int o\left(x^{2 n+1}\right) \mathrm{d} x=o\left(x^{2 n+2}\right)$ 是毫无道理的形式计算；
  2. 泰勒公式不是简单的等式, 而是刻画 $x \rightarrow 0$ 的极限, 我们曾经说过极限运算和积分运算通常不能换序, 因此不能简单的对于 $y^{\prime}$ 泰勒公式逐项地积分；

- 【例题】如果$f(x)$在$(0,\infin)$上二阶可导，且$a>0$，证明如下：

  - (1) $\lim _{x \rightarrow+\infty} a f(x)+f'(x)=l$，则有$ \quad \lim _{x \rightarrow+\infty} f(x)=\frac{l}{a}$
  - (2) $\lim _{x \rightarrow+\infty} a f(x)+2 \sqrt{x} f’(x)=l \quad$则有 $\lim _{x \rightarrow+\infty} f(x)=\frac{l}{a}$
  - (3) $\lim _{x \rightarrow+\infty} f(x)+f’(x)+f’’(x)=l$. 则有$\lim _{x \rightarrow+\infty} f(x)=l$

- 【例题】设函数 $f(x)$ 是 $(0,+\infty)$ 的有界可导函数, 且存在 $a>0$ 使得 $\lim _{x \rightarrow \infty}\left(a f(x)-f^{\prime}(x)\right)$ 存 在, 求证 $\lim _{x \rightarrow+\infty} f(x)$ 存在。
  分析: 洛必达法则在证明题中的主要作用, 是建立 $f$ 相关的极限与 $f^{\prime}$ 相关的极限之 间的关系。为了使用题目中条件 $\lim _{x \rightarrow \infty}\left(a f(x)-f^{\prime}(x)\right)$ 存在, 我们构造辅助函数。

  Proof. 构造辅助函数 $F(x)=\mathrm{e}^{-a x} f(x)$ 和 $G(x)=\mathrm{e}^{-a x}$, 由于函数 $f$ 有界, 当 $x \rightarrow$ $+\infty$ 时 $F(x)$ 和 $G(x)$ 都是无穷小量。且我们有极限
  $$
  \lim _{x \rightarrow+\infty} \frac{F^{\prime}(x)}{G^{\prime}(x)}=\lim _{x \rightarrow+\infty} \frac{-\mathrm{e}^{-a x}\left(a f(x)-f^{\prime}(x)\right)}{-a \mathrm{e}^{-a x}}=\frac{1}{a} \lim _{x \rightarrow \infty}\left(a f(x)-f^{\prime}(x)\right) .
  $$
  由于极限 $\lim _{x \rightarrow+\infty} \frac{F^{\prime}(x)}{G^{\prime}(x)}$ 收敛, 用洛必达法则有
  $$
  \lim _{x \rightarrow \infty} f(x)=\lim _{x \rightarrow \infty} \frac{F(x)}{G(x)}=\lim _{x \rightarrow+\infty} \frac{F^{\prime}(x)}{G^{\prime}(x)},
  $$
  也是收敛的极限。

- 【例题】设函数 $f(x)$ 在 $a$ 某个邻域二阶导连续, 根据拉格朗日中值定理$f(a+h)-f(a)=h f^{\prime}(a+h \theta(h)),$

  其中 $\theta(h) \in(0,1)$ 是依赖 $h$ 的参数。求证 $\lim _{h \rightarrow 0} \theta(h)=\frac{1}{2}$ 。
  Proof. 我们写出点 $a$ 处带Lagrange余项的二次泰勒公式$f(a+h)=f(a)+h f^{\prime}(a)+\frac{h^2}{2} f^{\prime \prime}(a+\xi(h))$

  其中 $\xi(h) \in(0,1)$ 是依赖 $h$ 的参数。消去 $h$ 得$f^{\prime}(a+\theta(h) h)-f^{\prime}(a)=\frac{h}{2} f^{\prime \prime}(a+\xi(h)) .$

  根据二阶导数的定义
  $$
  \lim _{h \rightarrow 0} \frac{f^{\prime}(a+\theta(h) h)-f^{\prime}(a)}{h \theta(h)}=f^{\prime \prime}(a)
  $$
  代入得$\lim _{h \rightarrow 0} \frac{f^{\prime \prime}(a+\xi(h))}{2 \theta(h)}=f^{\prime \prime}(a)$​,由于二阶导连续, 同时 $a<a+\xi(h) h<a+h$, 使用
  $$
  \lim _{h \rightarrow 0} f^{\prime \prime}(a+\xi(h))=f^{\prime \prime}(a) .
  $$
  得$\lim _{h \rightarrow 0} \theta(h)=\frac{1}{2} .$

- 【例题】$f(x)$ 在 $[-1,1]$ 上有二阶导数, 且 $f(0)=f^{\prime}(0)=0$. 对任意的 $x \in[-1,1]$, 有 $\left|f^{\prime \prime}(x)\right| \leqslant|f(x)|$. 证明: $f(x)$ 恒为 0 .
  证明. 由题目条件, 为了将二阶导数和函数本身联系起来, 我们考虑写出对 $f(x)$ 在 0 点处的 带有 Lagrange 余项的 Taylor 公式, 即$f(x)=\frac{1}{2} f^{\prime \prime}(\xi) x^2,$其中 $\xi \in(0, x)$, 这里我们不妨假设 $x>0$. 对于 $x<0$ 讨论是类似的. 利用题目条件, 可得$|f(x)| \leqslant \frac{|f(\xi)| x^2}{2} .$特别地, 设 $M$ 为 $|f|$ 在 $[-1,1]$ 上的最大值, 则有$|f(x)| \leqslant \frac{M x^2}{2} \leqslant \frac{M}{2} .$

  两边取最大值, 可得 $M \leqslant M / 2$, 从而 $M=0$.注: 此类题目还经常会用到递推, 例如

$$
|f(x)| \leqslant \frac{x^2}{2}|f(\xi)| \leqslant \frac{x^2}{2} \frac{\xi^2}{2}\left|f\left(\xi_1\right)\right| \leqslant \cdots \leqslant\left(\frac{x^2}{2}\right)^n M,
$$
再令 $n$ 趋于正无穷即可.

- 【例题】导函数插值估计

  (a) 设 $f(x)$ 在 $[0,1]$ 上二阶可导, 且对任意的 $x \in[0,1]$ 有 $|f(x)| \leqslant A$ 和 $\left|f^{\prime \prime}(x)\right| \leqslant B$. 证明: $\left|f^{\prime}(x)\right| \leqslant 2 A+B / 2$.
  (b) 设 $f(x)$ 在 $(0,+\infty)$ 上二阶可导, 且对任意的 $x \in(0,+\infty)$ 有 $|f(x)| \leqslant A$ 和 $\left|f^{\prime \prime}(x)\right| \leqslant B$. 证明: $\left|f^{\prime}(x)\right| \leqslant 2 \sqrt{A B}$.
  (c) 设 $f(x)$ 在 $(-\infty,+\infty)$ 上二阶可导, 且对任意的 $x \in(-\infty,+\infty)$ 有 $|f(x)| \leqslant A$ 和 $\left|f^{\prime \prime}(x)\right| \leqslant B$. 证明: $\left|f^{\prime}(x)\right| \leqslant \sqrt{2 A B}$.
  证明. (a) 由于 $f^{\prime}(x)$ 在 $[0,1]$ 上是连续的, 因此我们不妨假设 $x \in(0,1)$. 因此, 为了得到 $f^{\prime}(x)$, 由在 $x$ 处展开的带 Lagrange 余项的 Taylor 公式, 我们知道存在 $\xi \in(0, x)$ 和 $\eta \in(x, 1)$, 使得
  $$
  \begin{aligned}
  &f(0)=f(x)+f^{\prime}(x)(0-x)+\frac{f^{\prime \prime}(\xi)}{2}(0-x)^2, \\
  &f(1)=f(x)+f^{\prime}(x)(1-x)+\frac{f^{\prime \prime}(\eta)}{2}(1-x)^2,
  \end{aligned}
  $$
  为了消去 $x f^{\prime}(x)$ 项, 我们将两式做差, 得到
  $$
  f(0)-f(1)=-f^{\prime}(x)+\frac{f^{\prime \prime}(\xi)}{2} x^2-\frac{f^{\prime \prime}(\eta)}{2}(1-x)^2,
  $$
  整理可得
  $$
  \left|f^{\prime}(x)\right|=\left|f(1)-f(0)+\frac{f^{\prime \prime}(\xi)}{2} x^2-\frac{f^{\prime \prime}(\eta)}{2}(1-x)^2\right| \leqslant 2 A+\frac{B}{2}\left[x^2+\left(1-x^2\right)\right] \leqslant 2 A+\frac{B}{2} .
  $$

