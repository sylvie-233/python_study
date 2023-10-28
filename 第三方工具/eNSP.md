# eNSP基础

> Author: Sylvie233
>
> Date: 23/2/3
>
> Point: 
>
> ​	网工达叔最新全集：P2

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



网络可靠性





### AAA

Authentication、Authorization、Accounting

用户、NAS、AAA服务器

<img src="eNSP.assets/image-20230414180556174.png" alt="image-20230414180556174" style="zoom:67%;" />





#### RADIUS

<img src="eNSP.assets/image-20230414180921959.png" alt="image-20230414180921959" style="zoom:67%;" />





### ACL

规则集合



<img src="eNSP.assets/image-20230414174835137.png" alt="image-20230414174835137" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414174935660.png" alt="image-20230414174935660" style="zoom:67%;" />



通配符（反掩码）

<img src="eNSP.assets/image-20230414175158194.png" alt="image-20230414175158194" style="zoom:67%;" />



规则编号

<img src="eNSP.assets/image-20230414175622051.png" alt="image-20230414175622051" style="zoom:67%;" />



ACL分类

<img src="eNSP.assets/image-20230414175657099.png" alt="image-20230414175657099" style="zoom:67%;" />



匹配规则

<img src="eNSP.assets/image-20230414175917249.png" alt="image-20230414175917249" style="zoom:67%;" />





### 堆叠

堆叠、集群

iStack、CSS

<img src="eNSP.assets/image-20230414174653639.png" alt="image-20230414174653639" style="zoom:67%;" />







### LACP

链路聚合、LACP

<img src="eNSP.assets/image-20230414172458416.png" alt="image-20230414172458416" style="zoom:67%;" />



LACP

<img src="eNSP.assets/image-20230414173106506.png" alt="image-20230414173106506" style="zoom:67%;" />







### vlan

隔离广播域、mac帧的vlan标记



Vlan虚拟局域网

交换机中使用vlan，默认划分到编号为1的vlan域中

交换机之间的Trunk模式

vlan数据帧

<img src="eNSP.assets/image-20230209003310619.png" alt="image-20230209003310619" style="zoom:67%;" />



接口类型

<img src="eNSP.assets/image-20230209003904621.png" alt="image-20230209003904621" style="zoom:67%;" />



**单臂路由**



**vlanif**

vlanif接口可配置ip



交换机实现三层交换

<img src="eNSP.assets/image-20230414162105863.png" alt="image-20230414162105863" style="zoom:67%;" />



### STP

生成树、交换机、防环、二层环路、

<img src="eNSP.assets/image-20230414163658489.png" alt="image-20230414163658489" style="zoom:67%;" />





动态响应网络拓扑变化调整阻塞接口

桥ID（BID）、根桥（BID最小值）、根端口

<img src="eNSP.assets/image-20230414163738262.png" alt="image-20230414163738262" style="zoom:67%;" />



根桥

<img src="eNSP.assets/image-20230414164432710.png" alt="image-20230414164432710" style="zoom:67%;" />



Cost开销

<img src="eNSP.assets/image-20230414164525604.png" alt="image-20230414164525604" style="zoom: 67%;" />

RPC根路径开销

<img src="eNSP.assets/image-20230414164735341.png" alt="image-20230414164735341" style="zoom:67%;" />



Port ID 接口ID

<img src="eNSP.assets/image-20230414164845413.png" alt="image-20230414164845413" style="zoom:67%;" />



BPDU

<img src="eNSP.assets/image-20230414165018197.png" alt="image-20230414165018197" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414165129662.png" alt="image-20230414165129662" style="zoom:67%;" />

BPDU比较

<img src="eNSP.assets/image-20230414165738345.png" alt="image-20230414165738345" style="zoom:67%;" />



STP接口状态

<img src="eNSP.assets/image-20230414170834812.png" alt="image-20230414170834812" style="zoom:67%;" />









#### RSTP

<img src="eNSP.assets/image-20230414171538005.png" alt="image-20230414171538005" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414171755077.png" alt="image-20230414171755077" style="zoom:67%;" />



边缘端口

<img src="eNSP.assets/image-20230414171656100.png" alt="image-20230414171656100" style="zoom:67%;" />











#### MSTP





### telnet

```
telnet:
```



### NAT

网络地址转换

<img src="eNSP.assets/image-20230414181733070.png" alt="image-20230414181733070" style="zoom:67%;" />



地址转换表



#### 静态NAT

<img src="eNSP.assets/image-20230414181856639.png" alt="image-20230414181856639" style="zoom:67%;" />





#### 动态NAT

地址池

<img src="eNSP.assets/image-20230414182012458.png" alt="image-20230414182012458" style="zoom:67%;" />



#### NAPT

利用端口转换扩大ip的利用率

![image-20230414182302651](eNSP.assets/image-20230414182302651.png)



#### Easy IP

<img src="eNSP.assets/image-20230414182704655.png" alt="image-20230414182704655" style="zoom:67%;" />





