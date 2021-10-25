---
title: Price Priority Logic
description: Amazon销售渠道在确定Amazon上市的已发布价格时应用优先级。
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# 价格优先级逻辑

在以下示例中，系统如何确定您应发布31.99美元、24.99美元还是27.99美元？

![商业价格范围](assets/amazon-price-scope.png)

要确定产品在两个网站上使用的价格，并且每个网站的价格不同，请使用价格优先级逻辑(由 [排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}值)。

要查看商店的排序顺序，请转到 **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** 在 _管理员_ 侧栏。 在 _[!UICONTROL Web Site]_列中，单击网站名称。 的_[!UICONTROL Web Site Information]_ 页面 _[!UICONTROL Sort Order]_为网站设置，该设置可确定网站的优先级。 A value of `1` indicates the highest priority.

If the product price is set to `Use Default`, it falls back to the default price value instead of the website price value.

## Example 1

|  | 网站优先级 | Price (Website) | Use Default |
|---|---|---|---|
| Default | 0 | US$31.99 | — |
| 商店1 | 1 | US$24.99 | 否 |
| 商店2 | 2 | US$27.99 | 是 |

- 的 **[!UICONTROL Magento Price Source]** (在 [上市价格](./listing-price.md) 设置为 `Price` 属性。
- 查看网站优先级最高的网站，即商店1(由 [排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}值)。
- 由于“商店1”设置为使用网站价格（使用默认值=否），因此发布价格为$24.99。

## 示例2

|  | 网站优先级 | 价格网站 | 使用默认值 |
|---|---|---|---|
| 默认 | 0 | US$31.99 | — |
| 商店1 | 1 | $24.99 | 是 |
| Store 2 | 2 | US$27.99 | 否 |

- 的 **[!UICONTROL Magento Price Source]** (在 [上市价格](./listing-price.md) 设置为 `Price` 属性。
- 查看网站优先级最高的网站，即商店1(由 [排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;}值)。
- Since Store 1 **is not** set to use the website price (Use Default = Yes), look at the next website in the sort order.
- Since Store 2 **is** set to use the website price (Use Default = No), the published price is $27.99.

## 示例3

|  | Website Priority | 价格网站 | Use Default |
|---|---|---|---|
| 默认 | 0 | $31.99 | US$30.00 |
| 商店1 | 1 | US$24.99 | — |
| 商店2 | 2 | US$27.99 | US$20.00 |

此示例添加了非价格值，如果您为_选择其他值，则会使用该值[!UICONTROL Magento Price Source_] (在 [上市价格](./listing-price.md) 设置)。 非价格值始终使用价格作为回退价格。

- 的 **[!UICONTROL Magento Price Source]** (在 [[!UICONTROL Listing Price]](./listing-price.md) 设置) `Non-Price`.
- Look at the website with the highest website priority, which is `Store 1`(defined by the [Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){target=&quot;_blank&quot;} value).
- 自存储1起 **不是** 设置为使用 `Non-Price` 属性中，按排序顺序查看下一个网站。
- 自存储2起 **is** 设置为使用 `Non-Price` 属性（非价格） [网站] = $20.00)，则发布价格为$20.00。
