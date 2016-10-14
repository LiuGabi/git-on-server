# Getting Git on a Server

以下内容基于 Ubuntu 16.04 LTS \n \l

1. 在 server 的 root 用户下创建名为 git 用户 [ CMD: adduser git ]
2. set password
3. 在根目录下创建 sites 文件夹 [ CMD: mkdir sites ]
4. 赋予 git 用户修改 sites 文件夹的权限  [CMD: chown -R git:git /sites ]
5. 切换到 git 用户 [ CMD: sudo su git ]
6. 进入 sites 文件夹，并创建 vblog.limit.tech.git 文件夹并进入 [ CMD: mkdir vblog.limit.tech.git ]
7. 创建一个裸库，即初始化 vblog.limit.tech.git [ CMD: git init --bare ]
9. 在本地克隆服务器上的仓库 [ CMD: git clone git@192.168.0.0:/sites/vblog.limit.tech.git ]

   Finished ！！！O(∩_∩)O~
