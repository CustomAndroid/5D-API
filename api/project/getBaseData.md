## 获取基础词典数据

> 用于获取基础词典数据

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getBaseDat`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **userId**    |  String  |  Y   | 用户ID   |
| **ProjectID** |  String  |  Y   | 项目ID   |

示例:

```json
{
  "ProjectID": "61",
  "userId": "496"
}
```

### 3. 返回参数

| 字段      | 字段类型 | 字段说明                                                     |
| --------- | :------: | ------------------------------------------------------------ |
| **id**    |  string  | ID                                                           |
| **value** |  String  | 名称                                                         |
| **type**  |  String  | 数据类型：`QualityProblemType`-质量问题类别，`QualityProblemLevel`-质量问题严重程度,`ContractMode`-合同模式,`QualityProcessingResults`-审核意见同意不同意,`MaterialUnit`-材料单位列表，`Weather` - 天气，`ConstructionMajor`-施工专业 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "id": "1",
      "value": "工程质量缺陷",
      "type": "QualityProblemType"
    }
  ]
}
```
