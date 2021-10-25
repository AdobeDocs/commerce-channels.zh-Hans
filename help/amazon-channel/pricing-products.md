---
title: 管理Amazon定价
description: 您可以使用定价规则将Amazon列表的定价设置为与您的电子商务商店不同。
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# 管理Amazon定价

Amazon销售渠道允许您设置定价规则，以便将Amazon上市价格设置为与定义的 **[!UICONTROL Magento Price Source]** 在 [挂牌价格](./listing-price.md). 您还可以堆叠多个规则，甚至使用智能定价根据竞争对手的 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 价格或 [最低竞争者价格](./lowest-competitor-pricing.md).

定价规则有两种类型：

- [标准定价规则](./standard-price-rules.md)
- [智能重定价规则](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >如果将Amazon区域设置为 `Inactive` 状态，与载入期间一样。 您的定价计算取决于您的运费，您所在的地区必须在 `Active` 从Amazon同步的运费状态。
   >
   >要更新Amazon帐户中的区域状态，请转到设置>帐户信息>假期设置。 请参阅 [Amazon:假期的列表状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){target=&quot;_blank&quot;}（需要卖家中心登录）。

此功能允许您以类似于 [!DNL Commerce] [目录价格规则](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。 您可以创建复杂的规则，以便更改特定产品、特定类别中的产品，甚至包含特定属性的产品的价格。

您可以为Amazon列表添加定价规则。 价格规则可用于根据一组定义的条件自动调整您的上市价格。 在产品在Amazon上市之前，会触发价格规则并计算您的调整价格。

>[!NOTE]
>
>您的Amazon列表的价格来源是 **[!UICONTROL Magento Price Source]** 在 [挂牌价格](./listing-price.md) 设置。 定价规则中定义的任何调整计算均使用价格来源作为起始值。

定价规则允许您将Amazon的上市价格设置为与 **[!UICONTROL Magento Price Source]** 在 [挂牌价格](./listing-price.md) 设置。 您还可以堆叠多个可协同工作的规则以调整价格。

定价/重新定价规则在设置过程中需要三组信息：

- [常规设置](./pricing-rule-general-settings.md):定义规则的名称、描述、活动日期、优先级，并根据规则的优先级设置后续规则的行为。
- [条件](./pricing-rule-conditions.md):确定哪些产品符合价格规则。
- [操作](./pricing-rule-actions.md):定义应用于价格来源以确定上市价格的调整计算。

您可以创建 [标准定价规则](./standard-price-rules.md) 可自动调整您的Amazon上市价格(相对于选定的 **[!UICONTROL Magento Price Source]** 在 [挂牌价格](./listing-price.md) 设置。 此功能允许您以类似于 [!DNL Commerce] [目录价格规则](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}。 您可以创建复杂的规则，以自动更改特定产品、特定类别内的产品或具有特定属性的产品的价格。 您可以完成传统设置，并根据固定金额或百分比对产品重新定价以增加或减少。

另一个强大的工具是 [智能重定价](./intelligent-repricing-rules.md) 根据竞争对手调整Amazon上市价格的功能 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 价格或 [竞争者最低价格](./lowest-competitor-pricing.md). 与 [!DNL Commerce] [目录价格规则](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}，此高级功能允许您通过创建复杂规则来操纵Amazon价格。 规则可以定义特定产品、特定类别内的产品，甚至特定产品属性的价格更改范围。

根据竞争对手的定价，使用智能重新定价来调整您的Amazon上市价格。 Amazon销售渠道为您提供了内置的防护措施，用于配置以保护利润率或避免将商家的价格与低反馈相匹配。 使用 [智能重定价规则](./intelligent-repricing-rules.md)，则Amazon上市价格可自动以固定或百分比金额（上升或下降）进行操作，甚至可以同步到 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 价格或 [竞争者最低价格](./lowest-competitor-pricing.md) 按每个项目计算。 甚至可以堆叠规则，以提供无限的灵活性。

您可以控制规则的重要方面，例如活动/不活动状态、网站资格、可选日期范围和可选优先级级别（用于规则堆叠）。

例如，您可以为价格规则定义和设置条件，当满足条件时，该规则会在将您的列表价格发送到Amazon之前自动调整该价格。

另一个定价选项是 [价格覆盖](./overrides.md)，在单个列表级别设置。 A [价格覆盖](./overrides.md) ，并且覆盖会忽略/优先于所有其他默认值、设置和规则。 安 [覆盖](./overrides.md) 可以为价格、处理时间、条件和卖家附注设置（少数情况除外）。

![定价规则](assets/amazon-pricing-rules.png)

## 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Name] | 定价规则的名称，在 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | 规则类型，在 [定价规则操作](./pricing-rule-actions.md) （标准价格规则或智能重定价规则） |
| [!UICONTROL Is Active] | 规则是否处于活动状态(如 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | 优先于其他定价条件(如 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | 指示是否对符合此规则的产品进一步处理任何价格规则，如 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | 规则处于活动状态的时段的开始时间 |
| [!UICONTROL To Date] | 规则处于活动状态的时段的结束时间 |
| [!UICONTROL Action] | 列出可应用于特定列表的所有操作。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列。 选项： `Edit Price Rule` / `Delete Price Rule` |
