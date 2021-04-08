# Enable an IPv6 CIDR block for a VPC network

This topic describes how to enable an IPv6 CIDR block for a Virtual Private Cloud \(VPC\) network. After the IPv6 CIDR block is enabled, the system automatically creates an IPv6 gateway free of charge for the VPC network. You can use the IPv6 Gateway to manage the IPv6 Internet bandwidth and set egress-only rules.

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc).

2.  Select the region where your VPC network is deployed.

    **Note:** The following regions support IPv6 gateways: China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Chengdu\), China \(Hong Kong\), and Singapore \(Singapore\)..

3.  On the **VPCs** page, find the target VPC network and click **Enable IPv6 CIDR Block** in the **IPv6 CIDR Block** column.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4310509951/p33772.png)

4.  In the **Enable IPv6 CIDR Block** dialog box, select **Enable IPv6 CIDR Block of all VSwitches in VPC**, and then click **OK**.

    If you do not select **Enable IPv6 CIDR Block of all VSwitches in VPC**, you must enable IPv6 CIDR Block for each VSwitch. For more information, see [Enable IPv6 for a VSwitch](/intl.en-US/User Guide/Enable IPv6 for VSwitches/Enable IPv6 for a VSwitch.md).


