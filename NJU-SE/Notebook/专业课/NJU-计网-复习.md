[TOC]



# 名词解释（期末）：

1. UDP
2. HTTP
3. Split Horizon
4. Socket
5. DNS
6. Time Division Multiplexing
7. ✨ADSL： 非对称数字用户线（Asymmetric Digital Subscriber Line）是用数字技术对现有的模拟电话用户线进行改造，使它能够承载宽带数字业务。
8. Full Duplex
9. OSI reference model
10. CSMA/CD
11. STP：生成树协议 Spanning Tree Protocol
12. PPP
13. Flow Control
14. Computer Virus
15. IEEE MAC Sub-layer
16. RARP



# 复习



1. 协议与服务有何区别，有何联系
   * 服务是指下层为紧邻的上层提供的功能调用。
   * 协议是控制两个**对等实体**之间通信的规则的集合。
   * 在协议的控制下，两个对等实体间的通信使得本层能够向上一层提供服务，要实现本层协议，需要使用下一层提供的服务
   * 区别：
     * 协议的实现保证了能够向上一层提供服务。下层的协议对上层服务时透明的。
     * 协议是“水平的”，即控制两个对等实体之间通信的规则
     * 服务时“垂直的”，是由下层通过层间接口向上层提供的。
2. 点到点通信和端到端通信的区别：
   * 由物理层、数据链路层和网络层组成的通信子网为网络环境中的主机提供点到点的服务。
   * 而传输层为网络中的主机提供端到端的服务
   * 直接相连的结点之间的通信称为点到点通信，他提供一台机器到另一台机器宅男的通信，不涉及程序或进程的概念。点到点不能保证数据传输的可靠性
   * 端到端通信是建立在点到点通信的基础上，完成应用程序之间的通信。

## 物理层

1. 单工通信：只有一个方向的通信而没有反方向的通信

2. 半双工通信：通信双方都可以发送或接受信息，但不能同时进行

3. 全双工通信：通信双方可以同时发送和接受信息

4. 奈奎斯特定理（奈氏准则）：在理想低通信道（没有噪声，带宽有限）中

   * W: 理想低通信道的带宽  Hz
   * V：每个码元离散电平的数目（有多少中不同的码元）
   * 极限码元传输率 ：2W
   * 极限数据传输率 ：$2W log_2V$
   * 在任何信道中，码元的传输速率是有上限的

5. 香农定理：带宽受限且有高斯白噪声干扰的信道

   * W ： 信道带宽
   * S：信道所传输信号的平局功率
   * N：信道内部的高斯噪声功率
   * S/N: 信噪比
   * 信噪比 = $ 10 log_{10}(S/N)$    单位dB
   * 信道的极限数据传输速率：$ W log_2(1+S/N)$

6. 编码方式：

   * 非归零编码 NRZ ：
     * 低电平 = 0，高电平 = 1
   * 曼彻斯特编码 （Manchester）: 
     * 前高后低 = 1， 前低后高 = 0；每个码元中间出现跳变
     * 用于以太网
   * 差分曼彻斯特：
     * 前半个码元和上一个码元的后半个码元相同 = 0 
     * 用于局域网

7. 调制方式：

   * 幅移键控制 ASK
   * 频移键控制 FSK
   * 相移键控制 PSK
   * 正交振幅调制 QAM：
     * B：波特率
     * m：相位数
     * n:每个相位振幅种数
     * R:数据传输率
     * $R = B log_2(mn)$

8. 电路交换、报文交换和分组交换：

9. 数据报和 虚电路（网络层）：分组交换的两种方式

   | 数据报 | 虚电路   |
   | ------ | -------- |
   | 无连接 | 面向连接 |

   
