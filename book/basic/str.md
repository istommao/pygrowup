# 字符串

- 字符串基本操作

```python
s = 'Hello world'

# 格式化
s = 'Hello %s' % 'world'
print(s)

s = 'Hello {}'.format('world')
print(s)
```

## 字符串的一些常用方法

```python
# 分片操作
s = 'Hello world'
# s[start:end:step]
print(s[:5])
print(s[:-1])
print(s[::2])

# 所有英文字母变大写
s = 'hello world'
s = s.upper()
print(s)

# 所有英文字母变小写
s = 'HELLO WORLD'
s = s.lower()
print(s)

# 单词首字母大写
s = 'hello world'
s = s.title()
print(s)

# split 操作
s = 'Hello,world,你好世界'
lst = s.split(',')
print(lst)

# join 操作
s = 'Hello,world,你好世界'
lst = s.split(',')
print(' '.join(lst))

# replace 操作
s = 'Hello,world,你好世界'
newstr = s.replace(',', ' ')
print(newstr)
```
