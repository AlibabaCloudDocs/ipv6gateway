# Terms

This topic describes the terms used in IPv6 Gateway.

|Term|Description|
|:---|:----------|
|IPv6 address|The IPv6 address allocated by the system to an instance in a VPC. An IPv6 address is made of 128 binary bits that are divided into eight 16-bit groups separated by colons \(:\). Each group is represented as a 4-digit hexadecimal number. The following is an example of an IPv6 address:

 2001:xxx:0102::0304 |
|IPv6 gateway|The Internet gateway for IPv6 traffic flowing in and out of a VPC. You can use an IPv6 gateway to control and manage the bandwidth used by IPv6 traffic. IPv6 gateways allow you to create egress-only rules to funnel egress traffic.|
|IPv6 Internet bandwidth|The Internet bandwidth of an IPv6 address that limits the bandwidth of Internet connectivity for the IPv6 address. You must purchase and add IPv6 Internet bandwidth to an IPv6 address before the IPv6 address can be used to communicate over the Internet. |
|Egress-only rule|A rule by which an IPv6 gateway implements egress control for IPv6 traffic. After you configure an egress-only rule for an IPv6 address, the IPv6 gateway allows outbound only communication to the Internet over IPv6 using the IPv6 address, and prevents the Internet from initiating IPv6 connections with the instance associated with the IPv6 address. |
|IPv6 CIDR block for VPC|A /56 IPv6 CIDR block automatically allocated to a VPC after IPv6 is enabled for the VPC.|
|IPv6 CIDR block for VSwitch|An IPv6 CIDR block allocated to a VSwitch. The default subnet mask for the IPv6 CIDR block of a VSwitch is /64. When you enable IPv6 for a VSwitch, you can specify the last eight bits of the IPv6 CIDR block of the VSwitch.|

