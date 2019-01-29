## 验工计价明细

> 用于查询验工计价明细

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetInspectionPriceContentList`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **projectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userId** | String | Y | 用户ID |
| **Lid** | String | Y | 验工计价 |

示例:

``` json
{
  "userid": "string",
  "projectId": "string",
  "Lid": "string"
}
```
### 3. 返回参数

| 字段             | 字段类型 | 字段说明             |
| ---------------- | :------: | -------------------- |
| **Code**         |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**      |  String  | 失败时原因信息       |
| **Lid**          |  String  | 验工计价ID           |
| **id**           |  String  | id                   |
| **Did**          |  String  | 序号                 |
| **CAmount**      |  String  | 本次完成量           |
| **note**         |  String  | 备注                 |
| **DetailsName**  |  String  | 项目名称/项目特征    |
| **DetailsPrice** |  String  | 综合单价（元）       |
| **Amount**       |  String  |                      |
| **MAmunt**       |  String  |                      |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "id": "175", 
            "Lid": "85", 
            "Did": "139679", 
            "CAmount": "160.00", 
            "note": "110.00", 
            "DetailsName": "19-1#桩基_桩基_桩基-混凝土", 
            "DetailsPrice": "110.00", 
            "Amount": "190.09", 
            "MAmunt": null
        }
    ]
}
```