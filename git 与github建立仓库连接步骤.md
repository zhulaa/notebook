## git 与github建立仓库连接步骤
#### 一、先对git进行用户设置
下载git软件并安装
建立本地仓库：在git bash里进行用户名和邮箱设置

> git config --global user.name "用户名" (回车)
> git config --global user.email "邮箱" (回车)

#### 二、本地仓库
准备工作和仓库的建立（用指令）（bash中）

> cd E:                                       (打开E盘)
> cd MyGit                                (打开MyGit文件夹)
> mkdir learningCode            (创建一个learningCode的文件目录)
> cd learningCode                  (打开learningCode文件夹)
> pwd                                        (显示当前目录)
> git init                                     (将learningCode变成本地仓库)

此时手动打开刚刚的文件夹，会发现一个.git的文件夹，一般这个文件夹是隐藏的，如果你没有看见这个文件夹，不要着急，设置一下文件查看属性就好了，步骤如下：找到**工具栏->文件夹选项->查看->高级设置里面的隐藏文件和文件夹，选择显示隐藏的文件、文件夹和驱动器。**
设置之后，.gti文件就显示出来了。注意了，这个文件夹就是我们的本地仓库，是git用来管理跟踪的，千万不要乱动这里面的问价，否者，git仓库就会被破坏。

#### 三、github的远程仓库建立
1.生成密钥对
> ssh-keygen -t rsa -C "邮箱"  (回车，提示输入密码时建议输入密码。)

2.查看生成的公钥
> cat ~/.ssh/id_rsa.pub

3.复制公钥
> clip < ~/.ssh/id_rsa.pub

4.登录github网址，个人账户，settings，SSH and GPG keys
New SSH key ,复制公钥命名，确定。

