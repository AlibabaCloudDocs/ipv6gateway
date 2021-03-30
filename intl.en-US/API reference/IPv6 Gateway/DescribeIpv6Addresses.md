# DescribeIpv6Addresses

Queries one or more IPv6 addresses.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|DescribeIpv6Addresses|The name of this action. Value: **DescribeIpv6Addresses** |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 address belongs. |
|AssociatedInstanceId|String|No|i-123456|Optional. The ID of the instance associated with the IPv6 address. |
|AssociatedInstanceType|String|No|EcsInstance|Optional. The type of the instance associated with the IPv6 address. Value:

 -   **EcsInstance** \(default value\): ECS instances of the VPC type. |
|Ipv6Address|String|No|2408:4004:180:1701:94c7:bc38:3bfa:d2c|Optional. The IPv6 address to be queried. |
|Ipv6AddressId|String|No|ipv6gw-hp33of4uz4k4k7ccwhk95|Optional. The instance ID of the IPv6 address. Up to 20 IDs can be entered in a single API call. Separate multiple IDs with commas \(,\). |
|Ipv6InternetBandwidthId|String|No|1|Optional. The ID of the Internet bandwidth instance of the IPv6 address. |
|Name|String|No|test|Optional. The name of the IPv6 address. |
|NetworkType|String|No|Public|Optional. The network access capabilities of the IPv6 address. Valid values:

 -   **Private** : communication over the intranet.
-   **Public** : communication over the Internet. |
|PageNumber|Integer|No|1|Optional. The page number of the list. Default value: 1. |
|PageSize|Integer|No|10|Optional. The number of rows per page. Maximum value: 50. Default value: 10. |
|VSwitchId|String|No|vsw-123456|Optional. The ID of the VSwitch to which the IPv6 address belongs. |
|VpcId|String|No|vpc-123456|Optional. The ID of the VPC to which the IPv6 address belongs. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|Ipv6Addresses| | |Details of the IPv6 address. |
|└AllocationTime|String|2018-12-20T14:56:09Z|The time when the IPv6 address is created. |
|└AssociatedInstanceId|String|i-hp325kt6307whusdxxx|The ID of the instance associated with the IPv6 address. |
|└AssociatedInstanceType|String|EcsInstance|The type of the instance associated with the IPv6 address. |
|└Ipv6Address|String|2408:4004:0:2900:2901:3c61:9ff0:xxxx|The IPv6 address. |
|└Ipv6AddressId|String|ipv6-hp32vv2klzw4yr4dzxxx|The instance ID of the IPv6 address. |
|└Ipv6AddressName|String|test|The instance name of the IPv6 address. |
|└Ipv6GatewayId|String|ipv6gw-hp38x2x0fz785tlc6xx|The ID of the IPv6 Gateway to which the IPv6 address belongs. |
|└Ipv6InternetBandwidth| | |The Internet bandwidth details of the IPv6 address. |
|└Bandwidth|Integer|2|The dedicated Internet bandwidth of the IPv6 address. Unit: Mbit/s |
|└BusinessStatus|String|Normal|The status of the dedicated Internet bandwidth of the IPv6 address. Valid values:

 -   Normal: Indicates that the Internet bandwidth is normal.
-   FinacialLocked: Indicates that the Internet bandwidth is locked due to overdue bills.
-   SecurityLocked: Indicates that the Internet bandwidth is locked for security purposes. |
|└InstanceChargeType|String|PostPaid|The billing method of the IPv6 Gateway. Value:

 -   **PostPaid** : Pay-As-You-Go. |
|└InternetChargeType|String|PayByTraffic|The billing method of the IPv6 Gateway. Valid values:

 -   **PayByTraffic** : traffic-based billing.
-   **PayByBandwidth** : bandwidth-based billing. |
|└Ipv6InternetBandwidthId|String|ipv6bw-hp3b35oq1fj50kbvmxxx|The ID of the Internet bandwidth instance. |
|└NetworkType|String|Public|The network access capabilities of the IPv6 address. Valid values:

 -   **Private** : communication over the intranet.
-   **Public** : communication over the Internet. |
|└RealBandwidth|Integer|2|The actual peak bandwidth of the IPv6 address.

 -   If the IPv6 address is added to an Internet Shared Bandwidth instance, the value of **RealBandwidth** is the peak bandwidth of the Internet Shared Bandwidth instance.
-   If the IPv6 address is not added to any Internet Shared Bandwidth instance, the value of **RealBandwidth** is the Internet bandwidth of the IPv6 address.
-   If the IPv6 address is not added to any Internet Shared Bandwidth instance and you have not purchased any Internet bandwidth for the IPv6 address, the values of **RealBandwidth** and **Bandwidth** are 0. |
|└Status|String|Available|The status of the IPv6 address. Valid values:

 -   **Pending** : Indicates that the IPv6 address is being configured.
-   **Available** : Indicates that the IPv6 address is ready for use. |
|└VSwitchId|String|vsw-hp3123456|The ID of the VSwitch to which the IPv6 address belongs. |
|└VpcId|String|vpc-123456|The ID of the VPC to which the IPv6 address belongs. |
|PageNumber|Integer|1|The page number of the list. Default value: 1. |
|PageSize|Integer|10|The number of rows per page. Maximum value: 50. Default value: 10. |
|RequestId|String|AA4486A8-B6AE-469E-AB09-820EF8ECFA2B|The ID of the request. |
|TotalCount|Integer|2|The number of entries in the list. |

