# Numpy基础

>Author: Sylvie233
>
>Date: 2022/11/27
>
>Point: 

[TOC]

## 基础介绍





## Numpy

安装：

```

```



常用API：

```
numpy:


```







## Pandas

安装：

```


import pandas as pd
```



交叉表



常用API：

```
pandas:
	
数据读取：
	read_csv():
	merge(t1, t2, on=[k1, k2])
	
类型转换：
	DatetimeIndex(): 日期格式拆分
	to_datetime():
		date:
		unit: 's'/
	
交叉表：
	crosstab(c1, c2): （c1为新行、c2为新列）

实例：
	count(): 计数
	drop(): 删除列
		[列名]:
		axis:
	fillna(): 缺失值填充
	groupby(): 分组 
	head(n): 查看前n行
	isin(): in过滤
	mean(): 平均值
	query(): 条件查询
	reset_index(): 重置index列
```



























