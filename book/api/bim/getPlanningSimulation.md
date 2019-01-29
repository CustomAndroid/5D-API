## 获取进度沙盘-计划模拟

> 获取计划模拟

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/getPlanningSimulation`

### 2. 请求参数

body:

| 字段          | 字段类型 | 必填 | 字段说明                  |
| ------------- | :------: | :--: | ------------------------- |
| **userId**    |  String  |  Y   | 用户ID                    |
| **projectId** |  String  |  Y   | 项目ID                    |
| **startTime** |  String  |  Y   | 开始时间                  |
| **endTime**   |  String  |  Y   | 截止时间                  |
| **step**      |  String  |  Y   | 模拟步长 月-4  周-6  日-7 |



示例:

```json
{
  "userId": "496",
  "projectId":"61",
  "startTime":"",
  "endTime":"",
  "step":""
}
```

### 3. 返回参数

| 字段          | 字段类型 | 字段说明     |
| ------------- | :------: | ------------ |
| **time**      |  string  | 时间轴       |
| **planGuids** |  string  | 计划完成构件 |
| **realGuids** |  string  | 实际完成构件 |


返回示例：

```json
{
    "Code": 0, 
    "CodeMsg": "ok", 
    "Datas": [
        {
            "time": "", 
            "planGuids": "", 
            "realGuids": ""
        }
    ]
}
```

