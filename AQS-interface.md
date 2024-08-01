# AQS 接口API 

### 2.1 创建DPS接口修改

在CreateMAXIRDPSRequest中增加 EnableAQS bool 和 AQSSpec string


### 2.2 开启DPS接口(EnableMAXIRDPSAQS)
+ 请求参数
  
|参数名|类型|描述|Required|
|------|-------|------|-----|
|InstanceId| string| 实例ID | 是|
|DPSId| string | DPS ID|是| 
|Region| string | 地域 | 是|
|ProjectId| string |项目ID| 是|
|Action | string | 操作名称| 是|
|AQSSpec| string  | AQS规格| 是|

+ 返回参数
  
|参数名|类型|描述|
|------|-------|------|
|RetCode| int | 返回码|
|Action | string | 操作名称|
|Message | string | 返回信息| 

+ 请求示例

```
curl -X "POST" "https://api.ucloud.cn/" \
-H 'Content-Type: application/json; charset=utf-8' \
-d $'{
  "Action": "EnableMAXIRDPSAQS",
  "Region": "cn-gd",
  "InstanceID": "maxir-sdaqs",
  "AQSSpec": "s"
}'
```

+ 返回示例

```
{
    "RetCode": 0,
    "Action": "EnableMAXIRAQS",
    "Message": ""
}
```

### 2.3 关闭DPS接口(DisableMAXIRDPSAQS)

+ 请求参数
  
|参数名|类型|描述|Required|
|------|-------|------|-----|
|InstanceId| string| 实例ID | 是|
|DPSId| string | DPS ID|是| 
|Region| string | 地域 | 是|
|ProjectId| string |项目ID| 是|
|Action | string | 操作名称| 是|
|DisableAQS| bool  | AQS状态| 是|

+ 返回参数
  
|参数名|类型|描述|
|------|-------|------|
|RetCode| int | 返回码|
|Action | string | 操作名称|
|Message | string | 返回信息| 

+ 请求示例

```
curl -X "POST" "https://api.ucloud.cn/" \
-H 'Content-Type: application/json; charset=utf-8' \
-d $'{
  "Action": "DisableMAXIRDPSAQS",
  "Region": "cn-gd",
  "InstanceID": "maxir-sdaqs",
  “DisableAQS": true
}'
```

+ 返回示例

```
{
    "RetCode": 0,
    "Action": "DisableMAXIRAQS",
    "Message": ""
}
```

	



