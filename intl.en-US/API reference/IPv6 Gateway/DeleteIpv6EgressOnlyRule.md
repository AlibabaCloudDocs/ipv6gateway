# DeleteIpv6EgressOnlyRule

Deletes an egress-only rule.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6EgressOnlyRule&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteIpv6EgressOnlyRule|The operation that you want to perform. Set the value to **DeleteIpv6EgressOnlyRule**. |
|Ipv6EgressOnlyRuleId|String|Yes|ipv6py-hp3w98rmlbqp0xxxxxxxx|The ID of the egress-only rule that you want to delete. |
|RegionId|String|Yes|cn-huhehaote|The ID of the IPv6 gateway. |
|ClientToken|String|No|123456|The client token that is used to ensure the idempotence of the request.

 You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can contain only ASCII characters and cannot exceed 64 characters in length. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=DeleteIpv6EgressOnlyRule
&RegionId=cn-huhehaote
&Ipv6GatewayId=ipv6gw-123456
&Ipv6EgressOnlyRuleId=ipv6py-hp3w98rmlbqp0xxxxxxxx
&Common request parameters

```

Sample success responses

`XML` format

```
<DeleteIpv6EgressOnlyRuleResponse>
	  <RequestId>9DFEDBEE-E5AB-49E8-A2DC-CC114C67AF75</RequestId>
</DeleteIpv6EgressOnlyRuleResponse>
```

`JSON` format

```
{
	"RequestId":"4E40EAF1-783D-4C05-948D-DA0426C398C1"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

