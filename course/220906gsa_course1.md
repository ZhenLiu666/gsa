《高等数学A》第一次习题课

> Author ZhenLiu
>
> 2022/09/06



> 以极限为工具，以$\R^{n}$为平台，以函数为对象。



#### 1.1 基本符号

- 约定如下记号：

  - $\mathbb{N}$ 表示全体正整数组成的集合;
  - $\mathbb{Z}$ 表示全体整数组成的集合;
  - $\mathbb{Q}$ 表示全体有理数组成的集合;
  - $\mathbb{R}$ 表示全体实数组成的集合；
  - 闭区间 $[a, b]=\{x \in \mathbb{R}: a \leqslant x \leqslant b\}$；
  - 开区间 $(a, b)=\{x \in \mathbb{R}: a<x<b\}$；
  - 左开右闭区间，左闭右开区间类似可定义；

- 数域：指对加减乘除四则运算封闭的代数系统（除数不为0）

  - 有理数域是最小的数域；
  - 复数域是最大的数域；

- 命题：是一个陈述句所表达的判断，具有真值，即不是真的就是假的；

- 逻辑符号:

  -  $\forall$ 可以看成是大写字母 $\boldsymbol{A}$ 绕中心旋转得到, 它的意义与英文单词 All 直接有关, 也就表示“对所有”, “对任意”, “对每一个”, 表示全称量词。
  - $\exists$ 可以看成是大写字母 $\boldsymbol{E}$ 绕中心旋转得到, 它的意义与英文单词 Exist 一致, 表示“存 在”或“有”, 表示存在量词。

- 对偶法则：

  - 对偶法则：设命题 $P$ 可以写为：$p_1 q_1, p_2 q_2, \cdots, p_n q_n$, 使得 $q_{n+1}$ 成立，其中 $p_i(i=1,2, \cdots, n)$ 为逻辑符号 $\forall$ 或者 $\exists$; 而 $q_i(i=1,2, \cdots, n+1)$ 代表数学表达式, 这样对于命题 $\mathrm{P}$ 的否命题的正面表达, 只需要将所有逻辑符号 $p_i(i=1,2, \cdots, n)$ 从 $\forall(\exists)$ 改为 $\exists(\forall)$, 并将最后的 $q_{n+1}$ 改为其否定形式即可。
  - 如刻画一个数列 $\left\{a_n\right\}$ 有界的命题:$\exists M>0, \forall n$, 使得 $\left|a_n\right| \leqslant M$，对上述命题的否命题 (刻画一个数列无界) 也就是:$\forall M>0, \exists n$ 使得 $\left|a_n\right|>M$.

- 数学中常用$\varepsilon$表示充分小的正数，如果 $0 \leq a<\varepsilon \quad \forall \varepsilon>0 \Rightarrow a=0 .$

- 常用比较关系：$\lg n \ll n^k(k>0) \ll a^n(a>1) \ll n!<n^n$；

- 爱因斯坦求和（哑指标）：$a_i b_i=\sum_{i=1}^3 a_i b_i=a_1 b_1+a_2 b_2+a_3 b_3$；

  



#### 1.2 等式与不等式

- 平方差公式： $a^2-b^2=(a+b)(a-b)$. 此公式常用于将极限式中的根号去掉.

- 二项式公式：$(a+b)^n=\sum_{k=0}^n\left(\begin{array}{l}n \\ k\end{array}\right) a^k b^{n-k}$, 这里二项式系数 $\left(\begin{array}{l}n \\ k\end{array}\right)=\frac{n !}{k !(n-k) !}=\frac{n(n-1) \cdots(n-k+1)}{k(k-1) \cdots 1}$. 

  常用的情形是 $a=1$, 于是 $(1+t)^n=1+n t+\frac{n(n-1)}{2} t^2+\cdots+t^n$. 此公式常用于高阶项的比较和估计.

- 对任何 $x, y \in \mathbb{R}$, 有$-|x| \leqslant x \leqslant|x|, \quad-|y| \leqslant y \leqslant|y|$；

- 绝对值不等式$|| a|-| b|| \leqslant|a \pm b| \leqslant |a|+|b|$；

