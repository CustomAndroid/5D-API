## 项目基本信息

> 用于项目基本信息

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getProjectInfo`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **userId**    |  String  |  Y   | 用户ID   |
| **Projectid** |  String  |  Y   | 项目ID   |

示例:

```json
{
  "userId": "496",
  "Projectid": "61"
}
```

### 3. 返回参数

| 字段                    | 字段类型 | 字段说明                    |
| ----------------------- | :------: | --------------------------- |
| **peojectName**         |  string  | 项目名称                    |
| **projectStartTime**    |  String  | 项目开启时间                |
| **projectEndTime**      |  String  | 项目截止时间                |
| **projectChargePerson** |  String  | 项目负责人                  |
| **AddressPUA**          |  String  | 地址                        |
| **ProjectCost**         |  String  | 项目造价                    |
| **ProjectNaturet**      |  String  | 项目性质                    |
| **ProjectContract**     |  String  | 项目总承包单位              |
| **projectInfo**         |  String  | 项目简介                    |
| **Organization**        |  Object  | 各参建单位,多个单位 `,`间隔 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": {
    "peojectName": "贵州马岭河大桥",
    "projectStartTime": "2017-09-01",
    "projectEndTime": "2022-12-31",
    "projectChargePerson": "王猛",
    "AddressPUA": "贵州省贵阳市南明区",
    "ProjectCost": "12000000000.00",
    "ProjectNaturet": "桥梁",
    "ProjectContract": "",
    "projectInfo": "<p style=\"line-height: 1.5em;\">&nbsp; &nbsp;&nbsp;<img src=\"http://117.34.118.4:8095/uEdit/upload/image/20180906/6367182510546903753117681.jpg\" width=\"277\" height=\"150\" style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; white-space: normal; width: 277px; height: 150px; float:left; margin:0 10px 10px 0;\"/> &nbsp;<span style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; background-color: rgb(255, 255, 255);\">兴义马岭河大桥位于贵州省兴义市马岭河大峡谷，该桥全长1386米，最高塔高196米，为预应力混凝土双塔双索面斜拉桥，是现目前贵州省内建成的第一座也是最大一座三跨预应力混凝土双塔双索面斜拉桥（主桥为155+360+155m，引桥采用40m（1跨）、50m（13跨）预应力混凝土预制T梁先简支后刚构体系），大桥左幅全长1386m，右幅全长1367.5m。</span>&nbsp; &nbsp;</p><p style=\"line-height: 1.5em;\"><span style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; background-color: rgb(255, 255, 255);\">&nbsp; &nbsp; &nbsp; &nbsp;兴义马岭河大桥是国家高速公路“7918”网汕头至昆明高速公路贵州境板坝（桂黔界）至江底（黔滇界）段的组成部分，是贯穿南昆经济带的重要通道，跨越著名的国家4A级风景区--马岭河大峡谷，是汕昆高速公路的重点控制性工程。峡谷谷深流急，壁挂如织，银瀑飞泻，峡谷以地缝嶂谷、群瀑横飞、碳酸钙壁挂形成景观特色。峡谷谷长74.8公里，谷宽50---150米，谷深120--280米，谷底低于地面200米。</span><br/></p><p style=\"line-height: 1.5em;\"><span style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; background-color: rgb(255, 255, 255);\"><span style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; background-color: rgb(255, 255, 255);\">&nbsp; &nbsp; &nbsp; &nbsp;马岭河峡谷景区总面积450平方公里，是以万峰、千岛、百瀑、奇谷、彩画的神奇地地缝为景观特色的风景名胜区。景区内人文古迹众多，民族风情浓郁，气候温和湿润，年均温度15℃～18℃，四季如春，昼夜温差小，冬无严寒，夏无酷暑。</span><span style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; background-color: rgb(255, 255, 255);\">由于“千泉归壑，溪水溯蚀”的作用，孕育着多姿多彩的峡谷奇观。一是峡谷两壁孕育出规模宏大，气势壮观，错落有致的钙化岩，构成了特有的岩石瀑布；二是景区中有大小瀑布百余条,<span style=\"color: rgb(51, 51, 51); font-family: arial, 宋体, sans-serif; font-size: 14px; text-indent: 28px; background-color: rgb(255, 255, 255);\">其中：天星画廊1.7公里内有瀑布20余条，如万马咆哮瀑、珍珠瀑、间歇五叠瀑等，瀑高120--170米，瀑宽5--100米，壮如银河缺口，柔似袅袅娜娜</span>；三是有众多鲜为人知的水帘洞。在马岭河峡谷游览，可感受大自然的无限神奇。峡谷深幽，栈道攀崖而行，曲曲折折，引人入胜，沿道而游，如进画中，一步一景，步移景异，令人流连忘返。云奇石更奇，奇绝画难比。写奇惟有诗，诗在空山里。马岭河峡谷是空山里的一首诗！</span></span></p>",
    "Organization": {
      "业主单位": "贵州公投建设集团,",
      "总包单位": "中铁十二局,",
      "分包单位": "中铁十二局第二公司,中铁十二局第四公司,",
      "监理单位": "贵州桥梁质量检测贵阳分所,",
      "设计单位": "贵州桥梁设计建筑研究院,",
      "造价单位": "贵州评估造价有限公司,"
    },
    "VideosList": null,
    "ImgList": null,
    "ProjectAddress": null
  }
}
```
