# 版本控制工具

## 一、集中式版本控制工具

CVS、SVN（Subversion）、VSS

有一个单一的集中管理的服务器

缺点：服务器单点故障

## 二、分布式版本控制工具

Git、Mercurial、Bazaar

1. 服务器断网下也能开发，版本控制是在本地进行的
2. 每个客户端保存的是整个完整的项目，包含历史记录，更加安全

| 命令名称                            | 作用                           |
| ----------------------------------- | ------------------------------ |
| git config--global user.name 用户名 | 设置用户签名（与托管中心无关） |
| git config --global user.email 邮箱 | 设置用户签名（与托管中心无关） |
| git init                            | 初始化本地库                   |
| git status                          | 查看本地库状态                 |
| git add 文件名                      | 添加到暂存区                   |
| git rm [-r] --cached 文件名         | 删除暂存区                     |
| git commit -m “版本信息” 文件名     | 提交到本地库                   |
| git reflog                          | 查看历史记录                   |
| git log                             | 查看详细记录                   |
| git reset --hard 版本号             | 版本穿梭                       |



1. 设置用户签名，初次使用必须设置
2. 初始化本地库
3. 添加暂存区
4. 提交本地库
5. 版本穿梭

## 三、分支操作

| 命令名称          | 作用                       |
| ----------------- | -------------------------- |
| git branch 分支名 | 创建分支                   |
| git branch -v     | 查看分支                   |
| git switch 分支名 | 切换分支                   |
| git merge 分支名  | 把指定分支合并到当前分支上 |

1. 查看分支
2. 创建分支
3. 切换分支
4. 合并分支

底层两个指针

HEAD **---->** 分支 **---->** 版本

## 四、团队协作机制

- 团队内协作

  PUSH--->CLONE--->PUSH--->PULL

- 跨团队协作

  PUSH--->FORK--->CLONE--->PUSH--->PULL request--->审核--->merge

## 五、连接GitHub

1. 创建远程仓库

   账户左侧加号，复制仓库http

2. 创建远程库别名

   git remote -v    查看当前所有远程地址别名

   git remote add 别名 远程地址

3. 推送本地分支到远程库

   git push 别名或链接 分支

4. 拉取分支

   git pull 别名 分支

5. 克隆分支

   git clone 远程地址

6. ssh免密登录

   ssh-keygen -t rsa -C github账户

   user.ssh下复制公钥

