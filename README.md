安装方法
git clone https://github.com/caopeng19911002/v2ray -b master
cd v2ray
chmod +x install.sh
./install.sh local


2ray主程序安装

sudo -i

bash <(curl -s -L https://git.io/v2ray.sh)

如果提示 curl: command not found，请安装 Curl

ubuntu/debian 系统安装 Curl 方法: 

apt-get update -y && apt-get install curl -y

centos 系统安装 Curl 方法: 

yum update -y && yum install curl -y


四合一加速脚本代码

wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
