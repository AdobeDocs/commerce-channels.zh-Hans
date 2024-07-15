---
title: 管理Amazon订单
description: 您可以在订单设置中启用订单导入，以便更轻松地从Commerce管理员那里管理Amazon订单。
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# 管理Amazon订单

您可以查看从Amazon接收的Amazon订单信息，该信息位于[存储仪表板](./amazon-store-dashboard.md)的&#x200B;_[!UICONTROL Recent Orders]_部分或_[!UICONTROL Amazon orders]_&#x200B;页面上（也称为&#x200B;_[!UICONTROL All Orders]_视图）。

如何管理Amazon订单取决于您的[订单设置](./order-settings.md#configure-order-settings)中是启用还是禁用了订单导入。

## 启用了订单导入

在[存储集成](./store-integration.md)之后，[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)设置默认为`Enabled`。 通过此设置，可为您的Amazon订单创建相应的[!DNL Commerce]订单，并可在[[!DNL Commerce] 订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作流中进行管理。

>[!NOTE]
>
>无论您的订单导入设置如何，在您的[存储集成](./store-integration.md)之前的[!DNL Amazon Seller Central]帐户中存在的Amazon订单都不会导入。

导入的Amazon订单在[[!DNL Commerce] 订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作流中进行管理，就像您的其他[!DNL Commerce]商店一样。 单击&#x200B;*[!UICONTROL Order Number]*&#x200B;列中的Amazon订单号以打开[[!DNL Commerce] 订单流程](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions)中的订单。 请参阅[查看Amazon订单](./amazon-orders-all.md)。

### 订单导入流程

在Amazon上下达订单并启用[订单导入](./order-settings.md)后，将开始以下流程。

| 更改 | 操作 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 向Amazon下达订单。 | <ul><li>Amazon将订单状态设置为`Pending`。</li><li>订单信息已发送到[!DNL Commerce]。</li><li>订单已添加到状态为`Pending`的&#x200B;[_Amazon订单_&#x200B;表](./amazon-orders-all.md)。</li></ul> |
| Amazon将订单状态更改为`Unshipped`。 | <ul><li>状态更改已发送至[!DNL Commerce]。</li><li>在&#x200B;[_Amazon订单_&#x200B;表](./amazon-orders-all.md)中，订单状态更改为`Unshipped`。</li><li>在[[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)中，已创建状态为`Processing`的相应[!DNL Commerce]订单。</li></ul> |
| 在[[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)中，已处理[!DNL Commerce]订单并且状态更改为`Shipped`。 | <ul><li>在&#x200B;[_Amazon订单_&#x200B;表](./amazon-orders-all.md)中，订单状态更改为`Shipped`。</li><li>在下一个cron作业中，[[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)中的订单状态将更改为`Complete`。</li></ul> |

### 订单创建阻止程序

有一些情况会阻止创建相应的[!DNL Commerce]订单。 当出现以下任何问题时，不会为收到的订单创建[!DNL Commerce]订单。

| 方案 | 解决方案 |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!DNL Commerce]目录中不存在该项。 | [在您的[!DNL Commerce]目录中创建产品](./creating-assigning-catalog-products.md)，然后[手动将](./creating-assigning-catalog-products.md)产品与产品匹配。 |
| 目录中的项目已禁用。 | 确保已启用[产品状态](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html)。 |
| 所订购的物料缺货。 | 为数量和源更新或配置[产品选项](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html)。 |

当无法导入订单时，屏幕顶部会显示与以下内容类似的系统消息：

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

问题解决后，将在下次同步时创建[!DNL Commerce]订单。

## 禁用订单导入

如果不希望在[!DNL Commerce]中导入和管理Amazon订单，可将[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)设置更改为`Disabled`。 此设置意味着从Amazon收到新订单时，不会创建相应的[!DNL Commerce]订单。

禁用后，从Amazon收到的订单信息会显示在商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分和_[!UICONTROL All Orders]_&#x200B;视图中。 此订单信息仅供查看，您必须在[!DNL Amazon Seller Central]中管理这些订单。 要在[!DNL Amazon Seller Central]中打开订单详细信息，请单击&#x200B;_[!UICONTROL Order Number]_列中的Amazon订单号。

另请参阅[查看Amazon订单](./amazon-orders-all.md)、[查看Amazon订单详细信息](./amazon-order-details.md)和[常见订单处理任务](./common-order-processing.md)。
