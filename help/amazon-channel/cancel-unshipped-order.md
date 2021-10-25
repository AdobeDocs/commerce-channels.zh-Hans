---
title: 取消未发运订单
description: 通过您的Amazon取消待定或部分发运（未发运）订单 [!DNL Seller Central] 帐户。
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# 取消未发运订单

Amazon订单仅在位于 `Unshipped` 状态。 如果订单待定或部分发运（未发运），则只能通过 [!DNL Amazon Seller Central] 帐户。 如果该物料已发运，则还必须在 [!DNL Amazon Seller Central] 帐户。

>[!NOTE]
>
>对于除取消订单以外的任务：
>
>- 如果 [订单导入](./order-settings.md) 启用，则订单在 [[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}。
>- 如果 [订单导入](./order-settings.md) 已禁用，则必须在 [!DNL Amazon Seller Central].


## 在 `Unshipped` 状态

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在 _[!UICONTROL Recent Orders]_，单击订单号。

   的 _[!UICONTROL Amazon Order Details]_页面。

1. 单击 **[!UICONTROL Cancel Order]** 标题栏中。

   此选项仅对 `Unshipped` 状态。

1. 对于 **[!UICONTROL Reason for cancellation]**，选择一个选项。

1. 单击 **[!UICONTROL Confirm]**.

   订单被取消，状态更新为 `Canceled` 在订单详细信息中。

取消通知将发送到您的 [!DNL Amazon Seller Central] 帐户，并且还会通知与订单关联的客户。 对应的 [!DNL Commerce] 顺序（如果有）更改为 `Complete`.
