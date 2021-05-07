# Create an IPv6 VPC network

This topic describes how to create a Virtual Private Cloud \(VPC\) network that supports IPv6 CIDR blocks. After you create a VPC network with an IPv6 CIDR block, you can create an ECS instance that is assigned an IPv6 address in the VPC network and then access the ECS instance from an IPv6 client.

## Step 1: Create a VPC network and VSwitches

Before you deploy cloud resources in a VPC network, you must set up network connections. For more information, see [Plan and design a VPC](/intl.en-US/Quick Start/Plan and design a VPC.md).

To create a VPC network and VSwitches, follow these steps:

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  Select the region where you want to create a VPC network.

    The VPC network and the cloud resources that you want to deploy must be in the same region. In this topic, **China \(Hohhot\)** is selected.

    **Note:** The following regions support IPv6 gateways: China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\).

3.  On the VPCs page, click **Create VPC**.

4.  In the Create VPC dialog box, set the following parameters of the VPC network and VSwitches, and click **OK**.

    **Note:** Select Allocate in the IPv6 CIDR Block field in this topic. After you create the VPC network, the system automatically assigns an IPv6 CIDR block whose mask length is 56 to the VPC network and creates an IPv6 gateway free of charge. You can use the IPv6 gateway to control the network traffic forwarded by using IPv6 addresses.

    |Parameter|Description|
    |:--------|:----------|
    |**VPC**|
    |**Region**|Displays the region where you want to deploy the VPC.|
    |**Name**|Enter a name for the VPC that you want to create. The name must be 2 to 128 characters in length, and can contain letters, digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**IPv4 CIDR Block**|Enter an IPv4 CIDR block for the VPC. We recommend that you enter 192.168.0.0/16, 172.16.0.0/12, 10.0.0.0/8, or a subset of these CIDR blocks as the primary IPv4 CIDR block of the VPC. The subnet mask must be 8 to 24 bits in length. 192.168.0.0/24 is used in this example. To use a public CIDR block as the primary CIDR block of the VPC,[submit a ticket](https://workorder-intl.console.aliyun.com/console.htm#/ticket/add?productId=1218).

**Note:** After you create a VPC, you cannot change its primary IPv4 CIDR block. However, you can add a secondary IPv4 CIDR block to the VPC. For more information, see [Add a secondary IPv4 CIDR block](/intl.en-US/VPCs and vSwitchs/Work with VPCs.md). |
    |**IPv6 CIDR Block**|Specify whether to assign an IPv6 CIDR block to the VPC. By default, no IPv6 CIDR block is allocated. If you set this parameter to Assign, the system automatically creates a free IPv6 gateway for this VPC, and assigns an IPv6 CIDR block with the subnet mask /56, such as 2xx1:db8::/56. By default, IPv6 addresses can be used to communicate within only private networks. If you want to allow an instance assigned with an IPv6 address to access the Internet or be accessed by IPv6 clients over the Internet, you must purchase an Internet bandwidth plan for the IPv6 address. For more information, see [Enable Internet connectivity for an IPv6 address](/intl.en-US/User Guide/Manage IPv6 Internet bandwidth/Enable Internet connectivity for an IPv6 address.md).

**Note:**

    -   The following regions support IPv6 CIDR blocks: China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\).
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


## Step 2: Create and connect to an ECS instance

After you create an IPv6 VPC network and VSwitches, you can create an ECS instance that is assigned an IPv6 address. After you create an ECS instance, you can associate the assigned IPv6 address with the Elastic Network Interface \(ENI\) of the ECS instance.

To create and connect to an ECS instance, follow these steps:

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  In the left-side navigation pane, click **VSwitches**.

3.  On the top of the page, select the region where the VSwitch is deployed. In this topic, **China \(Hohhot\)** is selected.

4.  On the VSwitches page, find the VSwitch that you want to manage, and choose **Create** \> **ECS Instance** in the **Actions** column for the VSwitch.

5.  On the Custom Launch page, set the parameters of the ECS instance, and click **Create Order**.

    Set the networking parameters for the ECS instance based on the following requirements in this topic:

    -   To log on to the ECS instance, you must configure ENI of the ECS instance. Select **Assign Public IP Address** and set the bandwidth to 1Mbit/s. You can use an Elastic IP address instead of assigning a public IP address.
    -   Select **Assign IPv6 Address Free of Charge**.
6.  Return to the Instances page, and click the instance ID to view the assigned IPv6 address.

7.  Configure a static IPv6 address.


## Step 3: Purchase an IPv6 Internet bandwidth plan

By default, IPv6 addresses can be used for communication only over internal networks. If you want to enable the VPC network to access the Internet or use an IPv6 client to access the VPC network over the Internet, you must purchase IPv6 Internet bandwidth plan.

To purchase an IPv6 Internet bandwidth plan, follow these steps:

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  In the left-side navigation pane, click **IPv6 Gateway**.

3.  On the top of the page, select the region of the IPv6 gateway. In this topic, **China \(Hohhot\) is selected**.

4.  On the IPv6 Gateway page, find the IPv6 gateway that you want to manage, and click **Manage** in the **Actions** column for the IPv6 gateway.

5.  In the left-side navigation pane, click **IPv6 Internet Bandwidth**.

6.  On the IPv6 Internet Bandwidth page, find the IPv6 address that you want to manage, and click **Create IPv6 Internet Bandwidth** in the **Actions** column for the IPv6 address.

    ![Purchase an IPv6 Internet bandwidth plan](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8310509951/p33776.png)

7.  Set the billing method and peak bandwidth, and click **Buy Now** to complete the payment.


## Step 4: Configure the security group rules

ECS instances that are assigned IPv4 addresses and ECS instances that are assigned IPv6 addresses cannot communicate with each other. If the current security group rules cannot serve your IPv6 services, you must configure IPv6 security group rules for the ECS instance.

For more information, see [Add security group rules](/intl.en-US/Security/Security groups/Add security group rules.md).

## Step 5: Test the network connectivity

Log on to the ECS instance and run the Ping command to test whether the communication is normal.

![Test the network connectivity](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2310509951/p54447.png)

