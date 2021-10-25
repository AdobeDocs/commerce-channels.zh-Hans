---
title: 日志和存储报表
description: 使用日志和存储报表可查看Adobe Commerce或Magento Open Source存储以及Amazon Marketplace列表中发生的情况。
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 日志和存储报表

Amazon销售渠道扩展包含一些有价值的日志和存储报表，使您能够查看影响Amazon列表和订单的更改。 您可以使用这些报表来查看您的商店中发生的情况，并了解各种列表状态。

没有可用于日志或存储报表的操作，因为它们是仅供审阅的功能。

可以从 [存储仪表板](./amazon-store-dashboard.md).

- 的 [列出更改日志](./listing-changes-log.md) 显示在您的Amazon卖家帐户中发生的更改，以反映您的Amazon销售渠道设置。

- 的 [通信错误日志](./communication-errors-log.md) 显示与Amazon之间报告的任何通信错误。

可从 [存储仪表板](./amazon-store-dashboard.md).

- 的 [竞争价格分析](./competitive-price-analysis.md) 报表显示您的Amazon _地价_ （上市价加运价）与 [Buy Box](./buy-box-competitor-pricing.md) 价格和 [最低竞争对手](./lowest-competitor-pricing.md) 价格。

- 的 [列表改进](./listing-improvements.md) 报表显示Amazon为选定商店提供的所有建议列表改进。

>[!TIP]
>
>您还可以在需要进行故障诊断时，检查日志文件以获取其他信息。 请参阅 [销售渠道管理设置](./sales-channel-settings.md). Amazon销售渠道同步日志记录已写入 `{Commerce Root}/var/log/channel_amazon.log` 文件，并可在 [开发人员模式](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}。
