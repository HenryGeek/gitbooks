# rpm包管理

## 安装:

    [root@bogon packages]# rpm -qa | grep ncat
    [root@bogon packages]# ls
    nmap-ncat-6.40-7.el7.x86_64.rpm
    [root@bogon packages]# rpm -i nmap-ncat-6.40-7.el7.x86_64.rpm 
    [root@bogon packages]# rpm -qa | grep nmap-ncat
    nmap-ncat-6.40-7.el7.x86_64
    [root@bogon packages]#

## 卸载:

 rpm -e rpm_package_name ...

## 查询:

 rpm -q

## 升级:

 rpm -U/-F path_to_rpm_package ...

## 校验:

 rpm -V rpm_package_name ...



