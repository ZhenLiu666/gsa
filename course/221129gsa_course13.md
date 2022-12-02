《高等数学A》第十三次习题课

> Author ZhenLiu
>
> 2022/11/29



#### 13.1 多元函数的极限

- $\mathbb{R}^n$ 中点 $x=\left(x_1, x_2, \cdots, x_n\right)$ 和点 $y=\left(y_1, y_2, \cdots, y_n\right)$ 的内积:$(x, y)=\sum_{i=1}^n x_i y_i, \forall x, y \in \mathbb{R} .$

  此内积诱导出的 $\mathbb{R}^n$ 上的范数:$|x|=(x, x)^{1 / 2}, \quad \forall x \in \mathbb{R}^n$

  $\mathbb{R}^n$ 中点 $x$ 与点 $y$ 之间的距离: $d(x, y)=|x-y|$.有了度量才能定义收敛的概念，从而定义极限。

- 内点，外点，开集，闭集和区域：在研究多元函数微积分时, 我们对于区域有特殊的兴趣. 它相当于 $\mathbf{R}^1$ 中的开区间. 我们也对有界闭区域有特殊兴趣, 尤其在讨论连续函数的性质 时,它相当于 $\mathbf{R}^1$ 中的闭区间.

- 设有 $n$ 元函数 $f: D \subset \mathbb{R}^n \longrightarrow \mathbb{R}$, 并且 $x^{(0)}$ 是 $D$ 的聚点. 如果存在常数 $l$, 使得对于任意给定的 $\varepsilon>0$, 存在 $\delta>0$, 当 $0<\left|x-x^{(0)}\right|<\delta$ 且 $x \in D$ 时, 总有$|f(x)-l|<\varepsilon,$则称当 $x$ 趋于 $x^{(0)}$ 时, $f(x)$ 以 $l$ 为极限, 记为 $\lim _{x \longrightarrow x^{(0)}} f(x)=l$.

- 沿直线的极限 // 全极限 // 累次极限 与之间的关系和反例！！！ 累次极限存在和换序的充分条件：
  设 $f(x, y)$ 于 $D=\left\{(x, y):\left|x-x_0\right|<\delta_0,\left|y-y_0\right|<\delta_0\right\}$ 上有定义. 如果

  1. $\lim _{(x, y) \longrightarrow\left(x_0, y_0\right)} f(x, y)=a$;
  2. $\forall y \in\left(y_0-\delta_0, y_0+\delta_0\right), y \neq y_0, \lim _{x \longrightarrow x_0} f(x, y)$ 皆存在, 则
  $$
  \lim _{y \longrightarrow y_0} \lim _{x \longrightarrow x_0} f(x, y)=\lim _{(x, y) \longrightarrow\left(x_0, y_0\right)} f(x, y)=a .
  $$
  进一步, 如果还有 $\forall x \in\left(x_0-\delta, x_0+\delta\right), x \neq x_0, \lim _{y \longrightarrow y_0} f(x, y)$ 皆存在, 则
  $$
  \lim _{x \longrightarrow x_0} \lim _{y \longrightarrow y_0} f(x, y)=\lim _{(x, y) \longrightarrow\left(x_0, y_0\right)} f(x, y)=a .
  $$
  从而, 有
  $$
  \lim _{y \longrightarrow y_0} \lim _{x \longrightarrow x_0} f(x, y)=\lim _{x \longrightarrow x_0} \lim _{y \longrightarrow y_0} f(x, y)
  $$

- 求多元函数的极限有㛒下常用方法:

  1. 利用多元函数连续性和函数极限的性质；

  2. 利用不等式放缩或使由夹挤定理；
  3. 利用变量替换换成已知的极限： $\lim _{t \rightarrow 0} \frac{\sin t}{t}=1, \lim _{t \rightarrow 0} \frac{\tan t}{t}=1, \lim _{t \rightarrow \infty}\left(1+\frac{1}{t}\right)^t=e$
  4. 利用初等变形，如分母存理化、对指数形式取外数等等.