- Bernoulli不等式 $(1+x)^n \geqslant 1+n x \quad(x \geqslant-1)$和任意正整数$n$；

  证明 我们采用数学归纳法来证明这一不等式. 当 $n=1$ 上述不等式显然成立. 假设我们已经证明了
  $$
  (1+x)^{n-1} \geqslant 1+(n-1) x
  $$
  对一切的 $x \geqslant-1$ 成立, 则有
  $$
  \begin{aligned}
  (1+x)^n &=(1+x)^{n-1}(1+x) \\
  & \geqslant(1+(n-1) x)(1+x) \\
  &=1+n x+(n-1) x^2 \\
  & \geqslant 1+n x .
  \end{aligned}
  $$
  由数学归纳法原理知, 伯努利不等式对一切的正整数 $n$ 成立。

- 算术-几何平均不等式：对任意 $n$ 个非负实数 $x_1, x_2, \cdots, x_n$, 有 $\frac{x_1+x_2+\cdots+x_n}{n} \geqslant \sqrt[n]{x_1 x_2 \cdots x_n}$.

  证明： 我们同样采用数学归纳法来证明这一不等式. 当 $n=1$ 时, 上述不等式显然成立. 假设我们已经证明了, 对任意 $n-1$ 个非负 实数, 算术-几何平均不等式成立. 下面我们来考虑任意 $n$ 个非负实数 $x_1, x_2, \cdots, x_n$ 的情形. 不妨假定 $x_n$ 是这 $n$ 个数中最大的一个. 令
  $$
  y=\frac{x_1+x_2+\cdots+x_{n-1}}{n-1},
  $$
  从而有 $x_n \geqslant y=\frac{x_1+x_2+\cdots+x_{n-1}}{n-1} \geqslant \sqrt[n-1]{x_1 x_2 \cdots x_{n-1}}$,
  $$
  \begin{aligned}
  \left(\frac{x_1+x_2+\cdots+x_n}{n}\right)^n &=\left(y+\frac{x_n-y}{n}\right)^n \\
  &=y^n+n y^{n-1} \frac{x_n-y}{n}+\cdots+\left(\frac{x_n-y}{n}\right)^n \\
  & \geqslant y^n+n y^{n-1} \frac{x_n-y}{n} \\
  &=y^{n-1} x_n \\
  & \geqslant x_1 x_2 \cdots x_n
  \end{aligned}
  $$

- Cauchy-Schwarz 不等式$\left(\sum_{k=1}^n a_k b_k\right)^2 \leqslant\left(\sum_{k=1}^n a_k^2\right)\left(\sum_{k=1}^n b_k^2\right)$

  证： 注意, 对 $x \in R^1$ 皆有
  $$
  \begin{array}{r}
  \sum_{k=1}^n\left(a_k x+b_k\right)^2 \geqslant 0 . \\
  \text { 令 } A=\sum_{k=1}^n a_k^2, B=\sum_{k=1}^n a_k b_k, C=\sum_{k=1}^n b_k^2, \text { 于是 } \\
  A x^2+2 B x+C \geqslant 0 .
  \end{array}
  $$
  不妨设 $A>0$, 令 $x=-\frac{B}{A}$, 则有$B^2-A C \leqslant 0$，证毕。

- Mikowski不等式：$\left[\sum_{k=1}^n\left(a_k+b_k\right)^2\right]^{\frac{1}{2}} \leqslant\left(\sum_{k=1}^n a_k^2\right)^{\frac{1}{2}}+\left(\sum_{k=1}^n b_k^2\right)^{\frac{1}{2}} .$

  证：注意
  $$
  \sum_{k=1}^n\left(a_k+b_k\right)^2=\sum_{k=1}^n a_k^2+\sum_{k=1}^n b_k^2+2 \sum_{k=1}^n a_k b_k
  $$
  据 Cauchy-Schwarz不等式
  $$
  \sum_{k=1}^n a_k b_k \leqslant\left(\sum_{k=1}^n a_k^2\right)^{\frac{1}{2}}\left(\sum_{k=1}^n b_k^2\right)^{\frac{1}{2}}
  $$
  得到
  $$
  \begin{aligned}
  \sum_{k=1}^n\left(a_k+b_k\right)^2 & \leqslant \sum_{k=1}^n a_k^2+\sum_{k=1}^n b_k^2+2\left(\sum_{k=1}^n a_k^2\right)^{\frac{1}{2}}\left(\sum_{k=1}^n b_k^2\right)^{\frac{1}{2}} \\
  &=\left[\left(\sum_{k=1}^n a_k^2\right)^{\frac{1}{2}}+\left(\sum_{k=1}^n b_k^2\right)^{\frac{1}{2}}\right]^2,
  \end{aligned}
  $$

