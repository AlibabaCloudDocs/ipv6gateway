# What is an IPv6 Gateway？

This topic provides an overview of the IPv6 Gateways of Virtual Private Cloud \(VPC\). An IPv6 Gateway functions as an IPv6 traffic gateway for a VPC. You can configure the IPv6 Internet bandwidth and egress-only rules to manage the inbound and outbound IPv6 traffic.

![IPv6 Gateway diagram](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1310509951/p68034.png)

## Functions

The functions of an IPv6 gateway are as follows:

-   **IPv6 internal network communication**

    By default, an IPv6 address in a VPC is allocated with an Internet bandwidth of 0 Mbit/s and only supports communication over the internal network. Specifically, the cloud instances in a VPC can only access other IPv6 addresses in the same VPC through the IPv6 address. The resources cannot access the Internet with these IPv6 addresses or be accessed by IPv6 clients over the Internet.

-   **IPv6 public network communication**

    You can purchase an Internet bandwidth for the IPv6 address for which you have applied. In this way, the resources in the VPC can access the Internet through the IPv6 address and be accessed by IPv6 clients over the Internet.

    You can set the Internet bandwidth to 0 Mbit/s at any time to deny the IPv6 address Internet access. After this configuration, the IPv6 address can only communicate over the internal network.

-   **IPv6 public network communication with an egress-only rule**

    You can set an egress-only rule for an IPv6 Gateway. In this way, the IPv6 address can access the Internet, but IPv6 clients are denied access to your cloud resources in the VPC over the Internet.

    You can delete the egress-only rule at any time. After the rule is deleted, your resources in the VPC can access the Internet through the IPv6 address for which you have purchased Internet bandwidth, and IPv6 clients can access the resources in the VPC over the Internet.


The network access capability of IPv6 addresses is dependent on the settings of the network type, Internet bandwidth, and egress-only rule, as shown in the following table.

|IPv6 network type|Enable IPv6 Internet bandwidth?|Set an egress-only rule?|IPv6 network access capability|
|:----------------|:------------------------------|:-----------------------|:-----------------------------|
|Internal network|No|No|Internal network communication|
|Public network|Yes|No|Internal network communication

 Public network communication |
|Yes|Internal network communication

 Public network communication when access is initiated by VPCs |

## Benefits

IPv6 Gateway provides the following benefits:

-   **High availability**

    IPv6 Gateways provide cross-zone high availability and stable IPv6 Internet gateway services.

-   **High performance**

    A single IPv6 Gateway provides a 10-gigabit level throughput.

-   **Flexible management of public network communication**

    You can manage the Internet communication capability of an IPv6 Gateway by adjusting its Internet bandwidth and setting an egress-only rule.


