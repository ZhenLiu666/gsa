《高等数学A》第二次习题课

> Author ZhenLiu
>
> 2022/09/13



> 以极限为工具，以$\R^{n}$为平台，以函数为对象。



#### 2.1 集合

- 定义与表示；

- 关系；

- 交运算和无穷交；

- 并运算和无穷并；

- 余集：德摩根公式：$\left(\bigcup_{\lambda \in \Lambda} A_\lambda\right)^c=\bigcap_{\lambda \in \Lambda} A_\lambda^c,\left(\bigcap_{\lambda \in \Lambda} A_\lambda\right)^c=\bigcup_{\lambda \in \Lambda} A_\lambda^c$；

- 运算公式：$A \cap\left(\bigcup_{\lambda \in A} B_\lambda\right)=\bigcup_{\lambda \in \Lambda}\left(A \cap B_\lambda\right)$.

- 集合的上下极限：

  - 对于一串给定的集合 $A_1, A_2, \cdots, A_n, \cdots$. 我们定义$\left\{x\right.$; 有无穷多个 $n$, 使 $\left.x \in A_n\right\}$为这串集合的上极限, 记为或 $\operatorname{\varlimsup}_n A_n$或者$\limsup_n A_n$.
  - 定义$\left\{x\right.$; 只有有限多个 $n$, 使 $\left.x \bar{\in} A_n\right\}$为这串集合的下极限, 记为 $\varliminf_n A_n$ 或 $\underset{n}{\liminf } A_n$. 
  - $\underset{n}{\liminf } A_n \subset \limsup _n A_n$；
  - 设 $A_n=\left[\frac{1}{n}, 3+(-1)^n\right], n=1,2,3, \cdots$, $\liminf _n A_n=(0,2], \quad \limsup _n A_n=(0,4]$. 这时 $\liminf _n A_n \neq \limsup _n A_n$.
  - 如果一串集合 $A_1, A_2, \cdots, A_n, \cdots$ 的上、下极限相同, 则我们就 说这串集含是有极限的或收敛的, 并且我们把 $\limsup _n$ (也就是 $\liminf _n A_n$ ）记为 $\lim _n A_n$, 称为其极限；
- 基数：

  - 定义 设 $A, B$ 是两个集合, 如果存在二者元素之间的一个对应关系 $\varphi$, 使 $A$ 中任意元素 $x$, 通过 $\varphi$ 都恰与 $B$ 中一个元素 $y$ 对应，而 $B$ 中任意的 $y$ 也一定是 $A$ 中某一 $x$ (通过 $\varphi$ ) 在 $B$ 中的对应元素, 则我们就说 $A$ 和 $B$ 是对等的或具有相同的基数，记为 $A \sim B$ 。而满足上述条件的对应 $\varphi$ 称之为 $A$ 和 $B$ 之间的一个 $1-1$ 对应.（注意 $A \sim B$ 和 $A=B$ 不同）；
  - 集合 $A$ 的基数记为 $\overline{\bar{A},} A$ 和 $B$ 的基数相同便可记为 $\overline{\bar{A}}=\overline{\bar{B}}$. 显然基数的相等是具有对称性和传递性的. 即如果 $\overline{\bar{A}}=\overline{\bar{B}}$ 则 $\overline{\bar{B}}=\overline{\bar{A}}$; 如果 $\overline{\bar{A}}=\overline{\bar{B}}, \overline{\bar{B}}=\overline{\bar{C}}$, 则 $\overline{\bar{A}}$ $=\overline{\bar{C}}$ (集合的基数也称为集合的势或权)；
  - 例 1 设 $B$ 是全体正整数所作成的集合, $A$ 是全体偶数所作 成的集合, 则 $A \sim B$. 因为只要令 $B$ 中的 $n$ 与 $A$ 中的 $2 n$ 对应, 即 可建立一个 $B$ 和 $A$ 之间的 1-1 对应.
  - 例 2 设 $A$ 是 $(0,1)$ 开区间中所有的点所作成的集合, $B$ 是半.轴 $(0, \infty)$ 上所有的点所作成的集合, 则 $A \sim B$.
  - 无穷集合定义：它本身的一个真子集对等的集合；
  - Cantor定理： $[0,1]$ 闭区间上所有的点作成的点集是不能和由全.体正整数所作成的集合 $\mathbf{N}$ 对等的.
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



#### 2.2 确界

- 如果数集中的元素是有限数，可以写max，否则要注意只能写sup；

- 上下界：

  - 考虑非空数集 $X$. 如果存在常数 $M$, 使对任何 $x \in X$, 都有 $x \leq M$, 则称数集 $X$ 是有上界的, 并称 $M$ 为 $X$ 的一个上界. 
  - 类似地, 如果存在常数 $m$, 使对 任何 $x \in X$, 都有 $x \geq m$, 则称数集 $X$ 是有下界的, 并称 $m$ 为 $X$ 的一个下界. 
  - 如果数集 $X$ 既有上界又有下界, 则称该数集为有界数集.

- 上下确界：

  - 定义 $3.1$ 对于一个有上界的数集 $X$, 如果存在最小的上界 $M$, 则称 $M$ 为数集 $X$ 的上确界, 记为 $M=\sup X$. 
  - 类似地, 对于一个有下界的数集 $X$, 如果存 在最大的下界 $m$, 则称 $m$ 为数集 $X$ 的下确界, 记为 $m=\inf X$.
  - 如果数集 $X$ 没有上界, 则记 $\sup X=+\infty$. 同样, 如果数集 $X$ 没有下界, 则记 $\inf X=-\infty$.
  - 注意, 集合 $X$ 的上确界与最大元有联系, 但却不是一回事. 当集合 $X$ 的最 大元存在时, 它就是该集合的上确界。但在最大元不存在时, 只要集合是上方有界的, 它就总有上确界。下确界与最小元的关系也完全类似。
    事实上, $M$ 是集合 $X$ 的上确界, 这有两层意义:
    (i) $M$ 是 $X$ 的上界, 即对 $\forall x \in X$, 都有 $x \leq M$;
    (ii) $M$ 是 $X$ 的所有上界中最小的, 即任何小于 $M$ 的数都不是 $X$ 的上界, 亦即对 $\forall \varepsilon>0$, 都存在 $x^{\prime} \in X$, 使得 $x^{\prime}>M-\varepsilon$.

- 命题 $3.1$ 设 $X, Y$ 为两个非空有界数集, 则
  
  -  $\inf (X+Y)=\inf X+\inf Y$;
  
  -  $\sup (X+Y)=\sup X+\sup Y$.
  
  - 这里记号 $X+Y$ 表示数集 $\{x+y ; x \in X, y \in Y\}$.
  
- 推论 $3.1$ 设 $X$ 为非空有界数集, $a$ 为常数, 则
  $$
  \sup (a+X)=a+\sup X, \inf (a+X)=a+\inf X,
  $$
  这里记号 $a+X$ 表示数集 $\{a+x ; x \in X\}$.

- 命题 $3.2$ 设 $X, Y$ 为两个非空有界数集, 则$\inf (X+Y) \leq \inf X+\sup Y \leq \sup (X+Y)$；

- 命题 $3.3$ 设 $\left\{x_n\right\},\left\{y_n\right\}$ 是两个有界数列, 满足下述条件:
  $$
  x_n \leq y_n, \quad \forall n \in N,
  $$
  则 $\sup _{n \in N} x_n \leq \sup _{n \in N} y_n, \inf _{n \in N} x_n \leq \inf _{n \in N} y_n$.

- 定理 $3.2$ (确界原理) 任何非空的有上界的数集必有上确界.

- 定理 $3.3$ 确界原理蕴含单调有界原理。单调递增的有界数列的上确界就是它的极限, 而下确界自然就是首项. 同样, 单调递减的有界数列的极限是其下确界, 首项是其上确界.





#### 2.3 映射

- 定义域，对应法则，值域
- 单射，满射，双射
- 线性映射
- 复合映射
- 向量空间



#### 2.4 极限定义

- 演示：利用xy平面上$\varepsilon$带进行演示 // 利用区间方法说明 // 利用集合极限的定义引申；
- 数列 $\left\{x_n\right\}$ 以 $A$ 为极限: $\forall \varepsilon>0, \exists N_{\varepsilon} \in N^*$, s.t. 当 $n>N_{\varepsilon}$ 时 $\left|x_n-A\right|<\varepsilon$. 
- 数列 $\left\{x_n\right\}$ 不以 $A$ 为极限: $\exists \varepsilon>0, \forall N_{\varepsilon} \in N^*$,  $\exists n_{0}>N_{\varepsilon}$ 时 $\left|x_{n0}-A\right| \geq \varepsilon$. 
- 数列 $\left\{x_n\right\}$ 发散: $\forall A \in R,\left\{x_n\right\}$ 不以 $A$ 为极限.
- 数列无界必定没有极限，但是和数列趋于无穷是不同的概念。
- 【例题】求证 $x_n=n^{(-1)^n}(n=1,2, \cdots)$ 无界, 但当 $n \rightarrow \infty$ 时, 它并不趋于 $\infty$. 证明 因为

$$
x_n=n^{(-1)^n}= \begin{cases}2 k, & n=2 k, k \text { 为正整数, } \\ \frac{1}{2 k-1}, & n=2 k-1\end{cases}
$$
所以 $x_{2 k} \rightarrow \infty, x_{2 k-1} \rightarrow 0(k \rightarrow \infty)$.由于 $x_{2 k} \rightarrow \infty$ 故 $x_n$ 无界, 但因 $x_{2 k-1} \rightarrow 0$ 故 $x_n$ 并不趣于 $\infty$.

- 【例题】下述几种说法与数列极限定义是否等价? 

  (1) 对任给的 $\varepsilon>0$, 存在正整数 $N$, 当 $n \geq N$ 时, $\left|x_n-A\right| \leq \varepsilon$.
  (2) 存在正整数 $N$, 对任给的 $\varepsilon>0$, 当 $n>N$ 时, $\left|x_n-A\right|<\varepsilon$;
  (3)对 $\forall 0<\varepsilon<1$, 存在正整数 $N$, 当 $n>N$ 时, $\left|x_n-A\right|<\varepsilon$;
  (4) 对 $\forall \varepsilon>0$, 存在正整数 $N$, 当 $n>N$ 时, $\left|x_n-A\right|<k \varepsilon$, 此处 $k$ 是与 $\varepsilon$ 无关的正数;
  (5) 对任给的正整数 $m$, 存在正整数 $N$, 当 $n>N$ 时, $\left|x_n-A\right|<\frac{1}{m}$;
  (6) 对 $\forall \varepsilon>0$, 存在无限多个 $x_n$, 满足 $\left|x_n-A\right|<\varepsilon$.
  (1)(3)(4)(5) 都与数列极限的定义等价, (2)(6)不等价.
  (定义中强调 $\varepsilon$ 的任意性, $N$ 的存在性, (1)(3)(4)(5)注重理解, (2)(6) 举反例).

- 【例题】用定义证明 $\lim _{n \rightarrow \infty} \frac{7 n^3+3 n^2+6 n-2}{5 n^3+4 n^2-2 n+9}=\frac{7}{5}$.
  证明: $\forall \varepsilon>0$, 取 $N=\max \left\{2,\left[\frac{13}{25 \varepsilon}\right]+1\right\}$, 当 $n>N$ 时,
  $$
  \left|\frac{7 n^3+3 n^2+6 n-2}{5 n^3+4 n^2-2 n+9}-\frac{7}{5}\right|=\left|\frac{13 n^2-44 n+73}{25 n^3+20 n^2-10 n+45}\right|<\frac{13 n^2}{25 n^3}=\frac{13}{25 n}<\varepsilon .
  $$

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
- 【例题】证明: 数列 $\left\{2-(-1)^n\right\}$ 发散.
  证明: $\forall a \geq 2, \exists \varepsilon_0=1, \forall N \in N^*, \exists n=2 k>N\left(k \in N^*\right)$, 有
  $$
  \begin{gathered}
  \left|\left[2-(-1)^{2 k}\right]-a\right|=|1-a| \geq \varepsilon_0=1 \\
  \forall a<2, \exists \varepsilon_0=1, \forall N \in N^*, \exists n=2 k+1>N\left(k \in N^*\right), \text { 有 } \\
  \left|\left[2-(-1)^{2 k+1}\right]-a\right|=|3-a| \geq \varepsilon_0=1
  \end{gathered}
  $$
  于是, $\forall a \in R$, 有 $\lim _{n \rightarrow \infty}\left[2-(-1)^n\right] \neq a$, 即数列 $\left\{2-(-1)^n\right\}$ 发散.

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





#### 2.5 数列极限的七个性质

- 唯一性；

- 夹挤定理: 

  - $\left\{x_n\right\},\left\{y_n\right\},\left\{z_n\right\}$ 满足 $y_n \leq x_n \leq z_n, \forall n \geq N_0$ (已知正整数), 如果 $\lim _{n \rightarrow \infty} y_n=$ $\lim _{n \rightarrow \infty} z_n=A$ (某个常数), 则 $\lim _{n \rightarrow \infty} x_n=A$.
  - 【例题】求下列极限$x_n=\frac{\sqrt[3]{n^2} \sin n !}{n+1}$, 求 $\lim _{n \rightarrow \infty} x_n$：
    解: 因为 $|\sin n !| \leq 1$, 所以 $0 \leq\left|x_n\right| \leq \frac{\sqrt[3]{n^2}}{n+1} \leq \frac{1}{n^{\frac{1}{3}}}$, 而 $\lim _{n \rightarrow \infty} \frac{1}{n^{\frac{1}{3}}}=0$, 由夹挤定理知 $\lim _{n \rightarrow \infty} x_n=0$.

- 绝对值性质：

  - 数列绝对值的极限存在不代表对应数列极限存在；
  -  $\lim _{n \rightarrow+\infty}\left|x_n\right|=0 \Longleftrightarrow \lim _{n \rightarrow+\infty} x_n=0$；

- 有界性: 收敛数列必有界.

- (序关系) 设 $\lim _{n \rightarrow \infty} x_n=A, \lim _{n \rightarrow \infty} y_n=B$.

  - (i) 若 $A>B$, 则 $\exists N \in N^*$, s.t. $x_n>y_n, \forall n>N$.
  - (ii)(极限的保序性) 若 $x_n \geq y_n, \forall n \geq N_0$ (已知正整数), 则 $A \geq B$.
  - $\left(5^{\prime}\right)$ (极限的保号性) 设 $\lim _{n \rightarrow \infty} x_n=A$. 若 $x_n \geq 0, \forall n \geq N_0$, 则 $A \geq 0$.

- 四则运算: $\lim _{n \rightarrow \infty} x_n=A, \lim _{n \rightarrow \infty} y_n=B$, 则

  -  $\lim _{n \rightarrow \infty}\left(x_n \pm y_n\right)=A \pm B, \lim _{n \rightarrow \infty}\left(x_n y_n\right)=A B$. 
  - 如果 $B \neq 0$, 还有 $\lim _{n \rightarrow \infty} \frac{x_n}{y_n}=\frac{A}{B}$.
  - 注意：必须是极限都存在才能使用；必须是有限项的四则运算；

- 有界量乘以无穷小量仍为无穷小量.

  - 【例题】求下列极限$x_n=\frac{\sqrt[3]{n^2} \sin n !}{n+1}$, 求 $\lim _{n \rightarrow \infty} x_n$；
  - 主要是三角函数和其表达式的组合往往是有界的，因此可以用此方法在求解时忽略三角函数的影响；

  

  

  

- 重要关系: $\lg n<<n^k<<a^n<<n !<<n^n$, 其中 $a>1, k>0$.



#### 2.6 重要极限

- $e$

  - 【例题】设 $x_n=\left(1+\frac{1}{n}\right)^n, y_n=\left(1+\frac{1}{n}\right)^{n+1}, n=1,2, \cdots$ 试证明数列 $\left\{x_n\right\},\left\{y_n\right\}$ 有相同的极限.
    证明 对任何正整数 $n$, 利用 Bernoulli 不等式得
    $$
    \begin{aligned}
    & \frac{x_{n+1}}{x_n}=\frac{n^n(n+2)^{n+1}}{(n+1)^{2 n+1}}=\left(\frac{n^2+2 n}{(n+1)^2}\right)^n \frac{n+2}{n+1} \\
    =&\left(1-\frac{1}{n^2+2 n+1}\right)^n \frac{n+2}{n+1} \geq\left(1-\frac{n}{n^2+2 n+1}\right) \frac{n+2}{n+1} \\
    =& \frac{n^3+3 n^2+3 n+2}{n^3+3 n^2+3 n+1} \geq 1 .
    \end{aligned}
    $$
    类似地, 对任何正整数 $n \geq 2$, 利用 Bernoulli 不等式得
    $$
    \begin{aligned}
    & \frac{y_{n-1}}{y_n}=\frac{n^{2 n+1}}{(n-1)^n(n+1)^{n+1}}=\left(\frac{n^2}{n^2-1}\right)^n \frac{n}{n+1} \\
    =&\left(1+\frac{1}{n^2-1}\right)^n \frac{n}{n+1} \geq\left(1+\frac{n}{n^2-1}\right) \frac{n}{n+1} \\
    =& \frac{n^3+n^2-n}{n^3+n^2-n-1} \geq 1 .
    \end{aligned}
    $$
    因此, $\left\{x_n\right\},\left\{y_n\right\}$ 分别是递增和递减的数列. 另一方面, 对任何 $n$, 都有
    $$
    2=x_1 \leq x_n \leq y_n \leq y_1=4
    $$
    这表明 $\left\{x_n\right\},\left\{y_n\right\}$ 还是有界数列, 所以它们都是收敛数列. 由于 $y_n=x_n(1+1 / n)$, 两者的极限相等是明显的.
    记
    $$
    \mathrm{e}=\lim _{n \rightarrow \infty}\left(1+\frac{1}{n}\right)^n .
    $$
    这是一个非常重要的极限, 以后会经常用到。

  - 【例题】 求证 $\lim _{x \rightarrow-\infty}\left(1+\frac{1}{x}\right)^x=\mathrm{e}$.
    证明：作变量替换 $y=-(x+1)$, 则当 $x \rightarrow-\infty$ 时, $y \rightarrow+\infty$. 于是
    $$
    \begin{aligned}
    & \lim _{x \rightarrow-\infty}\left(1+\frac{1}{x}\right)^x=\lim _{y \rightarrow+\infty}\left(1-\frac{1}{y+1}\right)^{-(y+1)} \\
    =& \lim _{y \rightarrow+\infty}\left(\frac{y}{y+1}\right)^{-(y+1)}=\lim _{y \rightarrow+\infty}\left(1+\frac{1}{y}\right)^{y+1} \\
    =& \lim _{y \rightarrow+\infty}\left(1+\frac{1}{y}\right)^y\left(1+\frac{1}{y}\right)=\mathrm{e} .
    \end{aligned}
    $$
    合在一起给出 $\lim _{x \rightarrow \infty}\left(1+\frac{1}{x}\right)^x=e$.

  - 【例题】求证 $\lim _{x \rightarrow 0}(1+x)^{1 / x}=\mathrm{e}$.
    证明 作变量替换 $y=\frac{1}{x}$, 则当 $x \rightarrow 0$ 时, $y \rightarrow \infty$. 于是
    $$
    \lim _{x \rightarrow 0}(1+x)^{1 / x}=\lim _{y \rightarrow \infty}\left(1+\frac{1}{y}\right)^y=\mathrm{e}
    $$

  - 【结论】实际上，只要是$\lim _{x \rightarrow \infty}f(x)=0$就有$\lim _{x \rightarrow \infty}\left(1+f(x)\right)^{\frac{1}{f(x)}}=e$.

- 欧拉常数$c$

  - 【例题】证明数列

  $$
  \begin{aligned}
  &x_n=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n+1}-\ln n, \\
  &y_n=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n-1}-\ln n
  \end{aligned}
  $$
  都收敛且极限相等. 此极限值记为c, 称为Euler常数且
  $$
  c=0.5772156649 \cdots .
  $$
  证明：易得
  $$
  \begin{gathered}
  x_{n+1}-x_n=\frac{1}{n+2}-\ln \left(1+\frac{1}{n}\right)<\frac{1}{n+2}-\frac{1}{n+1}<0, \\
  y_n-y_{n+1}=-\frac{1}{n}+\ln \left(1+\frac{1}{n}\right)<-\frac{1}{n}+\frac{1}{n}=0,
  \end{gathered}
  $$
  从而可得 $\left\{x_n\right\}$ 为单调递减的数列, $\left\{y_n\right\}$ 为单调递增的数列,且利用 $x_n-y_n=\frac{1}{n}+\frac{1}{n+1}>0$ 得
  $$
  y_2<y_n<x_n<x_1 .
  $$
  即 $\left\{x_n\right\},\left\{y_n\right\}$ 均为有界数列, 利用单调有界原理可得这两个数列都收玫. 对 $x_n-y_n=\frac{1}{n}+\frac{1}{n+1}$ 等式 两边取极限, 得 $\left\{x_n\right\},\left\{y_n\right\}$ 极限相等.
  注：上述证明用到了不等式
  $$
  \frac{1}{n+1}<\ln \left(1+\frac{1}{n}\right)<\frac{1}{n},
  $$
  下面简单说下这个不等式的推导. 由 $\left\{\left(1+\frac{1}{n}\right)^n\right\}$ 严格单调递增收玫到 $\mathrm{e},\left\{\left(1+\frac{1}{n}\right)^{n+1}\right\}$ 严格单调 减收玫到 $\mathrm{e}$, 故 $\left(1+\frac{1}{n}\right)^n<e<\left(1+\frac{1}{n}\right)^{n+1}$, 两边同时取以 $\mathrm{e}$ 为底的对数, 则有 $n \ln \left(1+\frac{1}{n}\right)<1<$ $(n+1) \ln \left(1+\frac{1}{n}\right)$, 从而有上述不等式.

  - 【例题】利用上题结论,证明

  $$
  \lim _{n \longrightarrow \infty}\left(\frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{2 n}\right)=\ln 2
  $$
  证明： 定义数列 $z_n=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{n}-\ln n$, 则可得 $y_n<z_n<x_n$, 利用夹挤定理, 知 $\lim _{n \longrightarrow \infty} z_n=$ $\lim _{n \longrightarrow \infty} x_n=\lim _{n \longrightarrow \infty} y_n$. 且有
  $$
  z_{2 n}-z_n=\frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{2 n}+\ln \frac{n}{2 n},
  $$
  等式左右两边取极限, 并利用极限的四则运算可得
  $$
  \lim _{n \longrightarrow \infty}\left(\frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{2 n}\right)=\lim _{n \longrightarrow \infty} \ln \frac{2 n}{n}=\ln 2
  $$





