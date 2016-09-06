# wechat-dev
在前后端分离

angular ui-router

进页面需获取当前页的URL，切换路由的时候，不能改变值

千万不要使用$locationProvider.html5Mode(true);模式，

微信支付授权目录就是个坑，使用微信支付最好使用

$locationProvider.hashPrefix('?');

将微信的应用的url设置成以下格式：

``` js
http://wx.example.com/#?/
```

1. 分享失败，点击没有反应

解决方案:

分享方法外层添加

``` js
wx.ready();
```
建议:

能所有调用微信SDK都加上

2.config失败

解决方案:

每次切面跳转/或者页面切换路由都要重新

``` js
wx.config();
```

3.图片上传

wx.config() 是 ok

微信分享功能正常

解决方案:

非不得已不要在config promise后添加与微信无关的方法

4.其他问题

wx.hideOptionMenu();该方法能不用则不用

总结：

WechatService.js

``` js
/** 
 * 1.配置微信config
 * 2.每个需要调用微信SDK的都得执行该方法（解决Android兼容性）
 */
WechatService.config(() => {
	// 非不得已不要在内部添加与微信无关的方法
});
```
