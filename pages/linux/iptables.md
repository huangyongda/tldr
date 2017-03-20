# iptables
> Program that allows to configure tables, chains and rules provided by the Linux kernel firewall.

- See chains and rules for specific table:

`sudo iptables -t {{table_name}} -vnL`

- Set chain policy rule:

`sudo iptables -p {{chain}} {{rule}}`

- Append rule to chain policy for IP:

`sudo iptables -A {{chain}} -s {{ip}} -j {{rule}}`

- Append rule to chain policy for IP considering protocol and port:

`sudo iptables -A {{chain}} -s {{ip}} -p {{protocol}} --dport {{port}} -j {{rule}}`

- Delete chain rule:

`sudo iptables -D {{chain}} {{rule_line_number}}`

- Save iptables configuration:

`sudo iptables-save > {{path/to/iptables_file}}`


- config file : /proc/sys/net/ipv4/ip_forward，该文件内容为0，表示禁止数据包转发，1表示允许
- 端口转发  demo: 转发 192.168.1.147 的 43999端口转到22端口 实现用43999登录ssh

`iptables -t nat -A PREROUTING -p tcp -i eth0 -d 192.168.1.147 --dport 43999 -j DNAT --to 192.168.1.147:22`

- 端口转发  demo: 转发 192.168.11.105 的 9001端口转到9000端口

`iptables -t nat -A PREROUTING -d 192.168.11.105 -p tcp --dport 9001 -j DNAT --to 192.168.11.105:9000`

- 端口转发   ip伪装

`iptables -t nat -A POSTROUTING -j MASQUERADE`

