## 质量问题提报

> 用于获取质量问题提报

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/setQualityQuest`

### 2. 请求参数

body:

| 字段              | 字段类型 | 必填 | 字段说明                                                     |
| ----------------- | :------: | :--: | ------------------------------------------------------------ |
| **projectId**     |  String  |  Y   | 项目ID                                                       |
| **userId**        |  String  |  N   | 用户ID                                                       |
| **level**         |  String  |  N   | 问题危险登记，[GetBaseData](../../project/getBaseData.md)接口获取类型为`QualityProblemLevel` |
| **title**         |  String  |  N   | 问题标题                                                     |
| **arisesTime**    |  String  |  N   | 发现问题时间                                                 |
| **quesType**      |  String  |  Y   | 问题类型，[GetBaseData](../../project/getBaseData.md)接口获取类型为`QualityProblemType` |
| **guid**          |  String  |  Y   | 关联构件ID                                                   |
| **desc**          |  String  |  N   | 描述                                                         |
| **sendTo**        |  String  |  Y   | 发送人，仅一人  ,以`id#name`的格式                           |
| **copyTo**        |  String  |  N   | 抄送人，可多人，以`id#name,id#name`的格式                    |
| **LableLocation** |  String  |  N   | 标签                                                         |
| **FileLists**     |  String  |  N   | 附件，以`附件1:附件1的描述,附件2:附件2的描述`的格式返回，多个附件`,`间隔，附件名与其描述`:`间隔,附件ftp上传，文件名传ftp上文件相对路径，上传成功后，使用[login](../../login/login.md)中 `WebNetIPAndPort`拼接上提交的文件相对路径能打开即为成功上传，比如你提交附件数据为 `/uploadFile/attachment/EF_20181127_153853409.png:图片描述`，图片上传到ftp根目录`/uploadFile/attachment/`目录下，命名为`EF_20181127_153853409.png`,`WebNetIPAndPort`路径假如是`http://110.120.119.121:8090/`,那么图片完整访问地址是`http://110.120.119.121:8090/uploadFile/attachment/EF_20181127_153853409.png` |
| **TempId**        |  String  |  N   | android上用来标识一个临时ID，数据不会入库，提交成功后原样返回，以区分那个问题的提交 |
| **Viewpoint**     |  String  |  N   | 视点                                                         |

示例:

```json
{
  "userId": "string",
  "title": "string",
  "arisesTime": "string",
  "quesType": "string",
  "guid": "string",
  "level": "string",
  "desc": "string",
  "sendTo": "string",
  "copyTo": "string",
  "ProTree": "",//废弃字段留空
  "ProTreeData": "",//废弃字段留空
  "Post": "",//废弃字段留空
  "ProjectId": "string",
  "LableLocation": "string",
  "FileLists": "string",
  "TempId": "string",
  "Viewpoint": "string"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明               |
| ----------- | :------: | ---------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败   |
| **CodeMsg** |  String  | 失败时原因信息         |
| **Id**      |  String  | 问题ID                 |
| **LId**     |  String  | 问题流程ID             |
| **TempId**  |  String  | 提交问题提交的`TempId` |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": [
    {
      "Id": "119",
      "LId": "1",
      "TempId": "tmp"
    }
  ]
}
```