## 材料采购提报

> 用于材料采购提报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/submitPurchase`

### 2. 请求参数

body:

| 字段           | 字段类型 | 必填 | 字段说明 |
| -------------- | :------: | :--: | -------- |
| **projectId**  |  String  |  Y   | 项目ID   |
| **userId**     |  String  |  Y   | 用户ID   |
| **buyTime**    |  String  |  Y   | 采购时间 |
| **materialId** |  String  |  Y   | 材料ID   |
| **number**     |  String  |  Y   | 数量     |
| **perParice**  |  String  |  Y   | 单价     |
| **supplyUnit** |  String  |  Y   | 供货单位 |
| **note**       |  String  |  N   | 备注     |

示例:

```json
{
  "userid": "string",
  "projectId": "string",
  "buyTime": "string",
  "materialId": "string",
  "number": "string",
  "perParice": "string",
  "supplyUnit": "string",
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