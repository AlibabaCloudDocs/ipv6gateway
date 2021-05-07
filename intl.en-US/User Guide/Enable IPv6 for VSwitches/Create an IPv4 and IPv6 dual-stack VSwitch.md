# Create an IPv4 and IPv6 dual-stack VSwitch

This topic describes how to assign an IPv6 CIDR block to a VSwitch when you create the VSwitch.

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc).

2.  In the left-side navigation pane, click **VSwitches**.

3.  Select the region where you want to deploy the VSwitch.

    **Note:** The following regions support IPv6 gateways: China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\).

4.  On the **VSwitches** page, click **Create VSwitch**.

5.  On the **Create VSwitch** page, configure the VSwitch and click **OK**. The following table describes the configuration parameters.

    |Parameter|Description|
    |:--------|:----------|
    |**Resource Group**|Select the resource group to which the VSwitch belongs.|
    |**VPC**|Select the VPC to which the VSwitch belongs.|
    |**CIDR Block**|The IPv4 CIDR block of the specified VPC.|
    |**IPv6 CIDR Block**|The IPv6 CIDR block of the specified VPC. **Note:** If the specified VPC does not have an IPv6 CIDR block, click **Enable IPv6 CIDR Block**. After IPv6 is enabled for the VPC, the system automatically creates an IPv6 gateway of the Free Edition for the VPC. |
    |**Parameter**|Enter a name for the VSwitch. The name must be 2 to 128 characters in length and can contain letters, digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**Zone**|Select a zone to deploy the VSwitch. VSwitches within a VPC can communicate with each other across zones over the internal network.|
    |**IPv4 CIDR Block**|Specify an IPv4 CIDR block for the VSwitch. Note the following limits when you specify an IPv4 CIDR block for a VSwitch:     -   The IPv4 CIDR block of a VSwitch must be a subset of the IPv4 CIDR block of the VPC to which the VSwitch belongs.

For example, if the IPv4 CIDR block of a VPC is 192.168.0.0/16, the IPv4 CIDR block of a VSwitch in the VPC must be a segment from 192.168.0.0/17 to 192.168.0.0/29.

    -   The subnet mask of a VSwitch IPv4 CIDR block can be 16 to 29 bits in length. This means that 8 to 65,536 IP addresses can be provided.
    -   The first and the last three IP addresses of each VSwitch IPv4 CIDR block are reserved.

For example, if the VSwitch IPv4 CIDR block is 192.168.1.0/24, the IP addresses 192.168.1.0, 192.168.1.253, 192.168.1.254, and 192.168.1.255 are reserved.

    -   If the VSwitch is required to communicate with VSwitches in other VPCs or with on-premises data centers, make sure that the IPv4 CIDR blocks involved do not conflict with each other.
    -   The IPv4 CIDR block of a VSwitch must not be the same or larger than the CIDR range of a route in any of the VPC route tables.

For example, if a CEN route \(overlapping routing enabled\) with a destination of 172.16.0.0/24 is already added to a route table of the VPC, you cannot specify a CIDR block of the same or larger range as the IPv4 CIDR block of the VSwitch. However, you can use 172.16.0.0/25 or one of a smaller range as the IPv4 CIDR block of the VSwitch.

**Note:** After you create a VSwitch, you cannot modify its IPv4 CIDR block. |
    |**Number of Available Private IPs**|The number of available IPv4 addresses of the VSwitch.|
    |**IPv6 CIDR Block**|Specify an IPv6 CIDR block for the VSwitch.

The default subnet mask for the IPv6 CIDR block of a VSwitch is /64. You can enter a decimal number ranging from 0 to 255 to define the last 8 bits of the IPv6 CIDR block.

For example, if the IPv6 CIDR block of the VPC that contains the VSwitch is 2xx1:db8::/64, you can enter 255 \(FF in hexadecimal notation\) in this field to define the IPv6 CIDR block of the VSwitch as 2xx1:db8:ff::/64. |
    |**Description**|Enter a description for the VSwitch. The description must be 2 to 256 characters in length and cannot start with `http://` or `https://`. |


