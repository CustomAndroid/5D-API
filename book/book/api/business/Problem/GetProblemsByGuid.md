## 根据构件ID查询该构件相关的问题列表

> 用于电子沙盘点击选中构件查询与该构件相关的问题列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetProblemsByGuid `

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                  |
| ------------- | :------: | :--: | ------------------------- |
| **userid**    |  String  |  Y   | 用户ID                    |
| **projectid** |  String  |  Y   | 项目ID                    |
| **guid**      |  String  |  Y   | 构件ID                    |
| **modelName** |  String  |  Y   | 模型名称（模型zip文件名） |

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

| 字段        |  类型  | 字段说明                                      |
| ----------- | :----: | --------------------------------------------- |
| **Code**    | string | 0：成功 ；其他：失败                          |
| **CodeMsg** | String | 失败时原因信息                                |
| **Datas**   | Array  | 参考[问题列表](getQualityQuesList.md)返回结构 |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [/**参考问题列表返回**/]
}
```

