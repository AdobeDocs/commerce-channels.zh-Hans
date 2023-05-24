---
title: Amazon订单详细信息
description: 在Adobe Commerce或Magento Open Source管理员中查看您的Amazon Marketplace订单的详细信息。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon订单详细信息

![Amazon订单详细信息](assets/amazon-order-details-header.png)

## 查看Amazon订单详细信息

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在 _[!UICONTROL Recent Orders]_部分，单击订单编号。

   此 _[!UICONTROL Amazon Order Details]_页面打开。

>[!NOTE]
>
>如果您在中启用了订单导入，则 [订单设置](./order-settings.md) 顺序是 [由Amazon(FBA)履行](./fulfilled-by.md)，您可能会在订单详细信息中看到某些字段的虚数据。 Amazon不会为FBA订单发送以下数据。
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

此 _[!UICONTROL Order and Shipping Details]_选项卡显示从Amazon收到的详细订单信息。

>[!IMPORTANT]
>
>Amazon接受无法导入到Amazon sales channel中的非标准地址信息，从而阻止某些订单的州/国家/地区代码正确更新。 要更正地址错误，订单详细信息中的以下字段可编辑：
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

![订单和送货详细信息](assets/amazon-order-details.png)

### “订单项”选项卡

此 _[!UICONTROL Order Items]_选项卡显示从Amazon收到的与Amazon订单关联的所有项目。

![订单项目详细信息](assets/amazon-order-item-details.png)

### “跟踪”选项卡

此 _[!UICONTROL Tracking]_选项卡显示与Amazon订单关联的跟踪信息。

![跟踪详细信息](assets/amazon-order-tracking-details.png)
