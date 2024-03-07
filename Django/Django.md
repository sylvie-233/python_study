# Django基础

> Author: Sylvie233
>
> Date: 23/1/22
>
> Point:  
>	Python-Django手把手从零开发个人博客：P26
> ​	


## 基础介绍


一个项目中可以有多个app应用




#### 目录结构

```
django项目：
	/项目目录:
		asgi.py
		settings.py
		urls.pu
		wsgi.py
	/app目录:
		/migrations: 数据库迁移文件
		/static: 静态文件
		/templates: 视图模板文件
		admin.py: 管理后台设置
		apps.py: 应用配置
		forms.py: ModelForm表单、字段校验
		models.py:
		tests.py:
		urls.py: 项目urls.py的子路由
		views.py: 视图逻辑处理函数
	/templates: 模板目录(公用)
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
	startproject: 脚手架项目
	
```





### manage.py

```
manage.py:
	collectstatic: 收集静态文件
	createsuperuser:
	makemigrations: 生成迁移文件
	migrate: 数据库迁移
	runserver: 运行服务
	shell:
		
	startapp: 创建app应用
	
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

#### settings.py

settings.py

```python
# 主机
ALLOWED_HOSTS = []


# 密码校验器
AUTH_PASSWORD_VALIDATORS = [
	{
		"NAME": 'django.contrib.auth.password_validation.UserAttributeSimilariryValidator'
	},
]

# 自定义认证处理
AuTHENTICATION_BACKENDS = (
	'xxx.backend'
)


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

# 邮箱配置
EMAIL_HOST = ""
EMAIL_HOST_USER = ""
EMAIL_HOST_PASSWORD = ""
EMAIL_PORT = 
EMAIL_USE_SSL = 

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

# 语言
LANGUAGE_CODE = 'zh-hans'

# log日志配置
LOGGING = {
	"version": 1,
	"disable_existing_loggers": False,
	"formatters": {
		"standard": {
			"format" "%(message)s"
		}
	},
	"filters": {
		"require_debug_true": {
			"{}": "django.utils.log.RequireDebugTrue"
		}
	},
	"handlers": {
		"null": {
			"level": "DEBUG",
			"class": "logging.NullHandler",
		},
		"debug": {
			"level": "DEBUG",
			"class": "logging.handlers.RotatingFileHandler",
			"filename": os.path.join(BASE_DIR, "log", "debug.log"),
			"maxBytes": 1024 * 1024 * 5,
			"backupCount": 5,
			"formatter": "standard",
		}
	},
	"loggers": {
		"django.request": {
			"handlers": ["debug"],
			"level": "DEBUG",
			"propagate": True,
		}
	}
}

# media媒体文件目录
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



#### urls.py

urls.py

视图函数映射（控制器）

```python
urlpatterns = [
	path("/xxx", xx.xx.xx)
] + static()
```



#### asgi.py

asgi.py

```

```



#### wsgi.py

wsgi.py

```

```







### View
```
:
	
```

#### 视图函数


在`urls.py`中映射VIew视图函数
```python
from django.urls import path

urlpatterns = [
	path("xxx/<int:xxx>", views.xxx, name="xxx")
]

```


#### request

```

```













### Jinja2

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

# if 条件显示
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


# 用户认证
{% user.is_authenticated %}



内置变量/函数:
	date:
	safe: 字符串转html
	static: 静态资源引用
	url: 反向引用url
	user:
	
```


django模板引擎


#### 过滤器


#### 自定义标签
```python
from django.template import Library

register -Library()

@register.simple_tag
def xxx_tag():
	return xxx

```

### ORM

安装`mysqlclient`依赖

`models.py`定义实体模型

数据库迁移



```
自动生成表:
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



#### Model

`Model实例`

```
Model实例:
	objects:
		all():
		create():
		filter():
		get():
			xxx__contains:
			xxx__gt:
			xxx__gte:
			xxx__startswith:
			QuerySet:
                delete():
                first():
                update():
        
	---
    delete():
	save():
```



`Model定义`

```
django.db.models:
	CharField:
		max_length:
	ForeignKey:
```



#### 一对一关联
```python
models. OneToOneField()
```



### ModelForm
```python

```

input集合、字段校验







### Middleware

装饰器实现


Csrf中间件




### Admin
```
:
	
```

后台管理界面




