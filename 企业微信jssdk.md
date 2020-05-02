### 企业微信获取当前用户信息
[构造网页授权链接](https://work.weixin.qq.com/api/doc/90000/90135/91022)
[企业微信 获取当前用户信息](https://www.cnblogs.com/BinBinGo/p/11484802.html)
`
  假定当前
  企业CorpID：wxCorpId
  访问链接：http://api.3dept.com/cgi-bin/query?action=get
  根据URL规范，将上述参数分别进行UrlEncode，得到拼接的OAuth2链接为：
  https://open.weixin.qq.com/connect/oauth2/authorize?appid=wxCorpId&redirect_uri=http%3a%2f%2fapi.3dept.com%2fcgi-bin%2fquery%3faction%3dget&response_type=code&scope=snsapi_base&state=#wechat_redirect
  员工点击后，页面将跳转至 
  http://api.3dept.com/cgi-bin/query?action=get&code=AAAAAAgG333qs9EdaPbCAP1VaOrjuNkiAZHTWgaWsZQ&state=
  企业可根据code参数调用获得员工的userid
`
