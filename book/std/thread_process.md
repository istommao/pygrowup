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

```python
import os
import multiprocessing

def worker():
    print('pid', os.getppid())
    print('id', os.getpid())

p = multiprocessing.Process(target=worker)
p.start()
p.join()
```

## concurrent

```python
from concurrent import futures

def func(num):
    import time
    time.sleep(0.5)
    return time.ctime(), num

with futures.ThreadPoolExecutor(max_workers=1) as executor:
    future = executor.submit(func, 1)
    print(future.result())
```

## queue

```python
import queue

que = queue.Queue()

for i in range(5):
    que.put(i)

while not que.empty():
    print(que.get())
```
