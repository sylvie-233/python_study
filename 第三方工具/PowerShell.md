# Power Shell
>Author: Sylvie233
>
>Date: 24/03/11
>
>Point：

## 基础介绍


### PowerShell

```
PowerShell:
	Add-:
		Content: 追加内容
	Clear-:
		Host:
	ConvertTo-:
	Copy-:
		Item: 复制对象
	Disable-:
	Enable-:
	Export-:
		ModuleMember: 导出模块成员
			-Function: 导出函数
			-Variable: 导出变量
	Find-:
	ForEach-:
		Object:
	Get-:
		Alias: 命令别名
		ChildItem:
			-Path: 指定路径
			-Recurse: 递归
		Content: 获取内容
		Date: 获取日期
		ExecutionPolicy：获取ps执行策略
			RemoteSigned:
		Help: 获取命令信息
		Process: 获取进程信息
			-Name:
		PSDriver: 
		PSProvider: 内容提供者
		Service: 服务
		Variable: 获取变量
	Import-:
		Module: 导入模块
			-Name:
	Install-:
		Module:
	Invoke-:
	Measure-:
		Command:
			-Expression:
	Move-:
		Item: 移动对象
	New-:
		Item:
			-Path: 指定路径
			-ItemType:
				Directory: 新建目录
				File: 新建文件
		ModuleManifest: 生成模块清单文件
			-Author: 
			-ModuleVersion:
		Object:
			-TypeName:
		PsDriver:
			-Name:
			-PsProvider:
			-Root:
	Register-:
	Remove-:
		Item: 删除对象
		Module: 移除模块
	Rename-:
		Item: 重命名
			-NewName:rrr
			-Path:
			
	Reset-:
	Save-:
		Module:
	Set-:
		Content: 设置内容
			-Path:
			-Value:
		Location: 设置当前路径
		Printer:
		StrictMode:
			-Version:
	Start-:
		Trace:
	Stop-:
		Trace:
	Update-:
	Where-:
		Object:	
	Write-:
		Host: 控制台输出
		Object:
```
















#### 常用变量

```
Host:
	UI:
		RawUI:
			BufferSize:
			WindowSize:

Profile:
	CurrentUserAllHosts:

PsISE: 
	Options: ise环境配置
		FontName:


System:
	Array:
		Count:
		IsFixedSize:
		Add():
		ForEach():
			$_:
		RemoveAt():
	Boolean:
	Collections:
		ArrayList:
			Add():
			AddRange():
			Remove():
			RemoveAt():`
	Double:
	Hashtable:
		Keys:
		Values:
		Add():
		ContainsKey():
		ContainsValue():
	Int32:
	IO:
		FileInfo:
			FullName:
	Object:
		GetType():
	String:
		Tochararray():
	ValueType:

Variable：
	false:
	null:
	psVersionTable:
		psVersion:
	true:

```




## 核心内容

### 变量

#### 数组
```
arr = @(1, 2, 3)
```



#### 哈希表

```
map = @{key='value'}
```




### 流程控制

#### 运算符

```
:
	-Eq: 相等
	-Is:
	-Not: 取反
	-Or:
```




### 函数

```powershell
function hello{
	#固定语法
    [CmdletBinding()]
	#参数声明
	param(
        [Parameter()]
        [string] $content
    )
	#打印参数内容
    Write-Host "$content"
}
```



### 对象

`PSCustomObject`
```powershell
$obj = New-Object psobject



```


### 模块

```

```

`.psm1`文件

模块的三个组成部分
- 文件夹：存放脚本文件
- 清单文件：`.psd1`
- 模块文件：`.psm1`




### Provider
数据存储路径和访问组件的一个标准的接口
- 文件系统
- 注册表‘
- 函数
- 变量
- 别名
- 环境变量
- 证书
- WSwan


#### Driver