## Examples

Request example

```

https://vpc.cn-huhehaote.aliyuncs.com/?Action=DescribeIpv6Addresses
&RegionId=huhehaote
&CommonParameters
			
```

Response examples

`XML` format

```
<DescribeIpv6AddressesResponse>
  <PageNumber>1</PageNumber>
  <TotalCount>2</TotalCount>
  <Ipv6Addresses>
    <Ipv6Address>
      <Ipv6AddressId>ipv6-hp32vv2klzw4yr4dz83a2</Ipv6AddressId>
      <AssociatedInstanceType>EcsInstance</AssociatedInstanceType>
      <AllocationTime>2019-01-07T05:16:23Z</AllocationTime>
      <Ipv6InternetBandwidth>
        <BusinessStatus/>
        <Ipv6InternetBandwidthId/>
        <InternetChargeType/>
        <Bandwidth>0</Bandwidth>
      </Ipv6InternetBandwidth>
      <VSwitchId>vsw-hp3lyltb1dosj540yyxjv</VSwitchId>
      <VpcId>vpc-hp34hflqqsjh3a3q7lbtr</VpcId>
      <Ipv6GatewayId/>
      <Status>Available</Status>
      <NetworkType>Private</NetworkType>
      <Ipv6Address>2408:4004:0:2900:2901:3c61:9ff0:8fdc</Ipv6Address>
      <Ipv6AddressName/>
      <AssociatedInstanceId>i-hp325kt6307whusddmnu</AssociatedInstanceId>
      <RealBandwidth>0</RealBandwidth>
    </Ipv6Address>
    <Ipv6Address>
      <Ipv6AddressId>ipv6-hp331xt3oqafdxvwvna9n</Ipv6AddressId>
      <AssociatedInstanceType>EcsInstance</AssociatedInstanceType>
      <AllocationTime>2018-11-30T07:39:31Z</AllocationTime>
      <Ipv6InternetBandwidth>
        <BusinessStatus/>
        <Ipv6InternetBandwidthId/>
        <InternetChargeType/>
        <Bandwidth>0</Bandwidth>
      </Ipv6InternetBandwidth>
      <VSwitchId>vsw-hp3ju1q8dtgfg8iib14ql</VSwitchId>
      <VpcId>vpc-hp3kzilwd9yflssfdlgqe</VpcId>
      <Ipv6GatewayId>ipv6gw-hp33p10bdbt77xbeq6sgj</Ipv6GatewayId>
      <Status>Available</Status>
      <NetworkType>Private</NetworkType>
      <Ipv6Address>2408:4004:c0:200:35b:cd32:c460:6aa3</Ipv6Address>
      <Ipv6AddressName>name</Ipv6AddressName>
      <AssociatedInstanceId>i-hp37gpsnhjn4kf3bzr8t</AssociatedInstanceId>
      <RealBandwidth>0</RealBandwidth>
    </Ipv6Address>
  </Ipv6Addresses>
  <PageSize>10</PageSize>
  <RequestId>AA4486A8-B6AE-469E-AB09-820EF8ECFA2B</RequestId>
</DescribeIpv6AddressesResponse>
			
```

`JSON` format

```
{
	"PageNumber":1,
	"TotalCount":2,
	"Ipv6Addresses":{
		"Ipv6Address":[
			{
				"Ipv6AddressId":"ipv6-hp32vv2klzw4yr4dz83a2",
				"AssociatedInstanceType":"EcsInstance",
				"AllocationTime":"2019-01-07T05:16:23Z",
				"Ipv6InternetBandwidth":{
					"BusinessStatus":"",
					"Ipv6InternetBandwidthId":"",
					"InternetChargeType":"",
					"Bandwidth":0
				},
				"VSwitchId":"vsw-hp3lyltb1dosj540yyxjv",
				"VpcId":"vpc-hp34hflqqsjh3a3q7lbtr",
				"Ipv6GatewayId":"",
				"Status":"Available",
				"NetworkType":"Private",
				"Ipv6Address":"2408:4004:0:2900:2901:3c61:9ff0:8fdc",
				"Ipv6AddressName":"",
				"AssociatedInstanceId":"i-hp325kt6307whusddmnu",
				"RealBandwidth":0
			},
			{
				"Ipv6AddressId":"ipv6-hp331xt3oqafdxvwvna9n",
				"AssociatedInstanceType":"EcsInstance",
				"AllocationTime":"2018-11-30T07:39:31Z",
				"Ipv6InternetBandwidth":{
					"BusinessStatus":"",
					"Ipv6InternetBandwidthId":"",
					"InternetChargeType":"",
					"Bandwidth":0
				},
				"VSwitchId":"vsw-hp3ju1q8dtgfg8iib14ql",
				"VpcId":"vpc-hp3kzilwd9yflssfdlgqe",
				"Ipv6GatewayId":"ipv6gw-hp33p10bdbt77xbeq6sgj",
				"Status":"Available",
				"NetworkType":"Private",
				"Ipv6Address":"2408:4004:c0:200:35b:cd32:c460:6aa3",
				"Ipv6AddressName":"name",
				"AssociatedInstanceId":"i-hp37gpsnhjn4kf3bzr8t",
				"RealBandwidth":0
			}
		]
	},
	"PageSize":10,
	"RequestId":"AA4486A8-B6AE-469E-AB09-820EF8ECFA2B"
}
```

## Error codes

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).

