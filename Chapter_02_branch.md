# git branch

## 查看分支
1.查看所有分支信息
```
git branch -a
```

2.查看所有本地分支
```
git branch
```

3.查看所有远程分支
```
git branch -r
```


## 创建分支
1.创建分支
```
git branch branch_name
```

2.切换到指定分支
```
git checkout branch_name
```

3.创建分支并切换到指定分支
```
git checkout -b branch_name
```

4.将本地分支推送远程仓库
```
git push origin branch_name
```


## 删除分支
1.删除本地分支
```
git branch -d branch_name
```

2.强制删除本地分支
```
git branch -D branch_name
```

3.删除远程仓库的分支
```
git push origin --delete branch_name
```

官方文档对这个命令有一段说明：基本上这个命令做的只是从服务器上移除这个指针。Git 服务器通常会保留数据一段时间直到垃圾回收运行，所以如果不小心删除掉了，通常是很容易恢复的。

网上还介绍了一种删除远程分支的方法：
```
git push origin :branch_name
```
这种方式也可以删除远程仓库里分支，但是官方没有介绍这种方式，是否会保留数据未知，所以如果误删除了某个分支，可能无法恢复数据，因此不推荐使用该命令，用上面官方介绍的命令即可。
