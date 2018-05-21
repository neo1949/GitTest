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
