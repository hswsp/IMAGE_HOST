# IMAGES
Served as picture host

GitHub 一直拥有各种奇怪的用途，被发掘出来当图床也见怪不怪了。

速度：国内可以接受，海外速度很快

CDN：Fastly CDN，几个节点在国内都解禁了的

HTTPS：支持（似乎不支持 HTTP2）

域名： `user-images.githubusercontent.com`

上传方式是新建一个 Repo，然后在 Issue 中传图（直接将图片拖动到 issue 输入框即可），GitHub 会将你的图片分发到 GitHub 用的 CDN 中。

这和使用 GitHub Raw 需要 GitHub 的服务器动态生成文件不同，user-image 这个子域名是 GitHub 专门为静态文件准备的，不会让当年某某抢票助手 CC GitHub 的事情重现的。 当然，这个接口不是公开的。善待 GitHub。


