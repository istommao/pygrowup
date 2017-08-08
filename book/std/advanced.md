# 高级数据结构

## namedtuple

> 命名元组

```python
from collections import namedtuple

Point = namedtuple('Point', ['x', 'y'])
p = Point(11, y=22)
```

## deque

> 双端队列

```python
from collections import deque

d = deque(['Hello', 'world'])
d.append('你好')
d.appendleft('世界')
d.pop()
d.popleft()
```

## Counter

> 统计方法

```python
from collections import Counter

s = 'Hello world你好 Hello old'
c = Counter(s)

print(c.most_common(3))
```

## defaultdict

> 给字典不存在的key设置默认值

```python
from collections import defaultdict

dataset = [
    ('fruit', '苹果'),
    ('drink', '可乐'),
    ('fruit', 'orange'),
    ('drink', '雪碧'),
    ('fruit', 'banana'),
    ('vegetables', '花菜')
]

dst = defaultdict(list)
for key, value in dataset:
    dst[key].append(value)
```

## OrderedDict

> 有序字典，在Python3中默认是有序字典

```python
from collections import OrderedDict

dataset = (
    ('fruit', '苹果'),
    ('drink', '可乐'),
    ('vegetables', '花菜')
)

dst = OrderedDict(dataset)
print(dst)
```
