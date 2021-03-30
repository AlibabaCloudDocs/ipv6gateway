# Overdue payments

After an IPv6 gateway or IPv6 bandwidth plan has overdue payments, we recommend that you complete the payments to prevent service interruption.

|Type|Overdue payments|Top up your account balance|
|----|----------------|---------------------------|
|IPv6 gateway instance fees|If an IPv6 gateway of Enterprise Edition or Enhanced Enterprise Edition has overdue payments \(bills are generated but payments are not completed\), the Alibaba Cloud account to which the IPv6 gateway belongs is notified by SMS and email. -   If the fees generated after overdue payments do not exceed the overdraft threshold, the IPv6 gateway can work as expected.

**Note:**

-   If the fees generated after overdue payments exceed the overdraft threshold, the IPv6 gateway is suspended. In this case, the maximum forwarding capabilities and maximum pay-by-data-transfer bandwidth of the IPv6 gateway are downgraded to Free Edition. In addition, outbound rules that are configured for the IPv6 gateway become locked and invalid.
-   If the IPv6 gateway remains suspended for seven days, it is released. You will receive SMS or email notifications one day before the IPv6 gateway is released. After it is released, relevant configurations and data are deleted and cannot be restored.

|IPv6 gateways support the pay-as-you-go billing method. You can top up your Alibaba Cloud account after an overdue payment occurs. -   If you top up your Alibaba Cloud account within the service suspension protection period, your service is not suspended.
-   If you top up your Alibaba Cloud account within seven days after the IPv6 gateway becomes suspended, the system automatically completes the unpaid bills. After payments are completed, the IPv6 gateway can work as expected. |
|IPv6 Internet bandwidth fees|If the IPv6 Internet bandwidth plan of an IPv6 address has overdue payments \(bills are generated but payments are not completed\), the Alibaba Cloud account to which the IPv6 Internet bandwidth plan belongs is notified by SMS and email. -   If the fees generated after overdue payments do not exceed the overdraft threshold, the IPv6 Internet bandwidth can work as expected.

**Note:**

-   If the fees generated after overdue payments exceed the overdraft threshold, the IPv6 Internet bandwidth is throttled to 1 Kbit/s but the IPv6 Internet bandwidth plan is not released.
-   If the IPv6 Internet bandwidth remains throttled for seven days, the IPv6 Internet bandwidth plan is released. The IPv6 address is not released. However, its communication type is changed to private network communication.

|IPv6 Internet bandwidth plans support the pay-as-you-go billing method. You can top up your Alibaba Cloud account after an overdue payment occurs. -   If you top up your Alibaba Cloud account within the service suspension protection period, your service is not suspended.
-   If you top up your Alibaba Cloud account within seven days after the IPv6 Internet bandwidth becomes throttled, the system automatically settles the unpaid bills. After payments are completed, the IPv6 Internet bandwidth can work as expected. |

