《高等数学A》第五次习题课

> Author ZhenLiu
>
> 2022/10/04



> 以极限为工具，以$\R^{n}$为平台，以函数为对象。
>
> 本次习题课题目选自《数学分析》吉林大学+高等数学补充题目+刘震数学分析习题课+谢彦桐助教习题课+数学分析习题课精讲。



#### Review of Chapter1

- 数列极限的7个性质 + 证明方法；
- 实数完备性公理：单调有界//确界//Cauchy准则//子数列；
- 两个重要极限+求极限的补充方法（Stolz定理）；
- 特性函数：有界性/单调性/复合函数/反函数/周期函数/奇偶函数；
- 函数极限和数列极限的关系，函数极限的存在与非存在性证明；
- 间断函数的种类 + 复合函数连续性 + 基本初等函数的连续性；

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
  - 注 5 两个一致连续函数之积未必一致连续, 如 $x^2=x \cdot x$ // $x=\sqrt{x}\cdot\sqrt{x} $ 

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



#### 5.1 导数定义与计算

- 极限定义（左右极限）：设函数 $f(x)$ 在点 $x_0$ 及其附近有定义. 考虑在 $x_0$ 点咐近 (除 $x_0$ 点以外) 有定义的新的函数$Q(x)=\frac{f(x)-f\left(x_0\right)}{x-x_0} .$如果当 $x \rightarrow x_0$ 时, $Q(x)$ 有极限, 则说 $y=f(x)$ 在 $x_0$ 点是可导的, 或者说在 $x_0$ 点是有导数的. 而这个极限值 $\lim _{x \rightarrow x_0} Q(x)$, 便称为 $y=f(x)$ 在 $x_0$ 点的导数, 记为 $f^{\prime}\left(x_0\right)$, 即$f^{\prime}\left(x_0\right)=\lim _{x \rightarrow x_0} \frac{f(x)-f\left(x_0\right)}{x-x_0}$
- 【例题】设函数 $f$ 在 $(0,+\infty)$ 上有定义, 且 $\forall x, y \in(0,+\infty)$, 都有 $f(x y)=f(x)+f(y)$. 若 $f^{\prime}(1)$ 存在, 求 $f^{\prime}(x), x \in(0,+\infty)$.
  解: 在 $f(x y)=f(x)+f(y)$ 中, 令 $y=1$ 可得 $f(1)=0$. 又已知 $f^{\prime}(1)$ 存在, 故有

$$
\begin{aligned}
f^{\prime}(1) &=\lim _{h \rightarrow 0} \frac{f(1+h)-f(1)}{h} \\
&=\lim _{h \rightarrow 0} \frac{f(1+h)}{h}=\lim _{h \rightarrow 0} \frac{f(x+x h)-f(x)}{h} \\
&=\lim _{h \rightarrow 0} x \cdot \frac{f(x+x h)-f(x)}{x h}=x f^{\prime}(x) .
\end{aligned}
$$
- 【例题】如果 $f(x)$ 是某区间 $(a, b)$ 上的下凸函数, 则 $f(x)$ 在 $(a, b)$ 内连续, 且处处存在左、右导数.
  证明 任取 $x_0 \in(a, b)$. 考虑在 $\left(a, x_0\right) \cup\left(x_0, b\right)$ 上定义的函数
  $$
  F(x)=\frac{f(x)-f\left(x_0\right)}{x-x_0} \text {. }
  $$
  可以断言, $F(x)$ 在 $\left(a, x_0\right) \cup\left(x_0, b\right)$ 上是单调不减的. 事实上, 对满足 $x_0<x_1<$ $x_2<b$ 的任意 $x_1, x_2$, 在定义中改 $x_1$ 为 $x_0$, 得
  $$
  f\left((1-t) x_0+t x_2\right) \leq(1-t) f\left(x_0\right)+t f\left(x_2\right) .
  $$
  然后再对现在的 $x_0, x_1$ 和 $x_2$, 在上式中令 $t=\frac{x_1-x_0}{x_2-x_0}$ (相应地有 $1-t=\frac{x_2-x_1}{x_2-x_0}$, $\left.x_1=(1-t) x_0+t x_2\right)$, 即得
  $$
  f\left(x_1\right) \leq \frac{x_2-x_1}{x_2-x_0} f\left(x_0\right)+\frac{x_1-x_0}{x_2-x_0} f\left(x_2\right),
  $$

