《高等数学A》第十次习题课

> Author ZhenLiu
>
> 2022/11/08



#### 10.1 泰勒公式

- 唯一性定理: 设 $f(x)$ 在 $x_0$ 的某邻域内有定义, 若 $a_k$ 和 $b_k(k=0,1, \cdots, n)$ 都是常数, 当 $x \rightarrow x_0$ 时, 既有
  $$
  f(x)=a_0+a_1\left(x-x_0\right)+\cdots+a_n\left(x-x_0\right)^n+o\left(\left(x-x_0\right)\right),
  $$
  又有
  $$
  f(x)=b_0+b_1\left(x-x_0\right)+\cdots+b_n\left(x-x_0\right)^n+o\left(\left(x-x_0\right)\right),
  $$
  则必有 $a_k=b_k, \quad k=0,1, \cdots, n$.

- 【例题：taylor展开唯一性】设 $P(x)$ 是 $n$ 次多项式,试证：
  $$
  \sum_{k=0}^n \frac{P^{(k)}(0)}{(k+1) !} x^{k+1}=\sum_{k=0}^n(-1)^k \frac{P^{(k)}(x)}{(k+1) !} x^{k+1}, P^{(0)}(x) \equiv P(x) .
  $$

  证： $P(x)=a_0+a_1 x+\cdots+a_n x^n$, 则 $a_k=\frac{P^{(k)}(0)}{k !} \quad(k=$ $0,1,2, \cdots, n)$.
  令 $f(x)=a_0 x+a_1 \frac{x^2}{2}+\cdots+a_n \frac{x^{n+1}}{n+1}$, 则
  $$
  f^{(k+1)}(x)=P^{(k)}(x) \quad(k=0,1,2, \cdots, n) \text {. }
  $$
  $$
  f(x)=\sum_{k=0}^n a_k \frac{x^{k+1}}{k+1}=\sum_{k=0}^n \frac{P^{(k)}(0)}{(k+1) !} x^{k+1} \text {. }
  $$
  $\forall x_0$, 将 $f$ 在 $x_0$ 处展开, 有
  $$
  f(x)=f\left(x_0\right)+\sum_{i=0}^{n+1} \frac{f^{(i)}\left(x_0\right)}{i !}\left(x-x_0\right)^i .
  $$
  令 $x=0$​ 得
  $$
  0=f(0)=f\left(x_0\right)+\sum_{i=0}^{n+1} \frac{(-1)^i f^{(i)}\left(x_0\right)}{i !} x_0^i,
  $$
  注意 $x_0$ 的任意性, 不妨把 $x_0$ 改记为 $x$, 移项则得$f(x)=-\sum_{i=1}^{n+1} \frac{(-1)^i f^{(i)}(x)}{i !} x^i$
  $令k=i-1$，则$\sum_{k=0}^n \frac{(-1)^k f^{(k+1)}(x)}{(k+1) !} x^{k+1}$





#### 10.2 泰勒公式余项

- Peano 型: $f(x)=f\left(x_0\right)+f^{\prime}\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{1}{n !} f^{(n)}\left(x_0\right)\left(x-x_0\right)^n+o\left(\left(x-x_0\right)^n\right)$.

- Lagrange型: $f(x)=f\left(x_0\right)+f^{\prime}\left(x_0\right)\left(x-x_0\right)+\cdots+\frac{1}{n !} f^{(n)}\left(x_0\right)\left(x-x_0\right)^n+\frac{f^{(n+1)}(\xi)}{(n+1) !}\left(x-x_0\right)^{n+1}$. 

  【注1】需要注意的是Lagrange型公式需要n+1阶导数是存在的，必须满足条件才能使用。

  【注2】Peano型余项的 Taylor 公式只给了逼近误差的定性估计. 若 $f(x)$ 在 $x_0$ 点存在 $n$ 阶导数, 则 $f(x)$ 在 $x_0$ 点附近可以用 $n$ 次 Taylor 多项式逼近, 当 $x \rightarrow x_0$ 时, 误差为比 $\left(x-x_0\right)^n$ 高 阶的无穷小量. 而 Lagrange 型公式给出了定量估计, 但要求也更高了, 要求 $f(x)$ 在 $x_0$ 的 某个邻域内有 $n+1$ 阶导数.若把 $x_0$ 看成定点, $x$ 看成动点, 则上式通过定点 $x_0$ 处的 函数值 $f\left(x_0\right)$ 的导数值 $f^{\prime}\left(x_0\right), \cdots, f^{(n)}\left(x_0\right)$ 表达动点 $x$ 处的函数值 $f(x)$. 当问题涉及到 2 阶以上的导数时, 通常可考虑用 Taylor公式求解. 这里关键在于选取函数 $f$, 点 $x_0$, 展开的阶次 $n$, 以及余项的形式等。

