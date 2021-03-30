# Create a dual-stack VSwitch that supports both IPv4 and IPv6 addresses

This topic describes how to enable an IPv6 CIDR block when you create a VSwitch. After the IPv6 CIDR block is enabled, the system allocates an IPv6 CIDR block to the VSwitch.

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc).

2.  In the left-side navigation pane, click **VSwitches**.

3.  Select the region where you want to deploy a VSwitch.

    **Note:** The following regions support IPv6 gateways: China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Beijing\), China \(Hohhot\), China \(Chengdu\), China \(Hong Kong\), and Singapore \(Singapore\)..

4.  Click **Create VSwitch**, configure the VSwitch based on the following parameters, and then click **OK**.

    |Parameter|Description|
    |:--------|:----------|
    |**Resource Group**|The resource set to which the VSwitch belongs.|
    |**VPC**|The VPC network to which the VSwitch belongs.|
    |**CIDR Block**|The IPv4 CIDR block of the VPC network.|
    |**IPv6 CIDR Block**|The IPv6 CIDR block of the VPC. **Note:** If IPv6 CIDR block is not enabled for the VPC, click **Enable IPv6**. After the IPv6 CIDR block is enabled, the system automatically creates an IPv6 Gateway free of charge. |
    |**Name**|The name of the VSwitch. The name must be 2 to 128 characters in length and can contain letters, digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**Zone**|The zone of the VSwitch. In a VPC network, VSwitches in different zones can communicate with each other.|
    |**IPv4 CIDR Block**|The IPv4 CIDR block of the VSwitch. Note the following limits when you specify the VSwitch CIDR block:     -   The CIDR block of the VSwitch must be a subset of the CIDR block of the VPC network.

For example, if the CIDR block of a VPC network is 192.168.0.0/16, the CIDR block of the VSwitch can be any CIDR block from 192.168.0.0/17 to 192.168.0.0/29.

    -   The subnet mask of the VSwitch CIDR block can be 16 to 29 bits. This means the VSwitch can provide 8 to 65,536 IP addresses.
    -   The first and last three IP addresses of each VSwitch are reserved.

For example, if the VSwitch CIDR block is 192.168.1.0/24, the IP addresses 192.168.1.0, 192.168.1.253, 192.168.1.254, and 192.168.1.255 are reserved.

    -   If the VSwitch is required to communicate with VSwitches in other VPCs or with on-premises data centers, make sure that the CIDR blocks involved do not conflict with each other.
    -   The CIDR block of a VSwitch cannot be the same as or larger than the destination CIDR block of a route in route tables of the VPC network to which the VSwitch belongs.

For example, if Cloud Enterprise Network \(overlapping routing enabled\) is added to a VPC network routing table and the destination CIDR block is 172.16.0.0/24, you cannot create the same or a larger CIDR block as the CIDR block of the VSwitch. However, you can create CIDR block 172.16.0.0/25 or a smaller CIDR block as the CIDR block of the VSwitch.

**Note:** After you create a VSwitch, you cannot modify its CIDR block. |
    |**Number of Available Private IPs**|The number of available IPv4 addresses of the VSwitch.|
    |**IPv6 CIDR Block**|The IPv6 CIDR block of the VSwitch.

By default, the mask for the IPv6 CIDR block of a VSwitch is /64. You can enter a number from 0 to 255 to define the last 8 bits of the IPv6 CIDR block.

For example, if the IPv6 CIDR block of the VPC network is 2xx1:db8::/64, you can enter ff \(the hexadecimal string of 255\) for the IPv6 CIDR block of the VSwitch. The IPv6 CIDR block of the VSwitch is 2xx1:db8:ff::/64. |
    |**Description**|The description of the VSwitch. The description must be 2 to 256 characters in length and cannot start with `http://` or `https://`. |


