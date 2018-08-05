使用docker-compose开发django应用时，一般需要使用一下几个容器
web： 应用程序服务器
nginx： nginx服务器（开发时可以不用，实际部署时加上）
postgres： 数据库服务器（没有使用volume，数据直接保存在容器中，如果需要重建容器需要将数据备份）


初始化脚本：
docker-compose build
docker-compose run --rm web django-admin startproject mysite .
docker-compose up

其他脚本
docker-compose run --rm web python manage.py startapp myapp
docker-compose run --rm web python manage.py makemigrations
docker-compose run --rm web python manage.py migrate
docker-compose run --rm web python manage.py createsuperuser
docker-compose run --rm web python manage.py collectstatic