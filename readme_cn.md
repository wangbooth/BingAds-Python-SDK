# Bing Ads API

请务必仔细阅读官方文档！API 文档地址：https://learn.microsoft.com/en-us/advertising/guides/?view=bingads-13

> 文档中可能有部分内容是过时的，或者未对中国用户做调整的地方，需对 API 进行仔细测试以甄别。

## 如何开始

文档地址：https://learn.microsoft.com/en-us/advertising/guides/get-started?view=bingads-13

### 注册一个 Web 应用程序

文档地址：https://learn.microsoft.com/en-us/advertising/guides/authentication-oauth-register?view=bingads-13

注意，需要放开权限，让「任何组织目录(任何 Microsoft Entra ID 租户 - 多租户)中的帐户和个人 Microsoft 帐户(例如 Skype、Xbox)」都有权限使用此应用。

重定向 URI 选择 Web 平台，输入一个 redirect_uri，比如 http://localhost:8080/auth

注册完成后，会得到 client_id 和 client_secret，以及一个自定义的 redirect_uri。

### 开发者令牌 developer_token

文档地址：https://learn.microsoft.com/en-us/advertising/guides/get-started?view=bingads-13#get-developer-token

在调用 Bing Ads API 时，不仅要拿到用户授权后的 access_token，还要用到开发者令牌 developer_token。

> 开发者令牌需要用户在微软 Ads 开发者门户页面上生成，只有超级管理员有权限生成这个，需联系一级代理商来生成。

### Demo

第一步，需要参考 https://github.com/wangbooth/BingAds-Python-SDK/blob/bing_cn/examples/v13/auth_helper.py，设置代码中的 CLIENT_ID、CLIENT_SECRET、REDIRECTION_URI 和 DEVELOPER_TOKEN 为实际值。

然后，可以参考 https://github.com/wangbooth/BingAds-Python-SDK/blob/bing_cn/examples/v13/responsive_search_ads.py，创建响应式搜索广告，实现账户基建工作。

可以参考 https://github.com/wangbooth/BingAds-Python-SDK/blob/bing_cn/examples/v13/offline_conversions.py，将转化数据回传至对应的转化目标。

