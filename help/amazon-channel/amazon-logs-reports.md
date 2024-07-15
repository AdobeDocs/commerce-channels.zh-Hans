---
title: Amazon列表的日志和商店报表
description: 使用日志和商店报表可以查看您的Adobe Commerce或Magento Open Source商店中发生的事件以及Amazon Marketplace列表。
feature: Sales Channels, Logs
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Amazon列表的日志和商店报表

Amazon sales channel扩展包括一些有价值的日志和商店报表，利用这些报表，您可以查看影响Amazon列表和订单的更改。 您可以使用这些报表来查看您商店中发生的事件并了解各种列表状态。

日志或存储报告没有可用的操作，因为它们是仅审核功能。

可以从[存储仪表板](./amazon-store-dashboard.md)访问以下日志。

- [列表更改日志](./listing-changes-log.md)显示您的Amazon卖方帐户中发生的更改，以反映您的Amazon销售渠道设置。

- [通信错误日志](./communication-errors-log.md)显示报告的任何与Amazon的通信错误。

可以从[存储仪表板](./amazon-store-dashboard.md)访问以下特定于存储的报告。

- [竞争性价格分析](./competitive-price-analysis.md)报表显示您的Amazon _到岸价格_（上市价格加上运费）与[Buy Box](./buy-box-competitor-pricing.md)价格和[最低竞争对手](./lowest-competitor-pricing.md)价格的关系。

- [列表改进](./listing-improvements.md)报告显示了Amazon为所选存储提供的所有列表改进建议。

>[!TIP]
>
>在需要排除故障时，您还可以查看日志文件以获取其他信息。 查看[销售渠道管理员设置](./sales-channel-settings.md)。 Amazon sales channel同步日志记录已写入`{Commerce Root}/var/log/channel_amazon.log`文件，可以在[开发人员模式](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes)中查看。
