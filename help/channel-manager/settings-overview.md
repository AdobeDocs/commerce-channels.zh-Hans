---
title: 设置概述
description: '了解 [!DNL Channel Manager settings] 配置身份验证并映射产品目录属性和装运承运人，在两者之间协调销售操作时需要这些属性 [!DNL Commerce] 和 [!DNL Walmart Marketplace].'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 设置概述

销售渠道设置实现了以下两方面的通信和数据同步： [!DNL Commerce] 和 [!DNL Walmart Marketplace] 以便您管理 [!DNL Walmart Marketplace] 销售业务来自 [!DNL Commerce] 管理员。

In [!DNL Channel Manager]，您即可在新用户引导过程中配置一些销售渠道设置。 载入后，您可以通过选择查看和管理配置 **[!UICONTROL Channel Settings]** 从 [!UICONTROL Listings] 和 [!UICONTROL Orders] 功能板。

* **[沃尔玛网络](manage-wmt-connection.md)** — 期间 [!DNL Channel Manager] 载入流程，您提供 [API凭据](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) 来自您的 [!DNL Walmart Marketplace] 要连接的卖方帐户 [!DNL Commerce] 到 [!DNL Walmart Marketplace] 用于通信和数据同步。 如果需要，您可以从以下位置更新这些凭据 *渠道设置* 页面。

* **[映射唯一标识符](map-catalog-attributes.md)** — 从以下位置连接列表之前： [!DNL Commerce] 到 [!DNL Walmart Marketplace]，至少映射一个来自您的的唯一标识符 [!DNL Commerce] 目录到沃尔玛的相应标识符。 需要此步骤才能进行匹配 [!DNL Commerce] 产品到现有 [!DNL Walmart] 清单和产品数据同步方法 [!DNL Commerce] 和 [!DNL Walmart].

* **[映射装运承运人](map-shipping-carriers.md)** — 在处理之前 [!DNL Walmart Marketplace] 订单来源 [!DNL Commerce]，确保您映射的货运公司 [!DNL Commerce] 上的相应运营商的实例 [!DNL Walmart Marketplace].