#### 2.7 实数3个基本定理

- 单调有界原理：

  - 单调数列: 若 $x_{n+1} \geq(\leq) x_n, \forall n \in N^*$, 则称 $\left\{x_n\right\}$ 为递增(减)序列, 统称单调数列；

  - 有界数列: 如果存在 $M$, 使得 $x_n \geq(\leq) M, \forall n \in N^*$, 则称 $\left\{x_n\right\}$ 下(上) 方有界.若 $\left\{x_n\right\}$ 既有上界又有下界, 则称为有界数列.

  - 单调有界原理: 任何单调有界的数列必有极限, 可推广到从 $N_0$ 往后单调即可. 单调有界包括: 单调上升有上界和单调下降有下界.
    判定方法: $x_{n+1}-x_n \geq 0, \nearrow$. 若为正数列, 也可用 $\frac{x_{n+1}}{x_n} \geq 1$ 判断. $x_{n+1}-x_n \leq 0, \searrow$. 若为正数列, 也可用 $\frac{x_{n+1}}{x_n} \leq 1$ 判断.

  - 【例题】证明: 若 $a_1=\sqrt{6}, a_{n+1}=\sqrt{6+a_n}, n=1,2, \cdots$, 证明数列 $\left\{a_n\right\}$ 收玫, 并求其极限. 

    证明：证明单调性.
    当 $n=1$ 时, $a_1=\sqrt{6}<\sqrt{6+\sqrt{6}}=a_2$ 成立.
    假设 $n=k$ 时, $a_k<a_{k+1}$, 则有 $6+a_k<6+a_{k+1}$, 进而可得
    $$
    a_{k+1}=\sqrt{6+a_k}<\sqrt{6+a_{k+1}}=a_{k+2} .
    $$
    由数学归纳法可知 $\left\{a_n\right\}$ 单调递增.
    证明有上界.
    当 $n=1$ 时, $a_1=\sqrt{6}<3$ 成立.
    假设 $n=k$ 时, $a_k<3$, 则有
    $$
    a_{k+1}=\sqrt{6+a_k}<\sqrt{6+3}=3 .
    $$
    由数学归纳法可知数列 $\left\{a_n\right\}$ 有上界, 上界是 3 .
    根据单调有界原理, 数列 $\left\{a_n\right\}$ 收玫. 设 $\lim _{n \rightarrow \infty} a_n=a$, 有 $a=\sqrt{6+a}$,
    解得 $a=3$, 于是 $\lim _{n \rightarrow \infty} a_n=3$.
    注：也可按以下公式证明单调性
    $$
    a_{n+1}-a_n=\sqrt{6+a_n}-a_n=\frac{\left(3-a_n\right)\left(2+a_n\right)}{\sqrt{6+a_n}+a_n}>0 .
    $$

  - 【例题】设数列 $\left\{a_n\right\}$ 满足
    $$
    a_1=1, a_{n+1}=1+\frac{1}{a_n}, n=1,2, \cdots
    $$
    证明 $\left\{a_n\right\}$ 收敛, 并求其极限.
    证明: 我们先计算出 $\left\{a_n\right\}$ 的前几项:
    $$
    a_1=1, a_2=2, a_3=1+\frac{1}{2}=\frac{3}{2}, a_4=1+\frac{1}{\frac{3}{2}}=\frac{5}{3}
    $$
    $$
    a_5=1+\frac{1}{\frac{5}{3}}=\frac{8}{5}, a_6=1+\frac{1}{\frac{8}{5}}=\frac{13}{8}, \cdots
    $$
    从中初步判断出 $\left\{a_{2 k-1}\right\}$ 递增, $\left\{a_{2 k}\right\}$ 递减. 为证明这一点, 有
    $$
    a_{n+2}=1+\frac{1}{a_{n+1}}=1+\frac{1}{1+\frac{1}{a_n}}=1+\frac{a_n}{a_n+1}=2-\frac{1}{a_n+1}
    $$
    从而有
    $$
    a_{n+2}-a_n=\left(2-\frac{1}{a_n+1}\right)-\left(2-\frac{1}{a_{n-2}+1}\right)=\frac{a_n-a_{n-2}}{\left(a_n+1\right)\left(a_{n-2}+1\right)} .
    $$
    由数学归纳法容易得到 $a_n>0$, 故 $a_{n+2}-a_n$ 与 $a_n-a_{n-2}$ 同号. 于是由 $a_3>a_1, a_4<a_2$ 分 别可得 $\left\{a_{2 k-1}\right\}$ 递增, $\left\{a_{2 k}\right\}$ 递减, $1 \leq a_n<2$. 由单调有界原理知 $\left\{a_{2 k-1}\right\}$ 和 $\left\{a_{2 k}\right\}$ 都收敛。由于 $\left\{a_{2 k-1}\right\}$ 和 $\left\{a_{2 k}\right\}$ 的极限值都满足: $a=2-\frac{1}{a+1}$, 即 $a^2-a-1=0$. 从而得 到 $\left\{a_{2 k-1}\right\}$ 和 $\left\{a_{2 k}\right\}$ 的公共极限为 $\frac{1+\sqrt{5}}{2},\left(\frac{1-\sqrt{5}}{2}\right.$ 舍去). 所以 $\lim _{n \rightarrow \infty} a_n=\frac{1+\sqrt{5}}{2}$.

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

