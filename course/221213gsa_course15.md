《高等数学A》第十五次习题课

> Author ZhenLiu
>
> 2022/12/13



#### 15.1 方向导数与梯度

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



#### 15.2 多元函数的微分中值定理与Taylor公式

- 定理 ：设 $z=f(x, y)$ 在区域 $D$ 内有连续的偏导数. 又假定 $D$ 中有两 个点 $P_0\left(x_0, y_0\right)$ 与 $P_1\left(x_0+\Delta x, y_0+\Delta y\right)$, 并且 $P_0$ 到 $P_1$ 的直线段 $\overline{P_0 P_1} \subset D$. 则存在 $\theta, 0<\theta<1$, 使得
  $$
  \begin{aligned}
  f\left(x_0\right. & \left.+\Delta x, y_0+\Delta y\right)=f\left(x_0, y_0\right)+\frac{\partial f}{\partial x}\left(x_0+\theta \Delta x, y_0+\theta \Delta y\right) \Delta x \\
  & +\frac{\partial f}{\partial y}\left(x_0+\theta \Delta x, y_0+\theta \Delta y\right) \Delta y .
  \end{aligned}
  $$
  这就是二元函数的拉格朗日中值公式.

- 定理： 设 $D \subset \mathbf{R}^2$ 为一区域, 而函数 $f(x, y) \in C^{n+1}(D)$. 又设 $P_0\left(x_0, y_0\right) \in D, P_1\left(x_0+\Delta x, y_0+\Delta x\right) \in D$, 且 $P_0$ 至 $P_1$ 的连线 $\overline{P_0 P_1} \subset D$, 则 有
  $$
  \begin{aligned}
  f\left(x_0\right. & \left.+\Delta x, y_0+\Delta y\right) \\
  = & f\left(x_0, y_0\right)+\frac{1}{1 !} \mathrm{d} f\left(x_0, y_0\right)+\frac{1}{2 !} \mathrm{d}^2 f\left(x_0, y_0\right)+\cdots \\
  & +\frac{1}{n !} \mathrm{d}^n f\left(x_0, y_0\right)+\frac{1}{(n+1) !} \mathrm{d}^{n+1} f\left(x_0+\theta \Delta x, y_0+\theta \Delta y\right),
  \end{aligned}
  $$
  其中, $\mathrm{d}^k f$ 是 $f$ 的 $k$ 阶微分, 即
  $$
  \mathrm{d}^k f(x, y)=\left(\Delta x \frac{\partial}{\partial x}+\Delta y \frac{\partial}{\partial y}\right)^k f(x, y), \quad(k=1,2, \cdots, n+1) .
  $$

- 设 $z=z(x, y)$ 为由方程 $z^3-2 x z+y=0$ 确定的隐函数, 满足 $z(1,1)=1$. 将函数 $z(x, y)$ 在 $(1,1)$ 点附近展到 $(x-1),(y-1)$ 的二次项.
  解: 利用 Taylor 展开可得
  $$
  \begin{aligned}
  z(x, y)= & z(1,1)+\left((x-1) \frac{\partial}{\partial x}+(y-1) \frac{\partial}{\partial y}\right) z(1,1) \\
  & +\frac{1}{2}\left((x-1) \frac{\partial}{\partial x}+(y-1) \frac{\partial}{\partial y}\right)^2 z(1,1)+R_2 .
  \end{aligned}
  $$
  由题意知 $z(1,1)=1$, 下面只需求出一阶和二阶导数项. 根据一阶微分形式不变性, 在方程 两边同时求微分得
  $$
  3 z^2 \mathrm{~d} z-2 z \mathrm{~d} x-2 x \mathrm{~d} z+\mathrm{d} y=0 \text {, 即 } \mathrm{d} z=\frac{2 z}{3 z^2-2 x} \mathrm{~d} x-\frac{1}{3 z^2-2 x} \mathrm{~d} y ，
  $$
  因而有
  $$
  \begin{aligned}
  \frac{\partial z}{\partial x} & =\frac{2 z}{3 z^2-2 x}, \quad \frac{\partial z}{\partial y}=-\frac{1}{3 z^2-2 x}, & \frac{\partial^2 z}{\partial y^2}=\frac{6 z \frac{\partial z}{\partial y}}{\left(3 z^2-2 x\right)^2} \\
  \frac{\partial^2 z}{\partial x^2} & =\frac{2\left(3 z^2-2 x\right) \frac{\partial z}{\partial x}-2\left(6 z \frac{\partial z}{\partial x}-2\right) z}{\left(3 z^2-2 x\right)^2}, & \frac{\partial^2 z}{\partial y \partial x}=\frac{6 z \frac{\partial z}{\partial x}-2}{\left(3 z^2-2 x\right)^2}
  \end{aligned}
  $$
  于是
  $$
  \left.\frac{\partial z}{\partial x}\right|_{(1,1)}=2,\left.\quad \frac{\partial z}{\partial y}\right|_{(1,1)}=-1,\left.\quad \frac{\partial^2 z}{\partial x^2}\right|_{(1,1)}=-16,\left.\quad \frac{\partial^2 z}{\partial x \partial y}\right|_{(1,1)}=10,\left.\quad \frac{\partial^2 z}{\partial y^2}\right|_{(1,1)}=-6
  $$

