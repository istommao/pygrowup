# 线程、进程

## threading

```python
import threading

def worker(num):
    print('Worker {}'.format(num))

threads = []
for i in range(5):
    t = threading.Thread(target=worker, args=(i,))
    threads.append(t)
    t.start()
```

## multiproccessing

## concurrent

## queue
