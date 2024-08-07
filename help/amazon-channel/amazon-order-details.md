---
title: Amazon订单详细信息
description: 在Adobe Commerce或Magento Open Source管理员中查看您的Amazon Marketplace订单的详细信息。
feature: Sales Channels, Orders
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon订单详细信息

![Amazon订单详细信息](assets/amazon-order-details-header.png){width="600" zoomable="yes"}

## 查看Amazon订单详细信息

1. 单击商店信息卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在&#x200B;_[!UICONTROL Recent Orders]_部分中，单击订单编号。

   将打开&#x200B;_[!UICONTROL Amazon Order Details]_页面。

>[!NOTE]
>
>如果您在[订单设置](./order-settings.md)中启用了订单导入，并且订单已由Amazon (FBA)](./fulfilled-by.md)履行，则您可能会在订单详细信息中看到某些字段的虚数据。 [Amazon不会为FBA订单发送以下数据。
>
> - `AddressType`
> - `AddressLine1`
> - `AddressLine2`
> - `AddressLine3`
> - `BuyerName`
> - `Phone`
> - `PurchaseOrderNumber`
> - `RecipientName`
> - `CustomizedURL`
> - `GiftMessageText`

### “订单和发运详细信息”标签

_[!UICONTROL Order and Shipping Details]_选项卡显示从Amazon收到的详细订单信息。

>[!IMPORTANT]
>
>Amazon接受无法导入Amazon sales channel的非标准地址信息，因此导致某些订单的州/国家/地区代码无法正确更新。 要更正地址错误，订单详细信息中的以下字段可编辑：
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>进行编辑后，不要忘记单击&#x200B;**保存订单**。

![订单和送货详细信息](assets/amazon-order-details.png){width="600" zoomable="yes"}

### “订单项目”选项卡

_[!UICONTROL Order Items]_选项卡显示从Amazon接收的、与Amazon订单关联的所有项目。

![订单项详细信息](assets/amazon-order-item-details.png){width="600" zoomable="yes"}

### “跟踪”选项卡

_[!UICONTROL Tracking]_选项卡显示与Amazon订单关联的跟踪信息。

![跟踪详细信息](assets/amazon-order-tracking-details.png){width="600" zoomable="yes"}
