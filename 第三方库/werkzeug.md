# Werkzeug

>Author: Sylvie233
>
>Date: 24/03/09



Python WSGI（Web Server Gateway Interface）工具库


## 基础介绍

### WSGI

![[Pasted image 20240309193118.png]]

```python
# WSGI入门函数
def application(environ, start_response):  
	status = '200 OK'  
	output = 'World!'  
	response_headers = [('Content-type', 'text/plain'),  
                      ('Content-Length', str(12)]  
	write = start_response(status, response_headers)  
	write('Hello ')  
	return [output]
```


### ASGI

#### uvicorn
```
uvicorn:
	
```









## 核心内容

```
uvicorn:
	run():
werkzeug:
	contrib:
		session:
	exceptions:
		BadRequest:
		INTERNAL_SERVER_ERROR:
		MethodNotAllowed:
		NotFound:
	security:
		check_password_hash():
		generate_password_hash():
	test:
		Client:
			get():
			post():
				data:
	Middleware:
	Request:
		args:
		headers:
		path:
		remote_addr:
	Response:
		data:
		headers:
		respnse:
		status:
		status_code:
	url_for():
```

