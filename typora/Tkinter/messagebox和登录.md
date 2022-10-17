# messagebox和登录

```python
import tkinter as tk
from tkinter import *
from tkinter import messagebox
mk=tk.Tk()
mk.geometry("500x300+600+300")
mk.title("诗雅官网")
def check():
    if entyr1.get()=="shiya":
        messagebox.showinfo(title="判断用户是否存在",message="账户存在")
    else:
        messagebox.showinfo(title="判断用户是否存在",message="账户不存在")
ct=StringVar()
bn1=Label(mk,text="账号:")
bn2=Label(mk,text="密码:")
bn1.grid(row=1)
bn2.grid(row=2)
entyr1=Entry(mk,textvariable=ct,validate="focusout",validatecommand=check)
entyr2=Entry(mk)
entyr1.grid(row=1,column=1)
entyr2.grid(row=2,column=1)
mk.mainloop()
```

