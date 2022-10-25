《高等数学A》第七次习题课

> Author ZhenLiu
>
> 2022/10/18



#### 课前小测

- 【题目】求极限：$\lim _{x \rightarrow 0+0} \frac{1-\sqrt{\cos x}}{x-x \cos \sqrt{x}}=\lim _{x \rightarrow 0+0} \frac{1-\cos x}{x(1-\cos \sqrt{x})(1+\sqrt{\cos x})}=\lim _{x \rightarrow 0+0} \frac{1-\cos x}{2 x(1-\cos \sqrt{x})},$

  这里使用了 $\lim _{x \rightarrow 0+0} 1+\sqrt{\cos x}=2$ 。根据等价无穷小关系 $1-\cos x \sim \frac{x^2}{2}$ 和 $1-\cos \sqrt{x} \sim$ $\frac{x}{2}$ 得
  $$
  \lim _{x \rightarrow 0+0} \frac{1-\sqrt{\cos x}}{x-x \cos \sqrt{x}}=\lim _{x \rightarrow 0+0} \frac{1-\cos x}{2 x(1-\cos \sqrt{x})}=\lim _{x \rightarrow 0+0} \frac{\frac{x^2}{2}}{2 x \cdot \frac{x}{2}}=\frac{1}{2} .
  $$

- 【题目】求极限：$\lim _{x \rightarrow 0} \frac{\ln (1+\sqrt{x \sin x})}{|\tan x|}=\lim _{x \rightarrow 0} \frac{\sqrt{x \sin x}}{|x|}=\lim _{x \rightarrow 0} \sqrt{\frac{\sin x}{x}}=1$

- 【题目】设 $f(x)$ 在 $(-\infty,+\infty)$ 上二次可微, 且对 $\forall x, h$, 有 $f(x+h)-f(x)=h f^{\prime}\left(x+\frac{1}{2} h\right)$.
  求证: $f(x)$ 为二次函数.
  证明 已知$f(x+h)-f(x)=h f^{\prime}\left(x+\frac{1}{2} h\right),$两边对 $h$ 求导, 所以对 $\forall x, h$, 有
  $$
  f^{\prime}(x+h)=f^{\prime}\left(x+\frac{1}{2} h\right)+\frac{1}{2} h f^{\prime \prime}\left(x+\frac{1}{2} h\right) .
  $$
  特别对 $x=-\frac{1}{2} h$, 有$f^{\prime}\left(\frac{1}{2} h\right)=f^{\prime}(0)+\frac{1}{2} h f^{\prime \prime}(0) .$第一个式子中令 $x=0$, 得$f(h)-f(0)=h f^{\prime}\left(\frac{1}{2} h\right) .$整理得到$f(h)=f(0)+h f^{\prime}(0)+\frac{1}{2} h^2 f^{\prime \prime}(0) .$由 $h$ 的任意性知, $f$ 为二次函数.

- 【题目】2020年高等数学 $\boldsymbol{A}$ 期中考试题. 设 $f(x)$ 为 $(0,+\infty)$ 上定义, 在定义域的各个点连 续, 且 $f\left(x^2\right)=f(x)$ 对一切 $x$ 成立, 设 $f(2021)=1$, 求 $f(2022)$ 。
  Proof. 根据题设有$1=f(2021)=f(\sqrt{2021})=f(\sqrt[4]{2021})=\cdots$,由此对于一切 $n \in \mathbb{N}^*$ 有 $f\left(2021^{2^{-n}}\right)=f(2021)=1$ 。设 $y_n=2021^{2^{-n}}$, 显然 $\lim _{n \rightarrow \infty} y_n=$ 1。根据序列化的连续函数的定义有 $\lim _{n \rightarrow \infty} f\left(y_n\right)=f(1)$, 由此 $f(1)=1$ 。
  接下来再设 $z_n=2022^{2^{-n}}$, 同理也有 $f\left(z_n\right)=f(2022)$ 对一切 $n \in \mathbb{N}^*$ 成立, 此外我们 还有 $\lim _{n \rightarrow \infty} f\left(z_n\right)=f(1)$, 因此 $f(2022)=f(1)=1$ 。

  



#### 7.1 变上限积分

- 定义：设 $f(x)$ 在区间 $[a, b]$ 上可积. 定义 $G(x)=\int_a^x f(t) \mathrm{d} t(a \leq x \leq b)$, 称 $G(x)$ 为 $f(x)$ 在 $[a, b]$ 上的变动上限的积分
  - 注意它是积分上限$x$的函数.
  - 积分变量是$t$，其对应的积分区间是$[a,x]$.
