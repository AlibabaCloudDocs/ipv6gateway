# 为已有VPC开通IPv6网段 {#task_nhm_rf5_zfb .task}

您可以为已创建的VPC开通IPv6网段。开通IPv6网段后，系统将为VPC自动创建一个免费版的IPv6网关。您可以使用IPv6网关管理IPv6公网带宽和IPv6公网仅主动出规则。

1.  登录[专有网络管理控制台](https://vpcnext.console.aliyun.com)。
2.  选择专有网络的地域。 

    **说明：** 目前，仅华北5（呼和浩特）、华南1（深圳）、华北2（北京）地域支持开通IPv6网关。

3.  在专有网络页面，找到目标专有网络，单击**IPv6网段**列下的**开通IPv6**。 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/73825/156807977633772_zh-CN.png)

4.  在弹出的对话框中，勾选**自动开启VPC内所有交换机IPv6功能**，然后单击**确定**。 如果您不勾选**自动开启VPC内所有交换机IPv6功能**，您需要为每个交换机单独开通IPv6网段。详细信息，请参见[为已有交换机开启IPv6网段](cn.zh-CN/用户指南/交换机开启IPv6/为已有交换机开通IPv6网段.md#)。

