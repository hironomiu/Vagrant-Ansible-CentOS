# Vagrant-Ansible-CentOS

## OS
CentOS8

## Package
- Git
- Docker
- MySQL

## 事前準備
[ansible-galaxy](https://galaxy.ansible.com/)にてlean_delivery.mysqlのインストール
```
$ ansible-galaxy install lean_delivery.mysql -p provisioning/roles
```

## 注意
以下のエラーは無視して良い
```
TASK [lean_delivery.mysql : Check mysql version] *******************************
fatal: [192.168.56.19]: FAILED! => {"changed": false, "msg": "unable to find /root/.my.cnf. Exception message: (1045, \"Access denied for user 'root'@'localhost' (using password: YES)\")"}
```