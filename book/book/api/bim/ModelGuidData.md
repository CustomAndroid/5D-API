## 查询指定构件属性信息

> 在电子沙盘中用于查询指定构件属性信息

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/ModelGuidData`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                                     |
| ------------- | :------: | :--: | ------------------------------------------------------------ |
| **userid**    |  String  |  Y   | 用户ID                                                       |
| **projectid** |  String  |  Y   | 项目ID                                                       |
| **guid**      |  String  |  Y   | 构件ID                                                       |
| **modelName** |  String  |  Y   | 该构件所在模型名称，构件Id `_`前是模型Id，可用于查询对应 `modelName` |

示例:

```json
{
  "projectid": "string",
  "userid": "string",
  "guid": "string",
  "modelName": "string"
}
```

### 3. 返回参数

| 字段                 |  类型  | 字段说明             |
| -------------------- | :----: | -------------------- |
| **Code**             | string | 0：成功 ；其他：失败 |
| **CodeMsg**          | String | 失败时原因信息       |
| **externalId**       | String | 属性ID               |
| **propertyTypeName** | String | 组                   |
| **propertyname**     | String | 属性 key             |
| **value**            | String | 属性 value           |
| **groupname**        | String | 所属组名             |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
        "externalId" : "330795",
         "propertyTypeName" : "object", // 组
         "propertySetName" : "General",
         "propertyname" : "Ifc Label", //key
         "value" : "#330795", //value
         "groupname" : "梁"
    }
  ]
}
```

