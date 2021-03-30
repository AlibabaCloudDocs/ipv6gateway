# Pricing

When you use an IPv6 gateway, you are charged for the IPv6 gateway instance and Internet bandwidth.

## IPv6 gateway instance fees

IPv6 gateway instances support the pay-as-you-go billing method. Fees are calculated on a daily basis.

Total fee of a pay-as-you-go IPv6 gateway instance = Unit price \(CNY/day\) × Duration.

-   The duration refers to the time when the instance is created to the time when the instance is released. The instance is billed once per day. Bills are generated on a daily basis.

-   If you change the specification of an IPv6 gateway within a billing cycle, the instance fee is calculated based on the highest specification used during the cycle.

-   Various IPv6 gateway specifications are provided to meet different requirements. Fees vary based on different specifications, as shown in the following table.

**Note:** If the regions and corresponding prices are different from those displayed in the console, use the information in the console.

    |Region|Unit price of Free Edition \(CNY/day\)|Unit price of Enterprise Edition \(CNY/day\)|Unit price of Enterprise Enhanced Edition \(CNY/day\)|
    |------|--------------------------------------|--------------------------------------------|-----------------------------------------------------|
    |China \(Hohhot\), China \(Shenzhen\), China \(Beijing\), China \(Shanghai\), and China \(Hong Kong\) regions|0|12|23|


## IPv6 Internet bandwidth fee

IPv6 gateway instances support the pay-as-you-go billing method and can be billed by traffic or by bandwidth. Before you select a billing method, you need to know the peak bandwidth and the average bandwidth usage of your service.

In terms of the average bandwidth usage:

-   For business with a low average bandwidth usage \(lower than 20%\), we recommend that you use the pay-by-data-transfer billing method.

-   For business with a high average bandwidth usage \(higher than 35%\), we recommend that you use the pay-by-bandwidth billing method.

-   If the average bandwidth usage of your service is at a medium level, we recommend that you select a billing method based on previous running data of your service.


## IPv6 Internet bandwidth fee \(pay-by-bandwidth\)

Total fee of a bandwidth-based IPv6 gateway instance = Unit price \(CNY/day\) × Peak bandwidth.

-   The instance is billed once per day. Bills are generated on a daily basis. If you use an instance for less than one day within a billing cycle, the usage duration is calculated as one day.

-   You can modify the peak bandwidth at any time. If you change the peak bandwidth of an Internet bandwidth within a billing cycle \(one day\), the Internet bandwidth fee is calculated based on the maximum peak bandwidth that you set within the statistical period.

-   Bandwidth fees are calculated based on a tiered pricing strategy with 5 Mbit/s as the boundary.

**Note:** If the regions and corresponding prices are different from those displayed in the console, use the information in the console.

|Region|Bandwidth fee \(CNY/day/1-5 Mbit/s\)|Bandwidth fee \(CNY/day/higher than 5 Mbit/s\)|
|------|------------------------------------|----------------------------------------------|
|China \(Hohhot\), China \(Shenzhen\), China \(Beijing\), China \(Shanghai\), and China \(Hong Kong\) regions|0.96|3.36|


## IPv6 Internet bandwidth fee \(pay-by-data-transfer\)

Total fee of a pay-by-data-transfer IPv6 gateway instance = Unit price × Total traffic.

-   The billing cycle or accounting cycle of the instance fee is calculated by hour. If you use an instance for less than one hour within a billing cycle, the usage duration is calculated as one hour.

-   Total traffic refers to the accumulated outbound traffic IPv6 addresses. Inbound traffic is not billed. Outbound traffic refers to the traffic sent from Alibaba cloud data centers to the Internet.

-   The unit price does not change with the upper limit of the bandwidth. However, we recommend that you set the bandwidth based on your actual requirements. This allows you to avoid excessive data usage fees due to malicious requests or unexpected errors.

-   The following table lists the unit price of the traffic incurred in different regions.

**Note:** If the regions and corresponding prices are different from those displayed in the console, use the information in the console.

|Region|Traffic unit price \(CNY/GB\)|
|------|-----------------------------|
|China \(Hohhot\), China \(Shenzhen\), China \(Beijing\), China \(Shanghai\), and China \(Hong Kong\) regions|0.8|


