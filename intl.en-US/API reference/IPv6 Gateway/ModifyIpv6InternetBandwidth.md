# ModifyIpv6InternetBandwidth

Modifies the amount of Internet bandwidth resources of an IPv6 address.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=ModifyIpv6InternetBandwidth&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyIpv6InternetBandwidth|The operation that you want to perform. Set the value to **ModifyIpv6InternetBandwidth**. |
|Bandwidth|Long|Yes|4|The amount of Internet bandwidth resources of the IPv6 address, in Mbit/s. Valid values: **1** to **5000**.

 -   If **InternetChargeType** is set to **PayByBandwidth**, the Internet bandwidth of the IPv6 address is from **1** to **5,000** Mbit/s.
-   If **InternetChargeType** is set to **PayByTraffic**, the amount of Internet bandwidth resources of the IPv6 address is limited by the specification of the IPv6 gateway.
    -   **Small** \(default\) specifies the Free edition and the Internet bandwidth is from **1** to **500** Mbit/s.
    -   **Medium** specifies the Medium edition and the Internet bandwidth is from **1** to **1,000** Mbit/s.
    -   **Large** specifies the Large edition and the Internet bandwidth is from **1** to **2,000** Mbit/s. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|Ipv6AddressId|String|No|ipv6-1233456\*\*\*\*|The ID of the IPv6 address. |
|ClientToken|String|No|123456|The client token that is used to ensure the idempotence of the request.

 You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can contain only ASCII characters and cannot exceed 64 characters in length. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|D560AF68-4CE8-4A5C-B3FE-469F558094D0|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyIpv6InternetBandwidth
&Bandwidth=4
&RegionId=cn-huhehaote
&Common request parameters
```

Sample success responses

`XML` format

```
<ModifyIpv6InternetBandwidthResponse>
	  <RequestId>D560AF68-4CE8-4A5C-B3FE-469F558094D0</RequestId>
</ModifyIpv6InternetBandwidthResponse>
```

`JSON` format

```
{
	"RequestId": "D560AF68-4CE8-4A5C-B3FE-469F558094D0"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

