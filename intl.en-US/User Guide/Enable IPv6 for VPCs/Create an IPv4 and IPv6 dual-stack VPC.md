# Create an IPv4 and IPv6 dual-stack VPC

This topic describes how to configure both IPv4 and IPv6 CIDR blocks for a VPC when you create the VPC. By default, all VPCs are associated with IPv4 CIDR blocks which cannot be deleted. However, you can choose whether to allocate an IPv6 CIDR blocks to a VPC. After you choose to allocate an IPv6 CIDR block to a VPC, the system creates an IPv6 gateway of the Free Edition for the VPC for you to provision IPv6 bandwidth and manage IPv6 traffic.

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc).

2.  On the top of the page, select a region to deploy your VPC.

    **Note:** The following regions support IPv6 gateways: China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Chengdu\), China \(Hong Kong\), and Singapore \(Singapore\)..

3.  On the VPCs page, click **Create VPC**.

4.  On the Create VPC page, specify the following information and then click **OK**.

    |Parameter|Description|
    |:--------|:----------|
    |**VPC**|
    |**Region**|The region where the VPC network is to be deployed.|
    |**Name**|Enter a name for the VPC. The name must be 2 to 128 characters in length and can contain letters, digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**IPv4 CIDR Block**|Specify an IPv4 CIDR block for the VPC. The following setting methods are supported:     -   **Recommended CIDR Block**: Use 192.168.0.0/16, 172.16.0.0/12, or 10.0.0.0/8 as the IPv4 CIDR block of the VPC.
    -   **Custom CIDR Block**: Use 192.168.0.0/16, 172.16.0.0/12, 10.0.0.0/8, or one of their subnets as the IPv4 CIDR block of the VPC. The subnet mask must be 8 to 24 bits in length. For example, enter 192.168.0.0/16. If you need to use a public CIDR block as the IPv4 CIDR block of the VPC, [submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/add?productId=1218).
**Note:** After you create a VPC, you cannot modify its IPv4 CIDR block. |
    |**IPv6 CIDR Block**|Specify whether to assign an IPv6 CIDR block to the VPC. By default, no IPv6 CIDR block is assigned. If you set this parameter to Allocate, the system automatically creates an IPv6 gateway of the Free Edition for your VPC network, and assigns an IPv6 CIDR block with subnet mask /56, such as 2xx1: db8::/56. By default, IPv6 addresses can only be used for communication within private networks. If you need to enable an IPv6 address to access and be accessed over the Internet, you must purchase IPv6 Internet bandwidth for the IPv6 address. For more information, see [Enable Internet connectivity for an IPv6 address](/intl.en-US/User Guide/Manage IPv6 Internet bandwidth/Enable Internet connectivity for an IPv6 address.md).

**Note:** After you create a VPC, you cannot modify its IPv6 CIDR block. |
    |**Description**|Enter a description for the VPC. The description must be 2 to 256 characters in length and cannot start with `http://` or `https://`. |
    |**VSwitch**|
    |**Parameter**|Enter a name for the VSwitch. The name must be 2 to 128 characters in length and can contain letters, digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**Zone**|Select the zone to which the VSwitch belongs. VSwitches within a VPC can communicate with each other across zones over the internal network.|
    |**Zone Resource**|The cloud instances that can be created in the specified zone. The supported cloud resources vary, depending on the zone and the time when you want to create cloud resources. The buy page displays which cloud instances are available. You can check the availability of Elastic Compute Service \(ECS\) instances, ApsaraDB for RDS instances, and Server Load Balancer \(SLB\) instances on the buy page. |
    |**IPv4 CIDR Block**|Specify an IPv4 CIDR block for the VSwitch. Note the following limits when you specify an IPv4 CIDR block for a VSwitch:     -   The IPv4 CIDR block of a VSwitch must be a subset of the IPv4 CIDR block of the VPC to which the VSwitch belongs.

For example, if the IPv4 CIDR block of a VPC is 192.168.0.0/16, the IPv4 CIDR block of a VSwitch in the VPC must be a segment from 192.168.0.0/17 to 192.168.0.0/29.

    -   The subnet mask of a VSwitch IPv4 CIDR block can be 16 to 29 bits in length. This means that 8 to 65,536 IP addresses can be provided.
    -   The first and the last three IP addresses of each VSwitch IPv4 CIDR block are reserved.

For example, if the VSwitch IPv4 CIDR block is 192.168.1.0/24, the IP addresses 192.168.1.0, 192.168.1.253, 192.168.1.254, and 192.168.1.255 are reserved.

    -   If the VSwitch is required to communicate with VSwitches in other VPCs or with on-premises data centers, make sure that the IPv4 CIDR blocks involved do not conflict with each other.
    -   The IPv4 CIDR block of a VSwitch must not be the same or larger than the CIDR range of a route in any of the VPC route tables.

For example, if a Cloud Enterprise Network \(CEN\) route \(overlapping routing enabled\) with a destination of 172.16.0.0/24 is already added to a route table of the VPC, you cannot specify a CIDR block of the same or larger range as the IPv4 CIDR block of the VSwitch. However, you can use 172.16.0.0/25 or one of a smaller range as the IPv4 CIDR block of the VSwitch.

**Note:** After you create a VSwitch, you cannot modify its IPv4 CIDR block. |
    |**Number of Available Private IPs**|The number of available IP addresses.|
    |**IPv6 CIDR Block**|Specify an IPv6 CIDR block for the VSwitch. The default subnet mask for the IPv6 CIDR block of a VSwitch is /64. You can enter a decimal number ranging from 0 to 255 to define the last 8 bits of the IPv6 CIDR block.

For example, if the IPv6 CIDR block of the VPC that contains the VSwitch is 2xx8:4004:c0:b900::/56, you can enter 255 \(FF in hexadecimal notation\) in this field to define the IPv6 CIDR block of the VSwitch as 2xx8:4004:c0:b9ff::/64. |
    |**Description**|Enter a description for the VSwitch. The description must be 2 to 256 characters in length and cannot start with `http://` or `https://`. |


