# DeleteIpv6EgressOnlyRule {#doc_api_910122 .reference}

调用DeleteIpv6EgressOnlyRule接口删除仅主动出条目。

## 调试 {#apiExplorer .section}

单击[这里](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6EgressOnlyRule)在OpenAPI Explorer中进行可视化调试，并生成SDK代码示例。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteIpv6EgressOnlyRule|要执行的操作，取值：**DeleteIpv6EgressOnlyRule**。

 |
|Ipv6EgressOnlyRuleId|String|是|ipv6py-hp3w98rmlbqp0qvyrx9ju|要删除的仅主动出规则ID。

 |
|RegionId|String|是|cn-huhehaote|IPv6网关的ID。

 |
|ClientToken|String|否|123456|客户端token，用于保证请求的幂等性。

 由客户端生成该参数值，要保证在不同请求间唯一，最大不值过64个 ASCII 字符。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=DeleteIpv6EgressOnlyRule
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456
&Ipv6EgressOnlyRuleId=ipv6py-123456
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteIpv6EgressOnlyRuleResponse>
  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
</DeleteIpv6EgressOnlyRuleResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"4E40EAF1-783D-4C05-948D-DA0426C398C1"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

