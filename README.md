# Vagrant-Ansible-CentOS

## OS
CentOS8

## Package
- Git
- Docker
- MySQL
- Nginx

## 事前準備
[ansible-galaxy](https://galaxy.ansible.com/)にて[lean_delivery.mysql](https://galaxy.ansible.com/lean_delivery/mysql),[nginxinc.nginx](https://galaxy.ansible.com/nginxinc/nginx)のインストール
```
$ ansible-galaxy install lean_delivery.mysql -p provisioning/roles
$ ansible-galaxy install nginxinc.nginx -p provisioning/roles
```
削除したい場合
```
$ ansible-galaxy remove lean_delivery.mysql -p provisioning/roles
$ ansible-galaxy remove nginxinc.nginx -p provisioning/roles
```

## 注意
以下のエラーは無視して良い
```
TASK [lean_delivery.mysql : Check mysql version] *******************************
fatal: [192.168.56.19]: FAILED! => {"changed": false, "msg": "unable to find /root/.my.cnf. Exception message: (1045, \"Access denied for user 'root'@'localhost' (using password: YES)\")"}
```
