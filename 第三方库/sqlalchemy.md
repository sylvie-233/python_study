# Sqlalchemy

> Author: Sylvie233
>
> Date: 23/5/13
>
> Point:


## 基础介绍

直接使用table
`engine`->`metadata`->`table`
`table`->`connection`->`sql语句`->`result

或者使用映射类进行查询
`engine`->`BaseModel`->`自定义model`
`session`->`model`

连表查询relationship中的backref用于给别人添加一个自身类型的片段，就不用改变对方的模型结构了，backref只用写一次就行了
同理，多对多中的中间表secondary也只需要在其中一个类上定义就行







## 核心内容

```
sqlalchemy:
	engine:
		base:
			Connection: 连接执行
				close():
				commit():
				exec():
				execute(): 执行语句
		cursor:
			CursorResult:
				inserted_primaty_key:
				fetchall():
				fetchone():
		row:
			Row:
		Engine:
			connect(): 获取连接Connection
			dispose():
	ext:
		declarative:
			declarative_base:
				~:
				==:
				!=:
				in_():
				is():
				isnot():
				like():
				
	func:
		avg:
		count:
		max:
		min:
		sum:
	orm:
		declarative_base: 模型基础类（类似MetaData作用）
			__tablename__: 关联数据库表名
		mapped_column:
		relationship:
		sessionmaker: 绑定engine，生成session工厂
			bind:
		DeclarativeBase:
		Mapped:
		Query: 查询
			all():
			filter():
			first():
			one():
			scalar():
			update():
		Session: 类似Connection作用
			add():
			add_all():
			commit():
			delete():
			filter():
			query():
	sql:
		base:
			ReadOnlyColumnCollection:
		dml: 定义语句
			Delete:
			Insert:
			Join:
			Select:
				select_from():
				where():
			Update:
				values(): 设置更新字段、值
		and_:
		or_:
	__version__:
	Column: 字段定义
		autoincrement:
		default:
		name:
		nullable:
		onupdate:
		primary_key:
		unique:
	Date:
	ForeignKey: 外键定义
	Integer:
	MetaData:
		create_all():
	String:
	Table:
		c: 字段集合（可用于条件查询）
		delete():
		insert():
		join():
		select():
		update():
	create_engine():
	text():
```






