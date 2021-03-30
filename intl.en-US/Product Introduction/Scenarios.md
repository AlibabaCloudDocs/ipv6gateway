# Scenarios

This topic describes three different scenarios where IPv6 Gateway can be established to provide IPv6 addressing services.

## Scenario 1: Provide IPv6 support with an isolated IPv6 cloud environment

You can enable IPv6 for an existing VPC, which allows the VPC to support both IPv4 and IPv6 protocol stacks. You can also allocate IPv6 addresses to the ECS instances in the VPC. In this way, the ECS instances have both IPv4 and IPv6 addresses. Note that IPv6 addresses of ECS instances can only communicate with other IPv6 addresses over the intranet in the VPC by default.

IPv4 and IPv6 dual-stack ECS clusters can connect to each other through IPv4 intranets or IPv6 networks. However, the ECS instances cannot use IPv6 addresses to access the Internet or be accessed by IPv6 clients over the Internet.

![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6010509951/p33733.png)

## Scenario 2: IPv6-based communication between cloud resources in your VPC and the Internet

After you purchase an Internet bandwidth for your IPv6 addresses, the IPv6 addresses can access the Internet. Specifically, the IPv6 traffic between the cloud resources in the VPC and the IPv6 network passes through IPv6 Gateway, which functions as the transfer hub of IPv6 Internet traffic for dual-stack VPCs.

The IPv4 addresses of ECS clusters in the VPC communicate with IPv4 clients over the Internet through SLB and NAT Gateway, which serve as the inlet and outlet of IPv4 Internet traffic for dual-stack VPCs.

![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/6010509951/p33735.png)

## Scenario 3: Egress-only IPv6 traffic over the Internet

If you need your services to actively access IPv6 clients but do not want the IPv6 addresses of ECS instances to be accessed by external IPv6 clients, you can set an egress-only rule. In this way, the ECS instances you specified can access IPv6 networks by using IPv6 addresses. However, external IPv6 clients cannot access the specified ECS instances and access requests initiated by external IPv6 clients are discarded by IPv6 Gateway.

![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7010509951/p33736.tif)

