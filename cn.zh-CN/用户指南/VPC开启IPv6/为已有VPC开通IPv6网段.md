# 为已有VPC开通IPv6网段

您可以为已创建的VPC开通IPv6网段。开通IPv6网段后，系统将为VPC自动创建一个免费版的IPv6网关。您可以使用IPv6网关管理IPv6公网带宽和IPv6公网仅主动出规则。

您已经申请了IPv4/IPv6双栈VPC的公测资格。如需使用，请[提交申请](https://page.aliyun.com/form/act608662110/index.htm?spm=5176.11182174.0.0.5a1c4882UFiAde)。

**说明：** 目前，仅以下地域支持创建IPv4/IPv6双栈VPC：华北2（北京）、华北3（张家口）、华北5（呼和浩特）、华东1（杭州）、华东2（上海）、华南1（深圳）、西南1（成都）、中国（香港）、新加坡、美国（弗吉尼亚）。

1.  登录[专有网络管理控制台](https://vpcnext.console.aliyun.com/vpc)。

2.  在顶部菜单栏处，选择专有网络的地域。

3.  在**专有网络**页面，找到目标专有网络，单击**IPv6网段**列下的**开通IPv6**。

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/8816328951/p33772.png)

4.  在**开通IPv6**对话框中，勾选**自动开启VPC内所有交换机IPv6功能**，然后单击**确定**。

    如果您不勾选**自动开启VPC内所有交换机IPv6功能**，您需要为每个交换机单独开通IPv6网段。详细信息，请参见[为已有交换机开通IPv6网段](/cn.zh-CN/用户指南/交换机开启IPv6/为已有交换机开通IPv6网段.md)。


