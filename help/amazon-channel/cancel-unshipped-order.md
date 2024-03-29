---
title: 取消未发运的Amazon订单
description: 通过您的Amazon取消待定或部分发运（未发运）的订单 [!DNL Seller Central] 帐户。
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# 取消未发运的Amazon订单

仅当Amazon订单位于 `Unshipped` 状态。 如果订单处于待定状态或部分发运（未发运），则只能通过 [!DNL Amazon Seller Central] 帐户。 如果项目已发货，您还必须在 [!DNL Amazon Seller Central] 帐户。

>[!NOTE]
>
>对于取消订单以外的任务：
>
>- 如果您拥有 [订单导入](./order-settings.md) 启用，订单在 [[!DNL Commerce] 订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- 如果 [订单导入](./order-settings.md) 禁用，您必须在 [!DNL Amazon Seller Central].

## 取消中的订单 `Unshipped` 状态

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在 _[!UICONTROL Recent Orders]_，请单击订单号。

   此 _[!UICONTROL Amazon Order Details]_页面。

1. 单击 **[!UICONTROL Cancel Order]** 标题栏中。

   此选项仅对中的订单显示 `Unshipped` 状态。

1. 对象 **[!UICONTROL Reason for cancellation]**，选择一个选项。

1. 单击 **[!UICONTROL Confirm]**.

   订单已取消，且状态已更新为 `Canceled` 订单详细信息。

取消通知将发送至 [!DNL Amazon Seller Central] 另外，也会通知与订单关联的客户。 对应的状态 [!DNL Commerce] 订单（如果有）更改 `Complete`.
