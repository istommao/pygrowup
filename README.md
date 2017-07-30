# pygrowup
我的python成长之路

## python 标准库

### 基础数据结构

- str
- list
- tuple
- set
- dict

**str 字符串**

```python
word = 'Hello world!'
word2 = "Hello world"    # 双引号也是可以的
word3 = """
Hello
world
"""           # 三引符号

```

**list 列表**

在Python中列表和元组的主要区别是列表可以修改，而元组则不能(这里有一个重要点会在元组章节说明)

```python
lst = ['Hello', 'world', 1, 2.5]
lst[3] = 'list'
```

**tuple 元组**

元组: 不可变序列

dataset = ('hello', 'world')

**dict 字典**

```python
dataset = {'hello': 'world', 'age': 25}
```

**set 集合**

```python
dataset = {'hello', 'world'}
dataset = set(['hello', 'world'])
```

### 高级数据结构

- namedtuple
- deque
- Counter
- defaultdict
- OrderedDict

### 时间日期

- time
- datetime
- date
- timedelta
- calendar

### 其他

- re
- json
- math
- hashlib
- random
- logging
- unittest

### 线程、进程

- threading
- multiproccessing
- concurrent
- queue

### 网络

- urllib
- socket
- http
- asyncio

### 文件、系统

- os
- sys
- io

### 函数式

- itertools
- functools

### 扩展

- https://docs.python.org/3/library/
- https://docs.python.org/3.5/howto/index.html
- https://pymotw.com/3/index.html
