# python-to-C
This will help to convert your python code to C the compile with MigwGCC or other compiler which i did not test

So the first step is the .PYX is edited as:

from tkinter import Tk

cdef public void function():
    root = Tk()
    root.mainloop()

if __name__ == "__main__":
    function()
    
    
then python -m cython test.pyx --embed
lastly gcc -mconsole -DSIZEOF_VOID_P=8 -DMS_WIN64 C:\Users\Mohamed\Desktop\hope\your_app.c -IC:\Users\Mohamed\AppData\Local\Programs\Python\Python38\include -LC:\Users\Mohamed\AppData\Local\Programs\Python\Python38\libs -lpython38 -o C:\Users\Mohamed\Desktop\hope\out.exe
