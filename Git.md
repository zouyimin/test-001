# 关于反馈
> 无  
> 对于整个流程不太熟悉  
> 主要分支这块  
> perfect!老师，我想问下在文件夹里右键打开git bash 和我把git bash放在桌面单击，有什么区别
> 基本理解，需要多练习,加强记忆.  
> 挺好的  
> 无  
> 视频好像有杂音,不碰话桶 ,,好多命令是在git bash中写的,希望可以注释再详细一点!

## git 回顾git的使用
> 版本控制工具(备份工具!)  git config --global 
git init
git add -A
git commit -m "大"
git status
git log
git log --oneline
git reflog
git branch dev
git checkout dev
git branch -d dev
git merge dev


## 流程(争对于一个项目 project)
> 代码还是像以前一样去写
> 0.git init (一个项目次)
> 1. git add -A / git commit -m (当我们觉得有必要去备份时执行!)
> 2. 继续写代码,如果完成了一个功能，就 git add -A / git commit -m
> 3. git status//  git log

> 使用分支的情况
> 当我想要备份代码,代码的功能才写了一部分,如果如果此时备份到master，由于master分支会共享给别人,
> 别人得到的代码就只有一部分，运行不了!  
> 【创建分支，然后在分支中提交代码!，直到这个功能完成了，就可以回到master分支，然后合并】
> git branch dev
> git checkout dev
> git add -A, git commit -m 一样是这两个命令
> 功能完成之后回到master分支
> git checkout master
> git merge dev

## 忽略清单文件 
.idea  $('dd').hide()
// 如果是项目中的代码，不想备的话(因为备的话，就会被别人得到!),需要让git把我们要忽略的代码，忽略掉。
> git 会自动检测 .gitignore 这个文件。
> 这个文件中列出的文件，或者文件，可以被git忽略  
> 这里可以被忽略的意思是 不会被备份到仓库中, 即使我们执行 git add 或者 git commit 命令,也会被忽略!

## 使用方式(.gitignore)
1.在项目根目录，新建新建一个名为 .gitignore 的文件
2.假如，我们希望test文件中的内容不被备份, 就在.gitignore 文件中添加一行
```
# 忽略项目根目录的test文件夹中的内容
/test

# 忽略项目中所有名为test的文件夹，或者文件
test

# 忽略项目中的名为app.js的文件
app.js

# 忽略项目中的所有js
*.js

/test/*.*
```

## 公用的电脑来备份(github)(远端仓库)
> github本身是个网站 
> 但是这个网站所在的电脑可以做为公用的电脑来备份代码!  
> 我们可以用这个[公用电脑也创建一个.git的文件夹](就是创建一个仓库)(远端仓库)
> 可以[把自己电脑中.git文件夹中的分支 上传到 这个公用电脑上的 .git文件夹中!]

0.注册github账号，并登陆
0.1. 先使用git bash 窗口，生成一个唯一的字符串(每个人每一次生成的都不一样)
打开git bash 输入 `ssh-keygen -t rsa`// 这个命令就会生成一个标识,我们需要把这个标识上传到服务器
会在 【/c/Users/[用户名]/.ssh】目录中生成两个文件: 
【id_rsa, id_rsa.pub】, 我们用编辑器打开id_rsa.pub,复制内容并关闭
02.在github网站上,把复制的密钥,添加到github上去!

1.选择 new Responsity 来新建一个新的远端仓库
2.只需要指定一个名字，并设置为public就可以
3.点击下方的 Create Resposity按钮 就可以创建完成一个远端仓库!
4.在要上传的项目中打开git bash 执行命令: 
`git push git@github.com:huoqishi/fed01.git master:master`
把本地的master分支中的记录上传到远端(git@github.com:huoqishi/fed01.git)的master分支中

tmp
`git push git@github.com:huoqishi/fed01.git master:xxx`
把本地的master分支上传到远端 xxx 分支


## git 上传代码到远端分支的简化命令
> 原来是 git push git@github.com:huoqishi/fed02.git master
> 现在: 
先执行:  git remote add origin git@github.com:huoqishi/fed02.git
// 这个origin 随便起, 就相当于设置 var origin = "git@github.com:huoqishi/fed02.git"
git push origin master

<!--java javascript-->

## 从远端仓库(github)来获取代码
- 刚来公司，要下载完整的代码一次!

*注意，注意，注意，注意*
*当我们想push代码到远端服务器上是地，需要[先执行pull],把远端服务器拿过来，在本地进行合并(合并过程是自动完成)*
*先pull再push*

## gitlab
- 局域网版本的github
- gitlab和github区别，是可以建私有仓库(关键是不要钱)



## gulp


<!--function hello () {
 // ...
}

function hello(){

}
function hello(){ console.log(1)}
-->















账号：  WEB26@bj.itcast.cn   密码：89410796    大家连下