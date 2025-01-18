# 第3章 静止流体力学Fluid Statics
## 3.1 静止流体中的压力（pressure in a static fluid）
### 3.1.1 压力的各向同性（pressure and its isotropy）
当流体处于静止状态时，流体中任意表面所受的力垂直于该表面，不存在剪切力。考虑流体中一点，取面积为$\Delta A$的微小面元，设垂直作用于该面元的力为$\Delta F$，则极限值
$$p = \lim_{\Delta A \to 0} \frac{\Delta F}{\Delta A}$$
定义为作用在面元上的**压力强度**（intensity of pressure，圧力強度），或该点的**压力**（pressure，圧力）。

压力的单位在国际单位制（SI）中为**帕斯卡**（Pascal，パスカル），符号为$Pa$，$1 Pa = 1 N/m^2 = 1 kg/(m\cdot s^2)$。此外，还常用$kgf/cm^2$、$mmH_2O$（毫米水柱，millimeter of water column，ミリメートル水柱）、$mmHg$（毫米汞柱，millimeter of mercury column，ミリメートル水銀柱）、$atm$（标准大气压，standard atmosphere，標準大気圧）、$at$（工程大气压，technical atmosphere，工学大気圧）、$bar$（巴，bar，バール）等单位。

静止流体中任意一点的压力在各个方向上相等，且是位置的函数。这一性质称为压力的各向同性，证明如下。

如图3.1所示，在密度为$\rho$的静止流体中，取边长为$dx$、$dy$、$dz$的微小四面体$PABC$。作用在该流体微元上的力有垂直于各表面的压力和重力。采用直角坐标系（笛卡尔坐标系，Cartesian coordinate system，直交座標系（カルテシアン座標系）），使四面体的棱$PA$、$PB$、$PC$分别平行于$x$、$y$、$z$轴，$z$轴竖直向上，点$P$的坐标为$(x,y,z)$。设$p_x$、$p_y$、$p_z$分别为$x$、$y$、$z$轴方向的压力，$p$为垂直作用于斜面$ABC$且面积为$dA$的压力。设斜面$ABC$的法线与$x$、$y$、$z$轴的夹角分别为$\alpha$、$\beta$、$\gamma$，则斜面$ABC$在$x$、$y$、$z$轴方向的投影满足
$$dA\cos\alpha = \frac{dydz}{2}, \quad dA\cos\beta = \frac{dxdz}{2}, \quad dA\cos\gamma = \frac{dxdy}{2}$$
根据力的平衡条件，在$x$、$y$、$z$轴方向分别有
$$
\begin{cases}
p_x\frac{dydz}{2} - pdA\cos\alpha = 0 & (x轴方向) \\
p_y\frac{dxdz}{2} - pdA\cos\beta = 0 & (y轴方向) \\
p_z\frac{dxdy}{2} - pdA\cos\gamma - \rho g\frac{1}{6}dxdydz = 0 & (z轴方向)
\end{cases}
$$
在$z$轴方向的平衡方程中，考虑了流体微元的自重$\rho g\frac{1}{6}dxdydz$。将上述方程与投影关系式联立，可得
$$p_x - p = 0, \quad p_y - p = 0, \quad p_z - p - \frac{\rho gdz}{3} = 0$$
当微小四面体$ABC$向点$P$收缩取极限时，$dz \to 0$，最终有
$$p_x = p_y = p_z = p$$
由于斜面$ABC$的方向是任意的，这表明压力$p$在点$P$的各个方向上取值相同（帕斯卡原理，Pascal's principle，パスカルの原理）。同时，点$P$的位置也是任意的，所以静止流体中的压力是位置的函数，即点函数$p = p(x,y,z)$。
### 3.1.2 欧拉平衡方程式（Euler's equilibrium equation）
考虑密度$\rho$为常数的静止流体，取边长为$dx$、$dy$、$dz$的微小平行六面体（infinitesimal parallel hexahedron，微小平行六面体），如图3.2所示。该微小流体微元要处于静平衡状态，作用在其上的表面力（surface force，表面力）与体积力（body force，体積力）必须平衡。设作用在单位质量流体上的体积力为$\boldsymbol{K} = iX + jY + kZ$，其中$i$、$j$、$k$分别为$x$、$y$、$z$方向的单位向量，$X$、$Y$、$Z$分别为单位质量物体所受体积力向量在$x$、$y$、$z$方向的分量。作用在微小六面体面$ABCD$上的总压力为$pdydz$，与面$ABCD$沿$x$方向相距$dx$的面$EFGH$上的总压力为$\left[p + \frac{\partial p}{\partial x}dx\right]dydz$。设微小六面体的质量为$dm$，则沿$x$方向的总体积力为$Xdm = X\rho dxdydz$。根据$x$方向的力平衡条件
$$pdydz + X\rho dxdydz - \left(p + \frac{\partial p}{\partial x}dx\right)dydz = 0$$
整理可得：$\frac{\partial p}{\partial x} = X\rho$。同理，由$y$、$z$方向的力平衡条件可得：$\frac{\partial p}{\partial y} = Y\rho$，$\frac{\partial p}{\partial z} = Z\rho$。用单位向量$i$、$j$、$k$表示，上述方程可写为
$$i\frac{\partial p}{\partial x} + j\frac{\partial p}{\partial y} + k\frac{\partial p}{\partial z} = \rho(iX + jY + kZ)$$
或写成
$$\nabla p = \rho\boldsymbol{K}$$
其中，$\nabla \equiv i\frac{\partial}{\partial x} + j\frac{\partial}{\partial y} + k\frac{\partial}{\partial z}$，$\nabla p = grad p$表示压力的**梯度向量**（gradient vector of pressure，圧力の勾配ベクトル）。式(3.5)被称为**欧拉平衡方程式**（Euler's equilibrium equation，オイラーの平衡方程式）。将式(3.5)在$x$、$y$、$z$方向的分量分别乘以$dx$、$dy$、$dz$后相加，可得
$$\frac{\partial p}{\partial x}dx + \frac{\partial p}{\partial y}dy + \frac{\partial p}{\partial z}dz = \rho(Xdx + Ydy + Zdz)$$
由于函数$f(x,y,z)$的梯度$\nabla f = i\frac{\partial f}{\partial x} + j\frac{\partial f}{\partial y} + k\frac{\partial f}{\partial z}$，上式左边为压力$p$的全微分，即
$$dp = \rho(Xdx + Ydy + Zdz)$$
另一方面，由式(3.5)中各方向的平衡条件$\frac{\partial p}{\partial x} = \rho X$，$\frac{\partial p}{\partial y} = \rho Y$，$\frac{\partial p}{\partial z} = \rho Z$，对其进行偏微分运算，可得
$$\frac{\partial X}{\partial y} = \frac{\partial Y}{\partial x}, \quad \frac{\partial X}{\partial z} = \frac{\partial Z}{\partial x}, \quad \frac{\partial Y}{\partial z} = \frac{\partial Z}{\partial y}$$
这意味着物体所受体积力向量$\boldsymbol{K}$的**旋度**（curl，回転ベクトル）为零，即$rot\boldsymbol{K} = 0$。根据向量分析理论（例如，Aris, R.在1962年的著作中所述），这是体积力$\boldsymbol{K}$具有标量势函数$\Psi = \Psi(x,y,z)$的充分必要条件，即体积力可表示为
$$X = -\frac{\partial \Psi}{\partial x}, \quad Y = -\frac{\partial \Psi}{\partial y}, \quad Z = -\frac{\partial \Psi}{\partial z}$$
写成向量形式为
$$\boldsymbol{K} = -\nabla \Psi$$
将式(3.8a)代入式(3.7)，可验证式(3.7)成立。由于式(3.8a)和式(3.8b)是由欧拉平衡方程式(3.5)直接推导得出的，这表明当流体处于静止平衡状态时，作用在流体上的体积力具有势函数。

