## TODO

### 2019年3月23日

**1** 添加新接口 [查询指定构件ID的自定义属性信息](api/bim/ModelGuidCustomData.md)

 

### 2019年3月4日

**1 ** http://117.34.118.4:9040/api/AppApi/GetWarnings 查询项目预警列表

**[禅道#3394](http://eserver:83/zentao/bug-view-3394.html)**

参数：

``` json
{
  "userId": "609",
  "UserName": "zong bao",
  "projectid": "110",
  "pageIndex": "1",
  "pageSize": "10"
}
```

返回：

``` json
{
    "Code": 1, 
    "CodeMsg": "System.Exception: 列名或所提供值的数目与表定义不匹配。   在 Maticsoft.DBUtility.DbHelperSQL.Query(String SQLString)   在 ConstructionProcessManageAPI.Controllers.AppApiController.GetWarnings(Warnings Pmode)", 
    "Datas": null
}
```

> 注: http://117.34.118.4:9017 上正常

**2**  http://117.34.118.4:9040/api/AppApi/GetConstructMonthLogStatus 
查询施工日志填报状态

**[禅道#3399](http://eserver:83/zentao/bug-view-3399.html)** **[禅道#3405](http://eserver:83/zentao/bug-view-3405.html)**

参数：

``` json
{
  "userid": "610",
  "projectid": "110",
  "ConstructUnitId": "",
  "checkDate": "2019-03-04",
  "UserType": "2"
}
```
返回：
``` json
{
    "Code": 1, 
    "CodeMsg": "System.Exception: 关键字 'and' 附近有语法错误。   在 Maticsoft.DBUtility.DbHelperSQL.Query(String SQLString)   在 ConstructionProcessManageAPI.Controllers.AppApiController.GetConstructMonthLogStatus(tMonthLog Pmodel)", 
    "Datas": null
}
```
导致上面错误是由于 `ConstructUnitId`传空，`ConstructUnitId`来自于 [获取施工单位列表](https://sogrey.github.io/5D-API/book/api/project/getConstUnitList.html).而查询施工单位列表是传参为：
``` json
{
  "userId": "610"
}
```
返回为空：
``` json
{
  "Code": 0,
  "CodeMsg": "ok",
  "Datas": []
}
```
相关bug：**[禅道#3418](http://eserver:83/zentao/bug-view-3418.html)** **[禅道#3401](http://eserver:83/zentao/bug-view-3401.html)** 

**3** http://117.34.118.4:9040/api/AppApi/GetInspectionPriceList 查询验工计价列表

**[禅道#3415 ](http://eserver:83/zentao/bug-view-3415.html)** **[禅道#3406](http://eserver:83/zentao/bug-view-3406.html)**

参数：
``` json
{
  "userId": "609",
  "projectId": "110",
  "startTime": "2019-02-01",
  "endTime": "2019-03-04",
  "unit": "557",
  "Type": "1",
  "UserType": "1"
}
```
返回：
``` json
{
  "Code": 1,
  "CodeMsg": "System.Exception: ',' 附近有语法错误。\r\n   在 Maticsoft.DBUtility.DbHelperSQL.Query(String SQLString)\r\n   在 ConstructionProcessManageAPI.Controllers.AppApiController.GetInspectionPriceList(InspectionPrice Pmode)",
  "Datas": null
}
```

> 注： http://117.34.118.4:9017 上没有报错，但也查询不到数据.
> 参数如下：

http://117.34.118.4:9017/api/AppApi/GetInspectionPriceList

参数：
``` json
  "userId": "524",
  "projectId": "69",
  "startTime": "2019-02-01",
  "endTime": "2019-03-04",
  "unit": "478",
  "Type": "1",
  "UserType": "2"
```
返回：
``` json
{"Code":0,"CodeMsg":"OK","Datas":[]}
```

**4** http://117.34.118.4:9040/api/AppApi/submitMaterialUse 材料领用登记 后平台能查到   App查不到

参数：
``` json
{
  "userId": "539",
  "projectId": "75",
  "useTime": "2019-03-04",
  "materialId": "74",
  "number": "2",
  "usedPart": "123",
  "note": "1"
}
```
返回：
``` json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": null
}
```

http://117.34.118.4:9040/api/AppApi/GetUseStandingBookList 领用登记列表查询

参数：
``` json
{
  "userId": "539",
  "projectId": "75",
  "startTime": "2019-02-01",
  "endTime": "2019-03-04",
  "companyId": "491",
  "Keyword": ""
}
```
返回：
``` json
{"Code":0,"CodeMsg":"OK","Datas":[]}
```

**5**  http://117.34.118.4:9040/api/AppApi/submitPurchase 采购登记 

**[禅道#3402](http://eserver:83/zentao/bug-view-3402.html)**

参数：
``` json
{
  "userid": "539",
  "projectId": "75",
  "buyTime": "2019-03-04",
  "materialId": "71",
  "number": "25",
  "perParice": "26",
  "supplyUnit": "fffbb",
  "note": "xds"
}
```

返回：
``` json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": null
}
```


http://117.34.118.4:9040/api/AppApi/GetPurchaseStandingBookList 查询采购台账查不到已添加的采购数据

参数：
``` json
{
  "userId": "539",
  "projectId": "75",
  "startTime": "2019-02-01",
  "endTime": "2019-03-04",
  "companyId": "491",
  "Keyword": ""
}
```

###  2018年

* ~~2 手机端填报的在平台进度填报显示的填报人是数字~~ \[待回测\]

  > 禅道 [http://eserver:83/zentao/bug-view-3327.html](http://eserver:83/zentao/bug-view-3327.html)
  >
  > [提交施工进度填报](api/business/Progress/setPlanSubmitHistory.md)

* 4 待办、相关事项的问题类型再整理下之前的对不上

  > [待办事项](api/message/getTODOs.md)   [http://117.34.118.4:9017/api/AppApi/getTODOs](http://117.34.118.4:9017/api/AppApi/getTODOs)  中的  FlowType
  >
  > [获取相关事项列表](api/message/GetRelevants.md)  [http://117.34.118.4:9017/api/AppApi/GetRelevants](http://117.34.118.4:9017/api/AppApi/GetRelevants) 中的  Type

* 消息未读、未处理数目与实际未读未处理数目不一致，通知公告可能没有过滤已撤回的公告（4D中出现过）

  > 相关接口api：
  >
  > [获取未读未处理消息数](api/message/GetMessageNum.md)

* 发起问题，相关人查询问题列表其审核权限为1，不能反馈

  > 发起问题接口 [问题提报](api/business/Problem/setQualityQuest.md)
  >
  > api: [http://117.34.118.4:9017/api/AppApi/setQualityQuest](http://117.34.118.4:9017/api/AppApi/setQualityQuest)
  >
  > 查询审核列表 api:[http://117.34.118.4:9017/api/AppApi/getQualityQuesApplList](http://117.34.118.4:9017/api/AppApi/getQualityQuesApplList)
  >
  > [查询问题审核列表](api/business/Problem/getQualityQuesApplList.md)

  myJurisdiction     String  我的审核权限，`0`可审核/反馈，`1`仅查看

  isReView   String  0审核 1反馈

  传入参数：

  ```json
  {
    "userId": "497",
    "pageIndex": "1",
    "startTime": "",
    "endTime": "",
    "level": "",
    "status": "",
    "keyWord": "",
    "pagesize": "20",
    "qid": ""
  }
  ```

* 新增浙江建科院项目部分接口：

  [查询关键路径延期预警 getDelayWarningList](api/business/Progress/getDelayWarningList.md)

  [进度查询 getPlanSchedule](api/business/Progress/getPlanSchedule.md)

  [计划审核列表 getPlanAuditList](api/business/Progress/getPlanAuditList.md)

  [计划审核 submitPlanAudit](api/business/Progress/submitPlanAudit.md)

  [查询计划版本对比 getPlanVersionDiff](api/business/Progress/getPlanVersionDiff.md)

  [获取进度沙盘-形象进度 getGraphicProgress](api/bim/getGraphicProgress.md)

  ~~获取进度沙盘-差异分析 getDifferenceAnalysis   api/bim/getDifferenceAnalysis.md~~

  ~~获取进度沙盘-计划模拟 getPlanningSimulation  api/bim/getPlanningSimulation.md~~

### 记录留用

POST /api/AppApi/GetPlanStaticData

POST /api/AppApi/getQueryStaticData 1:未处理;2:正在处理;3:已完成

POST /api/AppApi/GetProfessionalType 37.获取模型专业类型 树级结构

POST /api/AppApi/AddandWorkFlow

