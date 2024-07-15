---
title: Amazon sales channel — 标准价格规则操作
description: 使用标准价格规则操作，增加或减少相对于Amazon目录价格（或价格来源）的Commerce上市价格。
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# 标准价格规则操作

标准价格规则操作允许您按[!DNL Commerce]目录价格（或价格来源）的特定百分比或固定美元金额增加或减少Amazon挂牌价格。

标准价格规则操作的部分包括：

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 配置价格规则操作

1. 对于&#x200B;**[!UICONTROL Rule Type]**，请选择`Standard price rule`。

   此选项禁用&#x200B;_[!UICONTROL Select Rule Type]_部分中的其他字段。

1. 如果需要，请展开&#x200B;_[!UICONTROL Price Adjustment]_部分。

1. 对于&#x200B;**[!UICONTROL Price Action]**，选择一个选项以确定您要如何更改&#x200B;*[!UICONTROL Magento Price Source]*（在您的[列表价格](./listing-price.md)中定义）值。

   - `Decrease By` — 选择您希望此值在列为Amazon之前减少的时间。

   - `Increase By` — 选择您希望此值在列为Amazon之前增加的时间。

1. 对于&#x200B;**[!UICONTROL Apply]**，请选择一个选项以确定如何调整[列表价格](./listing-price.md)值中定义的&#x200B;*[!UICONTROL Magento Price Source]*：

   - `Apply as percentage` — 选择何时希望在[列表价格](./listing-price.md)值中定义的按百分比调整的&#x200B;*[!UICONTROL Magento Price Source]*

   - `Apply as fixed amount` — 当您希望在[列表价格](./listing-price.md)值中定义的&#x200B;*[!UICONTROL Magento Price Source]*&#x200B;按固定金额调整时，请选择此选项。

1. 对于&#x200B;**[!UICONTROL Adjustment Amount]**（必需），输入价格调整的数值。

   - 当&#x200B;*[!UICONTROL Apply]*&#x200B;设置为`Apply as percentage`时，输入百分比值（例如：输入`25`作为25%的价格调整）。

   - 当&#x200B;*[!UICONTROL Apply]*&#x200B;设置为`Apply as fixed amount`时，输入固定金额的数值（例如：输入`25`作为$25的固定价格调整）。

1. 完成后，单击&#x200B;**[!UICONTROL Save pricing rule]**。

![标准价格规则](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | 选择`Standard price rule`。 |
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]** — 选择您何时希望先减少定义的[!DNL Commerce]价格来源值，然后再将其列为Amazon。</li><li>**[!UICONTROL Increase By]** — 当您希望在将定义的[!DNL Commerce]价格来源值列出到Amazon之前增加时，请选择此选项。</li></ul> |
| [!UICONTROL Apply] | 选项：<ul><li>**[!UICONTROL Apply as percentage]** — 选择何时希望按百分比调整定义的[!DNL Commerce]价格来源值。</li><li>**[!UICONTROL Apply as fixed amount]** — 选择何时希望按固定金额调整定义的[!DNL Commerce]价格来源值。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必需。<br><br>如果您为&#x200B;*[!UICONTROL Apply]*&#x200B;选择`Apply as percentage`，请输入百分比值（例如：输入`25`将调整百分比设为25%）。<br><br>如果您为&#x200B;*[!UICONTROL Apply]*&#x200B;选择了`Apply as fixed amount`，请输入固定金额的数值（例如：输入`25`作为$25固定调整）。 |
