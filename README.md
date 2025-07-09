# ddns-firewall

## 脚本参数
动态域名：域名/dns服务器，使用公共dns也可以，变更解析后生效时间不稳定，建议将dns服务器修改为对应域名运营商的地址
domains='www.annda.net/karina.ns.cloudflare.com'
信任IP：一般填写跳板机或其他授信的云节点静态IP
trust_ips='1.1.1.1'
端口：脚本需要处理拦截的端口
ports='22,3306'

调试日志
debug='0'
debug_exclude_ports='22,80,443'

网络接口：云主机的网卡接口
interface='eth0'
公网IP：当前云服务器的公网IP，避免应用填写公网IP，环路至云防火墙回到云服务器被拦截
external_ip='{{ inventory_hostname }}'
