# centos离线安装docker

- 下载选择下载版本(17需要依赖对应的selinux，并先安装selinux)

https://download.docker.com/linux/centos/7/x86_64/stable/Packages/

```shell
# 如果是17则运行（options）
sudo  yum install ***selinux.rpm
sudo  yum install ***.rpm
sudo groupadd docker
sudo gpasswd -a ${USER} docker
sudo systemctl enable docker
sudo systemctl start docker
```
