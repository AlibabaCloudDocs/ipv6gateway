# DescribeIpv6GatewayAttribute

Queries the details of an IPv6 Gateway.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|DescribeIpv6GatewayAttribute|The name of this action. Value: **DescribeIpv6GatewayAttribute** |
|Ipv6GatewayId|String|Yes|ipv6gw-123456|The ID of the IPv6 Gateway to be queried. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|BusinessStatus|String|Normal|The status of the IPv6 Gateway. Valid values:

 -   Normal: Indicates that the IPv6 Gateway is normal.
-   FinacialLocked: Indicates that the IPv6 Gateway is locked due to overdue bills.
-   SecurityLocked: Indicates that the IPv6 Gateway is locked for security purposes. |
|CreationTime|String|2018-12-05T09:21:35Z|The time when the IPv6 is created. |
|Description|String|test|A description of the IPv6 Gateway. |
|ExpiredTime|String|2018-12-05T09:21:35Z|The time when the IPv6 Gateway expires. |
|InstanceChargeType|String|PostPaid|The billing method of the IPv6 Gateway. |
|Ipv6GatewayId|String|ipv6gw-123456|The ID of the IPv6 Gatewy. |
|Name|String|test|The name of the IPv6 Gateway. |
|RegionId|String|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |
|RequestId|String|ipv6gw-hp33p10bdbt77xbeq6sgj|The ID of the request. |
|Spec|String|Medium|The specification of the IPv6 Gateway. |
|Status|String|Available|The status of the IPv6 Gateway. |
|VpcId|String|vpc-123456|The ID of the VPC to which the IPv6 Gateway belongs. |

## Examples

Request example

```

https://vpc.cn-huhehaote.aliyuncs.com/?Action=DescribeIpv6GatewayAttribute
&Ipv6GatewayId=ipv6gw-hp33p10bdbt77xbeq6sgj
&RegionId=cn-huhehaote
&CommonParameters
			
```

Response examples

`XML` format

```
<DescribeIpv6GatewayAttributeResponse>
  <Name>ipv6gateway</Name>
  <CreationTime>2018-12-05T09:21:35Z</CreationTime>
  <Status>Available</Status>
  <Description/>
  <BusinessStatus>Normal</BusinessStatus>
  <Spec>Medium</Spec>
  <RequestId>F4517005-A716-40EB-8B80-F6AF8508B25F</RequestId>
  <RegionId>cn-huhehaote</RegionId>
  <InstanceChargeType>PostPaid</InstanceChargeType>
  <ExpiredTime/>
  <VpcId>vpc-hp3kzilwd9yflssfdlgqe</VpcId>
  <Ipv6GatewayId>ipv6gw-hp33p10bdbt77xbeq6sgj</Ipv6GatewayId>
</DescribeIpv6GatewayAttributeResponse>
			
```

`JSON` format

```
{
	"CreationTime":"2018-12-05T09:21:35Z",
	"Name":"ipv6gateway",
	"Status":"Available",
	"Description":"",
	"Spec":"Medium",
	"BusinessStatus":"Normal",
	"RegionId":"cn-huhehaote",
	"RequestId":"F4517005-A716-40EB-8B80-F6AF8508B25F",
	"InstanceChargeType":"PostPaid",
	"ExpiredTime":"",
	"VpcId":"vpc-hp3kzilwd9yflssfdlgqe",
	"Ipv6GatewayId":"ipv6gw-hp33p10bdbt77xbeq6sgj"
}
```

## Error codes

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).

