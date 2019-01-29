## 获取安全整改通知单列表

> 用于获取安全整改通知单列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetSafetyRectificationNoticeList`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明    |
| ------------- | :------: | :--: | ----------- |
| **ProjectID** |  String  |  Y   | 项目ID      |
| **userId**    |  String  |  Y   | 用户ID      |
| **type**      |  String  |  Y   | 1审核 2反馈 |

示例:

```json
{
  "ProjectID": "61",
  "userId": "496",
  "type": "1"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |
| **Mid** | String | 整改通知单ID |
| **Logid** | String |  |
| **MassageName** | String | 标题 |
| **MCode** | String | 编号 |
| **SendDate** | String | 签发日期 |
| **Status** | String | 状态 1未处理 2正在处理 3已完成 |
| **Conent** | String | 内容 |
| **sendid** | String | 签发人 |
| **SendDate** | String | 签发日期 |
| **orgId** | String | 施工单位ID |
| **Star** | String | 开始整改时间 |
| **End** | String | 截止整改时间 |
| **modelIDs** | String | 构件IDs |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "Mid": "91", 
        "Logid": "79", 
        "MassageName": "2018-09-19 - 电源存在不安全隐患 - SHE整改通知书", 
        "MCode": "201809191429340418", 
        "BuidId": "0", 
        "projectid": "61", 
        "orgId": "418", 
        "show": "", 
        "modelIDs": "", 
        "Star": "2018/9/1 0:00:00", 
        "End": "2018/9/18 0:00:00", 
        "Conent": "危险源“外电防护措施缺乏或不符合要求；” 在“标段一” 检查“外电防护措施” 结果为“防护措施不到位” 建议整改措施“1、加强监督检查并立即整改； 2、严格按照规范要求设置外电防护。”；危险源“接地与接零保护系统不符合要求” 在“标段一” 检查“接地与接零保护系统” 结果为“接地未按要求设置” 建议整改措施“1、规范接地与接零保护系统； 2、加强监督检查并立即整改。”；", 
        "sendid": "495", 
        "SendDate": "2018/9/19 0:00:00", 
        "Status": "3", 
        "type": "1"
    }
}
```