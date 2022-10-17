# Tkinter

```python
from tkinter import *
import messagebox
root=Tk()
resp=Button(root)#设置按钮
resp["text"]="点我送花"#设置按钮文本
resp.pack()
def songhua(e):
    messagebox.showinfo("Message","送你一朵玫瑰花，亲亲我吧")
    print("送你九九朵玫瑰花")
resp.bind("<Button-1>",songhua)#设置左击
root.mainloop()
```

