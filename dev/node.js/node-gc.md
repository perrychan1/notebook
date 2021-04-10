# Node.js Garbage Collection 垃圾回收

## 程序内存特点

- 频繁地新建变量，频繁地销毁变量；
- 新生的变量中多数的存活时间短，老生的变量中多数存活时间长。

## 留意

- 垃圾回收有成本：需要计算和内存，会影响事件循环；

## 内存的组成

通过 `process.memoryUsage` 来查看内存。

- rss: 进程所占用的内存部分，包括代码本身、栈、堆；
- heapTotal: 堆中申请到的总内存空间；
- heapUsed: 堆中已用空间；
- external: V8 引擎内部的 C++ 对象所占的内存。

## 参考

- [Node.js内存管理和V8垃圾回收机制](https://juejin.cn/post/6844903878928891911)
