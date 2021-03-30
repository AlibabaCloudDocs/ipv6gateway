# ModifyIpv6GatewayAttribute

Modifies the information of an IPv6 gateway.

## Debug

[Use OpenAPI Explorer to perform debug operations and generate SDK code examples.](https://api.aliyun.com/#product=Vpc&api=ModifyIpv6GatewayAttribute&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|ModifyIpv6GatewayAttribute|The action to perform. Valid value: **ModifyIpv6GatewayAttribute**. |
|Ipv6GatewayId|String|Yes|ipv6gw-hp39kh1ya51yzp2lu\*\*\*\*|The ID of the IPv6 gateway to be modified. |
|RegionId|String|Yes|cn-huhehaote|The region ID of the IPv6 gateway. To query the region ID, call [DescribeRegions](~~36063~~). |
|Description|String|No|ipv6description|The description of the IPv6 gateway. |
|Name|String|No|ipv6name|The name of the IPv6 gateway. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|The ID of the request. |

## Examples

Request example

```

https://vpc.aliyuncs.com/?Action=ModifyIpv6GatewayAttribute
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-hp39kh1ya51yzp2lu****
&<CommonParameters>

```

Response example:

`XML` format

```
<ModifyIpv6GatewayAttributeResponse>
	  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
</ModifyIpv6GatewayAttributeResponse>
```

`JSON` format

```
{
	"RequestId":"9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75"
}
```

## Errors

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified RegionId does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

