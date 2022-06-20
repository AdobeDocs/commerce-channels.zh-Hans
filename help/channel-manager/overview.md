---
title: “关于 [!DNL Channel Manager]"
description: “了解如何安装和使用 [!DNL Channel Manager] 将Adobe Commerce和Magento Open Source商店与第三方市场集成，并创建销售渠道，从您的商务管理员无缝地管理Marketplace列表、定价、库存和销售。”
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 690eeb5d03b23cac11f3c14b04601c514c76e0bd
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---


# 关于 [!DNL Channel Manager]

[!DNL Channel Manager] 通过将Adobe Commerce或Magento Open Source产品目录与 [!DNL Walmart Marketplace].

![[!DNL Channel Manager] 扩展管理员视图](assets/channel-manager-home.png)

[!DNL Channel Manager] 支持Adobe Commerce或Magento Open Source商，他们希望销售 [!DNL Walmart Marketplace] 通过 [!DNL Commerce] 具有管理功能的管理员 [!DNL Walmart Marketplace] 销售、库存和产品定价。

扩展的管理员可简化操作，因为商家可以使用相同的工作流程和流程来管理来自商业店面和沃尔玛市场的销售。

安装和配置之后 [!DNL Channel Manager]，您可以使用以下功能管理Walmart Marketplace销售订单：

* **列表管理** — 通过匹配 [!DNL Commerce] 现有目录 [!DNL Walmart Marketplace] 列表。

* **Inventory management** — 商户的市场卖家帐户中的项目会自动同步并从Commerce更新，以确保准确的库存水平。

* **定价更新** — 通过自动价格同步为市场列表维护准确的定价。 当Adobe Commerce中的价格发生更改时，这些更改将反映在市场中。

* **订单管理** — 在市场中创建新订单时， [!DNL Channel Manager] 与Adobe Commerce同步订单，向市场发送订单确认以确保为每个订单保留库存，并在商务订单管理系统中创建相应的订单以进行处理。

* **装运管理** — 当订单在Adobe Commerce中标记为已发运时，发运更新将发送至 [!DNL Walmart Marketplace]. 此通知可确保销售商满足其履行SLA要求，并确保客户收到其当前订单的送货更新通知。

* **取消** — 在Adobe Commerce取消订单时， [!DNL Channel Manager] 向市场发送更新的订单信息，以复制相应市场订单的操作。  订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的物料和库存更新自动同步到 [!DNL Walmart Marketplace].

## 的预期滞后 [!DNL Channel Manager] 操作

数据同步在 [!DNL Channel Manager] 和链接 [!DNL Walmart Marketplace] 存储需要一些时间才能完成。 查看 [!DNL Channel Manager] 操作以帮助计划销售渠道操作。

**预计延迟 [!DNL Channel Manager] 操作**

| **操作** | **描述** | **预期延迟** |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 将产品添加到 [!DNL Channel Manager] | 从商务产品目录中选择产品并将其导入 [!DNL Channel Manager]. | **最多五分钟** — 如果您选择了许多产品（例如整个产品目录），则导入过程会花费更长的时间。 |
| 在上匹配产品 [!DNL Walmart Marketplace] | 选择 [!DNL Channel Manager] 送到沃尔玛进行配对。 | **最多30分钟** — 如果选择多个产品，则根据所选数量，匹配过程将花费更长的时间。 |
| 库存更新 | 当商务中的库存数量发生更改时， [!DNL Channel Manager] 同步更新到Walmart。 | **最多10分钟** |
| 价格更新 | 当产品价格发生变化时， [!DNL Channel Manager] 同步更新到Walmart。 | **最多五分钟** |
| Walmart与Commerce的订单同步 | 客户在Walmart Marketplace上订购商务产品。 沃尔玛下订单 [!DNL Channel Manager]. 顺序显示在订单仪表板中。 | **最多30分钟** |
| 在Oracle Commerce Order Management中创建的订单 | [!DNL Channel Manager] 从沃尔玛订单中创建商务订单，并更新订单仪表板以包含商务订单编号。 | **最多五分钟** |
| Oracle Commerce Order Management中的发运状态更新 | 从Commerce发运订单时， [!DNL Channel Manager] 更新订单仪表板中的“送货”状态，并将更新发送至Walmart marketplace，以便通知客户。 | **最多五分钟** |
| 商务订单管理中的订单取消更新 | 从商务中取消订单时， [!DNL Channel Manager] 更新订单仪表板中的订单状态，并将更新发送到Walmart marketplace，以便通知客户。 订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的项目。 然后， [!DNL Channel Manager] 同步更新到 [!DNL Walmart Marketplace]. | **最多五分钟** |