- $\sin x<x<\tan x \quad \forall x \in\left(0, \frac{\pi}{2}\right)$

- $\left|\sin x\right| \leqslant|x| \quad \forall x \in \mathbb{R}$



#### 1.3 集合

- 定义与表示：

  - 一般说来, 如果 $p(x)$ 是一个与 $x$ 有关的条件 (或命题), 则所有合乎这个条件 (或使这个命题成立) 的 $x$ 所构成的集合便记之为 $\{x ; p(x)\}$ 。例如当 $p(x)$ 是 “数 $x$ 的平方等于1"这一条件时, $\{x ; p(x)\}$ 就是 $\{-1,1\}$. 
  -  $E$ 是一个事先给定了的集合，则 $E[x ; p(x)]$ 便表示 $E$ 中所有使条件 $p(x)$ 满足的 $x$ 所构成的集合, 也就是 $\{x ; x \in E, p(x)\}$. 例如当 $f(x)$ 是一个给定的实函数且 $a$ 是一个常数时, $E[x ; f(x)>a]$ 就是 $E$ 中那些使 $f(x)$ 大于 $a$ 的 $x$ 所构成的集合.

- 关系：

  - =： 两个集合 $A$ 和 $B$ 是相等的, 记为 $A=B$, 就是说它们所包含的元素相同, 即它们实际上是同一个集合. 例如 $\left\{x ; x^2=1\right\}$ $=\{-1,1\}$.
  - $\subset$：设 $A, B$ 是两个集合, 如果属于 $A$ 的元素都属于 $B$, 则说 $A$ 包含于 $B$ 或 $A$ 是 $B$ 的子集，记为 $A \subset B, A$ 包含于 $B$ 也可以说成 $B$ 包含$\boldsymbol{A}$, 而记为 $B \supset A$.对于任何集合 $A,A\supset A$ 总成立, 所以 $A$ 也是 $A$ 本身的子集.
  - 如果集合 $B \subset A, B \neq A$, 即 $B$ 是 $A$ 的子集, 但 $B$ 还不等于 $A$, 则说 $B$ 是 $A$ 的真子集.
  - $\varnothing$: 不包含任何元素的集合称为空集，空集是任何集合的子集.
  - 定理1  $A=B$ 的充要条件是 $A \subset B$, 且 $B \subset A$.
  - 定理 2  如果 $A \subset B, B \subset C$, 则 $A \subset C$.

- 交运算和无穷交:

  - 设 $A, B$ 是两个给定的集合, 将它们所共有的元素拿来构成一个新的集合, 称为 $A$ 和 $B$ 的交,记作 $A \cap B$ 或 $A B$, 因此 $A \cap B=\{x ; x \in A$ 且 $x \in B\}$.例如 $A=\{1,2,3,4\}, B=\{3,4,5,6\}, C=\{6,7,8\}$, 则 $A \cap B=\{3,4\}, B \cap C=\{6\}, A \cap C=\varnothing$.

  - 一般来说,如果 $\Lambda$ 是一集合, 对于每一 $\lambda \in \Lambda$, 都相应地给定了一个集合 $A_\lambda$, 则我们就说给定了 (以 $A$ 为下标集的)一族集合.

  - 一族集合的交定义为$\left\{x\right.$; 对每一 $\lambda \in \Lambda$, 都有 $\left.x \in A_\lambda\right\}$,记为 $\bigcap_{\lambda \in A} A_{\lambda \cdot}$ 

  - 如果 $\Lambda=\{1,2, \cdots, n\}$ 或 $\{1,2,3, \cdots, n, \cdots\}$, 则述交就分别简记为 $\bigcap_{i=1}^n A_i$ 和 $\bigcap_{n=1}^{\infty} A_n$. 所以 $\bigcap_{n=1}^{\infty} A_n=\left\{x\right.$; 对任何正整数 $n$, 都有 $\left.x \in A_n\right\}$.

  - 若 $A_n=\left\{x ;-\frac{1}{n}<x<\frac{1}{n}\right\}, n=1,2,3, \cdots$, 则
    $$
    \bigcap_{i=1}^n A_i=\left\{x ;-\frac{1}{n}<x<\frac{1}{n}\right\}, \bigcap_{n=1}^{\infty} A_n=\{0\} .
    $$

