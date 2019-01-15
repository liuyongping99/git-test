* mkdir hello-word &cd hello-world
* git init 把这个目录变成Git可以管理的仓库
  是一个空的仓库（empty Git repository）
* 创建一个readme.txt文件
  *记得把Notepad++的默认编码设置为UTF-8 without BOM即可*
* git add readme.txt
* git status
* git commit -m "This is my first commit via Git!"
  提交到本地仓库
* git log
  查看历史提交记录
* git branch
  查看当前有哪些分支
* git checkout -b feature
  创建一个名为feature的分支
* origin，远程仓库的默认标签，代表一个远程仓库地址？
* git remote add origin git@github.com:liuyongping99/learngit.git
  本地仓库关联到远程仓库
* git push -u origin master
  一次推送master分支的所有内容
  把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。

  
