# DescribeIpv6Addresses

Queries the IPv6 addresses in a specified region.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6Addresses&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeIpv6Addresses|The operation that you want to perform. Set the value to **DescribeIpv6Addresses**. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 addresses are deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|AssociatedInstanceId|String|No|i-123456xxxxxxxx|The ID of the instance that is assigned the IPv6 address. |
|AssociatedInstanceType|String|No|EcsInstance|The type of the instance that is assigned the IPv6 address. Valid value:

 **EcsInstance** \(default\): an ECS instance deployed in a virtual private cloud \(VPC\). |
|Ipv6Address|String|No|2408:xxxx:180:1701:94c7:bc38:3bfa:d2c|The IPv6 address that you want to query. |
|Ipv6AddressId|String|No|ipv6gw-hp33of4uz4k4kxxxxxxxx|The ID of the IPv6 address. You can specify up to 20 IDs in each call. Separate multiple IDs with commas \(,\). |
|Ipv6InternetBandwidthId|String|No|1|The Internet bandwidth of the IPv6 address. |
|Name|String|No|test|The name of the IPv6 address. |
|NetworkType|String|No|Public|The type of connection supported by the IPv6 address. Valid values:

 -   **Private**: private network connections
-   **Public**: public network connections |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page. Maximum value: 50. Default value: 10. |
|VSwitchId|String|No|vsw-123456xxxxxxxx|The ID of the vSwitch to which the IPv6 address belongs. |
|VpcId|String|No|vpc-123456xxxxxxxx|The ID of the VPC to which the IPv6 address belongs. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Ipv6Addresses| | |The details about the IPv6 addresses. |
|AllocationTime|String|2018-12-20T14:56:09Z|The time when the IPv6 address was created. |
|AssociatedInstanceId|String|i-hp325kt6307xxxxxxxx|The ID of the instance that is assigned the IPv6 address. |
|AssociatedInstanceType|String|EcsInstance|The type of the instance associated with the IPv6 address. |
|Ipv6Address|String|2408:xxxx:0:2900:2901:3c61:9ff0:xxxx|The IPv6 address. |
|Ipv6AddressId|String|ipv6-hp32vv2klzw4xxxxxxxx|The ID of the IPv6 address. |
|Ipv6AddressName|String|test|The name of the IPv6 address. |
|Ipv6GatewayId|String|ipv6gw-hp38x2x0fz7xxxxxxxx|The ID of the IPv6 gateway to which the IPv6 address belongs. |
|Ipv6InternetBandwidth| | |The information about the public network bandwidth of the IPv6 address. |
|Bandwidth|Integer|2|The exclusive Internet bandwidth of the IPv6 address. Unit: Mbit/s. |
|BusinessStatus|String|Normal|The status of the exclusive bandwidth of the IPv6 address. Valid values:

 -   Normal: working as expected.
-   FinancialLocked: locked due to overdue payments.
-   SecurityLocked: locked due to security reasons. |
|InstanceChargeType|String|PostPaid|The billing method of the IPv6 gateway. Valid values:

 **PostPaid**: pay-as-you-go |
|InternetChargeType|String|PayByTraffic|The metering method of the IPv6 gateway. Valid values:

 -   **PayByTraffic**: pay-by-data-transfer
-   **PayByBandwidth**: pay-by-bandwidth |
|Ipv6InternetBandwidthId|String|ipv6bw-hp3b35oq1fj50kbvmxxx|The ID of the Internet bandwidth. |
|NetworkType|String|Public|The type of connection supported by the IPv6 address. Valid values:

 -   **Private**: private network connections
-   **Public**: public network connections |
|RealBandwidth|Integer|2|The peak bandwidth value of the IPv6 address. Valid value:

 -   If the IPv6 gateway uses an elastic IP address \(EIP\) bandwidth plan, the value of **RealBandwidth** is the peak bandwidth value of the EIP bandwidth plan.
-   If the IPv6 gateway does not use an EIP bandwidth plan, the value of **RealBandwidth** is the peak bandwidth value of the Internet bandwidth of the IPv6 gateway.
-   If the IPv6 gateway does not use an EIP bandwidth plan or Internet bandwidth resources, the values of **RealBandwidth** and **Bandwidth** are both 0. |
|Status|String|Available|The status of the IPv6 address. Valid values:

 -   **Pending**: being configured
-   **Available**: ready for use |
|VSwitchId|String|vsw-hp3123456xxxxxxxx|The ID of the vSwitch to which the IPv6 address belongs. |
|VpcId|String|vpc-123456xxxxxxxx|The ID of the VPC to which the IPv6 address belongs. |
|PageNumber|Integer|1|The page number of the returned page. Default value: 1. |
|PageSize|Integer|10|The number of entries returned per page. Maximum value: 50. Default value: 10. |
|RequestId|String|AA4486A8-B6AE-469E-AB09-820EF8ECFA2B|The ID of the request. |
|TotalCount|Integer|2|The total number of entries returned. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=DescribeIpv6Addresses
&RegionId=cn-huhehaote
&Common request parameters

