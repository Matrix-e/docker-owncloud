# GetNAS docker-owncloud

---
本项目基于 [owncloud:8.2-apache](https://hub.docker.com/_/owncloud/)、[mariadb:10.1](https://hub.docker.com/_/mariadb/)官方镜像，通过docker-compose工具构建使用。

###使用方法

	克隆项目到本地
	$ git clone https://github.com/getnas/docker-owncloud.git
	
	在本地创建数据目录，用于持久保存程序数据。
	$ mkdir apps config data mariadb mariadb/datadir
	
	执行docker-compose命令构建并运行owncloud
	$ docker-compose up -d
	
	浏览器访问 http://your-ip-address:88 执行owncloud程序安装
	
	安装时数据库选择 mysql/mariadb，配置信息如下：
	  主机: mariadb
	  数据库: owncloud
	  账号: root
	  密码: 123456
	  
	管理mariadb数据库请访问 http://your-ip-address:88/adminer.php


###HOST(宿主机)开启启动

	在Linux桌面环境找到启动管理工具，添加新启动项，其中命令部分参考如下：
	
	docker-compose -f /mnt/docker/owncloud/docker-compose.yml start
	
	注：-f 参数后面是项目的 docker-compose.yml 文件绝对路径。

