## TODO

- **1** 查询危险源识别审核流程接口报错

    > **API**:http://117.34.118.4:9017/swagger/ui/index#!/AppApi/AppApi_GetHazardIdentificationVerificationProcess
    >
    > **URL**:http://117.34.118.4:9017/api/AppApi/GetHazardIdentificationVerificationProcess
    > **参数**：
    > 
    >    ``` json
    >    {
    >      "userId": "494",
    >      "projectId": "61",
    >      "hid": "107"
    >    }
    >    ```
    >
    >    返回：
    >
    >   ``` json
    >   {
    >   "Code": 1,
    >   "CodeMsg": "System.NullReferenceException: 未将对象引用设置到对象的实例。\r\n   在 ConstructionProcessManageAPI.Controllers.AppApiController.GetHazardIdentificationVerificationProcess(HazardId Pmodel)",
    >   "Datas": null
    >   }
    >   ```

- **2** 新增[查询具体日期施工部位列表](api/business/Progress/GetconstructionSites.md)

- **3** 施工日志提交接口开发
    文档:

    > https://sogrey.gitbooks.io/5d-api/content/api/business/Progress/submitConstructMonthLog.html






### 记录留用

POST /api/AppApi/GetPlanStaticData

POST /api/AppApi/getQueryStaticData 1:未处理;2:正在处理;3:已完成

POST /api/AppApi/GetProfessionalType 37.获取模型专业类型 树级结构

POST /api/AppApi/AddandWorkFlow
