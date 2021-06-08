# AllocateIpv6InternetBandwidth

Purchases Internet bandwidth resources for an IPv6 address.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=AllocateIpv6InternetBandwidth&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AllocateIpv6InternetBandwidth|The operation that you want to perform. Set the value to **AllocateIpv6InternetBandwidth**. |
|Bandwidth|Integer|Yes|2|The amount of Internet bandwidth resources of the IPv6 address, in Mbit/s. Valid values: **1 to 5000**.

 -   If **InternetChargeType** is set to **PayByBandwidth**, the Internet bandwidth of the IPv6 address is from 1 to 5,000 Mbit/s.
-   If **InternetChargeType** is set to **PayByTraffic**, the amount of Internet bandwidth resources of the IPv6 address is limited by the specification of the IPv6 gateway.
    -   Small \(default\) specifies the Free edition and the Internet bandwidth is from 1 to 500 Mbit/s.
    -   Medium specifies the Medium edition and the Internet bandwidth is from 1 to 1,000 Mbit/s.
    -   Large specifies the Large edition and the Internet bandwidth is from 1 to 2,000 Mbit/s. |
|Ipv6AddressId|String|Yes|ipv6-123456xxxxxxxx|The ID of the IPv6 address. |
|Ipv6GatewayId|String|Yes|ipv5gw-123456xxxxxxxx|The ID of the IPv6 gateway. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|ClientToken|String|No|123456|The client token that is used to ensure the idempotence of the request.

 You can use the client to generate a token, but you must ensure that the token is unique among different requests. The token can contain only ASCII characters and cannot exceed 64 characters in length. |
|InternetChargeType|String|No|PayByTraffic|The metering method of the Internet bandwidth resources of the IPv6 gateway. Valid values:

 -   **PayByTraffic**: pay-by-data-transfer
-   **PayByBandwidth** \(default\): pay-by-bandwidth |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|InternetBandwidthId|String|2|The amount of Internet bandwidth resources purchased for the IPv6 gateway. |
|Ipv6AddressId|String|ipv6-hp352ungkzcknxxxxxxxx|The ID of the IPv6 address. |
|RequestId|String|6972A26E-99B1-4367-9890-FBDEBB0F5E7D|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?AllocateIpv6InternetBandwidth
&Ipv6AddressId=ipv6-123456xxxxxxxx
&Ipv6GatewayId=ipv6gw-123456xxxxxxxx
&RegionId=cn-huhehaote
&<Common request parameters>

```

Sample success responses

`XML` format

```
<AllocateIpv6InternetBandwidthResponse>
	  <RequestId>6972A26E-99B1-4367-9890-FBDEBB0F5E7D</RequestId>
	  <InternetBandwidthId>2</InternetBandwidthId>
	  <Ipv6AddressId>ipv6-hp352ungkzcknxxxxxxxx</Ipv6AddressId>
</AllocateIpv6InternetBandwidthResponse>
```

`JSON` format

```
{
	"Ipv6AddressId":"ipv6-hp352ungkzcknxxxxxxxx",
	"RequestId":"6972A26E-99B1-4367-9890-FBDEBB0F5E7D",
	"InternetBandwidthId":2
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID is invalid. Check whether the service is available in the specified region.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

