# Django基础

> Author: Sylvie233
>
> Date: 23/1/22
>
> Point: P26

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







### django-admin

```
django-admin:
	startproject
```





### manage.py

```
manage.py:
	makemigrations:
	migrate:	
	runserver:
	startapp:
	
```









## 核心内容

### 项目配置

#### settings配置

settings.py

```
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

# 静态目录
STATIC_URL = "/static/"

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

# WSGI
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
			QuerySet:
                delete():
                first():
                update():
```









































## API(django)

```
request:
	GET:
	POST:
	method:
	

```

### apps

#### AppConfig







### contrib

#### admin



### db

#### backends:

```
django.db.backends:
	mysql:
```



#### models

```
django.db.models:
	CASCADE:
	BigAutoField:
	CharField:
	DateTimeField:
	DecimalField:
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
            filter():
                QuerySet:
                    delete():
                    first():
                    update():
```





### shortcuts

#### HttpResponse

#### redirect

#### render





### urls

#### path













