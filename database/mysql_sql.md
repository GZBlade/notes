### 2017-9-11

#### 设置

忘记密码：linux下解决步骤：

停止服务器——添加skip-grant-table配置——重启——无密码登录——sql修改密码

在mysql库中 1. update user set password=PASSWORD('new password')where user='root';

​			2.set password for 'root'@'localhost'=PASSWORD('new password');

刷新权限——取消无密码登录——重启服务器

#### sqlalchemy操作

看[sqlalchemy](https://www.bilibili.com/video/av8738667/?from=search&seid=12065405772298657259) 的英文版入门视频，克服对纯英文的畏难情绪。Ajde。





#### 2017-9-13

##### Git学习

今天首先看的是一个借助github搭建静态网页服务器的教程。主要内容总结如下：

- 首先在github上创建项目，利用github客户端