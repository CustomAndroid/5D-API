## 获取库存材料图标数据

> 用于获取材料库存统计中某材料的图表库存数据

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetMaterialStockRecord`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                                     |
| ------------- | :------: | :--: | ------------------------------------------------------------ |
| **userId**    |  String  |  Y   | 用户ID                                                       |
| **projectId** |  String  |  Y   | 项目ID                                                       |
| **StartDate** |  String  |  Y   | 开始时间 yyyy-MM                                             |
| **EndDate**   |  String  |  Y   | 截止时间 yyyy-MM                                             |
| **OrgID**     |  String  |  Y   | 当前登录人所在单位组织ID，[登录](../../login/login.md)接口中返回的`userOrganizationId` |
| **Material**  |  String  |  Y   | 材料ID，从[GetMaterialIinventoryStatistics](GetMaterialIinventoryStatistics.md)接口获取 |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "OrgID": "418",
  "Material": "61",
  "StartDate": "2017-11-01",
  "EndDate": "2018-11-01"
}
```

### 3. 返回参数

| 字段               | 字段类型 | 字段说明             |
| ------------------ | :------: | -------------------- |
| **Code**           |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**        |  String  | 失败时原因信息       |
| **SMonth**         |  String  | 月份                 |
| **PurchaseAmount** |  String  | 采购量               |
| **UseAmount**      |  String  | 领用量               |
| **Stock**          |  String  | 库存                 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "SMonth": "2017-11",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2017-12",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-1",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-2",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-3",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-4",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-5",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-6",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-7",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-8",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "0.00"
    },
    {
      "SMonth": "2018-9",
      "PurchaseAmount": "12.00",
      "UseAmount": "10.00",
      "Stock": "2.00"
    },
    {
      "SMonth": "2018-10",
      "PurchaseAmount": "",
      "UseAmount": "",
      "Stock": "2.00"
    }
  ]
}
```