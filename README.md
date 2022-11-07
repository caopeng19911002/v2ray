安装方法

```bash
   git clone https://github.com/caopeng19911002/v2ray -b master
   cd v2ray
   chmod +x install.sh
   ./install.sh local
   ```

r2ray主程序安装

```bash
   sudo -i
   ```

```bash
   bash <(curl -s -L https://git.io/v2ray.sh)
   ```

如果提示 curl: command not found，请安装 Curl

ubuntu/debian 系统安装 Curl 方法: 

```bash
   apt-get update -y && apt-get install curl -y
   ```

centos 系统安装 Curl 方法: 

```bash
   yum update -y && yum install curl -y
   ```


四合一加速脚本代码

```bash
   wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
   ```


优化 V2Ray

由于本人的脚本在 Debian9 系统会自动开启 BBR 优化加速了，所以不需要再安装 BBR 优化了，
如果你还是觉得网络比较慢的话，你可以尝试使用含有 mKCP 的传输协议，这个 mKCP 的东东，简单一点说就像 Kcptun 一样加速，并且还能进行伪装 (可选)，但是由于 mKCP 是使用 UDP 协议的，也许运营商会限速得更加厉害，网络变得更加慢。但不管怎么样，你都可以随时尝试一下。
服务器输入 v2ray config 回车，然后选择 修改 V2Ray 传输协议，再接着选择 mKCP 相关的传输协议即可
如果你是使用其他商家的 VPS 并且是按照此教程流程来安装 V2Ray 的话，那么你可以输入 v2ray bbr 回车，然后选择安装 BBR 或者 锐速 来优化 V2Ray
只是还想再啰嗦一下，如果你是使用国际大厂的 VPS，并且是按照此教程流程来安装 V2Ray 的话，请自行在安全组 (防火墙) 开放端口和 UDP 协议 (如果你要使用含有 mKCP 的传输协议)

mKCP

mKCP 这个东东其实就是 KCP 协议，反正你知道是能提速的就行，但是不保证都能提速，还能避免 TCP 阻断，但是也可以会被运营商 Qos.
使用方法：服务器输入 v2ray config 回车，然后选择 修改 V2Ray 传输协议，之后再选择 mKCP 相关的就行
