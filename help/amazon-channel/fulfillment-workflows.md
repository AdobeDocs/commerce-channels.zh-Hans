---
title: Amazon履行工作流程
description: Amazon清單中的訂單履行會遵循從訂單提交到出貨的特定順序。
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon履行工作流程

## 範例：由商家履行

| 步驟 | 說明 |
|----|----|
| 1 | **在Amazon上下達商家履行的訂單。** Amazon指派狀態 `Pending` 直到客戶信用卡資訊得到驗證為止。 中的訂單 `Pending` 狀態會自動匯入Amazon sales channel，但不會顯示在 _[!UICONTROL Orders]_標籤。 |
| 2 | **訂單已由Amazon驗證。** 驗證後，Amazon會將狀態變更為 `Unshipped`. 此狀態變更後，訂單會在Amazon銷售管道中更新，並出現在 _[!UICONTROL Orders]_標籤。 |
| 3 | **訂單詳細資訊會更新。** Amazon sales channel會以價格、客戶電子郵件和客戶名稱更新訂單詳細資料。 在此更新期間，Amazon訂單會建立對應的 [!DNL Commerce] order管理頁面中的order。 此 [!DNL Commerce] 訂單編號會與訂單資訊一起顯示在 _[!UICONTROL Orders]_標籤。 |
| 4 | **已建立新的客戶帳戶。** 若已在您的訂單設定中設定，且客戶不存在於 [!DNL Commerce] 資料庫中，會在以下位置建立新客戶： [!DNL Commerce] 資料庫使用Amazon訂單中的對應客戶資訊。 如果您選擇 `No Customer Creation (guest)` 在您的訂單設定中，順序會遵循 [!DNL Commerce] 來賓程式，而不是在您的資料庫中建立客戶。 此時，如果您的 [!DNL Commerce] 系統與ERP/OMS/WMS整合，訂單會根據內部放置和建立的新訂單的整合擷取 [!DNL Commerce]. |
| 5 | **訂單已出貨。** 從 [!DNL Commerce] 訂單處理頁面，您會出貨訂單並新增追蹤編號。 當所有專案都標示在 `Shipped` 狀態：<ul><li>的狀態 [!DNL Commerce] 訂單變更至 `Complete`.</li><li>Amazon銷售管道訂單的狀態變更為 `Shipped`.</li><li>追蹤號碼會同步至Amazon，而Amazon中的訂單狀態會變更為 `Shipped`.</li><li>送貨通知會透過Amazon傳送給客戶，而非從 [!DNL Commerce] (根據Amazon的原則)。 |

## 範例：由Amazon (FBA)履行

| 步驟 | 說明 |
|---|---|
| 1 | **Amazon已履行的訂單是在Amazon上下達的。** |
| 2 | **訂單已匯入。** 在指派訂單之前，不會將訂單匯入Amazon銷售管道 `Shipped` 由Amazon顯示的狀態。 由於Amazon擁有此產品的詳細目錄，因此可避免干擾倉儲/詳細目錄管理。 |
| 3 | **訂單詳細資訊會更新。** 若已在您的 [訂單設定](./order-settings.md)，Amazon順序會建立 [!DNL Commerce] 訂單並將其建立為狀態為的訂單 `Complete`. |
