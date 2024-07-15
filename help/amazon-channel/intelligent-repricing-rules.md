---
title: '智能重新定价规则：选择规则类型'
description: 通过创建智能的重新定价规则，根据竞争对手的定价确定您的Amazon上市价格。
feature: Sales Channels, Products, Price Rules
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# 智能重新定价规则：选择规则类型

>[!IMPORTANT]
>
>如果Amazon区域设置为`Inactive`状态（与载入期间一样），则智能重新定价规则无法正常运行。 你的定价计算取决于你的运费，你的地区必须处于`Active`状态，你的运费才能与Amazon同步。<br><br>
>
>要在Amazon帐户中更新您所在地区的状态，请转到“设置”>“帐户信息”>“假期设置”。 请参阅[Amazon：假期列表状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

智能的重新定价规则使用Amazon竞争对手的定价来确定您的上市价格。 竞争对手是在Amazon中列出与您的产品相同的产品的其他销售商。

智能重新定价规则的部分包括：

- 选择规则类型
- [竞争对手条件差异](./competitor-conditional-variances.md)
- [价格调整](./price-adjustment.md)
- [底价](./floor-price.md)
- [可选最高价](./optional-ceiling-price.md)

## 配置规则类型

在&#x200B;_[!UICONTROL Select Rule Type]_部分中定义规则类型。

1. 对于&#x200B;**[!UICONTROL Rule Type]**，请选择`Intelligent repricing rule`。

   此设置启用&#x200B;_[!UICONTROL Competitor Price Source]_字段以及[_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md)、[_[!UICONTROL Floor Price]_](./floor-price.md)和[_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md)部分。

1. 对于&#x200B;**[!UICONTROL Competitor Price Source]**，请选择一个选项：

   - **[!UICONTROL Use "Buy Box" Price]** — 选择何时根据Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md)卖方价格调整Amazon定价。 当Amazon上的多个销售者提供相同的产品时，存在[!DNL Buy Box]价格。 Amazon根据性能要求定义了[!DNL Buy Box]销售方。 商家寻求赢得[!DNL Buy Box]卖方状态并提供其产品列表的最大可见性。

   - **[!UICONTROL Use Lowest Competitor Price]** — 选择何时比较并调整同一产品的上市价格与竞争对手的定价。 选择后，将启用&#x200B;_[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_&#x200B;字段。

1. 如果启用，请为&#x200B;**[!UICONTROL Minimum Positive Feedback]**&#x200B;选择一个选项。

   - **[!UICONTROL All Competitor's Prices]** — 选择何时根据同一产品的所有竞争对手价格比较和调整您的定价。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** — 选择何时希望限制与同一产品的价格比较的竞争对手。 这一设置进一步缩小了竞争对手的版面，要求它们在应用最低价格规则前，必须达到最低限度的所选正反馈百分比。

1. 如果启用，请输入&#x200B;**[!UICONTROL Minimum Feedback Count]**&#x200B;的数值。

   此可选数值进一步缩小了具有竞争力的定价。 例如，如果某个商家的正反馈评级为95%，但反馈次数仅为`20`，则可能不是您要修改定价的竞争对手。 但是，如果输入的值为`1000`，则要求商家有95%的积极反馈以及至少1000个商家审核。

>[!NOTE]
>
>您可以使用这些竞争对手的定价和反馈选项，避免根据反馈差且销售质量较低的产品的竞争对手来定价。

![智能重新定价规则 — 选择规则类型](assets/ob-intelligent-price-rule-type.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | 选择规则类型。 选项：<ul><li>**[!UICONTROL Standard price rule]** — 此规则类型允许您按特定百分比或固定美元金额增加或减少Amazon上市价格（相对于&#x200B;_[!UICONTROL Magento Price Source]_）。 </li><li>**[!UICONTROL Intelligent repricing rule]** — 此规则类型允许您根据竞争对手的定价调整您的Amazon上市价格。 选择后，将启用&#x200B;_[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_&#x200B;字段。</li></ul> |
| [!UICONTROL Competitor Price Source] | 选择所需的价格来源。 选项：<ul><li>**[!UICONTROL Use "Buy Box" Price]** — 当您要根据Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md)卖方价格调整Amazon定价时，请选择此选项。 当Amazon上的多个销售者提供相同的产品时，存在[!DNL Buy Box]价格。 Amazon根据性能要求定义了[!DNL Buy Box]销售方。 商家寻求赢得[!DNL Buy Box]卖方状态并提供其产品列表的最大可见性。</li><li>**[!UICONTROL Use Lowest Competitor Price]** — 当您要比较并调整您的上市价格以使其与同一产品的[最低竞争者定价](./lowest-competitor-pricing.md)相比较时，请选择此选项。 选择后，将启用&#x200B;_[!UICONTROL Minimum Positive Feedback]_和_[!UICONTROL Minimum Feedback Count]_&#x200B;字段。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 仅在选择了`Use Lowest Competitor Price`时有效。 选项：<ul><li>**[!UICONTROL All Competitor's Prices]** — 选择何时根据同一产品的所有竞争对手价格比较和调整您的定价。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** — 选择何时限制您与之比较的竞争对手，并调整您的定价。 此设置会进一步缩小您的竞争对手的范围，方法是：要求他们的列表必须满足所选正反馈百分比中的最低值，然后使用该竞争对手子集的最低价格。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 仅在选择了`Use Lowest Competitor Price`时有效。 此可选数值进一步缩小了竞争性定价比较的范围。 例如，如果某个商家的正反馈评级为95%，但反馈计数仅为`20`，则可能不是您要修改定价的竞争对手。 但是，如果输入的值为`1000`，则要求商家有95%的积极反馈以及至少1000个商家审核。 |
