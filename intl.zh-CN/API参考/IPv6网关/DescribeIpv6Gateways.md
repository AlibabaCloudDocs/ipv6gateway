# DescribeIpv6Gateways

调用DescribeIpv6Gateways接口查询已创建的IPv6网关。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6Gateways&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeIpv6Gateways|要执行的操作，取值：**DeleteIpv6Gateway**。 |
|RegionId|String|是|cn-huhehaote|IPv6网关所属的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|Ipv6GatewayId|String|否|ipv6gw-123456xxxxxxxx|IPv6网关的ID。 |
|Name|String|否|ipv6GW|IPv6网关的名称。 |
|PageNumber|Integer|否|1|当前页码。 |
|PageSize|Integer|否|10|每页包含的条目数。 |
|VpcId|String|否|vpc-123456xxxxxxxx|IPv6网关关联的VPC ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6Gateways| | |IPv6网关的详细信息。 |
|BusinessStatus|String|Normal|IPv6网关的状态，取值：

 -   **Normal**：正常。
-   **FinancialLocked**：欠费锁定。 |
|CreationTime|String|2018-12-20T14:51:23Z|IPv6网关的创建时间。 |
|Description|String|descriptionforIPv6GW|IPv6网关的描述信息。 |
|ExpiredTime|String|2018-12-20T14:51:23Z|IPv6网关的过期时间。 |
|InstanceChargeType|String|PostPaid|IPv6网关的计费方式。 |
|Ipv6GatewayId|String|ipv6gw-hp3rwmtmfhgisxxxxxxxx|IPv6网关的ID。 |
|Name|String|name|IPv6网关的名称。 |
|RegionId|String|cn-huhehaote|IPv6网关的地域。 |
|Spec|String|Small|IPv6网关的规格。 |
|Status|String|Available|IPv6网关的运行状态。 |
|VpcId|String|vpc-123456xxxxxxxx|IPv6网关关联的VPC ID。 |
|PageNumber|Integer|1|当前页码。 |
|PageSize|Integer|19|每页包含的条目数。 |
|RequestId|String|E3A06196-3E7C-490D-8F39-CB4B5A0CE8AD|请求ID。 |
|TotalCount|Integer|2|查询到的条目数量。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?Action=DescribeIpv6Gateways
&RegionId=cn-huhehaote
&公共请求参数

```

正常返回示例

`XML` 格式

```
<DescribeIpv6GatewaysResponse>
	  <PageNumber>1</PageNumber>
	  <Ipv6Gateways>
		    <Ipv6Gateway>
			      <Name></Name>
			      <CreationTime>2018-12-20T14:51:23Z</CreationTime>
			      <Status>Available</Status>
			      <Description></Description>
			      <BusinessStatus>Normal</BusinessStatus>
			      <Spec>Medium</Spec>
			      <RegionId>cn-huhehaote</RegionId>
			      <InstanceChargeType>PostPaid</InstanceChargeType>
			      <ExpiredTime></ExpiredTime>
			      <VpcId>vpc-hp3ag7ydchedxxxxxxxxx</VpcId>
			      <Ipv6GatewayId>ipv6gw-hp33of4uz4k4kxxxxxxxx</Ipv6GatewayId>
		    </Ipv6Gateway>
		    <Ipv6Gateway>
			      <CreationTime>2018-12-05T09:21:35Z</CreationTime>
			      <Name>IPv6网关</Name>
			      <Status>Available</Status>
			      <Description></Description>
			      <BusinessStatus>Normal</BusinessStatus>
			      <Spec>Medium</Spec>
			      <RegionId>cn-huhehaote</RegionId>
			      <InstanceChargeType>PostPaid</InstanceChargeType>
			      <ExpiredTime></ExpiredTime>
			      <VpcId>vpc-hp3kzilwd9yflxxxxxxxx</VpcId>
			      <Ipv6GatewayId>ipv6gw-hp33p10bdbt77xxxxxxxx</Ipv6GatewayId>
		    </Ipv6Gateway>
	  </Ipv6Gateways>
	  <TotalCount>2</TotalCount>
	  <PageSize>10</PageSize>
	  <RequestId>E3A06196-3E7C-490D-8F39-CB4B5A0CE8AD</RequestId>
</DescribeIpv6GatewaysResponse>
```

`JSON` 格式

```
{
	"Ipv6Gateways":{
		"Ipv6Gateway":[
			{
				"CreationTime":"2018-12-20T14:51:23Z",
				"Name":"",
				"Status":"Available",
				"Description":"",
				"Spec":"Medium",
				"BusinessStatus":"Normal",
				"RegionId":"cn-huhehaote",
				"InstanceChargeType":"PostPaid",
				"ExpiredTime":"",
				"VpcId":"vpc-hp3ag7ydchedxxxxxxxxx",
				"Ipv6GatewayId":"ipv6gw-hp33of4uz4k4kxxxxxxxx"
			},
			{
				"Name":"IPv6网关",
				"CreationTime":"2018-12-05T09:21:35Z",
				"Status":"Available",
				"Description":"",
				"Spec":"Medium",
				"BusinessStatus":"Normal",
				"RegionId":"cn-huhehaote",
				"InstanceChargeType":"PostPaid",
				"ExpiredTime":"",
				"VpcId":"vpc-hp3kzilwd9yflxxxxxxxx",
				"Ipv6GatewayId":"ipv6gw-hp33p10bdbt77xxxxxxxx"
			}
		]
	},
	"PageNumber":1,
	"TotalCount":2,
	"PageSize":10,
	"RequestId":"E3A06196-3E7C-490D-8F39-CB4B5A0CE8AD"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

