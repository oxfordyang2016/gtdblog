---
title: Computer science
date: 2018-11-08 16:01:49
tags:
---
# basic concepts
1.同步与异步
同步：顺序执行
异步：同时执行

# alamofire execute function asyn!!!


# cs five part
# Ios
[add search bar](https://www.youtube.com/watch?v=wVeX68Iu43E)

# Theory
[ai resource](https://github.com/allmachinelearning/MachineLearning)

# tools

# hexo 
## [how to install a new theme](http://theme-next.iissnan.com/getting-started.html)
### code of hexo theme change 
```
$ cd your-hexo-site
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
modify in _yml filetheme: next
hexo clean
hexo server
```
### [hexo add image](http://jeffa.tech/adding-images-to-a-hexo-post-via-markdown/)

### [python concatenate item to list](https://stackoverflow.com/questions/12453580/concatenate-item-in-list-to-strings)




[conda not found](https://stackoverflow.com/questions/49821930/conda-command-not-found-even-though-path-is-exported)

### ios
[ios experience](http://www.code4app.com/blog-950206-21313.html)
[important project](https://juejin.im/post/5b97743df265da0af21351aa)
[tab bar and head navigation](https://juejin.im/post/5b7135db6fb9a009a257e557)
[ximalaya](https://juejin.im/post/5b97743df265da0af21351aa)

### theme
[theme site](https://hexo.io/themes/)

## git

[git upgrade](https://stackoverflow.com/questions/21820715/how-to-install-latest-version-of-git-on-centos-7-x-6-x)
[git pull while not in a different directory](
 https://stackoverflow.com/questions/5083224/git-pull-while-not-in-a-git-directory/5083437)





## [python nested dictionary](https://stackoverflow.com/questions/16333296/how-do-you-create-nested-dict-in-python)



### ios ui
[ios ui repository](https://medium.mybridge.co/39-open-source-swift-ui-libraries-for-ios-app-development-da1f8dc61a0f)
[menu](https://uxplanet.org/16-ios-menu-open-source-ui-animation-components-libraries-swift-obj-c-75b0c3f7dcc8)
[ios ui repository2](https://uxplanet.org/16-ios-menu-open-source-ui-animation-components-libraries-swift-obj-c-75b0c3f7dcc8)




[machine learning](https://medium.mybridge.co/30-amazing-machine-learning-projects-for-the-past-year-v-2018-b853b8621ac7?source=placement_card_footer_grid---------1-41)


[numpy array to list](https://docs.scipy.org/doc/numpy/reference/generated/numpy.ndarray.tolist.html)

# algorithm
[bianry search tree delete](http://www.algolist.net/Data_structures/Binary_search_tree/Removal)



## chrome reload website
```
Chrome:
open dev chrome
Hold down Ctrl and click the Reload button.
Or, Hold down Ctrl and press F5.
just open the Chrome Dev Tools by pressing F12. Once the chrome dev tools are open, just right click on the refresh button and a menu will drop down
```






### golang gin 
[allow cros](https://gocn.vip/article/529)


return empty
```golang
 func Register(c *gin.Context) {

     fmt.Println("-----------------")
     fmt.Println(Yangming)
     Email := c.PostForm("email")
    

     
     count:= 0
     db.Model(&Teachers{}).Where("email = ?", Email).Count(&count)
     if(count >0){
       c.JSON(http.StatusOK,  gin.H{
            "status":  "this email had been Registered",
            "code":901,
        })
       return 
     }

     Passowrd:= c.DefaultPostForm("password", "anonymous")
     name:= c.PostForm("name")
     fmt.Println(name)
     description:=  c.PostForm("description")
     //User1 := Accounts{Email: Email,Username:Username,Password:Passowrd}
     Teacher:= Teachers{Email: Email,Teachername:name,Password:Passowrd,Description:description}
     fmt.Println(Email,Passowrd)
     //fmt.Println(User1)
    // db, _ = gorm.Open("mysql", "dt_admin:dt2016@/dreamteam_db?charset=utf8&parseTime=True&loc=Local")
     db.Save(&Teacher)
     c.JSON(http.StatusOK,  gin.H{
            "status":  "logined",
            "code":200,
        })
  }

```




### [golang interface(method sets)](http://www.golangbootcamp.com/book/interfaces)







# nginx
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

 
# database

### basic knowledge
主键：

主键是数据表的唯一索引，比如学生表里有学号和姓名，姓名可能有重名的，但学号确是唯一的，你要从学生表中搜索一条纪录如查找一个人，就只能根据学号去查找，这才能找出唯一的一个，这就是主键;如：id int(10) not null primary key auto_increment ；自增长的类型 ；



### often opeartions

create database 
db CREATE DATABASE testdb;


create table
create table if not exists  dataset(date DATE,tenyearsreutrnrate date);


Third, you can optionally specify the storage engine for the table in the ENGINE clause. You can use any storage engine such as InnoDB and MyISAM. If you don’t explicitly declare the storage engine, MySQL will use InnoDB by default.


describe table
describe tablename;


modify table column type:
ALTER TABLE `dataset` MODIFY `tenyearsreutrnrate` float  NOT NULL;


[modify table column name(u need to add type)](https://www.tutorialspoint.com/mysql/mysql-alter-command.htm)
ALTER TABLE dataset  CHANGE  tenyearsreutrnrate  tenyearsreturnrate float;


delete a table
drop table students;




delete a row from mysql
delete from dataset where date = "2020-08-04"




insert a row
insert into  dataset (date,tenyearsreturnrate) values ('2020-08-04','0.62')


add a new columns definition
ADD COLUMN droo7  float  AFTER tenyearsreturnrate;







#### [mysql and python](https://opensourceforu.com/2009/05/database-programming-in-python/)
```python
#Python and MySQL are a good combination to develop database applications. After starting the MySQL service on Linux, you need to acquire MySQLdb, a Python DB-API for MySQL to perform database operations. You can check whether the MySQLdb module is installed in your system with the following command:

import MySQLdb
#If this command runs successfully, you can now start writing scripts for your database.

#To write database applications in Python, there are five steps to follow:

#Import the SQL interface with the following command:
import MySQLdb
#Establish a connection with the database with the following command:
conn=MySQLdb.connect(host='localhost',user='root',passwd='')
#where host is the name of your host machine, followed by the user name and password. In case of the root, there is no need to provide a password.

#Create a cursor for the connection with the following command:
cursor = conn.cursor()
#Execute any SQL query using this cursor as shown below—here the outputs in terms of 1L or 2L show a number of rows affected by this query:
cursor.execute('Create database Library')
#1L      // 1L Indicates how many rows affected



cursor.execute('use Library')
# u need to note string use
table='create table books(book_accno char(30) primary key, book_name char(50),no_of_copies int(5),price int(5))'
cursor.execute(table)
0L
#Finally, fetch the result set and iterate over this result set. In this step, the user can fetch the result sets as shown below:
cursor.execute('select * from books')
2L
cursor.fetchall()
(('Py9098', 'Programming With Python', 100L, 50L), ('Py9099', 'Programming With Python', 100L, 50L))
#In this example, the fetchall() function is used to fetch the result sets.


#when u do insert op,u need to commit
#https://stackoverflow.com/questions/6027271/python-mysql-insert-not-working
conn.commit()
```

#### from python to insert data to mysql
```python

import MySQLdb
from readcolumns import *
day = readcolumns('r007.xls',0)
r007 = readcolumns('r007.xls',1)
print day[0:2],day[-2:]
print r007[0:2],r007[-2:]
newday = day[1:-2]
newr007 = r007[1:-2]
print len(newday) == len(newr007)
print newday[0:3],newr007[0:3]
print newday[-3:],newr007[-3:]



#Establish a connection with the database with the following command:
conn=MySQLdb.connect(host='localhost',user='root',passwd='123456')
#where host is the name of your host machine, followed by the user name and password. In case of the root, there is no need to provide a password.

#Create a cursor for the connection with the following command:
cursor = conn.cursor()
cursor.execute("use finance;")
#Execute any SQL query using this cursor as shown below—here the outputs in terms of 1L or 2L show a number of rows affected by this query:
import math
for day in newday:                                                                                                       
    id = newday.index(day)
    r007 = newr007[id]
    #float nan
    if math.isnan(r007):
        r007 = -1.00
    op = "update dataset set r007 ="+str(r007) + " where date = '"+str(day)+"';" 
    print(op)
    cursor.execute(op)



 conn.commit()   
```


### [mysql alter performance problem](https://stackoverflow.com/questions/12774709/mysql-very-slow-for-alter-table-query)
```
MySQL’s ALTER TABLE performance can become a problem with very large tables. MySQL performs most alterations by making an empty table with the desired new structure, inserting all the data from the old table into the new one, and deleting the old table. This can take a very long time, especially if you’re short on memory and the table is large and has lots of indexes. Many people have experience with ALTER TABLE operations that have taken hours or days to complete.

Anyway if you need to proceed with alter table, maybe the following resources could help you:

https://www.percona.com/doc/percona-toolkit/2.2/pt-online-schema-change.html
https://github.com/soundcloud/lhm
https://githubengineering.com/gh-ost-github-s-online-migration-tool-for-mysql/

```



## web user system
```golang
 func Register(c *gin.Context) {

     fmt.Println("-----------------")
     fmt.Println(Yangming)
     Email := c.PostForm("email")
     Passowrd:= c.DefaultPostForm("password", "anonymous")
     Username:= c.PostForm("username")
     User1 := Accounts{Email: Email,Username:Username,Password:Passowrd}
     fmt.Println(Email,Passowrd,Username)
     fmt.Println(User1)
    // db, _ = gorm.Open("mysql", "dt_admin:dt2016@/dreamteam_db?charset=utf8&parseTime=True&loc=Local")
     db.Save(&User1)
     c.HTML(http.StatusOK, "user.html", nil)
  }


func  Login(c *gin.Context) {
       //cookie set
      //store := sessions.NewCookieStore([]byte("secret"))
      //router.Use(sessions.Sessions("mysession", store))
        email := c.PostForm("email")
      passowrd:= c.PostForm("password")
      client:=c.PostForm("client")
            fmt.Println(client)
            //session := sessions.Default(c)
            //session.Set("count", "yangming")
            //session.Save()
            fmt.Println(email,passowrd,client)
            cookie := &http.Cookie{
                            Name:  "username",
                            Value: email,
                    }
            http.SetCookie(c.Writer, cookie)
            cookie1 := &http.Cookie{
                            Name:  "email",
                            Value: email,
                    }
            http.SetCookie(c.Writer, cookie1)
            cookie2 := &http.Cookie{
                            Name:  "logintime",
                            Value: "now-nounspecify",
                    }
            http.SetCookie(c.Writer, cookie2)
            cookie3 := &http.Cookie{
                            Name:  "client",
                            Value: client,
                    }
            http.SetCookie(c.Writer, cookie3)
                    //c.String(http.StatusOK, "0")
            if client == "web"{
                //https://github.com/gin-gonic/gin to redirect
                c.Redirect(http.StatusMovedPermanently, "/inbox")
                //c.Redirect(http.StatusMovedPermanently, "/mainboard")
         //c.HTML(http.StatusOK, "user.html", nil)
         }else{
             c.JSON(http.StatusOK,  gin.H{
            "status":  "logined",
        })
         }
  }

```




# js read last item in a array
```js
loc_array[loc_array.length-1]
```










# network
```golang
//from now see,the client send bytes to server ,server to accept all byte to convert it to string
    //https://github.com/gin-gonic/gin/issues/1295
     buf := make([]byte, 1024)
    num, _ := c.Request.Body.Read(buf)
        //reqBody := string(buf[0:num])
    req := buf[0:num]



```


### golang json struct unmashal
```json
{'courseid':'5677',
     'addedvideos':[{'videoname':u'线性代数','courseid':'1348355370','videoid':'2','chapterid':'2','videourl':'https://t.cn','Description':'i am ge','Chaptername':'机器学习'
     ,'Description':'this is a joke'},{'Videoname':u'关于svm','Courseid':'1348355370','Videoid':'1','Chapterid':'3','Videourl':'https://t.cn','Description':'i am ge','Chaptername':'机器学习'
     ,'Description':'this is a joke'}],
    'deletedvideos':['223','345'],
     'updatedvideos':[{'Videoname':u'生物电子的解释','Courseid':'1348355370','Videoid':'2','Chapterid':'2','Videourl':'https://t.cn','Description':'i am ge','Chaptername':'机器学习'
     ,'Description':'this is a joke'},{'Videoname':u'机器学习的方法','Courseid':'1348355370','Videoid':'1','Chapterid':'1','Videourl':'https://t.cn','Description':'i am ge','Chaptername':'机器学习'
     ,'Description':'this is a joke'}]} 
```


```golang

func Actiononvideos1(c *gin.Context) {

var videos Createdvideos
    //---------------get body string-------------
    //https://github.com/gin-gonic/gin/issues/1295
     buf := make([]byte, 1024)
        num, _ := c.Request.Body.Read(buf)
        //reqBody := string(buf[0:num])
        req := buf[0:num]
  
    err := json.Unmarshal(req, &videos)
   fmt.Println(err)
   fmt.Println(videos.Courseid)
   fmt.Println(videos.Addedvideos)
   fmt.Println(videos.Deletedvideos)
   fmt.Println(videos.Updatedvideos)}







```


### [对称加密与非对称加密]











# ![lan network](https://serverfault.com/questions/229441/how-do-i-access-a-local-web-server-on-my-laptop-from-another-computer)


i using ifconfig to show my local ip in same network and using fellowing
en1 (8):
  inet address  192.168.0.74
  netmask       255.255.255.0
  broadcast     192.168.0.255
  flags         UP BROADCAST NOTRAILERS RUNNING SIMPLEX MULTICAST
  mtu           1500






# allow jupyter was visited[https://stackoverflow.com/questions/39155953/exposing-python-jupyter-on-lan]
```
0.generate configure file using jupyter notebook --generate-config
1.set in configure file and add 
c.NotebookApp.ip = '0.0.0.0' # listen on all IPs
c.NotebookApp.token = ''     # disable authentication
c.NotebookApp.allow_origin = '*' # allow access from anywhere
c.NotebookApp.disable_check_xsrf = True # allow cross-site requests
2.jupyter notebook --ip <your_LAN_ip> --port 8888
```








# golang 


[hash](https://play.golang.org/p/_J2YysdEqE)


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

# python


### requests library
[set header](#http://docs.python-requests.org/en/master/)
get cookie
```python
r.cookies
r.cookies["email"]
```

[How does collections.defaultdict work?](https://stackoverflow.com/questions/5900578/how-does-collections-defaultdict-work)




### [python from 3.7 onward,the dictionary keep origin  indert irder!](https://stackoverflow.com/questions/1867861/dictionaries-how-to-keep-keys-values-in-same-order-as-declared)


### return 
when python function weill return None when there is no anything to return22

### jupyter run in macosx
[add to path](https://github.com/jupyter/help/issues/136),it may not work when u restart your macosx,these is very obvios
expose to lan---jupyter-notebook   --ip 192.168.0.74  --port 8888
when i run in a certain directory , it will expose fixed dir to lan
[all cells not run when u load a notebook](https://stackoverflow.com/questions/31984196/ipython-notebook-run-all-cells-on-open/38856870)
You can run the notebook document step-by-step (one cell a time) by pressing shift + enter.
You can run the whole notebook in a single step by clicking on the menu Cell -> Run All.








[jupyter show image](https://stackoverflow.com/questions/32370281/how-to-embed-image-or-picture-in-jupyter-notebook-either-from-a-local-machine-o)

[how to run many commands in os system](https://stackoverflow.com/questions/20042205/python-call-multiple-commands)

[jupyter check source code](readcolumns.readcolumns('alldata.xlsx',3))

```
jupyter run shortcut shift+enter
```
[plotly auth method](https://plot.ly/python/getting-started/)
```
jupyter install package u can in anaconda bin directory use pip to install
method1
```
[anaconda install package](https://github.com/jupyter/notebook/issues/1524)
method2
```
$ /Users/abc/anaconda/bin/python -m pip install ipykernel
$ /Users/abc/anaconda/bin/python -m  ipykernel install
```

#### [conda install mysqldb](https://stackoverflow.com/questions/34140472/how-can-i-use-conda-to-install-mysqldb)
```
You could either fall back on pip install:

pip install mysql-python
or, if there are issues with pip as in your case, use a binstar package like so:

conda install binstar
binstar search -t conda mysql-python
and then conda install -c a matching package.
```


# sql query last item
```
 select * from reviewofdays   order by id desc limit 1\G;
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



# js function example
```js
function myFunction(a, b) {
  return a * b;
}
```
[js splice](https://code.likeagirl.io/javascript-splice-explanation-665243503d8b)

console.log
```
console.log(event.data)
```




```
b = ['2015-08-28', 3.83, 3.795, 3.83, 3.795, 0]
(6) ["2015-08-28", 3.83, 3.795, 3.83, 3.795, 0]
rawData[i][0]
VM1349:1 Uncaught ReferenceError: i is not defined
    at <anonymous>:1:9
(anonymous) @ VM1349:1
b[0]
"2015-08-28"
c = b.splice(0,1)
["2015-08-28"]
b
(5) [3.83, 3.795, 3.83, 3.795, 0]
```







# markdown
[sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links)

```
If you want to embed images, this is how you do it:
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
use this direcotory to manage materail
```



# golang 

## how i make a gtdgolangserver
[setting gopath](https://github.com/golang/go/wiki/SettingGOPATH)
[many directory in gopath](https://stackoverflow.com/questions/36017724/can-i-have-multiple-gopath-directories)
[when the go file init() to run](https://stackoverflow.com/questions/24790175/when-is-the-init-function-run)
golang-fault  (default table name is `users`)







# interview

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


# [view relationship](https://www.youtube.com/watch?v=e5nxg5NzLks)


### scp command from desktop to aliyun server
```
 sudo scp -i     ~/Downloads/yangming.pem    ~/Desktop/teacher.jpg  root@47.100.100.141:~/ 
```
### scp from server to localhost
```
scp -i ~/Downloads/yangming.pem root@47.100.100.141:~/yangming/gtdgolangserver/src/github.com/yangming/templates/review.html       ~/Desktop
review.html
```



## python list
[how to modify a passed list](https://stackoverflow.com/questions/22054698/python-modifying-list-inside-a-function)

i believe that  a = [1,2,3,4,5]
a[2:3] __addr__ have no any relationship


## python print
[python dict 中文显示问题](https://blog.csdn.net/zhangchaoy/article/details/19337841)







# db

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

[拓扑排序](https://blog.csdn.net/lisonglisonglisong/article/details/45543451)
[拓扑排序结果不唯一](https://blog.csdn.net/Jasmine_shine/article/details/43488895)

about topological sort,u need to select the source --最开始的顶点




[set title of navigation bar](https://stackoverflow.com/questions/6154237/how-to-set-the-title-of-a-navigation-bar-programmatically)


ios struct
[task()] is a list that had in clude a empty instance
[task]() to indicate the list is a task struct-type,it is a empty list now


## mysql restore database
   mysql -u root -p123456<database_20181122_0303.sql





# linux 

https://unix.stackexchange.com/questions/64148/how-do-i-make-ls-show-file-sizes-in-megabytes

https://www.quora.com/Why-is-1-MB-1024-KB-instead-of-1000-KB



[scroll view sucess example](https://www.youtube.com/watch?v=LhhW3xqhCzg&t=17s)


# algorithm
 [前驱和后继](https://blog.csdn.net/zhaoyunfullmetal/article/details/47903319)


[windows lan accessed websockets](https://blog.csdn.net/Bruce_shan/article/details/69252370)

[dag shortest path](https://www.youtube.com/watch?v=TXkDpqjDMHA)
```
u need to know when u compute the node,the privious node may be the last seconde
node
```




# chrome
[Switching back to last *used* tab on Chrome](https://superuser.com/questions/402095/switching-back-to-last-used-tab-on-chrome)

# flask  quick start
```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
   return 'Hello World’


@app.route('/')
def index():
   return render_template('hello.html')




if __name__ == '__main__':
   app.run()
```

[flask server static file](https://github.com/oxfordyang2016/flask-help/blob/master/templates/register.html)

# flask
i had find that when u are running a flask ,when u modify the  html ,it may not leads any effects in html




# algorithm
[binary search tree search from tree root](https://www.cs.usfca.edu/~galles/visualization/BST.html)

[binary search tree exsit no have succssor and pressor当取到树中最大或最小值时](https://visualgo.net/bn/bst)

[How to implement a binary search tree in Python?](https://stackoverflow.com/questions/5444394/how-to-implement-a-binary-search-tree-in-python?answertab=oldest#tab-top)




# source
[source site](https://archive.org/)
[paper site](https://arxiv.org/)
[teach yourself cs](https://news.ycombinator.com/item?id=13862284)
[teach yourself cs](https://teachyourselfcs.com/)
[chance](https://bradfieldcs.com/)
[steve jobs](https://news.ycombinator.com/item?id=3078128)
[it hare](http://ithare.com/)
[indie hackers](https://www.indiehackers.com/products)
[some advice](https://docs.google.com/document/d/1MBpwNLl3AgsKi4Yh4PZ2X30PYy4gV9xK2xgqXKevaVQ/edit#heading=h.r7te9ign1nt1)
[how to get startup idea](https://news.ycombinator.com/item?id=4806852)
[how to get startup](http://paulgraham.com/startupideas.html)
[how to be haapy](https://www.lesswrong.com/posts/ZbgCx2ntD5eu8Cno9/how-to-be-happy)
[about learn](https://jamesaltucher.com/2010/12/breakdancing-universe/)
[manage your enegy](https://hbr.org/2007/10/manage-your-energy-not-your-time?utm_campaign=harvardbiz&utm_source=twitter&utm_medium=social)
[tech trends](https://whatsthebigdata.com/2017/01/04/a-timeline-of-future-technologies-2019-2055/)
[tech interview](http://blog.interviewing.io/lessons-from-3000-technical-interviews/)






# gin 
## pasrse json 
```golang

    //---------------get body string-------------
    //https://github.com/gin-gonic/gin/issues/1295
     buf := make([]byte, 1024)
        num, _ := c.Request.Body.Read(buf)
        reqBody := string(buf[0:num])


   //--------------using gjson to parse------------


  //emailcookie,_:=c.Request.Cookie("email")
  //fmt.Println(emailcookie.Value)
  //email:=emailcookie.Value
  coursename:= gjson.Get(reqBody, "coursename").String()
  fmt.Println(coursename)
  courseid := hash(coursename)
```













