# DDoS_awesome_papers_collection  
## 1. [RAD: A Statistical Mechanism Based on Behavioral Analysis for DDoS Attack Countermeasure](https://github.com/2654400439/DDoS_awesome_papers_collection/blob/main/papers/Hajimaghsoodi%20%E5%92%8C%20Jalili%20-%202022%20-%20RAD%20A%20Statistical%20Mechanism%20Based%20on%20Behavioral%20A.pdf)
**发表于IEEE TRANSACTIONS ON INFORMATION FORENSICS AND SECURITY(TIFS) 2022**  
<br/>
**简介：**  
本文提出了一种三阶段的基于统计模型的ddos处理机制。第一阶段外部用户被划分成正常或者可疑；第二阶段更新内部节点状态是否正常；第三阶段若受到攻击则对可疑用户进行阻止并进行连续评估。  
**借鉴：**  
1. 相关工作总结的很全面
2. 提出了用户合法概率--从用户（ip）的层面提取特征（流级别以上）并用贝叶斯概率计算与基准值之间的可能性偏差，思想类似于**节点分布偏离度**
3. 从用户层面将外部ip的特征（平均发包数等）和内部ip的特征（丢包率等）都用到了，且这些特征是有效的，超过了简单的机器学习模型
4. 用到的特征：外部用户刻画--每秒发流数、每秒发包数、流量负载生成数、并发连接数；内部用户刻画--包处理平均时延、包处理波动、每秒丢包率
5. 提到对每个用户构建应用层指纹  

## 2. [Developing Realistic Distributed Denial of Service (DDoS) Attack Dataset and Taxonomy](https://github.com/2654400439/DDoS_awesome_papers_collection/blob/main/papers/Sharafaldin%20%E7%AD%89%20-%202019%20-%20Developing%20Realistic%20Distributed%20Denial%20of%20Service.pdf)  
**发表于ICCST（非知名会议） 19**  
<br/>
**简介：**  
本文发布了cic ddos 2019数据集  
**借鉴：**  
1. 大部分是反射放大ddos，但是反射放大ddos与传统ddos的区别以及特定的检测方法未知
2. 本文使用的四个传统机器学习方法可以直接用来做对比实验（文献1中直接借鉴使用）  

## 3. Composite and efficient DDoS attack detection framework for B5G networks  
**发表于Computer Networks 21**  
```diff
- 注意避雷，本文很水
```
**简介：**  
本文提出了一种复合结构神经网络（两个不同结构的全连接神经网络）检测5g环境下的ddos攻击的方法  
**借鉴：**  
1. 背景知识介绍5G环境中面临的安全问题；实验部分写的很细致但有点像技术报告
2. 使用**泊松相关系数**做特征选择
3. 使用keras-tune自动选择最优超参数
4. 引用了一篇深度学习测试阶段防止投毒攻击的文章


# 其他
## 1. [ZeroWall: Detecting Zero-Day Web Attacks through Encoder-Decoder Recurrent Neural Networks](https://github.com/2654400439/DDoS_awesome_papers_collection/blob/main/papers/Tang%20%E7%AD%89%E3%80%82%20-%20ZeroWall%20Detecting%20Zero-Day%20Web%20Attacks%20through%20E.pdf)入侵检测
**发表于INFOCOM 2020**
<br/>  
**简介：**  
本文提出了一种无监督的检测0day web攻击的模型，使用包含循环神经网络结构的AE来实现自翻译任务，通过衡量翻译结果与原始样本差距来判断是否为0day攻击。  
**借鉴：**  
1. 行文很标准，可以**参考写作**  
2. 架构图画的挺好看的  
3. 进行攻击检测基于一个前提假设那就是正常流量符合http语言规范，而攻击流量一般不符合。可以在gan或扩散模型进行流量生成的时候增加这种http语言规范限制  
4. 除了孪生网络，这是另一种做未知检测的范式（自编码器重构损失），是否有可能将两种方法结合  
