# 远端创建，本地克隆

* 首先在远程创建库
* 然后在本地git clone git@github.com:<username>/<projectname>.git  
  git clone git@github.com:michaelliao/gitskills.git
  git clone操作是 拷贝一个 Git 仓库到本地，让自己能够查看该项目，或者进行修改
* git branch --all
  clone之后，默认是本地master分支和远程的origin/master分支关联起来
  远程也可能有多个分支
* git pull 拉取所有代码
* git checkout -b feature 创建新的开发分支，新的本地分支
  git checkout -b 本地分支名 远程分支名
  使用-t参数，它默认会在本地建立一个和远程分支名字一样的分支
  git checkout -b 远程分支名
* git commit -m "some message" 在feature分支上提交
* git checkout master，然后更新git pull

