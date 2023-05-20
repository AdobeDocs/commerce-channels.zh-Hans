---
title: 履行者
description: 使用「履行者」設定來決定如何履行（出貨）Amazon清單中的訂單。
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# 履行者

_[!UICONTROL Fulfilled By]_設定是商店清單設定的一部分。 清單設定可從以下位置存取： [存放區儀表板](./amazon-store-dashboard.md).

這些設定會定義履行（或出貨）訂單的一方。 如果您的所有訂單都是使用一種方式完成，請在貿易商（您）或Amazon之間選擇。 如果您打算完成所在位置的訂單並使用Amazon，最佳實務就是使用第三個選項並設定 [!DNL Commerce] 產品屬性。

- **[!UICONTROL Fulfilled by Merchant]**  — 選擇您（貿易商）是否履行所有訂單。 下訂單時，存貨會從您的帳戶中扣除。 [!DNL Commerce] 目錄。

- **[!UICONTROL Fulfilled by Amazon]**  — 選擇Amazon是否履行所有訂單。 使用此選項，產品詳細目錄不會從您的帳目中扣除 [!DNL Commerce] 下訂單時建立目錄。 Amazon已履行訂單的存貨存量會儲存起來，並從其倉庫中扣除。 指派此選項之前，您必須先驗證 [!DNL Amazon Seller Central] 您的產品符合資格的帳戶 _由Amazon履行_ (FBA)履行。 FBA詳細目錄直接透過您的 [!DNL Amazon Seller Central] 帳戶。 使用此履行方法，Amazon銷售管道不會將數量更新分享到 [!DNL Commerce] 和Amazon。 因此，並非所有數量設定中所述的行銷工具都可在Amazon銷售管道中使用。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 如果您的產品可能由您和Amazon履行，建議您建立 [!DNL Commerce] 具有「由商家履行」和「由Amazon履行」值的產品屬性。 為每個產品設定此值，即表示完成訂單的人員。

履行方法是地區屬性，且以 **[!UICONTROL Amazon Marketplace Country]** 設定定義於 [存放區整合](./store-integration.md). 進行變更時，該變更會影響共用該變更的所有Amazon清單 [!DNL Amazon Seller SKU] 在您的Amazon商店中，於相同地區銷售(定義見 _[!UICONTROL Amazon Marketplace Country]_期間 [存放區整合](./store-integration.md))。 共用專案的變更 [!DNL Amazon Seller SKU] 不會影響到您為不同地區設定的Amazon商店（如商店整合期間所定義）。

>[!NOTE]
>
>當訂單由Amazon (FBA)履行且訂單已匯入時，您可能會看到訂單明細中某些欄位的虛擬資料。 另請參閱 [Amazon訂單詳細資料](./amazon-order-details.md).

## 設定 [!UICONTROL Fulfilled By] 設定 {#configure-fulfilled-by-settings}

1. 按一下 **[!UICONTROL Listing Settings]** 在商店控制面板上。

1. 展開 _[!UICONTROL Fulfilled By]_區段。

1. 對象 **[!UICONTROL Product Fulfilled By]**，選擇履行（出貨）訂單的人員：

   - `Fulfilled by Merchant`  — 商家履行訂單。

   - `Fulfilled by Amazon` - Amazon倉儲履行訂單。

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] attribute指出誰能完成每個產品的訂單。

      若已選取，請選擇 [!DNL Commerce] 您要對應的屬性 **[!UICONTROL Fulfilled by Attribute]**.

1. 完成後，按一下 **[!UICONTROL Save listing settings]**.

![履行者設定](assets/amazon-fulfilled-by.png)

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | 選項：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM)選擇是否履行訂單。 下訂單時，存貨會從您的帳戶中扣除。 [!DNL Commerce] 目錄。 建立新產品時，會指派「已履行商家」的履行方式。</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA)選擇Amazon是否履行訂單。 使用此履行方式，產品詳細目錄不會從您的帳目中扣除 [!DNL Commerce] 下訂單時建立目錄。 建立產品時，其建立方式 _[!UICONTROL Fulfilled by Amazon (FBA)]_作為履行型態。 確保您的產品符合FBA履行資格(在 [!DNL Amazon Seller Central] 帳戶。 FBA詳細目錄也可透過以下方式直接管理 [!DNL Amazon Seller Central] 帳戶。 使用此履行方法，不會推出相對於您的數量的數量更新 [!DNL Commerce] 目錄，因此無法使用中說明的某些行銷工具 [庫存/數量設定](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 選擇您是否擁有 [!DNL Commerce] 決定是由商家履行或由Amazon履行的屬性。 選擇後， **[!UICONTROL Fulfilled by Attribute]** 啟用。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | 選擇 [!DNL Commerce] 用來決定履行方式的屬性。<br><br>例如，如果屬性為 _履行者_ 而您選擇屬性值作為 _[!UICONTROL Fulfilled By Merchant]_或_[!UICONTROL Fulfilled By Amazon (FBA)]_，系統會將該值作為新產品的履行型別。 身為商家，您應確保產品符合以下範疇的FBA履行資格： [!DNL Amazon Seller Central] 帳戶。 FBA詳細目錄也可透過您的Amazon賣家帳戶直接管理。<br><br>選項取決於您為Amazon產品設定的屬性。 |

**快速存取** - [!UICONTROL Listing Settings] 區段

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
