---
title: 價格規則範例
description: 若要協助您為Amazon清單設計定價規則，請根據常見案例檢閱這些範例。
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 價格規則範例

## 標準價格規則範例

### 捨棄後續規則

捨棄後續規則的功能是定價規則內的一項絕佳功能，可防止多個定價規則棧疊並提供意想不到的額外折扣。 若要捨棄後續規則，訂價規則必須使用 _[!UICONTROL Priority]_部分 [訂價規則一般設定](./pricing-rule-general-settings.md).

若 **[!UICONTROL Discard Subsequent Rules]** 設為 `Yes`，優先順序較低（數字較高）的規則不適用於合格產品。

例如，假設有三個定價規則：

| 範例 | 規則名稱 | 優先順序 | 捨棄後續規則 |
|----------|----|----|----|
| 1 | 優惠季產品10%優惠 | 1 | 否 |
| 2 | 優惠價$2的銷售產品 | 2 | 是 |
| 3 | 所有產品5%優惠 | 3 | 否 |

在此案例中，規則#1和#2適用於合格產品。 規則#3只適用於規則#2中未包含的合格產品，因為其優先順序低於範例#2和 **[!UICONTROL Discard Subsequent Rules]** 設為 `Yes`. 因此，銷售類別中符合資格的產品可享有10%的折扣，以及Amazon掛牌價的$2優惠。

### 套用兩個標準價格規則

| 欄位 | 設定 — 規則1 | 設定 — 規則2 |
|----------|----|----|
| [!UICONTROL Rule Name] | 規則–1 | 規則–2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 標準價格規則 | 標準價格規則 |
| [!UICONTROL Price action] | 減少依據 | 減少依據 |
| [!UICONTROL Apply] | 以百分比套用 | 套用為固定金額 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 產品1

價格：45.49美元

套用規則1：$45.49 x (0.9) = $40.94

套用規則2：$40.94 - $10.00 = $30.94

套用規則1和規則2後的最終價格：$30.94

#### 產品2

價格：47.76美元

套用規則1：$47.76 x (0.9) = $42.98

套用規則2：$42.98 - $10.00 = $32.98

套用規則1和規則2後的最終價格： $32.98

## 智慧型重新訂價規則範例

### 具有底價來源的Buy Box價格=價格

| 欄位 | 設定 |
|----------|----|
| [!UICONTROL Rule Name] | 規則–1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智慧型重新訂價規則 |
| [!UICONTROL Competitor Price Source] | 使用「Buy Box」價格 |
| [!UICONTROL Price Action] | 比對競爭者價格 |
| [!UICONTROL Floor Price Source] | 價格 |
| [!UICONTROL Floor Price Action] | 符合 |

#### 產品1

價格：15美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon價格： 10美元

因為 [Buy Box](./buy-box-competitor-pricing.md) 價格低於原始價格，產品會以原始價格列出。

套用規則後的最終價格： $15

#### 產品2

價格：5美元

[Buy Box](./buy-box-competitor-pricing.md) Amazon價格： 10美元

因為 [Buy Box](./buy-box-competitor-pricing.md) 價格高於原始價格，產品會列在 [Buy Box](./buy-box-competitor-pricing.md) 價格。

套用規則後的最終價格： $10

### 具有底價來源的Buy Box價格=價格與20%的價格下降

| 欄位 | 設定 |
|----------|----|
| [!UICONTROL Rule Name] | 規則–1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智慧型重新訂價規則 |
| [!UICONTROL Competitor Price Source] | 使用「Buy Box」價格 |
| [!UICONTROL Price Action] | 比對競爭者價格 |
| [!UICONTROL Floor Price Source] | 價格 |
| [!UICONTROL Floor Price Action] | 減少依據 |
| [!UICONTROL Apply] | 以百分比套用 |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### 產品1

價格：$20

計算底價：$16

[Buy Box](./buy-box-competitor-pricing.md) Amazon價格： 15美元

因為 [Buy Box](./buy-box-competitor-pricing.md) 價格小於計算值 [底價](./floor-price.md)，則產品會列在「已計算」 [底價](./floor-price.md).

套用規則後的最終價格： $16

#### 產品2

價格：15美元

已計算 [底價](./floor-price.md)： $12

[Buy Box](./buy-box-competitor-pricing.md) Amazon價格： 15美元

因為 [Buy Box](./buy-box-competitor-pricing.md) 價格大於計算值 [底價](./floor-price.md)，此產品會列於 [Buy Box](./buy-box-competitor-pricing.md) 價格。

套用規則後的最終價格： $15

#### 產品3

價格：17美元