- 闭区间套定理：
  a. $\left[a_n, b_n\right] \supset\left[a_{n+1}, b_{n+1}\right], n \in N^*$;
  b. $\lim _{n \rightarrow \infty}\left(b_n-a_n\right)=0$.
  则存在唯一的一点 $c \in\left[a_n, b_n\right](n \geq 1)$, 使得 $c=\lim _{n \rightarrow \infty} a_n=\lim _{n \rightarrow \infty} b_n$.

- 确界原理：

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





#### 2.8 求极限的一些方法总结

- 定义法：【例题】用定义证明 $\lim _{n \rightarrow \infty} \frac{3 n^2+n+1}{2 n^2-1}=\frac{3}{2}$.
  证明: $\forall \varepsilon>0$, 取 $N=\max \left\{5,\left[\frac{1}{\varepsilon}\right]+1\right\}$, 当 $n>N$ 时,

$$
\left|\frac{3 n^2+n+1}{2 n^2-1}-\frac{3}{2}\right|=\left|\frac{2 n+5}{4 n^2-2}\right|<\frac{2 n+5}{3 n^2}<\frac{3 n}{3 n^2}=\frac{1}{n}<\varepsilon .
$$
由定义得证.

- 夹挤定理：【例题】 $x_n=\sum_{k=1}^n\left[\left(n^k+1\right)^{-\frac{1}{k}}+\left(n^k-1\right)^{-\frac{1}{k}}\right]$, 求 $\lim _{n \rightarrow \infty} x_n$;
  解：由于 $n-1<\sqrt[k]{n^k-1}<n<\sqrt[k]{n^k+1}<n+1$,
  所以
  $$
  \frac{1}{n+1}+\frac{1}{n}<\left(n^k+1\right)^{-\frac{1}{k}}+\left(n^k-1\right)^{-\frac{1}{k}}<\frac{1}{n}+\frac{1}{n-1}
  $$
  故 $1+\frac{n}{n+1}<x_n<1+\frac{n}{n-1}$, 当 $n \rightarrow \infty$ 时, 两边极限均为 2 , 所以由夹挤定理知 $\lim _{n \rightarrow \infty} x_n=2$.

