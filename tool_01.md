apt：安装管理各种软件，主要在debian, ubuntu linux系统中<br>
git：开发软件的版本维护工具
npm: 

rpm:简化开源软件的安装和管理,用在redhat, centos
rpm基本命令：
- 安装软件 ```rpm -i software.rpm```
- 卸载软件 ```rpm -e software```
- 升级形式安装  ```rpm -U software-new.rpm```
- 通过http, ftp协议安装 ```rpm -ivh http://software.rpm```
- 查询软件 ``rpm -qa```   (-a(all) -f(filename) -i(info) -I(include包含的文件) -p(查询未安装rpm文件))

yum: RPM的前端程序，用来自动解决RPM的依赖关系问题    
