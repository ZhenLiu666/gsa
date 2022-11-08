《高等数学A》第九次习题课

> Author ZhenLiu
>
> 2022/11/01



> 微分中值定理建立了导数与函数值之间的联系, 使我们得以根据导数某些性质去推断函数值的性态; 
>
> 泰勒公式则告诉我们, 一个函数可以由一个多项式来近似替代;



#### 9.1 微分中值定理

- Fermat 引理: 设 $f(x)$ 在 $N\left(x_0, \delta\right)$ 内有定义, 且恒有 $f(x) \leq(\geq) f\left(x_0\right)$, 若其在 $x_0$ 点可导, 则 $f^{\prime}\left(x_0\right)=0$.

  - 【例题】证明 不妨设 $f(x) \leq f\left(x_0\right), \forall x \in N\left(x_0, \delta\right)$. 于是对任意 $h: 0<h<\delta$, 我们 有
    $$
    \begin{gathered}
    \frac{f\left(x_0+h\right)-f\left(x_0\right)}{h} \leq 0, \\
    \frac{f\left(x_0-h\right)-f\left(x_0\right)}{-h} \geq 0 .
    \end{gathered}
    $$
    从而当 $h \rightarrow 0^{+}$时, 既有 $f^{\prime}\left(x_0\right)=f_{+}^{\prime}\left(x_0\right) \leq 0$, 又有 $f^{\prime}\left(x_0\right)=f_{-}^{\prime}\left(x_0\right) \geq 0$. 故 $f^{\prime}\left(x_0\right)=0$

- Rolle 中值定理: 设 $f(x)$ 满足: 在 $[a, b]$ 上连续, 在 $(a, b)$ 内可微, 且 $f(a)=f(b)$, 则存在 $\xi \in(a, b)$, s.t. $f^{\prime}(\xi)=0$.

  - 【例题】设 $c_1, c_2, \cdots, c_n$ 为任意实数, 证明：函数 $f(x)=c_1 \cos x+c_2 \cos 2 x+\cdots+c_n \cos n x$ 在 $(0, \pi)$ 内必有根.（只需注意到其原函数在0和$\pi$处的函数值相同即可）

- Lagrange 中值定理: 设 $f(x)$ 满足: 在 $[a, b]$ 上连续, 在 $(a, b)$ 内可微, 则存在 $\xi \in(a, b)$, s.t. $f^{\prime}(\xi)=\frac{f(b)-f(a)}{b-a}$
  - 等价形式为: $f(b)-f(a)=f^{\prime}(a+\theta(b-a))(b-a), 0<\theta<1$. 

  - 推论 1 若 $f(x)$ 在区间 $I$ 上连续, 在 $I$ 内部满足 $f^{\prime}(x) \equiv 0$, 则 $f(x)$ 在 $I$ 上恒为常数. 

  - 【例题】 $3 \arccos x-\arccos \left(3 x-4 x^3\right)=\pi, x \in\left[-\frac{1}{2}, \frac{1}{2}\right]$.

    证明: 令 $f(x)=3 \arccos x-\arccos \left(3 x-4 x^3\right)$. 则
    $$
    \begin{aligned}
    f^{\prime}(x) &=-\frac{3}{\sqrt{1-x^2}}+\frac{3-12 x^2}{\sqrt{1-\left(3 x-4 x^3\right)^2}} \\
    &=-\frac{3}{\sqrt{1-x^2}}+\frac{3\left(1-4 x^2\right)}{\sqrt{\left(1-x^2\right)\left(1-4 x^2\right)^2}}=0, \quad x \in\left(-\frac{1}{2}, \frac{1}{2}\right) .
    \end{aligned}
    $$
    于是 $f(x)=C=f(0)=\pi, x \in\left(-\frac{1}{2}, \frac{1}{2}\right)$. 又因 $f(x)$ 在 $x=\frac{1}{2}$ 处左连续, 在 $x=-\frac{1}{2}$ 处 右连续, 故
    $$
    3 \arccos x-\arccos \left(3 x-4 x^3\right)=\pi, \quad x \in\left[-\frac{1}{2}, \frac{1}{2}\right] .
    $$

  - 推论 2 若 $f(x), g(x) \in C(I)$, 且 $f^{\prime}(x)=g^{\prime}(x), \forall x \in I$, 则必 $\exists$ 常数 $c$, s.t. $f(x)=g(x)+c$.

  - 推论3: 设 $y=f(x)$ 在 $[a, b]$ 上连续, 在 $(a, b)$ 上可导. 若 $f^{\prime}(x)>0(\geq 0), \quad \forall x \in(a, b)$,
    则函数 $f$ 在 $[a, b]$ 上严格递增 (递增); 若
    $$
    f^{\prime}(x)<0(\leqslant 0), \quad \forall x \in(a, b),
    $$
    则函数 $f$ 在 $[a, b]$ 上严格递减 (递减).

    注意：上述结论反之是不成立的。

  - 【思考】某个点处的函数导数大于0，是否能推出在其某个小邻域内单调递增？

