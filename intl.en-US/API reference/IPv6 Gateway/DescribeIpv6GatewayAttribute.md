# DescribeIpv6GatewayAttribute

Queries detailed information about a specified IPv6 gateway.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6GatewayAttribute&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeIpv6GatewayAttribute|The operation that you want to perform. Set the value to **DescribeIpv6GatewayAttribute**. |
|Ipv6GatewayId|String|Yes|ipv6gw-123456xxxxxxxx|The ID of the IPv6 gateway that you want to query. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|BusinessStatus|String|Normal|The status of the IPv6 gateway. Valid values:

 -   **Normal**: working as expected
-   **FinancialLocked**: locked due to overdue payments
-   **SecurityLocked**: locked due to security reasons |
|CreationTime|String|2018-12-05T09:21:35Z|The time when the IPv6 gateway was created. |
|Description|String|test|The description of the IPv6 gateway. |
|ExpiredTime|String|2018-12-05T09:21:35Z|The time when the IPv6 gateway expires. |
|InstanceChargeType|String|PostPaid|The metering method of the IPv6 gateway. |
|Ipv6GatewayId|String|ipv6gw-123456xxxxxxxx|The ID of the IPv6 gateway. |
|Name|String|test|The name of the IPv6 gateway. |
|RegionId|String|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. |
|RequestId|String|ipv6gw-hp33p10bdbt77xxxxxxxx|The ID of the request. |
|Spec|String|Medium|The specification of the IPv6 gateway. |
|Status|String|Available|The status of the IPv6 gateway. |
|VpcId|String|vpc-123456xxxxxxxx|The ID of the virtual private cloud \(VPC\) to which the IPv6 gateway belongs. |

## Examples

Sample requests

```

https://vpc.cn-huhehaote.aliyuncs.com/?Action=DescribeIpv6GatewayAttribute
&Ipv6GatewayId=ipv6gw-hp33p10bdbt77xxxxxxxx
&RegionId=cn-huhehaote
&Common request parameters

```

Sample success responses

`XML` format

```
<DescribeIpv6GatewayAttributeResponse>
	  <Name>ipv6gateway</Name>
	  <CreationTime>2018-12-05T09:21:35Z</CreationTime>
	  <Status>Available</Status>
	  <Description></Description>
	  <BusinessStatus>Normal</BusinessStatus>
	  <Spec>Medium</Spec>
	  <RequestId>F4517005-A716-40EB-8B80-F6AF8508B25F</RequestId>
	  <RegionId>cn-huhehaote</RegionId>
	  <InstanceChargeType>PostPaid</InstanceChargeType>
	  <ExpiredTime></ExpiredTime>
	  <VpcId>vpc-hp3kzilwd9yflxxxxxxxx</VpcId>
	  <Ipv6GatewayId>ipv6gw-hp33p10bdbt77xxxxxxxx</Ipv6GatewayId>
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
	"VpcId":"vpc-hp3kzilwd9yflxxxxxxxx",
	"Ipv6GatewayId":"ipv6gw-hp33p10bdbt77xxxxxxxx"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

