---
title: 依動作管理產品清單
description: 當您管理Amazon清單時，可以將動作套用至個別或多個清單。
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# 依動作管理產品清單

此 _[!UICONTROL Product Listings]_頁面包含數個索引標籤，您可在其中檢視所有清單的狀態，並將產品與Amazon清單比對。

每個標籤上的可用清單任務略有不同，但 [工作區控制項](./workspace-controls.md) 相同，並可讓您自訂針對清單顯示的資料。

下的選項 **[!UICONTROL Actions]** 可將動作套用至多個清單，而選項位於 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_欄只會將該動作套用至個別清單。

另請參閱 [按狀態/標籤管理清單](./managing-listings-by-tab.md).

| 動作 | 說明 | 索引標籤 |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 用於透過比對程式將未完成的產品移回。 若要嘗試重新比對，您必須修改 [清單](./listing-settings.md) 和 [目錄搜尋](./catalog-search.md) 增加自動比對可能性的設定。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 選取要比對的清單、輸入要比對的ASIN或指派缺少的條件，以手動比對目錄產品與Amazon清單。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | 檢視使用中產品的其他資訊，包括清單活動記錄，其中顯示個別SKU /產品的變更。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | 建立 [!DNL Commerce] 使用隨Amazon清單匯入的資訊建立產品目錄。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 嘗試自動比對 | 嘗試自動比對 [!DNL Commerce] 根據搜尋條件設定分類與您的Amazon清單。 若要嘗試重新比對，您必須修改 [清單](./listing-settings.md) 和 [目錄搜尋](./catalog-search.md) 增加自動比對可能性的設定。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | 手動選取中的現有產品 [!DNL Commerce] 並將它指派給Amazon清單。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | 建立 [!DNL Commerce] 使用隨Amazon清單匯入的資訊建立產品目錄。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （整批作業）用於重新列出已結束的清單，或手動列出符合清單規則資格的產品，但您的 _[!UICONTROL Product Listing Actions]_未設定為 `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （單一清單動作）用於重新列出已結束的清單。 此動作也用於手動列出符合您清單規則資格的產品，當 _[!UICONTROL Product Listing Actions]_未設定為 `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （整批作業）用於手動結束與移除Amazon上現有產品的清單。 已結束清單只要符合您的清單規則資格，即可重新列出。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （整批作業）手動編輯現有的「覆寫」，以設定個別清單的價格、處理時間、條件和賣家備註文字，忽略其他清單預設值、設定及規則。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 手動建立「覆寫」，為個別清單設定價格、處理時間、條件和賣家備註文字，忽略其他清單預設值、設定和規則。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | 用於符合目錄產品的ASIN必須修改（例如：如果產品符合錯誤列出的ASIN）。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 可提供兩種功能：<br><br>可用於在您的目錄產品與兩個Amazon清單之間建立一對二的關係。 範例： Amazon的產品以不同的ASIN值列出。 您可以將一個目錄產品與產品的兩個ASIN清單比對。<br><br>可用於控制不同Amazon地區的清單。 範例：您的型錄產品已根據Amazon地區（美國地區為FBA，加拿大地區為FBM）定義不同的出貨方式。 若要控制存貨/數量，您可以建立別名賣方SKU，並使用不同的賣方SKU重新列出該區域的相同產品。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 用於修改與產品相關的履行方式(由Amazon履行：FBA或由商家履行：FBM)。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （單一清單動作）用於手動結束和移除Amazon上現有產品的清單。 已結束清單只要符合您的清單規則資格，即可重新列出。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （單一清單動作）手動編輯現有的「覆寫」，以設定個別清單的價格、處理時間、條件和賣家備註文字，忽略其他清單預設值、設定和規則。 | [[!UICONTROL Overrides]](./overrides.md) |

## 存取產品清單

1. 於 _管理員_ 側欄，前往 **行銷** > _頻道_ > **AmazonSales Channel**.

1. 按一下 **檢視存放區** 在商店資訊卡上。

1. 在商店控制面板上，按一下 **管理清單** 在 _商店清單_ 區段。
