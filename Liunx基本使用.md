Liunx基本使用

sudo rm -r -f 文件夹名 删除包含文件的文件夹
rm -rf 文件名  删除文件(清空文件夹)

Linux反选删除文件

最简单的方法是
# shopt -s extglob      （打开extglob模式）
# rm -fr !(file1)
 
如果是多个要排除的，可以这样：
# rm -rf !(file1|file2) 

find / -name "*.mp3" |xargs rm -rf

find . -name 'download_url.txt' |xargs rm -rf当前目录下
find . -name ‘*.mp4’ |xargs rm -rf


pkill -f "process_name_pattern"  Linux下根据进程的名字杀死进程

查看端口
lsof -i :端口 
kill -9 PID  杀掉端口

生成并复制
cp config/index.js.example config/index.js

Wget 下载