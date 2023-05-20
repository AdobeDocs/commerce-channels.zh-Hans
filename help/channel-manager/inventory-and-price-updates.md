---
title: 存貨與價格更新
description: '[!DNL Channel Manager] 同步庫存與價格更新，以便 [!DNL Commerce] 存放區和 [!DNL Walmart Marketplace] 以便您能透過以下網站管理銷售管道作業： [!DNL Commerce] 管理員'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# 更新存貨與訂價

[!DNL Channel Manager] 追蹤中產品的存貨和定價 [!DNL Commerce] 產品目錄並將更新同步到連線的銷售管道和 [!DNL Walmart Marketplace]. 同步作業可確保產品清單能反映目前的庫存數量與訂價。


>[!IMPORTANT]
>
>晚於 [!DNL Channel Manager] 安裝與設定完成，所有存貨、價格及訂單更新會自動同步。 如果您已在沃爾瑪市集上銷售，請務必停用任何其他可更新產品和訂單資料的整合。 然後，確認存貨存貨水準與價格位於 [!DNL Commerce] 店面準確，資料符合 [!DNL Walmart Marketplace] 連線之前 [!DNL Channel Manager] 前往即時市集商店。


## 詳細目錄更新

當產品存貨層次在中變更時 [!DNL Commerce]， [!DNL Channel Manager] 將更新同步至 [!DNL Walmart Marketplace]. 庫存更新最多可能需要10分鐘，才能在銷售管道間同步至 [!DNL Walmart marketplace].

* **更新產品目錄中的庫存數量** — 當 [!DNL Commerce] 庫存數量變更的原因為 [手動庫存數量變更](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html)，退款或取消， [!DNL Channel Manager] 將變更同步至連線的通道，並 [!DNL Walmart Marketplace].

* **減少庫存量以反映 [!DNL Walmart Marketplace] 訂購** — 在 [!DNL Walmart Marketplace] 訂單同步至 [!DNL Channel Manager]， [!DNL Channel Manager] 將更新傳送至 [!DNL Commerce] 訂購系統。 [!DNL Commerce] 會根據順序調整庫存量。 然後，更新後的數量會同步至 [!DNL Walmart Marketplace]. 在同步處理作業完成之前，您可能會在sales channel清單和 [!DNL Walmart].

>[!IMPORTANT]
>
>晚於 [!DNL Walmart Marketplace] 訂單同步至 [!DNL Channel Manager]，存貨數量與訂單資訊只會針對起始 [!DNL Commerce]. 如果訂單已退款或取消自 [!DNL Walmart marketplace]，處理變更 [!DNL Commerce] 以確保的正確性 [!DNL Commerce] 存貨數量與訂單資訊。

## 價格更新

產品價格變更時 [!DNL Commerce]， [!DNL Channel Manager] 將更新同步至 [!DNL Walmart Marketplace]. 價格變更最多可能需要5分鐘的時間才會顯示在中 [!DNL Walmart Marketplace] 清單。

### 管理連線產品的定價

1. 從 [!UICONTROL Admin]，選取 **[!UICONTROL Catalog > Products]**.
1. 在產品格線中，找到要更新的產品並選取 **[!UICONTROL Edit]**.
1. 視需要複查並更新價格。
1. **[!UICONTROL Save]** 變更。

如需管理產品價格設定的協助，請前往 [!DNL Commerce]，請參閱 [管理定價](https://docs.magento.com/user-guide/catalog/pricing.html){target="_blank"}.
