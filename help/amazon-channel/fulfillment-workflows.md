---
title: Amazon履行工作流
description: 从Amazon列表完成订单后，需遵循从订单提交到发运的特定顺序。
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon履行工作流

## 示例：由商人履行

| 步骤 | 描述 |
|----|----|
| 1 | **商户履约订单被置于Amazon。** Amazon会为 `Pending` 直到客户的信用卡信息得到验证。 订单 `Pending` 状态会自动导入到Amazon销售渠道，但不会显示在 _[!UICONTROL Orders]_选项卡。 |
| 2 | **命令由Amazon验证。** 验证后，Amazon会将状态更改为 `Unshipped`. 此状态发生更改后，订单将在Amazon销售渠道中更新，并显示在 _[!UICONTROL Orders]_选项卡。 |
| 3 | **订单详细信息已更新。** Amazon销售渠道会使用价格、客户电子邮件和客户名称更新订单详细信息。 在此更新期间，Amazon订单会创建相应的 [!DNL Commerce] 订单管理页面中的订单。 的 [!DNL Commerce] 订单编号显示时，订单信息位于 _[!UICONTROL Orders]_选项卡。 |
| 4 | **将创建新的客户帐户。** 如果在订单设置中进行了配置，并且客户在 [!DNL Commerce] 数据库，在 [!DNL Commerce] 使用Amazon订单中相应的客户信息的数据库。 如果您选择 `No Customer Creation (guest)` 在您的订单设置中，顺序如下 [!DNL Commerce] 来宾进程，而不是在数据库中创建客户。 此时，如果 [!DNL Commerce] 系统与ERP/OMS/WMS集成，根据在内部放置和创建的新订单的集成来提取订单 [!DNL Commerce]. |
| 5 | **订单已发运。** 从 [!DNL Commerce] 订单处理页面，则需发运订单并添加跟踪编号。 当所有项目都标记在 `Shipped` 状态：<ul><li>的状态 [!DNL Commerce] 订单更改 `Complete`.</li><li>Amazon销售渠道订单的状态更改为 `Shipped`.</li><li>跟踪编号会同步到Amazon，并且Amazon中的顺序状态会更改为 `Shipped`.</li><li>发运通知通过Amazon发送给客户，而不是从 [!DNL Commerce] (根据Amazon的政策)。 |

## 示例：由Amazon(FBA)履行

| 步骤 | 描述 |
|---|---|
| 1 | **Amazon履行的订单将发送至Amazon。** |
| 2 | **订单已导入。** 在将订单分配到 `Shipped` 状态(由Amazon)。 由于Amazon有此产品的库存，因此它可以防止对您的仓库/库存管理造成干扰。 |
| 3 | **订单详细信息已更新。** 如果在 [订购设置](./order-settings.md)，则Amazon订单会创建相应的 [!DNL Commerce] 订单，并创建为状态为 `Complete`. |
