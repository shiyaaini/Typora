# bs4（获取href值）

```python
import requests
import re
from bs4 import BeautifulSoup
def bmg1():
    url="https://www.runoob.com/html/html5-intro.html"
    resp=requests.get(url)
    bresp=BeautifulSoup(resp.text,"html.parser")
    tresp=bresp.find("table",class_="reference")
    trresp=tresp.find_all("tr")[1:]
    for i in trresp:
        bnm=i.find_all("td")   #".text"拿到标记的内容
        vmb=bnm[0].text
        vm=bnm[1].text
        print(vmb,vm)

bmg1()
```

### 批量下载图片

```python
import requests
import re
from bs4 import BeautifulSoup
import urllib
def youmei():

    url="https://www.umei.cc/meinvtupian/meinvzipai/"
    resp=requests.get(url)
    resp.encoding="utf-8"
    bresp=BeautifulSoup(resp.text,"html.parser")
    divresp=bresp.find_all("a",class_="img_album_btn")  #获取页面的图片链接a
    # print(divresp)
    x=1
    for i in divresp:
        rdresp=i.get("href")#获取链接
        jhtml="https://www.umei.cc"+rdresp#拼接链接
        nimgshtml=requests.get(jhtml)
        nimgshtml.encoding="utf-8"
        imgd=BeautifulSoup(nimgshtml.text,"html.parser")
        mmm=imgd.find("div",class_="big-pic").find("img")#获取img内容
        imgget=mmm.get("src")#获取图片链接
        with open(f'{x}' + ".jpg", 'wb') as f:
            pic = requests.get(imgget).content
            f.write(pic)
            print(f'拿到第{x}张图片')
            x = x + 1

youmei()
```