- 【例题：用极限定义定明极限】 $\lim _{(x, y) \longrightarrow(0,0)} \frac{x^2 y}{x^2+y^2}=0$.
  证 $\forall \varepsilon>0$, 要使不等式
  $$
  \left|\frac{x^2 y}{x^2+y^2}-0\right| \leq\left|\frac{2 x y}{x^2+y^2}\right||x| \leq|x| \leq \varepsilon .
  $$
  成立, 只须 $|x|<\sqrt{x^2+y^2}=|(x, y)-(0,0)|<\varepsilon$. 取 $\delta=\varepsilon$, 于是 $\forall \varepsilon>0, \exists \delta=\varepsilon>0$, 当 $0<|(x, y)-(0,0)|<\delta$ 时, 总有
  $$
  \left|\frac{x^2 y}{x^2+y^2}-0\right|<\varepsilon
  $$
  即 $\lim _{(x, y) \longrightarrow(0,0)} \frac{x^2 y}{x^2+y^2}=0$.

- 【例题：变量替换】求 $\lim _{(x, y) \rightarrow(0,0)} \frac{x^3+y^3}{x^2+y^2}$.
  分析：直观上看分子的多洏式次数高于分母的多项式次数, 极限应该昰 0 .
  解 令 $x=r \cos \theta, y=r \sin \theta$, 则
  $$
  \lim _{(x, y) \rightarrow(0,0)} \frac{x^3+y^3}{x^2+y^2}=\lim _{r \rightarrow 0} r\left(\cos ^3 \theta+\sin ^3 \theta\right)=0 .
  $$

- 【例题：使用夹挤定理计算极限】求极限 $\lim _{(x, y) \longrightarrow(+\infty,+\infty)} \frac{x+y}{x^2-x y+y^2}$.
  解：由不等式 $x^2+y^2 \geq 2|x y|$ 得
  $$
  \begin{aligned}
  0 & \leq\left|\frac{x+y}{x^2-x y+y^2}\right| \leq \frac{|x+y|}{x^2+y^2-|x y|} \\
  & \leq \frac{|x+y|}{|x y|} \leq \frac{1}{|x|}+\frac{1}{|y|},
  \end{aligned}
  $$
  而 $\lim _{(x, y) \longrightarrow(+\infty,+\infty)}\left(\frac{1}{|x|}+\frac{1}{|y|}\right)=0$, 故有
  $$
  \lim _{(x, y) \longrightarrow(+\infty,+\infty)} \frac{x+y}{x^2-x y+y^2}=0
  $$

- 【例题：使用夹挤定理计算极限】求极限 $\lim _{(x, y) \longrightarrow(+\infty,+\infty)}\left(\frac{x y}{x^2+y^2}\right)^{x^2}$.
  解 由不等式

$$
0 \leq\left(\frac{x y}{x^2+y^2}\right)^{x^2} \leq\left(\frac{1}{2}\right)^{x^2}
$$
及 $\lim _{x \rightarrow+\infty}\left(\frac{1}{2}\right)^{x^2}=0$, 即得
$$
\lim _{(x, y) \longrightarrow(+\infty,+\infty)}\left(\frac{x y}{x^2+y^2}\right)^{x^2}=0 .
$$

- 【例题：使用对数法求极限】求极限 $\lim _{(x, y) \longrightarrow(0,0)}\left(x^2+y^2\right)^{x^2 y^2}$.
  解 由不等式
  $$
  \left|x^2 y^2 \ln \left(x^2+y^2\right)\right| \leq \frac{\left(x^2+y^2\right)^2}{4}\left|\ln \left(x^2+y^2\right)\right|
  $$
  及
  $$
  \lim _{(x, y) \longrightarrow(0,0)} \frac{\left(x^2+y^2\right)^2}{4}\left|\ln \left(x^2+y^2\right)\right|=\lim _{t \longrightarrow 0^{+}} \frac{1}{4} t^2 \ln t=0,
  $$
  即得
  $$
  \lim _{(x, y) \longrightarrow(0,0)}\left(x^2+y^2\right)^{x^2 y^2}=\lim _{(x, y) \longrightarrow(0,0)} e^{x^2 y^2 \ln \left(x^2+y^2\right)}=e^0=1
  $$

- 【例题：根式化简求极限】（思考？）$\text { 求极限 } \lim _{(x, y) \longrightarrow(0,0)} \frac{\sqrt{\left(1+4 x^2\right)\left(1+6 y^2\right)}-1}{2 x^2+3 y^2} \text {. }$

