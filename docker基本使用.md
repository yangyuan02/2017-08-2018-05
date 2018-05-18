docker基本使用

docker pull alpine

安装镜像 — docker pull 镜像名字

列出镜像 — docker image ls

查看正在运行的容器 docker ps

退出exit

后台运行—docker run -d 镜像名字

删掉容器  docker rm -f 1196d882e87a

进入镜像—   docker run -it nginx bach ssh

映射—docker run -d -p 8088:80 nginx   (-d后台运行 -p端口)

查看日志——docker logs -f 3339e5607627  （容器id）

cmd+k清屏容器

control+c退出日志

docker exec -it 3339e5607627 bash 另一种进入容器

docker run -d -v /Users/admin/test:/usr/share/nginx/html -p 8080:80 nginx:alpine 共享文件夹


docker logs -f jky_api 查看日志
rm tmp/pids/server.pid删除掉，重新down 然后up

git pull
docker-compose run app bundle install
docker-compose run app bin/rails db:migrate
docker-compose down
docker-compose up -d