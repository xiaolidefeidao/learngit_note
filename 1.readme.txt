#http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
Git跟踪并管理的是修改，而非文件。每次修改，如果不add到暂存区，那就不会加入到commit中。
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
$ mkdir learngit
$ cd learngit
$ pwd  //pwd命令用于显示当前目录
git init
git add readme.txt
git commit -m "create readme.txt"  //在哪个分支下commit，改变便提交给哪个分支，与在哪个分支时修改或add的文件无关
git status //查看工作区的状态
git diff readme.txt
git diff HEAD -- readme.txt //命令可以查看工作区和版本库里面最新版本的区别
git reset --hard <head^或commit_id或head~100> //版本更改
git log //穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。--graph命令可以看到分支合并图;--pretty=oneline一行显示;--abbrev-commit显示commit_id的缩写
git reflog //要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。
# 理解暂存区
cat readme.txt //读取readme.txt中的文本
git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
总之，就是让这个文件回到最近一次git commit或git add时的状态。
git reset HEAD file //可以把暂存区的修改撤销掉（unstage），重新放回工作区。
git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。
