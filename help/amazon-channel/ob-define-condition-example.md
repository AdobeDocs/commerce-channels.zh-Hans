---
title: '範例：定義條件'
description: 建立清單規則時，定義條件以識別要列在Amazon Marketplace上的Commerce目錄產品。
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 範例：定義條件

## 條件

條件中任何粗體區域都可以按一下以檢視各種選項。

**如果所選網站內的所有產品都符合條件，請勿新增條件。**

>[!NOTE]
>
>直接與Amazon的系統通訊時，有一組複雜的後端程式。 根據您嘗試列出的專案數量，以及Amazon的系統可能有多忙（例如「黑色星期五」），您的專案可能需要一些時間才會列在Amazon上。

請參閱的條件區段： [建立購物車價格規則](https://docs.magento.com/user-guide/marketing/price-rules-catalog-create.html){target="_blank"}.

## 定義條件

此程式可能簡單或詳細，視您的目錄設定而定。 您可以設定條件，以便 `ALL` 或 `ANY` 的定義條件為 `TRUE` 或 `FALSE` 若是產品，則該產品符合在Amazon上列出的資格。

條件是以現有的產品屬性值為基礎。 若要將規則套用至所有產品，請將「條件」區段保留空白。

>[!NOTE]
>
>如果您想要根據特定產品屬性定義條件，請設定 **[!UICONTROL Use for Promo Rule Conditions]** 將屬性設定為 `Yes`. 您可以在以下位置存取此設定： [店面屬性](https://docs.magento.com/user-guide/catalog/product-attributes-add.html){target="_blank"} 屬性的頁面。

![條件 — 第1行](assets/ob-listing-rule-conditions-start.png)

Amazon此範例中的規則會定義一個規則，該規則會為所有具有 _AMAZON FBA_ 屬性設定為 `Yes`.

規則陳述式有兩個粗體連結，按一下就會顯示陳述式該部分的選項。 如果您儲存條件而未變更粗體選項，則規則會套用至您的所有產品。

- 按一下 **[!UICONTROL ALL]** 並選擇 `ALL` 或 `ANY`.
- 按一下 **[!UICONTROL TRUE]** 並選擇 `TRUE` 或 `FALSE`.
- 若要將規則套用至所有產品，請保留條件不變。

您可以變更這些值的組合，以建立不同的條件。 在此範例中，會使用下列條件：

`If ALL of these conditions are TRUE:`

1. 按一下新增(![「新增」圖示](assets/btn-add-grn.png))圖示並選取條件所依據的屬性，例如條件組合或產品屬性。

   - **[!UICONTROL Conditions Combination]**  — 選擇以允許建立另一組 `All/Any` 和 `True/False` 現有集合內的條件。

      ![條件組合](assets/ob-conditions-combinations.png)

   - **[!UICONTROL Product Attribute]**  — 產品屬性取決於屬性的設定。 若要讓屬性出現在清單中，必須將其設定為用於促銷規則條件。 請參閱 _用於促銷規則條件_ 在 [產品屬性](https://docs.magento.com/user-guide/stores/attributes-product.html){target="_blank"}.

      在下的清單中 **[!UICONTROL Product Attribute]**，選擇您要當作條件基礎的屬性。 在此範例中，選取的條件為 `Amazon FBA`.

      ![條件行2，第2部分](assets/ob-condition-attribute-dropdown.png)

      選取的條件會顯示在陳述式中，後面接著兩個粗體連結。 選項會依您選取的產品屬性而有所不同。

      設定屬性後，便無法變更。 若要變更屬性，您必須刪除該行並新增屬性。 您可以按一下刪除(![「刪除」圖示](assets/btn-del-red.png))圖示來標籤行尾。

      1. 按一下 **[!UICONTROL is]** 並選擇描述產品符合條件的比較運運算元。

         在此範例中，比較運運算元為 `is`. 可用的選項取決於在上一步驟中選取的屬性。 選項可包含不同的比較選項，例如相符值（不包含或包含至少一個值）以及大於、等於和小於數字量。 在此範例中，選項為 `is` 和 `is not`.

      1. 按一下 **[!UICONTROL ...]** 並選擇條件所依據的屬性值。

         選項視屬性的設定而定。 系統可能會提示您選取選項，或輸入條件的文字或數值。 在此範例中，選取專案為 `Yes`.

         選取的專案會顯示在陳述式中，以完成條件。

         ![條件行2，第3部分](assets/ob-listing-rule-condition-is.png)
   此條件已完成。 如上所述，此條件表示您產品中任何一項 [!DNL Commerce] 將Amazon FBA屬性設定為值的目錄 `Yes` 有資格在本地區和商店中列為Amazon。 您可以新增更多條件行，進一步縮小合格產品的範圍。

1，若要將另一個條件行新增至陳述式，請返回步驟1並重複此程式，直到所有所需條件都完成為止。

您可以隨時按一下刪除(![「刪除」圖示](assets/btn-del-red.png))圖示來標籤行尾。
