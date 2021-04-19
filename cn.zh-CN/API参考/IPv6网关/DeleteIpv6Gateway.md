# DeleteIpv6Gateway

调用DeleteIpv6Gateway接口删除IPv6网关。

## 前提条件

删除企业版和企业增强版IPv6网关前，请先删除仅主动出规则。更多信息，请参见[DeleteIpv6EgressOnlyRule](~~102201~~)。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6Gateway&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteIpv6Gateway|要执行的操作，取值：**DeleteIpv6Gateway**。 |
|Ipv6GatewayId|String|是|ipv6gw-hp3y0l3ln89j8\*\*\*\*|要删除的IPv6网关实例ID。 |
|RegionId|String|是|cn-huhehaote|IPv6网关所属的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteIpv6Gateway
&Ipv6GatewayId=ipv6gw-hp3y0l3ln89j8****
&RegionId=cn-huhehaote
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DeleteIpv6GatewayResponse>
      <RequestId>E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE</RequestId>
</DeleteIpv6GatewayResponse>
```

`JSON`格式

```
{
	"RequestId": "E9A8AABE-A84B-4AF2-A68A-8E2EA190E7AE"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的regionid不存在。|

访问[错误中心](https://error-center.aliyun.com/status/product/Vpc)查看更多错误码。

