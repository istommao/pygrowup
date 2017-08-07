# 集合

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
