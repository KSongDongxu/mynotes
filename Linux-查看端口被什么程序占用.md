# Linux-查看端口被什么程序占用

### 使用 ss 查看

ss 一般用于转储套接字统计信息。它还可以显示所有类型的套接字统计信息，包括 PACKET、TCP、UDP、DCCP、RAW、Unix 域等。

> ss -lntpd | grep :22

###使用 netstat 查看

netstat 能够显示网络连接、路由表、接口统计信息、伪装连接以及多播成员。目前netstat 已经过时了，都推荐使用ss来代替。

> netstat -tnlp | grep :22

###使用 lsof 查看

lsof(list open files)是一个列出系统上被进程打开的文件的相关信息。

> lsof -i tcp:22

### 使用 fuser 查看

fuser 可以显示出当前哪个程序在使用磁盘上的某个文件、挂载点、甚至网络端口，并给出程序进程的详细信息。fuser只把PID输出到标准输出，其他的都输出到标准错误输出。

> 22/tcp: 6806

