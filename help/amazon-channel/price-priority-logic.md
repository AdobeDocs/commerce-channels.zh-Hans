---
title: Amazon sales channel — 价格优先级逻辑
description: Amazon sales channel在确定Amazon列表的已发布价格时应用优先顺序。
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 4%

---

# 价格优先级逻辑

在以下示例中，系统如何确定您应发布$31.99、$24.99还是$27.99？

![商业价格范围](assets/amazon-price-scope.png){width="400"}

要确定当产品位于两个网站上并且每个网站的价格不同时使用哪个价格，请使用价格优先级逻辑(由以下参数确定 [排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 值)。

要查看商店的排序顺序，请转到 **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** 在 _管理员_ 侧栏。 在 _[!UICONTROL Web Site]_列中，单击网站名称。 此_[!UICONTROL Web Site Information]_ 页面显示 _[!UICONTROL Sort Order]_网站的设置，它确定网站的优先级。 值 `1` 表示最高优先级。

如果产品价格设置为 `Use Default`，它会返回默认价格值，而不是网站价格值。

## 示例1

|         | 网站优先级 | 价格（网站） | 使用默认值 |
|---------|------------------|-----------------|-------------|
| 默认 | 0 | $31.99 | -- |
| 商店1 | 1 | $24.99 | 否 |
| 商店2 | 2 | $27.99 | 是 |

- 此 **[!UICONTROL Magento Price Source]** （在中定义） [挂牌价](./listing-price.md) 设置为 `Price` 属性。
- 查看网站优先级最高的网站，即“商店1”(由 [排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 值)。
- 由于商店1设置为使用网站价格（使用默认值=否），因此公布价格为24.99美元。

## 示例2

|         | 网站优先级 | 价格网站 | 使用默认值 |
|---------|------------------|---------------|-------------|
| 默认 | 0 | $31.99 | -- |
| 商店1 | 1 | $24.99 | 是 |
| 商店2 | 2 | $27.99 | 否 |

- 此 **[!UICONTROL Magento Price Source]** （在中定义） [挂牌价](./listing-price.md) 设置为 `Price` 属性。
- 查看网站优先级最高的网站，即“商店1”(由 [排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 值)。
- 自从商店1 **不是** 设置为使用网站价格（使用默认值=是），请按排序顺序查看下一个网站。
- 自从商店2 **是** 设置为使用网站价格（使用默认值=否），发布的价格为$27.99。

## 示例3

|         | 网站优先级 | 价格网站 | 使用默认值 |
|---------|------------------|---------------|-------------|
| 默认 | 0 | $31.99 | $30.00 |
| 商店1 | 1 | $24.99 | -- |
| 商店2 | 2 | $27.99 | $20.00 |

此示例添加非价格值，如果您为_选择其他值，则会使用此值[!UICONTROL Magento Price Source_] （在中定义） [挂牌价](./listing-price.md) 设置)。 非价格值始终使用价格作为回退价格。

- 此 **[!UICONTROL Magento Price Source]** (在中定义 [[!UICONTROL Listing Price]](./listing-price.md) settings)设置为 `Non-Price`.
- 查看网站优先级最高的网站，即 `Store 1`(由定义 [排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 值)。
- 自从商店1 **不是** 设置为使用 `Non-Price` 属性，按照排序顺序查看下一个网站。
- 自从商店2 **是** 设置为使用 `Non-Price` 属性（非价格） [网站] = $20.00)，发布的价格为$20.00。
