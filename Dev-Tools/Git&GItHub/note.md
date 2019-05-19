## 基本概念

**Repository**：仓库，对应一个**git库**用于存放项目代码，每个项目对一个仓库。

**Star**： 收藏

**Fork**：复制克隆一个项目到自己的GitHub中，该fork的项目是独立存在的。

![image-20190519110503099](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/fork.png)

**Pull Request**：基于fork实现，发起合并请求。

![image-20190519110616794](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/pull-request.png)

**Watch**：关注项目，可以接收到项目更新提醒。

**Issue**：事务卡片，发现代码bug，但目前没有成型代码，需要讨论时可用；或者使用开源项目出现问题时使用。

![image-20190519111011396](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/issue.png)



> 私有仓库只能自己或者指定的朋友才有权限操作（收费）。



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



## 使用GitHub

### GitHub主页



### 仓库主页

**Commits**：可以查看每次修改的相关信息，包括删除文件详细信息。

**Issues**：可以进行问题讨论，解决后可以close。



### 个人主页



## Git

> 通过Git管理GitHub托管项目代码。

### 安装



### 使用

#### 基本工作流程

Git工作区域：

1. **Git Repository（Git仓库）**：最终确定的文件保存到仓库，成为一个新的版本，并对他人可见。
2. **暂存区**：暂存已经修改的文件最后统一提交到Git仓库中。
3. **工作区（Working Directory）**：添加、编辑、修改文件等动作。

向仓库中添加文件流程：

![image-20190519145247188](/Users/yuexin/Documents/GitHub/Java-Learning/Dev-Tools/Git&GItHub/image-for-note/git.png)

#### 初始化及仓库创建和操作

基本信息设置

1. 设置用户名 `git config –-global user.name '这里填写自己的用户名'`

2. 设置用户名邮箱 `git config –-global user.email '这里填写自己的用户名邮箱'`
3. 查看设置 `git config --list`

初始化一个新的Git仓库：

1. 创建文件夹

2. 在文件夹内初始化Git（创建Git 仓库）

   命令行进入当前目录，使用 `git init`命令，成功会显示 .git 文件

3. 向仓库中添加文件