NAT Server



### DHCP

<img src="eNSP.assets/image-20230414192708922.png" alt="image-20230414192708922" style="zoom:67%;" />



<img src="eNSP.assets/image-20230414192749908.png" alt="image-20230414192749908" style="zoom:67%;" />



租期更新

<img src="eNSP.assets/image-20230414192909859.png" alt="image-20230414192909859" style="zoom:67%;" />





### FTP

主动模式

<img src="eNSP.assets/image-20230414183133328.png" alt="image-20230414183133328" style="zoom:67%;" />



被动模式

<img src="eNSP.assets/image-20230414183420095.png" alt="image-20230414183420095" style="zoom:67%;" />





#### TFTP

<img src="eNSP.assets/image-20230414192247462.png" alt="image-20230414192247462" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414192342419.png" alt="image-20230414192342419" style="zoom:67%;" />





### DNS

DNS查询

<img src="eNSP.assets/image-20230414194313801.png" alt="image-20230414194313801" style="zoom:67%;" />





### HTTP





### NTP

时钟同步

<img src="eNSP.assets/image-20230414194554388.png" alt="image-20230414194554388" style="zoom:67%;" />



<img src="eNSP.assets/image-20230414194606523.png" alt="image-20230414194606523" style="zoom:67%;" />



### PPP

wan广域网

<img src="eNSP.assets/image-20230414205025713.png" alt="image-20230414205025713" style="zoom:67%;" />

​		

<img src="eNSP.assets/image-20230414205141278.png" alt="image-20230414205141278" style="zoom:67%;" />

PPP链路连接

<img src="eNSP.assets/image-20230414205231895.png" alt="image-20230414205231895" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414205330121.png" alt="image-20230414205330121" style="zoom:67%;" />

LCP协商

<img src="eNSP.assets/image-20230414205422363.png" alt="image-20230414205422363" style="zoom:67%;" />

认证协商

PAP认证

<img src="eNSP.assets/image-20230414205612564.png" alt="image-20230414205612564" style="zoom:67%;" />

CHAP认证

<img src="eNSP.assets/image-20230414205709185.png" alt="image-20230414205709185" style="zoom:67%;" />



NCP协商

静态IP地址协商

<img src="eNSP.assets/image-20230414205801864.png" alt="image-20230414205801864" style="zoom:67%;" />



#### PPPoE

以太网PPP协议

<img src="eNSP.assets/image-20230414210329718.png" alt="image-20230414210329718" style="zoom:67%;" />



PPPoE会话

<img src="eNSP.assets/image-20230414210720858.png" alt="image-20230414210720858" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414210845327.png" alt="image-20230414210845327" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414210906827.png" alt="image-20230414210906827" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414210924167.png" alt="image-20230414210924167" style="zoom:67%;" />



PPPoE报文

<img src="eNSP.assets/image-20230414210817800.png" alt="image-20230414210817800" style="zoom:67%;" />







### WLAN

<img src="eNSP.assets/image-20230414194708642.png" alt="image-20230414194708642" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414195349172.png" alt="image-20230414195349172" style="zoom:67%;" />



wifi版本

<img src="eNSP.assets/image-20230414195501117.png" alt="image-20230414195501117" style="zoom:67%;" />





wlan组网

<img src="eNSP.assets/image-20230414200057136.png" alt="image-20230414200057136" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414200657566.png" alt="image-20230414200657566" style="zoom:67%;" />



#### 有线侧组网

<img src="eNSP.assets/image-20230414200743921.png" alt="image-20230414200743921" style="zoom:67%;" />



#### 无线侧组网

##### BSS、SSID、BSSID

<img src="eNSP.assets/image-20230414201559966.png" alt="image-20230414201559966" style="zoom:67%;" />

##### VAP

<img src="eNSP.assets/image-20230414201728460.png" alt="image-20230414201728460" style="zoom:67%;" />

##### ESS

使用同一个SSID、实现漫游

<img src="eNSP.assets/image-20230414201830116.png" alt="image-20230414201830116" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414204800686.png" alt="image-20230414204800686" style="zoom:67%;" />









#### AC、AP

AC可用作三层交换机使用

<img src="eNSP.assets/image-20230414200330875.png" alt="image-20230414200330875" style="zoom:67%;" />

<img src="eNSP.assets/image-20230414200352861.png" alt="image-20230414200352861" style="zoom:67%;" />

PoE交换机

<img src="eNSP.assets/image-20230414200514243.png" alt="image-20230414200514243" style="zoom:67%;" />



双频信号：2.4G、5G





AC与AP连接

<img src="eNSP.assets/image-20230414202524595.png" alt="image-20230414202524595" style="zoom:67%;" />

AC与AP连通性

<img src="eNSP.assets/image-20230414202553022.png" alt="image-20230414202553022" style="zoom:67%;" />

AC配置WLAN参数

