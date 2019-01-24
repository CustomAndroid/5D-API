## 构件管理

### 生产监控

​在线监控接口：gjOnlineJk
请求参数：

``` json
{
  "userId": "string",
  "UserName": "string",
  "projectid": "string"
}
```

返回结果：

``` json
[
	{
		"name":"线路一",
		"url":"string"
	}
]
```



​	

### 构件状态跟踪

构件生产信息追溯接口：gjProductionLists

请求参数：
{
  "userId": "string",
  "UserName": "string",
  "projectid": "string"
}
返回结果：
{
  "Code": 1,
  "CodeMsg": "",
  "Datas": 
  [
	{
		"gjId":"String",//构件id
		"gjName":"String",//构件名称
		"gjStatus":"String",//当前状态
		"gjUpdateTime":"String",//更新时间
		"gjProDatas"://生产信息集合
		[
			{
				"gjId":"String",//构件id
				"gjProTime":"String",//构件生产阶段时间点
				"gjProInfo":"String"//构件生产阶段时间点描述信息
			}
		]
	}
  ]
}



构件生产信息列表接口：gjProductionInfo
请求参数：
{
  "userId": "string",
  "UserName": "string",
  "gjId": "string"
}
返回结果：
{
  "Code": 1,
  "CodeMsg": "",
  "Datas": 
  [
	{
		"gjId":"String",//构件id
		"gjProTime":"String",//构件生产阶段时间点
		"gjProInfo":"String"//构件生产阶段时间点描述信息
	}
  ]
}

构件生产信息更新接口：gjProductionUpdata
请求参数：
{
  "userId": "string",
  "UserName": "string",
  "gjId":"String",//构件id
  "gjProTime":"String",//构件生产阶段时间点
  "gjProInfo":"String"//构件生产阶段时间点描述信息
}
返回结果：
{
  "Code": 1,
  "CodeMsg": "",
  "Datas":null 

}



构件状态管理接口：gjStatusManageLists

请求参数：
{
  "userId": "string",
  "UserName": "string",
  "projectid": "string"
}
返回结果：
{
  "Code": 1,
  "CodeMsg": "",
  "Datas": 
  [
	{
		"gjId":"String",//构件id
		"gjName":"String",//构件名称
		"gjStatus":"String",//当前状态
		"gjUpdateTime":"String",//更新时间
		"gjProDatas"://生产信息集合
		[
			{
				"gjId":"String",//构件id
				"gjProTime":"String",//构件生产阶段时间点
				"gjProInfo":"String"//构件生产阶段时间点描述信息
			}
		]
	}
  ]
}

### 生产计划查询

生化计划查询接口：proPlanLists
请求参数：
{
  "userId": "string",
  "UserName": "string"
}

返回 id-pid形式的树数据

