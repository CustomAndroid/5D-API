## TODO


* 2 手机端填报的在平台进度填报显示的填报人是数字

  ![](http://eserver:83/zentao/data/upload/1/201812/13163852019380f6.png)

    > 禅道 [http://eserver:83/zentao/bug-view-3327.html](http://eserver:83/zentao/bug-view-3327.html)
    >
    > [提交施工进度填报](api/business/Progress/setPlanSubmitHistory.md)


* 4 待办、相关事项的问题类型再整理下之前的对不上

  > [待办事项](api/message/getTODOs.md)   [http://117.34.118.4:9017/api/AppApi/getTODOs](http://117.34.118.4:9017/api/AppApi/getTODOs)  中的  FlowType
  >
  >
  > [获取相关事项列表](api/message/GetRelevants.md)  http://117.34.118.4:9017/api/AppApi/GetRelevants 中的  Type
  >

* 消息未读、未处理数目与实际未读未处理数目不一致，通知公告可能没有过滤已撤回的公告（4D中出现过）

  >相关接口api：
  >
  >[获取未读未处理消息数](api/message/GetMessageNum.md)

* 发起问题，相关人查询问题列表其审核权限为1，不能反馈

  >发起问题接口 [问题提报](api/business/Problem/setQualityQuest.md)
  >
  >api: http://117.34.118.4:9017/api/AppApi/setQualityQuest
  >
  >
  >
  >查询审核列表 api:http://117.34.118.4:9017/api/AppApi/getQualityQuesApplList
  >
  >[查询问题审核列表](api/business/Problem/getQualityQuesApplList.md)

  myJurisdiction     String  我的审核权限，`0`可审核/反馈，`1`仅查看

  isReView   String  0审核 1反馈

  传入参数：

  ``` json
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

  ~~[获取进度沙盘-差异分析 getDifferenceAnalysis](api/bim/getDifferenceAnalysis.md)~~

  ~~[获取进度沙盘-计划模拟 getPlanningSimulation](api/bim/getPlanningSimulation.md)~~

  [获取进度沙盘-形象进度 getGraphicProgress](api/bim/getGraphicProgress.md)



### 记录留用

POST /api/AppApi/GetPlanStaticData

POST /api/AppApi/getQueryStaticData 1:未处理;2:正在处理;3:已完成

POST /api/AppApi/GetProfessionalType 37.获取模型专业类型 树级结构

POST /api/AppApi/AddandWorkFlow

