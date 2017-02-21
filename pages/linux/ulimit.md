# ulimit

> Get and set user limits.

- Get the properties of all the user limits:

`ulimit -a`

- Get hard limit for the number of simultaneously opened files:

`ulimit -H -n`

- Get soft limit for the number of simultaneously opened files:

`ulimit -S -n`

- Set max per-user process limit:

`ulimit -u 30`

命   令：ulimit
功   能：控制shell程序的资源
    补充说明：ulimit为shell内建指令，可用来控制shell执行程序的资源。 
  
    参　　数：
    -a 　显示目前资源限制的设定。 
    -c <core文件上限> 　设定core文件的最大值，单位为区块。 
    -d <数据节区大小> 　程序数据节区的最大值，单位为KB。 
    -f <文件大小> 　shell所能建立的最大文件，单位为区块。 
    -H 　设定资源的硬性限制，也就是管理员所设下的限制。 
    -m <内存大小> 　指定可使用内存的上限，单位为KB。 
    -n <文件数目> 　指定同一时间最多可打开的文件数。 
    -p <缓冲区大小> 　指定管道缓冲区的大小，单位512字节。 
    -s <堆栈大小> 　指定堆叠的上限，单位为KB。 
    -S 　设定资源的弹性限制。 
    -t <CPU时间> 　指定CPU使用时间的上限，单位为秒。 
    -u <进程数目> 　用户最多可启动的进程数目。 
    -v <虚拟内存大小> 　指定可使用的虚拟内存上限，单位为KB。

    解除 Linux 系统的最大进程数和最大文件打开数限制：
        vi /etc/security/limits.conf
        # 添加如下的行
        * soft noproc 11000
        * hard noproc 11000
        * soft nofile 4100
        * hard nofile 4100 
       说明：* 代表针对所有用户
            noproc 是代表最大进程数
            nofile 是代表最大文件打开数 

