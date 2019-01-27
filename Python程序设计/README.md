# Python 程序设计（第三版）

### 实验环境

- 版本：Python 3.7

---

字符串拼接：`"a" + "b"`

### 输出

输出语句 `print`，默认就是自带换行。ß

```python
print(<expr>, <expr>, ..., end="\n")
```

空行输出：`print()`

覆盖输出默认行为：`print("abc", end = "")`



### 赋值

Python 是动态语言，变量可以多次赋值，完全可以赋值成不同的类型。这个就很方便了一会赋值 int，一会赋值字符串。

#### 赋值输入

和用户相关的，一个输出，另一个就是输入了。Python 的输入，是和命令行交互的，首先会把提示文字打印到命令号，然后等待用户输入，然后转换成值。很是好用。

格式：

```python
<variable> = input(<prompt>)
<variable> = eval(input(<prompt>))
```

- <variable>：变量名
- <prompt>：提示用户输入

`input`：默认是用户输入的是什么，接收的就是什么，结果是「字符串」。如果对用户输入的内容进行表达式计算的话，需要通过 `eval` 来执行。

#### 同时赋值

```python
<var1>,<var2>,...=<expr1>,<expr2>,...
```

有这个特性了，交换变量和函数返回可以传递更多信息了。

## 数据类型

`type()` 用来获取数据类型。

有个比较有意思的是：「除法」

python 中包含两种：「常规除法」和「整数除法」

- 常规除法：`a / b`
- 整数除法：`a // b`
  - int // int: int
  - float // float: float 

类型转换：

 - int()
    - int(1.2) -> 1
    - int("12") -> 12
    - 其他：ValueError
 - float()
    - float(1) -> 1.0
    - float("1") -> 1.0
    - 其他：ValueError

四舍五入：

round：使用的时候，对四舍五入浮点数的时候，可能计算结果不是预期。（慎用）

>  https://www.cnblogs.com/anpengapple/p/6507271.html

```python
round(number, ndigits=None)5
```