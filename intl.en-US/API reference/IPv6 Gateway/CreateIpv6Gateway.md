# CreateIpv6Gateway

Creates an IPv6 gateway.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateIpv6Gateway|The operation that you want to perform. Set the value to **CreateIpv6Gateway**. |
|RegionId|String|Yes|cn-huhehaote|The ID of the region where the IPv6 gateway is deployed. You can call the [DescribeRegions](~~36063~~) operation to query the most recent region list. |
|VpcId|String|Yes|vpc-123sedrfswd23\*\*\*\*|The ID of the virtual private cloud \(VPC\) for which you want to create the IPv6 gateway. |
|Spec|String|No|Small|The specification that you want to set for the IPv6 gateway. Valid values:

 -   **Small** \(default\): Free edition
-   **Medium**: Medium edition
-   **Large**: Large edition

 The forwarding and bandwidth capacity of an IPv6 gateway is based on the specification of the IPv6 gateway. For more information, see [Editions of IPv6 gateways](~~98926~~). |
|Name|String|No|ipv6GW|The name of the IPv6 gateway.

 The name must be 2 to 128 characters in length and can contain digits, periods \(.\), underscores \(\_\), and hyphens \(-\). It must start with a letter and cannot start with `http://` or `https://`. |
|Description|String|No|ipv6gatewayforVPC1|The description of the IPv6 gateway.

 The name must be 2 to 256 characters in length, and can contain letters, digits, periods \(.\), underscores \(\_\), and hyphens \(-\). It must start with a letter but cannot start with `http://` or `https://`. |
|ClientToken|String|No|123456|The client token that is used to ensure the idempotence of the request.

 You can use the client to generate the value, but you must ensure that it is unique among different requests. The token can contain only ASCII characters and cannot exceed 64 characters in length. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Ipv6GatewayId|String|ipv6gw-hp3y0l3ln89j8cdvf\*\*\*\*|The ID of the IPv6 gateway. |
|RequestId|String|0ED8D006-F706-4D23-88ED-E11ED28DCAC|The ID of the request. |

## Examples

Sample requests

```
https://vpc.aliyuncs.com/?Action=CreateIpv6Gateway
&RegionId=cn-huhehaote
&VpcId=vpc-123sedrfswd23****
&Common request parameters
```

Sample success responses

`XML` format

```
<CreateIpv6GatewayResponse>
        <RequestId>0ED8D006-F706-4D23-88ED-E11ED28DCAC0</RequestId>
        <Ipv6GatewayId>ipv6gw-hp3y0l3ln89j8cdvf****</Ipv6GatewayId>
</CreateIpv6GatewayResponse>
```

`JSON` format

```
{
    "RequestId": "0ED8D006-F706-4D23-88ED-E11ED28DCAC0",
    "Ipv6GatewayId": "ipv6gw-hp3y0l3ln89j8cdvf****"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because RegionId is set to an invalid value. Check whether the service is available in the specified region.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