- 【例题：证明中值公式】设 $f(x)$ 在 $[a, b]$ 上三次可导, 试证; $\exists c \in(a, b)$, 使 得
  $$
  f(b)=f(a)+f^{\prime}\left(\frac{a+b}{2}\right)(b-a)+\frac{1}{24} f^{\prime \prime \prime}(c)(b-a)^3 .
  $$
  证 ：(待定常数法) 设 $k$ 为使下式成立的实数:
  $$
  f(b)-f(a)-f^{\prime}\left(\frac{a+b}{2}\right)(b-a)-\frac{1}{24} k(b-a)^3=0
  $$
  此时我们的问题归为证明: $\exists c \in(a, b)$, 使得$k=f^{\prime \prime \prime}(c) . $
  $$
  \begin{gathered}
  \\
  \text { 令 } g(x)=f(x)-f(a)-f^{\prime}\left(\frac{a+x}{2}\right)(x-a)-\frac{k}{24}(x-a)^3 \text {. } \\
  \text { 则 } g(a)=g(b)=0 .
  \end{gathered}
  $$
  根据 Rolle定理, $\exists \xi \in(a, b)$, 使得 $g^{\prime}(\xi)=0$, 由 $(4)$ 式, 即：
  $$
  f^{\prime}(\xi)-f^{\prime}\left(\frac{a+\xi}{2}\right)-f^{\prime \prime}\left(\frac{a+\xi}{2}\right) \frac{(\xi-a)}{2}-\frac{k}{8}(\xi-a)^2=0 .
  $$
  这是关于 $k$ 的方程, 注意到 $f^{\prime}(\xi)$ 在点 $\frac{a+\xi}{2}$ 处的 Taylor 公式:
  $$
  f^{\prime}(\xi)=f^{\prime}\left(\frac{a+\xi}{2}\right)+f^{\prime \prime}\left(\frac{a+\xi}{2}\right) \frac{(\xi-a)}{2}+\frac{1}{2} f^{\prime \prime \prime}(c)\left(\frac{\xi-a}{2}\right)^2
  $$

- 【例题：证明不等式】设 $f(x)$ 在 $[a, b]$ 上二次可铰, $f^{\prime \prime}(x)<0$. 试证: $\forall a$ $\leqslant x_1<x_2<\cdots<x_n \leqslant b, k_i \geqslant 0, \sum_{i=1}^n k_i=1$, 有$f\left(\sum_{i=1}^n k_i x_i\right)>\sum_{i=1}^n k_i f\left(x_i\right) .$

  证:取 $x_0=\sum_{i=1}^2 k_i x_i$ 将 $f\left(x_i\right)$ 在 $x=x_0$ 处展开
  $$
  \begin{aligned}
  f\left(x_i\right)=& f\left(x_0\right)+f^{\prime}\left(x_0\right)\left(x_i-x_0\right)+\frac{1}{2}-f^{\prime \prime}\left(\xi_i\right)\left(x_i-x_0\right)^2 \\
  &<f\left(x_0\right)+f^{\prime}\left(x_0\right)\left(x_i-x_0\right) \quad(i=1,2, \cdots, n) .
  \end{aligned}
  $$
  以 $k_i$ 乘此式两端, 然后 $n$ 个不等式相加, 注意 $\sum_{i=1}^n k_i=1$,
  $$
  \sum_{i=1}^n k_i\left(x_i-x_i\right)=\sum_{i=1}^n k_i x_i-x_0=0,
  $$
  得
  $$
  \sum_{i=1}^n k_i f\left(x_i\right)<f\left(x_0\right)=f\left(\sum_{i=1}^n k_i x_i\right)
  $$

