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
#### Plot bar graph
```python
import matplotlib.pyplot as plt
import numpy as np
x = np.array([1, 2, 3]) #np.arange(start=1, stop=4)
y = np.array([1, 2, 3]) #must be an numpy array
plt.bar(x, y, align='center')
plt.show()
```