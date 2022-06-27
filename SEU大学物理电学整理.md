# 大学物理 电学

## Charpter 5 静电场

### 常量：

1. $e = 1.602\times10^{-19}\ C$
2. $\varepsilon_0$真空电容率

### 库仑定律

$$
\vec{F} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{q_1q_2}{r^2}\cdot \vec{e_r}
$$

### 电场强度

1. 定义式：$\vec{E} = \frac{\vec{E}}{q}$

2. 点电荷电场强度可由定义式导出：
   $$
   \vec{E} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{Q}{r^2}\cdot \vec{e_r}
   $$

3. 多个点电荷空间里任意一处的电场强度可以矢量叠加

***以下给出4个由叠加原理引出的结论：***

1. 电偶极子

   1. 轴$\vec{r_0}$：由$-q$指向$+q$的矢量

   2. 电偶极矩（电矩）：$\vec{p}=q\cdot\vec{r_0}$

   3. 以轴中点为原点，轴的方向为x轴正向，则

      1. 坐标$(x,0)$处的电场强度直接叠加就行我就不写了

      2. 当$x>>r_0$时，坐标$(x,0)$处电场强度可以近似表示为
         $$
         \vec{E} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{2qr_0}{x^3}\cdot\vec{i} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{2\vec{p}}{x^3}
         $$

      3. 坐标$(0,y)$处的电场强度也是直接叠加就行，垂直分量抵消，水平分量相等，我也就不写了

      4. 当$y>>r_0$时，坐标$(0,y)$处的电场强度可以近似表示为
         $$
         \vec{E} = -\frac{1}{4\pi\varepsilon_0}\cdot\frac{\vec{p}}{y^3}
         $$

2. 均匀带电圆环的电场分布

   带电量$+q$，半径为$R$，点$P$为圆环轴线上距离圆心$x$的一点，则整个圆环在$P$处产生的场强为：
   $$
   \vec{E} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{qx}{(x^2+R^2)^{\frac{3}{2}}}
   $$

   1. $x>>R$则$(x^2+R^2)^{\frac{3}{2}} \approx x^3$，因此有：
      $$
      E \approx \frac{1}{4\pi\varepsilon_0}\cdot\frac{q}{r^2}
      $$

   2. 环心处电场强度近似为0

   3. 由$\frac{dE}{dx} = 0$可以求得电场强度极大的位置：$x = \pm\frac{\sqrt{2}}{2}R$

3. 均匀带电薄圆盘

   电荷面密度为$\sigma$，半径为$R$，点$P$为圆环轴线上距离圆心$x$的一点。分成许多的细圆环带去作为$dE$然后积分，$P$处产生的场强为：
   $$
   \frac{\sigma x}{2\varepsilon_0}(\frac{1}{\sqrt{x^2}}-\frac{1}{\sqrt{x^2+R^2}})
   $$
   如果$x<<R$，即圆盘看成无限大的均匀带电平面，则$\frac{1}{\sqrt{x^2}}-\frac{1}{\sqrt{x^2+R^2}} \approx \frac{1}{\sqrt{x^2}}$，因此
   $$
   E = \pm\frac{\sigma}{2\varepsilon_0}
   $$
   符号和$x$的符号一样，正负号代表方向

4. 均匀带电球面

   带电量为$Q$，半径为$R$

   1. 球面外就是点电荷（高斯定理）
      $$
      \vec{E} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{Q}{r^2}\cdot \vec{e_r}
      $$

   2. 球面上的就是点电荷的一半（如何证明？）
      $$
      \vec{E} = \frac{1}{2}\cdot\frac{1}{\pi\varepsilon_0}\cdot\frac{Q}{r^2}\cdot \vec{e_r}
      $$

### 电通量和高斯定理

$$
d\phi = \vec{E}\cdot d\vec{S}
$$

**真空中的高斯定理：**

当高斯面$S$为闭合曲面时，有：
$$
\phi = \oint_S \vec{E}\cdot d\vec{S} = \frac{1}{\varepsilon_0}\sum q^{in}
$$
***以下给出高斯定理导出的结论：***

1. 无限长均匀直导线

   电荷线密度为$\lambda$，点$P$到直导线的垂直距离为$r$，则：
   $$
   E = \frac{\lambda}{2\pi\varepsilon_0r}
   $$

2. 无限长均匀带电圆筒

   内部$E = 0$，外部等同于无限长均匀直导线

3. 均匀带电球面

   带电量为$Q$，半径为$R$

   1. 球面外就是点电荷（高斯定理）
      $$
      \vec{E} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{Q}{r^2}\cdot \vec{e_r}
      $$

   2. 球面上的就是点电荷的一半（如何证明？）
      $$
      \vec{E} = \frac{1}{2}\cdot\frac{1}{\pi\varepsilon_0}\cdot\frac{Q}{r^2}\cdot \vec{e_r}
      $$

