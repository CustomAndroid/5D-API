## 材料领用提报选择材料清单

> 用于查询材料领用提报选择材料清单

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getUseMaterialList`

### 2. 请求参数

body:

| 字段             | 字段类型 | 必填 | 字段说明                                                     |
| ---------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId**    |  String  |  Y   | 项目ID                                                       |
| **userId**       |  String  |  Y   | 用户ID                                                       |
| **MaterialType** |  String  |  Y   | 材料类别ID,[getMaterialTypeList](getMaterialTypeList.md) 中的 `BaseValue` |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "MaterialType": ""
}
```

### 3. 返回参数

| 字段         | 字段类型 | 字段说明             |
| ------------ | :------: | -------------------- |
| **Code**     |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**  |  String  | 失败时原因信息       |
| **ID**       |   Int    | ID                   |
| **Name**     |  String  | 材料名称             |
| **Format**   |  String  | 材料规格             |
| **UnitName** |  String  | 材料单位             |
| **Stock**    |  String  | 库存                 |
| **Type**     |   Int    | 材料类别Id           |
| **TypeName** |   Int    | 材料类别名称         |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "ID": 61,
      "Type": 3,
      "TypeName": "木材",
      "Name": "圆木",
      "Format": "1",
      "UnitName": "米",
      "Stock": 12
    }
  ]
}
```