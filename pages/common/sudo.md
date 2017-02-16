# sudo

> Execute a command as another user.

- List of an unreadable directory:

`sudo {{ls}} {{/usr/local/scrt}}`

- To edit a file as user www:

`sudo -u {{www}} {{vi}} {{/var/www/index.html}}`

- To shutdown the machine:

`sudo {{shutdown}} -h +10 {{"Cya soon!"}}`

- To repeat the last command as sudo:

`sudo {{!!}}`

- 查看当前用户可用的sudo命令列表

`sudo -l`

- 删除之前sudo命令输入的密码记录使密码失效

`sudo -k`

- 配置 /etc/sudoers 文件
  chmod +w /etc/sudoers
  格式:UserName  Ip=（Who）    [NOPASSWD:]Command
`huangyd 192.168.10.250=(root) NOPASSWD: /bin/cat,/bin/ls`

