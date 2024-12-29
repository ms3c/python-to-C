# python-to-C
This example will assist you in converting your Python 3 code into C/C++ code. While the tested compiler is MinGW GCC for Windows, it is not limited to this option.

First step the .PYX file is edited as:

```python
from tkinter import Tk

cdef public void function():
    root = Tk()
    root.mainloop()

if __name__ == "__main__":
    function()
```
    
Then run ```python -m cython test.pyx --embed```
Lastly ```gcc -mconsole -DSIZEOF_VOID_P=8 -DMS_WIN64 C:\Users\admin\main.c -IC:\Users\admin\AppData\Local\Programs\Python\Python38\include -LC:\Users\admin\AppData\Local\Programs\Python\Python38\libs -lpython38 -o C:\Users\admin\Desktop\main.exe```