- 并运算和无穷并：

  - 两个集合 $A$ 和 $B$ 的并定义为
    $$
    \{x ; x \in A \text { 或 } x \in B\} \text {, }
    $$
    记为 $A \cup B$. 例如 $\{1,2,3,4\} \cup\{3,4,5,6\}=\{1,2,3,4,5$, 6 $\}$ 同样, 以 $A$ 为下标集的一族集合 $\left\{A_\lambda\right\}_{\lambda \in A}$ 的并就是
    $\bigcup_{\lambda \in A} A_\lambda=\left\{x\right.$; 有 $\lambda \in A$, 使 $\left.x \in A_\lambda\right\}$。

  - 当$\Lambda=\{1,2, \cdots, n\}$ 或 $\{1,2, \cdots, n, \cdots\}$ 时, 分别有 $\bigcup_{i=1}^n A_i=\left\{x\right.$; 有 $i \leqslant n$, 使 $\left.x \in A_i\right\}$, $\bigcup_{n=1}^{\infty} A_n=\left\{x\right.$; 有正整数 $n$, 使 $\left.x \in A_n\right\}$.

  - 例 6 若 $A_n=\left\{-1+\frac{1}{n} \leqslant x \leqslant 1-\frac{1}{n}\right\}, n=1,2,3, \cdots$, 则
    $$
    \bigcup_{i=1}^n A_i=\left\{x ;-1+\frac{1}{n} \leqslant x \leqslant 1-\frac{1}{n}\right\}=A_n=\left[-1 + \frac{1}{n}, 1-\frac{1}{n}\right]
    $$
    $$
    \bigcup_{n=1}^{\infty} A_n=\{x ;-1<x<1\}=(-1,1) .
    $$

- 余集：

  - 对于两个给定的集合 $A, B$, 我们定义 $A-B$ 为${A}-{B}=\{x ; x \in A, x \bar{\in} {B}\} .$即 $A-B$ 是由属于 $A$ 而不属于 $B$ 的那些元素构成的集合. 注意, 一 般说来 $(A-B) \cup B$ 未必等于 $A$ . 
  - 如果已知 $A \supset B$, 侧 $A-B$ 称为 $B$ 相对于 $A$ 的余集. 记为 $\mathscr{C}_A B$. 
  - 特别是如果我们在某 一问题中所考虑的一切集合都是某一给定集合 $S$ 的子集时，集合 $B$ 相对于 $S$ 的余集就简称为 $B$ 的余集，而把 $\mathscr{C}_S B$ 简记为 $\mathscr{C} B$ 或 $B^c .$
  - $S^c=\varnothing, \quad \varnothing^c=S$
  - $A \cup A^c=S, \quad A \bigcap A^c=\varnothing$
  - $A \cup A^c=S, \quad A \bigcap A^c=\varnothing $
  - $(A^c)^c=A$
  - 若 $A \supset B$, 则 $A^c \subset B^c$
  - 德摩根公式：$\left(\bigcup_{\lambda \in \Lambda} A_\lambda\right)^c=\bigcap_{\lambda \in \Lambda} A_\lambda^c,\left(\bigcap_{\lambda \in \Lambda} A_\lambda\right)^c=\bigcup_{\lambda \in \Lambda} A_\lambda^c$；

