# 5D-API



1. [目录](README.md)
2. [接口返回通用格式](api/接口返回通用格式.md)
3. [token](api/token.md)
4. [登录，修改密码](api/login/README.md)
    1. [登录](api/login/login.md)
    1. [修改密码](api/login/changePwd.md)
5. [项目基础数据](api/project/README.md)
    1. [项目基本信息](api/project/getProjectInfo.md)
    1. [获取基础数据](api/project/getBaseData.md)
    1. [人员组织机构](api/project/getOrganizatioNew.md)
    1. [获取标段列表(树级结构 id-pId)](api/project/getSectionList.md)
    1. [获取施工单位列表](api/project/getConstUnitList.md)
6. [消息](api/message/README.md)
    1. [待办事项](api/message/getTODOs.md)
    1. [通知公告](api/message/getNotices.md)
    1. [通知公告已读](api/message/updateNotice.md)
    1. [获取项目预警列表](api/message/GetWarnings.md)
    1. [获取相关事项列表](api/message/GetRelevants.md)
    1. [获取未读未处理消息数](api/message/GetMessageNum.md)
7. [电子沙盘](api/bim/README.md)
      8. [模型更新检查](api/bim/checkModels.md)
      2. [查询指定构件相关资料](api/business/DocumentMng/ModelFileList.md)
      3. [查询指定构件ID的属性信息](api/bim/ModelGuidData.md)
8. [业务功能](api/business/README.md)
      1. [资料管理](api/business/DocumentMng/README.md)
         2. [获取资料分类](api/business/DocumentMng/ProjectFileTree.md)
         2. [获取项目资料列表](api/business/DocumentMng/ProjectFileList.md)
         3. [查询指定构件相关资料](api/business/DocumentMng/ModelFileList.md)
      2. [进度管理](api/business/Progress/README.md)
         1. [获取/更新项目施工计划及版本](api/business/Progress/getPlanAndVersion.md)
         1. [获取进度日志填报](api/business/Progress/getPlanProgressInfo.md)
         2. [提交施工日志](api/business/Progress/setPlanSubmitHistory.md)
         3. [获取进度审核列表](api/business/Progress/GetPlanApplData.md)
         4. [根据ID获取进度填报](api/business/Progress/getPlanLogById.md)
         5. [根据ID获取进度审核详情](api/business/Progress/getProgressVerifyLogById.md)
         6. [根据FlowId 查询施工日志审批流程](api/business/Progress/getFlowInfoLogByLogID.md)
         8. [审核施工进度填报](api/business/Progress/auditingPlanLog.md)
         1. [查询施工日志月填报情况](api/business/Progress/GetConstructMonthLogStatus.md)
         2. [查询施工日志详情](api/business/Progress/GetConstructMonthLogInfo.md)
         3. [提交施工日志](api/business/Progress/submitConstructMonthLog.md)
      3. [安全管理](api/business/SafeWork/README.md)
         1. 危险源识别审核，反馈
         2. 危险源识别台账
         3. 危险源监控跟踪
         4. 安全隐患整改审核，反馈
         5. 安全隐患整改台账
      4. [问题管理](api/business/Problem/README.md)
         1. [查询问题列表](api/business/Problem/getQualityQuesList.md)
         2. [查询问题审核列表](api/business/Problem/getQualityQuesApplList.md)
         3. [问题提报](api/business/Problem/setQualityQuest.md)
         4. [问题审批处理进度](api/business/Problem/getQualityCheckProcess.md)
         5. [问题审核;IsFirst:0代表关闭，1代表审核提交](api/business/Problem/auditingQualityQues.md)
         6. [根据构件ID查询该构件相关的问题列表](api/business/Problem/GetProblemsByGuid.md)
      5. [材料管理](api/business/MaterialMng/README.md) 
         1. [采购台账查询](api/business/MaterialMng/GetPurchaseStandingBookList.md)
         2. [领用台账查询](api/business/MaterialMng/GetUseStandingBookList.md)
         3. [材料采购提报](api/business/MaterialMng/submitPurchase.md)
         4. [材料领用提报](api/business/MaterialMng/submitMaterialUse.md)
         5. [材料类别 – 采购领用时的材料清单](api/business/MaterialMng/getMaterialTypeList.md)
         6. [材料采购提报选择材料列表](api/business/MaterialMng/getPurchaseMaterialList.md)
         7. [材料领用提报选择材料清单](api/business/MaterialMng/getUseMaterialList.md)

      6. [成本管理](api/business/CostMng/README.md)
         1. [合同查询](api/business/CostMng/GetContracts.md)
         2. [验工计价查询](api/business/CostMng/GetInspectionPriceList.md)
         3. [ 验工计价明细](api/business/CostMng/GetInspectionPriceContentList.md)
         4. [变更台账查询](api/business/CostMng/GetChangeBook.md)
         5. [签证台账查询](api/business/CostMng/GetVisaStandingBookList.md)

