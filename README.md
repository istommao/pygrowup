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

**namedtuple **

> namedtuple是继承自tuple的子类, namedtuple创建一个和tuple类似的对象，
> 而且对象拥有可以访问的属性。这对象更像带有数据属性的类，不过数据属性是只读的。

```python
from collections import namedtuple

PointClass = namedtuple('Point', ['x', 'y'])
Point = PointClass(x=10, y=10)
print(Point.x, Point.y)
```

**deque 双向列表**

```python
from collections import deque

q = deque(['hello', 'world', 'python'])
q.append('age')
q.appendleft('25')
```

**Counter**

> Counter是一个简单的计数器

```python
from collections import Counter

s = 'Beautiful is better than ugly'

c = Counter(s)
print(c.most_common(3))    # 出现频率最高的3个字符
```

**defaultdict**

> 当字典的key不存在时会抛出KeyError, 使用defaultdict在key不存在时则会返回设置的默认值

```python
from collections import defaultdict

dst = defaultdict(lambda: '')
print(dst['key'])
```

**OrderedDict 有序字典**

> 有序字典，Python3中的dict就是OrderedDict

```python
from collections import OrderedDict

dst = OrderedDict([('hello', 'world'), ('age', 25), ('gender', 'male')])
```

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

**os 模块**

```python
import os

os.name    # 字符串指示你正在使用的平台。比如对于Windows，它是'nt'，而对于Linux/Unix用户，它是'posix'
os.getcwd()     # 获得当前工作目录
os.listdir()    # 返回指定目录下的所有文件和目录名。

os.cpu_count()    # 获得CPUs数量
```

**sys 模块**

```python
import sys

sys.argv    # 命令行参数列表
```

### 函数式

- itertools
- functools

### 扩展

- https://docs.python.org/3/library/
- https://docs.python.org/3.5/howto/index.html
- https://pymotw.com/3/index.html
