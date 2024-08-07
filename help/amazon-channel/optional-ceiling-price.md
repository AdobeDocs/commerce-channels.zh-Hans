---
title: “智能重新定价规则：可选最高价”
description: 使用可选的最高价格设置，根据管理Amazon清单的智能定价规则保护您的最高产品价格。
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 智能重新定价规则：可选最高价

智能重新定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争对手条件差异](./competitor-conditional-variances.md)
- [价格调整](./price-adjustment.md)
- [底价](./floor-price.md)
- 可选最高价

自动的最高价格设置会自动根据智能定价规则保护您的最高产品价格，从而使您能够为智能定价规则设置最高价格。

## 配置可选的上限价格

在&#x200B;_[!UICONTROL Optional Ceiling Price]_部分中定义您的可选最高价格设置。

1. 为&#x200B;**[!UICONTROL Ceiling Price Source]**&#x200B;选择一个属性。

   选择指示相对上限的[!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)。 例如，如果不希望您的Amazon列表价格高于项目的MSRP，则可以选择`Manufacturer's Suggested Retail Price`属性。

1. 为&#x200B;**[!UICONTROL Ceiling Price Action]**&#x200B;选择一个选项。

   - `Decrease By` — 选择何时希望向下调整定义的&#x200B;_[!UICONTROL Ceiling Price Source]_值，以便降低规则的最高价格，然后再将其列出到Amazon。

   - `Increase By` — 选择您希望何时向上调整定义的&#x200B;_[!UICONTROL Ceiling Price Source]_值，以便为规则创建更高的最高价格，然后再将其列出到Amazon。

   - `Match` — 选择何时不希望清单价格波动超过定义的&#x200B;_[!UICONTROL Ceiling Price Source]_值。 当设置为`Match`时，_[!UICONTROL Apply]_&#x200B;和&#x200B;_[!UICONTROL Ceiling Adjustment Amount]_字段被禁用。

1. 将&#x200B;**[!UICONTROL Apply]**&#x200B;默认值保留为`Apply as percentage`。

1. 对于&#x200B;**[!UICONTROL Ceiling Adjustment Price]**，输入百分比的数字值以调整您的&#x200B;_[!UICONTROL Ceiling Price Source]_值。

在此示例中，最高价格设置为比项目的管理系统更新项目低2%。

![智能重新定价规则 — 可选最高价格](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | 选择指示相对上限的[!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)。 例如，如果您不希望产品清单价格高于项目的MSRP，则可以选择`Manufacturer's Suggested Retail Price`属性。 |
| [!UICONTROL Ceiling Price Action] | 选择定价调整活动。 选项：<ul><li>**[!UICONTROL Decrease By]** — 选择何时希望向下调整定义的&#x200B;_[!UICONTROL Ceiling Price Source]_值，以便降低规则的最高价格，然后再将其列出到Amazon。</li><li>**[!UICONTROL Increase By]** — 选择您希望何时向上调整定义的&#x200B;_[!UICONTROL Ceiling Price Source]_值，以便为规则创建更高的最高价格，然后再将其列出到Amazon。</li><li>**[!UICONTROL Match]** — 选择何时不希望清单价格波动超过定义的&#x200B;_[!UICONTROL Ceiling Price Source]_值。 当设置为`Match`时，_[!UICONTROL Apply]_&#x200B;和&#x200B;_[!UICONTROL Ceiling Adjustment Amount]_字段被禁用。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** — 相对于&#x200B;_[!UICONTROL Ceiling Price Source]_值的百分比调整。 |
| [!UICONTROL Ceiling Price Adjustment] | 输入百分比的数字值以调整您的&#x200B;_[!UICONTROL Ceiling Price Source]_值。 |
