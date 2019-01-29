## 获取资料分类

> 用于获取资料分类返回id-pid树级结构

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/ProjectFileTree`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明             |
| ------------- | :------: | :--: | -------------------- |
| **userId**    |  String  |  Y   | 用户ID               |
| **Projectid** |  String  |  Y   | 项目ID               |
| **pageIndex** |  String  |  Y   | 没有分页，此字段无效 |
| **pageSize**  |  String  |  Y   | 没有分页，此字段无效 |

示例:

```json
{
  "userId": "496",
  "Projectid": "61",
  "pageIndex": "string",
  "pageSize": "string"
}
```

### 3. 返回参数

| 字段        |  类型  | 字段说明             |
| ----------- | :----: | -------------------- |
| **Code**    | string | 0：成功 ；其他：失败 |
| **CodeMsg** | String | 失败时原因信息       |
| **id**      | String | 资料分类ID           |
| **name**    | String | 资料分类名称         |
| **pid**     | String | 资料分类父ID         |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "id": "93",
      "name": "效果图",
      "pid": "0"
    }
  ]
}
```

