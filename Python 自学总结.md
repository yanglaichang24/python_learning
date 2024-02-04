# Python

- Python基础语法：标识符，关键字，变量，判断循环  。。。。
- 容器类型（数据类型中的高级类型）
- 函数
- 文件处理
- 面向对象
- 包和模块
- 异常处理
- 并发编程
- 网络处理



## 1、Python概述

- 创始人：吉多·范罗苏姆  龟叔
- 为什么要学习Python：大势所趋，简单易学，使用范围广
- 我们本次学习使用Python3.x版本
- Python在大数据生态中应用非常广泛

## 2、Python解释器和pycharmIDE工具

- Python解释器是将Python代码解释为机器语言（二进制文件）的一种工具
- Python代码必须经过解释器解释，计算机才能够去执行命令
- 常见的解释器版本：
  - CPython： 官方版本，稳定，持续更新
  - Ipython：可交互，在CPython基础上进行了升级
  - pypy：使用Python编写的解释器
  - JPython：使用java编写的解释器，可以将Python便以为字节码文件，在java平台上运行
- pycharm IDE：
  - 语法高亮
  - 工程管理
  - 代码提示
  - 错误检查
  - 。。。。。。。
- pychram基本设置
  - 主题：file --- settings---在搜索栏搜索 theme ----修改主题
  - 字体：file --- settings -- 在搜索栏输入font  ---- 修改字体
  - 修改解释器：file --- project：项目名称--- Python interpreter --修改解释器
  - 工程管理：file -- open ---选择工程
    - this windows ： 在当前窗口打开
    - new windows：在新窗口打开
    - attach ：合并项目窗口
  - 关闭工程： file -- close project

## 3、Python中的注释

- 单行注释： # 注释的内容
  - 可以在语句末尾注释
  - 快捷键：ctrl+ /
- 多行注释：三对单引号，或者三对双引号
  - 可以在注释内部换行

```python
"""
我是文件开头的多行注释,颜色不一样,
但是功能没有区别
"""

# 注释:有提示作用,注释不参与代码执行,但是可以增加代码的可读性
# 语法规范:单行注释#号与注释内容之间存在一个空格, 如果在语句末尾注释,语句和#之间要有两个空格
# 单行注释
print('hello world')
# 我是一个优秀的单行注释
print('hello bigdata')
print('hello python')  # 打印Python,可以添加在语句的末尾
print('hello itcast')
# 单行注释快捷键:ctrl + /
# 如果想要快捷注释多行内容,选中多行信息,使用ctrl+ /进行对多行代码依次进行单行注释
# print('hello itcast')
# print('hello itcast')
# print('hello itcast')


# 多行注释
'''
我是一个多行注释
在多行注释内,可以随意换行
换行后可以正常书写
'''

"""
在Python中单双引号不敏感,但要成对出现
双引号也可以构建多行注释
"""

# ???多行注释可以用在语句末尾么?  不能
# print('hello python') """ abc """

# 在文件开始位置,多行注释和文件中间的多行注释颜色不一样,效果一样么? 一样
```

## 4、变量

- 变量特性：
  - 容器
  - 临时
  - 可变
- 变量定义的格式：
  - **变量名 = 值**
- 标识符的命名规则：
  - **只能是数字字母下划线组成**
  - **首字母不能是数字**
  - **严格区分大小写**
  - **不能是关键字**
- 在Python中定义变量必须赋值，否则报错

```python
# 牛奶和可乐交换的案例
'''
交换方式:
获取一个空杯子
将牛奶倒入空杯子
将可乐倒入原牛奶现空杯子的杯子中.....
'''

'''
换一个方式进行描述:
# 开始
A杯子: 牛奶
B杯子: 可乐
C杯子: 空
# 过程
A >> C
B >> A
C >> B
# 结尾
A杯子: 可乐
B杯子: 牛奶
C杯子: 空
'''

a = '牛奶'
b = '可乐'
c = '空'
print(a, b)

c = a
a = b
b = c

print(a, b)

# 关键字: 系统定义的具有一定功能或者含义的字符组合.(关键字不要背诵,遇到了就记下来,如果记不下来,关键字有自己的高亮效果)
# 标识符: 程序员自己定义的具有一定功能或者含义的字符组合.

# 标识符的命名规则:
# 1/只能由数字,字母,下划线组成
# 2/首字母不能是数字
# 3/不能是关键字
# 4/严格区分大小写

# 什么地方使用了标识符:文件名,变量名, 函数名, 类型名  (只要是让程序员起名字,都是标识符)
# 文件名可以不遵循标识符的命名规则,但是在服务器中无法使用,不能当做模块进行导入,很多服务器工具或组件不支持非标识符文件.

'''
Python)abc  不能
_abc   可以
anc______  可以
123abc _____  不可以
and  不可以
ABC  可以
anc  可以
'''

# 在windows中文件名定义时,不严格区分大小写
# 程序员不可能定义变量出错

# aaa
# 在Python中创建变量必须赋值,否则将会报错
```

## 5、标识符的命名规范

- 见名知意
- 类名使用大驼峰命名法
  - ClassName
- 变量名，函数名，包名，模块名使用下划线命名法
  - class_name

```python
# 要见名知意
name = '小明'
age = 18

# abc = '小明'
# 见名知意不要写缩写,也不要写首字母,尤其是不要写拼音首字母,更不要写拼音全拼

# 命名法
# 大驼峰命名法:
# 首字母大写,如果由多个单词组成,所有单词的首字母大写
# 在Python中类名的书写使用大驼峰命名法
ClassName = 'Python+大数据54期'
# 小驼峰命名法:
# 首字母小写,如果由多个单词组成,第一个单词首字母小写,其余单词首字母大写
className = 'Python+大数据54期'
# 下划线命名法:
# 在Python中 变量,函数,文件名称(包和模块名称)使用下划线命名法
# 所有字母小写,多个单词中间用下划线连接
class_name = 'Python+大数据54期'

# 不满足命名规范一样不会报错,但是不利于协作开发
```

## 6、变量的使用

- **定义：变量名 = 值**
- **调用：函数（变量名）   或者    使用变量名进行运算  变量名1 + 变量名2**
- **变量必须先定义后调用**

```Python
# 使用变量直接调用变量名即可,我们使用的是变量名,参与执行和运算的是变量中的数据(值)
name = 'xiaoming'  # 定义
print(name)  # 调用

a = 1  # 定义
b = 1  # 定义
print(a + b)  # 调用

# 所有的变量,要先定义后调用
# 程序运行起来后,从上到下依次执行代码,解释一行运行一行,在打印方法被执行时,还不知道price已经被定义,会报错
# print(price)
# price = 15
```

## 7、Python中的数据类型

| int   | 整型   |
| ----- | ------ |
| float | 浮点型 |
| bool  | 布尔型 |
| str   | 字符型 |
| list  | 列表   |
| tuple | 元组   |
| set   | 集合   |
| dict  | 字典   |

查看数据类型使用的函数是 type（）

```python
# 数据类型查看的函数 type(数据/变量名)
# 基础数据类型:int  float  bool
# 容器类型: str  list tuple  set dict

# 整型
int1 = 12
print(type(int1))  # <class 'int'>
# 浮点型
float1 = 12.1
print(type(float1))  # <class 'float'>
# 布尔型  (True/False)
bool1 = True
print(type(bool1))  # <class 'bool'>
# 字符串型
str1 = 'hello Python'
print(type(str1))  # <class 'str'>
# 元组
tuple1 = (1, 2, 3, 4)
print(type(tuple1))  # <class 'tuple'>
# 列表
list1 = [1, 2, 3, 4]
print(type(list1))  # <class 'list'>
# 集合
set1 = {1, 2, 3, 4}
print(type(set1))  # <class 'set'>
# 字典
dict1 = {'name': 'xiaoming', 'age': 18}
print(type(dict1))  # <class 'dict'>

# 代码格式化的快捷键:ctrl + alt + L

# 练习:

a = 12
# a是什么数据类型? int
a = 'str'
# a是什么数据类型? str
a = '12'
# a是什么数据类型? str
a = True
# a是什么数据类型? bool
a = 13.4
# a是什么数据类型? float


# 通过上述演示,我们发现在Python程序执行过程中,可以随意改变变量的数据类型
```

## 8、Python中的bug和调试

- 常见的bug类型：

```Python
# 常见的bug
# NameError: name 'a' is not defined (一般只变量名错误)
# 如果遇到此类错误,查看变量名是否被定义或者变量名是否书写错误
# print(a)

# ZeroDivisionError: division by zero (零不能做分母)
# a = 10
# print(a / 0)

# IndentationError: unexpected indent  (缩进错误)
# 修改缩进,或者去调整函数关系
# a = 5
#     b = 10

# SyntaxError: unexpected EOF while parsing (语法错误)
# 找到报错位置,查看语法是否存在问题,最好的办法就是将其进行格式化
# print(123

# TypeError: can only concatenate str (not "int") to str (数据类型错误)
# a = '123'
# print(a + 12)

# Process finished with exit code 0 程序结束后 正常退出 code 为 0
# print('hello world')

# Process finished with exit code 1  程序异常结束 code 为 1
# print(a)
```

- bug调试工具的使用
  - 打断点：在行号后边点击出现小红点
  - 右键debug进入调试模式，代码执行暂停到断点位置代码执行之前
    - debugger ：查看参数及变量在执行过程中的变化情况
    - console：查看控制台输出内容
    - step over：单步执行代码
    - resume ：执行到下一次断点位置或者程序结束
    - stop：让程序终止

## 9、字符串的格式化及输出

- 格式化是字符串所具有的功能，与print无关，哪怕不进行输出，也可以进行字符串的格式化

```python
# 字符串格式化 :格式化是字符串所具有的功能
# print 输出: print函数只能将传入的内容显示到控制台中,与格式化没有任何关系

# 需求:想让小明的年龄,跟着age变量的变化,不断发生变化,那么我们应该怎么做?
age = 16
print('小明14岁')

# 字符串的格式化
# 格式化输出,到底是print 的功能还是字符串的功能呢?
print('小明 %d 岁' % age)

# 探索
str1 = '小明 %d 岁' % age
print(str1)
```

- 格式：
  - 单占位符：'要书写的内容，占位符' % 变量名
  - 多占位符: '要书写的内容，占位符1， 占位符2， 。。。。' % （变量1， 变量2，。。。。）
    - %之前的占位符数量要和%之后的变量数量相匹配，一一对应否则会报错

```python
# 格式: '字符串,占位符' % 变量
# 在上述格式中,格式化完成后,会将占位符位置填充上对应的变量
# 不同数据类型的变量,要使用不同的占位符进行占位

# 字符串数据使用 %s
# 浮点型数据使用 %f
# 整型数据使用   %d

name = 'xiaoming'
age = 18
height = 1.85
weight = 69.5
marriage = False

# 一个占位符的格式化输出
print('学员的姓名是 %s' % name)
print('学员的年龄是 %d' % age)
print('学员的身高是 %f' % height)
print('学员的体重是 %f' % weight)
print('学生的婚姻状况是 %s' % marriage)

# 有多个动态变量的时候,我们就需要使用多个占位符进行占位
# TypeError: not enough arguments for format string
# 如果前边有多个占位符,那后边的多个变量要使用括号进行包裹
print('学员的姓名是%s, 学员的年龄是%d岁, 学员的身高是%f米, 学员的体重是%fkg, 学员的婚姻状况是%s' % (name, age, height, weight, marriage))
# 括号内的变量数量不能少于占位符数量
# print('学员的姓名是%s, 学员的年龄是%d岁, 学员的身高是%f米, 学员的体重是%fkg, 学员的婚姻状况是%s' % (name, age, height, weight))
# not all arguments converted during string formatting
# 括号内的变量数量不能多于占位符的数量
# print('学员的姓名是%s, 学员的年龄是%d岁, 学员的身高是%f米, 学员的体重是%fkg, 学员的婚姻状况是%s' % (name, age, height, weight,marriage,name))

# 结论:占位符的数量,与%后的变量数量必须保持一致,如果是一个占位符,则可以使用一个变量,如果是多个占位符,那么多个变量必须使用括号包裹起来

# 能否控制变量输出的结果的样式:可以
name = 'xiaoming'
age = 18
height = 1.85
weight = 69.5
id = 12

# 需求:1.身高保留两位小数,体重保留三位小数
# 需求:2.学员的id共占用6位,不足位用0填充
# 使用ctrl + d 可以整行复制
print('学员的姓名是%s, 学员的年龄是%d岁, 学员的身高是%f米, 学员的体重是%fkg, 学员的编号是%d' % (name, age, height, weight, id))
# 浮点型保留n位小数: %.nf
# 整型占用n位数据,不足位用0补齐  %0nd
print('学员的姓名是%s, 学员的年龄是%d岁, 学员的身高是%.2f米, 学员的体重是%.3fkg, 学员的编号是%06d' % (name, age, height, weight, id))
```



## 10、转译字符

- \n:换行符
- \t：制表符
- %%：在字符串格式化拼接时输出%

```python
# \n  换行符
# 为什么两个print之间可以自动换行
# 在print定义时自动在结尾加上了'\n'所以每次打印结束后,会自动换行
print(123)
print('hello world \n')
print(456)
# 如果不想让其自动换行, 在字符串输入结束后,使用end = '结束符' 可以修改print打印结束后插入的字符
print(123, end='$$$')
print(456)

# \t 制表符
print('3  4\t5')
# %%  输出%
# 在不适用字符串格式化拼接时,可以进行%的单独输出
print('我的业绩增长了100%')

score = 100
# 在使用字符串格式化的时候,字符串中的%不能单独输出,必须配合占位符,或者使用%%进行输出
print('我的成绩增加了%d%%' % score)

# 转译字符:在字符串中,一般情况下n  或者 t这类字母没有特殊含义,如果想给他赋予特殊含义,则需要使用\进行转译
```

## 11、f-string

- f-string是Python3.6之后出现的格式化语法
- 格式：f'要输出的字符串{要拼接的变量}'
  - f可以是大写，也可以是小写，
  - 引号可以是单引号，也可以是双引号
  - 精度控制
    - {浮点型变量：.nf} 保留n位小数，四舍五入
    - {整型变量：0nd} 保留n位，不足位用0补齐，如果超出则原样显示
    - %可以单独输出

```python
# f-string是Python3.6以后推出的格式化方式
name = 'xiaoming'
age = 18
height = 1.85
weight = 69.5
score = 98
id = 12345678

# 格式化拼接上述变量
# 传统拼接方式
print('学员的姓名是%s, 学员的年龄是%d, 学员的身高是%f, 学员的体重是%f, 学员的分数是%d%%, 学员的学号是%d' % (name, age, height, weight, score, id))
# 使用f-string进行字符串拼接
# 格式:f'要输出的内容{变量}'
print(F'学员的姓名是{name}, 学员的年龄是{age}, 学员的身高是{height}, 学员的体重是{weight}, 学员的分数是{score}%%, 学员的学号是{id}')


# 修改格式:
print('学员的姓名是%s, 学员的年龄是%d, 学员的身高是%.2f, 学员的体重是%.3f, 学员的分数是%d%%, 学员的学号是%06d' % (name, age, height, weight, score, id))
# 如果需要调整精度
# {整数型变量:06d} 整型占六位,不足位用0补齐 d可以省略
# {浮点型变量:.2f} 浮点型保留两位小数, 四舍五入
# %可以单独输出
print(F'学员的姓名是{name}, 学员的年龄是{age}, 学员的身高是{height:.2f}, 学员的体重是{weight:.3f}, 学员的分数是{score}%, 学员的学号是{id:06d}')
print(F'学员的姓名是{name}, 学员的年龄是{age}, 学员的身高是{height:.2f}, 学员的体重是{weight:.3f}, 学员的分数是{score}%, 学员的学号是{id:06}')

# 练习:
# 输出自己的信息包括,姓名,年龄,身高(保留两位小数),学号(保留6位,不足位用0补齐),使用f-string进行拼接
```

## 12、数据类型转换

- 数据类型转换是为了不同类型数据之间可以进行拼接或运算
- 格式：数据类型（要转化类型的变量或值）
- int和float类型直接可以随意转换
  - float转换为int类型只保留整数部分
  - int转换为float类型在末尾添加。0

- 如果数值型转换为str类型，可以随意转换
- 如果str类型转换为数值型
  - float  必须保证str引号内部是浮点型数据或整型数据
  - int  必须保证str引号内部是整型数据

```Python
# 需求: 在超市中有两种水果,苹果和橘子
# 让售货员输入苹果的单价,苹果的重量,橘子的单价,橘子的重量,在控制台输出购买详情以及总价

# apple_price = input('请输入苹果的单价:')
# apple_weight = input('请输入苹果的重量:')
# orange_price = input('请输入橘子的单价:')
# orange_weight = input('请输入橘子的重量:')

# TypeError: can't multiply sequence by non-int of type 'str'
# 不同类型间的数据无法相乘
# 在此情况下,我们需要进行数据类型转换(input接收的数据默认为字符串类型),需要转化为float
# print(f'您购买了苹果{apple_weight}kg, 单价{apple_price}元, 橘子{orange_weight}kg, 单价{orange_price}元, 总共需要付款{apple_price * apple_weight + orange_price * orange_weight}')

# 如果需要将数据转换为float 就给其穿上float类型的衣服
# 格式: float(需要转换数据类型的变量或者值)
# apple_price = float(input('请输入苹果的单价:'))
# apple_weight = float(input('请输入苹果的重量:'))
# orange_price = float(input('请输入橘子的单价:'))
# orange_weight = float(input('请输入橘子的重量:'))
#
#
# print(f'您购买了苹果{apple_weight}kg, 单价{apple_price}元, 橘子{orange_weight}kg, 单价{orange_price}元, 总共需要付款{apple_price * apple_weight + orange_price * orange_weight}元')


int1 = 12
float1 = 14.9
str1 = '12'
str2 = '14.3'
str3 = 'python'

# 数据类型转换的细节
# int   float  str类型之间的转换
# int >> float
# int类型转换为float类型将会在整数末尾加.0
print(float(int1))
print(type(float(int1)))

# float >> int
# float转换为int类型,将会将小数部分去除,只保留整数部分
print(int(float1))

# int >> str
# int类型可以随意转换为str类型,但是输出结果不发生改变,转化为str类型后可以使用str类型的各种函数
print(str(int1))

# str >> int
# 字符串中是int类型数据,可以转换为int类型
print(int(str1))
# ValueError: invalid literal for int() with base 10: '14.3'
# 字符串中是float类型数据,不可以转换为int类型
# print(int(str2))
# ValueError: invalid literal for int() with base 10: 'python'
# 字符串中是字符型数据,不可以转换为int类型
# print(int(str3))

# float >> str
# float类型可以随意转换为str类型,但是输出结果不发生改变,转化为str类型后可以使用str类型的各种函数
print(str(float1))

# str >> float
# 字符串中是int类型数据,则可以转换为float类型数据,并且在末尾加.0
print(float(str1))
# 字符串中是float类型数据,可以转换为float类型数据
print(float(str2))
# ValueError: could not convert string to float: 'python'
# 字符串中是字符型数据则不能转换为float类型数据
print(float(str3))
```

# 运算

## 13、算数运算符

- `+ - * / // % **`
- `//`取商
- `%`取余
- `**`幂次运算

```python
#  + - * / % // **

# 案例:求梯形的面积
# a = float(input('请输入梯形的上底长度:'))
# b = float(input('请输入梯形的下底长度:'))
# h = float(input('请输入梯形的高:'))
#
# print(f'梯形的面积为{(a + b) * h / 2}')

# 算数运算符优先级可以使用小括号控制,  先乘除后加减,同级运算从左至右依次运算

float1 = 10.2
int1 = 4
int2 = 11

# +
# 数值型数据(float, int, bool)之间可以进行算数运算
print(int1 + float1)
# 了解  bool 可以参与算数运算  True 代表1  false 代表0
# print(int1 + True)

# -
# 同加法运算一致

# *
print(int1 * int2)
print(int1 * float1)

# /
print(int1 / int2)
print(int1 / float1)

# //(整除)  两个数据相除 取商
# 11 / 4 商 2 余 3
print(int2 // int1)  # 2

# %(取模  取余) 两个数相除  取余
# 11 / 4 商 2 余 3
print(int2 % int1)  # 3

# ** (幂次运算)
# 幂次运算就是求变量的多少次方
# 扩展int1 开根号等于几  int1 ** 0.5
print(int1 ** 2)


# 在除法运算中,结果必定为浮点型
print(9 / 3)  # 3.0
# 浮点型参与运算后,结果一定是浮点型
# 商 3 余 2.2
print(11.2 // 3)  # 3.0
print(9.9 // 3.3)  # 3.0

# print(0.1 + 0.2)   # 0.30000000000000004
```

- 结论算数运算符优先级: + - < * / // % < **

- 如果忘记了也没关系使用()提高运算符优先级即可

```python
print(1 + 2 * 3)

# 先乘除 后加减

# //运算  优先级

print(2 + 11 // 3 ) # 优先级高于+ -
# // 与 * / 平级
print(2 * 11 // 3)
print(11 // 3 * 2)

# % 也和 * / 平级
print(2 + 11 % 3)  # 优先级高于+ -
print(2 * 11 % 3)
print(11 % 3 * 2)

# ** 优先级  高于  * /
print(2 * 3 ** 2)

# 结论算数运算符优先级: + - < * / // % < **
# 如果忘记了也没关系使用()提高运算符优先级即可
```

## 5、赋值符号

- = ：将等号右侧的值赋值给等号左侧的变量
- 可以给单个变量赋值： 变量= 值
- 可以给多个变量赋不同的值 ： 变量1， 变量2，变量3 = 值1， 值2， 值3
- 可以给多个变量赋相同的值：变量1 = 变量2 = 变量3 = 值

```python
# = (在Python中等号不是判断相等的而是赋值使用)
# 赋值格式: 变量名 = 值

# 给单个变量赋值
a = 1

# 同时给多个变量赋值
# 等号左侧的变量数量一定要等于等号右侧的值的数量, 否则报错
name, age, gender = 'xiaoming', 18, '男'
# ValueError: not enough values to unpack (expected 3, got 2)
# name, age, gender = 'xiaoming', 18
print(name, age, gender)

# 同时给多个变量赋相同的值
# 此种情况前边可以有多个变量,但是最后只能有一个值,否则报错
a = b = c = 10
# a = b = c = 10 = 20
print(a, b, c)

# 等号左侧一定要是变量,右侧可以是值或者已经被定义的变量
int1 = 2
int2 = int1
print(int1, int2)
```

## 6、复合赋值运算符

- ```
  += -= *= /= //= %= **=
  ```

- 复合赋值运算符等号左侧一定是已经被定义的变量

- 复合赋值运算符右侧是已经被定义的变量或者值

```python
# += -= *= /= //= %= **=

a = 1
# a += 1  >>> a = a + 1  将a中的变量取出与1相加得到的数值赋值给a
a += 1
print(a)

# 符合赋值运算符等号左侧只能是已经定义的变量
# 符合赋值运算符等号右侧可以是已经定义的变量或者值

# NameError: name 'b' is not defined
# b必须已经被定义  b = b - 1  先计算b - 1  此时b必须存在
# b -= 1
# print(b)


# 复合赋值运算符不能连续使用
# a += 1 += 2


# 练习
a = 2

a *= 2
print(a)

b = 12
b //= 5
print(b)
```

## 7、比较运算

