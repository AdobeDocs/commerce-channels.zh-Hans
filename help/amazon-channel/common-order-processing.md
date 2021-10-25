---
title: 常见订单处理任务
description: 使用对应的 [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] 管理员。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# 常见订单处理任务

[[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}可以管理您的Amazon订单，包括向买方发送电子邮件、执行订单（发运）、发放信用证/退款、添加评论等。 要管理Amazon订单，请 [**导入Amazon订单**](./order-settings.md) 设置必须设置为 `Enabled` 这样对应 [!DNL Commerce] 在收到Amazon订单时会创建订单。 Amazon订单信息显示在 *[!UICONTROL Recent Orders]* 区域。

启用后，对应 [!DNL Commerce] 为Amazon订单创建订单，Amazon订单编号显示在 _[!UICONTROL Order Number]_列。 如果对应 [!DNL Commerce] 订单，单击订单编号以在 [!DNL Commerce] [订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}页。 您可以像管理其他 [[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}。

的 [!DNL Commerce] 订单编号不显示 _[!UICONTROL Recent Orders]_信息。 的 [!DNL Commerce] 订单编号仅在您单击商店仪表板上的订单编号并在 [[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}。 查看 [!DNL Commerce] 订单中，Amazon订单编号显示在&#x200B;*[!UICONTROL Payment & Shipping Method]*中。 此外，它还包含&#x200B;*[!UICONTROL View or Cancel Amazon Order]*和&#x200B;*[!UICONTROL View all Amazon Orders]*，具体取决于订单发运状态。

请参阅 [取消未发运订单](./cancel-unshipped-order.md).

![Amazon商务订单中的订单信息](assets/amazon-order-number-payment-info.png)

在处理Amazon订单时，Amazon销售渠道会更新订单信息，并将其与 [!DNL Amazon Seller Central] 帐户。 您的开关设置决定了在Amazon和Amazon销售渠道之间同步订单信息的频率。

常用 [!DNL Commerce] [订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}项任务包括：

- [订单操作](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [订单搜索](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [处理订单](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [查看订单](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [处理订单](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [订单和帐户信息](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [地址信息](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [付款和发运方法](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [审核订购的项目](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [发放贷项/退款](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [履行/发运订单](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [创建发票](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [取消未发运订单](./cancel-unshipped-order.md)

>[!NOTE]
>
>如果订单在 `Unshipped` 状态，您可以 [取消Amazon订单](./cancel-unshipped-order.md) 在 [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) 页面。 如果订单已发运，则无法取消。

请参阅 [商务订单管理](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}。