- 【例题：全极限与方向极限】若 $x=\rho \cos \phi, y=\rho \sin \phi,(0 \leq \phi \leq 2 \pi)$ 问下列极限沿怎样的方向 $\phi$ 有确定的极限值存在:
  (a) $\lim _{\rho \rightarrow 0^{+}} e^{\frac{x}{x^2+y^2}}$;
  (b) $\lim _{\rho \longrightarrow+\infty} e^{x^2-y^2} \cdot \sin 2 x y$.（思考？）
  解 (a)
  $$
  \lim _{\rho \longrightarrow 0^{+}} e^{\frac{x}{x^2+y^2}}=\lim _{\rho \longrightarrow 0^{+}} e^{\frac{\cos \phi}{\rho}}= \begin{cases}0, & \cos \phi<0 ; \\ 1, & \cos \phi=0 ; \\ +\infty, & \cos \phi>0 .\end{cases}
  $$
  于是, 仅当 $\cos \phi \leq 0$ 即 $\frac{\pi}{2} \leq \phi \leq \frac{3 \pi}{2}$ 时, 所给的极限才有确定的值.

- 【例题：全极限与方向极限】设 $f(x, y)=\frac{x^4 y^4}{\left(x^4+y^2\right)^3}$, 证明: 当点 $(x, y)$ 沿通过原点的任意直线 $(y=m x)$ 趋于 $(0,0)$ 时, 函 数 $f(x, y)$ 存在极限, 且极限相等. 但是, 此函数在原点不存在极限.
  证 设 $y=m x$ ( $m$ 是通过原点的直线的斜率 $), m \neq 0$ 时, 有
  $$
  \begin{aligned}
  \lim _{(x, y) \longrightarrow(0,0)} \frac{x^4 y^4}{\left(x^4+y^2\right)^3} &=\lim _{(x, y) \longrightarrow(0,0)} \frac{m^4 x^8}{\left(x^4+m^2 x^2\right)^3} \\
  &=\lim _{(x, y) \longrightarrow(0,0)} \frac{m^4 x^2}{\left(x^2+m^2\right)^3}=0 .
  \end{aligned}
  $$
  当 $m=0$ 时, 显然, 也有
  $$
  \lim _{(x, y) \longrightarrow(0,0)} \frac{x^4 y^4}{\left(x^4+y^2\right)^3}=0 .
  $$
  即 $f(x, y)$ 当 $(x, y)$ 沿任意直线 $y=m x$ 趋于 $(0,0)$ 时存在极限, 且极限值为 0 .
  但当 $y=x^2$ 时, 却有
  $$
  \lim _{(x, y) \longrightarrow(0,0)} \frac{x^4 y^4}{\left(x^4+y^2\right)^3}=\lim _{(x, y) \longrightarrow(0,0)} \frac{x^{12}}{8 x^{12}}=\frac{1}{8}
  $$

- 【例题：全极限与累次极限】证明对于函数$f(x, y)=\frac{x^2 y^2}{x^2 y^2+(x-y)^2},$具有 $\lim _{x \rightarrow 0} \lim _{y \rightarrow 0} f(x, y)=\lim _{y \rightarrow 0} \lim _{x \rightarrow 0} f(x, y)=0$, 然而 $\lim _{(x, y) \longrightarrow(0,0)} f(x, y)$ 不存在. 

  证 易得
  $$
  \begin{aligned}
  &\lim _{x \rightarrow 0} \lim _{y \rightarrow 0} \frac{x^2 y^2}{x^2 y^2+(x-y)^2}=\lim _{x \rightarrow 0} 0=0, \\
  &\lim _{y \rightarrow 0} \lim _{x \rightarrow 0} \frac{x^2 y^2}{x^2 y^2+(x-y)^2}=\lim _{y \rightarrow 0} 0=0,
  \end{aligned}
  $$
  现当 $(x, y)$ 沿 $y=k x$ 趋于 $(0,0)$ 时, 即有
  $$
  \lim _{(x, y) \longrightarrow(0,0)} \frac{x^2 y^2}{x^2 y^2+(x-y)^2}=\lim _{(x, y) \longrightarrow(0,0)} \frac{x^4 k^2}{x^4 k^2+x^2(1-k)^2},
  $$
  若 $k=0$ 时, 则该极限为 0 , 若 $k=1$ 时, 则该极限为 1 , 因此 $\lim _{(x, y) \longrightarrow(0,0)} f(x, y)$ 不存在.





