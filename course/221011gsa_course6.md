《高等数学A》第六次习题课

> Author ZhenLiu
>
> 2022/10/11



#### 课前小测

- 【题目1】设 $a_1=1, a_{n+1}=a_n+\frac{1}{a_n}$ ，
  (a). 证明: $\lim _{n \rightarrow \infty} \frac{a_n}{\sqrt{n}}=\sqrt{2} ;$ (5 分)
  (b). 计算: $\lim _{n \rightarrow \infty} \frac{\sqrt{n}\left(a_n-\sqrt{2 n}\right)}{\ln (n)}$. (5 分)
  证明: (a) 显然有 $\lim _{n \rightarrow \infty} a_n=+\infty$. 因此由 Stolz 定理就有
  $$
  \lim _{n \rightarrow \infty} \frac{a_n^2}{n}=\lim _{n \rightarrow \infty} \frac{a_n^2-a_{n-1}^2}{n-(n-1)}=\lim _{n \rightarrow \infty}\left(2+\frac{1}{a_{n-1}^2}\right)=2
  $$
  所以 $\lim _{n \rightarrow \infty} \frac{a_n}{\sqrt{n}}=\sqrt{2}$.
  (b)
  $$
  \begin{aligned}
  \lim _{n \rightarrow \infty} \frac{\sqrt{n}\left(a_n-\sqrt{2 n}\right)}{\ln (n)} &=\lim _{n \rightarrow \infty} \frac{\sqrt{n}}{a_n+\sqrt{2 n}} \lim _{n \rightarrow \infty} \frac{a_n^2-2 n}{\ln (n)} \\
  &=\frac{1}{2 \sqrt{2}} \lim _{n \rightarrow \infty} \frac{\left(a_n^2-2 n\right)-\left(a_{n-1}^2-2(n-1)\right)}{\ln (n)-\ln (n-1)} \\
  &=\frac{1}{2 \sqrt{2}} \lim _{n \rightarrow \infty} \frac{2+\frac{1}{a_{n-1}^2}-2}{\frac{1}{n}} \\
  &=\frac{\sqrt{2}}{8}
  \end{aligned}
  $$

- 【题目2】计算$\lim _{n \rightarrow \infty}\left(1+\frac{1}{n^3}\right)\left(1+\frac{4}{n^3}\right) \cdots\left(1+\frac{n^2}{n^3}\right)$

  解:只需注意上式是$p=2$的 令: $a_n=\ln \left[\left(1+\frac{1^p}{n^{p+1}}\right)\left(1+\frac{2^p}{n^{p+1}}\right) \cdots\left(1+\frac{n^p}{n^{p+1}}\right)\right]$, 注意到:
  $$
  \frac{k}{n+k}<\ln \left(1+\frac{k}{n}\right)<\frac{k}{n}
  $$
  就有:
  $$
  \begin{aligned}
  \sum_{k=1}^n \frac{k^p}{n^{p+1}+n^p} &<\sum_{k=1}^n \frac{k^p}{n^{p+1}+k^p} \\
  &<\sum_{k=1}^n \ln \left(1+\frac{k^p}{n^{p+1}}\right) \\
  &<\sum_{k=1}^n \frac{k^p}{n^{p+1}}
  \end{aligned}
  $$
  这样 $\lim _{n \rightarrow \infty} a_n=\frac{1}{p+1}$.

- 【题目3】设函数 $f(x)$ 在点 $x=0$ 处连续, 而且 $\lim _{x \rightarrow 0} \frac{f(2 x)-f(x)}{x}=m$, 求证 $f^{\prime}(0)=m$; 

  任对 $\varepsilon>0$, 存在 $\delta>0$, 当 $0 \leqslant|x|<\delta$ 时, 有:
  $$
  m-\varepsilon<\frac{f(2 x)-f(x)}{x}<m+\varepsilon
  $$
  注意 $0<\left|\frac{x}{2^n}\right|<\delta$, 有:
  $$
  \frac{1}{2^n}(m-\varepsilon)<\frac{f\left(\frac{x}{2^{n-1}}\right)-f\left(\frac{x}{2^n}\right)}{x}<\frac{1}{2^n}(m+\varepsilon)
  $$
  关于 $n$ 求和,
  $$
  \left(1-\frac{1}{2^n}\right)(m-\varepsilon)<\frac{f(x)-f\left(\frac{x}{2^n}\right)}{x}<\left(1-\frac{1}{2^n}\right)(m+\varepsilon)
  $$
  令 $n \rightarrow+\infty$, 有:
  $$
  m-\varepsilon \leqslant \frac{f(x)-f(0)}{x} \leqslant m+\varepsilon
  $$





