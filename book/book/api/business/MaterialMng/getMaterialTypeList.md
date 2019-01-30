## 材料类别查询

> 用于查询材料类别,采购领用时的材料类别清单

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getMaterialTypeList`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **projectId** |  String  |  Y   | 项目ID   |
| **userId**    |  String  |  Y   | 用户ID   |

示例:

```json
{
  "userId": "496",
  "projectId": "61"
}
```

### 3. 返回参数

| 字段          | 字段类型 | 字段说明             |
| ------------- | :------: | -------------------- |
| **Code**      |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**   |  String  | 失败时原因信息       |
| **ID**        |  String  | 主键ID               |
| **BaseName**  |  String  | 名称                 |
| **BaseKey**   |  String  | MaterialType         |
| **BaseValue** |  String  | 材料类别Id           |



返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "ID": 6098,
      "BaseName": "钢材",
      "BaseKey": "MaterialType",
      "BaseValue": "1"
    },
    {
      "ID": 6099,
      "BaseName": "水泥混凝土",
      "BaseKey": "MaterialType",
      "BaseValue": "2"
    },
    {
      "ID": 6100,
      "BaseName": "木材",
      "BaseKey": "MaterialType",
      "BaseValue": "3"
    },
    {
      "ID": 6101,
      "BaseName": "塑料",
      "BaseKey": "MaterialType",
      "BaseValue": "4"
    },
    {
      "ID": 6309,
      "BaseName": "钢材22",
      "BaseKey": "MaterialType",
      "BaseValue": "5"
    }
  ]
}
```