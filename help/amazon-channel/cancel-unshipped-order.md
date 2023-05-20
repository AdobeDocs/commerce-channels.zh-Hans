---
title: 取消未出貨的訂單
description: 透過您的Amazon取消擱置或部份出貨（未出貨）的訂單 [!DNL Seller Central] 帳戶。
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# 取消未出貨的訂單

Amazon訂單位於以下位置時，才能取消： `Unshipped` 狀態。 如果訂單為暫緩或部份出貨（未出貨），則訂單只能透過您的 [!DNL Amazon Seller Central] 帳戶。 若此料號已出貨，您也必須使用下列方式處理退貨與交換： [!DNL Amazon Seller Central] 帳戶。

>[!NOTE]
>
>對於取消訂單以外的工作：
>
>- 如果您有 [訂單匯入](./order-settings.md) 已啟用，訂單管理於 [[!DNL Commerce] 訂單工作流程](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.
>- 若 [訂單匯入](./order-settings.md) 已停用，您必須在以下位置管理訂單： [!DNL Amazon Seller Central].


## 取消中的訂單 `Unshipped` 狀態

1. 按一下 **[!UICONTROL View Store]** 在商店資訊卡上。

1. 在 _[!UICONTROL Recent Orders]_區段內，按一下訂單編號。

   此 _[!UICONTROL Amazon Order Details]_頁面便會顯示。

1. 按一下 **[!UICONTROL Cancel Order]** 標題列中的。

   此選項僅對中的訂單顯示 `Unshipped` 狀態。

1. 對象 **[!UICONTROL Reason for cancellation]**，選擇一個選項。

1. 按一下 **[!UICONTROL Confirm]**.

   訂單已取消，且狀態已更新為 `Canceled` 訂單詳細資料。

取消通知已傳送至您的 [!DNL Amazon Seller Central] 帳戶以及與訂單相關聯的客戶也會收到通知。 對應專案的狀態 [!DNL Commerce] 訂單（若有）變更至 `Complete`.
