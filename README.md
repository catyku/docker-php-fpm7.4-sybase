# docker-php-fpm7.4-sybase
docker php-fpm7.4 connect sybase(sqlanywhere)

## 參考此Dockerfile
https://github.com/yappabe/docker-php


### 執行docker
```
sudo docker-compose up -d --build
```
### apache2 需要使用到的VirtualHost上加上
```
ProxyPassMatch ^/(.*\.php(/.*)?)$ fcgi://127.0.0.1:9001/var/www/html/$1
```
