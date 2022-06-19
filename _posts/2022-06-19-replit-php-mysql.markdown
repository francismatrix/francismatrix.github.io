---
layout: post
title:  "【教程】如何白嫖Replit的免费云服务器建PHP+MySQL网站"
date:   2022-06-19 09:10:00 +0800
categories: 技术
---
Replit（https://repl.it）是一个基于浏览器的云端协同开发平台，可用于构建开发环境、实时协作、托管网络应用等。Replit提供创建HTML静态网站和PHP、SQLite动态网站项目的服务，并会自动生成免费https三级域名（格式为：项目.用户名.repl.co）。这代表着任何人都可以白嫖Replit的云服务器创建自己的网站，而不需要去godaddy等付费服务器商那里自讨苦吃。  
本人曾经尝试使用Vercel、SourceForge等网站托管平台托管自己的Typecho动态博客，无一例外皆被pass。后来在一个搭建Vercel PHP环境的文章里找到了Replit这个良心网站，经历两天的折腾，终于在Replit上搭建好自己的博客。  
以Typecho为例，在Replit上建立PHP+MySQL网站步骤如下：  
1：访问https://repl.it。Replit是国外的网站，所以加载会很慢。但起码没有github慢（逃  
2：注册帐号。可以用你常用的邮箱注册。注册后检查收件箱点击链接验证帐户。  
3：注册结束后Replit会自动登录你的帐号，并询问一些身份信息（可以跳过）。点选首页侧边栏按钮，选择“Create a Repl”（创建项目）  
4：在项目栏中选择“PHP Web Server”，并填写项目名称。  
5：Replit自动加载开发环境后，将测试用的“index.php”文件删除。在Typecho官网下载最新的Typecho程序文件，以比较麻烦的多个文件夹/文件形式导入。（必须这么做，不然大堆的temporary files会压得你喘不过气）导入完成后点击Start按钮，运行服务。  
6：搭建SQL数据库。免费的SQL Hosting服务不是没有，推荐一个https://freedb.tech。（亲测163可以正常注册）注册后点击dashboard，填写你的用户名和数据库名，系统会自动生成一个随机的密码。回到你托管的网站，访问 域名/install.php，在安装页面填入数据库信息，编码选择utf8mb4。（utf8会报500错误）  
7：网站搭建成功。  
其它架构同理。注意：Replit并不支持NET.ASP。  
（更新：mysql不稳定，建议使用sqlite建立网站）  
