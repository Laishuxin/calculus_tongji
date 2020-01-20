# 第二章 导数与微积分

## 引例

1. 我们已经一辆汽车在一段时间（t）内行驶的路程（s），我们很快就能知道它在这段时间内的平均速度： $\bar{v} = \dfrac{s}{t}$。

    但是，如果我们想知道它在某一特定时刻的速度（例如，汽车启动后第5s的速度），那我们该如何计算？  

    我们可以取第5s-第5.00001s汽车所行驶的路程，然后通过速度公式，我们就可以近似地得到汽车在第5s时的速度。当我们取时间间隔也小，所得出的速度就越接近汽车的瞬时速度。  

    将以上方法翻译成数学的语言就是：  

    $$v = \dfrac{\Delta s}{\Delta t}  \;\;\;(when \;\;\Delta t \rightarrow 0)$$

    

2. 如果我们已知一个函数的图像，我们想知道它在某一点（P）处的切线斜率(slope)，我们该怎么计算？

    我们可以在函数图像上再取一点（Q），这样我们可以知道割线PQ（secant）的斜率。我们可以固定P，让Q点不断地接近P点，这样算出的结果可以认为是函数再P点处的切线斜率。  

    ![1578718552168](images\1_secant.png)

## 导数的定义

由上面两个引例我们可以知道，对于求速度或者是函数的斜率都可以归结成极限问题。由此引出导数的定义：  

