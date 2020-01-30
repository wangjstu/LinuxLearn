# PHPer学go--安装环境

## 第一步：下载解压源文件
到[golang官方下载地址](https://golang.google.cn/dl/)下载需要的安装包，我这里下载的是linux编译后的版本：
```SHELL
[root@wangjstu wangjstu]# wget https://dl.google.com/go/go1.13.7.linux-amd64.tar.gz
--2020-01-30 13:34:21--  https://dl.google.com/go/go1.13.7.linux-amd64.tar.gz
Resolving dl.google.com (dl.google.com)... 203.208.40.98, 203.208.40.102, 203.208.40.96, ...
Connecting to dl.google.com (dl.google.com)|203.208.40.98|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 120071076 (115M) [application/octet-stream]
Saving to: ‘go1.13.7.linux-amd64.tar.gz’

100%[===============================================================================================================================================================>] 120,071,076 12.2MB/s   in 8.5s

2020-01-30 13:34:30 (13.4 MB/s) - ‘go1.13.7.linux-amd64.tar.gz’ saved [120071076/120071076]


[root@wangjstu wangjstu]# ll go1.13.7.linux-amd64.tar.gz
-rw-r--r-- 1 root root 120071076 Jan 29 00:23 go1.13.7.linux-amd64.tar.gz


[root@wangjstu wangjstu]# tar zxvf go1.13.7.linux-amd64.tar.gz -C /usr/local/
go/
go/AUTHORS
go/CONTRIBUTING.md
go/CONTRIBUTORS
......

```


## 第二步：配置环境变量
### 修改PATH
打开`/etc/profile`，在文件最后添加如下内容
```SHELL
export GOPATH=/home/wangjstu/golang
export PATH=$PATH:/usr/local/go/bin

```
执行以下命令生效及校验
```SHELL
[root@wangjstu wangjstu]# source $HOME/.profile
[root@wangjstu wangjstu]# go env
```

### 第三步：Hello world

```SHELL
#[wangjstu@wangjstu ~]$ vim /home/wangjstu/golang/hello.go
package main

import "fmt"

func main() {
        fmt.Printf("hello world\n")
}
```

### 关键概念讲解
* 




## 参考文献
* [golang官网](https://golang.google.cn/)
* [golang doc](https://golang.google.cn/doc/code.html)
* [SettingGOPATH](https://github.com/golang/go/wiki/SettingGOPATH)
* [Go语言规范](https://golang.google.cn/ref/spec)
* [Go命令教程](https://hyper0x.github.io/go_command_tutorial/#/)
* [Setting GOPATH](https://github.com/golang/go/wiki/SettingGOPATH)