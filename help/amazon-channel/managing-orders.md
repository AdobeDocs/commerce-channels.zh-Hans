---
title: 管理Amazon订单
description: 您可以在订单设置中启用订单导入，以便更轻松地从商务管理员那里管理Amazon订单。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# 管理Amazon订单

您可以查看从Amazon接收到的Amazon订单信息，这些信息位于 _[!UICONTROL Recent Orders]_部分 [存储仪表板](./amazon-store-dashboard.md) 或位于_[!UICONTROL Amazon orders]_ 页面(也称为 _[!UICONTROL All Orders]_视图)。

如何管理Amazon订单取决于您的订单导入是启用还是禁用 [订单设置](./order-settings.md#configure-order-settings).

## 启用了订单导入

晚于 [存储集成](./store-integration.md)，则 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 设置是 `Enabled` 默认情况下。 对于此设置，与 [!DNL Commerce] 订单是为您的Amazon订单创建的，并且可以在以下位置进行管理： [[!DNL Commerce] 订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) 工作流。

>[!NOTE]
>
>无论您的订单导入设置如何，您现有的Amazon订单 [!DNL Amazon Seller Central] 之前的帐户 [存储集成](./store-integration.md) 未导入。

导入的Amazon订单在 [[!DNL Commerce] 订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) 工作流，就像您的其他工作流 [!DNL Commerce] 商店。 单击中的Amazon订单号 *[!UICONTROL Order Number]* 列以打开中的订单 [[!DNL Commerce] 订购流程](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). 参见 [查看Amazon订单](./amazon-orders-all.md).

### 订单导入流程

在Amazon上下达订单时， [订单导入](./order-settings.md) 启用后，将开始以下进程。

| 更改 | 操作 |
|---|---|
| 在Amazon上下达了订单。 | <ul><li>Amazon将订单状态设置为 `Pending`.</li><li>订单信息发送至 [!DNL Commerce].</li><li>订单已添加至 [_Amazon订单_ 表](./amazon-orders-all.md) 带有 `Pending` 状态。</li></ul> |
| Amazon将订单状态更改为 `Unshipped`. | <ul><li>状态更改将发送至 [!DNL Commerce].</li><li>在 [_Amazon订单_ 表](./amazon-orders-all.md)，订单状态将更改为 `Unshipped`.</li><li>在 [[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)，相应 [!DNL Commerce] 订单是使用 `Processing` 状态。</li></ul> |
| In [[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)，则 [!DNL Commerce] 订单已处理，状态将更改为 `Shipped`. | <ul><li>在 [_Amazon订单_ 表](./amazon-orders-all.md)，订单状态将更改为 `Shipped`.</li><li>在下一个cron作业中，订单状态将更改为 `Complete` 在 [[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### 订单创建阻止程序

有一些场景会阻止创建对应的 [!DNL Commerce] 订购。 [!DNL Commerce] 当出现以下任何问题时，不会为收到的订单创建订单。

| 方案 | 解决方案 |
|---|---|
| 此项目不存在于 [!DNL Commerce] 目录。 | [创建产品](./creating-assigning-catalog-products.md) 在您的 [!DNL Commerce] 目录和 [手动匹配](./creating-assigning-catalog-products.md) 它对应到产品。 |
| 目录中的项目已禁用。 | 确保 [产品状态](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) 已启用。 |
| 订购的物料缺货。 | 更新或配置 [产品选项](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) 用于数量和来源。 |

当无法导入订单时，屏幕顶部会显示类似于以下内容的系统消息：

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

问题解决后， [!DNL Commerce] 在下次同步时创建订单。

## 禁用订单导入

如果您不想在中导入和管理Amazon订单 [!DNL Commerce]，您可以更改 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 将设置为 `Disabled`. 此设置表示从Amazon收到新订单时，将 [!DNL Commerce] 不创建订单。

禁用后，从Amazon收到的订单信息将显示在 _[!UICONTROL Recent Orders]_区段和_[!UICONTROL All Orders]_ 视图。 此订单信息仅供查看，您必须在以下位置管理这些订单 [!DNL Amazon Seller Central]. 要在中打开订单详细信息，请执行以下操作 [!DNL Amazon Seller Central]中，单击Amazon订单号 _[!UICONTROL Order Number]_列。

另请参阅 [查看Amazon订单](./amazon-orders-all.md)， [查看Amazon订单详细信息](./amazon-order-details.md)、和 [常见订单处理任务](./common-order-processing.md).
