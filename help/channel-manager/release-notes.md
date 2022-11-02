---
title: “[!DNLChannel Manager]发行说明”
description: “ [!DNL Channel Manager] 来自Adobe Commerce。”
source-git-commit: 501a76a126f090805f95e64078ec2c73de003aa4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Channel Manager] 发行说明

以下发行说明介绍了 [!DNL Channel Manager] 包括：

![新建](../assets/new.svg) 新增功能
![修复的问题](../assets/fix.svg) 修复和改进功能
![已知问题](../assets/bug.svg) 已知问题


## v1.1.0

![新建](../assets/new.svg)<!--CHAN-5204--> **退货和退款** — 您现在可以处理通过Adobe Commerce和Varmalt Channel Manger商店发送的订单的Walmart Marketplace退货和退款流程。 有关退货和退款的信息和更新将在沃尔玛和Adobe Commerce之间同步，以便在 [!DNL Commerce] 店面和店面 [!DNL Walmart Marketplace]. 请参阅 [退货和退款订单](return-refund-orders.md).

![已修复](../assets/fix.svg)<!--CHAN-5661--> 修复了 `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` 重新同步Channel Manager使用 `bin/magento saas:resync --feed orders` 命令。 通过更新Sales Data Exporter模块的Channel Manager包依赖项，该模块已从 `magento/module-sales-data-exporter` to `magento/module-sales-orders-data-exporter`.

## v1.0.0

初始版本，与以下商务版本兼容：

* 开源(CE):2.4.x
* Adobe Commerce(EE):2.4.x
* Adobe Commerce for Cloud(ECE):2.4.x
* 稳定性：稳定
