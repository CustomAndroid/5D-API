## 根据ID查询/新建安全整改通知单

> RT. 这个接口可两用：
>
> * 传入字段 `id`不为空时用于查询该整改通知单；
> * 传入字段`id`为空，其他字段不为空为新建整改通知单；

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/NewSafetyRectificationNotice`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                                                     |
| ------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId** |  String  |  Y   | 项目ID                                                       |
| **userid**    |  String  |  Y   | 用户ID                                                       |
| **id**        |  String  |  Y   | 传入字段 `id`不为空以下字段为空时用于查询该整改通知单；传入字段`id`为空，以下字段不为空为新建整改通知单； |
| **title**     |  String  |  Y   | 标题                                                         |
| **orgId**     |  String  |  Y   | 当前登录人所在组织ID                                         |
| **AddTime**   |  String  |  Y   | 签发日期                                                     |
| **unitId**    |  String  |  Y   | 施工单位                                                     |
| **GUID**      |  String  |  Y   | 模型位置,构件ID                                              |
| **StartTime** |  String  |  Y   | 整改时间 开始                                                |
| **EndTime**   |  String  |  Y   | 整改时间 截止                                                |
| **Content**   |  String  |  Y   | 整改内容                                                     |
| **filesList** |  String  |  N   | 附件                                                         |
| **sendTo**    |  String  |  Y   | 发送人                                                       |
| **copyTo**    |  String  |  N   | 抄送人                                                       |
| **SendDate**  |  String  |  Y   | 提交时间，默认当前时间 yyyy-MM-dd                            |
| **UserName**  |  String  |  Y   | 当前登录人名字，[login](../../login/login.md)中的`userNameText` |

示例:

```json
{
  "userid": "string",
  "projectId": "string",
  "id": "string",
  "title": "string",
  "orgId": "string",
  "AddTime": "string",
  "unitId": "string",
  "GUID": "string",
  "EndTime": "string",
  "StartTime": "string",
  "Content": "string",
  "filesList": "string",
  "sendTo": "string",
  "copyTo": "string",
  "SendDate": "string",
  "UserName": "string"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |

新建提交，返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": ""
}
```

查询整改通知单详情:

|  父字段  | 字段        | 字段类型 | 字段说明         |
| ---- |---- | :--: | ---- |
| **MassageModel** || Object | 通知单内容详情 |
| |**Mid** | String | 通知单ID |
| |**MassageName** | String | 标题 |
| |**MCode** | String | 编码 |
| |**projectid** | String | 项目ID |
| |**orgId** | String | 施工单位ID |
| |**Star** | String | 整改时间开始 |
| |**End** | String | 整改时间截止 |
| |**Conent** | String | 内容 |
| |**sendid** | String | 签发人 |
| |**SendDate** | String | 签发日期 |
| |**modelIDs** | String | 模型位置构件IDs |
| **MassageFlowsDataList**| | Array | 审核意见列表 |
| | **Lid** | String | 流程ID |
| | **Mid** | String | 整改通知单ID |
| | **SenderId** | String | 上次审核发送人 |
| | **SendDate** | String | 上次审核时间 |
| | **ExecuteId** | String | 本次审核人 |
| | **ExecuteDate** | String | 本次审核执行时间 |
| | **Attitude** | String | 处理意见 |
| | **Step** | String | 审核步骤 |
| | **treat** | String | 处理措施 |
| | **Status** | String | 状态 |
| | **Note** | String | 备注 |
| **MassageCopyList**| | Array | 反馈意见列表 |
| | **Lid** | String | 流程ID |
| | **Mid** | String | 整改通知单ID |
| | **SenderId** | String | 上次审核发送人 |
| | **SendDate** | String | 上次审核时间 |
| | **ExecuteId** | String | 本次审核人 |
| | **ExecuteDate** | String | 本次审核执行时间 |
| | **Attitude** | String | 处理意见 |
| | **Step** | String | 审核步骤 |
| | **Status** | String | 状态 |
| **IsEnd**| | Boolean | 是否结束 |

返回实例：

``` json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "MassageModel": {
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
            "type": "1", 
            "NextUserId": null, 
            "isHandle": false, 
            "CopyUserIds": null, 
            "HandleType": null
        }, 
        "MassageFlowsDataList": [
            {
                "Lid": "106", 
                "Mid": "91", 
                "SenderId": "495", 
                "SendDate": "2018/9/19 14:32:50", 
                "ExecuteId": "498", 
                "ExecuteDate": "2018/9/19 14:34:27", 
                "Attitude": "同意", 
                "Step": "1", 
                "treat": "同意", 
                "Status": "2", 
                "Note": ""
            }, 
            {
                "Lid": "107", 
                "Mid": "91", 
                "SenderId": "498", 
                "SendDate": "2018/9/19 14:32:50", 
                "ExecuteId": "499", 
                "ExecuteDate": "2018/9/19 14:35:42", 
                "Attitude": "同意", 
                "Step": "1", 
                "treat": "同意", 
                "Status": "2", 
                "Note": ""
            }, 
            {
                "Lid": "108", 
                "Mid": "91", 
                "SenderId": "499", 
                "SendDate": "2018/9/19 14:32:50", 
                "ExecuteId": "495", 
                "ExecuteDate": "2018/9/19 14:35:59", 
                "Attitude": "同意", 
                "Step": "1", 
                "treat": "同意", 
                "Status": "2", 
                "Note": ""
            }
        ], 
        "MassageCopyList": [
            {
                "ID": "32", 
                "MID": "91", 
                "SendUserID": "495", 
                "SendDate": "2018/9/19 14:32:50", 
                "ReceiveUserID": "494", 
                "ExecuteDate": null, 
                "Attitude": "同意,请及时处理现场产生的问题", 
                "Status": "2", 
                "LID": "106"
            }, 
            {
                "ID": "33", 
                "MID": "91", 
                "SendUserID": "498", 
                "SendDate": "2018/9/19 14:34:27", 
                "ReceiveUserID": "495", 
                "ExecuteDate": null, 
                "Attitude": "同意以上要求", 
                "Status": "2", 
                "LID": "107"
            }
        ], 
        "MassageAttachmentList": null, 
        "ProjectName": null, 
        "BuildName": null, 
        "IsEnd": true
    }
}
```

