# 第三章 微分中值定理与导数的应用

## 微分中值定理(Mean Value Theorem MVT)



引入费马引理：

(费马引理的大概思想为：对于函数上的可导并存在定义的某一点，若该点是极值点，则其导数等于0)

![1579528759588](D:\markdown笔记\calculus_tongji\images\3-8.png)

证明：  

设$x \in U(x_0)$时, $f(x) \le f(x_0)$ 

则$f(x) - f(x_0)\le 0  $

当$x > x_0 $时， $\dfrac{f(x) - f(x_0)}{x - x_0} \le 0$  

当$x < x_0 $时， $\dfrac{f(x) - f(x_0) }{x - x_0} \ge 0$

由极限局部保号性得：

$f_{-}^{'}(x_0) = \lim\limits_{x \to x_0^-} \dfrac{f(x) - f(x_0)}{x - x_0} \geq 0$

$f_{+}^{'}(x_0) = \lim\limits_{x \to x_0^+} \dfrac{f(x) - f(x_0)}{x - x_0} \leq 0$

由于函数的在$x_0$处的极限$f^{'}(x_0) = \lim\limits_{x \to x_0} \dfrac{f(x) - f(x_0)}{x - x_0}$存在

所以$f^{'}(x_0) = 0$

证明完毕。



**NOTE:** 

1. 导数等于0的点也称作驻点(stationary point)

2.  若函数在区间(不算区间端点)内取得最大值或者最小值，则函数在该点处的导数为0。
3. 导数为0不一定能推导出函数是该店的最大最小值，也不一定能推出极大极小值。(例如$y = x^3$)



### 罗尔(Rolle)中值定理

![1579529921610](D:\markdown笔记\calculus_tongji\images\3-610.png)

#### 证明

1. 当M=m时，即最大值等于最小值。则该函数为常数函数，即$f^{'}(x) = 0$， 所以必然存在$\xi \in(a, b)$，使得$f^{‘}(\xi) = 0$.

2. 当$M>m$时，即最大值不等于最小值。

    由于在区间端点处有$f(a) = f(b)$，所以M,m中至少有一个值不是在区间端点取得

    假设最大值M不是在区间端点处取得，即$f(a) \neq M$，则$\exists \xi \in(a, b)，使f(\xi) = M$, 

    即，$\forall x \in [a, b], f(x) \leq f(\xi)$，由费马引理得: $f(\xi)= 0$

    证明完毕。



**Note : **如果不满足定理的所有条件的函数，定理的结论不一定成立。例如：

![1579530626106](D:\markdown笔记\calculus_tongji\images\3-6.png)

![1579530638361](D:\markdown笔记\calculus_tongji\images\3~61.png)

![1579530659342](D:\markdown笔记\calculus_tongji\images\3~42.png)

![1579530675587](D:\markdown笔记\calculus_tongji\images\3~87.png)

#### 例子

![1579530759145](D:\markdown笔记\calculus_tongji\images\3~9145.png)



### 拉格朗日(Largrange)中值定理

(拉格朗日中值定理是罗尔定理的推广，其大致思想是构造一个函数，使得该函数在端点处相等，然后利用罗尔定理得出新的结论)

![1579531152594](D:\markdown笔记\calculus_tongji\images\3~94.png)

![1579531233765](C:\Users\htwoo\AppData\Roaming\Typora\typora-user-images\1579531233765.png)

![1579531263317](D:\markdown笔记\calculus_tongji\images\3~263317.png)



#### 证明

![1579531418023](D:\markdown笔记\calculus_tongji\images\3~23.png)

1. 构造一个在区间端点相等的函数

    我们观察到有向线段MN在A,B处等于0，于是我们利用有向线段MN构造我们想要的函数。 

    设有向线段MN的函数为$\varphi(x)$， 题目所给的函数为$f(x)$， 弦AB的函数为$L(x)$。

    则$\varphi(x) = f(x) - L(x)$。

    由$L(x) = f(a) + \dfrac{f(b) - f(a)}{b -a}(x - a)$

    所以：$\varphi(x) = f(x) - L(x) = f(x) - f(a) - \dfrac{f(b) - f(a)}{b -a}(x - a)$

    验证：

    $\varphi(a) = f(a) - f(a) -\dfrac{f(b) - f(a)}{b -a}(a - a) = 0$

    $\varphi(b) = f(b) - f(a) - \dfrac{f(b) - f(a)}{b -a}(b - a) = 0$

    所以：$\varphi(a) = \varphi(b)$

2. 利用罗尔定理完成证明。

    我们很容易能知道$\varphi(x)$满足罗尔定理的条件：在$[a, b]$连续、在$(a, b)$可导，且$\varphi(a) = \varphi(b)$。

    则$\exists \;\xi \in(a, b), 使得\varphi(\xi) = 0$。

    由$\varphi^{'}(x) = f^{’}(x) - \dfrac{f(b) - f(a)}{b-a}$，

    则$\varphi^{‘}(\xi) = f^{’}(\xi) - \dfrac{f(b) - f(a)}{b-a} = 0$

    所以：$f(b) - f(a) = f^{‘}(\xi)(b- a)$

证明完毕。



拉格朗日的其他写法：  

设x为区间$[a, b]$上的一点，另一点为$x + \Delta x$，则有

在区间$[x, x+ \Delta x]$上，$f(x + \Delta x) - f(x) = f^{’}(x + \theta\Delta x)\Delta x \;\;(0<\theta<1)$

若记$y = f(x)$，则上面的式子可以变为$\Delta y = f^{‘}(x + \theta\Delta x) \Delta x \;\;(0<\theta<1)$

我们已知$dy = f^{’}(x)\Delta x$是$\Delta y$的近似表达式，需要满足$\Delta x \to 0$。

但是上面式子的$\Delta y $可以是精确计算公式。  



#### 推论

![1579532979425](D:\markdown笔记\calculus_tongji\images\3~79425.png)

#### 例子

![1579533081485](D:\markdown笔记\calculus_tongji\images\3~1579533081485.png)



### 柯西(Cauchy)中值定理

（柯西中值定理的原理与拉格朗日相似，构造一个辅助函数，使得在该函数在端点处的函数值相等，再利用罗尔定理得出结论，只是柯西中值定理试用于两个函数)

![1579568626954](D:\markdown笔记\calculus_tongji\images\3~1579568626954.png)

![1579568639729](D:\markdown笔记\calculus_tongji\images\3~1579568639729.png)

![1579568690750](D:\markdown笔记\calculus_tongji\images\3~1579568690750.png)

#### 证明

1. 先对结论进行变换

    由$\dfrac{f(b) -f(a)}{F(b) - F(a)} = \dfrac{f^{’}(\xi)}{F^{‘}(\xi)}$

    得$f^{'}(\xi) - \dfrac{f(b) - f(a)}{F(b) - F(a)}F^{'}(\xi) = 0$

    构造辅助函数$\varphi(x) = f(x) - \dfrac{f(b) - f(a)}{F(b) - F(a)}F(x) = \dfrac{[F(b) -F(a)]f(x) - [f(b) -f(a)]F(x)}{F(b) - F(a)}$

    验证$\varphi(x)$在端点处相等：

    $\varphi(a) = \dfrac{[F(b) -F(a)]f(a) - [f(b) -f(a)]F(a)}{F(b) - F(a)} = \dfrac{f(a)F(b) - f(b)F(a)}{F(b) -F(a)}$

    $\varphi(b) = \dfrac{[F(b) -F(a)]f(b) - [f(b) -f(a)]F(b)}{F(b) - F(a)} = \dfrac{f(a)F(b) - f(b)F(a)}{F(b) -F(a)}$

    所以：$\varphi(a) = \varphi(b)$

2. 验没罗尔定理满足条件

    由拉格朗日中值定理得：$F(b) - F(a) = F^{’}(\eta)(b - a)$

    由于$F^{'}(x)\ne 0$，则$F(a) \ne F(b)$

    构造函数$\varphi(x) = f(x) - \dfrac{f(b) - f(a)}{F(b) - F(a)}F(x)$，在区间$[a, b]$连续， $(a, b)$可导，且$\varphi(a) = \varphi(b)$。

    由罗尔定理得：$\exists\;\xi \in (a, b), \;使\varphi^{‘}(\xi) = f^{’}(\xi) - \dfrac{f(b) - f(a)}{F(b) - F(a)}F^{‘}(\xi) = 0$

    所以，$\dfrac{f^{’}(\xi)}{F^{‘}(\xi)} = \dfrac{f(b) - f(a)}{F(b) - F(a)}$

证明完毕。

(当$F(x) = x$时，可以发现柯西中值定理就是拉格朗日中值定理)





#### 例子

![1579570010602](D:\markdown笔记\calculus_tongji\images\3~1579570010602.png)





## 洛必达法则(L' Hospital Rule)

![1579572135951](D:\markdown笔记\calculus_tongji\images\3~1579572135951.png)

(洛必达法则是为了解决未定式$\dfrac{0}{0}、\dfrac{\infty}{\infty}$而存在的)

### 证明：

由于$\lim\limits_{x \to a}\dfrac{f(x)}{g(x)}$与$f(a)、g(a)$无关，所以可以设$f(a) = g(a) = 0$ (或者说$f(x),g(x)$在x=a处无定义，或者本身就等于0)

1. 利用柯西定理证明

    我们设$f(a) = g(a) =0$后，可以得到$f(x), g(x)$在x=a处的某邻域内连续可导且$g^{’}(x)\ne 0$。

    由柯西中值定理得$\dfrac{f(x)}{g(x)} = \dfrac{f(x) - f(a)}{g(x) - g(a)} = \dfrac{f^{‘}(\xi)}{g^{’}(\xi)}$（其中，x为该邻域内一点）

    对两边取极限，即$x \to a时,\;\xi \to a$，所以有：  

    $\lim\limits_{x \to a} \dfrac{f(x)}{g(x)} = \lim\limits_{x \to a}\dfrac{f^{‘}(x)}{g^{’}(x)}$

2. 构造极限表达式证明

    $\lim\limits_{x \to a}\dfrac{f(x)}{g(x)} = \lim\limits_{x \to a}\dfrac{\dfrac{f(x) - f(a)}{x -a}}{\dfrac{g(x) - g(a)}{x - a}} = \dfrac{\lim\limits_{x \to a}\dfrac{f(x) - f(a)}{x -a}}{\lim\limits_{x \to a}\dfrac{g(x) - g(a)}{x - a}} = \lim\limits_{x \to a}\dfrac{f^{‘}(a)}{g^{'}(a)}$

3. 利用图像证明

    <img src="D:\markdown笔记\calculus_tongji\images\3~1579573800820.png" alt="1579573800820" style="zoom:67%;" />

    $\lim\limits_{ x\to a}\dfrac{f(x)}{g(x)}$的值就是函数$f(x)$与函数$g(x)$在x=a点处的比值，但是函数值在该点处等于0，无法直接比较，

    不过我们可以观察两个函数在无限接近于x=a点处的函数值微小变化量的比值。  

    所以，$\lim\limits_{ x\to a}\dfrac{f(x)}{g(x)} = \dfrac{\dfrac{df}{dx}(a) dx}{\dfrac{dg}{dx}(a)dx} = \dfrac{f^{’}(a)}{g^{‘}(a)}$

**NOTE:** 洛必达法则不仅适用于$x \to a$，也适用于其他情况。同时对于其他未定式($0·\infty、\infty -\infty、0^{\infty}...$)都可以通过变换转化成$\dfrac{0}{0}、\dfrac{\infty}{\infty}$型，在利用洛必达法则。  

### 例子

![1579574312768](D:\markdown笔记\calculus_tongji\images\3~1579574312768.png)

![1579574382686](D:\markdown笔记\calculus_tongji\images\3~1579574382686.png)

![1579574393803](D:\markdown笔记\calculus_tongji\images\3~1579574393803.png)

### 其他未定式例子

![1579574435983](D:\markdown笔记\calculus_tongji\images\3~1579574435983.png)

![1579574486229](D:\markdown笔记\calculus_tongji\images\3~1579574486229.png)





## 泰勒(Taylor)公式

(对于一些复杂的函数，为了方便起见，我们会趋向用简单的函数进行近似。一般而言用多项式进行近似代替能达到很好的效果。同时，多项式也有很多良好的特性，比如容易求导，容易计算等)

### 先决条件

设$f(x)$在$x_0$处存在n阶导数，求出一个关于$(x - x_0)$的n阶多项式(polynomial):$p_n(x) = a_0 + a_1(x - x_0) + a_2(x - x_0)^2 + \cdots + a_n(x - x_0)^n$来近似表示函数$f(x)$，且误差是$x \to x_0$时，比$(x - x_0)^n$的高阶无穷小。  

我们可以让$p_n(x) 与 f(x)$的各阶导数导数都相等，从而让$p_n(x)$逼近$f(x)$。

1、$p_n(x_0) = f(x_0)\Longleftrightarrow a_0 = f(x_0)$  

2、$p_n^{(1)}(x_0) = f^{(1)}(x_0)\Longleftrightarrow 1·a_1 = f^{(1)}(x_0)$

3、$p_n^{(2)}(x_0) = f^{(2)}(x_0)\Longleftrightarrow 2!·a_1 = f^{(2)}(x_0)$

...

n、$p_n^{(n)}(x_0) = f^{(n)}(x_0)\Longleftrightarrow n!·a_1 = f^{(n)}(x_0)$



即，$a_0 = f(x_0), \;a_1 = f^{(1)}(x_0),\;a_2 = \dfrac{f^{(2)}(x_0)}{2！},\;\cdots, a_n = \dfrac{f^{(n)}(x_0)}{n!}$。

所以，$p_n(x) = f(x_0) + f^{(1)}(x_0)(x - x_0) + \dfrac{f^{(2)}(x_0)}{2!}(x - x_0)^2 + \cdots + \dfrac{f^{(n)}(x_0)}{n!}(x - x_0)^n$

### 泰勒中值定理1(带有佩亚诺余项的泰勒公式)

![1579587386123](D:\markdown笔记\calculus_tongji\images\3~1579587386123.png)

![1579587490563](D:\markdown笔记\calculus_tongji\images\3~1579587490563.png)

![1579587504094](D:\markdown笔记\calculus_tongji\images\3~1579587504094.png)

所以，$f(x)$可以简写为：$f(x) = P_n(x) + R_n(x)$

#### 证明

记$R_n(x) = f(x) - p_n(x)$

则$R_n(x_0) = R_n^{(1)}(x_0) = R_n^{(2)}(x_0) = \cdots = R_n^{(n)}(x_0) = 0$

由于$f(x)$在$x = x_0$处的某领域内存在(n - 1)阶导数，所以$R_n(x)$在$x = x_0$处该邻域内也存在(n - 1)阶导数，不断地用洛必达可得：

$\lim\limits_{x \to x_0}\dfrac{R_n(x)}{(x - x_0)^n}\\ =\lim\limits_{x \to x_0}\dfrac{R^{(1)}_n(x)}{n(x - x_0)^{n-1}}\\ = \lim\limits_{x \to x_0}\dfrac{R^{(2)}_n(x)}{n(n-1)(x - x_0)^{n-2}}\\ =\cdots \\ \\= \lim\limits_{x \to x_0}\dfrac{R^{(n-1)}_n(x)}{n!(x - x_0)}\\ = \dfrac{1}{n!}\lim\limits_{x \to x_0}\dfrac{R^{(n-1)}_n(x) - R_n^{(n-1)}(x_0)}{(x - x_0)}\\ = \dfrac{1}{n!}R_n^{(n)}(x_0) \\= 0$

所以，$R_n{(x)} = o((x - x_0)^n)$

证明完毕。  

### 泰勒中值定理2(带有拉格朗日余项的泰勒公式)

(由于佩亚诺余项无法表示处误差的大小，所以引入拉格朗日余项)

![1579588900768](D:\markdown笔记\calculus_tongji\images\3~1579588900768.png)

![1579588962264](D:\markdown笔记\calculus_tongji\images\3~1579588962264.png)

![1579588975855](D:\markdown笔记\calculus_tongji\images\3~1579588975855.png)

![1579588993598](D:\markdown笔记\calculus_tongji\images\3~1579588993598.png)

#### 证明

记$R_n(x) = f(x) - p_n(x)$

证明$R_n(x) = \dfrac{f^{(n + 1)}(\xi)}{(n+1)!}(x - x_0)^{n+1}$， $\xi \in (x_0, x)$

由假设可得，$R_n(x_0)在U(x_0)$处存在（n+1）阶导数，且

$R_n(x_0) = R_n^{(1)}(x_0) = R_n^{(2)}(x_0) = \cdots = R_n^{(n)}(x_0) = 0$

对于函数$R_n(x)$与$(x - x_0)^{(n+1)}$在$(x_0, x)$ 满足柯西中值定理，所以

$\dfrac{R_n(x)}{(x - x_0)^{(n+1)}} = \dfrac{R_n(x) - R_n(x_0)}{(x - x_0)^{(n+1)} - 0} = \dfrac{R^{(1)}(\xi_1)}{(n+1)(\xi_1 - x_0)^{(n)}}\;\;其中：\xi_1 \in (x_0, x)$

不断地使用柯西中值定理得：

$\dfrac{R^{(1)}(\xi_1)}{(n+1)(\xi_1 - x_0)^{(n)}} = \dfrac{R^{(1)}(\xi_1) - R_n^{(1)}(x_0)}{(n+1)(\xi_1 - x_0)^{(n)} - 0} = \dfrac{R^{(2)}(\xi_2)}{(n+1)n(\xi_2 - x_0)^{(n-1)}}\;\;其中：\xi_2 \in (x_0, \xi_1)$

经过(n+1)次柯西中值定理后： 

$\dfrac{R_n(x)}{(x - x_0)^{(n+1)}} = \dfrac{R^{(n+1)}(\xi)}{(n+1)!}\;\;其中：\xi \in(x_0, \xi_n) \;or \;\xi \in(x_0, x)$

注意到$R^{(n+1)}(x) = f^{(n+1)}(x)$， 这是因为$p^{(n+1)}(x) = 0$

所以：$R_n(x) = \dfrac{f^{(n + 1)}(\xi)}{(n+1)!}(x - x_0)^{n+1}$，$\xi \in (x_0, x)$。

证明完毕。  



#### 利用拉格朗日余项估计误差

![1579590334701](D:\markdown笔记\calculus_tongji\images\3~1579590334701.png)

#### 麦克劳林公式(当$x_0 = 0$时的泰勒公式)



![1579590413873](D:\markdown笔记\calculus_tongji\images\3~1579590413873.png)



### 例子

![1579590461671](D:\markdown笔记\calculus_tongji\images\3~1579590461671.png)

![1579590479115](D:\markdown笔记\calculus_tongji\images\3~1579590479115.png)

![1579590567685](D:\markdown笔记\calculus_tongji\images\3~1579590567685.png)

![1579590596352](D:\markdown笔记\calculus_tongji\images\3~1579590596352.png)

![1579590640043](D:\markdown笔记\calculus_tongji\images\3~1579590640043.png)

![1579590687170](D:\markdown笔记\calculus_tongji\images\3~1579590687170.png)



## 函数的单调性与曲线的凹凸性

### 函数单调性的判别方法

![1579594363084](D:\markdown笔记\calculus_tongji\images\3~1579594363084.png)

![1579594375408](D:\markdown笔记\calculus_tongji\images\3~1579594375408.png)

![1579594395046](D:\markdown笔记\calculus_tongji\images\3~1579594395046.png)

### 证明

设函数$f(x)$在$[a, b]$处连续，在$(a, b)$处可导，在$[a, b]$处任取两点$x_1, x_2(x_1< x_2)$，由拉格朗日中值定理可得：  

$f(x_2) -f(x_1) = f^{’}(\xi) (x_2 - x_1)$

由$f^{‘}(\xi)\geq0, (x_2 - x_1)>0$ 得：$f(x_2) > f( x_1)$

所以函数为单调增函数。  

同理可证得单调减函数。  

### 将函数划分为多个单调区间

找出函数导数等于0的点，判断该点左右定义域导数的符号。  

### 例子

![1579595037871](D:\markdown笔记\calculus_tongji\images\3~1579595037871.png)

## 曲线的凹凸性与拐点(Convexity and inflection point of curve)

### 凹凸性（concave & convex）

![1579595104844](D:\markdown笔记\calculus_tongji\images\3~1579595104844.png)

![1579595117805](D:\markdown笔记\calculus_tongji\images\3~1579595117805.png)



### 凹凸性与二阶导数的关系

![1579595251518](D:\markdown笔记\calculus_tongji\images\3~1579595251518.png)

#### 证明

1. 从直观上看

    函数为凸函数，那么它的导函数为单调减函数

    函数为凹函数，那么它的导函数为单调增函数

2. 利用拉格朗日中值定理证明

    设$x_1, x_2 \in [a, b] $,且$x_1 < x_2$，记$\dfrac{x_1 + x_2}{2} = x_0, x_2 - x_0 = x_0 - x_1 = h$

    由拉格朗日中值定理的：  

    $f(x_0 + h) - f(x_0) = f^{’}(x_0 + \theta_1h)h$  

    $f(x_0 ) - f(x_0 -h) = f^{‘}(x_0 - \theta_2h)h$

    (其中，$0<\theta_1, \theta_2<1$)

    两市相减得：  

    $f(x_0 + h ) + f(x_0 - h ) - 2f(x_0) = [f^{‘}(x_0 + \theta_1h) - f^{‘}(x_0 - \theta_2h)]h$

    再利用拉格朗日中值定理对$f^{’}(x)$在区间$[x_0 - \theta_2h, x_0 + \theta_1h]$求得：  

    $[f^{‘}(x_0 + \theta_1h) - f^{‘}(x_0 - \theta_2h)]h = f^{''}(\xi)h^2$

    (其中，$\xi \in [x_0 - \theta_2h, x_0 + \theta_1h]$)

    由$f^{''}(\xi), h^2 > 0$得：

    $f(x_0 + h ) + f(x_0 - h ) - 2f(x_0) > 0 $

    所以，$\dfrac{f(x_0 + h ) + f(x_0 - h )}{2} > f(x_0)$

    即，$\dfrac{f(x_1) +f(x_2)}{2} > f(\dfrac{x_1+x_2}{2})$

    证得$f(x)在[a, b]$上为凹函数。  

    

#### 例子

![1579596890122](D:\markdown笔记\calculus_tongji\images\3~1579596890122.png)

### 拐点

![1579596956215](D:\markdown笔记\calculus_tongji\images\3~1579596956215.png)

![1579596982953](D:\markdown笔记\calculus_tongji\images\3~1579596982953.png)

#### 例子

![1579597001724](D:\markdown笔记\calculus_tongji\images\3~1579597001724.png)

![1579597061449](D:\markdown笔记\calculus_tongji\images\3~1579597061449.png)