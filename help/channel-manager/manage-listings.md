---
title: 管理清單
description: '管理銷售管道清單 [!DNL Commerce] 與Adobe Commerce和Magento Open Source的管道管理員一起儲存。'
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# 管理清單

管理產品清單 [!DNL Walmart Marketplace] Channel Manager UI中的銷售管道。

個別清單的狀態表示產品在 [!DNL Channel Manager] 工作流程，方便您決定後續步驟並解決任何錯誤。

![連線銷售管道的清單頁面](assets/listings-dashboard-view.png)

您可以從「清單」檢視完成下列作業。

* 檢視目前清單
* 排序和篩選清單
* 新增產品
* 比對產品
* 追蹤清單狀態
* 檢閱錯誤狀態清單的錯誤說明

## 檢視產品清單

1. 從管理員，前往 [!UICONTROL **行銷** > **頻道管理員**].

1. 從「商店」清單中，選取商店專案列中的眼睛圖示，以開啟商店檢視。

1. 選取 [!UICONTROL **清單**].

1. 排序 *清單* 選取「 」中的任何欄標題即可檢視 *清單* 表格。

1. 篩選 *清單* 選取其中一個狀態計數卡以檢視。

1. 重設排序順序並透過選取以下專案移除篩選器 **重新整理產品**.

## 新增 [!DNL Commerce] 產品至管道管理員

為建立產品分類 [!DNL Walmart Marketplace] 完成下列工作來建立頻道：

* [從新增產品 [!DNL Commerce] 目標產品目錄 [!DNL Channel Manager]](add-products-to-channel-store.md)

* [對應目錄屬性](map-catalog-attributes.md#configure-product-attribute-settings)

## 比對產品於 [!DNL Walmart]

您可以在上建立產品優惠方案 [!DNL Walmart Marketplace] 使用產品比對或手動上傳新產品的產品清單。

* **[匹配沃爾瑪的產品](connect-listings-to-marketplace.md)** — 將產品清單從您的頻道連結至 [!DNL Walmart Marketplace] 更新銷售相同產品的現有清單。 符合條件由 [attribute-mapping設定](map-catalog-attributes.md) 您的頻道。

* **[手動上傳新清單](connect-listings-to-marketplace.md#upload-new-product-listings)** — 針對不符合上現有清單的產品 [!DNL Walmart Marketplace]，使用 [!DNL Walmart] 產品類別Excel範本可大量上傳產品清單。

## 列出控制項與欄位摘要

下清單格說明可用的控制項和資料行 [!UICONTROL Listings].

**控制項[!UICONTROL Listings]**

| **控制** | **說明** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | 開啟 [!UICONTROL Admin Product Catalog] 選擇產品以新增至您的頁面 [!DNL Walmart Marketplace] 分類，或更新產品屬性以符合沃爾瑪市集列出的要求。 |
| [!UICONTROL Match products on Walmart] | 在中選取一或多個產品後 [!UICONTROL Draft] 狀態，選取 [!UICONTROL Match products on Walmart] 以檢查可新增至現有產品的優惠方案 [!DNL Walmart Marketplace] 清單。 |
| [!UICONTROL Refresh products] | 以最新的清單和狀態更新顯示。 此控制項也會將清單檢視重設為預設的排序順序，並移除任何篩選器。 |
| [!UICONTROL Filter by *狀態*] | 選取「清單」表格上方的其中一個狀態卡，僅顯示具有特定狀態的清單。 選取以移除篩選器 **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | 選取任何欄標題，變更清單的排序順序。 |


**欄說明**

| **欄位** | **說明** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | 來自的產品名稱 [!DNL Commerce] 存放區目錄。 |
| [!UICONTROL SKU (Unique ID)] | 指派給產品的SKU [!DNL Commerce] 目錄。 |
| [!UICONTROL  Quantity] | Adobe Commerce或Magento Open Source中可用的庫存量。 |
| [!UICONTROL Price] | 產品價格來自 [!DNL Commerce] 存放區目錄。 目錄價格更新會同步至「管道管理員」，然後傳送至 [!DNL Walmart Marketplace]  以便列出的專案顯示目前的價格。 |
| [!UICONTROL Status] | 指示中目前的訂單狀態 [!DNL Commerce] 訂單工作流程。 當您成功新增產品到時，狀態會更新 [!DNL Channel Manager] 以及匹配市集上的產品時。 如果作業失敗，清單會顯示錯誤狀態。 修正錯誤後， [!DNL Channel Manager] 請重試操作並更新狀態。 |
| [!UICONTROL Error Description] | 為產品提供其他錯誤資訊，包括 `[!DNL Error]` 狀態。 |

### 關於清單狀態

在「清單」工作區中，「狀態」標籤會顯示產品在 [!DNL Channel Manager] 工作流程，方便您決定後續步驟並解決錯誤。 清單可以有下列狀態標籤：

* **[!UICONTROL Draft]** — 識別尚未使用的產品 [已提交至 [!DNL Walmart] 進行比對](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** — 識別提交以供比對的產品 [!DNL Walmart Marketplace]. 產品保留在 *處理中* 狀態直到 [!DNL Walmart] 傳回HTTP狀態訊息，指出相符是否成功，或是否有錯誤。 最多可能需要30分鐘，匹配作業才能在 [!DNL Walmart Marketplace].

* **[!UICONTROL Match]** — 識別成功比對的產品 [!DNL Walmart].

   當產品屬性值（例如UPC代碼）與現存的UPC值相符時，就會發生相符專案 [!DNL Walmart Marketplace] 清單。 當產品符合時，Commerce產品選件會新增到現有清單中。

   檢查 [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) 資料面板，可複查更新的產品清單，並驗證產品詳細資訊、價格及存貨數量。

* **[!UICONTROL Match - Match in Stage]** — 識別相符的產品 [!DNL Walmart] 在URL之前 [!DNL Walmart Marketplace] 存放區已上線。 具有此狀態的產品會在以下狀況時自動連線： [!DNL Walmart Marketplace] 商店上線。

* **[!UICONTROL Error]** — 識別不匹配現有產品的產品 [!DNL Walmart Marketplace] 清單。

* **[!UICONTROL Error description]** — 提供有關清單錯誤的詳細資訊。

   解決錯誤後，請重新提交產品以進行比對。 另請參閱 [產品比對錯誤疑難排解](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
