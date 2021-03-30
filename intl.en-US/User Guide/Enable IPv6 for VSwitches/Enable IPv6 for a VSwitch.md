# Enable IPv6 for a VSwitch

This topic describes how to allocate an IPv6 CIDR block to a VSwitch.

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com/vpc).

2.  In the left-side navigation pane, click **VSwitches**.

3.  Select the region where your VSwitch resides.

    **Note:** The following regions support IPv6 gateways: China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Beijing\), China \(Hohhot\), China \(Chengdu\), China \(Hong Kong\), and Singapore \(Singapore\)..

4.  On the **VSwitches** page, find the target VSwitch, and click **Enable IPv6 CIDR Block** in the **IPv6 CIDR Block** column.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6310509951/p33773.png)

5.  In the **Enable IPv6 CIDR Block** dialog box, click **OK**.

    **Note:** This operation is required only when IPv6 is not enabled for the VPC to which the VSwitch belongs.

6.  Specify an IPv6 CIDR block and click **OK**.

    The default subnet mask for the IPv6 CIDR block of a VSwitch is /64. You can enter a decimal number ranging from 0 to 255 to define the last 8 bits of the IPv6 CIDR block.

    For example, if the IPv6 CIDR block of the VPC that contains the VSwitch is 2xx1:db8::/64, you can enter 255 \(FF in hexadecimal notation\) in this field to define the IPv6 CIDR block of the VSwitch as 2xx1:db8::ff/64.