### 辅助功能






### 第三方插件







### DRF


restful风格






## API

### django

```
django:
	apps:
		AppConfig:
			name:
			verbose_name:
	conf:
		settings: 配置
		urls:
			static:
				static():
					document_root:
	contrib:
    	admin:
    		site:
    			site_header:
    			register(): 管理界面注册模型
    			unregister(): 取消注册模型
    		
    		ModelAdmin: 模型管理
	    		Media: 静态资源
		    		css:
		    		js:
    			fields:
    			fieldset:
    			inlines:
    			list_display: （）
    			list_filter:
    			search_fields:
    		StackedInline: 管理界面显示模型
	    		model: 
    		register():
    	auth:
	    	admin:
		    	UserAdmin:
		    backends:
			    ModelBackend:
				    
	    	models:
		    	User:
		    authenticate(): 认证 
			    request:
			    username:
			    password:
		    login(): 登录
			    request:
				user:
	core:
		exceptions:
			ValidationError:
		mail:
			send_mail(): 发送邮件
		paginator:
			Paginator:
				---
				get_page():
					---
					has_next():
					has_previous():
		validators:
			RegexValidator:
	db: // orm框架
		backends:
			mysql:
		models:
			CASCADE: 级联操作
            BigAutoField:
            BooleanField:
            CharField:
	            blank:
	            choices: 二元组选项
	            default:
	            max_length:
	        DateField:
		        null:
            DateTimeField:
            DecimalField:
            F: 并发字段处理
            FileField:
                upload_to:
            ForeignKey:
                to:
                to_field:
                ondelete:
            ImageField:
	            upload_to:
            IntergerField:
            ManyToManyField:
            OneToOneField:
	            on_delete:
	            verbose_name:
            PositiveIntegerField:
	            choices:
            Q:
            SmallIntegerField:
                choices:
			---
            Model:
	            Meta:
		            verbose_name:
		            verbose_name:plural:
				__str__():
            	---
                objects:
                    all():
                    create():
                    dates(): 日期归档
                    exclude():
                    filter():
               		get():
               		update():
	               		xxx:
		               		__contains:
		               		__gt:
		               		__gte:f
		               		__lt:
		               		
                        QuerySet:
                            delete():
                            exists():
                            first():
                            get_xxx_display():
                            last():
                            order_by():
                            update():
                            values():
                            valuee_list():
		transaction:
        	atomic():
        	commic():
        	rollback():
        	savepoint():
        	savepoint_commit():
        	savepoint_rollback():
	forms: // ModelForm表单、字段校验
		utils:
			ErrorDict:
		CharField:
            label:
            max_length:
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
        ImageField:
        	upload_to:
        	verbose_name:
        IntegerField:
        ModelForm:
            Meta:
                fields: 显示的字段
                model: 模型
                widgets: {
                    xxx": forms.TextInput()
                }
            as_p:
            as_table:
            as_ul:
            cleaned_data: 原始数据(字典)
            data:
            errors:
                as_json():
            xxx:
                label:
                errors:
            instance:
            clean_xxx(): 字段校验钩子函数
            delete():
            is_valid(): 字段校验
            save(): 生成Model
	            commit:
	            ---
	            save(): 
	            set_xxx():
        PasswordInput:
        TextInput:
            attrs: html属性
        ValidationError:
	http:
		HttpResponse:
		JsonResponse:
	middleware: 中间件
		csrf:
			CsrfViewMiddleware:
	shotcuts:
		HttpResponse
        redirect(): 重定向
		render():
			request:
			context:
	template:
		loader:
			get_template():
				---
				render():
			render_to_string():
		Library:
			---
			simple_tag(): 模板标签装饰器
	urls:
		include(): 包含子路由
		path():
			name:
		re_path():
		url(): 路由映射处理
	utils:
		deprecation:
			MiddlewareMixin:
                process_request():
                process_response():
        functional:
	        cached_property: 缓存装饰器
        log:
		safestring:
			mark_safe():
	views:
		decorators:
            csrf:
                csrf_exempt(): 取消csrf（装饰器）

---
request:
	FILES:
		name:
		chunks():
		get():
	GET:
		[]:
		urlencode():
	POST:
		[]:
	method: 请求方法
	path_info:
	session:
		clear():
		set_expiry():
```



### restful_framework

```
restful_framework:
	
```









