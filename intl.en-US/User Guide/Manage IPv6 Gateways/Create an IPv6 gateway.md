# Create an IPv6 gateway

This topic describes how to create an IPv6 gateway for a VPC. After you create an IPv6 gateway, you can purchase IPv6 Internet bandwidth and set egress-only rules for the IPv6 gateway.

Make sure that IPv6 is enabled for the VPC before you create an IPv6 gateway for the VPC. For more information, see [Allocate an IPv6 CIDR block when you create a VPC](/intl.en-US/User Guide/Enable IPv6 for VPCs/Create an IPv4 and IPv6 dual-stack VPC.md) and [Enable an IPv6 CIDR block for a VPC network](/intl.en-US/User Guide/Enable IPv6 for VPCs/Enable an IPv6 CIDR block for a VPC network.md).

1.  Log on to the [IPv6 gateway console](https://vpc.console.aliyun.com/ipv6).

2.  On the **IPv6 Gateway** page, click **Create IPv6 Gateway**.

3.  Specify the following information and click **Buy Now** to make the payment.

    |Parameter|Description|
    |:--------|:----------|
    |**Region and Zone**|Select a region to deploy the IPv6 gateway. The IPv6 gateway must belong to the same region as the VPC for which you want to create the IPv6 gateway.

**Note:** The following regions support IPv6 gateways: China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\). |
    |**VPC ID**|Select the VPC for which you want to create an IPv6 gateway. The target VPC may not be available due to the following reasons:     -   Only one IPv6 gateway can be created for each VPC. The VPC already has an IPv6 gateway.
    -   The VPC has a custom route with the destination CIDR block set to ::/0. If this happens, you must delete this custom route before you can create an IPv6 gateway for the VPC.
 **Note:** After an IPv6 gateway is created, you cannot change the VPC that is associated with the IPv6 gateway. |
    |**Edition**|Select the edition of the IPv6 gateway. IPv6 gateways are available in the following editions:     -   Free Edition
    -   Enterprise Edition
    -   Enhanced Enterprise Edition
 Different quotas and limits apply to IPv6 gateways of different editions, such as the maximum forwarding bandwidth, maximum IPv6 bandwidth per IPv6 address, and maximum number of egress-only rules. For more information, see [Editions of IPv6 gateways](/intl.en-US/User Guide/Manage IPv6 Gateways/IPv6 Gateway specifications.md). |
    |**Billing Cycle**|IPv6 gateway instances are billed on a daily basis. For more information, see [Billing](/intl.en-US/Pricing/Pricing.md).|


