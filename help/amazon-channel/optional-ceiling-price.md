---
title: “智能重定价规则：可选最高价格”
description: 使用可选的最高价格设置，针对可管理Amazon列表的智能定价规则保护您的最高产品价格。
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 智能重定价规则：可选上限价格

智能重定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争者条件差异](./competitor-conditional-variances.md)
- [价格调整](./price-adjustment.md)
- [最低价格](./floor-price.md)
- 可选最高价格

自动上限价格设置可自动针对智能定价规则保护您的最高产品价格，从而允许您为智能定价规则设置最高价格（最高价格）。

## 配置可选的最高价格

在&#x200B;_[!UICONTROL Optional Ceiling Price]_部分中定义可选的最高价格设置。

1. 对于&#x200B;**[!UICONTROL Ceiling Price Source]**，选择一个属性。

   选择[!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}，以指示您的相对上限。 例如，如果您不希望Amazon列表价格高于项目MSRP，则应选择`Manufacturer's Suggested Retail Price`属性。

1. 对于&#x200B;**[!UICONTROL Ceiling Price Action]**，选择一个选项。

   - `Decrease By`  — 选择您希望何时向下调 _[!UICONTROL Ceiling Price Source]_整定义的值，为规则创建较低的上限价格，然后再将其列入Amazon。

   - `Increase By`  — 选择您希望何时调整定 _[!UICONTROL Ceiling Price Source]_义的值，为规则创建更高的上限价格，然后再将其列入Amazon。

   - `Match`  — 选择您不希望上市价格高于定义值的时 _[!UICONTROL Ceiling Price Source]_间。如果设置为`Match`，则_[!UICONTROL Apply]_&#x200B;和&#x200B;_[!UICONTROL Ceiling Adjustment Amount]_字段会被禁用。

1. 将默认的&#x200B;**[!UICONTROL Apply]**&#x200B;保留为`Apply as percentage`。

1. 对于&#x200B;**[!UICONTROL Ceiling Adjustment Price]**，输入百分比的数值以调整&#x200B;_[!UICONTROL Ceiling Price Source]_值。

在本例中，最高价格被设置为比项目MSRP低2%。

![智能重定价规则 — 可选的最高价格](assets/ob-intelligent-price-rule-ceiling.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Ceiling Price Source] | 选择[!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}，以指示您的相对上限。 例如，如果您不希望产品清单价格高于项目MSRP，则应选择`Manufacturer's Suggested Retail Price`属性。 |
| [!UICONTROL Ceiling Price Action] | 选择定价调整操作。 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择您希望何时向下调 _[!UICONTROL Ceiling Price Source]_整定义的值，为规则创建较低的上限价格，然后再将其列入Amazon。</li><li>**[!UICONTROL Increase By]**  — 选择您希望何时调整定 _[!UICONTROL Ceiling Price Source]_义的值，为规则创建更高的上限价格，然后再将其列入Amazon。</li><li>**[!UICONTROL Match]**  — 选择您不希望上市价格高于定义值的时 _[!UICONTROL Ceiling Price Source]_间。如果设置为`Match`，则_[!UICONTROL Apply]_&#x200B;和&#x200B;_[!UICONTROL Ceiling Adjustment Amount]_字段会被禁用。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 相对于值的百分比 _[!UICONTROL Ceiling Price Source]_调整。 |
| [!UICONTROL Ceiling Price Adjustment] | 输入百分比的数值以调整&#x200B;_[!UICONTROL Ceiling Price Source]_值。 |
