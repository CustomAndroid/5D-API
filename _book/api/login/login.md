## 用户登录

> 获取个人基本信息和项目基本信息 - 以及项目最新模型文件下载地址及版本（多个文件，列表） -- 模型添加到下载+版本管理

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/login`

### 2. 请求参数

header:

| 字段              | 字段类型 | 必填 | 字段说明                                                     |
| ----------------- | :------: | :--: | ------------------------------------------------------------ |
| **Authorization** |  String  |  Y   | `Bearer+空格+access_token`,其中`access_token`来自于[token](../token.md)接口 |

body:

| 字段         | 字段类型 | 必填 | 字段说明        |
| ------------ | :------: | :--: | --------------- |
| **userName** |  String  |  Y   | 用户名          |
| **password** |  String  |  Y   | 密码（MD5加密） |

示例:

```json
{
  "userName": "string",
  "password": "string"
}
```

### 3. 返回参数

| 字段                   | 字段类型 | 字段说明                                                     |
| ---------------------- | :------: | ------------------------------------------------------------ |
| **userId**             |  string  | 用户ID                                                       |
| **userName**           |  String  | 登录名                                                       |
| **userOrganizationId** |  String  | 当前登录人所在单位组织ID                                     |
| **userOrganization**   |  String  | 当前登录人所在单位组织名称                                   |
| **userPosition**       |  String  | 当前登录人角色名称                                           |
| **userPositionid**     |  String  | 当前登录人角色ID                                             |
| **projectName**        |  String  | 当前项目名称                                                 |
| **projectId**          |  String  | 当前项目ID                                                   |
| **projectSection**     |  String  |                                                              |
| **projectPlanType**    |  String  | 计划类型：4月计划，5旬计划，6周计划，7日计划，可组合使用：比如457表示该项目制定了月计划旬计划和周计划 |
| **WebNetIPAndPort**    |  String  | 平台地址                                                     |
| **userNameText**       |  String  | 当前登录人姓名                                               |
| **FTPAddress**         |  String  | ftp地址                                                      |
| **FTPPort**            |  String  | ftp端口                                                      |
| **FTPUser**            |  String  | ftp登录名                                                    |
| **FTPPassword**        |  String  | ftp密码                                                      |
| **roleData**           |  String  | 菜单动态权限。多个`,`间隔，对应平台上菜单`SystemName`        |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "ok", 
    "Datas": {
        "userId": "496", 
        "userName": "wang2", 
        "userOrganization": "中铁十二局第二公司", 
        "userOrganizationID": "418", 
        "userPosition": "施工负责人", 
        "userPositionid": "2", 
        "projectName": "贵州马岭河大桥", 
        "projectId": "61", 
        "projectSection": "", 
        "projectPlanType": "457", 
        "models": null, 
        "Special": null, 
        "WebNetIPAndPort": "http://xxx.xxx.xxx.xxx:xxxx/", 
        "userNameText": "wang2", 
        "FTPAddress": "xxx.xxx.xxx.xxx",
        "FTPPort": "xxxx",
        "FTPUser": "xxxxxx", 
        "FTPPassword": "xxxxxxxxxxxx", 
        "roleData": "Mydesktop,StayHandle,EarlyWarning,MessageRemind,ProjectStatus,ProgressAnalysis,CostAnalysis,SafeAnalysis,MaterialAnalysis,DataAnalysis,ProblemAnalysis,ProjectMangageSystemSettings,ProjectMangageBasicInformation,OA_NoticeListShow,OA_NoticeList,OA_NoticeListManage,ElectronicSandBox,BasisSandBox,ProgressSandBox,3DVisualization,OverallServiceSandBox,OverallSandBox,QRCodeSandBox,ProjectPlanManagement,PlanTakPreview,ConstructionLog,ProjectDelayWarn,CostManage,PerfectMaterialEdit,PerfectMaterialQuery,ContractControlList,ChangeControl,ChangeManagement,ChangeManagementDo,ChangeManagementView,ChangeManagementModel,VisaControl,VisaManagement,VisaManagementDo,VisaManagementView,InspectionPrice,SubInspectionPriceList,Payment,SubPaymentConstruction,Payment,SubIncomeLedger,CostControl,Equipment,EquipmentList,EquipmentUsageLedger,ManagementCost,OfficeSupplies,TransportationFee,StaffSalary,OtherFee,ProjectHazardSourceDistinguishManage,ProjectHazardSourceDistinguishList,ProjectHazardSourceDistinguishHandleList,ProjectHazardSourceDistinguishFeedBackList,ProjectHazardSourceMonitorList,ProjectHazardSourceMassageList,ProjectHazardSourceMassageHandleList,ProjectHazardSourceMassageFeedBackList,ProjectHazardSourceMassageLog,SubcontractSecurityCivilizationItem,SpecialEquipmentEntryRegistration,SpecialPersonnelRegistration,QualityControl,QualityControlList,QualityControlListDo,QualityControlListFeedBack,QualityControlAnalysis,ProjectModelFilesManagement,PlatformAdministratorPublicInfo,PlatformAdministratorPublicInfoType,PlatformAdministratorPublicInfoList,ProjectModelFilesType,ProjectModelFilesData,ProjectModelFilesAdd,ProjectModelFilesUpdate,ProjectModelFilesDelete,ProjectModelFilesDataView,MaterialControl,MaterialList,PurchaseMaterial,MaterialUse,StatisticsCenter,UserStat,ProgressCompareStat,ProgressDiffStat,PlanProgressWriteReport,CostControlStatistics,IncomeStatistics,IncomeHistory,ExpenditureStatistics,ExpenditureHistory,ProfitStatistics,ProblemStatisReport,SafeLibraryMointorReport,SafeWorkerMonitorReport,SafeMessageReport,MaterialStockStat,User,UserInfo,ChangePwd,ConstructionPlanControl,ConstructionPlanControlList,ConstructionPlanControlListDo,ConstructionPlanControlListFeedBack,ConstructionPlanControlAnalysis,ConstructionProcessControl,ConstructionProcessControlList,ConstructionProcessControlListDo,ConstructionProcessControlListFeedBack,ConstructionProcessControlAnalysis,Mydesktop,PlatformAdministratorChangePwd"
    }
}
```
