# Pricing

When you use an IPv6 gateway, you are charged for using the IPv6 gateway and Internet bandwidth resources.

## IPv6 gateway instance fees

IPv6 gateways support the pay-as-you-go billing method. Fees are calculated on a daily basis.

The instance fee of a pay-as-you-go IPv6 gateway = Unit price \(USD/day\) × Duration.

-   The duration refers to the time when the instance is created to the time when the instance is released. The instance is billed once per day. Bills are generated on a daily basis.

-   If you change the specification of an IPv6 gateway within a billing cycle, the instance fee is calculated based on the highest specification used during the cycle.

-   Various IPv6 gateway specifications are provided to meet different requirements. Fees vary based on different specifications, as shown in the following table.

**Note:** If the regions and corresponding prices are different from those displayed in the console, the information in the console shall prevail.

    |Region|Unit price of Free Edition \(USD/day\)|Unit price of Enterprise Edition \(USD/day\)|Unit price of Enterprise Enhanced Edition \(USD/day\)|
    |------|--------------------------------------|--------------------------------------------|-----------------------------------------------------|
    |China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\)|0|1.8

|3.5 |


## IPv6 Internet bandwidth fee

IPv6 gateways support the pay-as-you-go billing method and can be billed by data transfer or by bandwidth. Before you select a metering method, we recommend that you understand the required maximum bandwidth and the average bandwidth usage of your service.

In terms of the average bandwidth usage:

-   For business with a low average bandwidth usage \(lower than 20%\), we recommend that you use the pay-by-data-transfer metering method.

-   For business with a high average bandwidth usage \(higher than 35%\), we recommend that you use the pay-by-bandwidth metering method.

-   If the average bandwidth usage of your service is at a medium level, we recommend that you select a metering method based on previous service data.


## IPv6 Internet bandwidth fee \(pay-by-bandwidth\)

-   If you select this metering method, the billing cycle is one day and bills are generated on a daily basis. If you use an IPv6 gateway for less than one day within a billing cycle, the usage duration is rounded up to one day.

-   You can modify the maximum bandwidth value as needed. If you modify the maximum bandwidth value within a billing cycle \(one day\), the Internet bandwidth fee is charged based on the maximum bandwidth value that you set within the billing cycle.

-   Bandwidth fees are charged based on a tiered pricing model with 5 Mbit/s as the boundary.

**Note:** If the regions and corresponding prices are different from those displayed in the console, the information in the console shall prevail.

|Region|Unit price for 1 to 5 Mbit/s bandwidth \(USD/day\)|Unit price for over 5 Mbit/s bandwidth \(USD/day\)|
|------|--------------------------------------------------|--------------------------------------------------|
|China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\)|-   1 Mbit/s: 0.14
-   2 Mbit/s: 0.28
-   3 Mbit/s: 0.43
-   4 Mbit/s: 0.57
-   5 Mbit/s: 0.71
|0.71 + \(N - 5\) × 0.5

**Note:** N represents the maximum bandwidth value. |


## IPv6 Internet bandwidth fee \(pay-by-data-transfer\)

The fee of a pay-by-data-transfer IPv6 gateway = Unit price × Data transfer.

-   If you select this metering method, the billing cycle is 1 hour and bills are generated on an hourly basis. If you use an IPv6 gateway for less than 1 hour within a billing cycle, the usage duration is rounded up to 1 hour.

-   Data transfer refers to the accumulated outbound traffic of IPv6 addresses. Inbound traffic is not billed. Outbound traffic refers to the data that is transmitted from Alibaba Cloud to the Internet.

-   If you modify the maximum bandwidth value, the unit price does not change. However, we recommend that you set the bandwidth value based on your actual requirements. This allows you to avoid excessive data usage fees due to malicious requests or unexpected errors.

-   The following table lists the unit price of data transfer in different regions.

**Note:** If the regions and corresponding prices are different from those displayed in the console, the information in the console shall prevail.

|Region|Data transfer unit price \(USD/GB\)|
|------|-----------------------------------|
|China \(Beijing\), China \(Zhangjiakou\), China \(Hohhot\), China \(Hangzhou\), China \(Shanghai\), China \(Shenzhen\), China \(Chengdu\), China \(Hong Kong\), Singapore \(Singapore\), and US \(Virginia\)|0.123 |


