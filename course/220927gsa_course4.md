《高等数学A》第四次习题课

> Author ZhenLiu
>
> 2022/09/27



> 以极限为工具，以$\R^{n}$为平台，以函数为对象。



#### 4.1 函数

- 函数基础：函数定义/三要素/表示方法/函数相同只要定义域和对应规则相同即可；
- 特性函数：有界性/单调性/复合函数/反函数/周期函数/奇偶函数/
  - 如果定义域具有对称性，任意函数都可以分解成奇函数和偶函数的叠加；奇: $f(x)=\frac{f(x)-f(-x)}{2}$. 偶: $f(x)=\frac{f(-x)+f(x)}{2}$.
  - 严格单调的函数一定存在反函数, 且原函数和反函数的单调性一致；
- 函数分类 (要熟悉这些函数的图像, 重要点, 单调性等)
  - 初等函数: 常数函数, 三角函数, 反三角函数, 指数函数, 对数函数, 幂函数及它们的组合. 
  - 非初等函数: 如符号函数, 取整函数, 脉冲函数, Dirichlet 函数, Riemann 函数等.



#### 4.2 函数极限

- 定义
  
  - **函数在一点处极限的定义**: 设函数 $f(x)$ 在点 $x_0$ 的空心邻域中有定义, $A \in \mathbb{R}$. 如果对任 意给定的 $\varepsilon>0$, 都存在 $\delta>0$, 使得当 $0<\left|x-x_0\right|<\delta$ 时, 都有
  
  
  $$
  |f(x)-A|<\varepsilon
  $$
  则称 $x \longrightarrow x_0$ 时, $f(x)$ 以 $A$ 为极限, 记为 $\lim _{x \longrightarrow x_0} f(x)=A$.

  - - 若$0<\left|x-x_0\right|<\delta$ 改为 $-\delta<x-x_0<0$, 则称 $A$ 为 $f(x)$ 在 $x_0$ 点的左极限, 记为 $\lim _{x \longrightarrow x_0^{-}} f(x)=A$.
    - 若$0<\left|x-x_0\right|<\delta$ 改为 $0<x-x_0<\delta$, 则称 $A$ 为 $f(x)$ 在 $x_0$ 点的右极限, 记为 $\lim _{x \longrightarrow x_0^{+}} f(x)=A$. 
    - $f(x)$ 在点 $x_0$ 处是否有极限与 $f(x)$ 在该点处是否有定义及有定义时的函数值无关.
  
  - **函数在无穷远处极限的定义**: 设 $f(x)$ 在无穷远点附近有定义, $A \in \mathbb{R}$. 若 $\forall \varepsilon>0$, 都 $\exists M_{\varepsilon}>0$, 使得当 $|x|>M_{\varepsilon}$ 时有
  
  
  $$
  |f(x)-A|<\varepsilon,,
  $$
  则称 $x \longrightarrow \infty$ 时, $f(x)$ 以 $A$ 为极限, 记为 $\lim _{x \longrightarrow \infty} f(x)=A$.
  
  - - 若 $|x|>M_{\varepsilon}$ 改为 $x<-M_{\varepsilon}$, 则称 $A$ 为 $f(x)$ 在 $-\infty$ 点的极限, 记为 $\lim _{x \longrightarrow-\infty} f(x)=A$.
    - 若 $|x|>M_{\varepsilon}$ 改为 $x>M_{\varepsilon}$, 则称 $A$ 为 $f(x)$ 在 $+\infty$ 点的极限, 记为 $\lim _{x \rightarrow+\infty} f(x)=A$.
    - 注: 若将数列看作 $\mathbb{N}^*$ 上的函数, 则数列极限为函数极限的特例. 例如前面提到的 $\ln n$.
  
