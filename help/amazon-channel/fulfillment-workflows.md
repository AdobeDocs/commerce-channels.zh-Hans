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
| 1 | **商户履约订单被置于Amazon。** Amazon会分配状 `Pending` 态，直到验证客户的信用卡信息。处于`Pending`状态的订单会自动导入Amazon销售渠道，但不会显示在&#x200B;_[!UICONTROL Orders]_选项卡上。 |
| 2 | **命令由Amazon验证。** 验证后，Amazon会将状态更改为 `Unshipped`。此状态发生更改后，订单将在Amazon销售渠道中更新，并显示在&#x200B;_[!UICONTROL Orders]_选项卡中。 |
| 1 | **订单详细信息已更新。** Amazon销售渠道会使用价格、客户电子邮件和客户名称更新订单详细信息。在此更新期间，Amazon订单会在订单管理页面中创建相应的[!DNL Commerce]订单。 将显示[!DNL Commerce]订单编号，并在&#x200B;_[!UICONTROL Orders]_选项卡上显示订单信息。 |
| 4 | **将创建新的客户帐户。** 如果在订单设置中配置了客户，并且该客户在您的数据库中不 [!DNL Commerce] 存在，则会使用Amazon订单中的相 [!DNL Commerce] 应客户信息在您的数据库中创建新客户。如果您在订单设置中选择了`No Customer Creation (guest)`，则订单将遵循[!DNL Commerce]来宾进程，而不是在数据库中创建客户。 此时，如果您的[!DNL Commerce]系统与ERP/OMS/WMS集成，则会根据[!DNL Commerce]内放置并创建的新订单的集成来提取订单。 |
| 5 | **订单已发运。** 从订单 [!DNL Commerce] 处理页面中，您将发运订单并添加跟踪编号。当所有项目均标记为`Shipped`状态时：<ul><li>[!DNL Commerce]顺序的状态更改为`Complete`。</li><li>Amazon销售渠道订单的状态更改为`Shipped`。</li><li>跟踪编号会同步到Amazon,Amazon中顺序的状态会更改为`Shipped`。</li><li>发运通知通过Amazon发送给客户，而不是从[!DNL Commerce](根据Amazon的策略)发送。 |

## 示例：由Amazon(FBA)履行

| 步骤 | 描述 |
|---|---|
| 1 | **Amazon履行的订单将发送至Amazon。** |
| 2 | **订单已导入。** 在Amazon为订单分配了状态后，订单才会导入Amazon销 `Shipped` 售渠道。由于Amazon有此产品的库存，因此它可以防止对您的仓库/库存管理造成干扰。 |
| 1 | **订单详细信息已更新。** 如果在您的订 [单设置中配置](./order-settings.md),Amazon订单将创建相 [!DNL Commerce] 应的订单，并将其创建为状态为的 `Complete`订单。 |
