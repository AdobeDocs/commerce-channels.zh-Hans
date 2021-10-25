---
title: Amazon订单详细信息
description: 在Adobe Commerce或Magento Open Source管理员中查看Amazon Marketplace订单的详细信息。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon订单详细信息

![Amazon订单详细信息](assets/amazon-order-details-header.png)

## 查看Amazon订单详细信息

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在 _[!UICONTROL Recent Orders]_，单击订单号。

   的 _[!UICONTROL Amazon Order Details]_页面。

>[!NOTE]
>
>如果您在 [订单设置](./order-settings.md) 顺序是 [由Amazon(FBA)履行](./fulfilled-by.md)，则可能会在订单详细信息中看到某些字段的虚拟数据。 Amazon不会发送FBA订单的以下数据。
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

的 _[!UICONTROL Order and Shipping Details]_选项卡中显示从Amazon收到的详细订单信息。

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
>不要忘记单击 **保存顺序** 进行编辑之后。

![订单和发运详细信息](assets/amazon-order-details.png)

### “订单项目”选项卡

的 _[!UICONTROL Order Items]_选项卡显示从Amazon收到的与Amazon订单关联的所有项目。

![订单项目详细信息](assets/amazon-order-item-details.png)

### “跟踪”选项卡

的 _[!UICONTROL Tracking]_选项卡显示与Amazon订单关联的跟踪信息。

![跟踪详细信息](assets/amazon-order-tracking-details.png)
