《高等数学A》第三次习题课

> Author ZhenLiu
>
> 2022/09/20



> 以极限为工具，以$\R^{n}$为平台，以函数为对象。



#### 3.1 集合

- 基数：

  - 无穷集合定义：它本身的一个真子集对等的集合；

  - Cantor定理： $[0,1]$ 闭区间上所有的点作成的点集是不能和由全.体正整数所作成的集合 $\mathbf{N}$ 对等的.

  - 【例题】

    - (1) 证明 $\mathbb{N}^2$ 是可数集(即设计一种方案将 $\mathbb{N}^2$ 排成一列）

      给出一种排列(1,1)-(2,1)-(1,2)-(3,1)-(2,2)-(1,3)-，即以斜线的方式依次向下排列；

    - $(2)^*$ 利用对角线方法证明: $[0,1]$ 不是可数集. (提示: $[0,1]$ 里面的数 有小数表达 $0 . a_1 a_2 a_3 \ldots$, 其中 $a_i \in\{0,1,2,3,4,5,6,7,8,9\}$, 请说明如果能 排成一列, 则能够造一个新的小数.)

      反证法，假设[0,1]中的所有数能排成一个序列$a_{1},a_{2},\cdots,a_{n},\cdots$，每个数用小数的形式表达，然后构造一个小数$a$，使得其小数点后的第$i$个数不等于$a_{i}$,从而找到一个在[0,1]中但是不在序列中的数，矛盾。

  - 定义：设 $A, B$ 是两个集合. 如果 $A$ 和 $B$ 不对等, 但存在 $B$ 的某子集 $B^*$ 使 $A$ 和 $B^*$ 对等, 则我们就说 $A$ 的基数 $\bar{A}$ 小于 $B$ 的基数 $\bar{B}$,记为 $\bar{A}<\overline{\bar{B}}$.

  - 定理： 若 $A, B$ 是两个集合. 如果存在 $A$ 的子集 $A^*, B$ 的子 集 $B^*$, 使 $A \sim B^*, B \sim A^*$, 则 $A \sim B$.

  - 推论： 若 $A \subset B \subset C, A \sim C$, 则 $A \sim B, B \sim C$.

- 可数集合：

  - 定义 凡能与全体自然数所作成的集合 $\mathbf{N}$ 对等的集合都称为 可数集合；
  - 定理 1 任何无穷集合 $M$ 都包含一个可数子集.
  - 定理2 可数集合的子集如果不是有限集合则一定还是可数集合.
  - 定理 3 若 $A$ 可数, $B$ 有限,则 $A \cup B$ 可数.
  - 推论： 若 $A_1, \cdots, A_n$ 的每一个都是有限集合或可数集合, 则 $\bigcup_{i=1}^n A_i$ 是有限集合或可数集合,而只要其中有一个 $A_i$ 不是有限的, 则 $\bigcup_{i=1}^n A_i$ 就是可数的.
  - 定理 7 如果 $A$ 是一无穷集合, $B$ 是一可数集合, 则 $A \cup B$ $\sim A .$
  
- 不可数集合：

  - 定义: 与$[0,1]$ 对等的集合也一定是不可数无穷集.
  - 定理 1:   全体实数所作成的集合 $\mathbb{R}^{\prime}$ 的基数是 $c$.
  - 定理 2:  只要 $a<b$,开区间 $(a, b)$ 的基数都是 $c$.
  - 定理 3:  如果 $A_i(i=1,2,3, \cdots)$. 都是基数小于或等于 $c$ 的集:合且其中至少有一个的基数等于 $c$, 则 $\bigcup_{i=1}^{\infty} A_i$ 的基数是 ${c}$.
  - 定理 4: 设 $M$ 是任意的一个集合,如果用$\mathscr{M}$表示 $M$ 的全体子集构成的集合, 则 $\overline{\mathscr{M}}>\overline{\bar{M}}$.



#### 3.2 极限定义

- 【例题】设 $\lim _{n \rightarrow \infty} a_n=a$, 证明: $\lim _{n \rightarrow \infty} \frac{a_1+a_2+\cdots+a_n}{n}=a$.
  证明: 因 $\lim _{n \rightarrow \infty} a_n=a$, 故 $\forall \varepsilon>0, \exists N_1 \in N^{+}$, s.t. 当 $n>N_1$ 时, 有 $\left|a_n-a\right|<\frac{\varepsilon}{2}$. 又知

$$
\begin{aligned}
&\left|\frac{a_1+a_2+\cdots+a_n}{n}-a\right| \\
=&\left|\frac{\left(a_1-a\right)+\left(a_2-a\right)+\cdots+\left(a_{N_1}-a\right)+\left(a_{N_1+1}-a\right)+\cdots+\left(a_n-a\right)}{n}\right| \\
\leq &\left|\frac{\left(a_1-a\right)+\left(a_2-a\right)+\cdots+\left(a_{N_1}-a\right)}{n}\right|+\left|\frac{\left(a_{N_1+1}-a\right)+\cdots+\left(a_n-a\right)}{n}\right| \\
& \leq \frac{\left(a_1-a\right)+\left(a_2-a\right)+\cdots+\left(a_{N_1}-a\right)}{n} \mid+\frac{n-N_1}{n} \frac{\varepsilon}{2}
\end{aligned}
$$
因上式右端第一项的分子是定值, 故 $\exists N_2 \in N^{+}$, s.t. 当 $n>N_2$ 时
$$
\left|\frac{\left(a_1-a\right)+\left(a_2-a\right)+\cdots+\left(a_{N_1}-a\right)}{n}\right|<\frac{\varepsilon}{2},
$$
由上述可得, $\forall \varepsilon>0$, 取 $N=\max \left\{N_1, N_2\right\}$, 当 $n>N$ 时, $\left|\frac{a_1+a_2+\cdots+a_n}{n}-a\right|<\varepsilon .$由定义, 问题得证.

【类似】设 $x_n>0, n=1,2, \cdots, \lim _{n \rightarrow \infty} x_n=A>0, y_n=\sqrt[n]{x_1 x_2 \cdots x_n}$. 则可得$\lim _{n \rightarrow \infty} y_n=A$；
- 【例题】 $\lim _{n \longrightarrow \infty} \frac{n^k}{a^n}=0, \quad a>1$;
  证法 当 $k \leq 0$ 时, 结论显然成立.
  当 $k=1$ 时, 由 $a>1$, 故可令 $a=1+\lambda(\lambda>0)$, 则 $a^n=(1+\lambda)^n>\frac{n(n-1)}{2} \lambda^2(n>2)$. 于是
  $$
  0 \leq \frac{n}{a^n}<\frac{2 n}{n(n-1) \lambda^2} \longrightarrow 0(n \longrightarrow \infty)
  $$
  结论亦成立.
  当 $0<k<1$ 时, 由
  $$
  0 \leq \frac{n^k}{a^n}<\frac{n}{a^k},
  $$
  及 $k=1$ 的结论有 $\lim _{n \longrightarrow \infty} x_n=0$.
  当 $k>1$ 时, 由
  $$
  0 \leq \frac{n^k}{a^n}=\left[\frac{n}{\left(a^{1 / k}\right)^n}\right]^k
  $$
  且 $a>1, a^{1 / k}>1$, 由 $k=1$ 的结论有 $\lim _{n \longrightarrow \infty} x_n=0$.



#### 3.3  重要极限

- $e$

  - 【例题】设 $x_n=\left(1+\frac{1}{n}\right)^n, y_n=\left(1+\frac{1}{n}\right)^{n+1}, n=1,2, \cdots$ 试证明数列 $\left\{x_n\right\},\left\{y_n\right\}$ 有相同的极限.
    
  - 【例题】 求证 $\lim _{x \rightarrow-\infty}\left(1+\frac{1}{x}\right)^x=\mathrm{e}$.
    证明：作变量替换 $y=-(x+1)$，合在一起给出 $\lim _{x \rightarrow \infty}\left(1+\frac{1}{x}\right)^x=e$.
    
  - 【例题】求证 $\lim _{x \rightarrow 0}(1+x)^{1 / x}=\mathrm{e}$.
    证明 作变量替换 $y=\frac{1}{x}$
    
  - 【结论】实际上，只要是$\lim _{x \rightarrow \infty}f(x)=0$就有$\lim _{x \rightarrow \infty}\left(1+f(x)\right)^{\frac{1}{f(x)}}=e$.
  
  - 【例题】求 $\lim _{x \rightarrow 0}(\cos x)^{\frac{1}{x^2}}$.
    解 首先看出这个问题是 $1^{\infty}$ 型的不定式, 因此可以试用上述第二个重要极 限. 改写原问题如下:
    $$
    \begin{aligned}
    \lim _{x \rightarrow 0}(\cos x)^{\frac{1}{x^2}} &=\lim _{x \rightarrow 0}\left(1-2 \sin ^2 \frac{x}{2}\right)^{\frac{1}{x^2}} \\
    &=\lim _{x \rightarrow 0}\left(1-2 \sin ^2 \frac{x}{2}\right)^{\frac{1}{-2 \sin ^2 \frac{x}{2}}} \cdot \frac{-2 \sin ^2 \frac{x}{2}}{x^2}
    \end{aligned}
    $$
    由于 $\lim _{x \rightarrow 0} \frac{2 \sin ^2 \frac{x}{2}}{x^2}=\lim _{x \rightarrow 0}\left(\frac{\sin \frac{x}{2}}{\frac{x}{2}}\right)^2 \cdot \frac{1}{2}=\frac{1}{2}$, 因此答案是 $\mathrm{e}^{-1 / 2}$.
  
  - 【例题】求 $\lim _{x \rightarrow \infty}\left(\sin \frac{1}{x}+\cos \frac{1}{x}\right)^x$
    解：与上一题类似地可将原式改写如下:
    $$
    \begin{aligned}
    &\lim _{x \rightarrow \infty}\left[1+\left(\sin \frac{1}{x}+\cos \frac{1}{x}-1\right)\right]^x \\
    &=\lim _{x \rightarrow \infty}\left[1+\left(\sin \frac{1}{x}+\cos \frac{1}{x}-1\right)\right]^{\frac{x}{\sin \frac{1}{x}+\cos \frac{1}{x}-1} \cdot\left(\sin \frac{1}{x}+\cos \frac{1}{x}-1\right)}
    \end{aligned}
    $$
    可见只要计算出
    $$
    \lim _{x \rightarrow \infty} x\left(\sin \frac{1}{x}+\cos \frac{1}{x}-1\right)=\lim _{x \rightarrow \infty}\left(\frac{\sin \frac{1}{x}}{\frac{1}{x}}-\frac{2 \sin ^2 \frac{1}{2 x}}{\frac{1}{2 x} \cdot 2}\right)=1,
    $$
    即知原问题的答案为 $e$.
  
- 欧拉常数$c$

- $\lim _{x \rightarrow 0} \frac{\sin x}{x}=1$.
  证明：先设 $x \in\left(0, \frac{\pi}{2}\right)$， 得 $\frac{1}{2} \sin x<\frac{1}{2} x<\frac{1}{2} \tan x$ 。由于 $\cos x, \frac{\sin x}{x}$ 和 1 都是偶函数, 故上述不等式当 $x \in\left(-\frac{\pi}{2}, 0\right)$ 时仍然成立. 从 而当 $0<|x|<\frac{\pi}{2}$ 时, 有
  $$
  \left|\frac{\sin x}{x}-1\right|<1-\cos x=2 \sin ^2 \frac{x}{2} \leq 2\left(\frac{x}{2}\right)^2 \leq \frac{x^2}{2} .
  $$
  由夹挤定理即得所欲证者.



#### 3.4 子数列

- 定义：设 $\left\{x_n\right\}$ 为一个数列, $\left\{n_k\right\}$ 为严格遂增的正整数列. 称 $\left\{x_{n_k}\right\}$ 为 $\left\{x_n\right\}$ 的一个子数列.
  例如, $\left\{x_{2 n-1}\right\},\left\{x_{2 n}\right\},\left\{x_{3 n}\right\},\left\{x_{n^2}\right\}$ 等等都是 $\left\{x_n\right\}$ 的子数列. 易见, 如果数 列 $\left\{x_n\right\}$ 收玫于 $A$, 则其任何子数列都收敛于 $A$.

- 定理 ： (Bolzano-Weierstrass 定理) 任何有界数列必有收敛的子数列.

- 【例题】用子数列收敛定理证明 Cauchy 准则的充分性（Cauchy列必收敛）
  设 $\left\{x_n\right\}$ 为 Cauchy 数列, 则 $\left\{x_n\right\}$ 为有界数列. 据子数列收敛定理可知, 存在子数列 $\left\{x_{n_k}\right\}$, 使得
  $$
  \lim _{k \rightarrow \infty} x_{n_k}=A
  $$
  对某个常数 $A$ 成立. 由极限的定义, 对任意给定的正数 $\varepsilon>0$, 存在正整数 $k$, 使 得
  $$
  \left|x_{n_k}-A\right|<\varepsilon, \quad \forall k>K .
  $$
  另一方面, 由于 $\left\{x_n\right\}$ 为 Cauchy 数列, 对上述的 $\varepsilon$, 存在正整数 $N$, 使得
  $$
  \left|x_m-x_n\right|<\varepsilon, \quad \forall m, n \geq N .
  $$
  不妨设 $N>K$. 注意 $n_N \geq N$, 我们有
  $$
  \left|x_n-A\right| \leq\left|x_n-x_{n_N}\right|+\left|x_{n_N}-A\right|<2 \varepsilon, \quad \forall n>N \text {. }
  $$
  这就证明了 $\lim _{n \rightarrow \infty} x_n=A$.

- 【例题】数列 $\left\{x_n\right\}$ 以 $A$ 为极限的充分必要条件是, 它的任何子数列都有 以 $A$ 为极限的子数列.
  证明 必要性是显然的, 只须证明充分性. 用反证法. 假设 $\left\{x_n\right\}$ 不以 $A$ 为 极限, 则如上所述, 存在 $\varepsilon_0>0$ 和子数列 $\left\{x_{n_k}\right\}$, 使得
  $$
  \left|x_{n_k}-A\right| \geq \varepsilon_0, \quad \forall k \in \mathbb{N}^* .
  $$
  由假设, $\left\{x_{n_k}\right\}$ 有子数列 $\left\{x_{n_{k_i}}\right\}$ 收敛于 $A$. 但这个子数列仍然满足
  $$
  \left|x_{n_{k_2}}-A\right| \geq \varepsilon_0, \quad \forall i \in \mathbb{N}^*
  $$
  从而有
  $$
  0=\lim _{i \rightarrow \infty}\left|x_{n_{k_i}}-A\right| \geq \varepsilon_0,
  $$
  与 $\varepsilon_0>0$ 矛盾. 证毕.

- 定理：数列 $\left\{x_n\right\}$ 无界的充分必要条件是, 它存在一个子数列 $\left\{x_{n_h}\right\}$, 使得$\lim _{k \rightarrow \infty}\left|x_{n_k}\right|=+\infty$.

- 【例题】设 $\left\{x_n\right\}$ 为有界数列, $A \in \mathbb{R} .\left\{x_n\right\}$ 不以 $A$ 为极限的充分必要条 件是它有一个收敛的子数列 $\left\{x_{n_k}\right\}$, 使得 $\lim _{k \rightarrow \infty} x_{n_k} \neq A$.
  证明 充分性是显然的, 只证必要性. 由极限的定义, 存在正数 $\varepsilon_0$, 及子列 $\left\{x_{n_k}\right\}$, 使得
  $$
  \left|x_{n_k}-A\right| \geq \varepsilon_0, \quad \forall k \in \mathbb{N}^* .
  $$
  由于 $\left\{x_{n_k}\right\}$ 仍然是有界数列, 由子数列收玫定理可知, 存在 $\left\{x_{n_k}\right\}$ 的一个子数 列, 仍记为 $\left\{x_{n_k}\right\}$, 使得 $\lim _{k \rightarrow \infty} x_{n_k}=B$ 存在. 在上式中令 $k \rightarrow \infty$, 得
  $$
  |B-A| \geq \varepsilon_0 .
  $$

- 【例题】有界数列 $\left\{x_n\right\}$ 发散的充分必要条件是它有两个收敛于不同极限的 子数列 $\left\{x_{m_k}\right\}$ 和 $\left\{x_{n_k}\right\}$.
  证明：充分性也是显然的, 只证必要性. 既然 $\left\{x_n\right\}$ 发散, 那它就不以 0 为 极限. 据定理 6.4, 它有一收敛子数列 $\left\{x_{m_k}\right\}$, 使得 $\lim _{k \rightarrow \infty} x_{m_k}=A \neq 0$. 当然 $\left\{x_n\right\}$ 也不以 $A$ 为极限. 再据定理 6.4, 它又有一收敛子数列 $\left\{x_{n_k}\right\}$, 使得 $\lim _{k \rightarrow \infty} x_{n_k} \neq A$, 即
  $$
  \lim _{k \rightarrow \infty} x_{m_k} \neq \lim _{k \rightarrow \infty} x_{n_k} .
  $$







#### 3.5 实数4个基本定理

- 单调有界原理：

  - 单调有界原理: 任何单调有界的数列必有极限, 可推广到从 $N_0$ 往后单调即可. 单调有界包括: 单调上升有上界和单调下降有下界.
    判定方法: $x_{n+1}-x_n \geq 0, \nearrow$. 若为正数列, 也可用 $\frac{x_{n+1}}{x_n} \geq 1$ 判断. $x_{n+1}-x_n \leq 0, \searrow$. 若为正数列, 也可用 $\frac{x_{n+1}}{x_n} \leq 1$ 判断.
  - 【例题】设 $\lim _{n \rightarrow \infty}\left(x_{n+1}-x_n\right)=0$. 若还分别满足以下条件之一, 能否断定 $\left\{x_n\right\}$ 收敛?
    (1) $\left\{x_n\right\}$ 是单调的;
    (2) $\left\{x_n\right\}$ 是有界的;
    (3) $\left\{x_{2 n}\right\}$ 和 $\left\{x_{2 n+1}\right\}$ 分别是单调的;
    (4) $\left\{x_{2 n}\right\}$ 和 $\left\{x_{2 n+1}\right\}$ 分别是递增和递减的;
    (5) $\left\{x_{2 n}\right\}$ 和 $\left\{x_{2 n+1}\right\}$ 之一是收敛的.
    答: $(1)(2)(3)$ 均不能保证 $\left\{x_n\right\}$ 收玫. 分别举例如下:
    (1): $x_n=\sqrt{n}$, 则 $x_{n+1}-x_n=\frac{1}{\sqrt{n+1}+\sqrt{n}} \rightarrow 0, x_n$ 单调, 但 $x_n \rightarrow \infty$.
    (2): $x_n=\sin \sqrt{n}$.
    (3): 可取(1)相同的例子.
    (4)和(5)可保证 $\left\{x_n\right\}$ 收敛, 我们先证明(4) $\Longrightarrow(5)$.
    不妨设 $x_{2 n} \nearrow, x_{2 n+1} \searrow$, 则有 $x_{2 n} \leq x_{2 n+1}(n=1,2, \cdots)$. 因为若存在 $k$, 使得 $x_{2 k}>x_{2 k+1}$, 则对一切 $n>k$, 必有
  
  $$
  x_{2 n} \geq x_{2 k}>x_{2 k+1} \geq x_{2 n+1}, x_{2 n}-x_{2 n+1} \geq x_{2 k}-x_{2 k+1}>0,
  $$
  与 $x_{2 n}-x_{2 n+1} \rightarrow 0$ 矛盾.
  于是 $x_2 \leq x_{2 n} \leq x_{2 n+1} \leq x_1$, 即 $\left\{x_{2 n}\right\}$ 和 $\left\{x_{2 n+1}\right\}$ 均是单调有界数列, 都收敛
  再证(5)：
  若 $\left\{x_{2 n}\right\}$ 和 $\left\{x_{2 n+1}\right\}$ 之一收玫, 不妨设 $\lim _{n \rightarrow \infty} x_{2 n}=l$, 通过四则运算可知:
  $$
  x_{2 n+1}=\left(x_{2 n+1}-x_{2 n}\right)+x_{2 n} \rightarrow l(n \rightarrow \infty) .
  $$
  即有 $\lim _{n \rightarrow \infty} x_{2 n}=\lim _{n \rightarrow \infty} x_{2 n+1}=l$, 由此可得 $\lim _{n \rightarrow \infty} x_n=l$. 
  
- Cauchy准则：
  
  - 设 $\left\{x_n\right\}$ 为一数列. 如果对任意给定的 $\varepsilon>0$, 都存在正整数 $N$, 使得$\left|x_m-x_n\right|<\varepsilon, \quad \forall m \geq n>N,$则 $\left\{x_n\right\}$ 为 Cauchy 数列.
  
    如果 $\left\{x_n\right\}$ 是一 Cauchy 数列, 则按定义 (取 $\varepsilon=1$ ), 应存在正整数 $N$, 使 得
    $$
    \left|x_m-x_n\right|<1, \quad \forall m \geq n>N .
    $$
    特别, 取 $n=N+1$, 就有
    $$
    \left|x_m-x_{N+1}\right|<1, \quad \forall m>N .
    $$
    从而
    $$
    \text { 令 } M=1+\sum_{k=1}^{N+1}\left|x_k\right| \text {, 则 } \quad\left|x_m\right|<1+\left|x_{N+1}\right|, \quad \forall m>N .
    $$
    这就是说, Cauchy 数列一定有界.
    所谓 “ $\left\{x_n\right\}$ 为 Cauchy 数列”, 也就是, 对任意给定的 $\varepsilon>0$, 存在正整数 $N$, 使得
    $$
    \sup _{p \geq 0}\left|x_{n+p}-x_n\right|=\sup _{m \geq n}\left|x_m-x_n\right| \leq \varepsilon, \quad \forall n>N .
    $$
  
  - 设 $\left\{x_n\right\}$ 为一有界数列. 定义$\omega\left(x_n\right)=\sup _{p \geq 0}\left|x_{n+p}-x_n\right|$,称 $\left\{\omega\left(x_n\right)\right\}$ 为数列 $\left\{x_n\right\}$ 的振幅数列.
  
  - 数列 $\left\{x_n\right\}$ 为 Cauchy 数列的充分必要条件是 $\left\{x_n\right\}$ 有界, 而且$\lim _{n \rightarrow \infty} \omega\left(x_n\right)=0$；
  
  - (Cauchy 收敛准则) 数列收敛的充分必要条件是它是 Cauchy 数列.
  
  - 【例题】设 $x_n=\sum_{k=1}^n(-1)^{k+1} \frac{1}{k}, n=1,2, \cdots$. 试证明数列 $\left\{x_n\right\}$ 有极限. 证明对任何正整数 $n, p$, 有
    $$
    \left|x_{n+p}-x_n\right|=\left|\sum_{k=n+1}^{n+p}(-1)^{k+1} \frac{1}{k}\right| \leq \frac{1}{n+1} .
    $$
    于是
    $$
    \omega\left(x_n\right)=\sup _{p \geq 0}\left|x_{n+p}-x_n\right| \leq \frac{1}{n+1} .
    $$
    因此, $\lim _{n \rightarrow \infty} \omega\left(x_n\right)=0$. 可知 $\lim _{n \rightarrow \infty} x_n$ 存在. 
  
  - 【例题】设 $x_n=\sum_{k=1}^n \frac{1}{k}, n=1,2, \cdots$. 证明数列 $\left\{x_n\right\}$ 发散.
  
    证明 对任何正整数 $n, p$, 有
    $$
    \left|x_{n+p}-x_n\right|=\sum_{k=n+1}^{n+p} \frac{1}{k} .
    $$
    于是
    $$
    \omega\left(x_n\right)=\sup _{p \geq 0}\left|x_{n+p}-x_n\right| \geq \sum_{k=n+1}^{2 n} \frac{1}{k} \geq \frac{n}{2 n}=\frac{1}{2} .
    $$
    因此, $\lim _{n \rightarrow \infty} \omega\left(x_n\right) \neq 0$. 可知 $\lim _{n \rightarrow \infty} x_n$ 不存在.
  
- 闭区间套定理：
  a. $\left[a_n, b_n\right] \supset\left[a_{n+1}, b_{n+1}\right], n \in N^*$;
  b. $\lim _{n \rightarrow \infty}\left(b_n-a_n\right)=0$.
  则存在唯一的一点 $c \in\left[a_n, b_n\right](n \geq 1)$, 使得 $c=\lim _{n \rightarrow \infty} a_n=\lim _{n \rightarrow \infty} b_n$.

- 确界原理：

  - 如果数集中的元素是有限数，可以写max，否则要注意只能写sup；

  - 定理 $3.2$ (确界原理) 任何非空的有上界的数集必有上确界.
  - 定理 $3.3$ 确界原理蕴含单调有界原理。单调递增的有界数列的上确界就是它的极限, 而下确界自然就是首项. 同样, 单调递减的有界数列的极限是其下确界, 首项是其上确界.
  - 【例题】设数集 $S$ 有上界 $\xi=\sup S$.求证: 若 $\xi \notin S$, 则存在严格递增的数列 $\left\{a_n\right\} \subset S$, 使 $\lim _{n \rightarrow \infty} a_n=\xi$.
    证明: 取 $\alpha_1=\xi-1$, 由上确界的定义可知 $\exists a_1 \in S$, s.t. $\alpha_1<a_1$. 由于 $\xi \notin S$, 故

  $$
  \xi-1<a_1<\xi .
  $$
  取 $\alpha_2=\max \left\{\xi-\left(\xi-a_1\right), \xi-\frac{1}{2}\right\}, \exists a_2 \in S$, 使得 $\alpha_2<a_2<\xi$, 即同时满足
  $$
  \xi-\frac{1}{2}<a_2<\xi \quad \text { 和 } \quad a_1<a_2 .
  $$
  同理, 在找出 $a_{n-1}$ 之后, 取 $\alpha_n=\max \left\{a_{n-1}, \xi-\frac{1}{n}\right\}$, 则 $\exists a_n \in S$, 同时满足
  $$
  \xi-\frac{1}{n}<a_n<\xi, \quad a_{n-1}<a_n, \quad n=1,2, \cdots
  $$
  显然数列 $\left\{a_n\right\} \subset S$ 严格递增, 且
  $$
  \lim _{n \rightarrow \infty} a_n=\xi
  $$





#### 3.6 求极限的一些方法总结【补充】

- 根式有理化：【例题】 $\lim _{n \longrightarrow \infty}(\sqrt{n+2}-2 \sqrt{n+1}+\sqrt{n}) \sqrt{n^3}$; 解 多次利用分子有理化: $-\frac{1}{4}$.

- Stolz 定理：条件：(1) $\left\{y_n\right\}$ 严格单调且趋于正无穷；(2) $\lim _{n \rightarrow \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}=A$：结论： $\lim _{n \longrightarrow \infty} \frac{x_n}{y_n}=A$.

  - 【例题】计算 $\lim _{n \longrightarrow \infty}\left(\frac{1}{n}-\frac{1}{2 n}+\frac{1}{3 n}-\cdots+(-1)^{n+1} \frac{1}{n^2}\right)$. 证法一 (利用夹挤定理) 令 $x_n=\frac{1}{n}-\frac{1}{2 n}+\frac{1}{3 n}-\frac{1}{4 n}+\cdots+(-1)^{n+1} \frac{1}{n^2}$, $y_n=-\frac{1}{n}-\frac{1}{2 n}-\cdots-\frac{1}{n^2}, z_n=\frac{1}{n}+\frac{1}{2 n}+\cdots+\frac{1}{n^2}$. 易得 $y_n<x_n<z_n$. 且

  $$
  z_n=\frac{1}{n}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}\right)=\frac{1}{n}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}-\ln n\right)+\frac{\ln n}{n},
  $$
  可得 $\lim _{n \longrightarrow \infty} z_n=\lim _{n \longrightarrow \infty} \frac{c}{n}+\lim _{n \longrightarrow \infty} \frac{\ln n}{n}=0$. 同理 $\lim _{n \longrightarrow \infty} y_n=0$.由夹挤定理可 得 $\lim _{n \longrightarrow \infty} x_n=0$；

  证法二(利用Stolz定理)令 $x_n=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots+(-1)^{n+1} \frac{1}{n}, y_n=n$, 易知 $\left\{y_n\right\}$ 严格单调 且趋于无穷. 且有
  $$
  \lim _{n \longrightarrow \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}=\lim _{n \longrightarrow \infty}(-1)^{n+2} \frac{1}{n+1}=0 .
  $$
  利用stolz定理有 $\lim _{n \longrightarrow \infty} \frac{x_n}{y_n}=0$.

  - 【例题】设 $a_1>0, a_{n+1}=a_n+\frac{1}{a_n}, n \in \mathbf{N}_{+}$, 证明 $\lim _{n \rightarrow \infty} \frac{a_n}{\sqrt{2 n}}=1$.
    证：首先可看出 $\left\{a_n\right\}$ 为严格单调增加的正数列. 因此只有两种可能. 假定 它有极限 $a$, 在递推公式
    $$
    a_{n+1}=a_n+\frac{1}{a_n}
    $$
    的两边令 $n \rightarrow \infty$, 得到 $a=a+1 / a$, 这对任何有限数 $a$ 都不可能成立. 因此知道 $\left\{a_n\right\}$ 只能是正无穷大量.
    然后根据 2.1.5 小节的练习题 2, 只要用 Stolz 定理计算如下:
    $$
    \lim _{n \rightarrow \infty} \frac{a_n^2}{2 n}=\lim _{n \rightarrow \infty} \frac{a_{n+1}^2-a_n^2}{2(n+1)-2 n}=\frac{1}{2} \lim _{n \rightarrow \infty}\left(2+\frac{1}{a_n^2}\right)=1 .
    $$

  - 

- Cauchy判别法

- 等价无穷小（当$x$趋近于0的时候）$x // sinx // ln(1+x) // e^{x}-1 // tanx // arcsin(x)$

  【例题】 $\lim _{x \rightarrow 0} \frac{\ln \left(1+2 x^2\right)}{\tan ^2 x}=2$





【总结】

- 判定数列发散的方法
  - 无界数列一定发散.
  - 从数列收敛的定义出发, 用对偶法则就可得到 :$\left\{a_n\right\}$ 发散 $\Longleftrightarrow \forall a, \exists \varepsilon_0, \forall N, \exists n>N$, 使得 $\left|a_n-a\right| \geqslant \varepsilon_0$.
  - 有一个发散子列的数列一定发散.
  - 如果发现有两个子列不可能收敛于相同极限, 则这个数列一定发散.
  - Cauchy 收敛准则也是判定数列发散的充分必要条件.
