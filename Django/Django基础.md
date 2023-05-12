# Django基础

> Author: Sylvie233
>
> Date: 23/1/22
>
> Point: P

[TOC]

## 基础介绍



项目目录结构：

```
django项目：
	/项目目录:
		asgi.py
		settings.py
		urls.pu
		wsgi.py
	/app目录:
		/migrations:
		admin.py:
		apps.py:
		models.py:
		tests.py:
		views.py:
	/templates:
	manage.py:
```







nginx的uwsgi代理

```
location /xxx {
	uwsgi_pass x.x.x.x:x;
	include uwsgi_params;
}
```



django数据库表

```
:
	django_content_type:
	auth_user:
	auth_permission:
	auth_group: 权限组
	auth_user_user_permissions:
	auth_user_group:
	auth_group_permissions:
	django_admin_log:
```









### django-admin

```
django-admin:
	startproject
```





### manage.py

```
manage.py:
	collectstatic: 收集静态文件
	createsuperuser:
	makemigrations:
	migrate:	
	runserver:
	startapp:
	
```



### uwsgi

```
uwsgi:
	--ini: 指定配置文件
	--reload:
	--stop:
```



#### uwsgi.ini

```ini
[uwsgi]
master = true
processes = 1
threads = 2


# 指定项目目录
chdir = /www/wwwroot/xxx
wsgi-file = %(chdir)/xxx/wsgi.py
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
	
```









## 核心内容

### 项目配置

#### settings配置

settings.py

```
# 主机
ALLOWED_HOSTS = []

# 项目根目录
from pathlib import Path
BASE_DIR = Path(__file__).resolve().parent.parent

# 缓存
CACHES = {
	"default": {
		"BACKEND": "django.core.cache.backends.locmem.LocMemCache",
		"LOCATION":
	}
}

# 数据库
DATABASES = {
	"default": {
		"ENGINE": "django.db.backends.mysql",
		"NAME": "",
		"USER": "",
		"PASSWORD": ""
		"HOST": "",
		"PORT": ""
	}
}

# 调试模式
DEBUG = True

# 已安装的app应用
INSTALLED_APPS = [
	"django.contrib.admin",
	"django.contrib.auth",
	"django.contrib.contenttypes",
	"django.contrib.sesstions",
	"django.contrib.messages",
	"django.contrib.staticfiles",
	“自定义应用AppConfig”
]

# medi
MEDIA_ROOT = /xxx
MEDIA_URL = "/xx"

# 中间件
MIDDLEWARE = [
	"django.middleware.security.SecurityMiddleware",
	"django.contrib.sessions.middleware.SessionMiddleware",
	"django.middleware.common.CommonMiddleware",
	"django.middleware.csrf.CsrfViewMiddleware",
	"django.contrib.auth.middleware.AuthenticationMiddleware",
	"django.contrib.messages.middleware.MessageMiddleware",
	"django.middleware.clickjacking.XFrameOptionsMiddleware",
]

# url映射
ROOT_URLCONF = "xxx.urls"

# 密钥
SECRET_KEY = "xxx"

# 静态目录
STATIC_ROOT = os.path.join()
STATIC_URL = "/static/"
STATICFILES_DIRS = []

# 模板配置
TEMPLATES = [
	{
		"BACKEND": "django.template.backends.django.DjangoTemplates",
		"DIRS": [],
		"APP_DIRS": True,
		"OPTIONS": {
			"context_processors": [
				"django.template.context_processors.debug",
				"django.template.context_processors.request",
				"django.contrib.auth.context_processors.auth",
				"django.contrib.messages.context_processors.messages",
			]
		}
	}
]

# WSGI入口
WSGI_APPLICATION = "xxx.wsgi.applicaion"
```



#### urls配置

urls.py

视图函数映射（控制器）

```
urlpatterns = [
	path("/xxx", xx.xx.xx)
]
```



#### asgi配置

asgi.py

```

```



#### wsgi配置

wsgi.py

```

```





### 模板引擎



```
# 静态文件
{% load static %}
{% static "xxx/xxx" %}

# 变量
{{ xxx }}
{{ xxx.0 }}
{{ xxx.xxx }}
{{ request }}

# for循环
{% for it in items %}
{% endfor %}
## 字典 .keys|.values|.items

# if
{% if  %}
{% elif %}
{% else %}
{% endif %}

# csrf（csrfmiddlewaretoken）
{% csrf_token %}

# 模板函数
date

# 继承
{% block xxx %} {% endblock %}
{% extends "xxx.html" %}

```



### ORM

安装`mysqlclient`依赖

`models.py`定义实体模型

数据库迁移

自动生成表

```
auth_group
auth_group_permissions
auth_permission
auth_user
auth_user_groups
auth_user_user_permissions:
django_admin_log
django_content_type
django_migrations
django_session
```



Model实例

```
Xxx:
	objects:
		all():
		create():
		filter():
			xxx__contains:
			xxx__gt:
			xxx__gte:
			xxx__startswith:
			QuerySet:
                delete():
                first():
                update():
```







### ModelForm

input集合

字段校验







### 中间件

装饰器实现























## API

### django

```
django:
	apps:
		AppConfig
	conf:
		settings
	contrib:
    	admin:
	core:
		exceptions:
			ValidationError:
		validators:
			RegexValidator:
	db: // orm框架
		backends:
			mysql:
		models:
			CASCADE:
            BigAutoField:
            CharField:
            DateTimeField:
            DecimalField:
            FileField:
                upload_to:
            ForeignKey:
                to:
                to_field:
                ondelete:
            IntergerField:
            SmallIntegerField:
                choices:

            Model:
                objects:
                    all():
                    create():
                    exclude():
                    filter():
                        QuerySet:
                            delete():
                            exists():
                            first():
                            get_xxx_display():
                            order_by():
                            update():
                            values():
                            valuee_list():
	forms: // ModelForm
		CharField:
            label:
            validators:
            widget:
        FileField:
        Form:
            cleaned_data:
            data:
            files:
            xxx:
            add_error():
            clean_xxx():
            is_valid():
        IntegerField:
        ModelForm:
            Meta:
                fields:
                model:
                widgets: {
                    xxx": forms.TextInput()
                }
            cleaned_data:
            data:
            errors:
                as_json():
            xxx:
                label:
                errors:
            instance:
            clean_xxx(): 字段钩子函数
            is_valid():
            save():
        PasswordInput:
        TextInput:
            attrs:
		utils:
			ErrorDict:
	http:
		JsonResponse:
	shotcuts:
		HttpResponse
        redirect
		render
	urls:
		path():
		re_path():
	utils:
		deprecation:
			MiddlewareMixin:
                process_request():
                process_response():
		safestring:
			mark_safe():
	views:
		decorators:
            csrf:
                csrf_exempt():







request:
	FILES:
		name:
		chunks():
	GET:
		urlencode():
	POST:
	method:
	path_info:
	session:
		clear():
		set_expiry():
```









