---
title: Amazon订单详细信息
description: 在“Amazon商务”或“Magento Open Source管理员”中查看您的Adobe Marketplace订单的详细信息。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon订单详细信息

![Amazon订单详细信息](assets/amazon-order-details-header.png)

## 查看Amazon订单详细信息

1. 单击存储卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在&#x200B;_[!UICONTROL Recent Orders]_部分中，单击订单号。

   将打开&#x200B;_[!UICONTROL Amazon Order Details]_页面。

>[!NOTE]
>
>如果在[订单设置](./order-settings.md)中启用了订单导入，并且订单由Amazon(FBA)](./fulfilled-by.md)履行，则订单详细信息中可能会看到某些字段的虚拟数据。 [Amazon不会发送FBA订单的以下数据。
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


### “订单和发运详细信息”选项卡

_[!UICONTROL Order and Shipping Details]_选项卡显示从Amazon收到的详细订单信息。

>[!IMPORTANT]
>
>Amazon接受无法导入Amazon销售渠道的非标准地址信息，从而阻止某些订单的状态/国家/地区代码正确更新。 要更正地址错误，可在顺序详细信息中编辑以下字段：
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>编辑后，请勿忘记单击&#x200B;**保存顺序**。

![订单和发运详细信息](assets/amazon-order-details.png)

### “订单项目”选项卡

_[!UICONTROL Order Items]_选项卡显示从Amazon收到的与Amazon订单关联的所有项目。

![订单项目详细信息](assets/amazon-order-item-details.png)

### “跟踪”选项卡

_[!UICONTROL Tracking]_选项卡显示与Amazon顺序关联的跟踪信息。

![跟踪详细信息](assets/amazon-order-tracking-details.png)