#### 6.1  不定积分

- 原函数

  - 定义
  - 存在定理：连续函数一定有原函数；

- 性质：

  - 不唯一性：如果 $F(x)$ 和 $\Phi(x)$ 为函数 $f(x)$ 在区间 $I$ 上的两个原函数, 那么 $\Phi(x)=F(x)+C$, 其中 $C$ 为常数.
  - "互逆"性质：
    - 由不定积分和原函数的定义还可知道, 若 $f(x)$ 有原函数, 则$\left(\int f(x) \mathrm{d} x\right)^{\prime}=f(x) \text { 或 } \mathrm{d} \int f(x) \mathrm{d} x=f(x) \mathrm{d} x ；$
    - 若 $f(x)$ 可导, 则$\int f^{\prime}(x) \mathrm{d} x=f(x)+C \text { 或 } \int \mathrm{d} f(x)=f(x)+C .$

  - 线性性质:
    - 设函数 $f(x)$ 和 $g(x)$ 邦在某区间上有原函数, $\lambda$ 和 $\mu$ 为两个不全 为零的常数, 则函数 $\lambda f(x)+\mu g(x)$ 也在该区间上有原函数, 且 $\int[\lambda f(x)+\mu g(x)] \mathrm{d} x=\lambda \int f(x) \mathrm{d} x+\mu \int g(x) \mathrm{d} x$.

- 【例题】求不定积分 $\int \cos ^2 \frac{x}{2} \mathrm{~d} x$.
  由线性性质,
  $$
  \begin{aligned}
  & \int \cos ^2 \frac{x}{2} \mathrm{~d} x=\int \frac{1}{2}(1+\cos x) \mathrm{d} x \\
  =& \frac{1}{2} \int 1 \mathrm{~d} x+\frac{1}{2} \int \cos x \mathrm{~d} x \\
  =& \frac{1}{2}(x+\sin x)+C .
  \end{aligned}
  $$

- 

- 【例题】求不定积分 $\int \frac{\mathrm{d} x}{\sin ^2 x \cos ^2 x}$.
  由线性性质,
  $$
  \begin{aligned}
  & \int \frac{\mathrm{d} x}{\sin ^2 x \cos ^2 x}=\int \frac{\sin ^2 x+\cos ^2 x}{\sin ^2 x \cos ^2 x} \mathrm{~d} x \\
  =& \int\left(\frac{1}{\cos ^2 x}+\frac{1}{\sin ^2 x}\right) \mathrm{d} x=\tan x-\cot x+C .
  \end{aligned}
  $$



#### 6.2  定积分定义

- 定义：设函数 $f(x)$ 在区间 $[a, b]$ 上有定义. 如最对子 $[a, b]$ 的任五分划 $T$ 和任音取定的介点组 $\left\{\xi_k\right\}$, 当 $\|T\| \rightarrow 0$ 时, $f(x)$ 之与 $T$ 和 $\left\{\xi_k\right\}$ 相应的积分和 $\sum_{k=1}^n f\left(\xi_k\right) \Delta x_k$ 有极限, 则我们就说 $f(x)$ 在 $[a, b]$ 上可积, 并驰该极限称为 $f(x)$ 在 $[a, b]$ 上的定积分或积分值, 记为 $\int_a^b f(x) \mathrm{d} x$, 即
  $$
  \int_a^b f(x) \mathrm{d} x=\lim _{\|T\| \rightarrow 0} \sum_{k=1}^n f\left(\xi_k\right) \Delta x_k,
  $$
  其中 $f(x)$ 称为被积函数, $x$ 称为积分变罡, $a$ 和 $b$ 分别称为定积分的下限和上 限, 衣示积分变量的变化范围.

  - 另一种表述：对于一个定数 $I, \lim _{\|T\| \rightarrow 0} \sum_{k=1}^n f\left(\xi_k\right) \Delta x_k=I$ 的确切含义是, 对于任给的 $\varepsilon>0$, 存在 $\delta>0$, 不论分划 $T$ 的分点 $\left\{x_k\right\}$ 和介点组 $\left\{\xi_k\right\}$ 如何选取, 只要 $\|T\|<\delta$, 便 有 $\left|\sum_{k=1}^n f\left(\xi_k\right) \Delta x_k-I\right|<\varepsilon$.

