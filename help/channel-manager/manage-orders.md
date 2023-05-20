---
title: 檢視和管理訂單，從 [!DNL Channel Manager]'
description: '檢視和管理 [!DNL Walmart Marketplace] 訂單 [!DNL Channel Manager] 適用於Adobe Commerce和Magento Open Source。'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# 檢視與追蹤訂單，從 [!DNL Channel Manager]

[!DNL Walmart Marketplace] 訂單資料 [!DNL Commerce] 產品會自動同步至 [!DNL Channel Manager] 晚於 [!DNL Walmart] 處理訂單。

於 [!DNL Commerce] 成功同步處理會觸發下列動作：

- [!DNL Channel Manager] 傳送訂單確認函給沃爾瑪。

- 對應的 [!DNL Commerce] 訂單是從Walmart訂單建立的。

- 更新的訂單資訊會顯示在 [!DNL Channel Manager] 訂單儀表板。

在店面管理員中，您可以檢視訂單資料來源 [!DNL Channel Manager] 透過開啟sales channel商店並選取 **[!UICONTROL Orders]**.

![要管理的管道管理員訂單檢視 [!DNL Walmart Marketplace] 訂購](assets/orders-dashboard-view.png)

>[!NOTE]
>
>最長可能需要35分鐘 [!DNL Walmart Marketplace] 以便在以下專案顯示： [!DNL Channel Manager] 訂單清單。 [!DNL Walmart] 大約需要30分鐘來處理傳入的訂單並將它們傳送到 [!DNL Channel Manager]. Channel Manager收到訂單後，需要約五分鐘才能在Adobe Commerce或Magento Open Source中建立並顯示訂單。

## 訂單控制項與欄位說明

下清單格說明「訂單」可用的控制項與欄位。

**控制項[!UICONTROL Orders]**

<table>
<tr>
<td><strong>控制</strong></td>
<td><strong>說明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>選取其中一個選項來排序檢視 [!UICONTROL Order Status] 卡片。</td>
</tr>
<tr>
<td>狀態詳細資料</td>
<td>提供有關訂單錯誤和退貨請求的資訊。 若要檢視訂單的退貨資訊與退款狀態，請選取 <strong>[!UICONTROL Return requested]</strong> 文字以開啟 [!UICONTROL Returns] 儀表板。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>若要檢視訂單詳細資料，請選取 [!DNL Commerce] 中的訂單編號 [!UICONTROL Order] 表格。 然後，使用 [!DNL Commerce] 訂單選項以處理訂單。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>若要修改通道組態，請選取通道Walmart連線認證、對應的屬性或出貨識別碼，設定值請選取 [!DNL Commerce] 中的訂單編號 [!UICONTROL Order] 表格。 然後，使用 [!DNL Commerce] 訂單選項以處理訂單。</td>
</tr>
</table>


**欄說明**

