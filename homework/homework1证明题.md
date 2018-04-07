复振幅透过率：$$t(x_0,y_0)=[\frac{1}{2}+\frac{m}{2}cos(2\pi f_0x_0)]\cdot rect(\frac{x_0}{l})rect(\frac{y_0}{l})$$

$$m\leq1$$称为光栅的调制度
证明：用单位振幅的单色平面光波垂直照明该光栅，可得光栅的频谱为：

$$T(f_x,f_y)=\frac{l^2}2 sinc(lf_y)\cdot\{sinc(lf_x)+\frac{m}2\cdot sinc[l(f_x+f_0)]+\frac{m}2 \cdot sinc[l(f_x-f_0)]\}$$

证明：
令
$$
\begin{align}
&f(x,y)= \frac{1}{2}+\frac{m}{2}cos(2\pi f_0x_0)\\
\\
&g(x,y)= rect(\frac{x_0}{l})rect(\frac{y_0}{l})\\
\\
&t(x,y)=f(x,y)\cdot g(x,y)
\end{align}
$$
分别对$f(x)​$和$g(x)​$作傅里叶变换得:
$$
\begin{align}
&F(f_x,f_y)= \frac{1}2 \delta(f_x,f_y)+\frac{m}4 [\delta(f_x+f_0,f_y)+\delta(f_x-f_0,f_y)]\\
\\
&G(f_x,f_y)= l^2\cdot sinc(lf_x)sinc(lf_y)\\
\\
&T(f_x,f_y)=F(f_x,f_y)\ast G(f_x,f_y)
\end{align}
$$

任意函数$f(x,y)$与$\delta$函数卷积，结果是函数$f(x,y)$本身
$$
\begin{align}
f(x,y)\ast \delta(x,y)&=\iint_{-\infty}^\infty f(\xi,\eta)\delta(\xi-x,\eta-y)d\xi d\eta \\
\\
&=f(x,y)
\end{align}
$$
将上式简单推广得到$f(x,y)\ast \delta(x-x_0,y-y_0)=f(x-x_0,y-y_0)​$，这表明$\delta​$函数平移多少距离，原函数就要平移多少距离。

所以
$$
\begin{align}
T(f_x,f_y)&=F(f_x,f_y)\ast G(f_x,f_y)\\
\\
&=\{\frac{1}2 \delta(f_x,f_y)+\frac{m}4 [\delta(f_x+f_0,f_y)+\delta(f_x-f_0,f_y)]\}\ast [l^2\cdot sinc(lf_x)sinc(lf_y)]\\
\\
&=\frac{ l^2}{2}\cdot sinc(lf_x)sinc(lf_y)+\frac{m}4\cdot l^2sinc[l(f_x+f_0)]sinc(lf_y)+\frac{m}4\cdot l^2sinc[l(f_x-f_0)]sinc(lf_y)\\
\\
&=\frac{ l^2}{2}\cdot sinc(lf_y)\cdot\{sinc(lf_x)+\frac{m}2\cdot sinc[l(f_x+f_0)]+\frac{m}2\cdot sinc[l(f_x-f_0)]\}
\end{align}
$$

证明完毕

附件：
1、$\delta(t)$ 的傅里叶变换，由$\delta$函数的筛选特性可得：
$$\int_{-\infty}^\infty \delta(t) e^{-j2\pi ft}dt=1$$

2、$cos(2\pi f_0x)$的傅里叶变换：
$$
\begin{align}
F[cos(2\pi f_0x)]&=\int_{-\infty}^\infty [cos(2\pi f_0x)]\cdot e^{-j2\pi fx}dx\\
\\
&=\int_{-\infty}^\infty\frac{1}2(e^{-j2\pi f_0x}+e^{j2\pi f_0x})\cdot e^{-j2\pi fx}dx\\
\\
&=\frac{1}2\cdot \int_{-\infty}^\infty e^{-j2\pi (f+f_0)x}+e^{-j2\pi (f-f_0)x}dx\\
\\
&=\frac{1}2\cdot [\delta(f+f_0)+\delta(f-f_0)]
\end{align}
$$

3、$rect(x)$的傅里叶变换：
$$
\begin{align}
F[rect(x)]&=\int_{-\infty}^\infty rect(x)\cdot e^{-j2\pi fx}dx\\
\\
&=\int_{\frac{-1}2}^{\frac{1}2} e^{-j2\pi fx}dx\\
\\
&=\frac{e^{-j2\pi fx}}{-j2\pi f}|_{\frac{-1}2}^{\frac{1}2}\\
\\
&=\frac{e^{-j2\pi f}-e^{j2\pi f}}{-j2\pi f}\\
\\
&=\frac{sin(\pi f)}{\pi f}\\
\\
&=sinc(f)
\end{align}
$$