- `< > <= >= == !=`
- 比较运算就是比较数据值的大小
- 比较运算可以连续使用
- 比较运算中比较相等使用==  而 不能使用 = （赋值运算符）

```python
# < > <= >= !=  ==
# 比较运算符运算结果为bool值,如果成立,则返回True 如果不成立则返回False
print(1 < 2)  # True
print(5 > 6)  # False
print(1 >= 0)  # True
print(4 != 4)  # False

# 比较运算符可以连续使用(Python中的特性)
age = 13
print(12 < age < 30)  # True
# 不等号也可以连续使用
print(12 < age != 13)  # False

# <>  不可以使用
# print(1 <> 3)

# 判断是否相等使用==
print(age == 13)  # True
print(age == 11)  # False
# TypeError: 'age' is an invalid keyword argument for print()
# =是赋值运算不能判断是否相等
# print(age = 12)
```

## 8、逻辑运算

- and 同真即真
- or 同假即假
- not  真变假  假变真

```python
# and 同真即真
print(True and False)  # False
print(True and True)  # True
print(False and True)  # False
print(False and False)  # False

# or 同假即假
print(True or False)  # False
print(True or True)  # True
print(False or True)  # False
print(False or False)  # False

# not 真变假, 假变真
print(not True)  # False
print(not False)  # True

# 结论:逻辑运算符的运算结果都是bool类型数据

# 练习:
print(not(1 > 2 and 4 < 5))
```

## 9、短路运算

```python
# 短路运算:
a = 1
b = 2
# 当逻辑运算的第一个表达式已经可以决定整个逻辑运算的值的时候,后边的表达式将不会被运行
print(a > b and a < b)

# 在数值型数据中,非0即真
# 在容器型数据中,非空即真
# None 代表False
print(False and 1)  # False
print(0 and True)  # 0
print(12 or False)  # 12
print(None and True)  # None

print(True and False)  # False
print(True and 15)  # 15

print(False or "")  # ""
```

## 10、分支语句

- 单一条件判断

```python
if 条件：
		条件成立时执行的代码
# 格式:
'''
if 条件:
    条件成立时执行的代码
'''

age = int(input('请输入你的年龄:'))

# 上网
if age >= 18:
    print('小帅哥快来玩啊')

print('回家睡觉')
```

- 对立条件判断

```python
if 条件：
		条件成立时执行的代码
else：
		条件不成立时执行的代码
  
  
# if ... else ...
'''
if 条件:
    条件成立时执行的代码
else:
    条件不成立时执行的代码
'''

# 使用分支语句,只有一个分支内的代码会被执行
age = int(input('请输入你的年龄:'))

if age >= 18:
    print('小帅哥,快来玩啊')
else:
    print('老板我就进去看别人玩')

print('回家睡觉')
```

- 多条件判断

```Python
if 条件1：
		条件1成立时执行的代码
elif 条件2：
		条件2成立时执行的代码
elif 条件3：
		条件3成立时执行的代码
else：
		所有条件均不成立时执行的代码
  
  
# 格式;
'''
if 条件1:
    条件1成立时执行的代码
elif 条件2:
    条件2 成立时执行的代码
elif 条件3:
    条件3成立时执行的代码
else:
    所有条件均不成立时执行的代码
'''

# 需求:搭讪,主要是为了问路

age = int(input('请输入对方的年龄:'))

if age > 100 or age < 0:
    print('数据错误')
elif 0<= age <= 18:
    print('小妹妹你真可爱')
    print('叔叔 我们不约而同的认为我很可爱')
elif 18< age <= 30:
    print('美女,你真漂亮')
    print('流氓')
elif 30 < age <= 60:
    print('阿姨,我不想努力了')
    print('瞧你长那样')
else:
    print('老奶奶,您真慈祥')
    print('我北京三套房')

```

- 注意事项：
  - 分支语句中条件可以是bool值或者能够转换为bool值的数据或者表达式
  - 分支语句中只能执行其中一个分支的命令，如果一个条件符合则后续条件均不会进行判断

```python
# 什么样的内容可以作为条件出现?
# bool值或者可以转换为布尔值的数据或表达式
# 表达式:经过运算或者执行后,可以得到一个值的代码块或语句都是表达式
# 分支结构,循环结构,赋值,函数定义 不能作为条件出现
# if  a = 1:
#     print('qqwe')
# a = 1
# if if a==1:
#     print()

# 分支语句中只有一个分支的命令会被执行
# 如果运行过程中其中一个条件成立,则后续所有条件不会进行判断
age = int(input('请输入对方的年龄:'))

if age > 100 or age < 0:
    print('数据错误')
elif age <= 18:
    print('小妹妹你真可爱')
    print('叔叔 我们不约而同的认为我很可爱')
elif age <= 30:
    print('美女,你真漂亮')
    print('流氓')
elif age <= 60:
    print('阿姨,我不想努力了')
    print('瞧你长那样')
else:
    print('老奶奶,您真慈祥')
    print('我北京三套房')
```

## 11、分支语句嵌套

- 在分支语句中包含其他分支语句

```python
# 嵌套:在if语句控制的代码块中存在其他的if语句

# 需求: 如果有钱可以上车(money) 如果上车了又座位可以坐下(seat)

money = 12
seat = True

if money >= 2:
    print('快上车,里边有大座')
    if seat == True:
        print('快坐下吧,别累着')
    else:
        print('我骗你的你能咋办')
else:
    print('穷鬼,跟着车跑吧,不等你')

# 判断时正数负数 还是正奇数正偶数,负奇数,负偶数
# num = 12
# if num < 0:
#     print('负数')
#     if num % 2 == 0:
#         print('负偶数')
#     else:
#         print('负奇数')
# else:
#     print('正数')
#     if num % 2 == 0:
#         print('正偶数')
#     else:
#         print('正奇数')

num = -13
if num < 0:
    print('负', end='')
    if num % 2 == 0:
        print('偶数')
    else:
        print('奇数')
else:
    print('正', end='')
    if num % 2 == 0:
        print('偶数')
    else:
        print('奇数')
```



## 13、三目运算

- 格式：条件成立时返回的数据 if  条件 else 条件不成立时返回的数据

```python
# 三元运算符又叫三目运算
# 格式: 条件成立时返回的数据  if 条件 else 条件不成立时返回的数据

# 需求输出a和b中的最大值

a = 4
b = 5
max1 = a if a > b else b
print(max1)
```

# 循环

## 1、循环介绍

- 有条件的重复做相似的事情
- Python中循环分为while 和for

## 2、while循环的使用

- 格式： while 条件： 循环体
- while 循环的三个必要元素
  - while 关键字
  - 循环条件
  - 循环体
- 构造循环要想的四件事
  - 初始状态
  - 循环条件
  - 要重复做的事情
  - 循环控制

- 案例

```python
# 需求:求1-100的累加和

# 初始状态
i = 1
sum1 = 0
while i <= 100:
    # 求累加和
    # sum1 = sum1 + i
    sum1 += i
    # 为下一次循环做准备,自增
    i += 1

print('1-100的累加和是%d' % sum1)
```

```python
# 需求:输出10以内的所有奇数

# 初始状态
i = 1
# 循环结束条件
while i <= 10:
    # 要循环做什么
    if i % 2 != 0:
        print(i)
    # 为下一次循环做准备  自增
    i += 1
```

```python
# 需求: 1-100的偶数累加和
# 初始状态:
i = 1
sum1 = 0  # 累加器
# 循环条件
while i <= 100:
    # 要做什么?
    if i % 2 == 0:
        sum1 += i
    # 为下一次循环做准备  累加
    i += 1

print(f'1-100的偶数累加和是{sum1}')


# 练习 :计算 1-20 的奇数累乘积.
# 初始状态
i = 1
mult1 = 1
# 循环条件
while i <= 20:
    # 要做什么
    if i % 2 != 0:
        mult1 *= i
    # 自增
    i += 1
print(f'1-20的奇数累乘积是{mult1}')
```

## 3、continue和break

- continue ：跳出本次循环，进入下一次循环

```python
# continue: 跳出本次循环,继续执行下一次循环(不会影响循环的次数)

# 需求: 吃苹果,一个五个.吃到第三个 有个虫子,扔掉第三个,继续吃第四个第五个
# 注意,在循环结构中使用continue要在continue之前添加循环变量的自增,否则可能会造成无法跳出循环(死循环)
i = 1
while i <= 5:
    if i == 3:
        print('这个苹果有虫子,给女朋友吃吧')
        i += 1
        continue
    print(f'我吃了{i}个苹果')
    i += 1


# 写法二
# 可以先进行自增,再进行i的调用,此时,就不用担心continue的问题了
i = 0
while i < 5:
    i += 1
    if i == 3:
        print('这个苹果有虫子,给女朋友吃吧')
        continue
    print(f'我吃了{i}个苹果')


# 输出1-10 的数字
# 在循环体中,continue所在的分支中,continue之后不要书写任何代码,永远不可能被执行
i = 1
while i <= 10:
    print(i)
    continue
    i += 1


# break 和continue只能用在循环体中
# if True:
#     print('123')
#     break
#     continue
    
```

- break ： 结束当前循环，后续循环次数不再执行

```python
# break:跳出循环,终止此次循环之后的所有循环

# 吃苹果案例   吃到第三个 吃出半条虫子,后续无心再吃
i = 1
while i <= 5:
    print(f'我吃了{i}个苹果')
    if i == 3:
        print('吃不下了 虫子个太大吃撑了')
        # break之后的所有代码均不执行
        break
    i += 1

print('吃苹果完成')

# 输出1-10 十个数字
# 在循环体中,break所在的分支中,break之后不要写任何代码,不可能执行
# i = 1
# while i <= 10:
#     print(i)
#     break
#     i += 1
```

- break 和continue 只能在循环体中使用

## 4、死循环

- 死循环不是bug，是程序的一种特殊运行状态，程序员可以用死循环做很多事情
- 死循环就是循环条件永远满足的一种循环

```python
# 什么是死循环?  循环条件永远满足,可以持续循环的代码
# 死循环是bug么?  死循环不是bug可以利用死循环做很多事情
# 死循环可以退出么?  可以,死循环就是循环条件永远成立,但是在程序内部可以有很多方法跳出循环,  break

# 猜拳游戏  (死循环进阶版)
# 需求:在原来猜拳游戏的基础上,让电脑和玩家进行猜拳,一方达到3分则退出游戏,宣布获胜方,否则游戏持续进行
# 普通循环
# player_score = 0
# computer_score = 0
# while player_score < 3 and computer_score < 3:
#     # 获取玩家拳型
#     player1 = int(input('请输入您要出的拳型:(0 石头  1 剪刀  2 布)'))
#     # 获取电脑随机拳型
#     import random
#     computer = random.randint(0, 2)
#     result = player1 - computer
#     # 拳型比对     # 输出结果
#     if result == -1 or result == 2:
#         player_score += 1
#         print('玩家获胜')
#     elif result == 0:
#         print('平局')
#     else:
#         computer_score += 1
#         print('电脑获胜')
#     print(f'当前比分为{player_score}:{computer_score}')

# 死循环
player_score = 0
computer_score = 0
while True:
    # 获取玩家拳型
    player1 = int(input('请输入您要出的拳型:(0 石头  1 剪刀  2 布)'))
    # 获取电脑随机拳型
    import random
    computer = random.randint(0, 2)
    result = player1 - computer
    # 拳型比对     # 输出结果
    if result == -1 or result == 2:
        player_score += 1
        print('玩家获胜')
    elif result == 0:
        print('平局')
    else:
        computer_score += 1
        print('电脑获胜')
    print(f'当前比分为{player_score}:{computer_score}')
    if player_score >= 3:
        print('玩家取得最终胜利')
        break
    if computer_score >= 3:
        print('电脑取得最终胜利')
        break
```

## 5、循环嵌套

- 循环体中包含其他循环结构的状态叫做循环嵌套
- 外层循环执行一次，内层循环将全部执行完成

```python
# 需求:锻炼身体:跑步四圈,做深蹲10分钟,此为一组训练,要做三组
# 在循环嵌套中,外层循环执行一次,内层循环全部执行完成
# 做三组训练的初始状态
i = 1
# 做三组训练后退出循环
while i <= 3:
    print(f'第{i}组训练开始')
    # 跑圈初始状态
    j = 1
    # 跑四圈后退出循环
    while j <= 4:
        print(f'我跑了{j}圈')
        # 内层循环自增变量
        j += 1
    print('我做了10分钟深蹲')
    # 外层循环自增变量
    i += 1
```

- 注意：break 和continue 控制的是当前所在的循环结构

```Python
# 需求:锻炼身体:跑步四圈,做深蹲10分钟,此为一组训练,要做三组
# break 和continue 只能控制本身所在的循环结构
# 在循环嵌套中,外层循环的break和cotinue可能会影响内层循环, 但是内层循环中的break和continue不会影响外层循环

# 做三组训练的初始状态
i = 1
# 做三组训练后退出循环
while i <= 3:
    print(f'第{i}组训练开始')
    # 跑圈初始状态
    j = 1
    # 跑四圈后退出循环
    if  i== 2:
        print('我女朋友来找我了 先休息一下')
        i += 1
        continue
    while j <= 4:
        print(f'我跑了{j}圈')
        # 内层循环自增变量
        if j ==3 and i == 2:
            print('太累了 休息下')
            break
        j += 1
    print('我做了10分钟深蹲')
    # 外层循环自增变量
    i += 1
```

## 6、循环嵌套案例：

```python
# 需求:打印五行五列的一个*组成的矩形
"""
* * * * *
* * * * *
* * * * *
* * * * *
* * * * *
"""

# 打印一行*号,使用while循环实现?
# i = 1
# while i <= 5:
#     print('*', end=' ')
#     i += 1

# 使用while循环将刚才打印的* 输出5次,每次分别占用一行
# i 控制外层循环的次数
i = 1
while i <= 5:
    # j 控制内层循环的次数
    j = 1
    while j <= 5:
        # 打印* 后更换结束符, 防止打印后自动换行
        print('*', end=' ')
        j += 1
    # 一行结束后,强制换行
    print()
    i += 1

# 结论:外层循环控制的是行数, 内层循环控制的是列数 ,外层循环的i变量就是打印时的行号,内层循环的j变量就是打印列时的列号

# 如果现在要打印6行8列的矩阵  i = 6  j = 8

```

```python
# 使用while语句打印三角形,第一行一个* 第二行两个* .....
"""
*
* *
* * *
* * * *
* * * * *
"""

# 外层循环的数量:5 该图形有5行,所以i <= 5
# 内层循环的数量:根据行号进行设定,  第一行 j <= 1  第二行 j <= 2.......

i = 1
while i <= 5:
    j = 1
    while j <= i:
        print('*', end=' ')
        j += 1
    print()
    i += 1
```

```python
# 使用while循环的嵌套打印九九乘法表
"""
1 * 1 = 1
1 * 2 = 2  2 * 2 = 4
.......
"""

# 打印一个九行九列的直角三角形
# 外层循环控制行
i = 1
while i <= 9:
    # 内层循环控制列
    j = 1
    while j <= i:
        # 九九乘法表中,公式规则就是  列 * 行 = 值
        print(f'{j} * {i} = {i * j}', end='\t')
        j += 1
    print()
    i += 1
```

## 7、for循环

- for循环时遍历数据序列，每次获取一个元素，直到元素全部被获取，结束循环。

```python
# for循环的语法结构
"""
for 临时变量 in 数据序列(容器):
    要重复执行的代码
"""
# 循环逻辑:for循环会依次提取数据序列中的元素,每次提取一个,放入临时变量中储存,在循环体中可以使用临时变量,数据序列中有多少个元素,for循环的循环体将会被执行多少次

str1 = 'helloPython'
# 循环遍历str1  遍历:依次提取每一个元素
for i in str1:
    print(i)

# for循环和while循环的区别:
# 1/for循环数据序列,元素提取完成自动停止,不需要使用循环变量
# 2/for循环不需要循环条件,所以也不会有循环条件成立喝不成立的说法
# 3/在开发中我们使用for循环的比例居多,while循环主要是构造死循环结构
# 4/for循环需要配合容器类型(数据序列)进行使用
```

## 8、for循环中的break 和continue

- 和while循环中使用方法一致
  - break：打破循环，后续循环不再执行
  - continue： 结束本次循环，进入下一次循环，不会影响循环次数

```python
# break 打破循环,后续循环不会执行
str1 = 'itheima'
for i in str1:
    if i == 'e':
        print('遇到e了,结束循环')
        break
    print(i)

# continue 跳出本次循环,进入下一次循环,不会影响循环次数
str1 = 'itheima'
for i in str1:
    if i == 'e':
        print('遇到e了,进入下一次循环')
        continue
    print(i)

'''
案例：用for循环实现用户登录
① 输入用户名和密码
② 判断用户名和密码是否正确（username='admin'，password='admin888'） 
③ 登录仅有三次机会，超过3次会报错 
'''
# 循环三次
for i in range(3):
    # 获取用户名和密码
    username = input('请输入您的用户名:')
    password = input('请输入您的密码:')
    # 比对用户名和密码
    if username == 'admin' and password == 'admin888':
        print('登录成功')
        break
    else:
        print('用户名或密码错误')
    if i == 2:
        print('三次机会已经用完,账号被冻结')
```

## 9、for循环嵌套

```python
# 打印一个直角三角形

for i in range(1, 10):
    for j in range(1, i+1):
        print(f'{j} * {i} = {i * j}', end='\t')
    print()

# 在for循环之外还可以调用i 或者j 么? 能

# 在Python中for循环中创建的临时变量可以被外界调用,但是不要用
# print(i)
# print(j)
# 使用for循环临时变量可能会出现报错
# for i in range(1,1):
#     print(123)

# 当for循环执行后,没有一次进入循环体内,也就是遍历的序列是一个空序列,那么临时变量将不会被定义,所以不要使用
# NameError: name 'i' is not defined
# print(i)
```

## 1、循环中的else

- for...else...
- while...esle...
- 如果循环正常结束，则执行else中的代码，如果循环异常结束，不执行else中的代码
  - break 可以打破循环造成循环异常结束
  - continue不会造成循环异常结束

```python
# 语法结构
'''
while 循环条件:
    条件满足,则循环执行此代码
else:
    循环条件不成立执行此代码,执行后循环结构终止
'''

# 需求: 下载一个视频  从0% - 100%,下载完成后,显示下载完成 否则不显示
# 循环条件成立,则反复执行循环体中的代码,如果循环条件不成立,则执行else中的代码
# break打破了循环结构,循环异常终止,没有执行到循环条件不成立的那一刻,所以else不会被执行
# continue没有打破循环结构,循环正常进入循环条件不成立的状态后才会终止,此时执行else中的命令

i = 0
while i <= 100:
    if i == 60:
        print('下载非法文件,已经将你举报,下载终止')
        # break  # 会造成循环异常终止,不会执行else中的代码
        i += 1
        continue  # 不会造成循环异常终止,会执行else中的代码
    print(f'下载进度:{i}%')
    i += 1
else:
    print('下载完成')
```

```python
# 语法结构
'''
for 临时变量  in 数据序列(容器):
    循环执行的代码
else:
    所有元素遍历完成后执行的代码
'''

# 需求: 下载一个视频  从0% - 100%,下载完成后,显示下载完成 否则不显示
for i in range(0, 101):
    if i == 60:
        # print('别下了,网费用光了')
        # break  # 打破循环,造成循环异常结束,不会执行else 中的命令
        print('丢包,这里没有下载好继续下载别的吧')
        continue # 结束本次循环,进入下一次循环,不会造成循环异常结束,会执行else中的命令
    print(f'下载进度:{i}%')
else:
    print('下载完成')
```

# 字符串操作

## 2、字符串的定义以及输入输出

- 字符串定义方式
  - 一对单引号
  - 一对双引号
  - 三对单引号
  - 三对双引号
- 如果我们想输出单引号或者双引号，直接在最外层包裹其他的字符串定义形式即可
- 输入： input
- 输出：print
- 字符串可以进行格式化处理： f-string   传统占位符形式拼接

```python
# 字符串的定义方式
# 单引号
str1 = 'hello world!!!'  # <class 'str'>
print(type(str1))
# 双引号
str2 = "hello python"  # <class 'str'>
print(type(str2))
# 三对单引号
str3 = '''hello bigdata'''  # <class 'str'>
print(type(str3))
# 三对双引号
str4 = """hello china"""  # <class 'str'>
print(type(str4))


# 一对引号和三对引号的区别
# 在一对引号内部进行手动换行,无法修改其字符串的格式,必须使用转义字符\n \t等
str1 = 'hello ' \
       'world'
print(str1)

# 在三对引号内进行手动换行,可以在打印时输出换行格式,无需使用转义字符
str3 = '''hello 
bigdata'''
print(str3)

str4 = """
弃我去者昨日之日不可留
乱我心者今日之日多烦忧
长风万里送秋雁
对此可以酣高楼
......
"""

# 三对引号可以作为多行注释


# 需求 : 输出  I'm Jake.
# 如果字符串被双引号包裹,则内部可以单独使用单引号
print("I'm jake")
# 需求:输出"鲁迅说:I'm a 周树人"
print('''"孔子说:I'm a 文豪"''')
```

```python
# 输入 input
user_name = input('请输入你的用户名')

# 输出
print(f'您的用户名是{user_name}')
print('您输入的用户名是%s' % user_name)
```

## 3、字符串索引

- 索引就是系统给字符串中每一个元素的编号
  - 正数索引：从0开始，从左至右依次递增
  - 负数索引：从-1来时，从右至左依次递减
- 使用索引可以获取字符串中的元素
  - 字符串[元素的索引]

```python
# 什么是字符串索引?
# 就是保存字符串时,将所有字符依次存入字符串所在空间,并且按照顺序将元素依次存放, 为了方便存取数据,我们讲元素进行编号,从0开始依次递增
# 通过下标索引,可以获取元素,或者进行切片等操作

str1 = 'itheima'
# 通过索引获取元素的格式:  字符串[元素索引]
# 需求:想获取第5个元素
print(str1[4])
# 需求:获取t
print(str1[1])

'''
i  t  h  e  i  m  a
# 正数索引
0  1  2  3  4  5  6
# 负数索引
-7 -6 -5 -4 -3 -2 -1
'''
# 结论:字符串中的索引,正数索引从0开始,从左至右依次递增, 负数索引,从-1开始从右至左依次递减
# 需求:使用负数索引取 m
print(str1[-2])
print(str1[-4])
```

## 4、字符串切片

- 字符串切片就是讲字符串中的一部分数据按照指定规则进行分隔得到的新的字符串
- 字符串切片的格式

```python
字符串[起始位置索引：终止位置索引：步长]
```

- 起始位置可以省略：
  - 步长为正：起始位置默认为字符串开始
  - 步长为负：起始位置默认为字符串结束
- 终止位置可以省略：
  - 步长为正：终止位置默认为字符串结束
  - 步长为负：终止位置默认为字符串开始
- 步长可以省略，省略后默认为1，并且可以省略冒号
- 复制字符串：str[:]
- 反转字符串：str[::-1]
- 注意：如果步长为正，则起始位置在终止位置左侧，如果步长为负，则起始位置在终止位置右侧

