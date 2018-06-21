# studydaymsg
每日学习笔记

Centos linux 操作系统服务器
Nodejs 环境装配：
Cmd:  wget  https://npm.taobao.org/mirrors/node/v10.2.0/node-v10.2.0-aix-ppc64.tar.gz
下载文件
		tar -xf node-v6.10.1-linux-x64.tar   解压文件
		mv node-v6.10.1-linux-x64 node-v6.10.1  更名文件
		ln -s /root/node-v6.10.1/bin/node /usr/local/bin/node  配置node
ln -s /root/node-v6.10.1/bin/npm /usr/local/bin/npm	  配置npm
安装express 模板程序：
	Npm install express –global
	Npm install express-generator –global

使用linux 框架命令：epel的方法 安装
	sudo yum install epel-release  
	sudo yum install nodejs
	sudo yum install npm --enablerepo=epel
	sudo npm install -g express
	sudo npm install -g express-generator

// 首选需要查找运行在8888端口上的进程id
sudo lsof -i:端口
// 然后使用这个命令杀死进程
sudo kill -9 ID

热更新模块：
	Npm install supervisor –global

PM2应用程序启动进程保持：
npm install pm2 -g 
pm2启动：
pm2 start "/usr/local/src/node/bin/npm" --name "law" -- start .

pm2 list		列表
pm2 stop    停止
pm2 restart 重启
pm2 delete  删除
pm2 reload all 热更新

在www文件下配置端口号


多个域名指向不同服务器文件夹需要安装模块：
https://blog.csdn.net/yougoule/article/details/78186138

未解决：多域名指向不同文件，待定