<table>
<tr>
<td>欄位</td>
<td>說明</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>在中指派給訂單的採購單編號 [!DNL Walmart Marketplace]. 訂單最初匯入至時 [!DNL Channel Manager]，僅限 [!DNL Walmart] 訂單編號隨即顯示。 當 [!DNL Commerce] 建立訂單後， [!DNL Walmart] 訂單編號儲存在 [!UICONTROL External ID] 產品屬性。</td>
</tr>
<tr>
<td>[!DNL Commerce] 訂單編號</td>
<td>指派給 [!DNL Commerce] 訂單建立自 [!DNL Walmart Marketplace] 訂購。</td>
</tr>
<tr>
<td>專案</td>
<td>訂購的專案數 [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>訂購料號的總成本。</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>將訂單提交至的日期 [!DNL Walmart Marketplace] 轉換為當地時區。</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>訂單必須由哪個日期出貨才能符合 [!DNL Walmart Marketplace] 需求已轉換為當地時區。
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>訂單必須交貨給客戶才能達到的日期 [!DNL Walmart Marketplace] 需求已轉換為當地時區。</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>此[[!DNL Walmart Marketplace] 送貨方式](已針對訂單選取https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29。</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>表示上次更新訂單資料時間的時間戳記 [!DNL Channel Manager] 轉換為當地時區。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>指示中目前的訂單狀態 [!DNL Commerce] 訂單工作流程。 從匯入的訂單的初始狀態 [!DNL Walmart Marketplace] 是_Open_。 其他狀態更新會在以下情況下發生： [!DNL Commerce] 訂單已處理且 [!DNL Channel Manager] 成功將出貨、部份出貨及取消更新同步至 [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>提供有關有錯誤的訂單或退款請求的更多詳細資訊。</td>
</tr>
</table>

## 訂單狀態

[!UICONTROL Order Status] 提供目前狀態的相關資訊 [!DNL Walmart Marketplace] 從Adobe Commerce或Magento Open Source管理的訂單。 訂單狀態更新發生於 [!DNL Channel Manager] 會從以下任一位置接收更新的訂單資訊： [!DNL Walmart Marketplace] 或 [!DNL Commerce] 訂購系統。 訂單可以有以下狀態：

- **[!UICONTROL Shipped]** — 已出貨的訂單 [!DNL Commerce] 商店。 當訂單出貨時， [!DNL Channel Manager] 傳送更新至 [!DNL Walmart Marketplace] 更新「沃爾瑪」的出貨狀態，並提供出貨的訂單追蹤編號。 訂單出貨後，如果沃爾瑪簽發「退貨商品授權」表格，訂單專案可以部份或全部退款。 另請參閱 [退貨與退款](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** — 某些料號標示為已出貨，而其他料號則等待出貨的訂單。 當訂單中的料號出貨時， [!DNL Channel Manager] 傳送更新至 [!DNL Walmart Marketplace] 若要將出貨狀態更新為 _[!DNL Partially Shipped]_，並提供出貨的訂單追蹤編號。

- **[!UICONTROL Canceled]** — 已取消的訂單 [!DNL Commerce] 商店。

   訂單取消完成後， [!DNL Commerce] 庫存數量更新以反映退回的料號。 然後， [!DNL Channel Manager] 將更新同步至 [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]** — 如果Walmart Marketplace要求退回已出貨的訂單專案，則 `Return requested` 連結會顯示在 [!UICONTROL Status details] 欄。 選取連結會開啟 [!UICONTROL Returns] 儀表板，以檢視退貨及管理退款處理。

- **[!UICONTROL Error]** — 有錯誤的訂單。 訂單更新作業失敗時可能會發生錯誤。 例如，發生下列情況會發生錯誤： [!DNL Channel Manager] 無法收到沃爾瑪的新訂單。 在以下情況下也可能發生： [!DNL Channel Manager] 無法將訂單出貨或取消更新傳送至 [!DNL Walmart Marketplace]. 如果作業失敗，「訂單」頁面會顯示 _錯誤_ 訂單的狀態。 如需詳細資訊，請參閱 [修正訂單錯誤](process-orders.md#fix-shipping-and-cancellation-errors)。

- **[!UICONTROL Status details]** — 提供因遺漏資訊或無效值、不正確的出貨明細或訂單取消失敗等問題而發生訂單錯誤的詳細資訊。 說明可協助判斷 [!DNL Commerce] 執行個體或在 [!DNL Walmart Marketplace].

>[!NOTE]
>
>如果訂單料號是以多重出貨方式傳送，則訂單狀態會位於 [!DNL Channel Manager] 反映最後一個可用的訂單狀態。 例如，如果第一個料號出貨，且同步處理訂單更新時未傳回任何錯誤 [!DNL Channel Manager] 和 [!DNL Walmart Marketplace]，則 [!DNL Channel Manager] 訂單狀態為 _[!UICONTROL Partially Shipped]_. 若第二個料號已出貨，且 [!DNL Channel Manager] 傳回錯誤，訂單狀態會更新為_[!UICONTROL Error]_.

## 檢閱訂單

1. 從「管理員」中選取「 」 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 以開啟 [!UICONTROL Channel Manager Marketplace Stores] 頁面。

1. 選取商店專案列中的眼睛圖示，開啟商店檢視。

1. 若要檢視訂單資訊，請選取*[!UICONTROL *Orders]**。

1. 取得訂單的相關資訊，並核取 **[狀態](#order-status)** 欄。

## 複查訂單詳細資料

從市集收到訂單並匯入您的銷售管道商店後，請使用 [!DNL Commerce] 訂單ID可在Adobe Commerce中檢視訂單詳細資料。

從 **[!UICONTROL Orders]**，選取 **[!UICONTROL Commerce Order Number]** 以開啟 [!DNL Commerce] 訂單詳細資料。

![的商務訂單詳細資料檢視 [!DNL Walmart Marketplace] 訂購](assets/order-detail-with-external-order-id.png)

在Commerce店面，訂單匯入自 [!DNL Walmart Marketplace] 在訂單資料中包含下列額外資訊：

- **付款資訊和送貨方法** — 從Walmart匯入的訂單包含下列付款與出貨欄位的值：

   - **[!UICONTROL Offline Channel Payment]** — 指出訂單付款是由以下人員離線處理 [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** — 顯示 [!DNL Walmart Marketplace] 訂單編號。

   - **[!UICONTROL Channel Shipping - Value]** — 表示出貨費用是透過處理 [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** — 此欄位只有在訂單匯入來源時才會顯示 [!DNL Walmart Marketplace] 已取消。 取消原因包括：

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **訂購的專案** — 本節列出所有Commerce訂單上的訂單專案。 此 [!UICONTROL Qty] 欄提供訂單料號的狀態歷史記錄。 例如，如果訂單已開立商業發票、出貨及退款，您可以檢視狀態轉換。

   ![訂單明細訂購料號狀態歷史記錄 [!DNL Walmart Marketplace] 訂購](assets/order-detail-status-history.png)

選取「 」，檢視料號商業發票與退款明細 [!UICONTROL Invoice] 和 [!UICONTROL Credit Memo] 導覽功能表中的選項。 您也可以直接從以下存取銷退折讓單： [[!UICONTROL Returns]](return-refund-orders.md) 在您的sales channel store中的儀表板。
