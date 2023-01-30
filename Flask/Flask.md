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


# 指定项目目录
chdir = /www/wwwroot/xxx
wsgi-file = %(chdir)/app.py
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





## 核心内容

## API