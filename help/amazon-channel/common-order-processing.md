---
title: 常见Amazon订单处理任务
description: 使用相应的 [!DNL Commerce] 为Amazon订单创建的订单，用于管理订单活动和处理 [!UICONTROL Commerce] 管理员。
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# 常见Amazon订单处理任务

[商务订单处理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) 可以管理Amazon订单，包括向买方发送电子邮件、履行订单（发运）、发放贷项/退款、添加注释等。 要管理Amazon订单，请 [**导入Amazon订单**](./order-settings.md) 设置必须设置为 `Enabled` 因此相应 [!DNL Commerce] 在收到Amazon订单时创建订单。 Amazon订单信息显示在 *[!UICONTROL Recent Orders]* 区段。

启用时，相应 [!DNL Commerce] 系统会为Amazon订单创建订单，Amazon订单编号将显示在 _[!UICONTROL Order Number]_列。 如果 [!DNL Commerce] 创建订单后，单击订单编号以在 [商务订单处理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) 页面。 您可以像管理其他订单一样管理订单 [[!DNL Commerce] 订单处理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

此 [!DNL Commerce] 订单编号不显示在 _[!UICONTROL Recent Orders]_信息。 仅当您单击商店仪表板上的订单编号并在以下位置打开订单时，才会显示商务订单编号： [商务订单处理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). 查看 [!DNL Commerce] 订单，Amazon订单编号将显示在&#x200B;*[!UICONTROL Payment & Shipping Method]*部分。 它还包含用于&#x200B;*[!UICONTROL View or Cancel Amazon Order]*和&#x200B;*[!UICONTROL View all Amazon Orders]*，具体取决于订单配送状态。

请参阅 [取消未发运的订单](./cancel-unshipped-order.md).

![Commerce订单中的Amazon订单信息](assets/amazon-order-number-payment-info.png){width="500"}

在处理Amazon订单时，Amazon销售渠道会更新订单信息，并将其与您的 [!DNL Amazon Seller Central] 帐户。 您的cron设置决定了订单信息在Amazon和Amazon Sales Channel之间同步的频率。

通用商务 [订单处理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) 这些任务包括：

- [订购操作](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [订单搜索](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [处理订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [查看订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [处理订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [订单和帐户信息](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [地址信息](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [付款和配送方式](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [查看订购的项目](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [发放贷项/退款](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [完成/发运订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [创建发票](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [取消未发运的订单](./cancel-unshipped-order.md)

>[!NOTE]
>
>如果订单位于 `Unshipped` 状态，您可以 [取消Amazon订单](./cancel-unshipped-order.md) 在 [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) 页面。 如果订单已发运，则无法取消该订单。

请参阅 [Commerce订单管理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
