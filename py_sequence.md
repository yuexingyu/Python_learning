# Python 序列

Python的变量可分为数字型和非数字型。<b>非数字型变量包括</b>：元组、列表、字典、字符串。首先看一下它们的公共方法：
- 都是一个序列 sequence ，也可以理解为容器
- 都使用 "[]" 进行取值
- 都可以使用 for...in... 进行遍历
- 可以计算长度、最大/最小值、比较、删除
- 可以使用 "+" 进行连接，使用 "\*" 进行重复
- 都可以使用切片

## 列表
- Python 中使用最频繁的数据类型，其他语言中通常叫数组
- 专门用于存储一串信息
- 列表使用 "[]" 定义，元素之间使用 "," 隔开
- 列表的索引从 0 开始。在Python中，还可以使用负数索引

## 元组
- 元组和列表很相似，不过元组一旦定义，大小是不可变的
- 元组使用 "()" 定义，元素之间使用 "," 隔开

## 字典

## 字符串

## 解压序列赋值给多个变量
```python
p = ["python", "version", 3.6]
a, b, c = p
print(F"a={a},b={b},c={c}")
```
运行结果：
```
a=python,b=version,c=3.6
```

当变量个数和序列元素的个数不匹配时，就会出现ValueError错误。代码示例：
```python
x, y = p
print(x, y)

ValueError                                Traceback (most recent call last)
<ipython-input-2-1af30f55605e> in <module>()
----> 1 x, y = p
      2 print(x, y)

ValueError: too many values to unpack (expected 2)
```
这种解压序列的方式可以用在任何可迭代对象上面，而不仅仅是列表或者元组。 包括字符串，文件对象，迭代器和生成器。
<p>代码示例：</p>
```python
>>> s = "Hello"
>>> a,b,c,d,e=s
>>> a
'H'
>>> b
'e'
>>> c
'l'
>>>
>>> d
'l'
>>> e
'o'
```

## 解压可迭代对象赋值给多个变量
### 问题
如果一个可迭代对象的元素个数超过变量个数时，会抛出一个 ValueError 。 那么怎样才能从这个可迭代对象中解压出 N 个元素出来？
### 解决方案
Python 的星号表达式可以用来解决这个问题。比如，你在学习一门课程，在学期末的时候， 你想统计下家庭作业的平均成绩，但是排除掉第一个和最后一个分数。如果只有四个分数，你可能就直接去简单的手动赋值， 但如果有 24 个呢？这时候星号表达式就派上用场了：
```python
grades = range(20,100,5)
def drop_first_last(grades):
    first, *middle, last = grades
    return avg(middle)
```
另外一种情况，假设你现在有一些用户的记录列表，每条记录包含一个名字、邮件，接着就是不确定数量的电话号码。 你可以像下面这样分解这些记录：
```python
>>> record = ('Dave', 'dave@example.com', '773-555-1212', '847-555-1212')
>>> name, email, *phonenumbers = record
>>> name
'Dave'
>>> email
'dave@example.com'
>>> phonenumbers
['773-555-1212', '847-555-1212']
```
值得注意的是上面解压出的 phonenumbers 变量永远都是列表类型，不管解压的电话号码数量是多少（包括 0 个）。 所以，任何使用到 phonenumbers 变量的代码就不需要做多余的类型检查去确认它是否是列表类型了。
## 保留最后N个元素
