## 常用命令

### 全局和当前仓库配置

```
git config --global user.name ''
git config --global user.password ''
git config --local
git config --global --list
git config -unset --global 要删除的配置项
```

```
git status 
git add 
git add -A
git add 文件1 文件2 文件3
git commit
```

### diff

比较工作区和暂缓存区的差异

```
git diff
git diff 文件
git diff --cached
git diff --cached 文件
git diff HEAD 文件
```

### checkout

将工作区指定文件转换成和暂存区一致

```
git checkout 文件
```

### reset

将暂存区指定文件恢复成和HEAD一致

```
git reset 文件
git reset --hard
```

### 查看哪些文件没有被Git管控

```
git ls-files --others
```



### stash

将未处理完的变更先保存到stash中

```
git stash

```

临时任务处理完后继续之前的工作

pop不保留stash

```
git stash pop
git stash apply
```

查看所有的stash

```
git stash list
```

取回某次stash的变更

```
git stash pop stash@{1}
```



```
git add .
git commit --amend
```

## 分支操作

### branch

-v 查看当前工作分支及本地分支

-av 本地和远端

-rv 远端

```
git branch -v
```

基于当前分支创建新分支

```
git branch 新分支
```

基于指定分支创建新分支

```
git branch 新分支 指定分支
```

切换到分支

```
git checkout 指定分支
```

基于某个commit创建分支

```
git branch 新分支 某个commit的id
```

创建并切换到该分支

```
git checkout -b 新分支
```

删除本地某分支

-d 安全

-D 强行

```
git branch -d 要删除的分支
```

删除已合并到 master 分支的所有本地分支

```
git branch --merged master | grep -v '^\*\| master' | xargs -n 1 git branch -d 
```

删除远端origin已不存在的所有本地分支

```
git remote prune orign
```

将A分支合入到当前分支中且为merge创建commit

```
git merge A分支
```

将A分支合入到当B分支中且为merge创建commit

```
git merge A 分支 B分支
```

将当前分支基于B分支做rebase,以便将B分支合入到当前分支

```
git rebase B分支
```

将A分支基于B分支做rebase，以便B分支合入到A分支

```
git rebase B分支 A分支
```

## 变更历史

### log

```
git log --oneline
git log -n
git log --oneline --graph -all
git log 文件
```

某文件各行最后修改对应的commit以及对应作者

```
git blame 文件
```

## 标签操作

### tag

查看已有标签

```
git tag
```

新建标签

```
git tag v1.0
```

新建带备注标签

```
git tag -a v1.0 -m '备注'
```

给指定的commit打标签

```
git tag v1.0 commitid
```

推送一个本地标签

```
git push origin v1.0

git push origin --tags
```

删除一个本地标签

```
git tag -d v1.0
```

删除一个远端标签

```
git push origin :refs/tags/v1.0
```

## 远端交互

产看所有远端仓库

```
git remote -v
```

添加远端仓库

```
git remote add url
```

删除远端仓库

```
git remote remove 名称
```

重命名远端仓库

```
git remote rename 旧名称 新名称
```

将远端所有分支和标签都变更都拉到本地

```
git fetch remote
```

把远端分支的变更拉到本地，且merge到本地分支

```
git pull origin 分支名
```



删除远端分支

```
git push remote --delete 远端分支名
```





