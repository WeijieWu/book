# 共享笔记

- [C++](C++)


在服务端启动一个代理程序
```
docker run -e PASSWORD=PASSWORD -p 8388:8388 -p 8388:8388/udp -d --restart always shadowsocks/shadowsocks-libev
```
