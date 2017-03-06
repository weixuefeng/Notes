git init 初始化git
git branch 查看当前分支
git branch company 新建company分支
git checkout company 切换到company分支
git checkout -b home 新建home分支并且切换到home分支
git merge:先切换到master分支，git merge company 将company的分支代码合并过来
git branch -d company 删除company分支
------ssh--------
终端输入ssh,检测是否安装ssh
如果已经安装,输入:ssh-keygen -t rsa --指定rsa算法生成秘钥，连续三个回车，生成两个文件id_rsa和id_rsa.pub,一个公钥，一个秘钥，
这个两个文件的位置在Linux/Mac:~/.ssh下，win:/c/Documents and Settings/username/.ssh下。
---GitHub添加ssh key.
1.GitHub的setting页面中的SSH and GPG keys,点击NEW SSH KEY,在key的一栏把id_rsa.pub公钥文件内容复制进去，点击add SSH key就ok了。
2.测试成功与否:输入ssh -T git@github.com 测试，有个人信息就说明ok了.
