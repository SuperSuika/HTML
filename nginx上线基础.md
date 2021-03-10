# React项目简单的云服务器上线

## React项目路径 npm build

## 登录云服务器
    ssh 用户名@地址
    若电脑之前登录过，云服务器重置系统之后需要重置。ssh-keygen -R地址

## 上传build文件夹
    scp -r ~/React/my-app/build 用户名@地址:/usr/local/React/
    上传文件夹需要使用到-r

## 安装nginx
    Centos7：
    1. 下载ngin依赖
    wget  http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm
    2. 安装依赖
    rpm -ivh nginx-release-centos-7-0.el7.ngx.noarch.rpm
    3. 安装nginx
    yum install nginx  
    4. 启动并开机自启动
    systemctl start nginx.service  
    systemctl enable nginx.service

## nginx基础设置
    nginx -t 可以找到配置文件的地方
    nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
    nginx: configuration file /etc/nginx/nginx.conf test is successful

    nginx.conf，这是一个主配置文件
    conf.d，这是一个文件夹，里面包含着服务器的独立的配置文件
    因此打开conf.d，在里面创建服务器配置文件builder.conf(前缀自己定)：
    server {
        listen      80;
        server_name xx.xx.xxx.xxx;(自己的服务器IP)

        location / {
            root    /usr/local/React/build;(自己上传的build位置)
            index   index.html index.htm;
        }
    }
    配置好之后，重载一下nginx配置
    nginx -s reload
    systemctl stop nginx
    systemctl start nginx





