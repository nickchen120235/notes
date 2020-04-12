# Python Notes

#### String Reverse
```python
txt = "Hello World"[::-1]
print(txt) # dlroW olleH
```
#### Function parameter with type
Suppose: <code>a->int, b->list, c->string, return->tuple</code>
```python
def f(a: int, b: list, c: str) -> tuple:
    # ...
```