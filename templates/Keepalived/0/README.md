# Keepalived for Rancher HA-Proxy Loadbalancer

### 信息：

此模板用于在Rancher里为内置的基于HA-Proxy技术的多个LoadBalancer节点创建一个Failover高可用服务。

当你从catalog部署此应用时，一个全局（global）的集群被创建，因此你可以在创建此Catalog时先不启动它，创建之后利用Host Lable来设置容器调度策略，以确保此HA应用运行在适合的宿主机上。

### 使用方法:

在创建该Catalog应用时，请特别注意宿主机网卡名，例如有可能是`eth0`，也有可能是`eno16777984`这样的格式。
当集群部署完毕并运行起来后，使用在Catalog中定义好的虚拟IP地址及侦听端口访问应用。

`http://<Virtual IP>:<port>`
例如：`http://172.18.1.68:3000`
