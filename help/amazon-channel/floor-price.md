---
title: “智能重新定价规则：最低价格”
description: 使用最低价格设置来确定智能定价规则的最低价格，以便管理您的Amazon列表。
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# 智能重新定价规则：最低价格

智能重新定价规则的部分包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

[最低价格](./floor-price.md)设置会自动根据智能定价规则保护您的最低产品价格。 使用这些设置为您的智能定价规则设置下限（最低价格），确保您的产品不会低于所需价格。

如果您的[!DNL Commerce]商店使用网站定价范围，则最低价格属性基于网站范围。 查看[价格范围](./price-scope.md)。

只有当&#x200B;**[!UICONTROL Rule Type]**&#x200B;设置为`Intelligent repricing rule`时才使用最低价。

## 配置底价

在&#x200B;_[!UICONTROL Floor Price]_部分中定义最低价格设置。

1. 对于&#x200B;**[!UICONTROL Floor Price Source]**，请选择一个价格源属性。

   选择指示相对楼层限制的[!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)。 例如，如果您不希望您的Amazon列表价格低于项目的成本，则可以选择&#x200B;*成本*&#x200B;属性。

1. 为&#x200B;**[!UICONTROL Floor Price Action]**&#x200B;选择一个选项。

   - `Decrease By` — 选择何时希望向下调整定义的&#x200B;_[!UICONTROL Floor Price Source]_值，以便降低规则的最低价格，然后再将其列出到Amazon。

   - `Increase By` — 选择何时希望上调定义的&#x200B;_[!UICONTROL Floor Price Source]_值，以便为该规则创建更高的下限价格，然后再将其列出到Amazon。

   - `Match` — 选择何时不希望清单价格波动到定义的&#x200B;_[!UICONTROL Floor Price Source]_值以下。 当设置为`Match`时，_[!UICONTROL Apply]_&#x200B;和&#x200B;_[!UICONTROL Floor Adjustment Amount]_字段被禁用。

1. 将&#x200B;**[!UICONTROL Apply]**&#x200B;默认值保留为`Apply as percentage`。

1. 对于&#x200B;**[!UICONTROL Floor Adjustment Price]**，输入百分比的数字值以调整您的&#x200B;_[!UICONTROL Floor Price Source]_值。

在本例中，底价设置为比物料成本高3%。

![智能重新定价规则示例 — 底价](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | 选择指示相对下限（最低价格）限制的[!DNL Commerce]属性。 例如，如果您不希望您的Amazon列表价格低于项目的成本，则可以选择`Cost`属性。 |
| [!UICONTROL Floor Price Action] | 选择定价调整活动。 选项：<ul><li>**[!UICONTROL Decrease By]** — 选择何时希望向下调整定义的&#x200B;_[!UICONTROL Floor Price Source]_值，以便降低规则的最低价格，然后再将其列出到Amazon。</li><li>**[!UICONTROL Increase By]** — 选择何时希望上调定义的&#x200B;_[!UICONTROL Floor Price Source]_值，以便为该规则创建更高的下限价格，然后再将其列出到Amazon。</li><li>**[!UICONTROL Match]** — 选择何时不希望清单价格波动到定义的&#x200B;_[!UICONTROL Floor Price Source]_值以下。 选择后，_[!UICONTROL Apply]_&#x200B;和&#x200B;_[!UICONTROL Floor Adjustment Amount]_字段将被禁用。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** — 相对于&#x200B;_[!UICONTROL Floor Price Source]_值的百分比调整。 |
| [!UICONTROL Floor Adjustment Amount] | 输入百分比的数字值以调整您的&#x200B;_[!UICONTROL Floor Price Source]_值。 |