- 【例题：导数中值的估计】若 $f(x)$ 在 $[a, b]$ 上有二阶导数, $f^{\prime}(a)=f^{\prime}(b)=0$, 佣证: $\exists \xi \in(a, b)$, 使得
  $$
  \left|f^{''}(\xi)\right| \geqslant \frac{4}{(b-a)^2}|f(b)-f(a)| .
  $$
  证：这用 Taylor 公式, 将 $f\left(\frac{a+b}{2}\right)$ 分别在 $a, b$ 点展开, 注意 $f^{\prime}(a)=f^{\prime}(b)=0, \exists \xi, \eta ： a<\xi<\frac{a+b}{2}<\eta<b$ 使得
  $f\left(\frac{a+b}{2}\right)=f(a)+\frac{1}{2} f^{\prime \prime}(\zeta)\left(\frac{b-a}{2}\right)^2$,
  $f\left(\frac{a+b}{2}\right)=f(b)+\frac{1}{2} f^{\prime \prime}(\eta)\left(\frac{b-a}{2}\right)^2$.
  从而得 $f(b)-f(a)+\frac{1}{8}\left[f^{\prime \prime}(\eta)-f^{\prime \prime}(\xi)\right](b-a)^2=0$.
  故 $\frac{4|f(b)-f(a)|}{(b-a)^2} \leqslant \frac{1}{2}\left(\left|f^{\prime \prime}(\xi)\right|+\left|f^{\prime \prime}(\eta)\right|\right) \leqslant\left|f^{\prime \prime}(\xi)\right|$.（取两者之中较大的即可）

- 【例题：关于界的估计】设 $f(x)(-\infty<x<+\infty)$ 为二次可微函数 $M_k=\sup _{-\infty<x<+\infty}\left|f^{(k)}(x)\right|<+\infty \quad(k=0,2)$.$f^{(0)}(x)$ 表示 $f(x)$. 证明：

  $M_{\mathrm{1}}=\sup _{-\infty<x<+\infty}| f^{\prime}(x) \mid<+\infty$, 且$M_{\mathrm{1}}^2 \leqslant 2 M_0 M_2$.

  证： $f(x+h)=f(x)+f^{\prime}(x) h+\frac{1}{2} f^{\prime \prime}(\xi) h^2 \quad(\xi$ 在 $x$ 与 $x+h$ 之间)
  $f(x-h)=f(x)-f^{\prime}(x) h+\frac{1}{2} f^{\prime \prime}(\eta) h^2 \quad(\eta$ 在 $x-h$ 与 $x$ 之间）

  二式相减
  $$
  f(x+h)-f(x-h)=2 f^{\prime}(x) h+\frac{h^2}{2}\left[f^{\prime \prime}(\xi)-f^{\prime \prime}(\eta)\right],
  $$
  即 $2 f^{\prime}(x) h=f(x+h)-f(x-h)-\frac{h^2}{2}\left[f^{\prime \prime}(\xi)-f^{\prime \prime}(\eta)\right]$,
  所以 $2\left|f^{\prime}(x)\right| h \leqslant|f(x+h)|+|f(x-h)|+\frac{1}{2} h^2\left(\left|f^{\prime \prime}(\xi)\right|+\left|f^{\prime \prime}(\eta)\right|\right) \leqslant 2 M_0+h^2 M_2$,
  即 $M_2 h^2-2^{\prime} f^{\prime}(x) \mid h+2 M_0 \geqslant 0$ 对一切 $h$ 成立
  因此判别式 $\left.\quad \mid f^{\prime}(x)\right)^2-2 M_0 M_2 \leqslant 0$,
  即 $\left|f^{\prime}(x)\right|^2 \leqslant 2 M_0 M_2$ 所以 $M_1=\sup _{-\infty<x<+\infty}\left|f^{\prime}(x)\right|<+\infty$, 且 $M_1^2 \leqslant 2 M_0 M_2$.

