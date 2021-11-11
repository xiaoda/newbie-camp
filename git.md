# Git

## [基础命令](https://lexiangla.com/docs/9ff25c1c0bce11ec865c1e2e701dac04?company_from=385abcf0dd9d11e8a11752540005f435)[【备用链接】](https://fe.anchnet.com/2021/Git%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4%E6%B1%87%E6%80%BB/)
### git clone
克隆仓库

### git pull / git fetch
拉取代码

### git diff / git diff --staged
查看代码修改

### git add . / git add xxx
添加到暂存区

### git commit -m '解决 xxx 问题'
提交代码

### git push
推送代码

## 分支使用
### git checkout xxx / git checkout -b xxx
切换分支

### git merge xxx
合并分支

### git rebase xxx
另一种合并分支的方式：Reapply commits on top of another base tip.

## 解决冲突
经过沟通保留双方需要的代码片段

## 回滚版本
### git reset --hard xxx
回滚到之前的某个版本

### git revert xxx
撤销某一次提交

## .gitignore
gitignore 的作用是帮助我们在执行 git add 时将我们指定的一些文件自动排除在外，不提交到 Git 当中。

```
node_modules
/dist
/.idea
.DS_Store
```
