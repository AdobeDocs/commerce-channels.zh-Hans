---
title: '[!DNL Channel Manager]发行说明'
description: Adobe Commerce中 [!DNL Channel Manager] 的最新发行信息。
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# [!DNL Channel Manager]发行说明

这些发行说明描述了[!DNL Channel Manager]的初始版本，其中包括：

![新](../assets/new.svg)新功能
![已修复问题](../assets/fix.svg)修复和改进
![已知问题](../assets/bug.svg)已知问题

请参阅[即将发布的版本](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html)，了解版本计划和支持。

请参阅[产品可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html)，了解哪些Adobe Commerce版本支持此扩展。

## v2.1.0

*2023年10月3日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)渠道管理器现在与[Adobe Commerce版本2.4.7 beta](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html)版本兼容。

## v2.0.0

*2023年3月20日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)<!--CHAN-5893-->渠道管理器现在与Adobe Commerce版本2.4.6兼容。

## v1.1.0

*2022年11月23日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新建](../assets/new.svg)<!--CHAN-5204--> **退货和退款** — 您现在可以处理通过Adobe Commerce和Magento Open SourceChannel Manger商店发运的订单的Walmart Marketplace退货和退款流程。 有关退货和退款的信息和更新在Walmart和Adobe Commerce之间同步，以便当前数据在[!DNL Commerce]店面和[!DNL Walmart Marketplace]中均可用。 请参阅[退货和退款订单](return-refund-orders.md)。

![已修复](../assets/fix.svg)<!--CHAN-5661-->修复了使用`bin/magento saas:resync --feed orders`命令重新同步渠道管理器订单数据时发生的`Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist`错误。 通过更新销售数据导出程序模块的渠道管理器包依赖项（已从`magento/module-sales-data-exporter`重命名为`magento/module-sales-orders-data-exporter`），解决了该错误。

## v1.0.0

*2022年1月14日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)渠道管理器的初始版本已正式发布

