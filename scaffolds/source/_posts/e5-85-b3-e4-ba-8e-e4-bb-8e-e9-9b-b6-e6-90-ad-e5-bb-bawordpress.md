---
title: 关于从零搭建WordPress
url: 9.html
id: 9
categories:
  - Konw
date: 2017-11-09 21:33:02
tags:
---

​	使用阿里云镜像市场的WordPress，总有各种疑难杂症。 

​	于是从零搭建WordPress。 

​	环境是LAMP(Linux,Apache,MySQL,PHP)。 

​	运行CentOS 7+，一些命令不兼容。 

​	MariaDB衍生于MySQL，兼容，且要替代。 

​	PHP配套PhpMyAdmin。PhpMyAdmin解压，配置即可。

​	WordPress下载插件等，需要Ftp账户。但操作一顿VSFTPD，登陆用户时总是报530等错误。 改用不需要Ftp的解决方法。 在 WordPress 目录下找到 wp-config.php 文件并编辑，在最后一行加上 `define('FS_METHOD', "direct");` 又参见[本地wordpress后台需要FTP密码解决办法](http://isay.me/2011/07/wordpress-ftp-password.html) 

​	进入WordPress主页，二级页面的文章打不开。Apache未支持伪静态，开Rewrite模块。   

​	打开域名主页并非WordPress，而是CentOS介绍页。 找一“404”网页模板，点击跳转。 首页语自许知远《十三邀》。语以后可动态处理，更换不同内容。