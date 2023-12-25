# python-to-C
This will help you to convert your python3 code int to C/C++ code. The tested compile is obvious but not limited to MigwGCC Windows. 

So the first step is the .PYX file is edited as:

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
