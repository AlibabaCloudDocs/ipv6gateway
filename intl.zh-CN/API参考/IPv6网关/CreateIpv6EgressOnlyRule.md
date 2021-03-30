# CreateIpv6EgressOnlyRule

调用CreateIpv6EgressOnlyRule为IPv6地址添加仅主动出规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=CreateIpv6EgressOnlyRule&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateIpv6EgressOnlyRule|要执行的操作，取值：**CreateIpv6EgressOnlyRule**。 |
|InstanceId|String|是|ipv6-hp3nxjkfxn5pnhgl5\*\*\*\*|需要设置仅主动出规则的IPv6地址的ID。 |
|Ipv6GatewayId|String|是|ipv6gw-hp3c2paq0ywauasza\*\*\*\*|IPv6网关的ID。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|InstanceType|String|否|IPv6Address|需要设置仅主动出规则的实例类型，取值：

 **Ipv6Address**（默认值）：IPv6地址。 |
|Name|String|否|rulename|仅主动出规则的名称。

 长度为2~128个字符，必须以字母或中文开头，可包含数字、点号（.）、下划线（\_）和短橫线（-），但不能以`http://`或`https://`开头。 |
|Description|String|否|ruledescription|仅主动出规则的描述。

 长度为2~256个字符，必须以字母或中文开头，可包含数字、点号（.）、下划线（\_）和短橫线（-），但不能以`http://`或`https://`开头。 |
|ClientToken|String|否|123456|客户端token，用于保证请求的幂等性。

 由客户端生成该参数值，要保证在不同请求间唯一，最大值不超过64个ASCII字符。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6EgressRuleId|String|ipv6py-hp3w98rmlbqp01245\*\*\*\*|仅主动出规则的ID。 |
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|请求ID。 |

## 示例

请求示例

```
https://vpc.aliyuncs.com/?Action=CreateIpv6EgressOnlyRule
&RegionId=cn-huhehaote
&InstanceId=ipv6-hp3nxjkfxn5pnhgl5****
&Ipv6GatewayId=ipv6gw-hp3c2paq0ywauasza****
&公共请求参数
```

正常返回示例

`XML` 格式

```
<CreateIpv6EgressOnlyRuleResponse>
	  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
	  <Ipv6EgressRuleId>ipv6py-hp3w98rmlbqp01245****</Ipv6EgressRuleId>
</CreateIpv6EgressOnlyRuleResponse>
```

`JSON` 格式

```
{
    "Ipv6EgressRuleId": "ipv6py-hp3w98rmlbqp01245****",
    "RequestId": "9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

