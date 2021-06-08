# DeleteIpv6InternetBandwidth

Sets the Internet bandwidth value of an IPv6 address to zero.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6InternetBandwidth&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteIpv6InternetBandwidth|The operation that you want to perform. Set the value to **DeleteIpv6InternetBandwidth**. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|Ipv6AddressId|String|No|ipv6-123456xxxxxxxx|The ID of the IPv6 address. |
|Ipv6InternetBandwidthId|String|No|2|The Internet bandwidth value of the IPv6 address. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E07E0FE6-5C21-405F-AF82-7613AA81EF92|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=DeleteIpv6InternetBandwidth
&RegionId=cn-huhehaote
&<Common request parameters>

```

Sample success responses

`XML` format

```
<DeleteIpv6InternetBandwidthResponse>
	  <RequestId>6972A26E-99B1-4367-9890-FBDEBB0F5E7D</RequestId>
</DeleteIpv6InternetBandwidthResponse>
```

`JSON` format

```
{
	"RequestId":"E07E0FE6-5C21-405F-AF82-7613AA81EF92"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified RegionId parameter is invalid. Check whether the service is available in the specified region.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

