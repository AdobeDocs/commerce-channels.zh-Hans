---
title: 建立 [!DNL Commerce] Amazon的屬性
description: 在完成Amazon銷售管道上線流程之前，請確定您已具備 [!UICONTROL Commerce] 產品屬性。
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# 建立 [!DNL Commerce] Amazon的屬性

上線之前 [!DNL Amazon Seller Central] 帳戶，最佳作法是新增 [!DNL Commerce] [產品屬性](https://docs.magento.com/user-guide/stores/attributes-product.html){target="_blank"} 以對應您的產品清單。 完成入門後，您可以透過以下方式管理產品屬性： [屬性](./managing-attributes.md) 的標籤 [Amazon銷售管道首頁](./amazon-sales-channel-home.md) 頁面。

這些指示詳細說明如何建立 [!DNL Commerce] Amazon ASIN和Amazon條件的屬性。 建議建立其他屬性，包括Amazon EAN、Amazon ISBN和Amazon UPC。 如果您想要使用Amazon清單價格作為定價規則的價格來源，您也可以建立Amazon Price屬性。 在上線期間設定您的清單和定價設定時，會使用這些屬性。 在建立Amazon清單以及更新和同步時，也使用這些屬性 [!DNL Commerce] 包含Amazon清單的目錄。

目錄搜尋設定可讓您設定相符的搜尋引數，以協助對應符合條件的專案 [!DNL Commerce] 產品與Amazon清單。 對應後，Amazon會啟動與定價、數量、覆寫以及訂單和產品同步處理相關的動作。

定義這些值會增加完全相符的可能性，減少日後手動相符產品清單的需求。 將屬性新增為入門的一部分 [預先設定任務](./amazon-pre-setup-tasks.md)，Amazon銷售管道在入門期間自動比對您的產品以及在Amazon和之間同步產品資料的可能性較高 [!DNL Commerce] 上線後。

如果您只建立Amazon ASIN屬性（不新增每個產品的ASIN值），則您可以 [!DNL Commerce] 產品可能不會自動符合您的Amazon清單。 您可以透過以下方式手動比對產品： _商店評論_. 不過，手動比對不會建立共用和同步產品資料所需的資料元素。

>[!IMPORTANT]
>
>如果您更新ASIN、UPC或其他資料元素，以取得手動相符的產品，則必須在以下兩個位置更新資料： [!DNL Commerce] 目錄和您的清單中的清單 [!DNL Amazon Seller Central] 帳戶。

## 建立Amazon ASIN產品屬性

1. 登入 [!DNL Commerce] 管理員。

1. 按一下 **[!UICONTROL Stores]** 在左側功能表中。

1. 在 _[!UICONTROL Attributes]_區段，按一下&#x200B;**[!UICONTROL Product]**.

1. 若要開啟屬性屬性，請按一下 **[!UICONTROL Add New Attribute]**.

1. 對象 **[!UICONTROL Default Label]**，輸入 `Amazon ASIN` （屬性的名稱）。

1. 對象 **[!UICONTROL Catalog Input Type for Store Owner]**，選擇 `Text Field`.

1. 對象 **[!UICONTROL Values Required]**，選擇 `No`.

   雖然在Amazon上列出產品需要Amazon ASIN，但您的某些目錄產品可能未在Amazon上列出。

1. 展開 _[!UICONTROL Advanced Attribute Properties]_並設定選項：

   - 對象 **[!UICONTROL Attribute Code]**，輸入 `amazon_asin`.

   - 對象 **[!UICONTROL Scope]**，選擇 `Global`.

   - 對象 **[!UICONTROL Unique Value]**，選擇 `No`.

   - 對象 **[!UICONTROL Input Validation for Store Owner]**，選擇 `None`.

   - 對象 **[!UICONTROL Add to Column Options]**，選擇 `Yes`.

   - 對象 **[!UICONTROL Use in Filter Options]**，選擇 `Yes`.

1. 按一下 **[!UICONTROL Save Attribute]**.

![Amazon ASIN屬性](assets/creating-asin-attribute.png)

## 建立Amazon條件產品屬性

1. 登入 [!DNL Commerce] 管理員。

1. 按一下 **[!UICONTROL Stores]** 在左側功能表中。

1. 在 _[!UICONTROL Attributes]_區段，按一下&#x200B;**[!UICONTROL Product]**.

1. 若要開啟屬性屬性，請按一下 **[!UICONTROL Add New Attribute]**.

1. 對象 **[!UICONTROL Default Label]**，輸入 `Amazon Condition` （屬性的名稱）。

1. 對象 **[!UICONTROL Catalog Input Type for Store Owner]**，選擇 `Dropdown`.

   此 _[!UICONTROL Manage Options (Values of your Attribute)]_區段隨即顯示。

1. 對象 **[!UICONTROL Values Required]**，選擇 `No`.

1. 對象 **[!UICONTROL Manage Options (Values for your Attribute)]**，新增每個條件選項。

   標準Amazon條件包括：

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. 按一下 **[!UICONTROL Add Option]**.

1. 選取 **[!UICONTROL Is Default]** 要作為預設選取專案的條件選項。

1. 在 _[!UICONTROL Admin]_欄中，輸入您要新增之條件的標籤文字(例如 `New`， `Used`、和 `Used-Like New`)

1. 按一下 **[!UICONTROL Add Option]** 以視需要新增更多選項。

1. 展開 _[!UICONTROL Advanced Attribute Properties]_區段並設定選項。

   - 對象 **[!UICONTROL Attribute Code]**，輸入 `amazon_condition`.

   - 對象 **[!UICONTROL Scope]**，選擇 `Global`.

   - 對象 **[!UICONTROL Unique Value]**，選擇 `No`.

   - 對象 **[!UICONTROL Input Validation for Store Owner]**，選擇 `None`.

   - 對象 **[!UICONTROL Add to Column Options]**，選擇 `Yes`.

   - 對象 **[!UICONTROL Use in Filter Options]**，選擇 `Yes`.

1. 按一下 **[!UICONTROL Save Attribute]**.

![Amazon條件屬性](assets/creating-amazon-condition-attribute.png)

![「下一步」圖示](assets/btn-next.png) [**繼續新增或驗證API金鑰**](./amazon-verify-api-key.md)
