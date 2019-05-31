# DescribeIpv6GatewayAttribute {#doc_api_910118 .reference}

调用DescribeIpv6GatewayAttribute接口查询指定IPV6网关的详细信息。

## 调试 {#apiExplorer .section}

单击[这里](https://api.aliyun.com/#product=Vpc&api=DescribeIpv6GatewayAttribute)在OpenAPI Explorer中进行可视化调试，并生成SDK代码示例。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeIpv6GatewayAttribute|要执行的操作，取值：**DescribeIpv6GatewayAttribute**。

 |
|Ipv6GatewayId|String|是|ipv6gw-123456|要查询的IPv6网关ID。

 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|BusinessStatus|String|Normal|IPv6网关的商业状态，取值：

 -   Normal：正常
-   FinacialLocked：欠费锁定
-   SecurityLocked：安全锁定

 |
|CreationTime|String|2018-12-05T09:21:35Z|IPv6网关的创建时间。

 |
|Description|String|test|IPv6网关的描述信息。

 |
|ExpiredTime|String|2018-12-05T09:21:35Z|IPv6网关的过期时间。

 |
|InstanceChargeType|String|PostPaid|IPv6网关的计费方式。

 |
|Ipv6GatewayId|String|ipv6gw-123456|IPv6网关的实例ID。

 |
|Name|String|test|IPv6网关的名称。

 |
|RegionId|String|cn-huhehaote|IPv6网关所在的地域ID。

 |
|RequestId|String|ipv6gw-hp33p10bdbt77xbeq6sgj|请求ID。

 |
|Spec|String|Medium|IPv6网关的规格。

 |
|Status|String|Available|IPv6网关的状态。

 |
|VpcId|String|vpc-123456|IPv6网关所在的VPC ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.cn-huhehaote.aliyuncs.com/?Action=DescribeIpv6GatewayAttribute
&Ipv6GatewayId=ipv6gw-hp33p10bdbt77xbeq6sgj
&RegionId=cn-huhehaote
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
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

`JSON` 格式

``` {#json_return_success_demo}
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

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

