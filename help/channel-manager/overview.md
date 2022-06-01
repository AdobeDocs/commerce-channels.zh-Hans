---
title: “关于 [!DNL Channel Manager]"
description: “了解如何安装和使用 [!DNL Channel Manager] 将Adobe Commerce和Magento Open Source商店与第三方市场集成，并创建销售渠道，从您的商务管理员无缝地管理Marketplace列表、定价、库存和销售。”
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ae3d95fd0da6ee5013a19d7ac7ed5ef87e4a1325
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---


# 关于 [!DNL Channel Manager]

[!DNL Channel Manager] 通过将Adobe Commerce或Magento Open Source产品目录与 [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] 扩展管理员视图](assets/channel-manager-home.png)

渠道管理器支持要销售的Adobe Commerce或Magento Open Source销售商 [!DNL Walmart Marketplace].

安装和配置之后 [!DNL Channel Manager], [!DNL Commerce] 扩展了管理员，因此您可以管理 [!DNL Walmart Marketplace] 销售操作可在您的商务环境中无缝进行。

* **列表管理** — 通过匹配 [!DNL Commerce] 现有目录 [!DNL Walmart Marketplace] 列表。

* **Inventory management** — 商户的市场卖家帐户中的项目会自动同步并从Commerce更新，以确保准确的库存水平。

* **定价更新** — 通过自动价格同步为市场列表维护准确的定价。 当Adobe Commerce中的价格发生更改时，这些更改将在10分钟内反映在市场中。

* **订单管理** — 当在市场中创建新订单时，渠道管理器会与Adobe Commerce同步订单，并向市场发送订单确认，以确保为每个订单保留库存。

* **装运管理** — 当订单在Adobe Commerce中标记为已发运时，发运更新将发送至 [!DNL Walmart Marketplace]. 此通知可确保销售商满足其履行SLA要求，并确保客户收到其当前订单的送货更新通知。

* **取消** — 当在Adobe Commerce中取消订单时，渠道管理器会向市场发送更新的订单信息，以复制相应市场订单的操作。

## Channel Manager操作的预期滞后

数据同步在 [!DNL Channel Manager] 和链接 [!DNL Walmart Marketplace] 存储需要一些时间才能完成。 查看 [!DNL Channel Manager] 操作以帮助计划销售渠道操作。

**Channel Manager操作的预计延迟**

| **操作** | **描述** | **预期延迟** |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 将产品添加到渠道管理器 | 从商务产品目录中选择产品，然后将它们导入渠道管理器。 | **最多五分钟** — 如果您选择了许多产品（例如整个产品目录），则导入过程会花费更长的时间。 |
| 在上匹配产品[!DNL Walmart Marketplace] | 在渠道管理器中选择产品清单，然后发送到沃尔玛进行匹配。 | **最多30分钟** — 如果选择多个产品，则根据所选数量，匹配过程将花费更长的时间。 |
| 库存更新 | 当商务中的库存数量发生更改时， [!DNL Channel Manager] 同步更新到Walmart。 | **最多10分钟** |
| 价格更新 | 当产品价格发生更改时，渠道管理器会将更新同步到Walmart。 | **最多五分钟** |
| Walmart与Commerce的订单同步 | 客户在Walmart Marketplace上订购商务产品。 沃尔玛将订单发给渠道经理。 顺序显示在订单仪表板中。 | **最多30分钟** |
| 在Oracle Commerce Order Management中创建的订单 | 渠道管理器从沃尔玛订单中创建商务订单，并更新订单仪表板以包含商务订单编号。 | **最多五分钟** |