```python
# 切片:就是按照一定的索引位置和步长将字符串分割出一部分就是切片
# 切片的格式:数据序列[起始位置索引:结束位置索引:步长]   字符串,列表,元组,都可以进行切片

str1 = 'itheima'
# 需求:将the切片出来
# 字符串切片以及其他容器类型的切片操作,都会重新生成一个新的数据序列,不会对原有数据序列产生影响
str2 = str1[1:4:1]
print(str2)

# 切片逻辑
# 起始位置: 字符串切片的起点(包含)
# 结束位置:字符串切片的终点(不包含)
# 在开发中绝大多数范围区间是左闭右开区间,其余内容单独记忆(例如 randint是一个闭区间)
# 步长:步长就是每一次查找数据的间隔(相邻两个索引的差值就是步长)

str2 = '我爱北京天安门,天安门上太阳升!'
# 获取"北京天安门"
print(str2[2:7:1])
# 如果步长为1 可以被省略
# 步长省略后,:也可以省略
print(str2[2:7])

# 起始位置也可以省略
# 如果起始位置省略,步长为正数,则起始位置为字符串开始
print(str2[:7:1])  # 我爱北京天安门
# 如果起始位置省略,步长为负数,则起始位置为字符串末尾
print(str2[:7:-1])  # !升阳太上门安天
# 为什么为空?  字符串切片起点 是索引为2 的位置, 步长是-1  切片区间[2,7),此时从2的位置从右向左步长为1 切片此区域没有数据.
print(str2[2:7:-1]) # 空字符串
# 结论: 如果步长是负数,开始位置要在结束位置右侧,否则没有数据

# 结束位置可以省略
# 如果结束位置省略,步长为正数,则结束位置为字符串末尾
print(str2[8::1])  # 天安门上太阳升!
# 下方表达式和上一行是否含义相同? 不相同,因为结束位置写-1不包含结束位置
print(str2[8:-1:1])  # 天安门上太阳升


# 如果结束位置省略,步长为负数,则结束位置为字符串开始
print(str2[8::-1])  # 天,门安天京北爱我
# 如果结束位置写0  含义也不相同
print(str2[8:0:-1])  # 天,门安天京北爱我

# 需求:在字符串中截取"天门天门"
print(str2[4: 11: 2])  # 天门天门
# 在使用字符串切片进行非1步长书写时,要注意起始位置和结束位置,并且查看间隔

# Python中优雅的字符串反转方式
print(str2[::-1])  # !升阳太上门安天,门安天京北爱我

# python中复制数据序列的方法
str3 = str2[:]
print(str3)  # 我爱北京天安门,天安门上太阳升!
```

## 5、字符串查询

- index：查找字符串中子字符串所在位置i，如果有该字符串，查询其==从左至右==第一次出现的位置的正数索引，==否则报错==。
- find：查找字符串中子字符串所在位置i，如果有该字符串，查询其==从左至右==第一次出现的位置的正数索引，==否则返回-1==。
- rindex：查找字符串中子字符串所在位置i，如果有该字符串，查询其==从右至左==第一次出现的位置的正数索引，==否则报错==。
- rfind：查找字符串中子字符串所在位置i，如果有该字符串，查询其==从右至左==第一次出现的位置的正数索引，==否则返回-1==。
- count：查询子字符串在指定字符串中出现的次数。

```python
str1 = 'hello python'
# index
# 需求:查找p所在的索引位置
# 格式: 字符串.index(self(不用传值), sub(子字符串), start(起始位置), end(结束位置))
print(str1.index('p'))  # 6
# 如果字符串中含有多个子字符串,则会返回指定范围内的从左至右的第一个查找到的子字符串位置索引
print(str1.index('o'))  # 4
# 查询指定范围内的字符串,虽然指定了范围,但是计算索引是从左至右依次递增的
print(str1.index('o', 5, 12))  # 10
# ValueError: substring not found
# 结论:找不到对应的子字符串,则会报错,如果能够查找到数据返回当前子字符串的正数索引
# 指定查找范围是左闭右开区间
# print(str1.index('o', 5, 10))  # 10
print(str1.index('o', 10, 12))  # 10

# find
str1 = 'hello python'
# 需求:查找p所在的索引位置
# 格式: 字符串.find(self(不用传值), sub(子字符串), start(起始位置), end(结束位置))
print(str1.find('p'))  # 6
# 如果字符串中含有多个子字符串,则会返回指定范围内的从左至右的第一个查找到的子字符串位置索引
print(str1.find('o'))  # 4
# 指定范围查找
# 需求:查找o 指定范围为  5,10   10,12
# 结论:使用find进行查询时,如果查询的子字符串不存在,则返回-1,如果存在则返回指定正数索引
# find的查询范围是左闭右开区间
print(str1.find('o', 5, 10))
print(str1.find('o', 10, 12))
# 查询的子字符串可以是单个字符可以是多个字符
print(str1.find('python')) # 6

# rfind
# 和find使用方式完全相同,只是在查询时,从右至左查询,返回第一次查询到的字符索引,返回的依然是正数索引
print(str1.rfind('o'))  # 10
# rindex
# 和index使用方式完全相同,只是在查询时,从右至左查询,返回第一次查询到的字符索引,返回的依然是正数索引
print(str1.rindex('o'))

# 结论:index 和 find 使用方法完全一致,只是,index 在查询不到子字符串时会报错,find会返回-1

# count() 计数
# 使用count 可以返回当前子字符串在指定字符串中出现的次数
# 需求:查询o在str1 中出现的多少次
# 提示:在大多数编程语言中,  计数从1开始数,  索引或编号,从0开始编号
# 格式: 字符串.count(self(不用传值, x(要查询个数的子字符串), start(开始位置), end(结束位置)))
print(str1.count('o'))
# 需求,查询指定范围内h的个数   从1-9  9-12
# 结论:1.count查询的范围是一个左闭右开区间
#     2.如果没有查询到子字符串则返回0  不会报错
print(str1.count('h', 1, 9)) # 0
print(str1.count('h', 9, 12)) # 1
```

## 6、字符串替换

- replace：将旧值替换指定字符串中的新值

```python
# replace
str1 = 'hello python'
# 需求: 将o 替换为 $
# 格式: replace(self(不用传值), old(旧值), new(新值), count(替换次数))
print(str1.replace('o', '$'))  # hell$ pyth$n
# 指定替换次数
# 如果不指定替换次数,默认将所有的制定字符全部替换
print(str1.replace('o', '$', 1))  # hell$ python
# 如果指定的替换次数大于出现的次数,则也是只替换出现的次数
print(str1.replace('o', '$', 10))  # hell$ python
```

## 7、字符串的拆分和合并

- split：字符串按照指定分隔符进行拆分
  - 拆分后得到的结果是有拆分后的字符串组成的一个列表
  - 拆分后，所有的分隔符消失
- join：将字符串序列（容器类型中所有元素均为字符串）按照指定分隔符进行合并

```python
# split 字符串拆分
str1 = 'I love Python and java and c and lixiaolong'
# 需求: 将所有的单词按照空格为分隔符进行拆分,拆分为多个字符串
# split 会按照指定分隔符进行拆分,拆分完成后 会将所有的拆分后的结果以字符串形式保存到列表中
# split(self(不用传值), sep(分隔符), maxsplit(最大分割次数))
print(str1.split())  # ['I', 'love', 'Python', 'and', 'java', 'and', 'c', 'and', 'lixiaolong']
# 指定最大分割次数
# 可以把split看成一把刀,字符串看成一条线,砍一刀分成两份,砍两刀分成3分以此类推
print(str1.split(' ', 3))  # ['I', 'love', 'Python', 'and java and c and lixiaolong']

# 需求:按照以'a'为分割符进行拆分,将str1 最大拆分次数60次
# 使用谁作为分隔符,则拆分后该分隔符消失,
# 最大拆分次数如果超过可以拆分的上限,则保持拆分上线即可,不会报错
print(str1.split('a', 60))  # ['I love Python ', 'nd j', 'v', ' ', 'nd c ', 'nd lixi', 'olong']



# join 字符串合并
list1 = str1.split()
list2 = [1,2,3,4,'abc']
print(list1)
# 将list1  按照指定分隔符❤  合并为一个字符串
# 格式:分隔符.join(iterable(可迭代类型))
print('❤'.join(list1))  # I❤love❤Python❤and❤java❤and❤c❤and❤lixiaolong
# 进行join合并时,要注意可迭代类型中全部元素都要是字符串类型,否则无法合并
print('❤'.join(list2))  # TypeError: sequence item 0: expected str instance, int found
```

## 8、字符串转换

- capitalize：将字符串首字母大写，其余字母小写
- title： 将字符串中每个单词首字母大写（任何非字母字符都可以作为单词分隔符）
- upper：将字符全部变为大写
- lower：将字符全部变为小写

```python
# 字符串中各种大小写转换
str1 = 'hello woRld aNd Python'
# capitalize  将字符串的第一个字母大写,同时讲其余全部字母小写,  对数字和汉字等不做处理
print(str1.capitalize())  # Hello world and python

# title  将所有的单词首字母大写,其余字母变为小写
# 在Python中怎样对单词进行辨别, 非字母字符都可以作为分隔符
str2 = 'hello中国python'
print(str1.title())  # Hello World And Python
print(str2.title())  # Hello中国Python

# upper()将数据全部变为大写
print(str1.upper())  # HELLO WORLD AND PYTHON
# lower()将字符全部变为小写
print(str1.lower())  # hello world and python
```

## 9、字符串两侧指定字符删除

- strip：删除字符串两侧的指定字符
- rstrip：删除字符串右侧的制定字符
- lstrip：删除字符串左侧的指定字符

```python
# strip 去重字符串左右两侧指定字符
str1 = '    hello  python\t \n     '
# strip中如果不传参数,则去除字符串左右两侧的空白(包括空格,换行,制表位等)
print(str1.strip())  # hello  python
# 格式:字符串.strip(self(不传值), chars(可以传一个字符或多个字符))
str2 = '$$$hello Python$$$'
# 删除字符串左右两侧的$符号
# 删除一个指定字符
print(str2.strip('$'))  # hello Python
# 删除多个指定字符
str3 = '13214123123hello Python12314123123123'
print(str3.strip('12'))  # 314123123hello Python12314123123123
print(str3.strip('123'))  # 4123123hello Python12314
print(str3.strip('4231'))  # hello Python
# 结论:如果在strip中填写多个字符,等号左右两侧出现的字符如果在传入的字符串中,则删除,否则保留
# 传入多个字符时,和传入的顺序没有任何关系,只要是传入的字符就不能出现在指定字符串左右两侧,直到出现不属于其内容的字符删除结束

# rstrip 删除字符串右侧指定的字符
print(str3.rstrip('1234'))
# lstrip 删除字符串左侧指定的字符
print(str3.lstrip('1234'))
# TypeError: lstrip arg must be None or str
# strip, lstrip, rstrip 只能接收str类型参数或者None
# print(str3.lstrip(1234))
```

## 10、字符串对齐

- rjust：右对齐
- ljust：左对齐
- cneter： 居中对齐

```python
str1 = 'python'

# rjust 右对齐
# 字符在右侧,不足位置用空格补齐
# 如果不指定填充字符,则自动用空格补齐
print(str1.rjust(10))  #     python
# 格式:字符串.rjust(self(不用传值), width(字符宽度), fillchar(填充字符))
# 指定填充字符 为$
print(str1.rjust(10, '$'))  #$$$$python

# ljust 左对齐
# 和rjust使用方式一致,只不过字符在左侧
print(str1.ljust(10))  # python
print(str1.ljust(10, '$'))  # python$$$$

# center 居中对齐
# 格式: center(self(不用传值), width(字符宽度), fillchar(填充字符))
print(str1.center(10))  #   python
print(str1.center(10, '*'))  # **python**
```

## 11、字符串判断

- 所有的字符串判断结果都是布尔型数据
- isalnum：判断是否都为字母或数字
- isalpha：判断是否都为字母
- isdigit：判断是否都为数字
- isspace：判断是否都为空格
- endswith：是否以。。结尾
- startswith：是否以。。开头
- 其余内容自己测试学习

```python
# 判断字符串内的数据是否符合某种规则

str1 = 'hello itcast'
# startswith 判断是否以...开头
# 需求:判断当前字符串是否以he开头
# 结果是布尔值
print(str1.startswith('he'))  # True
print(str1.startswith('al'))  # False
# 指定范围  左闭右开区间
print(str1.startswith('he', 6, 12))  # False
print(str1.startswith('it', 6, 12))  # True

# endswith 判断是否以...结尾
print(str1.endswith('st'))  # True
print(str1.endswith('al'))  # False
# 指定范围的方式与startswith一致,不在赘述

# is 判断
# isalnum 判断是否全部为数字或字母  不能有空格
print(str1.isalnum())  # False
# isspace  判断是否全部为空格
str2 = ' '
print(str2.isspace())  # True
# isnumeric  isdecimal isdigit  都是判断是否为数字的
str3 = '1234'
print(str3.isnumeric())  # True
print(str3.isdecimal())  # True
print(str3.isdigit())  # True

# 判断中文数字
str4 = '123四肆④亖零〇'
print(str4.isnumeric())  # True  这个方法可以判断中文数字和罗马数字和阿拉伯数字
print(str4.isdecimal())  # False
print(str4.isdigit())  # False

# isidentifier判断是否为标识符
str5 = '2abc'
str6 = 'apple'
print(str5.isidentifier())  # False
print(str6.isidentifier())  # True

# isalpha 判断是否全部为字母
print(str6.isalpha())  # True
print(str5.isalpha())  # False
str7 = 'abc中国'
# 默认将中文当做字母来看
print(str7.isalpha())  # True
# 如果强制判断字母和汉字区分开(了解即可)
print(str7.encode('utf-8').isalpha())  # False
print(str6.encode('utf-8').isalpha())  # True
```

# 列表操作

## 1、列表的查询

- index：从左至右查询元素在列表中所处的位置，如果查询到该元素返回其第一次出现所在位置的正向下标，如果不存在则报错
- count：查询指定元素在列表中出现的次数
- in：查询指定元素是否在列表中
- not in：查询指定元素是否不在列表中

```python
# 索引查询
name_list = ['Bob', 'Jack', 'Rose']

# print(name_list[0])  # Bob
# print(name_list[1])  # Jack
# print(name_list[2])  # Rose
# print(name_list[-1])  # Rose
# print(name_list[-2])  # Jack
# print(name_list[-3])  # Bob

# 结论: 列表中的索引和字符串中完全一致,
# 正向索引从0开始,从左至右依次递增
# 负向索引,从-1开始,从右至左依次递减

# index  查询指定元素在列表中的索引,如果查询成功则返回该元素的正向索引,否则报错
# index  是从左至右查询,返回第一次出现的索引位置

num_list = [1, 2, 3, 4, 5, 6, 7, 8, 5]
# 会返回从左至右第一次查询到的数据索引
print(num_list.index(5))  # 4
# ValueError: 9 is not in list
# 如果没有查询到数据则会报错
# print(num_list.index(9))


# rindex  在列表中没有这个方法
# AttributeError: 'list' object has no attribute 'rindex'
# print(num_list.rindex(5))

# find  在列表中没有这个方法
# AttributeError: 'list' object has no attribute 'find'
# print(num_list.find(5))

# count  计数, 查询指定元素在列表中出现的次数
print(num_list.count(5))  # 2

# in  判断数据元素是否在列表内  如果在  True  如果不在False
# TypeError: argument of type 'int' is not iterable
# print(num_list in 5)
# 注意使用in或者not in  数据元素在左边,  列表或者其他数据序列在右侧
print(5 in num_list)  # True
print(9 in num_list)  # False
# not in  判断数据元素是否不在列表内  如果不在  True  如果在False
print(5 not in num_list)  # False
print(9 not in num_list)  # True
```

## 2、列表的增加

- append： 在类表的末尾追加数据
- extend：将数据序列进行迭代依次提取出每一个元素添加到列表末尾
- insert：在指定位置追加数据元素

```python
# append 在列表末尾追加数据
num_list = [1, 2, 3, 4]
# 能够打印出1,2,3,4,5么?
# print(num_list.append(5)) # None
# 如果直接打印append方法的调用,将不会输出任何内容
# list类型在使用append 方法时不会产生新的列表,而是在原有列表上进行修改
num_list.append(5)
# append 追加的数据,默认追加到列表末尾,追加完成后在原有数据上修改
print(num_list)  # [1, 2, 3, 4, 5]

# # str
# str1 = 'abc'
# # str类型数据,调用replace方法时,不会修改原有数据,而是产生了一个新的字符串
# str2 = str1.replace('abc', 'cba')
# print(str1)
# print(str2)


# extend  追加数据序列
# 格式: 列表1.extend(数据序列)
list1 = [1, 2, 3]
list2 = [4, 5, 6]
# 追加数据序列后,调用extend的列表发生变化, 括号内的数据序列不变
# 其实底层逻辑就是讲括号内的数据序列迭代,依次放入调用该方法的列表中
list1.extend(list2)
print(list1)  # [1, 2, 3, 4, 5, 6]
print(list2)  # [4, 5, 6]

# 追加字符串序列时,会将字母依次拆分并放入列表中
str1 = 'itcast'
list2.extend(str1)
print(list2)  # [4, 5, 6, 'i', 't', 'c', 'a', 's', 't']

# 如果括号内填写的数据,不是数据序列会怎样?
# TypeError: 'int' object is not iterable  括号内必须是可迭代对象
# list2.extend(4)
# 字符串累心哪怕只有一个值,或者只有一个空字符串,都是可迭代类型,同理可知,列表,元组等  哪怕只有以数据或者为空类型也是可迭代类型
list2.extend('3')
print(list2)

# insert 插入
num_list = [1, 2, 3, 4]
# 格式:列表.insert(要插入位置的索引, 要插入的对象)
# 在insert中第一个参数是要插入位置的索引,所以如果插入了数,则该被插入数据的索引变为第一参数所显示的索引
# 原来该位置的元素以及之后的元素下标+1(向后移动一位)
# 如果使用insert进行 插入,可能会造成索引混乱,原来引用的索引发生错误
# 在开发中除非明确所有的索引引用都修改完成,否则不要使用insert
# append 插入数据,要比insert插入数据更安全
num_list.insert(1, 5)
print(num_list)

# extend 和append 进行对比
list1 = [1, 2, 3, 4]
list2 = [5, 6, 7, 8]
# append将list2 当做一个元素追加到列表末尾
# list1.append(list2)  # [1, 2, 3, 4, [5, 6, 7, 8]]
# extend将list2 当做多个元素进行拆分后追加
list1.extend(list2)  # [1, 2, 3, 4, 5, 6, 7, 8]
print(list1)
```

## 3、列表中的删除

- del  先对列表中的元素进行查找（使用下标），找到后使用del删除

- pop：删除类表中指定下标位置的元素，如果不指定默认删除最后一个，并且返回被删除的值
- remove：删除指定值的下标，只删除丛左至右的第一次出现的该值元素
- clear：清空列表，和重新赋值为空有逻辑上的区别。

```python
# del  将数据引用切断
list1 = [1, 2, 3, 4]
# del list1
# NameError: name 'list1' is not defined
# del不仅可以删除元素,也可以删除任何变量,非常强大,但是有些不安全
# print(list1)
# 那del 怎样删除元素呢?  通过索引获取当前元素,并删除
del list1[2]
# IndexError: list assignment index out of range
# 使用下标查找数据时,下标索引不能不存在
# del list1[9]
print(list1)  # [1, 2, 4]

# 如果要是循环中能够删除么?
# 此处并没有删除,因为i是临时变量,我们使用del是在讲i和2的引用关系删除,但是list1 和 2 的引用关系没有删除
# for i in list1:
#     if i == 2:
#         del i
#
# print(list1)

# pop  删除指定索引的元素,并且返回该元素
list1 = [1, 2, 3, 4]
# 删除后可以返回被删除的对象
print(list1.pop(2))
# IndexError: pop index out of range
# 使用pop进行删除的元素下标一定要存在
# print(list1.pop(12))
# 删除后,指定索引位置的元素消失后边的元素统一向左移动一位
# pop也会造成索引变换
print(list1)
# 如果不给pop进行传值,默认删除最后一个元素
print(list1.pop())
# 查看删除后结果
print(list1)

# remove 删除指定的元素(从左至右第一次出现的元素)

list1 = [1, 2, 3, 3, 4, 2, 1]
# 删除列表中的2
# 将从左至右查询第一次遇到的2进行了删除,并不能删除类表中所有的的2
list1.remove(2)
print(list1)  # [1, 3, 3, 4, 2, 1]

# remove会返回被删除的内容? 不会
print(list1.remove(3))  # None
# remove删除的内容不存在会怎样?
# list1.remove(123)  # ValueError: list.remove(x): x not in list

# clear  清空列表
# 就是讲列表置为[],但是与list1 = [] 有本质区别
list1.clear()
print(list1)  # []
```

## 4、列表的修改

- 使用索引修改： 列表[索引] = 新值
  - 查询列表索引值必须在列表中存在
- reverse: 列表的反转
- sort：列表的排序，默认为升序
  - reverse：可以进行列表倒排，降序
  - key:添加函数，使排序规则更加复杂多变

```python
# 通过索引进行修改
list1 = [1, 2, 3, 4]
# 通过索引查找到指定位置的数据,并进行修改
list1[1] = 6
# IndexError: list assignment index out of range
# 获取的元素位置,必须是存在的
# list1[6] = 6
print(list1)

# 通过索引修改可以同时修改多个值么?  不能
# list1[(2,3)] = 6,7
# 可以使用对多变量赋值的形式修改多个值
list1[2], list1[3] = 6, 7
print(list1)

# reverse  列表的反转
list1 = [1, 2, 3, 4]
# 列表反转后,索引倒置,并且在原数据上修改,没有产生新的列表
print(list1.reverse())  # None
print(list1)  # [4, 3, 2, 1]

# sort  排序
list2 = [2, 6, 43, 2, 41, 421]
# sort是对原有的数据进行了排序,没有产生新的列表.同时,默认排序规则为升序
# print(list2.sort())  # None
# print(list2)  # [2, 2, 6, 41, 43, 421]
# 如果我想让列表降序排列怎么办?
# 方法一:可以先排序再反转
# list2.sort()
# list2.reverse()
# print(list2)  # [421, 43, 41, 6, 2, 2]
# 方法二: 可以直接使用倒叙排列
# list2.sort(reverse=True)  # [421, 43, 41, 6, 2, 2]
# print(list2)

# list2.sort(key=排序规则函数)可以帮助我们进行更加复杂的排序
# 根据每个元素 % 7 的余数大小进行排序
# 了解, 不要求掌握 后续会讲
list2.sort(key=lambda x: x % 7)
print(list2)
```

## 5、列表遍历

- for遍历
- while遍历

```python
# while遍历列表
# len()函数可以查询列表的长度

list1 = [12, 123, 1, 1, 1234, 12, 34, 8]
# print(len(list1))
i = 0
while i < len(list1):
    print(list1[i])
    i += 1

# for 遍历列表
# 推荐使用for循环遍历容器类型(数据序列)
for i in list1:
    print(i)
```

## 6、列表的嵌套

- 列表中嵌套其他的子列表，就是列表的嵌套
- 嵌套后的列表可以使用循环嵌套来进行遍历

