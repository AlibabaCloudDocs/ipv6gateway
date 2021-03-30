# Manage IPv6 routes in the route table

You can control the IPv6 traffic in VPCs by managing IPv6 routes in the route table. IPv6 routes include system routes and custom routes.

After you create an IPv6 Gateway or enable IPv6 CIDR block for a VPC, the system automatically adds the following two route entries to the system route table of the VPC:

-   A custom route entry whose destination CIDR block is ::/0, and the next hop is the ID of the IPv6 Gateway. It is used for communication between the cloud resources in the VPC and the Internet.

-   A system route entry whose destination CIDR block is the IPv6 CIDR block of the VSwitch. It is used for communication between the cloud resources within the VSwitch.


**Note:** If you create a custom route table and associate a VSwitch that has an enabled IPv6 CIDR block to the route table, you need to manually add a route entry whose destination CIDR block is ::/0, and next hop is the ID of the IPv6 Gateway.

