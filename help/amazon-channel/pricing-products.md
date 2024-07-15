---
title: 管理Amazon定价
description: 您可以使用定价规则将Amazon清单的定价设置为与Commerce应用商店不同。
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 管理Amazon定价

Amazon sales channel允许您设置定价规则，从而允许您设置与[列表价格](./listing-price.md)中定义的&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;不同的Amazon列表价格。 您还可以栈叠多个规则，甚至使用智能定价根据竞争对手的[[!DNL Buy Box]](./buy-box-competitor-pricing.md)价格或[最低竞争对手价格](./lowest-competitor-pricing.md)来调整您的Amazon上市价格。

定价规则有两种类型：

- [标准定价规则](./standard-price-rules.md)
- [智能重新定价规则](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >如果Amazon区域设置为`Inactive`状态（与载入期间一样），则智能重新定价规则无法正常运行。 您的定价计算取决于您的运费，并且您的地区必须处于`Active`状态，您的运费才能与Amazon同步。
  >
  >要在Amazon帐户中更新您所在地区的状态，请转到“设置”>“帐户信息”>“假期设置”。 请参阅[Amazon：假期列表状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) （需要卖方中心登录）。

此功能允许您以类似于[!DNL Commerce] [目录价格规则](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html)的方式操纵Amazon价格。 您可以创建复杂的规则，以便更改特定产品、特定类别中的产品甚至具有特定属性的价格。

您可以为Amazon列表添加定价规则。 价格规则可用于根据一组已定义的条件自动调整您的上市价格。 在产品在Amazon上上市之前，将触发价格规则并计算调整后的价格。

>[!NOTE]
>
>在您的[列表价格](./listing-price.md)设置中，已为&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;定义Amazon列表的价格源。 定价规则中定义的任何调整计算均使用价格来源作为起始值。

定价规则允许您在[列表价格](./listing-price.md)设置中将您的Amazon列表价格设置为与&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;不同的价格。 您还可以栈叠多个规则来共同调整价格。

定价/重新定价规则在设置过程中需要三组信息：

- [常规设置](./pricing-rule-general-settings.md)：定义规则的名称、描述、活动日期、优先级，并根据其优先级设置设置后续规则的行为。
- [条件](./pricing-rule-conditions.md)：确定哪些产品符合价格规则的条件。
- [操作](./pricing-rule-actions.md)：定义应用于价格来源的调整计算，以确定上市价格。

您可以创建[标准定价规则](./standard-price-rules.md)，以自动调整您的Amazon上市价格（相对于您在[上市价格](./listing-price.md)设置中选择的&#x200B;**[!UICONTROL Magento Price Source]**）。 此功能允许您以类似于[!DNL Commerce] [目录价格规则](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)的方式操纵Amazon价格。 您可以创建复杂的规则，以自动更改特定产品、特定类别内的产品或具有特定属性的产品的价格。 您可以完成传统设置，并重新定价产品，以根据固定金额或百分比增加或减少价格。

另一个功能强大的工具是[智能重新定价](./intelligent-repricing-rules.md)功能，该功能可根据竞争对手[[!DNL Buy Box]](./buy-box-competitor-pricing.md)价格或[最低竞争对手价格](./lowest-competitor-pricing.md)来调整Amazon的上市价格。 与[!DNL Commerce] [目录价格规则](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)类似，此高级功能允许您通过创建复杂规则来操纵Amazon价格。 规则可以定义特定产品、特定类别中的产品甚至具有特定产品属性的价格更改范围。

使用智能重新定价，根据竞争对手的定价调整您的Amazon上市价格。 Amazon sales channel内置了保护功能，可让您配置保护利润率，或避免与反馈率较低的商家的价格相匹敌。 使用[智能重新定价规则](./intelligent-repricing-rules.md)，Amazon列表价格可以自动按固定金额或百分比金额（涨价或跌价）进行处理，甚至可以按每个项目与[[!DNL Buy Box]](./buy-box-competitor-pricing.md)价格或[最低竞争对手价格](./lowest-competitor-pricing.md)同步。 甚至可以栈叠规则以提供无限的灵活性。

您可以控制规则的重要方面，如活动/不活动状态、网站资格、可选日期范围和可选优先级（用于规则栈叠）。

例如，您可以为价格规则定义和设置条件，以便在满足条件时自动调整您的挂牌价格，然后再将其发送至Amazon。

另一个定价选项是在单个列表级别设置的[价格覆盖](./overrides.md)。 可以设置[价格覆盖](./overrides.md)，并且覆盖将忽略/优先于所有其他默认值、设置和规则。 可以为价格、处理时间、条件和卖方备注设置[覆盖](./overrides.md)（少数例外）。

![定价规则](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## 默认列

| 列 | 描述 |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | 定价规则的名称，在[定价规则常规设置](./pricing-rule-general-settings.md)中设置 |
| [!UICONTROL Rule Type] | 在[定价规则操作](./pricing-rule-actions.md)中设置的规则类型（标准价格规则或智能重新定价规则） |
| [!UICONTROL Is Active] | 该规则是否处于活动状态，如[定价规则常规设置](./pricing-rule-general-settings.md)中所设置 |
| [!UICONTROL Priority] | 优先于其他定价条件，如[定价规则常规设置](./pricing-rule-general-settings.md)中所设置 |
| [!UICONTROL Stop Further Rules Processing] | 指示是否对符合此规则的产品处理任何其他价格规则，如[定价规则常规设置](./pricing-rule-general-settings.md)中所设置 |
| [!UICONTROL From Date] | 规则处于活动状态的时段的开始 |
| [!UICONTROL To Date] | 规则处于活动状态的时段的结束 |
| [!UICONTROL Action] | 列出可应用于特定列表的所有操作。 要应用操作，请单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**。 选项： `Edit Price Rule` / `Delete Price Rule` |
