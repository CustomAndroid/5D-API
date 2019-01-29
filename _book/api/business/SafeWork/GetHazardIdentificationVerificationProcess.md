## 查询危险源识别详情+审核流程

> 用于查询危险源识别审核流程

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetHazardIdentificationVerificationProcess`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明     |
| ------------- | :------: | :--: | ------------ |
| **ProjectID** |  String  |  Y   | 项目ID       |
| **userId**    |  String  |  Y   | 用户ID       |
| **hid**       |  String  |  Y   | 危险源识别ID |

示例:

```json
{
  "userId": "496",
  "projectId": "61",
  "hid": "107"
}
```

### 3. 返回参数

| 字段                           | 字段类型 | 字段说明             |
| ------------------------------ | :------: | -------------------- |
| **Code**                       |  string  | 0：成功 ；其他：失败 |
| **CodeMsg**                    |  String  | 失败时原因信息       |
| **m**                          |  Object  | 危险源识别详情       |
| **list**                       |  Array   | 危险源列表           |
| **ProjectHazardFlowsDataList** |  Array   | 审核流程列表         |
| **CopyModelList**              |  Array   | 反馈列表             |

**`m`**各字段：

| 字段                | 字段类型 | 字段说明                           |
| ------------------- | :------: | ---------------------------------- |
| **Hid**             |  String  | 危险源识别ID                       |
| **Projectid**       |  String  | 项目ID                             |
| **Title**           |  String  | 标题                               |
| **SignDate**        |  String  | 识别时间                           |
| **AllNum**          |  String  | 危险源总数                         |
| **ControllableNum** |  String  | 可控危险源数量                     |
| **veryNum**         |  String  | 异常危险源数量                     |
| **Status**          |  String  | 处理状态 1未处理 2正在处理 3已处理 |
| **Adder**           |  String  | 填报人                             |
| **Addtime**         |  String  | 填报时间                           |

**`list`**字段:

| 字段              | 字段类型 | 字段说明                         |
| ----------------- | :------: | -------------------------------- |
| **Sid**           |          | 危险源ID                         |
| **SafeName**      |          | 危险源标题                       |
| **Typeid**        |          | 类别ID                           |
| **ProcessShow**   |          |                                  |
| **AllowRisk**     |          | 可导致的风险                     |
| **Level**         |          | 风险等级                         |
| **ModelID**       |          | 关联的构件ID，为空则没有关联模型 |
| **LabelPosition** |          | 标签                             |

**`ProjectHazardFlowsDataList`**字段：

| 字段            | 字段类型 | 字段说明   |
| --------------- | :------: | ---------- |
| **Lid**         |  String  | 审核流程ID |
| **Hid**         |  String  | 危险源识别 |
| **SenderId**    |  String  | 发送人ID   |
| **SendDate**    |  String  | 发送日期   |
| **ExecuteId**   |  String  | 审核人ID   |
| **ExecuteDate** |  String  | 审核时间   |
| **Attitude**    |  String  | 处理意见   |
| **treat**       |  String  | 处理结果   |
| **Status**      |  String  | 状态       |
| **Note**        |  String  | 处理措施   |

**`CopyModelList`**字段：

| 字段              | 字段类型 | 字段说明   |
| ----------------- | :------: | ---------- |
| **ID**            |  String  | 反馈ID     |
| **Lid**           |  String  | 反馈流程ID |
| **Hid**           |  String  | 危险源识别 |
| **SendUserID**    |  String  | 发送人ID   |
| **SendDate**      |  String  | 发送日期   |
| **ReceiveUserID** |  String  | 反馈人ID   |
| **ExecuteDate**   |  String  | 反馈时间   |
| **Attitude**      |  String  | 反馈意见   |
| **Status**        |  String  | 状态       |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "m": {
            "Hid": "105", 
            "Projectid": "61", 
            "Title": "危险源识别测试", 
            "SignDate": "2018/9/19 0:00:00", 
            "Optionid": "495", 
            "AllNum": "4", 
            "ControllableNum": "4", 
            "veryNum": "0", 
            "Status": "3", 
            "Adder": "wang1", 
            "Addtime": "2018/9/19 14:20:37", 
            "TrueName": null, 
            "isHandle": null, 
            "HandleType": null, 
            "rq": null
        }, 
        "list": [
            {
                "Sid": "23", 
                "SafeName": "外电防护措施缺乏或不符合要求；", 
                "Typeid": "8", 
                "ProcessShow": "临时用电", 
                "AllowRisk": "触电等", 
                "Measures": "", 
                "LVal": "3", 
                "EVal": "6", 
                "CVal": "15", 
                "DVal": "270", 
                "Level": "2", 
                "SourceId": "0", 
                "Addtime": "2018/4/12 14:07:34", 
                "adder": "admin", 
                "ProjectID": "61", 
                "TypeName": null, 
                "IndexNum": null, 
                "PlanIdStr": null, 
                "timeSlot": null, 
                "ModelID": "599_664683;599_542423", 
                "LabelPosition": ";;4228.45751953125,4005.0546875,1804296.8125,0.7798426074651325,0,0.7853981633974483,9955.420142052768,-22432.76166331605,1839339.201804956;4228.45751953125,4005.0546875,1804296.8125,0.7798426074651325,0,0.7853981633974483,3502.0126377998267,-17227.434498662362,1812978.3736574862"
            }, 
            {
                "Sid": "24", 
                "SafeName": "接地与接零保护系统不符合要求", 
                "Typeid": "8", 
                "ProcessShow": "临时用电", 
                "AllowRisk": "触电等", 
                "Measures": "", 
                "LVal": "3", 
                "EVal": "5", 
                "CVal": "6", 
                "DVal": "90", 
                "Level": "3", 
                "SourceId": "0", 
                "Addtime": "2018/4/12 14:07:19", 
                "adder": "admin", 
                "ProjectID": "61", 
                "TypeName": null, 
                "IndexNum": null, 
                "PlanIdStr": null, 
                "timeSlot": null, 
                "ModelID": "600_943592", 
                "LabelPosition": ";;74654.98974609375,290820.966796875,1810079.4375,0.7853981633974483,0,0.7853981633974483,50786.469790261384,210503.63516288856,1757490.3256216529"
            }, 
            {
                "Sid": "25", 
                "SafeName": "施工用电作业用电施工组织设计缺失或缺陷", 
                "Typeid": "8", 
                "ProcessShow": "临时用电", 
                "AllowRisk": "触电等", 
                "Measures": "", 
                "LVal": "3", 
                "EVal": "4", 
                "CVal": "5", 
                "DVal": "60", 
                "Level": "4", 
                "SourceId": "0", 
                "Addtime": "2018/4/12 14:03:32", 
                "adder": "admin", 
                "ProjectID": "61", 
                "TypeName": null, 
                "IndexNum": null, 
                "PlanIdStr": null, 
                "timeSlot": null, 
                "ModelID": "600_943594;600_943592", 
                "LabelPosition": ";;74654.98974609375,169912.16061206392,1810079.4375,0.7853981633974483,0,0.7853981633974483,92772.09743893571,64151.11114691757,1722018.3243774911;74654.98974609375,169912.16061206392,1810079.4375,0.7853981633974483,0,0.7853981633974483,50252.91043693101,94488.22649935493,1753074.4859886812"
            }, 
            {
                "Sid": "26", 
                "SafeName": "违反“一机、一闸、一漏、一箱”", 
                "Typeid": "8", 
                "ProcessShow": "临时用电", 
                "AllowRisk": "触电等", 
                "Measures": "", 
                "LVal": "3", 
                "EVal": "6", 
                "CVal": "7", 
                "DVal": "126", 
                "Level": "3", 
                "SourceId": "0", 
                "Addtime": "2018/4/12 13:50:04", 
                "adder": "admin", 
                "ProjectID": "61", 
                "TypeName": null, 
                "IndexNum": null, 
                "PlanIdStr": null, 
                "timeSlot": null, 
                "ModelID": "600_943791;600_943577", 
                "LabelPosition": ";;74654.98974609375,-1140.6085020753399,1810079.4375,0.12428700745186749,0,2.65206495665556,-12681.32794392237,-338131.57721118425,1786670.7989467927;74654.98974609375,-1140.6085020753399,1810079.4375,0.12428700745186749,0,2.65206495665556,1869.50225437287,-313416.39965902705,1785264.2014340328"
            }
        ], 
        "detailList": null, 
        "NextUserIds": null, 
        "CopyUserIds": null, 
        "ProjectHazardFlowsDataList": [
            {
                "Lid": "160", 
                "Hid": "105", 
                "SenderId": "495", 
                "SendDate": "2018/9/19 14:20:37", 
                "ExecuteId": "498", 
                "ExecuteDate": "2018/9/19 14:25:12", 
                "Attitude": "同意", 
                "Step": "1", 
                "treat": "同意", 
                "Status": "2", 
                "Note": ""
            }, 
            {
                "Lid": "161", 
                "Hid": "105", 
                "SenderId": "498", 
                "SendDate": "2018/9/19 14:20:37", 
                "ExecuteId": "494", 
                "ExecuteDate": "2018/9/19 14:28:07", 
                "Attitude": "同意", 
                "Step": "1", 
                "treat": "同意", 
                "Status": "2", 
                "Note": ""
            }, 
            {
                "Lid": "162", 
                "Hid": "105", 
                "SenderId": "494", 
                "SendDate": "2018/9/19 14:20:37", 
                "ExecuteId": "495", 
                "ExecuteDate": "2018/9/19 14:28:41", 
                "Attitude": "同意", 
                "Step": "1", 
                "treat": "同意", 
                "Status": "2", 
                "Note": ""
            }
        ], 
        "CopyModelList": [
            {
                "ID": "67", 
                "LID": "161", 
                "HID": "105", 
                "SendUserID": "498", 
                "SendDate": "2018/9/19 14:25:12", 
                "ReceiveUserID": "495", 
                "ExecuteDate": "2018/9/19 14:27:33", 
                "Attitude": "可以按照指定的危险源进行安全监控跟踪", 
                "Status": "2"
            }
        ], 
        "DistinguishProcessResultList": null, 
        "IsEditHazardSource": false, 
        "IsEnd": true
    }
}
```