- 判断函数极限存在的方法总结

  - 定义法

  - 夹挤定理：特别地, 若 $|f(x)-A| \leq g(x), \lim _{x \rightarrow x_0} g(x)=0$, 则 $\lim _{x \rightarrow x_0} f(x)=A$.

    - 【例题】设 $f(x) \geq 0$, 在 $(0,+\infty)$ 上递增, 且 $\lim _{x \rightarrow+\infty} \frac{f(2 x)}{f(x)}=1$. 证明 $\forall \alpha>0, \lim _{x \rightarrow+\infty} \frac{f(\alpha x)}{f(x)}=1$. 

      证明: 由 $\lim _{x \longrightarrow+\infty} \frac{f(2 x)}{f(x)}=1$ 可知, $\forall n \in N^*$, 都有
      $$
      \lim _{x \rightarrow+\infty} \frac{f\left(2^n x\right)}{f(x)}=1 \text { 和 } \lim _{x \rightarrow+\infty} \frac{f\left(\frac{x}{2^n}\right)}{f(x)}=1 .
      $$
      $\forall \alpha>0, \exists n \in N^*$, 使得 $\frac{1}{2^n}<\alpha<2^n$, 故因 $f$ 是递增的, 有
      $$
      \frac{f\left(\frac{x}{2^n}\right)}{f(x)} \leq \frac{f(\alpha x)}{f(x)} \leq \frac{f\left(2^n x\right)}{f(x)}
      $$
      由夹挤定理得 $\lim _{x \longrightarrow+\infty} \frac{f(\alpha x)}{f(x)}=1$.

  - 左右极限：设函数 $f(x)$ 在点 $x_0$ 的一个空心邻域内有定义. 则 $\lim _{x \rightarrow x_0} f(x)$ 存 在的充分必要条件是 $\lim _{x \rightarrow x_0^{-}} f(x)$ 和 $\lim _{x \rightarrow x_0^{+}} f(x)$ 那存在, 而且二者相等.

  - Heine定理：设函数 $f(x)$ 在 $x_0$ 的一个空心邻域内有定义. 则 $\lim _{x \rightarrow x_0} f(x)=A$ 的充分必要条件是, 对任何 $x_n \rightarrow x_0(n \rightarrow \infty)$ 且 $x_n \neq x_0(n=1,2, \cdots)$, 恒有 $\lim _{n \rightarrow \infty} f\left(x_n\right)=A$

  - 单调收敛准则：若函数 $f(x)$ 在 $(a, b)$ 内单调道增而且上方有界, 或单调递减而且下方有界, 则 $\lim _{x \rightarrow b^{-}} f(x)$ 存在.

  - Cauchy准则：函数 $f(x)$ 在点 $x_0$ 处有极限的充分必要条件是对任何给定的 $\varepsilon>$ 0 , 存在 $\delta>0$, 使得
    $$
    \left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon, \quad \forall x_1, x_2: 0<\left|x_1-x_0\right|<\delta, 0<\left|x_2-x_0\right|<\delta
    $$

- 判断函数极限不存在的方法总结

  - 左右极限不相等

  - 无界子列：设函数 $f(x)$ 在 $x_0$ 的某个空心郃域内有定义. 如果存在数列 $\left\{x_n\right\}$, $\lim _{n \rightarrow \infty} x_n=x_0$, 使得 $\lim _{n \rightarrow \infty} f\left(x_n\right)=\infty$, 则 $\lim _{x \rightarrow x_0} f(x)$ 不存在.

  - 两个子列：设 $\left\{a_n\right\}$ 和 $\left\{b_n\right\}$ 为异于 $x_0$ 但又趋于 $x_0$ 的数列, 满足 $\lim _{n \rightarrow \infty} f\left(a_n\right) \neq \lim _{n \rightarrow \infty} f\left(b_n\right)$, 则 $\lim _{x \rightarrow x_0} f(x)$ 不存在.

  - 【例题】试证函数 $f(x)=\sin \frac{1}{x}$ 在点 $x=0$ 处没有极限. 证明 令
    $$
    a_n=\frac{1}{2 n \pi+\frac{\pi}{2}}, \quad b_n=\frac{1}{2 n \pi} .
    $$
    则
    $$
    \lim _{n \rightarrow \infty} f\left(a_n\right)=1, \quad \lim _{n \rightarrow \infty} f\left(b_n\right)=0 .
    $$
    由上述推论可知, $\lim _{x \rightarrow 0} f(x)$ 不存在.

  - 【例题】试证 Dirichlet 函数 $D(x)$ 在任何点处都没有极限.
    证明 对于任何 $x_0 \in \mathbb{R}$, 由有理数和无理数在实数中的稠密性知可选取有 理数列 $\left\{x_n\right\}$ 和无理数列 $\left\{x_n^{\prime}\right\}$, 满足条件 $x_n \rightarrow x_0, x_n^{\prime} \rightarrow x_0(n \rightarrow \infty)$ 且 $x_n \neq$ $x_0, x_n^{\prime} \neq x_0, n=1,2, \cdots$. 于是按 $D(x)$ 的定义有
    $$
    \lim _{n \rightarrow \infty} D\left(x_n\right)=1 \neq 0=\lim _{n \rightarrow \infty} D\left(x_n^{\prime}\right) .
    $$
    从而 $D(x)$ 在 $x_0$ 点没有极限.

