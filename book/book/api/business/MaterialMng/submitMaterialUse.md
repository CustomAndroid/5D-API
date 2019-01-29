## 材料领用提报

> 用于材料领用提报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/submitMaterialUse`

### 2. 请求参数

body:

| 字段           | 字段类型 | 必填 | 字段说明 |
| -------------- | :------: | :--: | -------- |
| **projectId**  |  String  |  Y   | 项目ID   |
| **userId**     |  String  |  Y   | 用户ID   |
| **useTime**    |  String  |  Y   | 领用时间 |
| **materialId** |  String  |  Y   | 材料ID   |
| **number**     |  String  |  Y   | 数量     |
| **usedPart**   |  String  |  Y   | 使用部位 |
| **note**       |  String  |  N   | 备注     |

示例:

```json
{
  "userId": "string",
  "projectId": "string",
  "useTime": "string",
  "materialId": "string",
  "number": "string",
  "usedPart": "string",
  "note": "string"
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
  "CodeMsg": "OK",
  "Datas": null
}
```