- 【例题：无穷远处的极限】设函数 $\varphi(x)$ 在 $[0,+\infty)$ 上二次连续可微, 如果 $\lim _{x \rightarrow+\infty} \varphi(x)$ 存在, 且 $\varphi^{\prime \prime}(x)$ 在 $[0,+\infty)$ 上有界. 试证: $\lim _{x \rightarrow+\infty} \varphi^{\prime}(x)=0$. 
  证：要证明 $\lim _{x \rightarrow+\infty} \varphi^{\prime}(x)=0$, 即要证明: $\forall \varepsilon>0, \exists \Delta>0$, 当 $x>\Delta$ 时 $\left|\varphi^{\prime}(x)\right|<\varepsilon$ ，利用 Taylor 公式, $\forall h>0$,$\varphi(x+h)=\varphi(x)+\varphi^{\prime}(x) h+\frac{1}{2} \varphi^{\prime \prime}(\xi) h^2,$即 $\varphi^{\prime}(x)=\frac{1}{h}[\varphi(x + h)-\varphi(x)]-\frac{1}{2} \varphi^{\prime \prime}(\xi) h$.
  记 $A=\lim _{x \rightarrow+\infty} \varphi(x)$. 因 $\varphi^{\prime \prime}$ 有界, 所以 $\exists M>0$, 使得 $\left|\varphi^{\prime \prime}(x)\right| \leqslant M$ $(\forall x \geqslant a)$. 故由 $(1)$ 知
  $$
  \left|\varphi^{\prime}(x)\right| \leqslant \frac{1}{h}(|\varphi(x+h)-A|+|A-\varphi(x)|)+\frac{1}{2} M h^2 .
  $$
  $\forall \varepsilon>0$, 首先可取 $h>0$ 充分小, 使得 $\frac{1}{2} M h^2<\frac{\varepsilon}{2}$. 然后将 $h$ 固定. 因 $\lim _{x \rightarrow+\infty} \varphi(x)=A$, 所以 $\exists \Delta>0$, 当 $x>\Delta$ 时
  $$
  \frac{1}{h}(|\varphi(x+h)-A|+|A-\varphi(x)|)<\frac{\varepsilon}{2} .
  $$
  从而可以得 $\quad | \varphi^{\prime}(x) \mid<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$.

- 【例题：函数方程中的应用】设 $f(x)$ 在 $(-\infty,+\infty)$ 内有连续三阶导数, 且满足方程:
  $$
  f(x+h)=f(x)+h f^{\prime}(x+\theta h), 0<\theta<1,(\theta \text { 与 } h \text { 无关) } .
  $$
  试证: $f(x)$ 是一次或二次函数。
  证 问题在于证明: $f^{\prime \prime}(x) \equiv 0$ 或 $f^{\prime \prime \prime}(x) \equiv 0$. 为此将式子对 $h$ 求导, 注意 $\theta$ 与 $h$ 无关, 我们有
  $$
  f^{\prime}(x+h)=f^{\prime}(x+\theta h)+\theta h f^{''}(x+\theta h) .
  $$
  从而 $\frac{f^{\prime}(x+h)-f^{\prime}(x)+f^{\prime}(x)-f^{\prime}(x+\theta h)}{h}=\theta f^{\prime \prime}(x+\theta h)$.令 $h \rightarrow 0$ 取极限, 得
  $$
  f^{\prime \prime}(x)-\theta f^{\prime \prime}(x)=\theta f^{\prime \prime}(x), f^{\prime \prime}(x)=2 \theta f^{\prime \prime}(x) .
  $$
  若 $\theta \neq \frac{1}{2}$, 由此知 $f^{\prime \prime}(x) \equiv 0, f(x)$ 为一次函数; 若 $\theta=\frac{1}{2}$, 第一次求导之后的式子给出
  $$
  f^{\prime}(x+h)=f^{\prime}\left(x+\frac{1}{2} h\right)+\frac{1}{2} h f^{\prime \prime}\left(x+\frac{1}{2} h\right)
  $$
  此式两端同时对 $h$ 求导, 减去 $f^{\prime \prime}(x)$, 郃以 $h$, 然后令 $h \rightarrow 0$ 取极限, 即得 $f^{\prime \prime \prime}(x) \equiv 0, f(x)$ 为二次函数.

