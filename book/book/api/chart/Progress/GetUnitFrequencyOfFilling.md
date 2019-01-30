## 获取施工单位进度填报频次

> 用于获取施工单位进度填报频次

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetUnitFrequencyOfFilling`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **projectId** |  String  |  Y   | 项目ID   |
| **userid**    |  String  |  Y   | 用户ID   |
| **startTime** |  String  |  Y   | 开始时间 |
| **endTime**   |  String  |  Y   | 截止时间 |
| **unit**      |  String  |  N   | 施工单位 |

示例:

```json
{
  "userid": "496",
  "projectId": "61",
  "startTime": "2018-8-01",
  "endTime": "2018-11-01",
  "unit": "0"
}
```

### 3. 返回参数

| 字段         | 字段类型 | 字段说明             |
| ------------ | :------: | -------------------- |
| **Code**     |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**  |  String  | 失败时原因信息       |
| **unit**     |  String  | 施工单位             |
| **mon**      |  String  | 月份                 |
| **number**   |  String  | 填报次数             |
| **lastdate** |  String  | 最后一次填报时间     |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "unit": "中铁十二局第二公司", 
            "mon": "9", 
            "number": 0, 
            "lastdate": "2018/10/22 14:18:52"
        }
    ]
}
```