```python
# 列表的嵌套: 在一个列表中包含其他的列表元素

name_list = [['小明', '小红', '小绿'], ['Tom', 'Lily', 'Rose'], ['张三', '李四', '王五']]

# 需求:想要获取李四的值
# 获取李四所在的子列表的索引,并通过索引获取该子列表值
print(name_list[2])
# 再从子列表中通过李四所在的索引获取其值
print(name_list[2][1])

# 如果我们想要获取嵌套列表中的每一个值,我们需要怎么做?
# 如果进行一次循环,每次循环所得到的都一级列表中的元素,也就是每一个子列表
for i in name_list:
    print(i)

# 如果想要对嵌套后的列表进行输出,需要进行循环嵌套
for sub_list in name_list:
    for name in sub_list:
        print(name)

# 这样就可以进行所有名称的输出了

# 如果当前的列表内的数据不都是子列表,有其他数据类型的数据,则不能直接使用循环嵌套,需要先进行类型判断
```

# 元组操作

## 7、元组的定义

- 单元素元组： 变量 = （数据，）
- 多元素元组：变量 =  （数据1， 数据2， 数据3....）

```python
# 元组:可以储存多个数据,但是元组内的数据不能被修改(元定义后只能被查询)
# 元组的定义:变量 = (数据1, 数据2, 数据3......)
tuple1 = (1, 2, 3, 4)
# 打印后可以展示元组中的全部信息
print(tuple1)  # (1, 2, 3, 4)
# 查询数据类型
print(type(tuple1))  # <class 'tuple'>

# 如果元组中只有一个元素怎么办? 在单一元素后添加逗号
tuple2 = (10)
print(type(tuple2))  # <class 'int'>

tuple3 = ('10')
print(type(tuple3))  # <class 'str'>

tuple4 = (10,)
print(type(tuple4))  # <class 'tuple'>

# 如果小括号包裹单一元素数据不添加逗号,则小括号的意义是提升算术运算符优先级

# 在定义元素或者传值时,元组的括号可以省略

tuple5 = 1, 2, 3, 4, 5
print(tuple5)  # (1, 2, 3, 4, 5)
print(type(tuple5))  # <class 'tuple'>

tuple6 = 5,
print(tuple6)  # (5,)
print(type(tuple6))

tuple7 = (1,2,3,)
print(tuple7)
```

## 8、元组的相关操作

- 元组中的数据不能增删改，所以只能查询
- 元组的查询方式
  - 索引查询：和列表的使用方式一致
  - index ：从左至右查询指定元素在元组中第一次出现的位置索引，如果存在则返回正向索引，如果不存在则报错
  - count：查询指定元素在元组中出现的次数
  - len：查询元组的长度：也就是查询元组中元素的个数

```python
# 元组的增删改:由于元组中的数据不可修改,所以元组中的数据不能进行增删改操作
tuple1 = (1, 2, 3, 4)
# 修改
print(tuple1[2])
# TypeError: 'tuple' object does not support item assignment
# 元组中的数据不能修改
# tuple1[2] = 6
# 删除
# TypeError: 'tuple' object doesn't support item deletion
# 元组中的数据不能删除
# del tuple1[2]

# 查询
# 通过索引进行查询
# 查询方法和列表一致
# 正向索引,从0开始,从左至右依次递增
# 负向索引,从-1开始,从右至左依次递减
tuple1 = (1, 2, 3, 4, 3)
# 需求:通过正向索引取出3
print(tuple1[2])
# 需求:通过负向索引取出3
print(tuple1[-2])

# index  查询指定元素在元组中所在的位置索引
# 需求:查询3所对应的索引值
# index是从左至右依次查询,返回第一个查到的数据的正向索引值
print(tuple1.index(3))  # 2
# 如果查询的内容不存在,则报错
# print(tuple1.index(8))  # ValueError: tuple.index(x): x not in tuple

# count 查询指定元素在元组中出现的次数
print(tuple1.count(3))  # 2
print(tuple1.count(1))  # 1

# len  查询元组的长度(对所有容器适用)  长度就是计算当前容器中有多少个元素
print(len(tuple1))  # 5
# 其实len()就是调用了括号内对象的__len__方法
print(tuple1.__len__())  # 5
```

## 9、字典的定义

- 格式：变量 = {key1 : value1, key2: value2......}
- 空字典定义：
  - {}
  - dict（）
- 字典中键不能重复，是唯一的，但是值可以重复
- 字典中的键要见名知意，体现字典可以见名知意的特性

```python
# 字典:储存多个数据,以键值对形式存储,方便快速存取
# 字典的键要见名知意

# 字典定义格式: 变量 = {键1:值1, 键2:值2.....}
dict1 = {'name': 'xiaoming', 'age': 18, 'gender': '女'}
# 使用print打印可以显示字典中的所有数据
print(dict1)
# 查看字典类型
print(type(dict1))  # <class 'dict'>

# 空字典定义方法
dict2 = {}
# 或者
dict3 = dict()
print(dict2, dict3)
print(type(dict2), type(dict3))

# 见名知意的重要性
# 需求: 使用字典保存一个人的信息  xiaoming  18   男  001
# 保存方式一:
# dict4 = {'name': 'xiaoming', 'age': 18, 'gender': '男', '学号': '001'}
# print(dict4)
# 保存方式二:
# 字典的优势是快速存取,注意命名键的时候要见名知意,并且易于记忆
# 字典占用空间远大于列表,使用字典存储数据本来就是牺牲空间确保时间,所以要尽量利用字典快速存取的特性,而不要想空间的节省
# dict5 = {'xiaoming':18, '男':'001'}  # 不建议这样写

# 定义字典时 ,不能有重复的键,否则后定义的键值对会覆盖先定义的

dict6 = {'name': 'xiaoming', 'age': 18, 'name': 'rose'}
# 字典中的键是惟一的,后定义的内容值会覆盖先定义的
print(dict6)

# 字典中键是唯一的但是值可以随意重复
dict7 = {'name': '小明', 'age': 18, 'id': 18}
print(dict7)
```

## 10、字典的增加

- 字典[新的key] = 值
- 如果key在原字典中已经存在则为修改原key对应的值

```python
# 增  使用新的键 = 值的形式增加键值对
dict1 = {'name':'xiaoming', 'age': 18}
# 使用新的键= 值
# 格式:字典变量[key] = 值  如果为新增,则key在原字典中不存在
dict1['gender'] = '男'
print(dict1)  # {'name': 'xiaoming', 'age': 18, 'gender': '男'}

# 如果原字典中存在该key 则为修改原key所对应的值
dict1['name'] = 'xiaowang'
print(dict1)  # {'name': 'xiaowang', 'age': 18, 'gender': '男'}

# update
# 一般用于两个字典间的拼接
# 如果update中添加的键已经存在则修改原有的值
dict1.update({'id': '001', 'color': 'yellow', 'name': 'rose'})
print(dict1)
```

## 11、字典的删除

- del  查找到字典的键所对应的值进行删除
- clear（）清空字典所在数据空间中的多有键值对
- pop：删除指定键所对应的键值对，会将删除的键值对所对应的值进行返回
- popitem： 删除随机一个键值对，尝试后发现总是删除最后一个，会将删除的键值对以元组的形式进行返回

```python
# del
# 使用del删除键值对,先要找到dict所对应的键,进行删除
# 注意,在字典中键值对是成对出现的,删除键值也就消失了,不能出现单独的键或者单独的值
dict1 = {'name': 'xiaoming', 'age': 18}
del dict1['age']
print(dict1)  # {'name': 'xiaoming'}

# clear() 清空字典
# 使用clear将字典所对应的内存空间中的数据进行了清空
dict1.clear()
print(dict1)  # {}

# 通过之前的学习经验我们猜测 pop是删除简直对用的
dict2 = {'name': 'xiaoming', 'age': 18, 'gender': '男'}
# 使用pop可以根据指定的key删除键值对
# 使用pop删除键值对后会将其键对应的值进行返回
# print(dict2.pop('name'))  # xiaoming
# print(dict2)  # {'age': 18, 'gender': '男'}

# 猜测:popitem也是删除键值对使用的
# 随机删除一个键值对,一般都是删除最后一个
# 删除后会将我们所删除的键值对以元组的形式进行返回
print(dict2.popitem())  # ('gender', '男')
print(dict2.popitem())  # ('age', 18)
print(dict2)  # {'name': 'xiaoming'}

# dict  无序的  因为其不能通过索引进行键值对的获取(了解)
# Python3.5以后,字典中键值对的顺序和我们插入键值对的顺序保持一致,但是该顺序没法被利用(了解)
```

## 12、字典的修改

- 字典[key] = 值
  - 字典中key必须存在
- update：
  - update（键 = 值）
  - update（{键：值}）
  - 对应的键一定存在

```python
# 通过索引修改字典中的键值对
dict1 = {'name':'小明', 'age':18}
dict1['name'] = '小红'
print(dict1)

# update
# 可以进行制定字段值的修改
# dict1.update(name='小绿')
dict1.update({'name': '小绿'})
print(dict1)
```

## 13、字典的查询

- 使用键查询值：字典[key]
  - 查询的键不存在时则报错
- get：字典.get(key)
  - 查询的键不存在时，不报错，可以默认返回None，或者手动设置返回内容
- keys：获取所有的键
- values：获取所有的值
- items：获取所有的键值对组成的元组

```python
# 直接使用key进行查询
dict1 = {'name': '小明', 'age': 18, 'gender': '男', 'id': '001'}
# 查询学员的名称?
print(dict1['name'])

# get查询
# 如果我们查询的键不存在会真么样??? 报错
# KeyError: 'apple'  会出现keyerror  表示查询的键不存在  报错
# print(dict1['apple'])
# 使用get进行查询,只需要在get中传入对应的键即可
# 如果使用get查询的键不存在,则不会报错,会默认返回一个None
print(dict1.get('name'))  # 小明
print(dict1.get('apple'))  # None
# 如果查询的键不存在,get可以自定义默认返回值
# 格式 字典.get(要查询的键, 查询的键不存在时返回的数据)
print(dict1.get('apple', '小刚'))
print(dict1.get('apple', 9))

# keys 获取当前字典中所有的键
print(dict1.keys())  # dict_keys(['name', 'age', 'gender', 'id'])
# keys返回的内容不是列表,而是dict_keys,该数据类型不能直接使用索引查询数据,但是可以进行for遍历
print(type(dict1.keys()))  # <class 'dict_keys'>
keys_1 = dict1.keys()
#  不能使用索引查询
# TypeError: 'dict_keys' object is not subscriptable
# print(keys_1[1])
# 可以被迭代
for i in keys_1:
    print(i)

# values 获取当前字典中所有的值
print(dict1.values())  # dict_values(['小明', 18, '男', '001'])
# dict_values不能使用索引查询,但是可以迭代
print(type(dict1.values()))  # <class 'dict_values'>

# items 获取当前字典中所有的键值对,键值对以元组形式展示
print(dict1.items())  # dict_items([('name', '小明'), ('age', 18), ('gender', '男'), ('id', '001')])
# dict_items不能使用索引查询,但是可以迭代
print(type(dict1.items()))  # <class 'dict_items'>
```

## 14、字典的遍历

```python
# 字典的遍历
dict1 = {'name': '小明', 'age': 18, 'gender': '男', 'id': '001'}

# 使用for循环对字典进行遍历,默认获取的是字典的每一个键
for i in dict1:
    print(i)
'''
name
age
gender
id
'''
# 获取的是字典的每一个键
for i in dict1.keys():
    print(i)
'''
name
age
gender
id
'''

# 获取的是字典的每一个值
for i in dict1.values():
    print(i)
'''
小明
18
男
001
'''

# 获取的是字典中每一个键值对组成的元组
for i in dict1.items():
    print(i)
'''
('name', '小明')
('age', 18)
('gender', '男')
('id', '001')
'''
# 有没有办法可以分别拿到字典的键和值呢?

for i in dict1:
    print(i, dict1[i])

for key, value in dict1.items():
    print(key, value )
```

## 15、集合的定义

- 变量 = {数据1， 数据2， 数据3.。。。}
- 空集合：set（）
- 集合是一个无序的 不重复的数据序列

```python
# 集合: 集合是一个无序,不重复的数据序列
# 无序: 程序员无法控制其排不顺序,  程序员无法使用索引查找或修改数据
# 不重复:没有办法在字典中放入相同的值,会自动去重,类似于字典的键

# 无序:
set1 = {1, 2, 5, 6, 3, 4}
# 程序员无法利用其顺序,有顺序也无用
# 了解:在集合中会使用数据的值计算哈希值,根据哈希值顺序进行排序
print(set1)  # {1, 2, 3, 4, 5, 6}

# 不重复
set2 = {1, 2, 3, 4, 5, 6, 7, 2, 3}
# set会自动去重
print(set2)  # {1, 2, 3, 4, 5, 6, 7}

# 定义空集合
set3 = set()
# {} 是定义空字典的
print(set3)

# 集合中能够储存什么数据?
# 布尔值在进行计算时  True == 1 Fasle == 0
# 基础数据类型 int  float  bool  字符串 都可以用集合储存
set4 = {1, 12.3, True, 0, False, ''}
print(set4)

# TypeError: unhashable type: 'list'
# 列表数据无法用集合储存
# set5 = {1, 12.3, True, 0, False, '', [1, 2]}
# print(set5)

# 元组类型可以放入集合内储存
set6 = {1, 12.3, True, 0, False, '', (1, 2)}
print(set6)

# TypeError: unhashable type: 'dict'
# 字典类型无法用集合储存
# set6 = {1, 12.3, True, 0, False, '', {1:2}}

# TypeError: unhashable type: 'set'
# 集合类型同样不能使用集合嵌套
# set6 = {1, 12.3, True, 0, False, '', {1,2}}

# 结论:列表  字典  集合,不能放入集合中,作为元素出现

# 拓展:不能作为集合元素的数据类型,同样不能作为字典的键出现
dict1 = {(1, 2): 3}
print(dict1)
# TypeError: unhashable type: 'list'
# 列表 字典 集合不能作为字典的键出现
dict2 = {[1, 2]: 3}
print(dict2)
```

## 16、集合的相关操作

- 集合的增加
  - add：添加一个元素，如果值已存在，则去重
  - update： 更新元素（在括号中添加可迭代类型），如果值已存在则去重

```python
# add 增加
set1 = {1, 2, 3, 4}
# set 在使用add命令后,不会产生新的数据,而是原集合中进行修改
set1.add(5)
print(set1)  # {1, 2, 3, 4, 5}

# update 更新
# TypeError: 'int' object is not iterable
# update内部只能填写容器类型(数据序列)
# set1.update(6)
set1.update([6, 7])
print(set1)  # {1, 2, 3, 4, 5, 6, 7}
# 如果更新的数据已经存在,则去重
set1.update([1,2])
print(set1)  # {1, 2, 3, 4, 5, 6, 7}
```

- 集合的删除
  - remove：根据元素值进行删除，如果元素不存在则报错
  - discard：根据元素值进行删除，如果元素值不存在则不报错
  - pop：删除任意元素，并返回被删除的值

```python
# remove
set1 = {1, 2, 3, 4}
# 使用remove可以删除指定值的元素
# set1.remove(3)
# print(set1)  # {1, 2, 4}

# pop 随机删除一个元素,并且将删除的元素返回
# print(set1.pop())
# print(set1)

# discard
# 如果使用remove删除的元素不存在会怎样?  报错
# set1.remove(13)  # KeyError: 13
# 如果使用discard删除元素呢?  不会报错
set1.discard(3)
print(set1)  # {1, 2, 4}
set1.discard(13)
print(set1)
```

- 集合判断：
  - in
  - not in

```python
# 数据是否在集合中
set1 = {1, 2, 3, 4}
# in 判断元素是否在集合中出现
print(4 in set1)  # True
print(5 in set1)  # Fasle

# not in 判断元素是否不在集合中
print(4 not in set1)  # False
print(5 not in set1)  # True

# 注意:格式  元素 in  集合

# 判断的数据必须要在集合中能够被储存
# TypeError: unhashable type: 'list'
# print([1, 2] in set1)
```

- 集合可以使用for循环遍历，但是遍历顺序随机

```python
# for 遍历
set1 = {1, 2, 3, 4}
for i in set1:
    print(i)

# 注意遍历集合,顺序不定
name_set = {'Tom', 'Bob', 'Rose'}
for i in name_set:
    print(i)
'''
Rose
Tom
Bob
'''
```



## 1、公共方法

- `+`
  - 加法运算适用于所有的基础数据类型（int  float  bool）
  - 加法运算所有两侧要是同种数据类型
  - 加法运算再容器类型中是拼接的意思，不是相加计算值

```python
# +法运算,都可以用于哪些数据类型之间
# int float  bool 肯定可以用于加法运算,不再赘述
print(1 + 12.3)  # 13.3

# str 可以相加么? 可以
str1 = 'hello'
str2 = ' python'
# 字符串相加,可以快速将字符串进行拼接
print(str1 + str2)
# 相加过后,str1 和str2 没有发生变化,可以推断+法运算产生了新的数据,源数据不变化
print(str1, str2, sep='\n')

# list 可以相加么? 可以
list1 = [1, 2, 3]
list2 = [4, 5, 6]
# 列表相加可以将列表进行拼接,效果类似于extend
print(list1 + list2)  # [1, 2, 3, 4, 5, 6]
# list相加后,原数据不发生变化,将产生一个新的数据
print(list1)  # [1, 2, 3]
print(list2)  # [4, 5, 6]

# tuple 可以相加么?  可以
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
print(tuple1 + tuple2)  # (1, 2, 3, 4, 5, 6)
# 由于元组内部元素不能修改,索引相加肯定没有对源数据产生影响,而是生成了新的数据

# set
# set1 = {1, 2, 3}
# set2 = {4, 5, 6}
# # TypeError: unsupported operand type(s) for +: 'set' and 'set'
# # set之间不能进行加法运算
# print(set1 + set2)

# dict
# TypeError: unsupported operand type(s) for +: 'dict' and 'dict'
# dict 类型间不能进行加法运算
# dict1 = {'name': '小明'}
# dict2 = {'age':18}
# print(dict1 + dict2)

# 结论: 基础数据类型都可以进行加法运算,容器类型间只有列表,元组,字符串可以进行加法运算


# 不同容器类型间可以相加么?
list1 = [1,2,3]
tuple1 = (1,2,3)
set1 = {1,2,3}
dict1 = {'name': 'xiaoming'}

# TypeError: can only concatenate list (not "tuple") to list
# print(list1 + tuple1)
# TypeError: can only concatenate list (not "set") to list
# print(list1 + set1)
# TypeError: can only concatenate tuple (not "set") to tuple
print(tuple1 + set1)

# 结论,数据类型布偶无法进行加法运算(特指容器类型之间)
```

- `*`
  - 基础数据类型（int  float  bool）都可以进行乘法运算
  - 容器类型只能和int类型数据进行乘法运算
  - 容器类型进行乘法运算，就是将容器复制指定次数，并进行拼接

```python
# * 效果是设么?
# * 什么容器类型可以使用*

# 基础数据类型  int  float  bool都可以使用*法运算
print(12.1 * 2)

# 容器类型的乘法运算
# 格式: 容器类型 * int类型数据
# 乘法运算的 效果,就是讲容器类型复制指定次数,并拼接到一起

# list 可以使用*法运算么?  可以
list1 = [1, 2, 3]
# 将list1 复制3次并进行拼接
print(list1 * 3)  # [1, 2, 3, 1, 2, 3, 1, 2, 3]
# 使用list 类型乘以float类型可以实现么?
# TypeError: can't multiply sequence by non-int of type 'float'
# 乘法运算不能让容器与非int类型相乘
# print(list1 * 1.3)
# list 能乘以负数么?  可以相乘,但是结果为空列表
print(list1 * -3)  # []
# 可以与0 相乘,结果为空列表
print(list1 * 0)  # []

# tuple 可以使用*法运算么? 可以
tuple1 = (1, 2, 3, 4)
print(tuple1 * 2)  # (1, 2, 3, 4, 1, 2, 3, 4)
# tuple 只能与int类型相乘


# set可以使用 * 法运算么?  不可以
set1 = {1, 2, 3}
# TypeError: unsupported operand type(s) for *: 'set' and 'int'
# 集合类型数据不能做乘法运算
# print(set1 * 3)

# dict 能够使用 * 法运算么?  不可以
dict1 = {'name': 'jack'}
# TypeError: unsupported operand type(s) for *: 'dict' and 'int'
# 字典不能做乘法运算
# print(dict1 * 3)

# 乘号左右两侧的数据可以互换位置么?  可以
print(3 * list1)  # [1, 2, 3, 1, 2, 3, 1, 2, 3]
```

- `in`和`not in`
  - 判断元素是否在数据序列当中
  - 字符串，列表，元组，集合 ，字典都可以使用

```python
# in 判断元素是否存在于容器当中
list1 = [1, 2, 3]
tuple1 = (1, 2, 3)
set1 = {1, 2, 3}

print(3 in list1)  # True
print(3 in tuple1)  # True
print(3 in set1)  # True
# 如果要判断是否在set当中,要注意被判断的元素必须可以保存在set当中,如果是列表,字典,集合,则不能判断
# print([1, 2] in list1)  # False  可以判断,引为[1,2] 可以保存在list1当中
# print([1, 2] in set1)  # TypeError: unhashable type: 'list' 不能判断,因为[1,2]不能保存到set1当中


# str类型可以使用in么? 可以
str1 = '123'
# TypeError: 'in <string>' requires string as left operand, not int
# 字符串判断时,左侧的元素只能是字符串类型,否则报错
# print(1 in str1)
print('1' in str1)  # True

# dict 是否可以使用in???
dict1 = {'name': 123}
# dict使用in判断的是当前元素是否是dict中存在的键
print(123 in dict1)  # False
print('name' in dict1)  # True

# 如果使用此方法则不能判断字典  列表 集合
# TypeError: unhashable type: 'list'
# print([1,2] in dict1)

# not in  : 所有用法和in相同,只是取反而已

# 结论:
# 1.使用in 和not in  被判断的元素在关键字左侧, 数据序列在关键字右侧
# 2.如果想要判断该元素是否在容器内,该元素必须能保存到容器内,比如集合不能保存列表,字典,集合 所以就不能判断其类型的元素是否在集合内
# 3.字典判断的是元素是否在keys内,也就是是否是其中的键
```

- 切片
  - 通过切片按照规则获取数据序列中的一部分元素
  - tuple list str 可以使用切片
  - dict  set 不可以使用切片

```python
# 切片:通过切片方法可以按照一定规则截取容器的一部分数据

# str切片
str1 = 'abcde'
# 格式:[起始位置:终止位置:步长]
# 不会修改原有字符串,而是产生了一个新的字符串
print(str1[2:])  # cde

# list可以切片么?
list1 = [1, 2, 3, 4]
# list切片方式方法和str完全相同
# list切片后不会在原有数据上进行修改,而是产生了一个新的列表
print(list1[1:3:1])  # [2, 3]
print(list1)

# tuple 可以切片么?
tuple1 = (1, 2, 3, 4)
# tuple1切片方式方法和str完全相同
# 切片后不会在原有数据上进行修改,而是产生了一个新的列表
print(tuple1[1:3:1])  # (2, 3)
print(tuple1)

# dict可以切片么?  肯定不行,因为不能使用索引获取数据
# set 可以切片么?  肯定不行,因为不能使用索引获取数据

# 结论:
# 1.list str tuple 可以使用切片,格式是:[起始位置:终止位置:步长],三者使用方式完全一致
# 2.所有的切片都不会在原有的数据上进行修改,而是产生一个新的数据序列
# 3.集合和字典无法切片,因为不能使用索引获取数据元素
```

## 2、公共函数

