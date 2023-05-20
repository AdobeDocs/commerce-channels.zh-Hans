---
title: 清單規則
description: 使用清單規則可決定以Amazon Marketplace清單形式發佈的Commerce目錄產品。
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# 清單規則

您可以存取中存放區的清單規則 [存放區儀表板](./amazon-store-dashboard.md).

清單規則定義用來決定Amazon銷售管道會將哪些產品發佈至Amazon的規則。 這些規則提供許多選項，可建立從簡單到複雜的規則，以將產品納入清單或從中排除。 每個規則都包含設定產品清單適用性要求的條件。

您的清單規則會持續與 [!DNL Commerce] 目錄。 當您新增時 [!DNL Commerce] 產品若符合上市規則所設定的資格要求，系統就會自動處理這些產品，以便在Amazon上上市。

- 如果您希望將所有產品發佈至Amazon清單，請勿為清單規則定義任何條件。

- 如果您想要限制發佈至Amazon的目錄產品，請定義清單規則條件。 定義Amazon清單規則的條件，會遵循與定義條件相同的邏輯和程式 [購物車價格規則](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target="_blank"}.

- 如果您的清單規則排除產品，則該產品的資格狀態會變更為 `Ineligible`. 不符合資格的產品不會發佈至Amazon。

- 如果不符合資格的產品已列於Amazon上，且您將Amazon清單與您的產品比對， [!DNL Commerce] 目錄產品，Amazon清單的數量變更為 `0` 以防止產品銷售。 Amazon清單可以是 [手動移除](./end-listings-manually.md).

數量和資格狀態的變更會影響市集中針對同一地區商店銷售而共用Amazon賣家SKU的所有清單(定義見 _[!UICONTROL Amazon Marketplace Country]_期間 [存放區整合](./store-integration.md))。 但是，對共用的 [!DNL Amazon Seller SKU] 不會在一個地區影響產品在其他國家/地區的Amazon清單。

![清單規則](assets/ob-listing-rules.png)

## 設定清單規則設定

1. 按一下 **[!UICONTROL Listing Rules]** 在商店控制面板上。

1. 定義您想要的條件，讓產品符合在Amazon上列出的資格。

另請參閱 [範例：定義條件](./ob-define-condition-example.md).

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Websites] | 可用的選項取決於 [網站](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target="_blank"} 您已設定在 [!DNL Commerce] 設定。 為Amazon上列出的合格產品選取網站。 只能選取一個網站，因為每個網站都需要在Amazon銷售管道中建立唯一的Amazon商店。 |
| [!UICONTROL Conditions] | 用於定義 [!DNL Commerce] 適用於您Amazon區域內產品資格的屬性。 另請參閱 [範例：定義條件](./ob-define-condition-example.md). |

## 條件工作區

條件中任何粗體區域都可以按一下以檢視各種選項。

- 如果所選網站內的所有產品都符合條件，請勿新增條件。
- 直接與Amazon的系統通訊時，有一組複雜的後端程式。 根據您嘗試列出的專案數量，以及Amazon的系統可能有多忙（例如「黑色星期五」），您的專案可能需要一些時間才會列在Amazon上。

如需條件的詳細資訊，請參閱 [說明條件](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target="_blank"}.

## 清單規則預覽

當您修改清單規則的條件定義時，可以按一下 **[!UICONTROL Preview Changes]** 以套用規則變更，並檢視清單如何受到影響。 儲存清單規則變更之前，請先在此清單預覽功能中驗證您的清單。

您的Amazon清單會與規則和定義的條件做比較。 然後您可以檢閱：

- 根據您目前的狀況，哪些產品會移至不合格狀態 [!DNL Amazon Seller Central] 帳戶
- 哪些產品會從不符合資格的狀態移回符合資格的狀態
- 哪些產品是新的Amazon清單，並從您的合格清單新增到您的Amazon清單 [!DNL Commerce] 產品

清單預覽可讓您預覽潛在的Amazon清單，並對清單規則進行任何必要的調整。

您潛在的Amazon清單會填入 _[!UICONTROL Listing Preview]_頁面位於下列三個索引標籤之一：

- **[!UICONTROL Ineligible Listings]**  — 根據您目前的清單規則及條件，所列產品不符合Amazon清單資格。

   不符合資格的產品不會發佈至Amazon。 如果不符合資格的產品已列於Amazon上，且您將Amazon清單與您的產品比對， [!DNL Commerce] 目錄產品，Amazon清單的數量變更為 `0` 以防止產品銷售。 若要手動移除清單，請參閱 [結束Amazon清單](./end-listings-manually.md). 此處不列出不符合Amazon要求的產品。 這些產品會列在 [非使用中清單頁標](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]**  — 根據您目前的上市規則和條件，所列產品符合Amazon上市資格，也符合Amazon要求。 此清單包含您匯入的現有Amazon清單(如果您有 **匯入協力廠商清單** 設定為 `Import Listing` 在 [清單設定](./third-party-listing-settings.md))。

- **[!UICONTROL New Listings]**  — 列出的產品包含您的 [!DNL Commerce] 根據您目前的清單規則與條件，將新符合Amazon清單資格的產品列入目錄，並建立並發佈新的Amazon清單。

### 檢視您的清單預覽

1. 按一下 **[!UICONTROL Listing Rules]** 在商店控制面板上。

1. 檢視或新增您的 [清單規則](./listing-rules.md).

1. 修改您的 [清單規則條件](./ob-define-condition-example.md).

1. 按一下 **[!UICONTROL Preview Changes]**.

1. 檢閱並確認您在 _[!UICONTROL Ineligible Listings]_，_[!UICONTROL Eligible Listings]_、和 _[!UICONTROL New Listings]_索引標籤。

1. 如果您的清單符合預期，請按一下 **[!UICONTROL Save and close]**.

   如果您的清單未如預期顯示，請按一下 **[!UICONTROL Back]** 並修改您的規則和條件，直到清單符合您的預期為止。

![清單規則預覽](assets/amazon-listing-rule-preview.png)

### 列出預覽記錄

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Product ID] | 指派給的唯一、連續編號 [!DNL Commerce] 新增目錄產品時。 |
| [!UICONTROL Thumbnail] | 顯示主要產品影像的縮圖。 |
| [!UICONTROL Name] | 產品的名稱，受管理於 [!DNL Commerce] [產品格線](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"}. |
| [!UICONTROL Type] | 產品的型別，管理於 [!DNL Commerce] 產品格線。 |
| [!UICONTROL Attribute Set] | 作為產品範本使用的屬性集名稱，管理於 [!DNL Commerce] 產品格線。 |
| [!UICONTROL SKU] | 指派給產品的唯一庫存單位，管理於 [!DNL Commerce] 產品格線。 |
| [!UICONTROL Visibility] | 指出產品可見的位置，並在下列位置管理： [!DNL Commerce] 產品格線。 選項：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| 狀態 | 表示產品的狀態，管理於 [!DNL Commerce] 產品格線。 選項： `Enabled` / `Disabled` |

![清單預覽工作流程](assets/listing-preview-flowchart.png)
