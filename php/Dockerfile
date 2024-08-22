# 使用官方的 PHP 7.2 FPM 镜像
FROM php:7.2-fpm

# 安装 PDO 和 PDO MySQL 扩展
RUN docker-php-ext-install pdo pdo_mysql

# 安装 Redis 扩展
RUN pecl install redis && docker-php-ext-enable redis

# 可选：复制项目文件到容器中
COPY . /var/www/html

# 设置工作目录
WORKDIR /var/www/html