- Cauchy 中值定理: 设 $f(x), g(x) \in C([a, b])$, 均在 $(a, b)$ 内可微, 且 $g^{\prime}(x) \neq 0, \forall x \in(a, b)$, 则 $\exists \xi \in(a, b)$, s.t. $\frac{f^{\prime}(\xi)}{g^{\prime}(\xi)}=\frac{f(b)-f(a)}{g(b)-g(a)}$.
  - 注 1 Cauchy 中值定理包含 Lagrange 中值定理, 当 $g(x)=x$ 时, 就是 Lagrange 中值定理.
    Lagrange 中值定理包含 Rolle定理, 当 $f(a)=f(b)$ 时, 就是 Rolle定理.
  - 注 2 中值定理只证明了 $\xi$ 的存在性, 并末指明 $\xi$ 是唯一的以及 $\xi$ 的确切位置.
  - 注 3 使用中值定理时, 一定要验证是否满足假设条件.

- Darboux 定理: 设 $f(x)$ 在区间 $[a, b]$ 上可导, 而 $\eta \in \mathbb{R}$ 介于 $f_{+}^{\prime}(a)$ 与 $f_{-}^{\prime}(b)$ 之间, 则必 $\exists \xi \in(a, b)$, s.t. $f^{\prime}(\xi)=\eta$.

  - 证明：先设 $f_{+}^{\prime}(a)>0, f_{-}^{\prime}(b)<0$, 往证存在 $\xi \in(a, b)$ 使得 $f^{\prime}(\xi)=0$. 因为
    $$
    \lim _{x \rightarrow a^{+}} \frac{f(x)-f(a)}{x-a}=f_{+}^{\prime}(a)>0,
    $$
    故有 $\delta>0$, 使当 $a<x<a+\delta$ 时, 就有$\frac{f(x)-f(a)}{x-a}>0,$因 $x-a>0$, 所以 $f(x)-f(a)>0$, 即当 $a<x<a+\delta$ 时, $f(x)>f(a)$, 从而 $f(a)$ 不是 $f(x)$ 在 $[a, b]$ 上的聂大值. 类似地可以证明, $f(b)$ 也不是 $f(x)$ 的最大 值. 又因 $f(x)$ 在 $[a, b]$ 上可导, 当然连续, 故 $f(x)$ 必在某点 $\xi \in(a, b)$ 取得最大 值. 由 Fermat 引理知 $f^{\prime}(\xi)=0$.回到一般情形, 不妨设 $f_{-}^{\prime}(b)<\eta<f_{+}^{\prime}(a)$, 令$F(x)=f(x)-\eta x .$于是 $F(x)$ 在 $[a, b]$ 上可导, 且 $F_{+}^{\prime}(a)=f_{+}^{\prime}(a)-\eta>0, F_{-}^{\prime}(b)=f_{-}^{\prime}(b)-\eta<0$. 由 前段证明知存在 $\xi \in(a, b)$, 使得 $F^{\prime}(\xi)=0$. 这表明 $f^{\prime}(\xi)-\eta=F^{\prime}(\xi)=0$, 即有 $f^{\prime}(\xi)=\eta$.
    注意, 这个定理不能用连续函数的介值定理来证明, 因为定理中并末假设 $f^{\prime}(x)$ 连续.