<img src="eNSP.assets/image-20230414202701865.png" alt="image-20230414202701865" style="zoom:67%;" />

AP加入AP组

<img src="eNSP.assets/image-20230414202739983.png" alt="image-20230414202739983" style="zoom:67%;" />





#### CAPWAP

<img src="eNSP.assets/image-20230414200938110.png" alt="image-20230414200938110" style="zoom:67%;" />





### 硬件

#### 交换机

##### 框式交换机

<img src="eNSP.assets/image-20230414172235472.png" alt="image-20230414172235472" style="zoom:67%;" />![image-20230414172256618](eNSP.assets/image-20230414172256618.png)

<img src="eNSP.assets/image-20230414172301388.png" alt="image-20230414172301388" style="zoom:67%;" />











#### 路由器









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
aaa: 
	local-user: 用户配置	
		ftp-directory:
			flash:
		password: 用户密码
			cipher:
		privilege: 用户级别
			level:
		service-type:
			ftp:
			telnet:
	---
	domain:
		---
		
acl:
	name:
	number:
	basic:
		rule:
			permit:
				source:
	---
	rule:
		deny:
			ip:
				destination:
				source:
				
bgp:
clock:
	datetime:
dhcp:
	enable
	
dir:
	
display:
	acl:
		all: 
	clock:
	configuration:
		candidate:
	current-configuration:
	domain:
		name:
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
	
ftp:
	server:
		enable:
	---
	get:
	
info-center:
	logfile:
	
interface:
	GigabitEthernet:
		x/x/x: 指定端口
		---
		arp:
			broadcast:
				enable:
		dhcp:
			select: 选择自定义地址池
				global:
				interface:
			server:
				dns-list: 配置dns服务器ip
				excluded-ip-address:
				lease:
		dot1q: 子接口vlan配置
			termination:
				vid:
		ip:
			address: 给接口配置ip
		link-protocol:
			ppp:
		nat:
			outbound:
				address-group: 使用指定的地址池
			server:
				global:
				inside:
        ospf:
        	cost:
        ping:
        ppp:
        	authentication-mode:
        		pap:
        	pap:
        		local-user:
        		password:
        quit:
        traffic-filter: 通行过滤（应用acl）
        	inbound:
        		acl:
        	outbound:
        		acl:
    LoopBack:
    	
ip:
	policy-based-route:
	pool: 地址池
        ---
        dns-list:
        gateway-list:
        lease:
        mask:
        network:
	route-static: 静态路由配置
	
nat:
	address-group: 地址池
	
ospf:
	area:
		network:
			
	router-id:
	
reboot:

sysname: 设备名

system-view: 进入系统视图（默认用户视图）

telnet: 远程连接路由器
	server:
		enable: 开启telnet服务
		
tftp:
		
undo: 方向操作
	ip:
		address: 删除ip地址
		
		
user-interface:
	vty: 开启远程管理连接
        ---
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
	stp:
		brief:
	
interface:
	x/x/x:
	eth-trunk:
		least:
			active-linknumber:
		max:
			active-linknumber:
		mixed-rate:
		mode:
			lacp:
		trunkport:
	
	lacp:
		priority:
	mac-vlan:
		enable:
	traffic-filter:
		inbound:
			acl: 指定acl规则
				name:
    port:
        default:
            vlan: 设置端口的vlan划分
        eth-trunk:
        hybrid:
        	tagged:
        		vlan:
        	untagged:
        		vlan:
        link-type:
            access:
            trunk:
        pvid:
        	vlan:
        trunk:
            allow-pass:
                vlan:
                    all:
            pvid:    
    quit:
    stp:
    	cost:
 
lacp:
	priority:

stp:
	mode:
		stp:
		rstp:
		mstp:
	pathcost-standard:
	priority:
		
	root:
		primary:
		secondary:
		

vlan: 创建vlan区域
	batch:
```



### AC

```
capwap:
	source:
		interface:
			Vlanif:

wlan:
	---
	ap-group:
		name:
			---
			radio: 所有信号（2.4G、5G）
				all:
			vap-profile: ap组关联vap配置模板
			wlan:
	ap-id:
        ap-mac:
            ---
            ap-group: ap加入到ap组中
            ap-name:
	security-profile:
		name:
			---
			security:
				wpa-wpa2:
					psk:
						pass-phrase:
							aes:
	ssid-profile:
		name: 配置模板名称
            ---
            ssid: 配置wlan名称
    vap: vap配置信息
    	name:
    		---
    		forward-mode:
    			tunnel:
    		security-profile:
    		service-vlan:
    			vlan-id:
    		ssid-profile:
```



### AP

```

```





### VRP

华为硬件操作系统

<img src="eNSP.assets/image-20230206213227548.png" alt="image-20230206213227548" style="zoom:67%;" />

文件系统、存储设备、



Console控制、设备调试

设备com口



![image-20230206221723439](eNSP.assets/image-20230206221723439.png)

