$$f^{'}(x) = \lim\limits_{\Delta x \to 0} \dfrac{\Delta y}{\Delta x} = \lim\limits_{\Delta x \to 0} \dfrac{f(x + \Delta x) - f(x)}{\Delta x}$$

其他形式有：  $f^{'}(x) = \lim\limits_{h \to 0} \dfrac{f(x + h) - f(x)}{h}$

（从几何角度上看，导数就是函数在某一点处切线的斜率。从物理角度上看，导数可以是瞬时速度，电流等物理量。关键是理解导数的意义：瞬时变化率）

![1578729426872](images\2——！.png)

### 单侧导数

左导数： $f^{'}_{-}(x) = \lim\limits_{h \to 0^-} \dfrac{f(x + h) - f(x)}{h}$

右导数： $f^{'}_{+}(x) = \lim\limits_{h \to 0^+} \dfrac{f(x + h) - f(x)}{h}$

函数在某一点可导的等价条件：函数在该点处的左导数和右导数存在且相等。

函数f(x)在区间[a, b]可导的条件：函数f(x)在(a, b)可导，且$f^{'}_+(a), f^{'}_-(b)$存在。



## 函数可导与连续的关系

### 函数连续的定义

函数f(x)在$x_0$处连续(continuous):  

$$\lim\limits_{x \to x_0} f(x) = f(x_0)$$

如果不满足上面的公式，我们就称函数在$x_0$处不连续。

### 函数不连续的常见形式

#### 可去间断点(Removable Discontinuity)

![1578730695033](images\2——3.png)





定义：函数f(x)在$x_0$处的**无定义**， 但$\lim\limits_{x \to x_0^+}f(x) = \lim\limits_{x \to x_0^-}f(x)$。

例如：$\dfrac{sinx}{x}$在x=0处，无定义，但是$\lim\limits_{x \to x_0} \dfrac{sinx}{x} = 0$



#### 跳跃间断点(Dump Discontinuity)

![1578731004463](images\2——4.png)

定义：函数f(x)在$x_0$处存在$\lim\limits_{x \to x_0^+}f(x) , \; \lim\limits_{x \to x_0^-}f(x)$， 但$\lim\limits_{x \to x_0^+}f(x) \ne \lim\limits_{x \to x_0^-}f(x)$



#### 无穷间断点

![1578731109919](images\2——5.png)

$\lim\limits_{x \to x_0^+}f(x) =\infty, \;\; \lim\limits_{x \to x_0^-}f(x) = \infty$

#### 其他类型的间断点(Other Discontinuity)

![1578731227213](images\1——6.png)

### 两个三角极限的证明

$\lim\limits_{\theta \to 0} \dfrac{sin\theta}{\theta} = 1 ; \;\;\;\lim\limits_{\theta \to 0} \dfrac{1 - cos\theta}{\theta} = 0$

$其中，\theta为弧度而不是角度$

![1578731416820](images\1-7.png)

![1578731449464](images\1-8.png)





由上图可以看出当$\theta \to 0$时，$sin\theta \to \theta$，证明完毕。  





![1578731534613](images\1-9.png)



![1578731569144](images\2-10.png)





由上图，我们可以看出$\theta \to 0$时，$1 - cos\theta \to 0$， 但是$1 - cos\theta \to 0$的速度比$\theta \to 0$还要快，证明完毕。

### 可导一定连续，连续不一定可导



![1578730409729](images\2——2.png)





## 函数的求导法则

### 函数的和，差，积，商的求导法则。

![1578732035282](images\2-11.png)



![1578732983816](images\2-21.png)



![1578733021959](images\2-23.png)

乘积求导的几何解释：  

![1578733088400](images\2-24.png)

$\Delta uv$为最外面的矩形面积减去里面橙色矩形的面积。

由图我们可以得到$\Delta (uv) = u\Delta v + v\Delta u + \Delta u \Delta v$。当$\Delta u, \Delta v \to 0 $时，$\Delta u\Delta v$相比于$u\Delta v, v\Delta u$更微不足道，所以化简得$\Delta (uv) = u\Delta v + v\Delta u $



例子: 

![1578733584555](images\2-25.png)



### 复合函数求导法则（Chain Rule）

如果u = g(x) 在点x处可导，而f(u) 在u = g(x)可导，那么复合函数f[g(x)] 在点x处可导，其导数为：

$$\dfrac{dy}{dx} = f^{'}(u) \times g^{'}(x) 或\dfrac{dy}{dx} = \dfrac{dy}{du}·\dfrac{du}{dx}$$



![1578812250779](images\2-22.png)



相关例题：  

![1578812291397](images\2-27.png)

![1578812360382](images\2-32.png)

### 反函数求导法则

##### 反函数(inverse function):

形如，y = f(x), g(y) = x的函数。

($x = g(y) = f^{-1}(y)$)

##### 反函数的性质

关于y=x对称。

![1578814266546](images\152-46.png)

##### 反函数的导数

如果函数x = f(y) 在区间$I_y$内单调、可导且$f^{'}(y) \ne 0$，那么它的反函数$y = f^{-1}(x)$在区间$I_x = \{x|x=f(y), y∈I_y\}$内也可导，且$[f^{-1}(x)]^{'} = \dfrac{1}{f^{'}(y)} 或 \dfrac{dy}{dx} = \dfrac{1}{\dfrac{dx}{dy}}$

证明：

$$y = f(x) \\ f^{-1}(y) = x \\  \dfrac{d}{dx}(f^{-1}(y)) = \dfrac{d}{dx}x = 1 \\chain rule: \dfrac{d}{dy}(f^{-1}(y))\dfrac{dy}{dx} = 1  \\ \dfrac{d}{dy}f^{-1}(y) = \dfrac{1}{\dfrac{dy}{dx}}$$

**简而言之：反函数的导数 = 1/原函数的导数**

##### 相关例子

example 1:

求y = arctan(x)的导数。

![1578813732022](images\2-022.png)

![1578813851704](images\2-、04.png)

example 2：

求y = arcsinx 导数

![1578814167096](images\2-96.png)





### 高阶导数(Higher derivatives)

![1578814759108](images\2-08.png)

Example 2:

求出 y = sin x 的n阶导数。

$$y = sinx\\y^{(1)} = cosx = sin(x + 1\times\dfrac{\pi}{2})\\ y^{(2)} = -sinx = sin(x + 2\times\dfrac{\pi}{2})\\y^{(3)} = -cosx = sin(x + 3\times\dfrac{\pi}{2})\\y^{(4)} = sinx = sin(x + 4\times\dfrac{\pi}{2})\\\cdots\\y^{(n)} = sin(x + n\times\dfrac{\pi}{2})$$



Example 3:

求出$y = \ln\dfrac{1}{1+x}$的n阶导数。

$$y^{(1)} = \dfrac{1}{1+x} = \dfrac{(-1)^0·0!}{(1+x)^1}\\y^{(2)} = -\dfrac{1}{(1+x)^2} = \dfrac{(-1)^1·1!}{(1+x)^2}\\y^{(3)} = \dfrac{2}{(1+x)^3} = \dfrac{(-1)^2·2!}{(1+x)^3}\\y^{(4)} = -\dfrac{6}{(1+x)^4} = \dfrac{(-1)^3·3!}{(1+x)^4}\\ \cdots\\y^{(n)} = \dfrac{(-1)^{(n-1)}·(n-1)!}{(1+x)^n}$$



##### 和、乘积公式

和公式： $(u±v)^{(n)} = u^{(n)} ± v^{(n)}$   

乘积公式：(类似于二项式展开)$(uv)^{(n)} = u^{(n)}v + nu^{(n-1)}v^{(1)} + \dfrac{n(n-1)}{2!}u^{(n-2)}v^{(2)} + \cdots+\dfrac{n(n-1)\cdots(n-k+1)}{k!}u^{(n-k)}v^{(k)} + \cdots + uv^{(n)}$



### 隐函数求导(Implicit Derivatives)

隐函数求导的原理是chain rule

例如：求出$x = e^y$的导数$\dfrac{dy}{dx}$  

$$两边同时对x求导数: \\ \dfrac{d}{dx}x = \dfrac{d}{dx}e^y \\1 = \dfrac{d}{dy}e^y\dfrac{dy}{dx}\\ 1 = e^y\dfrac{dy}{dx}\\ \dfrac{dy}{dx} = e^{-y}$$



##### 相关例子：

Example 1:  

求$y = x^{\frac{m}{n}}$的导数

$$y^n = x^m\\ ny^{n-1}\dfrac{dy}{dx} = mx^{m-1}\\ \dfrac{dy}{dx} = \dfrac{m}{n}\dfrac{x^{m-1}}{y^{n-1}}$$

![1578816933547](images\2-47.png)

##### 参数方程的求导。

已知：

$$f(x) = \begin{cases}x= \varphi(t),\\y = \psi(t)\end{cases}$$

求 $\dfrac{dy}{dx}$

$$\dfrac{dy}{dx} = \dfrac{dy}{dt}\dfrac{dt}{dx} = \dfrac{dy}{dx}·\dfrac{1}{\dfrac{dx}{dt}} = \dfrac{\psi^{’}(t)}{\varphi^{'}(t)}$$

$$\dfrac{d}{dx}(\dfrac{dy}{dx}) = \dfrac{d}{dt}(\dfrac{\psi^{'}(t)}{\varphi^{'}(t)})·\dfrac{dt}{dx} = \dfrac{d}{dt}(\dfrac{\psi^{'}(t)}{\varphi^{'}(t)})·\dfrac{1}{\varphi^{'}(t)}$$



### 指数，对数求导以及双曲函数

(Exponential and Log, Logarithmic Differentiation, Hyperbolic Functions )

##### 引例：求出$\dfrac{d}{dx}a^x$

由定义可得：

$\dfrac{d}{dx}a^x = \lim\limits_{\Delta x \to 0}\dfrac{a^{x+\Delta x} - a^x}{\Delta x} = a^x\lim\limits_{\Delta x \to 0}\dfrac{a^{\Delta x} - 1}{\Delta x}$

Let:  

$M(a) \equiv \lim\limits_{\Delta x \to 0}\dfrac{a^{\Delta x} - 1}{\Delta x}$

so:

$\dfrac{d}{dx}a^x = a^xM(a)$

but, we don't yet know what $M(a)$ is.

Indeed,

$M(a) = \lim\limits_{\Delta x \to 0}\dfrac{a^{\Delta x} - 1}{\Delta x} = \lim\limits_{\Delta x \to 0}\dfrac{a^{0+\Delta x} - a^0}{\Delta x} = \dfrac{d}{dx}a^x|_{x=0}$

Geometrically, M(a) is the slope of the graph $y =a^x$ at x=0.

We define a natural number **e** which satisfies $M(e) = 1$.

How we to find the number of **e**.

We can notice that when the base *a* is increase, the graph $a^x$ gets steeper.  

so we can increase the base *a* slowly until we find **M(a) = 1**



 

<img src="images\2-183.png" alt="1578820535183" style="zoom: 50%;" />

<img src="images\2-93.png" alt="1578820548793" style="zoom:50%;" />

<img src="images\2-668.png" alt="1578820561668" style="zoom:50%;" />



Thus:

$M(e) = 1$

$M(e) = \lim\limits_{h \to 0}\dfrac{e^h - 1}{h } =1$

or,

$\dfrac{d}{dx}(e^x) = 1 \; at \;x= 1$

so,

$\dfrac{d}{dx}e^x = e^x$

rewrite $a^x$,

$a^x = e^{xlna}$

so,

$\dfrac{d}{dx} a^x = \dfrac{d}{dx}e^{xlna} = lna·e^{xlna} = a^xlna$

##### 对数微分法

如果我们想算出$\dfrac{d}{dx}f(x)$，我们可以先通过算出$\dfrac{d}{dx}ln(f(x))$，具体步骤如下：  

让，$u = f(x)$

则，$\dfrac{d}{dx}ln(u) = \dfrac{dln(u)}{du}\dfrac{du}{dx} = \dfrac{1}{u}(\dfrac{du}{dx})$

因为，$u = f, \dfrac{du}{dx} = f^{'}$

所以，$(lnf)^{'} = \dfrac{f^{‘}}{f} \Rightarrow f^{'} = f(lnf)^{'}$

##### 相关例子

![1578821400747](images\2-147.png)

![1578821529936](images\2-36.png)

![1578821542724](images\2-44.png)

##### 双曲函数（hyperbolic function）

双曲正弦(hyperbolic sine)： $sinh(x) = \dfrac{e^x - e^{-x}}{2}$

双曲余弦(hyperbolic cosine)：$cosh(x) = \dfrac{e^x  + e^{-x}}{2}$ 

$\dfrac{d}{dx}sinh(x) = cosh(x)$

$\dfrac{d}{dx}cosh(x) = sinh(x)$

重要等式：

$sinh^2(x) + cosh^2(x) = 1$



## 函数的微分

##### 定义：  

设函数$y = f(x)$在某区间内有定义，$x_0$以及$x_0 +\Delta x$在该区间内，如果函数的增量:$\Delta y = f(x_0+\Delta x) - f(x_0)$可表示为$\Delta y = A\Delta x + o(\Delta x)$, 其中A 为不依赖于$\Delta x$的常数，则称函数y = f(x)在$x_0$处可微，$A\Delta x$叫做函数y=f(x)在$x_0$处的微分，记作：$dy = A\Delta x$ 



##### 可微于可导是关系

由$\dfrac{\Delta y}{\Delta x} = A + \dfrac{o(\Delta x)}{\Delta x}$

得$A = \lim\limits_{\Delta x \to 0}\dfrac{\Delta y}{\Delta x}  = f^{'}(x)$

所以，可微一定可导。

由极限与无穷小的关系得：

$\dfrac{\Delta y}{\Delta x} = f^{'}(x) +\alpha$，其中，$\alpha \to 0 \;\; when \;\Delta x \to 0$

$\Delta y = f^{'}(x)\Delta x + \alpha \Delta x$

由于$f^{'}(x)$不依赖于$\Delta x $， 

所以，可导也是可微。  

综上，可导$\Leftrightarrow$可微

##### 微分的几何意义

![1578899947971](images\2-971.png)



##### 微分公式以及微分运算法则

函数的微分表达式：$dy = f^{'}(x)dx$

运算法则与导数运算法则一致(和、积、商、链式法则等)，只需把导数换成微分形式。

##### 微分在计算上的近似应用

1. 线性近似

    ![1578965847184](images\2-84.png)

    由图像可知，我们想计算函数在某一点的值，我们可以用函数在该点的切线近似。通过点斜式，我们可以得到近似公式为：$f(x) ≈ f(x_0) + f^{'}(x_0)(x - x_0)$

    相关例子：

    Example 1: $f(x) = lnx ,\;\; x_0=1(basepoint)$

    $f(x) = 0,\;\;f^{'}(1) = \dfrac{1}{x}|_{x=1} = 1$  

    $lnx ≈ f(1) + f^{'}(1)(x -1) = 0 + 1(x-1) = x- 1$  

    如果我们改变基点：

    $x = 1 +\mu \;\;\; u = x- 1$

    $ln(1 + u ) = u$

    

​		线性近似列表：（在$x_0 = 0, \;\;|x|<<1$时的近似）

​		$sinx ≈ x\\cosx ≈ 1\\e^x ≈ 1+x\\ln(1+x)≈x\\(1+x)^r≈1 +rx$ 

​		![1578967502112](images\2-112.png)



​		Example 2:

​		Find the linear approximation of $f(x) = \dfrac{e^{-2x}}{\sqrt{1+ x}} ;\;near\; x=0$

​		由上述可得$e^{-2x} ≈ 1 + (-2x) = 1-2x$

​		$\sqrt{1+x} ≈ 1 + \frac{1}{2}x$

​		把两个近似公式结合在一起可以得到：

​		$\dfrac{e^{-2x}}{\sqrt{1+ x}} ≈ (1 - 2x)(1 + \frac{1}{2}x)^{-1}$			

​		而$(1 + \frac{1}{2}x)^{-1}≈ 1 - \frac{1}{2}x$

​		从而得到：$\dfrac{e^{-2x}}{\sqrt{1+ x}} ≈ (1 - 2x)(1 - \frac{1}{2}x) = 1 - \frac{5}{2}x + \frac{1}{2}x^2$

​		忽视高阶无穷小量$x^2$ ，得到最终结果为

​		$\dfrac{e^{-2x}}{\sqrt{1+ x}} ≈ 1- \frac{5}{2} x$

​		

​		Example 3: 计算$\lim\limits_{x \to 0} \dfrac{(1 + 2x)^{10} -1}{x}$

​		way1:

​			$\lim\limits_{x \to 0} \dfrac{(1 + 2x)^{10} -1}{x} = \lim\limits_{x \to 0} \dfrac{(1 + 2x)^{10} -(1 + 2·0)^{10}}{x -0 } = 20(1 + 2x)|_{x=0} = 20$

​		way2:

​			由于$(1+2x)^{10} ≈ 1 + 10(2x) = 1+ 20x$，代入可以得

​			$\lim\limits_{x \to 0} \dfrac{(1 + 2x)^{10} -1}{x} = \lim\limits_{x \to 0} \dfrac{1 + 20x -1}{x} = 20$



2. 二项式近似(quadratic approximation)

    $f(x) ≈ f(x_0) + f^{’}(x_0)(x - x_0) + \dfrac{f^{‘’}(x_0)}{2}(x - x_0)^2\;\;\;x≈x_0$

    二项式近似列表($x ≈ 0,\;\;|x|<<1$)

    ![1578969049195](images\2-195.png)

##### 误差估计

如果某个量的精确值(测量值)为A， 它的近似值为$\mu$，则，

绝对误差：$|A - \mu|$  

相对误差：$|\dfrac{A - \mu}{\mu}| \le \delta_A$， 其中$\delta_A$为误差上限



Example 1:

设测得圆钢截面的直径$D = 60.03mm$， 测量D的绝对误差限$\delta_D = 0.05mm$。利用公式$A = \dfrac{\pi}{4}D^2$计算圆钢的截面积时，试估计面积差时的误差。



如果我们把测量D时产生的误差记作$\Delta D$，利用公式$A = \dfrac{\pi}{4}D^2$产生的误差记作$\Delta A$，则当$|\Delta D|$很小时，$\Delta A$可用$dA$近似替代，即：$\Delta A ≈ dy = \dfrac{\pi}{2}D\Delta D$

由于$|\Delta D | \le \delta_D = 0.05$

而$\Delta A ≈ dy = \dfrac{\pi}{2}D\Delta D \le\dfrac{\pi}{2}D·\delta_D $

从而得到：$\delta_A = \dfrac{\pi}{2} ·60.03·0.05 ≈ 4.712$

A的相对误差为：$\dfrac{\delta_A}{A} = \dfrac{\dfrac{\pi}{2}D\Delta D}{\dfrac{\pi}{4} D^2}= 2·\dfrac{\delta_D}{d} = 2·\dfrac{0.05}{60.03}$