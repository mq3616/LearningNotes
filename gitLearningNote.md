# git init  
 
* 把当前目录变成git可管理的仓库,之后目录下会有一个.git目录,使用ls -ah可见

# git status  
	
* 可以查看当前仓库的状态(修改,添加,删除)

# git add  
	
* 把一个文件的修改添加到暂存区,加-A,添加所有修改

# git log
	
* 可以查看所有修改的log
* --graph,可以看到分支合并图

# git reset
	
* --hard HEAD^ 表示回退到上一版本,HEAD^^表示上上版本,HEAD~20表示回退到上20个版本
* --hard commitID指定回退到哪个版本

# git checkout
	
* xx,表示切换到xx分支
* -b xx,表示创建并指向xx分支
* --  readme.md,表示撤销文件在工作区的修改,回退到上次commit或add的状态

# git rm 
	
* 在git中删除指定文件,可以通过git checkout -- xx撤销删除xx文件

# git commit
	
* -m “xx”,提交更改,把暂存区的所有内容提交到当前分支

# git push
	
* origin xxx, 推送本地的xxx分支内容到远程origin上的xxx分支(也可以用来推送tag)
* -u origin xxx,第一次推送是加-u,git会把本地的xxx分支内容推送到远程的新xxx分支,并把本地xxx分支和远程的xxx分支关联起来(xxx为要推送到的分支名)
* origin --tags, 推送所有未推送到远程的tag

# git clone git地址
	
* 根据git地址克隆对应的远程库到本地

# git branch
	
* 查看当前所有分支,并显示当前所指向的分支
* -d xx,删除xx分支
* -D xx,强制删除xx分支
* xx,创建xx分支

# git merge 
	
* xx,合并xx分支到当前分支

# git stash
	
* 把工作区暂存起来,之后可以恢复
* list,查看暂存的列表
* apply,恢复上一个暂存,stash内容不删除,也可以恢复到指定暂存
* drop,删除上一个暂存,或删除指定暂存
* pop,恢复上一个暂存,并删除对应stash内容,也可以指定暂存

# git remote
	
* 查看远程分支
* -v, 查看详细信息
* add origin xxx, 将远程库与本地关联,xxx是git地址
* rm origin, 删除已有的远程库

# git pull
	
* 抓取当前分支对应的远程分支上的最新提交,并合并. 如果失败提示”no tracking information”,	说明本地分支和远程分支的链接关系没有创建,	用git branch --set-upsteam branchName origin/branchName

# git tag 
	
* 查看所有标签
* xxx, 当前分支版本打标签xxx,标签在本地(推送到远程标签git push origin v1.0)
* xxx yyy, 在commitID为yyy处,添加标签xxx
* -a yyy -m “xxx”, 指定标签yyy的标签信息
* -d xxx, 删除xxx标签(如果已经推送到远程,本地删除之后还要删除远程, git push origin :refs/tags/xxx或者git push origin --delete tag xxx)

# git show xxx
	
* 查看标签xxx信息

# git .gitignore文件书写规则:
	 
	 # 此为注释 – 将被 Git 忽略
	 *.cs     # 忽略所有 .cs 结尾的文件
	 !ABC.cs  # 但 ABC.cs 除外
	 /BLL     # 仅仅忽略项目根目录下的BLL文件,不包括subdir/BLL
	build/    # 忽略 build/ 目录下的所有文件
	doc/*.txt # 会忽略doc/notes.txt,但不包括doc/server/arch.txt

* 自动生成网站:https://www.gitignore.io
* git官方网站:https://github.com/github/gitignore


	
	


	
	
