# 奈氏准则&香农定理

### 奈氏准则

背景：带宽受限无噪声条件下，为了避免码间串扰，码元传输速率的上限 2W Baud。

理想低通信道下的极限数据传输率
$$
2W\log_2{M}(b/s)
$$

### 香农定理

背景：带宽受限且有噪声的信道中，为了不产生误差，信息的数据传输速率有上限值。

信道的极限数据传输速率
$$
W\log_2{(1+S/N)}(b/s)
$$
信噪比（分贝）

- S是信道所传信号的平均功率

- N是信道内的高斯噪声功率
  $$
  1dB = 10\log_{10}(S/N)
  $$

注

- 只有在这两个公式中，带宽采用Hz
- 两个公式都可用时，取最小min(奈氏准则，香农定理)

**2009** 在无噪声的情况下，若某通信链路的带宽为3kHz，采用4个相位，每个相位具有4种振幅的QAM调制技术，则该通信链路的最大数据传输速率是 **B**

A 12kbps

B 24kbps

C 48kbps

D 96kbps

**2014** 下列因素中，不会影响信道数据传输速率的是 **D**

A 信噪比

B 频率带宽

C 调制速率

D 信号传播速度

**2016** 若连接R2和R3链路的频率带宽为8kHz，信噪比为30dB，该链路实际数据传输速率约为理论最大数据传输速率的50%，则该链路的实际数据传输速率约是 **C**

A 8kbps

B 20kbps

C 40kbps

D 80kbps

**2017** 若信道在无噪声情况下的极限传输速率不小于信噪比为30dB条件下的极限数据传输速率，则信号状态数至少是 **D**

A 4

B 8

C 16

D 32