Linux系统UOS SP1上搭建go/golang开发环境
===========================


例子中的版本:

go版本：go1.13.4.linux-amd64.tar.gz

golang版本：goland-2019.2.3.tar.gz


go官网下载链接：https://dl.google.com/go/go1.13.4.linux-amd64.tar.gz

golang官网下载链接：https://www.jetbrains.com/go/download/other.html


## go环境配置

### 下载并解压

	# cd /usr/local/
	# sudo wget https://dl.google.com/go/go1.13.4.linux-amd64.tar.gz
	# sudo chomd +x go1.13.4.linux-amd64.tar.gz
	# sudo tar -C /usr/local -zxvf go1.13.4.linux-amd64.tar.gz

### 配置环境变量

注：在uos系统上，配置到/etc/profile，只在当前终端生效，重开终端，不生效;
可以配置到这里：全局配置到/etc/bash.bashrc，用户环境变量配置到~/.bashrc

	export GOROOT=/usr/local/go
	export PATH=$PATH:$GOROOT/bin
	或
	export PATH=$PATH:/usr/local/go/bin

永久全局环境变量：将以上内容添加到/etc/bash.bashrc中

	# sudo vim /etc/bash.bashrc
	# source /etc/bash.bashrc

### 查看版本和验证

	# go version
	# go env

### 代码编写/编译/执行

	# cd ~/workspace/code/system/go/
	# ls
	# vim hello.go 
	# go build hello.go 
	# ./hello 

## Golang安装和配置

### 下载并解压

	# cd /usr/local/
	# sudo chomd +x goland-2019.2.3.tar.gz
	# sudo tar -C /usr/local -zxvf goland-2019.2.3.tar.gz

### 运行

	# cd GoLand-2019.2.3/bin/
	# ./goland.sh

### 破解汉化

参考：http://c.biancheng.net/view/6124.html

	# cp ~/workspace/tools/Goland破解+汉化补丁/jetbrains-agent.jar .
	# sudo chmod +x jetbrains-agent.jar 
	# ls
	# vim goland64.vmoptions
	# vim goland.vmoptions 
	# ./goland.sh
	# sudo chmod +x go*