- 【例题】设 $f(x)$ 在无穷区间 $\left(x_0,+\infty\right)$ 上可微分两次, 并且 $\lim _{x \rightarrow+\infty} f(x)$ $=\lim _{x \rightarrow x_0^{+}} f(x)$ 存在且有限, 试证: 在区间 $\left(x_0,+\infty\right)$ 内 至少有一点 $\xi$, 满足 $f^{\prime \prime}(\xi)=0$. 
  提示：若 $f^{\prime \prime}(x)$ 在 $\left(x_0,+\infty\right)$ 内变号, 由导数的介值性(Darboux 定理), 知 $\exists \xi$ 使 $f^{\prime \prime}(\xi)=0$. 若 $f^{\prime \prime}(x)$ 不变号 (恒大于 0 , 或恒小于 $0 ̣$ ), 必导致 矛盾.
  再提示 $f(+\infty)=f\left(x_0+0\right){\Longrightarrow} \exists \eta \in(0,+\infty)$ 使得 $\left.f^{\prime} (\eta\right)=0$. 若 $f^{\prime \prime}(x)$ 恒大于 0 , 则 $f^{\prime}$ 严 $\pi, x_1>\eta$ 时, 有 $f^{\prime}\left(x_1\right)>f^{\prime}(\eta)=0$. 从而
  $$
  \begin{aligned}
  f(x) &=f\left(x_1\right)+f^{\prime}\left(x_1\right)\left(x-x_1\right)+\frac{f^{\prime \prime}(\zeta)}{2}\left(x-x_1\right)^2 \\
  &>f\left(x_1\right)+f^{\prime}\left(x_1\right)\left(x-x_1\right) \rightarrow+\infty(\text { 当 } x \rightarrow+\infty) .
  \end{aligned}
  $$
  与 $\lim _{x \rightarrow+\infty} f(x)$ 存在且有限相矛盾.同理 $f^{\prime \prime}(x)$ 恒小于 0 也不可能.

  





#### 10.3 常见泰勒公式

- Maclaurin公式

  $$\begin{aligned} \mathrm{e}^x &=1+x+\frac{1}{2 !} x^2+\cdots+\frac{1}{n !} x^n+\frac{\mathrm{e}^{\theta x}}{(n+1) !} x^{n+1} \quad(0<\theta<1) \\ \sin x=x-& \frac{x^3}{3 !}+\frac{x^5}{5 !}-\cdots+\frac{(-1)^{k+1}}{(2 k-1) !} x^{2 k-1}+(-1)^k \frac{\cos \theta x}{(2 k+1) !} x^{2 k+1} \quad(0<\theta<1) \\ \cos x=1-& \frac{x^2}{2 !}+\frac{x^4}{4 !}-\cdots+\frac{(-1)^k}{(2 k) !} x^{2 k}+(-1)^{k+1} \frac{\cos \theta x}{(2 k+2) !} x^{2 k+2} \quad(0<\theta<1) \\ \ln (1+x)=& x-\frac{1}{2} x^2+\frac{1}{3} x^3-\cdots+(-1)^{n-1} \frac{1}{n} x^n+(-1)^n \frac{x^{n+1}}{(n+1)(1+\theta x)^{n+1}} \quad(0<\theta<1) \\(1+x)^\alpha=& 1+\alpha x+\frac{\alpha(\alpha-1)}{2 !} x^2+\cdots+\frac{\alpha(\alpha-1) \cdots(\alpha-n+1)}{n !} x^n \\ &+\frac{\alpha(\alpha-1) \cdots(\alpha-n)}{(n+1) !}(1+\theta x)^{\alpha-(n+1)} x^{n+1} \quad(0<\theta<1) \end{aligned}$$

- 【例题】利用 Taylor 公式求下列极限
  (1) $\lim _{x \rightarrow+\infty}\left[\sqrt[3]{x^3+3 x}-\sqrt{x^2-2 x}\right]$;
  解: 设 $y=\frac{1}{x}$, 则原问题等价于求 $\lim _{y \rightarrow 0^{+}} \frac{1}{y}\left[\sqrt[3]{1+3 y^2}-\sqrt{1-2 y}\right]$, 又当 $y \rightarrow 0^{+}$时,

