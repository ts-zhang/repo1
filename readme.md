## git多仓库测试

一份代码提交到repo1和repo2

```
git init
git add .
git commit -m "init"
#添加第一个远程仓库
git remote add repo1 https://github.com/ts-zhang/repo1.git
#添加第二个远程仓库
git remote add repo2 https://github.com/ts-zhang/repo2.git

#将代码提交到repo1仓库的master分支
git push -u repo1 master
#将代码提交到repo2仓库的master分支
git push -u repo2 master
```

如果只执行 ```git push``` 命令，那么代码只会提交到一个仓库中，默认推送的远程仓库为```branch.master.remote```配置中指定的仓库

通过 ```git config --local branch.master.remote``` 命令查看

使用```git config --local branch.master.remote repo1```命令可以配置默认远程仓库地址