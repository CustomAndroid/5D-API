## 获取进度沙盘-差异分析

> 获取差异分析

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getDifferenceAnalysis`

### 2. 请求参数

body:

| 字段                 | 字段类型 | 必填 | 字段说明 |
| -------------------- | :------: | :--: | -------- |
| **userId**           |  String  |  Y   | 用户ID   |
| **constructionUnit** |  String  |  N   | 施工单位 |
| **modelId**          |  String  |  N   | 模型ID   |

传入参数 constructionUnit（施工单位）与modelId（模型ID）二选一,另外一个则传空。

示例:

```json
{
  "userId": "496",
  "constructionUnit":"418",
  "modelId":""
}
```

### 3. 返回参数

| 字段                   | 字段类型 | 字段说明                                                     |
| ---------------------- | :------: | ------------------------------------------------------------ |
| **unfinished** |  string  | 未完成 - 构件ID                                      |
| **advance** | string | 提前完工-构件ID |
| **normal** | string | 正常完工-构件ID |
| **delayFinished** | string | 延期完工-构件ID |


返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "ok", 
    "Datas": {
        "unfinished": "", 
        "advance": "", 
        "normal": "", 
        "delayFinished": ""
    }
}
```
