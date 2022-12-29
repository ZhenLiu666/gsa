《高等数学A》第十四次习题课

> Author ZhenLiu
>
> 2022/12/06



#### 14.1 偏导数与全微分

- 定义： $f_x\left(x_0, y_0\right)$ 就是 $f\left(x, y_0\right)$ 作为 $x$ 的一元函数在 $x_0$ 处的微商, 而 $f_y\left(x_0, y_0\right)$ 是函数 $f\left(x_0, y\right)$ 作为 $y$ 的一元函数在 $y_0$ 处的微商.

- 几何含义：偏导数的几何意义：由于 $f_x\left(x_0, y_0\right)=\left.\frac{\mathrm{d} f\left(x, y_0\right)}{\mathrm{d} x}\right|_{x=x_0}$, 所以 $f_x\left(x_0, y_0\right)$ 的几何意义是平面曲线
  $$
  l_1:\left\{\begin{array}{l}
  z=f(x, y), \\
  y=y_0
  \end{array}\right.
  $$
  在 $x=x_0$ 处的切线关于 $x$ 轴的斜率。

- 高阶偏导数：对于混合偏导数有个记法问题. 根据通常的习惯, $f_{x y}\left(\right.$ 或 $\left.\frac{\partial^2 f}{\partial x \partial y}\right)$ 表示函 数先对 $x$ 求偏导数然后再对 $y$ 求偏导数。

- 混合偏导数相等的条件：若函数 $f(x, y)$ 的两个混合偏导数 $f_{y x}(x, y)$ 和 $f_{x y}(x, y)$ 在区 域 $D$ 内连续,则在该区域内这两个二阶偏导数必相等, 即$f_{x y}(x, y)=f_{y x}(x, y), \quad \forall(x, y) \in D .$

- 记号： 我们用 $C^n(D)$ 表示区域 $D$ 内全体函数 $f(x, y)$ 的集合, 其中 $f$ 在 $D$ 中有 $n$ 阶偏导数且每个 $n$ 阶偏导数都在 $D$ 中连续.

- 定义：设函数 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 的某个邻域内有定义. 若 $f(x, y)$ 的 全增量 $\Delta z=f\left(x_0+\Delta x, y_0+\Delta y\right)-f\left(x_0, y_0\right)$ 可写成
  $$
  \Delta z=A \Delta x+B \Delta y+o(\rho), \quad \rho \rightarrow 0,
  $$
  其中 $A, B$ 只与点 $\left(x_0, y_0\right)$ 有关而与自变量的改变量 $\Delta x, \Delta y$ 无关, $\rho=$ $\sqrt{(\Delta x)^2+(\Delta y)^2}$, 则称 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 处可微, 并称 $A \Delta x+B \Delta y$ 为 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 处的全微分, 记做 $\mathrm{d} z$, 即
  $$
  \mathrm{d} z=A \Delta x+B \Delta y .
  $$
  必要条件: $f(x, y)$ 在 $\left(x_0, y_0\right)$ 处可微 $\Rightarrow f(x, y)$ 在 $\left(x_0, y_0\right)$ 处连续且偏导数, 方向导数都存在. 

  充分条件: $f(x, y)$ 在 $\left(x_0, y_0\right)$ 处可微 $\Leftarrow f(x, y)$ 在 $\left(x_0, y_0\right)$ 的某个邻域内偏导数存在且连续.
  注: (1) 若 $f(x, y)$ 可微, 则其在 $\left(x_0, y_0\right)$ 处沿方向 $\vec{l}$ 的导数等于该点梯度在 $\vec{l}$ 方向的投影.
  (2) $f(x, y)$ 在 $\left(x_0, y_0\right)$ 处可微 $\nRightarrow f(x, y)$ 在 $\left(x_0, y_0\right)$ 处的偏导数连续.
  (3) 微分具有四则运算性质.

- 定理  (可微的充分条件) 若函数 $z=f(x, y)$ 的偏导数 $f_x(x, y)$ 与 $f_y(x, y)$ 在点 $\left(x_0, y_0\right)$ 的某个邻域内存在, 且这两偏导数在 $\left(x_0, y_0\right)$ 处连续, 则 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 处可微.

- 推论若 $D$ 是 $\mathbf{R}^2$ 中的一个区域, 而 $f \in C^1(D)$, 也即 $f$ 在区域 $D$ 中有 连续的一阶偏导数, 则 $f$ 在 $D$ 内可微.

- 【例题】求偏导数和偏导数在某个点的值；

- 【例题】对于二元函数而言, 在一点 $\left(x_0, y_0\right)$ 对于 $x$ 与 $y$ 的偏导数存在, 但不能推出它在该点连续. 例如, 函数
  $$
  u=\operatorname{sgn}(x y)
  $$
  (其中 $\operatorname{sgn}$ 为符号函数). 当 $x=0$ 或 $y=0$ 时 $\operatorname{sgn}(x y) \equiv 0$. 因而 $\operatorname{sgn}(x y)$ 在 $(0,0)$ 点两个偏导数都存在并等于 0 . 但是它在 $(0,0)$ 点并不连续.因此也不可微。

- 【例题】设 $f(x, y)=\left\{\begin{array}{ll}\frac{x^3-x y}{x^2+y^2}, & x^2+y^2 \neq 0, \\ 0 & x^2+y^2=0\end{array}\right.$, 求 $f_x(x, y)$ 和 $f_y(x, y)$.

  解: 对于 $x^2+y^2 \neq 0$, 有
  $$
  \begin{aligned}
  & \frac{\partial f}{\partial x}(x, y)=\frac{\left(3 x^2-y\right)\left(x^2+y^2\right)-2 x\left(x^3-x y\right)}{\left(x^2+y^2\right)^2}=\frac{x^4+x^2 y+3 x^2 y^2-y^3}{\left(x^2+y^2\right)^2} \\
  & \frac{\partial f}{\partial y}(x, y)=\frac{-x\left(x^2+y^2\right)-2 y\left(x^3-x y\right)}{\left(x^2+y^2\right)^2}=\frac{-x^3-2 x^3 y+x y^2}{\left(x^2+y^2\right)^2}
  \end{aligned}
  $$
  当 $x^2+y^2=0$ 时, 有
  $$
  \begin{aligned}
  & \frac{\partial f}{\partial x}(0,0)=\lim _{\Delta x \rightarrow 0} \frac{f(\Delta x, 0)-f(0,0)}{\Delta x}=\lim _{\Delta x \rightarrow 0} \frac{\Delta x}{\Delta x}=1 \\
  & \frac{\partial f}{\partial y}(0,0)=\lim _{\Delta y \rightarrow 0} \frac{f(0, \Delta y)-f(0,0)}{\Delta y}=\lim _{\Delta y \rightarrow 0} \frac{0}{\Delta y}=0
  \end{aligned}
  $$

- 【例题】若函数 $f(x, y)$ 的两个偏导数在点 $\left(x_0, y_0\right)$ 的某一邻域内存在且有界, 则 $f(x, y)$ 在 点 $\left(x_0, y_0\right)$ 处连续.
  证明: 根据假设, 存在常数 $M>0$, 使得在 $\left(x_0, y_0\right)$ 的某一邻域内
  $$
  \left|f_x(x, y)\right|<M, \quad\left|f_y(x, y)\right|<M,
  $$
  于是, 利用三角不等式和 Lagrange 中值定理有
  $$
  \begin{aligned}
  & \left|f(x, y)-f\left(x_0, y_0\right)\right| \\
  & \leq\left|f(x, y)-f\left(x, y_0\right)\right|+\left|f\left(x, y_0\right)-f\left(x_0, y_0\right)\right| \\
  & =\left|f_y\left(x, y_0+\theta_1 \Delta y\right)\left\|\Delta y|+| f_x\left(x_0+\theta_2 \Delta x, y_0\right)\right\| \Delta x\right| \\
  & <M(|\Delta x|+|\Delta y|),
  \end{aligned}
  $$
  其中 $\Delta x=x-x_0, \Delta y=y-y_0$. 由此可见
  $$
  \lim _{(x, y) \rightarrow\left(x_0, y_0\right)} f(x, y)=f\left(x_0, y_0\right),
  $$
  即 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 处连续.

- 【例题】证明: 函数
  $$
  f(x, y)= \begin{cases}\frac{x y}{\sqrt{x^2+y^2}}, & x^2+y^2 \neq 0, \\ 0, & x^2+y^2=0 .\end{cases}
  $$
  在 $\mathbf{R}^2$ 上连续, 且 ${f_x^{\prime}}^{\prime}, f_y^{\prime}$ 有界, 但 $f$ 在 $(0,0)$ 处不可微. (山东大学、 北京航空航天大学)
  提示 $f$ 在 $(0,0)$ 处不可微最后归结为证明:
  $$
  \frac{x y}{x^2+y^2} \nrightarrow 0 \quad(\text { 当 } \underset{y \rightarrow 0}{x \rightarrow 0} \text { 时 }) \text {. }
  $$

- 【例题】若 $f_x^{\prime}(x, y)$ 在点 $\left(x_0, y_0\right)$ 处存在, $f_y^{\prime}(x, y)$ 在 点 $\left(x_0, y_0\right)$ 处连续, 证明 $f(x, y)$ 在点 $\left(x_0, y_0\right)$ 处可微. (吉林工业 大学, 辽宁师范大学)
  $$
  \text { 证 } \begin{aligned}
  & f\left(x_0+\Delta x, y_0+\Delta y\right)-f\left(x_0, y_0\right) \\
  = & {\left[f\left(x_0+\Delta x, y_0+\Delta y\right)-f\left(x_0+\Delta x, y_0\right)\right]+\left[f\left(x_0+\Delta x, y_0\right)\right.} \\
  & \left.-f\left(x_0, y_0\right)\right] \\
  = & f_y^{\prime}\left(x_0+\Delta x, y_0+\theta \Delta y\right) \Delta y+f_x^{\prime}\left(x_0, y_0\right) \Delta x+\varepsilon_1 \Delta x \quad(0<\theta<1) \\
  = & {\left[f_y^{\prime}\left(x_0, y_0\right)+\varepsilon_2\right] \Delta y+f_x^{\prime}\left(x_0, y_0\right) \Delta x+\varepsilon_1 \Delta x } \\
  = & f_x^{\prime}\left(x_0, y_0\right) \Delta x+f_y^{\prime}\left(x_0, y_0\right) \Delta y+\varepsilon_1 \Delta x+\varepsilon_2 \Delta y,
  \end{aligned}
  $$
  其中 $\varepsilon_1 、 \varepsilon_2 \rightarrow 0$ (当 $\Delta x 、 \Delta y \rightarrow 0$ 时). 故 $f$ 在点 $\left(x_0, y_0\right)$ 处可微.

- 【思考】设 $f_x^{\prime}, f^{\prime}$, 在 $\left(x_0, y_0\right)$ 的某个邻域里存在, 且在 点 $\left(x_0, y_0\right)$ 处可微, 则
  $$
  f^{\prime \prime \prime}\left(x_0, y_0\right)=f_{y a}^{\prime \prime}\left(x_0, y_0\right) .
  $$

- 【例题】设 $z=f(x, y)=\left\{\begin{array}{ll}\left(x^2+y^2\right) \sin \frac{1}{x^2+y^2}, & x^2+y^2 \neq 0, \\ 0, & x^2+y^2=0,\end{array}\right.$ 证明:
  (1) $f(x, y)$ 于 $(0,0)$ 处可微;
  (2) $f(x, y)$ 在 $(0,0)$ 点的偏导数不连续.
  证明: (1) 要证明 $f(x, y)$ 于 $(0,0)$ 处可微, 只需证明

$$
f(\Delta x, \Delta y)-f(0,0)=f_x(0,0) \Delta x+f_y(0,0) \Delta y+o(\rho), \rho=\sqrt{\Delta x^2+\Delta y^2}
$$
因为
$$
\begin{aligned}
f_x(0,0) & =\lim _{\Delta x \rightarrow 0} \frac{f(\Delta x, 0)-f(0,0)}{\Delta x}=\lim _{\Delta x \rightarrow 0} \frac{(\Delta x)^2 \sin \frac{1}{(\Delta x)^2}}{\Delta x}=0, \\
f_y(0,0) & =\lim _{\Delta y \rightarrow 0} \frac{f(0, \Delta y)-f(0,0)}{\Delta y}=\lim _{\Delta x \rightarrow 0} \frac{(\Delta y)^2 \sin \frac{1}{(\Delta y)^2}}{\Delta y}=0, \\
& \lim _{\rho \rightarrow 0} \frac{f(\Delta x, \Delta y)-f(0,0)}{\rho}=\lim _{\rho \rightarrow 0} \frac{\rho^2 \sin \frac{1}{\rho^2}}{\rho}=0
\end{aligned}
$$
故 $(*)$ 式成立, 即 $f(x, y)$ 于 $(0,0)$ 处可微.
(2) 只须讨论 $\lim _{(x, y) \rightarrow(0,0)} f_x(x, y)$ 与 $f_x(0,0)$ 以及 $\lim _{(x, y) \rightarrow(0,0)} f_y(x, y)$ 与 $f_y(0,0)$ 是否相等.

当 $x^2+y^2 \neq 0$ 时
$$
\begin{aligned}
f_x(x, y) & =2 x \sin \frac{1}{x^2+y^2}+\left(x^2+y^2\right) \cos \frac{1}{x^2+y^2} \frac{-2 x}{\left(x^2+y^2\right)^2} \\
& =2 x \sin \frac{1}{x^2+y^2}-\frac{2 x}{x^2+y^2} \cos \frac{1}{x^2+y^2}, \\
f_y(x, y) & =2 y \sin \frac{1}{x^2+y^2}+\left(x^2+y^2\right) \cos \frac{1}{x^2+y^2} \frac{-2 y}{\left(x^2+y^2\right)^2} \\
& =2 y \sin \frac{1}{x^2+y^2}-\frac{2 y}{x^2+y^2} \cos \frac{1}{x^2+y^2},
\end{aligned}
$$
$\lim _{(x, y) \rightarrow(0,0)} f_x(x, y)$ 和 $\lim _{(x, y) \rightarrow(0,0)} f_y(x, y)$ 都不存在, 故 $f(x, y)$ 在 $(0,0)$ 点的偏导数不连续.
注: 结合定理 $2.1$ 和此例可知, 一阶偏导数连续是可微的充分条件, 而非必要条件.

- 【例题：求偏导数】设 $z=\mathrm{e}^u \sin v, u=x y, v=x+y$, 求 $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$.
  法一: 直接将 $z$ 看做 $(x, y)$ 的函数. 由于 $z=\mathrm{e}^u \sin v=\mathrm{e}^{x y} \sin (x+y)$, 得
  $$
  \begin{aligned}
  & \frac{\partial z}{\partial x}=y \mathrm{e}^{x y} \sin (x+y)+\mathrm{e}^{x y} \cos (x+y)=\mathrm{e}^{x y}[y \sin (x+y)+\cos (x+y)] \\
  & \frac{\partial z}{\partial y}=x \mathrm{e}^{x y} \sin (x+y)+\mathrm{e}^{x y} \cos (x+y)=\mathrm{e}^{x y}[x \sin (x+y)+\cos (x+y)]
  \end{aligned}
  $$
  法二: 运用链锁规则, 得
  $$
  \begin{aligned}
  \frac{\partial z}{\partial x} & =\frac{\partial z}{\partial u} \frac{\partial u}{\partial x}+\frac{\partial z}{\partial v} \frac{\partial v}{\partial x}=\mathrm{e}^u \sin v \cdot y+\mathrm{e}^u \cos v \cdot 1 \\
  & =y \mathrm{e}^{x y} \sin (x+y)+\mathrm{e}^{x y} \cos (x+y)=\mathrm{e}^{x y}[y \sin (x+y)+\cos (x+y)] \\
  \frac{\partial z}{\partial y} & =\frac{\partial z}{\partial u} \frac{\partial u}{\partial y}+\frac{\partial z}{\partial v} \frac{\partial v}{\partial y}=\mathrm{e}^u \sin v \cdot x+\mathrm{e}^u \cos v \cdot 1 \\
  & =x \mathrm{e}^{x y} \sin (x+y)+\mathrm{e}^{x y} \cos (x+y)=\mathrm{e}^{x y}[x \sin (x+y)+\cos (x+y)]
  \end{aligned}
  $$

- 【例题：求微分】

  (1) $u=x^4+y^4-4 x^2 y^2$;
  (2) $u=x^y$.
  法一: 先求偏导(要求连续), 然后给出微分形式
  (1) $\frac{\partial u}{\partial x}=4 x^3-8 x y^2, \quad \frac{\partial u}{\partial y}=4 y^3-8 x^2 y$, $\mathrm{d} u=\frac{\partial u}{\partial x} \mathrm{~d} x+\frac{\partial u}{\partial y} \mathrm{~d} y=\left(4 x^3-8 x y^2\right) \mathrm{d} x+\left(4 y^3-8 x^2 y\right) \mathrm{d} y$.
  (2) $\frac{\partial u}{\partial x}=y x^{y-1}, \quad \frac{\partial u}{\partial y}=x^y \ln x$ $\mathrm{d} u=\frac{\partial u}{\partial x} \mathrm{~d} x+\frac{\partial u}{\partial y} \mathrm{~d} y=y x^{y-1} \mathrm{~d} x+x^y \ln x \mathrm{~d} y$.
  法二: 直接利用微分四则运算和一阶微分形式不变性
  (1) $\mathrm{d} u=\mathrm{d}\left(x^4\right)+\mathrm{d}\left(y^4\right)-4 \mathrm{~d}\left(x^2 y^2\right)=4 x^3 \mathrm{~d} x+4 y^3 \mathrm{~d} y-8 x y^2 \mathrm{~d} x-8 x^2 y \mathrm{~d} y$
  $$
  \begin{aligned}
  &=\left(4 x^3-8 x y^2\right) \mathrm{d} x+\left(4 y^3-8 x^2 y\right) \mathrm{d} y \\
  & \text { (2) } \mathrm{d} u \stackrel{v=y \ln x}{=} \mathrm{d}\left(\mathrm{e}^v\right)=\mathrm{e}^v \mathrm{~d} v=\mathrm{e}^{y \ln x}(\ln x \mathrm{~d} y+y \mathrm{~d} \ln x) \\
  &=x^y\left(\ln x \mathrm{~d} y+\frac{y}{x} \mathrm{~d} x\right)=y x^{y-1} \mathrm{~d} x+x^y \ln x \mathrm{~d} y .
  \end{aligned}
  $$







#### 14.2 复合函数与隐函数的微分法

- 定理 1 设函数 $u=\varphi(x, y)$ 与 $v=\psi(x, y)$ 在点 $(x, y)$ 处对 $x, y$ 的偏导 数存在, 又设函数 $z=f(u, v)$ 在相应的点 $(u, v)$ 处对 $u, v$ 的偏导数存在且库 续, 则复合函数 $z=f(\varphi(x, y), \psi(x, y))$ 在点 $(x, y)$ 处对 $x, y$ 的偏导数也存 在,且有公式
  $$
  \begin{aligned}
  & \frac{\partial z}{\partial x}=\frac{\partial f}{\partial u} \cdot \frac{\partial u}{\partial x}+\frac{\partial f}{\partial v} \cdot \frac{\partial v}{\partial x}, \\
  & \frac{\partial z}{\partial y}=\frac{\partial f}{\partial u} \cdot \frac{\partial u}{\partial y}+\frac{\partial f}{\partial v} \cdot \frac{\partial v}{\partial y} .
  \end{aligned}
  $$
  使用这种链规则规要求 $f$ 的可微性以及中间变量 (作为自变量的函数)的偏导数的存在性.

- 微分形式不变性：设函数 $z=f(u, v), u=u(x, y), v=v(x, y)$ 都有连续的偏导 数, 则复合函数
  $$
  z=f(u(x, y), v(x, y))
  $$
  在点 $(x, y)$ 处的全微分仍可表为$\mathrm{d} z=f_u \mathrm{~d} u+f_v \mathrm{~d} v .$当 $u, v$ 是自变量时, 函数 $z=f(u, v)$ 的全微分为$\mathrm{d} z=f_u \mathrm{~d} u+f_v \mathrm{~d} v .$所以定理表明, 不论 $u, v$ 是中间变量还是自变量, 一阶全微分可表成相同的形式. 这就是所谓一阶全微分的形式不变性.

- 高阶微分：一般地, 当 $f \in C^n(D)$ 时, 则 $f$ 在区域 $D$ 内的 $n$ 次微分
  $$
  \mathrm{d}^n f=\left(\mathrm{d} x \frac{\partial}{\partial x}+\mathrm{d} y \frac{\partial}{\partial y}\right)^n f .
  $$

- 【例题】若 $z=f(x, y)$ 满足
  $$
  f(t x, t y)=t^k f(x, y) \quad(t>0), (1)
  $$
  则称 $f(x, y)$ 为 $k$ 次齐次函数, 试证下述关于齐次函数的 Euler 定 理: 设 $f(x, y)$ 可微, 则 $f(x, y)$ 为 $k$ 次齐次函数的充要条件是
  $$
  x f_x^{\prime}(x, y)+y f_y^{\prime}(x, y)=k f(x, y) \text {. } (2)
  $$
  证 必要性. (1) 式对 $t$ 求导, 再令 $t=1$ 即得 (2). 充分性. 方法一, 要证 $t>0$ 时 (1) 成立, 即要证
  $$
  \varphi(t) \equiv \frac{f(t x, t y)}{t^k}=f(x, y) .
  $$
  因 $\varphi(1)=f(x, y)$, 因此只要证明 $\varphi^{\prime}(t) \equiv 0$ 即可. 利用复合函数 微分法及式(2)这是明显的.
  方法二（按必要性的证法倒退回去）在式 (2) 中分别用 $t x, t y$ 代替自变量 $x, y$,得
  记$t x f^{\prime}{ }_x(t x, t y)+t y f^{\prime}{ }_y(t x, t y)=k f(t x, t y) .$记$\varphi(t)=f(t x, t y)$.则 (3) 为$t \varphi^{\prime}(t)=k \varphi,$

  且 $\varphi(1)=f(x, y)$.由此解微分方程即得式 (1).

- 【例题】设 $f(x, y)$ 为 $n$ 次齐次函数, 且 $m$ 次可微, 证明
  $$
  \left(x \frac{\partial}{\partial x}+y \frac{\partial}{\partial y}\right)^m f=n(n-1) \cdots(n-m+1) f \text {. }
  $$
  方法一 直接在 $f(t x, t y)=t^n f(x, y)$ 两端同时对 $t$ 求 $m$ 阶 导数,然后令 $t=1$.
  方法二 利用数学归纳法.

- 【例题】设 $z=f(x, y)$ 有连续的一阶偏导数, 且 $x=r \cos \theta, y=r \sin \theta$. 求 $\frac{\partial z}{\partial r}$ 及 $\frac{\partial z}{\partial \theta}$, 并证明关系式
  $$
  \left(\frac{\partial z}{\partial r}\right)^2+\frac{1}{r^2}\left(\frac{\partial z}{\partial \theta}\right)^2=\left(\frac{\partial z}{\partial x}\right)^2+\left(\frac{\partial z}{\partial y}\right)^2 .
  $$
  解 由链规则, 我们得到
  $$
  \begin{aligned}
  & \frac{\partial z}{\partial r}=\frac{\partial z}{\partial x} \cdot \frac{\partial x}{\partial r}+\frac{\partial z}{\partial y} \cdot \frac{\partial y}{\partial r}=\cos \theta \cdot \frac{\partial z}{\partial x}+\sin \theta \cdot \frac{\partial z}{\partial y}, \\
  & \frac{\partial z}{\partial \theta}=\frac{\partial z}{\partial x} \cdot \frac{\partial x}{\partial \theta}+\frac{\partial z}{\partial y} \cdot \frac{\partial y}{\partial \theta}=-r \sin \theta \frac{\partial z}{\partial x}+r \cos \theta \frac{\partial z}{\partial y} .
  \end{aligned}
  $$
  所以
  $$
  \begin{aligned}
  \left(\frac{\partial z}{\partial r}\right)^2+\left(\frac{1}{r} \cdot \frac{\partial z}{\partial \theta}\right)^2= & \left(\cos \theta \frac{\partial z}{\partial x}+\sin \theta \frac{\partial z}{\partial y}\right)^2 \\
  & +\left(-\sin \theta \frac{\partial z}{\partial x}+\cos \theta \frac{\partial z}{\partial y}\right)^2 \\
  = & \left(\frac{\partial z}{\partial x}\right)^2+\left(\frac{\partial z}{\partial y}\right)^2 .
  \end{aligned}
  $$

- 【例题】设 $u=\sin \left(x^2+y^2\right)+\mathrm{e}^{x t}$, 求在 $(1,0,1)$ 处的全微分 $\mathrm{d} u$. 解 由一阶微分形式的不变性, 我们有
  $$
  \begin{aligned}
  \mathrm{d} u & =\cos \left(x^2+y^2\right) \mathrm{d}\left(x^2+y^2\right)+\mathrm{e}^{x z} \mathrm{~d}(x z) \\
  & =\cos \left(x^2+y^2\right)(2 x \mathrm{~d} x+2 y \mathrm{~d} y)+\mathrm{e}^{x z}(z \mathrm{~d} x+x \mathrm{~d} z) .
  \end{aligned}
  $$
  将 $x=1, y=0, z=1$ 代人上式, 我们得到：
  $$
  \begin{aligned}
  \mathrm{d} u & =\cos 1 \cdot 2 \mathrm{~d} x+\mathrm{e}(\mathrm{d} x+\mathrm{d} z) \\
  & =(2 \cos 1+\mathrm{e}) \mathrm{d} x+\mathrm{ed} z .
  \end{aligned}
  $$

- 【例题】设 $z=f(x, y)$ 是二次连续可微函数, 又有关系式 $u=x+$ $a y, v=x-a y(a$ 是不为零的常数 $)$
  证明: $a^2 \frac{\partial^2 z}{\partial x^2}-\frac{\partial^2 z}{\partial y^2}=4 a^2 \frac{\partial^2 z}{\partial u \partial v}$. (北京大学)
  提示 可用逆变换 $x=\frac{1}{2}(u+v) y=\frac{1}{2 a}(u-v)$将欲证的等式右端变换成左端.
  也可用 $u=x+a y, v=x-a y$ 将左端变换成右端.





#### 14.3 方向导数与梯度

- 定义：设 $z=f(x, y)$ 在一点 $P_0\left(x_0, y_0\right)$ 的一个邻域内有定义, 又设 $\boldsymbol{l}$ 是 给定的一个方向, 其方向余弦为 $(\cos \alpha, \cos \beta)$. 若极限
  $$
  \lim _{t \rightarrow 0} \frac{f\left(x_0+t \cos \alpha, y_0+t \cos \beta\right)-f\left(x_0, y_0\right)}{t}
  $$
  存在, 则我们称此极限值为函数 $z=f(x, y)$ 在 $P_0$ 点沿方向 $l$ 的方向导数, 记做 $\left.\frac{\partial z}{\partial l}\right|_{\left(x_0, y_0\right)}$ 或 $\left.\frac{\partial f}{\partial l}\right|_{\left(x_0, y_0\right)}$.

- 定理：若函数 $f(x, y)$ 在点 $P_0\left(x_0, y_0\right)$ 处可微, 则 $f(x, y)$ 在该点沿任一 方向 $\boldsymbol{l}$ 的方向导数均存在,且
  $$
  \left.\frac{\partial f}{\partial l}\right|_{P_0}=f_x\left(x_0, y_0\right) \cos \alpha+f_y\left(x_0, y_0\right) \cos \beta
  $$
  其中 $\cos \alpha, \cos \beta$ 为 $l$ 的方向余弦.

- 梯度方向：$\left.\operatorname{grad} f\right|_{\left(x_0, y_0\right)}=\left(f_x\left(x_0, y_0\right), f_y\left(x_0, y_0\right)\right)$，优化方法：梯度下降法。由此可见, 函数值沿 $-\left.\operatorname{grad} f\right|_{P_0}$ 的方向时方向导数达到最小, 并且其方向导数的值是 $-|\boldsymbol{g}|$. 换 句话说, 负梯度的方向是函数值减少最快的方向.

- $$
  \frac{\partial f}{\partial x}\left(x_0, y_0\right) \text { 存在 } \Leftrightarrow \frac{\partial f}{\partial \vec{e}_1^{+}}\left(x_0, y_0\right)=-\frac{\partial f}{\partial{\overrightarrow{e_1}}^{-}}\left(x_0, y_0\right)
  $$
  注: (1) $f_x\left(x_0, y_0\right), f_y\left(x_0, y_0\right)$ 都存在且相等 $\nRightarrow f(x, y)$ 于 $\left(x_0, y_0\right)$ 连续.
  (2) 所有方向导数都存在且相等 $\nRightarrow f(x, y)$ 于 $\left(x_0, y_0\right)$ 连续.
  (3) 所有方向导数都存在 $\Rightarrow$ 偏导数存在; 偏导数存在 $\Rightarrow$ 所有方向导数存在.

- 要点 计算方向导数的基本方法如下：
  1) 利用定义. 函数 $y=f(x)\left(x \in \mathbf{R}^n\right)$ 在点 $P=\left(x_1, x_2, \cdots\right.$, $\left.x_n\right)$ 处沿单位向量 $l=\left(l_1, l_2, \cdots, l_n\right)$ 方向的方向导数定义为
  $$
  \left.\frac{\partial f}{\partial l}\right|_P=\lim _{t \rightarrow 0} \frac{f(P+t l)-f(P)}{t}=\left.\frac{\mathrm{d} f(P+t l)}{\mathrm{d} t}\right|_{t=0} .
  $$
  2) 利用偏导数与方向导数的关系. 若 $f$ 在 $P$ 处可微, 则 $f$ 在 $P$ 点沿任意方向 $l=\left(\cos \alpha_1, \cos \alpha_2, \cdots, \cos \alpha_n\right)$ 的方向导数存在, 并 且
  $$
  \left.\frac{\partial f}{\partial l}\right|_P=f_{x_1}^{\prime}(P) \cos \alpha_1+f_{x_2}^{\prime}(P) \cos \alpha_2+\cdots+f_{x_n}^{\prime}(P) \cos \alpha_n .
  $$
  3) 利用梯度与方向导数的关系. 若 $f$ 在 $P$ 处可微, 则 $f$ 在 $P$ 点沿任意方向 $l=\left(\cos \alpha_1, \cos \alpha_2, \cdots, \cos \alpha_n\right)$ 方向的方向导数
  $$
  \begin{aligned}
  \left.\frac{\partial f}{\partial l}\right|_P & =\operatorname{grad} f(P) \cdot\left(\cos \alpha_1, \cos \alpha_2, \cdots, \cos \alpha_n\right) \\
  & =\operatorname{grad}_l f(P)=|\operatorname{grad} f(P)| \cos \theta,
  \end{aligned}
  $$
  其中 $\theta$ 表示 $\operatorname{grad} f(P)$ 与 $l$ 的夹角.

