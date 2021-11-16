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

### git status
查看当前状态

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
另一种合并分支的方式：Reapply commits on top of another base tip

### git branch -d xxx
删除分支

## 解决冲突
经过沟通保留双方需要的代码片段

## [代码回滚](https://lexiangla.com/docs/909861520afd11ec8b19568564ad7a16?company_from=385abcf0dd9d11e8a11752540005f435)[【备用链接】](https://fe.anchnet.com/2021/%E6%8A%80%E6%9C%AF%E5%88%86%E4%BA%AB%E4%B9%8BGit%E6%92%A4%E9%94%80%E6%8F%90%E4%BA%A4/)
### git reset xxx / git reset --hard xxx
回滚到之前的某个版本

### git revert xxx
撤销某一次提交

## 其它常用命令
### git config / git config --global
查看或修改 git 配置信息

### git branch / git branch -r
查看或创建分支

### git log
查看提交日志

### git tag
查看或创建标签

### git blame
查看文件修改记录

## .gitignore
gitignore 的作用是帮助我们在执行 git add 时将我们指定的一些文件自动排除在外，不提交到 Git 当中。

```
node_modules
/build
/dist
/.idea
/.vscode
.DS_Store
```

## 注意事项
1. 尽量使用命令行而不是各类工具操作 Git
2. Git 操作出现问题或意料之外的情况时，停止操作、保留命令行并及时向组长/主管求助。
3. git push -f 强制推送很危险，绝大部分时候不允许使用。
4. 在进行有风险、没有把握的操作时，先对分支进行备份。

## 参考资料
1. [git 使用简易指南](https://www.bootcss.com/p/git-guide/)
