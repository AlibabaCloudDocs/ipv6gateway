# AllocateIpv6InternetBandwidth

调用AllocateIpv6InternetBandwidth接口为IPv6地址购买公网带宽。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=AllocateIpv6InternetBandwidth&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AllocateIpv6InternetBandwidth|要执行的操作，取值：**AllocateIpv6InternetBandwidth**。 |
|Bandwidth|Integer|是|2|IPv6地址的公网带宽，单位：Mbps，取值范围：**1-5000**。

 -   当**InternetChargeType**为**PayByBandwidth**，IPv6地址的公网带宽为1-5000。
-   当**InternetChargeType**为**PayByTraffic**，IPv6地址的公网带宽范围同时受到IPv6网关规格的制约。
    -   Small（默认免费版），公网带宽范围为1-500。
    -   Medium（企业版），公网带宽范围为1-1000。
    -   Large（企业增强版），公网带宽范围为1-2000。 |
|Ipv6AddressId|String|是|ipv6-123456xxxxxxxx|IPv6地址的实例ID。 |
|Ipv6GatewayId|String|是|ipv5gw-123456xxxxxxxx|IPv6网关的ID。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|ClientToken|String|否|123456|请求的幂等性。

 由客户端生成该参数值，要保证在不同请求间唯一，最大值不超过64个ASCII字符。 |
|InternetChargeType|String|否|PayByTraffic|IPv6公网带宽的计费方式，取值：

 -   **PayByTraffic**：按使用流量计费。
-   **PayByBandwidth**（默认值）：按带宽计费。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InternetBandwidthId|String|2|购买的公网带宽。 |
|Ipv6AddressId|String|ipv6-hp352ungkzcknxxxxxxxx|IPv6地址的实例ID。 |
|RequestId|String|6972A26E-99B1-4367-9890-FBDEBB0F5E7D|请求ID。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?AllocateIpv6InternetBandwidth
&Ipv6AddressId=ipv6-123456xxxxxxxx
&Ipv6GatewayId=ipv6gw-123456xxxxxxxx
&RegionId=cn-huhehaote
&<公共请求参数>

```

正常返回示例

`XML` 格式

```
<AllocateIpv6InternetBandwidthResponse>
	  <RequestId>6972A26E-99B1-4367-9890-FBDEBB0F5E7D</RequestId>
	  <InternetBandwidthId>2</InternetBandwidthId>
	  <Ipv6AddressId>ipv6-hp352ungkzcknxxxxxxxx</Ipv6AddressId>
</AllocateIpv6InternetBandwidthResponse>
```

`JSON` 格式

```
{
	"Ipv6AddressId":"ipv6-hp352ungkzcknxxxxxxxx",
	"RequestId":"6972A26E-99B1-4367-9890-FBDEBB0F5E7D",
	"InternetBandwidthId":2
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

