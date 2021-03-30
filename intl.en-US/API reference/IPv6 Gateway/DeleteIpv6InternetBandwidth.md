# DeleteIpv6InternetBandwidth

Deletes the Internet bandwidth of an IPv6 address.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|DeleteIpv6InternetBandwidth|The name of this action. Value: **DeleteIpv6InternetBandwidth** |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |
|Ipv6AddressId|String|No|ipv6-123456|Optional. The ID of the IPv6 address. |
|Ipv6InternetBandwidthId|String|No|2|Optional. The ID of the Internet bandwidth of the IPv6 address. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|RequestId|String|E07E0FE6-5C21-405F-AF82-7613AA81EF92|The ID of the request. |

## Examples

Request example

```

https://vpc.cn-huhehaote.aliyuncs.com?Action=DeleteIpv6InternetBandwidth
&Ipv6AddressId=ipv6-hp351bytt9inrfp6tgubd
&RegionId=cn-huhehaote
&CommonParameters
			
```

Response examples

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
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified RegionId does not exist. Please check if the product is available in the specified region.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).

