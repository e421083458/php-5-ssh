#### 操作步骤 ####
- 编写Docker文件，继承php:5-apache，详细参见文件: https://github.com/e421083458/php-5-ssh/blob/master/Dockerfile
- git clone git@github.com:e421083458/php-5-ssh.git 
- cd php-5-ssh 
- docker build -t e421083458/php-5-ssh . 
- docker run -it -p888:80 -p228:22 --link loving_bassi:docker_mysql -v - /Users/niuyufu/docker/lamp/www/:/var/www/html/ e421083458/php-5-ssh 

####测试使用####
- ssh登陆： ssh root@127.0.0.1 -p228
- Mysql扩展测试：http://127.0.0.1:888/mysql.php

