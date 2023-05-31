---
title: Amazon列表的目录搜索
description: 要设置有助于将符合条件的Commerce目录产品映射到Amazon列表的属性匹配，请更新“目录搜索”设置。
redirect_from: /sales-channels/asc/ob-catalog-search.html
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Amazon列表的目录搜索

_目录搜索_ 设置是商店列表设置的一部分。 列表设置可从以下位置访问： [存储仪表板](./amazon-store-dashboard.md).

这些设置使您能够设置有助于映射符合条件的属性的匹配 [!DNL Commerce] 产品与Amazon列表。 在映射后，Amazon会激活与定价、数量、覆盖以及订单和产品同步相关的操作。

定义这些映射值会增加完全匹配的可能性，从而最大限度地降低手动匹配产品清单的需求。 将属性添加为的一部分 [预设置任务](./amazon-pre-setup-tasks.md)，Amazon销售渠道具有更大的潜力，可以在新用户引导期间自动匹配您的产品，并在Amazon和之间同步产品数据 [!DNL Commerce].

如果您只创建Amazon ASIN属性（而不为每个产品添加ASIN值），则您可以 [!DNL Commerce] 产品可能不会自动匹配您的Amazon列表。 您可以 [手动分配](./creating-assigning-catalog-products.md) 您的产品。 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您手动匹配了产品，并且想要更新该产品的ASIN、UPC或其他数据元素，则必须在两个位置更新数据。 在您的 [!DNL Commerce] 目录和Amazon中的列表 [!DNL Amazon Seller Central] 帐户。

如果可用，最佳做法是映射这些属性和值。 完成此映射不是必需的，但有利于产品匹配，并且是Amazon与之间正确目录同步所必需的 [!DNL Commerce].

如果要添加属性，请参阅 [为Amazon匹配创建产品属性](./ob-creating-magento-attributes.md).

## 配置 [!UICONTROL Catalog Search] 设置

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Catalog Search]_部分。

1. 对象 **[!UICONTROL ASIN]**，选择您为Amazon ASIN值创建的产品属性。

   ASIN ([!DNL Amazon Standard Identification Number])是标识项目的十个字母和/或数字组成的唯一块。 对于图书，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到它们的目录时，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。

1. 对象 **[!UICONTROL EAN]**，选择您为Amazon EAN值创建的产品属性。

   欧洲文章编号(EAN)是一种条形码标准，由12位或13位产品标识代码组成。 每个EAN都唯一地标识产品、制造商及其属性；通常，EAN会打印在产品标签上或作为条形码的包装上。 Amazon需要EAN代码来提高搜索结果的质量和目录的质量。 您可以从制造商处获取EAN。

1. 对象 **[!UICONTROL GCID]**，选择您为Amazon GCIN值创建的产品属性。

   全局目录标识符(GCID)是没有UPC代码或ISBN的产品的ID。 Amazon Brand Registry允许您注册为品牌所有者并为产品创建唯一ID。

1. 对象 **[!UICONTROL ISBN]**，选择您为Amazon ISBN值创建的产品属性。

   国际标准书号(ISBN)是一种唯一的商业书籍标识符条形码。 每个ISBN代码唯一地标识一本书籍。 ISBN有10位或13位。 2007年1月1日之后分配的所有ISBN均为13位。

1. 对象 **[!UICONTROL UPC]**，选择您为Amazon UPC值创建的产品属性。

   通用产品代码(UPC)是一个12位的条形码，在美国广泛用于零售包装。

1. 对象 **[!UICONTROL General Search]**，选择要用于常规搜索匹配项的产品属性。

   此属性是您可以选择进行匹配的属性 [!DNL Commerce] 产品添加到相应的Amazon列表。 常规搜索使用目录中的关键词搜索。 因此，建议使用 [!DNL Commerce] 带有相关关键字（如产品SKU或产品名称）的属性。 常规搜索可能会返回许多可能的匹配项，在这种情况下，您可以从可能的匹配项中选择相应的Amazon列表。 此字段的一个常见选择是 `Product Name`.

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![目录搜索](assets/amazon-catalog-search.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的用于标识项目的唯一块。<br><br>ASIN表示 [!DNL Amazon Standard Identification Number]. ASIN是一个由10个字母和/或数字组成的唯一块，用于标识项目。 对于图书，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到它们的目录时，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL EAN (European Article Number)] | 12位或13位数的产品标识代码。 欧洲文章编号(EAN)是一种条形码标准，由12位或13位产品标识代码组成。 每个EAN都唯一地标识产品、制造商及其属性；通常，EAN会打印在产品标签上或作为条形码的包装上。 Amazon需要EAN代码来提高搜索结果的质量和目录的质量。 您可以从制造商处获取EAN。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | 全局目录标识符(GCID)是没有UPC代码或ISBN的产品的ID。 Amazon的Brand Registry允许您注册为品牌所有者，并为可能没有UPC或ISBN的产品创建唯一ID。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 10位或13位数的唯一商业书籍标识符条形码。 国际标准书号(ISBN)是一种唯一的商业书籍标识符条形码。 每个ISBN代码唯一地标识一本书籍。 ISBN有10位或13位。 2007年1月1日之后分配的所有ISBN均为13位。 |
| UPC （通用产品代码） | 12位数的条形码。 通用产品代码(UPC)是一个12位的条形码，在美国广泛用于零售包装。 |
| [!UICONTROL General Search] | 选择属性。 此属性是您可以选择进行匹配的属性 [!DNL Commerce] 产品添加到相应的Amazon列表。 常规搜索使用目录中的关键词搜索。 因此，建议使用 [!DNL Commerce] 带有相关关键字（如产品SKU或产品名称）的属性。 常规搜索可能会返回许多可能的匹配项，在这种情况下，您可以从可能的匹配项中选择相应的Amazon列表。 此字段的一个常见选择是 `Product Name`. |

**快速访问** - [!UICONTROL Listing Settings] 区域

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
