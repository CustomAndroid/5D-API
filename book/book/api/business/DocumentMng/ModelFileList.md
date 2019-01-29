## 查询指定构件相关资料

> 在电子沙盘中用于查询指定构件相关资料

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/ModelFileList`

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

| 字段                |  类型  | 字段说明                                                     |
| ------------------- | :----: | ------------------------------------------------------------ |
| **Code**            | string | 0：成功 ；其他：失败                                         |
| **CodeMsg**         | String | 失败时原因信息                                               |
| **Fid**             | String | 资料ID                                                       |
| **FileName**        | String | 资料名称                                                     |
| **FileType**        | String | 资料分类ID                                                   |
| **fileTypeName**    | String | 资料分类名称                                                 |
| **modeids**         | String | 关联的构件ID,为空视为关联了全部模型                          |
| **FileVer**         | String | 资料版本                                                     |
| **id**              | String | (不知道有何用)                                               |
| **Adder**           | String | 资料添加人                                                   |
| **adddate**         | String | 添加时间                                                     |
| **FilePath**        | String | 资料路径，前缀为 [login](../../login/login.md) 接口返回的 `WebNetIPAndPort` |
| **FileAttributive** | String | 1-项目资料 2-构件资料  其他-未指定资料归属                   |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Fid": "90",
      "FileName": "效果图1",
      "FileType": "3",
      "fileTypeName": "项目施工指导",
      "modeids": "",
      "FileVer": "20180911042625684",
      "id": "93",
      "Adder": "wang1",
      "adddate": "2018/9/11 16:26:00",
      "FilePath": "/uploadFile/attachment/1cn3rsla9slq1d3r1grk1fgq126c7.jpg",
      "FileAttributive": null
    }
  ]
}
```

