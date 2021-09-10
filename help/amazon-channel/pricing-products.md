---
title: 管理Amazon定价
description: 您可以使用定价规则将Amazon列表的定价设置为与您的电子商务商店不同。
redirect_from: /sales-channels/asc/ob-pricing-rules.html: 
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 865
ht-degree: 0%

---

# 管理Amazon定价

Amazon销售渠道允许您设置定价规则，这些规则允许您设置与[上市价格](./listing-price.md)中定义的&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;不同的Amazon上市价格。 您还可以堆叠多个规则，甚至使用智能定价来根据竞争者的[[!DNL Buy Box]](./buy-box-competitor-pricing.md)价格或最低竞争者的[价格](./lowest-competitor-pricing.md)来调整您的Amazon上市价格。

定价规则有两种类型：

- [标准定价规则](./standard-price-rules.md)
- [智能重定价规则](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >如果将Amazon区域设置为`Inactive`状态，则智能重定价规则无法正常运行，因为该区域在载入期间。 您的定价计算取决于您的运费，并且您所在的地区必须处于`Active`状态，才能从Amazon同步运费。
   >
   >要更新Amazon帐户中的区域状态，请转到设置>帐户信息>假期设置。 请参阅[Amazon:列出假期的状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){:target=&quot;_blank&quot;}（需要卖家中心登录）。

此功能允许您以类似于[!DNL Commerce] [目录价格规则](https://docs.magento.com/user-guide/catalog/pricing.html){:target=&quot;_blank&quot;}的方式处理Amazon价格。 您可以创建复杂的规则，以便更改特定产品、特定类别中的产品，甚至包含特定属性的产品的价格。

您可以为Amazon列表添加定价规则。 价格规则可用于根据一组定义的条件自动调整您的上市价格。 在产品在Amazon上市之前，会触发价格规则并计算您的调整价格。

>[!NOTE]
>
>在[列表价格](./listing-price.md)设置中为&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;定义Amazon列表的价格源。 定价规则中定义的任何调整计算均使用价格来源作为起始值。

定价规则允许您在[上市价格](./listing-price.md)设置中设置与&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;不同的Amazon上市价格。 您还可以堆叠多个可协同工作的规则以调整价格。

定价/重新定价规则在设置过程中需要三组信息：

- [常规设置](./pricing-rule-general-settings.md):定义规则的名称、描述、活动日期、优先级，并根据规则的优先级设置后续规则的行为。
- [条件](./pricing-rule-conditions.md):确定哪些产品符合价格规则。
- [操作](./pricing-rule-actions.md):定义应用于价格来源以确定上市价格的调整计算。

您可以创建[标准定价规则](./standard-price-rules.md)，以根据您的[列价](./listing-price.md)设置中的选定&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;自动调整您的Amazon列价。 此功能允许您以类似于[!DNL Commerce] [目录价格规则](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}的方式处理Amazon价格。 您可以创建复杂的规则，以自动更改特定产品、特定类别内的产品或具有特定属性的产品的价格。 您可以完成传统设置，并根据固定金额或百分比对产品重新定价以增加或减少。

另一个功能强大的工具是[智能重定价](./intelligent-repricing-rules.md)功能，该功能可根据竞争者[[!DNL Buy Box]](./buy-box-competitor-pricing.md)价格或[最低竞争者价格](./lowest-competitor-pricing.md)调整您的Amazon列表价格。 与[!DNL Commerce] [目录价格规则](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}类似，此高级功能允许您通过创建复杂规则来操纵Amazon价格。 规则可以定义特定产品、特定类别内的产品，甚至特定产品属性的价格更改范围。

根据竞争对手的定价，使用智能重新定价来调整您的Amazon上市价格。 Amazon销售渠道为您提供了内置的防护措施，用于配置以保护利润率或避免将商家的价格与低反馈相匹配。 使用[智能重定价规则](./intelligent-repricing-rules.md),Amazon上市价格可以自动以固定金额或百分比金额（上下）进行操作，甚至可以按每个项目与[[!DNL Buy Box]](./buy-box-competitor-pricing.md)价格或[最低竞争者价格](./lowest-competitor-pricing.md)同步。 甚至可以堆叠规则，以提供无限的灵活性。

您可以控制规则的重要方面，例如活动/不活动状态、网站资格、可选日期范围和可选优先级级别（用于规则堆叠）。

例如，您可以为价格规则定义和设置条件，当满足条件时，该规则会在将您的列表价格发送到Amazon之前自动调整该价格。

另一个定价选项是[价格覆盖](./overrides.md)，在单个列表级别设置。 可以设置[价格覆盖](./overrides.md)，并且覆盖会忽略/优先于所有其他默认值、设置和规则。 可以为价格、处理时间、条件和卖方附注设置[override](./overrides.md)（少数情况除外）。

![定价规则](assets/amazon-pricing-rules.png)

## 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Name] | 定价规则的名称，在[定价规则常规设置](./pricing-rule-general-settings.md)中设置 |
| [!UICONTROL Rule Type] | 规则类型，在[定价规则操作](./pricing-rule-actions.md)中设置（标准价格规则或智能重定价规则） |
| [!UICONTROL Is Active] | 规则是否处于活动状态，如[定价规则常规设置](./pricing-rule-general-settings.md)中所设置 |
| [!UICONTROL Priority] | 与其他定价条件相比的优先级，如[定价规则常规设置](./pricing-rule-general-settings.md)中所设置 |
| [!UICONTROL Stop Further Rules Processing] | 指示是否对符合此规则的产品进一步处理任何价格规则，如[定价规则常规设置](./pricing-rule-general-settings.md)中所设置 |
| [!UICONTROL From Date] | 规则处于活动状态的时段的开始时间 |
| [!UICONTROL To Date] | 规则处于活动状态的时段的结束时间 |
| [!UICONTROL Action] | 列出可应用于特定列表的所有操作。 要应用某个操作，请单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**。 选项：`Edit Price Rule` / `Delete Price Rule` |
