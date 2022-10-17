1、首先如图所示的web结构即一个html和css即可实现。

[![img](https://iknow-pic.cdn.bcebos.com/32fa828ba61ea8d3c4412ad5990a304e241f58fb?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_600%2Ch_800%2Climit_1%2Fquality%2Cq_85%2Fformat%2Cf_auto)](https://iknow-pic.cdn.bcebos.com/32fa828ba61ea8d3c4412ad5990a304e241f58fb)

2、打开html页面 定义一个大的div和两个小div 如图所示。

[![img](https://iknow-pic.cdn.bcebos.com/adaf2edda3cc7cd98d4f6a083701213fb90e9184?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_600%2Ch_800%2Climit_1%2Fquality%2Cq_85%2Fformat%2Cf_auto)](https://iknow-pic.cdn.bcebos.com/adaf2edda3cc7cd98d4f6a083701213fb90e9184)

3、最常用的float浮动，只要两个小div的宽度小于等于大div的宽度，即可实现并排了。

[![img](https://iknow-pic.cdn.bcebos.com/bf096b63f6246b60c36ceca5e5f81a4c500fa285?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_600%2Ch_800%2Climit_1%2Fquality%2Cq_85%2Fformat%2Cf_auto)](https://iknow-pic.cdn.bcebos.com/bf096b63f6246b60c36ceca5e5f81a4c500fa285)

4、使用position进行绝对定位，然后使用margin-left除去第一个小div的宽度即可。

[![img](https://iknow-pic.cdn.bcebos.com/d31b0ef41bd5ad6e80da3a3b8fcb39dbb6fd3c3b?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_600%2Ch_800%2Climit_1%2Fquality%2Cq_85%2Fformat%2Cf_auto)](https://iknow-pic.cdn.bcebos.com/d31b0ef41bd5ad6e80da3a3b8fcb39dbb6fd3c3b)

5、使用table盒子实现div并排，这个是等宽的。

[![img](https://iknow-pic.cdn.bcebos.com/b3119313b07eca808b5967369f2397dda0448387?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_600%2Ch_800%2Climit_1%2Fquality%2Cq_85%2Fformat%2Cf_auto)](https://iknow-pic.cdn.bcebos.com/b3119313b07eca808b5967369f2397dda0448387)

6、如图所示 这是上面三个方法运行后的结果图，可以看到一个大的DIV中嵌套两个小的DIV。

[![img](https://iknow-pic.cdn.bcebos.com/8435e5dde71190ef6760cc0ec01b9d16fcfa6043?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_600%2Ch_800%2Climit_1%2Fquality%2Cq_85%2Fformat%2Cf_auto)](https://iknow-pic.cdn.bcebos.com/8435e5dde71190ef6760cc0ec01b9d16fcfa6043)