​	从而：$\frac{f\left(x_1\right)-f\left(x_0\right)}{x_1-x_0} \leq \frac{f\left(x_2\right)-f\left(x_0\right)}{x_2-x_0},$即$F\left(x_1\right) \leq F\left(x_2\right) .$类似地, 我们可以证明当 $a<x_1<x_2<x_0$ 以及 $a<x_1<x_0<x_2<b$ 时上式 亦成立. 因此, $F(x)$ 在 $\left(a, x_0\right) \cup\left(x_0, b\right)$ 上单调不减. 特别地, $F(x)$ 在 $\left(a, x_0\right)$ 上单调不减, 且以 $F(x)$ 在 $\left(x_0, b\right)$ 上任何点的值为其上界, 由单调有界原理可知 $\lim _{x \rightarrow x_0^{-}} F(x)$ 存在, 从而 $f_{-}^{\prime}\left(x_0\right)$ 存在. 同理 $f_{+}^{\prime}\left(x_0\right)$ 亦存在. 进而 $f(x)$ 在 $x_0$ 点既 左连续又右连续, 即 $f(x)$ 在 $x_0$ 点连续.由 $x_0$ 的任意性知定理的结论成立.

- 【思考】如果 $f(x)$ 是某区间 $(a, b)$ 上的下凸函数, 则
  (i) 对任音的 $x \in(a, b)$ 均有 $f_{-}^{\prime}(x) \leq f_{+}^{\prime}(x)$;
  (ii) 对满足 $a<x_1<x_2<b$ 的任音 $x_1, x_2$, 均有 $f_{+}^{\prime}\left(x_1\right) \leq f_{\neg}^{\prime}\left(x_2\right)$.

- 导数的性质：
  - 可导的充要条件是左右导数存在且相等；
  - 可导的函数必定是连续的，但是反之不一定成立；
- 计算导数的方法总结：
  - 定义法
  - 四则运算与求导公式表
  - 复合函数求导的链式法则和反函数求导法则
  - 对数求导法则：
    - 适用范围：对数求导法对于幂指函数 $u(x)^{v(x)}$ 以及只有乘除和乘方开方运算的复合函数 的求导是非常有效的.
    - 原理：考虑$y=u(x)^{v(x)}$,两边取对数（注意这里对数内部的值是正数）得$\ln y=v(x) \ln u(x) \text {. }$注意 $\ln y$ 作为 $x$ 的函数是复合函数. 故对上式两边关于 $x$ 求导得$\frac{1}{y} y^{\prime}=v^{\prime}(x) \ln u(x)+v(x) \frac{u^{\prime}(x)}{u(x)} .$从而$y^{\prime}=u(x)^{v(x)}\left(v^{\prime}(x) \ln u(x)+v(x) \frac{u^{\prime}(x)}{u(x)}\right) .$
