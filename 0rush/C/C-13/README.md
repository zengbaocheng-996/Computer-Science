# 连续分配管理方式

### 连续分配方式

| 分配方式     | 单一连续分配                                                 | 固定分区分配                                                 | 动态分区分配                                                 |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 说明         | 分为系统区和用户区。<br />系统区仅提供给操作系统使用，通常在低地址部分。<br />用户区是为用户提供的除系统外的内存空间。 | 将内存用户空间划分为若干个固定大小的区域，每个分区只装入一道作业。当有空闲分区时，便可以再从外存的后备作业队列中选择适当大小的作业装入该分区，如此循环。 | 是一种动态划分内存的分区方法。不预先将内存划分，而是在进程装入内存时，根据进程的大小动态地建立分区，并使分区的大小正好适合进程的需要。因此系统中分区的大小和数目是可变的。 |
| 碎片         | 内部碎片                                                     | 内部碎片                                                     | 外部碎片                                                     |
| 作业道数     | 1                                                            | <=N（用户空间划分N块）                                       | 不确定                                                       |
| 硬件         | 界地址寄存器、越界监察机构                                   | 上下界寄存器、越界检查机构<br />基地址寄存器、长度寄存器、动态地址转换机构 | 上下界寄存器、越界检查机构<br />基地址寄存器、长度寄存器、动态地址转换机构 |
| 解决空间不足 | 覆盖                                                         | 覆盖/交换                                                    | 交换                                                         |

### 动态分区分配算法

| 算法             | 说明                                                         | 特点                                                         |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 首次适应算法     | 空闲分区以地址递增的次序链接。分配内存时从链首开始顺序查找，直到找到大小能满足要求的第一个空闲分区 | 实现方法简答；<br />查找速度快，平均性能最好；<br />碎片多出现于低地址空间。 |
| 循环首次适应算法 | 空闲分区以地址递增的次序链接。分配内存时，从上次查找结束的位置开始继续查找，直到找到第一个满足要求的空闲分区。 | 平均性能比首次适应算法差；<br />碎片多出现于高地址空间。     |
| 最佳适应算法     | 空闲分区按容量递增的次序链接。分配内存时，从链首开始顺序查找，直到找到第一个能满足要求的空闲分区。 | 需要对分区排序，开销大；形成许多难以利用的小碎片。           |
| 最差适应算法     | 空闲分区以容量递减的次序链接。分配内存时，从链首开始顺序查找，直到找到第一个能满足要求的空闲分区，也就是挑选出最大的分区。 | 需要对分区排序，开销大；<br />使系统缺少大的连续空闲地址空间 |