#### 13.2 多元函数的连续

- 定义 设函数 $u=f(x, y)$ 在点 $\left(x_0, y_0\right)$ 的一个邻域内有定义. 若函数 $u=f(x, y)$ 当 $(x, y) \rightarrow\left(x_0, y_0\right)$ 时有极限, 且其极限等于函数值 $f\left(x_0, y_0\right)$, 也 即
  $$
  \lim _{(x, y) \rightarrow\left(x_0, y_0\right)} f(x, y)=f\left(x_0, y_0\right),
  $$
  则称函数 $f(x, y)$ 在 $\left(x_0, y_0\right)$ 点连续.

- 多元连续函数的性质：

  - 有界性： $D \subset \mathbb{R}^n$ 为有界闭区域, $f(x)$ 为 $D$ 上的连续函数, 则 $f(x)$ 于 $D$ 上有界.
  - 最值定理： $D \subset \mathbb{R}^n$ 为有界闭区域, $f(x)$ 为 $D$ 上的连续函数, 则 $f(x)$ 于 $D$ 上必取得最大值和最小 值, 即存在 $x_{\min }, x_{\max }$, 使得 $f\left(x_{\min }\right) \leq f(x) \leq f\left(x_{\max }\right), \forall x \in D$.
  - 一致连续性： $D \subset \mathbb{R}^n$ 为有界闭区域, $f(x)$ 为 $D$ 上的连续函数, 则 $f(x)$ 于 $D$ 上一致连续.
  - 介值定理： $D \subset \mathbb{R}^n$ 为有界闭区域, $f(x)$ 于 $D$ 连续, $x^{(1)}, x^{(2)} \in D$, 若 $f\left(x^{(1)}\right) \neq f\left(x^{(2)}\right)$, 则对介 于 $f\left(x^{(1)}\right)$ 与 $f\left(x^{(2)}\right)$ 之间的任何数 $\eta$, 总有 $x^{(0)} \in D$, 使得 $f\left(x^{(0)}\right)=\eta$.

- $\mathbb{R}^n$ 中点集的几个性质

  -  (子点列收敛定理) $\mathbb{R}^n$ 中任意有界点列必有收敛子点列.
  -  (Bolzano-Weierstrass聚点原则) $\mathbb{R}^n$ 中任意含有无限多个点的有界点集必有聚点.
  - (有限覆盖定理) $E \subset \mathbb{R}^n$ 为有界闭集 $\Rightarrow E$ 的任何一个开覆盖, 必存在其有限子覆盖.
  - 紧性与列紧性
    - 紧性—— $E \subset \mathbb{R}^n, E$ 的任何开覆盖, 都存在其有限子覆盖, 称 $E$ 为紧集.
    - 列紧性—— $E \subset \mathbb{R}^n, E$ 中任意点列, 都存在于 $E$ 中收玫的子列, 称 $E$ 为列紧集.
  - $E \subset \mathbb{R}^n, E$ 为列紧集 $\Leftrightarrow E$ 为紧集 $\Leftrightarrow E$ 为有界闭集.

