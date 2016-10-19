# Getting Git on a Server

### 方法一

   以下内容基于 Ubuntu 16.04 LTS \n \l

+ 在 server 的 root 用户下创建名为 git 用户 [ CMD: adduser git ]
+ set password
+ 在根目录下创建 sites 文件夹 [ CMD: mkdir sites ]
+ 赋予 git 用户修改 sites 文件夹的权限  [CMD: chown -R git:git /sites ]
+ 切换到 git 用户 [ CMD: sudo su git ]
+ 进入 sites 文件夹，并创建 vblog.limit.tech.git 文件夹并进入 [ CMD: mkdir vblog.limit.tech.git ]
+ 创建一个裸库，即初始化 vblog.limit.tech.git [ CMD: git init --bare ]
+ 在本地克隆服务器上的仓库 [ CMD: git clone git@192.168.0.0:/sites/vblog.limit.tech.git ]

   Finished ！！！O(∩_∩)O~
   
### 方法二

   此处省略 server 上 git 用户的创建
   
+ 在本地创建 vblog.limit.tech 文件夹，然后初始化它 [ CMD: git init ]
+ 登录远程 git 服务器，在 sites 目录下创建 vblog.limit.tech.git 文件夹 [ CMD: mkdir vblog.limit.tech.git ]
+ 初始化 vblog.limit.tech.git 文件夹为一个裸库 [ CMD: git init --bare ]
+ 在本地 vblog.limit.tech 目录里新增远程仓库。[ CMD: git remote -v 显示目前项目的远程仓库 ] [CMD: git remote add orgin git@192.168.0.0:/sites/vblog.limit.tech.git 新增加远程仓库]
+ 最后，git commit 提交本地代码
 
   Finished ！！！O(∩_∩)O~
   
   
   
   Note: 进入服务器端，若无法查看 git 库目录下已被提交的文件时用 git --work-tree=. checkout -f 命令
