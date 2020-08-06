# Golang的数据结构

[//]: # (__author__ = "Wenger Binning")
[//]: # (__version__ = "v0.0")

## 数据类型

Golang的数据类型分为值类型与引用类型，值类型即直接存储数据值的类型，而引用类型是存储指向真实变量的首地址的类型；其中值类型有数值类型、字符串类型与逻辑类型，引用类型有指针、数组、结构体、函数、切片、接口、映射、通道。

### 数值类型

* `int`与`uint`：
* `int8`与`uint8`：
* `int16`与`uint16`：
* `int32`与`uint32`：
* `int64`与`uint64`：
* `float32`与`float64`：
* `complex64`与`complex128`：
* `byte`：
* `rune`：
* `uintptr`：

### 字符串类型

字符串

### 布尔类型

### 指针

### 数组

### 结构体

### 函数

### 切片

### 接口

### 映射

### 通道

## 变量

变量是用于存储数据的内存空间，由变量名与变量值组成，变量值的类型必须是Golang中合法的数据类型。

### 变量的声明

在Golang中声明的变量必须使用，否在会变量未使用的错误。

* 变量的一般声明：

  ```go
  var <varName> <type>
  // 多个同类型变量的声明
  var <varName_1>, <varName_2> <type>
  // 多个全局变量的声明
  var (
	<varName_1> <type_1>
	<varName_2> <type_2>
  )
  ```

  > Note: 在Golang中，一般varName通常以小驼峰命名规则，type为数据类型；一般数值类型默认初始化为0，字符串默认初始化为空字符串，布尔类型默认初始化为flase，引用类型默认初始化为nil。

* 类型自动推断：

  ```go
  var <varName> = <value>
  // 多个类型自动推断的声明
  var <varName_1>, <varName_2> = <value_1> <value_2>
  ```

* `:=`声明变量并赋值

  ```go
  <varName> := <value>
  // 多个变量自动声明
  <varName_1>, <varName_2> := <value_1>, <value_2>
  ```

  > Note: 在Golang中，使用:=赋值符号可以声明变量并为之赋值，但是该符号的左侧必须存在至少一个未声明的变量,且一般只在函数内部使用。

### 变量的使用

* 变量的交换：

  ```go
  var varA, VarB int = 1, 2
  // 交换varA与varB的值
  varA, varB = varB, varA
  ```

  > Note: 该方法必须是同一类型时才能操作。


### 特殊变量


* 空白标识符`_`：只写变量，常用于抛弃函数的返回值。

#### 常量

常量是一种变量值恒定的变量，必须在声明时初始化，且常量的数据类型必须是值类型。

##### 常量的定义

常量的定义使用`const`来修饰。

* 常量的显式定义：

  
  ```go
  const <constName> <type>
  ```

* 常量的隐式定义：

  ```go
  const <constName> = <value>
  // 多个常量的定义
  const <constName_1>, <constName_2> = <value_1>,<value_2>
  ```

##### 常量的使用

* 枚举：

  ```go
  const (
 	MONDAY = 1
	TUESDAY = 2
	WEDNESDAY = 3
	THURSDAY = 4
	FRIDAY = 5
	SATURDAY = 6
	SUNDAY = 7
  )
  ```

  > Note: 可以使用`len()`获取变量的长度，`unsafe.Sizeof()`获取变量的内存大小。

* `iota`：iota在const使用时初始化为0，之后没增加一行常量的定义，其值自动加一

## 运算符

在Golang中存在算数运算符、关系运算符、逻辑运算符、位运算符、赋值运算符等其他运算符。

### 算数运算符

* `*`：乘法运算,
* `/`：除法运算，
* `%`：取余运算，
* `+`：加法运算，
* `-`：减法运算，
* `++`：自增运算，
* `--`：自减运算，

### 关系运算符

* `==`与`!=`：等于与不等于
* `>`与`<=`：大于与不大于
* `<`与`>=`：小于与不小于


### 逻辑运算符

* `&&`：逻辑与
* `||`：逻辑或
* `!`：逻辑非

### 位运算符

* `&`：按位与
* `|`：按位或
* `^`：按位异或
* `<<`：左移
* `>>`：右移

### 赋值运算符

* `=`：赋值
* `*=`：先乘法再赋值
* `/=`：先除法再赋值
* `%=`：先取余再赋值
* `+=`：先加法再赋值
* `-=`：先减法再赋值
* `&=`：先位与再赋值
* `|=`：先位或再赋值
* `^=`：先异或再赋值
* `<<=`：先左移再赋值
* `>>=`：先右移再赋值

### 地址运算符

* `*`：取地址内容
* `&`：取变量地址