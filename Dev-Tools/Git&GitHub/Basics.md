

## 使用GitHub

### 基本概念

**Repository**：仓库，对应一个**git库**用于存放项目代码，每个项目对一个仓库。

**Star**： 收藏

**Fork**：复制克隆一个项目到自己的GitHub中，该fork的项目是独立存在的。

![image-20190519110503099](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/fork.png)

**Pull Request**：基于fork实现，发起合并请求。

![image-20190519110616794](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/pull-request.png)

**Watch**：关注项目，可以接收到项目更新提醒。

**Issue**：事务卡片，发现代码bug，但目前没有成型代码，需要讨论时可用；或者使用开源项目出现问题时使用。

![image-20190519111011396](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/issue.png)



> **如何为开源项目做出贡献**：
>
> 1. 新建issue
>
> ​       提交使用问题或者建议或者想法
>
> 2. Pull request
>    1. fork项目
>    2. 修改自己仓库的项目代码
>    3. 新建pull request
>    4. 等待作者操作（合并）



### GitHub主页



### 仓库主页

**Commits**：可以查看每次修改的相关信息，包括删除文件详细信息。

**Issues**：可以进行问题讨论，解决后可以close。



### 个人主页



### GitHub Pages搭建个人网站

#### 个人网站

搭建步骤：

1. 创建个人站点 -> 新建仓库（注意：仓库名必须是 用户名.github.io）
2. 在仓库下新建index.html的文件

访问：[https://用户名.github.io](https://用户名.github.io)

注意：github pages只支持静态网页，仓库里面只能是.html文件

 

#### 项目站点

搭建步骤：

1. 进入项目主页，点击settings
2. ...

访问：[https://用户名.github.io/仓库名](https://用户名.github.io/仓库名)





## Git

> 通过Git管理GitHub托管项目代码。

### 安装



### 通用操作流程

![image-20190519183537733](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git9.png)

主要涉及到四个关键点：

1. 工作区：本地电脑存放项目文件的地方，比如learnGitProject文件夹；
2. 暂存区（Index/Stage）：在使用git管理项目文件的时候，其本地的项目文件会多出一个.git的文件夹，将这个.git文件夹称之为版本库。其中.git文件夹中包含了两个部分，一个是暂存区（Index或者Stage）,顾名思义就是暂时存放文件的地方，通常使用add命令将工作区的文件添加到暂存区里；
3. 本地仓库：.git文件夹里还包括git自动创建的master分支，并且将HEAD指针指向master分支。使用commit命令可以将暂存区中的文件添加到本地仓库中；
4. 远程仓库：不是在本地仓库中，项目代码在远程git服务器上，比如项目放在github上，就是一个远程仓库，通常使用clone命令将远程仓库拷贝到本地仓库中，开发后推送到远程仓库中即可；



### 基本操作

#### 基本信息设置

1. 设置用户名 `git config –-global user.name '这里填写自己的用户名'`
2. 设置用户名邮箱 `git config –-global user.email '这里填写自己的用户名邮箱'`
3. 查看设置 `git config --list`

#### 初始化一个新的Git仓库

1. 创建文件夹

2. 在文件夹内初始化Git（创建Git 仓库）

   命令行进入当前目录，使用 `git init`命令，成功会显示 .git 文件

#### 向仓库中添加文件

![image-20190519145247188](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git.png)

1. 创建新文件；

   ![image-20190519154001392](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git1.png)

2. 添加到暂存区

   ![image-20190519154127997](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git2.png)

3. 提交到仓库

   ![image-20190519154616259](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git3.png)

####  修改仓库文件

1. 修改文件；

2. 添加到暂存区
3. 提交到仓库

#### 删除仓库文件

1. 删除工作目录文件；![image-20190519155642800](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git4.png)
2. 从Git中删除；![image-20190519155816949](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git5.png)
3. 提交到仓库。![image-20190519160302709](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git6.png)

#### 多个文件的操作

使用git add提交多个文件：

1. `git add .   `  提交被修改的和新建的文件，但不包括被删除的文件                            

2. `git add -u 或 --update`  update tracked files；提交已被修改和已被删除文件，但是不包括新的文件。

3. `git add -A 或 --all`  add changes from all tracked and untracked files；更新所有改变的文件，即提交所有变化的文件。   

### Git远程仓库

使用目的：备份、实现代码共享集中化管理。![image-20190519160908979](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git7.png)

#### 克隆操作

将远程仓库（github对应的项目）复制到本地：`git clone 仓库地址`

> 仓库地址在 `clone or download` 按钮下取得

#### 将本地仓库同步到远程仓库

使用命令：`git push`

> 如果`git push`出现`The requested URL returned error：403 Forbidden while accessing`问题如何解决？
>
> ![image-20190519164230168](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git8.png)

