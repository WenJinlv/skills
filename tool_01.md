dpkg(deb): 类似(rpm)安装和管理各种软件，主要在debian, ubuntu linux系统中
apt：
git：开发软件的版本维护工具
npm: 

rpm:简化开源软件的安装和管理,用在redhat, centos
- rpm基本命令：
    - 安装软件 ```rpm -i software.rpm```
        - 通过http, ftp协议安装 ```rpm -ivh http://software.rpm```
    - 卸载软件 ```rpm -e software```
    - 升级形式安装  ```rpm -U software-new.rpm```  
    - 查询软件 
        - 查询已安装   ``rpm -qa``` (-a(all) -f(filename) -i(info) -I(include包含的文件) 
        - 查询未安装    -p(查询未安装rpm文件))

yum: RPM的前端程序，用来自动解决(通过仓库repo)RPM的依赖关系问题    
- YUM仓库
    - 仓库的配置文件： ```/etc/yum.repos.d/```目录下以```.repo```结尾
    - 配置YUM源(国内)
    - 创建YUM仓库: createrepo软件
- YUM基本命令
    - 安装软件  ```yum install software```
    - 卸载软件   ```yum remove software```
    - 升级软件    ```yum update software```
    - 查询软件    
        - 查询已安装 ```yum list, yum info packagename```
        - 查询未安装  ```yum search keyword```
