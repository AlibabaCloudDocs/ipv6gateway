# DescribeIpv6Addresses

调用DescribeIpv6Addresses接口查询IPv6地址列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6Addresses&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeIpv6Addresses|要执行的操作，取值：**DescribeIpv6Addresses**。 |
|RegionId|String|是|cn-huhehaote|IPv6地址所在的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|AssociatedInstanceId|String|否|i-123456xxxxxxxx|IPv6地址关联的实例ID。 |
|AssociatedInstanceType|String|否|EcsInstance|IPv6地址所关联的实例类型，取值：

 **EcsInstance**（默认值）：VPC类型的ECS。 |
|Ipv6Address|String|否|2408:xxxx:180:1701:94c7:bc38:3bfa:d2c|要查询的IPv6地址。 |
|Ipv6AddressId|String|否|ipv6gw-hp33of4uz4k4kxxxxxxxx|IPv6地址实例的ID。每次调用最多可以输入20个实例ID，以逗号（,）分隔。 |
|Ipv6InternetBandwidthId|String|否|1|IPv6地址的公网带宽。 |
|Name|String|否|test|IPv6地址的名称。 |
|NetworkType|String|否|Public|IPv6地址的通信能力类型，取值：

 -   **Private**：私网通信类型。
-   **Public**：公网通信类型。 |
|PageNumber|Integer|否|1|列表的页码，默认值为1。 |
|PageSize|Integer|否|10|分页查询时每页的行数，最大值为50，默认值为10。 |
|VSwitchId|String|否|vsw-123456xxxxxxxx|IPv6地址所在的交换机ID。 |
|VpcId|String|否|vpc-123456xxxxxxxx|IPv6地址所在的VPC ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6Addresses| | |IPv6地址的详细信息。 |
|AllocationTime|String|2018-12-20T14:56:09Z|IPv6地址的创建时间。 |
|AssociatedInstanceId|String|i-hp325kt6307xxxxxxxx|IPv6地址关联的实例ID。 |
|AssociatedInstanceType|String|EcsInstance|IPv6地址关联的实例类型。 |
|Ipv6Address|String|2408:xxxx:0:2900:2901:3c61:9ff0:xxxx|IPv6地址。 |
|Ipv6AddressId|String|ipv6-hp32vv2klzw4xxxxxxxx|IPv6地址的实例ID。 |
|Ipv6AddressName|String|test|IPv6地址的实例名称。 |
|Ipv6GatewayId|String|ipv6gw-hp38x2x0fz7xxxxxxxx|IPv6地址的所属IPv6网关ID。 |
|Ipv6InternetBandwidth| | |IPv6地址的公网带宽信息。 |
|Bandwidth|Integer|2|IPv6地址的独享公网带宽，单位Mbps。 |
|BusinessStatus|String|Normal|IPv6地址的独享带宽的商业状态，取值：

 -   Normal：正常。
-   FinacialLocked：欠费锁定。
-   SecurityLocked：安全锁定。 |
|InstanceChargeType|String|PostPaid|IPv6网关的付费方式，取值：

 **PostPaid**：后付费。 |
|InternetChargeType|String|PayByTraffic|IPv6网关的计费方式，取值：

 -   **PayByTraffic**：按流量计费。
-   **PayByBandwidth**：按带宽计费。 |
|Ipv6InternetBandwidthId|String|ipv6bw-hp3b35oq1fj50kbvmxxx|公网带宽ID。 |
|NetworkType|String|Public|IPv6地址的通信能力类型，取值：

 -   **Private**：私网通信类型。
-   **Public**：公网通信类型 。 |
|RealBandwidth|Integer|2|IPv6地址的实际带宽峰值：

 -   如果加入了共享带宽，则**RealBandwidth**的值为共享带宽峰值。
-   如果没有加入，则**RealBandwidth**的值即IPv6本身的公网带宽。
-   如果IPv6地址没有加入共享带宽，且本身没有购买公网带宽，则**RealBandwidth**和**Bandwidth**的值都为零。 |
|Status|String|Available|IPv6地址的状态，取值：

 -   **Pending**：配置中。
-   **Available**：可用。 |
|VSwitchId|String|vsw-hp3123456xxxxxxxx|IPv6地址所在的交换机的ID。 |
|VpcId|String|vpc-123456xxxxxxxx|IPv6地址所在的VPC ID。 |
|PageNumber|Integer|1|列表的页码，默认值为1。 |
|PageSize|Integer|10|分页查询时每页的行数，最大值为50，默认值为10。 |
|RequestId|String|AA4486A8-B6AE-469E-AB09-820EF8ECFA2B|请求ID。 |
|TotalCount|Integer|2|列表条目数。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?Action=DescribeIpv6Addresses
&RegionId=cn-huhehaote
&<公共请求参数>

```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

