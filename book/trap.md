# Python 陷阱

## 参数默认值问题

```python
def func(lst=[]):
    lst.append(1)
    print(lst)

func()
func()
```

