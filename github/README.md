- [git手册](https://git-scm.com/docs)
- [git book](https://git-scm.com/book/en/v2)
# git命令
## git rebase
```
git rebase -i commit_digest
```
squash commit压缩,pick commit保存</br>
git reflog,git reset ref_digest 可以撤销rebase </br>
## git reset
git reset 信息摘要码
不要加把这次修改的本地内容也清除的选项
## 生成公钥
用于https协议
```sh
ssh-keygen -t rsa -C "youremail"
start C:\Users\Admin\.ssh
```
## 加速访问
start C:\Windows\System32\Drivers\etc</br>
增加 ip github.com</br>
ip从工具网站上查找</br>

## git stash基本用法
- [https://www.cnblogs.com/zndxall/archive/2018/09/04/9586088.html]

## git push的用法
- [创建远程分支](https://blog.csdn.net/u012701023/article/details/79222731)
## git merge
- 当前分支合并其他分支内容,如果有冲突,就解决冲突再commit就ok
- git merge --abort
## git pull基本用法
- [link](https://www.cnblogs.com/taohuaya/p/10761799.html) git pull origin master:master 冒号可以省略
## 分支
- 删除分支 git branch -d dev20181018 [删除本地和远程分支](https://www.cnblogs.com/liyong888/p/9822410.html)
- git push origin --delete oldBranchName
- git branch --set-upstream-to origin/newBranchName
