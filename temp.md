在等温条件下，设基准面处的压力、密度和绝对温度分别为$p_0$、$\rho_0$、$T_0$，高度为$z$处的压力、密度和温度分别为$p$、$\rho$、$T( = T_0)$。由理想气体状态方程可知$\frac{p}{\rho} = \frac{p_0}{\rho_0} = RT_0$，其中$R$为气体常数。根据$dz = -\frac{dp}{\rho g}=-\frac{p_0}{\rho_0 g}\frac{dp}{p}=-\frac{RT_0}{g}\frac{dp}{p}$，对其进行积分：
$$\int_{0}^{z} dz = -\frac{RT_0}{g} \int_{p_0}^{p} \frac{dp}{p}$$
可得$z = -\frac{RT_0}{g} \ln(\frac{p}{p_0})$，整理后压力$p$关于高度$z$的表达式为$p = p_0 e^{\frac{gz}{RT_0}}$ 。

在绝热条件下，$\rho$与$p$满足$p\rho^{-\kappa}=p_0\rho_0^{-\kappa}= \text{常数}$，这里$\kappa$为**定压比热**（specific heat at constant pressure，定圧比熱）$C_p$与**定容比热**（specific heat at constant volume，定積比熱）$C_v$之比，即$\kappa = \frac{C_p}{C_v}$，$\kappa$也被叫做**比热比**（specific heat ratio，比熱比）或**绝热指数**（adiabatic index，断熱指数）。对$dz = -\frac{dp}{\rho g}$积分：
$$
\begin{align*}
z&=-p_0^{\frac{1}{\kappa}}(g\rho_0)^{-1}\int_{p_0}^{p}p^{-\frac{1}{\kappa}}dp\\
&=\frac{\kappa}{\kappa - 1}\frac{p_0^{\frac{1}{\kappa}}}{\rho_0 g}(p_0^{\frac{\kappa - 1}{\kappa}} - p^{\frac{\kappa - 1}{\kappa}})
\end{align*}
$$
整理可得压力$p$关于高度$z$的表达式为$p = p_0\left\{1 - \left(\frac{\kappa - 1}{\kappa}\right)\frac{\rho_0 g z}{p_0}\right\}^{\frac{\kappa}{\kappa - 1}} = p_0\left\{1 - \left(\frac{\kappa - 1}{\kappa}\right)\frac{g z}{RT_0}\right\}^{\frac{\kappa}{\kappa - 1}}$ 。

式$(3.14a)$、$(3.14b)$以及式$(3.15a)$、$(3.15b)$分别表示了等温及绝热变化过程中气体高度与压力的关系。在大气的情况中，对流层（距地面约$11km$ ）内气温并非恒定，高度每升高$100m$，气温约降低$0.65K$。这种温度随高度的变化与绝热变化情况稍有差异。考虑高度$z[m]$处大气的绝对温度$T[K]$近似由下式表示：
$$T = T_0 - Bz$$
其中$T_0$为海平面（$z = 0$）处的绝对温度，$B = 6.5×10^{-3}[K/m]$。根据理想气体状态方程$\rho = \frac{p}{RT} = \frac{p}{R(T_0 - Bz)}$，对于空气，气体常数$R = 287[J/(kg·K)]$。将$\rho$代入式$(3.11)$并积分，可得大气中压力$p$与高度$z$关系的高精度近似式为：
$$p = p_a\left(1 - \frac{Bz}{T_0}\right)^{\frac{g}{RB}}$$
其中$p_a$为海平面（$z = 0$）处的大气压，$\frac{g}{RB} = 5.257$。

