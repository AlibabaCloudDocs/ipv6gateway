# DescribeIpv6EgressOnlyRules

Queries egress-only rules.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6EgressOnlyRules&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeIpv6EgressOnlyRules|The operation that you want to perform. Set the value to **DescribeIpv6EgressOnlyRules**. |
|Ipv6GatewayId|String|Yes|ipv6gw-123456xxxxxxxx|The ID of the IPv6 gateway. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|InstanceId|String|No|i-123456xxxxxxxx|The ID of the instance that is associated with the IPv6 address to which the egress-only rule is applied. |
|InstanceType|String|No|Ipv6Address|The type of the instance to which you want to apply the egress-only rule. Set the value to:

 **Ipv6Address**. This value indicates that the egress-only rule is applied to an IPv6 address. |
|Ipv6EgressOnlyRuleId|String|No|ipv6gwpy-123456xxxxxxxx|The ID of the egress-only rule that you want to query. |
|Name|String|No|rulename|The name of the egress-only rule. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page. Maximum value: 50. Default value: 10. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Ipv6EgressOnlyRules| | |The details about the egress-only rule. |
|Description|String|ruledescription|The description of the egress-only rule. |
|InstanceId|String|i-123456xxxxxxxx|The ID of the instance to which the egress-only rule is applied. |
|InstanceType|String|Ipv6Address|The type of the instance to which the egress-only rule is applied. |
|Ipv6EgressOnlyRuleId|String|ipv6gwpy-123456xxxxxxxx|The ID of the egress-only rule. |
|Name|String|rulename|The name of the egress-only rule. |
|Status|String|Available|The status of the egress-only rule. |
|PageNumber|Integer|1|The page number of the returned page. Default value: 1. |
|PageSize|Integer|10|The number of entries retuned on each page. Maximum value: 50. Default value: 10. |
|RequestId|String|E16671B7-DEA6-48E0-8E9C-41913DAD44DD|The ID of the request. |
|TotalCount|Integer|1|The total number of entries returned. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=DescribeIpv6EgressOnlyRules
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456xxxxxxxx
&Common request parameters

```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

