# CreateIpv6EgressOnlyRule {#doc_api_910121 .reference}

调用CreateIpv6EgressOnlyRule接口为IPv6地址添加仅主动出条目。

## 调试 {#apiExplorer .section}

单击[这里](https://api.aliyun.com/#product=Vpc&api=CreateIpv6EgressOnlyRule)在OpenAPI Explorer中进行可视化调试，并生成SDK代码示例。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateIpv6EgressOnlyRule|要执行的操作，取值：**CreateIpv6EgressOnlyRule**。

 |
|InstanceId|String|是|2408:4004:c0:200:35b:cd32:c460:6aa4|需要设置仅主动出权限的IPv6地址所关联的ECS实例ID。

 |
|Ipv6GatewayId|String|是|i-hp3fr680paz389tbd3vk|IPv6网关的ID。

 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。

 |
|ClientToken|String|否|123456|客户端token，用于保证请求的幂等性。

 由客户端生成该参数值，要保证在不同请求间唯一，最大不值过64个 ASCII 字符。

 |
|Description|String|否|ruledescription|仅主动出条目的描述。

 长度为2-256个字符，必须以字母或中文开头，可包含数字、点号\(.\)、下划线\(\_\)和短橫线\(-\)。但不能以 http:// 或 https:// 开头。

 |
|InstanceType|String|否|IPv6Address|需要设置仅主动出权限的实例类型，取值：

 -   Ipv6Address（默认值）：IPv6地址。

 |
|Name|String|否|rulename|仅主动出条目的名称。

 长度为2-128个字符，必须以字母或中文开头，可包含数字、点号\(.\)、下划线\(\_\)和短橫线\(-\)。但不能以 http:// 或 https:// 开头。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6EgressRuleId|String|ipv6py-hp3w98rmlbqp0qvyrx9ju|仅主动出规则的ID。

 |
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=CreateIpv6EgressOnlyRule
&RegionId=cn-huhehaote
&InstanceId=i-hp3aehvan9212tb07ld4
&Ipv6GatewayId=ipv6gw-hp38x2x0fz785tlc65pfv
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateIpv6EgressOnlyRuleResponse>
  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
  <Ipv6EgressRuleId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</Ipv6EgressRuleId>
</CreateIpv6EgressOnlyRuleResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"4E40EAF1-783D-4C05-948D-DA0426C398C1",
	"Ipv6EgressRuleId":"ipv6py-hp3w98rmlbqp0qvyrx9ju"
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