- 【例题】函数 $f(x) \in C[0,1]$ 在 $(0,1)$ 内可导, 且满足 $f(0)=f(1)=0$, 证明: $\exists \xi \in(0,1)$, s.t $f(\xi)=f^{\prime}(\xi)$.
  证明: 令 $F(x)=e^{-x} f(x)$, 故 $F(0)=F(1)=0$, 由 Rolle 定理可知 $\exists \xi \in(0,1)$, s.t $F^{\prime}(\xi)=0$. 即 $-e^{-\xi} f(\xi)+e^{-\xi} f^{\prime}(\xi)=0$, 进而有 $f(\xi)=f^{\prime}(\xi)$.

- 【例题】设函数 $f(x) \in C\left[\frac{1}{2}, 1\right]$, 在 $\left(\frac{1}{2}, 1\right)$ 内可导, 且满足 $f\left(\frac{1}{2}\right)=f(1)=0$, 证明: $\exists \xi \in$ $\left(\frac{1}{2}, 1\right)$, s.t. $3 f(\xi)=-\xi f^{\prime}(\xi)$. (令 $F(x)=x^3 f(x)$, 利用 Rolle 中值定理)

- 【例题】设 $f(x), g(x), h(x) \in C[a, b]$ 是 $(a, b)$ 内可微的函数. 证明必存在 $\xi \in(a, b)$, 使得

- $$
  \left|\begin{array}{ccc}
  f(a) & g(a) & h(a) \\
  f(b) & g(b) & h(b) \\
  f^{\prime}(\xi) & g^{\prime}(\xi) & h^{\prime}(\xi)
  \end{array}\right|=0
  $$
  并用这个结论导出 Lagrange 中值定理和 Cauchy 中值定理.
  证明: 令 $F(x)=\left|\begin{array}{lll}f(a) & g(a) & h(a) \\ f(b) & g(b) & h(b) \\ f(x) & g(x) & h(x)\end{array}\right|$, 易得 $F^{\prime}(x)=\left|\begin{array}{ccc}f(a) & g(a) & h(a) \\ f(b) & g(b) & h(b) \\ f^{\prime}(x) & g^{\prime}(x) & h^{\prime}(x)\end{array}\right|$. 对 $F(x)$ 在 $[a, b]$ 上应用 Rolle 定理即可得结论. 进一步, 若令 $h(x) \equiv 1$ 可得 Cauchy 中 值定理, 若令 $h(x) \equiv 1, g(x)=x$ 可得 Lagrange 中值定理.

- 【例题】设函数 $f(x)$ 在 $[a, b]$ 上可积, $F(x)$ 是 $f(x)$ 在 $[a, b]$ 上的一个原 函数, 则
  $$
  \int_a^b f(x) \mathrm{d} x=F(b)-F(a) .
  $$
  证明 设 $T=\left\{x_k\right\}_{0 \leq k \leq n}$ 是 $[a, b]$ 的任意分划. 对 $F(x)$ 在 $\left[x_{k-1}, x_k\right](k=$ $1,2, \cdots, n)$ 上应用 Lagrange 中值定理, 即得 $\xi_k \in\left(x_{k-1}, x_k\right)$ 满足
  $$
  \begin{aligned}
  & F(b)-F(a)=F\left(x_n\right)-F\left(x_0\right)=\sum_{k=1}^n\left[F\left(x_k\right)-F\left(x_{k-1}\right)\right] \\
  =& \sum_{k=1}^n F^{\prime}\left(\xi_k\right) \Delta x_k=\sum_{k=1}^n f\left(\xi_k\right) \Delta x_k .
  \end{aligned}
  $$
  因为 $f(x)$ 在 $[a, b]$ 上可积, 故对上式取极限, 即得
  $$
  F(b)-F(a)=\lim _{\|T\| \rightarrow 0} \sum_{k=1}^n f\left(\xi_k\right) \Delta x_k=\int_a^b f(x) \mathrm{d} x .
  $$

