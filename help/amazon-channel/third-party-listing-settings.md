---
title: 第三方列表
description: 更新第三方列表设置，以确定您的商务目录是否从现有的Amazon销售中心列表中导入产品。
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 第三方列表

第三方列表设置是您的商店列表设置的一部分。 可从[存储功能板](./amazon-store-dashboard.md)访问列表设置。

这些设置可确定[!DNL Commerce]目录是否从现有[!DNL Amazon Seller Central]列表导入产品。 最好从Amazon导入列表，以确保所有列表都具有匹配的[!DNL Commerce]产品。 如果您的列表是[!DNL Commerce]目录的一部分，则可以从单个目录管理所有产品并使用Amazon销售渠道功能。 这些功能包括Amazon的履行和订单管理、智能重定价和数量管理。

当配置为导入Amazon列表时，Amazon销售渠道会将您的Amazon列表导入[!DNL Commerce]目录，尝试将它们与现有产品进行匹配。 如果未自动找到匹配项，您可以将Amazon列表导入为新的[!DNL Commerce]产品，或手动将列表与产品进行匹配。

如果选择导入Amazon列表，请选择[!DNL Commerce]属性，其中包含Amazon卖家SKU和Amazon ASIN的值。 如果您没有[!DNL Commerce] [产品属性](./ob-creating-magento-attributes.md)，请考虑创建和分配它们。 映射这些属性有助于将导入的Amazon列表与您的[!DNL Commerce]产品正确匹配。

完成[存储集成](./store-integration.md)时，将启动初始列表导入。 之后，根据您的cron设置， [!DNL Commerce]会持续检查新添加的Amazon列表(未在AmazonSales Channel中创建)，并根据第三方列表设置更新您的[!DNL Commerce]目录。

## 配置第三方列表设置

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Third Party Listings]_部分。

1. 对于&#x200B;**[!UICONTROL Import Third Party Listings]**（必需），选择一个选项：

   - `Import Listing`  — （默认）选择您希望何时将Amazon列表中的产品信息导入产 [!DNL Commerce] 品目录。此选项是默认选项，建议使用此选项。

   - `Do Not Import Listing`  — 选择您希望何时手 [动创建新产品并将](https://docs.magento.com/user-guide/catalog/products.html){:target=&quot;_blank&quot;}分配给您的Amazon [!DNL Commerce] 列表目录。
   >[!NOTE]
   >以下选项字段仅在设置为`Import Listing`时才处于活动状态。

1. 对于&#x200B;**[!UICONTROL Attribute That Contains Amazon Seller SKU]**，选择与Amazon卖家SKU值匹配的[!DNL Commerce]属性。

1. 对于&#x200B;**[!UICONTROL Attribute That Contains Amazon ASIN]**，选择您创建的[!DNL Commerce]属性，并将其与Amazon ASIN匹配。

   >[!NOTE]
   >如果您没有为Amazon列表创建这些[!DNL Commerce]属性，请参阅[为Amazon匹配创建属性](./ob-creating-magento-attributes.md) 。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![第三方列表](assets/amazon-third-party-listings.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Import Third Party Listings] | 必需。 选项：<ul><li>**[!UICONTROL Import Listing]**  — （默认）选择您希望何时将Amazon列表中的产品信息导入产 [!DNL Commerce] 品目录。 </li><li>**[!UICONTROL Do Not Import Listing]**  — 选择您希望何时手 [动创建新产品并将](https://docs.magento.com/user-guide/catalog/products.html){:target=&quot;_blank&quot;}分配给您的Amazon [!DNL Commerce] 列表目录。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | 仅在设置为`Import Listing`时处于活动状态。<br>选择该 [!DNL Commerce] 属性作为与Amazon卖家SKU的Amazon属性的匹配项。如果此属性不存在，请参阅[为Amazon Matching](./ob-creating-magento-attributes.md)创建Amazon产品属性。 如果需要，请查看[!DNL Commerce] [属性](./managing-attributes.md)，并创建或编辑与此Amazon数据匹配的属性。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | 仅在设置为`Import Listing`时处于活动状态。<br>选择与 [!DNL Commerce] Amazon ASIN的Amazon属性匹配的属性。如果此属性不存在，请参阅[为Amazon Matching](./ob-creating-magento-attributes.md)创建Amazon产品属性。 如果需要，请查看[!DNL Commerce] [属性](./managing-attributes.md)，并创建或编辑与此Amazon数据匹配的属性。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
