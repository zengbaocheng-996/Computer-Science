# 设备的分配与回收

### 逻辑设备与物理设备

为了提高设备分配的灵活性和设备的利用率、方便实现I/O重定向，引入了设备独立性。设备独立性是指应用程序独立于具体使用的物理设备。而为了实现设备独立性引入了逻辑设备和物理设备这两个概念。在应用程序中，使用逻辑设备名称来请求使用某类设备；而系统在实际执行时，则使用物理设备名称。逻辑设备名与物理设备名通过系统中设置的一张逻辑设备表（LUT）进行映射。