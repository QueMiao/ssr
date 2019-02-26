一键脚本安装shadowsocks/shadowsocksR/V2Ray + 开启bbr
---

一键脚本搭建shadowsocks/shadowsocksR/V2Ray + 设置开启自启动 + 升级内核&开启bbr加速。

## 支持系统
CentOS 6+

Debian 7+

Ubuntu 12+



---
## 操作命令

#### 下载一键搭建ssr脚本
git clone https://github.com/QueMiao/ssr

#### 运行搭建ssr脚本代码
ssr/ssr.sh -ssr

- 启动：/etc/init.d/shadowsocks start
- 停止：/etc/init.d/shadowsocks stop
- 重启：/etc/init.d/shadowsocks restart
- 状态：/etc/init.d/shadowsocks status
- 配置文件路径：/etc/shadowsocks.json
- 日志文件路径：/var/log/shadowsocks.log
- 代码安装目录：/usr/local/shadowsocks

#### 卸载ssr服务
./shadowsocksR.sh uninstall


#### 一键开启BBR加速
ssr/ssr.sh -bbr

#### 判断BBR加速有没有开启成功
sysctl net.ipv4.tcp_available_congestion_control

#### BBR开启成功
net.ipv4.tcp_available_congestion_control = bbr cubic reno

