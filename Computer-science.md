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

# Theory
[ai resource](https://github.com/allmachinelearning/MachineLearning)

# tools

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
### golang code
```golang
func Blogupdate (c *gin.Context){

var (
                cmdOut []byte
                err    error
        )
        cmdName := "git"
        cmdArgs := []string{"-C","/root/yangming/blog/source/_posts","pull","origin","master"}
        if cmdOut, err = exec.Command(cmdName, cmdArgs...).Output(); err != nil {
                fmt.Fprintln(os.Stderr, "There was an error running git rev-parse command: ", err)
                os.Exit(1)
        }
        sha := string(cmdOut)
        firstSix := sha[:6]
        fmt.Println("The first six chars of the SHA at HEAD in this repo are", firstSix)

  c.JSON(200, gin.H{
                        "status": "blog had updated",
                })

}
```

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
	###these are two list
    x=comp[1],
    y=comp[0]
)
data = [trace0]
py.iplot(data, filename = 'basic-line')
```
### pdf merge code 

```python
# use pip install to install this package
from PyPDF2 import PdfFileMerger

pdfs = ['file1.pdf', 'file2.pdf', 'file3.pdf', 'file4.pdf']

merger = PdfFileMerger()

for pdf in pdfs:
    merger.append(open(pdf, 'rb'))

with open('result.pdf', 'wb') as fout:
    merger.write(fout)
   
```



## markdown
[sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links)

```
If you want to embed images, this is how you do it:
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
use this direcotory to manage materail
```



