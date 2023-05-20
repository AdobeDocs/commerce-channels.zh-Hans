---
title: 「智慧型重新訂價規則：底價」
description: 使用底價設定來決定智慧型訂價規則的最低價格，以管理您的Amazon清單。
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 智慧型重新訂價規則：底價

智慧型重新訂價規則的區段包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

此 [底價](./floor-price.md) 設定會自動根據智慧型定價規則保護您的最低產品價格。 使用這些設定來設定智慧型訂價規則的下限（最低價格），確保您的產品不會列在所需價格之下。

若您符合以下條件，則底價屬性會以網站範圍為基礎： [!DNL Commerce] 商店正在使用網站定價範圍。 另請參閱 [價格範圍](./price-scope.md).

底價僅用於 **[!UICONTROL Rule Type]** 設為 `Intelligent repricing rule`.

## 設定底價

在下列欄位中定義您的最低價格設定： _[!UICONTROL Floor Price]_區段。

1. 對象 **[!UICONTROL Floor Price Source]**，選擇價格來源屬性。

   選擇 [!DNL Commerce] [產品屬性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} 表示您的相對樓層限制。 例如，如果您不想讓Amazon的清單價格低於專案的成本，您可以選擇 *成本* 屬性。

1. 對象 **[!UICONTROL Floor Price Action]**，選擇一個選項。

   - `Decrease By`  — 選擇您想要定義何時 _[!UICONTROL Floor Price Source]_值會向下調整，為規則建立較低的底價，然後再列為Amazon。

   - `Increase By`  — 選擇您想要定義何時 _[!UICONTROL Floor Price Source]_值進行調整，為規則建立較高的底價，然後再列為Amazon。

   - `Match`  — 選擇您不想讓清單價格波動到低於所定義價格的時間 _[!UICONTROL Floor Price Source]_值。 當設定為 `Match`，則_[!UICONTROL Apply]_ 和 _[!UICONTROL Floor Adjustment Amount]_欄位已停用。

1. 離開 **[!UICONTROL Apply]** 預設為 `Apply as percentage`.

1. 對象 **[!UICONTROL Floor Adjustment Price]**，輸入百分比的數值，以調整您的 _[!UICONTROL Floor Price Source]_值。

在此範例中，底價設定為高於料號成本3%。

![智慧型重新訂價規則範例 — 底價](assets/ob-intelligent-pricde-rule-floor-price.png)

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Floor Price Source] | 選擇 [!DNL Commerce] 指出您相對下限（最低價格）限制的屬性。 例如，如果您不想讓Amazon的清單價格低於專案的成本，您可以選擇 `Cost` 屬性。 |
| [!UICONTROL Floor Price Action] | 選擇訂價調整作業。 選項：<ul><li>**[!UICONTROL Decrease By]**  — 選擇您想要定義何時 _[!UICONTROL Floor Price Source]_值會向下調整，為規則建立較低的底價，然後再列為Amazon。</li><li>**[!UICONTROL Increase By]**  — 選擇您想要定義何時 _[!UICONTROL Floor Price Source]_值進行調整，為規則建立較高的底價，然後再列為Amazon。</li><li>**[!UICONTROL Match]**  — 選擇您不想讓清單價格波動到低於所定義價格的時間 _[!UICONTROL Floor Price Source]_值。 選擇後，_[!UICONTROL Apply]_ 和 _[!UICONTROL Floor Adjustment Amount]_欄位已停用。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 相對於 _[!UICONTROL Floor Price Source]_值。 |
| [!UICONTROL Floor Adjustment Amount] | 輸入百分比的數值，以調整您的 _[!UICONTROL Floor Price Source]_值。 |
