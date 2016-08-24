# wechat-dev
在前后端分离
angular ui-router
1. 无论何时都要加wx.ready();

2. 每次切面跳转/或者页面切换路由都要重新wx.config();


3.非不得已不要加微信以外的方法wx.ready(() => {});


4.微信支付授权目录
全部都加上
http://test.com/
http://test.com/pay/
http://test.com/pay/index/

5.微信hideOptionMenu能不用则不用。
