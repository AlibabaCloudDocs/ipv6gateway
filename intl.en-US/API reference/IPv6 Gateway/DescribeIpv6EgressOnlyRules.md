# DescribeIpv6EgressOnlyRules

Queries one or more created egress-only rules.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|DescribeIpv6EgressOnlyRules|The name of this action. Value: **DescribeIpv6EgressOnlyRules** |
|Ipv6GatewayId|String|Yes|ipv6gw-123456|The ID of the IPv6 Gateway. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |
|InstanceId|String|No|i-123456|Optional. The ID of the ECS instance associated with the IPv6 address for which the egress-only rule is created. |
|InstanceType|String|No|Ipv6Address|Optional. The type of the instance that requires egress-only permissions. Value:

 -   Ipv6Address: IPv6 addresses. |
|Ipv6EgressOnlyRuleId|String|No|ipv6gwpy-123456|Optional. The ID of the egress-only rule. |
|Name|String|No|rulename|Optional. The name of the egress-only rule. |
|PageNumber|Integer|No|1|Optional. The page number of the rules list. Default value: 1. |
|PageSize|Integer|No|10|Optional. The number of rows per page. Maximum value: 50. Default value: 10. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|Ipv6EgressOnlyRules| | |A list of created egress-only rules. |
|└Description|String|ruledescription|A description of the egress-only rule. |
|└InstanceId|String|i-123456|The ID of the instance for which the egress-only rule is created. |
|└InstanceType|String|Ipv6Address|The type of the instance for which the egress-only rule is created. |
|└Ipv6EgressOnlyRuleId|String|ipv6gwpy-123456|The ID of the egress-only rule. |
|└Name|String|rulename|The name of the egress-only rule. |
|└Status|String|Available|The status of the egress-only rule. |
|PageNumber|Integer|1|The page number. Default value: 1. |
|PageSize|Integer|10|The number of rows per page. Maximum value: 50. Default value: 10. |
|RequestId|String|E16671B7-DEA6-48E0-8E9C-41913DAD44DD|The ID of the request. |
|TotalCount|Integer|1|The number of egress-only rules. |

## Examples

Request example

```

https://vpc.aliyuncs.com/?Action=DescribeIpv6EgressOnlyRules
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456
&CommonParameters
			
```

Response examples

`XML` format

```
<DescribeIpv6EgressOnlyRulesResponse>
  <Ipv6EgressOnlyRules>
    <Ipv6EgressOnlyRule>
      <Name/>
      <Status>Available</Status>
      <Description/>
      <InstanceId>ipv6-hp3b5a8t12ihy7c669i13</InstanceId>
      <Ipv6EgressOnlyRuleId>ipv6py-hp3w98rmlbqp0qvyrx9ju</Ipv6EgressOnlyRuleId>
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
				"Ipv6EgressOnlyRuleId":"ipv6py-hp3w98rmlbqp0qvyrx9ju",
				"InstanceId":"ipv6-hp3b5a8t12ihy7c669i13",
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

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).

