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
$$F(x)=P\lbrace{X\le{x}}\rbrace=\int_{-\inft}y^xf(t)dt$$

