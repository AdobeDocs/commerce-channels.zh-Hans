---
title: 管理订单
description: 您可以在“订单设置”中启用订单导入，以便更轻松地从商务管理员处管理Amazon订单。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# 管理订单

您可以在[存储功能板](./amazon-store-dashboard.md)的&#x200B;_[!UICONTROL Recent Orders]_部分或在_[!UICONTROL Amazon orders]_&#x200B;页面（也称为&#x200B;_[!UICONTROL All Orders]_视图）中查看从Amazon收到的Amazon订单信息。

如何管理Amazon订单取决于您的[订单设置](./order-settings.md#configure-order-settings)中是启用还是禁用订单导入。

## 启用订单导入

在[存储集成](./store-integration.md)之后，默认情况下，[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)设置为`Enabled`。 通过此设置，将为您的Amazon订单创建相应的[!DNL Commerce]订单，并可在[[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作流中进行管理。

>[!NOTE]
>
>无论您的订单导入设置如何，在[store integration](./store-integration.md)之前，您的[!DNL Amazon Seller Central]帐户中存在的Amazon订单都不会导入。

导入的Amazon订单在[[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作流中进行管理，就像您的其他[!DNL Commerce]存储一样。 单击&#x200B;*[!UICONTROL Order Number]*&#x200B;列中的Amazon订单号以打开[[!DNL Commerce] order process](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}中的顺序。 请参阅[查看Amazon订单](./amazon-orders-all.md)。

### 订单导入流程

在Amazon上下订单并启用[订单导入](./order-settings.md)后，将开始以下过程。

| 更改 | 操作 |
|---|---|
| 订单被下达到Amazon。 | <ul><li>Amazon将顺序状态设置为`Pending`。</li><li>订单信息将发送到[!DNL Commerce]。</li><li>将顺序添加到状态为`Pending`的&#x200B;[_Amazon订单_&#x200B;表](./amazon-orders-all.md)中。</li></ul> |
| Amazon将顺序状态更改为`Unshipped`。 | <ul><li>状态更改将发送到[!DNL Commerce]。</li><li>在&#x200B;[_Amazon订单_&#x200B;表](./amazon-orders-all.md)中，订单状态更改为`Unshipped`。</li><li>在[[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}中，创建具有`Processing`状态的相应[!DNL Commerce]订单。</li></ul> |
| 在[[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}中，将处理[!DNL Commerce]顺序，并将状态更改为`Shipped`。 | <ul><li>在&#x200B;[_Amazon订单_&#x200B;表](./amazon-orders-all.md)中，订单状态更改为`Shipped`。</li><li>在下一个cron作业中，订单状态在[[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}中变为`Complete`。</li></ul> |

### 订单创建阻止程序

有一些情况会阻止创建相应的[!DNL Commerce]顺序。 [!DNL Commerce] 发生以下任何问题时，不会为接收的订单创建订单。

| 方案 | 解决方案 |
|---|---|
| 该项目在[!DNL Commerce]目录中不存在。 | [在目录](./creating-assigning-catalog-products.md) 中创 [!DNL Commerce] 建产品 [并手](./creating-assigning-catalog-products.md) 动将其与产品匹配。 |
| 目录中的项目处于禁用状态。 | 确保已启用[产品状态](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;}。 |
| 订购的物料无现货。 | 更新或配置[产品选项](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;}，以获取数量和来源。 |

当无法导入订单时，屏幕顶部会显示与以下类似的系统消息：

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

问题解决后，会在下次同步时创建[!DNL Commerce]顺序。

## 禁用订单导入

如果您不想在[!DNL Commerce]中导入和管理Amazon订单，可以将[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)设置更改为`Disabled`。 此设置表示从Amazon接收新订单时，不会创建相应的[!DNL Commerce]订单。

禁用后，从Amazon收到的订单信息将显示在存储仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分和_[!UICONTROL All Orders]_&#x200B;视图中。 此订单信息仅供查看，您必须在[!DNL Amazon Seller Central]中管理这些订单。 要在[!DNL Amazon Seller Central]中打开订单详细信息，请单击&#x200B;_[!UICONTROL Order Number]_列中的Amazon订单编号。

另请参阅[查看Amazon订单](./amazon-orders-all.md)、[查看Amazon订单详细信息](./amazon-order-details.md)和[常见订单处理任务](./common-order-processing.md)。
