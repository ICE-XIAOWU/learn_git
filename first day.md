## 1. 本地设置用户名和邮箱
$ git config --global user.name "Firstname Lastname"  
$ git config --global user.email "your_email@example.com"  

## 2. SSH
#### 2.1 创建SSH Key
$ ssh-keygen -t rsa -C "your_email@example.com" Generating public/private rsa key pair.  
Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa): 按回车键   
Enter passphrase (empty for no passphrase): 输入密码   
Enter same passphrase again: 再次输入密码  
#### 2.2 输入密码后会出现一下截图
![image](https://raw.githubusercontent.com/ICE-XIAOWU/picxImg/master/picxImg/image.6bwmlm3ntd80.webp)

#### 2.3 在github上添加了ssh公开的密钥使用以下命令进行测试
$ ssh -T git@github.com

#### 2.4 成功之后出现以下命令
Hi hirocastest! You've successfully authenticated, but GitHub does notprovide shell access.

## 3. 创建仓库的时的问题
#### 3.1 add.gitignore
这个设定会帮我们把不需要在 Git 仓库中进行版本管理的文件记录在 .gitignore 文件中，省去了每次根据框架进行设置的麻烦。下拉菜单中包含了主要的语言及框架，选择今后将要使用的即可。
#### 3.2 license
如果这个仓库中包含的代码已经确定了许可协议，那么请在这里进行选择。随后将自动生成包含许可协议内容的 LICENSE 文件，用来表明该仓库内容的许可协议。
## 4. git初使用
#### 4.1 克隆仓库到本地
git clone git@github.com:用户名/仓库名
##### 完成出现以下命令
Cloning into 'Hello-World'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0) Receiving objects: 100% (3/3), done.
##### 4.2 查看状态
git status
当文件还没被添加到仓库中时，会出现Untracked filesd的提示
##### 4.3 提交
###### 4.3.1 git add
git add命令会将文件加入到暂存区
###### 4.3.2 git commit
git commit命令将文件进行提交到本地（疑惑）
##### 4.4 git push
git push将文件提交到github
