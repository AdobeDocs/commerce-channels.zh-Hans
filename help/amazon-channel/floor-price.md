---
title: “智能重定价规则：楼价'
description: 使用底价设置来确定用于管理Amazon列表的智能定价规则的最低价格。
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# 智能重定价规则：底价

智能重定价规则的部分包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

的 [底价](./floor-price.md) 设置会自动根据智能定价规则保护您的最低产品价格。 使用这些设置为智能定价规则设置下限（最低价格），以确保您的产品不会低于所需价格。

最低价格属性基于网站范围(如果您的 [!DNL Commerce] 商店使用网站定价范围。 请参阅 [价格范围](./price-scope.md).

最低价格仅在 **[!UICONTROL Rule Type]** 设置为 `Intelligent repricing rule`.

## 配置最低价格

在 _[!UICONTROL Floor Price]_中。

1. 对于 **[!UICONTROL Floor Price Source]**，请选择价格来源属性。

   选择 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}，表示您的相对下限。 例如，如果您不希望Amazon列表价格低于项目成本，则可以选择 *成本* 属性。

1. 对于 **[!UICONTROL Floor Price Action]**，选择一个选项。

   - `Decrease By`  — 选择要定义的时间 _[!UICONTROL Floor Price Source]_值，为规则创建较低的底价，然后再上市至Amazon。

   - `Increase By`  — 选择要定义的时间 _[!UICONTROL Floor Price Source]_值，为规则创建更高的底价，然后再上市至Amazon。

   - `Match`  — 选择您不希望上市价格在定义价格以下波动的时间 _[!UICONTROL Floor Price Source]_值。 当设置为 `Match`,_[!UICONTROL Apply]_ 和 _[!UICONTROL Floor Adjustment Amount]_字段。

1. 离开 **[!UICONTROL Apply]** 默认为 `Apply as percentage`.

1. 对于 **[!UICONTROL Floor Adjustment Price]**，输入百分比的数值以调整 _[!UICONTROL Floor Price Source]_值。

在本例中，底价设置为比项目成本高3%。

![智能重定价规则示例 — 楼价](assets/ob-intelligent-pricde-rule-floor-price.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Floor Price Source] | 选择 [!DNL Commerce] 表示相对下限（最低价格）限制的属性。 例如，如果您不希望Amazon列表价格低于项目成本，则可以选择 `Cost` 属性。 |
| [!UICONTROL Floor Price Action] | 选择定价调整操作。 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择要定义的时间 _[!UICONTROL Floor Price Source]_值，为规则创建较低的底价，然后再上市至Amazon。</li><li>**[!UICONTROL Increase By]**  — 选择要定义的时间 _[!UICONTROL Floor Price Source]_值，为规则创建更高的底价，然后再上市至Amazon。</li><li>**[!UICONTROL Match]**  — 选择您不希望上市价格在定义价格以下波动的时间 _[!UICONTROL Floor Price Source]_值。 选择后，_[!UICONTROL Apply]_ 和 _[!UICONTROL Floor Adjustment Amount]_字段。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 相对于 _[!UICONTROL Floor Price Source]_值。 |
| [!UICONTROL Floor Adjustment Amount] | 输入百分比的数值以调整 _[!UICONTROL Floor Price Source]_值。 |