- 【性质】【例题】：设 $f(x)$ 在 $[a, b]$ 上有定义, $G(x)$ 为 $f(x)$ 在 $[a, b]$ 上的变动上限的积分.
  (i) 若 $f(x)$ 在 $[a, b]$ 上可积, 则 $G(x)$ 在 $[a, b]$ 上连续;
  (ii) 若 $f(x)$ 在 $[a, b]$ 上可积, 且在点 $x_0 \in[a, b]$ 连绔, 则 $G(x)$ 在点, $x_0$ 可导 且 $G^{\prime}\left(x_0\right)=f\left(x_0\right)$.(对于区间的左 (右) 端点, $g(x)$ 自然只是右 (左) 可导.)
  证明 (i) 因为 $f(x)$ 在 $[a, b]$ 上可积, 所以 $G(x)$ 在 $[a, b]$ 上有定义, 且 $f(x)$ 在 $[a, b]$ 上有界, 即有常数 $M>0$, 使得 $|f(x)| \leq M$. 从而对任意 $x, x+\Delta x \in[a, b]$, 有

$$
\begin{aligned}
|G(x+\Delta x)-G(x)| &=\left|\int_a^{x+\Delta x} f(t) \mathrm{d} t-\int_a^x f(t) \mathrm{d} t\right| \\
&=\left|\int_x^{x+\Delta x} f(t) \mathrm{d} t\right| \\
& \leq\left|\int_x^{x+\Delta x}\right| f(t)|\mathrm{d} t| \leq M|\Delta x|
\end{aligned}
$$
因而当 $\Delta x \rightarrow 0$ 时, 有 $|G(x+\Delta x)-G(x)| \rightarrow 0$. 这就证明了 $G(x)$ 在点 $x \in[a, b]$ 连续. 再由 $x$ 的任意性即知 $G(x)$ 在 $[a, b]$ 上连续.

实际上，我们证明了原函数是Lipsthiz连续的，从而一定是连续的。

(ii) 按 $G(x)$ 的定义, 当 $x_0, x_0+\Delta x \in[a, b]$ 时, 有
$$
\begin{aligned}
&\frac{G\left(x_0+\Delta x\right)-G\left(x_0\right)}{\frac{1 x}{\Delta x}}-f\left(x_0\right) \\
&=\frac{1}{\Delta x} \int_{x_0}^{x_0+\Delta x} f(t) \mathrm{d} t-f\left(x_0\right) \\
&=\frac{1}{\Delta x} \int_{x_0}^{x_0+\Delta x}\left[f(t)-f\left(x_0\right)\right] \mathrm{d} t .
\end{aligned}
$$
因为 $f(x)$ 在点 $x_0$ 连续, 故对任给的 $\varepsilon>0$, 都有 $\delta>0$, 使当 $t \in[a, b],\left|t-x_0\right|<\delta$ 时, 就有
$$
\left|f(t)-f\left(x_0\right)\right|<\varepsilon .
$$
从而当 $|\Delta x|<\delta$ 时, 由 (4.1) 和 (4.2) 得到
$$
\begin{aligned}
&\left|\frac{G\left(x_0+\Delta x_0\right)-G\left(x_0\right)}{\Delta x}-f\left(x_0\right)\right| \\
&\leq \frac{1}{|\Delta x|}\left|\int_{x_0}^{x_0+\Delta x}\right| f(t)-f\left(x_0\right)|\mathrm{d} t| \\
&<\frac{\varepsilon}{|\Delta x|}\left|\int_{x_0}^{x_0+\Delta x} \mathrm{~d} x\right|=\varepsilon .
\end{aligned}
$$
这表明 $G(x)$ 在点 $x_0$ 可导, 且 $G^{\prime}\left(x_0\right)=f\left(x_0\right)$.

- 积分中值定理：设函数 $f(x)$ 在区间 $[a, b]$ 上连续,则在 $[a, b]$ 内至少存在一点 $c$, 使得$\int_a^b f(x) \mathrm{d} x=f(c) \cdot(b-a)$

- 【例题】设 $F(x)$ 在 $[a, b]$ 上有连续的导函数 $F^{\prime}(x)$. 试证明: 存在一点 $c \in[a, b]$, 使$F(b)-F(a)=F^{\prime}(c)(b-a) .$

  只需注意$F(b)-F(a)= \int_{a}^{b}F'(t)dt = F'(c)(b-a) $即可。

