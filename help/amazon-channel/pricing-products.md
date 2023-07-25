---
title: 管理Amazon定价
description: 您可以使用定价规则将Amazon清单的定价设置为与商务区不同。
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# 管理Amazon定价

Amazon sales channel允许您设置定价规则，从而允许您设置与定义的不同Amazon列表价格 **[!UICONTROL Magento Price Source]** 在您的 [挂牌价](./listing-price.md). 您还可以栈叠多个规则，甚至还可以使用智能定价，根据竞争对手的规则来调整您的Amazon上市价格 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 价格或 [最低竞争对手价格](./lowest-competitor-pricing.md).

有两种定价规则：

- [标准定价规则](./standard-price-rules.md)
- [智能重新定价规则](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >如果Amazon区域设置为，则智能重新定价规则无法正常运行 `Inactive` 状态，就像在载入过程中一样。 您的定价计算取决于您的运费，并且您的地区必须位于 `Active` 要从Amazon同步的运费状态。
  >
  >要更新Amazon帐户中的地区状态，请转到“设置”>“帐户信息”>“假期设置”。 请参阅 [Amazon：休假的列表状态](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) （需要以Seller Central登录）。

Amazon此功能允许您以类似于 [!DNL Commerce] [目录价格规则](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). 您可以创建复杂的规则，以便更改特定产品、特定类别内的产品甚至具有特定属性的价格。

您可以为Amazon列表添加定价规则。 价格规则可用于根据一组已定义的条件自动调整您的上市价格。 在产品在Amazon上上市之前，将触发价格规则并计算调整后的价格。

>[!NOTE]
>
>您为Amazon清单定义的价格来源 **[!UICONTROL Magento Price Source]** 在您的 [挂牌价](./listing-price.md) 设置。 定价规则中定义的任何调整计算都使用价格来源作为起始值。

定价规则允许您设置与您的Amazon不同的上市价格 **[!UICONTROL Magento Price Source]** 在您的 [挂牌价](./listing-price.md) 设置。 您还可以栈叠多个规则来共同调整价格。

定价/重新定价规则在设置过程中需要三组信息：

- [常规设置](./pricing-rule-general-settings.md)：定义规则的名称、描述、活动日期、优先级，并根据规则的优先级设置设置后续规则的行为。
- [条件](./pricing-rule-conditions.md)：确定哪些产品符合价格规则的要求。
- [操作](./pricing-rule-actions.md)：定义应用于价格来源的调整计算，以确定挂牌价格。

您可以创建 [标准定价规则](./standard-price-rules.md) 会自动调整相对于选定内容的Amazon挂牌价格 **[!UICONTROL Magento Price Source]** 在您的 [挂牌价](./listing-price.md) 设置。 Amazon此功能允许您以类似于 [!DNL Commerce] [目录价格规则](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). 您可以创建复杂的规则，以自动更改特定产品、特定类别内的产品或具有特定属性的产品的价格。 您可以完成传统设置，并重新定价产品，以根据固定金额或百分比增加或减少价格。

另一个强大的工具是 [智能重新定价](./intelligent-repricing-rules.md) 根据竞争对手调整Amazon挂牌价的功能 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 价格或 [最低竞争对手价格](./lowest-competitor-pricing.md). 与 [!DNL Commerce] [目录价格规则](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)，利用此高级功能，您可以通过创建复杂规则来操纵Amazon价格。 规则可以定义特定产品、特定类别中的产品，甚至具有特定产品属性的价格更改范围。

使用智能重新定价，根据竞争对手的定价调整您的Amazon上市价格。 Amazon sales channel内置了保护机制，可让您配置以保护利润率，或避免与低反馈商家的价格相匹配。 使用 [智能重定价规则](./intelligent-repricing-rules.md)，Amazon列表价格可以自动作为固定金额或百分比金额（向上或向下）进行处理，甚至可以与 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 价格或 [最低竞争对手价格](./lowest-competitor-pricing.md) 以每个项目为基础。 甚至可以栈叠规则以提供无限的灵活性。

您可以控制规则的重要方面，例如活动/不活动状态、网站资格、可选日期范围和可选优先级级别（用于规则栈叠）。

例如，您可以为价格规则定义和设置条件，以便在满足条件时，在将其发送到Amazon之前自动调整您的挂牌价格。

另一个定价选项是 [价格覆盖](./overrides.md)，在单个列表级别设置。 A [价格覆盖](./overrides.md) 可以设置，并且覆盖会忽略/优先于所有其他默认值、设置和规则。 An [覆盖](./overrides.md) 可以设置价格、处理时间、条件和卖方注释（少数例外）。

![定价规则](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## 默认列

| 列 | 描述 |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | 定价规则的名称，如中所设置 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | 规则类型，如中所设置 [定价规则操作](./pricing-rule-actions.md) （标准价格规则或智能重新定价规则） |
| [!UICONTROL Is Active] | 规则是否处于活动状态（如中所设置） [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | 优先于其他定价条件，如 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | 指示是否对符合此规则条件的产品处理任何其他价格规则，如中所设置 [定价规则常规设置](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | 规则处于活动状态的时段的开始 |
| [!UICONTROL To Date] | 规则处于活动状态的时段的结束 |
| [!UICONTROL Action] | 列出可应用于特定列表的所有操作。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列。 选项： `Edit Price Rule` / `Delete Price Rule` |
