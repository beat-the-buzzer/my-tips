## 给GitHub提速

#### 问题背景

我们在使用GitHub的时候，页面加载经常很慢，有时候上传了图片之后，在MarkDown里面引用`https://raw.githubusercontent.com....../`，图片需要很长时间才能下载下来。

#### 知识回顾

[在浏览器地址栏输入地址到页面渲染完成发生了什么？](https://blog.csdn.net/weixin_38150378/article/details/79443584)

#### 解决方案

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

#### hosts文件的其他作用