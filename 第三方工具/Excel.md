# Excel基础

> Author: Sylvie233
>
> Date: 23/2/23
>
> Point: 
>
> ​	【Excel高阶】宏与VBA，办公自动化！：P15
> ​	【PPT教程】WPS2019全套新手自学教程，从零基础开始超详细讲解（完结）：P34
> 	【文字教程】WPS2019全套新手自学教程，从零开始超详细讲解（完结）：P5

## 基础介绍

快速填充、原位填充



快速分析



### 文件



### 开始

#### 剪切板

#### 字体

#### 对齐方式

##### 自动换行



#### 数字

##### 常规

##### 数值

##### 货币

##### 文本

##### 百分比

##### 日期

##### 时间

##### 分数

##### 科学计数

##### 特殊

##### 自定义

```
自定义:
	0:
	#:
	?:
	@:
	;:
```







#### 样式

##### 条件格式

```
条件格式:
	突出显示单元格规则:
	最前/最后规则:
	数据条:
	色阶:
	图标集:
	新建规则:
	清除规则:
	管理规则:
```





#### 单元格

##### 插入

##### 删除

##### 格式



#### 编辑

##### 自动求和

```
自动求和:
	其他函数:
```



##### 清除

##### 排序和筛选

```
排序和筛选:
	升序:
	降序:
	自定义排序:
	筛选:
```



##### 查找和选择

```
查找和选择:
	查找:
	替换:
	转到:
	定位条件:
		批注:
		常量:
		公式:
		空值:
		可见单元格:
	选择对象:
```





### 插入

#### 表格

#### 插图

#### 加载项

#### 图表

#### 演示

#### 迷你图

##### 折线

##### 柱形

##### 盈亏



#### 筛选器

#### 链接

#### 批注

#### 文本

#### 符号



### 页面布局

#### 主题

#### 页面设置

##### 打印标题



#### 调整为合适大小

#### 工作表选项

#### 排列



### 公式

#### 函数库

##### 文本



#### 定义的名称

#### 公式审核

#### 计算



### 数据

有效性可以设置数据校验









#### 获取和转换数据

##### 自网站



#### 查询和连接



#### 排序和筛选



#### 数据工具

##### 分列

##### 数据验证



#### 预测



#### 分级提示



### 审阅



### 视图

#### 工作薄视图

#### 显示

#### 缩放

#### 窗口

##### 新建窗口

##### 全部重排

##### 冻结窗格

##### 并排查看

##### 切换窗口

#### 宏





### 开发工具



### 帮助

















### 表格工具

#### 表格样式





### 查询工具



## 核心内容

### 函数

```
:
	and(): 多个条件成立
	average(): 平均值
	averagea(): 平均值（可求逻辑值、文本）
	averageif(): 平均值（条件区域）
	averageifs(): 平均值（多条件区域）
	column(): 返回列号
	columns(): 返回列数
	count(): 数字个数
	counta(): 非空单元格个数
	countblank(): 空值个数
	countif():
	countifs():
	datedif(): 
	false():
	find():
	if(): 条件选择值
		logical_test: 逻辑判断值
		value_if_true:
		value_if_false:
	index():
	int():
	left():
	len():
	max():
	match():
	mid():
	min():
	not(): 逻辑值求反
	now(): 当前时间日期
	or(): 至少有一个条件成立
	rank():
	right():
	round():
		num:
		num_digits:
	rounddown():
	roundup():
	row(): 返回行号
	rows(): 返回行数
	sum(): 求和
	sumif():
		range: 名称区域
		criteria: 名称
		[sum_range]: 求和区域
	sumifs(): 求和（多条件）
	sumproduct(): 区域乘积求和
	today(): 当前日期
	true():
	trunc(): 数字截取
	value():
	vlookup(): 连表查询
		lookup_value: 要查找的值
		table_array: 表的数据
		col_index_num: 列索引
		[range_lookup]: 模糊匹配
			模糊匹配返回符合条件的最后一个
```



### 域

```
域: {}
	Date:
	Eq:
	Filename: 文件名
	Page:
	PageRef:
	Print:
	PrintDate:
	Private:
	Quote:
	RD:
	Ref:
	Section:
	SectionPages:
	Seq:
		标识符:
		[书签]:
		[开关]:
			\c: 沿用上一个编号
			\h: 隐藏编号 
			\r: 重置编号
			CHINESENUM3:
	Set:
	Subject:
	Time:
		\@:
	Toc:
		\c:
		\h:
		\O:
		\z:
```


构建基块
域开关：通用开关、域专用开关
`F9`：更新域




## Power Query







## VBA