- 变上限积分的导数：$\frac{\mathrm{d}}{\mathrm{d} x} \int_a^x f(t) \mathrm{d} t=f(x)$并且$\int_x^b f(t) \mathrm{d} t=-\int_b^x f(t) \mathrm{d} t$，可以推出一般的公式.

  【例题】构造变上限积分求导数：设函数 $f(x)$ 在 $[0,1]$ 上可导, 且 $0 \leq f^{\prime}(x) \leq 1, f(0)=0$, 求证$\left[\int_0^1 f(x) \mathrm{d} x\right]^2 \geq \int_0^1 f^3(x) \mathrm{d} x .$

  证明:令$F(t)=\left[\int_0^t f(x) \mathrm{d} x\right]^2-\int_0^t f^3(x) \mathrm{d} x$,则 $F(0)=0, F(t)$ 在 $[0,1]$ 上两次可导, 且有
  $$
  F^{\prime}(t)=2 f(t) \int_0^t f(x) \mathrm{d} x-f^3(t)=f(t) G(t),
  $$
  其中$G(t)=2 \int_0^t f(x) \mathrm{d} x-f^2(t)$,在 $[0,1]$ 上有定义, 满足条件 $G(0)=0$, 且有
  $$
  G^{\prime}(t)=2 f(t)-2 f(t) f^{\prime}(t)=2 f(t)\left(1-f^{\prime}(t)\right) \geq 0 .
  $$
  可见 $G(t)$ 为 $[0,1]$ 上的递增函数, 故有 $G(t) \geq 0$.因为 $f(0)=0$ 且 $f^{\prime}(t) \geq 0$, 故在 $[0,1]$ 上有 $f(t) \geq 0$. 从而知 $F^{\prime}(t) \geq 0$. 又因为 $F(0)=0$, 所以在 $[0,1]$ 上有 $F(t) \geq 0$, 特别地有 $F(1) \geq 0$.

- 【例题】已知当 $a \leq x \leq b$ 时, $f^{\prime}(x)>0, f^{\prime \prime}(x)>0$, 证明$(b-a) f(a)<\int_a^b f(x) \mathrm{d} x<\frac{b-a}{2}[f(a)+f(b)] .$

证法一: 中值定理 + 辅助函数(1) $f(x)$ 在 $[a, b]$ 上可导, 故连续, 应用积分第一中值定理有$\int_a^b f(x) \mathrm{d} x=f(\xi)(b-a), \quad \xi \in[a, b] .$

又因 $f^{\prime}(x)>0$, 即 $f(x)$ 在 $[a, b]$ 上严格递增, 故必有 $\xi \in(a, b)$, 从而有 $f(a)<f(\xi)<f(b)$, 所证不等式左端成立.
(2) 构造辅助函数$F(t)=\frac{t-a}{2}[f(a)+f(t)]-\int_a^t f(x) \mathrm{d} x,$

易知
$$
\begin{gathered}
F(a)=0, \quad F^{\prime}(t)=\frac{1}{2}[f(a)-f(t)]+\frac{t-a}{2} f^{\prime}(t), \\
F^{\prime}(a)=0, \quad F^{\prime \prime}(t)=\frac{t-a}{2} f^{\prime \prime}(t),
\end{gathered}
$$
又因 $f^{\prime \prime}(t)>0$, 故当 $t>a$ 时, $F^{\prime \prime}(t)>0, F^{\prime}(t)$ 严格单调递增, $F^{\prime}(t)>F^{\prime}(a)=0$. 进而可 知 $F(t)$ 在 $[a, b]$ 上严格单调递增, $F(b)>F(a)=0$, 即$\frac{b-a}{2}[f(a)+f(b)]-\int_a^b f(x)>0 .$

证法二: 积分序关系+函数凸性 
(1) 由 $f^{\prime}(x)>0$ 可知 $f(x)$ 在 $[a, b]$ 上严格单调递增, 因此 $\forall x \in(a, b]$, 都有 $f(x)>f(a)$, 故$\int_a^b f(x) \mathrm{d} x>\int_a^b f(a) \mathrm{d} x=(b-a) f(a) .$

(2) 由 $f^{\prime \prime}(x)>0$ 可知 $f(x)$ 在 $[a, b]$ 上严格下凸, 故
$$
\int_a^b f(x) \mathrm{d} x=(b-a) \int_0^1 f((1-t) a+t b) \mathrm{d} t<(b-a) \int_0^1[(1-t) f(a)+t f(b)] \mathrm{d} t=\frac{b-a}{2}[f(a)+f(b)]
$$

