---
title: 協力廠商清單
description: 更新協力廠商清單設定可判斷您的Commerce目錄是否從您現有的Amazon賣家中心清單匯入產品。
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# 協力廠商清單

協力廠商清單設定是商店清單設定的一部分。 清單設定可從以下位置存取： [存放區儀表板](./amazon-store-dashboard.md).

這些設定會決定 [!DNL Commerce] 目錄會從您現有的匯入產品 [!DNL Amazon Seller Central] 清單。 最佳實務是從Amazon匯入清單，以確保所有清單都符合 [!DNL Commerce] 產品。 當您的清單屬於您的時 [!DNL Commerce] 型錄，您就可以從單一型錄管理所有產品，並使用Amazon銷售管道功能。 這些功能包括Amazon的履行與訂單管理、智慧型重新訂價，以及數量管理。

設定為匯入您的Amazon清單時，Amazon銷售管道會將您的Amazon清單匯入您的 [!DNL Commerce] 目錄，嘗試將它們與現有產品配對。 如果系統未自動找到相符專案，您可以將Amazon清單匯入為新清單 [!DNL Commerce] 或手動比對清單與產品。

如果您選擇匯入Amazon清單，請選擇 [!DNL Commerce] 具有Amazon賣家SKU和Amazon ASIN值的屬性。 如果您沒有 [!DNL Commerce] [產品屬性](./ob-creating-magento-attributes.md)，考慮建立並指派這些人員。 對應這些屬性有助於正確比對匯入的Amazon清單與您的 [!DNL Commerce] 產品。

初始清單匯入起始時間 [存放區整合](./store-integration.md) 完成。 之後，根據您的密碼設定， [!DNL Commerce] 持續檢查新新增的Amazon清單(未在AmazonSales Channel中建立)並更新您的 [!DNL Commerce] 根據您的協力廠商清單設定建立目錄。

## 設定協力廠商清單設定

1. 按一下 **[!UICONTROL Listing Settings]** 在商店控制面板上。

1. 展開 _[!UICONTROL Third Party Listings]_區段。

1. 對象 **[!UICONTROL Import Third Party Listings]** （必要），選擇一個選項：

   - `Import Listing` - （預設）選擇您何時希望Amazon清單中的產品資訊匯入您的 [!DNL Commerce] 產品目錄。 此選項為預設值，建議使用。

   - `Do Not Import Listing`  — 選擇您想要手動執行的時機 [建立和指派新產品](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"} 至您的 [!DNL Commerce] Amazon清單的目錄。
   >[!NOTE]
   >下列選項欄位只有在設定為時才會啟用 `Import Listing`.

1. 對象 **[!UICONTROL Attribute That Contains Amazon Seller SKU]**，選擇 [!DNL Commerce] 符合Amazon賣家SKU值的屬性。

1. 對象 **[!UICONTROL Attribute That Contains Amazon ASIN]**，選擇 [!DNL Commerce] 您建立的屬性，並將其與Amazon ASIN比對。

   >[!NOTE]
   >如果您沒有建立這些 [!DNL Commerce] Amazon清單的屬性，請參閱 [建立Amazon比對的屬性](./ob-creating-magento-attributes.md).

1. 完成後，按一下 **[!UICONTROL Save listing settings]**.

![協力廠商清單](assets/amazon-third-party-listings.png)

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Import Third Party Listings] | 必填。 選項：<ul><li>**[!UICONTROL Import Listing]** - （預設）選擇您何時希望Amazon清單中的產品資訊匯入您的 [!DNL Commerce] 產品目錄。 </li><li>**[!UICONTROL Do Not Import Listing]**  — 選擇您想要手動執行的時機 [建立和指派新產品](https://docs.magento.com/user-guide/catalog/products.html){target="_blank"} 至您的 [!DNL Commerce] Amazon清單的目錄。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | 僅在設定為時啟用 `Import Listing`.<br>選擇 [!DNL Commerce] 屬性做為Amazon賣家SKU的Amazon屬性的相符專案。 如果此屬性不存在，請參閱 [建立Amazon產品屬性以進行Amazon比對](./ob-creating-magento-attributes.md). 如有需要，請檢閱您的 [!DNL Commerce] [屬性](./managing-attributes.md) 和建立或編輯屬性，以符合此Amazon資料。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | 僅在設定為時啟用 `Import Listing`.<br>選擇 [!DNL Commerce] 與Amazon ASIN的Amazon屬性相符的屬性。 如果此屬性不存在，請參閱 [建立Amazon產品屬性以進行Amazon比對](./ob-creating-magento-attributes.md). 如有需要，請檢閱您的 [!DNL Commerce] [屬性](./managing-attributes.md) 和建立或編輯屬性，以符合此Amazon資料。 |

**快速存取** - [!UICONTROL Listing Settings] 區段

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
