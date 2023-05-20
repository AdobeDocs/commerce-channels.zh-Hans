---
title: 對應出貨承運商
description: '對應屬性以符合[DNL！ Commerce]產品至現有 [!DNL Walmart Marketplace] 清單和同步資料 [!DNL Channel Manager] 和 [!DNL Walmart].'
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# 對應出貨承運商

在您之前 [處理訂單出貨](process-orders.md#ship-an-order) 的 [!DNL Walmart Marketplace] 訂單，將Walmart偏好的運送公司對應至中的對應承運商 [!DNL Commerce] 以便同步運送資料 [!DNL Walmart] 和 [!DNL Commerce].

未對應至偏好電信業者的商業電信業者會標示為 *[!UICONTROL Other Carrier]* 於 [!DNL Walmart].

**必要條件**

在對映出貨承運商之前，請完成下列作業：

1. 檢閱 [準時交貨的承運商方法與運送最佳實務](https://sellerhelp.walmart.com/s/guide?article=000009473) 的 [!DNL Walmart Marketplace].

1. 驗證 [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) 和 [[!UICONTROL Shipping Settings]](https://docs.magento.com/user-guide/configuration/sales/shipping-settings.html) 設定於 [!DNL Commerce] 存放區以確保您已針對最佳化設定 [!DNL Walmart Marketplace sales].

## 對應出貨承運商

1. 從 **[!UICONTROL Listings]** 或 **[!UICONTROL Orders]** 頁面，選取 **[!UICONTROL Channel Settings]**.

1. 開啟 **[!UICONTROL Channel Settings]**，選取 **[!UICONTROL Shipping Carriers]**.

   ![對應出貨承運商](assets/map-shipping-carriers.png)

1. 針對每個 [!DNL Walmart] 列出偏好的電信業者，選取 [!DNL Commerce] 如果電信業者可用，則從下拉式清單中選取電信業者名稱。

1. 選取 **[!UICONTROL Save]** 以套用組態。

