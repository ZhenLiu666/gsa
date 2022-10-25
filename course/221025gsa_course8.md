《高等数学A》第八次习题课

> Author ZhenLiu
>
> 2022/10/25





#### 课前测试

- 【题目】计算定积分 $\int_0^{\frac{\pi}{4}} \ln (1+\tan x) \mathrm{d} x$ 。
  Proof. 这一被积函数的原函数不能写成初等函数的形式, 我们用换元法。我们进行下 述计算
  $$
  f\left(\frac{\pi}{4}-x\right)=\ln \left(1+\tan \left(\frac{\pi}{4}-x\right)\right)=\ln \left(1+\frac{1-\tan x}{1+\tan x}\right)=\ln 2-\ln (1+\tan x) .
  $$
  整理得 $f(x)+f\left(\frac{\pi}{4}-x\right)=\ln 2$ 。即关于直线 $x=\frac{\pi}{8}$ 对称的两个点 $x$ 与 $\frac{\pi}{4}$ 上函数值和为 $\ln 2$, 由此
  $$
  \int_0^{\frac{\pi}{4}} \ln (1+\tan x) \mathrm{d} x=\frac{\pi}{4} \cdot \frac{\ln }{2}=\frac{\pi \ln 2}{8} .
  $$

- 【题目】计算$\int_{-2}^2 x \ln \left(1+\mathrm{e}^x\right) \mathrm{d} x$
  首先计算$f(-x)=-x \ln \left(1+\mathrm{e}^{-x}\right)=-x\left[\ln \left(\mathrm{e}^{-x}\right)+\ln \left(1+\mathrm{e}^x\right)\right]=x^2-f(x) .$由此得关系式 $f(x)+f(-x)=x^2$ 。阼看此式找不到 $f$ 任何对称性, 但是结合图 7 我们发 现, 对于相反的两个点 $x$ 与 $-x$, 函数 $f$ 在 $x$ 处多出 $\frac{x^2}{2}$ 的部分和 $f$ 在 $-x$ 处少于 $\frac{x^2}{2}$ 部分一样 多。 函数 $g(x)=x \ln \left(1+\mathrm{e}^x\right)-\frac{x^2}{2}$ 是奇函数,从而$\int_{-2}^2 x \ln \left(1+\mathrm{e}^x\right) \mathrm{d} x=\int_{-2}^2 \frac{x^2}{2} \mathrm{~d} x=\frac{8}{3} .$

- 【题目】设 $f(x)$ 是 $[0,2 \pi]$ 的连续函数, 求证$\lim _{n \rightarrow \infty} \int_0^{2 \pi} f(x)|\sin n x| \mathrm{d} x=\frac{2}{\pi} \int_0^{2 \pi} f(x) \mathrm{d} x .$

  分析：本题依然涉及对积分 $\int_0^{2 \pi} f(x)|\sin n x| \mathrm{d} x$ 的估计, 当 $n$ 很大时, 项 $\sin n x$ 的存 在使得被积函数是高频震荡的。为此我们使用分段的方法, 同时结合积分中值定理（完 整版本进行证明。
  Proof. 根据 $\sin n x$ 的周期将区间 $[0,2 \pi]$ 划分, 并使用完整版的积分中值定理
  $$
  \begin{aligned}
  \int_0^{2 \pi} f(x)|\sin n x| \mathrm{d} x &=\sum_{k=1}^n \int_{(2(k-1) \pi) / n}^{(2 k \pi) / n} f(x)|\sin n x| \mathrm{d} x \\
  &=\sum_{k=1}^n f\left(\xi_k\right) \int_{(2(k-1) \pi) / n}^{(2 k \pi) / n}|\sin n x| \mathrm{d} x .
  \end{aligned}
  $$
  其中 $\xi_k \in\left[\frac{(2 k-2) \pi}{n}, \frac{2 k \pi}{n}\right]$ 。注意到积分
  $$
  \int_{(2(k-1) \pi) / n}^{(2 k \pi) / n}|\sin n x| \mathrm{d} x \stackrel{y=n x}{=} \frac{1}{n} \int_{2(k-1) \pi}^{2 k \pi}|\sin y| \mathrm{d} y=\frac{4}{n} .
  $$
  由此
  $$
  \int_0^{2 \pi} f(x)|\sin n x| \mathrm{d} x=\sum_{k=1}^n \frac{4}{n} f\left(\xi_k\right)=\frac{2}{\pi} \sum_{k=1}^n \frac{2 \pi}{n} f\left(\xi_k\right) \rightarrow \frac{2}{\pi} \int_0^{2 \pi} f(x) \mathrm{d} x
  $$
  最后一个极限式使用了黎曼和的定义。

  