- 【例题】设 $f$ 在 $[a, b]$ 上有连续的导数, 证明: (1) 对于任意 $x \in[a, b]$, 有$|f(x)| \leq\left|\frac{1}{b-a} \int_a^b f(x) \mathrm{d} x\right|+\int_a^b\left|f^{\prime}(x)\right| \mathrm{d} x .$

  (2) 如果 $f(a) \neq f(b)$, 则$|f(x)|<\left|\frac{1}{b-a} \int_a^b f(x) \mathrm{d} x\right|+\int_a^b\left|f^{\prime}(x)\right| \mathrm{d} x .$

  只需注意$f(x)=\int_{c}^{x}f'(t)dt+f(c)$，其中$c$是中值定理中的常数，再利用积分保序相关推论即可；第二问反证法，只需注意在连续不等式中如果首尾相等，那么中间的所有不等号都取成等号，再由$x$的任意性得到导数恒为0，从而矛盾。

  





#### 7.2 微积分基本定理

- 定理: 设函数 $f(x)$ 在 $[a, b]$ 上可积, $F(x)$ 是 $f(x)$ 在 $[a, b]$ 上的一个原 函数, 则
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

  - 注意：上式中关于$f(x)$的要求减弱为可积，但是这里需要用到后边才能学到的$Lagrange$中值定理，只要$F(x)$可导即可。

  - 注意：可积函数不一定有原函数$R(x)$

  - 注意：有原函数不一定是可积函数，参考课本例题$\frac{1}{2}x^{2}-\frac{1}{x}$是可导的，但是其导函数在[0,1]上是不可积的。

    【例题】验证 $\frac{1}{2} x^2-\frac{1}{x}$ 是 $x+\frac{1}{x^2}$ 的一个原函数并计算定积分$\int_2^4\left(x+\frac{1}{x^2}\right) \mathrm{d} x .$

    试问下式$\int_{-1}^1\left(x+\frac{1}{x^2}\right) \mathrm{d} x=\left.\left(\frac{1}{2} x^2-\frac{1}{x}\right)\right|_{-1} ^1$是否成立? 为什么?

- 【例题】由微积分基本定理不难验证下列表达式:
  $$
  \begin{gathered}
  \arcsin x=\int_0^x \frac{\mathrm{d} t}{\sqrt{1-t^2}} \quad(-1<x<1), \\
  \arctan x=\int_0^x \frac{\mathrm{d} t}{1+t^2}, \quad \ln x=\int_1^x \frac{\mathrm{d} t}{t} \quad(x>0) .
  \end{gathered}
  $$
  这些公式告诉我们一个有趣的事实: 反三角函数及对数函数可以表示成某些简单函数的积分. 

- 【例题】设函数 $x=\varphi(y)$ 在 $[c, d]$ 上连续且 $\varphi(y)>0$. 试用定积分表示由曲线 $x=\varphi(y)$, $y=c, y=d$ 及 $y$ 轴所围的图形的面积; 又设 $c \geqslant 0$, 函数 $x=\varphi(y)$ 在 $[c, d]$ 上严格递增. 试 求积分和$\int_c^d \varphi(y) \mathrm{d} y+\int_a^b \psi(x) \mathrm{d} x,$其中 $y=\psi(x)$ 是 $x=\varphi(y)$ 的反函数, $a=\varphi(c), b=\varphi(d)$.

- 【例题】设 $f(x)$ 在 $(A, B)$ 上连续, $[a, b] \subset(A, B)$. 证明: $\lim _{h \rightarrow 0} \int_a^b \frac{f(x+h)-f(x)}{h} \mathrm{~d} x=f(b)-f(a)$. 

  证明: 由于 $f(x)$ 在 $(A, B)$ 连续, 因此 $F(x)=\int_a^x f(t) \mathrm{d} t$ 在 $[a, b]$ 内处处可导, 且 $F^{\prime}(x)=f(x)$. 因此$\int_a^b f(x) \mathrm{d} x=F(b)-F(a),$

