# 配置alias
st = status  
co = checkout  
cm = commit  
br = branch  
lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit  
dt = difftool  
mt = mergetool  

# 本地操作
`git add -u` 所有tracked文件中被修改过或已删除文件的信息添加到暂存区  
`git add -A` 所有tracked文件中被修改过或已删除文件和所有untracted的文件信息添加到暂存区  
`git branch -d <本地分支名>` 删除分支  

# 远程操作
`git remote -v` 显示远程主机url  
`git remote show <主机名>` 显示远程主机详细信息  

`git clone -b <远程分支名> url` clone远程指定分支  

`git push <远程主机名> <本地分支名>:<远程分支名>`  
`git push origin master`  本地master分支推送到远程主机origin  push后加-u表示本地master和远程master关联  
`git push origin :master` 等同于 git push origin --delete master  

`git fetch origin master` 从远程主机origin的master分支下载最新的版本到本地分支origin/master(不强制合并有冲突的信息)  
`git fetch origin branch1:branch2`  使用远程branch1分支在本地创建branch2(不切换)，不存在branch2则自动创建  

`git pull <远程主机> <远程分支>:<本地分支>`  fetch and merge  

`git log -p master..origin/master` 比较本地master分支和远程分支的差别  
`git merge origin/master` 在当前分支上合并远程分支  

# github ssh
`ssh-keygen -t rsa -C "xxx@yyy.com"`

# 网络资源
[常用命令](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)  
[配置1](https://blog.csdn.net/ylyuanlu/article/details/12583503)  
[配置2](https://blog.csdn.net/yuxin6866/article/details/74835735)  
