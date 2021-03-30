# ModifyIpv6AddressAttribute

调用ModifyIpv6AddressAttribute接口修改IPv6地址的名称和描述。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=ModifyIpv6AddressAttribute&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyIpv6AddressAttribute|要执行的操作，取值：**ModifyIpv6AddressAttribute**。 |
|Ipv6AddressId|String|是|ipv6-hp32vv2klzw4yerdf\*\*\*\*|IPv6地址的实例ID。 |
|RegionId|String|是|cn-huhehaote|IPv6地址所在的地域。您可以通过调用[DescribeRegions](~~36063~~)获取地域ID。 |
|Name|String|否|test|IPv6地址的名称。

 长度为2~128个字符，必须以字母或中文开头，可包含数字、点号（.）、下划线（\_）和短橫线（-）。但不能以`http://`或`https://`开头。 |
|Description|String|否|test|IPv6地址的描述信息。

 长度为2~256个字符，必须以字母或中文开头，可包含数字、点号（.）、下划线（\_）和短橫线（-）。但不能以`http://`或`https://`开头。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|D560AF68-4CE8-4A5C-B3FE-469F558094D0|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyIpv6AddressAttribute
&Ipv6AddressId=ipv6-hp32vv2klzw4yerdf****
&RegionId=cn-huhehaote
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ModifyIpv6AddressAttributeResponse>
	  <RequestId>D560AF68-4CE8-4A5C-B3FE-469F558094D0</RequestId>
</ModifyIpv6AddressAttributeResponse>
```

`JSON` 格式

```
{
	"RequestId": "D560AF68-4CE8-4A5C-B3FE-469F558094D0"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

