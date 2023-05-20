---
title: 價格調整
description: 設定價格調整，以便在您識別Amazon競爭者價格來源時定義價格計算。
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 價格調整

>[!NOTE]
>
>「價格調整」區段在「標準」與「智慧」重新訂價規則上稍有不同。 **[!UICONTROL Match Competitor Price]** 僅適用於 _[!UICONTROL Price Action]_時間&#x200B;**[!UICONTROL Rule Type]**設為 `Intelligent repricing rule`.

智慧型重新訂價規則的區段包括：

- [選取規則型別](./intelligent-repricing-rules.md)
- [競爭者條件差異](./competitor-conditional-variances.md)
- 價格調整
- [底價](./floor-price.md)
- [選擇性最高價格](./optional-ceiling-price.md)

當您識別競爭者的價格來源時，價格調整會定義價格計算。

## 設定價格調整

在「 」中定義您的訂價調整 _[!UICONTROL Price Adjustment]_區段。

1. 對象 **[!UICONTROL Price Action]**，選擇一個選項：

   - `Decrease By`  — 選擇您要在將定義的價格來源值向下調整的時間，為規則建立較低的價格，然後再列示至Amazon。

   - `Increase By`  — 選擇您要在何時調整已定義的價格來源值，以便為規則建立較高的價格，然後再列示至Amazon。

   - `Match Competitor Price` - （僅限智慧型重新訂價規則）選擇何時要變更Amazon清單價格以符合 [最低競爭者](./lowest-competitor-pricing.md) 價格，根據競爭者的意見反應和差異引數而定。 當設定為 `Match Competitor Price`，則 _[!UICONTROL Apply]_和_[!UICONTROL Adjustment Amount]_ 欄位會被移除。

1. 對象 **[!UICONTROL Apply]**，選擇一個選項：

   - `Apply as percentage`  — 選擇您想要定義何時 **[!UICONTROL Magento Price Source]** 在中定義 [清單價格](./listing-price.md) 以百分比調整。

   - `Apply as fixed amount`  — 選擇您想要定義何時 **[!UICONTROL Magento Price Source]** 在中定義 [清單價格](./listing-price.md) 依固定金額調整。

1. 對象 **[!UICONTROL Adjustment Amount]** （必要），輸入價格調整的數值。

   - 時間 **[!UICONTROL Apply]** 設為 `Apply as percentage`，輸入百分比值(範例：輸入 `25` 25%的調整)。

   - 時間 **[!UICONTROL Apply]** 設為 `Apply as fixed amount`，輸入固定金額的數值(範例： enter `25` 25美元的固定調整)。

![智慧型重新訂價規則 — 價格調整](assets/amazon-price-adjustment.png)

| 欄位 | 說明 |
|---|---|
| [!UICONTROL Price Action] | 選擇訂價調整作業。 選項：<br>**[!UICONTROL Decrease By]**— 選擇您想要定義何時 _[!UICONTROL Magento Price Source]_在中定義 [清單價格](./listing-price.md) 向下調整，在列為Amazon之前，降低規則的價格。<br>**[!UICONTROL Increase By]**— 選擇您想要定義何時_[!UICONTROL Magento Price Source]_ 在中定義 [清單價格](./listing-price.md) 即將調整，在列為Amazon之前，為規則建立較高的價格。<br>**[!UICONTROL Match Competitor Price]**- （僅限智慧型重新訂價規則）選擇何時要變更Amazon清單價格以符合 [最低競爭者](./lowest-competitor-pricing.md) 價格，根據競爭者的意見反應和差異引數而定。 選擇後， _套用_ 和 _調整金額_ 欄位會被移除。 |
| [!UICONTROL Apply] | 選項：<br>**[!UICONTROL Apply as percentage]**— 選擇您想要定義何時 _[!UICONTROL Magento Price Source]_在中定義 [清單價格](./listing-price.md) 以百分比調整。<br>**[!UICONTROL Apply as fixed amount]**— 選擇您想要定義何時_[!UICONTROL Magento Price Source]_ 在中定義 [清單價格](./listing-price.md) 依固定金額調整。 |
| [!UICONTROL Adjustment Amount] | 必填。<br>如果您選擇 `Apply as percentage` 的 **[!UICONTROL Apply]**，輸入百分比值(範例：輸入 `25` 25%的調整)。<br>如果您選擇 `Apply as fixed amount` 的 **[!UICONTROL Apply]**，輸入固定金額的數值(範例： enter `25` 25美元的固定調整)。 |
