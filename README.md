# load_balancer

##  Install and config keepalived
apt update
apt install keepalived -y
systemctl enable keepalived

vim /etc/sysctl.conf
net.ipv4.ip_nonlocal_bind=1
sysctl -p

### Conf:
vim /etc/keepalived/keepalived.conf

##  Install and config HAproxy
apt update
apt install haproxy -y
systemctl enable haproxy

### Conf:
vim /etc/haproxy/haproxy.cfg
