---
title: 目录搜索
description: 要设置属性匹配，以帮助将符合条件的商务目录产品与Amazon列表进行映射，请更新“目录搜索”设置。
redirect_from: /sales-channels/asc/ob-catalog-search.html: 
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 981
ht-degree: 0%

---

# 目录搜索

_目录_ 搜索设置是商店列表设置的一部分。可从[存储功能板](./amazon-store-dashboard.md)访问列表设置。

通过这些设置，可设置属性匹配，以帮助将符合条件的[!DNL Commerce]产品与Amazon列表进行映射。 映射后，Amazon将激活与定价、数量、改写以及订单和产品同步相关的活动。

定义这些映射值会增加进行精确匹配的可能性，从而最大限度地减少手动匹配产品清单的需要。 将属性添加为[预设置任务](./amazon-pre-setup-tasks.md)的一部分，Amazon销售渠道在Amazon和[!DNL Commerce]之间载入和同步产品数据期间更有可能自动匹配您的产品。

如果仅创建Amazon ASIN属性（不为每个产品添加ASIN值），则[!DNL Commerce]产品可能不会自动与您的Amazon列表匹配。 您可以[手动分配](./creating-assigning-catalog-products.md)您的产品。 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您手动匹配某个产品，并且想要更新该产品的ASIN、UPC或其他数据元素，则必须在两个位置更新数据。 在[!DNL Commerce]目录和[!DNL Amazon Seller Central]帐户的Amazon列表中更新它。

最佳做法是映射这些属性和值（如果可用）。 无需完成此映射，但这有利于产品匹配，而且需要在Amazon和[!DNL Commerce]之间正确同步目录。

如果要添加属性，请参阅[为Amazon Matching](./ob-creating-magento-attributes.md)创建产品属性。

## 配置[!UICONTROL Catalog Search]设置

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Catalog Search]_部分。

1. 对于&#x200B;**[!UICONTROL ASIN]**，选择为Amazon ASIN值创建的产品属性。

   ASIN([!DNL Amazon Standard Identification Number])是由十个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。

1. 对于&#x200B;**[!UICONTROL EAN]**，选择为Amazon EAN值创建的产品属性。

   欧洲文章编号(EAN)是条形码标准，是12位或13位产品标识代码。 每个EAN都唯一标识产品、制造商及其属性；通常，EAN将作为条形码打印在产品标签或包装上。 Amazon要求使用EAN代码来提高搜索结果质量和目录质量。 您可以从制造商处获取EAN。

1. 对于&#x200B;**[!UICONTROL GCID]**，选择为Amazon GCIN值创建的产品属性。

   全局目录标识符(GCID)是指没有UPC代码或ISBN的产品的ID。 Amazon的Brand Registry允许您注册为品牌所有者，并为产品创建唯一ID。

1. 对于&#x200B;**[!UICONTROL ISBN]**，选择您为Amazon ISBN值创建的产品属性。

   国际标准书号(ISBN)是唯一的商业书籍标识码条形码。 每个ISBN代码都唯一地标识一本书。 ISBN有10位或13位。 2007年1月1日之后分配的所有ISBN都有13位数字。

1. 对于&#x200B;**[!UICONTROL UPC]**，选择为Amazon UPC值创建的产品属性。

   通用产品代码(UPC)是一个12位条形码，广泛用于美国的零售包装。

1. 对于&#x200B;**[!UICONTROL General Search]**，选择要用于常规搜索匹配的产品属性。

   此属性可供您选择，以将[!DNL Commerce]产品与相应的Amazon列表进行匹配。 常规搜索使用目录中的关键词搜索。 因此，建议使用带有相关关键字（如产品SKU或产品名称）的[!DNL Commerce]属性。 常规搜索可能会返回许多可能的匹配项，在这种情况下，您可以从可能的匹配项中选择相应的Amazon列表。 此字段的常见选择是`Product Name`。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![目录搜索](assets/amazon-catalog-search.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一块，用于标识项目。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]。ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。 |
| [!UICONTROL EAN (European Article Number)] | 12位或13位产品标识码。 欧洲文章编号(EAN)是条形码标准，是12位或13位产品标识代码。 每个EAN都唯一标识产品、制造商及其属性；通常，EAN将作为条形码打印在产品标签或包装上。 Amazon要求使用EAN代码来提高搜索结果质量和目录质量。 您可以从制造商处获取EAN。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | 全局目录标识符(GCID)是指没有UPC代码或ISBN的产品的ID。 Amazon的品牌注册允许您注册为品牌所有者，并为可能没有UPC或ISBN的产品创建唯一ID。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 10位或13位唯一商业书籍标识符条形码。 国际标准书号(ISBN)是唯一的商业书籍标识码条形码。 每个ISBN代码都唯一地标识一本书。 ISBN有10位或13位。 2007年1月1日之后分配的所有ISBN都有13位数字。 |
| UPC（通用产品代码） | 12位的条形码。 通用产品代码(UPC)是一个12位条形码，广泛用于美国的零售包装。 |
| [!UICONTROL General Search] | 选择属性。 此属性可供您选择，以将[!DNL Commerce]产品与相应的Amazon列表进行匹配。 常规搜索使用目录中的关键词搜索。 因此，建议使用带有相关关键字（如产品SKU或产品名称）的[!DNL Commerce]属性。 常规搜索可能会返回许多可能的匹配项，在这种情况下，您可以从可能的匹配项中选择相应的Amazon列表。 此字段的常见选择是`Product Name`。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
