# 共享笔记

- [C++](C++)


在服务端启动一个代理程序
```
docker run -d --name shadowsocks -p 8389:12306 oddrationale/docker-shadowsocks -s 
0.0.0.0 -p 12306 -k demopdfssf -m aes-256-cfb
```
