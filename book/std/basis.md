# 基础数据结构

Python文档地址: https://docs.python.org/3/tutorial/datastructures.html

**在python中 str list tuple 同属于序列**

`序列共有的一些操作`

- len
- index
- 切片


## str

> 字符串, 不可变类型

```python
data = 'Hello world!'
```

## list

> 列表 可变类型

**基本操作**

- append
- extend
- insert
- remove
- pop
- index
- count
- sort
- reverse


```python
lst = ['Hello']
lst.append('world')
lst.extend(['你好', '世界'])
lst.insert(3, 'Hi')
lst.remove('Hi')
lst.pop()
lst.index('world')
lst.count('world')
lst.sort()
lst.reverse()
```

**使用list实现stack**

```python
stack = ['Hello', 'world']
stack.append('你好')
stack.append('世界')

stack.pop()
```

**列表解析**

```python
# Common
lst = []
for i in range(10):
    lst.append(i**2)

# List Comprehensions
lst = [i**2 for i in range(10)]
```

## tuple

> 元组 不可变类型

```python
tuples = 'Hello', 'world'
# 等价的写法
tuples = ('Hello', 'world')

# 当只有一个元素时需要加上逗号，否则会变成其他的类型
tuples = ('Hello',)

# 元组不可变
tuples[0] = '你好'     # 会抛出异常

# pythonic 的 变量交换

hello = 'Hello'
world = 'World'

hello, world = world, hello

```

## dict

> 字典, hashtable(稀疏数组) 开放寻址解决冲突

```python
data = {'hello': 'world', 'age': 26}
data['height'] = 175
data['age'] = 25

# 判断key是否在dict中
'age' in data
```

**字典解析**

```python
data = {i: i**2 for i in range(10)}
```

## set

> 集合，内部实现和dict类似，可以看作只有key的dict

```python
fruits = {'orange', 'apple', 'banana'}
data = {'你好', 'orange', '世界'}

# 在 fruits集合中但不在data集合中
print(fruits - data)

# fruits 与 data 并集
print(fruits | data)

# fruits 与 data 交集
print(fruits & data)

# fruits 与 data 异惑
print(fruits ^ data)
```

**集合解析**

```python
data = {i**2 for i in range(10)}
```