4. 无限大均匀带电平面（也可以由叠加原理导出）
   $$
   E = \frac{\sigma}{2\varepsilon_0}
   $$

5. 两块等量异号无限大带电平面（电容器的前身）

   外部$E = 0$，内部$E = 2\cdot\frac{\sigma}{2\varepsilon_0}$

### 静电场的环路定理

$$
\oint_l \vec{E}\cdot dl = 0
$$

上式说明了静电场是保守场，积分和路径无关，因此可以定义势函数

### 电势&电势能

实验电荷由点$A$移动到$B$静电力所做的功：
$$
W_{AB} = q0\int_A^B\vec{E}\cdot dl = E_{pA} - E_{pB}
$$
取$B$为电势0点，即$E_{pB} = 0$，那么有
$$
E_{pA} = q0\int_A^0\vec{E}\cdot dl = W_{A0}
$$
$A$点的电势能等于把该点电荷从$A$处移到电势0点过程中静电场力做的功

电势：
$$
V_A = \int_A^B\vec{E}\cdot dl + V_B
$$
通常选无穷远为电势0点，那么
$$
V_A = \int_A^{\infty}\vec{E}\cdot dl
$$
电势差：
$$
U_{AB} = V_A - V_B = \int_A^B\vec{E}\cdot dl = \frac{W_{AB}}{q}
$$
点电荷电场的电势：
$$
V = \int_r^{\infty} \vec{E}\cdot dl = \frac{1}{4\pi\varepsilon_0}\cdot\frac{Q}{r}
$$
电势叠加原理：多个点电荷的系统在某点激发的电势等于各个点电势在该处产生电势的代数和

***以下给出导出结论：***

1. 均匀带电圆环：

   带电量为$q$，半径为$R$

   轴线上距离圆心$x$处的电势:
   $$
   V_P = \frac{1}{4\pi\varepsilon_0}\cdot\frac{q}{\sqrt{(x^2+R^2)}}
   $$

2. 均匀带电薄圆环平面：

   切成许多的小圆环
   $$
   V_P = \frac{\sigma}{2\varepsilon_0}(\sqrt{x^2+R^2}-x)
   $$
   当$x>>R$时近似为点电荷的电势

3. 均匀带电球面：

   带电量为$Q$，半径为$R$

   1. 内部场强为0，因此是等势体，$V_{面内} = V_{面上} =  \frac{1}{4\pi\varepsilon_0}\cdot\frac{Q}{R}$
   2. 外部等同与点电荷电场在$r$处的电势$V = \frac{1}{4\pi\varepsilon_0}\cdot\frac{Q}{r}$

   如果球面套球面，两个球壳那也是叠加原理

### 电场强度和电势梯度

$$
\vec{E} = -\frac{dV}{dl}\cdot\vec{e_n} = -grad V = -\grad V
$$

$\vec{E}$的方向由高电势指向低电势，$\vec{e_n}$方向为电势增加的方向，分量式偏导数也正确

### 其余结论

1. 电偶极子静电场$xoy$面中任意一点$P$的电场强度和电势

   点$P$到电偶极子中点的距离为$r$，$\vec{OP}$和$r_0$夹角为$\theta$，当$r>>r_0$时
   $$
   V \approx \frac{1}{4\pi\varepsilon_0}\cdot\frac{qr_0cos\theta}{r^2} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{pcos\theta}{r^2} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{prcos\theta}{r^3} = \frac{1}{4\pi\varepsilon_0}\cdot\frac{px}{(x^2+y^2)^{\frac{3}{2}}}
   $$

   $$
   \vec{E} = -\grad V
   $$

   $$
   E = |\vec{E}| = \sqrt{E_x^2+E_y^2}
   $$

   当$x=0|\theta=0$或者$y=0|\theta=\frac{\pi}{2}$时，两种情况$E$算出来和电场强度矢量叠加原理算出来是一样的。

### 静电场中的电偶极子

匀强电场中的电偶极子：仅发生转动
$$
\vec{M} = \vec{p}\times\vec{E}
$$

$$
\vec{F} = 0
$$

如果是非匀强磁场则会转动和移动

#  

## Charpter 6 静电场中的导体和电介质

### 静电场中的导体

1. 导体会静电平衡，处于静电平衡状态

2. 导体内部$\vec{E} = 0$，$U_{AB} = \int_A^B\vec{E}\cdot dl = 0$，导体为等势体（包括表面和内部）

3. 导体表面的$\vec{E}$永远垂直表面

4. 由高斯定理得，导体内部没有净电荷，净电荷只能分布在表面上。如果导体内部有空腔也是一样，空腔内表面不会有任何形式的电荷分布（仅考虑空腔内没有电荷的情况）

5. 某点处场强和电荷面密度的关系：
   $$
   \oint\vec{E}\cdot d\vec{S} = E\cdot\Delta S = \frac{\sigma\Delta S}{\varepsilon_0}\ \ \ \Rightarrow\ \ \ E = \frac{\sigma}{\varepsilon_0}
   $$