**例3.4** 已知海平面压力为$101350Pa$，分别使用(1)精确公式$(3.17)$和(2)假设海平面标准温度为$15^{\circ}C( = 288.16K)$的等温近似公式，计算海拔$7000m$处的标准压力，并判断等温近似是否合理。
**解**(1) 在精确公式$(3.17)$中使用绝对温度：
$$
\begin{align*}
p&=p_a\left(1 - \frac{0.00650×7000}{288.16}\right)^{5.257}\\
&=101350×0.8421^{5.257}\\
&=101350×0.40512\\
&=41059(Pa)
\end{align*}
$$
(2) 使用等温近似公式：
$$
\begin{align*}
p&\approx p_a\exp\left(-\frac{gz}{RT}\right)\\
&=101350×\exp\left(-\frac{9.81×7000}{287×288.16}\right)\\
&=101350×\exp(- 0.830)\\
&\approx 44200(Pa)
\end{align*}
$$
该结果比精确值高$7.6\%$，说明在对流层中，等温公式并不准确。
### 3.1.4 压力计（manometer）
利用液柱高度来测量流体压力的仪器称为**液柱压力计**或**压力计**（manometer，マノメーター）。
- **普通压力计（simple manometer）**：当被测流体为液体且压力相对较低时，如图$3.5$所示，将液体容器与管子适当连接，通过测量液柱自身高度$h$，可得知点$A$的压力。若液体密度为$\rho$，则点$A$的压力$p$可表示为$p = p_a + \rho gh$，其中$p_a$为液面压力，等于大气压。若用表压力表示$p$，则为$p = \rho gh$。当$h$较大时，可采用如图$3.6$所示的$U$形管压力计（U - tube manometer，U字管マノメーター）。在$U$形管内装入密度较大的液体，当测定容器内压力较高时，可按图$3.6$所示方法测量容器内压力。在图$3.6$的情况下，设容器内流体密度为$\rho_1$，$U$形管内液体密度为$\rho_2$，$U$形管另一端与大气压$p_a$相通。点$B$的压力为$p_A + \rho_1gh_1$，点$C$的压力为$p_a + \rho_2gh_2$，由于$B$、$C$两点在同一水平面上，压力相等，因此有$p_A + \rho_1gh_1 = p_a + \rho_2gh_2$，整理可得容器内点$A$的压力为$p_A = p_a + g(\rho_2h_2 - \rho_1h_1)$，其表压力为$p_A - p_a = g(\rho_2h_2 - \rho_1h_1)$。
- **差压计（differential manometer）**：如图$3.7(a)$、$3.7(b)$所示，用于测量两点$A$、$B$压力差的液柱压力计称为**差压计**（differential manometer，示差マノメーター）。在图$3.7(a)$中，当$U$形管内液体密度$\rho_s$大于容器内液体密度$\rho_1$、$\rho_2$时使用该装置。点$A$与点$B$的压力差$p_A - p_B$可通过以下方式求得：点$C$的压力为$p_A + \rho_2gh_2$，与点$C$水平位置的点$D$的压力为$p_B + \rho_1gh_1 + \rho_sgh$，由于这两点压力相等，即$p_A + \rho_2gh_2 = p_B + \rho_1gh_1 + \rho_sgh$，整理可得$p_A - p_B = g(\rho_1h_1 + \rho_s h - \rho_2h_2)$。在图$3.7(b)$中，$U$形管倒立，上部封闭有密度小于容器内液体的流体（如空气）。此时压力差为$p_A - p_B = g(\rho_2h_2 - \rho_1h_1 - \rho_s h)$。
**例3.5** 如图$3.8$所示，求压力差$\Delta p = p_A - p_B$。已知$\rho_A = 1.255×10^3 kg/m^3$，$\rho_B = 868 kg/m^3$，$\rho_s = 13.520×10^3 kg/m^3$，重力加速度$g = 9.81 m/s^2$。
**解** 根据式$(3.20)$：
$$
\begin{align*}
\Delta p&=p_A - p_B\\
&=g(\rho_Bh_1 + \rho_S h - \rho_Ah_2)\\
&=9.81×\{868×(0.7 - 0.1)+13520×(0.1 + 0.1)-1255×(0.1 + 0.4)\}\\
&=25.5×10^3(Pa)\\
&=25.5(kPa)
\end{align*}
$$
- **微压计（micro manometer）**：用于测量微小压力差的压力计称为**微压计**（micro manometer，微圧計），有多种形式。如图$3.9$所示的双液微压计（two - liquid micro manometer，2液微圧マノメーター），在断面为$a$的$U$形管上方连接一个断面面积为$A$（$A\gg a$）的容器，先向容器内注入密度为$\rho_3$的液体，再注入密度为$\rho_2$的液体，两种液体不混合且密度差较小。容器上部充满密度为$\rho_1$的流体，当$p_A$、$p_B$的压力作用于容器时，设容器内液面的位移为$\Delta y$，则两点压力差$p_A - p_B$可通过以下方式求得：点$C$的压力为$p_A + \rho_1g(h_1 + \Delta y) + \rho_2g(h_2 + \frac{h}{2} - \Delta y)$，点$D$（与点$C$等高）的压力为$p_B + \rho_1g(h_1 - \Delta y) + \rho_2g(h_2 - \frac{h}{2} + \Delta y) + \rho_3gh$，由于这两点压力相等，即
$$
\begin{align*}
&p_A + \rho_1g(h_1 + \Delta y) + \rho_2g(h_2 + \frac{h}{2} - \Delta y)\\
=&p_B + \rho_1g(h_1 - \Delta y) + \rho_2g(h_2 - \frac{h}{2} + \Delta y) + \rho_3gh
\end{align*}
$$
整理可得$p_A - p_B = \rho_3gh - \rho_2g(h - 2\Delta y) - 2\rho_1g\Delta y$。根据体积恒定原理$2a\Delta y = ha$，消去$\Delta y$可得$p_A - p_B = h\left\{\rho_3g - \rho_2g\left(1 - \frac{a}{A}\right)-\rho_1g\frac{a}{A}\right\}$。由于$\frac{a}{A}$很小，可忽略包含$\frac{a}{A}$的项，近似得到$p_A - p_B \approx (\rho_3 - \rho_2)gh$。由此式可知，$\rho_3$与$\rho_2$的差值越小，对于相同的压力差$p_A - p_B$，$h$的值越大，压力计的灵敏度越高。
**例3.6** 在图$3.9$所示的双液微压计中，系统内为空气，液体$2$的比重$S_2 = 1.0$，液体$3$的比重$S_3 = 1.10$，$A = 0.01$，$h = 10mm$，$t = 20^{\circ}C$，大气压为$760mmHg$。计算压力差$p_A - p_B$。已知标准条件下纯水的密度为$1000 kg/m^3$，水银的比重为$13.6$。
**解** 空气的密度为：
$$
\begin{align*}
\rho_1&=\frac{p}{RT}\\
&=\frac{0.76×13.6×1000×9.81}{287×(273 + 20)}\\
&=1.21(kg/m^3)
\end{align*}
$$
$\rho_1g\frac{a}{A} = 1.21×9.81×0.01 = 0.119(N/m^3)$
$$
\begin{align*}
\rho_3g - \rho_2g\left(1 - \frac{a}{A}\right)&=1000×9.81×(1.10 - 0.99)\\
&=1080(N/m^3)
\end{align*}
$$
将上述结果代入式$(3.22)$可得：
$$
\begin{align*}
p_A - p_B&=0.01×(1080 - 0.119)\\
&=10.8(Pa)
\end{align*}
$$
如图$3.10$所示的倾斜式压力计（inclined - tube manometer，傾斜管マノメーター），通常用于测量气体的微小压力。图中$0 - 0$为倾斜式压力计的液面，当$A$、$B$两侧存在压力差$\Delta p = p_A - p_B$时，容器内液面下降$\Delta h$，倾斜管内液柱上升$h$。由于两侧作用的流体通常为气体，其重量影响可忽略不计，因此点$C$与点$D$的压力相等，即$p_A = p_B + \rho g(h + \Delta h)$，整理可得压力差$\Delta p = p_A - p_B = \rho g(h + \Delta h)$。设容器与倾斜管的横截面积分别为$S$、$a$，根据体积恒定原理$S\Delta h = al$，且$h = l\sin\theta$，将其代入上式可得$\Delta p = \rho gl\left(\sin\theta + \frac{a}{S}\right)$。若$\frac{a}{S} \approx 0$，则$\Delta p \approx \rho gl\sin\theta$。由此可知，$\theta$越小，$l$越大，压力计的灵敏度越高。
