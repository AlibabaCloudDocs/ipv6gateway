# DeleteIpv6EgressOnlyRule

调用DeleteIpv6EgressOnlyRule接口删除仅主动出规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6EgressOnlyRule&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteIpv6EgressOnlyRule|要执行的操作，取值：**DeleteIpv6EgressOnlyRule**。 |
|Ipv6EgressOnlyRuleId|String|是|ipv6py-hp3w98rmlbqp0xxxxxxxx|要删除的仅主动出规则ID。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的ID。 |
|ClientToken|String|否|123456|客户端token，用于保证请求的幂等性。

 由客户端生成该参数值，要保证在不同请求间唯一，最大值不超过64个ASCII字符。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|请求ID。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?Action=DeleteIpv6EgressOnlyRule
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456
&Ipv6EgressOnlyRuleId=ipv6py-hp3w98rmlbqp0xxxxxxxx
&公共请求参数

```

正常返回示例

`XML` 格式

```
<DeleteIpv6EgressOnlyRuleResponse>
	  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
</DeleteIpv6EgressOnlyRuleResponse>
```

`JSON` 格式

```
{
	"RequestId":"4E40EAF1-783D-4C05-948D-DA0426C398C1"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

