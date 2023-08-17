---
title: '[!DNL Channel Manager] 发行说明'
description: 的最新发行信息 [!DNL Channel Manager] 来自Adobe Commerce的。
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# [!DNL Channel Manager] 发行说明

以下发行说明介绍了的初始版本 [!DNL Channel Manager] 并包括：

![新建](../assets/new.svg) 新增功能
![修复的问题](../assets/fix.svg) 修复和改进功能
![已知问题](../assets/bug.svg) 已知问题


## v2.0.0

*2023年3月20日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg)<!--CHAN-5893--> 渠道管理器现在与Adobe Commerce版本2.4.6兼容。

## v1.1.0

*2022年11月23日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg)<!--CHAN-5204--> **退货和退款** — 您现在可以处理通过Adobe Commerce和Magento Open SourceChannel Manger商店发运的订单的Walmart Marketplace退货和退款流程。 有关退货和退款的信息和更新会在沃尔玛和Adobe Commerce之间同步，以便当前数据可以在沃尔玛和中获取。 [!DNL Commerce] 店面和 [!DNL Walmart Marketplace]. 请参阅 [退货和退款单](return-refund-orders.md).

![固定](../assets/fix.svg)<!--CHAN-5661--> 修复了 `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` 使用重新同步渠道管理器订单数据时出错 `bin/magento saas:resync --feed orders` 命令。 通过更新销售数据导出器模块的渠道管理器包依赖项（已从中重命名），解决了该错误。 `magento/module-sales-data-exporter` 到 `magento/module-sales-orders-data-exporter`.

## v1.0.0

*2022年1月14日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg) Channel Manager的初始版本已正式发布