- len ：获取容器内元素个数
- del：删除容器内元素
- max ：获取容器内数据的最大值
- min ： 获取容器内元素的最小值
- enumerate ： 获取容器内元素时可以携带序号
- range：根据一定规则获取整数序列

```python
# len  获取容器类型的元素个数,  或者说获取容器的长度
str1 = '123'
list1 = [1, 2, 3]
tuple1 = (1, 2, 3)
set1 = {1, 2, 3}
dict1 = {'name': 123, 'age': 18}
# 使用len可以获取list  str  tuple set中的元素个数
print(len(str1))
print(len(list1))
print(len(tuple1))
print(len(set1))
# 使用len可以获取dict中的键值对的个数
print(len(dict1))

# len() 可以写成  容器.__len__()
print(list1.__len__())

# del
# 删除容器内指定的元素
# list
# del list1[0]
# print(list1)

# tuple
# del tuple1[0]
# TypeError: 'tuple' object doesn't support item deletion
# 元组内元素不能被删除
# print(tuple1)

# set
# for i in set1:
#     del i

# dict
# del dict1['name']
# del 在dict中删除的是键值对
print(dict1)

# str
# TypeError: 'str' object doesn't support item deletion
# str 不能够使用del 删除内部元素
# 注意 :str内部的元素也是不可修改的,类似于元组
# del str1[0]
# print(str1)

# 结论:
# 1.列表,字典可以使用del删除内部元素,但是,列表中是删除元素,字典中是删除键值对
# 2.使用del 没法循环遍历删除set中的元素,因为引用机制问题
# 3.str  tuple内部的元素都不可更改所以不能使用del删除元素


# max  min
# list tuple set str可以使用max  min获取容器内的最大最小值
print(max(list1))
print(max(tuple1))
print(max(set1))
print(max(str1))
# dict是使用max和min获取键的最大最小值
print(max(dict1))

# enumerate  枚举函数:获取容器内数据时添加序号(默认序号从0开始可以作为索引使用)

list2 = [1, 2, 3, 4, 5, 6, 7, 8]

for i in list2:
    print(i)

# 可不可以同时获取元素的值和元素的索引?  可以 使用enumerate

# for i in enumerate(list2):
#     # 直接打印,获取的是以(索引,值)组成的元组
#     print(i)

# list
for index, value in enumerate(list2):
    print(index, value, sep=' : ')

# tuple
for index, value in enumerate(tuple1):
    print(index, value, sep=' : ')

# set
for index, value in enumerate(set1):
    print(index, value, sep=' : ')

# str
for index, value in enumerate(str1):
    print(index, value, sep=' : ')

# dict  
for index, value in enumerate(dict1):
    print(index, value, sep=' : ')
    
# 结论:所有的容器和课迭代类型都可以使用enumerate,并且产生序号,这个序号并不是索引值,而是在生成序号时默认从0开始,碰巧可以在list,str,tuple中当做索引使用
```

## 3、推导式

- 列表推导式
  - 格式：[要插入的值  for 临时变量 in 数据序列   if  条件]
- 集合推导式
  - 格式：{要插入的值 for 临时变量 in 数据序列 if 条件}
- 字典推导式
  - 格式：{要插入的键：要插入的值 for 临时变量 in 数据序列 if 条件 }
- 没有元组推导式和字符串推导式，因为其内部元素无法被修改

```python
# 推导式:通过一定的规则快速构建数据序列
# 列表推导式
# 获取从0 到9的数据序列
# while
list1 = []
i = 0
while i < 10:
    list1.append(i)
    i += 1
print(list1)

# for
list2 = []
for i in range(10):
    list2.append(i)
print(list2)

# 推导式
# 格式: [要插入列表的表达式 for 临时变量 in 数据序列]
list3 = [i for i in range(10)]
print(list3)

# 使用推导式,创建一个从1-100的偶数的数据序列

# for
list4 = []
for i in range(1, 101):
    if i % 2 == 0:
        list4.append(i)

print(list4)

# 推导式
# 格式: [要插入列表的表达式 for 临时变量 in 数据序列 if  条件]
list5 = [i for i in range(1, 101) if i % 2 == 0]
print(list5)

# 练习:
# 用推导式进行九九乘法表的生成,将所有的算式放入列表中
list6 = []
for i in range(1, 10):
    for j in range(1, i + 1):
        list6.append(f'{j} * {i} = {j * i}')

print(list6)

# 改写为推导式:
list7 = [f'{j} * {i} = {j * i}' for i in range(1, 10) for j in range(1, i + 1)]
print(list7)

# 集合推导式
# 集合推导式和列表推导式完全一致,只不过使用推导式时,外层用{}包裹,并且在序列中会去重
set1 = {i for i in range(10)}
print(set1)

# 获取从1-10 的偶数集合
set2 = {i for i in range(1, 11) if i % 2 == 0}
print(set2)

# 字典推导式
keys = ['name', 'age', 'gender', 'id']
values = ['xiaoming', 18, '女', '001']

# 需求想将key 和value以一对应,形成一个字典
dict1 = {}
for i in range(len(keys)):
    dict1[keys[i]] = values[i]

print(dict1)

# 改写推导式
# 格式:{要插入的键:要插入的值  for 临时变量 in 数据序列  if 条件}
dict2 = {keys[i]: values[i] for i in range(len(keys))}
print(dict2)

# 所有的推导式都可以使用for循环改写,所以我们进行推导式的时候先不要急于求成,多改写几次就不用再改写了直接可以写出推导式
```

# 函数

## 4、函数介绍

- 函数的定义：

  - def 函数名（参数）：

    ​		函数体

    ​		return 返回值

- 函数的调用：函数名（参数）

```python
# 函数: 将特定的功能所对应的代码片段进行打包,封存在一个函数内,如果我们想要重复使用该功能,就直接调用函数即可
# 函数的作用: 提高代码复用率,提高开发效率,易于维护

'''
函数定义的格式:
def 函数名(参数1, 参数2,参数3....):
    函数体
    return 返回值

函数调用的格式:
函数名(参数1,参数2,参数3.....)

# 函数名:绝大多数函数都有函数名,没有函数名的函数不能被复用
# 参数:为了让函数灵活性更高,更容易被复用,会动态对函数进行传值,传递的值可以在函数体内部进行使用
# 函数体: 特定功能的代码,写在函数内部,调用函数时可全部执行
# 返回值: 写在return之后,将函数内部计算或运行得到的数据传递到函数体外部
'''

# 定义的时候可以不传参,如果不传调用的时候也不用传参
def run():
    print('我跑的老快了,没人追的上我,钱包在我手里')
    print('我跑的老快了,没人追的上我,手机在我手里')
    print('我跑的老快了,没人追的上我,女朋友在我手里')

# 调用时可以将函数内的代码全部执行一遍
run()
run()
```

- 函数的调用顺序：从上到下依次执行，先键函数名保存到函数列表中，调用的时候去类表中查询，如果存在则调用其中的代码，如果不存在则报错

```python
# NameError: name 'sing' is not defined
# 函数需要先定义后调用否则会报错
# sing()
# 定义一个唱歌方法
def sing():
    print('我再唱青藏高原')
# 定义一个跳舞方法
def dance():
    print('我再跳广场舞')

sing()
dance()

# 执行顺序: 先讲所有函数的函数名执行一遍将其储存到缓存中的方法列表中,后续调用函数时去方法列表中查询,如果函数名存在,则调用函数内部的代码,如果函数名不存在将报错
```

## 5、函数参数

- 函数的参数可以增加代码的灵活性
  - 在定义时传入的参数是形参，只能在函数体内部使用
  - 在调用的时候传入的参数是实参，可以传入到函数体内部被形参接收

```Python
# 定义一个eat方法,通过传入不同的参数,可以输出不同的生物吃不同的食物


def eat_cat():
    print('猫吃鱼')

def eat_dog():
    print('狗吃肉')

def eat_person():
    print('人吃藕')

# 上述函数定义方法不太方便,因为如果有更多的生物去吃不同的东西,就要重复书写函数不利于函数的复用

# 改进 >> 传参
# 通过传入参数,可以控制函数体内部的执行结果发生变化,让函数更加灵活
def eat(who, food):  # 在定义时传入的参数叫做形参,只能在函数体内部使用
    print(f'{who}吃{food}')

# 在调用的时候传入的参数叫做实参,会传入到函数内部被形参接收
eat('猫', '🐟')
eat('狗', '肉')
eat('人', '藕')

# TypeError: eat() missing 1 required positional argument: 'food'
# 进行传值时需要保证传参数量满足要求,否则会报错
# eat('人')
```

## 6、函数返回值

- 1.返回值是将函数内计算或运行的结果返回到函数外部调用位置,参与计算或运行
- 2.函数可以不写返回值或者只写一个return不写返回值内容,都会默认返回一个None
- 3.return后将会立即跳出函数,如果在retrun后仍有代码,则不会被执行
- 4.return只能返回一个元素,如果想返回多个元素需要使用容器类型

```python
# 返回值:将函数体内部运行或计算得到的数据传递到函数体外部

# def sum(a, b):
#     print(a + b)
#
#
# sum(1, 2)


# 思考?如果我们想在函数体外部使用这个结果进行二次运算我应该怎么做?
# NameError: name 'a' is not defined  a, b 是形参,只能在函数体内部使用
# print(a + b)

# 如果我们想将数据传递出来可以使用return
def sum1(a, b):
    return a + b


print(sum1(1, 3))  # 当函数执行完毕,函数调用位置就替换为函数的返回值
# 返回的数据可以参与计算
print(sum1(1, 3) + 12)
# 注意:返回值内容不会自动打印到控制台,将数据返回后如果想要查看数据需要手动打印或者debug调试


# 如果没有return 那么就没有返回值么?
list1 = [1, 2]
# 因为此处,append方法,没有返回值,默认返回None
print(list1.append(3))  # None


def eat():
    print('猫吃鱼,狗吃肉,奥特曼吃小怪兽')


# 如果没有书写返回值,则返回值为None
print(eat())  # None


# 如果只写了return 没有写返回值内容会怎么样?  None

def sum1(a, b):
    print(a + b)
    return


print(sum1(1, 2))  # None


# return 执行后会跳出函数,return之后的所有代码将不会继续执行
# 在函数中可以有多个return 但是只能执行一个
def function():
    print('hello python')
    return
    return
    # 同一分支中,在return之后的所有代码不会被执行
    print('hello bigdata')


function()


# 返回值只能是一个么?  可以返回多个返回值么?
# 返回值只能是一个元素,如果要返回多个值只能通过容器类型进行打包
def function1():
    return 1, 2, 3, 4
print(function1())  # (1, 2, 3, 4)

# 结论:
'''
1.返回值是将函数内计算或运行的结果返回到函数外部调用位置,参与计算或运行
2.函数可以不写返回值或者只写一个return不写返回值内容,都会默认返回一个None
3.return后将会立即跳出函数,如果在retrun后仍有代码,则不会被执行
4.return只能返回一个元素,如果想返回多个元素需要使用容器类型
'''
```

## 7、函数的嵌套

- 在一个函数体内部嵌套了另一个函数的调用

```python
# 函数的嵌套,就是在一个函数的内部嵌套了另一个函数的调用

def function2():
    print('我是func2-----')
    function1()
    print('我是func2-----')

def function1():
    print('func1执行开始')
    print('func1执行结束')


# def function2():
#     print('我是func2-----')
#     function1()
#     print('我是func2-----')

function2()

# 执行顺序,只要函数在调用之前被定义即可,定义函数的顺序不做规定
```

## 8、局部变量和全局变量

- 局部变量就是在函数体内部进行定义函数体外部无法调用的变量
- 全局变量就是在函数体外部，一般在文件顶格处书写，函数体内外都可以使用的变量
- if 和for结构中的控制语句中定义的变量都是全局变量

```python
# 全局变量就是在函数体外部书写的一般要在文件内顶格书写,在函数体内部外部都可以调用的变量
a = 1
b = 2


def sum1():
    # 函数体内部可以使用
    print(a + b)


sum1()
# 函数体外部也可以使用
print(a)
print(b)

# for 循环中,  if 分支中创建的变量是全局变量还是局部变量呢? 全局变量
# for i in range(10):
#     pass
#
# print(i)
#
# if True:
#     c = 1
# print(c)
```

## 9、gloal

- global能声明我们当前使用的变量是全局变量
- LEGB原则
  - L：在函数体内部查找
  - E：在外层函数中查找
  - G：在全局变量中查找
  - B：在内置变量中查找

```python
# global  全局  :作用就是声明我要使用的这个变量是全局变量

# 如果要在函数体内修改全局变量,就要使用global
a = 100

# 此处,使用a=1相当于再函数体内定义了一个局部变量,并没有修改全局变量的值
# def func1():
#     a = 1
# 如果想要在函数体内修改全局变量就要使用global
# def func1():
#     global a
#     a = 1
#
# func1()
# print(a)

# 扩展:  在Python中所有的变量查询遵循legb原则
# 调用变量时的查询顺序
'''
L:local :首先在函数体内部查询
E:edge :在外部函数中查询
g:global:在全局变量中查询
b:built-in:在系统内置变量中查询
'''
def func1():
    # L:我们再调用变量时,先在函数体内部查找
    a = 1
    print(a)
func1()

def out_func():
    # E: 如果当前函数中没有此变量,我们将在外部函数中查找
    a = 2
    def in_func():
        print(a)
    in_func()

out_func()

def func2():
    # 如果函数体内部和外部函数中都没有该变量,则去全局变量中查找
    print(a)

func2()

# 当这个函数在函数体内部,外部函数中,全局变量中都不存在时, 则去内置变量中查找
print(__name__) # __main__


def func3():
    # a = a + 10
    # 首先用a + 10 进行计算,根据legb原则先从函数体内部查找,查找后发现a 在函数体内部定义,但是在调用时未定义则报错
    # a += 10
    # print(a)
    a = 1

def func4():
    # SyntaxError: name 'a' is assigned to before global declaration
    # 如果要对全局变量进行修改,则先对变量进行global修饰,在修改,否则报错
    a = 15
    # global a
func4()
print(a)

# 能否在函数体内部创建全局变量  可以 只要用global修饰即可
def func5():
    global num1
    num1 = 105

func5()
print(num1)
```

## 10、函数参数进阶

- 位置参数：直接书写参数名，在传值时顺序传值，调用时既不能多传参，也不能少传参（形参）
- 关键字参数：使用”参数名 = 值“的形式进行传参（实参）
  - 可以不按顺序赋值
  - 必须在顺序赋值之后完成赋值
- 缺省参数：在定义函数时，给参数一个默认值，如果调用时，不给其传参，则使用默认值，如果传参，则使用传入的值

```python
# 位置参数:按照位置顺序进行赋值的参数(形参)

def func(a, b, c, d):
    print(a)
    print(b)
    print(c)
    print(d)


# TypeError: func() missing 1 required positional argument: 'd'
# 如果有位置参数没有被赋值,则报错
# func(1, 2, 3)

# TypeError: func() takes 4 positional arguments but 5 were given
# 如果位置参数传参过多也会报错
# func(1, 2, 3, 4, 5)
# 结论:位置参数在使用时需要保证每个参数都被赋值,且不要重复赋值或赋多个值
# 在为位置参数顺序赋值时,所有的参数按序赋值给每个位置参数
func(1, 2, 3, 4)


# 关键字参数 : 关键字参数就是通过"参数名 = 值"的形式进行赋值的参数(实参)

def func(a, b, c, d):
    print(a)
    print(b)
    print(c)
    print(d)

# 使用关键字参数,不需要按照顺序赋值,只要参数名称正确即可
func(d=4, a=1, c=3, b=2)


# 使用参数=值的形式赋值,就是关键字参数
# func(a=1, b=2, c=3, d=4)
# TypeError: func() got an unexpected keyword argument 'f'
# 使用关键字参数赋值时,要注意所使用的参数是否存在,最好是提示出来在用
# func(f=1, b=2, c=3, d=4)
# 注意:使用关键字参数要防止重复赋值
# TypeError: func() got multiple values for argument 'a'
# func(1,2,3,a=5)
# 一般情况下,关键字参数都是给默认参数(缺省参数)赋值的

# 缺省参数:就是在定义时给参数一个默认值,如果参数没有赋值,则使用默认值
def func(a, b, c, d=10):
    print(a)
    print(b)
    print(c)
    print(d)


# 不给缺省参数传值则使用默认值
# func(1, 2, 3)
# 给缺省参数传值则使用传入的值
# func(1, 2, 3, 4)

# 一般使用关键字参数给缺省参数赋值
# func(1, 2, 3, d=12)
# 关键字参数赋值,不能在顺序赋值之前
# func(d=12,1, 2, 3)
```



- 



## 1、不定长参数

- 位置不定长参数（*args）：多余的位置参数，可以被args接收,并且打包为一个元组，保存在args当中。

```python
# 不定长参数主要就是在定义函数时,不确定参数的个数时即可进行不定长参数的书写

'''
位置不定长参数的定义格式:
def 参数名(*args):
    函数体
'''


# def func(*args):
#     print(*args)  # 相当于书写内容为  print(1,2,3)
#
#
# func(1, 2, 3)
# print(1, 2, 3)

# args变量到底内部是什么样子的?
# def func(*args):
#     return args

# 数据传入函数内部时,将传入的多个数据进行打包,转换为一个元组,被args接收.并且在函数体内部可以使用该元组参与运算
# print(func(1, 2, 3))  # (1, 2, 3)


# 案例:
# 输入不确定数量的多个值,判断其中的最大值

def max1(*args):
    max_num = args[0]  # 如果max_num = 0 这个时候我们所有值都没负的时候会判断出错
    for i in args:
        if i > max_num:
            max_num = i
    return max_num


print(max1(1, 4, 5, 3, 6, 12, 3))

# 如果输入的数值全部为负呢?
print(max1(-1, -2, -5))
```

- 关键字不定长参数（**kwargs）：将多余的关键字 参数，打包为一个字典，保存在kwargs当中

```python
# 关键字不定长参数,可以接收多个未定义参数的关键字赋值

'''
关键字不定长参数的格式:
def 函数名(**kwargs):
    函数体
'''


# TypeError: 'a' is an invalid keyword argument for print()
# def func(**kwargs):
#     print(**kwargs)  # 相当于给print输入了多个关键字参数  print(a=1, b=2, c=3)
#
#
# func(a=1, b=2, c=3)

# 使用**kwargs可以将关键字参数进行传递
# def func(**kwargs):
#     print(1, 2, **kwargs)  # 相当于print(1, 2, sep='&', end='a')
#
#
# func(sep='&', end='a')

# kwargs 内部到底是什么存储结构呢?
def func(**kwargs):
    # kwargs 在从传参之后,会将实参位置的所有未定义参数的关键字参数转换为字典的键值对,保存在kwargs当中
    print(kwargs)  # {'a': 1, 'b': 2, 'c': 3}


func(a=1, b=2, c=3)


# 案例:
# 使用创建一个函数可以保存学员的全部信息,并将其储存到字典当中

def student_info(**kwargs):
    print(f'学员信息为:{kwargs}')


student_info(name='xiaoming', age=18, gender='男')
```



## 2、函数定义和调用时各类参数的排布顺序

- 形参： 位置参数》》位置不定长参数》》缺省参数》》关键字不定长参数
- 实参：顺序赋值》》关键字参数赋值
- 在开发中除非有特殊需求，一般参数种类不超过三种，参数个数不超过5个，如果种类或数量太多，会造成我们开发中沟通成本加大

```python
# 在定义函数时:位置参数,缺省参数,位置不定长参数,关键字不定长参数  到底在定义时怎么排列呢?
# 调用函数时:顺序赋值, 关键字赋值  调用时的传参顺序是什么样的呢?


# 定义函数时:形参

# 位置参数和缺省参数的位置关系:
# def func1(a, b, c=10):
#     print(a)
#     print(b)
#     print(c)
# 缺省参数c 能否放到a,b之前或之间
# SyntaxError: non-default argument follows default argument
# 有默认值的参数只能放到没有默认值的参数之后,不能前置
# def func1(c=10,a, b ):
#     print(a)
#     print(b)
#     print(c)
#
# # 赋值时可以不给c传参因为其有默认值
# func1(1, 2)

# 结论: 在定义函数时,位置参数在缺省参数之前

# 位置参数,缺省参数,位置不定长参数之间的位置关系
# 顺序赋值多个参数,位置参数优先接收,然后缺省参数接收数据,多余的参数被args以元组形式打包接收
# 思考:为什么要设置缺省参数呢?  一般情况下,缺省参数是不进行赋值的,因为绝大多数情况下都会赋默认值,极少情况下会使用关键字参数赋值
# 如果放到*args之前,是不是每次给*args赋值,都要给缺省参数赋值,所以不是很方便
# 综上考虑,我们决定将缺省参数放到*args之后

# def func2(a, b, c=10, *args):
#     print(a)
#     print(b)
#     print(c)
#     print(args)
# 传值逻辑如下:1.先给位置参数赋值 2.多余的未接收数据,被args打包为一个元组进行接收  3.缺省参数一般情况下不赋值,如果需要赋值,使用关键字参数赋值
# 在官方文档或者系统模块中,都是这种顺序书写的
# def func2(a, b, *args, c=10):
#     print(a)
#     print(b)
#     print(c)
#     print(args)
#
#
# func2(1, 2, 3, 4, 5)


# 结论:在定义函数时,先写位置参数,再写位置不定长参数,最后写缺省参数


# 位置参数,缺省参数,位置不定长参数,关键字不定长参数之间的位置关系

# def func2(a, b, *args, c=10, **kwargs):
#     print(a)
#     print(b)
#     print(c)
#     print(args)
#     print(kwargs)
#
#
# func2(1, 23, 4, 5, 3, 2, c=1, name='xiaoming', age=18)

# 思考:**kwargs可不可以往前放
# **kwargs只能放到最后,否则会报错

# 结论:形参排布顺序为:位置参数>>位置不定长参数>>缺省参数>>关键字不定长参数


# 调用函数时:实参

def sum1(a, b):
    print(a + b)

# SyntaxError: positional argument follows keyword argument
# 顺序赋值,不能在关键字赋值之后
# sum1(a=1, 2)

# 结论,调用参数时,先使用顺序赋值,后使用关键字赋值
```

## 3、组包和拆包

- 组包：将多个数据，组合为一个容器类型，进行使用或变量保存
- 拆包：将一个容器类型，进行拆分，其中的每一个元组赋值给其他的变量

```python
# 组包:就是讲多个值进行组合,打包为一个容器类型的过程
# 拆包:就是讲一个容器类型,拆分成多个数据,分别赋值给多个变量的过程

# 组包
def func1():
    return 1, 2, 3, 4


# func1返回了多个数据,Python自动将其打包为一个元组,这个过程就是组包
print(func1())  # (1, 2, 3, 4)
# 将多个数据打包整合为一个容器,赋值给变量,这个就是组包过程
a = 1, 2, 3, 4
print(a)

# 拆包(解包)
# 将等号右侧的列表,拆分为四个数据元素,分别赋值给a,b,c,d这个过程就是拆包
a, b, c, d = [1, 2, 3, 4]
print(a, b, c, d)

# 之前我们在循环汇总用过拆包过程
list1 = [1, 2, 3, 4]
for index, value in enumerate(list1):
    print(index, value)

dict1 = {'name': 'xiaoming', 'age': 18}
for key, value in dict1.items():
    print(key, value)

# 同时应用组包和拆包的案例

a = 1
b = 2
# 需求:将a, b进行互换值
# 这个互换过程,是先讲a,b的值提取出来,组包为一个元组,然后进行拆包,将元组内的两个数据分别赋值给,a,b变量
a, b = b, a
print(a, b)

# 注意:字典可以拆包么?可以
dict1 = {'a': 1, 'b': 2, 'c': 3}
# 对字典进行拆包,得到的是字典的键
char1, char2, char3 = dict1
print(char1, char2, char3)

# 集合可以拆包么?  可以
# 对于集合进行拆包,没有任何问题,但是一般不会这样做,因为赋值顺序无法指定
set1 = {'Tom', 'Bob', 'Rose'}
a, b, c = set1
print(a, b, c)
```

