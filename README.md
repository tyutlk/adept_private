# adept_private
This is a  private repositorty for essay disscuion and work progress note 
# guide to use git
## 本地创建版本库
创建一个空目录：
    `mkdir learngit && cd learngit`

git init命令把这个目录变成Git可以管理的仓库：
    `git init`

在该目录下创建编辑论文笔记（*.md文件）
    `vim PointPillars.md`

使用git add把文件添加到仓库(可一次添加多篇）：
    `git add  PointPillars.md`

命令git commit告诉Git，把文件提交到仓库：
    `git commit -m "wrote a new essay:PointPillars"`
## 关联本地仓库与远程仓库
### 创建SSH Key。
在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：
`ssh-keygen -t rsa -C "youremail@example.com"`，把邮件地址换成你自己的邮件地址。

如果一切顺利的话，可以在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。

登陆GitHub，打开“Account settings”，“SSH Keys”页面：然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容，点“Add Key”，你就应该看到已经添加的Key。
### 克隆仓库到本地
`git clone git@github.com:tyutlk/adept_private.git`
## 推送到远程仓库
查看远程库信息，使用`git remote -v`；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用`git push origin branch-name`，如果推送失败，先用`git pull`抓取远程的新提交；

在本地创建和远程分支对应的分支，使用`git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用`git branch --set-upstream branch-name origin/branch-name`；

从远程抓取分支，使用`git pull`，如果有冲突，要先处理冲突。
