# AllocateIpv6InternetBandwidth

Purchases an Internet bandwidth for an IPv6 address.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|AllocateIpv6InternetBandwidth|The name of this action. Value: **AllocateIpv6InternetBandwidth** |
|Bandwidth|Integer|Yes|2|The Internet bandwidth of the IPv6 address. Unit: Mbit/s. Value range: **1 to 5000**

 -   If the value of **InternetChargeType** is **PayByBandwidth,** the IPv6 Internet bandwidth value range is 1 to 5000.
-   If the value of **InternetChargeType** is **PayByTraffic,** the IPv6 Internet bandwidth value range depends on the specification of the IPv6 Gateway.
    -   If the specification is Small \(the default version that is free\), the Internet bandwidth value range of the IPv6 address is 1 to 500.
    -   If the specification is Medium \(the enterprise version\), the Internet bandwidth value range of the IPv6 address is 1 to 1000.
    -   If the specification is Large \(the enhanced enterprise version\), the Internet bandwidth value range of the IPv6 address is 1 to 2000. |
|Ipv6AddressId|String|Yes|ipv6-123456|The instance ID of the IPv6 address. |
|Ipv6GatewayId|String|Yes|ipv5gw-123456|The ID of the IPv6 Gateway. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |
|ClientToken|String|No|123456|Optional. The client token. This parameter is used to ensure the idempotence of the request.

 The value of this parameter is generated by the client. Make sure that this value is unique among different requests and does not exceed 64 ASCII characters. |
|InternetChargeType|String|No|PayByTraffic|Optional. The billing method of the IPv6 Internet bandwidth. Valid values:

 -   **PayByTraffic:** traffic-based billing.
-   **PayByBandwidth** \(default value\): bandwidth-based billing. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|InternetBandwidthId|String|2|The purchased Internet bandwidth. |
|Ipv6AddressId|String|2408:4004:c0:200:35b:cd32:c460:6aa4|The IPv6 address. |
|RequestId|String|6972A26E-99B1-4367-9890-FBDEBB0F5E7D|The ID of the request. |

## Examples

Request example

```

https://vpc.cn-huhehaote.aliyuncs.com?Action=AllocateIpv6InternetBandwidth
&Bandwidth=2
&Ipv6AddressId=ipv6-hp351bytt9inrfp6tgubd
&Ipv6GatewayId=ipv6gw-hp38x2x0fz785tlc65pfv
&RegionId=cn-huhehaote
&CommobParameters
			
```

Response examples

`XML` format

```
<AllocateIpv6InternetBandwidthResponse>
  <RequestId>6972A26E-99B1-4367-9890-FBDEBB0F5E7D</RequestId>
  <InternetBandwidthId>2</InternetBandwidthId>
  <Ipv6AddressId>ipv6-hp352ungkzcknmeicfvss</Ipv6AddressId>
</AllocateIpv6InternetBandwidthResponse>
			
```

`JSON` format

```
{
	"Ipv6AddressId":"ipv6-hp352ungkzcknmeicfvss",
	"RequestId":"6972A26E-99B1-4367-9890-FBDEBB0F5E7D",
	"InternetBandwidthId":2
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified RegionId does not exist. Please check if the product is available in the specified region.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).
