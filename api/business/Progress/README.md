## 进度管理

1. 计划查询
2. 进度填报 
3. 进度填报审核
4. 施工日志填报 

* [POST /api/AppApi/submitConstructMonthLog 84.提交施工日志](submitConstructMonthLog.md)











POST /api/AppApi/GetConstructMonthLogStatus 82.查询施工日志月填报情况,checkDate:格式传yyyy-mm-dd
POST /api/AppApi/GetConstructMonthLogInfo 83.查询施工日志详情 checkDate:格式传yyyy-mm-dd
POST /api/AppApi/submitConstructMonthLog 84.提交施工日志(暂无实现)



POST /api/AppApi/getPlanAndVersion 获取/更新项目施工计划及版本
POST /api/AppApi/getPlanProgressInfo 获取进度日志填报
POST /api/AppApi/setPlanSubmitHistory 提交施工日志
POST /api/AppApi/GetPlanApplData 获取进度审核列表
POST /api/AppApi/AddandWorkFlow

POST /api/AppApi/getFlowInfoLogByLogID
POST /api/AppApi/getPlanLogById 32.根据ID获取进度填报
POST /api/AppApi/auditingPlanLog 33.审核施工进度填报;Type:1代表审核结束；0:代表审核并发送下一人;logId:审核第几步ID;idea:1同意 2不同意



POST /api/AppApi/getProgressVerifyLogById 38.根据ID获取进度审核详情