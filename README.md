### 目录结构
```
.
├── conf/   # wireguard 配置文件
├── linux/
├── macOS/
└── win/
```

* `conf/`下为`wireguard`通用配置文件
* `linux/` `macos/` `win/`下分别为系统对应二进制文件及配置

### Linux
1. 解压`wstunnel_x.x.x_linux_xxxxx.tar.gz`
1. 复制`wstunnel`至`/usr/local/bin/`: `sudo cp wstunnel /usr/local/bin/`
1. 复制`wstunnel-client.service`至`/etc/systemd/system/`: `sudo cp wstunnel-client.service /etc/systemd/system/`
1. 启动`wstunnel`: `sudo systemctl enable --now wstunnel-client.service`
1. 安装`wireguard`: `sudo apt install wireguard-tools`
1. 复制`wireguard`配置文件至`/etc/wireguard/`: `sudo cp conf/xxx.conf /etc/wireguard/`
1. 启动`wireguard`: `sudo systemctl enable --now wg-quick@xxx.service`

### MacOS
1. 解压`wstunnel_x.x.x_darwin_xxxxx.tar.gz`
1. 执行`wstunnel.sh`
1. 解压`wireguard_x_x_x.zip` [wireguard-macos-app](https://github.com/mintc2/wireguard-macos-app)
1. 启动`wireguard`
1. `wireguard`中新建隧道，导入配置文件`conf/xxx.conf`
1. 连接

### Windows
1. 执行`wstunnel.cmd`
1. 安装`wireguard-amd64-x.x.x.msi`
1. 启动`wireguard`
1. `wireguard`中新建隧道，导入配置文件`conf/xxx.conf`
1. 连接
