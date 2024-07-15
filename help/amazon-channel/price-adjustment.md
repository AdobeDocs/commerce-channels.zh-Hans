---
title: Amazon销售渠道 — [!UICONTROL Price Adjustment]
description: 配置价格调整，以便在您确定Amazon竞争对手的价格来源时定义价格计算。
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>对于“标准”和“智能”重新定价规则，“价格调整”部分略有不同。 当&#x200B;**[!UICONTROL Rule Type]**&#x200B;设置为`Intelligent repricing rule`时，**[!UICONTROL Match Competitor Price]**&#x200B;仅在&#x200B;_[!UICONTROL Price Action]_下可用。

智能重新定价规则的部分包括：

- [选择规则类型](./intelligent-repricing-rules.md)
- [竞争对手条件差异](./competitor-conditional-variances.md)
- 价格调整
- [底价](./floor-price.md)
- [可选最高价](./optional-ceiling-price.md)

当您确定了竞争对手的价格来源时，价格调整将定义价格计算。

## 配置价格调整

在&#x200B;_[!UICONTROL Price Adjustment]_部分中定义您的定价调整。

1. 对于&#x200B;**[!UICONTROL Price Action]**，请选择一个选项：

   - `Decrease By` — 选择何时希望向下调整定义的价格来源值，以便在Amazon中列出之前降低规则的价格。

   - `Increase By` — 选择何时希望调整定义的价格来源值，以便在Amazon中列出之前提高规则的价格。

   - `Match Competitor Price` - （仅限智能重新定价规则）根据竞争对手的反馈和差异参数，选择何时更改Amazon上市价格以使其与[最低竞争对手](./lowest-competitor-pricing.md)价格匹配。 当设置为`Match Competitor Price`时，将删除&#x200B;_[!UICONTROL Apply]_和_[!UICONTROL Adjustment Amount]_&#x200B;字段。

1. 对于&#x200B;**[!UICONTROL Apply]**，请选择一个选项：

   - `Apply as percentage` — 当您希望在[列表价格](./listing-price.md)中定义的&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;按百分比调整时，请选择此选项。

   - `Apply as fixed amount` — 当您希望在[列表价格](./listing-price.md)中定义的&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;按固定金额调整时选择。

1. 对于&#x200B;**[!UICONTROL Adjustment Amount]**（必需），输入价格调整的数值。

   - 当&#x200B;**[!UICONTROL Apply]**&#x200B;设置为`Apply as percentage`时，输入百分比值（例如：输入`25`作为25%的调整百分比）。

   - 当&#x200B;**[!UICONTROL Apply]**&#x200B;设置为`Apply as fixed amount`时，输入固定金额的数值（例如：输入`25`作为$25的固定调整）。

![智能重新定价规则 — 价格调整](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | 选择定价调整活动。 选项：<br>**[!UICONTROL Decrease By]**— 选择何时希望向下调整在[列表价格](./listing-price.md)中定义的&#x200B;_[!UICONTROL Magento Price Source]_，以便在Amazon中列表之前降低该规则的价格。<br>**[!UICONTROL Increase By]**— 当您希望调整在[列表价格](./listing-price.md)中定义的_[!UICONTROL Magento Price Source]_&#x200B;时，请选择相应的时间，这样在将该规则添加到Amazon之前，可以为该规则创建更高的价格。<br>**[!UICONTROL Match Competitor Price]**- （仅限智能重新定价规则）根据竞争对手的反馈和差异参数，选择何时更改Amazon上市价格以使其与[最低竞争对手](./lowest-competitor-pricing.md)价格匹配。 选择后，_应用_和&#x200B;_调整金额_字段将被删除。 |
| [!UICONTROL Apply] | 选项：<br>**[!UICONTROL Apply as percentage]**— 当您希望在[列表价格](./listing-price.md)中定义的已定义&#x200B;_[!UICONTROL Magento Price Source]_按百分比调整时选择。<br>**[!UICONTROL Apply as fixed amount]**— 当您希望在[列表价格](./listing-price.md)中定义的_[!UICONTROL Magento Price Source]_&#x200B;按固定金额调整时选择。 |
| [!UICONTROL Adjustment Amount] | 必需。<br>如果您为&#x200B;**[!UICONTROL Apply]**&#x200B;选择了`Apply as percentage`，请输入百分比值（例如：输入`25`将调整百分比设为25%）。<br>如果您为&#x200B;**[!UICONTROL Apply]**&#x200B;选择了`Apply as fixed amount`，请输入固定金额的数值（例如：输入`25`作为$25固定调整）。 |