- 【例题】设函数 $f(x) \in C[a, b]$, 在 $(a, b)$ 内二阶可导, $f(a)=f(b)=0$, 且 $\exists c \in(a, b)$, s.t. $f(c)>0$. 证明 $\exists \xi \in(a, b)$, s.t. $f^{\prime \prime}(\xi)<0$.
  证明: 由题设可知, $f(x)$ 在闭区间 $[a, c],[c, b]$ 上均满足 Lagrange 中值定理的条件, 所以存在 $\xi_1 \in(a, c), \xi_2 \in(c, b)$, 使得
  $$
  \begin{gathered}
  f^{\prime}\left(\xi_1\right)=\frac{f(c)-f(a)}{c-a}=\frac{f(c)}{c-a}>0, \quad a<\xi_1<c \\
  f^{\prime}\left(\xi_2\right)=\frac{f(b)-f(c)}{b-c}=-\frac{f(c)}{b-c}<0, \quad c<\xi_2<b .
  \end{gathered}
  $$
  又知 $f(x)$ 二阶可导, 故 $f^{\prime}(x)$ 在 $\left[\xi_1, \xi_2\right]$ 上连续, 在 $\left(\xi_1, \xi_2\right)$​ 内可导, 由 Lagrange 中值定理可知, 存在 $\xi \in\left(\xi_1, \xi_2\right) \subset(a, b)$, 使得
  $$
  f^{\prime \prime}(\xi)=\frac{f^{\prime}\left(\xi_2\right)-f^{\prime}\left(\xi_1\right)}{\xi_2-\xi_1}<0 .
  $$

- 【例题】设函数 $f(x) \in C[a, b]$, 在 $(a, b)$ 内可导 $(0 \leq a<b)$, 且 $f(a) \neq f(b)$, 证明 $\exists \xi, \eta$, s.t. $\frac{f^{\prime}(\eta)}{2 \eta}=\frac{f^{\prime}(\xi)}{b+a}$.
  证明: 令 $g(x)=x^2, x \in[a, b]$, 那么 $g(x)$ 在 $[a, b]$ 上连续, 在 $(a, b)$ 内可导, 且 $g^{\prime}(x)=2 x \neq 0$. 由 Cauchy 中值定理知 $\exists \eta \in(a, b)$, 使
  $$
  \frac{f(b)-f(a)}{b^2-a^2}=\frac{f^{\prime}(\eta)}{g^{\prime}(\eta)}=\frac{f^{\prime}(\eta)}{2 \eta} .
  $$
  又由 Lagrange 中值定理, $\exists \xi \in(a, b)$, 使 $f(b)-f(a)=f^{\prime}(\xi)(b-a)$, 故有
  $$
  \frac{f^{\prime}(\eta)}{2 \eta}=\frac{f^{\prime}(\xi)}{b+a}
  $$





#### 9.2 洛必达法则

-  $\frac{0}{0}$ 型: 设 $f(x), g(x)$ 均在 $\omega$ 的某个邻域内可微, 且 $g^{\prime}(x) \neq 0$. 若 $\lim _{x \rightarrow \omega} f(x)=\lim _{x \rightarrow \omega} g(x)=0$, $\lim _{x \rightarrow \omega} \frac{f^{\prime}(x)}{g^{\prime}(x)}$ 存在(或为无穷), 则必有 $\lim _{x \rightarrow \omega} \frac{f(x)}{g(x)}$ 存在(或为无穷), 且 $\lim _{x \rightarrow \omega} \frac{f(x)}{g(x)}=\lim _{x \rightarrow \omega} \frac{f^{\prime}(x)}{g^{\prime}(x)}$.

-  $\frac{\infty}{\infty}$ 型: 设 $f(x), g(x)$ 均在 $\omega$ 的某个邻域内可微, 且 $g^{\prime}(x) \neq 0$. 若 $\lim _{x \rightarrow \omega} g(x)=\infty$, $\lim _{x \rightarrow \omega} \frac{f^{\prime}(x)}{g^{\prime}(x)}$ 存在(或为无穷), 则必有 $\lim _{x \rightarrow \omega} \frac{f(x)}{g(x)}$ 存在(或为无穷), 且 $\lim _{x \rightarrow \omega} \frac{f(x)}{g(x)}=\lim _{x \rightarrow \omega} \frac{f^{\prime}(x)}{g^{\prime}(x)}$. 

  - 注 1: $\omega$ 的邻域有 6 种, 极限存在(或为无穷) 有 4 种, 每个类型包括 24 种.
  - 注 2 L'Hospital 法则只适合 $\frac{0}{0}$ 和 $\frac{\infty}{\infty}$ 型. $1^{\infty}, \infty^0, 0^0$ 型可通过对数变换化为 $\frac{0}{0}$ 和 $\frac{\infty}{\infty}$ 型.

