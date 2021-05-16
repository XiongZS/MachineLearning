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
  意义：对于独立同分布且具有相同均值$\mu$的随机变量$X_1,X_2,....,X_n$，当$n$很大时，它们的算数平均数$\frac{1}{n}\Sigma_{k=1}^nX_k$很接近与$\mu$。$\to$ 可以使用样本的均值去估计总体的均值。
### 伯努利大数定律
  设$f_A$是$n$次独立重复实验中事件A发生的次数，$p$是事件A在每次试验中发生的概率，则对任意的正数$\epsilon>0$，有
  $$\lim\limits_{n\to\infty}P\lbrace{|\frac{f_A}{n}-p|<\epsilon}\rbrace=1$$
  意义：当实验的次数趋近于无穷大时，事件A发生的频率会依概率收敛与事件A发生的概率。
### 独立同分布的中心极限定理
  $n$个独立同分布的随机变量之和的分布近似于正态分布，$n$愈大，此种近似程度愈好。
  对于均值为$\mu$，方差为$\sigma_2>0$的独立同分布的随机变量$X_1,X_2,...,X_n$之和$\Sigma_{i=1}^nX_i$，当$n$足够大时，有
  $$\frac{\Sigma_{i=1}^nX_i-n\mu}{\sqrt{n}\sigma}\sim{N(0,1)}$$
### Lyapunov定理
### 二项分布近似正态分布
  * 高尔顿板实验
### 简单随机抽样
  总体中每个个体被抽中的概率都相等
  * 样本均值
  $$\overline{X}=\frac{1}{n}\Sigma_{i=1}^nX_i$$
  * 样本均值观察值
  $$\overline{x}=\frac{1}{n}\Sigma_{i=1}^nx_i$$
  样本均值是总体均值的无偏估计量--样本均值的期望等于总体均值
  $$E(\frac{1}{n}\Sigma_{i=1}^nX_i)=\mu$$
  * 样本均值的方差
  $$D(\overline{X})=\frac{\sigma^2}{n}$$
  * 样本方差
  $$S^2=\frac{1}{n-1}\Sigma_{i=1}^n(X_i-\overline{X}^2)$$
  样本方差是总体方差的无偏估计
### 样本分布之$\chi^2$分布
  设$X_1,X_2,...,X_n$是来自总体$N(0,1)$的样本，则称统计量
  $$\chi^2=X_1^2+X_2^2+...+X_n^2$$
  服从自由度为$n$的卡方分布，记为：$\chi^2\sim{\chi^2(n)}$
### $t$分布-student分布
  设$X\sim{N(0,1)},Y\sim{\chi^2(n)}$,且$X,Y$相互独立，则称随机变量$t=\frac{X}{\sqrt{\frac{Y}{n}}}$服从自由度为$n$的$t$分布。记为：$t\sim{t(n)}$.
### F分布
  设$U\sim{\chi^2(n_1)},V\sim{\chi^2(n_2)}$,且$U,V$相互独立，则称随机变量$F=\frac{U/n_1}{V/n_2}$服从自由度为$(n_1,n_2)$的F分布。记为：$F\sim{F(n_1,n_2)}$.
  * 对于F分布上的$\alpha$分位点，有
  $$F_{1-\alpha}(n_1,n_2)=\frac{1}{F_\alpha(n_2,n_1)}$$
### 正态总体的抽样分布
  设$X_1,X_2,...,X_n$是来自正态总体$N(\mu,\sigma^2)$,$\overline{X}$是样本均值，$S^2$是样本方差，则有：
  * $(1) \overline{X}\sim{N(\mu,\frac{\sigma^2}{n})}$
  * $(2) \frac{(n-1)S^2}{\sigma^2}\sim{\chi^2(n-1)}$
  * $(3) \overline{X}$与$S^2$相互独立
  * $(4) \frac{\overline{X}-\mu}{\frac{S}{\sqrt{n}}}\sim{t(n-1)}$
### 两个正态总体的样本均值与样本方差
  设$X_1,X_2,....,X_{n_1}$与$Y_1,Y_2,...,Y_{n_2}$分别来自正态总体$N(\mu_1,\sigma_1^2),N(\mu_2,\sigma_2^2)$的样本，且这两个样本相互独立。其样本均值分别为$\overline{X},\overline{Y}$,
  其方差分别为$S_1^2,S_2^2$,则有：
  * $\frac{S_1^2/S_2^2}{\sigma_1^2/\sigma_2^2}\sim{F(n_1-1,n_2-1)}$
### 点估计--置信区间
  * 中心极限定理：样本比例$\hat{p}$近似正态分布$N(p,p(1-p)/n)$
  * 样本比例落在尾部的概率非常小
  * 样本比例落在阴影尾部的总概率为$\alpha$
  * 样本比例落在中间部分的概率为$1-\alpha$
### 置信区间--名词解析
  * 置信区间(confidence interval):用来估计总体参数真实值的一个区间，通常形式：估计值$\pm$误差界限
  * 误差界限(margin of error):估计值的最大误差，使用E表示
  * 置信度(confidence level): $1-alpha$
  * 置信水平：$\alpha$
  * 临界值(critical values):$Z_{\alpha{/2}}$
  * 置信区间边界(confidence interval limits):置信上限，置信下限

  
  
  
  
  


