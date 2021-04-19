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