## 4、引用

- 数据的三个维度：值， 数据类型，唯一标识
  - 值： 数据计算时使用的值
  - 数据类型：数据的存储类型
  - 唯一标识：id ，也就是数据的内存地址的标识
- 如果我们想要判断id 或者说唯一标识是否相等，我们使用is进行判断

```python
# 在Python中所有的数据分为三个维度: 值(判断==), 数据类型(int...float...), 唯一标识(id)

# 值相等的数据,唯一标识和数据类型不一定相等
bool1 = False
int1 = 0
# 0 和False的值相等
print(bool1 == int1)  # True
# 数据类型不等
print(type(bool1) == type(int1))  # False
# 唯一标识不等
# id 判断数据是否是同一内存空间中的数据(同一内存空间中的数据必相等)
print(id(bool1) == id(int1))  # False

# 值和数据类型相等的,唯一标识不一定相等
list1 = [1, 2, 3]
list2 = [1, 2, 3]
# list1 和list2 值相等
print(list1 == list2)  # True
# list1和list2 数据类型相等
print(type(list1) == type(list2))  # True
# list1 和list2 的唯一标识不等,也就是说,其所在的内存空间不一致
print(id(list1) == id(list2))  # False

# 唯一标识相等的, 值和数据类型必然相等
# 在同一内存空间中只能储存同一个值
str1 = 'abc'
str2 = 'abc'
# str1 和str2 的唯一标识相等
print(id(str1) == id(str2))  # True
# 数据类型相等
print(type(str1) == type(str2))  # True
# 数据值相等
print(str1 == str2)  # True

# 怎样判断id  唯一标识是否相等呢?  is关键字
# 使用is可以判断是否为同一个内存空间中的数据
print(list1 is list2)  # False
print(str1 is str2)  # True
```

## 5、可变类型和不可变类型

- 可变类型：内存空间中的数据可以被修改的数据类型
  - list  set  dict
- 不可变数据类型：内存空间中的数据不可以被修改的数据类型
  - int  float  bool str  tuple

```python
# 传参或者变量的传递是进行了值的传递 还是进行了引用地址的传递呢?

list1 = [1, 2, 3, 4]
list2 = [1, 2, 3, 4]
#  id的值,我们称呼他为引用地址,list1 和list2 的引用地址不相同
print(id(list1))  # 140652966394496
print(id(list2))  # 140652968507776

# 如果我向list1 中添加以数字,次数list2 中的值为多少? [1,2,3,4]
list1.append(5)
print(list1)
print(list2)
# 在list1中添加了数据,那list1的引用地址会发生变化么? 不会变化
# list1,在使用append方法时,是将内存空间中的值进行了变化,没有修改内存地址,所以id值不变
print(id(list1))  # 140652966394496

# 如果我们使用list1 = list2,list1的引用地址发生变化了么?  变化
list1 = list2
# 在对list1赋值时,list2 将list1中的内存地址赋值给了list1,此时,list1和list2指向同一块内存空间
print(id(list1))  # 140652968507776

# 如果在list1中删除下标为1的元素,list2 会发生变化么? 会变化
# list1  和list2 指向同一块内存空间,所以内存空间中的数据发生了改变,list1 和list2 均发生了变化
list1.pop(1)
print(list1)  # [1, 3, 4]
print(list2)  # [1, 3, 4]

# list 内存空间中的数据可以发生改变,这种数据类型我们称之为可变数据类型

# 练习:
list1 = [1, 2, 3, 4]
list2 = [1, 2, 3, 4]
list1 = [1, 2, 3, 4, 5]
list2 = list1
list1.pop(2)
list1 + list2
# list1 和list2  分别是多少
print(list1)
print(list2)

# 练习:
str1 = '12345'
str2 = '12345'
str1 = str2
str1 = '123'
str2 + str1
print(str1)
print(str2)

str1 = '123'
str2 = '123'
print(id(str1))  # 140509725727984
print(id(str2))  # 140509725727984

# 我么可以修改str内部的元素么?  不可以
# TypeError: 'str' object does not support item assignment
# str1[0] = '2'
# 既然内部元素不可修改,系统定义其值相同时,数据引用地址也相同

# 我么称这种内存空间中的数据无法被修改的值为不可变数据类型


# 结论:
# 可变数据类型:  列表,集合,字典
# 不可变数据类型: 字符串,元组,整型,浮点型,布尔型

# 结论:在数据的传递过程中,是引用传递,不是值的传递
```



## 6、引用当做参数传递

- 在函数传参过程中，变量会以引用的形式进行传参，也就是说我们的变量或参数传递是引用传递，不是值传递
  - 如果参数是可变数据类型，那么在函数内修改其引用地址指向空间内的数据，外部数据同时发生变化
  - 如果参数是不可变数据类型，其实也是引用传递，只不过引用地址指向的数据空间中的数据无法被修改

```python
# 将数字1所在空间的引用地址赋值给了a
# a = 1
# 将a所保存的引用你地址给了b
# b = a


def func(num_list):
    print(id(num_list))  # 140490414045760
    num_list.append(2)
    return num_list


# 在进行参数传递时,是进行了地址传递,将list1 的引用地址传递给了num_list,num_list 修改内存空间中的数据时,list1,也会发生变化
list1 = [1, 2, 3, 4]


# print(id(list1))  # 140490414045760
# print(func(list1))
# print(list1)

def func2(num_list):
    print(id(num_list))  # 140326362233472
    # 无论什么情况下,使用=赋值运算,就是讲等号右侧数据的引用地址,赋值给等号左侧的变量
    num_list = [1, 2, 3, 4, 5]
    print(id(num_list))  # 140466340833664
    return num_list


print(id(list1))  # 140326362233472
print(func2(list1))  # [1, 2, 3, 4, 5]
print(list1)  # [1, 2, 3, 4]


# 不可变数据类型
def func1(char1):
    print(id(char1))  # 140228523715632
    # 不可变数据类型,在进行参数传递时,也是引用传递,但是他无法修改原有数据空间内的数据,如果想要修改只能改变引用地址,重新赋值(只有=才有改变引用的功能)
    char1.replace('a', 'b')
    return char1


str1 = 'abc'
print(id(str1))  # 140228523715632
print(func1(str1))  # abc
print(str1)  # abc
```



## 8、函数递归

- 函数内部调用函数本身
- 函数有明确的递归跳出条件
- 不超出最大调用深度

```python
# 函数递归的三个必备条件
'''
1/函数体内部,调用函数本身
2/递归够明确的跳出条件
3/不能超出最大调用深度
'''

# 需求:
'''
func(1) = 1
func(2) = 1 + 2 = func(1) + 2
func(3) = 1 + 2 + 3 = func(2) + 3
func(4) = 1 + 2 + 3 + 4 = func(3) + 4
.....
func(n) = 1 + 2 + 3 .... + n = func(n-1) + n
'''

# RecursionError: maximum recursion depth exceeded
# 这种方式无法跳出递归,所以在使用的时候就会无限递归下去
# def func(n):
#     return func(n-1) + n

'''
func(1) = 1
func(2) = func(1) + 2
func(3) = func(2) + 3
func(4) = func(3) + 4
.....
func(n) = func(n-1) + n
'''

def func(n):
    if n == 1:
        return 1
    return func(n-1) + n


print(func(999))


# Python中默认的最大调用深度,是1000 也就是在Python中函数最多嵌套1000层
# 最大调用深度是为了保证系统性能的,否则无限递归下去,一会内存就满了
# 最大调用深度可以调整,可以调整到非常大的数字只要系统性能跟得上
# RecursionError: maximum recursion depth exceeded in comparison

# 注意事项:
# 在编程初期,尽量少使用递归,但是要理解递归的特性,别人写的递归函数也要能看懂
```

## 9、lambda函数

- 匿名函数，在函数定义时没有函数名
- 可以用变量保存，在变量之后添加括号即可调用

```Python
# lambda表达式,也叫匿名函数
# 格式: lambda 参数: 返回值

# 需求: 根据传入的参数返回最大值  使用lambda函数书写
# 三目运算  :  条件成立时返回的代码 if 条件 else 条件不成立时返回的代码
max_num = lambda a, b: a if a > b else b
# 使用变量可以储存lambda函数
print(max_num(1, 2))
print(max_num(9, 2))

print(type(max_num))  # <class 'function'>


def func():
    print('abc')


print(type(func))  # <class 'function'>
# 通过对数据类型的查看,我们发现lambda和普通函数本质上是一样的,只不过在使用时构造更为简单

# 在使用lambda函数时可以不用变量接收
print((lambda a, b: a if a > b else b)(3, 4))  # 4
# 但是不适用变量接收,lambda函数只能使用一次,使用后集被释放,无法再次使用


# lambda缺点: 没有办法书写负责的函数,因为其没有函数体,只有返回值,所以返回值后边只能书写一个表达式,lambda可读性极差


# 使用lambda完成递归(了解,一般不建议写复杂的代码)
func1 = lambda n: func1(n - 1) + n if n != 1 else 1
# RecursionError: maximum recursion depth exceeded
# 超出最大调用深度,没有明确的递归跳出条件
print(func1(100))

# lambda应用场景
# 可以用于一次性函数使用
# 可以作为函数的参数进行传递

# list  sort(key= )
# lsit sort排序方法中的key所需要的参数就是一个函数,我们可以传入lambda表示

list1 = [{'a': 1}, {'b': 12}, {'c': 10}]
# 排序规则:根据字典的第一个键所对应的值进行排序

list1.sort(key=lambda x:list(x.values())[0])
# 格式: 列表.sort(key = lambda 每次传入的元素: 排序所依据的规则)
print(list1)
```



# 文件

## 1、文件的基本操作

- 文件打开的格式：
  - file = open（文件路径，读写模式）
    - 文件路径：可以写相对路径，也可以写绝对路径
    - 读写模式：r（读取） w（写入） a（追加）
- 文件打开后，必须关闭，否则持续消耗服务器性能。

```python
# 文件读写,在使用的时候和我们正常使用文件一样
# 1.打开文件
# 2.操作文件
# 3.关闭文件

# 打开文件使用open函数即可
# 格式: open(file_name(文件路径), mode(读写模式)) 使用该函数会返回一个文件对象
# 文件路径:可以写相对路径, 也可以写绝对路径,路径需要以字符串形式传入
# 读写模式: r(只读)  w(写入)  a()追加
file = open('python.txt', 'r')
print(file) # <_io.TextIOWrapper name='python.txt' mode='r' encoding='UTF-8'>  在windows中默认读写格式是gbk
print(type(file))  # <class '_io.TextIOWrapper'>
# 将读取出来的内容进行打印
print(file.read())
# 关闭文件
file.close()

# 为什么要关闭文件?
# 在文件打开状态是会保持连接,这种状态下会持续消耗内存,不利于服务器性能优化(内存泄漏)

# 关闭文件后,文件对象有没有被释放?
# 没有释放
print(file)  # <_io.TextIOWrapper name='python.txt' mode='r' encoding='UTF-8'>
# 文件关闭后,相当于与文件的连接状态消失了,但是文件对象没有发生变化
# 在文件关闭后,file对象不能进行任何读写操作,因为已经无法连接文件
# ValueError: I/O operation on closed file.  无法操作一个已经关闭的文件
print(file.read())
```

## 2、文件的读取操作

- read：如果（）内填写数字，则读取指定字符的字符串，每次读取指定字符，在一个文件开启后，多次读取会持续向后读取字符，如果字符全部读取完成将会返回空字符串“”
  - 格式： 文件对象.read(单次最大读取字符数)
- 如果读取的文件不存在则直接报错

```python
# 文件在'r'模式下可以进行文件读取
# read 可以读取文件

# 打开文件
file = open('python.txt', 'r')
# 读取文件
# n:在read中传入数值,代表我们读取的最大字符数
# 如果开发中有一个文本文件,比如网络小说,4个G大小,一次性读取,用户依次读取这么大的文件,极度消耗性能,而且 等待时间过长
# 所以在开发中我们经常会给读取数据的值做一个限定,最大读取字符一般限定为(1024*1024)

# 那我们使用read只能依次读取3个字符,那省下的字符我们怎样读取呢?
# 文件每一次读取,都会持续向后读取,直到文件关闭或程序结束,所以可以使用循环进行读取
# 在所有的文件内容读取完成后,会持续返回空字符串("")
while True:
    content = file.read(3)
    if content == '':
        break
    print(content)

# 关闭文件
file.close()
```

- readline: 每次读取一行数据，以\n为分隔符，在一个文件开启后，多次执行读取操作会持续向后读取，如果字符全部被读取完成，则返回空字符串“”
  - 格式：文件对象.readline()

- readlines：一次性将文件全部读取，读取后，将文字以一行为一个元素保存到列表当中进行返回
  - 文件对象.readlines()

```python
# 除了read外还有一些读取方式
# 文件打开
file = open('python.txt', 'r')
# 文件操作
# readline  使用这种方式读取文件,每次读取一行以\n为分隔符,并且在文件打开状态下,会持续向下读取,直到所有文件被读取完成后,会读取空字符串""
# while True:
#     content = file.readline()
#     if content == '':
#         break
#     print(content,end='')

# readlines 读取所有的文件以\n为分隔符,将所有的行以字符串元素的方式保存到列表当中进行返回
# ['吴丝蜀桐张高秋\n', '空山凝云颓不流\n', '举头望明月\n', '低头思故乡\n']
content = file.readlines()

print(content)
# 文件关闭
file.close()
```

## 3、文件的写入操作

- 使用写入模式‘w’打开文件
  - 如果文件存在，则清空源数据
  - 如果文件不存在，则新建文件，不会报错
- 使用write可以写入字符
- 在windows电脑中书写文件读写时，需要使用encoding进行编码格式指定
  - 格式：open（文件路径， 读写模式， encoding = 编码格式）

```python
# write 写入
# 当文件读写模式时 'w',可以使用文件的写入操作
# 当文件执行写入模式打开时,如果被打开的文件不存在,则重新创建一个新的文件,不会报错
# file = open('test.txt', 'w')
# 当文件执行写入模式打开时,如果被打开的文件存在,则会将源文件内的字符清空
# 如果使用windows电脑进行开发,在写入文件时,需要制定编码格式为'utf-8'
# 如果使用linux 或者mac 默认是utf-8编码 不需要转码
file = open('python.txt', 'w', encoding='utf-8')
# 当完成文件的读写操作时,我们写入文件  和读取文件所使用的编码格式必须一致
# UnicodeDecodeError: 'gbk' codec can't decode byte 0x89 in position 14: illegal multibyte sequence
print(file)  # <_io.TextIOWrapper name='python.txt' mode='w' encoding='UTF-8'>
# 写入操作
# file.write('我爱北京天安门,天安门上太阳升')
# 如果写入的字符串时三对引号包过内部的换行符会不会写入呢?  会写入格式
file.write("""
我爱北京天安门,
天安门上太阳升
""")

# writelines 是配合readlines进行使用的,可以将一个由字符串元素组成的列表一次性写入文件
# file.writelines('我爱北京天安门')
lines = ['吴丝蜀桐张高秋\n', '空山凝云颓不流\n', '举头望明月\n', '低头思故乡\n']
file.writelines(lines)

file.close()
```

## 4、文件的追加操作

- ‘a’：模式下进行文件打开
  - 如果文件不存在，则创建新文件
  - 如果文件存在，则在原有文件内进行字符串追加，不会清空源文件
- 在追加模式下，也是使用write进行文件写入，没有单独的追加方法，写入方式和‘w’模式一致

```python
# 'a'模式写入:追加模式
# 在追加模式下可以进行文件字符的追加,在原有数据的末尾添加 新的字符
# 在追加模式下打开文件,如果文件存在,则不会讲源文件清空
# file = open('python.txt', 'a', encoding='utf-8')
# 在追加模式下打开文件,如果文件不存在,则新建一个文件
# 打开文件
file = open('bigdata.txt', 'a', encoding='utf-8')
# 进行追加操作(注意:没有append方法,追加操作也是使用write进行写入,只不过不会清空源文件)
file.write('乱我心者今日之日多烦忧')
# 关闭文件
file.close()
```

## 5、文件读写模式拓展（了解，看到能明白意思即可）

- a： a  a + ab ab+
  - a：字符追加模式
  - a+ ：字符追加模式下可以进行字符读取
  - ab：字节追加
  - ab+：字节追加模式下，可以进行字节读取

- w： w  w + wb wb+
  - w：字符写入模式
  - w+：字符写入模式下可以进行字符读取
  - wb：字节写入模式
  - wb+：字节写入模式下，可以进行字节读取

- r： r  r + rb rb+
  - r：字符读取模式
  - r+：字符读取模式下可以进行字符写入
  - rb：字节读取模式
  - rb+：字节读取模式下，可以进行字节写入

## 6、文件备份案例

```python
# 需求:用户输入一个文件名,通过文件读写操作进行文件备份,并且将备份文件名称更改为:源文件名[备份].后缀

# 1.获取用户键入的文件名
# 2.要通过文件读写操作进行备份
#   2.1.拼接备份后的文件的文件名
#   2.2.读取源文件
#   2.3.写入新文件

# 1.获取用户键入的文件名
file_name = input('请输入您要备份的文件名称:')
file = open(file_name, 'r', encoding='utf-8')
# 2.要通过文件读写操作进行备份
# 2.1.拼接备份后的文件的文件名
copy_file_name = file_name.replace('.', '[备份].')
# 打开新文件
copy_file = open(copy_file_name, 'a')
# # 读取旧文件数据
# content = file.read()
# # 写入新文件
# copy_file.write(content)
# 一般情况下,文件都是指定单次读取的最大字符的
# 循环进行读取并写入,直到所有字符读取完成
while True:
    content = file.read(3)
    if content == '':
        break
    copy_file.write(content)

# 关闭文件
file.close()
copy_file.close()
```

## 7、rename和remove

- rename可以进行文件的重命名或文件移动
- remove 可以进行文件删除

```python
# 如果想要使用这两个方法,就要去进行模块导入
import os

# rename  重命名  >>>类似于linux命令中的mv
# 格式:os.rename(旧文件路径,新文件路径)
# 需求:将Python.txt重命名为 abc.txt
# rename可以对文件进行重命名
# rename中源文件路径必须存在
# os.rename('bigdata.txt', 'abcd.txt')
# 文件可以通过rename进行移动,移动的位置根据新文件路径决定,移动后同样可以修改名称
# os.rename('abcd.txt', '文件/abcd.txt')
# 文件移动时必须有文件名称,否则无法移动,移动后可以改名
# os.rename('abc.txt', '文件/a.txt')


# remove  删除文件  >>> 类似于linux里的rm
# 可以删除文件,但是不会有任何提示,但是也不会出现在回收站中,误删后无法回复,删除需谨慎
# os.remove('bigdata[备份].txt')
# 可以删除指定路径下的文件
# 如果被删除的路径不存在,则报错  (路径可以使用绝对路径,和相对路径)
# os.remove('文件/a.txt')
# os.remove('python[备份].txt')
# PermissionError: [Errno 1] Operation not permitted: '文件'
# 使用remove不能删除文件夹
os.remove('文件')
```

## 8、文件夹的操作

- mkdir：创建一个空文件夹，不能创建多级文件夹
- rmdir：删除空文件夹，不能删除有文件的文件夹
- getcwd：获取当前使用的工作目录的路径
- chdir：切换当前的工作目录
- listdir：查询指定目录的目录结构，将该目录下所有文件名以字符串形式保存在列表中进行返回
  - 括号内不填写任何内容则为查询工作目录的目录结构
  - 如果填写路径，则是对指定目录的查询

```python
# 在使用下方函数或方法时,需要先导入os模块方可使用
import os
# mkdir 创建文件夹
# FileExistsError: [Errno 17] File exists: 'student'
# 如果创建的文件夹已经存在则报错
# os.mkdir('student')
# 可以在已经存在的文件夹下创建文件夹
# os.mkdir('文件/students')
# FileNotFoundError: [Errno 2] No such file or directory: 'aaa/bbb'
# os.mkdir('aaa/bbb')  # 如果上级目录不存在则无法创建文件夹

# rmdir 删除文件夹
# FileNotFoundError: [Errno 2] No such file or directory: 'aaa/bbb'
# 如果删除的文件已经不存在,则会报错
# os.rmdir('student')
# os.rmdir('文件/students')
# 如果文件夹非空使用rmdir能否删除
# OSError: [Errno 66] Directory not empty: '文件'
# 如果文件非空则不能使用rmdir删除,需要进行递归删除
# os.rmdir('文件')


# getcwd  可以获取当前活动的工作目录 >> 类似于linux中的pwd
# /Users/day08/02-代码
# 默认工作目录就是我们工程所在的根目录
print(os.getcwd())


# chdir  切换工作目录  >> 类似于linux中的cd
# os.chdir('文件')
# /Users/day08/02-代码/文件
# print(os.getcwd())

# listdir  指定目录下的目录结构  >>> 类似于linux命令中的ls
# ['04-文件写入.py', '文件', '.DS_Store', '08-文件夹的操作.py', 'python[备份].txt', '01-文件读写操作体验.py', '00-作业讲解.py', '02-文件的读取.py', 'test.txt', '07-rename和remove.py', '06-文件备份案例.py', '03-其他读取方式.py', '05-文件追加.py', '.idea']
# print(os.listdir())
# os.chdir('文件')
# 如果listdir括号内没有书写对应的路径,则我们使用的路径就是工作目录,如果工作目录进行了切换则查找目录结构的位置也发生了变化
# ['abcd.txt']
# print(os.listdir())

# 查询指定位置的目录结构,可以在listdir括号内填写指定的目录,我们就会查询该目录的结构
# ['abcd.txt']
print(os.listdir('文件'))
```

## 9、批量修改文件名案例

```python
# 需求:批量修改指定目录下所有文件的文件名
'''
1.修改时可以通过参数控制是增加,还是删除字符
2.传入指定字符用于增加或者删除
3.使用rename进行重命名
'''

# 导入os模块
import os

# 定义一个控制增加还是删除的变量,True是增加 False 是删除
flag = False
# 指定字符的定义
str1 = '[黑马出品]'


# 构造多个文件:要在文件目录下构造 test1-test10 十个文件
# for i in range(1, 11):
#     open('文件/test' + str(i), 'w')

# 定义函数
def modify_files_name(flag, str1, path):
    # 切换工作目录为指定的目录path
    os.chdir(path)
    # 遍历指定路径下的所有文件名称
    for file_name in os.listdir():
        # 判断时增加字符还是删除字符
        if flag:
            # 重命名添加文件前缀
            os.rename(file_name, str1 + file_name)
        else:
            # 重命名删除文件名中指定的字符
            os.rename(file_name, file_name.replace(str1, ''))


# 将文件目录下所有的文件添加[黑马出品]的前缀
# modify_files_name(flag, str1, '文件')
modify_files_name(flag, str1, '文件')
```