- 【例题：二元连续性和一元连续性】证明函数 $f(x, y)=\left\{\begin{array}{ll}\frac{x^4 y^4}{\left(x^2+y^4\right)^3}, & x^2+y^2 \neq 0, \\ 0, & x^2+y^2=0 .\end{array}\right.$ 当一个变量固定时, 对另一个变量是连 续的, 但 $f(x, y)$ 在原点处是不连续的.
  证：先固定 $y=a$, 若 $a \neq 0$ 则得变量 $x$ 的函数 $g(x)=f(x, a)=\frac{a^4 x^4}{\left(x^2+a^4\right)^3}$, 显然 $g(x)$ 对一 切 $x \in(-\infty,+\infty)$ 均连续; 若 $a=0$, 则 $f(x, 0) \equiv 0$, 显然连续, 故当变量 $y$ 固定时, 函数 $f(x, y)$ 对变 量 $x$ 是连续的.
  同理可证, 当变量 $x$ 固定时, 函数 $f(x, y)$ 对变量 $y$ 也是连续的.
  对 $k \neq 0$, 当点 $(x, y)$ 沿直线 $y=k x$ 趋于 0 时,
  $$
  \lim _{\substack{(x, y) \rightarrow(0,0) \\ y=k x}} f(x, y)=\lim _{x \rightarrow 0} \frac{k^4 x^2}{\left(1+k^4 x^2\right)^3}=0,
  $$
  当点 $(x, y)$ 沿曲线 $y=\sqrt{x}$ 趋于 $(0,0)$ 时, 有
  $$
  \lim _{(x, y) \rightarrow(0,0)} f(x, y)=\lim _{x \rightarrow 0} \frac{x^4 \cdot x^2}{\left(x^2+x^2\right)^3}=\frac{1}{8},
  $$
  由此知道 $\lim _{(x, y) \rightarrow(0,0)} f(x, y)$ 不存在, 即 $f(x, y)$ 在原点 $(0,0)$ 不连续.
  注 此例说明对二元函数 $f(x, y)$, 即使 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 处对变量 $x$ 和 $y$ 均连续, 但也保证不了 其在该点的连续性.

- 【例题：连续性的描述】设 $f(x)$ 是 $\mathbb{R}^n$ 上的函数. 求证 $f(x)$ 连续 $\Leftrightarrow$ 对于任意实数 $c$, 点集 $E_1=\left\{x \in \mathbb{R}^n ; f(x)<c\right\}$ 与 $E_2=\left\{x \in \mathbb{R}^n ; f(x)>c\right\}$ 都是开集.
  证 $\Rightarrow \forall x_0 \in E_1$, 由 $f(x)$ 连续及函数保序性, $\exists \delta>0$, s.t. 当 $x \in B\left(x_0, \delta\right)$ 时, $f(x)<c$, 从而 $B\left(x_0, \delta\right) \subset E_1$, 故 $E_1$ 为开集. 同理 $E_2$ 亦为开集.
  $\Leftarrow$ 对任意 $x_0 \in \mathbb{R}^n, \forall \varepsilon>0$, 令 $\alpha=f\left(x_0\right)-\varepsilon, \beta=f\left(x_0\right)+\varepsilon$. 由于 $\forall c \in \mathbb{R},\left\{x \in \mathbb{R}^n ; f(x)<\right.$
  $c\}$ 与 $\left\{x \in \mathbb{R}^n ; f(x)>c\right\}$ 均为开集, 故 $\left\{x \in \mathbb{R}^n ; \alpha<f(x)<\beta\right\}$ 亦开. 记 $E=\left\{x \in \mathbb{R}^n ; \alpha<f(x)<\beta\right\}$,
  显然 $x_0 \in E$, 由于 $E$ 是开集, $\exists \delta>0$, s.t. $B\left(x_0, \delta\right) \subset E$, 即 $\left|x-x_0\right|<\delta$ 时,
  $$
  f\left(x_0\right)-\varepsilon=\alpha<f(x)<\beta=f\left(x_0\right)+\varepsilon .
  $$
  即 $\left|f(x)-f\left(x_0\right)\right|<\varepsilon$.

- 【例题：】若 $y \neq 0$ 时, $f(x, y)=x \sin \frac{1}{y}$, 且 $f(x, 0)=0$, 证明: 该函数的不连续点集不是闭集.
  证 当 $y_0 \neq 0$ 时, 函数 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 显见是连续的, 即 $f(x, y)$ 在横轴以外的一切点均连 续, 又 $|f(x, y)-f(0,0)|=|f(x, y)| \leq|x|$, 于是 $f(x, y)$ 在原点连续. 设 $x_0 \neq 0$, 由 $\lim _{y \longrightarrow 0} f\left(x_0, y\right)=$ $\lim _{y \rightarrow 0} x_0 \sin \frac{1}{y}$ 不存在, 于是 $f(x, y)$ 在点 $\left(x_0, 0\right)$ 处不连续. 综上所述, $f(x, y)$ 的全部不连续点为 $x=$ 0轴上除去原点外的一切点, 而原点是不连续点集合的一个聚点, 但它本身却不是不连续点, 因此, $f(x, y)$ 的不连续点的集合不是闭集.

- 【例题：一致连续】研究函数 $f(x, y)=\sqrt{x^2+y^2}$ 在平面 $\mathbb{R}^2=\{|x|<+\infty,|y|<+\infty\}$ 上的一致连续性.
  解 $\left(x_1, y_1\right),\left(x_2, y_2\right)$ 不同时为 $(0,0)$ 时, 有
  $$
  \begin{aligned}
  &\left|f\left(x_1, y_1\right)-f\left(x_2, y_2\right)\right|=\left|\sqrt{x_1^2+y_1^2}-\sqrt{x_2^2+y_2^2}\right| \\
  =&\left|\frac{x_1^2+y_1^2-x_2^2-y_2^2}{\sqrt{x_1^2+y_1^2}+\sqrt{x_2^2+y_2^2}}\right| \\
  \leq & \frac{\left|x_1+x_2\right|\left|x_1-x_2\right|+\left|y_1+y_2\right|\left|y_1-y_2\right|}{\sqrt{x_1^2+y_1^2}+\sqrt{x_2^2+y_2^2}} \\
  \leq &\left|x_1-x_2\right|+\left|y_1-y_2\right|
  \end{aligned}
  $$
  又若 $\left(x_2, y_2\right)=(0,0)$, 显然
  $$
  \sqrt{x_1^2+y_1^2} \leq\left|x_1\right|+\left|y_1\right|=\left|x_1-x_2\right|+\left|y_1-y_2\right|
  $$
  于是我们有
  $$
  \left|\sqrt{x_1^2+y_1^2}-\sqrt{x_2^2+y_2^2}\right| \leq\left|x_1-x_2\right|+\left|y_1-y_2\right|
  $$
  因此, 对任意的 $\varepsilon>0$, 取 $\delta=\frac{\varepsilon}{2}$, 当 $\left|x_1-x_2\right| \leq \delta,\left|y_1-y_2\right| \leq \delta$ 时有
  $$
  \left|f\left(x_1, y_1\right)-f\left(x_2, y_2\right)\right|=\left|\sqrt{x_1^2+y_1^2}-\sqrt{x_2^2+y_2^2}\right|<\varepsilon
  $$
  成立. 故函数 $f(x, y)=\sqrt{x^2+y^2}$ 在平面 $\mathbb{R}^2$ 上有一致连续性.

- 【例题：一致连续性】证明若函数 $f(x, y)$ 在 $D=\{(x, y) \mid a \leq x \leq A, b \leq y \leq B\}$ 连续, 函数列 $\left\{\varphi_n(x)\right\}$ 在 $[a, A]$ 一 致收玫, 且 $b \leq \varphi_n(x) \leq B$, 则函数列 $F_n(x)=f\left[x, \varphi_n(x)\right], n=1,2, \cdots$ 在 $[a, A]$ 一致收玫.
  证 由已知 $f(x, y)$ 在有界闭矩形区域 $D$ 连续, 从而一致连续, 即
  $\forall \varepsilon>0, \exists \delta>0, \forall\left(x_1, y_1\right),\left(x_2, y_2\right) \in D:\left|x_1-x_2\right|<\delta,\left|y_1-y_2\right|<\delta$, 有
  $$
  \left|f\left(x_1, y_1\right)-f\left(x_2, y_2\right)\right|<\varepsilon \text {. }
  $$
  特别地 $x_1=x_2=x,\left|y_1-y_2\right|<\delta$, 有
  $$
  \left|f\left(x, y_1\right)-f\left(x, y_2\right)\right|<\varepsilon .
  $$
  已知 $\left|\varphi_n(x)\right|$ 在 $[a, A]$ 一致收玫, 则对上述 $\delta>0, \exists N \in \mathbb{N}_{+}, \forall n, m>N, \forall x \in[a, A]$, 有
  $$
  \left|\varphi_m(x)-\varphi_n(x)\right|<\delta,
  $$
  从而, 有
  $$
  \left|F_m(x)-F_n(x)\right|=\left|f\left[x, \varphi_m(x)\right]-f\left[x, \varphi_n(x)\right]\right|<\varepsilon,
  $$
  即 $F_n(x)$ 在 $[a, A]$ 一致收敛.

