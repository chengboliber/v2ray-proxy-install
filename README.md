# v2ray-proxy-install

注意：务必保证域名解析已经成功了，再使用下面的脚本安装。

打开电脑命令行，ping 你的域名，如果显示VPS的IP地址，则解析生效了。

1、使用SSH工具连接VPS，执行下列命令，选择安装v2ray+ws+tls

curl -O https://raw.githubusercontent.com/atrandys/v2ray-ws-tls/master/v2ray_ws_tls.sh && chmod +x v2ray_ws_tls.sh && ./v2ray_ws_tls.sh
2、等待脚本执行，过程中会提示需要输入域名，输入解析到本VPS的域名，然后回车

3、等待安装完成，你可以看到配置参数，客户端配置时用到。

4、安装BBR加速，指向下面命令

cd /usr/src && wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
5、注意在弹出的安装界面首先选择1，安装BBR内核,安装过程可能时间较长,耐心等待。

6、安装完成后会提示重启VPS,输入Y，然后回车，确认重启。然后等待几分钟，再使用xshell连接vps（连接方法是点软件上打开，找到之前保存的连接，然后点连接）登陆后执行下列命令

cd /usr/src && ./tcp.sh
7、在弹出安装界面,输入5,然后回车，使用BBR魔改版加速，等待安装完成提示bbr启动成功即可