```

Sample success responses

`XML` format

```
<DescribeIpv6Addresses>
	  <PageNumber>1</PageNumber>
	  <TotalCount>2</TotalCount>
	  <Ipv6Addresses>
		    <Ipv6Address>
			      <Ipv6AddressId>ipv6-hp32vv2klzw4yxxxxxxxx</Ipv6AddressId>
			      <AssociatedInstanceType>EcsInstance</AssociatedInstanceType>
			      <AllocationTime>2019-01-07T05:16:23Z</AllocationTime>
			      <Ipv6InternetBandwidth>
				        <BusinessStatus></BusinessStatus>
				        <Ipv6InternetBandwidthId></Ipv6InternetBandwidthId>
				        <InternetChargeType></InternetChargeType>
				        <Bandwidth>0</Bandwidth>
			      </Ipv6InternetBandwidth>
			      <VSwitchId>vsw-hp3lyltb1dosjxxxxxxxx</VSwitchId>
			      <VpcId>vpc-hp34hflqqsjh3xxxxxxxx</VpcId>
			      <Ipv6GatewayId></Ipv6GatewayId>
			      <Status>Available</Status>
			      <NetworkType>Private</NetworkType>
			      <Ipv6Address>2408:xxxx:0:2900:2901:3c61:9ff0:8fdc</Ipv6Address>
			      <Ipv6AddressName></Ipv6AddressName>
			      <AssociatedInstanceId>i-hp325kt6307wxxxxxxxx</AssociatedInstanceId>
			      <RealBandwidth>0</RealBandwidth>
		    </Ipv6Address>
		    <Ipv6Address>
			      <Ipv6AddressId>ipv6-hp331xt3oqafdxxxxxxxx</Ipv6AddressId>
			      <AssociatedInstanceType>EcsInstance</AssociatedInstanceType>
			      <AllocationTime>2018-11-30T07:39:31Z</AllocationTime>
			      <Ipv6InternetBandwidth>
				        <BusinessStatus></BusinessStatus>
				        <Ipv6InternetBandwidthId></Ipv6InternetBandwidthId>
				        <InternetChargeType></InternetChargeType>
				        <Bandwidth>0</Bandwidth>
			      </Ipv6InternetBandwidth>
			      <VSwitchId>vsw-hp3ju1q8dtgfgxxxxxxxx</VSwitchId>
			      <VpcId>vpc-hp3kzilwd9yflxxxxxxxx</VpcId>
			      <Ipv6GatewayId>ipv6gw-hp33p10bdbt77xxxxxxxx</Ipv6GatewayId>
			      <Status>Available</Status>
			      <NetworkType>Private</NetworkType>
			      <Ipv6Address>2408:xxxx:c0:200:35b:cd32:c460:6aa3</Ipv6Address>
			      <Ipv6AddressName>abc</Ipv6AddressName>
			      <AssociatedInstanceId>i-hp37gpsnhjn4xxxxxxxx</AssociatedInstanceId>
			      <RealBandwidth>0</RealBandwidth>
		    </Ipv6Address>
	  </Ipv6Addresses>
	  <PageSize>10</PageSize>
	  <RequestId>AA4486A8-B6AE-469E-AB09-820EF8ECFA2B</RequestId>
</DescribeIpv6Addresses>
```

`JSON` format

```
{
	"PageNumber":1,
	"TotalCount":2,
	"Ipv6Addresses":{
		"Ipv6Address":[
			{
				"Ipv6AddressId":"ipv6-hp32vv2klzw4yxxxxxxxx",
				"AssociatedInstanceType":"EcsInstance",
				"AllocationTime":"2019-01-07T05:16:23Z",
				"Ipv6InternetBandwidth":{
					"BusinessStatus":"",
					"Ipv6InternetBandwidthId":"",
					"InternetChargeType":"",
					"Bandwidth":0
				},
				"VSwitchId":"vsw-hp3lyltb1dosjxxxxxxxx",
				"VpcId":"vpc-hp34hflqqsjh3xxxxxxxx",
				"Ipv6GatewayId":"",
				"Status":"Available",
				"NetworkType":"Private",
				"Ipv6Address":"2408:xxxx:0:2900:2901:3c61:9ff0:8fdc",
				"Ipv6AddressName":"",
				"AssociatedInstanceId":"i-hp325kt6307wxxxxxxxx",
				"RealBandwidth":0
			},
			{
				"Ipv6AddressId":"ipv6-hp331xt3oqafdxxxxxxxx",
				"AssociatedInstanceType":"EcsInstance",
				"AllocationTime":"2018-11-30T07:39:31Z",
				"Ipv6InternetBandwidth":{
					"BusinessStatus":"",
					"Ipv6InternetBandwidthId":"",
					"InternetChargeType":"",
					"Bandwidth":0
				},
				"VSwitchId":"vsw-hp3ju1q8dtgfgxxxxxxxx",
				"VpcId":"vpc-hp3kzilwd9yflxxxxxxxx",
				"Ipv6GatewayId":"ipv6gw-hp33p10bdbt77xxxxxxxx",
				"Status":"Available",
				"NetworkType":"Private",
				"Ipv6Address":"2408:xxxx:c0:200:35b:cd32:c460:6aa3",
				"Ipv6AddressName":"abc",
				"AssociatedInstanceId":"i-hp37gpsnhjn4xxxxxxxx",
				"RealBandwidth":0
			}
		]
	},
	"PageSize":10,
	"RequestId":"AA4486A8-B6AE-469E-AB09-820EF8ECFA2B"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