6. 曲率半径越小的地方$E$越大

### 静电屏蔽

1. 空腔内电荷和内表面电荷在外部的合电势、合场强均为0
2. 外部电荷和外表面电荷在内部的合电势、合场强也均为0
3. 总结来说就是外部电场不受内部电场影响，内部电场也不受外部影响
4. 如果空腔导体接地，那么唯一结论是导体电势为0，接地可以用来屏蔽空腔内的电场

### 静电场中的电介质

1. 电介质相对电容率：$\varepsilon_r$
2. 真空电容率：$\varepsilon_0$
3. 电容率：$\varepsilon = \varepsilon_0\varepsilon_r$

### 电极化强度

单位体积分子电偶极矩矢量和
$$
P = \frac{\sum\vec{p}}{\Delta V}
$$
如果各处$P$都一样则称均匀极化

*两平行平板之间的电介质的电极化强度大小数值上等于电介质表面极化电荷面密度*

各向同性电介质中电极化强度和电场强度的关系：
$$
\vec{P} = (\varepsilon_r-1)\varepsilon_0\vec{E} = \chi_e\varepsilon_0\vec{E}
$$
其中$\chi_e = \varepsilon_r-1$为电极化率

### 电位移和有电介质的高斯定理

$$
\oint_S \varepsilon_r\vec{E}\cdot d\vec{S} = \frac{1}{\varepsilon_0}\sum q^{in}\\
if\ let\ D = \varepsilon_0\varepsilon_r\vec{E} = \varepsilon\vec{E}\ then:\\
\oint\vec{D}\cdot d\vec{S} = \sum q_{in}
$$

$\vec{D}$称为电位移，$\oint_S\vec{D}\cdot d\vec{S}$称为电位移通量，而$\oint_S\vec{E}\cdot d\vec{S}$称为电通量

### 电介质中 电场强度$\vec{E}$ 电极化强度$\vec{P}$ 电位移$\vec{D}$ 之间的关系

$$
D = \varepsilon_0\varepsilon_r\vec{E} = \varepsilon\vec{E}\\
\vec{P} = (\varepsilon_r-1)\varepsilon_0\vec{E} = \chi_e\varepsilon_0\vec{E}\\
\Rightarrow\\
\vec{D} = \vec{P}+\varepsilon_0\vec{E}
$$



### 电容与电容器

孤立导体的电容$C = \frac{Q}{V}$，因此真空中的球形导体$C = 4\pi\varepsilon_0R$

两个带电量等值异号的导体，电容$C = \frac{Q}{U} = \frac{Q}{V_1-V_2}$，$U = V_1-V_2 = \int_l\vec{E}\cdot dl$

***由定义式导出结论：***

1. 平行板电容器
   $$
   C = \frac{Q}{U} = \frac{\varepsilon_0\varepsilon_rS}{d}
   $$

2. 两同轴圆柱面构成的圆柱形电容器
   $$
   C = \frac{Q}{U} = \frac{2\pi\varepsilon_0\varepsilon_rl}{ln\frac{R_2}{R_1}}
   $$
   其中$R_1<R_2$，$l$为圆柱面长度

   当$R_2-R_1 << R_1$时
   $$
   C \approx \frac{2\pi\varepsilon_0\varepsilon_rlR_1}{d} = \frac{\varepsilon_0\varepsilon_rS}{d}
   $$
   近似平行板电容器

3. 两同心球面构成的球形电容器
   $$
   C = \frac{Q}{U} = 4\pi\varepsilon_0(\frac{R_2R_1}{R_2-R_1})
   $$
   其中$R_1<R_2$，当$R_2-R_1 << R_1$，且$R_2\rightarrow\infty$时，则有：
   $$
   C \approx 4\pi\varepsilon_0R_2
   $$
   近似球形孤立导体电容

4. 两根平行长直导线单位长度的电容

   两根之间的距离为$d$，每一根横截面半径为$R$，线密度的绝对值为$\lambda$
   $$
   C_l = \frac{\lambda}{U} \approx \frac{\pi\varepsilon_0}{ln\frac{d}{R}}
   $$

电容器的串并联：

1. 串联公式和电阻并联公式一样
2. 并联公式和电阻串联公式一样



### 静电场的能量

电容器存储的电能：
$$
W_e = \frac{1}{2}\frac{Q^2}{C} = \frac{1}{2}QU = \frac{1}{2}CU^2
$$
如果是平板电容器，
$$
W_e = \frac{1}{2}CU^2 = \frac{1}{2}\frac{\varepsilon_0\varepsilon_rS}{d}(Ed)^2  =\frac{1}{2}\varepsilon E^2Sd
$$
电场的能量密度：单位体积电场所具有的电场能量
$$
w_e = \frac{W_E}{\Delta V} = \frac{1}{2}\varepsilon E^2
$$















