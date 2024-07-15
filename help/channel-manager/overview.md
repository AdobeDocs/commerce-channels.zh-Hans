---
title: '简介 [!DNL Channel Manager]'
description: “了解如何安装和使用 [!DNL Channel Manager] 将Adobe Commerce和Magento Open Source商店与沃尔玛商城集成，并创建销售渠道，以便从Commerce管理员无缝管理商城列表、定价、库存和销售额。”
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# [!DNL Channel Manager]简介

[!DNL Channel Manager]通过将Adobe Commerce或Magento Open Source产品目录与[!DNL Walmart Marketplace]集成，帮助商家提高销售额、接触新客户、简化销售操作并节省时间。

![[!DNL Channel Manager]扩展管理员视图](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager]通过扩展[!DNL Commerce]管理员支持希望在[!DNL Walmart Marketplace]上销售的Adobe Commerce或Magento Open Source商家。 安装[!DNL Channel Manager]后，商店管理员和运营人员可以从Commerce环境中无缝管理[!DNL Walmart Marketplace]的销售、库存和产品定价。

扩展的管理简化了操作，因为商家可以使用相同的工作流程和流程来管理[!DNL Commerce]店面和Walmart商场的销售。

安装并配置[!DNL Channel Manager]后，您可以使用以下功能来管理Walmart Marketplace销售订单：

* **列表管理** — 通过将[!DNL Commerce]目录中的产品与现有[!DNL Walmart Marketplace]列表进行匹配，轻松连接产品列表。

* **Inventory management** — 商家市场卖家帐户中的项目会自动从[!DNL Commerce]同步并更新，以确保库存水平准确无误。

* **定价更新** — 通过自动价格同步保持市场清单的准确定价。 当Adobe Commerce中的价格发生变化时，这些变化将反映在市场中。

* **订单管理** — 在商城中创建新订单时，[!DNL Channel Manager]将订单与Adobe Commerce同步，并向商城发送订单确认。 此确认可确保为每张订单预留库存。 最后一步是在[!DNL Commerce] Order Management系统中创建相应的订单以进行处理。

* **发运管理** — 在Adobe Commerce中将订单标记为发运时，会将发运更新发送到[!DNL Walmart Marketplace]。 此通知可确保销售商满足其履行SLA要求，并且客户会收到其当前订单的送货更新通知。

* **取消** — 在Adobe Commerce中取消订单时，[!DNL Channel Manager]将更新的订单信息发送到市场，以复制相应市场订单的操作。 订单取消完成后，[!DNL Commerce]库存数量更新以反映返回的物料，库存更新将自动同步到[!DNL Walmart Marketplace]。

* **退货和退款** — 当沃尔玛商城请求通过Adobe Commerce或Magento Open Source销售渠道订购的商品退货时，[!DNL Channel Manager]将退货请求信息发送到Commerce销售渠道商店，以复制退货请求。 然后，可以使用[!DNL Commerce] [退款工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow)脱机方法处理退款。 退款完成后，[!DNL Channel Manager]将更新同步到沃尔玛，以便可以更新市场卖方帐户中的退货状态以反映退款。

## [!DNL Channel Manager]操作的预期延迟

[!DNL Channel Manager]和链接的[!DNL Walmart Marketplace]存储区之间的数据同步过程需要一些时间才能完成。 查看[!DNL Channel Manager]操作的预期处理时间，以帮助规划销售渠道操作工作。

**预计延迟[!DNL Channel Manager]操作**

| **操作** | **描述** | **预期延迟** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 将产品添加到[!DNL Channel Manager] | 从[!DNL Commerce]产品目录中选择产品并将其导入[!DNL Channel Manager]。 | **最多5分钟** — 如果您选择许多产品，例如整个产品目录，则导入过程会花费较长时间。 |
| 匹配[!DNL Walmart Marketplace]上的产品 | 选择[!DNL Channel Manager]中的产品列表并发送到Walmart进行匹配。 | **最多30分钟** — 如果选择多个产品，则根据所选数量，匹配过程会花费较长时间。 |
| 清单更新 | 当Commerce中的库存数量发生变化时，[!DNL Channel Manager]将更新同步到沃尔玛。 | **最多10分钟** |
| 价格更新 | 当产品价格发生变化时，[!DNL Channel Manager]将更新同步到沃尔玛。 | **最多5分钟** |
| 从Walmart到[!DNL Commerce]的订单同步 | 客户在沃尔玛商城中订购[!DNL Commerce]产品。 沃尔玛将订单发送至[!DNL Channel Manager]。 订单会显示在订单控制面板中。 | **最多30分钟** |
| 在[!DNL Commerce] Order Management中创建的订单 | [!DNL Channel Manager]从Walmart订单创建[!DNL Commerce]订单并更新订单仪表板以包含[!DNL Commerce]订单编号。 | **最多5分钟** |
| [!DNL Commerce] Order Management中的配送状态更新 | 从Commerce发运订单时，[!DNL Channel Manager]会更新订单仪表板中的发运状态，并将更新发送到Walmart商城，以便通知客户。 | **最多5分钟** |
| Commerce Order Management中的订单取消更新 | 从Commerce取消订单后，[!DNL Channel Manager]会在订单仪表板中更新订单状态，并将更新发送到沃尔玛商城，以便通知客户。 订单取消完成后，[!DNL Commerce]库存数量会更新以反映返回的物料。 然后，[!DNL Channel Manager]将更新同步到[!DNL Walmart Marketplace]。 | **最多5分钟** |


