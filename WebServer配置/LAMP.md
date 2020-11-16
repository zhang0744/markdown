

# Linux + apache + MySql + PHP

## 使用包管理器安装

### apache

安装

centos7:

```shell
yum install httpd
```

启动并设置开机自启

```shell
systemctl start httpd
systemctl enable httpd
```

设置防火墙

```shell
firewall-cmd --permanent --zone=public --add-service=http
firewall-cmd --permanent --zone=public --add-service=https
firewall-cmd --reload ##重新加载配置
```

