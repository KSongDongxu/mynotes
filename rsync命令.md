# rsync命令

## **rsync格式**

```
rsync [OPTION] … SRC   DEST
rsync [OPTION] … SRC   [user@]host:DEST
rsync [OPTION] … [user@]host:SRC   DEST
rsync [OPTION] … SRC   [user@]host::DEST
rsync [OPTION] … [user@]host::SRC   DEST
```



## **rsync常用选项**

```
-a 包含-rtplgoD
-r 同步目录时要加上，类似cp时的-r选项
-v 同步时显示一些信息，让我们知道同步的过程
-l 保留软连接
-L 加上该选项后，同步软链接时会把源文件给同步
-p 保持文件的权限属性
-o 保持文件的属主
-g 保持文件的属组
-D 保持设备文件信息
-t 保持文件的时间属性
--delete 删除DEST中SRC没有的文件
--exclude 过滤指定文件，如--exclude “logs”会把文件名包含logs的文件或者目录过滤掉，不同步
-P 显示同步过程，比如速率，比-v更加详细
-u 加上该选项后，如果DEST中的文件比SRC新，则不同步
-z 传输时压缩
```



参考：[rsync基本使用](https://my.oschina.net/ccLlinux/blog/1859116)

​			[inotify+rsync实时备份总结](https://blog.51cto.com/lzhnb/2088224) 