1. 复制`wstunnel`至`/usr/local/bin/`: `sudo cp wstunnel /usr/local/bin/`
2. 复制`wstunnel-client.service`至`/etc/systemd/system/`: `sudo cp wstunnel-client.service /etc/systemd/system/`
3. 启动`wstunnel`: `sudo systemctl enable --now wstunnel-client.service`
4. 安装`wireguard`: `sudo apt install wireguard-tools`
5. 复制配置文件至`/etc/wireguard/`: `sudo cp conf/xxx.conf /etc/wireguard/`
6. 启动`wireguard`: `sudo systemctl enable --now wg-quick@xxx.service`
