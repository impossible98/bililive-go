## 开发环境搭建（linux系统）
```
一、环境准备
  1. 前端环境
    1）前往https://nodejs.org/zh-cn/下载当前版本node（18.12.1）
    2）命令行运行 node -v 若控制台输出版本号则前端环境搭建成功
  2.后端环境
    1)下载golang安装 版本号1.19
      国际: https://golang.org/dl/
      国内: https://golang.google.cn/dl/
    2)命令行运行 go 若控制台输出各类提示命令 则安装成功 输入 go version 确认版本
  3.安装 ffmpeg (以centos7为例)
    1) yum install -y epel-release rpm
    2) rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7
    3) yum repolist
    4) rpm --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro
    5) rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-1.el7.nux.noarch.rpm
    6) yum repolist
    7) yum install -y ffmpeg
二、克隆代码并编译(linux环境)    
   1. git clone https://github.com/hr3lxphr6j/bililive-go.git
   2. cd bililive-go
   3. make build-web
   4. make 
三、linux编译其他环境(以windows 为例)
   1. GOOS=windows GOARCH=amd64 CGO_ENABLED=0 UPX_ENABLE=0 TAGS=dev ./src/hack/build.sh bililive
   2.如果不需要调试，可以改成
      GOOS=windows GOARCH=amd64 CGO_ENABLED=0 UPX_ENABLE=0 TAGS=release ./src/hack/build.sh bililive
```