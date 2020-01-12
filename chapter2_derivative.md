# 第二章 导数与微积分

## 引例

1. 我们已经一辆汽车在一段时间（t）内行驶的路程（s），我们很快就能知道它在这段时间内的平均速度： $\bar{v} = \dfrac{s}{t}$。

    但是，如果我们想知道它在某一特定时刻的速度（例如，汽车启动后第5s的速度），那我们该如何计算？  

    我们可以取第5s-第5.00001s汽车所行驶的路程，然后通过速度公式，我们就可以近似地得到汽车在第5s时的速度。当我们取时间间隔也小，所得出的速度就越接近汽车的瞬时速度。  

    将以上方法翻译成数学的语言就是：  

    $$v = \dfrac{\Delta s}{\Delta t}  \;\;\;(when \;\;\Delta t \rightarrow 0)$$

    

2. 如果我们已知一个函数的图像，我们想知道它在某一点（P）处的切线斜率(slope)，我们该怎么计算？

    我们可以在函数图像上再取一点（Q），这样我们可以知道割线PQ（secant）的斜率。我们可以固定P，让Q点不断地接近P点，这样算出的结果可以认为是函数再P点处的切线斜率。  

    ![1578718552168](D:\markdown笔记\calculus_tongji\images\1_secant.png)

## 导数的定义

由上面两个引例我们可以知道，对于求速度或者是函数的斜率都可以归结成极限问题。由此引出导数的定义：  

$$f^{'}(x) = \lim\limits_{\Delta x \to 0} \dfrac{\Delta y}{\Delta x} = \lim\limits_{\Delta x \to 0} \dfrac{f(x + \Delta x) - f(x)}{\Delta x}$$

其他形式有：  $f^{'}(x) = \lim\limits_{h \to 0} \dfrac{f(x + h) - f(x)}{h}$

（从几何角度上看，导数就是函数在某一点处切线的斜率。从物理角度上看，导数可以是瞬时速度，电流等物理量。关键是理解导数的意义：瞬时变化率）

![1578729426872](D:\markdown笔记\calculus_tongji\images\2——！.png)

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

![1578730695033](D:\markdown笔记\calculus_tongji\images\2——3.png)





定义：函数f(x)在$x_0$处的**无定义**， 但$\lim\limits_{x \to x_0^+}f(x) = \lim\limits_{x \to x_0^-}f(x)$。

例如：$\dfrac{sinx}{x}$在x=0处，无定义，但是$\lim\limits_{x \to x_0} \dfrac{sinx}{x} = 0$



#### 跳跃间断点(Dump Discontinuity)

![1578731004463](D:\markdown笔记\calculus_tongji\images\2——4.png)

定义：函数f(x)在$x_0$处存在$\lim\limits_{x \to x_0^+}f(x) , \; \lim\limits_{x \to x_0^-}f(x)$， 但$\lim\limits_{x \to x_0^+}f(x) \ne \lim\limits_{x \to x_0^-}f(x)$



#### 无穷间断点

![1578731109919](D:\markdown笔记\calculus_tongji\images\2——5.png)

$\lim\limits_{x \to x_0^+}f(x) =\infty, \;\; \lim\limits_{x \to x_0^-}f(x) = \infty$

#### 其他类型的间断点(Other Discontinuity)

![1578731227213](D:\markdown笔记\calculus_tongji\images\1——6.png)

### 两个三角极限的证明

$\lim\limits_{\theta \to 0} \dfrac{sin\theta}{\theta} = 1 ; \;\;\;\lim\limits_{\theta \to 0} \dfrac{1 - cos\theta}{\theta} = 0$

$其中，\theta为弧度而不是角度$

![1578731416820](D:\markdown笔记\calculus_tongji\images\1-7.png)

![1578731449464](D:\markdown笔记\calculus_tongji\images\1-8.png)





由上图可以看出当$\theta \to 0$时，$sin\theta \to \theta$，证明完毕。  





![1578731534613](D:\markdown笔记\calculus_tongji\images\1-9.png)



![1578731569144](D:\markdown笔记\calculus_tongji\images\2-10.png)





由上图，我们可以看出$\theta \to 0$时，$1 - cos\theta \to 0$， 但是$1 - cos\theta \to 0$的速度比$\theta \to 0$还要快，证明完毕。

### 可导一定连续，连续不一定可导



![1578730409729](D:\markdown笔记\calculus_tongji\images\2——2.png)





## 函数的求导法则

### 函数的和，差，积，商的求导法则。

![1578732035282](D:\markdown笔记\calculus_tongji\images\2-11.png)



![1578732983816](D:\markdown笔记\calculus_tongji\images\2-21.png)



![1578733021959](D:\markdown笔记\calculus_tongji\images\2-23.png)

乘积求导的几何解释：  

![1578733088400](D:\markdown笔记\calculus_tongji\images\2-24.png)

$\Delta uv$为最外面的矩形面积减去里面橙色矩形的面积。

由图我们可以得到$\Delta (uv) = u\Delta v + v\Delta u + \Delta u \Delta v$。当$\Delta u, \Delta v \to 0 $时，$\Delta u\Delta v$相比于$u\Delta v, v\Delta u$更微不足道，所以化简得$\Delta (uv) = u\Delta v + v\Delta u $



例子: 

![1578733584555](D:\markdown笔记\calculus_tongji\images\2-25.png)