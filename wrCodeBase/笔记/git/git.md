# Git

## 什么是Git?

  - Git是一款源代码管理工具(版本控制工具)
    - 我们写的代码需要使用Git进行管理。
  - 源代码有必要管理起吗？
  - 1.0
  - 2.0 // 
  - svn,vss,vcs.... git
  - 有必要，因为人工的去处理不同的版本，做相应备份会很麻烦。
  - Git是linux之父当年为了维护linux---linus之前也是手动维护合并把文件发给Linus
  - linus自己写了一个版本管理的工具(Git)

## 版本管理

把编码过程中的每一步记录下来

后续如果出现了问题，只要记录了，就可以找回  （玩游戏存档）

## 常见版本管理软件

1. **git**分布式版本控制系统，没有中央服务器，每个人的电脑是一个完整的版本库，这样，工作的时候可不需要联网，因为版本都在自己电脑上，即每个人的电脑都有一个完整的版本库，那么如何实现多人协作呢？比如自己在电脑上修改了文件A，别人也修改了文件A，此时，需要把两人之间各自所做的修改推送给对方，就可以互相看到对方所做的修改了。

2. svn：集中式版本控制系统，版本库是集中放在中央服务器，工作的时候用的都是自己的电脑，所以开始工作之前需要从中央服务器那里获取最新的版本，然后开始工作，工作完后，需要把自己所做的工作推送到中央服务器。集中式版本控制系统必须要联网才能工作，如果在局域网中，有足够的宽带，运行速度够快，而在互联网环境下，网速慢通常会导致服务难以进行。

## 安装

官网地址：https://git-scm.com/downloads

![image-20200218231641653](images/image-20200218231641653-2039014.png)

![image-20200218231758663](images/image-20200218231758663.png)

![image-20200218231827679](images/image-20200218231827679.png)

![image-20200218231852127](images/image-20200218231852127.png)

选择好安装路径后，点击“Next”进入下一步，弹出安装配置窗口，包括git命令行、git图形窗口等

![image-20200218231909777](images/image-20200218231909777.png)

Additional icons 附加图标
	On the Desktop 在桌面上
Windows Explorer integration  Windows资源管理器集成鼠标右键菜单
	Git Bash Here
	Git GUI Here
Git LFS (Large File Support)  大文件支持
Associate .git* configuration files with the default text editor  将 .git 配置文件与默认文本编辑器相关联
Associate .sh files to be run with Bash  将.sh文件关联到Bash运行
Use a TrueType font in all console windows  在所有控制台窗口中使用TrueType字体
Check daily for Git for Windows updates  每天检查Git是否有Windows更新

![image-20200218232054029](images/image-20200218232054029.png)
Use the Nano editor by default  默认使用 Nano 编辑器
Use Vim (The ubiquitous text editor) as Git's default editor  使用 Vim 作为 Git 的默认编辑器
Use Notepad++ as Git's default editor  使用 Notepad++ 作为 Git 的默认编辑器
Use Visual Studio Code as Git's default editor  使用 Visual Studio Code 作为Git 的默认编辑器
Use Visual Studio Code Insiders as Git's default editor  使用Visual Studio Code Insiders 作为 Git 的默认编辑器

调整Path环境变量

![image-20200218232105734](images/image-20200218232105734.png)

配置PATH环境
Use Git from Git Bash only
This is the safest choice as your PATH will not be modified at all.You will only be able to use the Git command line tools form Git Bash.
这是最安全的选择，因为您的PATH根本不会被修改。您只能使用 Git Bash 的 Git 命令行工具。

Use Git from the Windows Command Prompt
This option is considered safe as it only adds some minimal Git wrappers to your PATH to avoid cluttering your environment with optional Unix tools . You will be able to use Git from both Git Bash and the Windows Command Prompt.
这个选项被认为是安全的，因为它只向PATH添加一些最小的 Git包，以避免使用可选的Unix工具混淆环境。 您将能够从 Git Bash 和 Windows 命令提示符中使用 Git。

Use Git and optional Unix tools from the Windows Command Prompt
从Windows命令提示符使用Git和可选的Unix工具
Both Git and the optional Unix tools will be added to you PATH
Git和可选的Unix工具都将添加到您计算机的 PATH 中
Warning:This will override Windows tools like "find and sort".Only use this option if you understand the implications.
警告：这将覆盖Windows工具，如 “ find 和 sort ”。只有在了解其含义后才使用此选项。

![image-20200218232120658](images/image-20200218232120658.png)

Use the OpenSSL library
使用 OpenSSL 库
Server certificates will be validated using the ca-bundle.crt file.
服务器证书将使用ca-bundle.crt文件进行验证。

Use the native Windows Secure Channel library
使用本地 Windows 安全通道库
Server certificates will be validated using Windows Certificate Stores.This option also allows you to use your company's internal Root CA certificates distributed e.g. via Active Directory Domain Services.
服务器证书将使用Windows证书存储验证。此选项还允许您使用公司的内部根CA证书，例如， 通过Active Directory Domain Services 。

