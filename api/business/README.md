## 业务功能

1. [资料管理](DocumentMng/README.md)

   1. [POST /api/AppApi/ProjectFileTree  获取资料分类](DocumentMng/ProjectFileTree.md)
   2. [POST /api/AppApi/ProjectFileList 获取项目资料列表](DocumentMng/ProjectFileList.md)
   3. [POST /api/AppApi/ModelFileList FileAttributive:1标示项目资料，2标示构件资料](DocumentMng/ModelFileList.md)
2. [进度管理](Progress/README.md)

   施工计划：

     1. [POST /api/AppApi/getPlanAndVersion 获取/更新项目施工计划及版本](Progress/getPlanAndVersion.md)

   进度填报：

     1. [POST /api/AppApi/getPlanProgressInfo 获取进度日志填报](Progress/getPlanProgressInfo.md)
     2. [POST /api/AppApi/setPlanSubmitHistory 提交施工日志](Progress/setPlanSubmitHistory.md)
     3. [POST /api/AppApi/GetPlanApplData 获取进度审核列表](Progress/GetPlanApplData.md)
     4. [POST /api/AppApi/getPlanLogById 32.根据ID获取进度填报](Progress/getPlanLogById.md)
     5. [POST /api/AppApi/getProgressVerifyLogById 38.根据ID获取进度审核详情](Progress/getProgressVerifyLogById.md)
     6. [POST /api/AppApi/getFlowInfoLogByLogID 根据FlowId 查询施工日志审批流程](Progress/getFlowInfoLogByLogID.md)
     7. [POST /api/AppApi/auditingPlanLog 33.审核施工进度填报](Progress/auditingPlanLog.md)

   施工日志：

     1. [POST /api/AppApi/GetConstructMonthLogStatus 82.查询施工日志月填报情况](Progress/GetConstructMonthLogStatus.md)
     2. [POST /api/AppApi/GetConstructMonthLogInfo 83.查询施工日志详情](Progress/GetConstructMonthLogInfo.md)
     3. [POST /api/AppApi/submitConstructMonthLog 84.提交施工日志](Progress/submitConstructMonthLog.md)
     4. [POST /api/AppApi/GetconstructionSites 查询具体日期施工部位列表](Progress/GetconstructionSites.md)

3. [安全管理](SafeWork/README.md)

   危险源识别：

   1. [POST /api/AppApi/getHazardIdentificationAuditList 71.危险源识别审核列表](SafeWork/getHazardIdentificationAuditList.md)
   2. [POST /api/AppApi/getHazardIdentificationInfo 72.危险源识别详情](SafeWork/getHazardIdentificationInfo.md)
   3. [POST /api/AppApi/AuditingHazardDistinguish 39.危险源识别审核](SafeWork/AuditingHazardDistinguish.md)
   4. [POST /api/AppApi/GetHazardIdentificationVerificationProcess 81.查询危险源识别审核流程](SafeWork/GetHazardIdentificationVerificationProcess.md)
   5. [POST /api/AppApi/GetHazardSourceDistinguishLog 85.查询危险源识别台账列表](SafeWork/GetHazardSourceDistinguishLog.md)

   危险源监控跟踪:

   1. [POST /api/AppApi/GetHazardMonitoringTrackingList 40.危险源监控跟踪列表](SafeWork/GetHazardMonitoringTrackingList.md)
   2. [POST /api/AppApi/GetHazardMonitoringTrackingHistoryList 41危险源监控跟踪历史](SafeWork/GetHazardMonitoringTrackingHistoryList.md)
   3. [POST /api/AppApi/GetHazardMonitoringTrackingHistoryContent 42.危险源监控跟踪历史详情](SafeWork/GetHazardMonitoringTrackingHistoryContent.md)

   安全整改通知单：

   1. [POST /api/AppApi/GetSafetyRectificationNoticeList 46.获取安全整改通知单列表](SafeWork/GetSafetyRectificationNoticeList.md)
   2. [POST /api/AppApi/GetSafetyRectificationNoticeProcess 47.获取安全整改通知单审核流程](SafeWork/GetSafetyRectificationNoticeProcess.md)
   3. [POST /api/AppApi/AuditingSafetyRectificationNotice 49.整改通知单审核](SafeWork/AuditingSafetyRectificationNotice.md)
   4. [POST /api/AppApi/GetHazardSourceMassageLog 86.查询安全隐患整改通知单台账列表](SafeWork/GetHazardSourceMassageLog.md)
   5. [POST /api/AppApi/NewSafetyRectificationNotice 48.根据ID查询/新建安全整改通知单](SafeWork/NewSafetyRectificationNotice.md)

