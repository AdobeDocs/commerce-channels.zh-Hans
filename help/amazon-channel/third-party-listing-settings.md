---
title: 第三方列表
description: 更新第三方列表设置，以确定您的商务目录是否从现有的Amazon销售中心列表中导入产品。
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 第三方列表

第三方列表设置是您的商店列表设置的一部分。 列表设置可从 [存储仪表板](./amazon-store-dashboard.md).

这些设置可确定 [!DNL Commerce] 从现有目录导入产品 [!DNL Amazon Seller Central] 列表。 最好从Amazon导入列表，以确保所有列表都具有匹配的 [!DNL Commerce] 产品。 列表是 [!DNL Commerce] 目录下，您可以从单个目录管理所有产品，并使用Amazon销售渠道功能。 这些功能包括Amazon的履行和订单管理、智能重定价和数量管理。

当配置为导入Amazon列表时，Amazon销售渠道会将您的Amazon列表导入 [!DNL Commerce] 目录，尝试将它们与现有产品进行匹配。 如果未自动找到匹配项，则可以将Amazon列表导入为 [!DNL Commerce] 产品或手动将列表与产品进行匹配。

如果选择导入Amazon列表，请选择 [!DNL Commerce] 属性，其值分别适用于Amazon卖家SKU和Amazon ASIN。 如果您没有 [!DNL Commerce] [产品属性](./ob-creating-magento-attributes.md)，请考虑创建和分配它们。 映射这些属性有助于将导入的Amazon列表与 [!DNL Commerce] 产品。

初始列表导入在 [存储集成](./store-integration.md) 完成。 之后，根据你的密码设置， [!DNL Commerce] 持续检查新添加的Amazon列表(未在AmazonSales Channel中创建)，并更新您的 [!DNL Commerce] 目录。

## 配置第三方列表设置

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Third Party Listings]_中。

1. 对于 **[!UICONTROL Import Third Party Listings]** （必需），选择选项：

   - `Import Listing`  — （默认）选择您希望何时将Amazon列表中的产品信息导入 [!DNL Commerce] 产品目录。 此选项是默认选项，建议使用此选项。

   - `Do Not Import Listing`  — 选择要手动执行的时间 [创建和分配新产品](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} [!DNL Commerce] 目录。
   >[!NOTE]
   >以下选项字段仅在设置为时才处于活动状态 `Import Listing`.

1. 对于 **[!UICONTROL Attribute That Contains Amazon Seller SKU]**，选择 [!DNL Commerce] 与Amazon卖家SKU值匹配的属性。

1. 对于 **[!UICONTROL Attribute That Contains Amazon ASIN]**，选择 [!DNL Commerce] 属性，并将其与Amazon ASIN匹配。

   >[!NOTE]
   >如果您未创建这些 [!DNL Commerce] Amazon列表的属性，请参阅 [为Amazon匹配创建属性](./ob-creating-magento-attributes.md).

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![第三方列表](assets/amazon-third-party-listings.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Import Third Party Listings] | 必需。 选项：<ul><li>**[!UICONTROL Import Listing]**  — （默认）选择您希望何时将Amazon列表中的产品信息导入 [!DNL Commerce] 产品目录。 </li><li>**[!UICONTROL Do Not Import Listing]**  — 选择要手动执行的时间 [创建和分配新产品](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;} [!DNL Commerce] 目录。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | 仅在设置为时处于活动状态 `Import Listing`.<br>选择 [!DNL Commerce] 属性与Amazon卖家SKU的Amazon属性的匹配。 如果此属性不存在，请参阅 [为Amazon匹配创建Amazon产品属性](./ob-creating-magento-attributes.md). 如果需要，请查看 [!DNL Commerce] [属性](./managing-attributes.md) 并创建或编辑与此Amazon数据匹配的属性。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | 仅在设置为时处于活动状态 `Import Listing`.<br>选择 [!DNL Commerce] 与Amazon ASIN的Amazon属性匹配的属性。 如果此属性不存在，请参阅 [为Amazon匹配创建Amazon产品属性](./ob-creating-magento-attributes.md). 如果需要，请查看 [!DNL Commerce] [属性](./managing-attributes.md) 并创建或编辑与此Amazon数据匹配的属性。 |

**快速访问** - [!UICONTROL Listing Settings] 章节

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
