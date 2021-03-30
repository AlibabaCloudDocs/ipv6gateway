# Create an IPv6 VPC

This topic describes how to create a Virtual Private Cloud \(VPC\) with an IPv6 CIDR block. After you create a VPC with an IPv6 CIDR block, you can associate it with an ECS instance and enable the IPv6 Internet bandwidth for the VPC.

## Step 1: Create a VPC and a VSwitch

To deploy cloud resources in a VPC, you must complete network planning. For more information, see [Plan and design a VPC](/intl.en-US/Quick Start/Plan and design a VPC.md).

To create a VPC and a VSwitch, follow these steps:

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  Select the region in which you want to create a VPC.

    The VPC must be in the same region as the cloud resources that you want to deploy. In this topic, **China \(Hohhot\)** is selected.

    **Note:** IPv6 CIDR blocks are only supported in the China \(Shenzhen\), China \(Beijing\), and China \(Hohhot\) regions.

3.  On the VPCs page, click **Create VPC**.

4.  On the Create VPC page, configure the VPC and VSwitch, and then click **OK**. The following table describes the parameters.

    **Note:** In this topic, Allocate is selected in the IPv6 CIDR block field. After the VPC is created, the system automatically assigns an IPv6 network CIDR block whose mask is /56 to the VPC and creates an IPv6 Gateway free of charge. You can use the IPv6 Gateway to control the flow of traffic over the IPv6 CIDR block.

    |Parameter|Description|
    |:--------|:----------|
    |**VPC**|
    |**Region**|Displays the region where you want to deploy the VPC.|
    |**Name**|Enter a name for the VPC that you want to create. The name must be 2 to 128 characters in length, and can contain digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**IPv4 CIDR Block**|Enter an IPv4 CIDR block for the VPC. We recommend that you enter 192.168.0.0/16, 172.16.0.0/12, 10.0.0.0/8, or a subset of these CIDR blocks as the primary IPv4 CIDR block of the VPC. The subnet mask must be 8 to 24 bits in length. 192.168.0.0/24 is used in this example. To use a public CIDR block as the primary CIDR block of the VPC,[submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/add?productId=1218).

**Note:** After you create a VPC, you cannot change its primary IPv4 CIDR block. However, you can add a secondary IPv4 CIDR block to the VPC. For more information, see [Add a secondary IPv4 CIDR block](/intl.en-US/VPCs and vSwitchs/Work with VPCs.md). |
    |**IPv6 CIDR Block**|Specify whether to assign an IPv6 CIDR block to the VPC. By default, no IPv6 CIDR block is allocated. If you set this parameter to Assign, the system automatically creates a free IPv6 gateway for this VPC, and assigns an IPv6 CIDR block with the subnet mask /56, such as 2xx1:db8::/56. By default, IPv6 addresses can be used to communicate within only private networks. If you want to allow an instance assigned with an IPv6 address to access the Internet or be accessed by IPv6 clients over the Internet, you must purchase an Internet bandwidth plan for the IPv6 address. For more information, see [Enable Internet connectivity for an IPv6 address](/intl.en-US/User Guide/Manage IPv6 Internet bandwidth/Enable Internet connectivity for an IPv6 address.md).

**Note:**

    -   The following regions support IPv6 CIDR blocks: China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Beijing\), China \(Hohhot\), China \(Chengdu\), China \(Hong Kong\), and Singapore \(Singapore\)..
    -   After you create a VPC, you cannot change its IPv6 CIDR block. |
    |**Description**|Enter a description for the VPC. The description must be 2 to 256 characters in length and cannot start with `http://` or `https://`. |
    |**Resource Group**|Select the resource set to which the VPC belongs.|
    |**vSwitch**|
    |**Name**|Enter a name for the vSwitch. The name must be 2 to 128 characters in length, and can contain digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**Zone**|Select a zone for the vSwitch. In the same VPC, vSwitches in different zones can communicate with each other.|
    |**Zone Resource**|Displays the cloud resources that can be created in the specified zone. The supported cloud resources vary based on the zone and the time when you create cloud resources. The instances provided in this topic are for reference only. The actual instances on the buy page shall prevail. Only ECS, ApsaraDB RDS, and SLB instances can be queried on the buy page. |
    |**IPv4 CIDR Block**|Specify an IPv4 CIDR block for the vSwitch. When you specify an IPv4 CIDR block for the vSwitch, take note of the following limits:

    -   The CIDR block of a vSwitch must be a subset of the CIDR block of the VPC to which the vSwitch belongs.