4. [问题管理](Problem/README.md)
   1. [POST /api/AppApi/getQualityQuesList 16.查询问题列表](Problem/getQualityQuesList.md)
   2. [POST /api/AppApi/getQualityQuesApplList 16.查询问题审核列表](Problem/getQualityQuesApplList.md)
   3. [POST /api/AppApi/setQualityQuest 18.问题提报](Problem/setQualityQuest.md)
   4. [POST /api/AppApi/getQualityCheckProcess 17.问题审批处理进度](Problem/getQualityCheckProcess.md)
   5. ~~POST /api/AppApi/setQualityQuestFJ 19.质量问题提报（附件）~~ --- 【废弃】
   6. ~~POST /api/AppApi/getQualityQuestChart 20.质量问题分析报表-问题分析~~ --- 【废弃】
   7. ~~POST /api/AppApi/getQualityQuestChartByUnit 21.质量问题分析报表~~ --- 【废弃】
   8. [POST /api/AppApi/auditingQualityQues 34.质量问题审核;IsFirst:0代表关闭，1代表审核提交](Problem/auditingQualityQues.md)
   9. POST /api/AppApi/getQualityQuesListItem  根据问题ID获取问题详情 --- 【此接口暂时无用且返回有问题】
   10. [POST /api/AppApi/GetProblemsByGuid 36根据构件ID查询该构件相关的问题列表](Problem/GetProblemsByGuid.md)
5. [材料管理](MaterialMng/README.md) 

   6. [POST /api/AppApi/GetPurchaseStandingBookList 62.采购台账查询](MaterialMng/GetPurchaseStandingBookList.md)
   2. [POST /api/AppApi/GetUseStandingBookList 63.领用台账查询](MaterialMng/GetUseStandingBookList.md)
   3. [POST /api/AppApi/submitPurchase 73.材料采购提报](MaterialMng/submitPurchase.md)
   4. [POST /api/AppApi/submitMaterialUse 74.材料领用提报](MaterialMng/submitMaterialUse.md)
   5. [POST /api/AppApi/getMaterialTypeList 75.材料类别 – 采购领用时的材料清单](MaterialMng/getMaterialTypeList.md)
   6. [POST /api/AppApi/getPurchaseMaterialList 76.材料采购提报选择材料列表](MaterialMng/getPurchaseMaterialList.md)
   7. [POST /api/AppApi/getUseMaterialList 77.材料领用提报选择材料清单](MaterialMng/getUseMaterialList.md)

6. [成本管理](CostMng/README.md)

   7. [POST /api/AppApi/GetContracts 59. 合同查询](CostMng/GetContracts.md)
   2. [POST /api/AppApi/GetInspectionPriceList 60.验工计价查询](CostMng/GetInspectionPriceList.md)
   3. [POST /api/AppApi/GetInspectionPriceContentList 验工计价明细](CostMng/GetInspectionPriceContentList.md)
   4. [POST /api/AppApi/GetChangeBook 59.变更台账查询](CostMng/GetChangeBook.md)
   5. [POST /api/AppApi/GetVisaStandingBookList 61.签证台账查询](CostMng/GetVisaStandingBookList.md)