- 在应用 L'Hospital 法则求待定型时, 应注意以下几点:
  (1) 只有 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 型待定式才能用 L'Hospital 法则, 否则会得到荒谬的结果. 例如
  $$
  \lim _{x \rightarrow 0} \frac{\sin x}{1+x}=0 .
  $$
  但如果用 L'Hospital 法则, 则将导致
  $$
  \lim _{x \rightarrow 0} \frac{\sin x}{1+x}=\lim _{x \rightarrow 0} \cos x=1 .
  $$
  所以我们以后在使用 L'Hosipital 法则求极限前, 一定要检验待求极限是否为 $\frac{0}{0}$ 型或 $\frac{\infty}{\infty}$ 型.
  (2) $\lim \frac{f^{\prime}(x)}{g^{\prime}(x)}$ 不存在, 并不能断言 $\lim \frac{f(x)}{g(x)}$ 不存在. 例如
  $$
  \lim _{x \rightarrow \infty} \frac{x+\sin x}{x}=1,
  $$
  但极限
  $$
  \lim _{x \rightarrow \infty} \frac{1+\cos x}{1}
  $$
  不存在.
  (3) 为了简化计算, 在每次使用 L'Hospital 法则之前, 应尽可能提出极限非零的因子. 例如, 为求 $\frac{0}{0}$ 型待定式极限 $\lim _{x \rightarrow 0} \frac{x^{100}\left(\mathrm{e}^x-1\right)}{(2+x) \sin ^{101} x}$, 如果立即直接用 L'Hospital 法则将导致非常籘复的计算. 但若这样去做:
  $$
  \begin{aligned}
  \lim _{x \rightarrow 0} \frac{x^{100}\left(\mathrm{e}^x-1\right)}{(2+x) \sin ^{101} x} &=\lim _{x \rightarrow 0} \frac{1}{2+x} \cdot \lim _{x \rightarrow 0}\left(\frac{x}{\sin x}\right)^{100} \cdot \lim _{x \rightarrow 0} \frac{\mathrm{e}^x-1}{\sin x} \\
  &=\frac{1}{2} \lim _{x \rightarrow 0} \frac{\mathrm{e}^x-1}{\sin x}=\frac{1}{2} \lim _{x \rightarrow 0} \frac{\mathrm{e}^x}{\cos x}=\frac{1}{2},
  \end{aligned}
  $$
  当收事半功倍之效.
  (4) 在处理 $0 . \infty$ 型待定式时, 谁作分子, 谁作分母是有讲究的. 例如
  $$
  \lim _{x \rightarrow+\infty} x \mathrm{e}^{-x}=\lim _{x \rightarrow+\infty} \frac{x}{\mathrm{e}^x}=\lim _{x \rightarrow+\infty} \frac{1}{\mathrm{e}^x}=0 .
  $$
  但如果像下面这样做:
  $$
  \lim _{x \rightarrow+\infty} x \mathrm{e}^{-x}=\lim _{x \rightarrow+\infty} \frac{\mathrm{e}^{-x}}{1 / x}=\lim _{x \rightarrow+\infty} \frac{-\mathrm{e}^{-x}}{-1 / x^2}=\cdots
  $$
  就会越来越复杂.

- 【例题】利用 L'Hospital 法则求下列极限
  (1) $\lim _{x \rightarrow 0} \frac{\tan x-x}{x-\sin x}=2$;
  (2) $\lim _{x \longrightarrow 0} \frac{x \cot x-1}{x^2}=-\frac{1}{3}$;
  (3) $\lim _{x \rightarrow 0}\left(\frac{1}{x}-\frac{1}{\mathrm{e}^x-1}\right)=\frac{1}{2}$;
  (4) $\lim _{x \longrightarrow 1}\left(\frac{1}{\ln x}-\frac{1}{x-1}\right)=\frac{1}{2}$.

3. 【例题】设 $f(x)$ 二阶可导, 求证

$$
\lim _{h \longrightarrow 0} \frac{f(x+2 h)-2 f(x+h)+f(x)}{h^2}=f^{\prime \prime}(x) .
$$
证明: 只能用定义, 不能用 L'Hospital 法则, 因为没有说二阶导数具有连续性.因此需要先使用一次洛必达法则，再使用导数的定义去证明上述极限存在。