$$
\begin{aligned}
&\sqrt[3]{1+3 y^2}=1+y^2+o\left(y^2\right) \\
&\sqrt{1-2 y}=1-y+o(y) .
\end{aligned}
$$
故 $\lim _{y \rightarrow 0^{+}} \frac{1}{y}\left[\sqrt[3]{1+3 y^2}-\sqrt{1-2 y}\right]=\lim _{y \rightarrow 0^{+}} \frac{1}{y}\left[y^2+o\left(y^2\right)+y-o(y)\right]=1$.
(2) $\lim _{x \rightarrow+\infty} x^2 \ln \left(x \sin \frac{1}{x}\right)$.
解: 设 $y=\frac{1}{x}$, 则原问题等价于求 $\lim _{y \rightarrow 0^{+}} \frac{1}{y^2} \ln \left(\frac{1}{y} \sin y\right)=\lim _{y \rightarrow 0^{+}} \frac{1}{y^2} \ln \left(1+\frac{1}{y} \sin y-1\right)$. 由因
$$
\frac{1}{y} \sin y-1=\frac{1}{y}\left(y-\frac{1}{3 !} y^3+o\left(y^3\right)\right)-1=-\frac{1}{3 !} y^2+o\left(y^2\right) .
$$
故由 Taylor 公式可知
$$
\lim _{y \rightarrow 0^{+}} \frac{1}{y^2} \ln \left(1+\frac{1}{y} \sin y-1\right)=\lim _{y \rightarrow 0^{+}} \frac{1}{y^2}\left[-\frac{1}{3 !} y^2+o\left(y^2\right)+o\left(-\frac{1}{3 !} y^2+o\left(y^2\right)\right)\right]=-\frac{1}{6} .
$$
(3) $\lim _{x \rightarrow \infty}\left[\left(x^3-x^2+\frac{x}{2}\right) e^{\frac{1}{x}}-\sqrt{1+x^6}\right]$
解: 当 $x \longrightarrow \infty$ 时,
$$
\begin{aligned}
e^{\frac{1}{x}} &=1+\frac{1}{x}+\frac{1}{2 x^2}+\frac{1}{6 x^3}+o\left(\frac{1}{x^3}\right), \\
\sqrt{1+x^6} &=x^3 \sqrt{1+\frac{1}{x^6}}=x^3\left[1+\frac{1}{2 x^6}+o\left(\frac{1}{x^6}\right)\right],
\end{aligned}
$$
故
$$
\left[\left(x^3-x^2+\frac{x}{2}\right) e^{\frac{1}{x}}-\sqrt{1+x^6}\right]=\frac{1}{12 x}+\frac{1}{12 x^2}-\frac{1}{2 x^3}+\frac{1}{6}+o(1) .
$$
由此可得 $\lim _{x \longrightarrow \infty}\left[\left(x^3-x^2+\frac{x}{2}\right) e^{\frac{1}{x}}-\sqrt{1+x^6}\right]=\frac{1}{6}$.
注 若使用 L'Hospital 法则, 需变换 $\lim _{x \rightarrow \infty} \frac{\frac{\left(x^3-x^2+\frac{x}{2}\right) e^{\frac{1}{x}}}{\sqrt{1+x^6}}-1}{\frac{1}{\sqrt{1+x^6}}}$, 计算较为复杂, 容易出错.

- 【例题】设 $f(x)=x^2 \ln (x+1)$, 求 $f^{(n)}(0)$.
  分析: 可用 Leibniz 公式, 但较麻烦. 所以先用 Maclaurin 公式将 $f(x)$ 展开.
  解: 因为 $\ln (1+x)=x-\frac{1}{2} x^2+\frac{1}{3} x^3-\cdots+(-1)^{n-1} \frac{1}{n-2} x^{n-2}+o\left(x^{n-2}\right)$, 所以 $x^2 \ln (1+x)=x^3-\frac{x^4}{2}+\frac{x^5}{3}-\cdots+(-1)^{n-1} \frac{x^n}{n-2}+o\left(x^n\right)$. 由多项式导数和系数的关系可知 $\frac{f^{(n)}(0)}{n !}=(-1)^{n-1} \frac{1}{n-2}$, 故 $f^{(n)}(0)=\frac{(-1)^{n-1} n !}{n-2}$.



#### 补充内容

- 【例题】称函数 $f(x)$ 在闭区间 $[a, b]$ 上满足李普希茨条件, 若存在常数 $L>0$, 使对任意 $x_1, x_2 \in[a, b]$, 都有

$$
\left|f\left(x_2\right)-f\left(x_1\right)\right| \leqslant L\left|x_2-x_1\right| .
$$
(1) 若 $f^{\prime}(x)$ 在 $[a, b]$ 上连续,证明: $f(x)$ 在 $[a, b]$ 上满足李普希茨条件.
(2) 在 (1) 中所述事实的逆命题是否成立?
(3) 举一个在 $[a, b]$ 上连续但不满足李普希茨条件的函数.

