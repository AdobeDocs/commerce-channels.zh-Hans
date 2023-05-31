---
title: '智能重新定价规则：最低价格'
description: 使用最低价格设置确定用于管理Amazon清单的智能定价规则的最低价格。
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# 智能重新定价规则：底价

智能重新定价规则的部分包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

此 [底价](./floor-price.md) 设置会自动根据智能定价规则保护您的最低产品价格。 使用这些设置为您的智能定价规则设置下限（最低价格），确保您的产品不会低于所需的价格。

在以下情况下，最低价格属性基于网站范围： [!DNL Commerce] 商店正在使用网站定价范围。 参见 [价格范围](./price-scope.md).

只有符合以下条件时才使用最低价格 **[!UICONTROL Rule Type]** 设置为 `Intelligent repricing rule`.

## 配置底价

在中定义最低价格设置 _[!UICONTROL Floor Price]_部分。

1. 对象 **[!UICONTROL Floor Price Source]**&#x200B;中，选择价格来源属性。

   选择 [!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) 表示你的相对下限。 例如，如果您不希望自己的Amazon挂牌价低于商品成本，则可以选择 *成本* 属性。

1. 对象 **[!UICONTROL Floor Price Action]**，选择一个选项。

   - `Decrease By`  — 选择何时需要定义的 _[!UICONTROL Floor Price Source]_价值进行向下调整，从而降低规则的最低价格，然后才可挂牌到Amazon。

   - `Increase By`  — 选择何时需要定义的 _[!UICONTROL Floor Price Source]_价值调整，从而为规则创造更高的底价，然后再将价格挂牌到Amazon。

   - `Match`  — 选择您不希望上市价格波动低于所定义价格的时间 _[!UICONTROL Floor Price Source]_值。 当设置为 `Match`，则_[!UICONTROL Apply]_ 和 _[!UICONTROL Floor Adjustment Amount]_字段被禁用。

1. 保留 **[!UICONTROL Apply]** 默认为 `Apply as percentage`.

1. 对象 **[!UICONTROL Floor Adjustment Price]**，输入百分比的数字值以调整 _[!UICONTROL Floor Price Source]_值。

在本例中，底价设置为比物料成本高3%。

![智能重新定价规则示例 — 最低价格](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Floor Price Source] | 选择 [!DNL Commerce] 指示相对下限（最低价格）限制的属性。 例如，如果您不希望自己的Amazon挂牌价低于商品成本，则可以选择 `Cost` 属性。 |
| [!UICONTROL Floor Price Action] | 选择定价调整活动。 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择何时需要定义的 _[!UICONTROL Floor Price Source]_价值进行向下调整，从而降低规则的最低价格，然后才可挂牌到Amazon。</li><li>**[!UICONTROL Increase By]**  — 选择何时需要定义的 _[!UICONTROL Floor Price Source]_价值调整，从而为规则创造更高的底价，然后再将价格挂牌到Amazon。</li><li>**[!UICONTROL Match]**  — 选择您不希望上市价格波动低于所定义价格的时间 _[!UICONTROL Floor Price Source]_值。 选择后，_[!UICONTROL Apply]_ 和 _[!UICONTROL Floor Adjustment Amount]_字段被禁用。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 相对于 _[!UICONTROL Floor Price Source]_值。 |
| [!UICONTROL Floor Adjustment Amount] | 输入百分比的数字值，以调整 _[!UICONTROL Floor Price Source]_值。 |
