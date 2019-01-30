## 查询危险源监控跟踪历史详情

> 用于查询危险源监控跟踪历史详情

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetHazardMonitoringTrackingHistoryContent`

### 2. 请求参数

body:

| 字段           | 字段类型 | 必填 | 字段说明                                                     |
| -------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId**  |  String  |  Y   | 项目ID                                                       |
| **userid**     |  String  |  Y   | 用户ID                                                       |
| **keyword**    |  String  |  N   | 关键字                                                       |
| **hazardMTId** |          |      | 危险源监控跟踪历史ID(从[GetHazardMonitoringTrackingHistoryList](GetHazardMonitoringTrackingHistoryList.md)而来，`Logid`) |

示例:

```json
{
  "userid": "496",
  "projectId": "61",
  "keywords": "",
  "hazardMTId": "105"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |
| **ProjectInfo** | Object | 基本信息 |
| **SafetyLibraryList** | Array | 危险源列表 |
| **ProjectLogUserList** | Array | 人员列表 |
| **TotalUser** | String | 人员总数 |
| **Actionshow** | String | 安全活动情况 |
| **equipmentShow** | String | 机械使用情况 |
| **Connet** | String | 施工内容简述 |
| **MajorSecurityRisks** | String | 重大安全隐患 |
| **Other** | String | 其他情况 |
| **ProjectType** | String | 项目类型 |
| **ProjectAddress** | String | 建设地点 |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "ProjectInfo": {
            "peojectName": "贵州马岭河大桥", 
            "projectStartTime": "2017/9/1 0:00:00", 
            "projectEndTime": "2022/12/31 0:00:00", 
            "projectChargePerson": null, 
            "AddressPUA": null, 
            "ProjectCost": null, 
            "ProjectNaturet": null, 
            "ProjectContract": null, 
            "projectInfo": null, 
            "Organization": null, 
            "VideosList": null, 
            "ImgList": null, 
            "ProjectAddress": "贵州省贵阳市南明区"
        }, 
        "SafetyLibraryList": [
            {
                "Sid": "23", 
                "SafeName": "外电防护措施缺乏或不符合要求；", 
                "LibraryIndexList": [
                    {
                        "Iid": "29", 
                        "Sid": null, 
                        "IndexName": "外电防护措施", 
                        "Sort": null, 
                        "AddType": "0", 
                        "Adder": null, 
                        "Addtime": null, 
                        "Isdef": null, 
                        "LibraryIndexValDataList": null, 
                        "ProjectLogConnectModel": {
                            "Tid": null, 
                            "Logid": null, 
                            "ItemName": null, 
                            "ItemVal": "防护措施不到位", 
                            "CheckParts": "标段一", 
                            "isVery": "1", 
                            "isMessage": "1", 
                            "Measures": "1、加强监督检查并立即整改； 2、严格按照规范要求设置外电防护。", 
                            "SafeName": null, 
                            "IndexName": null, 
                            "OrgIDStr": null
                        }
                    }
                ]
            }, 
            {
                "Sid": "24", 
                "SafeName": "接地与接零保护系统不符合要求", 
                "LibraryIndexList": [
                    {
                        "Iid": "32", 
                        "Sid": null, 
                        "IndexName": "接地与接零保护系统", 
                        "Sort": null, 
                        "AddType": "0", 
                        "Adder": null, 
                        "Addtime": null, 
                        "Isdef": null, 
                        "LibraryIndexValDataList": null, 
                        "ProjectLogConnectModel": {
                            "Tid": null, 
                            "Logid": null, 
                            "ItemName": null, 
                            "ItemVal": "接地未按要求设置", 
                            "CheckParts": "标段一", 
                            "isVery": "1", 
                            "isMessage": "1", 
                            "Measures": "1、规范接地与接零保护系统； 2、加强监督检查并立即整改。", 
                            "SafeName": null, 
                            "IndexName": null, 
                            "OrgIDStr": null
                        }
                    }
                ]
            }
        ], 
        "userName": null, 
        "ProjectLogAffixList": null, 
        "ProjectLogModel": {
            "Logid": "79", 
            "projectid": null, 
            "Hid": "95", 
            "rq": "2018/9/19 0:00:00", 
            "Usercode": "495", 
            "Actionshow": "无", 
            "equipmentShow": "无", 
            "Connet": "无", 
            "MajorSecurityRisks": "无", 
            "Other": "无", 
            "ProjectType": "ppp", 
            "adder": "wang1", 
            "addtime": "2018/9/19 14:29:34", 
            "CheckUser": "wang1", 
            "Mid": null, 
            "Mcount": null
        }, 
        "ProjectLogUserList": [
            {
                "Uid": "92", 
                "Projectid": "61", 
                "Logid": "79", 
                "ConstructionUnit": "418", 
                "ManageUsers": "1", 
                "SafeUsers": "1", 
                "isWork": "1", 
                "WorkUsers": "52", 
                "OrgName": "中铁十二局第二公司"
            }
        ], 
        "TotalUser": "54"
    }
}
```