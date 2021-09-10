---
title: 价格优先级逻辑
description: Amazon销售渠道在确定Amazon上市的已发布价格时应用优先级。
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# 价格优先级逻辑

在以下示例中，系统如何确定您应发布31.99美元、24.99美元还是27.99美元？

![商业价格范围](assets/amazon-price-scope.png)

要确定在两个网站上使用的产品的价格，并且每个网站的价格不同，请使用价格优先级逻辑（由[排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}值确定）。

要查看您的商店的排序顺序，请转到&#x200B;_Admin_&#x200B;侧栏中的&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL All Stores]**。 在&#x200B;_[!UICONTROL Web Site]_列中，单击网站名称。_[!UICONTROL Web Site Information]_&#x200B;页面显示网站的&#x200B;_[!UICONTROL Sort Order]_设置，该设置可确定网站的优先级。 值`1`表示最高优先级。

如果将产品价格设置为`Use Default`，它会回落到默认价格值，而不是网站价格值。

## 示例1

|  | 网站优先级 | 价格（网站） | 使用默认值 |
|---|---|---|---|
| 默认 | 0 | US$31.99 | — |
| 商店1 | 1 | US$24.99 | 否 |
| 商店2 | 2 | US$27.99 | 是 |

- **[!UICONTROL Magento Price Source]**（在[Listing Price](./listing-price.md)中定义）将设置为`Price`属性。
- 查看网站优先级最高的网站，即“商店1”（由[排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}值定义）。
- 由于“商店1”设置为使用网站价格（使用默认值=否），因此发布价格为$24.99。

## 示例2

|  | 网站优先级 | 价格网站 | 使用默认值 |
|---|---|---|---|
| 默认 | 0 | US$31.99 | — |
| 商店1 | 1 | US$24.99 | 是 |
| 商店2 | 2 | US$27.99 | 否 |

- **[!UICONTROL Magento Price Source]**（在[Listing Price](./listing-price.md)中定义）将设置为`Price`属性。
- 查看网站优先级最高的网站，即“商店1”（由[排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}值定义）。
- 由于第1商店&#x200B;**未**&#x200B;设置为使用网站价格（使用默认值=是），请按排序顺序查看下一个网站。
- 由于第2商店&#x200B;**是**，因此将其设置为使用网站价格（使用默认值=否），因此发布价格为$27.99。

## 示例3

|  | 网站优先级 | 价格网站 | 使用默认值 |
|---|---|---|---|
| 默认 | 0 | US$31.99 | US$30.00 |
| 商店1 | 1 | US$24.99 | — |
| 商店2 | 2 | US$27.99 | US$20.00 |

此示例添加了非价格值，如果您为_[!UICONTROL Magento Price Source_]（在[Listing Price](./listing-price.md)设置中定义）选择其他值，则会使用该值。 非价格值始终使用价格作为回退价格。

- **[!UICONTROL Magento Price Source]**（在[[!UICONTROL Listing Price]](./listing-price.md)设置中定义）将设置为`Non-Price`。
- 查看网站优先级最高的网站，即`Store 1`（由[排序顺序](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}值定义）。
- 由于存储1 **未**&#x200B;设置为使用`Non-Price`属性，因此请按排序顺序查看下一个网站。
- 由于Store 2 **是**&#x200B;设置为使用`Non-Price`属性（非价格[Website] = $20.00），因此发布价格为$20.00。
