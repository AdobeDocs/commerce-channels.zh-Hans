---
title: 标准价格规则操作
description: 使用标准价格规则操作可以相对于商务目录价格（或价格来源）增加或减少Amazon上市价格。
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# 标准价格规则操作

通过标准价格规则操作，您可以按与 [!DNL Commerce] 目录价格（或价格来源）。

标准价格规则操作的部分包括：

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 配置价格规则操作

1. 对于 **[!UICONTROL Rule Type]**，选择 `Standard price rule`.

   此选项会禁用 _[!UICONTROL Select Rule Type]_中。

1. 展开 _[!UICONTROL Price Adjustment]_，如果需要。

1. 对于 **[!UICONTROL Price Action]**，选择一个选项以确定要如何更改 *[!UICONTROL Magento Price Source]* (在 [上市价格](./listing-price.md))值。

   - `Decrease By`  — 在列入Amazon之前，选择希望何时减小该值。

   - `Increase By`  — 在将值列入Amazon之前，选择希望何时增加该值。

1. 对于 **[!UICONTROL Apply]**，选择一个选项和一个选项，以确定您希望定义的方式 *[!UICONTROL Magento Price Source]* 在 [上市价格](./listing-price.md) 值：

   - `Apply as percentage`  — 选择要定义的时间 *[!UICONTROL Magento Price Source]* 在 [上市价格](./listing-price.md) 值按百分比调整

   - `Apply as fixed amount`  — 选择要定义的时间 *[!UICONTROL Magento Price Source]* 在 [上市价格](./listing-price.md) 值按固定金额调整。

1. 对于 **[!UICONTROL Adjustment Amount]** （必需），输入价格调整的数值。

   - When *[!UICONTROL Apply]* 设置为 `Apply as percentage`，输入百分比值(例如：enter `25` 价格调整25%)。

   - When *[!UICONTROL Apply]* 设置为 `Apply as fixed amount`，输入固定金额的数值(例如：enter `25` 25美元的固定价格调整)。

1. 完成后，单击 **[!UICONTROL Save pricing rule]**.

![标准价格规则](assets/ob-price-rule-action-standard-example.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Rule Type] | 选择 `Standard price rule`. |
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择要定义的时间 [!DNL Commerce] 价格来源价值，将在上市前降低至Amazon。</li><li>**[!UICONTROL Increase By]**  — 选择要定义的时间 [!DNL Commerce] 价格来源价值将在上市前提高至Amazon。</li></ul> |
| [!UICONTROL Apply] | 选项：<ul><li>**[!UICONTROL Apply as percentage]**  — 选择要定义的时间 [!DNL Commerce] 价格来源值，按百分比调整。</li><li>**[!UICONTROL Apply as fixed amount]**  — 选择要定义的时间 [!DNL Commerce] 按固定金额调整的价格来源值。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必需。<br><br>如果您选择 `Apply as percentage` 表示 *[!UICONTROL Apply]*，输入百分比值(例如：enter `25` 25%的调整)。<br><br>如果您选择 `Apply as fixed amount` 表示 *[!UICONTROL Apply]*，输入固定金额的数值(例如：enter `25` 25美元的固定调整)。 |
