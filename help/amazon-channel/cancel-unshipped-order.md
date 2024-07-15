---
title: 取消未发运的Amazon订单
description: 通过您的Amazon [!DNL Seller Central] 帐户取消待处理或部分发运（未发运）的订单。
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# 取消未发运的Amazon订单

Amazon订单处于`Unshipped`状态时才能取消。 如果订单待处理或部分发运（未发运），则只能通过您的[!DNL Amazon Seller Central]帐户取消该订单。 如果项目已发货，则还必须在您的[!DNL Amazon Seller Central]帐户中处理退货和交换。

>[!NOTE]
>
>对于取消订单以外的任务：
>
>- 如果您启用了[订单导入](./order-settings.md)，则在[[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)中管理订单。
>- 如果[订单导入](./order-settings.md)被禁用，您必须在[!DNL Amazon Seller Central]中管理您的订单。

## 取消处于`Unshipped`状态的订单

1. 单击商店信息卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分中，单击订单编号。

   此时会显示&#x200B;_[!UICONTROL Amazon Order Details]_页面。

1. 单击标题栏中的&#x200B;**[!UICONTROL Cancel Order]**。

   此选项仅对处于`Unshipped`状态的订单显示。

1. 为&#x200B;**[!UICONTROL Reason for cancellation]**&#x200B;选择一个选项。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

   订单已取消，订单详细信息中的状态更新为`Canceled`。

取消通知将发送到您的[!DNL Amazon Seller Central]帐户，并且还将通知与订单关联的客户。 相应的[!DNL Commerce]订单的状态（如果有）更改为`Complete`。
