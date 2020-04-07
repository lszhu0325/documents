# 配置个人用户名称和电子邮件地址, --systtem为设置系统变量, --global为本用户全局变量, 空为当前项目变量
git config --global user.name "账户"
git config --global user.email "邮箱"

# 在当前文件夹下创建仓库
git init
# 指定文件夹创建仓库
git init 仓库名
# 克隆远程仓库
git clone repository地址
# 克隆远程仓库并指定仓库名
git clone repository地址 仓库名

# 将远程仓库与本地仓库建立连接
git remote add orgin 远程仓库地址

# 增加指定文件到暂存区
git add 文件全名
# 保存修改到暂存区(包括新增文件, 删除文件, 修改文件)
git add .

# 提交保存到暂存区的修改
git commit -m "提交说明"

# 将提交到暂存区的修改隐藏起来
git stash save "暂存标记"
# 弹出最新的隐藏暂存, 不删除
git stash apply
# 查看所有的stash
git stash list
# 恢复指定的暂存, 不删除
git stash apply 暂存标记

# 参看仓库提交记录
git log
# 查看仓库历史版本信息
git reflog
# 回退到指定版本
git reset commit-id
# 回退到指定版本, 修改移动到暂存区
git reset --soft HEAD~1
# 回退到指定版本, 工作区的修改会清空
git reset --hard HEAD~1
# 将指定文件从暂存区回退到工作区
git reset HEAD 文件名
# 将git回退到历史版本并重新提交一次
git revert commit-id

# 创建分支
git branch 分支名
# 切换分支
git checkout 分支名
# 回退工作区的文件修改
git checkout 文件名
# 回退工作区的全部文件修改
git checkout --hard HEAD
# 创建本地分支并与远程分支建立关系
git checkout -b 分支名称 远程分支名称
# 查看本地分支与远程分支的映射关系
git branch -vv
# 查看所有分支
git branch --list
# 删除分支
git branch -d 分支名称
# 删除分支(不管他有没有merge)
git branch -D 分支名称
# 将指定分支合并到当前分支
git merge 分支名
# 将远程仓库更新合并到当前分支
git merge FETCH_HEAD
# 将指定分支合并到当前分支
git rebase 分支名

# 拉取远程分支与本地分支进行合并
git pull orgin 远程分支名:本地分支名

# 将当前分支修改推送到远程分支
git push origin 本地分支名:远程分支名

# 查看所有分支
git branch -a
# 将远程仓库上的所有更新拉取到本地
git fetch 远程主机名
# 将远程仓库指定的分支更新到本地
git fetch 远程主机名 远程分支名
# 合并拉取的最新分支
git merge FETCH_HEAD

# 将当前分支建立追踪关系
git branch --set-upstream-to origin/master

# ********************
# 总结代买提交流程
# 1. 将本地修改提交到暂存区
git add .
# 2. 将暂存区修改隐藏
git stash save "暂存标记"
# 3. 将远程仓库最新提交拉取到本地
git fetch orgin master
# 4. 将远程仓库更新合并到本地, 如遇冲突解决冲突
git merge FETCH_HEAD
# 5. 弹出最新的隐藏暂存, 如遇冲突解决冲突
git stash apply 暂存标记
# 6. 将修改内容提交
git commit -m "提交说明"
# 6. 将本地仓库修改同步到远程仓库, 如遇冲突, 解决冲突后提交再同步
git push origin 本地分支名:远程分支名


