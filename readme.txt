#http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
$ mkdir learngit
$ cd learngit
$ pwd  //pwd命令用于显示当前目录
git init
git add readme.txt
git commit -m "create readme.txt"
git status //查看工作区的状态
git diff readme.txt
git reset --hard <head^或commit_id或head~100>
git log //穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
git reflog //要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。
# 理解暂存区