- 【例题】1.设 $f(x)=\left\{\begin{array}{cc}x^m \cos \frac{1}{x}, & x>0, \\ 0, & x=0 .\end{array}\right.$, 求参数 $m$ 的取值范围, 使得 $f(x)$ 在 $x=0$ 右连续但是 右导数不存在。2.设 $f(x)=\left\{\begin{array}{cc}x^4 \sin \frac{1}{x}, & x \neq 0 . \\ 0, & x=0 .\end{array}\right.$, 求二阶导数 $f^{\prime \prime}(0)$ 。
  1. 首先 $f(x)$ 是右连续的, 因此极限$\lim _{x \rightarrow 0+0} x^m \cos \frac{1}{x}=0,$这说明 $m>0$, 即振幅 $x^m$ 在 0 处收玫于 0 。接着 $f(x)$ 不存在右导数, 所以极限$\lim _{x \rightarrow 0+0} \frac{x^m \cos \frac{1}{x}-0}{x}=\lim _{x \rightarrow 0+0} x^{m-1} \cos \frac{1}{x},$是发散的, 这要求 $m-1 \leq 0$, 此时振幅 $x^{m-1}$ 不收敛于 0 。综上 $m \in(0,1]$ 。
  2. 我们分别在 $x \neq 0$ 和 $x=0$ 计算 $f(x)$ 的导函数, 得到

$$
f^{\prime}(x)=\left\{\begin{array}{cl}
4 x^3 \sin \frac{1}{x}-x^2 \cos \frac{1}{x}, & x \neq 0 \\
0, & x=0 .
\end{array}\right.
$$
由此计算$f^{\prime \prime}(0)=\lim _{x \rightarrow 0} \frac{f^{\prime}(x)-f^{\prime}(0)}{x}=\lim _{x \rightarrow 0}\left(4 x^2 \sin \frac{1}{x}-x \cos \frac{1}{x}\right)=0$。







#### 5.2 微分和高阶导数

- 当 $f(x)$ 在 $x$ 点有导数时, $\Delta y$ 可分解为两项之和. 第一项与 $\Delta x$ 成正比, 是 $\Delta x$ 的线性函数, 非常便于计算. 第二项当 $\Delta x \rightarrow 0$ 时是比 $\Delta x$ 高阶的无穷小量, 在 $f^{\prime}(x) \neq 0,|\Delta x|$ 充分小时常可忽略不计. 

- 微分的性质

  - 定理： 函数 $y=f(x)$ 在 $x$ 点可澂的充分必要条件是, $f(x)$ 在 $x$ 点可 导. 这时微分 $\mathrm{d} y$ 中 $\Delta x$ 的系数 $A=f^{\prime}(x)$.
  - 无论$u$是自变量还是中间变量，都有$\mathrm{d} y=f^{\prime}(u) \mathrm{d} u$

- 高阶导数的计算：

  - 常见的高阶导数公式：

    $\begin{aligned}(\sin x)^{(n)} &=\sin \left(x+\frac{n \pi}{2}\right) \\(\cos x)^{(n)} &=\cos \left(x+\frac{n \pi}{2}\right) \\\left(\frac{1}{x}\right)^{(n)} &=(-1)^n \frac{n !}{x^{n+1}} \\(\ln (1+x))^{(n)} &=(-1)^{n-1} \frac{(n-1) !}{(1+x)^n} \\\left(\mathrm{e}^x\right)^{(n)} &=\mathrm{e}^x \end{aligned}$

  - 定理(Leibniz 公式) 设函数 $f(x)$ 和 $g(x)$ 咾有 $n$ 阶导数, 则 $f(x) g(x)$ 亦布 $n$ 阶导数, 且$[f(x) g(x)]^{(n)}=\sum_{j=0}^n C_n^j f^{(j)}(x) g^{(n-j)}(x)$

- 【例题】找规律加上归纳的方法 设 $f(x)=x^{n-1} \mathrm{e}^{\frac{1}{x}}$, 求 $f^{(n)}(x)$, 其中 $n \in \mathbb{N}^*$ 。

  当 $n=1$ 时有 $\left(\mathrm{e}^{\frac{1}{x}}\right)^{\prime}=-\frac{1}{x^2} \mathrm{e}^{\frac{1}{x}}$ 。当 $n=2$ 时有 $\left(x \mathrm{e}^{\frac{1}{x}}\right)^{\prime \prime}=\frac{1}{x^3} \mathrm{e}^{\frac{1}{x}}$ 。当 $n=3$ 时 有 $\left(x^2 \mathrm{e}^{\frac{1}{x}}\right)^{\prime \prime \prime}=-\frac{1}{x^4} \mathrm{e}^{\frac{1}{x}}$ 。我们希望证明$\left(x^n \mathrm{e}^{\frac{1}{x}}\right)^{(n)}=\frac{(-1)^n}{x^{n+1}} \mathrm{e}^{\frac{1}{x}} .$我们用数学归纳法。对 $n=1$ 成立。假如对 $n=k$ 成立, 即$\left(x^k \mathrm{e}^{\frac{1}{x}}\right)^{(k)}=\frac{(-1)^k}{x^{k+1}} \mathrm{e}^{\frac{1}{x}} .$

  我们想计算 $\left(x^{k+1} \mathrm{e}^{\frac{1}{x}}\right)^{(k+1)}$ 。由于归纳假设与我们的目标函数不一致, 所以我们首先使 用Leibniz公式计算
  $$
  \begin{aligned}
  \left(x^{k+1} \mathrm{e}^{\frac{1}{x}}\right)^{(k)} &=\left(x \cdot x^k \mathrm{e}^{\frac{1}{x}}\right)^{(k)} \\
  &=x \cdot\left(x^k \mathrm{e}^{\frac{1}{x}}\right)^{(k)}+k \cdot\left(x^k \mathrm{e}^{\frac{1}{x}}\right)^{(k-1)} \\
  &=\frac{(-1)^k}{x^k} \mathrm{e}^{\frac{1}{x}}+k \cdot\left(x^k \mathrm{e}^{\frac{1}{x}}\right)^{(k-1)} .
  \end{aligned}
  $$
  再对左右两端求导数
  $$
  \begin{aligned}
  \left(x^{k+1} \mathrm{e}^{\frac{1}{x}}\right)^{(k+1)} &=(-1)^k \mathrm{e}^{\frac{1}{x}}\left(\frac{-k}{x^{k+1}}-\frac{1}{x^{k+2}}\right)+k \cdot\left(x^k \mathrm{e}^{\frac{1}{x}}\right)^{(k)} \\
  &=(-1)^k \mathrm{e}^{\frac{1}{x}}\left(\frac{-k}{x^{k+1}}-\frac{1}{x^{k+2}}\right)+\frac{k(-1)^k}{x^{k+1}} \mathrm{e}^{\frac{1}{x}} \\
  &=\frac{(-1)^{k+1}}{x^{k+2}} \mathrm{e}^{\frac{1}{x}}
  \end{aligned}
  $$
  

- 【例题】设 $f(x)=\arctan x$, 求 $f^{(n)}(0)$, 其中 $n \in \mathbb{N}^*$ 。化 显为隐：能够成立的主要原因是 $y^{\prime}$ 和 $x$ 的隐关系比较简单, 使得使用Leibniz公式得到的 $n$ 阶导数表达式只有三项, 如 $y^{\prime}$ 和 $x$ 的隐关系的隐关系比较复杂, 则可能需要寻找更高阶导数的隐关系；
  证明： 我们设 $y=\arctan x$, 可以计算一阶导数$y^{\prime}=\frac{1}{1+x^2} \text {. }$移项得$\left(1+x^2\right) y^{\prime}=1 .$确定 $x$ 与 $y^{\prime}$ 关系的隐函数后，求 $n$ 次导数
  $$
  \left(\left(1+x^2\right) y^{\prime}\right)^{(n)}=0, \quad \forall n \in \mathbb{N}^* .
  $$
  再用Leibniz公式展开
  $$
  \left(1+x^2\right) y^{(n+1)}+2 n x y^{(n)}+n(n-1) y^{(n-1)}=0, \quad \forall n \geq 2 .
  $$
  代入 $x=0$ 得
  $$
  y^{(n+1)}(0)=-n(n-1) y^{(n-1)}(0), \quad \forall n \geq 2 .
  $$
  结合 $y^{\prime}(0)=1$ 和 $y^{\prime \prime}(0)=0$ 得
  $$
  y^{(n)}(0)= \begin{cases}0 & n \text { 是偶数, } \\ (-1)^{\frac{n-1}{2}}(n-1) ! & , n \text { 是奇数. }\end{cases}
  $$

- 【例题】设 $f(x)=\frac{2 x}{1-x^2}$, 求 $f^{(n)}(x)$, 其中 $n \in \mathbb{N}^*$ 。
  证明：经过代数变形$f(x)=\frac{2 x}{1-x^2}=\frac{1}{1-x}-\frac{1}{1+x} .$可得到
  $$
  \begin{aligned}
  \left(\frac{1}{1+x}\right)^{(n)} &=(-1)^n \frac{n !}{(x+1)^{n+1}}, \\
  \left(\frac{1}{-1+x}\right)^{(n)} &=(-1)^n \frac{n !}{(x-1)^{n+1}} .
  \end{aligned}
  $$
  这里我们不直接对 $\frac{1}{1-x}$ 求导而选择对 $\frac{1}{x-1}$ 求导, 是为了避免 $-x$ 对导数的影响。因此
  $$
  f^{(n)}(x)=(-1)^{n+1} n !\left(\frac{1}{(x+1)^{n+1}}+\frac{1}{(x-1)^{n+1}}\right) .
  $$

- 【例题】求方程 $\mathrm{e}^x-\mathrm{e}^y-x y=0$ 所确定的䧔函数 $y=f(x)$ 的二阶导数.

  首先利用一阶微分的形式不变性计算一阶导数：$y^{\prime}=\frac{\mathrm{e}^x-y}{\mathrm{e}^y+x}$

  对上式两端再求一次导数, 得到：
  $$
  \begin{aligned}
  y^{\prime \prime} &=\frac{\left(\mathrm{e}^x-\frac{\mathrm{e}^x-y}{\mathrm{e}^y+x}\right)\left(\mathrm{e}^y+x\right)-\left(\mathrm{e}^x-y\right)\left(\mathrm{e}^y \frac{\mathrm{e}^x-y}{\mathrm{e}^y+x}+1\right)}{\left(\mathrm{e}^y+x\right)^2} \\
  &=\frac{\mathrm{e}^x\left(\mathrm{e}^y+x\right)^2-2\left(\mathrm{e}^x-y\right)\left(\mathrm{e}^y+x\right)-\mathrm{e}^y\left(\mathrm{e}^x-y\right)^2}{\left(\mathrm{e}^y+x\right)^3}
  \end{aligned}
  $$

- 【例题】求由参数方程$x=a \cos t, \quad y=b \sin t, \quad 0<t<\pi$所确定的函数 $y=f(x)$ 的二阶导数.（要计算参数方程二阶导, 应首先把 $\frac{\mathrm{d} y}{\mathrm{~d} x}$ 写成关于 $x$ 的表达式, 然后用复合函数求导法)
  由于
  $$
  \begin{aligned}
  \frac{\mathrm{d} x}{\mathrm{~d} t} &=-a \sin t, & \frac{\mathrm{d} y}{\mathrm{~d} t} &=b \cos t \\
  \frac{\mathrm{d}^2 x}{\mathrm{~d} t^2} &=-a \cos t, & \frac{\mathrm{d}^2 y}{\mathrm{~d} t^2} &=-b \sin t
  \end{aligned}
  $$
  所以
  $$
  \begin{aligned}
  \frac{\mathrm{d}^2 y}{\mathrm{~d} x^2} &=\frac{\mathrm{d}}{\mathrm{d} x}\left(\frac{\mathrm{d} y}{\mathrm{~d} x}\right)=\frac{\frac{\mathrm{d}}{\mathrm{d} t}\left(\frac{\mathrm{d} y}{\mathrm{~d} t} / \frac{\mathrm{d} x}{\mathrm{~d} t}\right)}{\frac{\mathrm{d} x}{\mathrm{~d} t}} \\
  &=\frac{\frac{\mathrm{d}^2 y}{\mathrm{~d} t^2} \frac{\mathrm{d} x}{\mathrm{~d} t}-\frac{\mathrm{d} y}{\mathrm{~d} t} \frac{\mathrm{d}^2 x}{\mathrm{~d} t^2}}{\left(\frac{\mathrm{d} x}{\mathrm{~d} t}\right)^3} \\
  &=\frac{(-b \sin t)(-a \sin t)-(b \cos t)(-a \cos t)}{(-a \sin t)^3} \\
  &=-\frac{b}{a^2 \sin ^3 t} .
  \end{aligned}
  $$

- 【例题】  $\left\{\begin{array}{l}x=3 \mathrm{e}^{-t} \\ y=2 \mathrm{e}^t\end{array}\right.$, 求 $\frac{\mathrm{d}^2 y}{\mathrm{~d} x^2}$.
  解: $y^{\prime}=\frac{\mathrm{d} y}{\mathrm{~d} x}=\frac{\mathrm{d} y}{\mathrm{~d} t} / \frac{\mathrm{d} x}{\mathrm{~d} t}=\frac{2 \mathrm{e}^t}{-3 \mathrm{e}^{-t}}=-\frac{2}{3} \mathrm{e}^{2 t}$, 故
  $$
  \frac{\mathrm{d}^2 y}{\mathrm{~d} x^2}=\frac{\mathrm{d} y^{\prime}}{\mathrm{d} x}=\frac{\mathrm{d} y^{\prime}}{\mathrm{d} t} / \frac{\mathrm{d} x}{\mathrm{~d} t}=\frac{-\frac{4}{3} \mathrm{e}^{2 t}}{-3 \mathrm{e}^{-t}}=\frac{4}{9} \mathrm{e}^{3 t}
  $$

- 【例题】设 $f(x)=\left\{\begin{array}{ll}\mathrm{e}^{-\frac{1}{x^2}}, & x \neq 0 \\ 0, & x=0\end{array}\right.$, 求高阶导数 $f^{(2021)}(0)$ 

  如果 $x \neq 0$, 我们考虑高阶导数 $f^{(n)}(x)$ 表达式。不难验算 $f^{\prime}(x)=\frac{2}{x^3} \mathrm{e}^{-\frac{1}{x^2}}, f^{\prime \prime}(x)=$ 果 $x \neq 0$, 我们可以将 $f^{(n)}(x)$ 写成如下形式
  $$
  f^{(n)}(x)=P_n\left(\frac{1}{x}\right) \mathrm{e}^{-\frac{1}{x^2}},
  $$
  其中 $P_n$ 是一个多项式。当 $n=0$ 时, $f(x)=\mathrm{e}^{-\frac{1}{x^2}}$, 因此多项式 $P_0=1$ 。我们假定 $n=$ $k$ 时可以将 $f^{(k)}(x)$ 写成式(67)形式, 即
  $$
  f^{(k)}(x)=P_k\left(\frac{1}{x}\right) \mathrm{e}^{-\frac{1}{x^2}} .
  $$
  我们继续计算导数 $f^{(k+1)}(x)$ 得
  $$
  f^{(k+1)}(x)=\mathrm{e}^{-\frac{1}{x^2}}\left[-\frac{2}{x^3} P_k\left(\frac{1}{x}\right)-\frac{1}{x^2} P_k^{\prime}\left(\frac{1}{x}\right)\right] .
  $$
  考虑到 $P_k$ 及其导数 $P_k^{\prime}$ 仍然是多项式，那么
  $$
  P_{k+1}\left(\frac{1}{x}\right)=-\frac{2}{x^3} P_k\left(\frac{1}{x}\right)-\frac{1}{x^2} P_k^{\prime}\left(\frac{1}{x}\right),
  $$
  也是关于 $\frac{1}{x}$ 的多项式。接下来我们用归纳法证明 $f^{(n)}(0)=0$ 总成立, 其中 $n \in \mathbb{N}^*$ 。首先
  $$
  f^{\prime}(0)=\lim _{x \rightarrow 0} \frac{1}{x} \mathrm{e}^{-\frac{1}{x^2}}=\lim _{y \rightarrow \infty} y \mathrm{e}^{-y^2}=0,
  $$
  其中换元 $y=\frac{1}{x}$ 。对于一般的 $k \in \mathbb{N}^*$ 如果 $f^{(k)}(0)=0$, 计算
  $$
  f^{(k+1)}(0)=\lim _{x \rightarrow 0} \frac{1}{x} P_k\left(\frac{1}{x}\right) \mathrm{e}^{-\frac{1}{x^2}}=\lim _{y \rightarrow \infty} y P_k(y) \mathrm{e}^{-y^2} .
  $$
  由于 $y P_k(y)$ 是关于 $y$ 的多项式, 其量级是比指数型无穷大量 $\mathrm{e}^{y^2}$ 小的, 所以 $\lim _{y \rightarrow \infty} y P_k(y) \mathrm{e}^{-y^2}=$ 0。一般地, $f^{(2021)}(0)=0$ 。



#### 5.3  无穷小量和无穷大量

- 定义：设 $\left\{x_n\right\}$ 是一个序列. 若 $x_n \rightarrow 0(n \rightarrow \infty)$, 则称序 列 $\left\{x_n\right\}$ 为无穷小量, 记为 $x_n=o(1)(n \rightarrow \infty)$.

  - 这里需特别指出的是, 无穷小量并不是一个很小的量, 而是极限为 零的一个变量.

- 性质：设 $\left\{x_n\right\}$ 是一个序列.

  - 无穷小量具有传递性；
  - $\left\{x_n\right\}$ 是无穷小量的充分必要条件是 $\left\{\left|x_n\right|\right\}$ 是无穷小量；
  - 若 $\left\{x_n\right\}$ 是无穷小量, $M$ 是一个常数, 则 $\left\{M x_n\right\}$ 是无穷小量;
  - $\lim _{n \rightarrow \infty} x_n=a$ 的充分必要条件是 $\left\{x_n-a\right\}$ 是无穷小量.
  - 当 $x \rightarrow 0$ 时, $f(x) \sim g(x)$, 必有 $f^2(x) \sim g^2(x)$. 若还有 $\varphi(x) \rightarrow 0$, 则 $f(\varphi(x)) \sim g(\varphi(x))$.
  - 定理： $\left\{x_n\right\}$ 是无穷小量的充分必要条件是 $\left\{\frac{1}{x_n}\right\}$ 是无穷大量, 这里假定对任意的正整数 $n$, 有 $x_n \neq 0$.

- 【例题】如果不是乘积和商的极限, 则一般不能用等价无穷小 (大) 量 来代替. 例如:
  $$
  \lim _{x \rightarrow 0} \frac{\tan x-\sin x}{x^3}=\frac{1}{2} \neq \lim _{x \rightarrow 0} \frac{x-x}{x^3}=0
  $$