- 定义得到的简单性质：

  - 有限点值不影响积分值，并且不影响可积性；

  - 从定积分的定义可以看出, 定积分的值只与被积函数和积分上下限有关, 而与积分变量无关, 即有$\int_a^b f(x) \mathrm{d} x=\int_a^b f(t) \mathrm{d} t .$因此, 在进行运算或论证时, 可随时根据需要而改换积分变量.

  - 从定义还可看出, 对于任意常数 $C$,$\int_a^b C \mathrm{~d} x=C(b-a) .$

  - 在定义中我们假定 $a<b$, 即下限小于上限. 为了以后书写和运算的方便, 我 们规定
    $$
    \begin{gathered}
    \int_a^a f(x) \mathrm{d} x=0 . \\
    \int_a^b f(x) \mathrm{d} x=-\int_b^a f(x) \mathrm{d} x, \text { 若 } a>b .
    \end{gathered}
    $$

- 【例题】
  - 求序列极限$\lim _{n \rightarrow \infty} \sum_{i=1}^n \frac{\sqrt{i}}{n \sqrt{n}} .$
  -  求序列极限$\lim _{n \rightarrow \infty} \sum_{i=1}^n \frac{\sqrt{i}}{n \sqrt{n}} \cos \left(\frac{\sqrt{i}}{n} \sin (n)\right) \text {. }$

（见板书：第一问化简成积分的定义，第二问利用放缩$1\leq i \leq n$，再分别求极限即可）





#### 6.3  定积分可积性

- **必要条件**： $[a, b]$ 上的可积函数是有界的.事实上有界函数未必可积.例. 狄利克雷函数在 $[0,1]$ 上不可积.

- 【拓展】Darboux 和：设函数 $f(x)$ 在区间 $[a, b]$ 上有界, 分划 $T$ 把 $[a, b]$ 分成 $n$ 个小区间 $\left[x_{k-1}, x_k\right]$, $k=1,2, \cdots, n$. 本节以下, 我们总用 $m_k, M_k$ 表示 $f(x)$ 在区间 $\left[x_{k-1}, x_k\right]$ 上的下 确界与上确界, 令 $\Delta x_k=x_k-x_{k-1}$, 然后作和数
  $$
  s(T)=\sum_{k=1}^n m_k \Delta x_k, \quad S(T)=\sum_{k=1}^n M_k \Delta x_k,
  $$
  并分别称之为函数 $f(x)$ 之与分划 $T$ 相应的 Darboux 小和与 Darboux 大和,统称为 Darboux 和. 易见, 对于同一分划 $T$, 有$s(T) \leq \sum_{k=1}^n f\left(\xi_k\right) \Delta x_k \leq S(T) .$

  - 【例题】当在分划 $T$ 中加入新的分点时, 大和不增而小和不减, 当把加入新的分点后的分划记为 $T^{\prime}$ 时, 总有 $s(T) \leq s\left(T^{\prime}\right) \leq S\left(T^{\prime}\right) \leq S(T)$.
    证明：设分划 $T$ 为$a=x_0<x_1<x_2<\cdots<x_n=b .$不妨设分划 $T^{\prime}$ 是由分划 $T$ 添加 1 个分点 $x^{\prime} \in\left(x_{j-1}, x_j\right)$ 而成. 令 $M_{j 1}, M_{j 2}$ 分 别表示 $f(x)$ 在 $\left[x_{j-1}, x^{\prime}\right],\left[x^{\prime}, x_j\right]$ 上的上确界.于是有 $M_{j 1} \leq M_j, M_{j 2} \leq M_j$, 从而$M_{j 1}\left(x^{\prime}-x_{j-1}\right)+M_{j 2}\left(x_j-x^{\prime}\right) \leq M_j \Delta x_j .$由于 $S(T)$ 与 $S\left(T^{\prime}\right)$ 中的其余各项对应相同, 故得$S\left(T^{\prime}\right) \leq S(T) .$
  - 【例题】设 $T_1$ 和 $T_2$ 是 $[a, b]$ 的任意两个分划, 则有 $s\left(T_1\right) \leq S\left(T_2\right)$. 
    证明：令 $T=T_1 \cup T_2$, 即 $T_1$ 和 $T_2$ 的分点合并构成 $T$ 的全部分点. 于是, 分划 $T$ 既可看作由 $T_1$ 添加分点而成, 又可看作由 $T_2$ 添加分点而成. 此表明, 一切小和的集合 $\{s(T)\}$ 有上界, 从而必有上确界, 记为 $\underline{I}$; 一切大和的集合 $\{S(T)\}$ 有下界, 从而必有下确界, 记为 $\bar{I}$. 显然有 $I \leq \bar{I} . \underline{I}$ 和 $\bar{I}$ 分别称为 $f(x)$ 在区间 $[a, b]$ 上的下积分与上积分.