进而有
$$
z(x, y)=1+2(x-1)-(y-1)-8(x-1)^2+10(x-1)(y-1)-3(y-1)^2+R_2
$$




#### 15.3 隐函数存在定理

- 设 $x, x^0 \in \mathbb{R}^n, u, u_0 \in \mathbb{R}$, 如果 $F(x, u)$ 满足条件:
  (1) $F\left(x^0, u_0\right)=0, \quad F_u\left(x^0, u_0\right) \neq 0$
  (2) $F(x, u), F_u(x, u)$ 在 $\left(x^0, u_0\right)$ 及其附近连续.
  则存在 $\delta, \eta>0$ 和唯一定义于 $\left\{x|| x-x^0 \mid<\delta\right\}$ 取值于 $\left\{u|| u-u_0 \mid<\eta\right\}$ 的函数 $u(x)$, 使得
  $$
  F(x, u(x)) \equiv 0, \quad \forall x \in\left\{x|| x-x^0 \mid<\delta\right\}, \quad u_0=u\left(x^0\right)
  $$

且 $u(x)$ 在 $\left\{x|| x-x^0 \mid<\delta\right\}$ 内连续. 进一步, 若再有
(3) $\frac{\partial F}{\partial x_i}(i=1,2, \cdots, n)$ 还在 $\left(x^0, u_0\right)$ 附近连续,
则在 $x^0$ 附近, $\frac{\partial u}{\partial x_i}$ 存在, 连续, 且有
$$
\frac{\partial u}{\partial x_i}=-\frac{\partial F}{\partial x_i} / \frac{\partial F}{\partial u}, i=1,2, \cdots, n .
$$

