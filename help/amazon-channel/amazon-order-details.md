---
title: Amazon訂單詳細資料
description: 在Adobe Commerce或Magento Open Source管理員中檢視您Amazon Marketplace訂單的詳細資料。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon訂單詳細資料

![Amazon訂單詳細資料](assets/amazon-order-details-header.png)

## 檢視Amazon訂單詳細資料

1. 按一下 **[!UICONTROL View Store]** 在商店資訊卡上。

1. 在 _[!UICONTROL Recent Orders]_區段，按一下訂單編號。

   此 _[!UICONTROL Amazon Order Details]_頁面隨即開啟。

>[!NOTE]
>
>如果您已在以下專案中啟用訂單匯入： [訂單設定](./order-settings.md) 順序為 [由Amazon (FBA)履行](./fulfilled-by.md)，您可能會在訂單詳細資料中看到某些欄位的虛擬資料。 Amazon不會針對FBA訂單傳送下列資料。
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


### 訂單與出貨明細頁標

此 _[!UICONTROL Order and Shipping Details]_標籤會顯示從Amazon收到的詳細訂單資訊。

>[!IMPORTANT]
>
>Amazon接受無法匯入Amazon sales channel的非標準地址資訊，因此導致某些訂單的州/國家/地區代碼無法正確更新。 若要更正地址錯誤，可在訂單詳細資料中編輯下列欄位：
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>別忘了按一下 **儲存訂單** 編輯之後。

![訂單與送貨詳細資料](assets/amazon-order-details.png)

### 訂單專案頁標

此 _[!UICONTROL Order Items]_索引標籤會顯示從Amazon收到的與Amazon訂單相關聯的所有專案。

![訂單料號明細](assets/amazon-order-item-details.png)

### 「追蹤」標籤

此 _[!UICONTROL Tracking]_索引標籤會顯示與Amazon訂單相關聯的追蹤資訊。

![追蹤詳細資料](assets/amazon-order-tracking-details.png)
