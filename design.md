---
title: 用芯学项目
date: 2018-11-28 16:01:49
tags:
---


# 基本框架
以微信作为ID，来保证授权进行，获取对应课程，设计购物车功能


# 设计页面


# 基本功能
  收费系统-微信接入
  对应院校新闻栏目
  邀请好友
  精品课程
  大学选择部分，课程代码选择
  视频播放功能
  课程介绍模块
  经验贴讲解
  学员反馈部分
  用户系统支持（教师,学生）
  管理后台
  支持文件系统功能
  搜索功能

  
## 教师文件上传模块
1.支持视频上传功能
2.支持pdf等文档进行上传与下载
3.不设计文件删除功能



# 硬件事宜
阿里云服务器
阿里云域名


# design
![design](/images/design.jpg)
![teacher](/images/teacher.jpg)

#[小程序申请页面注册](https://mp.weixin.qq.com/wxopen/waregister?action=step1)
请注册企业类型





# API
1.except courseid,all items are string type!
2.server return a int type of  courseid  
3.chapterid and videoid should be created by request

## all api 

- [x] /course-------create  a course
- [x] /createvideo------create a video
- [ ] /getallcourse------get all course info from server
- [ ] /news-----------get news from server
- [ ] /user------------get user info
- [ ] /mainpage---------get mainpage info


## create a course

### application type is json
### url
/course
### method
post
### server implemention 
```golang
             Courses  struct {
                gorm.Model

                Courseid      uint32 `json:"Courseid"`
                Courseurls     string    `json:"coursesurls"`
                Description    string     `json:"description"`
                Teacheremail    string     `json:"Teacheremail"`
                Coursename      string   `json:"coursename"`
        }
```
### requests example
r.post('http://localhost:8082/course',json={'coursename':'马克思主义原理','description':"this is a good course"}).text


### response example
{"courseid":1107522238,"message":"u have uploaded info,please come on!","status":"posted"}



## create single video
### application type is json
### method
post
### server implemention
```golang
  videoname:= gjson.Get(reqBody, "videoame").String()
  courseid:= gjson.Get(reqBody, "courseid").String()
  videoid:= gjson.Get(reqBody, "videoid").String()
  chapterid:= gjson.Get(reqBody, "chapterid").String()
  videourl:= gjson.Get(reqBody, "videourl").String()
```

### request example
r.post('http://localhost:8082/createvideo',json={'videoname':'machine learning intro','courseid':255734,'videoid':'hvs','chapterid':'tre','videourl':"https://t.cn"})


### response type is json

{"message":"u have uploaded info,please come on!","status":"posted","videoid":"hvs"}

























# 进度事宜
12.2
1.使用测试服务器搭建服务器/小程序开发环境
3.建立代码仓库
3.[测试多媒体服务器](http://47.100.100.141:8081/)
4.其他事宜


12.3 
1.小程序接受bytes测试



12.4
1.视频从服务端推流测试
2.小程序播放视频测试
3.教师端上传界面设计



12.5
1.根据服务规模调研服务器框架
2.架设web服务器框架
3.设计数据库中的教师表学生表课程表
4.小程序页面主要ui组件设计



12.6
1.教师端上传教程接口设计
2.教师端文件结构解析设计




12.9
1.小程序用户页面
2.设计课程评论树存储结构
3.教师端视频上传api代码编写以及单元测试
4.接口文档
5.视频上传接口
6.创建章表节表
7.教师端上传视频联调





12.10
1.接口文档
2.教师端页面实现
3.解决跨域问题


12.11
1.教师端联调完成
2.教师端登录页面&视频传输页面设计完成
4.数据库测试完成

12.12
1.编写单个课程获取接口
2.编写所有课程获取接口
3.修正数据库编码问题
4.教师端页面创建课程的结构优化





