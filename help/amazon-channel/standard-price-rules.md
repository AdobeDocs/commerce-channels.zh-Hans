---
title: Amazon sales channel — 标准价格规则操作
description: 使用标准价格规则操作增加或减少相对于Commerce目录价格（或价格来源）的Amazon上市价格。
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 标准价格规则操作

通过标准价格规则操作，您可以按特定百分比或相对于的固定美元金额增加或减少Amazon上市价格。 [!DNL Commerce] 目录价格（或价格来源）。

标准价格规则操作的部分包括：

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 配置价格规则操作

1. 对象 **[!UICONTROL Rule Type]**，选择 `Standard price rule`.

   此选项禁用 _[!UICONTROL Select Rule Type]_部分。

1. 展开 _[!UICONTROL Price Adjustment]_部分（如果需要）。

1. 对象 **[!UICONTROL Price Action]**，选择一个选项以确定要如何更改 *[!UICONTROL Magento Price Source]* （在中定义） [挂牌价](./listing-price.md))值。

   - `Decrease By`  — 在将该值列为Amazon之前，选择希望减小该值的时间。

   - `Increase By`  — 选择希望在将值添加到Amazon之前增加值的时间。

1. 对象 **[!UICONTROL Apply]**，选择一个选项以确定要如何定义 *[!UICONTROL Magento Price Source]* 在中定义 [挂牌价](./listing-price.md) 要调整的值：

   - `Apply as percentage`  — 选择您何时需要 *[!UICONTROL Magento Price Source]* 在中定义 [挂牌价](./listing-price.md) 按百分比调整的值

   - `Apply as fixed amount`  — 选择您何时需要 *[!UICONTROL Magento Price Source]* 在中定义 [挂牌价](./listing-price.md) 按固定金额调整的值。

1. 对象 **[!UICONTROL Adjustment Amount]** （必需），输入价格调整的数值。

   - 时间 *[!UICONTROL Apply]* 设置为 `Apply as percentage`，输入百分比值(例如：输入 `25` 25%的价格调整)。

   - 时间 *[!UICONTROL Apply]* 设置为 `Apply as fixed amount`，输入固定金额的数值(例如：输入 `25` 25美元的固定价格调整)。

1. 完成后，单击 **[!UICONTROL Save pricing rule]**.

![标准价格规则](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | 选择 `Standard price rule`. |
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]**  — 选择您何时需要 [!DNL Commerce] 在上市到Amazon之前要减少的价格来源值。</li><li>**[!UICONTROL Increase By]**  — 选择您何时需要 [!DNL Commerce] 在列为Amazon之前要增加的价格来源值。</li></ul> |
| [!UICONTROL Apply] | 选项：<ul><li>**[!UICONTROL Apply as percentage]**  — 选择您何时需要 [!DNL Commerce] 按百分比调整的价格来源值。</li><li>**[!UICONTROL Apply as fixed amount]**  — 选择您何时需要 [!DNL Commerce] 按固定金额调整的价格来源值。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必需。<br><br>如果您选择 `Apply as percentage` 对象 *[!UICONTROL Apply]*，输入百分比值(例如：输入 `25` 25%的调整)。<br><br>如果您选择 `Apply as fixed amount` 对象 *[!UICONTROL Apply]*，输入固定金额的数值(例如：输入 `25` 25美元的固定调整)。 |
