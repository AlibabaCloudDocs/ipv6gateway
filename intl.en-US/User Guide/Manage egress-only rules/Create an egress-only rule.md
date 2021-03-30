# Create an egress-only rule

This topic describes how to create an egress-only rule. If the cloud resources in your VPC need to access the Internet by using IPv6 addresses, but you do not want these resources to be accessed by external IPv6 clients, you can create an egress-only rule.

Make sure that you have enabled IPv6 Internet bandwidth for the IPv6 address. For more information, see [Enable Internet connectivity for an IPv6 address](/intl.en-US/User Guide/Manage IPv6 Internet bandwidth/Enable Internet connectivity for an IPv6 address.md).

The Free Version specification does not support egress-only rules. The medium specification supports up to 50 egress-only rules. The large specification supports up to 200 egress-only rules.

1.  Log on to the [VPC console](https://vpcnext.console.aliyun.com).

2.  In the left-side navigation pane, click **IPv6 Gateway**.

3.  Select the region of the target IPv6 Gateway.

4.  On the IPv6 Gateway page, find the target IPv6 Gateway, and click **Manage** in the **Actions** column.

5.  In the left-side navigation pane, click **Egress-only Rule**.

6.  On the Egress-only Rule page, click **Create Egress-only Rule**.

7.  On the Create Egress-only Rule page, select the ECS instance that needs to access the Internet by using IPv6 addresses, and click **OK**.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2771958951/p33777.png)