# 面向对象

## 10、面向对象的思维方式

- 面向对象，是一个编程思想，并不是一项技术，重在理解
- 面向过程：一步一步的完成功能：自上而下，逐步细化
- 面向对象：找到或者构造一个可以完成功能的主体：找到实体，功能完备

## 11、类和对象

- 类就是一系列拥有相同或相似功能的对象的集合，或者说类就是一系列事物的统称
- 对象就是类的具体的表现形式

```Python
1、手机是对象还是类？
2、苹果手机，是对象还是类？
3、iPhonex 手机是对象还是类？
4、我手里的苹果手机，是对象还是类？
```

## 12、类的定义

- 经典类
  - class 类名：
- 新式类
  - class 类名（父类名）：

```Python
# 定义一个类:
'''
格式:
# 经典类
class 类名:
# 新式类
class 类名(父类名):
'''

# 经典类
# 不由任何类派生,或者说不继承任何类
class student:
    pass  # 为了保证代码结构完整,在类下边必须书写表达式,如果没有使用pass占位

# 新式类
# 括号内就是我们的父类,也就是存在一定的继承关系
# 有些地方称其为object的派生类
class teacher(object):
    # pass
    ...  # 为了保障代码结构完整,也可以使用...来进行占位
```

## 13.类的实例化

- 类的实例化又叫做创建对象
- 类中实例化后的对象可以调用类中的方法
- 一个类理论上可以实例化无数个对象
- 格式： 类名（）

```python
# 类的实例化又称为创建对象
# 定义一个类
class Student(object):
    # 定义方法.定义方式和函数定义类似
    def study(self):
        print('我在听直播课,贼有意思,就是学习非常不努力我也能听懂')

    def eat(self):
        print('我在吃脑白金,补补脑子继续学习')


# 类的实例化(创建对象)
# 格式: 类名()

s1 = Student()
# 我们可以直接打印对象,得到的是其所对应的类和所在的内存地址
print(s1)  # <__main__.Student object at 0x7f9be20848e0>
# 也可以打印对象的类型,其实就是我们创建对象所使用的类
print(type(s1))  # <class '__main__.Student'>

# 实例可以调用实例方法
s1.study()
s1.eat()

# 理论上类可以创建无数个实例对象
s2 = Student()
print(s2)

# 类名的定义要使用大驼峰命名法
# 类名严格区分大小写,类名遵循标识符的命名规则
# class ChineseStudent():
#     pass
#
# s3 = Student()
# s4 = student()
# s3.eat()
# s4.eat()
```

## 14、self

- self就是讲调用方法的实例传入方法内部，在方法内部可以调用实例的属性和方法

```python
# 在类的内部定义方法的时候,自动传入一个self
# 在调用实例方法时,不需要对self 进行传值

# self到底是什么?有什么用?
class Student(object):
    def study(self):
        # 由于s1和self指向同一块内存空间,所以其必为同一个对象
        # 也就是说在对象调用方法时会将对象本身传入方法内部进行使用
        print(self)  # <__main__.Student object at 0x7fa2654848e0>
        print('我要学习了,谁也不要打扰我,我知道你们为了超过我不择手段,但是没有用')

    def eat(self):
        # self 有什么作用呢?
        # 可以在方法内部调用实例所拥有的属性或者方法
        print('我要吃饭了吃完就学习')
        self.study()


# 实例化对象
s1 = Student()
print(s1)  # <__main__.Student object at 0x7fa2654848e0>
s1.study()
s1.eat()

# 我们为什么要讲对象传入进去呢?
# 方法时定义在类的内部的,所有的对象共有一个类,所以我们再调用方法的时候,需要传入我们调用方法所使用的类

# s2 调用study方法时所指向的空间和s1无关所以两个对象指向不同的内存空间,修改一个,另一个不发生变化
s2 = Student()
s2.study()
```





## 1、实例属性的添加和获取

- 在类的外部添加和获取实例属性
  - 添加：对象名.属性名 = 值
  - 获取：对象名.属性名
  - 创建对象后，我们对其中一个对象添加实例属性，其他对象不发生变化

```python
# 在类的外部可以添加或获取实例属性
# 格式:
# 实例属性添加:对象.属性名 = 值
# 实例属性获取:对象.属性名

# 定义类
class Person(object):
    def eat(self):
        print('早饭吃了油条和包子,血糖110')


# 实例化属性
p1 = Person()
# 给p1添加实例属性
p1.name = 'xiaoming'
# 调用实例属性
print(p1.name)  # xiaoming

# 如果我们再创建一个对象,其实例属性name是否存在?  不存在
p2 = Person()
p2.age = 18
# AttributeError: 'Person' object has no attribute 'name'
# print(p2.name)
# print(p1.age)
# 结论:对象被创建后,添加实例属性,对其他的对象不产生影响

# 如果我们对同一个实例属性添加两次值会怎样?
p1.name = 'Rose'
print(p1.name)
# 对象名.属性名 = 值,  如果当前对象的该属性名存在,则重新赋值,如果不存在,则新建一个属性
# 类似于dict

# 扩展  __dict__
# 可以通过__dict__去查询对象的属性,该属性以字典形式保存
# 在计算机底层,对象的属性,保存在一个字典结构的空间内,多以多次赋值会覆盖原来的值,给新的属性赋值,会增加属性数量
print(p1.__dict__)

# 对象属性删除del(扩展)
del p1.name
# AttributeError: 'Person' object has no attribute 'name'
print(p1.name)
```

- 在类的内部添加和获取实例属性
  - 添加：self.属性名 = 值
  - 获取：self.属性名
  - 一般实例属性写在实例方法中，调用该方法才能获取实例属性，对象创建后，其中一个实例调用该方法，获取实例属性，其余对象不发生变化

```python
# 实例属性在类的内部添加或获取的格式
# self.属性名 = 值

class Person(object):
    def add_attr(self):
        self.name = 'xiaoming'
        self.age = 18
        self.gender = '女'


# 实例化对象
p1 = Person()
# 创建完成后,p1的实例属性添加了么?
# AttributeError: 'Person' object has no attribute 'name'\
# print(p1.name, p1.age, p1.gender)
# 为什么没有属性呢?  我们定义的添加实例属性的方法没有被调用
# 所以需要先调用添加实例属性的方法,才能使用实例属性
p1.add_attr()
print(p1.name, p1.age, p1.gender)  # xiaoming 18 女

p2 = Person()
# AttributeError: 'Person' object has no attribute 'name'
# 哪怕是在类的内部添加实例属性,两个对象之间没有任何关系,也就是执行方法在第一个对象中添加了实例属性,对第二个对象不产生影响,如果想要添加实例属性,需要再次调用方法
# print(p2.name)

# 在类的外部可以修改类内部添加的实例属性么?  可以
p1.name = 'Rose'
print(p1.name)  # Rose

# 同一个对象在类的内部和外部添加实例属性 本质上是一样的
# 在类的外部使用对象名,其实使用的是对象的引用地址,在其引用地址位置添加了对应的实例属性
# 在类的内部使用self,其实也代表该应用地址,也是在其应用地址位置添加了对饮的实例属性

# 为什么在类的内部要使用self 而不使用对象名?   简便,灵活.复用性高
# 1.我们每次使用的对象不一致,如果使用对象名,需要每次都传入不同的对象名,或者每个对象定义一个方法,这样不利于代码的复用.
# 2.在某些时刻,我们在没有将对象赋值给变量的时候,就需要添加其属性,这个时候,没有办法获取对象的名称.
```

## 2、`__init__（）`方法

- `__init__()`方法在对象创建完成后，初始化对象时，自动调用
- 在init方法中添加的属性，由于每个对象都会执行该方法，所以都包含该属性，被称之为共有属性
- 在init方法之外添加的属性，由于不是每个对象都拥有，所以被称之为独有属性

```python
# __init__():在对象创建完成后,初始化对象过程中自动调用的方法

# class Person(object):
#     def __init__(self):
#         print('我被调用了')


# init方法在什么时候被调用

# p1 = Person()  # 只需要实例化对象,不需要手动调用,init方法即可自动调用
# 在类的内部和外部都可以轻松调用init方法,但是不要调用
# p1.__init__()

# 既然init方法可以在对象被创建后自动调用,那我们讲添加实例属性的代码写入init方法中,是不是可以每个对象被创建后,都自动添加实例属性呢?

class Person(object):

    def __init__(self):
        # 由于init方法在对象被赋值之前就已经调用了,多以此时不能使用对象名.属性名进行属性添加,只能使用self
        self.name = 'xiaoming'
        self.age = 18


p1 = Person()
# 由于其自动调用init,所以对象被创建后,自动拥有name和age属性
print(p1.name)  # xiaoming
# 创建多个对象,每个对象都包含init中的属性名
p2 = Person()
print(p2.age)  # 18

# 结论: 在init方法中添加的属性,每一个由该类创建的对象,都包含,这种属性,我们称之为公有属性
# 在init之外添加的属性,只有被添加属性的对象本身才拥有,这种属性被称为独有属性
```

## 3、带参数的`__init__()`方法

- init方法在对象被创建时，可以将“类名（）”这里边括号添加的参数传递到init方法内部
- 在接收到参数时，可以动态给对象添加实例属性
- 如果init方法添加了参数，那么在创建对象时，必须给其赋值，否则报错

```python
# 每次我们创建对象时,如果使用init方法,是不是只能添加同一个值的属性呢?
# 如果我们能够将参数传递到init方法中,是不是就可以在创建对象时,动态添加属性值了呢?
# 我们怎样给init进行传参呢?
# 面临的问题: 1.我们不需要手动调用init  在哪里给他传参呢?  2.我们传参时到底传什么参数给init方法呢?

# 在实例化对象时,类名(参数1, 参数2....)这些参数会传递给init方法,进行使用

# class Person(object):
#     def __init__(self, name, age):
#         print(name, age)


# TypeError: __init__() missing 2 required positional arguments: 'name' and 'age'
# p1 = Person()
# 既然我们给init方法中添加了参数,就必须传值,否则就会报错
# 在Person的括号中传参,就可以传递到init方法中,传参的数量,就是init方法中除了self之外的位置参数的数量
# p1 = Person('Jack', 18)  # Jack 18
# 结论: 在Person类创建对象时,在()内添加参数,可以被init接收但是,传参数量和inti方法中的形参必须一致

# 怎样实现动态的实例属性添加呢?

class Person(object):
    def __init__(self, name, age):
        # self.属性名 = 参数  将函数外部传递进来的参数赋值给对象,创建实例属性
        self.name = name
        self.age = age


# 实例化对象时要正确传参
p1 = Person('Rose', 17)
print(p1.name, p1.age)
# 创建第二个对象,查看属性是否动态传递成功
p2 = Person('Jack', 18)
print(p2.name, p2.age)

# 通过这种方式,我们在创建对象时可以指定其不同对象属性的值不同,但是所有的对象包含的属性类别相同
# 这种形式下一定要给每一个对象单独赋值,或者给init方法中的属性一些默认值,否则会报错
```

## 4、`__str__()`方法

- 在类的内部实现`__str__()`方法，他会在我们讲对象转换为str类型时自动调用，返回其return内的数据
- str方法内只能返回str类型的数据
- str方法自动调用的场景
  - 强制类型转换： str（对象）
  - ==隐式==类型转换： %s作为占位符接收对象，或者 print打印等，都会自动调用

```python
# __str__()方法是在数据被转换为str类型时自动调用的方法

class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.age = age


    def __str__(self):
        # 在__str__方法中只能返回字符串类型数据,否则就会报错
        # TypeError: __str__ returned non-string (type int)
        # return 123
        # return None
        return f'我的名字是{self.name}, 我的年龄是{self.age}'


p1 = Person('Rose', 18)
# 如果我们打印p1会在控制台输出什么? # <__main__.Person object at 0x7fb70db848e0>
# 默认会输出对象类型,和内存地址
# print(p1)
# 我们如果让其在打印时输出我们想要输出的内容?  重写str方法

# 重写str方法后
# 结论:打印p1时,会自动调用__str__()方法
print(p1)

# 是因为print方法我们才将p1变为我们改写的str方法中的内容么?  不是
# 其实我们再执行print时,会做一次隐式的数据类型转换 也就是使用str(对象)

str1 = str(p1)
print(str1)

# 在什么场景下会自动调用__str__呢?
# 1.强制类型转换  str(对象)
# 2.隐式类型转换  %s 作为占位符,接收p1   print打印
```

## 5、`__del__()`方法

- 对象被释放前，自动执行`__del__()`方法
- 释放对象的几个场景
  - 出了函数作用域后，局部变量被释放
  - 程序执行完成后，所有变量被释放
  - 执行del操作后，可以提前释放变量

```python
# 之前我们学过del操作
# del 变量名  或者  del (变量名)

# del操作  可以切断数据和引用位置的联系
# 切断引用后,a 没有引用任何数据,1也没有任何变量引用,所以双双被释放掉
# a = 1
# del a
# print(a)

# __del__()方法,在c语言中成为析构函数
# 在对象被释放前自动执行该方法,执行后,对象立即被释放

# 定义类
# class Person(object):
#     def __init__(self,name, age):
#         self.name = name
#         self.age = age


# p1 = Person('Rose', 18)

# del p1
# NameError: name 'p1' is not defined
# 在这种情况下,我们能否知道p1已经被释放了?  没有提示
# 如果已经被释放了还继续使用,是不是会报错? 会报错
# 我么你怎样去进行提示?  使用__del__()
# print(p1)


class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __del__(self):
        print('我被释放了,真爽',self.name)


p1 = Person('Rose', 18)

# del p1 # 使用del造成p1被提前释放,在程序结束前将对象释放了
# p1被释放后,我们就接收到了提示,证明p1不存在了,之后就不要使用了
# print(p1)
# 如果没有del操作,则在程序结束后,会将所有的变量进行统一释放
# print('程序结束')

# 结论:在对象被释放时,会自动调用__del__方法,并且,使用del操作可以提前释放对象,否则在程序结束后,也会将变量统一释放

# 如果一个对象,或者说同一块内存空间,被多个变量引用,使用del可以释放么?
# p2 = p1  # p1和p2指向同一内存空间,或者说两个变量引用同一个数据
# del p1
# # 如果只删除p1的引用,对象还被p2引用着,该对象不会被释放,必须切断所有引用,才能正常 释放
# del p2
# # 如果将p2的引用也切断了,则对象正常释放
# print('程序结束')


# 结论:对象被引用时无法释放,除非程序终止,如果一个对象被多个变量引用,必须将所有引用切断才能正常释放,否则无法释放对象
# 举例:多个主人牵一条狗,如果有一个主人没有撒手,狗也跑不了
p4 = None
def func():
    p3 = Person('xiaoming', 15)
    global p4
    p4 = p3
    print(p3)

func()
# 上述代码可以推断,在函数执行完成后,出了作用域,会将函数内所有的临时变量释放掉,除非其被外部变量引用

print('程序结束')

# 切断引用或释放对象的几个场景
# 1.出了函数作用域会自动释放函数内的局部变量
# 2.程序结束会自动释放所有的变量
# 3.使用del操作可以提前释放变量
```

## 6、面向对象案例

```python
'''
需求:
1.创建phone类  Phone
2.在类中添加方法,  充电   听歌  打电话  玩游戏
3.每个手机都有初始的电量,并且在创建对象时可以手动输入电量
4.充电可以输入充电时长, 充电1小时获得20个单位的电量
5.听歌(15)  打电话(10)  玩游戏(30)都会消耗电量
6.电量最高100  最低 0  充电到100 就就会结束,  使用手机,如果电量不足以支撑完成操作则警告,并自动关机
'''

# 分析:
'''
1.在上述需求中有哪些类?  一个 Phone
2.在上述类中有哪些属性?  一个 电量
3.在上述类中有哪些方法?  四个  充电  听歌 打电话 玩游戏
4.有哪些数值判断:在使用手机  和充电过程中,让电量范围保持在0-100之间
'''


# 定义类
class Phone(object):

    def __init__(self, power):
        """初始化对象的方法,在定义对象时,需要输入电量"""
        if power >= 100:
            self.power = 100
        elif power <= 0:
            self.power = 0
        else:
            self.power = power

    def add_power(self, time):
        """充电方法"""
        print(f'充电开始,共充电{time}小时')
        # 对于对象中的电量进行增加
        self.power += 20 * time
        if self.power > 100:
            self.power = 100
            print('充满电了,赶紧收起来吧不然充坏了')
        else:
            # 输出电量
            print(f'充电结束,当前电量为{self.power}')

    def music(self):
        """听音乐"""
        print('音乐真好听呀,再来一首大河向东流')
        self.power -= 15
        if self.power > 0:
            print(f'听歌结束,剩余电量为{self.power}')
        else:
            # 在手机没电时需要将电量赋值为0,防止出现负数电量
            self.power = 0
            print(f'手机没电了赶紧充电吧,别听歌了')

    def call(self):
        """打电话"""
        print('给女朋友打个电话,希望还没睡觉')
        self.power -= 10
        if self.power > 0:
            print(f'电话打完了,成功分手,剩余电量为{self.power}')
        else:
            # 在手机没电时需要将电量赋值为0,防止出现负数电量
            self.power = 0
            print(f'手机没电了赶紧充电吧,别打电话了')

    def play_game(self):
        """玩游戏"""
        print('我最爱玩游戏了,每次都赢没办法,就是这么厉害')
        self.power -= 30
        if self.power > 0:
            print(f'游戏打完了,打游戏太爽了,我打游戏,舍友打我,剩余电量{self.power}')
        else:
            # 在手机没电时需要将电量赋值为0,防止出现负数电量
            self.power = 0
            print('手机没电了,赶紧充电吧,别玩游戏了')


p1 = Phone(20)
p1.music()
p1.call()
p1.play_game()
p1.add_power(4)
p1.add_power(4)
print(p1.power)
```

## 7、单继承

- 单继承就是某个类只继承自一个父类，同时，继承关系中可以有多级继承
  - 继承过程中，子类可以使用父类的所有非私有属性或方法
  - 如果父类或更高级的父类，实现了init方法，并且进行了参数设定，实例化子类对象时必须传值

```python
# 单继承:一个子类,只继承一个父类,并且可以多级继承

# 定义一个Person类
class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.__age = age

# 定义一个Father类,继承Person
class Father(Person):
    def __sing(self):
        print('我会唱学猫叫,跟我一起来')

    def dance(self):
        print('我会跳四小天鹅,就是天鹅还缺仨')

# 定义一个Son类,继承Father
class Son(Father):
    def play(self):
        # AttributeError: 'Son' object has no attribute '_Son__sing'
        # 继承父类时,只能继承父类中的非私有属性和方法
        self.__sing()
        self.dance()

# 实例化一个Son对象
# TypeError: __init__() missing 2 required positional arguments: 'name' and 'age'
# 应为son继承了father father继承了person, 在person中书写了init方法的参数,所以此处必须传参
# s1 = Son()
s1 = Son('xiaoming', 12)
# s1 继承了父类的属性和方法,在Son类中我们没有书写任何内容,但是可以调用父类及其父类的父类中的方法
# s1.sing()
# 调用方法时如果父类中书写了 我们就可以调用到,但是父类中的私有属性或者方法,我们无法调用
# AttributeError: 'Son' object has no attribute '__age'
# print(s1.__age)
# AttributeError: 'Son' object has no attribute '__sing'
# s1.__sing()
# s1.play()

# 结论:
# 1.在继承中可以多级继承,子类中可以使用父类及父类的父类中非私有的属性和方法
# 2.如果在父类或者更高级的父类中实现了init方法,并且书写了参数,则实例化对象时,必须传值

# 扩展:
# 怎样查询类的继承链条
# (<class '__main__.Son'>, <class '__main__.Father'>, <class '__main__.Person'>, <class 'object'>)
# 使用类名.__mro__可以输出类的继承链条,同时这个顺序也是方法或属性查找的顺序
print(Son.__mro__)
```



## 8、多继承

- 一个子类，继承多个父类的过程就是多继承
- 在多继承中，子类可以调用多个父类中的非私有方法或者属性

- 多继承中，如果出现同名属性或方法，优先调用继承位置靠前的父类中的方法或属性

```python
# 多继承:一个类定义时,继承了多个父类,同时可以使用多个父类中的方法或者属性
# 格式: class 子类名(父类名1, 父类名2):

class Father(object):
    def dance(self):
        print('我现在要跳一个舞,赶紧出去')

    def sing(self):
        print('我要唱一个学猫叫,一起来')


class Mother(object):
    def dance(self):
        print('我现在要跳一个广场舞,离我远点,不然摔倒了赖你')

    def sing(self):
        print('我要唱一个大河向东流,赶紧跑')


# 同时继承两个父类,则在使用子类对象时可以调用两个父类中的所有非私有属性和方法
# class Son(Father, Mother):
#     pass
#
#
# s1 = Son()
#
# s1.dance()
# s1.sing()

# 疑问: 如果两个父类中有重名方法该怎么办?
# 在下述情况下,只会调用Father类中的sing和dance方法
# class Son(Father, Mother):
#     pass
#
#
# s1 = Son()
#
# s1.dance()
# s1.sing()

# 如果我将两个父类的顺序进行调换
# 此时,只会调用Mother类中的sing 和dance方法
class Son(Mother, Father):
    pass


s1 = Son()

s1.dance()
s1.sing()

# 结论:如果存在同名方法,在继承时,谁的继承位置更靠前就调用谁内部的代码
```

## 9、子类中重写父类方法

- 子类中重写父类方法，则调用方法时，直接调用子类中的方法，不会调用父类的
- 重写时只要方法名称相等即可，不需要进行参数的校对
- 为什么可以重写父类方法，因为在调用方法或者属性时，会按照继承层级依次查找

```python
# 定义一个Person类
class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.age = age


# 定义一个Father类,继承Person
class Father(Person):
    def sing(self):
        print('我会唱学猫叫,跟我一起来')

    def dance(self):
        print('我会跳四小天鹅,就是天鹅还缺仨')


# 定义一个Son类,继承Father
class Son(Father):
    # 需求:在Son执行sing方法时,我么你让他唱一分钱
    def sing(self):
        print('我喜欢唱一分钱, 你自己学猫叫吧')

    # 我们进行方法 重写的时候,不需要关注参数,只需方法名相同即可
    def __init__(self):
        pass


# s1 = Son('xiaoming', 12)
# s1.sing()

# 为什么子类中重写了父类方法就不能进行调用了?
# 之前我么讲了__mro__  打印继承顺序,同时其也是方法或属性的调用顺序,例如想使用Son对象调用sing方法,但是不知道sing在哪个类中
# 所以,系统先去当前Son类中查找,查看是否存在sing方法
# 如果存在,则调用,如果不存在,则去父类中 Father中查找,如果Father类中存在sing则调用,如果不存在,则去更高级父类(person)中查找
# 直到查询到object类中,如果依然不存在,则报错

# 所以如果子类中书写了对应的方法,则父类中的同名方法无法被调用

# 可不可以让Son类不需要使用name和age就可以创建对象呢?  在Son中重写init方法
s1 = Son()
s1.sing()
```



## 1、在子类中调用父类方法

- super（）.方法名（）
- 类名.方法名（self）
- spuer（要从哪一个类的上一级类开始查找， self）.方法名（）

- 子类调用父类方法时，一般都是想对父类方法进行扩展

