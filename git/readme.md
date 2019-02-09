# GIT

![maincommands](https://github.com/liuyongping99/git-test/blob/master/images/maincommands.png?raw=true)

## 工作区
- 工作区：工作区就是除开.git目录的其他东西。通过操作系统的文件索引来管理的内容。就是我们正常使用电脑的时候所看到，能编辑的内容。

## 暂存区
- 暂存区/缓冲区：暂存区并不存放文件内容，暂存区仅仅是一份处于编辑状态的快照（索引文件），这份快照没有编号。commit就是把暂存区保存到版本库，并给版本日志新增一个编号（HEAD/版本号）指向这个快照副本。
- 也叫index 或者 stage

## GIT本地仓库
平时的各种操作主要针对的是本地仓库
- 工作区和本地提交的内容都在.git目录下？
- git仓库：就是用来存放备份文件的地方，但是备份文件存入仓库的时候会压缩， 这些压缩的备份文件存放在.git/objects目录中，直接打开是乱码，而且为了节省空间，仓库不会存放重复的文件，只有新增和修改过的文件才会存入 git仓库，删除的时候并不会从仓库移除文件，不然我们怎么恢复呢。

## 操作系统文件系统层面对单个文件进行快照组织
![file-snapshot](https://github.com/liuyongping99/git-test/blob/master/images/fileblock-snap.png?raw=true)
- 文件快照，记录时块结构信息?

## GIT快照
- 一次COMMIT提交，对应一个快照。
- 所谓快照，就是保存当前的目录结构，以及每个文件对应的二进制对象。上一个ADD操作，目录结构已经保存好了，现在需要将这个目录结构与一些元数据一起写入版本历史。

## GIT提交时是快照
GIT每次提交保存的是文件快照，而不是文件备份
- 对单个文件进行SHA1计算，提交记录中保存的是相关文件的SHA1值
- Every time you commit, or save the state of your project in Git, it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot.
- 为提高性能，若文件没有变化，在COMMIT提交时Git 不会再次保存，而只对上次保存的快照作一链接。
![commit-snapshot](https://github.com/liuyongping99/git-test/blob/master/images/git-snapshot.png?raw=true)

## GIT快照原理
![structure](https://github.com/liuyongping99/git-test/blob/master/images/git-structure.jpg?raw=true)
- 文件的实际压缩存储和提交信息分离

## 分支
- 所谓分支（branch）就是指向某个快照的指针，分支名就是指针名。哈希值是无法记忆的，分支使得用户可以为快照起别名。而且，分支会自动更新，如果当前分支有新的快照，指针就会自动指向它。比如，master 分支就是有一个叫做 master 指针，它指向的快照就是 master 分支的当前快照。
- Git 有一个特殊指针HEAD， 总是指向当前分支的最近一次快照。另外，Git 还提供简写方式，HEAD^指向 HEAD的前一个快照（父节点），HEAD~6则是HEAD之前的第6个快照。
- 每一个分支指针都是一个文本文件，保存在.git/refs/heads/目录，该文件的内容就是它所指向的快照的二进制对象名（哈希值）。
~~~
refs/
refs目录存储都是引用文件，如本地分支，远端分支，标签等
refs/heads/xxx 本地分支
refs/remotes/origin/xxx 远端分支
refs/tags/xxx 本地tag
~~~
请参考[Git 原理入门](http://www.ruanyifeng.com/blog/2018/10/git-internals.html)

## SHA1
- Git把它所管理的所有对象（blob，tree，commit，tag……），全部根据它们的内容生成SHA1哈希串值作为对象名
- blob文件内容













