## 材料库存量统计

> 用于材料库存量统计

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetMaterialIinventoryStatistics`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                                     |
| ------------- | :------: | :--: | ------------------------------------------------------------ |
| **userId**    |  String  |  Y   | 用户ID                                                       |
| **projectId** |  String  |  Y   | 项目ID                                                       |
| **time**      |  String  |  Y   | 月份                                                         |
| **keywords**  |  String  |  Y   | 关键字                                                       |
| **Unit**      |  String  |  Y   | 当前登录人所在单位组织ID，[登录](../../login/login.md)接口中返回的`userOrganizationId` |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "time": "2018-11",
  "keywords": "",
  "Unit": "418"
}
```

### 3. 返回参数

| 字段                   | 字段类型 | 字段说明             |
| ---------------------- | :------: | -------------------- |
| **Code**               |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**            |  String  | 失败时原因信息       |
| **MaterialType**       |  String  | 材料类型             |
| **MaterialName**       |  String  | 材料名称             |
| **MonthPurchaseAmout** |  String  | 当月采购量           |
| **MonthUseAmout**      |  String  | 当月领用量           |
| **SumPurchaseAmout**   |  String  | 累计采购量           |
| **SumUseAmout**        |  String  | 累计领用量           |
| **MaterialStock**      |  String  | 库存                 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "id": "61",
      "HOrgID": null,
      "OrgName": null,
      "MaterialType": "木材",
      "MaterialName": "圆木",
      "MonthPurchaseAmout": "",
      "MonthUseAmout": "",
      "SumPurchaseAmout": "12.00",
      "SumUseAmout": "10.00",
      "MaterialStock": "2.00"
    }
  ]
}
```