- 函数极限的性质

  - 唯一/绝对值/有界/保序/四则运算/夹挤定理；

  - 复合函数性质：设 $\lim _{y \rightarrow y_0} f(y)=A, \lim _{x \rightarrow x_0} g(x)=y_0$, 且存在 $x_0$ 的一个空心邨戓, 当 $x$ 在此邻域内时 $g(x) \neq y_0$, 则 $\lim _{x \rightarrow x_0} f(g(x))=A$.

  - 【例题】应当注意, 当 $y_0$ 为有限数时, 仅有 $\lim _{y \rightarrow y_0} f(y)=A$ 和 $\lim _{x \rightarrow x_0} g(x)=y_0$ 不足以 保证 $\lim _{x \rightarrow x_0} f(g(x))=A$. 例如：
    $$
    f(y)=\left\{\begin{array}{ll}
    1, & y \neq 0, \\
    0, & y=0 ;
    \end{array} \quad g(x) \equiv 0,\right.
    $$
    显然有 $\lim _{y \rightarrow 0} f(y)=1, \lim _{x \rightarrow 0} g(x)=0$, 但 $f(g(x)) \equiv 0$. 因此
    $$
    \lim _{x \rightarrow 0} f(g(x))=0 \neq \lim _{y \rightarrow 0} f(y)
    $$





#### 4.3 函数连续

- 单点处函数连续的定义：设函数 $f(x)$ 在点、 $x_0$ 的某个邻域内有定义. 郧 $f(x)$ 在点, $x_0$ 处连 续䛑是, 对任㶳给定的 $\varepsilon>0$, 存在 $\delta>0$, 使得
  $$
  \left|f(x)-f\left(x_0\right)\right|<\varepsilon, \quad \forall x:\left|x-x_0\right|<\delta
  $$

- 判断函数在单点处连续的方法：定义法/左右极限/Heine定理；

- 三类间断点的定义：第一/第二/可去；

- 连续函数的定义：如果函数 $f(x)$ 在区间 $(a, b)$ 的每一点陣是连续的, 则称 $f(x)$ 在 $(a, b)$ 上连续, 或说 $f(x)$ 是 $(a, b)$ 上的连续函数. 如果 $f(x)$ 在 $(a, b)$ 上连续, 而 且在 $a$ 点右连续, 在 $b$ 点左连续, 则称 $f(x)$ 在 $[a, b]$ 上连续, 或说 $f(x)$ 是 $[a, b]$ 上的连续函数.

- 复合函数的性质：设 $\lim _{x \rightarrow x_0} f(x)=y_0, \varphi(y)$ 在 $y_0$ 点连续, 则$\lim _{x \rightarrow x_0} \varphi(f(x))=\varphi\left(\lim _{x \rightarrow x_0} f(x)\right)=\varphi\left(y_0\right) .$

  特别, 若 $f(x)$ 在 $x_0$ 点连续, $\varphi(y)$ 在 $y_0=f\left(x_0\right)$ 点连续, 则 $\varphi(f(x))$ 在 $x_0$ 点连续.

- 【例题】$\lim _{x \longrightarrow a} \frac{\sin x-\sin a}{x-a}=\lim _{x \longrightarrow a} \frac{2 \sin \frac{x-a}{2} \cos \frac{x+a}{2}}{x-a}=\lim _{x \longrightarrow a} \frac{\sin \frac{x-a}{2}}{\frac{x-a}{a}} \lim _{x \longrightarrow a} \cos \frac{x+a}{2}=\cos a$
- 【例题】$\lim _{x \rightarrow \pi} \frac{\sin m x}{\sin n x} \stackrel{y=x-\pi}{=} \quad \lim _{y \longrightarrow 0} \frac{\sin m(y+\pi)}{\sin n(y+\pi)} =\lim _{y \longrightarrow 0} \frac{(-1)^m}{(-1)^n} \lim _{y \longrightarrow 0} \frac{\sin m y}{\sin n y}=\frac{m}{n}(-1)^{m-n} .$
- 【例题】$\lim _{x \longrightarrow 1}(1-x) \tan \frac{\pi}{2} x \stackrel{1-x=y}{=} \quad \lim _{y \longrightarrow 0} y \cdot \tan \left(\frac{\pi}{2}(1-y)\right)=\lim _{y \longrightarrow 0} y \cot \frac{\pi}{2} y =\lim _{y \longrightarrow 0} y \frac{\cos \frac{\pi}{2} y}{\sin \frac{\pi}{2} y}=\frac{2}{\pi} $
- 【例题】$$\begin{aligned} & \lim _{n \longrightarrow \infty} \cos \frac{x}{2} \cos \frac{x}{4} \cdots \cos \frac{x}{2^n} \\=& \lim _{n \longrightarrow \infty}\left(\cos \frac{x}{2} \cos \frac{x}{4} \cdots \cos \frac{x}{2^n}\right) \sin \frac{x}{2^n} / \sin \frac{x}{2^n} \\=& \lim _{n \longrightarrow \infty} \frac{\sin x}{2^n \sin \frac{x}{2^n}}=\lim _{n \longrightarrow \infty} \frac{\frac{x}{2^n}}{\sin \frac{x}{2^n}} \cdot \frac{\sin x}{x} \\ \stackrel{\text { Heine }}{=} & \frac{\sin x}{x} . \end{aligned}$$
- 【例题】$\begin{aligned} \lim _{x \rightarrow 1} & \frac{x+x^2+\cdots+x^n-n}{x-1} \\ &=\lim _{x \rightarrow 1}\left(\frac{x-1}{x-1}+\frac{x^2-1}{x-1}+\cdots+\frac{x^n-1}{x-1}\right) \\ &=\lim _{x \rightarrow 1}\left[1+(1+x)+\cdots+\left(x^{n-1}+x^{n-2}+\cdots+1\right)\right] \\ &=1+2+\cdots+n=\frac{1}{2} n(n+1) . \end{aligned}$
- 解: 令 $y=\frac{\pi}{2}-x$, 则 $\lim _{x \rightarrow \frac{\pi}{2}}(\sin x)^{\tan x}=\lim _{y \rightarrow 0}(\cos y)^{\cot x}=\lim _{y \rightarrow 0} e^{\cot y \ln (\cos y)}$. 由:
  $$
  \begin{aligned}
  \lim _{y \rightarrow 0} \cot y \ln (\cos y) &=\lim _{y \rightarrow 0} \frac{\cos y}{\sin y}(\cos y-1) \frac{\ln [1+(\cos y-1)]}{\cos y-1} \\
  &=\lim _{y \rightarrow 0} \cos y \frac{-y^2 / 2}{\sin y} \frac{\ln [1+(\cos y-1)]}{\cos y-1} \\
  &=0 .
  \end{aligned}
  $$
  其中用到了 $\cos y-1 \sim-\frac{y^2}{2}(y \rightarrow 0)$, 以及 $\ln (1+x) \sim x(x \rightarrow 0)$, 所以原极限等于 1 .
- 解: 令 $y=\frac{1}{x}$, 有: $\lim _{x \rightarrow \infty}\left(\cos \frac{a}{x}\right)^{x^2}=\lim _{x \rightarrow \infty} e^{x^2 \ln \left(\cos \frac{a}{x}\right)}$, 再由
  $$
  \begin{aligned}
  \lim _{x \rightarrow \infty} x^2 \ln \left(\cos \frac{a}{x}\right) &=\lim _{x \rightarrow \infty} x^2\left(\cos \frac{a}{x}-1\right) \frac{\ln [1+(\cos (a /)}{\cos (a / x)} \\
  &=\lim _{x \rightarrow \infty} x^2\left(-\frac{a^2}{2 x^2}\right) \frac{\ln [1+(\cos (a / x)}{\cos (a / x)-} \\
  &=-\frac{a^2}{2}
  \end{aligned}
  $$





#### 4.4  无穷小量和无穷大量

- 定义：设 $\left\{x_n\right\}$ 是一个序列. 若 $x_n \rightarrow 0(n \rightarrow \infty)$, 则称序 列 $\left\{x_n\right\}$ 为无穷小量, 记为 $x_n=o(1)(n \rightarrow \infty)$.

  - 这里需特别指出的是, 无穷小量并不是一个很小的量, 而是极限为 零的一个变量.

- 性质：设 $\left\{x_n\right\}$ 是一个序列.

  - $\left\{x_n\right\}$ 是无穷小量的充分必要条件是 $\left\{\left|x_n\right|\right\}$ 是无穷小量；
  - 若 $\left\{x_n\right\}$ 是无穷小量, $M$ 是一个常数, 则 $\left\{M x_n\right\}$ 是无穷小量;
  -  $\lim _{n \rightarrow \infty} x_n=a$ 的充分必要条件是 $\left\{x_n-a\right\}$ 是无穷小量.
  - 定理： $\left\{x_n\right\}$ 是无穷小量的充分必要条件是 $\left\{\frac{1}{x_n}\right\}$ 是无穷大量, 这里假定对任意的正整数 $n$, 有 $x_n \neq 0$.

- 【例题】如果不是乘积和商的极限, 则一般不能用等价无穷小 (大) 量 来代替. 例如:
  $$
  \lim _{x \rightarrow 0} \frac{\tan x-\sin x}{x^3}=\frac{1}{2} \neq \lim _{x \rightarrow 0} \frac{x-x}{x^3}=0
  $$





#### 4.5 闭区间上连续函数的性质

- 闭区间上连续函数的性质. 设 $f(x)$ 为闭区间 $[a, b]$ 上的连续函数, 则
  -  $f(x)$ 在 $[a, b]$ 上有界(有界性定理);
  -  $f(x)$ 在 $[a, b]$ 上取得最大值和最小值(最值定理);
  -  $\exists \xi \in(a, b)$, s.t. $f(\xi)=\mu$, 其中 $\mu$ 是介于 $f(a), f(b)$ 之间的任何一个常数(介值定理);
  -  $f(x)$ 在 $[a, b]$ 上必一致连续(一致连续性定理).
  - 推论(零点定理) 设 $f(x)$ 是 $[a, b]$ 上的连续函数, 且 $f(a) \cdot f(b)<0$, 则 $\exists \xi \in(a, b)$, s.t. $f(\xi)=0$. 
  - 注一致连续 $\Rightarrow$ 逐点连续 $\Leftrightarrow$ 区间连续, 反之不成立. 例如 $\frac{1}{x}$ 在 $(0,1]$ 上连续, 但不一致连续.
- 【例题】设 $f(x) \in C[a, b], a<x_1<x_2<\cdots<x_n<b$, 求证 $\exists \xi \in\left[x_1, x_n\right]$, s.t.

$$
f(\xi)=\frac{1}{n}\left[f\left(x_1\right)+f\left(x_2\right)+\cdots+f\left(x_n\right)\right] .
$$

证明: 由 $f(x)$ 在 $\left[x_1, x_n\right]$ 上连续可知, $f(x)$ 在 $\left[x_1, x_n\right]$ 上存在最大值 $M$ 、最小值 $m$, 且
$$
m \leq f(x) \leq M, \quad \forall x \in\left[x_1, x_n\right],
$$
故 $m \leq \frac{1}{n}\left[f\left(x_1\right)+\cdots+f\left(x_n\right)\right] \leq M$. 由介值定理可得 $\exists \xi \in\left[x_1, x_n\right]$, s.t.$f(\xi)=\frac{1}{n}\left[f\left(x_1\right)+f\left(x_2\right)+\cdots+f\left(x_n\right)\right]$

- 【例题】设 $f \in C([a, b])$. 若 $f(a)=f(b)$, 则在 $[a, b]$ 中存在 $c, d, d-c=$ $(b-a) / 2$, 使得 $f(c)=f(d)$.

   令 $F(x)=f(x+(b-a) / 2)-f(x)$, 则
  $$
  F(a)=f\left(\frac{a+b}{2}\right)-f(a), \quad F\left(\frac{a+b}{2}\right)=f(b)-f\left(\frac{a+b}{2}\right) .
  $$
  由此知 $F\left(\frac{a+b}{2}\right)=-F(a)$. 从而存在 $\xi \in\left[a, \frac{a+b}{2}\right]$, 使得 $F(\xi)=f\left(\xi+\frac{b-a}{2}\right)-$ $f(\xi)=0$, 即
  $$
  f\left(\xi+\frac{b-a}{2}\right)=f(\xi) .
  $$
  令 $\xi=c, d=\xi+(b-a) / 2$, 则 $d-c=(b-a) / 2, f(d)=f(c)$.





#### 4.6 一致连续

> 以下我们来讨论函数的一致连续性问题. 为此先来考查函数 $f(x)=$ $\frac{1}{x}, x \in(0,1)$. 我们知道 $f(x)$ 在 $(0,1)$ 是连续的. 换句话说, 对每 个 $x_0 \in(0,1)$, 对任意给定的 $\varepsilon>0$, 都存在 $\delta>0$, 使得当 $\left|x-x_0\right|<\delta$ 时, 有 $\left|\frac{1}{x}-\frac{1}{x_0}\right|<\varepsilon$. 这里有个值得注意的现象是, 对于同一个 $\varepsilon$, 当 $x_0$ 与 0 越近时, 相应得到的 $\delta$ 也就越小. 换句话说, 我们不可能找到一个 仅依赖 $\varepsilon$, 而不依赖 $x_0$ 的 $\delta$, 使得对所有的 $x_0 \in(0,1)$, 有 $\left|\frac{1}{x}-\frac{1}{x_0}\right|<\varepsilon$. 基于这一现象, 我们引入如下的概念:

- 定义：设函数 $f(x)$ 在区间 $I$ 上有定义, 如果对于任何 $\varepsilon>0$, 都存在 $\delta>0$, 使当 $x_1, x_2 \in I$ 且 $\left|x_1-x_2\right|<\delta$ 时, 就有
  $$
  \left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon,
  $$
  则称函数 $f(x)$ 在区间 $I$ 上一致连续.

  等价描述：如果令$\omega(r)=\sup _{x_1, x_2 \in I ;\left|x_1-x_2\right| \leq r}\left|f\left(x_1\right)-f\left(x_2\right)\right| \text {, }$则 $f(x)$ 在区间 $I$ 上一致连续指的就是$\lim _{r \rightarrow 0^{+}} \omega(r)=0 .$

- 【例题】判别下列函数在指定区间上的一致连续性:
  (1) $f(x)=\ln x,(0,1]$.
  (2) $f(x)=\frac{\sin x}{x},(0,1]$.
  (3) $f(x)=\sin ^2 x,[0, \infty)$.
  (4) $f(x)=\sin x^2,[0, \infty)$.
  (5) $f(x)=\sqrt{x},[0, \infty)$.
  (6) $f(x)=\mathrm{e}^x,[0, \infty)$.
  解： (1) 因为 $\lim _{x \rightarrow 0+} \ln x=-\infty$, 所以不一致连续.
  (2) 因为存在 $\lim _{x \rightarrow 0+} \sin x / x=1$, 所以是一致连续的.
  (3) 因为 $\left|\sin ^2 x_1-\sin ^2 x_2\right|=\left|\sin x_1-\sin x_2\right|\left|\sin x_1+\sin x_2\right| \leqslant 2\left|x_1-x_2\right|$, 所 以是一致连续的, 且属于 $\operatorname{Lip} 1([0, \infty))$.
  (4) 取 $x_n^{\prime}=\sqrt{2 n \pi}, x_n^{\prime \prime}=\sqrt{2 n \pi+\pi / 2}$ 时, 我们有 $\lim _{n \rightarrow \infty}\left(x_n^{\prime}-x_n^{\prime \prime}\right)=0$, 但 $\left|f\left(x_n^{\prime}\right)-f\left(x_n^{\prime \prime}\right)\right|=1$. 故不一致连续.
  (5) 因为 $\left|\sqrt{x_1}-\sqrt{x_2}\right| \leqslant \sqrt{\left|x_1-x_2\right|}$, 所以是一致连续的.
  (6) 取 $x_n^{\prime}=\ln n, x_n^{\prime \prime}=\ln (n+1)$ 时, 我们有 $\lim _{n \rightarrow \infty}\left(x_n^{\prime}-x_n^{\prime \prime}\right)=0$, 但 $\left|f\left(x_n^{\prime}\right)-f\left(x_n^{\prime \prime}\right)\right|=1$. 故不一致连续.

- 【例题】证明 $f(x)=\sin x$ 在 $\mathbb{R}$ 上一致连续.
  证明：因为对任何 $x_1, x_2 \in \mathbb{R}$,
  $$
  \begin{aligned}
  \left|\sin x_1-\sin x_2\right| &=\left|2 \cos \frac{x_1+x_2}{2} \sin \frac{x_1-x_2}{2}\right| \\
  & \leq 2\left|\sin \frac{x_1-x_2}{2}\right| \leq\left|x_1-x_2\right|
  \end{aligned}
  $$
  故
  $$
  \omega(r) \equiv \sup _{x_1, x_2 \in I ;\left|x_1-x_2\right| \leq r}\left|f\left(x_1\right)-f\left(x_2\right)\right| \leq r .
  $$
  从而 $\lim _{r \rightarrow 0^{+}} \omega(r)=0$, 即 $f(x)=\sin x$ 在 $\mathbb{R}$ 上一致连续.

- 不一致连续的两个写法：

  - 否命题 I: 不一致连续 $\Leftrightarrow \exists \varepsilon_0>0, \forall \delta>0$, 都 $\exists x_\delta^{\prime}, x^{\prime \prime}{ }_\delta \in I$ 且 $\left|x_\delta^{\prime}-x^{\prime \prime}{ }_\delta\right|<\delta$,

  $$
  \text { s.t. }\left|f\left(x_1\right)-f\left(x_2\right)\right| \geq \varepsilon_0 .
  $$
  - 否命题 II: 不一致连续 $\Leftrightarrow \exists \varepsilon_0>0$ 及满足 $\lim _{n \longrightarrow \infty}\left(a_n-b_n\right)=0$ 的数列 $\left\{a_n\right\},\left\{b_n\right\} \subset I$, s.t. $\left|f\left(a_n\right)-f\left(b_n\right)\right| \geq \varepsilon_0, \quad \forall n \in \mathbb{N}^*$

- 一致连续的性质：

  - 注 1 一致连续函数的定义域缩小时仍为一致连续函数.
  - 注 2 有限开区间 $(a, b)$ 上的连续函数 $f(x)$ 一致连续 $\Leftrightarrow f(a+0)$ 和 $f(b+0)$ 都存在. 
  - 注 3 有限开区间 $(a, b)$ 上的一致连续函数必有界.
  - 注 4 两个一致连续函数之和仍一致连续, 推广到有限个仍成立.
  - 注 5 两个一致连续函数之积未必一致连续, 如 $x^2=x \cdot x$.

- 【例题】证明若函数 $f(x)$ 在 $[a,+\infty)$ 上连续, 且 $\lim _{x \longrightarrow+\infty} f(x)$ 存在, 则 $f(x)$ 在 $[a,+\infty)$ 上一致连续. 

  证明: $\lim _{x \longrightarrow+\infty} f(x)$ 存在, 故 $\forall \varepsilon>0$, 都 $\exists M>a, \forall x_1, x_2>M$, 恒有$\left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon .$

$f(x)$ 在闭区间 $[a, M+1]$ 上连续, 故一致连续, 从而 $\forall \varepsilon>0$, 必 $\exists \delta_1>0$, s.t.$\left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon .$
$\forall x_1, x_2 \in[a, M+1]$ 且 $\left|x_1-x_2\right|<\delta_1$ 时, 恒有$\left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon .$现令 $\delta=\min \left\{1, \delta_1\right\}$, 则 $\forall x_1, x_2 \in[a,+\infty)$, 且满足 $\left|x_1-x_2\right|<\delta$ 时, 必有 $x_1$ 和 $x_2$ 同时属 于 $[a, M+1]$ 或 $(M,+\infty)$. 因此, 恒有$\left|f\left(x_1\right)-f\left(x_2\right)\right|<\varepsilon .$故 $f(x)$ 在 $[a,+\infty)$ 上一致连续.

- 【例题】设函数 $f(x)$ 在区间 $I$ 上满足 Lipschitz连续条件, 即 $\exists L>0, \forall x_1, x_2 \in I$, 有

$$
\left|f\left(x_1\right)-f\left(x_2\right)\right| \leq L\left|x_1-x_2\right| .
$$
证明 $f(x)$ 在 $I$ 上一致连续.
证明: $\forall \varepsilon>0, \exists \delta=\frac{\varepsilon}{L}, \forall x_1, x_2 \in I$ 且 $\left|x_1-x_2\right|<\delta$ 时, 有
$$
\left|f\left(x_1\right)-f\left(x_2\right)\right| \leq L\left|x_1-x_2\right|<L \delta<\varepsilon .
$$
由定义可知 $f(x)$ 在 $I$ 上一致连续.

- 【例题】证明 $f(x)=\sqrt{x}$ 在 $[0,+\infty)$ 上一致连续.
  证明：显然 $f(x)$ 在 $[0,+\infty)$ 连续. 下面我们证明 $f(x)=\sqrt{x}$ 在 $[0,+\infty)$ 一致连续.
  事实上, 任取 $\varepsilon>0$, 取 $\delta_1=\varepsilon$, 则当 $x^{\prime}, x^{\prime \prime} \in[1,+\infty)$ 且 $\left|x^{\prime}-x^{\prime \prime}\right|<$ $\delta_1$ 时, 有
  $$
  \begin{aligned}
  &\left|f\left(x^{\prime}\right)-f\left(x^{\prime \prime}\right)\right|=\left|\sqrt{x^{\prime}}-\sqrt{x^{\prime \prime}}\right| \\
  &\quad=\frac{\left|x^{\prime}-x^{\prime \prime}\right|}{\left|\sqrt{x^{\prime}}+\sqrt{x^{\prime \prime}}\right|} \leqslant\left|x^{\prime}-x^{\prime \prime}\right|<\varepsilon .
  \end{aligned}
  $$
  其次, 由康托尔定理, $f(x)$ 在 $[0,2]$ 上连续, 从而一致连续. 因此对上 述 $\varepsilon>0, \exists \delta_2>0$, 使得当 $x^{\prime}, x^{\prime \prime} \in[0,2]$ 且 $\left|x^{\prime}-x^{\prime \prime}\right|<\delta_2$ 时, 有
  $$
  \left|f\left(x^{\prime}\right)-f\left(x^{\prime \prime}\right)\right|<\varepsilon .
  $$
  因此取 $\delta=\min \left\{\delta_1, \delta_2, \frac{1}{2}\right\}$, 对任意的 $x^{\prime}, x^{\prime \prime} \in[0,+\infty)$, 当 $\left|x^{\prime}-x^{\prime \prime}\right|<\delta$ 时, 必有 $x^{\prime}, x^{\prime \prime}$ 同时落在 $[0,2]$ 或 $[1,+\infty)$ 上. 因此, 由上所证, 有
  $$
  \left|f\left(x^{\prime}\right)-f\left(x^{\prime \prime}\right)\right|<\varepsilon .
  $$
  这就证明了 $f(x)=\sqrt{x}$ 在 $[0,+\infty)$ 上一致连续.

