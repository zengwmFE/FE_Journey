### 引起Nodejs内存泄漏

1. 全局变量需要进程退出才能释放
2. 闭包引用中间函数，中间函数也不会释放，会使原始作用域也不会释放，作用域不被释放他产生的内存也不会被释放。所以使用过后重置为null等待垃圾回收
3. 谨慎使用内存当作缓存，建议Redis或者Memcached.好处：外部缓存软件有着良好的缓存过期淘汰策略以及自有的内存管理，不影响Node主进程性能。减少内部常驻内存的对象数量垃圾回收更高效率，进程之间共享缓存

redis就是一个缓存管理工具   

### 分析具体问题

- 通过分析找到原因如果是Javascript通过v8-profiles来分析
- 硬件加速与重排
- node-inspector
推荐《webkit技术内幕》