将式(3.8a)代入式(3.6)，可得
$$dp = -\rho\left(\frac{\partial \Psi}{\partial x}dx + \frac{\partial \Psi}{\partial y}dy + \frac{\partial \Psi}{\partial z}dz\right) = -\rho d\Psi$$
对上式积分可得
$$p = -\rho \Psi + C$$
其中$C$为积分常数。$p$和$\Psi$是位置$x = (x,y,z)$的函数，即点函数$p(x,y,z)$和$\Psi(x,y,z)$。设某一基点$x_0$处$p$和$\Psi$的值分别为$p_0$和$\Psi_0$，则$p_0 = -\rho \Psi_0 + C$，故有$p = p_0 - \rho(\Psi - \Psi_0)$。这表明等压面（isobaric surface，等圧面）与等势面（equipotential surface，等ポテンシャル面）是一致的。
### 3.1.3 重力场中的压力分布（pressure distribution in the gravity field）
在等压面上，$dp = 0$。设等压面上的微小线素向量为$d\boldsymbol{s} = (dx,dy,dz)$，体积力向量为$\boldsymbol{K}$，则由式(3.6)可知
$$Xdx + Ydy + Zdz = \boldsymbol{K} \cdot d\boldsymbol{s} = 0$$
这表明等压面与体积力向量垂直，如图3.3所示。

