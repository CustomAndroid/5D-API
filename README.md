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
7. [模型更新检查](api/bim/checkModels.md)
8. [业务功能](api/business/README.md)
9. [统计报表](api/chart/README.md)
	1. [进度相关](api/chart/Progress/README.md)
        1. [进度与计划完成比](api/chart/Progress/GetScheduleCompletionRatio.md)
        1. [进度与计划完成比 – 图表数据](api/chart/Progress/GetScheduleCompletionRatioCharts.md)
        1. [进度差异分析](api/chart/Progress/GetScheduleVarianceAnalysis.md)
        1. [进度差异分析报表 – 图表数据](api/chart/Progress/GetScheduleVarianceAnalysisCharts.md)
        1. [施工单位进度填报频次](api/chart/Progress/GetUnitFrequencyOfFilling.md)
	1. [成本相关](api/chart/Cost/README.md)
        1. [获取当月收入](api/chart/Cost/GetIncomeStatistics.md)
        1. [获取历史收入](api/chart/Cost/GetIncomeHistory.md)
        1. [获取当月支出](api/chart/Cost/GetExpenditureStatistics.md)
        1. [获取历史支出](api/chart/Cost/GetExpenditureHistory.md)
        1. [获取当月利润](api/chart/Cost/GetProfitStatistics.md)
        1. [获取历史利润](api/chart/Cost/GetProfitHistory.md)
	1. [问题相关](api/chart/Problem/README.md)
		1. [问题统计分析报表](api/chart/Problem/GetStatisticalAnalysisReport.md)
	1. [安全相关](api/chart/Safework/README.md)
        1. [危险源整改通知单报表](api/chart/Safework/GetRiskSourceRectificationNotice.md)
        1. [安全员跟踪统计分析](api/chart/Safework/GetTrackingStatisticalOfSecurityPersonnel.md)
        1. [危险源统计分析](api/chart/Safework/GetStatisticalAnalysisOfHazardSources.md)
	1. [材料相关](api/chart/Material/README.md)
        1. [材料库存量统计](api/chart/Material/GetMaterialIinventoryStatistics.md)
        1. [获取库存材料图标数据](api/chart/Material/GetMaterialStockRecord.md)
10. [其他](api/other/README.md)
	1. [扫描二维码返回构件集合，以#链接](api/other/GetActorIDsByQrNumber.md)
11. [更新日志](log.md)
12. [TODO](TODO.md)




消息

	待办事项、项目预警、相关事项、通知公告

电子沙盘

项目详情

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