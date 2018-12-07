## 更新日志

<!--sec data-title="2018-11-30" data-id="20181130" data-show=true ces-->

* [A] 增加**[业务功能](api/business/README.md)-[材料管理](api/business/MaterialMng/README.md)**的**7**个接口文档
* [U] 关联**[引擎二次开发简易API](api/other/README.md)**
* [A] 增加**[业务功能](api/business/README.md)-[安全管理](api/business/SafeWork/README.md)**的**12**个接口文档

<!--endsec-->

<!--sec data-title="2018-12-03" data-id="20181203" data-show=true ces-->

* [A] 增加接口**[查询具体日期施工部位列表](api/business/Progress/GetconstructionSites.md)**
* [U] 更新**[登录](api/login/login.md)**，返回增加**`roleData`**字段用于菜单权限动态控制
* [A] 增加接口**[查询危险源识别审核流程](api/business/SafeWork/GetHazardIdentificationVerificationProcess.md)**

<!--endsec-->

<!--sec data-title="2018-12-07" data-id="20181203" data-show=true ces-->

- [R] 废弃~~[查询危险源识别详情-危险源列表](api/business/SafeWork/getHazardIdentificationInfo.md)~~，被[查询危险源识别详情+审核流程](api/business/SafeWork/GetHazardIdentificationVerificationProcess.md)取代
- [R] 废弃~~[查询具体日期施工部位列表（施工日志）](api/business/Progress/GetconstructionSites.md)~~,被[查询施工日志详情](api/business/Progress/GetConstructMonthLogInfo.md)替代
- [U] 更新[查询施工日志详情](api/business/Progress/GetConstructMonthLogInfo.md)添加`PlanTaskList`字段未填报时查询相关施工任务

<!--endsec-->