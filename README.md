# MachineLearning
study and review
+ *备注*
  + [latex简介]： https://blog.csdn.net/chaipp0607/article/details/78815933 “md文件中插入公式简单介绍”
  + [latex简介]： https://liam.page/2014/09/08/latex-introduction/ “LateX数学公式语法详细版本”
  + [md语法]：https://www.cnblogs.com/liugang-vip/p/6337580.html “md文件简要书写方式”

***

## 统计基础重要知识点
### 古典概型
### 几何概型
$$p(A) = \frac{构成时间A的区域长度（面积或体积）} {全部结果构成的区域长度（面积或体积）}$$
  * [buffon投针实验]：https://www.cnblogs.com/liugang-vip/p/6337580.html
### 条件概率
1. 条件概率公式
$$P(B|A) = \frac{ P(AB) } {P(A)}$$
  * [汽车与山羊]：https://blog.csdn.net/u012557765/article/details/82682654
2. 全概率公式
$$P(A)=P(A|B_{1}) P(B_{1}) + P(A|B_{2}) P(B_{2}) + ... + P(A|B_{n}) P(B_{n})$$
3. 贝叶斯公式
$$P(B_{i}|A) = \frac{P(A|B_{i}) P(B_{i})} {\sum_{j}^{n} P(A|B_{j})P(B_{j})}$$
### 离散随机变量及其分布
1. （0-1）分布
  * [伯努利实验]： https://baike.baidu.com/item/%E4%BC%AF%E5%8A%AA%E5%88%A9%E8%AF%95%E9%AA%8C/238488?fr=aladdin
2. 二项分布
  * 分布律
  $$P(X=k) = C_n^kp^k(1-p)^{n-k}$$
  记：$X\sim{B(n,p)}$
  * [n重伯努利实验]： https://baike.baidu.com/item/n%E9%87%8D%E4%BC%AF%E5%8A%AA%E5%88%A9%E8%AF%95%E9%AA%8C/238667?fr=aladdin
3. 泊松分布
  * 分布律
  $$ P(X=k) = \frac{e^{-\lambda}\lambda^k} {k!} $$
  记：$X\sim\pi(\lambda)$  其中$\lambda=np$
### 连续随机变量及其分布
$$F(x)=P\lbrace{X\le{x}}\rbrace=\int_{-\infty}^xf(t)dt$$
  f(t)成为概率密度函数
1. 均匀分布
  当$f(x)=\frac{1}{b-a}$时，称随机事件X在a,b上均匀分布，记为：$X\sim{U(a,b)}$
2. 正态分布
  $$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
  记$X\sim{N(\mu,\sigma^2)}$
3. 标准正态分布
  即$\mu=0  \sigma=1$
  $$f(x)=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}$$
  * 正态分布$\rightarrow$标准正态分布 
    若$X\sim{\mu,\sigma^2}$,则 $Z=\frac{X-\mu}{\sigma}\sim{\Phi(\frac{x-\mu}{\sigma})}$
  * 二项分布与正态分布
    $X\sim{B(n,p)}$,当n足够大时，有X近似服从正态分布$X\sim{N(np,np(1-p))}$
### 离散二维随机变量
$$F(x,y)=P\lbrace{(X<x)UP(Y<y)}\rbrace=P\lbrace{X<x,Y<y}\rbrace$$
次二元函数成为随机变量(X,Y)的联合分布函数
### 连续型二维随机变量
$$F(x,y)=\int_{-\infty}^x\int_{-infty}^yf(\mu,\nu)d\mu{d\nu}$$
函数$f(x,y)$为连续型二维随机变量(X,Y)的联合概率密度
### 边缘分布
在多维随机变量中，将$X,Y$各自的分布称为边缘分布函数，分别记为$F_X,F_Y$
$$F_X=P\lbrace{X\leq{x}}\rbrace=P\lbrace{X\leq{x},Y<\infty}\rbrace=F(x,\infty)$$
### 边缘概率密度
$$f_X(x)=\int_{-\infty}^\infty{f(x,y)}dy$$
### 条件分布
* 离散条件分布律
  $$P(X=x_i|Y=y_j)=\frac{P(X=x_i,Y=y_j)}{P(Y=y_j)}=\frac{P_{ij}}{P_{.j}}$$
  称为在$Y=y_j$的条件下随机变量X的条件分布律
* 条件概率密度
  $$f_{X|Y}(x|y)=\frac{f(x,y)}{f_Y(y)}$$
* 条件分布函数
  $$F_{X|Y}(x|y)=\int_{-\infty}^x\frac{f(t,y)}{f_Y(y)}dt$$
  在$Y=y$条件下$X$的条件分布函数
### 离散型随机变量的数学期望
  对离散型随机变量$X$的分布律为$P\lbrace{X=x_k}\rbrace=p_k$，若级数$\Sigma_{k=1}^\infty{x_kp_k}$绝对收敛，
  则随机变量的数学期望记为：
  $$E(X)=\Sigma_{k=1}^\infty{x_kp_k}$$
  * ps:二项式定理：$(x+y)^n=\Sigma_{k=0}^nC_n^kx^ky^n-k$
### 连续型随机变量的数学期望
  对连续型随机变量$X$，其概率密度函数为$f(x)$，若积分$\int_{-\infty}^\infty{xf(x)dx}$绝对收敛，
  则连续型随机变量$X$的数学期望记为：
  $$E(X)=\int_{-\infty}^\infty{xf(x)dx}$$
### 离散型随机变量的方差
  $$D(X)=\Sigma_{k=1}^{\infty}[x_k-E(X)]^2p_k$$
### 连续型随机变量的方差
  $$D(X)=\int_{-\infty}^{\infty}[x-E(X)]^2f(x)dx$$
  化简式：$D(X)=E(X^2)-[E(X)]^2$
### 协方差与相关系数
  称$E\lbrace{(X-E(X))(Y-E(Y))}\rbrace$为随机变量$X,Y$的协方差，记为$Cov(X,Y)$,即
  $$Cov(X,Y)=E(XY)-E(X)E(Y)$$
  随机变量$X,Y$的相关系数为：
  $$\rho_{XY}=\frac{Cov(X,Y)}{\sqrt{D(X)}\sqrt{D(Y)}}$$
  相关系数用于衡量两个随机变量之间的线性相关性
### 矩
  $X$的$k$阶原点矩（若存在）：
  $$E(X^k)$$
  $X$的$k$阶中心矩（若存在）：
  $$E\lbrace{[X-E(X)]^k}\rbrace$$
  $X$和$Y$的$k+l$阶混合矩（若存在）：
  $$E(X^kY^l)$$
  $X$和$Y$的$k+l$阶混合中心矩（若存在）：
  $$E\lbrace{[X-E(X)]^k[Y-E(Y)]^l}\rbrace$$
### 弱大数定律
  设$X_1,X_2,...$是相互独立，服从同一分布的随机变量序列，且具有数学期望$E(X_k)=\mu,(K=1,2,...)$,做前$n$个变量的算数平均$\frac{1}{n}\Sigma_{k=1}^nX_k$,则对于任意的$\epsilon>0$,有
  $$\lim\limits_{n\to\infty}P\lbrace{|\frac{1}{n}\Sigma_{k=1}^nX_k-\mu|<\epsilon}\rbrace=1$$
    
    
    


