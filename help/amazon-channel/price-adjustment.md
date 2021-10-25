---
title: 价格调整
description: 配置价格调整，以在您确定Amazon竞争者的价格来源时定义价格计算。
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 价格调整

>[!NOTE]
>
>对于标准和智能重定价规则，“价格调整”部分会略有不同。 **[!UICONTROL Match Competitor Price]** 只能在 _[!UICONTROL Price Action]_when **[!UICONTROL Rule Type]**设置为 `Intelligent repricing rule`.

智能重定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争者条件差异](./competitor-conditional-variances.md)
- 价格调整
- [最低价格](./floor-price.md)
- [可选最高价格](./optional-ceiling-price.md)

价格调整定义在您确定竞争者价格来源时的价格计算。

## 配置价格调整

在 _[!UICONTROL Price Adjustment]_中。

1. 对于 **[!UICONTROL Price Action]**，选择选项：

   - `Decrease By`  — 选择您希望何时向下调整定义的价格来源值，为规则创建较低的价格，然后再上市到Amazon。

   - `Increase By`  — 选择您希望何时调整定义的价格来源值，为规则创建更高的价格，然后再上市到Amazon。

   - `Match Competitor Price`  — （仅限智能重定价规则）选择您希望何时更改Amazon列表价格以匹配 [最低竞争对手](./lowest-competitor-pricing.md) 价格，根据您的竞争者反馈和方差参数。 当设置为 `Match Competitor Price`, _[!UICONTROL Apply]_和_[!UICONTROL Adjustment Amount]_ 字段。

1. 对于 **[!UICONTROL Apply]**，选择选项：

   - `Apply as percentage`  — 选择要定义的时间 **[!UICONTROL Magento Price Source]** 在 [上市价格](./listing-price.md) 按百分比调整。

   - `Apply as fixed amount`  — 选择要定义的时间 **[!UICONTROL Magento Price Source]** 在 [上市价格](./listing-price.md) 按固定金额调整。

1. 对于 **[!UICONTROL Adjustment Amount]** （必需），输入价格调整的数值。

   - When **[!UICONTROL Apply]** 设置为 `Apply as percentage`，输入百分比值(例如：enter `25` 25%的调整)。

   - When **[!UICONTROL Apply]** 设置为 `Apply as fixed amount`，输入固定金额的数值(例如：enter `25` 25美元的固定调整)。

![智能重定价规则 — 价格调整](assets/amazon-price-adjustment.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Price Action] | 选择定价调整操作。 选项：<br>**[!UICONTROL Decrease By]**— 选择要定义的时间 _[!UICONTROL Magento Price Source]_在 [上市价格](./listing-price.md) 在上市到Amazon之前，将向下调整，为规则创建较低的价格。<br>**[!UICONTROL Increase By]**— 选择要定义的时间_[!UICONTROL Magento Price Source]_ 在 [上市价格](./listing-price.md) 将进行调整，为规则创造更高价格，然后再上市至Amazon。<br>**[!UICONTROL Match Competitor Price]**— （仅限智能重定价规则）选择您希望何时更改Amazon列表价格以匹配 [最低竞争对手](./lowest-competitor-pricing.md) 价格，根据您的竞争者反馈和方差参数。 选择后， _应用_ 和 _调整金额_ 字段。 |
| [!UICONTROL Apply] | 选项：<br>**[!UICONTROL Apply as percentage]**— 选择要定义的时间 _[!UICONTROL Magento Price Source]_在 [上市价格](./listing-price.md) 按百分比调整。<br>**[!UICONTROL Apply as fixed amount]**— 选择要定义的时间_[!UICONTROL Magento Price Source]_ 在 [上市价格](./listing-price.md) 按固定金额调整。 |
| [!UICONTROL Adjustment Amount] | 必需。<br>如果您选择 `Apply as percentage` 表示 **[!UICONTROL Apply]**，输入百分比值(例如：enter `25` 25%的调整)。<br>如果您选择 `Apply as fixed amount` 表示 **[!UICONTROL Apply]**，输入固定金额的数值(例如：enter `25` 25美元的固定调整)。 |
