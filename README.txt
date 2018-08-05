使用docker-compose开发django应用时，一般需要使用一下几个容器
web： 应用程序服务器
nginx： nginx服务器（开发时可以不用，实际部署时加上）
postgres： 数据库服务器


初始化脚本：
docker-compose build
docker-compose run --rm web django-admin startproject mysite .
docker-compose up