#### 8.1 有理式的不定积分和有理化方法

- 关于自变量 $x$ 的有理式、关于三角函数的有理式以及关于某些根式的有理式都是可以“积出来”的；

- 定义：有理函数$\frac{P(x)}{Q(x)} \equiv \frac{a_0 x^n+\cdots+a_n}{b_0 x^m+\cdots+b_m},$通常我们假定 $P(x)$ 与 $Q(x)$ 没有公因子, $a_0 \neq 0, b_0 \neq 0$.

  根据$Q(x)$的适当的分解求根，可以将上述有理函数表示成：$\frac{P(x)}{Q(x)}=\sum_{j=1}^k \sum_{n=1}^{n_j} \frac{A_{n j}}{\left(x-a_j\right)^n}+\sum_{i=1}^l \sum_{m=1}^{m_i} \frac{B_{m i} x+C_{m i}}{\left(x^2+p_i x+q_i\right)^m}$

  因此实际上只需要考虑基本的四个简单积分计算公式即可，具体见课本134-137页。

- 计算待定系数的方法：（1）通分比较多项式的系数法；（2）取特例的方法；

- 【例题】计算两个不定积分$I=\int \frac{\mathrm{d} x}{1+x^4}$和$J=\int \frac{x^2 \mathrm{~d} x}{1+x^4}$

  Proof. 首先计算 $I+J$ 得, 考虑换元 $y=x-\frac{1}{x}$, 那么 $\mathrm{d} y=\left(1+\frac{1}{x^2}\right) \mathrm{d} x$ :
  $$
  \begin{aligned}
  \int \frac{1+x^2}{1+x^4} \mathrm{~d} x &=\int \frac{\left(\frac{1}{x^2}+1\right) \mathrm{d} x}{\frac{1}{x^2}+x^2} \\
  &=\int \frac{\mathrm{d}\left(x-\frac{1}{x}\right)}{\left(x-\frac{1}{x}\right)^2+2}=\int \frac{\mathrm{d} y}{y^2+2} \\
  &=\frac{\sqrt{2}}{2} \arctan \left(\frac{\sqrt{2}}{2} y\right)+C=\frac{\sqrt{2}}{2} \arctan \left(\frac{\sqrt{2}}{2}\left(x-\frac{1}{x}\right)\right)+C .
  \end{aligned}
  $$
  再计算 $-I+J$, 考虑换元 $z=x+\frac{1}{x}$, 那么 $\mathrm{d} z=\left(1-\frac{1}{x^2}\right) \mathrm{d} x$ :
  $$
  \begin{aligned}
  \int \frac{x^2-1}{1+x^4} \mathrm{~d} x &=\int \frac{\left(1-\frac{1}{x^2}\right) \mathrm{d} x}{\frac{1}{x^2}+x^2} \\
  &=\int \frac{\mathrm{d}\left(x+\frac{1}{x}\right)}{\left(x+\frac{1}{x}\right)^2-2}=\int \frac{\mathrm{d} z}{z^2-2}=\frac{\sqrt{2}}{4} \int\left(\frac{1}{z-\sqrt{2}}-\frac{1}{z+\sqrt{2}}\right) \\
  &=\frac{\sqrt{2}}{4} \ln \left|\frac{z-\sqrt{2}}{z+\sqrt{2}}\right|+C=\frac{\sqrt{2}}{4} \ln \left|\frac{x-\sqrt{2} x+1}{x+\sqrt{2} x+1}\right|+C .
  \end{aligned}
  $$
  由此可得$I=\frac{\sqrt{2}}{4} \arctan \left(\frac{\sqrt{2}}{2}\left(x-\frac{1}{x}\right)\right)-\frac{\sqrt{2}}{8} \ln \left|\frac{x-\sqrt{2} x+1}{x+\sqrt{2} x+1}\right|+C .$

  以及$J=\frac{\sqrt{2}}{4} \arctan \left(\frac{\sqrt{2}}{2}\left(x-\frac{1}{x}\right)\right)+\frac{\sqrt{2}}{8} \ln \left|\frac{x-\sqrt{2} x+1}{x+\sqrt{2} x+1}\right|+C .$





