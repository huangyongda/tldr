# ifconfig

> Network Interface Configurator.

- View network settings of an ethernet adapter:

`ifconfig eth0`

- Display details of all interfaces, including disabled interfaces:

`ifconfig -a`

- Disable eth0 interface:

`ifconfig eth0 down`

- Enable eth0 interface:

`ifconfig eth0 up`

- Assign IP address to eth0 interface:

`ifconfig eth0 {{ip_address}}`

-静态ip设置 编辑文件 /etc/sysconfig/network-scripts/ifcfg-eth0 并设置内容

DEVICE=eth0
HWADDR=00:0C:29:2E:36:16
TYPE=Ethernet
ONBOOT=yes(默认为no,修改为yes意为每次reboot后 ifup eth0)
MM_CONTROLLED=yes(默认)
#BOOTPROTO=dhcp(dhcp为自动分配ip地址,我们把他注释了，在下面另外加)
BOOTPROTO=static
IPV6INIT=no
USERCTL=no
IPADDR=192.168.164.100
NETMASK=255.255.255.0


