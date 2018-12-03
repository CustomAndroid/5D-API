## TODO

- [ ] **1** 查询施工日志详情，日志未填写，但计划施工部位（R_Construction_logDetailsModelList）有一条 接口未返回，另 IsCanEdit =false 是不可编辑吗

    > http://117.34.118.4:9017/api/AppApi/GetConstructMonthLogInfo
    参数：
    ``` json
    {
      "userid": "496",
      "projectid": "61",
      "ConstructUnitId": "418",
      "checkDate": "2018-11-27",
      "UserType": "2"
    }
    ```
    返回:
    ``` json
    {
      "Code": 0,
      "CodeMsg": "OK",
      "Datas": {
        "R_Construction_logModel": null,
        "R_Construction_logFileModelList": null,
        "R_Construction_logDetailsModelList": null,
        "PlanTaskList": null,
        "jsonYMD": null,
        "ConstructionUnitName": null,
        "FilePathAndName": null,
        "LogDetails": null,
        "userType": null,
        "IsCanEdit": false
      }
    }
    ```


- [ ] **2** 查询危险源识别审核流程接口报错
    > http://117.34.118.4:9017/api/AppApi/GetHazardIdentificationVerificationProcess
    参数：
    ``` json
    {
      "userId": "496",
      "projectId": "61",
      "hid": "109"
    }
    ```
    返回：
    ``` json
    {
      "Code": 1,
      "CodeMsg": "System.NullReferenceException: 未将对象引用设置到对象的实例。\r\n   在 ConstructionProcessManageAPI.Controllers.AppApiController.GetHazardIdentificationVerificationProcess(HazardId Pmodel)",
      "Datas": null
    }
    ```

- [ ] **3**【PC】危险源识别审核时没有审核结果，那平台上是不是要将审核结果去掉
    > http://117.34.118.4:9017/api/AppApi/AuditingHazardDistinguish
    > 
    > http://117.34.118.4:8095/Safety/HazardSourceDistinguishHandleList#HazardSourceDistinguishHandleList

- [ ] **4** 危险源识别台账列表 - 分页无效
    > http://117.34.118.4:9017/api/AppApi/GetHazardSourceDistinguishLog
    参数：
    ``` json
    {
      "userId": "495",
      "projectId": "61",
      "pageIndex": "10",
      "pageSize": "5",//页码
      "startTime": "",
      "endTime": "",
      "keyword": ""
    }
    ```

- [ ] **5** 施工日志提交接口开发
    文档:

    > https://sogrey.gitbooks.io/5d-api/content/api/business/Progress/submitConstructMonthLog.html

- [ ] **6** [登录接口](api/login/login.md)增加菜单权限字段，平台上控制菜单`SystemName`多个用`,`间隔，字段名可命名为 `SystemNames`

- [ ] **7** 新增[查询具体日期施工部位列表](api/business/Progress/GetconstructionSites.md)



### 记录留用

POST /api/AppApi/GetPlanStaticData

POST /api/AppApi/getQueryStaticData 1:未处理;2:正在处理;3:已完成

POST /api/AppApi/GetProfessionalType 37.获取模型专业类型 树级结构

POST /api/AppApi/AddandWorkFlow
