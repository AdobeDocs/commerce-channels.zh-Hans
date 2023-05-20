---
title: 不符合資格的清單
description: Amazon銷售管道提供 [!UICONTROL Ineligible] 標籤可協助您管理專案，但根據您目前的清單規則，此標籤不符合清單資格。
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 不符合資格的清單

此 _[!UICONTROL Ineligible]_索引標籤會顯示目前在Amazon上發佈，但根據您目前的清單規則不符合清單資格的所有產品清單。 如果先前產品符合資格，且清單規則已修改為現在不符合資格，則與產品相關的數量會降至0，且產品會標籤為_&#x200B;不合格&#x200B;_. 但是，它仍存在於您的 [!DNL Amazon Seller Account].

將產品移出 _[!UICONTROL Ineligible]_標籤，您可以 [修改您的清單規則](./listing-rules.md) 讓您的產品符合資格。

上的可用動作 _[!UICONTROL Ineligible]_索引標籤包括：

下 _[!UICONTROL Actions]_：

- **[!UICONTROL End Listing(s) on Amazon]**：選擇以從「 」中移除所有選取的清單 [!DNL Amazon Marketplace]. 另請參閱 [結束Amazon清單](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**：選擇以變更清單的覆寫設定。 另請參閱 [覆寫](./overrides.md) 或 [編輯或移除覆寫](./creating-editing-overrides.md#edit-override-single-listing).

下 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_欄：

- **[!UICONTROL View Details]**：選擇檢視清單詳細資訊，包括 [列出活動記錄](./product-listing-details.md#listing-activity-log)， [Buy Box競爭者定價](./product-listing-details.md#buy-box-competitor-pricing)、和 [最低競爭者價格](./product-listing-details.md#lowest-competitor-pricing). 此動作僅供檢視。 清單詳細資料無法變更。 另請參閱 [檢視詳細資料](./product-listing-details.md).

- **[!UICONTROL Create Override]**：選擇建立覆寫並將其套用至此清單。 另請參閱 [建立覆寫](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**：選擇以修改指派給目錄產品的ASIN。 如果目錄中的產品符合錯誤的ASIN，則會使用此動作。 另請參閱 [編輯指派的ASIN](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**：選擇建立別名SKU，此SKU可用來從相同目錄產品建立Amazon清單。 另請參閱 [建立別名賣家SKU](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：選擇以變更與訂單相關聯的履行方式。 另請參閱 [設定履行者設定](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**：選擇將清單從 [!DNL Amazon Marketplace]. 另請參閱 [結束Amazon清單](./end-listings-manually.md).

>[!NOTE]
>如果您有處理中的清單，清單數量會顯示在標籤上方的訊息中。

![不符合資格的Amazon清單](assets/amazon-ineligible-listings.png)

Amazon銷售管道首頁有一些共同之處 [工作區控制項](./workspace-controls.md) 可讓您自訂顯示的資料。

## 預設欄

| 欄 | 說明 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazon指派給產品的SKU （庫存單位），用於識別產品、選項、價格和製造商。 |
| [!UICONTROL ASIN] | 識別專案的10個字母和/或數字的唯一區塊。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]. ASIN是識別專案的10個字母和/或數字的唯一區塊。 對於書籍，ASIN與ISBN編號相同，但對於所有其他產品，當專案上傳到其目錄時會建立新的ASIN。 您可以在Amazon的產品詳細資訊頁面上找到專案ASIN，以及與該專案相關的進一步詳細資訊。 |
| [!UICONTROL Product Listing Name] | 產品的名稱。 |
| [!UICONTROL Condition] | 此 [條件](./product-listing-condition.md) 產品的。 |
| [!UICONTROL Landed Price] | 產品的清單價格加上其送貨價格。 |
| [!UICONTROL Amazon Quantity] | 產品在Amazon上積極列出時的可用數量。 |
| [!UICONTROL Action] | 可套用至特定清單的可用動作清單。 若要套用動作，請按一下 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_欄並選取一個選項：<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[建立覆寫](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
