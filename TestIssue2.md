测试合并分支存在冲突时如何解决问题。

1.新建分支
```
git checkout -b issue2
```

2.解决问题：这里以提交一个文件作为测试
```
touch TestIssue2.md
```

3.将文件提交到仓库
```
gti add TestIssue2.md
git commit -m "add TestIssue2.md for test"
```

4.切换回主分支，将 issue2 分支合并到主分支上
```
git checkout master
git merge issue2
```
此时应该一切操作正常。

5.在文件 TestIssue2 继续添加一些内容后再执行 merge 操作：
