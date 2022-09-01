# IMAGES
Served as picture host

GitHub 一直拥有各种奇怪的用途，被发掘出来当图床也见怪不怪了。

速度：国内可以接受，海外速度很快

CDN：Fastly CDN，几个节点在国内都解禁了的

HTTPS：支持（似乎不支持 HTTP2）

域名： `user-images.githubusercontent.com`

上传方式是新建一个 Repo，然后在 Issue 中传图（直接将图片拖动到 issue 输入框即可），GitHub 会将你的图片分发到 GitHub 用的 CDN 中。

这和使用 GitHub Raw 需要 GitHub 的服务器动态生成文件不同，user-image 这个子域名是 GitHub 专门为静态文件准备的，不会让当年某某抢票助手 CC GitHub 的事情重现的。 当然，这个接口不是公开的。善待 GitHub。

# 使用jsdelivr作为CDN

使用前点击release发布

## 通过jsDelivr引用资源，自定义发布版本号

使用方法：https://cdn.jsdelivr.net/gh/你的用户名/你的仓库名@发布的版本号/文件路径

例如：

https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@1.0/images/trhx.png

https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@2.0.1/css/style.css

https://cdn.jsdelivr.net/gh/moezx/cdn@3.1.3//The%20Pet%20Girl%20of%20Sakurasou.mp4

注意：版本号不是必需的，是为了区分新旧资源，如果不使用版本号，将会直接引用最新资源，除此之外还可以使用某个范围内的版本，查看所有资源等，具体使用方法如下：

```java
// 加载任何Github发布、提交或分支
https://cdn.jsdelivr.net/gh/user/repo@version/file

// 加载 jQuery v3.2.1
https://cdn.jsdelivr.net/gh/jquery/jquery@3.2.1/dist/jquery.min.js

// 使用版本范围而不是特定版本
https://cdn.jsdelivr.net/gh/jquery/jquery@3.2/dist/jquery.min.js
https://cdn.jsdelivr.net/gh/jquery/jquery@3/dist/jquery.min.js

// 完全省略该版本以获取最新版本
https://cdn.jsdelivr.net/gh/jquery/jquery/dist/jquery.min.js

// 将“.min”添加到任何JS/CSS文件中以获取缩小版本，如果不存在，将为会自动生成
https://cdn.jsdelivr.net/gh/jquery/jquery@3.2.1/src/core.min.js

// 在末尾添加 / 以获取资源目录列表
https://cdn.jsdelivr.net/gh/jquery/jquery/
```



