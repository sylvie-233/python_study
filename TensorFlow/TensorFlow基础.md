# TensorFlow基础

>Author: Sylvie233
>
>Date: 2022/11/29
>

[TOC]

## 基础介绍

应用领域：

1. 图像识别
2. 语音识别
3. 自然语言处理
4. 机器自主



卷积神经网络、循环神经网络



CPU、GPU版本



数据流图



placeholder提供占位符，run()时提供值









### 张量

tensor，Tensorflow基本的数据类型

```
Tensor{"name", shape={}, dtype}
```

底层是numpy的ndarray

阶、数据类型

张量的形状

<img src="TensorFlow基础.assets/image-20221130003701047.png" alt="image-20221130003701047" style="zoom:67%;" />

基础数据类型

<img src="TensorFlow基础.assets/image-20221130003733632.png" alt="image-20221130003733632" style="zoom:67%;" />



















### 操作

operation操作（计算单位）

<img src="TensorFlow基础.assets/image-20221130001429033.png" alt="image-20221130001429033" style="zoom:67%;" />

默认会给运算符重载成op类型



形状的改变shape

动态形状、静态形状（是否生成新的张量）









### 变量







### 数据流图

一张图包含了一组op和tensor





### 会话

session

只能运行一张图











### 模型











## 常用API

### graph

```
graph:
	as_default():
```





### session

tf.Session()创建

```
session:
	graph
	close():
	run():
		fetchs: 运行的tensor
		feed_dict: tensor值覆盖（placeholder占位符）
```



### tensor

```
tensor:
	graph:
	name: 
	op: 操作
	shape: 形状
	
	eval(): 执行获取值
	set_shape(): 设置形状（设置后不可修改、不能跨维度）（静态形状）
```







### tensorflow

```
tensorflow:
	float32:
	
	------------------------------
	constant(): 
	ConfigProto():
	Graph():
	InteractiveSession():
	ones():
	ones_like():
		tensor:
		dtype:
		name:
	placeholder():
	random_normal(): 随机张量生成
		shape:
		mean:
		stddev:
		dtype:
		seed:
		name:
	Session():
		config:
		graph: 指定图
	zeros():
		shape: 形状
		dtype: 类型
		name: 名称
	------------------------------
	string_to_number():
	to_double():
	to_float():
	to_int32():
	to_int64():
	------------------------------
	add():
	cast(): 类型转换
		x:
		dtype:
		name:
    concat(): 拼接
    	values:
    	axis: （0: 增加行）
    expand_dims():
	fill():
	get_default_graph():
	rank():
	reshape(): 修改形状（生成新的张量）（动态形状）
		tensor: 
		shape:
	shape():
	size():
	squeeze():
	

	------------------------------
	





```

