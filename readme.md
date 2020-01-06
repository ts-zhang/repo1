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