且若 $a+h \in(A, B), b+h \in(A, B)$, 则$\int_a^b f(x+h) \mathrm{d} x=F(b+h)-F(a+h) .$这样就有
$$
\begin{aligned}
\lim _{h \rightarrow 0} \int_a^b \frac{f(x+h)-f(x)}{h} \mathrm{~d} x &=\lim _{h \rightarrow 0} \frac{1}{h}\left[\int_a^b f(x+h) \mathrm{d} x-\int_a^b f(x) \mathrm{d} x\right] \\
&=\lim _{h \rightarrow 0} \frac{1}{h}[F(b+h)-F(a+h)-F(b)+F(a)] \\
&=\lim _{h \rightarrow 0}\left[\frac{F(b+h)-F(b)}{h}-\frac{F(a+h)-F(a)}{h}\right] \\
&=F^{\prime}(b)-F^{\prime}(a) \\
&=f(b)-f(a)
\end{aligned}
$$




#### 7.3 不定积分的换元法

- 第一换元积分法：凑微分法！

- 第二换元积分法：注意必须要在变换的区间具有反函数，注意最终结果的表示方式！

- 分部积分法：$\int f(x) g^{\prime}(x) d x=f(x) g(x)-\int f^{\prime}(x) g(x) d x$

  反对幂三指！谁在后边就把谁放后边！

  分部积分法有四种典型模式, 如下:
  (1) 降幂: $\int P_m(x)\left\{\sin x, \cos x, e^x\right\} d x$.
  (2) 升幂: $\int P_m(x)\{\arcsin x, \arccos x, \arctan x, \operatorname{arccot} x, \ln x\} d x$.
  (3) 循环: $\int e^{a x}\{\cos b x, \sin b x\} d x$
  (4) 递推: $\int f^n(x) d x$ 例如: $\int \frac{1}{\left(x^2+a^2\right)^n} d x$

- 【例题 】分部积分法有时候会构成一个循环或者递推，给出一个例子：
  $$
  \begin{aligned}
  \int_1^{e^\pi} \cos (\ln x) d x &=\left.x \cos (\ln x)\right|_1 ^{e^\pi}-\int_1^{e^\pi} x d \cos (\ln x) \\
  &=\left.x \cos (\ln x)\right|_1 ^{e^\pi}+\int_1^{e^\pi} \sin (\ln x) d x \\
  &=\left.x \cos (\ln x)\right|_1 ^{e^\pi}+\left.x \sin (\ln x)\right|_1 ^{e^\pi}-\int_1^{e^\pi} x d \sin (\ln x) \\
  &=\left.x \cos (\ln x)\right|_1 ^{e^\pi}+\left.x \sin (\ln x)\right|_1 ^{e^\pi}-\int_1^{e^\pi} \cos (\ln x) d x . \\
  \int_1^{e^\pi} \cos (\ln x) d x &=\frac{1}{2}\left[\left.x \cos (\ln x)\right|_1 ^{e^\pi}+\left.x \sin (\ln x)\right|_1 ^{e^\pi}\right]=-\frac{1}{2}\left(e^\pi+1\right) .
  \end{aligned}
  $$

- 必须掌握的一组公式：
  $$
  \begin{aligned}
  &\int \frac{\mathrm{d} x}{x^2+a^2}=\frac{1}{a} \arctan \frac{x}{a}+C \quad(a>0) ; \\
  &\int \frac{\mathrm{d} x}{x^2-a^2}=\frac{1}{2 a} \ln \left|\frac{x-a}{x+a}\right|+C \quad(a>0) ; \\
  &\int \frac{\mathrm{d} x}{a^2-x^2}=-\frac{1}{2 a} \ln \left|\frac{x-a}{x+a}\right|+C \quad(a>0) ; \\
  &\int \frac{\mathrm{d} x}{\sqrt{x^2 \pm a^2}}=\ln \left|x+\sqrt{x^2 \pm a^2}\right|+C; \\
  &\int \frac{\mathrm{d} x}{\sqrt{a^2-x^2}}=\arcsin \frac{x}{a}+C \quad(a>0) ; \\
  & \int \sqrt{x^2 \pm a^2}  =\frac{1}{2} x \sqrt{x^2 \pm a^2} \pm \frac{a^2}{2} \ln \left|x+\sqrt{x^2 \pm a^2}\right|+C \quad(a>0);\\
  &\int \sqrt{a^2-x^2} \mathrm{~d} x=\frac{x}{2} \sqrt{a^2-x^2}+\frac{a^2}{2} \arcsin \frac{x}{a}+C \quad(a>0).
  \end{aligned}
  $$

