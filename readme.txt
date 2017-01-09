git config --list 查看配置信息
git help
mkdir 'resposity path'
cd 'resposity path'
git init  ->生成.git
git add <file> or<./dir/ '文件夹'>
...
git commit -m '提交说明'
git status 可以让我们时刻掌握仓库当前的状态
git diff 查看修改的内容 绿色字体
提交修改
git add      git commit
git log   查看commit信息
git log --pretty=oneline
git reset --hard HEAD^or commit_id 版本回退
git reflog
git diff HEAD -- readme.txt命令可以查看工作区和版本库里面最新版本的区别
git checkout -- file可以丢弃工作区的修改 未commit
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)
git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区
直接丢弃工作区的修改时，用命令git checkout -- file。
添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，第二步按上操作。
撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
git rm用于删除一个文件

添加远程库
1.在GitHub.com 上新建一个repository
2.远程库与本地库关联  git remote add origin git@github.com:muzili314/cmdline.git (origin 远程库的名字)
3.把本地库的所有内容推送到远程库上  git push -u origin master
加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
以后就直接git push origin master
从远程克隆库git clone git@github.com:muzili314/name.git
创建dev分支，然后切换到dev分支 git checkout -b dev
等同于$ git branch dev        (-d 删除分支)
	  $ git checkout dev
git merge命令用于合并指定分支到当前分支
git log --graph命令可以看到分支合并图
git tag