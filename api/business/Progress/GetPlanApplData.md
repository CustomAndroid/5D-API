## 获取进度填报审核列表

> 用于获取进度填报审核列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetPlanApplData`

### 2. 请求参数

body:

| **参数**                | **数据类型** |  是否必须  | 描述     |
| ------------------------- | :--------: | :--: | ------------------------------------------------------------ |
| **ProjectId** | **String** |  Y   | 项目ID(审核人)                                               |
| **userid** | String | Y | 用户ID |
| **pageIndex** | String | Y | 页码 |
| **pagesize** | String | Y | 每页条数 |
| **startTime** | String | N | 开始时间 |
| **endTime** | String | N | 截止时间 |
| **status** | String | N | 状态 1未处理 2正在处理 3已处理 |
| **keyWord** | String | N | 关键字 |

示例:

``` json
{
  "userid": "string",
  "pageIndex": "string",
  "startTime": "string",
  "endTime": "string",
  "status": "string",
  "keyWord": "string",
  "pagesize": "string",
  "ProjectId": 0
}
```
### 3. 返回参数

| 字段               | 字段类型 | 字段说明                                                     |
| ------------------ | :------: | ------------------------------------------------------------ |
| **Code**           |  string  | 0：成功 ；其他：失败                                         |
| **CodeMsg**        |  String  | 失败时原因信息                                               |
| **title**          |  String  | 标题                                                         |
| **addTime**        |  String  | 提交时间                                                     |
| **status**         |  String  | 状态 1未处理 2正在处理 3已处理                               |
| **logId**          |  String  | 进度填报ID,调用[getPlanLogById](getPlanLogById.md)查询填报详情 |
| **myJurisdiction** |  String  | 我的审核权限 0可审核 1仅查看                                 |



返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": [
        {
            "title": "[施工日志填报申请]43号桩基下部", 
            "addTime": "2018/1/31 11:47:00", 
            "status": "1", 
            "logId": "921a46d7-e0f7-418b-8dab-c162af6b418e", 
            "myJurisdiction": "0"
        }
    ]
}
```