#### 8.2 三角函数有理式的不定积分

- 三角函数的有理式：对三角函数及常数函数进行有限次加、减、乘、除所得的表达式.

  一般说来,若 $R(x, y)$ 是 $x$ 与 $y$ 的有理式 (也即 $x, y$ 的两个多项式之 商), 则称 $R(\sin x, \cos x)$ 是一个三角函数之有理式.

- 通用解法：变量替换$t=\tan \frac{x}{2}$将三角函数有理式变为关于 $t$ 的有理函数；
  设 $R(x, y)$ 是关于 $x, y$ 的有理式, 而我们要求的不定积分是$\int R(\sin x, \cos x) \mathrm{d} x .$因为 $\sin x=2 \sin \frac{x}{2} \cos \frac{x}{2}=2 \tan \frac{x}{2} \cdot\left(1+\tan ^2 \frac{x}{2}\right)^{-1}$, 故 $\sin x=2 t /\left(1+t^2\right)$. 又因为 $\cos x=2 \cos ^2 \frac{x}{2}-1$, 故 $\cos x=\left(1-t^2\right) /\left(1+t^2\right)$. 而 $\mathrm{d} t=\frac{1}{2} \sec ^2 \frac{x}{2} \mathrm{~d} x$, 也即 $\mathrm{d} x=2\left(1+t^2\right)^{-1} \mathrm{~d} t$. 这样, 在变量替换之后上述积分变成
  $$
  \int R\left(\frac{2 t}{1+t^2}, \frac{1-t^2}{1+t^2}\right) \cdot \frac{2}{1+t^2} \mathrm{~d} t .
  $$

- 常见关于三角函数的求解方法：

  - 如果可以写成$f(sinx)cosx$的形式，可以利用换元法；
  - 如果是关于$sinx,cosx$的齐次式的形式，可以利用$t=tanx$的换元法化成有理函数的积分；
  - 如果被积函数都是 $\sin x$ 及 $\cos x$ 的偶次方幂, 我们可以利用倍 角公式降低其方幂；

