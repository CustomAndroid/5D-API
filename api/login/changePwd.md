## 修改密码

> 用于修改登录密码（默认密码分发账号时初始化），若修改密码后忘记新密码，需联系系统管理进行密码初始化

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/changePwd`

### 2. 请求参数

body:

| 字段       | 字段类型 | 必填 | 字段说明      |
| ---------- | :------: | :--: | ------------- |
| **oldPwd** |  String  |  Y   | 旧密码（MD5） |
| **newPwd** |  String  |  Y   | 新密码（MD5） |
| **userId** |  String  |  Y   | 用户ID        |

示例:

```json
{
  "oldPwd": "string",
  "newPwd": "string",
  "userId": "string"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "修改成功",
  "Datas": null
}
```
