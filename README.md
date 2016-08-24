# wechat-dev
在前后端分离

angular ui-router

1. 分享失败，点击没有反应

解决方案:

分享方法外层添加

``` js
wx.ready();
```
建议:

能所有调用微信SDK都加上

2. config失败

解决方案:

每次切面跳转/或者页面切换路由都要重新

``` js
wx.config();
```

3.图片上传

wx.config() 是 ok

微信分享功能正常

解决方案:

非不得已不要加微信以外的方法微信wx.config();

4.微信支付

iOS 能正常支付

Android <= 6.0 没有任何反应

Android >= 6.0 支付闪现，没有任何反应，可能是支付授权目录错误

解决方案:

http://test.com/

http://test.com/pay/

http://test.com/pay/index/

5.微信hideOptionMenu能不用则不用
