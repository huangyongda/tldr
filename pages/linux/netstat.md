# netstat

> Displays various networks related information such as open connections, open socket ports etc.

- List all ports:

`netstat -a`

- List all listening ports:

`netstat -l`

- List listening TCP ports:

`netstat -t`

- Display PID and program names:

`netstat -p`

- List information continuously:

`netstat -c`

- List routes and do not resolve IP to hostname:

`netstat -rn`

- List listening TCP and UDP ports (+ user and process if you're root):

`netstat -lepunt`

- 查看端口

`netstat -ano `
-  参数说明
　　-t : 指明显示TCP端口

　　-u : 指明显示UDP端口

　　-l : 仅显示监听套接字(所谓套接字就是使应用程序能够读写与收发通讯协议(protocol)与资料的程序)

　　-p : 显示进程标识符和程序名称，每一个套接字/端口都属于一个程序。

　　-n : 不进行DNS轮询(可以加速操作)
