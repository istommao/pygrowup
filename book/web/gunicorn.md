# gunicorn

> Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.
> It's a pre-fork worker model. The Gunicorn server is broadly compatible with various web frameworks,
> simply implemented, light on server resources, and fairly speedy.

## 简单的Hello world 示例

```shell
pip install gunicorn
```

```python
# wsgi.py
def app(environ, start_response):
    data = b'Hello world!\n'
    start_response('200 OK', [
        ('Content-Type', 'text/plain'),
        ('Content-Length', str(len(data)))
    ])
    return iter([data])
```

```shell
gunicorn -w 2 wsgi:app
```
