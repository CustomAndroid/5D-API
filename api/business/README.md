## 业务功能

1. [资料管理](DocumentMng/README.md)
   1. 资料查询
2. [进度管理](Progress/README.md)
   1. 计划查询
   2. 进度填报 
   3. 进度填报审核
   4. 施工日志填报 
3. [安全管理](SafeWork/README.md)
   1. 危险源识别审核，反馈
   2. 危险源识别台账
   3. 危险源监控跟踪
   4. 安全隐患整改审核，反馈
   5. 安全隐患整改台账
4. [问题管理](Problem/README.md)
   1. [POST /api/AppApi/getQualityQuesList 16.查询问题列表](getQualityQuesList.md)
   2. [POST /api/AppApi/getQualityQuesApplList 16.查询问题审核列表](getQualityQuesApplList.md)
   3. [POST /api/AppApi/setQualityQuest 18.问题提报](setQualityQuest.md)
   4. [POST /api/AppApi/getQualityCheckProcess 17.问题审批处理进度](getQualityCheckProcess.md)
   5. POST /api/AppApi/setQualityQuestFJ 19.质量问题提报（附件） --- 【废弃】
   6. POST /api/AppApi/getQualityQuestChart 20.质量问题分析报表-问题分析 --- 【废弃】
   7. POST /api/AppApi/getQualityQuestChartByUnit 21.质量问题分析报表 --- 【废弃】
   8. [POST /api/AppApi/auditingQualityQues 34.质量问题审核;IsFirst:0代表关闭，1代表审核提交](auditingQualityQues.md)
   9. POST /api/AppApi/getQualityQuesListItem  根据问题ID获取问题详情 --- 【此接口暂时无用且返回有问题】
   10. [POST /api/AppApi/GetProblemsByGuid 36根据构件ID查询该构件相关的问题列表](GetProblemsByGuid.md)
5. [材料管理](MaterialMng/README.md) 
   1. 采购台账
   2. 采购登记
   3. 领用台账   
   4. 领用登记
6. [成本管理](CostMng/README.md)
   1. 合同查询
   2. 验工计价
   3. 变更查询
   4. 签证查询

