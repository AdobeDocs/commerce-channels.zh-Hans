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
>对于标准和智能重定价规则，“价格调整”部分会略有不同。 **[!UICONTROL Match Competitor Price]** 仅当设置为 _[!UICONTROL Price Action]_时，**[!UICONTROL Rule Type]**在 `Intelligent repricing rule`下可用。

智能重定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争者条件差异](./competitor-conditional-variances.md)
- 价格调整
- [最低价格](./floor-price.md)
- [可选最高价格](./optional-ceiling-price.md)

价格调整定义在您确定竞争者价格来源时的价格计算。

## 配置价格调整

在&#x200B;_[!UICONTROL Price Adjustment]_部分中定义定价调整。

1. 对于&#x200B;**[!UICONTROL Price Action]**，选择一个选项：

   - `Decrease By`  — 选择您希望何时向下调整定义的价格来源值，为规则创建较低的价格，然后再上市到Amazon。

   - `Increase By`  — 选择您希望何时调整定义的价格来源值，为规则创建更高的价格，然后再上市到Amazon。

   - `Match Competitor Price`  — （仅限智能重定价规则）根据您的竞争者反馈和差异参数，选择要更改Amazon上市价格以匹配 [最低](./lowest-competitor-pricing.md) 竞争者价格的时间。设置为`Match Competitor Price`时，将删除&#x200B;_[!UICONTROL Apply]_和_[!UICONTROL Adjustment Amount]_&#x200B;字段。

1. 对于&#x200B;**[!UICONTROL Apply]**，选择一个选项：

   - `Apply as percentage`  — 选择您希望在“上市价格”中 **[!UICONTROL Magento Price Source]** 定义的定 [义](./listing-price.md) 时间，并按百分比调整。

   - `Apply as fixed amount`  — 选择您希望何时定义 **[!UICONTROL Magento Price Source]** 的上市 [价](./listing-price.md) 格调整固定金额。

1. 对于&#x200B;**[!UICONTROL Adjustment Amount]**（必需），输入价格调整的数值。

   - 将&#x200B;**[!UICONTROL Apply]**&#x200B;设置为`Apply as percentage`时，输入百分比值(例如：输入`25`以进行25%的调整)。

   - 将&#x200B;**[!UICONTROL Apply]**&#x200B;设置为`Apply as fixed amount`时，输入固定金额的数值(例如：输入`25`，即$25的固定调整)。

![智能重定价规则 — 价格调整](assets/amazon-price-adjustment.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Price Action] | 选择定价调整操作。 选项：<br>**[!UICONTROL Decrease By]**— 选择您希望在[列表价格](./listing-price.md)中定义的&#x200B;_[!UICONTROL Magento Price Source]_何时下调整，为规则创建较低的价格，然后再列入Amazon。<br>**[!UICONTROL Increase By]**— 选择您希望何时调整_[!UICONTROL Magento Price Source]_ 上市价格 [中](./listing-price.md) 定义的内容，为规则创建更高的价格，然后再上市到Amazon。<br>**[!UICONTROL Match Competitor Price]**— （仅限智能重定价规则）根据您的竞争者反馈和差异参数，选择要更改Amazon上市价格以匹配 [最低](./lowest-competitor-pricing.md) 竞争者价格的时间。选择&#x200B;_Apply_和&#x200B;_Adjustment Amount_字段后，将删除。 |
| [!UICONTROL Apply] | 选项：<br>**[!UICONTROL Apply as percentage]**— 选择您希望在[Listing Price](./listing-price.md)中定义的&#x200B;_[!UICONTROL Magento Price Source]_的时间，并按百分比调整。<br>**[!UICONTROL Apply as fixed amount]**— 选择您希望何时定义_[!UICONTROL Magento Price Source]_ 的上市 [价](./listing-price.md) 格调整固定金额。 |
| [!UICONTROL Adjustment Amount] | 必需。<br>如果您选 `Apply as percentage` 择 **[!UICONTROL Apply]**&#x200B;了，请输入百分比值(例如：输 `25` 入25%的调整)。<br>如果选择 `Apply as fixed amount` 为 **[!UICONTROL Apply]**，请输入固定金额的数值(例如：输入 `25` $25的固定调整)。 |
