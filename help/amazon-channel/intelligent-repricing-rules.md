---
title: 「智慧型重新訂價規則：選取規則型別」
description: 建立智慧型重新訂價規則，根據競爭者的定價來決定您的Amazon清單價格。
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# 智慧型重新訂價規則：選取規則型別

>[!IMPORTANT]
>
>如果Amazon區域設為，智慧型重新定價規則就無法正常運作 `Inactive` 狀態，就像在上線期間一樣。 您的訂價計算取決於您的運費，而且您的地區必須位於 `Active` 要從Amazon同步的運費狀態。<br><br>
>
>若要更新Amazon帳戶中的地區狀態，請前往「設定>帳戶資訊>假期設定」。 請參閱 [Amazon：休假的清單狀態](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

智慧型重新定價規則會使用Amazon競爭者的定價來決定您的掛牌價格。 競爭對手是在Amazon上列出與您相同的產品的其他銷售商。

智慧型重新訂價規則的區段包括：

- 選取規則型別
- [競爭者條件差異](./competitor-conditional-variances.md)
- [價格調整](./price-adjustment.md)
- [底價](./floor-price.md)
- [選擇性最高價格](./optional-ceiling-price.md)

## 設定規則型別

在中定義規則型別 _[!UICONTROL Select Rule Type]_區段。

1. 對象 **[!UICONTROL Rule Type]**，選擇 `Intelligent repricing rule`.

   此設定會啟用 _[!UICONTROL Competitor Price Source]_欄位和 [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md)， [_[!UICONTROL Floor Price]_](./floor-price.md)、和 [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) 區段。

1. 對象 **[!UICONTROL Competitor Price Source]**，選擇一個選項：

   - **[!UICONTROL Use "Buy Box" Price]**  — 選擇您想要根據Amazon調整Amazon定價的時間 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 賣家價格。 A [!DNL Buy Box] 當Amazon上有多個賣家提供相同的產品時，就會出現價格。 Amazon定義 [!DNL Buy Box] 根據效能需求決定賣家。 商戶尋求贏得 [!DNL Buy Box] 賣家狀態並提供其產品清單的最大可見度。

   - **[!UICONTROL Use Lowest Competitor Price]**  — 選擇您要比較並調整相同產品的上市價格與競爭者訂價的時間。 選擇後， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 欄位已啟用。

1. 如果已啟用，請選擇選項 **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]**  — 選擇何時要根據相同產品的所有競爭者價格，比較並調整您的價格。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 選擇何時要限制與相同產品價格比較的競爭對手。 此設定可進一步縮小競爭者的範圍，方法是在套用最低價格規則前，要求他們的清單至少要有所選正反饋的百分比。

1. 如果已啟用，請輸入數值 **[!UICONTROL Minimum Feedback Count]**.

   此選擇性數值可進一步縮小具競爭力的價格。 例如，如果商家有95%的正面的意見反應評分，但只有意見反應計數 `20`，可能不是您想要修改其定價的競爭對手。 不過，如果您輸入的值為 `1000`，要求商家有95%的正面意見回饋，以及至少1000個商家評論。

>[!NOTE]
>
>您可以使用這些競爭者定價和意見回饋選項，避免讓您的定價以意見回饋差且銷售品質較低產品的競爭者為依據。

![智慧型重新訂價規則 — 選取規則型別](assets/ob-intelligent-price-rule-type.png)

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Rule Type] | 選取規則型別。 選項：<ul><li>**[!UICONTROL Standard price rule]**  — 此規則型別可讓您以特定百分比或相對於下列專案的固定金額增加或減少Amazon掛牌價格： _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]**  — 此規則型別可讓您根據競爭者的定價調整您的Amazon上市價格。 選擇後， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 欄位已啟用。</li></ul> |
| [!UICONTROL Competitor Price Source] | 選取所需的價格來源。 選項：<ul><li>**[!UICONTROL Use "Buy Box" Price]**  — 當您想要根據Amazon調整Amazon定價時，請選擇此選項 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 賣家價格。 A [!DNL Buy Box] 當Amazon上有多個賣家提供相同的產品時，就會出現價格。 Amazon定義 [!DNL Buy Box] 根據效能需求決定賣家。 商戶尋求贏得 [!DNL Buy Box] 賣家狀態並提供其產品清單的最大可見度。</li><li>**[!UICONTROL Use Lowest Competitor Price]**  — 當您想要比較並調整您的上市價格時，請選擇此選項 [最低競爭者價格](./lowest-competitor-pricing.md) 相同的產品。 選擇後， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 欄位已啟用。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 僅在以下情況下有效： `Use Lowest Competitor Price` 已選取。 選項：<ul><li>**[!UICONTROL All Competitor's Prices]**  — 選擇何時要根據相同產品的所有競爭者價格，比較並調整您的價格。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 選擇何時要限制您與之比較的競爭對手，並調整您的定價。 此設定會進一步縮小您的競爭對手，要求他們的清單具有最低選定百分比的正面回饋，然後使用該競爭對手子集的最低價格。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 僅在以下情況下有效： `Use Lowest Competitor Price` 已選取。 此選擇性數值可進一步縮小具競爭力的價格比較。 例如，如果商家有95%的正面的意見反應評分，但只有意見反應計數 `20`，可能不是您想要修改其定價的競爭對手。 不過，如果您輸入的值為 `1000`，要求商家有95%的正面意見回饋，以及至少1000個商家評論。 |
