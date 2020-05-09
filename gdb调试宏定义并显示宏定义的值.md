gdb跟踪调试宏定义的值时，出现如下提示：No symbol "XXXX" in current context.

原因：编译器默认没有把宏定义扩展信息编译进二进制文件

解决：编译时需在CFLAGS参数后添加-gdwarf-2和-g3两个参数。

加了-g3的参数后，gcc编译的时候，会将扩展的debug 信息编译进二进制文件里面，包括宏定义信息。

参考：[传送门](https://blog.csdn.net/zhangjs0322/article/details/39666889)