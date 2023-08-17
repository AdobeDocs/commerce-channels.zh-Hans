---
title: Amazon Sales Channel - [!UICONTROL Price Adjustment]
description: 配置价格调整，以便在您确定Amazon竞争对手的价格来源时定义价格计算。
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>对于“标准”和“智能”重新定价规则，“价格调整”部分略有不同。 **[!UICONTROL Match Competitor Price]** 仅在 _[!UICONTROL Price Action]_时间&#x200B;**[!UICONTROL Rule Type]**设置为 `Intelligent repricing rule`.

智能重新定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争对手条件差异](./competitor-conditional-variances.md)
- 价格调整
- [底价](./floor-price.md)
- [可选最高价](./optional-ceiling-price.md)

当您确定了竞争对手的价格来源时，价格调整将定义价格计算。

## 配置价格调整

在中定义您的定价调整 _[!UICONTROL Price Adjustment]_部分。

1. 对象 **[!UICONTROL Price Action]**，选择一个选项：

   - `Decrease By`  — 选择何时希望向下调整定义的价格来源值，以便在Amazon中列出之前降低规则的价格。

   - `Increase By`  — 选择何时希望调整定义的价格来源值，以便在Amazon中列出之前提高规则的价格。

   - `Match Competitor Price`  — （仅限智能重新定价规则）选择何时更改Amazon上市价格以匹配 [最低竞争对手](./lowest-competitor-pricing.md) 价格，基于您的竞争对手反馈和差异参数。 当设置为 `Match Competitor Price`， _[!UICONTROL Apply]_和_[!UICONTROL Adjustment Amount]_ 字段会被删除。

1. 对象 **[!UICONTROL Apply]**，选择一个选项：

   - `Apply as percentage`  — 选择您何时需要 **[!UICONTROL Magento Price Source]** 在中定义 [挂牌价](./listing-price.md) 按百分比调整。

   - `Apply as fixed amount`  — 选择您何时需要 **[!UICONTROL Magento Price Source]** 在中定义 [挂牌价](./listing-price.md) 按固定金额调整。

1. 对象 **[!UICONTROL Adjustment Amount]** （必需），输入价格调整的数值。

   - 时间 **[!UICONTROL Apply]** 设置为 `Apply as percentage`，输入百分比值(例如：输入 `25` 25%的调整)。

   - 时间 **[!UICONTROL Apply]** 设置为 `Apply as fixed amount`，输入固定金额的数值(例如：输入 `25` 25美元的固定调整)。

![智能重新定价规则 — 价格调整](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | 选择定价调整活动。 选项：<br>**[!UICONTROL Decrease By]**— 选择您何时需要 _[!UICONTROL Magento Price Source]_在中定义 [挂牌价](./listing-price.md) 进行向下调整，从而降低规则价格，然后才将规则发布到Amazon。<br>**[!UICONTROL Increase By]**— 选择您何时需要_[!UICONTROL Magento Price Source]_ 在中定义 [挂牌价](./listing-price.md) 调整，抬高规则价格，然后才可将其上市至Amazon。<br>**[!UICONTROL Match Competitor Price]**— （仅限智能重新定价规则）选择何时更改Amazon上市价格以匹配 [最低竞争对手](./lowest-competitor-pricing.md) 价格，基于您的竞争对手反馈和差异参数。 选择后， _应用_ 和 _调整金额_ 字段会被删除。 |
| [!UICONTROL Apply] | 选项：<br>**[!UICONTROL Apply as percentage]**— 选择您何时需要 _[!UICONTROL Magento Price Source]_在中定义 [挂牌价](./listing-price.md) 按百分比调整。<br>**[!UICONTROL Apply as fixed amount]**— 选择您何时需要_[!UICONTROL Magento Price Source]_ 在中定义 [挂牌价](./listing-price.md) 按固定金额调整。 |
| [!UICONTROL Adjustment Amount] | 必需。<br>如果您选择 `Apply as percentage` 对象 **[!UICONTROL Apply]**，输入百分比值(例如：输入 `25` 25%的调整)。<br>如果您选择 `Apply as fixed amount` 对象 **[!UICONTROL Apply]**，输入固定金额的数值(例如：输入 `25` 25美元的固定调整)。 |
