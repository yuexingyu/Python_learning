# Python字符串
在```Python数据类型```中我们简单的介绍过字符串。字符串是 Python 中最常用的数据类型。我们可以使用引号('或")来创建字符串。
## Python字符串运算符

| 操作符 | 描述 |
| :--| :-- |
| +    | 字符串连接                |
| *    | 重复输出字符串             |
| []   | 通过索引获取字符串中的字符  |
| [ : ]  | 截取字符串中的一部分     |
| in   | 成员运算符，如果字符串中包含给定的字符，返回True
| not in | 成员运算符，如果字符串中不包含给定的字符，返回True

代码示例：
```python
>>> a = "hello"
>>> b = "Python"
>>> a+b
'helloPython'
>>> a *3
'hellohellohello'
>>> a[1],b[2]
('e', 't')
>>> a[0:3]
'hel'
>>> print("h" in a)
True
>>> print("h" not in a)
False
```
## Python字符串格式化
之前特意整理了Python字符串格式化的笔记。<a href="https://blog.csdn.net/kouyi5627/article/details/83246716"><u><b>传送门</a>
## Python字符串内置函数
同样单独整理了Python字符串内置函数的笔记。<a href="https://blog.csdn.net/kouyi5627/article/details/80552798"><u><b>传送门</a>
