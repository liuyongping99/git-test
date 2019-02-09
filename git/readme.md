# GIT

## 工作区
- 工作区：工作区就是除开.git目录的其他东西。通过操作系统的文件索引来管理的内容。就是我们正常使用电脑的时候所看到，能编辑的内容。

## 暂存区
- 暂存区/缓冲区：暂存区并不存放文件内容，暂存区仅仅是一份处于编辑状态的快照（索引文件），这份快照没有编号。commit就是把暂存区保存到版本库，并给版本日志新增一个编号（HEAD/版本号）指向这个快照副本。

## GIT本地仓库
平时的各种操作主要针对的是本地仓库
- 工作区和本地提交的内容都在.git目录下？
- git仓库：就是用来存放备份文件的地方，但是备份文件存入仓库的时候会压缩， 这些压缩的备份文件存放在.git/objects目录中，直接打开是乱码，而且为了节省空间，仓库不会存放重复的文件，只有新增和修改过的文件才会存入 git仓库，删除的时候并不会从仓库移除文件，不然我们怎么恢复呢。

## GIT快照原理
![structure](https://github.com/liuyongping99/git-test/blob/master/images/git-structure.jpg?raw=true)

## 文件系统层面对文件进行快照组织
![file-snapshot](https://github.com/liuyongping99/git-test/blob/master/images/fileblock-snap.png?raw=true)
- 文件快照，记录时块结构信息?

## 提交时的文件快照
GIT每次提交保存的是文件快照，而不是文件备份
- 对单个文件进行SHA1计算，提交记录中保存的是相关文件的SHA1值
- Every time you commit, or save the state of your project in Git, it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot.
- 为提高性能，若文件没有变化，在COMMIT提交时Git 不会再次保存，而只对上次保存的快照作一链接。
![commit-snapshot](https://github.com/liuyongping99/git-test/blob/master/images/git-snapshot.png?raw=true)








