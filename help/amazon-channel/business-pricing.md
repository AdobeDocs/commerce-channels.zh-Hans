---
title: ”[!DNL (B2B) Business Price] 用于Amazon列表”
description: 您可以列出您的 [!DNL Commerce] 通过在Amazon中启用业务来在Amazon Business (B2B)网站上存储产品 [!DNL Seller Central] 帐户。
redirect_from: /sales-channels/asc/ob-business-pricing.html
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# [!DNL (B2B) Business Price] 对于Amazon列表

(B2B)业务价格设置是商店列表设置的一部分。 列表设置可从以下位置访问： [Amazon store功能板](./amazon-store-dashboard.md).

[!DNL Amazon Business] 是一个专属于Amazon注册商业帐户的市场，仅在美国、法国、德国和英国可用。 如果市场允许B2B业务定价，则可在列表设置中对其进行编辑。

[!DNL B2B Business Pricing] 允许具有商业帐户的商家彼此之间以Amazon购物体验的预期性能进行购买。 通过B2B业务定价，企业可以根据购买的数量提供分层定价。

您的产品将列在 [!DNL Amazon Business (B2B)] 网站中，您必须首先在 [!DNL Amazon Seller Central] 帐户。 有关B2B功能的更多信息，请参阅 [Amazon：B2B Central](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} （需要Seller Central登录）。

## 配置 [!DNL (B2B) Business Price] 设置

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL (B2B) Business Price]_部分。

1. 对象 **[!UICONTROL Enable Business Pricing]**，选择一个选项。

   - `Disabled`  — （默认）选择您不想启用企业对企业销售的时间。 选择后，此部分中的所有其他字段都将被禁用。

   - `Enabled`  — 选择何时启用企业对企业的销售。 启用后，业务价格将设置为等于应用所有定价规则后的价目表价格。 业务价格遵循网站定价范围（如果已启用）。 商业价格不能低于1美元。

1. 对象 **[!UICONTROL Enable Tiered Pricing]**，选择一个选项。

   - `Disabled`  — （默认值）选择何时需要所有订单数量的相同列表价格。 选择后，所有 _[!UICONTROL Pricing Level]_此分区中的字段已禁用。

   - `Enabled`  — 选择何时启用基于订单数量的定价调整。 选择后， _[!UICONTROL Pricing Level]_字段已启用。

1. 完成 **[!UICONTROL Pricing Level]** 设置。

   您最多可以定义5个数量/折扣设置，用于设置业务清单的层定价。 在每行中，输入要应用的数量阈值和折扣百分比。 例如，如果您输入 `5` 在第一行的第一个字段中，并 `5` 在第二个字段中，当其他企业购买数量为5个或更多时，该价格将应用5%的折扣。

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![Amazon Business Pricing (B2B)](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Enable Business Pricing] | 选项： <ul><li>**[!UICONTROL Disabled]**  — （默认）选择您不想启用B2B销售的时间。 选中后，将禁用此分区中的所有其他字段。</li><li>**[!UICONTROL Enabled]**  — 选择何时让您的业务对企业销售启用。 选择后，业务价格将设置为等于所有定价规则应用后的价目表价格。 业务价格遵循网站定价范围（如果已启用）。 商业价格不能低于1美元。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | （必需）选项： <ul><li>**[!UICONTROL Disabled]**  — （默认值）选择何时需要所有订单数量的相同列表价格。 选择后，所有 _[!UICONTROL Pricing Level]_此分区中的字段已禁用。</li><li>**[!UICONTROL Enabled]**  — 选择何时启用根据订货量进行调整的定价。 选择后， _[!UICONTROL Pricing Level]_字段已启用。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | 启用“分层定价”后，您最多可以定义5个数量/折扣设置来为您的业务列表设置分层定价。 在每行中，输入要应用的数量阈值和折扣百分比。 例如，如果您输入 `5` 在第一行的第一个字段中，并 `5` 在第二个字段中，当另一个企业购买数量达到或超过五件时，该价格将应用5%的折扣。 |

**快速访问** - [!UICONTROL Listing Settings] 区域

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
