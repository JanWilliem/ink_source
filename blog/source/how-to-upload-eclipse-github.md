
title: 如何在Mac中把Eclipse项目上传到github
date: 2015-08-22 18:00:00 +0800
update: 2015-08-22 10:00:00 +0800
author: me
cover: -/images/githome.png
tags:
    - Design
    - Writing
preview: 本文记录了如何在Mac中把Eclipse项目上传到github

---

## 如何在Mac中把Eclipse中Java项目上传到github

![如何在Mac中把Eclipse中Java项目上传到github
](-/images/githome.png)

1. 在https://github.com   new repository

2. 在eclipse中new project  比如:Test项目

3. 右击"Test"->Team->share project...  ->select a repository type：Git
勾选  Use or create repository in parent folder of project

4. 点击  Create Repository  ->  Finish
这时候打开在workspace中的Test目录会发现多了一个.git文件夹。
5. 再右击"Test"->Team->Remote->Push

URI就是github上面指定的地址:
![image](http://static.oschina.net/uploads/space/2014/0723/151532_60HW_159239.jpg)

username和password就是github网站的用户名和密码

source ref 选择 refs/heads/master  destination ref会自动填充，点击  Add Spec勾选Focus update
开始提交。

6. 可以刷新网页查看提交的代码了。。。

注:在Eclipse中生public key, 并添加到GitHub Repository中。

     在菜单栏依次打开window → preference → general → network connection → SSH2 → Key Management → generate RSA Key... → apply → save private key...
     
    生成 SSH 的 public key在GitHub中通过：edit your profile -> ssh key -> Add SSH Key 添加SSH Key, 