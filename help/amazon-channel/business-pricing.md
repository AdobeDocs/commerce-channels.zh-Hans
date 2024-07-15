---
title: "[!DNL (B2B) Business Price] for Amazon列表"
description: 通过在Amazon [!DNL Seller Central] 帐户中启用业务，您可以在Amazon业务(B2B)网站上列出 [!DNL Commerce] 商店产品。
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# 用于Amazon列表的[!DNL (B2B) Business Price]

(B2B)业务价格设置是商店列表设置的一部分。 列表设置可从[Amazon应用商店仪表板](./amazon-store-dashboard.md)访问。

[!DNL Amazon Business]是Amazon注册企业帐户专属的市场，仅在美国、法国、德国和英国可用。 如果Marketplace允许B2B业务定价，则可以在列表设置中进行编辑。

[!DNL B2B Business Pricing]允许拥有业务帐户的商户以Amazon购物体验的预期性能互相购买。 通过B2B业务定价，企业可以根据购买的数量提供分层定价。

对于要列在[!DNL Amazon Business (B2B)]网站上的产品，必须首先在[!DNL Amazon Seller Central]帐户中启用业务。 有关B2B功能的详细信息，请参阅[Amazon： B2B Central](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"}（需要卖方中心登录）。

## 配置[!DNL (B2B) Business Price]设置

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL (B2B) Business Price]_部分。

1. 为&#x200B;**[!UICONTROL Enable Business Pricing]**&#x200B;选择一个选项。

   - `Disabled` — （默认）选择您不想启用企业对企业销售的时间。 选择后，将禁用此分区中的所有其他字段。

   - `Enabled` — 选择何时启用企业对企业的销售。 启用后，业务价格将设置为等于应用所有定价规则后的价目表价格。 业务价格遵循网站定价范围（如果启用）。 业务价格不得低于1美元。

1. 为&#x200B;**[!UICONTROL Enable Tiered Pricing]**&#x200B;选择一个选项。

   - `Disabled` — （默认）当您希望对所有订单数量使用相同的列表价格时，请选择此选项。 选中后，此分区中的所有&#x200B;_[!UICONTROL Pricing Level]_字段都将被禁用。

   - `Enabled` — 选择何时启用基于订单数量的定价调整。 选择后，将启用&#x200B;_[!UICONTROL Pricing Level]_字段。

1. 完成&#x200B;**[!UICONTROL Pricing Level]**&#x200B;设置。

   您最多可以定义5个数量/折扣设置，用于设置业务清单的层定价。 在每行中，输入要应用的数量阈值和折扣百分比。 例如，如果您在第一行的第一个字段中输入`5`，在第二个字段中输入`5`，则当其他企业购买的数量为5个或更多时，该价格将应用5%的折扣。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![Amazon业务定价(B2B)](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | 选项： <ul><li>**[!UICONTROL Disabled]** — （默认）选择您不想启用Business到Business销售的时间。 选中后，将禁用此分区中的所有其他字段。</li><li>**[!UICONTROL Enabled]** — 选择何时启用业务对业务销售。 选择此选项后，业务价格将设置为等于应用所有定价规则后的价目表价格。 业务价格遵循网站定价范围（如果启用）。 业务价格不得低于1美元。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | （必需）选项： <ul><li>**[!UICONTROL Disabled]** — （默认）当您希望对所有订单数量使用相同的列表价格时，请选择此选项。 选中后，此分区中的所有&#x200B;_[!UICONTROL Pricing Level]_字段都将被禁用。</li><li>**[!UICONTROL Enabled]** — 选择何时启用根据订货量进行调整的定价。 选择后，将启用&#x200B;_[!UICONTROL Pricing Level]_字段。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | 启用“分层定价”后，您最多可以定义5个数量/折扣设置来为您的业务列表设置分层定价。 在每行中，输入要应用的数量阈值和折扣百分比。 例如，如果您在第一行的第一个字段中输入`5`，在第二个字段中输入`5`，则当其他企业购买的数量为5个或更多时，该价格将应用5%的折扣。 |

**快速访问** - [!UICONTROL Listing Settings]分区

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
