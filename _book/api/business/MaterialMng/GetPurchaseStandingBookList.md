## 采购台账查询

> 用于查询采购台账

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetPurchaseStandingBookList`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明             |
| ------------- | :------: | :--: | -------------------- |
| **projectId** |  String  |  Y   | 项目ID               |
| **startTime** |  String  |  Y   | 开始时间             |
| **endTime**   |  String  |  Y   | 结束时间             |
| **userId**    |  String  |  N   | 用户ID               |
| **companyId** |  String  |  N   | 当前登录人所在单位ID |
| **Keyword**   |  String  |  N   | 关键字               |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "startTime": "2018-10-01",
  "endTime": "2018-11-30",
  "companyId": "418",
  "Keyword": ""
}
```

### 3. 返回参数

| 字段               | 字段类型 | 字段说明                                                     |
| ------------------ | :------: | ------------------------------------------------------------ |
| **Code**           |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**        |  String  | 失败时原因信息                                               |
| **id**             |  String  | 台账ID                                                       |
| **projectid**      |  String  | 项目ID                                                       |
| **PurchaseOrgId**  |  String  | 采购单位ID                                                   |
| **Supplier**       |  String  | 材料供应商                                                   |
| **PurchaseDate**   |  String  | 采购日期                                                     |
| **Material**       |  String  | 材料ID                                                       |
| **MaterialName**   |  String  | 材料名称                                                     |
| **MaterialFormat** |  String  | 材料规格                                                     |
| **Unit**           |  String  | 材料计量单位ID，比如 米 ，从[getBaseData](../../project/getBaseData.md)中`MaterialUnit`类 |
| **Quantity**       |  String  | 数量                                                         |
| **price**          |  String  | 单价                                                         |
| **Note**           |  String  | 备注                                                         |
| **Adder**          |  String  | 登记人                                                       |
| **Addtime**        |  String  | 登记时间                                                     |
| **Usercode**       |  String  | 登记人ID                                                     |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "id": "68", 
        "projectid": "61", 
        "PurchaseOrgId": "417", 
        "Supplier": "贵州预制厂", 
        "PurchaseDate": "2018/9/8 0:00:00", 
        "Material": "60", 
        "MaterialName": "C20", 
        "MaterialFormat": "100", 
        "Unit": "2", 
        "Quantity": "1000.00", 
        "price": "100.00", 
        "Note": "", 
        "Adder": "wang1", 
        "Addtime": "2018/9/8 14:06:17", 
        "Usercode": "495"
    }
}
```