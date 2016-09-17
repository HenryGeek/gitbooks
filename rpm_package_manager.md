# rpm包管理

## 安装: -i

    [root@bogon packages]# rpm -qa | grep ncat
    [root@bogon packages]# ls
    nmap-ncat-6.40-7.el7.x86_64.rpm
    [root@bogon packages]# rpm -i nmap-ncat-6.40-7.el7.x86_64.rpm 
    [root@bogon packages]# rpm -qa | grep nmap-ncat
    nmap-ncat-6.40-7.el7.x86_64
    [root@bogon packages]# rpm -i nmap-ncat
    错误：打开 nmap-ncat 失败： 没有那个文件或目录

-i选项后面必须跟着rpm包的路径,不然会报open错误

## 卸载: -e

    [root@bogon packages]# rpm -e nmap-ncat
    [root@bogon packages]# rpm -qa | grep nmap-ncat
    [root@bogon packages]# rpm -e nmap-ncat
    错误：未安装软件包 nmap-ncat 
    [root@bogon packages]#

如果要卸载的包不存在rpm数据库里，则会报错，存在就直接删除

## 查询: -q

    [root@bogon packages]# rpm -q nmap-ncat
    未安装软件包 nmap-ncat 
    [root@bogon packages]# rpm -i nmap-ncat-6.40-7.el7.x86_64.rpm 
    [root@bogon packages]# rpm -q nmap-ncat
    nmap-ncat-6.40-7.el7.x86_64

-q后面跟着rpm包名,如果包存在RPM数据库里，那么打印该包名，不存在则显示未安装包

## 升级:  -U 或 -F
    [root@bogon packages]# rpm -U nmap-ncat-6.40-7.el7.x86_64.rpm 
    [root@bogon packages]# rpm -U nmap-ncat-6.40-7.el7.x86_64.rpm 
	软件包 nmap-ncat-2:6.40-7.el7.x86_64 已经安装

-U选项后面必须跟着rpm包的路径，如果存在旧版本的软件包，则直接升级，否则直接安装
如果存在同版本的软件包，则报已经安装

-F选项后面必须跟着rpm包的路径，如果存在旧版本的软件包，则直接升级，否则跳过不安装


## 校验:

 rpm -V rpm_package_name ...



