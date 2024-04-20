# 创建自己的hugo博客

## 1. 环境准备

**操作系统：** Debian12.5(WSL2)

> 我这里使用的是WSL版本的Debian。

除了操作系统之外，我们需要安装搭建hugo项目的依赖，详情可见 [hugo官网](https://gohugo.io/getting-started/quick-start/)

以Debain12.5为例，需要安装go，dart-sass，然后安装hugo

1. 安装go语言

```sh
# 下载Linux的go包
wget https://golang.google.cn/dl/go1.22.2.linux-amd64.tar.gz 
# 解压
tar -zxvf go1.22.2.linux-amd64.tar.gz
# 将解压后的文件夹移动/usr/local
sudo mv go /usr/local/go 
# 将bin路径写入当前用户的./bashrc
cd ~
vim .bashrc
export PATH="$PATH:/usr/local/go/bin"
#刷新.bashrc
source .bashrc
# 查询go版本，能正确显示版本号即可
go version 
```

2. 安装dart-cass

```sh
# 下载dart-cassd
wget https://github.com/sass/dart-sass/releases/download/1.75.0/dart-sass-1.75.0-linux-x64.tar.gz
# 解压
tar -zxvf dart-sass-1.75.0-linux-x64.tar.gz
# 将解压后的文件移动到/usr/local
sudo mv dart-sass /usr/local/
# 将移动后的文件夹路径直接写道.bashrc
cd ~
vim .bashrc
export PATH="$PATH:/usr/local/dart-sass"
# 刷新.bashrc
source .bashrc
```

3. 安装hugo

```sh
# 直接使用apt安装即可
sudo apt-get install hugo
```

## 2. 创建一个新的站点

```bash
hugo new site new_site_name
```

## 3. 下载LoveIt主题，参考LoveIt文档创建网站

[LoveIt](https://hugoloveit.com/zh-cn/)

## 4. 将public下的文件放在nginx服务器的nginx文件夹下的html文件夹下

## 5. 直接访问即可

