## 请求/更新token

> 请求/更新access_token,该token用于后续接口请求header中，用法详见该字段说明

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：/token

### 2. 请求参数

| 字段              | 字段类型 | 必填 | 字段说明                                                     |
| ----------------- | :------: | :--: | ------------------------------------------------------------ |
| **client_id**     |  String  |  Y   | 默认值 `GlBIMWeb`                                            |
| **client_secret** |  String  |  Y   | 默认值 `h3cgQfiit4yGaaV2R1FVpA68WFZ8P0PS8`                   |
| **grant_type**    |  String  |  Y   | 默认值 `client_credentials`（定值）                          |
| **refresh_token** |  String  |  N   | 获取token后得到的refresh_token,用于刷新已过期的access_token,第一次请求token时为空 |

示例:

``` json
{
    "client_id": "GlBIMWeb", 
    "client_secret": "h3cgQfiit4yGaaV2R1FVpA68WFZ8P0PS8", 
    "grant_type": "client_credentials", 
    "refresh_token": ""
}
```

### 3. 返回参数

| 字段              | 字段类型 | 字段说明                                                     |
| ----------------- | :------: | ------------------------------------------------------------ |
| **access_token**  |  string  | 有效期30分钟，用于带有oauth2.0身份验证的接口，添加在请求header中：key为`Authorization` ,value为`Bearer+空格+access_token` |
| **refresh_token** |  String  | 用于刷新已过期的access_token                                 |
| **expires_in**    |   int    | Access_token到期时间（单位s）                                |

返回示例：

``` json
{
    "access_token": "r6PCZIQ_McnUizYbO5bvkhQbJhZpE-Yjsq9imGdNkNdALKkaZV43AHbDJX8NqYqVeYQyKEVrd-6yI1_1vWXT8CdCCThY4c_he6mWyA0EuJYbAiYBadlffdsY5QRao6AgN_ga0q-sv8QgV1vqz89LhP-CHudG2PeHxnuDePQ0BF1SdhafazPDTvu6vxXBwmvXPUAqeo1vSJFhdZOaklDRfuY8uj2oaTOrgXw3v71PzWc", 
    "token_type": "bearer", 
    "expires_in": 1799, 
    "refresh_token": "2196465b-ec9e-4221-9cbe-9d787ffa29bb", 
    "as:GlBIMWeb": "GlBIMWeb", 
    ".issued": "Sat, 16 Sep 2017 06:48:50 GMT", 
    ".expires": "Sat, 16 Sep 2017 07:18:50 GMT"
}
```

