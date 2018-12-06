# 为已有VPC开启IPv6网段 {#task_nhm_rf5_zfb .task}

您可以为已创建的VPC配置IPv6网段。开通IPv6网段后，系统将为VPC自动创建一个免费版的IPv6网关。您可以使用IPv6网关管理IPv6公网带宽、创建IPv6公网仅主动出规则。

1.  登录[专有网络管理控制台](https://vpcnext.console.aliyun.com)。 
2.  选择专有网络的地域，然后单击**创建专有网络**。 

    **说明：** 目前仅华北5（呼和浩特）地域支持开通IPv6网关。

3.  在专有网络列表页面，找到目标专有网络，然后单击**开通IPv6**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/73825/154406714933772_zh-CN.png)

4.  在弹出的对话框中，选择是否为VPC内所有的交换机开启IPv6网段，然后单击**确定**。 如果您选择不为VPC内的交换机开通IPv6网段，您需要为每个交换机单独开通。