計算底價：$13.60

[Buy Box](./buy-box-competitor-pricing.md) Amazon價格： 15美元

因為 [Buy Box](./buy-box-competitor-pricing.md) 價格大於計算值 [底價](./floor-price.md)，此產品會列於 [Buy Box](./buy-box-competitor-pricing.md) 價格。

套用規則後的最終價格： $15

### 最低價格（包含所有競爭者的價格）並使用所有競爭者的產品條件

| 欄位 | 設定 |
|----------|-----|
| [!UICONTROL Rule Name] | 規則–1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | 智慧型重新訂價規則 |
| [!UICONTROL Competitor Price Source] | 使用最低競爭者價格 |
| [!UICONTROL Minimum Positive Feedback] | 所有競爭者價格 |
| [!UICONTROL Conditional Variance] | 使用所有競爭者的產品條件 |
| [!UICONTROL Price Action] | 比對競爭者價格 |
| [!UICONTROL Floor Price Source] | 價格 |
| [!UICONTROL Floor Price Action] | 符合 |

| 價格 | 條件 |
|----------|----|
| $17 | 新增 |
| $15 | 新增 |
| $14 | 已使用；非常好 |
| $13 | 已使用；良好 |

#### 產品1

價格：$10

條件：新增

因為新條件的最低競爭者價格是$15，所以產品價格為$15。

套用規則後的最終價格： $15

#### 產品2

價格：$10

條件：已使用；可接受

因為 [最低競爭者價格](./lowest-competitor-pricing.md) 若已使用條件為$13，則產品價格為$13。

套用規則後的最終價格： $13

### 結合最高價格、幣別兌換及VAT的智慧型重新訂價規則

| 欄位 | 設定 |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1.25歐元：1美元 |

[最高價格](./optional-ceiling-price.md) 歐洲(VAT)市場：$10 x 1.25 = $12.50

當 [最高價格](./optional-ceiling-price.md) 在歐洲(VAT)市場中，會計算並新增VAT。

加值後最終價格：$12.50 x (1.1) = $13.75

### 結合多重訂價規則、最高價格、幣別換算及VAT

#### 智慧型定價規則（來自上一個範例）

| 欄位 | 設定 |
|----------|----|
| 優先順序 | 1 |
| VAT | 10% |
| 最高價格來源 | $10 |
| 貨幣轉換 | 1.25歐元：1美元 |

[最高價格](./optional-ceiling-price.md) 歐洲(VAT)市場：$10 x 1.25 = $12.50

加值後最終價格：$12.50 x (1.1) = $13.75

#### 標準訂價規則

| 欄位 | 設定 |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 增加方式 |
| [!UICONTROL Apply] | 套用為固定金額 |
| [!UICONTROL Adjustment Amount] | $5.00 |

當 [最高價格](./optional-ceiling-price.md) 點選，標準訂價規則會套用至智慧型訂價規則之上。

套用標準訂價規則後的最終價格：$13.75 + $5.00 = $18.75

### 價格調整

在此範例中，最具競爭力的價格是透過檢視Amazon來定義 [競爭者的最低價格](./lowest-competitor-pricing.md) 正面意見佔95%，最低數量為1,000個商家評論。

![價格調整範例](assets/amazon-price-adjustment-example.png)

根據這些引數執行搜尋後，競爭性價格會回到$25。

從這裡開始，有三個不同的 [價格規則動作](./pricing-rule-actions.md) 根據此最低價格進行選擇。

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Price Action] | 選項：<ul><li>**[!UICONTROL Decrease By]**  — 此選項會降低您的上市價格，相對於 [最低競爭者價格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]**  — 此選項會提高您的掛牌價格，相對於 [最低競爭者價格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]**  — 此選項會根據引數變更您的Amazon上市價格，以符合最低價格。 在範例中，Amazon的掛牌價為$25。</li></ul> |
| [!UICONTROL Apply] | 選項：以百分比沖銷/以固定金額沖銷 |
| [!UICONTROL Adjustment Amount] | 用於定義要套用之折扣的百分比或固定金額的數值。 <br>這些選擇會產生最低價格，並將其設定為減少$0.01。 |

### 底價

| 欄位 | 設定 |
|----------|----|
| [!UICONTROL Floor Price Source] | 成本= $5 |
| [!UICONTROL Floor Price Action] | 增加方式 |
| [!UICONTROL Apply] | 以百分比套用 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[底價](./floor-price.md) 計算=底價來源 `$5` x下限調整金額 `5%` = $5.25

套用智慧型定價規則時，當成本為$5美元時，可允許此特定產品的掛牌價低於$5.25。