- 极限四则运算：【例题】利用极限的运算法则求 $\lim _{n \rightarrow \infty} \frac{2 n^2-3 n}{3 n^2+2}$.

- 极限性质：有界量乘以无穷小量，【例题】$x_n=\frac{\sqrt[3]{n^2} \sin n !}{n+1}$, 求 $\lim _{n \rightarrow \infty} x_n$;

- 根式有理化：【例题】 $\lim _{n \longrightarrow \infty}(\sqrt{n+2}-2 \sqrt{n+1}+\sqrt{n}) \sqrt{n^3}$; 解 多次利用分子有理化: $-\frac{1}{4}$.

- Stolz 定理：条件：(1) $\left\{y_n\right\}$ 严格单调且趋于正无穷；(2) $\lim _{n \rightarrow \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}=A$：结论： $\lim _{n \longrightarrow \infty} \frac{x_n}{y_n}=A$.

  【例题】计算 $\lim _{n \longrightarrow \infty}\left(\frac{1}{n}-\frac{1}{2 n}+\frac{1}{3 n}-\cdots+(-1)^{n+1} \frac{1}{n^2}\right)$. 证法一 (利用夹挤定理) 令 $x_n=\frac{1}{n}-\frac{1}{2 n}+\frac{1}{3 n}-\frac{1}{4 n}+\cdots+(-1)^{n+1} \frac{1}{n^2}$, $y_n=-\frac{1}{n}-\frac{1}{2 n}-\cdots-\frac{1}{n^2}, z_n=\frac{1}{n}+\frac{1}{2 n}+\cdots+\frac{1}{n^2}$. 易得 $y_n<x_n<z_n$. 且
  $$
  z_n=\frac{1}{n}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}\right)=\frac{1}{n}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}-\ln n\right)+\frac{\ln n}{n},
  $$
  可得 $\lim _{n \longrightarrow \infty} z_n=\lim _{n \longrightarrow \infty} \frac{c}{n}+\lim _{n \longrightarrow \infty} \frac{\ln n}{n}=0$. 同理 $\lim _{n \longrightarrow \infty} y_n=0$.由夹挤定理可 得 $\lim _{n \longrightarrow \infty} x_n=0$；

  证法二(利用Stolz定理)令 $x_n=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots+(-1)^{n+1} \frac{1}{n}, y_n=n$, 易知 $\left\{y_n\right\}$ 严格单调 且趋于无穷. 且有
  $$
  \lim _{n \longrightarrow \infty} \frac{x_{n+1}-x_n}{y_{n+1}-y_n}=\lim _{n \longrightarrow \infty}(-1)^{n+2} \frac{1}{n+1}=0 .
  $$
  利用stolz定理有 $\lim _{n \longrightarrow \infty} \frac{x_n}{y_n}=0$.

- 单调有界原理//闭区间套//数列的上下数列//Cauchy判别法；
