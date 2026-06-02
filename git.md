# git 推荐看蛋老师
### 基础配置:
- 配置库姓名和邮箱
- git config --global user.name "名字"
- git config --global user.email "邮箱"

**config** 是设置的意思,**--gobal**是当前用户(**这个电脑上的所以库都会有效**),**--local**是当前仓库(**只对这个仓库有效**),**--system**是对全系统,一般不用
- git init 初始化
- git status 查看状态,或者看下一步该干什么
- git add 文件名 git add . 这样子把文件添加到暂存区
- git commit 把文件提交到本地仓库, git commit -m "备注名字什么的东西"
- git log 查看版本信息
- .gitignore 不跟踪文件,可以把不想上传的东西丢到里面,就不会被上传了

### 分支:
- git branch abc 创建了一个叫abc的分支,分支命名要按照规则,下面解释
- git branch 查看分支
- git checkout abc 切换到abc分支
- git branch -d abc 删除分支,如果没有合并分支,会有提示
- git branch -D abc 强制删除该分支
- git checkout -b temp 创建一个temp分支,并且转移到该分支
- git commit -a -m "内容" -a是--amend,是给老文件的,如果只修改了文件里的代码,可以图省事直接用,也可以直接-am,可以合在一起写的
- git merge temp 把temp合并到当前分支,如果temp和master都在同一个地方修改了,并且修改成了不一样的东西,就会发生冲突,这时候要自己手动修改

### 上手github!
- 创建仓库自己摸索摸索就欧克欧克
- git clone github链接 拷贝github里的东西
- git remote -v remote是操控远程仓库的意思,-v是-verbose,查看详细信息
- git push 更新,要输入用户名和token,token再github生成
- git fetch 取回,只下载,不合并
- git diff origin/main 远程仓库名和分支名,可以看见远处仓库和分支的区别
- git pull origin/main取回加合并,把远程仓库内容直接整合到工作区,这时候用git log 可以看到所有版本历史
- git push -u origin dev 更新内容,-u是建立绑定,推送到dev分支里