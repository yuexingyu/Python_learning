# Python字典
字典是另一种可变容器类型，且可以存储任意类型对象。我们前面学到的字符串、元组和列表也可理解为容器。
<br />字典的每个键值对使用```:```分割，键值对之间使用```,```分割，整个字典包括在```{}```中。
<br>代码示例：
```python
>>> dict = {"name" : "Tom","age":23,"sex":"man"}
>>> dict
{'name': 'Tom', 'age': 23, 'sex': 'man'}
```
字典的值可以取任何数据类型，但键必须是不可变的，如字符串，数字或元组。代码示例：
```python
>>> dict = {"name":"Tom",23:"age",(1995,12,12):"birthday"}
>>> dict
{'name': 'Tom', 23: 'age', (1995, 12, 12): 'birthday'}
```
## 访问字典中的值
使用```[key]```可以获得对应key的值，代码示例：
```python
>>> dict["name"]
'Tom'
```
如果使用字典中不存在的key进行访问，程序就会出现错误。因为字典是无序的，所以不能对字典使用切片。
## 修改字典
可以向字典中添加新的键值对，修改或删除已有的键值对。
<p>代码示例：
```python
>>> dict = {"name":"Tom",23:"age",(1995,12,12):"birthday"}
>>> dict
{'name': 'Tom', 23: 'age', (1995, 12, 12): 'birthday'}
>>> dict["sex"] = "man" # 插入新的键值对
>>> dict
{'name': 'Tom', 23: 'age', (1995, 12, 12): 'birthday', 'sex': 'man'}
>>> dict["name"] = "Jonh"   # 修改已有的键值对
>>> del dict[23]    # 删除键值对
>>> dict
{'name': 'Jonh', (1995, 12, 12): 'birthday', 'sex': 'man'}
>>> del dict    # 删除整个字典
```
## 字典键的特性
字典值可以没有限制地取任何python对象，既可以是标准的对象，也可以是用户定义的，但键不行。两个重要的点需要记住：
- 字典键是不可重复的，如果同一个键被赋值两次，后一次操作会覆盖前一次
- 键必须不可变，所以可以使用数字、字符串或元组充当，但是列表就不行。

代码示例：
```python
>>> dict = {"name":"Tom","name":"Jonh"}
>>> dict
{'name': 'Jonh'}
>>> dict = {[1]:"Tom"}
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'list'
```
## 字典内置函数&方法
Python字典包含的内置函数：

|函数|描述|
|:--|:--|
| len(dict) | 计算字典元素个数，即键的总数 |
| str(dict) | 输出字典可打印的字符串表示
| type(var) | 返回输入的变量类型，如果变量是字典就返回字典类型。
Python字典内置方法：

| 函数| 描述|
|:--|:--|
|dict.clear()|删除字典内所有元素
|dict.copy()|返回一个字典的浅复制
|dict.fromkeys(seq[, val])|创建一个新字典，以序列 seq 中元素做字典的键，val 为字典所有键对应的初始值
|dict.get(key, default=None)|返回指定键的值，如果值不在字典中返回default值
|dict.has_key(key)|如果键在字典dict里返回true，否则返回false
|dict.items()|以列表返回可遍历的(键, 值) 元组数组
|dict.keys()|以列表返回一个字典所有的键
|dict.setdefault(key, default=None)|和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default
|dict.update(dict2)|把字典dict2的键/值对更新到dict里
|dict.values()|以列表返回字典中的所有值
|pop(key[,default])|删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。
|popitem()|随机返回并删除字典中的一对键和值。
