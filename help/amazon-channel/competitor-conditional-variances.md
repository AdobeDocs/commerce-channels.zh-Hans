---
title: 「智慧型重新訂價規則：競爭者條件差異」
description: 建立智慧型重新訂價規則，根據競爭者的定價和產品狀況來決定您的Amazon清單價格。
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 智慧型重新訂價規則：競爭者條件差異

智慧型重新訂價規則的區段包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

智慧型重新定價規則會使用Amazon競爭者的定價來決定您的掛牌價格。 競爭對手是其他銷售商，列出的產品與您在Amazon上列出的產品相同。

如果存在具有相同條件的產品，則基本符合價格為 [最低競爭者](./lowest-competitor-pricing.md) 條件相同的價格。 如果沒有符合您條件的競爭者產品，則基礎符合價格會透過其他可用的競爭者條件進行，從新增、翻新開始，然後透過可用條件繼續進行。 找到條件後，基本相符價格將是該條件中的最低價格。

如果您的產品列有條件 `Used; Good` 而基本符合價格，且競爭對手以較低價格提供相同條件的相同產品，則會使用競爭對手價格。 如果競爭者不存在具有相同條件的競爭者，則系統會檢查是否存在具有下一個條件的競爭者，即 `New`. 如果發現競爭者符合該條件，則會使用最低價格。

## 設定競爭者條件差異

在「 」中定義您的條件差異 _[!UICONTROL Competitor Conditional Variances]_區段。

對象 **[!UICONTROL Conditional Variance]**，選擇一個選項：

- `Use all competitor's product conditions` - （預設）選擇何時將產品與任何可用條件進行比較（如果列出的條件不存在相符專案）。

- `Use Only Matching Competitor's Product Condition`  — 選擇何時希望您的產品僅與相同條件下的競爭者產品進行比較。 如果沒有相符專案，則產品價格為 _Magento價格來源_ 在中定義 [清單價格](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)`  — 選擇先嘗試與相符的產品條件進行比較。 如果不存在相符條件，則會套用相對於您的產品條件和最低競爭者條件的變異數（以百分比表示）。

   當 _[!UICONTROL Apply Variance]_功能已選取，則會針對您的每個Amazon條件顯示其他變異欄位。 此功能可讓您在提供與競爭者處於不同狀況的產品時，使用智慧型重新定價規則。 若要瞭解條件變異數背後的計算，您必須先瞭解所有變異數都是根據基本比對價來決定。

   出現的條件變異選項是根據您的清單設定 `Condition` 對應至條件值的變數 [!DNL Commerce] [產品屬性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. 對於所有對應的條件，您可以定義1-100的差異百分比。 可收集專案則為例外，在此情況下，可套用大於100的百分比。

![智慧型重新訂價規則 — 競爭者條件差異](assets/amazon-competitor-cond-variances.png)

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | 選項： <ul><li>**[!UICONTROL Use all competitor's product conditions]**  — 若您列出產品的條件不符合，則此選項會比對任何可用條件。 它會先嘗試符合您的條件，然後從 `New` 完成情況 `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]**  — 此選項符合您產品的條件。 若不存在相符專案，則產品價格為 _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]**  — 此選項會先嘗試比對您的產品條件。 如果不存在相符條件，則會套用相對於您的產品條件和最低競爭者條件的變異數（以百分比表示）。</li></ul><br><br>根據您條件清單設定（已使用「 」對應至條件值）顯示的條件變異選項 [!DNL Commerce] [產品屬性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. 對於所有對應的條件，您可以表示差異百分比1-100。 可收集專案則為例外，在此情況下，可套用大於100的百分比。<br><br>此功能可讓您在提供與競爭者處於不同狀況的產品時，使用智慧型重新定價規則。 若要瞭解條件變異數背後的計算，您必須先瞭解所有變異數都是根據基本比對價來決定。 |

## 計算條件變異數基礎

- 基本比對條件差異(BMC) =基本比對價格競爭者的條件差異。 使用先前的範例，BMC是 `New` 條件。
- 商家條件差異(MCV) =產品條件的差異。 根據先前的範例，MCV =的變數 `Used; Good` 條件。
- 基本比對價(BMP) = $7.99 （以上說明）

計算條件差異基礎的公式如下：

![條件變異數基準計算公式](assets/amazon-cond-variance-calc-1.png)

## 範例

條件變異數設定如下：

![條件變異數設定範例](assets/amazon-cond-variances.png)

- BMC = 100 （競爭者條件=新增）
- MCV = 80 （商家條件=已使用；良好）
- BMP = $7.99 （基本比對價格=相符競爭條件的最低價格）

![條件變異數基準計算範例](assets/amazon-cond-variance-calc-2.png)

使用上述的條件差異基準計算，您的條件差異基準= $6.39。此計算方式是價格規則動作所使用的競爭者價格來源，詳情請參閱 [價格調整](./price-adjustment.md).
