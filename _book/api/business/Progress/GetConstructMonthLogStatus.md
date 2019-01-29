## 查询施工日志月填报情况

> 用于查询施工日志月填报情况,返回查询月内已填报施工日志的日期

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetConstructMonthLogStatus `

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **userid**          | **String** |  Y   | 用户ID（填报人ID）                                           |
| **projectid**    | **String** |  Y   | 项目ID(审核人)                                               |
| **ConstructUnitId** | **String** | Y | 施工单位ID |
| **checkDate** | **String** | Y | 查询月 |
| **UserType** | **String** | Y | 用户类型 |

示例:

``` json
{
  "userid": "496",
  "projectid": "61",
  "ConstructUnitId": "418",
  "checkDate": "2018-09",
  "UserType": "2"
}
```
### 3. 返回参数

| 字段        |  字段类型  | 字段说明             |
| ----------- | :--------: | -------------------- |
| **Code**    |   string   | 0：成功 ；其他：失败 |
| **CodeMsg** |   String   | 失败时原因信息       |
| **Datas**   | Array[Int] | 查询月已填报日期     |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    19,
    18,
    17,
    16,
    15,
    14,
    13,
    12,
    11,
    10,
    9,
    8,
    7,
    6,
    5,
    4,
    3,
    2,
    1
  ]
}
```