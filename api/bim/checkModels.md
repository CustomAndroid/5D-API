## 检查模型更新

> 获取项目模型树

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/checkModels`

### 2. 请求参数

body:

| 字段       | 字段类型 | 必填 | 字段说明 |
| ---------- | :------: | :--: | -------- |
| **userId** |  String  |  Y   | 用户ID   |

示例:

```json
{
  "userId": "496"
}
```

### 3. 返回参数

| 字段                   | 字段类型 | 字段说明                                                     |
| ---------------------- | :------: | ------------------------------------------------------------ |
| **userId**             |  string  | 用户ID                                                       |
| **userName**           |  String  | 登录名                                                       |
| **userOrganizationId** |  String  | 当前登录人所在单位组织ID                                     |
| **userOrganization**   |  String  | 当前登录人所在单位组织名称                                   |
| **userPosition**       |  String  | 当前登录人角色名称                                           |
| **userPositionid**     |  String  | 当前登录人角色ID                                             |
| **projectName**        |  String  | 当前项目名称                                                 |
| **projectId**          |  String  | 当前项目ID                                                   |
| **projectSection**     |  String  |                                                              |
| **projectPlanType**    |  String  | 计划类型：4月计划，5旬计划，6周计划，7日计划，可组合使用：比如457表示该项目制定了月计划旬计划和周计划 |
| **WebNetIPAndPort**    |  String  | 平台地址                                                     |
| **userNameText**       |  String  | 当前登录人姓名                                               |
| **FTPAddress**         |  String  | ftp地址                                                      |
| **FTPPort**            |  String  | ftp端口                                                      |
| **FTPUser**            |  String  | ftp登录名                                                    |
| **FTPPassword**        |  String  | ftp密码                                                      |
| **models**             |  Array  | 模型树结构数据                                               |
| **MileageID**  |  String  | 模型ID(节点ID)  |
| **TreeName**  |  String  | 节点名称  |
| **PMileageID**  |  String  | 父节点名称  |
| **modelFilePath**  |  String  | 模型下载地址  |
| **modelFileVersion**  |  String  | 模型版本  |
| **Postid**  |  String  | 所属专业ID，在`Special`中查找  |
| **Modelname**  |  String  | 模型压缩包文件名，加载模型时用类似于`{Modelname}/{Modelname}List.json`的路径加载  |
| **Special**  |  Array  | 模型专业列表，包含ID和name  |


返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "ok",
  "Datas": {
    "userId": "496",
    "userName": "wang2",
    "userOrganization": "中铁十二局第二公司",
    "userOrganizationID": "418",
    "userPosition": "项目管理员",
    "userPositionid": null,
    "projectName": "贵州马岭河大桥",
    "projectId": "61",
    "projectSection": "",
    "projectPlanType": "457",
    "models": [
      {
        "MileageID": "598",
        "TreeName": "马岭河大桥",
        "PMileageID": "0",
        "modelFilePath": "",
        "modelFileVersion": null,
        "Postid": "0",
        "Modelname": ""
      },
      {
        "MileageID": "600",
        "TreeName": "引桥",
        "PMileageID": "598",
        "modelFilePath": "http://xxx.xxx.xxx.xxx:xxxx/ZipFile/malingheyinqiao.zip",
        "modelFileVersion": "20180906154735V1.0",
        "Postid": "126",
        "Modelname": "malingheyinqiao"
      }
    ],
    "Special": [
      {
        "id": "125",
        "SpecialName": "主桥"
      },
      {
        "id": "126",
        "SpecialName": "引桥"
      }
    ],
    "WebNetIPAndPort": null,
    "userNameText": null,
    "FTPAddress": "xxx.xxx.xxx.xxx",
    "FTPPort": "xxxx",
    "FTPUser": "xxxxxx",
    "FTPPassword": "xxxxxxxxxxxxx"
  }
}
```
