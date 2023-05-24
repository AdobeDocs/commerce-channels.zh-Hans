---
title: Amazon Fulfillment工作流
description: Amazon列表中的订单履行将遵循从订单提交到发运的特定顺序。
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon Fulfillment工作流

## 示例：由商家履行

| 步骤 | 描述 |
|----|----|
| 1 | **在Amazon上下达了商家履行的订单。** Amazon分配状态 `Pending` 直到客户信用卡信息得到确认。 中的订单 `Pending` 状态会自动导入到Amazon sales channel中，但不会显示在 _[!UICONTROL Orders]_选项卡。 |
| 2 | **该订单已由Amazon验证。** 验证后，Amazon会将状态更改为 `Unshipped`. 此状态更改后，订单将在Amazon sales channel中更新，并显示在 _[!UICONTROL Orders]_选项卡。 |
| 3 | **订单详细信息已更新。** Amazon sales channel使用价格、客户电子邮件和客户名称更新订单详细信息。 在此更新期间，Amazon订单将创建相应的 [!DNL Commerce] order management页面中的order。 此 [!DNL Commerce] 订单编号与订单信息一起显示在 _[!UICONTROL Orders]_选项卡。 |
| 4 | **将创建一个新的客户帐户。** 如果您在订单设置中进行了配置，但您的中不存在该客户 [!DNL Commerce] 数据库，则会在以下位置创建一个新客户： [!DNL Commerce] 数据库使用Amazon订单中的相应客户信息。 如果您选择 `No Customer Creation (guest)` 在订单设置中，顺序遵循 [!DNL Commerce] 来宾进程，而不是在数据库中创建客户。 此时，如果您的 [!DNL Commerce] 系统与ERP/OMS/WMS集成，根据新订单的集成来提取订单，并在其中放置和创建新订单 [!DNL Commerce]. |
| 5 | **订单已装运。** 从 [!DNL Commerce] 订单处理页面，您可以发送订单并添加跟踪编号。 当所有项目都在 `Shipped` 状态：<ul><li>的状态 [!DNL Commerce] 订单更改至 `Complete`.</li><li>Amazon销售渠道订单的状态更改为 `Shipped`.</li><li>跟踪编号已同步到Amazon，并且Amazon中订单的状态将更改为 `Shipped`.</li><li>送货通知是通过Amazon发送给客户的，而不是从 [!DNL Commerce] (根据Amazon的政策)。 |

## 示例：由Amazon (FBA)履行

| 步骤 | 描述 |
|---|---|
| 1 | **Amazon履行的订单是在Amazon上下达的。** |
| 2 | **订单已导入。** 在为该订单分配了以下内容之前，该订单不会导入Amazon Sales Channel： `Shipped` 状态(按Amazon)。 由于Amazon拥有此产品的库存，因此可防止对仓库/库存管理的干扰。 |
| 3 | **订单详细信息已更新。** 如果您已在以下项目中配置： [订单设置](./order-settings.md)，Amazon订单会创建相应的 [!DNL Commerce] 订单并将其创建为状态为的订单 `Complete`. |
