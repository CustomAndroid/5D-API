## 通知公告列表

> 获取通知公告列表

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getNotices`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **userid**    |  String  |  Y   | 用户ID   |
| **projectid** |  String  |  Y   | 项目ID   |
| **pageIndex** |  String  |  Y   | 页码     |
| **pageSize**  |  String  |  Y   | 每页条数 |

示例:

```json
{
  "userid": "494",
  "projectid": "61",
  "pageIndex": "1",
  "pageSize": "20"
}
```

### 3. 返回参数

| 字段           | 字段类型 | 字段说明                             |
| -------------- | :------: | ------------------------------------ |
| **caseid**     |  string  | ID                                   |
| **addTime**    |  String  | 时间                                 |
| **isReaded**   |  String  | 是否已读，1 已读/已完成 0未读/待完成 |
| **noticeName** |  String  | 标题                                 |
| **content**    |  String  | 内容                                 |
| **source**     |  String  | 发起者                               |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "noticeName": "马岭河大桥工程启动仪式",
      "addTime": "2018-09-06",
      "source": "王萌",
      "content": "<p><span style=\"color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; background-color: rgb(255, 255, 255);\">&nbsp; &nbsp; &nbsp; &nbsp;马岭河大桥工程前期工作在马岭镇启动，州、市领导出席启动仪式。黔西南州委书记张政宣布项目启动。</span><br style=\"box-sizing: content-box; color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; white-space: normal; background-color: rgb(255, 255, 255);\"/><span style=\"color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; background-color: rgb(255, 255, 255);\">　　马岭河大桥工程位于马岭河中游，距马岭镇政府驻地3公里，坝址距兴义市城区16公里，是贵州省三大水利枢纽之一。</span><br style=\"box-sizing: content-box; color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; white-space: normal; background-color: rgb(255, 255, 255);\"/><span style=\"color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; background-color: rgb(255, 255, 255);\">　　马岭河大桥工程的任务是以城乡供水为主，结合灌溉，兼顾发电等综合利用，工程主体为水源工程和供水灌溉工程两部分，其中水源工程包含碾压混凝土双曲拱坝及坝身泄洪系统，右岸引水发电系统;供水灌溉工程包含右岸城市供水工程、左岸城乡供水工程及左岸灌溉工程。工程建成后多年平均供水量2.11亿立方米，设计灌溉面积1.32万亩，多年平均发电量1.14亿千瓦时。</span><br style=\"box-sizing: content-box; color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; white-space: normal; background-color: rgb(255, 255, 255);\"/><span style=\"color: rgb(51, 51, 51); font-family: &quot;Helvetica Neue&quot;, Helvetica, Arial, sans-serif; font-size: 14px; background-color: rgb(255, 255, 255);\">　　坝址以上集水面积1914平方公里，多年平均流量每小时43.6立方米;水库校核洪水位1032.58米，正常蓄水位1030米，死水位985米，最大坝高92米，总库容1.32亿立方米，兴利调节库容1.07亿立方米，死库容0.13亿立方米，坝后电站装机3.6万千瓦。右岸城市供水工程由两级泵站和两条供水管道组成，总扬程307米，输水干管总长8.53公里，左岸城乡供水工程由三级泵站、两个支管加压泵站和灌溉输水渠、供水管道组成，总扬程401.5米，供水干管总长12.97公里;灌溉渠道总长11.34公里，与左岸城乡供水共用第一级泵站提水，提水扬程156.5米。工程规模为大二型，估算工程静态总投资231478万元。(通讯员 晏金国 鲍灵芝报道)</span></p>",
      "isReaded": "0",
      "caseid": "152"
    }
  ]
}
```

