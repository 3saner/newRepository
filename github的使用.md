1. 登录github。

2. 点击右上角的new repository（新的仓库）。![1651384185140](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651384185140.png)

   

   3.创建仓库![1651384482052](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651384482052.png)

4.生成公钥

```
$ cat ~/.ssh/id_rsa.pub
查看公钥
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCeaETgaAj3c8upYdjrDkh4TJF3hHN675Ll+wks82t2FQ+uK84itmEhmOvzsSvTxNfL4A0MZ4TS3S25IM2tGmALaenWcM+dlAtq74btMbCukzTrDQlDdWkDpMrZo0VFjGRzlODpNcHerhq5Jdv7Hf+N3/EOsqOQrMgiKL3pYKf/vhXkfxaoHMX27CehXcyCzYNoQ9f2146M5EI0RzPJQ2D+e8BdsOgCELJUQ3CrfZKVGhglzqfAO1mX4cOcqQtxposrNUAnNG+AkUVLuxUn4aoJq2WlwYAVcNMuzSqIFNOunp9yYa0OewR7nK+f7kLsTdYi2eh+UQA/GceOVayA8AvYvfk8FpPoHFi2Joorllbohjk0JT0sv3GPPstir3SdZQ4QLyscggrcmiLQW5Ju1M1km6c4/HZfYvy4cHRp4aRCDKVskchk3NOmtLbyAOYKN90JipsqDlNl//81r/n/+i85bL7f0dfOWEHTRmZWK4+9gTH7uVg3+WPq0moUsn6EO9U= 610886002@qq.com

```

5.设置公钥在github里面

点击settings

![1651385272912](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651385272912.png)

点击SSH

![1651385558627](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651385558627.png)

输入点击添加

![1651385696996](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651385696996.png)

添加完成

![1651385725020](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651385725020.png)

将本地与远程git仓库链接

1.打开终端初始化 git init,生成.git文件

![1651385938979](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651385938979.png)

2.存入本地

![1651386082830](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651386082830.png)

3.添加到历史区

![1651386156548](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651386156548.png)

4.和远程关联

![1651386233908](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651386233908.png)

放到远程仓库主分支

![1651387337559](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651387337559.png)

成功连接

![1651387525483](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1651387525483.png)

5.当一堆人开分一个项目的时候，注意不要在主分支master上开发。防止冲突。

5-1.新建分支 git branch 分支名称   比如：git branch dev4.0

5-2.从主分支跳到创建的分支上：git checkout 分支名称

比如：git checkout dev4.0

5-3.在新建一个分支：git branch feature-login

5-4.进到这个新建的分支：git checkout feature-login

5-5.开发完成之后。先加暂存区，在加历史区，

5-6.开发完成之后，跳到dev4.0分支上：git checkout dev4.0

5-7.合并开发的分支feature-login。 git merge feature-login



6.注意事项：如果发生了冲突

上来第一件事情就是：把本地的dev删掉。冲突修复完之后，再从master上切换一个分支。

7.删除本地分支：

git branch -d dev