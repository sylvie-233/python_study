# Latex基础

>Author: Sylvie233
>Date: 23/10.29
>Point：LaTeX入门教程：P10


## 基础介绍
```
Latex:
	tex:
		-V:
	xelatex:
		-interaction:
			nonstopmode:
		-synctex:
			1:
```
`.tex`文件


## 核心内容

```
latex:
	%: 注释
	$$: 公式(行内)
		$$: 行间公式
		^: 上标
		_: 下标
		\alpha:
		\approx:
		\Bar{}:
		\because:
		\beta:
		\cap:
		\cdot:
		\cdots:
		\cos:
		\cup:
		\ddots:
		\delta:
		\div: 
		\epsilon:
		\equiv:
		\exists:
		\frac{}{}: 分式
			\dfrac{}:
		\forall:
		\gamma:
		\ge:
		\in:
		\infty:
		\int{}:
			\iint{}:
			\iiint{}:
		\left:
			\right: 
		\leftarrow:
			\longleftarrow:
			\Leftarrow:
			\rightarrow:
			\Rightarrow:
			\leftrightarrows:
			\Leftrightarrows:
		\ln{}:
		\lim:
		\limits_{}:
		\log{}{}:
		\le:
		\mathbb{}: 罗马体
		\mathscr{}:
		\nexists:
		\notin:
		\oint{}:
		\omega:
		\overline{}:
		\overrightarrow{}:
		\prod{}:
		\sigma:
		\sin{}:
		\smallmatrix:
		\sqrt[]{}: 根式
		\subseteq:
		\subsetneqq:
		\sum{}:
		\text{}: 文字
		\textbaclslash:
		\textbar:
		\textgreater:
		\textless:
		\therefore:
		\times:
		\to:
		\varnothing:
		\Vec{}:
		\vdots:
		\\: 另起一行
		\,:
		\#:
		\^{}
		\--{}:
		\{:
		\}:
		\(:
			\):

	{\xxx}: 内容分组
	\addcontentsline{}{}{}: 添加内容
		{}:
			toc: 目录
		{}:
			section:
		{}:
	\author: 作者
	\begin{}[]:
		\end{}
			{}:
		{}:
			abstract: 摘要
				\keywords{}: 关键字
			align: 对齐
				&: 对齐符号
			array: 矩阵
				\hline: 
			bmatrix:
			Bmatrix:
			document: 文档开始
			description: 描述
			enumerate: 有序列表开始
				[]:
					label:
				\item: 列表元素
			equation: 公式
				aligned: 对齐
					&:
				bmatrix: 矩阵
				cases:
					
				split:
			figure:
				\caption:
				\center:
				\includegraphics[]{}:
					[]:
						\textwidth:
					{}:
				\label{}:
					{}:
			gather: 多行公式
				\notag:
			itemize: 无序开始
				\item[]: 列表元素
					[]: 自定义符号	
			matrix: 矩阵
				\cdots: 
				\ddots:
				\multicolumn{}{}{}:
				\vdots:
					
			pmatrix:
			verbatim: 行内代码
			vmatirx:
			Vmatrix:
	\date{}: 日期
		\today:
	\documentclass[]{}
		[]:
			UTF8:
		{}:
			article:
			book:
			letter:
			report:
	\LaTex: Logo
	\maketitle: 生成标题
	\newpage: 新起一页
	\par: 换行
	\paragraph: 四级标题
	\PassOptionsToPackage{}{}:
		{}:
			quiet:
		{}:
	\qquad:
	\quad: 空格
	\ref{}: 引用
	\section*{}: 一级标题
		\subsection{}:
			\subsubsection{}:
				{}:
			{}:
		*: 不带标号
		{}:
	\tableofcontents: 目录
	\text{}:
		\textmd{}:
		\textrm{}:
		\textsf{}:
		\texttt{}:
	\title: 标题
	\usepackage{}:
		{}:
			amsmath:
			amssymb:
			ctex:
			graphicx:
	\verb||:
		||: 
	\zihao{}: 字号
		{}:
```




