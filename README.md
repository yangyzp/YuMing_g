# node.sh
# sspanel节点一键对接脚本

### 测试环境：
>AWS lighsail CentOS7/Debian9/Ubuntu18 测试通过

### 脚本功能：
1.  一键安装后端
2.  自动填写节点配置
3.  安装supervisor守护后端
4.  安装crontab定时重启后端
5.  安装bbr
6.  修改iptables，开放22-65535端口
7.  修改openfiles
8.  设置系统时间为北京时间
9.  自动同步时间
10. 关闭selinuix

### 使用方法：
方法一：（推荐）一键对接命令
1.  打开一键对接命令生成器网站：https://dump0.github.io/auto
2.  填入各项参数
3.  生成一键对接命令
4.  复制命令，粘贴到后端上，以root权限执行
5.  保存这段命令，用于以后对接

方法二：
1.  复制下面的命令，粘贴到后端上，以root权限执行

    `wget -N --no-check-certificate https://raw.githubusercontent.com/dump0/node.sh/master/node.sh && chmod +x node.sh && ./node.sh`
 
2.  在终端上输入各项参数

方法三：
1.  Centos:
 - 数据库对接
 ![Centos-glzjinmod](https://raw.githubusercontent.com/yangyzp/node.sh/master/img/Centos-glzjinmod.png)
   ```
   yum install wget screen -y && screen -S node
   wget -N --no-check-certificate https://raw.githubusercontent.com/dump0/node.sh/master/node.sh && chmod +x node.sh && Auto_Install="y" INTERFACE="2" NODE_ID="3" RESTART="4" SPEEDTEST="0" CLOUDSAFE="1" ANTISSATTACK="0" AUTOEXEC="0" MU_SUFFIX="zhaoj.in" MU_REGEX="%5m%id.%suffix" MYSQL_HOST="1.1.1.1" MYSQL_PORT="3306" MYSQL_USER="sspanel" MYSQL_PASS="123456" MYSQL_DB="sspanel" ./node.sh
   ```
 - API对接
 ![Centos-API](https://raw.githubusercontent.com/yangyzp/node.sh/master/img/Centos-API.png)
   ```
   yum install wget screen -y && screen -S node     #Centos 
   apt install wget screen -y && screen -S node     #Debian/Ubuntu 
   ```
   ```    
   wget -N --no-check-certificate https://raw.githubusercontent.com/dump0/node.sh/master/node.sh && chmod +x node.sh && Auto_Install="y" INTERFACE="2" NODE_ID="3" RESTART="4" SPEEDTEST="0" CLOUDSAFE="1" ANTISSATTACK="0" AUTOEXEC="0" MU_SUFFIX="zhaoj.in" MU_REGEX="%5m%id.%suffix" MYSQL_HOST="1.1.1.1" MYSQL_PORT="3306" MYSQL_USER="sspanel" MYSQL_PASS="123456" MYSQL_DB="sspanel" ./node.sh
   ```  

