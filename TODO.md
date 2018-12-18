## TODO

<<<<<<< HEAD
=======
* 1 发起协同问题给相关人，平台上相关人未收到，

  > 禅道：[http://eserver:83/zentao/bug-view-3330.html](http://eserver:83/zentao/bug-view-3330.html)
  >
  > [问题提报](api/business/Problem/setQualityQuest.md)
  >
  > api: [http://117.34.118.4:9017/api/AppApi/setQualityQuest](http://117.34.118.4:9017/api/AppApi/setQualityQuest)

  ```
  "copyTo": "495",     <----- 这个字段
  ```

  ```json
    {
      "userId": "496",
      "title": "测试问题12",
      "arisesTime": "2018-12-18",
      "quesType": "1",
      "guid": "600_1111654,600_943832",
      "level": "2",
      "desc": "描述啦12",
      "sendTo": "494",
      "copyTo": "495",   
      "ProTree": "",
      "ProTreeData": "",
      "Post": "",
      "ProjectId": "61",
      "LableLocation": "74654.98974609375,290820.966796875,1810079.4375,0.7853981633974483,0,0.7853981633974483,92813.44214218613,172072.3669942927,1743687.0864398812",
      "FileLists": "/uploadFile/attachment/EF_20181218_152821382.png:当前问题所在",
      "TempId": "tmp_1545118013888",
      "Viewpoint": "74654.98974609375,290820.966796875,1810079.4375,0.7853981633974483,0,0.7853981633974483"
    }
  ```

    返回

    ``` json
     {"Code":0,"CodeMsg":"OK","Datas":{"Id":"122","LId":"198","TempId":"tmp_1545118013350"}}
    ```

>>>>>>> fe1b3459dbd520553277db0c4500141ccb2dd37a
* 2 手机端填报的在平台进度填报显示的填报人是数字

![](http://eserver:83/zentao/data/upload/1/201812/13163852019380f6.png)

> 禅道 [http://eserver:83/zentao/bug-view-3327.html](http://eserver:83/zentao/bug-view-3327.html)
>
> [提交施工进度填报](api/business/Progress/setPlanSubmitHistory.md)

<<<<<<< HEAD
=======
* 3 查询分包验工计价台账报错

  > [验工计价查询](api/business/CostMng/GetInspectionPriceList.md)
  >
  > api [http://117.34.118.4:9017/api/AppApi/GetInspectionPriceList](http://117.34.118.4:9017/api/AppApi/GetInspectionPriceList)

  * "unit": "418",  &lt;-  分包单位ID，查询总包时没有
  *  "Type": "1",    &lt;-  1分包 0总包

  ```json
  {
  "userId": "496",
  "projectId": "61",
  "startTime": "2018-11-01",
  "endTime": "2018-12-18",
  "unit": "418", 
  "Type": "1",   
  "UserType": "2"
  }
  ```

  返回

  ```json
  {"Code":1,"CodeMsg":"System.Exception: ',' 附近有语法错误。\r\n   在 Maticsoft.DBUtility.DbHelperSQL.Query(String SQLString)\r\n   在 ConstructionProcessManageAPI.Controllers.AppApiController.GetInspectionPriceList(InspectionPrice Pmode)","Datas":null}
  ```
>>>>>>> fe1b3459dbd520553277db0c4500141ccb2dd37a

* 4 待办、相关事项的问题类型再整理下之前的对不上

  > [待办事项](api/message/getTODOs.md)   [http://117.34.118.4:9017/api/AppApi/getTODOs](http://117.34.118.4:9017/api/AppApi/getTODOs)  中的  FlowType
  >
<<<<<<< HEAD
  >
  > [获取相关事项列表](api/message/GetRelevants.md)  http://117.34.118.4:9017/api/AppApi/GetRelevants 中的  Type

​    

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

=======
  > [获取相关事项列表](api/message/GetRelevants.md)  [http://117.34.118.4:9017/api/AppApi/GetRelevants](http://117.34.118.4:9017/api/AppApi/GetRelevants) 中的  Type
>>>>>>> fe1b3459dbd520553277db0c4500141ccb2dd37a

​

### 记录留用

POST /api/AppApi/GetPlanStaticData

POST /api/AppApi/getQueryStaticData 1:未处理;2:正在处理;3:已完成

POST /api/AppApi/GetProfessionalType 37.获取模型专业类型 树级结构

POST /api/AppApi/AddandWorkFlow

