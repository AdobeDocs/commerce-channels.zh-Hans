---
title: '智能重新定价规则：选择规则类型'
description: 通过创建智能重新定价规则，根据竞争对手的定价确定您的Amazon上市价格。
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# 智能重新定价规则：选择规则类型

>[!IMPORTANT]
>
>如果Amazon区域设置为，则智能重新定价规则无法正常运行 `Inactive` 状态，就像在载入过程中一样。 您的定价计算取决于您的运费，并且您的地区必须位于 `Active` 要从Amazon同步的运费状态。<br><br>
>
>要更新Amazon帐户中的地区状态，请转到“设置”>“帐户信息”>“假期设置”。 请参阅 [Amazon：休假的列表状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

智能重新定价规则使用Amazon竞争对手的定价来确定您的上市价格。 竞争对手是在Amazon中列出与您的产品相同的产品的其他销售商。

智能重新定价规则的部分包括：

- 选择规则类型
- [竞争对手条件差异](./competitor-conditional-variances.md)
- [价格调整](./price-adjustment.md)
- [底价](./floor-price.md)
- [可选最高价](./optional-ceiling-price.md)

## 配置规则类型

在中定义规则类型 _[!UICONTROL Select Rule Type]_部分。

1. 对象 **[!UICONTROL Rule Type]**，选择 `Intelligent repricing rule`.

   此设置将启用 _[!UICONTROL Competitor Price Source]_字段和 [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md)， [_[!UICONTROL Floor Price]_](./floor-price.md)、和 [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) 部分。

1. 对象 **[!UICONTROL Competitor Price Source]**，选择一个选项：

   - **[!UICONTROL Use "Buy Box" Price]**  — 选择何时根据Amazon调整Amazon定价 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 卖家价格。 A [!DNL Buy Box] 当Amazon上有多个销售者提供相同的产品时，即存在价格。 Amazon定义 [!DNL Buy Box] 销售商基于性能要求。 商人们寻求赢得 [!DNL Buy Box] 卖家状态并提供其产品列表的最大可见性。

   - **[!UICONTROL Use Lowest Competitor Price]**  — 选择您要比较并调整同一产品的上市价格与竞争对手定价的时间。 选择后， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 字段已启用。

1. 如果启用，请选择选项 **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]**  — 选择何时根据同一产品的所有竞争对手价格来比较和调整您的定价。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 选择何时希望限制与同一产品的价格进行比较的竞争对手。 该设置进一步缩小了竞争对手的版面，要求它们在应用最低价格规则之前，必须获得最低选定百分比的正反馈。

1. 如果启用，请输入 **[!UICONTROL Minimum Feedback Count]**.

   这一可选数值进一步缩小了竞争性定价的范围。 例如，如果商户的正面反馈评级为95%，但反馈次数仅为 `20`，则它可能不是您想要修改定价的竞争对手。 但是，如果输入的值为 `1000`，它将要求商户获得95%的积极反馈以及至少1000个商户评论。

>[!NOTE]
>
>您可以使用这些竞争对手的定价和反馈选项，避免将定价基于反馈差且销售质量较低的竞争对手之上。

![智能重新定价规则 — 选择规则类型](assets/ob-intelligent-price-rule-type.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Rule Type] | 选择规则类型。 选项：<ul><li>**[!UICONTROL Standard price rule]**  — 此规则类型允许您按特定百分比或固定美元金额增加或减少Amazon挂牌价格，具体金额与 _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]**  — 此规则类型允许您根据竞争对手的定价调整您的Amazon上市价格。 选择后， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 字段已启用。</li></ul> |
| [!UICONTROL Competitor Price Source] | 选择所需的价格来源。 选项：<ul><li>**[!UICONTROL Use "Buy Box" Price]**  — 当您要根据Amazon调整Amazon定价时，请选择此选项 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 卖家价格。 A [!DNL Buy Box] 当Amazon上有多个销售者提供相同的产品时，即存在价格。 Amazon定义 [!DNL Buy Box] 销售商基于性能要求。 商人们寻求赢得 [!DNL Buy Box] 卖家状态并提供其产品列表的最大可见性。</li><li>**[!UICONTROL Use Lowest Competitor Price]**  — 当您要比较并调整您的上市价格时，请选择此选项 [最低竞争对手价格](./lowest-competitor-pricing.md) 同一产品的名称。 选择后， _[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_ 字段已启用。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 仅在以下情况下处于活动状态： `Use Lowest Competitor Price` 已选中。 选项：<ul><li>**[!UICONTROL All Competitor's Prices]**  — 选择何时根据同一产品的所有竞争对手价格来比较和调整您的定价。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 选择何时要限制与之比较的竞争对手，并调整定价。 此设置会进一步缩小您的竞争对手的范围，方法是：要求他们的列表必须满足所选正反馈百分比的最低值，然后使用该竞争对手子集的最低价格。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 仅在以下情况下处于活动状态： `Use Lowest Competitor Price` 已选中。 此可选数值进一步缩小了竞争性定价比较的范围。 例如，如果商户的正面反馈评级为95%，但反馈计数仅为 `20`，则它可能不是您想要修改定价的竞争对手。 但是，如果输入的值为 `1000`，它将要求商户获得95%的积极反馈以及至少1000个商户评论。 |
