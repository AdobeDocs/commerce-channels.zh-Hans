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

通过标准价格规则操作，您可以相对于[!DNL Commerce]目录价格（或价格来源），按特定百分比或固定美元金额增加或减少Amazon列表价格。

标准价格规则操作的部分包括：

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 配置价格规则操作

1. 对于&#x200B;**[!UICONTROL Rule Type]**，选择`Standard price rule`。

   此选项会禁用&#x200B;_[!UICONTROL Select Rule Type]_部分中的其他字段。

1. 根据需要展开&#x200B;_[!UICONTROL Price Adjustment]_部分。

1. 对于&#x200B;**[!UICONTROL Price Action]**，选择一个选项以确定要更改&#x200B;*[!UICONTROL Magento Price Source]*（在[列出价格](./listing-price.md)中定义）值的方式。

   - `Decrease By`  — 在列入Amazon之前，选择希望何时减小该值。

   - `Increase By`  — 在将值列入Amazon之前，选择希望何时增加该值。

1. 对于&#x200B;**[!UICONTROL Apply]**，选择一个选项和一个选项，以确定您希望如何调整[Listing Price](./listing-price.md)值中定义的&#x200B;*[!UICONTROL Magento Price Source]*:

   - `Apply as percentage`  — 选择您希望何时定义 *[!UICONTROL Magento Price Source]* 在列表价 [格](./listing-price.md) 值中按百分比调整

   - `Apply as fixed amount`  — 选择您希望何时定义 *[!UICONTROL Magento Price Source]* 的上市价 [值](./listing-price.md) 按固定金额调整。

1. 对于&#x200B;**[!UICONTROL Adjustment Amount]**（必需），输入价格调整的数值。

   - 将&#x200B;*[!UICONTROL Apply]*&#x200B;设置为`Apply as percentage`时，输入百分比值(例如：输入`25`以调整价格25%)。

   - 将&#x200B;*[!UICONTROL Apply]*&#x200B;设置为`Apply as fixed amount`时，输入固定金额的数值(例如：输入`25`以调整$25的固定价格)。

1. 完成后，单击&#x200B;**[!UICONTROL Save pricing rule]**。

![标准价格规则](assets/ob-price-rule-action-standard-example.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Rule Type] | 选择`Standard price rule`。 |
| [!UICONTROL Price Action] | 选项：<ul><li>**[!UICONTROL Decrease By]**  — 在列入Amazon之前，选 [!DNL Commerce] 择您希望何时减少定义的价格来源值。</li><li>**[!UICONTROL Increase By]**  — 在列入Amazon之前，选 [!DNL Commerce] 择希望何时增加定义的价格来源值。</li></ul> |
| [!UICONTROL Apply] | 选项：<ul><li>**[!UICONTROL Apply as percentage]**  — 选择您希望何时按百 [!DNL Commerce] 分比调整定义的价格来源值。</li><li>**[!UICONTROL Apply as fixed amount]**  — 选择您希望何时按固 [!DNL Commerce] 定金额调整定义的价格来源值。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必需。<br><br>如果选择 `Apply as percentage` , *[!UICONTROL Apply]*&#x200B;请输入百分比值(例如：输 `25` 入25%的调整)。<br><br>如果选择 `Apply as fixed amount` 为 *[!UICONTROL Apply]*，请输入固定金额的数值(例如：输入 `25` $25的固定调整)。 |
