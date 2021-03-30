# DescribeIpv6EgressOnlyRules

调用DescribeIpv6EgressOnlyRules接口查询创建的仅主动出规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6EgressOnlyRules&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeIpv6EgressOnlyRules|要执行的操作，取值：**DescribeIpv6EgressOnlyRules**。 |
|Ipv6GatewayId|String|是|ipv6gw-123456xxxxxxxx|IPv6网关的ID。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|InstanceId|String|否|i-123456xxxxxxxx|设置了仅主动出规则的IPv6地址关联的实例ID。 |
|InstanceType|String|否|Ipv6Address|需要设置仅主动出规则的实例类型，取值：

 **Ipv6Address**：IPv6地址。 |
|Ipv6EgressOnlyRuleId|String|否|ipv6gwpy-123456xxxxxxxx|要查看的仅主动出规则ID。 |
|Name|String|否|rulename|规则名称。 |
|PageNumber|Integer|否|1|列表的页码，默认值为1。 |
|PageSize|Integer|否|10|分页查询时每页的行数，最大值为50，默认值为10。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6EgressOnlyRules| | |仅主动出规则的详细信息。 |
|Description|String|ruledescription|仅主动出规则的描述信息。 |
|InstanceId|String|i-123456xxxxxxxx|配置了仅主动出规则的实例ID。 |
|InstanceType|String|Ipv6Address|配置了仅主动出规则的实例类型。 |
|Ipv6EgressOnlyRuleId|String|ipv6gwpy-123456xxxxxxxx|仅主动出规则的ID。 |
|Name|String|rulename|仅主动出规则的名称。 |
|Status|String|Available|仅主动出规则的状态。 |
|PageNumber|Integer|1|列表的页码，默认值为1。 |
|PageSize|Integer|10|分页查询时每页的行数，最大值为50，默认值为10。 |
|RequestId|String|E16671B7-DEA6-48E0-8E9C-41913DAD44DD|请求ID。 |
|TotalCount|Integer|1|列表条目数。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?Action=DescribeIpv6EgressOnlyRules
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456xxxxxxxx
&公共请求参数

```

正常返回示例

`XML` 格式

```
<DescribeIpv6EgressOnlyRulesResponse>
	  <Ipv6EgressOnlyRules>
		    <Ipv6EgressOnlyRule>
			      <Name></Name>
			      <Status>Available</Status>
			      <Description></Description>
			      <InstanceId>ipv6-hp3b5a8t12ihyxxxxxxxx</InstanceId>
			      <Ipv6EgressOnlyRuleId>ipv6py-hp3w98rmlbqp0xxxxxxxx</Ipv6EgressOnlyRuleId>
			      <InstanceType>Ipv6Address</InstanceType>
		    </Ipv6EgressOnlyRule>
	  </Ipv6EgressOnlyRules>
	  <PageNumber>1</PageNumber>
	  <TotalCount>1</TotalCount>
	  <PageSize>10</PageSize>
	  <RequestId>D1FFB517-D1A7-49BA-9169-C7E7194A9B55</RequestId>
</DescribeIpv6EgressOnlyRulesResponse>
```

`JSON` 格式

```
{
	"Ipv6EgressOnlyRules":{
		"Ipv6EgressOnlyRule":[
			{
				"Name":"",
				"Status":"Available",
				"Description":"",
				"Ipv6EgressOnlyRuleId":"ipv6py-hp3w98rmlbqp0xxxxxxxx",
				"InstanceId":"ipv6-hp3b5a8t12ihyxxxxxxxx",
				"InstanceType":"Ipv6Address"
			}
		]
	},
	"PageNumber":1,
	"TotalCount":1,
	"PageSize":10,
	"RequestId":"D1FFB517-D1A7-49BA-9169-C7E7194A9B55"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

