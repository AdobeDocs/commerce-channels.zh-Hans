---
title: 常见订单处理任务
description: 使用相应的 [!DNL Commerce] 为Amazon订单创建的订单，用于管理订单活动和处理 [!UICONTROL Commerce] 管理员。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 常见订单处理任务

[[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} 可以管理您的Amazon订单，包括向买方发送电子邮件、履行订单（发运）、发放贷项/退款、添加注释等。 要管理Amazon订单，请 [**导入Amazon订单**](./order-settings.md) 设置必须设置为 `Enabled` 因此相应 [!DNL Commerce] 在收到Amazon订单时创建订单。 Amazon订单信息显示在 *[!UICONTROL Recent Orders]* 区段。

启用时，相应 [!DNL Commerce] 系统会为Amazon订单创建订单，Amazon订单编号将显示在 _[!UICONTROL Order Number]_列。 如果 [!DNL Commerce] 创建订单后，单击订单编号以打开 [!DNL Commerce] [订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} page. You can manage the order as you do your other [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

此 [!DNL Commerce] 订单编号不显示 _[!UICONTROL Recent Orders]_信息。 此 [!DNL Commerce] 订单编号仅在您单击商店仪表板上的订单编号并在以下位置打开订单时显示： [[!DNL Commerce] 订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}. 查看 [!DNL Commerce] 订单编号，Amazon订单编号将显示在&#x200B;*[!UICONTROL Payment & Shipping Method]*部分。 此外，还包含以下选项：*[!UICONTROL View or Cancel Amazon Order]*和&#x200B;*[!UICONTROL View all Amazon Orders]*，具体取决于订单配送状态。

参见 [取消未发运的订单](./cancel-unshipped-order.md).

![商务订单中的Amazon订单信息](assets/amazon-order-number-payment-info.png)

在处理Amazon订单时，Amazon销售渠道会更新订单信息，并将其与您的 [!DNL Amazon Seller Central] 帐户。 您的cron设置决定了订单信息在Amazon和Amazon Sales Channel之间同步的频率。

公共 [!DNL Commerce] [订单处理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} 这些任务包括：

- [订购操作](https://docs.magento.com/user-guide/sales/order-actions.html){target="_blank"}
- [订单搜索](https://docs.magento.com/user-guide/sales/orders-search.html){target="_blank"}
- [处理订单](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}
   - [查看订单](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target="_blank"}
   - [处理订单](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target="_blank"}
   - [订单和帐户信息](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target="_blank"}
   - [地址信息](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target="_blank"}
   - [付款和配送方式](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target="_blank"}
   - [查看已订购的项目](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target="_blank"}
- [签发贷项/退款](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target="_blank"}
- [履行/发运订单](https://docs.magento.com/user-guide/sales/shipments-create.html){target="_blank"}
- [创建发票](https://docs.magento.com/user-guide/sales/invoice-create.html){target="_blank"}
- [取消未发运的订单](./cancel-unshipped-order.md)

>[!NOTE]
>
>如果订单位于 `Unshipped` 状态，您可以 [取消Amazon订单](./cancel-unshipped-order.md) 在 [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) 页面。 如果订单已发运，则无法取消。

参见 [商务订单管理](https://docs.magento.com/user-guide/sales/order-management.html){target="_blank"}.
