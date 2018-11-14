---
title: Computer science
date: 2018-11-08 16:01:49
tags:
---
# cs five part
# Ios
[add search bar](https://www.youtube.com/watch?v=wVeX68Iu43E)

# Theory
[ai resource](https://github.com/allmachinelearning/MachineLearning)

# tools

## hexo 
[how to install a new theme](http://theme-next.iissnan.com/getting-started.html)
#### code of hexo theme change 
```
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
modify in _yml filetheme: next
hexo clean
hexo server
```


### theme
[theme site](https://hexo.io/themes/)

## git

[git upgrade](https://stackoverflow.com/questions/21820715/how-to-install-latest-version-of-git-on-centos-7-x-6-x)
[git pull while not in a different directory](
 https://stackoverflow.com/questions/5083224/git-pull-while-not-in-a-git-directory/5083437)




## nginx
```
server {

    listen       80;

    server_name  47.100.100.141;

    location / {

        proxy_pass http://127.0.0.1:8000;

    }


  # location /static {

  #     proxy_pass http://127.0.0.1:8000;

  # }

    location /v1 {

        proxy_pass http://127.0.0.1:801;

    }


#    location /wubin {

#        proxy_pass https://127.0.0.1:444;

#    }

    #rewrite (.*) https://blackboxo.top$1 permanent;

}


server {

     listen 443 ssl;

     server_name www.blackboxo.top;

     ssl on;

     index index.html;

     ssl_certificate   all.crt;

     ssl_certificate_key  server.key;

     ssl_session_timeout 5m;

     ssl_ciphers ECDHE-RSA-AES128-GCM-SHA256:ECDHE:ECDH:AES:HIGH:!NULL:!aNULL:!MD5:!ADH:!RC4;

     ssl_protocols TLSv1 TLSv1.1 TLSv1.2;

     ssl_prefer_server_ciphers on;


     location / {

         proxy_pass http://127.0.0.1:8000;

     }


     location /v1 {

         proxy_pass http://127.0.0.1:801;

     }


     location /wubin {

         proxy_pass https://127.0.0.1:444;

     }

}


#the above content is default.conf configure content

nginx -s reload #reload the nginx

nginx -t   #to test nginx change effection
```

 


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



### return 
when python function weill return None when there is no anything to return22




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

## interview

```
1.美团ios开发面试（处女面）

简单介绍你自已

tcp三次握手

链表中的环如何检测

谈谈你的项目

hash表的一些问题，例如冲突如何解决

线程与进程的区别

有没有用过oc

你有什么想问的

http的情况
```


someblog

a. about IOS and career 

ipython run in maxosx python -m IPython

resource

1.swift 

Swift
a.delete all array element 
b.How do I check if a string contains another string in Swift? 
c.swift open url in safari 

design
a.app icon generator 

var

access viewcontrller var from another vc 

ios tutorail
1.add a viewcontroller 
2.add background image
3.add background video https://www.youtube.com/watch?v=L5j5kQEWN7o4.get
4.get ios device position https://www.youtube.com/watch?v=XyncTJdXbbw(need to run in iphone )
5.turn off device sound https://stackoverflow.com/questions/31828654/turn-off-audio-playback-of-avplayer
6.textfield height https://stackoverflow.com/questions/8641557/how-to-set-uitextfield-height
7.understand delegate mode https://blog.csdn.net/lwjok2007/article/details/48087011
8.iOS simulator permission denied and not showing permission alert dialog
https://stackoverflow.com/questions/40386819/ios-simulator-permission-denied-and-not-showing-permission-alert-dialog
navigation controller(why we need navigator controller)
a.How To Use The Navigation Controller In Xcode 8 (Swift 3.0) https://www.youtube.com/watch?v=XARzl84FZW0
b.

viewcontroller
a.Same view controller loads twice https://stackoverflow.com/questions/46018202/same-view-controller-loads-twice


UI
a.How to set the border of UITextView to same as border color of UITextField https://stackoverflow.com/questions/25962449/how-to-set-the-border-of-uitextview-to-same-as-border-color-of-uitextfield

Tableview
8.tableview of ios https://www.youtube.com/watch?v=kYmZ-4l0Yy4
9.Expected Declaration error creating array in ViewController, can't work out why https://stackoverflow.com/questions/24479700/expected-declaration-error-creating-array-in-viewcontroller-cant-work-out-why
10.class wired init writting https://www.youtube.com/watch?v=YwE3_hMyDZA 4:30-5:00
11.How To Create A TableView In Xcode 8 (Swift 3.0) https://www.youtube.com/watch?v=fFpMiSsynXM
12.How To Create Custom Tableview Cells In Xcode 8 (Swift 3.0) https://www.youtube.com/watch?v=uBesaTUJZi0
13.Expandable and Collapsible Sections UITableView (Ep 3) https://www.youtube.com/watch?v=Q8k9E1gQ_qg
14.select a row in cell https://stackoverflow.com/questions/8404922/uitableview-didselectrowatindexpath
15.How to Pass Data Between View Controllers Using a Segue https://www.youtube.com/watch?v=HzKcLccB8FI
16.pass data in different conctroller https://www.youtube.com/watch?v=czWu1RXnnUE
17.tableviewcell action https://www.youtube.com/watch?v=A6Wl8ySrOZI
18.UITableView Cell Action (Swift 4 + Xcode 9.0) https://www.youtube.com/watch?v=5js6nwDcedE
19.tableview cell add icon https://www.youtube.com/watch?v=qSO9oir9JrM

db

 a.sqlite

1.how to use sqlite

navagator contorller
a. Adding Buttons to the Navigation Bar with Storyboards https://www.andrewcbancroft.com/2016/04/14/adding-buttons-to-the-navigation-bar-with-storyboards/
b.dissmiss a viewcontroller https://github.com/andrewcbancroft/StoryboardNavigationControllerExamples/blob/master/StoryboardNavigationControllerExamples/AddScreenViewController.swift
c.pass data via navigator controller https://stackoverflow.com/questions/25369412/swift-pass-data-through-navigation-controller

Xcode
a.Xcode 9 “iPhone is busy: Preparing debugger support for iPhone” https://stackoverflow.com/questions/46316373/xcode-9-iphone-is-busy-preparing-debugger-support-for-iphone

golang
1.string contain substring https://golang.org/pkg/strings/#Contains


html
1.empty html href https://stackoverflow.com/questions/22940761/best-way-to-create-an-a-link-with-empty-href
2.html background image https://www.computerhope.com/issues/ch000966.htm
3.how to learn them https://www.quora.com/What-is-the-best-way-to-learn-HTML-CSS-and-JavaScript

js
1.jquery get https://www.w3schools.com/jquery/ajax_get.asp
2.js var https://www.w3schools.com/js/js_variables.asp
3.json example 

4.a 3d js library

5. a  presentation js

6.json object and string

presentation
a.web presentation https://impress.js.org/#/bored

python
1.get ip of request https://stackoverflow.com/questions/3759981/get-ip-address-of-visitors
2.flask cross domain https://flask-cors.readthedocs.io/en/latest/

3.matplotib show on macosx https://markhneedham.com/blog/2015/03/26/python-matplotlib-hangs-and-shows-nothing-mac-os-x/

linux
1.screen commands https://www.howtoforge.com/linux_screen


database
a.Will MySQL reuse deleted ID's when Auto Increment is applied https://stackoverflow.com/questions/18692068/will-mysql-reuse-deleted-ids-when-auto-increment-is-applied

b.mysql record all query log for backup

0.about the init setup maybe this link is good 

1.add somethings in mysqld section of my.cnf

2.restart mysql/mariadb

3.about datadir use the command that is  

SHOW VARIABLES LIKE 'datadir';  

4.cat the file ls -al datadir/*.log


note:when the genearl log was started ,the log file when u deleted,it will cannot be created automatically,u need to restart ur mysql server,that is systemctl restart mariadb.service

c.about replication,i just kknow some direction,such as add some item in mysqld section of my.cnf

log-basename=master

log-bin

binlog-format=row

server_id=1

 







linux 

https://unix.stackexchange.com/questions/64148/how-do-i-make-ls-show-file-sizes-in-megabytes

https://www.quora.com/Why-is-1-MB-1024-KB-instead-of-1000-KB





