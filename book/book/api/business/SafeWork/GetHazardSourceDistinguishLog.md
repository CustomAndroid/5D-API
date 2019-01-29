## 查询危险源识别台账

> 用于查询危险源识别台账

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/GetHazardSourceDistinguishLog`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明 |
| ------------- | :------: | :--: | -------- |
| **projectId** |  String  |  Y   | 项目ID   |
| **userId**    |  String  |  Y   | 用户ID   |
| **pageIndex** |  String  |  Y   | 页码     |
| **pageSize**  |  String  |  Y   | 每页条数 |
| **startTime** |  String  |  Y   | 开始时间 |
| **endTime**   |  String  |  Y   | 截止时间 |
| **keyword**   |  String  |  N   | 关键字   |

示例:

```json
{
  "userId": "string",
  "projectId": "string",
  "pageIndex": "string",
  "pageSize": "string",
  "startTime": "string",
  "endTime": "string",
  "keyword": "string"
}
```

### 3. 返回参数

| 字段        | 字段类型 | 字段说明             |
| ----------- | :------: | -------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败 |
| **CodeMsg** |  String  | 失败时原因信息       |
| **Hid**             | String | ID                   |
| **Projectid**       | String | 项目ID               |
| **Title**           | String | 标题                 |
| **SignDate**        | String | 识别时间             |
| **AllNum**          | String | 危险源总数           |
| **ControllableNum** | String | 可控危险源数量       |
| **veryNum**         | String | 异常危险源数量       |
| **Status**          | String | 处理状态             |
| **Adder**           | String | 提报人ID             |
| **Addtime**         | String | 提报时间             |
| **TrueName**        | String | 提报人名字           |
| **isHandle**        | String | 是否可操作           |
| **HandleType**      | String | 1审核；2：反馈       |

返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "OK", 
    "Datas": {
        "Hid": "105", 
        "Projectid": "61", 
        "Title": "危险源识别测试", 
        "SignDate": "2018/9/19 0:00:00", 
        "Optionid": "495", 
        "AllNum": "4", 
        "ControllableNum": "4", 
        "veryNum": "0", 
        "Status": "3", 
        "Adder": "wang1", 
        "Addtime": "2018/9/19 14:20:37", 
        "TrueName": "wang1", 
        "isHandle": null, 
        "HandleType": null, 
        "rq": ""
    }
}
```