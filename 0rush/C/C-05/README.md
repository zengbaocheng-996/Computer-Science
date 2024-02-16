# 操作系统引导

**2021** 某计算机用硬盘作为启动盘，硬盘的第一个扇区存放主引导记录，其中包含磁盘引导程序和分区表。磁盘引导程序用于选择要引导哪个分区的操作系统，分区表记录硬盘上各分区的位置等描述信息。硬盘被划分成若干个分区，每个分区的第一个扇区存放分区引导程序，用于引导该分区中的操作系统。系统采用多阶段引导方式，除了执行磁盘引导程序和分区引导程序外，还需要执行ROM中的引导程序。请回答下列问题。

1. 系统启动过程中操作系统的初始化程序、分区引导程序、ROM中的引导程序、磁盘引导程序的执行顺序是什么？

   **ROM中的引导程序、磁盘引导程序、分区引导程序、操作系统的初始化程序**

2. 把硬盘制作为启动盘时，需要完成操作系统的安装、磁盘的物理格式化、逻辑格式化、对磁盘进行分区，执行这4个操作的正确顺序是什么？

   **磁盘物理格式化、对磁盘进行分区、逻辑格式化、操作系统的安装**

3. 磁盘扇区的划分和文件系统根目录的建立分别是在第2问的哪个操作中完成的？

   **磁盘扇区的划分 物理格式化**

   **文件系统根目录的建立 逻辑格式化**

**2022** 下列选项中，需要在操作系统进行初始化过程中创建的是 **A**

A 中断向量表

B 文件系统的根目录

C 硬盘分区表

D 文件系统的索引节点表