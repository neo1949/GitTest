# 初始化仓库

## 创建本地仓库
### 创建新仓库
1.在本地创建一个新的文件夹：
```
mkdir GitTest
```
本地项目的文件夹名称可以与远程仓库不一致，为了避免混淆，最好保持一致。

2.打开文件夹，初始化仓库：
```
cd GitTest
git init
```

3.将本地仓库与远程仓库相关联：
```
git remote add origin git@github.com:neo1949/GitTest.git
```

4.查看当前仓库的状态
```
git status
```

### 检出仓库
可以通过命令直接克隆远程仓库到本地：
```
git clone git@github.com:neo1949/GitTest.git
```

也可以指定克隆到本地仓库的文件夹名称：
```
git clone git@github.com:neo1949/GitTest.git GitTest2
```
如果不指定克隆仓库的名称，默认使用远程仓库的仓库名称。

从效果来看，检出仓库实际上是通过一个命令完成了创建本地仓库中的1、2、3步骤。


## 配置用户名和邮箱
### 查看配置信息
```
git config --list
```

### 配置用户信息
在使用 Git 正式提交之前需要配置用户名和邮箱，这两条配置很重要，每次 Git 提交时都会引用这两条信息，说明是谁提交了更新，所以会随更新内容一起被永久纳入历史记录。如果之前已经在其它地方配置过用户信息，那么在查看配置信息时会看到类似的配置信息：
```
user.email=you.email
user.name=you.name
```

如果还没有配置过用户信息，通过下面的信息配置用户名和邮箱：
```
git config --global user.name "you.name"
git config --global user.email "you.email"
```

配置完用户信息之后，使用上面查看配置信息的命令可以看到相关配置。

如果使用了 <code>--global</code> 选项，那么更改的配置文件就是位于你用户主目录下的那个，以后你所有的项目都会默认使用这里配置的用户信息。


如果要在某个当前项目中使用其他名字或者电邮，只要去掉 <code>--global</code> 选项或者使用 <code>--local</code> 选项重新配置即可，新的设定保存在当前项目的 .git/config 文件里：

不使用 <code>--global</code> 参数：
```
git config user.name "neo"
git config user.email "neo@qq.com"
```
查看配置信息：
```
user.name=neo
user.email=neo@qq.com
```

使用 <code>--local</code> 参数：
```
git config --local user.name "neo1949"
git config --local user.email "neo1949@qq.com"
```
查看配置信息：
```
user.name=neo1949
user.email=neo1949@qq.com
```

如果我们想撤销本地配置的用户名或邮箱，使用默认的全局配置，只需要通过下面的命令取消本地配置即可：
```
git config --unset user.name
git config --unset user.email
```

再查看本地配置信息的时候，发现刚才的本地用户名和邮箱配置已经没了。

通过上面几部简单的操作，一个本地仓库就创建好了。下次再创建仓库时，默认使用之前配置信息，如果需要修改用户名和邮箱，按照上面的命令操作即可。

更多配置请参考 [起步 - 初次运行 Git 前的配置](https://git-scm.com/book/zh/v1/%E8%B5%B7%E6%AD%A5-%E5%88%9D%E6%AC%A1%E8%BF%90%E8%A1%8C-Git-%E5%89%8D%E7%9A%84%E9%85%8D%E7%BD%AE)。
