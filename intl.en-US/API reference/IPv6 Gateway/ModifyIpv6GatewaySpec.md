# ModifyIpv6GatewaySpec

Changes the specification of an IPv6 gateway.

The forwarding and bandwidth capacity of an IPv6 gateway is based on the specification of the IPv6 gateway. For more information, see [Editions of IPv6 gateways](~~98926~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=ModifyIpv6GatewaySpec&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyIpv6GatewaySpec|The operation that you want to perform. Set the value to **ModifyIpv6GatewaySpec**. |
|Ipv6GatewayId|String|Yes|ipv6gw-123456xxxxxxxx|The ID of the IPv6 gateway. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|Spec|String|Yes|Middle|The new specification that you want to set for the IPv6 gateway. Valid values:

 -   **Small** \(default\): Free edition
-   **Middle**: Medium edition
-   **Large**: Large edition |
|ClientToken|String|No|123456|The client token that is used to ensure the idempotence of the request.

 You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can contain only ASCII characters and cannot exceed 64 characters in length. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=ModifyIpv6GatewaySpec
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456xxxxxxxx
&Spec=Middle
&Common request parameters

```

Sample success responses

`XML` format

```
<ModifyIpv6GatewaySpecResponse>
	  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
</ModifyIpv6GatewaySpecResponse>
```

`JSON` format

```
{
	"RequestId":"9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because RegionId is set to an invalid value. Check whether the service is available in the specified region.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

