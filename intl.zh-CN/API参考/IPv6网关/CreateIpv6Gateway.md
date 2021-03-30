# CreateIpv6Gateway

调用CreateIpv6Gateway接口创建IPv6网关。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=CreateIpv6Gateway&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateIpv6Gateway|要执行的操作，取值：**CreateIpv6Gateway**。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|VpcId|String|是|vpc-123sedrfswd23\*\*\*\*|要开通IPv6网关的VPC ID。 |
|Spec|String|否|Small|IPv6网关的规格，取值：

 -   **Small**（默认值）：免费版。
-   **Medium**：企业版。
-   **Large**：企业增强版。

 不同规格的IPv6网关的转发能力都不同。详细信息，请参见[IPv6网关规格](~~98926~~)。 |
|Name|String|否|ipv6GW|IPv6网关的名称。

 长度为2~128个字符，必须以字母或中文开头，可包含数字、点号（.）、下划线（\_）和短橫线（-），但不能以`http://`或`https://`开头。 |
|Description|String|否|ipv6gatewayforVPC1|IPv6网关的描述信息。

 长度为2~256个字符，必须以字母或中文开头，可包含数字、点号（.）、下划线（\_）和短橫线（-），但不能以`http://`或`https://`开头。 |
|ClientToken|String|否|123456|客户端token，用于保证请求的幂等性。

 由客户端生成该参数值，要保证在不同请求间唯一，最大值不超过64个ASCII字符。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6GatewayId|String|ipv6gw-hp3y0l3ln89j8cdvf\*\*\*\*|IPv6网关的ID。 |
|RequestId|String|0ED8D006-F706-4D23-88ED-E11ED28DCAC|请求ID。 |

## 示例

请求示例

```
https://vpc.aliyuncs.com/?Action=CreateIpv6Gateway
&RegionId=cn-huhehaote
&VpcId=vpc-123sedrfswd23****
&公共请求参数
```

正常返回示例

`XML` 格式

```
<CreateIpv6GatewayResponse>
        <RequestId>0ED8D006-F706-4D23-88ED-E11ED28DCAC0</RequestId>
        <Ipv6GatewayId>ipv6gw-hp3y0l3ln89j8cdvf****</Ipv6GatewayId>
</CreateIpv6GatewayResponse>
```

`JSON` 格式

```
{
    "RequestId": "0ED8D006-F706-4D23-88ED-E11ED28DCAC0",
    "Ipv6GatewayId": "ipv6gw-hp3y0l3ln89j8cdvf****"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

