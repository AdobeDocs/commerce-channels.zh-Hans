---
title: 常见订单处理任务
description: 使用相应的 [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] 管理员。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# 常见订单处理任务

[[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}可以管理您的Amazon订单，包括向买方发送电子邮件、执行订单（发运）、发放信用证/退款、添加评论等。要管理Amazon订单，必须将&#x200B;[**导入Amazon订单**](./order-settings.md)&#x200B;设置设置为`Enabled`，以便在收到Amazon订单时创建相应的[!DNL Commerce]订单。 Amazon订单信息显示在商店仪表板的&#x200B;*[!UICONTROL Recent Orders]*&#x200B;部分。

启用后，将为Amazon订单创建相应的[!DNL Commerce]订单，并且Amazon订单编号显示在&#x200B;_[!UICONTROL Order Number]_列中。 如果创建了相应的[!DNL Commerce]顺序，请单击顺序号以在[!DNL Commerce] [顺序处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}页面中打开顺序。 您可以像处理其他[[!DNL Commerce] 订单处理一样管理订单](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}。

[!DNL Commerce]订单编号不显示，其中包含&#x200B;_[!UICONTROL Recent Orders]_信息。 [!DNL Commerce]订单编号仅在您单击商店仪表板上的订单编号并在[[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}中打开订单时显示。 查看[!DNL Commerce]顺序时，“Amazon订单号”显示在&#x200B;*[!UICONTROL Payment & Shipping Method]*部分。 它还包含&#x200B;*[!UICONTROL View or Cancel Amazon Order]*和&#x200B;*[!UICONTROL View all Amazon Orders]*选项，具体取决于订单发运状态。

请参阅[取消未发运订单](./cancel-unshipped-order.md)。

![Amazon商务订单中的订单信息](assets/amazon-order-number-payment-info.png)

处理Amazon订单时，Amazon销售渠道会更新订单信息，并将其与您的[!DNL Amazon Seller Central]帐户同步。 您的开关设置决定了在Amazon和Amazon销售渠道之间同步订单信息的频率。

常见[!DNL Commerce] [顺序处理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}任务包括：

- [订单操作](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [订单搜索](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [处理顺序](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [查看顺序](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [处理顺序](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [订单和帐户信息](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [地址信息](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [付款和装运方法](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [查看排序的项](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [发放点数/退款](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [正在执行/发送订单](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [创建发票](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [取消未发运订单](./cancel-unshipped-order.md)

>[!NOTE]
>
>如果订单处于`Unshipped`状态，则可以在[[!UICONTROL Amazon Order Details]](./amazon-order-details.md)页面上[取消Amazon订单](./cancel-unshipped-order.md)。 如果订单已发运，则无法取消。

请参阅[Commerce Order Management](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}。