- 【充要条件】 【例题】有界函数 $f(x)$ 在区间 $[a, b]$ 上可积的充分必要条件是 $\lim _{\|T\| \rightarrow 0}(S(T)-s(T))=0$, 即对任何 $\varepsilon>0$, 那存在 $\delta>0$, 使当 $\|T\|<\delta$ 时, 就有$0 \leq S(T)-s(T)<\varepsilon$；

- 【拓展】对于区间 $[a, b]$ 上的任一分划 $T=\left\{x_k\right\}_{0 \leq k \leq n}$, 我们令 $\omega_k=M_k-m_k$, 并称 之为 $f(x)$ 在区间 $\left[x_{k-1}, x_k\right]$ 上的振幅. 容易验证，有如下表达式：$\omega_k=\sup _{x_1, x_2 \in\left[x_{k-1}, x_k\right]}\left|f\left(x_1\right)-f\left(x_2\right)\right| .$

- 【充要条件】有界函数 $f(x)$ 在区间 $[a, b]$ 上可积的充分必要条件是$\lim _{\|T\| \rightarrow 0} \sum_{k=1}^n \omega_k \Delta x_k=0 .$

- 结论：

  - 【例题】定理： 任何闭区间 $[a, b]$ 上的单调函数都是可积的.
  - 【例题】定理： 任何闭区间 $[a, b]$ 上的连续函数都是可积的.
  - 【例题】定理： 设函数 $f(x)$ 在 $(a, b)$ 内连续, 在 $[a, b]$ 上有界, 则它必在 $[a, b]$ 上可积.

