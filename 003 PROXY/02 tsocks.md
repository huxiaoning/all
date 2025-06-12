### tsocks
强制命令socks代理
```bash
$ wget -O /etc/yum.repos.d/tsocks-epel-7.repo https://copr.fedoraproject.org/coprs/neteler/tsocks/repo/epel-7/neteler-tsocks-epel-7.repo
$ yum install -y tsocks

$ vim /etc/tsocks.conf
local = 192.168.1.0/255.255.255.0
local = 172.17.0.0/255.255.0.0
server = 127.0.0.1
server_type = 5
server_port = 7890

# enjoy
$ tsocks wget https://github.com/mihomo-party-org/mihomo-party/releases/download/v1.7.5/mihomo-party-windows-1.7.5-ia32-setup.exe
```