- 【例题】若多项式 $P(x)-a$ 与 $P(x)-b$ 的全部根都是单实根,证明：对任意实数 $c \in$ $(a, b)$, 多项式 $P(x)-c$ 的根也全都是单实根.

- 不等式的证明方法

  - 【例题：单调性】证明 $\frac{|a+b|}{1+|a+b|} \leqslant \frac{|a|}{1+|a|}+\frac{|b|}{1+|b|}$.
    证 记 $f(x)=\frac{x}{1+x}$, 则 $f^{\prime}(x)=\frac{1}{(1+x)^2}>0, f(x)=\frac{x}{1+x}$$\nearrow$.
    于是由 $|a+b| \leqslant|a|+|b|$ 知
    $$
    \begin{aligned}
    \frac{|a+b|}{1+|a+b|} & \leqslant \frac{|a|+|b|}{1+|a|+|b|}=\frac{|a|}{1+|a|+|b|}+\frac{|b|}{1+|a|+|b|} \\
    & \leqslant \frac{|a|}{1+|a|}+\frac{|b|}{1+|b|} .
    \end{aligned}
    $$

  - 【例题：利用微分中值公式】设 $f(x)$ 在 $(0,+\infty)$ 上单调下降, 可微, 如果当 $x \in(0$, $+\infty)$ 时, $0<f(x)<\left|f^{\prime}(x)\right|$ 成立, 则当 $0<x<1$ 时, 必有 $x f(x)>\frac{1}{x} f\left(\frac{1}{x}\right)$. (北京大学)

    目标在于证明 $(0,1)$ 内$\frac{f\left(\frac{1}{x}\right)}{f(x)}<x^2 \text {, 或 } \ln \frac{f\left(\frac{1}{x}\right)}{f(x)}<\ln x^2=2 \ln x \text {. }$

    事实上, 因 $f \searrow, f^{\prime}<0$, 有 $f^{\prime}(x)=-\left|f^{\prime}(x)\right|$.
    $$
    \ln \frac{f\left(\frac{1}{x}\right)}{f(x)}=\ln f\left(\frac{1}{x}\right)-\ln f(x)=\frac{f^{\prime}(\xi)}{f(\xi)}\left(\frac{1}{x}-x\right),
    $$
    注意到 $0<f(x)<\left|f^{\prime}(x)\right|=-f^{\prime}(x), \frac{f^{\prime}(x)}{f(x)}<-1, \frac{1}{x}-x>0$ (当 $0<x<1$ 时), 再利用 (1) 题结果知上式 $<x-\frac{1}{x}<2 \ln x$. 证 毕.

  - 【例题：利用Taylor公式】上述已经给了算例。

  - 【例题：用求极值的方法证明】要点 要证明 $f(x) \geqslant g(x)$, 只要求函数
    $$
    F(x) \equiv f(x)-g(x)
    $$
    的极值, 证明 $\min F(x) \geqslant 0$.这是证明不等式的基本方法.





#### 期中试题讲解

三、设 $a_1=\sqrt{2}, a_2=\sqrt{2}^{\sqrt{2}}, a_3=\sqrt{2}^{\sqrt{2} \sqrt{2}}, a_{n+1}=\sqrt{2}^{a_n}(n=1,2,3, \ldots)$. 试问此数列当 $n \rightarrow+\infty$ 时是否有极限? 若有, 求之; 若无, 为何?

【需要注意的是单调上升有上界必有极限，但是如果直接

四、设 $g(x)$ 满足方程 $g^{\prime}(x)+g(x)=1+e^{-x}$, 试求 $g(x)$.

【讲解评分标准：求解一阶常微分方程过程；直接待定系数求解常系数偏微分方程，通解+特解】

五、设 $f(x)=x \ln x, x \in(0,+\infty)$, 试求出同时满足下面二条件的一组 $\xi_n$ :
(1). $\lim _{n \rightarrow+\infty}\left|\xi_n-e^n\right|=0$
(2). $\lim _{n \rightarrow+\infty}\left|f\left(\xi_n\right)-f\left(e^n\right)\right| \neq 0$

【注意必须要求第二项的极限是存在的，极限可以是无穷，需要证明】

