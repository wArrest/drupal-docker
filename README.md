### 说明
1. 首先不太建议开发环境用docker跑。不是很方便，同步的项目太多，其他环境不知道，在macOs下网站加载速度会非常慢。
2. 建议本地直接安装drupal console，直接部署。
```
composer global require drupal/console:@stable
echo "PATH=$PATH:~/.composer/vendor/bin" >> ~/.bash_profile
drupal server
```
3. 等项目在本地已经开发完毕，便可以使用该项目进行部署上线。
### 步骤

1. 将本项目的docker文件夹还有docker-compose.yml移到你的项目根目录下
2. 同步一份composer.json到./docker/drupal下
3. 配置数据库信息(默认账户密码为default)，drupal网站填写数据库连接信息时，用docker的内网名
例如：drupal-db:3306
或者你也可以直接填写你本地的数据库
4. 
```
docker-compose up -d
```
5. 访问127.0.0.1:9002         
### enjoy it!
