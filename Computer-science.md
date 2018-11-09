---
title: Computer science
date: 2018-11-08 16:01:49
tags:
---

# cs five part
```
i can understand all this part from this month
can add part to it
u know this is a goog start


```

## hexo 
[how to install a new theme](http://theme-next.iissnan.com/getting-started.html)
### theme
[theme site](https://hexo.io/themes/)

## git

[git upgrade](https://stackoverflow.com/questions/21820715/how-to-install-latest-version-of-git-on-centos-7-x-6-x)
[git pull while not in a different directory](
 https://stackoverflow.com/questions/5083224/git-pull-while-not-in-a-git-directory/5083437)
 


## golang 

[invoke system comand](https://nathanleclaire.com/blog/2014/12/29/shelled-out-commands-in-golang/)


## python

[how to run many commands in os system](https://stackoverflow.com/questions/20042205/python-call-multiple-commands)

[jupyter check source code](readcolumns.readcolumns('alldata.xlsx',3))

```
jupyter run shortcut shift+enter
```
[plotly auth method](https://plot.ly/python/getting-started/)
```
jupyter install package u can in anaconda bin directory use pip to install
```

### drawing with plotly simple code
```python
from readcolumns import *
rate = readcolumns('alldata.xlsx',1)
iav = readcolumns('alldata.xlsx',3)
from compare import *
comp = compare(rate,iav)
trace0 = go.Scatter(
    x=comp[1],
    y=comp[0]
)
data = [trace0]
py.iplot(data, filename = 'basic-line')
```






## markdown
[sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links)