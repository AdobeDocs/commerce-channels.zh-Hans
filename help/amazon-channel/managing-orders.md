---
title: 管理订单
description: 您可以在“订单设置”中启用订单导入，以便更轻松地从商务管理员处管理Amazon订单。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 1d1b888db4de4f6e3658af768cd6f5cf30828788
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# 管理订单

您可以在 _[!UICONTROL Recent Orders]_部分 [存储仪表板](./amazon-store-dashboard.md) 或_[!UICONTROL Amazon orders]_ 页面(也称为 _[!UICONTROL All Orders]_视图)。

如何管理Amazon订单，取决于您的 [订单设置](./order-settings.md#configure-order-settings).

## 启用订单导入

之后 [存储集成](./store-integration.md), [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 设置 `Enabled` 默认情况下。 使用此设置时，对应 [!DNL Commerce] 为Amazon订单创建订单，并可在 [[!DNL Commerce] 订单数](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作流。

>[!NOTE]
>
>无论您的订单导入设置如何，Amazon中存在的订单 [!DNL Amazon Seller Central] 帐户之前 [存储集成](./store-integration.md) 未导入。

导入的Amazon订单在 [[!DNL Commerce] 订单数](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作流，与您的其他工作流一样 [!DNL Commerce] 商店。 单击 *[!UICONTROL Order Number]* 列，以在 [[!DNL Commerce] 订购流程](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}。 请参阅 [查看Amazon订单](./amazon-orders-all.md).

### 订单导入流程

在Amazon和 [订单导入](./order-settings.md) 启用后，将开始以下进程。

| 更改 | 操作 |
|---|---|
| 订单被下达到Amazon。 | <ul><li>Amazon将订单状态设置为 `Pending`.</li><li>订单信息将发送到 [!DNL Commerce].</li><li>订单已添加到 [_Amazon订单_ 表](./amazon-orders-all.md) 带有 `Pending` 状态。</li></ul> |
| Amazon将订单状态更改为 `Unshipped`. | <ul><li>状态更改将发送到 [!DNL Commerce].</li><li>在 [_Amazon订单_ 表](./amazon-orders-all.md)，则顺序状态将更改为 `Unshipped`.</li><li>在 [[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}，对应 [!DNL Commerce] 使用 `Processing` 状态。</li></ul> |
| 在 [[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, [!DNL Commerce] 订单会得到处理，状态会更改为 `Shipped`. | <ul><li>在 [_Amazon订单_ 表](./amazon-orders-all.md)，则顺序状态将更改为 `Shipped`.</li><li>在下一个Cron作业中，订单状态将更改为 `Complete` 在 [[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}。</li></ul> |

### 订单创建阻止程序

有一些情况会阻止创建相应的 [!DNL Commerce] 订单。 [!DNL Commerce] 发生以下任何问题时，不会为接收的订单创建订单。

| 方案 | 解决方案 |
|---|---|
| 该项目在 [!DNL Commerce] 目录。 | [创建产品](./creating-assigning-catalog-products.md) 在 [!DNL Commerce] 目录和 [手动匹配](./creating-assigning-catalog-products.md) 就是产品。 |
| 目录中的项目处于禁用状态。 | 确保 [产品状态](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html)已启用{target=&quot;_blank&quot;}。 |
| 订购的物料无现货。 | 更新或配置 [产品选项](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target=&quot;_blank&quot;}表示数量和来源。 |

当无法导入订单时，屏幕顶部会显示与以下类似的系统消息：

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

问题解决后， [!DNL Commerce] 下次同步时会创建顺序。

## 禁用订单导入

如果您不想在 [!DNL Commerce]，您可以更改 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 设置为 `Disabled`. 此设置表示当从Amazon收到新订单时，对应 [!DNL Commerce] 不会创建订单。

禁用后，从Amazon收到的订单信息将显示在 _[!UICONTROL Recent Orders]_的_[!UICONTROL All Orders]_ 中。 此订单信息仅供查看，您必须在 [!DNL Amazon Seller Central]. 要在 [!DNL Amazon Seller Central]，请单击 _[!UICONTROL Order Number]_列。

另请参阅 [查看Amazon订单](./amazon-orders-all.md), [查看Amazon订单详细信息](./amazon-order-details.md)和 [常见订单处理任务](./common-order-processing.md).
