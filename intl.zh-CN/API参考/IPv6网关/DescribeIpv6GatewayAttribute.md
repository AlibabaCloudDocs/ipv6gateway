# DescribeIpv6GatewayAttribute

调用DescribeIpv6GatewayAttribute接口查询指定IPV6网关的详细信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6GatewayAttribute&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeIpv6GatewayAttribute|要执行的操作，取值：**DescribeIpv6GatewayAttribute**。 |
|Ipv6GatewayId|String|是|ipv6gw-123456xxxxxxxx|要查询的IPv6网关ID。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|BusinessStatus|String|Normal|IPv6网关的状态，取值：

 -   **Normal**：正常。
-   **FinacialLocked**：欠费锁定。
-   **SecurityLocked**：安全锁定。 |
|CreationTime|String|2018-12-05T09:21:35Z|IPv6网关的创建时间。 |
|Description|String|test|IPv6网关的描述信息。 |
|ExpiredTime|String|2018-12-05T09:21:35Z|IPv6网关的过期时间。 |
|InstanceChargeType|String|PostPaid|IPv6网关的计费方式。 |
|Ipv6GatewayId|String|ipv6gw-123456xxxxxxxx|IPv6网关的实例ID。 |
|Name|String|test|IPv6网关的名称。 |
|RegionId|String|cn-huhehaote|IPv6网关所在的地域ID。 |
|RequestId|String|ipv6gw-hp33p10bdbt77xxxxxxxx|请求ID。 |
|Spec|String|Medium|IPv6网关的规格。 |
|Status|String|Available|IPv6网关的状态。 |
|VpcId|String|vpc-123456xxxxxxxx|IPv6网关所在的VPC ID。 |

## 示例

请求示例

```

https://vpc.cn-huhehaote.aliyuncs.com/?Action=DescribeIpv6GatewayAttribute
&Ipv6GatewayId=ipv6gw-hp33p10bdbt77xxxxxxxx
&RegionId=cn-huhehaote
&公共请求参数

```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

