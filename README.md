1.什么是git?

	个人理解:分布式版本控制系统

2.集中式和分布式？

	集中式就是都是从主服务器获取，提交也是到主服务器上，下次工作的时候也是到主服务器上获取下来.
	缺点就是必须要联网，否则无法更新下来工作.

	分布式就是每个人的电脑都有一个自己的版本库，你提交更新的时候就提交到自己电脑上就行了.
	不需要联网，当有网络的时候，你再把它推送到远程仓库里去就行。
		
3.git安装？

	参考文档:
	https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/00137396287703354d8c6c01c904c7d9ff056ae23da865a000

4.git版本库的创建？

	1.首先在自己电脑上建立一个目录。

	2.git init 把这个目录变成可管理的仓库。

	3.git add filename 表示将那个文件先加入到暂存区。

	4.git commit -m "" 表示将暂存区的文件提交到本地版本库里。

5.修改版本文件并提交

	git add  加入暂存区

	git commit  提交到版本库

	git log  历史记录

	git log --pretty=oneline 记录一行显示,提交记录结构更直观些
6.版本回退
	git reset --hard commit_id(回退编号) 将版本回退到那个版本号之前

	git reflog 命令记录，有助于你确定要回到未来的哪个版本。

	
7.工作区和暂存区
	工作区：就是你的项目目录.

	暂存区：就是你就是你奖需要提交的东西先添加进的区域(需要提交的文件修改通通放到暂存区，然后，一次性提交暂存区的所有修改).

8:如何提交多次修改

	第一次修改 -> git add -> 第二次修改 -> git add -> git commit(每次修改，如果不add到暂存区，那就不会加入到commit中).

9:撤销修改
	git checkout -- file 让这个文件回到最近一次git commit或git add时的状态(其实就是将我在工作区所做的全部撤销掉，不要了).

10.删除文件
	git rm file. 

	git commit -m "" 先删除文件,在提交.

11.创建合并分支

	分支:每次提交，Git把它们串成的一条时间线，这条时间线就是一个分支.

	查看分支:git branch

	创建分支: git branch <name> 

	切换分支: git checkout <name>

	创建并切换到某分支: git chechout -b <name>

	将某分支合并到当前分支:git merge <name>

	删除某分支: git branch -d <name>


12.冲突解决

	当多个分支都提交同一处时，有可能会产生冲突

	到冲突页面去手动解决冲突

	然后添加，提交，删除无用分支等

	git log --graph --pretty=oneline --abbrev-commit 查看分支合并情况
	