- 【例题】求不定积分 $\int \sqrt{x^2 \pm a^2} \mathrm{~d} x, a>0$.

  解 由分部积分公式,
  $$
  \begin{aligned}
  \int \sqrt{x^2 \pm a^2} \mathrm{~d} x &=x \sqrt{x^2 \pm a^2}-\int x \mathrm{~d} \sqrt{x^2 \pm a^2} \\
  &=x \sqrt{x^2 \pm a^2}-\int \frac{x^2}{\sqrt{x^2 \pm a^2}} \mathrm{~d} x \\
  &=x \sqrt{x^2 \pm a^2}-\int \frac{x^2 \pm a^2 \mp a^2}{\sqrt{x^2 \pm a^2}} \mathrm{~d} x \\
  &=x \sqrt{x^2 \pm a^2}-\int \sqrt{x^2 \pm a^2} \mathrm{~d} x \pm a^2 \int \frac{\mathrm{d} x}{\sqrt{x^2 \pm a^2}}
  \end{aligned}
  $$

- 总结: 常用代换 
  (1) 被积函数含有 $\sqrt{a^2-x^2}$, 用 $x=a \sin t$. 因为 $\sin ^2 t+\cos ^2 t=1$;
  (2) 被积函数含有 $\sqrt{a^2+x^2}$, 用 $x=a \tan t$. 因为 $1+\tan ^2 t=\sec ^2 t$;
  (3) 被积函数含有 $\sqrt{x^2-a^2}$, 用 $x=a \sec t$. 因为 $\sec ^2 t-1=\tan ^2 t$;
  (4) 被积函数含有 $\frac{1}{x \sqrt{a x^2+b x+c}}$, 用 $x=\frac{1}{t}$ (倒代换). 因为可以消掉 $\frac{1}{x}$;
  (5) 被积函数含有 $\sqrt[n]{a x+b}$, 用 $t=\sqrt[n]{a x+b}$ (根式代换). 因为可以去掉根号.

- 【例题】求 $\int \frac{x-2}{\sqrt{2 x^2+4 x+5}} \mathrm{~d} x$.
  解 因为$2 x^2+4 x+5=2(x+1)^2+3=[\sqrt{2}(x+1)]^2+3,$故令 $x=\frac{t}{\sqrt{2}}-1$, 即 $\sqrt{2}(x+1)=t$, 便有
  $$
  \begin{aligned}
  & \int \frac{x-2}{\sqrt{2 x^2+4 x+5}} \mathrm{~d} x=\frac{1}{\sqrt{2}} \int \frac{t-3 \sqrt{2}}{\sqrt{t^2+3}} \frac{1}{\sqrt{2}} \mathrm{~d} t \\
  =& \frac{1}{2} \int \frac{t}{\sqrt{t^2+3}} \mathrm{~d} t-\frac{3}{\sqrt{2}} \int \frac{\mathrm{d} t}{\sqrt{t^2+3}} \\
  =& \frac{1}{2} \sqrt{t^2+3}-\frac{3}{\sqrt{2}} \ln \left(t+\sqrt{t^2+3}\right)+C \\
  =& \frac{1}{2} \sqrt{2 x^2+4 x+5}-\frac{3}{\sqrt{2}} \ln \left[\left(\sqrt{2}(x+1)+\sqrt{2 x^2+4 x+5}\right)\right]+C .
  \end{aligned}
  $$

- 【例题】求 $\int \frac{\sqrt[3]{1+\sqrt[4]{x}}}{\sqrt{x}} \mathrm{~d} x$.
  解：令 $\sqrt[3]{1+\sqrt[4]{x}}=t$, 则 $x=\left(t^3-1\right)^4, \mathrm{~d} x=12 t^2\left(t^3-1\right)^3 \mathrm{~d} t$. 于是
  $$
  \begin{aligned}
  & \int \frac{\sqrt[3]{1+\sqrt[4]{x}}}{\sqrt{x}} \mathrm{~d} x=\int \frac{t}{\left(t^3-1\right)^2} \cdot 12 t^2\left(t^3-1\right)^3 \mathrm{~d} t \\
  =& 12 \int\left(t^6-t^3\right) \mathrm{d} t=12\left(\frac{t^7}{7}-\frac{t^4}{4}\right)+C \\
  =& \frac{3}{7} t^4\left(4 t^3-7\right)+C=\frac{3}{7}(\sqrt[3]{1+\sqrt[4]{x}})^4(4 \sqrt[4]{x}-3)+C .
  \end{aligned}
  $$