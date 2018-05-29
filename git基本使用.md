git基本使用
git checkout -b dev  创建
删除本地分支
$ git branch -d <BranchName>
获取远程分支到本地并创建
git fetch origin 远程分支名x:本地分支名x

git blame src/views/specialist/grade.vue 查看该文件那些人修改过

git diff查看修改

git checkout .撤销没有git add之前的

git reset 文件 撤销git commit之前git add之后

 git revert commit_id 撤销git commit之后


git push origin --delete DEV  删除远端分支

git push origin dev:dev  推送本地分支到远程分支


git fetch upstream
git merge upstream/master

删除本地和远程库关联
git remote remove origin

关联远程仓库
git remote add origin https://github.com/yangyuan02/yuejuan_app.git

git push -u origin master  第一次推

ssh相关
[ssh生成key博客](https://gist.github.com/yisibl/8019693)

###如何创建公钥

```
首先启动一个Git Bash窗口（非Windows用户直接打开终端）

执行：

cd ~/.ssh

如果返回“… No such file or directory”，说明没有生成过SSH Key，直接进入第4步。否则进入第3步备份!

备份：

mkdir key_backup mv id_isa* key_backup

生成新的Key：（引号内的内容替换为你自己的邮箱）

ssh-keygen -t rsa -C "your_email@youremail.com"

输出显示：

>Generating public/private rsa key pair. Enter file in which to save the key 
(/Users/your_user_directory/.ssh/id_rsa):<press enter>
直接回车，不要修改默认路劲。

>Enter passphrase (empty for no passphrase):<enter a passphrase>
Enter same passphrase again:<enter passphrase again>
设置一个密码短语，在每次远程操作之前会要求输入密码短语！闲麻烦可以直接回车，不设置。

成功：

Your identification has been saved in /Users/your_user_directory/.ssh/id_rsa. Your public key has been saved in /Users/your_user_directory/.ssh/id_rsa.pub. The key fingerprint is: ... ...

提交公钥：

6.1 找到.ssh文件夹，用文本编辑器打开“id_rsa.pub”文件，复制内容到剪贴板。

6.2 打开 https://github.com/settings/ssh ，点击 Add SSH Key 按钮，粘贴进去保存即可。


```

ssh-add -K ~/.ssh/id_rsa  提交免输入密码

cat ~/.ssh/id_rsa.pub

pbcopy < ~/.ssh/id_rsa.pub

rm -rf .git  删除git 重新初始化

…or create a new repository on the command line
本地库与远程库关联

echo "# node-download-img" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/yangyuan02/node-download-img.git
git push -u origin master
…or push an existing repository from the command line

git remote add origin https://github.com/yangyuan02/node-download-img.git
git push -u origin master

echo "node_modules/" >> .gitignore

Mac下采用zsh代替bash
https://www.jianshu.com/p/ae378aa725cf

Commit message 的格式