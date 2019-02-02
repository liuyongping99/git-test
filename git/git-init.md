* mkdir hello-word & cd hello-world
* git init 把这个目录变成Git可以管理的仓库
  是一个空的仓库（empty Git repository）
* 创建一个readme.txt文件
  *记得把Notepad++的默认编码设置为UTF-8 without BOM即可*
* git add readme.txt 保存到工作区（暂存区）
* git status
* git commit -m "This is my first commit via Git!"
  提交到本地仓库
* git log
  查看历史提交记录
* git branch
  查看当前有哪些分支
* git checkout -b feature
  创建一个名为feature的本地分支
* 在GitHub上创建远程库，--注意最好不要自动生成README文件--
* origin，是默认的远程版本库名称，远程仓库的默认标签，代表一个远程仓库地址
  一个origin, 可以有多个分支，默认主分支为master
* git remote add origin git@github.com:liuyongping99/learngit.git 
  将本地仓库关联到远程仓库
* git fetch origin
  拉取远程所有信息
  git fetch 命令会将数据拉取到你的本地仓库
* git push -u origin master
  git push origin master 的意思是 git push origin master:master 
  第1个master是本地分支，第2个是远程分支
  （将本地的 master 分支推送至远端的 master 分支，如果没有就新建一个
  -u参数表示一次推送master分支的所有内容
  把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。
  

  
