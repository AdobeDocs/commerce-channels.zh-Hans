---
title: 取消未发运订单
description: 通过您的Amazon [!DNL Seller Central] 帐户取消待定或部分发运（未发运）订单。
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# 取消未发运订单

Amazon订单只有处于`Unshipped`状态时才可取消。 如果订单待定或部分发运（未发运），则只能通过您的[!DNL Amazon Seller Central]帐户取消订单。 如果该物料已发运，则还必须在[!DNL Amazon Seller Central]帐户中处理退货和兑换。

>[!NOTE]
>
>对于除取消订单以外的任务：
>
>- 如果启用了[订单导入](./order-settings.md)，则在[[!DNL Commerce] 订单工作流](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}中管理订单。
>- 如果[订单导入](./order-settings.md)处于禁用状态，则必须在[!DNL Amazon Seller Central]中管理订单。


## 取消`Unshipped`状态的订单

1. 单击存储卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在存储仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分，单击订单号。

   此时将显示&#x200B;_[!UICONTROL Amazon Order Details]_页面。

1. 单击标题栏中的&#x200B;**[!UICONTROL Cancel Order]**。

   此选项仅对处于`Unshipped`状态的订单显示。

1. 对于&#x200B;**[!UICONTROL Reason for cancellation]**，选择一个选项。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

   订单被取消，订单详细信息中的状态将更新为`Canceled`。

取消通知将发送到您的[!DNL Amazon Seller Central]帐户，并且与订单关联的客户也会收到通知。 相应[!DNL Commerce]顺序的状态（如果有）更改为`Complete`。