For example, if the CIDR block of a VPC is 192.168.0.0/16, the CIDR block of a vSwitch in the VPC must be a subset of 192.168.0.0/16. In this example, the CIDR block of the vSwitch can range from 192.168.0.0/17 to 192.168.0.0/29.

    -   The first IP address and last three IP addresses of a vSwitch CIDR block are reserved.

For example, if a vSwitch CIDR block is 192.168.1.0/24, the IP addresses 192.168.1.0, 192.168.1.253, 192.168.1.254, and 192.168.1.255 are reserved.

    -   If the vSwitch is required to communicate with vSwitches in other VPCs or with data centers, make sure that the CIDR block of the vSwitch does not overlap with the destination CIDR blocks.
**Note:** After you create a vSwitch, you cannot modify its CIDR block. |
    |**Number of Available Private IPs**|Displays the number of available IP addresses.|
    |**IPv6 CIDR Block**|Specify an IPv6 CIDR block for the vSwitch. By default, the subnet mask for the IPv6 CIDR block of a vSwitch is /64. You can enter a number from 0 to 255 to define the last 8 bits of the IPv6 CIDR block.

For example, if the IPv6 CIDR block of the VPC is 2xx8:4004:c0:b900::/56, you can specify 255 to define the last 8 bits of the IPv6 CIDR block. In this case, the IPv6 CIDR block of the vSwitch is 2xx8:4004:c0:b9ff::/64. ff is the hexadecimal value of 255. |
    |**Description**|Enter a description for the vSwitch. The description must be 2 to 256 characters in length and cannot start with `http://` or `https://`. |


## Step 2: Create an ECS instance

After you create a VPC and a VSwitch with an IPv6 CIDR block, you must create an ECS instance with an IPv6 address. After you create an ECS instance, you need to associate the assigned IPv6 address with the ENI of the ECS instance.

To create an ECS instance, follow these steps:

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  In the left-side navigation pane, click **VSwitches**.

3.  Select the region to which the target VSwitch belongs. In this topic, select **China \(Hohhot\)**.

4.  On the VSwitches page, find the target VSwitch, and then choose **Purchase** \> **ECS Instance** in the **Actions** column.

5.  On the Custom Launch page, configure the ECS instance, and then click **confirm to pay**.

    The networking parameters are set as follows:

    -   In the Network Billing Method area of the Networking page, select **Assign Public IP Address**, and then set the bandwidth to 1 Mpbs. Alternatively, you can clear this check box and use an EIP instead.
    -   Select **Assign IPv6 Address Free of Charge**.
6.  Go back to the Instances page, and then click the instance ID to view the assigned IPv6 address.

7.  Configure a static IPv6 address.


## \(Optional\) Step 3: Enable IPv6 Internet bandwidth for the VPC

By default, IPv6 addresses only support intranet communication. To enable the assigned IPv6 address to access the Internet or be accessed by Internet IPv6 clients, you must enable IPv6 Internet bandwidth for the VPC.

To enable IPv6 Internet bandwidth for the VPC, follow these steps:

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  In the left-side navigation pane, click **IPv6 Gateway**.

3.  Select the region to which the target IPv6 Gateway belongs. In this topic, select **China \(Hohhot\)**.

4.  On the IPv6 Gateway page, find the target IPv6 Gateway, and then click **Manage** in the **Actions** column.

5.  In the left-side navigation pane, click **IPv6 Internet Bandwidth**.

6.  On the IPv6 Internet Bandwidth page, find the target IPv6 address, and then click **Create IPv6 Internet Bandwidth** in the **Actions** column.

    ![ Create IPv6 Internet Bandwidth](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8310509951/p33776.png)

7.  Select a billing method and a peak bandwidth value, and then click **Buy Now** and complete the payment.


## Step 4: Configure security group rules

IPv4 communication and IPv6 communication are isolated from each other. If the current security group rules cannot meet your requirements, you can configure an IPv6 security group rule for the ECS instance.

For more information, see [Add security group rules](/intl.en-US/Security/Security groups/Add security group rules.md).

## Step 5: Test the network connectivity

Log on to the ECS instance and ping an IPv6 service to test whether the communication is normal.

![Test Connectivity](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2310509951/p54447.png)

