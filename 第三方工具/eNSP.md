# eNSP基础

> Author: Sylvie233
>
> Date: 23/2/3
>
> Point: P91

[TOC]

## 基础介绍

HCIA、HCIP、HCIE





三层交换机

单臂路由



acl访问控制列表



nat网络地址转换

私网地址

```
:
	192.168.x.x:
	10.x.x.x:
	172.16.x.x~172.31.x.x:
```



datacom数据通信



Ethernet以太网：局域网技术



路由汇总



### vlan

隔离广播域、mac帧的vlan标记



Vlan虚拟局域网

交换机中使用vlan，默认划分到编号为1的vlan域中

交换机之间的Trunk模式

vlan数据帧

<img src="eNSP.assets/image-20230209003310619.png" alt="image-20230209003310619" style="zoom:67%;" />



接口类型

<img src="eNSP.assets/image-20230209003904621.png" alt="image-20230209003904621" style="zoom:67%;" />







### telnet

```
telnet:
```

















## 核心内容

### 主机

```
ipconfig:
ping:
```



### 服务器

```

```



### 路由器

```
aaa: 账号配置
	local-user:
		password:
			cipher:
		privilege:
			level:
		service-type:
			telnet:
acl:
	name:
	basic:
		rule:
			permit:
				source:
				
bgp:
clock:
	datetime:
dhcp:
	enable
display:
	acl:
		all: 
	clock:
	configuration:
		candidate:
	current-configuration:
	ip:
		interface:
		routing-table: 路由表
	ospf:
		lsdb:
		peer:
			brief:
	startup: 启动参数
	this: 显示设置
	vlan:
info-center:
	logfile:
interface:
	GigabitEthernet:
		x/x/x: 指定端口
		arp:
			broadcast:
				enable:
		dhcp:
			select:
				interface:
			server:
				dns-list: 配置dns服务器ip
		dot1q:
			termination:
				vid:
		ip:
			address: 给接口配置ip
		nat:
			outbound:
				address-group:
			server:
				global:
				inside:
        ospf:
        	cost:
        ping:
        quit:
    LoopBack:
    	
ip:
	route-static: 静态路由配置
nat:
	address-group:
ospf:
	area:
		network:
			
	router-id:
reboot:
sysname: 设备名
system-view: 进入系统视图（默认用户视图）
telnet:
	server:
		enable: 开启telnet服务
undo: 方向操作
	ip:
		address: 删除ip地址
user-interface:
	vty: 开启远程管理连接
		authentication-mode: 连接验证模式
			aaa: 账号+密码
            password:
```



### 交换机

```
acl:
	name:
	advance:
		rule:
			deny:
				ip:
					destination:
					source:
						any:
			permit:
display:
	mac-address:
interface:
	x/x/x:
	traffic-filter:
		inbound:
			acl: 指定acl规则
				name:
    port:
        default:
            vlan: 设置端口的vlan划分
        link-type:
            access:
            trunk:
        trunk:
            allow-pass:
                vlan:
                    all:
            pvid:
vlan: 创建vlan区域
	batch:
```





### VRP

华为硬件操作系统

<img src="eNSP.assets/image-20230206213227548.png" alt="image-20230206213227548" style="zoom:67%;" />

文件系统、存储设备、



Console控制、设备调试

设备com口



![image-20230206221723439](eNSP.assets/image-20230206221723439.png)

