- 设 $F(x, y, u, v)$ 和 $G(x, y, u, v)$ 为定义在区域 $V \subset R^4$ 上的函数, 存在点 $p_0\left(x_0, y_0, u_0, v_0\right) \in V$, 如果满足以下条件:
  (i) $F\left(x_0, y_0, u_0, v_0\right)=G\left(x_0, y_0, u_0, v_0\right)=0$,
  (ii) $F(x, y, u, v)$ 和 $G(x, y, u, v)$ 在 $p_0$ 邻域连续可微,
  (iii) $\left.J\right|_{p_0}=\left|\begin{array}{ll}\frac{\partial F}{\partial u} & \frac{\partial F}{\partial v} \\ \frac{\partial G}{\partial u} & \frac{\partial G}{\partial v}\end{array}\right|_{p_0} \neq 0$
  则在 $p_0$ 的邻域 $U\left(p_0\right) \subset V$ 中, 方程组
  $$
  \left\{\begin{array}{c}
  F(x, y, u, v)=0 \\
  G(x, y, u, v)=0
  \end{array}\right.
  $$
  唯一地确定了一组连续可微的隐函数
  $$
  u=f(x, y), v=g(x, y)
  $$
  且其偏导数 $\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial v}{\partial x}, \frac{\partial v}{\partial x}$ 由方程组
  $$
  \left\{\begin{array}{l}
  \frac{\partial F}{\partial x} \mathrm{~d} x+\frac{\partial F}{\partial y} \mathrm{~d} y+\frac{\partial F}{\partial u} \mathrm{~d} u+\frac{\partial F}{\partial v} \mathrm{~d} v=0 \\
  \frac{\partial G}{\partial x} \mathrm{~d} x+\frac{\partial G}{\partial y} \mathrm{~d} y+\frac{\partial G}{\partial u} \mathrm{~d} u+\frac{\partial G}{\partial v} \mathrm{~d} v=0
  \end{array}\right.
  $$
  所确定.

- 【例题】对于由方程 $x+y+z=\mathrm{e}^{-x-y-z}$ 所确定的关于 $x, y$ 的隐函数 $z$, 求出 $\frac{\partial z}{\partial x}, \frac{\partial z}{\partial y}$. 

  - 法一: 利用一阶微分形式不变性有：$\mathrm{d} x+\mathrm{d} y+\mathrm{d} z=\mathrm{de}^{-x-y-z}=\mathrm{e}^{-x-y-z}(-\mathrm{d} x-\mathrm{d} y-\mathrm{d} z)$
    $$
    \left(1+\mathrm{e}^{-x-y-z}\right) \mathrm{d} z=-\left(1+\mathrm{e}^{-x-y-z}\right) \mathrm{d} x-\left(1+\mathrm{e}^{-x-y-z}\right) \mathrm{d} y
    $$
    从而 $\mathrm{d} z=-\mathrm{d} x-\mathrm{d} y$, 则 $\frac{\partial z}{\partial x}=\frac{\partial z}{\partial y}=-1$.
    法二: 把 $z$ 看作以 $x, y$ 为自变量的函数, 则对方程分别关于 $x$ 和 $y$ 求偏导数得
    $$
    1+\frac{\partial z}{\partial x}=\mathrm{e}^{-x-y-z}\left(-1-\frac{\partial z}{\partial x}\right), \quad 1+\frac{\partial z}{\partial y}=\mathrm{e}^{-x-y-z}\left(-1-\frac{\partial z}{\partial y}\right)
    $$
    从而有 $\frac{\partial z}{\partial x}=\frac{\partial z}{\partial y}=-1$.
    法三: 利用隐函数存在定理, 令 $F(x, y, z)=x+y+z-\mathrm{e}^{-x-y-z}=0$, 可得
    $$
    \frac{\partial F}{\partial x}(x, y, z)=\frac{\partial F}{\partial y}(x, y, z)=\frac{\partial F}{\partial z}(x, y, z)=1+\mathrm{e}^{-x-y-z} .
    $$
    故
    $$
    \frac{\partial z}{\partial x}=-\frac{\frac{\partial F}{\partial x}}{\frac{\partial F}{\partial z}}=-1, \quad \frac{\partial z}{\partial y}=-\frac{\frac{\partial F}{\partial y}}{\frac{\partial F}{\partial z}}=-1
    $$

- 【例题】设 $\left\{\begin{array}{l}x=\mathrm{e}^u+u \sin v \\ y=\mathrm{e}^u-u \cos v\end{array}\right.$
  (i) 求 $\frac{\partial x}{\partial u}, \frac{\partial x}{\partial v}, \frac{\partial y}{\partial u}, \frac{\partial y}{\partial v}$;
  (ii) 求 $\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial v}{\partial x}, \frac{\partial v}{\partial y}$;
  (iii) 检验两组 导数的关系.
  解:(i) 分别对 $u, v$ 求导, 得
  $$
  \begin{cases}\frac{\partial x}{\partial u}=e^u+\sin v, & \frac{\partial x}{\partial v}=u \cos v \\ \frac{\partial y}{\partial u}=e^u-\cos v, & \frac{\partial y}{\partial v}=u \sin v\end{cases}
  $$
  因此, 我们有
  $$
  \boldsymbol{L}=\left(\begin{array}{cc}
  e^u+\sin v & u \cos v \\
  e^u-\cos v & u \sin v
  \end{array}\right)
  $$
  (ii) 法一：求导
  在两个方程两端分别对 $x$ 求导, 得
  $$
  \left\{\begin{array}{l}
  1=\mathrm{e}^u \frac{\partial u}{\partial x}+\frac{\partial u}{\partial x} \sin v+u \cos v \frac{\partial v}{\partial x} \\
  0=\mathrm{e}^u \frac{\partial u}{\partial x}-\frac{\partial u}{\partial x} \cos v+u \sin v \frac{\partial v}{\partial x}
  \end{array}\right.
  $$
  解得
  $$
  \frac{\partial u}{\partial x}=\frac{\sin v}{\mathrm{e}^u(\sin v-\cos v)+1}, \quad \frac{\partial v}{\partial x}=\frac{\cos v-\mathrm{e}^u}{u \mathrm{e}^u(\sin v-\cos v)+u},
  $$
  同样将方程两端分别对 $y$ 求导, 得
  $$
  \left\{\begin{array}{l}
  0=\mathrm{e}^u \frac{\partial u}{\partial y}+\frac{\partial u}{\partial y} \sin v+u \cos v \frac{\partial v}{\partial y} \\
  1=\mathrm{e}^u \frac{\partial u}{\partial y}-\frac{\partial u}{\partial y} \cos v+u \sin v \frac{\partial v}{\partial y}
  \end{array}\right.
  $$
  解得
  $$
  \frac{\partial u}{\partial y}=\frac{-\cos v}{\mathrm{e}^u(\sin v-\cos v)+1}, \quad \frac{\partial v}{\partial y}=\frac{\mathrm{e}^u+\sin v}{u \mathrm{e}^u(\sin v-\cos v)+u} .
  $$
  因此, 我们有
  $$
  \boldsymbol{M}=\left(\begin{array}{cc}
  \frac{\sin v}{\mathrm{e}^u(\sin v-\cos v)+1} & \frac{-\cos v}{\mathrm{e}^u(\sin v-\cos v)+1} \\
  \frac{\cos v-\mathrm{e}^u}{u \mathrm{e}^u(\sin v-\cos v)+u} & \frac{\mathrm{e}^u+\sin v}{u \mathrm{e}^u(\sin v-\cos v)+u}
  \end{array}\right)
  $$
  法二：求微分 用一阶微分形式不变性两端求微分, 得
  $$
  \left\{\begin{array}{c}
  \mathrm{d} x=\mathrm{e}^u \mathrm{~d} u+\sin v \mathrm{~d} u+u \cos v \mathrm{~d} v \\
  \mathrm{~d} y=\mathrm{e}^u \mathrm{~d} u-\cos v \mathrm{~d} u+u \sin v \mathrm{~d} v
  \end{array}\right.
  $$
  然后解方程组得
  $$
  \mathrm{d} u=\frac{\sin v \mathrm{~d} x-\cos v \mathrm{~d} y}{\sin v \mathrm{e}^u-\cos v \mathrm{e}^u+1}, \quad \mathrm{~d} v=\frac{\left(\cos v-\mathrm{e}^u\right) \mathrm{d} x+\left(\mathrm{e}^u+\sin v\right) \mathrm{d} y}{u \sin v \mathrm{e}^u-u \cos v \mathrm{e}^u+u},
  $$
  从而得到本小题结果.
  (iii) 不难验证, 我们有
  $$
  L M=\left(\begin{array}{ll}
  1 & 0 \\
  0 & 1
  \end{array}\right) .
  $$
  由此可见,
  $$
  \frac{\partial x}{\partial u} \cdot \frac{\partial u}{\partial x}+\frac{\partial x}{\partial v} \cdot \frac{\partial v}{\partial x}=1, \quad \frac{\partial y}{\partial u} \cdot \frac{\partial u}{\partial y}+\frac{\partial y}{\partial v} \cdot \frac{\partial v}{\partial y}=1,
  $$
  而并不是
  $$
  \frac{\partial x}{\partial u} \cdot \frac{\partial u}{\partial x}=1, \quad \frac{\partial y}{\partial u} \cdot \frac{\partial u}{\partial y}=1 .
  $$
  这与一元函数的原函数和反函数导数关系不同,
  $$
  \frac{d x}{d y} \cdot \frac{d y}{d x}=1
  $$

- 【例题】设 $u, v, w$ 是由方程组 $\left\{\begin{array}{l}x=u+v+w, \\ y^2=\mathrm{e}^{u v}, \\ x z=u v w\end{array}\right.$ 确定的 $x, y, z$ 的函数, $u \neq v$, 求 $\frac{\partial u}{\partial x}, \frac{\partial u}{\partial y}, \frac{\partial u}{\partial z}$. 

  解: 利用一阶微分形式不变性得：
  $$
  \left\{\begin{aligned}
  \mathrm{d} x & =\mathrm{d} u+\mathrm{d} v+\mathrm{d} w \\
  2 y \mathrm{~d} y & =v \mathrm{e}^{u v} \mathrm{~d} u+u \mathrm{e}^{u v} \mathrm{~d} v \\
  z \mathrm{~d} x+x \mathrm{~d} z & =v w \mathrm{~d} u+u w \mathrm{~d} v+u v \mathrm{~d} w
  \end{aligned}\right.
  $$
  解方程组得

  $\mathrm{d} u=\frac{\left|\begin{array}{ccc}\mathrm{d} x & 1 & 1 \\ 2 y \mathrm{~d} y & u \mathrm{e}^{u v} & 0 \\ z \mathrm{~d} x+x \mathrm{~d} z & u w & u v\end{array}\right|}{\left|\begin{array}{ccc}1 & 1 & 1 \\ v \mathrm{e}^{u v} & u \mathrm{e}^{u v} & 0 \\ v w & u w & u v\end{array}\right|}=\frac{\left(u^2 v-u z\right) \mathrm{e}^{u v} \mathrm{~d} x+2 y u(w-v) \mathrm{d} y-u x \mathrm{e}^{u v} \mathrm{~d} z}{u v \mathrm{e}^{u v}(u-v)}$

  所以
  $$
  \frac{\partial u}{\partial x}=\frac{\left(u^2 v-u z\right) \mathrm{e}^{u v}}{u v \mathrm{e}^{u v}(u-v)}, \quad \frac{\partial u}{\partial y}=\frac{2 y u(w-v)}{u v \mathrm{e}^{u v}(u-v)}, \quad \frac{\partial u}{\partial z}=\frac{u x \mathrm{e}^{u v}}{u v \mathrm{e}^{u v}(u-v)}
  $$
  





#### 15.4 极值问题

- 无条件极值问题：

  - 必要条件: 设 $x^0$ 是 $n$ 元函数 $f(x)$ 的极值点. 若 $f(x)$ 于 $x^0$ 处的偏导数存在, 则有
    $$
    \frac{\partial f}{\partial x_i}\left(x^0\right)=0, \quad i=1,2, \cdots, n .
    $$
    充分条件: 设 $f(x)$ 为定义于区域 $\Omega \subseteq \mathbb{R}^n$ 上的函数, 并于 $\Omega$ 上存在连续的二阶偏导数. 设 $x^0$ 为 $f(x)$ 的临界点, 若 $f(x)$ 于 $x^0$ 点的 Hesse 矩阵正定, 则 $x^0$ 是 $f(x)$ 的极小值点; 若 Hesse 矩 阵为负定, 则 $x^0$ 是 $f(x)$ 的极大值点; 若矩阵为不定矩阵, 则 $x^0$ 一定不是极值点.

- 条件极值问题：

  - 必要条件: 设 $f(x)$ 为定义于区域 $\Omega \subseteq \mathbb{R}^n$ 上的可微函数, $\varphi_j(x), j=1,2, \cdots, k(k<n)$ 也 是区域 $\Omega$ 上的 $n$ 元可微函数. 如果 $x^0$ 是函数 $f(x)$ 在条件 $\varphi_j(x)=0, j=1,2, \cdots, k$ 下的极 值点, 则必存在一组常数 $\lambda_j, j=1,2, \cdots, k$, 使得

  $$
  \frac{\partial f}{\partial x_i}\left(x^0\right)=\sum_{j=1}^k \lambda_j \frac{\partial \varphi_j}{\partial x_i}\left(x^0\right), \quad i=1,2, \cdots, n .
  $$
  - 充分条件: Lagerange 乘数法, 求 $n$ 元函数 $f(x)$ 在条件 $\varphi_j(x)=0, j=1,2, \cdots, k(k<n)$ 下 的极值点, 首先引入 Lagrange 函数

  $$
  F\left(x, \lambda_1, \lambda_2, \cdots, \lambda_k\right)=f(x)-\sum_{j=1}^k \lambda_j \varphi_j(x),
  $$
  然后计算此函数临界点, 即求解方程组
  $$
  \begin{aligned}
  & \frac{\partial F}{\partial x_i}\left(x, \lambda_1, \lambda_2, \cdots, \lambda_k\right)=0, \quad i=1,2, \cdots, n, \\
  & \frac{\partial F}{\partial \lambda_i}\left(x, \lambda_1, \lambda_2, \cdots, \lambda_k\right)=0, \quad i=1,2, \cdots, k .
  \end{aligned}
  $$
  在这个方程组的解中进一步判断那些点是条件极值点.
  注: 对可微函数, 极值点 $\rightleftharpoons$ 临界点.

- 【例题】设 $f(x, y)=x^2+4 x y-2 y^2$, 证明: 当 $\frac{1}{2} x^2+2 y^2 \leq 10$ 时, $-20 \leq f(x, y) \leq 30$.
  解: 原题可转化为求函数 $f(x, y)=x^2+4 x y-2 y^2$ 在有界区域 $D=\left\{(x, y) \in \mathbb{R}^2 ; \frac{1}{2} x^2+2 y^2<\right.$
  $10\}$ 的闭包 $\bar{D}$ 上的最大值和最小值问题. 首先考虑 $f(x, y)$ 在区域 $D$ 内的临界点和临界值, 为此求解方程组

$$
\begin{aligned}
& \frac{\partial f}{\partial x}=2 x+4 y=0, \\
& \frac{\partial f}{\partial y}=4 x-4 y=0 .
\end{aligned}
$$
此方程组只有平凡解 $x=y=0$, 而函数 $f(x, y)$ 在仅有的临界点上的值为 $f(0,0)=0$.
其次, 考虑 $f(x, y)$ 在区域 $D$ 的边界 $\partial D=\left\{(x, y) \in \mathbb{R}^2 ; \frac{1}{2} x^2+2 y^2=10\right\}$ 上的最大, 最小值. 这是一个求函数 $f(x, y)$ 在条件 $\varphi(x, y)=\frac{1}{2} x^2+2 y^2-10=0$ 下的最大最小值问题, 我们采 用 Lagrange 乘数法. 引入 Lagrange 函数
$$
F(x, y, \lambda)=f(x, y)+\lambda \varphi(x, y)=x^2+4 x y-2 y^2+\lambda\left(\frac{1}{2} x^2+2 y^2-10\right) .
$$
求解方程组
$$
\left\{\begin{array}{l}
F_x=2 x+4 y+\lambda x=0 \\
F_y=4 x-4 y+4 \lambda y=0 \\
F_\lambda=\frac{1}{2} x^2+2 y^2-10=0 .
\end{array}\right.
$$
由于 $x=y=0$ 不会是方程组的解, 由线性方程组理论得:
$$
\left|\begin{array}{cc}
2+\lambda & 4 \\
4 & 4(\lambda-1)
\end{array}\right|=0,
$$
由此可得 $\lambda=-3$ 或 $\lambda=2$, 并且相应的 $(x, y)$ 为
$$
(-4,-1),(4,1) \text { 或 }(2,-2),(-2,2) \text {, }
$$
由于 $f(-4,-1)=f(4,1)=30, f(2,-2)=f(-2,2)=-20$. 有闭区域上连续函数的性质 可知 $f(x, y)$ 在 $\bar{D}$ 上取最值. 最大值点为 $(-4,-1)$ 和 $(4,1)$, 最大值为 30 , 最小值点为 $(2,-2)$ 和 $(-2,2)$, 最小值为 $-20$.

