# DeleteIpv6Gateway

Deletes an IPv6 gateway.

## Prerequisites

Before you can delete an IPv6 gateway of the Enterprise Edition or Advanced Enterprise Edition, you must delete the egress-only rule. For more information, see [DeleteIpv6EgressOnlyRule](~~102201~~) .

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6Gateway&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteIpv6Gateway|The name of this action. Value: **DeleteIpv6Gateway**. |
|Ipv6GatewayId|String|Yes|ipv6gw-hp3y0l3ln89j8\*\*\*\*|The ID of the IPv6 gateway to be deleted. |
|RegionId|String|Yes|cn-huhehaote|The region ID of the IPv6 gateway. You can call [DescribeRegions](~~36063~~) Interface to obtain the region ID. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE|The ID of the request. |

## Examples

Sample requests

```

     http(s)://[Endpoint]/?Action=DeleteIpv6Gateway &Ipv6 GatewayId=ipv6gw-hp3y0l3ln89j8 **** &RegionId=cn-huhehaote &<public request parameters> 
   
```

Sample success responses

`XML`format

```

     <DeleteIpv6GatewayResponse> <RequestId>E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE</RequestId> </DeleteIpv6GatewayResponse> 
   
```

`JSON`Address format

```

     { "RequestId": "E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE" } 
   
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified Region ID does not exist.|

Go to the [Error Center](https://error-center.alibabacloud.com/status/product/Vpc) see more error codes.

