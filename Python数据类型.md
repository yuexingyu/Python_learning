# Python数据类型

- 布尔类型
- 数字
- 字符串
- 列表、元组、字典
- 日期

## 布尔类型
Python使用 ```True```和```False```来表示布尔值。
## 数字
Python3支持三种不同的数字类型：```int```、```float```和```complex```。
## 字符串
可以使用单引号```''```或者双引号```""```进行定义字符串，例如：```str='hello world'```和```str="hello world"```是一样的。我们还可以使用```''' '''```表示多行字符串，可以在三引号中自由的使用单引号和双引号，例如：
```python
>>> str = '''python string
... 'my name is python'
... "i'm fine" '''
>>> print(str)
python string
'my name is python'
"i'm fine"
```
Python字符串有两种取值顺序：
- 从左到右索引默认0开始，最大索引是字符串长度-1
- 从右到左索引默认-1开始，最大索引是-字符串长度

如果你要实现从字符串中获取一段子字符串的话，可以使用 ```[头下标:尾下标]``` 来截取相应的字符串，其中下标是从 0 开始算起，可以是正数或负数，下标可以为空表示取到头或尾。 ``` [头下标:尾下标] ``` 获取的子字符串包含头下标的字符，但不包含尾下标的字符。例如：
```python
>>> str = 'python'
>>> str[0:3]
'pyt'
```

``` + ```是字符串连接运算符，``` * ``` 是重复操作。例如：
```python
>>> str1 = "hello"
>>> str2 = "world"
>>> print(str1 + str2)
helloworld
>>> print(str1 * 3 + str2)
hellohellohelloworld
```
## 列表
- List（列表） 是 Python 中使用最频繁的数据类型。
- 列表可以完成大多数集合类的数据结构实现。它支持字符，数字，字符串甚至可以包含列表（即嵌套）。
- 列表用 ```[ ]``` 标识，是 python 最通用的复合数据类型。
- 列表中值的切割也可以用到变量 ```[头下标:尾下标]``` ，就可以截取相应的列表，从左到右索引默认 ```0``` 开始，从右到左索引默认 ```-1``` 开始，下标可以为空表示取到头或尾。

列表也可以使用```+```进行连接，使用```*```重复。代码示例：

```python
>>> list1 = ["I","love","python",3,"years"]
>>> list2 = ["I", "also","like", "java"]
>>> print(list1[2])     # 打印列表第3个元素
python
>>> print(list1[0:3])   # 获取list1里第1个到第三个元素
['I', 'love', 'python']
>>> print(list1 + list2)    # 连接list1和list2
['I', 'love', 'python', 3, 'years', 'I', 'also', 'like', 'java']
>>> print(list1 * 2)    # 将list1重复两次
['I', 'love', 'python', 3, 'years', 'I', 'love', 'python', 3, 'years']
```
## 元组
- 元组和列表很相似，不过元组是不可变的，相当于只读列表
- 元组使用 ```()``` 定义，元素之间使用 ```,``` 隔开
- 元组取值的方式和列表一样，都是采用```[]```加上```索引```的方式

## 字典
- 字典(dictionary)是除列表以外python之中最灵活的内置数据结构类型。
- 列表是有序的对象集合，字典是无序的对象集合。
- 两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。
- 字典用```{}```标识。字典由```索引key```和它对应的```值value```组成。

代码示例：
```python
>>> dict1 = {}
>>> dict2 = {"one":1,"two":2}
>>> print(dict2)    # 输出整个字典
{'one': 1, 'two': 2}
>>> dict1["name"] = "Tom"   # 给dict1添加键"name"，值为"Tom"
>>> dict1["age"] = 23
>>> dict1["sex"] = "boy"
>>> print(dict1)
>>> print(dict1["name"])    # 打印dict1键为"name"的值
Tom
>>> print(dict1.keys())     # 输出所有的键
dict_keys(['name', 'age', 'sex'])
>>> print(dict1.values())   # 输出所有的值
dict_values(['Tom', 23, 'boy'])
```

## 数据类型转换
有时候，我们需要对数据类型进行转换，数据类型的转换，只需要将数据类型作为函数名即可。

| 函数        |  描述 |
| :--       | :--  |
| int(x [,base]) | 将x转换为一个整数|
| float(x)  | 将x转换为一个浮点数 |
| complex(real [,imag])|创建一个复数|
| str(x)    | 将对象x转换为字符串|
| repr(x)   | 将对象x转换为字符串显示出来|
| eval(str) | 将一串基本数据类型的字符串，转换成基本数据类型|
| tuple(s)  | 将序列s转换为一个元组   |
| list(s)   | 将序列s转换为一个列表   |
| set(s)    | 转换为可变集合         |
| dict(d)   | 创建一个字典。d必须是一个序列(key,value)元组|
| frozenset(s)| 转换为不可变集合    |
| chr(x)    | 将一个整数转换为一个字符  |
| unichr(x) | 将一个整数转换为Unicode字符 |
| ord(x)    | 将一个字符转换为它的整数值|
| hex(x)    | 将一个整数转换为一个十六进制字符串 |
| oct(x)    | 将一个整数转换为一个八进制字符串  |

代码示例：
```python
>>> str = "[1,2,3,4]"
>>> print(eval(str))
[1, 2, 3, 4]
>>> print(type(eval(str)))
<class 'list'>

# repr()和str()的区别：
>>> s = 'hello world'
>>> str(s)
'hello world'
>>> repr(s)
"'hello world'"
```
