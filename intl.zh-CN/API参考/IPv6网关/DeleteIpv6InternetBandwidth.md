# DeleteIpv6InternetBandwidth

调用DeleteIpv6InternetBandwidth接口删除公网带宽。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DeleteIpv6InternetBandwidth&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteIpv6InternetBandwidth|要执行的操作，取值：**DeleteIpv6InternetBandwidth**。 |
|RegionId|String|是|cn-huhehaote|IPv6网关的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|Ipv6AddressId|String|否|ipv6-123456xxxxxxxx|IPv6地址的实例ID。 |
|Ipv6InternetBandwidthId|String|否|2|IPv6地址的公网带宽。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E07E0FE6-5C21-405F-AF82-7613AA81EF92|请求ID。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?Action=DeleteIpv6InternetBandwidth
&RegionId=cn-huhehaote
&<公共请求参数>

```

正常返回示例

`XML` 格式

```
<DeleteIpv6InternetBandwidthResponse>
	  <RequestId>6972A26E-99B1-4367-9890-FBDEBB0F5E7D</RequestId>
</DeleteIpv6InternetBandwidthResponse>
```

`JSON` 格式

```
{
	"RequestId":"E07E0FE6-5C21-405F-AF82-7613AA81EF92"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

