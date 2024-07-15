---
title: Amazon sales channel — 价格优先级逻辑
description: Amazon sales channel在确定Amazon列表的已发布价格时应用优先次序。
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---

# 价格优先级逻辑

在以下示例中，系统如何确定您应发布$31.99、$24.99还是$27.99？

![Commerce价格范围](assets/amazon-price-scope.png){width="400"}

要确定产品在两个网站上并且每个网站的价格不同时使用哪个价格，请使用价格优先级逻辑（由[排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)值确定）。

要查看商店的排序顺序，请在&#x200B;_管理员_&#x200B;侧边栏中转到&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL All Stores]**。 在&#x200B;_[!UICONTROL Web Site]_列中，单击网站名称。_[!UICONTROL Web Site Information]_&#x200B;页面显示网站的&#x200B;_[!UICONTROL Sort Order]_设置，该设置决定了网站的优先级。 值`1`表示最高优先级。

如果产品价格设置为`Use Default`，则它回退到默认价格值，而不是网站价格值。

## 示例1

|         | 网站优先级 | 价格（网站） | 使用默认值 |
|---------|------------------|-----------------|-------------|
| 默认 | 0 | 31.99美元 | — |
| 商店1 | 1 | 24.99美元 | 否 |
| 商店2 | 2 | 27.99美元 | 是 |

- **[!UICONTROL Magento Price Source]**（在您的[列表价格](./listing-price.md)中定义）设置为`Price`属性。
- 查看网站优先级最高的网站，即商店1（由[排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)值定义）。
- 由于商店1设置为使用网站价格（使用默认值=否），因此发布的价格为24.99美元。

## 示例2

|         | 网站优先级 | 价格网站 | 使用默认值 |
|---------|------------------|---------------|-------------|
| 默认 | 0 | 31.99美元 | — |
| 商店1 | 1 | 24.99美元 | 是 |
| 商店2 | 2 | 27.99美元 | 否 |

- **[!UICONTROL Magento Price Source]**（在您的[列表价格](./listing-price.md)中定义）设置为`Price`属性。
- 查看网站优先级最高的网站，即商店1（由[排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)值定义）。
- 由于商店1 **未设置为使用网站价格（使用默认值=是），请按照排序顺序查看下一个网站。**
- 由于商店2的&#x200B;**为**，且设置为使用网站价格（使用默认值=否），因此发布的价格为$27.99。

## 示例3

|         | 网站优先级 | 价格网站 | 使用默认值 |
|---------|------------------|---------------|-------------|
| 默认 | 0 | 31.99美元 | 30.00美元 |
| 商店1 | 1 | 24.99美元 | — |
| 商店2 | 2 | 27.99美元 | 20.00美元 |

此示例添加非价格值，如果您为_[!UICONTROL Magento Price Source_]选择另一个值（在您的[列表价格](./listing-price.md)设置中定义），则会使用此值。 非价格值始终使用价格作为回退价格。

- **[!UICONTROL Magento Price Source]**（在[[!UICONTROL Listing Price]](./listing-price.md)设置中定义）设置为`Non-Price`。
- 查看网站优先级最高的网站，其优先级为`Store 1`（由[排序顺序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)值定义）。
- 由于商店1 **未设置为使用`Non-Price`属性，请按照排序顺序查看下一个网站。**
- 由于商店2的&#x200B;**是**&#x200B;且设置为使用`Non-Price`属性（非价格[网站] = $20.00），因此发布的价格为$20.00。
