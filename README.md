# wechat-dev
在前后端分离\n
angular ui-router\n
1. 分享失败，点击没有反应\n

解决方案:\n
分享方法外层添加wx.ready()\n
建议:\n
能所有的方法都加wx.ready()\n

2. config失败\n

解决方案:\n
每次切面跳转/或者页面切换路由都要重新wx.config()\n

3.图片上传\n
wx.config() 是 ok\n
微信分享功能正常\n

解决方案:\n
非不得已不要加微信以外的方法微信config\n

4.微信支付\n
iOS 能正常支付\n
Android <= 6.0 没有任何反应\n
Android >= 6.0 支付闪现，没有任何反应，可能是支付授权目录错误\n

解决方案:\n
http://test.com/\n
http://test.com/pay/\n
http://test.com/pay/index/\n

5.微信hideOptionMenu能不用则不用\n