- 【例题】求在原点处的方向导数：
  $$
  f(x, y)=\left\{\begin{array}{l}
  \frac{x y}{\sqrt{x^2+y^2}}, x^2+y^2 \neq 0, \\
  0, \quad x^2+y^2=0 .
  \end{array}\right.
  $$

证 任取方向 $l=(\cos \alpha, \sin \alpha)$, 则
$$
\begin{aligned}
f(t \cos \alpha, t \sin \alpha) & = \begin{cases}t \cos \alpha \sin \alpha, & t \neq 0, \\
0, & t=0\end{cases} \\
& =t \cos \alpha \sin \alpha .
\end{aligned}
$$
于是 $\left.\quad \frac{\partial f}{\partial l}\right|_{(0,0)}=\left.\frac{\mathrm{d}}{\mathrm{d} t} f(t \cos \alpha, t \sin \alpha)\right|_{t=0}$ $=(t \cos \alpha \sin \alpha)^{\prime},\left.\right|_{t=0}=\cos \alpha \sin \alpha$.
可见在 $(0,0)$ 处沿任意方向导数存在.

- 【例题】设 $y=\varphi(x)$ 是区间 $a \leqslant x \leqslant b$ 上的可微函数,在 $O x y$ 直角坐标平面内其图像为曲线 $\Gamma$, 若二元函数 $f(x, y)$ 在包 含曲线 $\Gamma$ 的某区域上连续可微 (即具有连续的偏导数), 且在曲线 $\Gamma$ 上恒为 0 , 求证: $f(x, y)$ 在曲线 $\Gamma$ 上任一给定点处沿该曲线切 线方向的导数等于 0 . 
  分析 设 $l=(\cos \alpha, \cos \beta)$ 是曲线 $\Gamma$ 上点 $P$ 处的单位切向 量.利用公式 (B),
  $$
  \frac{\partial f}{\partial l}=f_x^{\prime} \cos \alpha+f^{\prime}{ }_y \cos \beta,
  $$
  可见, 要计算 $\frac{\partial f}{\partial l}$, 关键在于求出 $\cos \alpha, \cos \beta$. 按已知条件
  因此 $\quad f_x^{\prime}(P)+{f_y^{\prime}}^{\prime}(P) \varphi^{\prime}(x)=0 \quad(P \in \Gamma)$.故 $\tan \alpha=\varphi^{\prime}(x)=-\frac{f_x^{\prime}(P)}{f_y^{\prime}(P)}$.
  从而
  $$
  \begin{gathered}
  \cos \alpha=\frac{1}{\pm \sqrt{1+\tan ^2 \alpha}}=\frac{\left|f_y^{\prime}\right|}{\pm \sqrt{f_x^{\prime 2}+f_y^{\prime 2}}}, \\
  \cos \beta=\sin \alpha=\tan \alpha \cos \alpha=\frac{-\frac{f_x^{\prime}}{f_y^{\prime}}\left|f_y^{\prime}\right|}{\pm \sqrt{f_x^{\prime 2}+f_y^{\prime 2}}} .
  \end{gathered}
  $$
  代人(1) 得
  $$
  \left.\cdot \frac{\partial f}{\partial l}\right|_P=f_x^{\prime} \cos \alpha+f_y^{\prime} \cos \beta=\frac{f_x^{\prime}\left|f_y^{\prime}\right|-f_x^{\prime}\left|f_y^{\prime}\right|}{\pm \sqrt{f_x^{\prime 2}+f_y^{\prime 2}}}=0 .
  $$

- 【例题】设 $l_1, l_2, \cdots, l_n$ 为 $\mathbf{R}^n$ 中 $n$ 个线性无关的单位向量, 函数 $f(x)$ 在 $\mathbf{R}^n$ 中可微, 方向导数 $\frac{\partial f}{\partial l_i} \equiv 0(i=1,2, \cdots, n)$, 试证 $f(x) \equiv$ 常数
  证 记 $l_i=\left(a_{i 1}, a_{i 2}, \cdots, a_{i n}\right)(i=1,2, \cdots, n)$ 因 $\frac{\partial f}{\partial l_i} \equiv 0$, 应用 公式(B)，得
  $$
  \begin{gathered}
  0=\frac{\partial f}{\partial l_i}=f_{x_1}^{\prime} \cdot a_{i 1}+f_{x_2}^{\prime} \cdot a_{i 2}+\cdots+f_{x_n}^{\prime} \cdot a_{i n} \\
  (i=1,2, \cdots, n) .
  \end{gathered}
  $$
  因为 $l_i$ 线性无关, 故
  $$
  \operatorname{det}\left(a_{i j}\right)_{i, j=1}^n \neq 0,
  $$
  从而(1)式只有零解.
  $$
  f_{x_1}^{\prime} \equiv 0 \quad(i=1,2, \cdots, n) .
  $$
  记 $P=\left(x_1, x_2, \cdots, x_n\right), P_0=\left(x_{0.1}, x_{0.2}, \cdots, x_{0, n}\right)$,
  根据微分中值公式,
  $$
  \begin{aligned}
  & f(P)=f\left(P_0\right)+\sum_{i=1}^n f_{x_i}^{\prime}\left(P^*\right)\left(x_i-x_{0 . i}\right)=f\left(P_0\right) \quad\left(P \in \mathbf{R}^n\right) . \\
  & \text { 此即表明 } \quad f(P) \equiv \text { 常数. }
  \end{aligned}
  $$





#### 14.4 补充内容

- 一个写成微分形式的微分方程
  $$
  M(x, y) \mathrm{d} x+N(x, y) \mathrm{d} y=0,
  $$
  如果存在可微函数 $U(x, y)$, 使得
  $$
  \mathrm{d} U(x, y)=M(x, y) \mathrm{d} x+N(x, y) \mathrm{d} y,
  $$
  $$
  U_x(x, y)=M(x, y), \quad U_y(x, y)=N(x, y),
  $$
  则称为恰当方程, 或全微分方程. 在这种情形下, 方程可以写成 $\mathrm{d} U(x$, $y)  \equiv 0$. 于是
  $$
  U(x, y) \equiv C
  $$
  就是方程的隐式通解, 此处 $C$ 是任意常数.

- 定理：设函数 $M(x, y)$ 和 $N(x, y)$ 均于矩形域 $G: a<x<b, \alpha<y$ $<\beta$ 连续可微. 则方程 (2.19) 是恰当方程的充要条件是$M_y(x, y)=N_x(x, y), \quad(x, y) \in G .$而且相应的原函数可取为
  $$
  U(x, y)=\int_{x_0}^x M(s, y) \mathrm{d} s+\int_{y_0}^y N\left(x_0, t\right) \mathrm{d} t,
  $$
  也可取为
  $$
  U(x, y)=\int_{x_0}^x M\left(s, y_0\right) \mathrm{d} s+\int_{y_0}^y N(x, t) \mathrm{d} t,
  $$
  其中 $\left(x_0, y_0\right) \in G$ 是任意取定的一点.

- 【例题】解方程
  $$
  x y \mathrm{~d} x+\left(\frac{x^2}{2}+\frac{1}{y}\right) \mathrm{d} y=0 .
  $$
  解 这里 $M=x y, N=\frac{x^2}{2}+\frac{1}{y}$. 故 $M_y=x=N_x$. 因为 $N$ 于 $y=0$ 处无意义, 所以应分别在区域 $y>0$ 和 $y<0$ 上应用定理。可以按下述任意一条途径去求相应的原函数 $U(x, y)$.
  1. 先选取 $\left(x_0, y_0\right)=(0,1)$, 代人公式有
  $$
  U=\int_0^x s y \mathrm{~d} s+\int_1^y \frac{1}{t} \mathrm{~d} t=\frac{x^2}{2} y+\ln y, \quad y>0 .
  $$
  再选取 $\left(x_0, y_0\right)=(0,-1)$, 代人公式 $(2.22)$ 有
  $$
  U=\int_0^x s y \mathrm{~d} s+\int_{-1}^y \frac{1}{t} \mathrm{~d} t=\frac{x^2}{2} y+\ln (-y), \quad y<0 .
  $$
  合在一起,不论 $y>0$ 和 $y<0$ 都有
  $$
  U=\frac{x^2}{2} y+\ln |y|
  $$
  也可分别取 $\left(x_0, y_0\right)=(0,1)$ 和 $\left(x_0, y_0\right)=(0,-1)$ 代人公式 $(2.23)$ 而得到同 样的结果:
  $$
  \begin{aligned}
  & U=\int_0^x s \mathrm{~d} s+\int_1^y\left(\frac{x^2}{2}+\frac{1}{t}\right) \mathrm{d} t=\frac{x^2}{2} y+\ln y, \quad y>0, \\
  & U=\int_0^x(-s) \mathrm{d} s+\int_{-1}^y\left(\frac{x^2}{2}+\frac{1}{t}\right) \mathrm{d} t=\frac{x^2}{2} y+\ln (-y), \quad y<0 .
  \end{aligned}
  $$
  2. 从 $U_x=M$ 出发, 有

  $$
  U(x, y) \equiv \int M(x, y) \mathrm{d} x+\varphi(y)=\frac{x^2}{2} y+\varphi(y),
  $$

其中 $\varphi(y)$ 待定. 再利用 $(2.20)$ 第二式 $U_y=N$, 有
$$
\frac{x^2}{2}+\varphi^{\prime}(y)=\frac{x^2}{2}+\frac{1}{y},
$$
即$\varphi^{\prime}(y)=\frac{1}{y},$从而$\varphi(y)=\ln |y|,$这里省略了积分常数, 因为只需求出一个 $U(x, y)$ 即可. 把它代人便得
$$
U=\frac{x^2}{2} y+\ln |y| .
$$
也可以从 $U_y=N$ 出发:
$$
U(x, y) \equiv \int N(x, y) \mathrm{d} y+\psi(x)=\frac{x^2}{2} y+\ln |y|+\psi(x),
$$
其中 $\psi(x)$ 待定.再利用 $U_x=M$, 有 即
$$
x y+\psi^{\prime}(x)=x y,
$$
$$
\psi^{\prime}(x)=0,
$$
特别可取 $\psi(x)=0$, 于是也得到上面的表达式 $U(x, y)$.
3 . 重新组合以求出原函数 $U(x, y)$. 为此, 左端改写成
$$
x y \mathrm{~d} x+\left(\frac{x^2}{2}+\frac{1}{y}\right) \mathrm{d} y=\left(x y \mathrm{~d} x+\frac{x^2}{2} \mathrm{~d} y\right)+\frac{1}{y} \mathrm{~d} y=\mathrm{d}\left(\frac{x^2}{2} y+\ln |y|\right) .
$$
从而看出
$$
U \equiv \frac{x^2}{2} y+\ln |y| \text {. }
$$
总之, 不论通过哪一个途径都可求出的隐式通解:
$$
U \equiv \frac{x^2}{2} y+\ln |y|+C .
$$






