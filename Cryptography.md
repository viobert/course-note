# Cryptography



## 1. Introduction  What is cryptography

### 1.1 Crypto core
  1. Secret key establishment
  2. Secret communication

###  1.2 some examples/application

1. Digital signature
2. anonymous communication
3. protocol
	+ secure mutip-party computation **安全安全计算**   它去除了可信任中心
4. privately outsourcing computation -->  Homomorphic encryption ？
5. zero knowledge 零知识证明  (换句话说 基于大质数分解，Alice可以让Bob知道自己分解方式，但不必让Bob知道因数p、q) 

### 1.3 The three step in cryptography

1. Precisely specify threat model
2. Propose a construction
3. Prove that breaking construction under threat mode will solve an underlying hard problem

## 2. Cryptographical History

 ### 2.1Symmetric Encryption 对称密码体制

1. Substitution cipher  					

   ​	对于26个字母来说，密钥空间为26!，26!近似为$2^{88}$  每个密钥88位表示，其实空间与许多相当安全的算法密钥空间近似，但仍然十分不安全。

   ​	**How to break a substitution cipher? 那么如何破解替换密码？**

   ​	我们使用的是字频分析 *frequency* ，从密文中找到出现次数最多的单词*letter*和词组*digrams*,对应概率上出现次数最多的单词和词组，可以极大程度上锁定密钥。这种攻击方式 ==a ciphertext only attack== 唯密文攻击。仅凭借密文即可还原明文。

   example：*caesar cipher* 		严格来说不算密码，因为没有密钥

   ​				vigener cipher

2.  waiting......

## 3. Discrete probability

> ###### There's classical joke that the only think cryptographers knows how to do is just XOR things together.

### Why we see XOR so frequently in cryptograhy

+ XOR $\bigoplus$ 有一个十分重要的性质：

  X an idenp. Uniform var. on $`\{0,1\}^n`$        X是独立的随机变量在{0,1}$^n$均匀分布               Y an rand. var over {0,1}$^n$

  若 Z := X $\bigoplus$ Y 当我们可以确定变量X是均匀分布的且X, Y独立，那么Z依然是均匀分布的（即便Y是malicious distribution 恶意分布的）。

 

![image](picture_cryptography/1.png)