考虑受重力$\boldsymbol{g}$作用的静止流体，在式(3.6)中令$X = 0$，$Y = 0$，$Z = -g$（$g$为重力加速度），则压力变化可表示为
$$dp = -\rho g dz$$
对于液体，假设密度$\rho$为常数，对上式积分可得
$$p = -\rho g z + C$$
设$z = z_0$（液表面）处的压力为$p_a$，则$C = p_a + \rho g z_0$，因此静止液体中的压力分布为
$$p = p_a + \rho g(z_0 - z)$$
若以$p_a$为基准压力，将$p - p_0$记为$p$，并令液表面到测量点的垂直距离（深度）为$h = z_0 - z$，则有
$$p = \rho g h$$
由该式可知，压力与液面下的深度$h$成正比。式(3.13)表明压力可以用液柱高度来表示，此液柱高度称为**水头**（head，水頭）。这就是使用$mmH_2O$、$mmAq$、$mmHg$等单位表示压力的原因。压力的表示方法有两种，一种是以绝对真空状态为基准表示的**绝对压力**（absolute pressure，絶対圧力），另一种是以大气压为基准表示的**表压力**（gage pressure，ゲージ圧力）。标准大气压的绝对压力，在$g = 9.80665 m/s^2$的地方，相当于$0^{\circ}C$时$760mm$水柱产生的压力（即$760mmHg$），在工程单位中为$1.0332 kgf/cm^2$，在国际单位制（SI）中为$101.325 kPa$，在理学单位中为$1.01325 bar$或$1013.25 mbar$，常将此标准大气压的压力简称为$1 atm$（1大气压）。在工程上，将$1 kgf/cm^2$的压力称为$1 at$（1工程大气压），$1 at = 98.0665 kPa = 735.52 mmHg$。在式(3.12)中，若将$p_a$视为大气压，则式(3.13)表明液体中的表压力与液面下的深度$h$成正比。压力单位换算表如表3.1所示。
| 传统单位 | SI单位（$Pa$） | 换算关系 |
| ---- | ---- | ---- |
| $kgf/cm^2$ | $9.80665×10^4 Pa$ |  |
| $kgf/m^2$ | $9.80665 Pa$ |  |
| $mmHg$ | $1.33322×10^2 Pa$ |  |
| $mmH_2O$ | $9.80665 Pa$ |  |
| $mH_2O$ | $9.80665×10^2 Pa$ |  |
| $at$（工程大气压） | $9.80665×10^4 Pa$ |  |
| $atm$（标准大气压） | $1.01325×10^5 Pa$ |  |
| $bar$（巴） | $10^5 Pa$ |  |
| $Torr$（托） | $1.33322×10^2 Pa$ |  |

图3.4展示了大气压、绝对压力和表压力的关系。当测定压力低于大气压时，两者的差值（取正值）称为**负压**（negative pressure，負圧）或**真空表压力**（vacuum gage pressure，真空ゲージ圧力）。

**例3.1** 已知压力$p = 3×10^5 Pa$，水的密度$\rho = 10^3 kg/m^3$，求对应的水头$h$。
**解** 由$p = \rho gh$，可得
$$h = \frac{p}{\rho g} = \frac{3×10^5}{10^3×9.81} = 30.6(m)$$

**例3.2** 求水面下$15m$处的压力（表压力），设水面压力为标准大气压，同时求出该点的绝对压力。
**解** 取$\rho g$的平均值为$9810 N/m^3$，根据式(3.13)，表压力$p$为
$$p = \rho gh = 9810×15 = 147150(N/m^2) = 147.15(kPa)$$
绝对压力$p_{abs}$等于标准大气压$p_a = 101.325 kPa$与表压力$p$之和，即
$$p_{abs} = p_a + p = 101.325 + 147.15 = 248.475(kPa) \approx 248(kPa)$$

**例3.3** 水银的比重$s = 13.6$，求在表压力为$1.65 bar$时水银柱的高度，同时求出相同压力下水柱的高度。设水的密度$\rho_w = 1000 kg/m^3$。
**解** 水银的密度$\rho = s\rho_w = 13.6×1000 = 13600 kg/m^3$，$1.65 bar = 1.65×10^5 Pa$。
根据$h = \frac{p}{\rho g}$，可得水银柱的高度为
$$h = \frac{1.65×10^5}{13600×9.81} = 1.24(m)$$
由于水的密度是水银密度的$\frac{1}{13.6}$，所以相同压力下水柱的高度为
$$h = \frac{1.24}{\frac{1}{13.6}} = 16.9(m)$$

对于气体，由于其密度$\rho$是压力$p$的函数，因此不能直接对式(3.11)进行积分。然而，在理想气体假设下，当气体在等温状态（isothermal state，等温状態）或绝热状态（adiabatic state，断熱状態）下变化时，可以进行积分。以下分别进行讨论。

在等温条件下，设基准面处的压力、密度和绝对温度分别为$p_0$、$\rho_0$、$T_0