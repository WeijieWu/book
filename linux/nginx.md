# 安装nginx

* sudo yum install epel-release(安装yum源)
* sudo yum install nginx(安装nginx)
* sudo systemctl start nginx
* sudo firewall-cmd --permanent --zone=public --add-service=http 
* sudo firewall-cmd --permanent --zone=public --add-service=https
* sudo firewall-cmd --reload
* sudo systemctl enable nginx
