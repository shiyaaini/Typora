# re

### 正则表达式

| .    | 匹配所有字符串                           |
| ---- | ---------------------------------------- |
| \w   | 匹配数字，字母，下划线（大写字母则相反） |
| \d   | 匹配数字（大写字母则相反）               |
|      |                                          |
|      |                                          |



| match    | match是从头开始匹配                      |
| -------- | ---------------------------------------- |
| search   | 检索到第一个内容就返回值，只返回第一个值 |
| findall  | 匹配字符串中所有的符合正则的内容         |
| finditer | 匹配字符串中所有内容【返回的是迭代器】   |

```python
import re
# hello=re.findall(r"\d+","我的电话号码是：10086,我女朋友的电话号码是：10010")
# print(hello)
#
#
# #迭代器
# love=re.finditer(r"\d+","我的电话号码是：10086,我女朋友的电话号码是：10010")
# print(love)
# for i in love:
#     print(i)

app=re.search(r"\d+","我的电话号码是：10086,我女朋友的电话号码是：10010")
print(app.group())
```

### re.S

```
api=re.compile(r"<div class='.*?'><span id='\d+'>.*?</span></div>",re.S)
re.S支持换行搜索
```

## strip（取消空格）

print(i.group("dianfei").strip())
