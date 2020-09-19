# adept_private
This is a  private repositorty for essay disscuion and work progress note 
# guide to use git
## 本地创建版本库
创建一个空目录：
    `mkdir learngit`

    `cd learngit`

git init命令把这个目录变成Git可以管理的仓库：
    `git init`

在该目录下创建编辑论文笔记（*.md文件）
    `vim PointPillars.md`

使用git add把文件添加到仓库(可一次添加多篇）：
    `git add  PointPillars.md`

命令git commit告诉Git，把文件提交到仓库：
    `git commit -m "wrote a new essay:PointPillars"`
## 推送到远程仓库
查看远程库信息，使用`git remote -v`；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用`git push origin branch-name`，如果推送失败，先用`git pull`抓取远程的新提交；

在本地创建和远程分支对应的分支，使用`git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用`git branch --set-upstream branch-name origin/branch-name`；

从远程抓取分支，使用`git pull`，如果有冲突，要先处理冲突。
