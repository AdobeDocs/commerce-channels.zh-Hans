---
title: “智能重定价规则：选择规则类型'
description: 通过创建智能的重新定价规则，根据竞争者定价确定您的Amazon上市价格。
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# 智能重定价规则：选择规则类型

>[!IMPORTANT]
>
>如果将Amazon区域设置为 `Inactive` 状态，与载入期间一样。 您的定价计算取决于您的运费，您所在的地区必须在 `Active` 从Amazon同步的运费状态。<br><br>
>
>要更新Amazon帐户中的区域状态，请转到设置>帐户信息>假期设置。 请参阅 [Amazon:假期的列表状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

智能的重新定价规则使用Amazon竞争者的定价来确定您的上市价格。 竞争对手是在Amazon上列出与您相同产品的其他销售商。

智能重定价规则的部分包括：

- 选择规则类型
- [竞争者条件差异](./competitor-conditional-variances.md)
- [价格调整](./price-adjustment.md)
- [最低价格](./floor-price.md)
- [可选最高价格](./optional-ceiling-price.md)

## 配置规则类型

在 _[!UICONTROL Select Rule Type]_中。

1. 对于 **[!UICONTROL Rule Type]**，选择 `Intelligent repricing rule`.

   此设置将启用 _[!UICONTROL Competitor Price Source]_字段和 [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md)和 [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) 中。

1. 对于 **[!UICONTROL Competitor Price Source]**，选择选项：

   - **[!UICONTROL Use "Buy Box" Price]**  — 选择何时要根据Amazon调整Amazon定价 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 卖方价格。 A [!DNL Buy Box] 当Amazon的多个卖家提供相同的产品时，即存在价格。 Amazon定义 [!DNL Buy Box] 卖方，根据绩效要求。 商人想赢 [!DNL Buy Box] 销售者状态，并提供其产品清单的最大可见性。

   - **[!UICONTROL Use Lowest Competitor Price]**  — 选择您希望何时根据同一产品的竞争对手定价来比较和调整上市价格。 选择后， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 字段。

1. 如果启用，请为 **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]**  — 根据同一产品的所有竞争者价格选择何时比较和调整定价。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 选择您希望何时限制将同一产品的价格与之比较的竞争对手。 此设置会进一步缩小竞争对手的范围，要求他们的上市在应用最低价格规则之前必须达到所选正反馈的最低百分比。

1. 如果启用，请输入 **[!UICONTROL Minimum Feedback Count]**.

   这个可选数值进一步缩小了竞争性定价的范围。 例如，如果某商家的反馈评级为95%，但反馈计数为 `20`，则您可能不希望针对其修改定价。 但是，如果输入的值为 `1000`，这要求商户有95%的正面反馈，至少有1000个商户评论。

>[!NOTE]
>
>您可以使用这些竞争对手的定价和反馈选项来避免根据反馈较差且销售质量较低产品的竞争对手进行定价。

![智能重定价规则 — 选择规则类型](assets/ob-intelligent-price-rule-type.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Rule Type] | 选择规则类型。 选项：<ul><li>**[!UICONTROL Standard price rule]**  — 利用此规则类型，可按相对于 _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]**  — 利用此规则类型，可根据竞争对手的定价调整Amazon上市价格。 选择后， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 字段。</li></ul> |
| [!UICONTROL Competitor Price Source] | 选择所需的价格来源。 选项：<ul><li>**[!UICONTROL Use "Buy Box" Price]**  — 当您想要根据Amazon调整Amazon定价时，请选择此选项 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 卖方价格。 A [!DNL Buy Box] 当Amazon的多个卖家提供相同的产品时，即存在价格。 Amazon定义 [!DNL Buy Box] 卖方，根据绩效要求。 商人想赢 [!DNL Buy Box] 销售者状态，并提供其产品清单的最大可见性。</li><li>**[!UICONTROL Use Lowest Competitor Price]**  — 当您要根据 [最低竞争对手定价](./lowest-competitor-pricing.md) 对同一产品。 选择后， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 字段。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 仅在 `Use Lowest Competitor Price` 中。 选项：<ul><li>**[!UICONTROL All Competitor's Prices]**  — 根据同一产品的所有竞争者价格选择何时比较和调整定价。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 选择您希望何时限制您比较的竞争对手并调整定价。 此设置会进一步缩小您的竞争对手的范围，要求他们的上市必须达到所选正反馈百分比的最低值，然后使用该竞争对手子集的最低价格。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 仅在 `Use Lowest Competitor Price` 中。 此可选数值进一步缩小了竞争性定价比较的范围。 例如，如果某商家的反馈评级为95%，但反馈计数为 `20`，则您可能不希望针对其修改定价。 但是，如果输入的值为 `1000`，这要求商户有95%的正面反馈，至少有1000个商户评论。 |