- 【例题】计算定积分 $\int_0^\pi \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x$ 。
  函数 $\frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}}$ 图像如图4所示, 显然有 $f(x)+f(\pi-x)=0$, 即关于轴 $x=\frac{\pi}{2}$ 对 称的点 $x$ 和 $\pi-x$ 的函数值相反, 由此积分值 $\int_0^\pi \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x$ 显然为 0 。不过我们即将 用一些不同的视角看这个积分。
  视角 1：从NL公式出发 我们首先计算不定积分
  $$
  \begin{aligned}
  \int \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x \stackrel{t=\sin x}{=} \int \frac{\mathrm{d} t}{\sqrt{1+t^2}}=\ln \left(\sqrt{1+t^2}+t\right)+C \\
  &=\ln \left(\sqrt{1+\sin ^2 x}+\sin x\right)+C .
  \end{aligned}
  $$
  显然函数 $F(x)=\ln \left(\sqrt{1+\sin ^2 x}+\sin x\right)$ 是 $f(x)=\frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}}$ 在 $[0, \pi]$ 上一个原函 数。由 $\mathrm{NL}$ 公式
  $$
  \int_0^\pi \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x=\left.\ln \left(\sqrt{1+\sin ^2 x}+\sin x\right)\right|_0 ^\pi=0
  $$
  视角2: 从定积分换元法出发 根据不定积分的分析, 我们希望使用定积分换元法 计算这一问题。如果直接套用公式(17), 并选择换元关系 $t=\sin x$, 由于 $\sin \pi=\sin 0=$ 0 , 很容易错误地得到下述式子
  $$
  \int_0^\pi \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x=\int_0^0 \frac{\mathrm{d} t}{\sqrt{1+t^2}} .
  $$
  实际上上述换元法的使用方式是错误的。因为根据换元法的要求, 我们必须要 求 $x$ 从 0 到 $\pi$ 变化时, $t=\sin x$ 在 $[\sin 0, \sin \pi]=\{0\}$ 变化, 即只能取 0 , 这显然是错误的换 元。实际上, 当 $x$ 从 0 到 $\pi$ 变化, 虽然 $t$ 的 “起点” 和 “终点”都是0, 但是其变化过程是 先由0变化到 1 ( $t=\frac{\pi}{2}$​ 时）然后回到0, 而不是在0 “原地不动”。因此正确的换元法应该取如下分段:
  $$
  \begin{gathered}
  \int_0^{\frac{\pi}{2}} \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x=\int_0^1 \frac{\mathrm{d} t}{\sqrt{1+t^2}} . \\
  \int_{\frac{\pi}{2}}^\pi \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x=\int_1^0 \frac{\mathrm{d} t}{\sqrt{1+t^2}} .
  \end{gathered}
  $$
  在 $x \in\left[0, \frac{\pi}{2}\right]$ 和 $x \in\left[\frac{\pi}{2}, \pi\right]$ 用换元法, 得到的关于 $t$ 的积分被积函数一致但上下限相反, 分 别代表了 $t$ 从 0 变为 1 和 $t$ 从 1 回到 0 过程, 由此 $\int_0^\pi \frac{\cos x}{\sqrt{\cos ^2 x+2 \sin ^2 x}} \mathrm{~d} x=0$ 





#### 8.3 某些根式的不定积分

- 某些特殊形式的无理式的积分也能经过变量替换, 使被积函数变成新变量的有理式, 从而求出其积分.
- 常见根式的求解方法：
  - 如果是$\int R(x, \sqrt[n]{a x+b}) \mathrm{d} x \quad(a \neq 0)$的形式可以采用：$x=\left(t^n-b\right) / a$；
  - 如果是$\int R\left[x, \sqrt[n]{\frac{a x+b}{c x+d}}\right] \mathrm{d} x$的形式可以采用：$t=\sqrt[n]{\frac{a x+b}{c x+d}}$;

- 【例题】求 $\int \frac{\sqrt[3]{1+\sqrt[4]{x}}}{\sqrt{x}} \mathrm{~d} x$.
  解：令 $\sqrt[3]{1+\sqrt[4]{x}}=t$, 则 $x=\left(t^3-1\right)^4, \mathrm{~d} x=12 t^2\left(t^3-1\right)^3 \mathrm{~d} t$. 于是
  $$
  \begin{aligned}
  & \int \frac{\sqrt[3]{1+\sqrt[4]{x}}}{\sqrt{x}} \mathrm{~d} x=\int \frac{t}{\left(t^3-1\right)^2} \cdot 12 t^2\left(t^3-1\right)^3 \mathrm{~d} t \\
  =& 12 \int\left(t^6-t^3\right) \mathrm{d} t=12\left(\frac{t^7}{7}-\frac{t^4}{4}\right)+C \\
  =& \frac{3}{7} t^4\left(4 t^3-7\right)+C=\frac{3}{7}(\sqrt[3]{1+\sqrt[4]{x}})^4(4 \sqrt[4]{x}-3)+C .
  \end{aligned}
  $$







#### 8.4 定积分的分部积分法则与换元积分法则

- 分部积分法计算定积分的方法：

  - 直接利用定积分的分部积分公式：$\int_a^b u(x) v^{\prime}(x) \mathrm{d} x=\left.u(x) v(x)\right|_a ^b-\int_a^b v(x) u^{\prime}(x) \mathrm{d} x .$
  - 先利用不定积分求解出原函数，然后再利用NL公式进行计算，注意不定积分的常数项在左右侧相减的时候消去了；
  - 可以利用不定积分求导数检测计算结果，也可以利用定积分的值检测，但是定积分的值只是“部分检测”；

- 必须要记住的结论：
  $$
  \begin{aligned}
  &\int_0^{\frac{\pi}{2}} \sin ^{2 k} x \mathrm{~d} x=\frac{(2 k-1) ! !}{(2 k) ! !} \cdot \frac{\pi}{2}, \quad k=1,2, \cdots ; \\
  &\int_0^{\frac{\pi}{2}} \sin ^{2 k+1} x \mathrm{~d} x=\frac{(2 k) ! !}{(2 k+1) ! !}, \quad k=0,1,2, \cdots,
  \end{aligned}
  $$

- 换元积分方法：设 $f(x)$ 在 $[A, B]$ 上连续, 又设 $\varphi(t)$ 在 $[\alpha, \beta]$ 上有连续的导函 数, 且当 $t$ 在 $[\alpha, \beta]$ 中 变动 时 $\varphi(t)$ 在 $[A, B]$ 内变动. 假定$\varphi(\alpha)=a, \quad \varphi(\beta)=b, \quad a, b \in[A, B],$则$\int_a^b f(x) \mathrm{d} x=\int_a^\beta f(\varphi(t)) \varphi^{\prime}(t) \mathrm{d} t$.

  - 定积分的换元方法中不要求变换具有反函数，因为不需要反解出$x$；
  - 在换元的时候务必注意积分上下限也要做相应的改变，只需注意换元过程中的对应关系！

- 关于偶函数奇函数和周期函数的积分：

  - 奇函数在关于原点对称的区间上积分值为0！ 虽然待求解的函数不一定是奇函数，但是通过配凑或分解可以分解出奇函数；
  - 周期函数积分的性质：$\int_0^T f(x) \mathrm{d} x=\int_a^{a+T} f(x) \mathrm{d} x$.
  - 关于周期函数的积分常常是将积分区间进行拆解，拆解出一个或者多个周期和剩下的部分进行做题；

- 周期函数的性质补充：

  - 只要存在一个严格大于0的周期就是周期函数，可以没有最小正周期，比如狄利克雷函数；
  - 周期函数不要求在整个数轴上是有定义的；
  - 周期函数的周期是有无穷多个的，因此周期的正整数倍均是其周期；

- 【例题】利用换元积分法证明:$\int_0^\pi x f(\sin x) \mathrm{d} x=\pi \int_0^{\frac{\pi}{2}} f(\sin x) \mathrm{d} x .$

  参见课本例7，只需将区间分成$[0,\pi/2]$和$[\pi/2,\pi]$，并在后边的区间上使用换元法$t=\pi-x$即可。

- 【例题】设 $f(x)$ 是以 $T$ 为周期的连续函数, $f\left(x_0\right) \neq 0$, 且 $\int_0^T f(x) \mathrm{d} x=0$, 证明: $f(x)$ 在 区间 $\left(x_0, x_0+T\right)$ 内至少有两个根.

  周期函数的性质：在一个周期的左右端点值相等,$f(0)=f(T)$。连续函数在闭区间上的性质：介值性，最值性。

  首先不妨假设$f(x_{0}) = f(x_{0}+T) > 0 $成立：

  利用积分为0并且函数不可能是0函数，说明最小值一定是严格小于0，并且不可能在左右端点处取得，比如$\xi \in \left(x_0, x_0+T\right)$；

  然后再利用介值定理说明在$\xi$的左右两侧至少各存在一个根即可；

- 【例题】计算定积分 $\int_{-1}^1 x^4 \sqrt{1-x^2} \mathrm{~d} x$ 。
  分析：本题为思路明确的三角换元法题目, 还要涉及递推定积分 $I_n=\int_0^{\frac{\pi}{2}} \sin ^n x \mathrm{~d} x$ 的 计算, 是具有综合性的习题。
  Proof. 首先显然 $x^4 \sqrt{1-x^2}$ 是偶函数, 因此$\int_{-1}^1 x^4 \sqrt{1-x^2} \mathrm{~d} x=2 \int_0^1 x^4 \sqrt{1-x^2} \mathrm{~d} x .$

  接着进行三角换元 $x=\sin t$，也就是$\int_0^1 x^4 \sqrt{1-x^2} \mathrm{~d} x=\int_0^{\frac{\pi}{2}} \sin ^4 t \cos ^2 t \mathrm{~d} t=\int_0^{\frac{\pi}{2}} \sin ^4 t \mathrm{~d} t-\int_0^{\frac{\pi}{2}} \sin ^6 t \mathrm{~d} t$

- 【例题】考虑积分 $\int_{-1}^1 \frac{x^2 \arcsin x}{1+x^2} \mathrm{~d} x$, 被积函数 $\frac{x^2 \arcsin x}{1+x^2}$ 是奇函数, 由此$\int_{-1}^1 \frac{x^2 \arcsin x}{1+x^2} \mathrm{~d} x=0 .$

由此$\int_{-1}^1 \frac{x^2(1+\arcsin x)}{1+x^2} \mathrm{~d} x=\int_{-1}^1 \frac{x^2}{1+x^2} \mathrm{~d} x=\left.(x-\arctan x)\right|_{-1} ^1=2-\frac{\pi}{2}$.

- 【例题】求极限$\lim _{x \rightarrow 0+0} \frac{1}{x} \int_0^x \sin \frac{1}{t} \mathrm{~d} t$
  $$
  \begin{aligned}
  \int_0^x \sin \frac{1}{t} \mathrm{~d} t &=\int_0^x t^2 \cdot\left(\frac{1}{t^2} \sin \frac{1}{t}\right) \mathrm{d} t=\int_0^x t^2 \cdot\left(\cos \frac{1}{t}\right)^{\prime} \mathrm{d} t \\
  &=\left.t^2 \cos \frac{1}{t}\right|_0 ^x-2 \int_0^x t \cos \frac{1}{t} \mathrm{~d} t \\
  &=x^2 \cos \frac{1}{x}-2 \int_0^x t \cos \frac{1}{t} \mathrm{~d} t
  \end{aligned}
  $$
  那么分别计算有$\lim _{x \rightarrow 0+0} \frac{x^2 \cos \frac{1}{x}}{x}=0 .$此外由于
  $$
  \left|\int_0^x t \cos \frac{1}{t} \mathrm{~d} t\right| \leq \int_0^x\left|t \cos \frac{1}{t}\right| \mathrm{d} t \leq \int_0^x t \mathrm{~d} t=\frac{x^2}{2} .
  $$
  由夹逼原理$\lim _{x \rightarrow 0+0} \frac{\int_0^x t \cos \frac{1}{t} \mathrm{~d} t}{x}=0 .$因此$\lim _{x \rightarrow 0+0} \frac{1}{x} \int_0^x \sin \frac{1}{t} \mathrm{~d} t=\lim _{x \rightarrow 0+0} \frac{x^2 \cos \frac{1}{x}-2 \int_0^x t \cos \frac{1}{t} \mathrm{~d} t}{x}=0$.

  



#### 8.5 定积分的应用

- 平面图形的面积
  - 用一般方程计算两个曲线 $y=f(x)$ 与 $y=g(x)$ 夹出图形面积: $S=\int_a^b \mid f(x)-g(x) \mid \mathrm{d} x$, 积分上下限 $a, b$ 需要由图形决定。
  - 用极坐标计算图形面积: $S=\frac{1}{2} \int_\alpha^\beta r^2(\theta) \mathrm{d} \theta$ 。
- 曲线弧长的计算：
  - 用一般方程算弧长: $s=\int_a^b \sqrt{1+f^{\prime}(x)^2} \mathrm{~d} x$ 。
  - 用参数方程算弧长: $s=\int_\alpha^\beta \sqrt{x^{\prime}(t)^2+y^{\prime}(t)^2} \mathrm{~d} t$ 。
  - 用极坐标方程算弧长: $s=\int_\alpha^\beta \sqrt{r(\theta)^2+r^{\prime}(\theta)^2} \mathrm{~d} \theta$ 。
- 旋转体的体积和侧面积
  - 用一般方程算旋转体体积: $V=\pi \int_a^b f^2(x) \mathrm{d} x$ ；
  - 用一般方程算侧面积: $S=2 \pi \int_a^b f(x) \sqrt{1+f^{\prime}(x)^2} \mathrm{~d} x$ ；
  - 用参数方程算侧面积: $S=2 \pi \int_\alpha^\beta y(t) \sqrt{x^{\prime}(t)^2+y^{\prime}(t)^2} \mathrm{~d} t$ ；
  - 用极坐标方程算侧面积: $S=2 \pi \int_\alpha^\beta r(\theta) \sin \theta \sqrt{r(\theta)^2+r^{\prime}(\theta)^2} \mathrm{~d} \theta$ ；
- 微元法：将被积分的量看成是常数，或者说积分得到量的导数值看成在dx微段上是常数，即可得其一阶近似，然后计算其积分。
- 定积分在物理上的应用：
  - 路程: $S=\int_{t_1}^{t_2} v(t) d t$ (速度关于时间积分)
  - 做功: $W=\int_{s_1}^{s_2} F(x) d x$ (力关于位移积分)
  - 质量: $m=\int_a^b \rho(s) d s$ (曲线质量)
  - 质心: $\bar{x}=\frac{\int_a^b x \rho(s) d s}{\int_a^b \rho(s) d s}, \bar{y}=\frac{\int_a^b y \rho(s) d s}{\int_a^b \rho(s) d s}$ (曲线质心)
- 【例题】