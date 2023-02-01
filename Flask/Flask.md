# Flask基础

> Author: Sylvie233
>
> Date: 23/1/29
>
> Point: P56

[TOC]

## 基础介绍



### uwsgi.ini

```ini
[uwsgi]
master = true
processes = 1
threads = 2

# 虚拟环境目录
home = /xxx
# 指定项目目录
chdir = /www/wwwroot/xxx
wsgi-file = %(chdir)/app.py
callable = app
# http = x.x.x.x:x
socket = x.x.x.x:x


logto = /xxx
chmod-socket = 660
vacuum = true
max-request = 1000

# uwsgi的运行状态
stats = %(chdir)/uwsti.status
pidfile = %(chdir)/uwsgi.pid
```



### gunicorn

```
gunicorn:
	-b: 监听地址
	-c: .py配置文件
	-D: 后台运行
	-h:
	-v:
	-w: 进程数
	--access-logfile:
	--error-logfile:
	xxx: 文件
		xxx: 对象
	
```









## 核心内容

## API