- 【例题】讨论下列函数在 $[0,1]$ 上的可积性。
  (1) $f(x)=\left\{\begin{array}{ll}\frac{1}{x}-\left[\frac{1}{x}\right], & x \neq 0, \\ 0, & x=0 ;\end{array} \quad(2) f(x)= \begin{cases}0, & x \text { 为有理数, } \\ x, & x \text { 为无理数; }\end{cases}\right.$
  (3) $f(x)= \begin{cases}\operatorname{sgn}\left(\sin \frac{\pi}{x}\right), & x \neq 0 \\ 0, & x=0\end{cases}$

  (1)可积 // （2）不可积  // （3）可积

- 【例题】求证 Riemann 函数 $R(x)$ 在 $[0,1]$ 上可积.
  证明：设 $T$ 是 $[0,1]$ 上的任一分划, $\left\{\xi_k\right\}$ 是对应于分划 $T$ 的任意取定的介点组. 作积分和$\sum_{k=1}^n R\left(\xi_k\right) \Delta x_k .$对任给 $\varepsilon>0$, 总有正整数 $N$ 使 $\frac{1}{N}<\frac{\varepsilon}{2}$. 注意在 $[0,1]$ 内满足 $q<N$ 的有理点 $x=\frac{p}{q}$ 只有有限个, 不妨设为 $K_N$ 个. 若 $R\left(\xi_k\right) \geq \frac{\varepsilon}{2}$, 则 $\xi_k$ 必为有理点 $\frac{p}{q}$, 而 $R\left(\xi_k\right)=\frac{1}{q}$. 因此, $\frac{1}{q} \geq \frac{\varepsilon}{2}>\frac{1}{N}$, 从而 $q<N$. 故在积分和 $\sum_{k=1}^n R\left(\xi_k\right) \Delta x_k$ 中使 $R\left(\xi_k\right) \geq \frac{\varepsilon}{2}$ 的 $\xi_k$ 至多有 $K_N$ 个. 再注意到 $R(x) \leq 1, x \in[0,1]$. 取 $\delta=\frac{\varepsilon}{2 K_N}>0$, 则当 $\|T\|<\delta$ 时, 便有

$$
\begin{aligned}
&\left|\sum_{k=1}^n R\left(\xi_k\right) \Delta x_k-0\right|=\sum_{k=1}^n R\left(\xi_k\right) \Delta x_k \\
=& \sum_{q<N} R\left(\xi_k\right) \Delta x_k+\sum_{q \geq N} R\left(\xi_k\right) \Delta x_k \\
\leq & K_N\|T\|+\frac{\varepsilon}{2} \sum_{k=1}^n \Delta x_k<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon .
\end{aligned}
$$
- 【例题】证明函数 $f(x)=\left\{\begin{array}{ll}\sin \frac{1}{x}, & x \neq 0, \\ 0, & x=0\end{array}\right.$ 在任何区间 $[a, b]$ 上可积.
  证明 当 $0 \notin[a, b]$ 时, $f(x)$ 在 $[a, b]$ 上连续, 从而 $f(x) \in R[a, b]$; 当 $0 \in[a, b]$ 时, $f(x)$ 在 $[a, b]$ 上有界, 且只有一个间断点 $x_0=0$, 因此知 $f(x) \in R[a, b]$.

- 【例题】设函数 $f(x)$ 在 $[a, b]$ 上可积, 则 $f(x)$ 在 $(a, b)$ 内至少有一个连续点.

  证明: 由于 $f(x)$ 在 $[a, b]$ 可积, 故 $\forall \varepsilon>0$, 有分划 $T$, 使 $\sum_i w_i \Delta x_i<\varepsilon$.取 $\varepsilon=b-a$, 则有某个子区间 $\left[x_i, x_{i+1}\right]$, 在其上 $w_1(f)<1$. 再在 $\left(x_i, x_{i+1}\right)$ 内取一子区间 $\left[a_1, b_1\right]$, 使 $b_1-a_1<1$. 这时 $w_{\left[a_1, b_1\right]} \leq w_1(f)<1$.$f(x)$ 在 $\left[a_1, b_1\right]$ 上仍然可积, 故同样可选 $\left[a_2, b_2\right] \subset\left(a_1, b_1\right)$, 使得 $b_2-a_2<\frac{1}{2}, w_{\left[a_2, b_2\right]}<\frac{1}{2}, \cdots$. 如此下去, 可取 $\left\{\left[a_n, b_n\right]\right\}$, 满足 $\left[a_n, b_n\right] \subset\left(a_{n-1}, b_{n-1}\right), b_n-a_n<\frac{1}{n}$ 且 $w_{\left[a_n, b_n\right]}<\frac{1}{n}$. 由闭区间套 定理, 必存在唯一的 $c \in\left[a_n, b_n\right](n=1,2, \cdots)$ (实际上由作法知 $\left.a_n<c<b_n\right)$. 由 $w_{\left[a_n, b_n\right]} \rightarrow 0$ 即 知 $f(x)$ 在 $c$ 连续.

- 【例题】设 $f(x)$ 在 $[a, b]$ 上可积, 且 $I=\int_a^b f(x) d x>0$, 则有子区间 $[c, d] \subset[a, b]$ 和 $\mu>0$, 使在区 间 $[c, d]$ 上成立 $f(x) \geq \mu$.
  证明: 从定积分定义可知, 存在 $[a, b]$ 的一个分划 $T=\left\{x_k\right\}_{0 \leq k \leq n}$, 使得对从属于 $T$ 的任何介点 组 $\left\{\xi_k\right\}$, 成立$\sum_{i=1}^n f\left(\xi_i\right) \Delta x_i>\frac{I}{2}>0 .$记$m_i=\inf _{x_{i-1} \leq x \leq x_i} f(x), i=1,2, \cdots, n,$并对于上面的和式取下确界, 就得到$\sum_{i=1}^n m_i \Delta x_i \geq \frac{I}{2}>0 .$

显然在和式中至少有一项大于 0 , 设这一项为第 $k$ 项, 则就可取 $\mu=m_k,[c, d]=\left[x_{k-1}, x_k\right]$.









#### 6.4  定积分的性质

- 积分的性质：

  - 线性性质：$\int_a^b[\alpha f(x)+\beta g(x)] \mathrm{d} x=\alpha \int_a^b f(x) \mathrm{d} x+\beta \int_a^b g(x) \mathrm{d} x$.

  - 绝对值性质；

  - 保序性质；如果 $f, g \in \mathcal{R}[a, b], f \leq g$, 则$\int_a^b f(x) \mathrm{d} x \leq \int_a^b g(x) \mathrm{d} x$；

    - 【推论】若非负函数 $f(x)$ 在 $[a, b]$ 上可积, 则$\int_a^b f(x) \mathrm{d} x \geq 0$;
    - 【推论】设 $f(x)$ 在 $[a, b]$ 上可积, 则$\left|\int_a^b f(x) \mathrm{d} x\right| \leq \int_a^b|f(x)| \mathrm{d} x .$
    - 【推论】设 $f(x)$ 在 $[a, b]$ 上可积, $M$ 和 $m$ 分别是 $f(x)$ 在 $[a, b]$ 上的上界和下界, 则$m(b-a) \leq \int_a^b f(x) \mathrm{d} x \leq M(b-a)$；

  - 乘法性质：设函数 $f(x), g(x)$ 都在 $[a, b]$ 上可积, 则 $f(x) \cdot g(x)$ 也在 $[a, b]$ 上 可积.
    【例题】 因为 $f(x)$ 和 $g(x)$ 都在 $[a, b]$ 上可积, 故都在 $[a, b]$ 上有界, 即有正数 $M$, 使得 $|f(x)| \leq M,|g(x)| \leq M$. 对于 $[a, b]$ 的任意分划 $T=\left\{x_k\right\}_{0 \leq k \leq n}$, 任取两 点 $x^{\prime}, x^{\prime \prime} \in\left[x_{k-1}, x_k\right]$, 我们有
    $$
    \begin{aligned}
    &\left|f\left(x^{\prime \prime}\right) g\left(x^{\prime \prime}\right)-f\left(x^{\prime}\right) g\left(x^{\prime}\right)\right| \\
    =&\left|\left[f\left(x^{\prime \prime}\right)-f\left(x^{\prime}\right)\right] g\left(x^{\prime \prime}\right)+f\left(x^{\prime}\right)\left[g\left(x^{\prime \prime}\right)-g\left(x^{\prime}\right)\right]\right| \\
    \leq & M\left(\left|f\left(x^{\prime \prime}\right)-f\left(x^{\prime}\right)\right|+\left|g\left(x^{\prime \prime}\right)-g\left(x^{\prime}\right)\right|\right)
    \end{aligned}
    $$
    用 $\omega_k(f), \omega_k(g), \omega_k(f g)$ 分别表示 $f(x), g(x), f(x) g(x)$ 在 $\left[x_{k-1}, x_k\right]$ 上的振幅. 于是得到$\omega_k(f g) \leq M\left[\omega_k(f)+\omega_k(g)\right]$

    从而$\sum_{k=1}^n \omega_k(f g) \Delta x_k \leq M\left(\sum_{k=1}^n \omega_k(f) \Delta x_k+\sum_{k=1}^n \omega_k(g) \Delta x_k\right)$因为 $f(x)$ 和 $g(x)$ 都在 $[a, b]$ 上可积, 故有
    $$
    \lim _{\|T\| \rightarrow 0} \sum_{k=1}^n \omega_k(f) \Delta x_k=0, \quad \lim _{\|T\| \rightarrow 0} \sum_{k=1}^n \omega_k(g) \Delta x_k=0 .
    $$
    从而有$\lim _{\|T\| \rightarrow 0} \sum_{k=1}^n \omega_k(f g) \Delta x_k=0$ 知 $f(x) g(x)$ 在 $[a, b]$ 上可积.

  - 区间可加性质；

    - 【推论】定理当 $c$ 在 $[a, b]$ 之外时也成立. 事实上, 不妨设 $a<b<c$, 且 $f(x)$ 在 $[a, b],[b, c]$ 上可积. 有$\int_a^c f(x) \mathrm{d} x=\int_a^b f(x) \mathrm{d} x+\int_b^c f(x) \mathrm{d} x .$
    - 【推论】若函数 $f(x)$ 在 $[a, b]$ 上有界, 且仅有有限个间断点, 则它必在 $[a, b]$ 上可积.

- 【例题】当 $f(x), g(x) \in R[a, b]$ 时, $\frac{f(x)}{g(x)}$ 末必在 $[a, b]$ 上可积 (如此时 $\frac{f(x)}{g(x)}$ 可以是无界函数); 

- 【例题】若 $f(x)$ 与 $g(x)$ 可以复合, $f(g(x))$ 在 $[a, b]$ 上也不一定可积. 例如, 取 $g(x)=R(x)$, 其中 $R(x)$ 是区间 $[0,1]$ 上的黎曼函数, 而取$f(x)= \begin{cases}1, & x \neq 0, \\ 0, & x=0,\end{cases}$,则 $f(g(x))$ 为区间 $[0,1]$ 上的狄利克雷函数. 因此 $f(g(x))$ 在 $[0,1]$ 上 不可积. 

- 【例题】当 $f(x)$ 连续时, 若 $g(x)$ 是 $[a, b]$ 上的可积函数并且 $f(g(x))$ 在 $[a, b]$ 上有定义, 则必定有 $f(g(x)) \in R[a, b]$ 

- 【例题】设函数 $f(x)$ 在区间 $[a, b]$ 上连续, 证明:
  (1) 如果对 $[a, b]$ 的任何子区间 $\left[a_1, b_1\right]$ 有 $\int_{a_1}^{b_1} f(x) \mathrm{d} x=0$, 则 $f(x) \equiv$ $0, x \in[a, b] ;$
  (2) 若 $f(x) \geqslant 0$, 并且 $\int_a^b f(x) \mathrm{d} x=0$, 则 $f(x) \equiv 0, x \in[a, b]$.
  证明 (1) 用反证法. 倘若 $f(x)$ 不恒为 0 , 则存在 $x_0 \in[a, b]$, 使 得 $f\left(x_0\right) \neq 0$. 不妨设 $f\left(x_0\right)>0$, 且 $x_0 \in(a, b)$. 由 $f(x)$ 的连续性, 存在 $\delta_0>0$, 使得 $\left[x_0-\delta_0, x_0+\delta_0\right] \subset[a, b]$, 且当 $x \in\left[x_0-\delta_0, x_0+\delta_0\right]$ 时, 有$f(x) \geqslant \frac{f\left(x_0\right)}{2} .$因此$\int_{x_0-\delta_0}^{x_0+\delta_0} f(x) \mathrm{d} x \geqslant \frac{f\left(x_0\right)}{2} \int_{x_0-\delta_0}^{x_0+\delta_0} \mathrm{~d} x=\delta_0 f\left(x_0\right)>0 .$

  (2) 用反证法. 当 $f(x)$ 不恒为 0 时, 必存在 $x_0 \in(a, b)$, 使得 $f\left(x_0\right)>$ 0 . 由 (1) 的证明过程知, 存在 $\delta_0>0$, 使得$\int_{x_0-\delta_0}^{x_0+\delta_0} f(x) \mathrm{d} x>0 .$

但此时有$\int_a^b f(x) \mathrm{d} x \geqslant \int_{x_0-\delta_0}^{x_0+\delta_0} f(x) \mathrm{d} x>0 .$这与已知矛盾. (2) 得证.

- 【例题】设 $f(x)$ 在 $[a, b]$ 上连续, 且满足条件$\int_a^b x^k f(x) d x=0 \quad(k=0,1, \cdots, n),$证明: 函数 $f(x)$ 在 $(a, b)$ 内至少有 $n+1$ 个不同的零点.
  证明: 用反证法. 设有一个函数 $f(x)$ 满足所有题设条件, 但其零点个数不超过 $n$. 这时 $f(x)$ 不会恒等于 0 , 因此从条件 $\int_a^b x^k f(x) d x=0$ 及 $f(x)$ 为连续函数, 可见 $f(x)$ 在 $[a, b]$ 内一定变号. 利用 $f(x)$ 的所有零点, 可以作出区间 $[a, b]$ 的一个分划

$T=\left\{x_0, x_1, \cdots, x_k\right\},$其中 $x_0=a, x_k=b$, 中间的 $k-1$ 个分点都是 $f(x)$ 的零点, $f(x)$ 在每个子区间上不变号, 而在相邻的子区间上 $f(x)$ 的符号相反.由反证法的前提可见 $k-1 \leq n$. 对于分划 $T$ 可以构造辅助多项式$g(x)=\left(x-x_1\right)\left(x-x_2\right) \cdots\left(x-x_{k-1}\right) .$$g(x)$ 关于分划 $T$ 具有与 $f(x)$ 相同的性质: 即在每个子区间上不变号, 而在相邻的子区间上符号相反, 这样就知道 $f(x) g(x)$ 在整个区间 $[a, b]$ 上不变号, 因此$\int_a^b g(x) f(x) d x \neq 0$.另一方面, 由于 $g$ 是次数不超过 $n$ 的多项式, 从题设条件可见上述积分应当等于 0 , 从而引出矛盾. 

【推广】请问若已知条件减弱为 $f(x)$ 在 $[\mathrm{a}, \mathrm{b}]$ 上可积, 且足条件 $\int_a^b x^k f(x) d x=0 \quad(k=0,1, \cdots, n)$, 那么结论是否仍然成立?
答案是否定的, 反例如下:
$$
f(x)= \begin{cases}-1, & 0 \leq x<1 \\ 2, & 1 \leq x<2 \\ -1, & 2 \leq x \leq 3\end{cases}
$$
容易验证 $\int_a^b f(x) d x=0, \int_a^b x f(x) d x=0$, 但函数 $f(x)$ 并无零点.

- 【例题】求证
  (i) $\lim _{n \rightarrow \infty} \int_0^{\pi / 2} \sin ^n x \mathrm{~d} x=0$;
  (ii) $\lim _{n \rightarrow \infty}\left\{\int_0^{\pi / 2} \sin ^n x \mathrm{~d} x\right\}^{1 / n}=1$.
  证明 (i) 对于任给的 $\varepsilon>0$ (不妨设 $\varepsilon<\pi$ ), 我们有
  $$
  \begin{aligned}
  0 & \leq \int_0^{\pi / 2} \sin ^n x \mathrm{~d} x=\int_{(\pi-\varepsilon) / 2}^{\pi / 2} \sin ^n x \mathrm{~d} x+\int_0^{(\pi-\varepsilon) / 2} \sin ^n x \mathrm{~d} x \\
  & \leq \frac{\varepsilon}{2}+\frac{\pi}{2} \sin ^n \frac{\pi-\varepsilon}{2}<\frac{\varepsilon}{2}+2 \sin ^n \frac{\pi-\varepsilon}{2}
  \end{aligned}
  $$
  因为 $0<\sin \frac{\pi-\varepsilon}{2}<1$, 故有 $\lim _{n \rightarrow \infty} \sin ^n \frac{\pi-\varepsilon}{2}=0$, 所以存在 $N$, 使得当 $n>N$ 时, 就有$0<\sin ^n \frac{\pi-\varepsilon}{2}<\frac{\varepsilon}{4} .$将两者结合起来, 我们得到$0 \leq \int_0^{\pi / 2} \sin ^n x \mathrm{~d} x<\varepsilon, \quad \text { 当 } n>N \text {. }$

- 【例题】设非负函数 $f(x)$ 在 $[a, b]$ 上连续, 证明$\lim _{n \rightarrow \infty}\left(\int_a^b f^n(x) d x\right)^{\frac{1}{n}}=\max \{f(x) \mid x \in[a, b]\}$

  证明: 如果 $f(x) \equiv 0$, 则所证等式显然成立. 否则, 设 $f(x)$ 在 $x_0$ 点取到最大值, $f\left(x_0\right)=\max \{f(x) \mid x \in$ $[a, b]\} \triangleq M$, 则 $M>0$. 利用函数 $f(x)$ 在 $x_0$ 点的连续性可得, $\forall 0<\varepsilon<M, \exists \delta>0$, s.t.$M-\varepsilon \leq f(x) \leq M, \quad x \in\left(x_0-\delta, x_0+\delta\right),$令 $\alpha=x_0-\delta, \beta=x_0+\delta($ 若 $\alpha<a$, 取 $\alpha=a$; 若 $\beta>b$, 取 $\beta=b)$.
  即: 对 $0<\varepsilon<M, \exists[\alpha, \beta] \subseteq[a, b]$, 使得$M-\varepsilon \leq f(x) \leq M, \quad x \in[\alpha, \beta] .$于是有
  $$
  \left(\int_a^b f^n(x) d x\right)^{\frac{1}{n}} \geq\left(\int_\alpha^\beta f^n(x) d x\right)^{\frac{1}{n}} \geq(M-\varepsilon)(\beta-\alpha)^{\frac{1}{n}} .
  $$
  对于不等式$M(b-a)^{\frac{1}{n}} \geq\left(\int_a^b f^n(x) d x\right)^{\frac{1}{n}} \geq(M-\varepsilon)(\beta-\alpha)^{\frac{1}{n}},$

  利用上、下极限工具就得到$M \geq \varlimsup_{n \longrightarrow \infty}\left(\int_a^b f^n(x) d x\right)^{\frac{1}{n}} \geq \varliminf_{n \longrightarrow \infty}\left(\int_a^b f^n(x) d x\right)^{\frac{1}{n}} \geq M-\varepsilon .$

  从 $\varepsilon$ 的任意性可见上、下极限相等且等于 $M$.

  【推广】注: 请问若已知条件减弱为 $f(x)$ 在 $[\mathrm{a}, \mathrm{b}]$ 上可积, 那么结论是否仍然成立?
  答案是否定的, 反例如下:
  $$
  f(x)= \begin{cases}0, & a<x \leq b ; \\ 1, & x=a .\end{cases}
  $$
  容易验证 $\lim _{n \rightarrow \infty}\left(\int_a^b f^n(x) d x\right)^{\frac{1}{n}}=0$, 但 $\max \{f(x) \mid x \in[a, b]\}=1$, 二者并不相等.
