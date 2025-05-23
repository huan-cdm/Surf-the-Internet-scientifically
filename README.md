<h3>安装命令</h3>
bash <(curl -L https://raw.githubusercontent.com/v2fly/fhs-install-v2ray/master/install-release.sh)<br>
<h3>卸载命令</h3>
bash <(curl -L https://raw.githubusercontent.com/v2fly/fhs-install-v2ray/master/install-release.sh) --remove<br>
<h3>服务管理</h3>
systemctl start v2ray #启动v2ray<br>
systemctl status v2ray #运行状态<br>
systemctl restart v2ray #重启v2ray<br>
systemctl stop v2ray #停止v2ray<br>
systemctl enable v2ray #v2ray开机自启<br>
systemctl disable v2ray #v2ray取消开机自启<br>
journalctl -u v2ray -f #查看实时日志<br>
<h3>服务检测</h3>
v2ray test -config /usr/local/etc/v2ray/config.json<br>
<h3>代理测试</h3>
curl --socks5 127.0.0.1:10808 https://www.google.com<br>
# 设置http代理<br>
export http_proxy=socks5://127.0.0.1:10808<br>
# 设置https代理<br>
export https_proxy=socks5://127.0.0.1:10808<br>
# 设置ftp代理<br>
export ftp_proxy=socks5://127.0.0.1:10808<br>
