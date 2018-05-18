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