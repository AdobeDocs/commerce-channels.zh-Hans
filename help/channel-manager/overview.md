---
title: '''简介 [!DNL Channel Manager]’'
description: '''了解如何安装和使用 [!DNL Channel Manager] 将Adobe Commerce和Magento Open Source商店与沃尔玛商城集成在一起，创建销售渠道，以便从商务管理员那里无缝管理商城列表、定价、库存和销售额。'
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# 简介 [!DNL Channel Manager]

[!DNL Channel Manager] 通过将Adobe Commerce或Magento Open Source产品目录与 [!DNL Walmart Marketplace].

![[!DNL Channel Manager] 扩展管理员视图](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] 支持希望向以下产品销售的Adobe Commerce或Magento Open Source商家： [!DNL Walmart Marketplace] 通过扩展 [!DNL Commerce] 管理员。 替换为 [!DNL Channel Manager] 安装、存储管理员和操作人员可以管理 [!DNL Walmart Marketplace] 从Commerce环境中无缝地获取销售、库存和产品定价。

扩展的管理流程简化了操作，因为商家可以使用相同的工作流程和流程来管理来自两者的销售 [!DNL Commerce] 店面和沃尔玛商场。

安装和配置之后 [!DNL Channel Manager]，则可以使用以下功能来管理沃尔玛商城的销售订单：

* **列表管理** — 通过匹配您的产品，轻松连接产品清单 [!DNL Commerce] 目录到现有 [!DNL Walmart Marketplace] 列表。

* **Inventory management** — 商户的Marketplace卖方帐户中的项目将自动同步并更新，从 [!DNL Commerce] 以确保准确的库存水平。

* **定价更新** — 通过自动价格同步来维护市场清单的准确定价。 当Adobe Commerce中的价格发生变化时，这些变化将反映在市场中。

* **订单管理** — 在市场中创建新订单时， [!DNL Channel Manager] 与Adobe Commerce同步订单，并将订单确认发送到市场。 此确认可确保为每张订单预留库存。 最后一步是在以下位置创建相应的订单： [!DNL Commerce] 订单管理系统进行处理。

* **配送管理** — 在Adobe Commerce中将订单标记为已发运时，会将发运更新发送至 [!DNL Walmart Marketplace]. 此通知可确保销售商满足其履行SLA要求，并且客户会收到其当前订单的送货更新通知。

* **取消次数** — 在Adobe Commerce中取消订单时， [!DNL Channel Manager] 将更新的订单信息发送到市场，以复制相应市场订单的操作。 订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的物料和库存更新会自动同步到 [!DNL Walmart Marketplace].

* **退货和退款** — 当沃尔玛商店要求退货通过Adobe Commerce或Magento Open Source销售渠道订购的商品时， [!DNL Channel Manager] 将返回请求信息发送到Commerce sales channel store以复制返回请求。 然后，可以使用处理退款 [!DNL Commerce] [退款工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow)，脱机方法。 退款完成之后， [!DNL Channel Manager] 将更新同步到沃尔玛，以便可以更新市场卖方帐户中的退货状态以反映退款。

## 的预期延迟 [!DNL Channel Manager] 操作

数据同步过程介于 [!DNL Channel Manager] 和链接的 [!DNL Walmart Marketplace] 存储需要一些时间才能完成。 查看以下项的预期处理时间 [!DNL Channel Manager] 操作以帮助计划销售渠道操作工作。

**估计滞后时间 [!DNL Channel Manager] 操作**

| **操作** | **描述** | **预期延迟** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 将产品添加到 [!DNL Channel Manager] | 从中选择产品 [!DNL Commerce] 产品目录并将其导入 [!DNL Channel Manager]. | **最多五分钟** — 如果选择多个产品（例如，整个产品目录），则导入过程会花费较长时间。 |
| 匹配产品 [!DNL Walmart Marketplace] | 选择产品列表 [!DNL Channel Manager] 送去沃尔玛进行配对。 | **长达30分钟** — 如果选择多个产品，则匹配过程会花费较长时间，具体取决于所选数量。 |
| 清单更新 | 当Commerce中的库存数量发生变化时， [!DNL Channel Manager] 将更新同步到沃尔玛。 | **最多10分钟** |
| 价格更新 | 当产品价格发生变化时， [!DNL Channel Manager] 将更新同步到沃尔玛。 | **最多五分钟** |
| 订单同步从Walmart到 [!DNL Commerce] | 客户订购 [!DNL Commerce] 在沃尔玛市场出售的商品。 沃尔玛把订单发给 [!DNL Channel Manager]. 订单会显示在订单控制面板中。 | **长达30分钟** |
| 订单创建于 [!DNL Commerce] Order Management | [!DNL Channel Manager] 创建 [!DNL Commerce] 沃尔玛订单中的订单，并更新订单仪表板，以包含 [!DNL Commerce] 订单号。 | **最多五分钟** |
| 装运状态更新于 [!DNL Commerce] Order Management | 从Commerce发送订单时， [!DNL Channel Manager] 更新订单仪表板中的送货状态，并将更新发送到沃尔玛商城，以便通知客户。 | **最多五分钟** |
| Commerce Order Management中的订单取消更新 | 从Commerce取消订单时， [!DNL Channel Manager] 更新订单仪表板中的订单状态，并将更新发送到沃尔玛商城，以便通知客户。 订单取消完成后， [!DNL Commerce] 库存数量更新以反映退回的物料。 然后， [!DNL Channel Manager] 将更新同步到 [!DNL Walmart Marketplace]. | **最多五分钟** |


