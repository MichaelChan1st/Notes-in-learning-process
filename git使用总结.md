# git使用总结

## 基本步骤

* 首先要知道git和github是不同的，我们最不熟悉的就是git的使用而非github的使用

1. 使用SSH让本地仓库与远程仓库github建立连接，MAC和Linux自带SSH，Window在安装git的时候勾选openSSH就自动安装上了SSH
2. 在本地某个文件夹的目录下使用命令 git init初始化为本地git仓库，对于新进文件夹的文件使用git add去追踪他们，实际上就是放入本地git仓库的缓存区中，然后使用git commit 提交它们，这一步就讲这些文件正式上传到本地git仓库里面了（不然只是在文件夹中）
3. 将本地git仓库与远程具体的库建立联系 git remote add 远程库的别名 [git@github.com](mailto:git@github.com):git_username/repository_name.git，如果不小心添加错了可以通过代码git remote remove 远程库名称 来取消关联

4. 连接之后就可以使用git push 远程库别名 分支名称 命令上传文件到远程的github中了

* 另外一种方式就是直接对远程库迭代更新

1. 在指定的文件夹下使用git clone 远程库地址
2. git pull name master 
3. 对拉取的文件进行更改，然后git add 和git commit
4. 最后git push name master

## 过程中的遇到的问题以及发现

### 遇到的问题

#### 父目录子目录多个.git初始化

1. 在clone一个空的远程仓库时，会提示您clone的是空，实际上是克隆成功的，

   他会把远程仓库的名字也克隆下来，在仓库里面才是git初始化的根目录

   *注意克隆和建立与远程仓库连接还是有区别*

2. 当对本地文件夹clone远程仓库时，会把仓库本地克隆下来，即在本地文件夹里面会出现远程仓库的名称，在这个仓库里面才是git初始化的本地仓库。此时如果你对本地根目录进行git init 就会发生git冲突，导致无法add

#### push时的问题

1. `git push name master`是老版代码，现在变成了`git push origin main`这里的origin和main可以通过查看远程分支的代码检查`git branch -a`
