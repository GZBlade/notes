### Git Learn

#### 2017-9-13

##### 错误——上传错误

```shell
git push -u origin master
To github.com:GZBlade/notes.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:GZBlade/notes.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

其根本原因是在远程端已经有了一个README，不是空仓，不能直接push -u

##### 错误——下载错误

 ```shell
git pull 
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master
 ```

及时设置后也会出错



因为两个是没有关联的项目没有-u关联，使用`--allow-unrelated-histories` 参数后便可以愉快地push和pull了。

```shell
$ git push -u origin master
Counting objects: 21, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (11/11), done.
Writing objects: 100% (21/21), 2.31 KiB | 0 bytes/s, done.
Total 21 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), done.
To github.com:GZBlade/notes.git
   a6197d4..7bd995f  master -> master
Branch master set up to track remote branch master from origin.
```

**总结**

从本次悲伤的例子中可以总结出：

1.  在github创建远程仓库的时候，最好什么都不要加，面对搞得很麻烦。
2. 遇见问题的时候，最好沿着错误的提示，对最相似最可能的解决方法进行控制式的尝试，在后来的npm安装webpack的时候遇见了类似的情况。

#### 2017-9-14

##### git远程仓库问题



