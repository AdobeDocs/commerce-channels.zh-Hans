---
title: '智能重新定价规则：可选最高价格'
description: 使用可选的最高价格设置来根据管理Amazon清单的智能定价规则保护您的最高产品价格。
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 智能重新定价规则：可选最高价格

智能重新定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争对手条件差异](./competitor-conditional-variances.md)
- [价格调整](./price-adjustment.md)
- [底价](./floor-price.md)
- 可选最高价

自动的最高价格设置可自动根据智能定价规则保护您的最高产品价格，从而使您能够为智能定价规则设置最高价格（最高价格）。

## 配置可选最高价格

在中定义可选的最高价格设置 _[!UICONTROL Optional Ceiling Price]_部分。

1. 对象 **[!UICONTROL Ceiling Price Source]**，选择一个属性。

   选择您的 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} 表示你的相对上限。 例如，如果您不希望自己的Amazon上市价格高于项目的MSRP，则可以选择 `Manufacturer's Suggested Retail Price` 属性。

1. 对象 **[!UICONTROL Ceiling Price Action]**，选择一个选项。

   - `Decrease By`  — 选择何时需要定义的 _[!UICONTROL Ceiling Price Source]_值后向下调整，从而降低规则的上限，然后再将值发布到Amazon。

   - `Increase By`  — 选择何时需要定义的 _[!UICONTROL Ceiling Price Source]_值进行调整，从而为规则创建更高的最高价格，然后再将资产挂牌到Amazon。

   - `Match`  — 选择何时不希望挂牌价波动超过定义的价格 _[!UICONTROL Ceiling Price Source]_值。 当设置为 `Match`，则_[!UICONTROL Apply]_ 和 _[!UICONTROL Ceiling Adjustment Amount]_字段被禁用。

1. 保留 **[!UICONTROL Apply]** 默认为 `Apply as percentage`.

1. 对象 **[!UICONTROL Ceiling Adjustment Price]**，输入百分比的数字值以调整 _[!UICONTROL Ceiling Price Source]_值。

在此示例中，最高价格设置为比物料的MSRP低2%。

![智能重新定价规则 — 可选最高价格](assets/ob-intelligent-price-rule-ceiling.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Ceiling Price Source] | 选择 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} 表示你的相对上限。 例如，如果您不希望产品清单价格高于项目的MSRP，则可以选择 `Manufacturer's Suggested Retail Price` 属性。 |
| [!UICONTROL Ceiling Price Action] | 选择定价调整活动。 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择何时需要定义的 _[!UICONTROL Ceiling Price Source]_值后向下调整，从而降低规则的上限，然后再将值发布到Amazon。</li><li>**[!UICONTROL Increase By]**  — 选择何时需要定义的 _[!UICONTROL Ceiling Price Source]_值进行调整，从而为规则创建更高的最高价格，然后再将资产挂牌到Amazon。</li><li>**[!UICONTROL Match]**  — 选择何时不希望挂牌价波动超过定义的价格 _[!UICONTROL Ceiling Price Source]_值。 当设置为 `Match`，则_[!UICONTROL Apply]_ 和 _[!UICONTROL Ceiling Adjustment Amount]_字段被禁用。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 相对于 _[!UICONTROL Ceiling Price Source]_值。 |
| [!UICONTROL Ceiling Price Adjustment] | 输入百分比的数字值，以调整 _[!UICONTROL Ceiling Price Source]_值。 |
