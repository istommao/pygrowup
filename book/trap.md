# Python 陷阱

`相关文章`

- http://pythonguidecn.readthedocs.io/zh/latest/writing/gotchas.html
- http://cenalulu.github.io/python/default-mutable-arguments/

## 参数默认值问题

`可变参数问题`

```python
def func(val, lst=[]):
    lst.append(val)
    return lst

func(1)
>>> [1]

func(2)
>>> [1, 2]
```

并不是预期的[2]

`解决方法`

```python
def func(val, lst=None):
    if lst is None:
        lst = []
    lst.append(val)
    return lst

func(1)
>>> [1]

func(2)
>>> [2]
```

**原因**

> 按理说这个在其他语言中就是个大bug了，但在python中为什么会出现这样的情况呢？

`因为在Python中函数也是对象`

> 函数的默认参数是以对象的属性来保存的，但你再次调用时，默认值已保存，不会再重现生成

