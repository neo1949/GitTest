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

5.在文件 TestIssue2 继续添加一些内容按照下面的操作进行：
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   TestIssue2.md
$ git add .
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   TestIssue2.md
$ git commit --amend
[master 2ed25e3] add TestIssue2.md for test
 Date: Wed May 23 15:27:48 2018 +0800
 1 file changed, 26 insertions(+)
 create mode 100644 TestIssue2.md
$ git merge issue2
[master 2ed25e3] add TestIssue2.md for test
 Date: Wed May 23 15:27:48 2018 +0800
 1 file changed, 26 insertions(+)
 create mode 100644 TestIssue2.md
```

可以看到发生了冲突。
