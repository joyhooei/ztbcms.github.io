### 购物车-添加


#### request

 **method** ：post
 
 **URL**： `index.php?g=Shop&m=Cart&a=set_num`
 

 
字段 | 类型|是否必须|描述
---|---|---|---|
goods_id | varchar|是|用户注册的邮箱或者手机|
set_num | int|是|设置数量|
goods_spec | array|是|商品规格，goods_spec[尺寸],goods_spec[内存],goods_spec[颜色]|

#### response

```
{
  "info": 4,
  "status": 1,
  "url": "",
  "state": "success"
}
```

**ps: 失败返回 status != 1,具体看msg信息**


**登录成功之后返回的shop_user表上的信息。**