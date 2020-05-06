### 企业微信获取当前用户信息

[构造网页授权链接](https://work.weixin.qq.com/api/doc/90000/90135/91022)
[企业微信 获取当前用户信息](https://www.cnblogs.com/BinBinGo/p/11484802.html)

### 问题

jsweixin引入时报错Cannot read property 'title' of undefined
jweixin-1.2.0.js里面的执行方式不适合直接webpack。我看到的报错是cannot read title of undefined，不知道你们是不是这个问题。

这个问题的原因是，里面在执行this.document.title的时候出的问题，这个js期望实在浏览器全局作用域下执行（this指向window），但是webpack之后，是在一个function作用域下执行，因此this.document为undefined。

因此有几种方式修改：

改源码，将jweixin-1.2.0.js中第一个this改为window

在html中使用script引入

webpack有个script-loader可以让模块文件在global环境下执行，可以试试看



