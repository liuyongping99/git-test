a overview of markdown syntax

markdown语法

# title1
## title2
### title3

# 列表
```
-
*
```

# 引用代码
用三个连续单引号前后包围

# 插入本地图片
只需要在基础语法的括号中填入图片的位置路径即可，支持绝对路径和相对路径。
例如：
```
![avatar](/home/picture/1.png)
```

# 插入网络图片
比如： 
```
![avatar](https://github.com/youyou-579/123/blob/master/2.8.jpg?raw=true)
```
![avatar](https://github.com/youyou-579/123/blob/master/2.8.jpg?raw=true)

# 把图片存入MARKDOWN文件
- 基础用法
用base64转码工具把图片转成一段字符串，然后把字符串填到基础格式中链接的那个位置。
```
![avatar](data:image/png;base64,iVBORw0......)
```
这个时候会发现插入的这一长串字符串会把整个文章分割开，非常影响编写文章时的体验。如果能够把大段的base64字符串放在文章末尾，然后在文章中通过一个id来调用，文章就不会被分割的这么乱了。
- 高级用法
比如：
```
> ![avatar][base64str]
> [base64str]:data:image/png;base64,iVBORw0......
```
