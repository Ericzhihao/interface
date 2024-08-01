# AQS Interface Design - 开启AQS（EnableAQS)

## 接口说明

### 1. Instance ID 验证：如果请求中的数据包含不存在的 Instance ID，接口将拒绝该请求。

+ 请求参数
  
|参数名|类型|描述|Required|
|------|-------|------|-----|
|InstancedId| string| 实例ID | 是|
|DPSName| string | DPS名称| 是|
|DPSType| string |DPS类型| 是|
|DPSSpec | string | DPS规格| 是|
|AQSConfigs| AQSConfig object | AQS配置| 是|

+ AQSConfig object
  
|参数名|类型|描述|Required|
|------|-------|------|-----|
|EnableAQS| bool | 开启AQS| 是|
|AQSSize| string| AQS规格| 是|

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
  "Action": "EnableAQS",
  "InstanceID": "111111",
      "AQSConfig": {
        "Enable": true,
        "MaxSize": "s"
      }
}'
```

+ 返回示例

```
{
    "RetCode": 0,
    "Action": "EnableAQS",
    "Message": ""
}
```

	



