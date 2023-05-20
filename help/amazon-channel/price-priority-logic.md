---
title: 價格優先順序邏輯
description: Amazon sales channel會套用優先順序來決定Amazon清單的已公佈價格。
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 4%

---

# 價格優先順序邏輯

在下列範例中，系統如何判斷您應發佈$31.99、$24.99或$27.99？

![商務價格範圍](assets/amazon-price-scope.png)

若要判斷當產品位於兩個網站上且每個網站的價格各有不同時，所使用的價格，請使用價格優先順序邏輯(由以下專案決定： [排序順序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target="_blank"} 值)。

若要檢視商店的排序順序，請前往 **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** 在 _管理員_ 側欄。 在 _[!UICONTROL Web Site]_欄中，按一下網站名稱。 此_[!UICONTROL Web Site Information]_ 頁面顯示 _[!UICONTROL Sort Order]_網站的設定，可決定網站的優先順序。 值 `1` 表示最高優先順序。

如果產品價格設為 `Use Default`，會回覆為預設價格值，而非網站價格值。

## 範例1

|  | 網站優先順序 | 價格（網站） | 使用預設值 |
|---|---|---|---|
| 預設 | 0 | $31.99 | -- |
| 商店1 | 1 | $24.99 | 否 |
| 商店2 | 2 | $27.99 | 是 |

- 此 **[!UICONTROL Magento Price Source]** (定義於 [清單價格](./listing-price.md) 設為 `Price` 屬性。
- 檢視網站優先順序最高的網站，也就是「商店1」(由 [排序順序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target="_blank"} 值)。
- 由於「商店1」設為使用網站價格（使用預設值=否），因此公佈價格為$24.99美元。

## 範例2

|  | 網站優先順序 | 價格網站 | 使用預設值 |
|---|---|---|---|
| 預設 | 0 | $31.99 | -- |
| 商店1 | 1 | $24.99 | 是 |
| 商店2 | 2 | $27.99 | 否 |

- 此 **[!UICONTROL Magento Price Source]** (定義於 [清單價格](./listing-price.md) 設為 `Price` 屬性。
- 檢視網站優先順序最高的網站，也就是「商店1」(由 [排序順序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target="_blank"} 值)。
- 自從商店1 **不是** 設定為使用網站價格（使用預設值=是），以排序順序檢視下一個網站。
- 自從商店2 **是** 設定為使用網站價格（使用預設值=否），則公佈價格為$27.99。

## 範例3

|  | 網站優先順序 | 價格網站 | 使用預設值 |
|---|---|---|---|
| 預設 | 0 | $31.99 | $30.00 |
| 商店1 | 1 | $24.99 | -- |
| 商店2 | 2 | $27.99 | $20.00 |

此範例新增非價格值，如果您為_選取其他值，則會使用此值[!UICONTROL Magento Price Source_] (定義於 [清單價格](./listing-price.md) 設定)。 非價格值一律會使用價格作為遞補價格。

- 此 **[!UICONTROL Magento Price Source]** (定義於 [[!UICONTROL Listing Price]](./listing-price.md) settings)設為 `Non-Price`.
- 檢視網站優先順序最高的網站，也就是 `Store 1`(定義於 [排序順序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target="_blank"} 值)。
- 自從商店1 **不是** 設定為使用 `Non-Price` 屬性，以排序順序檢視下一個網站。
- 自從商店2 **是** 設定為使用 `Non-Price` 屬性（非價格） [網站] = $20.00)，公佈價格為$20.00。
