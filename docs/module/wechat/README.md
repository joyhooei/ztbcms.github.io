## 微信管理 ![version](https://img.shields.io/github/release/ztbcms/ztbcms-Wechat.svg?maxAge=36000)

### 配置

微信模块的正常使用需要提供一些微信信息，

#### 需要配置的信息如下：

- wx_app_id ： 微信公众号 app_id
- wx_secret ： 微信公众号 app_secret

#### 配置位置：

为了所有的模块都能使用这些微信配置，我们使用后台的站点配置来设置这些信息。（系统设置 -> 站点设置 -> 扩展配置）

 ![图片](https://dn-coding-net-production-pp.qbox.me/4268d248-a811-4e36-a9b7-caf6cbfeed8b.png) 

### 获取js-sdk

#### 地址：

Wechat\Service\AppService::getJsSdk

#### 调用方式：

静态方法

#### 参数：

| 参数名 | 说明 | 必要 | 默认 |
| -- | -- | -- | -- |
| options | 需要获取的 js-sdk 权限，[权限列表](https://mp.weixin.qq.com/wiki?action=doc&id=mp1421141115&t=0.8300217118358675#fl2) | 是 | 无 |
| debug | 是否开启调试模式 | 否 | false |
| beta | - | 否 | false |
| json | 是否返回 Json 格式结果 | 否 | true |

#### 调用示例：

后台返回方式
```php
use Wechat\Service\AppService;
$jsSdkConfig = AppService::getJsSdk(['onMenuShareTimeline']);
$this-assign('jsConfig',$jsSdkConfig);
```

前端直接渲染方式

```php
<script src="//res.wx.qq.com/open/js/jweixin-1.2.0.js"></script>
<script>
    wx.config(<?php echo Wechat\Service\AppService::getJsSdk(['onMenuShareTimeline']); ?>);
</script>
```