- 运算公式：

  - $A \cup(B \cup C)=(A \cup B) \cup C, \quad A \cap(B \cap C)=(A \cap B) \cap C$
  - $A \cap(B \cup C)=(B \cup C) \cap A=(A \cap B) \cup(A \cap C)$
  - $A \cup A=A, A \cap A=A$
  -  $A \cap B \subset A \subset A \cup B$
  -  若 $A_\lambda \subset B_\lambda(\lambda \in \Lambda)$, 则 $\bigcup_{\lambda \in A} A_\lambda \subset \bigcup_{\lambda \in\Lambda} B_\lambda$. 特别若 $A_\lambda \subset C$ $(\lambda \in \Lambda)$, 则 $\bigcup_{\lambda \in \Lambda} A_\lambda \subset C$.
  -  若 $A_\lambda \subset B_\lambda(\lambda \in \Lambda)$, 则 $\bigcap_{\lambda \in \Lambda} A_\lambda \subset \bigcap_{\lambda \in \Lambda} B_\lambda$, 特别若 $C \subset B_\lambda$$(\lambda \in \Lambda)$, 则 $C \subset \bigcap_{\lambda \in \Lambda} B$.
  -  $\bigcup_{\lambda \in \Lambda}\left(A_\lambda \cup B_\lambda\right)=\left(\bigcup_{\lambda \in \Lambda} A_\lambda\right) \cup\left(\bigcup_{\lambda \in \Lambda} B_\lambda\right)$.
  -  $A \cap\left(\bigcup_{\lambda \in A} B_\lambda\right)=\bigcup_{\lambda \in \Lambda}\left(A \cap B_\lambda\right)$.

- 集合的上下极限：

  - 对于一串给定的集合 $A_1, A_2, \cdots, A_n, \cdots$. 我们定义$\left\{x\right.$; 有无穷多个 $n$, 使 $\left.x \in A_n\right\}$为这串集合的上极限, 记为或 $\operatorname{\varlimsup}_n A_n$或者$\limsup_n A_n$.

  - 定义$\left\{x\right.$; 只有有限多个 $n$, 使 $\left.x \bar{\in} A_n\right\}$为这串集合的下极限, 记为 $\varliminf_n A_n$ 或 $\underset{n}{\liminf } A_n$. 

  - $\underset{n}{\liminf } A_n \subset \limsup _n A_n$；

  - 设 $A_n=\left[\frac{1}{n}, 3+(-1)^n\right], n=1,2,3, \cdots$, $\liminf _n A_n=(0,2], \quad \limsup _n A_n=(0,4]$. 这时 $\liminf _n A_n \neq \limsup _n A_n$.

  - 如果一串集合 $A_1, A_2, \cdots, A_n, \cdots$ 的上、下极限相同, 则我们就 说这串集含是有极限的或收敛的, 并且我们把 $\limsup _n$ (也就是 $\liminf _n A_n$ ）记为 $\lim _n A_n$, 称为其极限；

  - 定理： 对于任意一串集合 $A_1, A_2, \cdots, A_n, \cdots$, 都有
    $$
    \begin{aligned}
    \underset{n}{\liminf } A_n &=\bigcup_{m=1}^{\infty} \bigcap_{i=m}^{\infty} A_i, \\
    \underset{n}{\limsup A_n} &=\bigcap_{m=1}^{\infty} \bigcup_{i=m}^{\infty} A_i .
    \end{aligned}
    $$
    证明： 若 $x \in \liminf _n A_n$, 则只有有限个 $n$, 使 $x \in A_n$, 所以有 $m_0$ 使 $n \geqslant m_0$ 时, $x \in A_n$, 从而 $x \in \bigcap_{i=m_0}^{\infty} A_i$, 于是 $x \in \bigcup_{m=1}^{\infty} \bigcap_{i=m}^{\infty} A_i$. 反之, 如果 $x \in \bigcup_{m=1}^{\infty} \bigcap_{i=m}^{\infty} A_i$, 则有 $m_0$ 使 $x \in \bigcap_{i=m_0}^{\infty} A_i$, 这说明当 $n \geqslant m_0$ 时, $x \in A_n$, 可 见最多有 $m_0-1$ 个 $n$ 使 $x \in A_n$. 因而 $x \in \liminf A_n$. 这证明了第一个等式.

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



#### 1.4 确界

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
  (i) $\inf (X+Y)=\inf X+\inf Y$;
  (ii) $\sup (X+Y)=\sup X+\sup Y$.
  这里记号 $X+Y$ 表示数集 $\{x+y ; x \in X, y \in Y\}$.

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





#### 1.4 映射

- 定义域，对应法则，值域
- 单射，满射，双射
- 线性映射
- 复合映射
- 向量空间



