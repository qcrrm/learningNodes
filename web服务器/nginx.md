## nginx安装

### CentOS

安装gcc  pcre-devel zlib-devel openssl-devel

```
yum -y install gcc pcre-devel zlib-devel openssl openssl-devel
```

下载tar.gz 

```
#解压
tar -zxvf nginx-XXX.tar.gz

cd nginx-XXX
#配置
./configure --prefix=/usr/local/nginx

make
make install
#测试是否成功
./sbin/nginx -t 

启动
./nginx
```

### ubuntu

安装

```
sudo apt-get install nginx 
```

启动

```
service nginx restart
```

配置文件

cd /etc/nginx/nginx.conf

## Nginx基础复习

## 核心配置分析

### 添加ssl配置



## 虚拟主机配置

## Location匹配原则解析

## 日志配置和切割处理

## Rewrite的使用

## 缓存配置及Gzip配置

## 反向代理实战

## 负载均衡配置说明

## 进程模型

## 产栈配置

## Nginx+keepalived实现高可用

## 进程模型

## 配置https请求

