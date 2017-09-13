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



