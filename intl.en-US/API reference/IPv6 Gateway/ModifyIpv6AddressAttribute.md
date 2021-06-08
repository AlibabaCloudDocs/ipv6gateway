# ModifyIpv6AddressAttribute

Modifies the name and description of an IPv6 address.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=ModifyIpv6AddressAttribute&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyIpv6AddressAttribute|The operation that you want to perform. Set the value to **ModifyIpv6AddressAttribute**. |
|Ipv6AddressId|String|Yes|ipv6-hp32vv2klzw4yerdf\*\*\*\*|The ID of the IPv6 address. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 address is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|Name|String|No|test|The name of the IPv6 address.

 The name must be 2 to 128 characters in length, and can contain letters, digits, periods \(.\), underscores \(\_\), and hyphens \(-\). It cannot start with `http://` or `https://`. |
|Description|String|No|test|The description of the IPv6 address.

 The description must be 2 to 256 characters in length and can contain letters, digits, periods \(.\), underscores \(\_\), and hyphens \(-\). It cannot start with `http://` or `https://`. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|D560AF68-4CE8-4A5C-B3FE-469F558094D0|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyIpv6AddressAttribute
&Ipv6AddressId=ipv6-hp32vv2klzw4yerdf****
&RegionId=cn-huhehaote
&Common request parameters
```

Sample success responses

`XML` format

```
<ModifyIpv6AddressAttributeResponse>
	  <RequestId>D560AF68-4CE8-4A5C-B3FE-469F558094D0</RequestId>
</ModifyIpv6AddressAttributeResponse>
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
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because RegionId is set to an invalid value. Check whether the service is available in the specified region.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