![image-20200218232137463](images/image-20200218232137463.png)

Checkout Windows-style,commit Unix-style line endings
Git will convert LF to CRLF when checking out text files.When committing text files,CRLF will be converted to LF .For cross-pltform projects,this is the recommended setting on Windows ("core.autocrlf" is set to "true")
在检出文本文件时，Git会将LF转换为CRLF。当提交文本文件时，CRLF将转换为LF。 对于跨平台项目，这是Windows上推荐的设置（“core.autocrlf”设置为“true”）

Checkout as-is , commit Unix-style line endings
Git will not perform any conversion when checking out text files. When committing text files, CRLF will be converted to LF. For cross-platform projects,this is the recommended setting on Unix ("core.autocrlf" is set to "input")
在检出文本文件时，Git不会执行任何转换。 提交文本文件时，CRLF将转换为LF。 对于跨平台项目，这是Unix上的推荐设置 （“core.autocrlf”设置为“input”）

Checkout as-is,commit as-is
Git will not perform any conversions when checking out or committing text files.Choosing this option is not recommended for cross-platform projects ("core.autocrlf"is set to "false")
在检出或提交文本文件时，Git不会执行任何转换。对于跨平台项目，不推荐使用此选项（“core.autocrlf”设置为“false”）

![image-20200218232152859](images/image-20200218232152859.png)

Use MinTTY (the default terminal of MSYS2)
Git Bash will use MinTTY as terminal emulator,which sports a resizable window,non-rectangular selections and a Unicode font. Windows console programs (such as interactive Python) must be launched via 'winpty' to work in MinTTY.
Git Bash将使用MinTTY作为终端模拟器，该模拟器具有可调整大小的窗口，非矩形选区和Unicode字体。 Windows控制台程序（如交互式Python）必须通过'winpty'启动才能在MinTTY中运行。

Use Windows' default console window
Git will use the default console window of Windows ("cmd.exe"),which works well with Win32 console programs such as interactive Python or node.js , but has a very limited default scroll-back,needs to be configured to use aUnicode font in order to display non-ASCII characters correctly,and prior to Windows 10 its windows was not freely resizable and it only allowed rectangular text selections.
Git将使用Windows的默认控制台窗口（“cmd.exe”），该窗口可以与Win32控制台程序（如交互式Python或node.js）一起使用，但默认的回滚非常有限，需要配置为使用unicode 字体以正确显示非ASCII字符，并且在Windows 10之前，其窗口不能自由调整大小，并且只允许矩形文本选择。

![image-20200218232206673](images/image-20200218232206673.png)

Enable file system caching
启用文件系统缓存
File system data will be read in bulk and cached in memory for certain operations ("core.fscache" is set to "true"). This provides a significant performance boost.
文件系统数据将被批量读取并缓存在内存中用于某些操作（“core.fscache”设置为“true”）。 这提供了显着的性能提升。

Enable Git Credential Manager
启用Git凭证管理器
The Git Credential Manager for Windows provides secure Git credential storage for Windows,most notably multi-factor authentication support for Visual Studio Team Services and GitHub. (requires .NET framework v4.5.1 or or later).
Windows的Git凭证管理器为Windows提供安全的Git凭证存储，最显着的是对Visual Studio Team Services和GitHub的多因素身份验证支持。 （需要.NET Framework v4.5.1或更高版本）。

Enable symbolic links
启用符号链接
Enable symbolic links (requires the SeCreateSymbolicLink permission).Please note that existing repositories are unaffected by this setting.
启用符号链接（需要SeCreateSymbolicLink权限）。请注意，现有存储库不受此设置的影响。

![image-20200218232218619](images/image-20200218232218619.png)

![image-20200218232229109](images/image-20200218232229109.png)

## git使用步骤

### 初始化Git仓储/(仓库)

- 这个仓库会存放，git对我们项目代码进行备份的文件

  ​	mkdir learngit 		//创建一个名叫learngit的空目录

  ​	cd learngit 			//把learngit设置为当前目录

- 在项目目录右键打开 git bash

- 命令: `git init`

### 自报家门

- 就是在git中设置当前使用的用户是谁
- 每一次备份都会把当前备份者的信息存储起来
- 命令: 
  + 配置用户名:`git config --global user.name "yourname"`
  + 配置邮箱:  `git config --global user.email "email@qq.com"`

### 把代码存储到.git仓储中

- 1.把代码放到仓储的门口
  + `git add ./readme.md` 所指定的文件放到大门口
  + `git add ./` 把所有的修改的文件添加到大门口
- 2.把仓储门口的代码放到里面的房间中去
  + `git commit -m "这是对这次添加的东西的说明" `

### 可以一次性把我们修改的代码放到房间里(版本库)

- `git commit --all -m "一些说明"`
  + --all 表示是把所有修改的文件提交到版本库

### 查看当前的状态

