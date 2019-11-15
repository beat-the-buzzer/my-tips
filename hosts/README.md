## 给GitHub提速——Hosts文件修改教程

#### 问题背景

我们在使用GitHub的时候，页面加载经常很慢，有时候上传了图片之后，在MarkDown里面引用`https://raw.githubusercontent.com....../`，图片需要很长时间才能下载下来。

#### 知识回顾

[在浏览器地址栏输入地址到页面渲染完成发生了什么？](https://blog.csdn.net/weixin_38150378/article/details/79443584)

浏览器访问网站，要首先通过DNS服务器把要访问的网站域名解析成其指定的IP地址，之后，浏览器才能对此网站进行定位并且访问其数据。

操作系统规定，在进行DNS请求以前，先检查系自己的Hosts文件中是否有这个域名和IP的映射关系。如果有，则直接访问这个IP地址指定的网络位置，如果没有，再向已知的DNS服务器提出域名解析请求。也就是说Hosts的IP解析优先级比DNS要高。

也就是说，我们在访问一些网站，尤其是国外网站，例如Github，我们可以事先在Hosts文件里面设置好地址映射，这样我们在访问网站时，就不需要去进行域名解析了。

#### 解决方式

修改hosts

```shell
# GitHub Start
192.30.253.112 github.com
192.30.253.119 gist.github.com
151.101.100.133 assets-cdn.github.com
151.101.100.133 raw.githubusercontent.com
151.101.100.133 gist.githubusercontent.com
151.101.100.133 cloud.githubusercontent.com
151.101.100.133 camo.githubusercontent.com
151.101.100.133 avatars0.githubusercontent.com
151.101.100.133 avatars1.githubusercontent.com
151.101.100.133 avatars2.githubusercontent.com
151.101.100.133 avatars3.githubusercontent.com
151.101.100.133 avatars4.githubusercontent.com
151.101.100.133 avatars5.githubusercontent.com
151.101.100.133 avatars6.githubusercontent.com
151.101.100.133 avatars7.githubusercontent.com
151.101.100.133 avatars8.githubusercontent.com
# GitHub End
```

#### hosts文件的作用总结

加快地址解析

这个就是我们上面用到的，本机设置，跳过域名解析的过程。

屏蔽网站

90%以上的人都会去访问百度去判断自己的网络是否正常[doge]，我们如果偷偷在Hosts文件里面设置百度的地址，把它指向一个不可用的地址，这样访问百度会一直失败。

自定义域名

有时候在局域网内，我们访问一些资源需要输入比较难记的ip地址，其实我们可以在hosts里面自定义一个地址映射，这样就能用我们自定义的、易于记忆的域名来访问了。