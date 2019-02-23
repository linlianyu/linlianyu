# UserWarning: No parser was explicitly specified

---

## 前记

&#8195;&#8195;本文参考[Beautiful Soup 4.4.0 文档](https://beautifulsoup.readthedocs.io/zh_CN/v4.4.0/)

---

## 代码

```
import bs4
exampleFile = open('Test.html')
exampleSoup = bs4.BeautifulSoup(exampleFile)
print(type(exampleSoup))
```

![](https://ws4.sinaimg.cn/large/006tNc79gy1fzt92mahmej30fs02faai.jpg)

## 错误信息

```
/Users/linlianyu/github/Python/start/TestHtml.py:7: UserWarning: No parser was explicitly specified, so I'm using the best available HTML parser for this system ("html5lib"). This usually isn't a problem, but if you run this code on another system, or in a different virtual environment, it may use a different parser and behave differently.

The code that caused this warning is on line 7 of the file /Users/linlianyu/github/Python/start/TestHtml.py. To get rid of this warning, pass the additional argument 'features="html5lib"' to the BeautifulSoup constructor.

  exampleSoup = bs4.BeautifulSoup(exampleFile)
<class 'bs4.BeautifulSoup'>
```

![](https://ws4.sinaimg.cn/large/006tNc79gy1fzt950ciqjj30wj04wt9m.jpg)

## 解决办法

在声明 exampleSoup 时,传入'html.parser'

```
exampleSoup = bs4.BeautifulSoup(exampleFile, 'html.parser')
```
