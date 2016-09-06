# centos-global-proxy

首先安装配置好 shadowsocks 确保正常使用

安装privoxy  
yum install privoxy

修改 /etc/privoxy/config

forward-socks5 / 127.0.0.1:          端口换为1080


此处即将SS的socks5流量前接了一个privoxy代理，而prixovy允许各种协议流量通过，包括HTTP、HTTPS、FTP、SOCKS等。


export http_proxy=http://127.0.0.1:8118
export ftp_proxy=http://127.0.0.1:8118
export https_proxy=http://127.0.0.1:8118

如果需要在sudo 中使用环境变量 sudo -E command....

如果wget 要用代理 在URL后面加上 -e use_proxy=yes -e http_proxy=127.0.0.1:8118
