# DeleteIpv6Gateway

Deletes an IPv6 Gateway.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|DeleteIpv6Gateway|The name of this action. Value:**DeleteIpv6Gateway** |
|Ipv6GatewayId|String|Yes|ipv6gw-hp3y0l3ln89j8fv0m5som|The IPv6 Gateway to be deleted. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|RequestId|String|E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE|The ID of the request. |

## Examples

Request example

```


https://vpc.aliyuncs.com/?Action=DeleteIpv6Gateway
&RegionId=cn-hangzhou
&CidrBlock=10.10.0.0/24
&CommonParameters
			
```

Response examples

`XML` format

```
<DeleteIpv6GatewayResponse>
  <RequestId>E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE</RequestId>
</DeleteIpv6GatewayResponse>
			
```

`JSON` format

```
{
    "RequestId":"E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified RegionId does not exist. Please check if the product is available in the specified region.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).

