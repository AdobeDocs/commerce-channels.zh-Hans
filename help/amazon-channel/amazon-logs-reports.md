---
title: Amazon列表的日志和存储报告
description: 使用日志和商店报表可查看Adobe Commerce或Magento Open Source商店中的动态以及Amazon Marketplace列表。
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Amazon列表的日志和存储报告

Amazon sales channel扩展包括一些有价值的日志和商店报告，利用这些报告，您可以查看影响Amazon清单和订单的更改。 您可以使用这些报表来查看您商店中发生的事件并了解各种列表状态。

日志或存储报告没有可用的操作，因为它们是仅审核功能。

以下日志可从 [存储仪表板](./amazon-store-dashboard.md).

- 此 [列出更改日志](./listing-changes-log.md) 显示在您的Amazon卖方帐户中发生的更改，以反映您的Amazon销售渠道设置。

- 此 [通信错误日志](./communication-errors-log.md) 显示与Amazon之间报告的任何通信错误。

以下特定于存储的报告可从 [存储仪表板](./amazon-store-dashboard.md).

- 此 [有竞争力的价格分析](./competitive-price-analysis.md) 报表显示您的Amazon _到岸价格_ （上市价格加运费）与关连公司有关 [Buy Box](./buy-box-competitor-pricing.md) 价格和 [最低竞争对手](./lowest-competitor-pricing.md) 价格。

- 此 [列表改进](./listing-improvements.md) 报表显示了Amazon为选定商店提供的所有列表改进建议。

>[!TIP]
>
>在需要进行故障排除时，您还可以查看日志文件以了解其他信息。 参见 [sales channel管理设置](./sales-channel-settings.md). Amazon sales channel synchronization logging将写入 `{Commerce Root}/var/log/channel_amazon.log` 文件并可在中查看 [开发人员模式](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes).
