# pve


- 为防止系统没安装curl，使用不了一键命令，使用下面的一键命令之前先执行一次安装curl命令
```sh
apt -y update && apt -y install curl || yum install -y curl || apk add curl bash
```

- 使用root用户登录alpine系统，后执行以下命令安装curl
```sh
apk add curl bash
```
- ### PVE开启直通+CPU硬盘温度显示,风扇转速+一键开启换源，去订阅+CPU睿频模式选择
```sh
bash -c  "$(curl -fsSL https://ghproxy.com/https://raw.githubusercontent.com/shidahuilang/pve/main/pve.sh)"
```
- ### PVE一键升级PVE，lxc换源，去掉无效订阅
```sh
bash -c  "$(curl -fsSL https://ghproxy.com/https://raw.githubusercontent.com/shidahuilang/pve/main/pvehy.sh)"
```
- ### 开启ssh
```
sed -i "s/.*PermitRootLogin.*/PermitRootLogin yes/g"   /etc/ssh/sshd_config && systemctl restart sshd.service && service sshd restart
```
- ### (centos、ubuntu、debian、alpine)一键开启SSH
```sh
bash -c  "$(curl -fsSL https://ghproxy.com/https://raw.githubusercontent.com/shidahuilang/pve/main/ssh.sh)"
```



- ### PVE升级系统
```sh
apt update && apt dist-upgrade -y
```
