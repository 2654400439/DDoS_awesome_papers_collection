# DDoS_awesome_papers_collection  
### 1. RAD: A Statistical Mechanism Based on Behavioral Analysis for DDoS Attack Countermeasure
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
