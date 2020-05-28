# NetKeeper-Interception
## 一、使用方法
#### 1.将nk4conf.sh,nk4.sh和nk4三个文件拷入openwrt的/root/目录。 未安装rp-pppoe-server请看步骤2,已安装的直接看步骤4。
#### 2.将rp-pppoe-common_3.12-7_mipsel_24kc.ipk 和 rp-pppoe-server_3.12-7_mipsel_24kc.ipk文件拷入openwrt的/tmp目录下。
#### 2.ssh登入openwrt,并运行一下命令
```sh
cd /tmp
opkg install rp-pppoe-common_3.12-7_mipsel_24kc.ipk
opkg install rp-pppoe-server_3.12-7_mipsel_24kc.ipk
```
#### 4.运行sh nk4conf.sh。
```sh
chmod a+x *.sh
sh nk4conf.sh
```
### 电脑端

1.连接路由器

2.netkeeper输入账号密码拨号，会提示错误不用理会，登录openwrt网页，在 网络 -> 接口 查看NETKEEPER是否获取到IPv4。

3.获取到IPv4则表示拦截成功，连接路由器的设备都能正常浏览网页。

## 特别鸣谢
netkeeper的核心源码来自于miao1007的Openwrt-NetKeeper
