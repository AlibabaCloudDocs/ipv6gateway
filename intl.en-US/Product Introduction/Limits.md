# Limits

This topic describes the limits of IPv6 Gateway and includes limits related to egress-only rules, IPv6 bandwidth usage, and Internet speed.

## Limits on IPv6 Gateways

-   Only one IPv6 Gateway can be configured for a VPC.
-   You cannot delete the IPv6 CIDR block of a VPC after the IPv6 CIDR block is enabled.
-   You cannot delete the IPv6 CIDR block of a VSwitch after the IPv6 CIDR block is enabled.
-   Before you delete an IPv6 Gateway, you must first delete the IPv6 Internet bandwidths and egress-only rules configured in the IPv6 Gateway.
-   Before you delete a VPC, you must first delete the IPv6 Gateway created for the VPC.
-   Currently, only custom routes of which the destination CIDR block is ::/0 and the next hops are IPv6 Gateway instances are supported.

## Limits on egress-only rules

Before you create an egress-only rule, make sure that you have enabled the Internet bandwidth function for the corresponding IPv6 address.

Different IPv6 Gateway specifications have different quotas for egress-only rules, which are described in the following table.

|IPv6 Gateway specification|Egress-only rule quota|
|:-------------------------|:---------------------|
|Free Version|0|
|Medium|50|
|Large|200|

## Limits on IPv6 Internet bandwidth

Different IPv6 Gateway specifications support different peak Internet bandwidth values, which are described in the following table.

|IPv6 Gateway specification|Peak Internet bandwidth|
|:-------------------------|:----------------------|
|Free Version|2 Gbit/s|
|Medium|2 Gbit/s|
|Large|2 Gbit/s|

|IPv6 Gateway specification|Peak Internet bandwidth|
|:-------------------------|:----------------------|
|Free version|200 Mbit/s|
|Medium|500 Mbit/s|
|Large|1 Gbit/s|

## Limits on IPv6 Internet speed

The IPv6 Internet speed can be limited through IPv6 Internet bandwidth and IPv6 Gateway.

-   If the total IPv6 Internet bandwidth under an IPv6 Gateway is smaller than the maximum traffic forwarding capacity of the IPv6 Gateway, the speed of the IPv6 traffic sent from the cloud resources in the corresponding VPC is limited based on the IPv6 peak Internet bandwidth value you set.
-   If the total IPv6 Internet bandwidth under an IPv6 Gateway is greater than the maximum traffic forwarding capacity of the IPv6 Gateway, the total IPv6 Internet bandwidth capacity is limited based on the maximum traffic forwarding capacity of the IPv6 Gateway.

Different IPv6 Gateway specifications have different traffic forwarding capacities, which are described in the following table.

|IPv6 Gateway specification|Maximum forwarding capacity|
|:-------------------------|:--------------------------|
|Free Version|10 Gbit/s|
|Medium|20 Gbit/s|
|Large|50 Gbit/s|