```
VBA:
	xlAutomatic:
	xlPasteFormats:
	xlPasteValues:
	xlSheetVisible:
	xlUp:
	ActiveCell:
	ActiveSheet:
	ActiveWorkbook:
		RefreshAll:
	ADODB:
		Connection:
			Open():
			OpenSchema():
	Application:
		DisplayAlerts:
		FileDialog:
			():
			SelectedItems:
			Show:
		ScreenUpdating:
	Button:
		Characters:
			Text:
		Name:
		OnAction:
	Buttons:
		Add:
			():
	Cell:
		Offset:
			(): 
		Range:
			():
	Cells:
		():
		ClearContents:
		Interior:
			ColorIndex:
	Columns:
		():
		ClearContents:
	DateSerial:
	Dir:
		():
	Err:
		Clear:
	InputBox:
	Kill:
	MsgBox:
	Name:
	Nothing:
	Range:
		():
		Activate:
		Cells:
			():
		Clear:
		Columns:
			Count:
		CurrentRegion:
		MergeArea:
		NumberFormat:
		PasteSpecial:
			():
				Paste:
		Resize:
			():
		Rows:
			Count:
		Select:
		UnMerge:
		Value: 内容
	Rows:
		():
		Count:
		Interior:
			ColorIndex:
	Scripting:
		Dictionary:
	Selecttion:
		Font:
			Bold:
			ThemeColor:
			TintAndShade:
		HorizontalAlignment:
		IndentLevel:
		Interior:
		MergeCells:
		NumberFormatLocal:
		Orientation:
		Pattern:
		PatternColorIndex:
		PatternTintAndShade:
		ReadingOrder:
		ShrinkTOFit:
		ThemeColor:
		TintAndShade:
		VerticalAlignment:
		WrapText:
	ThisWorkbook:
	Worksheet:
		Activate:
		Cells:
			Copy:
				():
			Value:
			End():
				Row:
		ChangeFileAccess:
		Close:
		Delete:
		Hyperlinks:
			Add:
		Name:
		Path:
		Protect:
		SaveAs:
			():
		Shapes:
			():
		UnProtect:
		UsedRange:
		Visible:
		
	Worksheets:
		Add:
		
	Sheets:
		():
		Count:
	CreateObject():
	Right():
	UBound() 边界值
	Val():
```





Visual Basic

```
Sub xxx()
	Dim xxx As xxx类型,
	
	Set xxx = xxx
	
	For i = 1 To 100
		...
	Next
	
	For Each xxx In Worksheets:
		...
	Next
	
	Do While ...
		...
	Loop
	
	If xxx Then
		...
	End If
	
	With xxx
		...
	End With
	
	OnError Resume Next
	
End Sub
	
	
数据类型:
	Array:
	Boolean:
	Byte:
	CStr:
	Currency:
	Date:
		#...#:
	Double:
	Integer:
	Long:
	Object:
	Single:
	String:
		&: 字符串拼接
	
	
Call 函数名: 直接调用函数
```





Microsoft Excel对象、模块



## WPS宏

启用宏的工作簿：`.xlsm`



js宏





```
:
	Cells():
		Value2:
	Dir():
	InputBox():
	MsgBox():
	Range(): 单元格区域
		Interiro:
			Color:
		Borders: 边框
			Color:
		Row:
		Value2: 值操作
		Copy():
		End():
		Select():
	Application: 全局变量（应用）
		ActiveWorkbook:
		Env:
			GetTempPaht():
		FileSystem:
			Exists():
		Sheets:
		WorkSheets:
			Item():
	Selection:
		Formula:
		Interior:
			Color:
			Pattern:
			PatternColorIndex:
			TintAndShade:
	Sheet:
		Name:
		Cells(): 
		Column():
			Find():
			FindNext():
		Copy(): 复制一个工作表（返回工作簿）
		Delete(): 
		Range(): 单元格区域
	Sheets:
        Count: 工作表数量
        Add(): 添加工作表
	ThisWorkbook:
		Name:
		Path: 文件路径
		Close():
		Save():
		SaveAs():
		Sheets(): 获取工作表
			Activate():
			Rows():
				Copy():
	UserForm:
		StartUpPostion:
		Close():
		Show():
		CheckBox:
		ComboBox:
			AddItem():
		CommmandButton:
			Caption:
		Frame:
		Label:
		OptionButton:
		Page:
		TextEdit:
			Text:
		ToggleButton:
	Workbooks:
		Add():
		Open():
```









## 快捷键

- `alt`+`=`：选中区域快速求和
- `ctrl`+`1`：单元格格式
- `ctrl`+`t`：创建表
- `ctrl`+`shift`+`enter`: 转为数组形式
- `f4`：切换相对引用与绝对引用
- 双击格式刷：持久化格式刷
- 

