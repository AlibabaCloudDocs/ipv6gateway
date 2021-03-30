# ModifyIpv6AddressAttribute

Modifies the name and description of an IPv6 address.

## Debug

[Use OpenAPI Explorer to perform debug operations and generate SDK code examples.](https://api.aliyun.com/#product=Vpc&api=ModifyIpv6AddressAttribute&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|ModifyIpv6AddressAttribute|The action to perform. Valid value: **ModifyIpv6AddressAttribute**. |
|Ipv6AddressId|String|Yes|ipv6-hp32vv2klzw4yerdf\*\*\*\*|The instance ID of the IPv6 address. |
|RegionId|String|Yes|cn-huhehaote|The region of the IPv6 address. To query the region ID, call [DescribeRegions](~~36063~~). |
|Description|String|No|test|The description of the IPv6 address.

 The description must be 2 to 256 characters in length and can contain letters, numbers, periods \(.\), underscores \(\_\), and hyphens \(-\). It must start with a letter. It cannot start with `http://`or `https://`. |
|Name|String|No|test|The name of the IPv6 address.

 The name must be 2 to 128 characters in length and can contain letters, numbers, periods \(.\), underscores \(\_\), and hyphens \(-\). The name must start with a letter. It cannot start with `http://`or `https://`. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|RequestId|String|D560AF68-4CE8-4A5C-B3FE-469F558094D0|The ID of the request. |

## Examples

Request example

```

https://vpc.cn-huhehaote.aliyuncs.com/?Action=ModifyIpv6AddressAttribute
&Ipv6AddressId=ipv6-hp331xt3oqafdxvwv****
&Name=test
&RegionId=cn-huhehaote
&<CommonParameters>


```

Response example:

`XML` format

```
<ModifyIpv6AddressAttributeResponse>
	  <RequestId>D560AF68-4CE8-4A5C-B3FE-469F558094D0</RequestId>
</ModifyIpv6AddressAttributeResponse>
```

`JSON` format

```
{
	"RequestId":"D560AF68-4CE8-4A5C-B3FE-469F558094D0"
}
```

## Errors

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified region ID does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

