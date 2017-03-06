--- 
#1.git init
git init 初始化git
git branch 查看当前分支
git branch company 新建company分支
git checkout company 切换到company分支
git checkout -b home 新建home分支并且切换到home分支
git merge:先切换到master分支，git merge company 将company的分支代码合并过来
git branch -d company 删除company分支
git branch -D company

---
#2.---ssh--------
终端输入ssh,检测是否安装ssh
如果已经安装,输入:ssh-keygen -t rsa --指定rsa算法生成秘钥，连续三个回车，生成两个文件id_rsa和id_rsa.pub,一个公钥，一个秘钥，
这个两个文件的位置在Linux/Mac:~/.ssh下，win:/c/Documents and Settings/username/.ssh下。
---
#3.GitHub添加ssh key.
1.GitHub的setting页面中的SSH and GPG keys,点击NEW SSH KEY,在key的一栏把id_rsa.pub公钥文件内容复制进去，点击add SSH key就ok了。
2.测试成功与否:输入ssh -T git@github.com 测试，有个人信息就说明ok了.
--- 
#4.Push & Pull
1.push:推，将本地推到远程仓库，保持同步　
    eg:git push origin master 将本地推到远程master分支
  pull:拉，如果别人提交代码到远程，你需要拉取最新代码类似svn up,保证同步。
    eg:git pull origin master ,在push之前先pull,不容易冲突.
---
#5.提交代码
方法1:clone自己的项目，修改添加完之后，进行commit 之后git push origin master.
方法2:
    step1:在github上建一个test项目
    setp2:把本地test2项目与github上的test进行关联，切换到test2目录，执行git remote add origin git@github.com:stormzhang/test.git
        --- 添加一个远程仓库，地址是xxxxxx,origin 是给这个项目的远程仓库起的名字。
git remote -v 查看当前项目有那些远程仓库，接下来就可以想远程仓库进行代码提交了:git push origin master.
提交之前需要设置用户名和邮箱:
git config -global user.name "weixuefeng"
git config -global user.email "18735404398@163.com"
