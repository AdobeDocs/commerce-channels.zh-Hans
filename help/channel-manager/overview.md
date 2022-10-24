---
title: '简介 [!DNL Channel Manager]'
description: “了解如何安装和使用 [!DNL Channel Manager] 将Adobe Commerce和Magento Open Source店与Walmart Marketplace集成，并创建销售渠道，从您的商务管理员处无缝地管理市场列表、定价、库存和销售。
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 2e3f8e51b765cda0559d8624d61e1ae9dc1c9667
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# 简介 [!DNL Channel Manager]

[!DNL Channel Manager] 通过将Adobe Commerce或Magento Open Source产品目录与 [!DNL Walmart Marketplace].

![[!DNL Channel Manager] 扩展管理员视图](assets/channel-manager-home.png)

[!DNL Channel Manager] 支持Adobe Commerce或Magento Open Source商，他们希望销售 [!DNL Walmart Marketplace] 通过 [!DNL Commerce] 管理员。 使用 [!DNL Channel Manager] 安装、存储管理员和操作人员可以管理 [!DNL Walmart Marketplace] 销售、库存和产品定价。

扩展的管理员可简化操作，因为商家可以使用相同的工作流程和流程来管理来自这两种渠道的销售 [!DNL Commerce] 店面和沃尔玛市场。

安装和配置之后 [!DNL Channel Manager]，您可以使用以下功能管理Walmart Marketplace销售订单：

* **列表管理** — 通过匹配 [!DNL Commerce] 现有目录 [!DNL Walmart Marketplace] 列表。

* **Inventory management** — 商户的市场卖家帐户中的项目自动同步并更新自 [!DNL Commerce] 以确保准确的库存水平。

* **定价更新** — 通过自动价格同步为市场列表维护准确的定价。 当Adobe Commerce中的价格发生更改时，这些更改将反映在市场中。

* **订单管理** — 在市场中创建新订单时， [!DNL Channel Manager] 与Adobe Commerce同步订单，并向市场发送订单确认。 此确认可确保为每笔订单保留库存。 最后一步是在 [!DNL Commerce] 订单管理系统。

* **装运管理** — 在Adobe Commerce中将订单标记为已发运时，发运更新将发送至 [!DNL Walmart Marketplace]. 此通知可确保销售商满足其履行SLA要求，并确保客户收到其当前订单的送货更新通知。

* **取消** — 在Adobe Commerce取消订单时， [!DNL Channel Manager] 向市场发送更新的订单信息，以复制相应市场订单的操作。 订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的物料和库存更新，自动同步到 [!DNL Walmart Marketplace].

* **退货和退款** — 当Walmart Marketplace请求退回通过Adobe Commerce或Magento Open Source销售渠道订购的商品时， [!DNL Channel Manager] 将回访请求信息发送到Commerce sales channel存储区以复制回访请求。 然后，可以使用 [!DNL Commerce] [退款工作流](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow)，脱机方法。 退款完成后， [!DNL Channel Manager] 将更新同步到沃尔玛，以便能够更新市场卖家帐户中的退货状态，以反映退款。

## 的预期滞后 [!DNL Channel Manager] 操作

数据同步在 [!DNL Channel Manager] 和链接 [!DNL Walmart Marketplace] 存储需要一些时间才能完成。 查看 [!DNL Channel Manager] 操作以帮助计划销售渠道操作。

**预计延迟 [!DNL Channel Manager] 操作**

| **操作** | **描述** | **预期延迟** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 将产品添加到 [!DNL Channel Manager] | 从 [!DNL Commerce] 产品目录，并将其导入 [!DNL Channel Manager]. | **最多五分钟** — 如果您选择了许多产品（例如整个产品目录），则导入过程会花费更长的时间。 |
| 在上匹配产品 [!DNL Walmart Marketplace] | 选择 [!DNL Channel Manager] 送到沃尔玛进行配对。 | **最多30分钟** — 如果选择多个产品，则根据所选数量，匹配过程将花费更长的时间。 |
| 库存更新 | 当商务中的库存数量发生更改时， [!DNL Channel Manager] 同步更新到Walmart。 | **最多10分钟** |
| 价格更新 | 当产品价格发生变化时， [!DNL Channel Manager] 同步更新到Walmart。 | **最多五分钟** |
| 从Walmart到 [!DNL Commerce] | 客户订购 [!DNL Commerce] 产品。 沃尔玛下订单 [!DNL Channel Manager]. 顺序显示在订单仪表板中。 | **最多30分钟** |
| 在中创建的订单 [!DNL Commerce] Order Management | [!DNL Channel Manager] 创建 [!DNL Commerce] 从Walmart订单下单并更新订单仪表板以包含 [!DNL Commerce] 订单编号。 | **最多五分钟** |
| 中的装运状态更新 [!DNL Commerce] Order Management | 从Commerce发运订单时， [!DNL Channel Manager] 更新订单仪表板中的“送货”状态，并将更新发送至Walmart marketplace，以便通知客户。 | **最多五分钟** |
| 商务订单管理中的订单取消更新 | 从商务中取消订单时， [!DNL Channel Manager] 更新订单仪表板中的订单状态，并将更新发送到Walmart marketplace，以便通知客户。 订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的项目。 然后， [!DNL Channel Manager] 同步更新到 [!DNL Walmart Marketplace]. | **最多五分钟** |


