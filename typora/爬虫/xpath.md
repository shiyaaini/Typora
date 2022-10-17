

# xpath

# 1



```python
import requests
from lxml import etree
xml="""
<body>
    <id>1</id>
    <name>野花遍地香</name>
    <price>1.23</price>
    <nick>臭豆腐</nick>
    <author>
        <nick id="10086">周大强</nick>
        <nick id="10010">周芷若</nick>
        <nick class="joy">周杰伦</nick>
        <nick class="jolin">蔡依林</nick>
        <div>
            <nick>爱你爱你1</nick>
            <div>
                <nick>我不爱你</nick>
            </div>
        </div>
        <span>
            <nick>爱你爱你2</nick>
        </span>
    </author>
    <parter>
        <nick id="ppc">胖子</nick>
        <nick id="ppbc">胖子2</nick>
    </parter>

</body>
"""
resp=etree.XML(xml)
bm1=resp.xpath("/body/name/text()")#拿文本
bm=resp.xpath("/body/text()")#后代
bm2=resp.xpath("/body/*/nick/text()")#检索body下的父子节点
bm3=resp.xpath("/body/author//nick/text()")#检索author下的所有节点+
bm4=resp.xpath("/body//nick//text()")#检索body下的所有节点
print(bm4)
```

## 2.可查找href,id,class也可以找到所属得组的内容

```python
import requests
import re
from lxml import etree
resp=etree.parse("b.html")
bm=resp.xpath("/html/body/ul/li/text()")
bm1=resp.xpath("/html//a/text()")
bm2=resp.xpath("/html/body/ul/li/a[@href='bnm']/text()")#@class="..."或者@id=""
bm3=resp.xpath("/html/body/ol/li[1]/text()")#打印第一个li内容
bm4=resp.xpath("/html/body/ol/li")#生成迭代器
# print(bm3)
for i in bm4:
    d=i.xpath("./a/text()")#从li目录中继续找
    print(d)
    z=i.xpath("./a/@href")#输出href
    print(z)
```