---
title: “智能重定价规则：可选最高价格”
description: 使用可选的最高价格设置，针对可管理Amazon列表的智能定价规则保护您的最高产品价格。
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
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

在 _[!UICONTROL Optional Ceiling Price]_中。

1. 对于 **[!UICONTROL Ceiling Price Source]**，请选择一个属性。

   选择 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}，表示您的相对上限。 例如，如果您不希望Amazon列表价格高于项目的MSRP，则可以选择 `Manufacturer's Suggested Retail Price` 属性。

1. 对于 **[!UICONTROL Ceiling Price Action]**，选择一个选项。

   - `Decrease By`  — 选择要定义的时间 _[!UICONTROL Ceiling Price Source]_值，为规则创建较低的最高价格，然后再上市到Amazon。

   - `Increase By`  — 选择要定义的时间 _[!UICONTROL Ceiling Price Source]_值，为规则创建更高的最高价格，然后再上市到Amazon。

   - `Match`  — 选择不希望上市价格在定义价格以上波动的时间 _[!UICONTROL Ceiling Price Source]_值。 当设置为 `Match`,_[!UICONTROL Apply]_ 和 _[!UICONTROL Ceiling Adjustment Amount]_字段。

1. 离开 **[!UICONTROL Apply]** 默认为 `Apply as percentage`.

1. 对于 **[!UICONTROL Ceiling Adjustment Price]**，输入百分比的数值以调整 _[!UICONTROL Ceiling Price Source]_值。

在本例中，最高价格被设置为比项目MSRP低2%。

![智能重定价规则 — 可选的最高价格](assets/ob-intelligent-price-rule-ceiling.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Ceiling Price Source] | 选择 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}，表示您的相对上限。 例如，如果您不希望产品列表价格高于项目的MSRP，则可以选择 `Manufacturer's Suggested Retail Price` 属性。 |
| [!UICONTROL Ceiling Price Action] | 选择定价调整操作。 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择要定义的时间 _[!UICONTROL Ceiling Price Source]_值，为规则创建较低的最高价格，然后再上市到Amazon。</li><li>**[!UICONTROL Increase By]**  — 选择要定义的时间 _[!UICONTROL Ceiling Price Source]_值，为规则创建更高的最高价格，然后再上市到Amazon。</li><li>**[!UICONTROL Match]**  — 选择不希望上市价格在定义价格以上波动的时间 _[!UICONTROL Ceiling Price Source]_值。 当设置为 `Match`,_[!UICONTROL Apply]_ 和 _[!UICONTROL Ceiling Adjustment Amount]_字段。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 相对于 _[!UICONTROL Ceiling Price Source]_值。 |
| [!UICONTROL Ceiling Price Adjustment] | 输入百分比的数值以调整 _[!UICONTROL Ceiling Price Source]_值。 |