- 可以用来查看当前代码有没有被放到仓储中去
- 命令: `git status`

### git中的忽略文件

- .gitignore,在这个文件中可以设置要被忽略的文件或者目录。
- 被忽略的文件不会被提交仓储里去.
- 在.gitignore中可以书写要被忽略的文件的路径，以/开头，
  一行写一个路径，这些路径所对应的文件都会被忽略，
  不会被提交到仓储中
  + 写法
    * ` /.idea  ` 会忽略.idea文件
    * ` /js`      会忽略js目录里的所有文件
    * ` /js/*.js` 会忽略js目录下所有js文件

### 查看日志

- `git log` 查看历史提交的日志
- `git log --oneline` 可以看到简洁版的日志



### 常见问题

命令输入的时候 有回车
1. git add . 							 add和.之间有空格

   （1）.git add all无论在哪个目录执行都会提交相应文件。

   （2）git add .只能够提交当前目录或者它后代目录下相应文件。

2. git commit   -m   "信息" 		commit 和-m之间有空格

### git版本穿梭

- `git reset --hard Head~0`
  + 表示回退到上一次代码提交时的状态
- `git reset --hard Head~1`
  + 表示回退到上上次代码提交时的状态

- `git reset --hard 版本号`
  + 可以通过版本号精确的回退到某一次提交时的状态

- `git reflog`
  + 可以看到每一次切换版本的记录:可以看到所有提交的版本号

### 修改用户名和邮箱

不用删除直接重新设置即可覆盖

```
git config --global user.email "you@example.com"

git config --global user.name "Your Name"
```

## 分支

- 默认是有一个主分支master

### 创建分支

- `git branch dev`
  + 创建了一个dev分支
  + 在刚创建时dev分支里的东西和master分支里的东西是一样的

### 切换分支

- `git checkout dev`
  + 切换到指定的分支,这里的切换到名为dev的分支
    `git branch` 可以查看当前有哪些分支


### 合并分支

- `git merge dev`
  + 合并分支内容,把当前分支与指定的分支(dev),进行合并
  + 当前分支指的是`git branch`命令输出的前面有*号的分支
- 合并时如果有冲突，需要手动去处理，处理后还需要再提交一次.
  - git branch -d dev

## GitHub 

### 远程仓库

**免费的远程仓库**，这个网站作用为开发人员提供免费的git远程仓库，让你把代码存起来

**全世界最大的开源软件平台**，很多流行的框架，项目会在github上公开，谁都可以看，学习

”全世界最大的同性交友平台“

- https://github.com
- 不是git,只是一个网站
- 只不过这个网站提供了允许别通过git上传代码的功能

另外一台电脑上有一个跟本地相同的 .git文件夹

多个地方都保存了同一个副本（仓库）

常见免费的远程仓库

1. github
2. gitlab
3. 码云
4. 公司内部的仓库
5. ..

### 使用步骤

#### 新建远程仓库



![1558601552540](assets/1558601552540.png)

### 提交代码到github(当作git服务器来用)

- `git push [地址] master`

 + 示例: `git push https://github.com/buka/test330.git master`
 + 会把当前分支的内容上传到远程的master分支上

- `git pull [地址] master`

 + 示例: `git pull https://github.com/buka/test330.git master`
 + 会把远程分支的数据得到:(*注意本地-要初始一个仓储!*)

#### 克隆到本地 

打开小黑窗

git clone 远程仓库地址

会得到远程仓储相同的数据,如果多次执行会覆盖本地内容。

![1558601567440](assets/1558601567440.png)

#### 易错点

输入用户名和密码

![1558602181097](assets/1558602181097.png)

输入用户名看的到，输入密码是看不到的

#### 本地编码 （最为频繁的操作）

1. 写东西
2. git add .
3. git commit -m "信息”

#### 提交到远程

git push 

把本地的推送到远程

一般不会那么频繁

建议 1天 1到2次即可



#### 用户名和邮箱设置建议

当你用了github之后 建议把你本地的git 设置的用户名和邮箱改为和github一致

github查看提交人的时候可以匹配到对应的github账号，更方便别人找到你

git config --global user.email "github邮箱"

git config --global user.name "github用户名"

## git辅助工具

简化git的操作，让开发人员专注于编码

1. tortoisegit
2. sourceTree
3. githubDesktop
4. *vscode*s

## github设置个人主页

1. 新建仓库

   你的用户名.github.io

![1558605716294](assets/1558605716294.png)

1. 克隆到本地
2. 编码 add commit 
3. 推送即可



## ssh方式上传代码

- 公钥 私钥,两者之间是有关联的。 密钥
- 生成公钥,和私钥
  + `ssh-keygen -t rsa -C "buka@sina.com"`

## 在push和pull操作进

- 先pull , 再push

- 当我们在push时，加上-u参数，那么在下一次push时
  我们只需要写上`git push`就能上传我们的代码。(加上-u之后，git会把
  当前分支与远程的指定的分支进行关联。git push origin master)







   

​    





