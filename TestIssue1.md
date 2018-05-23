This is file uesd for 'git merge' test.

1.首先新建一个解决 issue1 问题的分支并切换到该分支
```
$ git checkout -b issue1
```

2.在 issue1 分支上解决该问题后再切换回 master 分支
```
$ git checkout master
```

3.合并分支 issue1 到 master 分支
```
$ git merge issue1
Updating aed99ae..9d456f3
Fast-forward
 TestIssue1.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 TestIssue1.md
```

4.解决问题后，你应该先删除 hotfix 分支，因为你已经不再需要它了 —— master 分支已经指向了同一个位置
```
git branch -d issue1
```
