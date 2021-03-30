# DescribeIpv6Gateways

Queries one or more created IPv6 Gateways.

## Debug

We recommend that you use [OpenAPI Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway) to call APIs, generate SDK code examples, perform debug operations, and search for APIs.

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|DescribeIpv6Gateways|The name of this action. Value: **DeleteIpv6Gateway** |
|RegionId|String|Yes|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |
|Ipv6GatewayId|String|No|ipv6gw-123456|Optional. The ID of the IPv6 Gateway. |
|Name|String|No|ipv6GW|Optional. The name of the IPv6 Gateway. |
|PageNumber|Integer|No|1|Optional. The current page number. |
|PageSize|Integer|No|10|Optional. The number of entries per page. |
|VpcId|String|No|vpc-123456|Optional. The ID of the VPC with which the IPv6 Gateway is associated. |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|Ipv6Gateways| | |A list of IPv6 Gateways. |
|└BusinessStatus|String|Normal|The status of the IPv6 Gateway. |
|└CreationTime|String|2018-12-20T14:51:23Z|The time when the IPv6 Gateway is created. |
|└Description|String|descriptionforIPv6GW|The description of the IPv6 Gateway. |
|└ExpiredTime|String|2018-12-20T14:51:23Z|The time when the IPv6 Gateway expires. |
|└InstanceChargeType|String|PostPaid|The billing method of the IPv6 Gateway. |
|└Ipv6GatewayId|String|ipv6gw-hp3rwmtmfhgistofzypyf|The ID of the IPv6 Gateway. |
|└Name|String|name|The name of the IPv6 Gateway. |
|└RegionId|String|cn-huhehaote|The ID of the region to which the IPv6 Gateway belongs. |
|└Spec|String|Small|The specification of the IPv6 Gateway. |
|└Status|String|Available|The status of the IPv6 Gateway. |
|└VpcId|String|vpc-123456|The ID of the VPC with which the IPv6 Gateway is associated. |
|PageNumber|Integer|1|The current page number. |
|PageSize|Integer|19|The number of entries per page. |
|RequestId|String|E3A06196-3E7C-490D-8F39-CB4B5A0CE8AD|The ID of the request. |
|TotalCount|Integer|2|The number of IPv6 Gateways. |

## Examples

Request example

```


https://vpc.aliyuncs.com/?Action=DescribeIpv6Gateways
&RegionId=cn-huhehaote
&CommonParameters
			
```

Response examples

`XML` format

```
<DescribeIpv6GatewaysResponse>
  <PageNumber>1</PageNumber>
  <Ipv6Gateways>
    <Ipv6Gateway>
      <Name/>
      <CreationTime>2018-12-20T14:51:23Z</CreationTime>
      <Status>Available</Status>
      <Description/>
      <BusinessStatus>Normal</BusinessStatus>
      <Spec>Medium</Spec>
      <RegionId>cn-huhehaote</RegionId>
      <InstanceChargeType>PostPaid</InstanceChargeType>
      <ExpiredTime/>
      <VpcId>vpc-hp3ag7ydchedxpt0smw00</VpcId>
      <Ipv6GatewayId>ipv6gw-hp33of4uz4k4k7ccwhk95</Ipv6GatewayId>
    </Ipv6Gateway>
    <Ipv6Gateway>
      <CreationTime>2018-12-05T09:21:35Z</CreationTime>
      <Name>IPv6 Gateway</Name>
      <Status>Available</Status>
      <Description/>
      <BusinessStatus>Normal</BusinessStatus>
      <Spec>Medium</Spec>
      <RegionId>cn-huhehaote</RegionId>
      <InstanceChargeType>PostPaid</InstanceChargeType>
      <ExpiredTime/>
      <VpcId>vpc-hp3kzilwd9yflssfdlgqe</VpcId>
      <Ipv6GatewayId>ipv6gw-hp33p10bdbt77xbeq6sgj</Ipv6GatewayId>
    </Ipv6Gateway>
  </Ipv6Gateways>
  <TotalCount>2</TotalCount>
  <PageSize>10</PageSize>
  <RequestId>E3A06196-3E7C-490D-8F39-CB4B5A0CE8AD</RequestId>
</DescribeIpv6GatewaysResponse>
			
```

`JSON` format

```
{
    "Ipv6Gateways":{
        "Ipv6Gateway":[
            {
                "CreationTime":"2018-12-20T14:51:23Z",
                "Name":"",
                "Status":"Available",
                "Description":"",
                "Spec":"Medium",
                "BusinessStatus":"Normal",
                "RegionId":"cn-huhehaote",
                "InstanceChargeType":"PostPaid",
                "ExpiredTime":"",
                "VpcId":"vpc-hp3ag7ydchedxpt0smw00",
                "Ipv6GatewayId":"ipv6gw-hp33of4uz4k4k7ccwhk95"
            },
            {
                "Name":"IPv6 Gateway",
                "CreationTime":"2018-12-05T09:21:35Z",
                "Status":"Available",
                "Description":"",
                "Spec":"Medium",
                "BusinessStatus":"Normal",
                "RegionId":"cn-huhehaote",
                "InstanceChargeType":"PostPaid",
                "ExpiredTime":"",
                "VpcId":"vpc-hp3kzilwd9yflssfdlgqe",
                "Ipv6GatewayId":"ipv6gw-hp33p10bdbt77xbeq6sgj"
            }
        ]
    },
    "PageNumber":1,
    "TotalCount":2,
    "PageSize":10,
    "RequestId":"E3A06196-3E7C-490D-8F39-CB4B5A0CE8AD"
}
```

## Error codes

[See common error codes](https://error-center.aliyun.com/status/product/Vpc).

