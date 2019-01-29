## 人员组织机构

> 用于人员组织机构,树级结构

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getOrganizatioNew`

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

| 字段         | 字段类型 | 字段说明                                                  |
| ------------ | :------: | --------------------------------------------------------- |
| **DataId**   |  string  | 节点ID                                                    |
| **text**     |  String  | 名称                                                      |
| **ParentId** |  String  | 父ID                                                      |
| **NoteId**   |  String  | 如果是人即就是该人的userId，如果是单位组织 将以`org_`开头 |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": {
    "text": null,
    "ParentId": 0,
    "DataId": 0,
    "NoteId": null,
    "OrgNature": 0,
    "selectable": true,
    "nodes": [
      {
        "text": "业主单位",
        "ParentId": 0,
        "DataId": 0,
        "NoteId": null,
        "OrgNature": 0,
        "selectable": false,
        "nodes": [
          {
            "text": "贵州公投建设集团",
            "ParentId": 0,
            "DataId": 416,
            "NoteId": "org_416",
            "OrgNature": 0,
            "selectable": false,
            "nodes": [
              {
                "text": "总经办",
                "ParentId": 416,
                "DataId": 424,
                "NoteId": "org_424",
                "OrgNature": 0,
                "selectable": false,
                "nodes": [
                  {
                    "text": "wang0",
                    "ParentId": 424,
                    "DataId": 494,
                    "NoteId": "494",
                    "OrgNature": 0,
                    "selectable": true,
                    "nodes": null
                  }
                ]
              },
              {
                "text": "财务部",
                "ParentId": 416,
                "DataId": 425,
                "NoteId": "org_425",
                "OrgNature": 0,
                "selectable": false,
                "nodes": []
              }
            ]
          }
        ]
      },
      {
        "text": "总包单位",
        "ParentId": 0,
        "DataId": 1,
        "NoteId": null,
        "OrgNature": 0,
        "selectable": false,
        "nodes": [
          {
            "text": "中铁十二局",
            "ParentId": 1,
            "DataId": 417,
            "NoteId": "org_417",
            "OrgNature": 0,
            "selectable": false,
            "nodes": [
              {
                "text": "计划部",
                "ParentId": 417,
                "DataId": 426,
                "NoteId": "org_426",
                "OrgNature": 0,
                "selectable": false,
                "nodes": []
              },
              {
                "text": "财务部",
                "ParentId": 417,
                "DataId": 427,
                "NoteId": "org_427",
                "OrgNature": 0,
                "selectable": false,
                "nodes": []
              },
              {
                "text": "资料部",
                "ParentId": 417,
                "DataId": 428,
                "NoteId": "org_428",
                "OrgNature": 0,
                "selectable": false,
                "nodes": []
              },
              {
                "text": "总经办",
                "ParentId": 417,
                "DataId": 437,
                "NoteId": "org_437",
                "OrgNature": 0,
                "selectable": false,
                "nodes": [
                  {
                    "text": "wang1",
                    "ParentId": 437,
                    "DataId": 495,
                    "NoteId": "495",
                    "OrgNature": 0,
                    "selectable": true,
                    "nodes": null
                  }
                ]
              }
            ]
          }
        ]
      },
      {
        "text": "分包单位",
        "ParentId": 0,
        "DataId": 2,
        "NoteId": null,
        "OrgNature": 0,
        "selectable": false,
        "nodes": [
          {
            "text": "中铁十二局第二公司",
            "ParentId": 2,
            "DataId": 418,
            "NoteId": "org_418",
            "OrgNature": 0,
            "selectable": false,
            "nodes": []
          },
          {
            "text": "中铁十二局第四公司",
            "ParentId": 2,
            "DataId": 419,
            "NoteId": "org_419",
            "OrgNature": 0,
            "selectable": false,
            "nodes": [
              {
                "text": "wang21",
                "ParentId": 419,
                "DataId": 497,
                "NoteId": "497",
                "OrgNature": 0,
                "selectable": true,
                "nodes": null
              }
            ]
          }
        ]
      },
      {
        "text": "监理单位",
        "ParentId": 0,
        "DataId": 3,
        "NoteId": null,
        "OrgNature": 0,
        "selectable": false,
        "nodes": [
          {
            "text": "贵州桥梁质量检测贵阳分所",
            "ParentId": 3,
            "DataId": 420,
            "NoteId": "org_420",
            "OrgNature": 0,
            "selectable": false,
            "nodes": [
              {
                "text": "wang3",
                "ParentId": 420,
                "DataId": 498,
                "NoteId": "498",
                "OrgNature": 0,
                "selectable": true,
                "nodes": null
              }
            ]
          }
        ]
      },
      {
        "text": "设计单位",
        "ParentId": 0,
        "DataId": 4,
        "NoteId": null,
        "OrgNature": 0,
        "selectable": false,
        "nodes": [
          {
            "text": "贵州桥梁设计建筑研究院",
            "ParentId": 4,
            "DataId": 421,
            "NoteId": "org_421",
            "OrgNature": 0,
            "selectable": false,
            "nodes": [
              {
                "text": "wang4",
                "ParentId": 421,
                "DataId": 499,
                "NoteId": "499",
                "OrgNature": 0,
                "selectable": true,
                "nodes": null
              }
            ]
          }
        ]
      },
      {
        "text": "造价单位",
        "ParentId": 0,
        "DataId": 5,
        "NoteId": null,
        "OrgNature": 0,
        "selectable": false,
        "nodes": [
          {
            "text": "贵州评估造价有限公司",
            "ParentId": 5,
            "DataId": 422,
            "NoteId": "org_422",
            "OrgNature": 0,
            "selectable": false,
            "nodes": []
          }
        ]
      }
    ]
  }
}
```
