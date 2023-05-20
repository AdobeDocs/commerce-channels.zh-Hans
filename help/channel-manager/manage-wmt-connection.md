---
title: 管理Walmart市集連線
description: '''更新API認證以授權[DNL！之間的連線 Commerce]商店檢視和 [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] 產品清單，並同步化存貨、價格、訂單和出貨資料，介於 [!DNL Commerce] 還有沃爾瑪。'
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 對應出貨承運商

在您之前 [處理訂單出貨](process-orders.md#ship-an-order) 的 [!DNL Walmart Marketplace] 訂單，將Walmart偏好的運送公司對應至中的對應承運商 [!DNL Commerce] 以便同步運送資料 [!DNL Walmart] 和 [!DNL Commerce].

未對應至偏好電信業者的商業電信業者會標示為 *[!UICONTROL Other Carrier]* 於 [!DNL Walmart].

**必要條件**

檢閱 [沃爾瑪要求](walmart-requirements.md) 的 [!DNL Marketplace Seller account].

## 更新連線認證

1. 於 [!UICONTROL Listings] 銷售管道商店的頁面，選取 **[!UICONTROL Channel Settings]**.

1. 開啟 **[!UICONTROL Channel Settings]**，選取 **[!UICONTROL Walmart Connection]**.

1. 若要修改證明資料，請選取 **[!UICONTROL Change Credentials]**

   ![更新Walmart API認證以授權連線](assets/update-connection-credentials.png)

1. 輸入 **[!UICONTROL Walmart Client ID]** 和 **[!UICONTROL Walmart Client Secret]**.

1. 選取 **[!UICONTROL Save]** 以套用組態。