9. [统计报表](api/chart/README.md)
      1. [进度相关](api/chart/Progress/README.md)
            1. [进度与计划完成比](api/chart/Progress/GetScheduleCompletionRatio.md)
            2. [进度与计划完成比 – 图表数据](api/chart/Progress/GetScheduleCompletionRatioCharts.md)
            3. [进度差异分析](api/chart/Progress/GetScheduleVarianceAnalysis.md)
            4. [进度差异分析报表 – 图表数据](api/chart/Progress/GetScheduleVarianceAnalysisCharts.md)
            5. [施工单位进度填报频次](api/chart/Progress/GetUnitFrequencyOfFilling.md)
      2. [成本相关](api/chart/Cost/README.md)
            1. [获取当月收入](api/chart/Cost/GetIncomeStatistics.md)
            2. [获取历史收入](api/chart/Cost/GetIncomeHistory.md)
            3. [获取当月支出](api/chart/Cost/GetExpenditureStatistics.md)
            4. [获取历史支出](api/chart/Cost/GetExpenditureHistory.md)
            5. [获取当月利润](api/chart/Cost/GetProfitStatistics.md)
            6. [获取历史利润](api/chart/Cost/GetProfitHistory.md)
      3. [问题相关](api/chart/Problem/README.md)
            1. [问题统计分析报表](api/chart/Problem/GetStatisticalAnalysisReport.md)
      4. [安全相关](api/chart/Safework/README.md)
            1. [危险源整改通知单报表](api/chart/Safework/GetRiskSourceRectificationNotice.md)
            2. [安全员跟踪统计分析](api/chart/Safework/GetTrackingStatisticalOfSecurityPersonnel.md)
            3. [危险源统计分析](api/chart/Safework/GetStatisticalAnalysisOfHazardSources.md)
      5. [材料相关](api/chart/Material/README.md)
            1. [材料库存量统计](api/chart/Material/GetMaterialIinventoryStatistics.md)
            2. [获取库存材料图标数据](api/chart/Material/GetMaterialStockRecord.md)
10. [其他](api/other/README.md)
        ​    1. [扫描二维码返回构件集合，以#链接](api/other/GetActorIDsByQrNumber.md)

11. [更新日志](log.md)

12. [TODO](TODO.md)



进度管理
​    计划查询、进度/施工日志(?)填报  - ok
​	进度填报审核

成本管理
​    合同查询、验工计价、变更查询、签证查询

安全管理
​	危险源跟踪查询、整改通知单查询
​	危险源跟踪填报、整改通知单填报
​	危险源识别审核、整改通知单审核

问题管理
​    问题查询、问题填报 - ok
​	问题审核

资料管理
​	资料查询 - ok

材料管理 
​	采购台账、领用台账
​	采购登记、领用登记
​	
​	


​	
​	
报表

进度相关
​	进度与计划完成比、进度差异分析、施工单位进度填报频次
​	
成本相关
​	收入统计、收入历史统计、支出统计、支出历史统计、利润统计对比

问题相关
​	问题统计分析报表

安全相关
​	危险源统计分析、安全员跟踪统计分析、危险源整改通知单报表
​	
材料相关
​	材料库存量统计