```python
class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def driver(self):
        print('开车太好玩了 ,10迈,太快了')


class Father(Person):
    # 如果我们现在想在原有父类方法基础上扩展,例如我们现在需要重写一个init方法
    # 可以接收 name, age ,gender三个属性
    def __init__(self, name, age, gender):
        # 在父类方法中已经添加了name,和age我们可不可以直接使用呢???
        super().__init__(name, age)
        # 在父类方法的基础上我们在添加一个子类方法独有的功能
        self.gender = gender

    def driver(self):
        print('我要去天安门完,开挖掘机不让我进')

    def __str__(self):
        return f'我的姓名是{self.name},我的年龄是{self.age},我的性别是{self.gender}'

class Son(Father):
    def driver(self):
        # 调用Person中的dirver
        # TypeError: driver() missing 1 required positional argument: 'self'
        # Person.driver()
        Person.driver(self)
        # 从Father类的上一级类开始查找方法,并进行调用
        super(Father,self).driver()

        # 调用Father中的dirver
        super().driver()
        # 格式:super(从哪个类的上一级开始查找,self).方法名()
        # 如果类名是当前类,可以省略括号内的内容
        super(Son, self).driver()
        # 书写特有功能


# 所有的参数都传递到了Father类中,并且添加为当前对象的属性
print(Father('Jack', 28, '男'))
s1 =Son('xiaoming', 12, '男')
s1.driver()

# 子类中调用父类方法的三种方式:
# super().方法名()   # 只能调用当前类的上一级类中的方法或函数
# 类名.方法名(self)  # 所使用的类名,必须在当前类的继承关系中  这种方法可以调用不在类中的类方法，但是不能使用self作为对象出现
# super(要从哪一个类的上级类开始查询,self).方法名()  # 类名必须在继承关系内,如果类名是当前所在的类,则可以将括号内内容省略,就是第一中方式
```

## 2、多态

- 在继承链条中，子类重写父类方法，即多个子类和父类中都拥有同名方法，将其对象传入函数或方法内部，执行相同方法后，所展示的效果完全不同，这种现象叫做多态

```Python
class Person(object):

    def driver(self):
        print('开车太好玩了 ,10迈,太快了')


class Father(Person):

    def driver(self):
        print('我要去天安门完,开挖掘机不让我进')


class Mother(Person):
    def driver(self):
        print('我会开小汽车,嘟嘟嘟')


class Son(Father):
    def driver(self):
        print('我会骑自行车,真好玩')


def go_shopping(Driver):
    Driver.driver()
    print('很快就到超市了,真好呀')

class Monkey(object):
    def driver(self):
        print('我在骑自行车')


# 在我调用go_shopping时,可以将什么对象传进来???

p1 = Person()
f1 = Father()
s1 = Son()
m1 = Mother()

# 多态: 在继承链条中,无论是多级继承还是多继承,不同的类同种方法会进行重写,重写后在函数或者方法中传入不同的子类创建的对象,调用相同方法所展示的效果完全不同
go_shopping(p1)
go_shopping(f1)
go_shopping(s1)
go_shopping(m1)

# 如果创建一个Monkey对象,能否传入go_shopping并正确执行???
# 如果一个没有继承关系的类,也存在指定方法,也可以进行对象的传递,并在方法或函数内部使用,但是逻辑会有偏差,这种语法没有问题,但是逻辑上有严重偏差的方式叫做"鸭子类型"(扩展,不要求掌握)
# monkey1 = Monkey()
# go_shopping(monkey1)
```

## 3、类属性

- 类属性，就是所有的对象所共有的属性，在对其修改够，所有对象的类属性放生了改变
- 实例属性，每个对象所独有的，对象被创建后，添加修改实例属性，对其他对象不产生影响

```python
# 类属性 ,有些地方也叫类变量  就是在类中创建的属于所有对象的属性

class Chinese(object):
    # 类属性是所有对象所共有的
    color = 'yellow'
    def __init__(self, name):
        self.name = name


c1 = Chinese('xiaohong')
c2 = Chinese('xiaohuang')
c3 = Chinese('xiaolv')

# 上述三个对象拥有的实例属性是什么???  name
# 他们每个人的实例属性相同么???之间有联系么???  不相同,每个对象间的实例属性互不相关
# 但是三个对象的类属性是完全相同的
print(c1.color)
print(c2.color)
print(c3.color)
# 类属性的获取方式
# 格式1:对象名.类属性名  在实例属性中,不能有与类属性同名的属性,否则类属性不能通过这种方式提取
# 格式2:类名.类属性名  (推荐)

# 修改类属性
# 格式:类名.类属性名 = 值
Chinese.color = 'orange'
# 注意:修改类属性不能使用  对象名.属性名 = 值  这种方式会添加一个实例属性
print(c1.color)
print(c2.color)
print(c3.color)

# 类属性使用场景:
# 可以进行计数
# 可以控制或者包含多个对象
class Apple(object):
    apple_list = []
    def __init__(self):
        Apple.apple_list.append(self)

    count = 10
    def eat(self):
        Apple.count -= 1

a1 = Apple()
a2 = Apple()
a3 = Apple()
a4 = Apple()

a1.eat()
a2.eat()
a3.eat()
a4.eat()
print(Apple.count)
print(Apple.apple_list)
```

## 4、类方法

- 如果在方法内部不需要使用实例属性和实例方法，但是需要使用类属性或者类方法我们就定义类方法
- 定义方式：需要在方法上方写@classmethod
- 在类方法中会自动传入cls，这个参数代表的是当前类本身

```python
class Apple(object):
    num = 10
    def __init__(self):
        self.eat_num = 0

    def eat(self):
        # 每次吃苹果,当前的食用数量加1
        self.eat_num += 1
        # 每次吃苹果,让苹果总数 -1
        Apple.num -= 1
    # 当方法中不适用实例属性和实例方法,只会使用到类属性和类方法的时候我们就选择类方法
    # 因为类方法,不需要创建实例去进行调用,可以直接使用类名调用
    @classmethod
    def eat_apple_num(cls):
        # 在类方法中传入的cls即为当前类的类名
        print(f'一共被吃了{10-cls.num}个,还剩{cls.num}个')

# 类方法的调用
# 格式: 类名.类方法名
Apple.eat_apple_num()

# 创建对象
a1 = Apple()
a2 = Apple()
a3 = Apple()
a4 = Apple()
# 吃苹果
a1.eat()
a2.eat()
a3.eat()
a4.eat()
a4.eat()

# 调用类方法
Apple.eat_apple_num()

# 查看每人吃了几个苹果
print(a1.eat_num)
print(a2.eat_num)
print(a3.eat_num)
print(a4.eat_num)

# 类方法可以使用对象调用么?
# a1.eat_apple_num()  不推荐这样使用
```

## 5、静态方法

- 既不依赖于实例，也不依赖于类，这种方法我们就可以定义为静态方法

```python
class Person(object):
    # 在静态方法中,不会传入self, 也不会传入cls 所以在我们使用静态方法时,最好再静态方法中不要使用类或对象的属性或者方法
    # @classmethod  类方法修饰

    @staticmethod
    def func():
        print('我是一个静态方法')

# def func():
#     print('我是一个静态方法')
# 一般能够定义为函数的内容,都可以改写为静态方法,理论静态方法不依赖与类和对象,但是为了更好的封装,我们会将其写到类中
Person.func()


# 静态方法就是一个普通函数,放到类内部就是为了封装,方便我们去继承和导入模块
```

## 6、面向对象案例

```python
# 需求: 进行游戏
# 1/显示游戏信息
# 2/展示历史最高分
# 3/开始游戏

class Game(object):
    top_score = 100

    def __init__(self, name):
        self.name = name
    # 定义一个静态方法,与类和实例都没有关系
    @staticmethod
    def print_game_info():
        print('游戏信息展示')
    # 定义类方法,内部可以调用类属性和类方法,依赖于类
    @classmethod
    def show_top_score(cls):
        print(f'历史最高分数为{cls.top_score}')
    # 定义了一个实例方法,内部可以调用实例属性和实例方法,依赖于实例
    def start_game(self):
        print(f'{self.name}开始游戏')

Game.print_game_info()
Game.show_top_score()
# 实例方法必须使用实例进行调用
g1 = Game('xiaoming')
g1.start_game()
```

# 异常

## 7、异常捕获

- 使用try和except可以捕获异常，也就是在出现异常后不会将代码终止运行，而是执行except中的代码处理异常

```python
# 异常捕获:通过代码将可能出现异常的文件放入try中,然后如果出现异常就执行except中的命令
'''
格式:
try:
    可能出现异常的代码
except:
    如果出现了异常,就执行其中的代码
'''

# 需求:读取文件,如果文件不存在,则以写入方式打开
# 如果我们try中的代码出现了异常,则执行except中的命令
# 如果我们try中的代码没有出现异常,则不会执行
try:
    file = open('test.py', 'r')
except:
    file = open('test.py', 'w')

# 在正常的Python开发中基本每个函数中都要出现一次异常捕获
# 代码健壮性:代码抵御异常的能力
```

## 8、捕获指定类型的异常

- 在except后边添加异常类型，就可以捕获指定类型的异常
- 如果我们想要捕获多种异常
  - 可以在except后边添加多个异常类型，中间用逗号隔开，但是需要用括号包裹，变成一个元组
  - 可以书写多个except
- 如果所有的异常类型都无法捕获到该异常， 或者我们需要捕获未知类型的异常，可以使用Exception

```python
# try:
#     # NameError: name 'a' is not defined
#     # 如果先出现NameError  我们的后边一句没有办法执行  ZeroDivisionError没有办法捕捉到
#     # print(a)
#     print(1/0)
# # 如果想要捕获指定异常,就在except 后边添加异常的类型
# except ZeroDivisionError: # 这种方式只能捕获指定异常
#     print('出现异常了!!!')

# 在出现异常后, NameError和 ZeroDivisionError  之类的Error就是异常类型
# ZeroDivisionError: division by zero
# print(1/0)
# NameError: name 'a' is not defined
# print(a)


# 能不能同时捕获多种异常呢?  可以
# 方法一:在except后边添加多个异常名称
# try:
#     # NameError: name 'a' is not defined
#     # 如果先出现NameError  我们的后边一句没有办法执行  ZeroDivisionError没有办法捕捉到
#     # print(a)
#     print(1 / 0)
# # 如果想要捕获指定异常,就在except 后边添加异常的类型
# except (ZeroDivisionError, NameError):  # 这种方式只能捕获指定异常
#     print('出现异常了!!!')

# 方法二: 在try后边书写多个except
# try:
#     # NameError: name 'a' is not defined
#     # 如果先出现NameError  我们的后边一句没有办法执行  ZeroDivisionError没有办法捕捉到
#     # 在出现异常之后,后续代码将不会继续执行
#     print(a)
#     print(1 / 0)
# # 如果想要捕获指定异常,就在except 后边添加异常的类型
# except ZeroDivisionError:
#     print('出现ZeroDivisionError异常了!!!')
# except  NameError:
#     print('出现NameError异常!!')

# 如果我们想要展示异常信息怎么办?
# 异常信息就是异常类型冒号之后的注释
# 可以通过获取异常对象,并对异常对象进行打印,得到异常信息
# try:
#     print(a)
#     print(1 / 0)
# # 如果想要捕获指定异常,就在except 后边添加异常的类型
# # 在异常类型之后添加上个as  变量名  这时候 变量就是异常对象,打印该对象就可以出现错误信息
# except ZeroDivisionError as error:
#     print(error)  # division by zero
# except  NameError as error:
#     print('出现NameError异常!!', error)

# 如果我们不知道异常类型是什么怎么办?

# 可以使用Exception进行捕获,Exception是所有异常类的父类,可以捕获所有异常类型

try:
    print('2' + 1)
    print(a)
    print(1 / 0)
except ZeroDivisionError as error:
    print(error)  # division by zero
except NameError as error:
    print('出现NameError异常!!', error)
except Exception:
    print('出现了未知异常')
```

## 9、else 和 finally

- else： try中控制的代码没有出现异常，则执行该结构内的代码

```python
'''
格式:
try:
    可能会出现异常的代码
except:
    在出现异常后执行该命令处理异常
else:
    当没有出现异常时,执行该代码
'''

try:
    a = 1
    print(a)
except:
    print('出现异常了')
else:
    # try中的代码正常执行没有任何异常,则执行else里边的代码
    print('没有异常,虚惊一场')
```

- finally：无论出现什么情况都会执行finally里边的代码，哪怕程序崩溃

```python
'''
try:
    可能出现异常的代码
except:
    代码出现异常后执行该代码处理异常
else:
    如果try中的代码不出现异常,则执行其中的代码
finally:
    无论如何都会执行finally中的代码
'''

# 无论任何情况,finally中的代码都要被执行
try:
    a = 1
    print(a)
    print(1/0)
except NameError:
    print('出现异常了')
else:
    print('没有出现异常')
finally:
    print('出现不出现异常都要执行')
# 代码写到finally中,哪怕程序报错终止,代码依旧需要执行完成,但是写到try结构之外,程序报错终止将不会继续执行外部代码
print('try结构之外书写内容')
```

## 10、自定义异常抛出

- 自定义异常一定要继承自Exception
- 自定义异常可以使用raise抛出，可以进行捕获或者导致程序终止
- raise可以抛出系统异常，也可以抛出自定义异常

```python
# 自定义异常的逻辑
# 在自定义异常时,只要继承自Exception就可以当做异常抛出
# 继承后要重写 Exception方法,添加我们需要的内容

class PassWorldError(Exception):
    error_count = 0

    def __init__(self, str):
        super().__init__(str)
        # 在此处可以添加自定义操作
        PassWorldError.error_count += 1

# raise可以手动抛出异常,抛出异常后,可以直接终止程序,或者使用try except进行捕获
# raise可以抛出自定义异常,也可以抛出系统异常
try:
    password = input('请输入您的密码:')
    if len(password) < 6:
        raise PassWorldError('您的密码不足6位,请重新输入')
        # raise NameError('您的密码错误了')
except PassWorldError as error:
    print(error)

# raise PassWorldError('密码错误')
```

# 模块与包

## 11、模块的导入

```python
import 模块名
调用: 模块名.功能名

from 模块名 import 功能名
调用: 功能名

from 模块名  import  *
import 模块名  as 别名
from 模块名 import 功能名 as 别名
```

```python
# Python中的模块就是可以将别人写好的,或者自己以前写好的功能直接导入新的文件或工程内,导入后可以直接调用  例如 : random  time os

# 我们没有实现模块中的功能,但是我们讲模块导入后就可以使用该功能,类似于继承

# 导入模块的方式
'''
import 模块名
调用: 模块名.功能名

from 模块名 import 功能名
调用: 功能名

from 模块名  import  *
import 模块名  as 别名
from 模块名 import 功能名 as 别名
'''
# # 导入os模块
# import os
#
# # 使用os模块
# print(os.listdir())

# # 导入os模块中部分功能
# from os import listdir, mkdir
# # 使用os模块中的功能
# print(listdir())

# # 导入os模块中的所有功能
# from os import *
# # *就是通配符,表示导入os模块中所有允许导入的模块
#
# # 使用os模块
# print(listdir())

# # 导入os模块,将模块改名为xitong
# import os as xitong
# # 使用os模块
# # NameError: name 'os' is not defined
# # print(os.listdir())
# # 如果给模块起了别名.则原名称不可使用
# print(xitong.listdir())

# from os import listdir as ls
# print(ls())
# NameError: name 'listdir' is not defined
# 给功能名称起别名后,无法使用原名称只能使用新的功能名称
# print(listdir())
```

## 12、自定义模块

- 模块名一定要遵循标识符的命名规则才能被导入

- 模块中书写的全局变量，函数，类可以盗取其他文件

- 导入模块时，会将模块中的所有文件执行一遍

- 为了保证测试代码在导入模块时不被执行，我们的测试代码需要写入

  `if __name__ == '__main__:'`

```python
# 标识符的命名规则
# 1/以字母数字下划线组成
# 2/不能以数字开头
# 3/不能是关键字
# 4/严格区分大小写

age = 18


def func():
    print('我是module中的函数')


class Person(object):
    def eat(self):
        print('西瓜真好吃呀')




# 在书写模块或者工具类的时候,经常需要调试,每次调试完成后还要将代码删除,否则导包结束后测试代码都会被执行一遍

# 所以我们需要想一个办法,将我们写的测试代码在当前模块中执行时,调用,在导入模块时不调用
# __name__就是说明当前文件执行的模块名是什么?
# print(__name__)   # __main__如果在当前文件中执行,模块名就是main
# 如果导入其他模块,则__name__的值就是文件名称module_01
# 所以我们根据__name__的值的判断,就可以断定他是咋当前文件执行,还是导入模块

# 使用该判断,让我们的测试代码只有在当前文件中执行的时候才会被调用
if __name__ == '__main__':
    if age > 10:
        print('今晚不能尿床了')
```

## 13、模块查询顺序

- sys.path可以查询模块调用路径列表，越靠前的路径越优先查询

```python
# 可以使用sys.path查看模块的定位顺序,如果模块名相同,优先从最新的序列查找

import sys
print(sys.path)
# sys.path的返回值是一个路径列表,排名越靠前的路径,在调用模块时优先查找,如果这个路径下没有对应模块才去下一个路径中查找.

# 在开发中可以在列表中你添加路径(了解)
```

- 开发中可以添加调用路径  sys.path.append(路径)

## 14、`__all__`的使用方式

```python
# __all__可以控制模块使用功能from 模块名 import *所导入的功能列表

from module_02 import *

# NameError: name 'age' is not defined
# 如果__all__控制的类表中没有改功能则不能在文件中使用
# print(age)
# 如果写到__all__中则可以使用
func()


import module_02
# __all__不能控制import的导入效果
print(module_02.age)

from module_02 import age
# 如果针对性导入某个功能,不受__all__影响
print(age)
```

## 15、包的的导入

- 导入包
  - import 包名.模块名
  - from 包名 import 模块名
  - 如果想要使用功能from 包名 import *
    - 要在`__init__.py`文件中书写`__all__`添加指定模块名才能导入

```python
# 包:多个有关联的模块在一起,保存在同一个文件夹内,并且文件内有一个__init__.py为文件,这种文件夹就叫做包
# 创建包的方式: mew >>> package   这中创建方式会自动添加一个__init__.py文件

# # 导入包 : import 报名.模块名
# import my_package.module_02
# # 调用 : 包名.模块名.功能名称
# my_package.module_02.func()

# 导入包: from 包名 import 模块名
# from my_package import module_01
# # 调用: 模块名.功能名称
# print(module_01.age)

# 导入包: from 包名 import *
from my_package import *
# 必须在__init__.py文件中的__all__里添加模块列表,才能使用import* 进行导入

print(module_01.age)
module_02.func()
```

## 16、学生管理系统面向对象版

- main.py

```python
# 主程序入口
# 一般开发中 文件夹会使用大驼峰命名法, 包和模块都是下划线分割法
from StudentManagerSystem.student_manager import StudentManager

def main():
    # 需求:循环输入,直到用户选择7 则退出
    s1 = StudentManager()
    s1.load_student_info()
    while True:
        # 提示用户输入信息 调用静态方法
        StudentManager.show_info()
        # 接收用户输入的信息
        num = int(input('请输入您要执行的功能:'))
        # 判断要执行的功能并且执行
        s1.choose_option(num)
        input()


main()
```

- Student.py

```python
# 定义学员类,并且在创建学员对象的时候添加学员信息

class Student(object):
    def __init__(self, student_id, name, age):
        """在创建学员对象时,传入学员信息"""
        self.student_id = student_id
        self.name = name
        self.age = age

    def __str__(self):
        """在打印学员对象时,展示学员信息"""
        return f'学员的名字是{self.name}, 今年{self.age}岁, 学号是{self.student_id}'
```

- Student_manager.py

```python
# 方法:
# 1.判断用户键入的数字,执行不同的命令
# 2.添加学员
# 3.删除学员
# 4.修改学员
# 5.查询学员
# 6.展示所有学员
# 7.退出程序
# 8.展示信息
from StudentManagerSystem.student import Student


class StudentManager(object):

    def __init__(self):
        self.students_list = []

    @staticmethod
    def show_info():
        print('请选择如下功能-----------------')
        print('1:添加学员')
        print('2:删除学员')
        print('3:修改学员信息')
        print('4:查询学员信息')
        print('5:显示所有学员信息')
        print('6:保存学员信息')
        print('7:退出系统')

    def choose_option(self, num):
        if num == 1:
            self.add_student_info()
        elif num == 2:
            self.delete_student_info()
        elif num == 3:
            self.modify_student_info()
        elif num == 4:
            self.search_student_info()
        elif num == 5:
            self.show_all_student_info()
        elif num == 6:
            self.save_student_info()
        elif num == 7:
            self.exit_program()
        else:
            print('数据有误')

    def add_student_info(self):
        """添加学员信息"""
        # 获取要添加的学员id
        student_id = input('请输入您要添加的学员id:')
        # 判断学员id是否存在
        for student_info in self.students_list:
            if student_info.student_id == student_id:
                print('该id已经存在,无法添加')
                return
        else:
            name = input('请输入您要添加的学员姓名:')
            age = input('请输入您要添加的学员年龄:')
            s1 = Student(student_id, name, age)
            self.students_list.append(s1)
            print('学员添加成功')

    def delete_student_info(self):
        """删除学员信息"""
        # 获取要删除的学员id
        student_id = input('请输入您要删除的学员id:')
        for student_info in self.students_list:
            if student_info.student_id == student_id:
                self.students_list.remove(student_info)
                print('学员删除成功')
                return
        else:
            print('此学员不存在')

    def modify_student_info(self):
        """修改学员信息"""
        # 获取要修改的学员的id
        student_id = input('请输入您要修改的学员id')
        for student_info in self.students_list:
            if student_info.student_id == student_id:
                name = input('请输入您要修改为的姓名')
                age = input('请输入您要修改为的年龄')
                student_info.name = name
                student_info.age = age
                print('学员信息修改完成')
                return
        else:
            print('查无此学员')

    def search_student_info(self):
        """查询学员信息"""
        # 获取要查询学员的id
        student_id = input('请输入要查询学员的id')
        for student_info in self.students_list:
            if student_info.student_id == student_id:
                # 由于已经重写对了__str__方法,所以打印对象就可以输出信息
                print(student_info)
                return
        else:
            print('要查询的学员不存在')

    def show_all_student_info(self):
        for student_info in self.students_list:
            print(student_info)

    def save_student_info(self):
        """保存学员信息"""
        # 打开文件  如果要依次写入,我们使用a模式
        file = open('student_info.txt', 'a')
        # 遍历学员列表依次将学员信息写入, 学员对象.__dict__
        for student_info in self.students_list:
            file.write(str(student_info.__dict__) + '\n')
        # 关闭文件
        file.close()

    def load_student_info(self):
        """加载学员信息"""
        # 打开文件
        file = open('student_info.txt', 'r')
        # 将学员信息读取出来
        while True:
            content = file.readline()
            # 将字典类型的字符串转换为字典
            if content == '':
                break
            dict1 = eval(content)
            # 创建一个student对象
            # 字典前面+ ** 可以转换为  key = 值的 这种关键字参数赋值形式
            # 将学员信息赋值给对象
            s1 = Student(**dict1)
            self.students_list.append(s1)

        # 关闭文件
        file.close()

    def exit_program(self):
        """退出程序"""
        self.save_student_info()
        exit()
```

# 并发编程

# 网络编程