- 【例题】求 $\lim _{x \rightarrow 0} \frac{\int_0^x \cos t^2 \mathrm{~d} t}{x}$
  由于 由于
  $$
  0 \leq\left|\int_0^x \cos t^2 \mathrm{~d} t\right| \leq|x| \rightarrow 0 \quad(x \rightarrow 0)
  $$
  且
  $$
  \left(\int_0^x \cos t^2 \mathrm{~d} t\right)^{\prime}=\cos x^2
  $$
  所以, 由 L'Hospital 法则有
  $$
  \lim _{x \rightarrow 0} \frac{\int_0^x \cos t^2 \mathrm{~d} t}{x}=\lim _{x \rightarrow 0} \frac{\cos x^2}{1}=1 .
  $$

- 【例题】求 $\lim _{x \rightarrow+\infty}\left(\frac{2}{\pi} \arctan x\right)^x$.
  这是 $1^{\infty}$ 㺫待定式. 由于
  $$
  \left(\frac{2}{\pi} \arctan x\right)^x=\mathrm{e}^{\ln \left(\frac{2}{\pi} \arctan x\right)^\pi}
  $$
  $$
  \ln \left(\frac{2}{\pi} \arctan x\right)^x=x \ln \left(\frac{2}{\pi} \arctan x\right)=\frac{\ln \left(\frac{2}{\pi} \arctan x\right)}{1 / x}
  $$

故问题转化为处理 $\frac{0}{0}$ 型待定式. 由 L'Hospital 法则,
$$
\lim _{x \rightarrow+\infty} \frac{\ln \left(\frac{2}{\pi} \arctan x\right)}{1 / x}=\lim _{x \rightarrow+\infty} \frac{\frac{1}{\left(1+x^2\right) \arctan x}}{-1 / x^2}=-\frac{2}{\pi} .
$$
从而
$$
\lim _{x \rightarrow+\infty}\left(\frac{2}{\pi} \arctan x\right)^x=\lim _{x \rightarrow+\infty} \mathrm{e}^{x \ln \left(\frac{2}{\pi} \arctan x\right)}=e^{-2 / \pi}
$$



#### 9.3 期中测试

 一、(本题 10 分) 简要回答下面的问题, 说明理由:
1. 有理数的有理数次幂一定是有理数吗?

2. 无理数的无理数次幂一定是无理数吗? 可考察 $\sqrt{2}^{\sqrt{2}}$ 和 $\left(\sqrt{2}^{\sqrt{2}}\right)^{\sqrt{2}}$ 来 支持你的结论。

  二、 (本题 15 分) 求下面的极限

3. $\lim _{x \rightarrow+\infty} \frac{\sqrt{x+2 \sqrt{x+3 \sqrt{x}}}}{\sqrt{x+4}}$.

4. $\lim _{x \rightarrow 1}\left(\frac{1}{x-1}-\frac{2}{x^2-1}+\frac{3}{x^3-1}-\frac{4}{x^4-1}\right)$.

5. $\lim _{n \rightarrow+\infty}(2021 \sqrt{n+2021}+2023 \sqrt{n+2023}-2 \cdot 2022 \sqrt{n+2022})$.

三、设 $a_1=\sqrt{2}, a_2=\sqrt{2}^{\sqrt{2}}, a_3=\sqrt{2}^{\sqrt{2} \sqrt{2}}, a_{n+1}=\sqrt{2}^{a_n}(n=1,2,3, \ldots)$. 试问此数列当 $n \rightarrow+\infty$ 时是否有极限? 若有, 求之; 若无, 为何?

四、设 $g(x)$ 满足方程 $g^{\prime}(x)+g(x)=1+e^{-x}$, 试求 $g(x)$.

五、设 $f(x)=x \ln x, x \in(0,+\infty)$, 试求出同时满足下面二条件的一组 $\xi_n$ :
(1). $\lim _{n \rightarrow+\infty}\left|\xi_n-e^n\right|=0$
(2). $\lim _{n \rightarrow+\infty}\left|f\left(\xi_n\right)-f\left(e^n\right)\right| \neq 0$

