---
title: '[!DNL Channel Manager] 发行说明'
description: 的最新发行信息 [!DNL Channel Manager] 从Adobe Commerce。
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: d3acde7aa297ba33dffa7854aa7578985ad12c9b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# [!DNL Channel Manager] 发行说明

以下发行说明介绍了 [!DNL Channel Manager] 包括：

![新建](../assets/new.svg) 新增功能
![修复的问题](../assets/fix.svg) 修复和改进功能
![已知问题](../assets/bug.svg) 已知问题


## v2.0.0

*2023年3月20日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg)<!--CHAN-5893--> “渠道管理器”现在与Adobe Commerce版本2.4.6兼容。

## v1.1.0

*2022年11月23日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg)<!--CHAN-5204--> **退货和退款** — 您现在可以处理通过Adobe Commerce和Varmalt Channel Manger商店发送的订单的Walmart Marketplace退货和退款流程。 有关退货和退款的信息和更新将在沃尔玛和Adobe Commerce之间同步，以便在 [!DNL Commerce] 店面和店面 [!DNL Walmart Marketplace]. 请参阅 [退货和退款订单](return-refund-orders.md).

![已修复](../assets/fix.svg)<!--CHAN-5661--> 修复了 `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` 重新同步Channel Manager使用 `bin/magento saas:resync --feed orders` 命令。 通过更新Sales Data Exporter模块的Channel Manager包依赖项，该模块已从 `magento/module-sales-data-exporter` to `magento/module-sales-orders-data-exporter`.

## v1.0.0

*2022年1月14日*

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg) Channel Manager的初始版本正式发布

