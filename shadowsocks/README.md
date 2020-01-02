### 科学上网工具——shadowsocks

#### 使用翻墙的场合

我们在平时工作的时候，难免会需要科学上网，例如：

 - Google应用商店

 ![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-01.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-01.png)

 - 一些国外的视频（图为babel官网）

  ![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-02.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-02.png)

 - 真机调试

  ![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-03.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-03.png)

下面就使用shadowsocks工具以及网上可以查到的SS节点进行免费翻墙。

#### shadowsocks工具下载和使用

1、百度搜索关键字“free ss”：

![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-04.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-04.png)

2、在`ishadow`里面下载`shadowsocks`工具，根据自己的系统下载对应的安装包。

[https://get.ishadowx.biz/](https://get.ishadowx.biz/)

3、在这个网站上，我们还能获取到节点的信息，点击图中的位置，可以在屏幕上生成一个二维码。

![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-05.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-05.png)

4、打开shadowsocks，右键右下角的图标（Mac的图标在屏幕最上方），选择服务器 => 扫描屏幕上的二维码

![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-06.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-06.png)


5、测试是否成功：[https://www.google.com.hk/webhp?hl=zh-CN&sourceid=cnhp&gws_rd=ssl](https://www.google.com.hk/webhp?hl=zh-CN&sourceid=cnhp&gws_rd=ssl)


#### 可能遇到的问题

1、二维码无法扫描或者扫描成功之后无法翻墙

不是所有的二维码都能成功，要多次尝试。

2、500 Internal Privoxy Error

![https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-07.png](https://gitee.com/beat-the-buzzer/pictures/raw/master/my-tips/shadowsocks/ss-07.png)

我是换了工位之后出现了这个错误，网上搜了一下，需要重置网络。

```shell
netsh interface ipv4 reset
netsh interface ipv6 reset
netsh winsock reset
```


