git config --list 查看配置信息
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