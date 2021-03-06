# 服务启停

使用由Websoft9提供的 BT 部署方案，可能需要用到的服务如下：

### BT 启停

通过控制台，启动和关闭 BT 面板  

![](http://libs.websoft9.com/Websoft9/DocsPicture/zh/btlinux/bt-disablebt-websoft9.png)

或运行命令

```shell
sudo service bt start
sudo service bt stop
sudo service bt restart

## 删除（慎用）
service bt stop && chkconfig --del bt && rm -f /etc/init.d/bt && rm -rf /www/server/panel
```


### Apache

```shell
##For Ubuntu&Debian
sudo systemctl start apache2
sudo systemctl stop apache2
sudo systemctl restart apache2
sudo systemctl status apache2

##For Centos&Redhat
sudo systemctl start httpd
sudo systemctl stop httpd
sudo systemctl restart httpd
sudo systemctl status httpd
```


### Nginx

```shell
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```

### PHP-FPM

```shell
systemctl start php-fpm
systemctl stop php-fpm
systemctl restart php-fpm
systemctl status php-fpm
```

### MySQL&MariaDB

```shell
sudo systemctl start mysql
sudo systemctl stop mysql
sudo systemctl restart mysql
sudo systemctl status mysql
```