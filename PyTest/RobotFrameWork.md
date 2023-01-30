# RobotFrameWork基础

> Author: Sylvie233
>
> Date: 23/1/27

[TOC]

## 基础介绍

安装：

```
pip install robotframework
pip install robotframework-seleniumlibrary
```



.robot文件









### robot

```
robot:
	--version:
```









## 核心内容

### Resource

资源文件、模块文件

可被.robot文件引入





### Settings

```
*** Settings ***
Documentation xxx
Library SeleniumLibrary
Resource xxx.resource



Suite Setup XXX
Suite Teardown XXX
Test Setup XXX
Test Teardown XXX
```



### Variables

```
*** Variables ***
${xxx} xxx
${EMPTY}
```



### Keywords

```
*** Keywords ***
XXX
	[Arguments]
	[Teardown]
```





### Test Cases

```
*** Test Cases ***
xxx
	Capture Page Screenshot:
	Click Button:
	Click Element:
	Click Link:
		link:
	Element Text Should Be:
	Input Password:
	Input Text:
		id:
		locator:
		xpath:
	Maximize Browser Window:
	Open Browser:
		browser:
		url:
	Press Keys:
	Select From List By Value:
	Set Screenshow Directory:
```



### Python集成

```
class Xxx:
	def xxx_xxx(self):
```



使用Library加载进robot中

