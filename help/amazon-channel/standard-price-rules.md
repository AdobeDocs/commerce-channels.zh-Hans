---
title: Amazon sales channel — 标准价格规则操作
description: 使用标准价格规则操作增加或减少相对于Commerce目录价格（或价格来源）的Amazon上市价格。
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 标准价格规则操作

通过标准价格规则操作，您可以按特定百分比或相对于的固定美元金额增加或减少Amazon挂牌价格。 [!DNL Commerce] 目录价格（或价格来源）。

标准价格规则操作的部分包括：

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 配置价格规则操作

1. 对象 **[!UICONTROL Rule Type]**，选择 `Standard price rule`.

   此选项禁用 _[!UICONTROL Select Rule Type]_部分。

1. 展开 _[!UICONTROL Price Adjustment]_部分（如果需要）。

1. 对象 **[!UICONTROL Price Action]**，选择一个选项以确定更改更改的方式 *[!UICONTROL Magento Price Source]* （在中定义） [挂牌价](./listing-price.md))值。

   - `Decrease By`  — 选择您希望值在列为Amazon之前减少的时间。

   - `Increase By`  — 选择您希望值在列为Amazon之前增加的时间。

1. 对象 **[!UICONTROL Apply]**，选择一个选项以确定如何定义 *[!UICONTROL Magento Price Source]* 在中定义 [挂牌价](./listing-price.md) 要调整的值：

   - `Apply as percentage`  — 选择何时需要定义的 *[!UICONTROL Magento Price Source]* 在中定义 [挂牌价](./listing-price.md) 按百分比调整的值

   - `Apply as fixed amount`  — 选择何时需要定义的 *[!UICONTROL Magento Price Source]* 在中定义 [挂牌价](./listing-price.md) 按固定金额调整的值。

1. 对象 **[!UICONTROL Adjustment Amount]** （必需），输入价格调整的数值。

   - 时间 *[!UICONTROL Apply]* 设置为 `Apply as percentage`，输入百分比值(例如：输入 `25` 价格调整的25%)。

   - 时间 *[!UICONTROL Apply]* 设置为 `Apply as fixed amount`，输入固定金额的数值(例如：输入 `25` （固定价格调整为$25）。

1. 完成后，单击 **[!UICONTROL Save pricing rule]**.

![标准价格规则](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|---|---|
| [!UICONTROL Rule Type] | 选择 `Standard price rule`. |
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择何时需要定义的 [!DNL Commerce] 在挂牌到Amazon之前要降低的价格来源值。</li><li>**[!UICONTROL Increase By]**  — 选择何时需要定义的 [!DNL Commerce] 在上市到Amazon之前要增加的价格来源值。</li></ul> |
| [!UICONTROL Apply] | 选项：<ul><li>**[!UICONTROL Apply as percentage]**  — 选择何时需要定义的 [!DNL Commerce] 按百分比调整的价格来源值。</li><li>**[!UICONTROL Apply as fixed amount]**  — 选择何时需要定义的 [!DNL Commerce] 按固定金额调整的价格来源值。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必需。<br><br>如果您选择 `Apply as percentage` 对象 *[!UICONTROL Apply]*，输入百分比值(例如：输入 `25` （例如，25%的调整）。<br><br>如果您选择 `Apply as fixed amount` 对象 *[!UICONTROL Apply]*，输入固定金额的数值(例如：输入 `25` 25美元的固定调整)。 |
