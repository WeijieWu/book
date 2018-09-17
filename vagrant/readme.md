
# vagrant 
Vagrant是一个用于构建和维护可移植虚拟软件开发环境的开源软件产品，[4]例如VirtualBox，Hyper-V，Docker容器，VMware和AWS，它们试图简化虚拟化的软件配置管理，以便增加开发生产率。Vagrant是用Ruby语言编写的

## 常见操作

```
vagrant box add	添加box的操作
vagrant init	初始化box的操作，会生成vagrant的配置文件Vagrantfile
vagrant up	启动本地环境
vagrant ssh	通过 ssh 登录本地环境所在虚拟机
vagrant halt	关闭本地环境
vagrant suspend	暂停本地环境
vagrant resume	恢复本地环境
vagrant reload	修改了 Vagrantfile 后，使之生效（相当于先 halt，再 up）
vagrant destroy	彻底移除本地环境
vagrant box list	显示当前已经添加的box列表
vagrant box remove	删除相应的box
vagrant package	打包命令，可以把当前的运行的虚拟机环境进行打包
vagrant plugin	用于安装卸载插件
vagrant status	获取当前虚拟机的状态
vagrant global-status	显示当前用户Vagrant的所有环境状态
```

## 常见插件

```
vagrant-proxyconf 配置代理
vagrant-vbguest virtualbox文件共享
```
## e.g:
```
Vagrant.configure("2") do |config|
  config.vm.box = "centos7"
  config.vm.hostname = "m1"
  config.vm.network "public_network", ip: "192.168.10.110", bridge: [
    "en0: Wi-Fi (AirPort)",
  ]
  # 依赖与vagrant-proxyconf
  config.proxy.http = "http://192.168.10.62:8118"
  config.proxy.https = "http://192.168.10.62:8118"
  # 配置运行环境
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end
end
```