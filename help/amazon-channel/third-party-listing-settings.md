---
title: AmazonSales Channel- [!UICONTROL Third-party Listings]
description: 更新第三方列表设置可确定您的Commerce目录是否从现有Amazon销售商中心列表导入产品。
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

第三方列表设置是商店列表设置的一部分。 列表设置可从[存储仪表板](./amazon-store-dashboard.md)访问。

这些设置确定您的[!DNL Commerce]目录是否从现有[!DNL Amazon Seller Central]列表导入产品。 最佳做法是从Amazon导入列表，以确保所有列表都具有匹配的[!DNL Commerce]产品。 当您的列表包含在[!DNL Commerce]目录中时，您可以从单个目录管理您的所有产品，并使用Amazon销售渠道功能。 这些功能包括使用Amazon进行履行和订单管理、智能重新定价以及数量管理。

当配置为导入Amazon列表时，Amazon Sales Channel会将您的Amazon列表导入您的[!DNL Commerce]目录，并尝试将它们与现有产品匹配。 如果未自动找到匹配项，您可以将Amazon列表导入为新的[!DNL Commerce]产品，或手动将该列表与某个产品进行匹配。

如果选择导入Amazon列表，请选择包含Amazon销售方SKU和Amazon ASIN值的[!DNL Commerce]属性。 如果您没有[!DNL Commerce] [产品属性](./ob-creating-magento-attributes.md)，请考虑创建和分配这些属性。 映射这些属性有助于将导入的Amazon列表正确匹配到您的[!DNL Commerce]产品。

在[存储集成](./store-integration.md)完成时启动初始列表导入。 之后，根据您的cron设置，[!DNL Commerce]会不断检查新添加的Amazon列表(未在AmazonSales Channel中创建)，并根据您的第三方列表设置更新您的[!DNL Commerce]目录。

## 配置第三方列表设置

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Third Party Listings]_部分。

1. 对于&#x200B;**[!UICONTROL Import Third Party Listings]** （必需），请选择一个选项：

   - `Import Listing` — （默认）选择何时将Amazon清单中的产品信息导入到[!DNL Commerce]产品目录中。 此选项是默认选项，建议使用此选项。

   - `Do Not Import Listing` — 选择何时要手动[为Amazon列表创建新产品](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html)并将其分配给您的[!DNL Commerce]目录。

   >[!NOTE]
   >以下选项字段仅在设置为`Import Listing`时处于活动状态。

1. 对于&#x200B;**[!UICONTROL Attribute That Contains Amazon Seller SKU]**，选择与Amazon销售方SKU值匹配的[!DNL Commerce]属性。

1. 对于&#x200B;**[!UICONTROL Attribute That Contains Amazon ASIN]**，选择您创建的[!DNL Commerce]属性，并将其与Amazon ASIN匹配。

   >[!NOTE]
   >如果您没有为Amazon列表创建这些[!DNL Commerce]属性，请参阅[为Amazon匹配创建属性](./ob-creating-magento-attributes.md)。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![第三方列表](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | 必需。 选项：<ul><li>**[!UICONTROL Import Listing]** — （默认）选择何时将Amazon清单中的产品信息导入到[!DNL Commerce]产品目录中。 </li><li>**[!UICONTROL Do Not Import Listing]** — 选择何时要手动[为Amazon列表创建新产品](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html)并将其分配给您的[!DNL Commerce]目录。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | 仅在设置为`Import Listing`时处于活动状态。<br>选择[!DNL Commerce]属性作为与Amazon销售商SKU的Amazon属性的匹配项。 如果此属性不存在，请参阅[为Amazon匹配创建Amazon产品属性](./ob-creating-magento-attributes.md)。 如果需要，请检查您的[!DNL Commerce] [属性](./managing-attributes.md)，并创建或编辑属性以匹配此Amazon数据。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | 仅在设置为`Import Listing`时处于活动状态。<br>选择与Amazon ASIN的Amazon属性匹配的[!DNL Commerce]属性。 如果此属性不存在，请参阅[为Amazon匹配创建Amazon产品属性](./ob-creating-magento-attributes.md)。 如果需要，请检查您的[!DNL Commerce] [属性](./managing-attributes.md)，并创建或编辑属性以匹配此Amazon数据。 |

**快速访问** - [!UICONTROL Listing Settings]分区

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
