---
title: 目录搜索
description: 要设置属性匹配，以帮助将符合条件的商务目录产品与Amazon列表进行映射，请更新“目录搜索”设置。
redirect_from: /sales-channels/asc/ob-catalog-search.html
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# 目录搜索

_目录搜索_ 设置是商店列表设置的一部分。 列表设置可从 [存储仪表板](./amazon-store-dashboard.md).

这些设置允许您设置属性匹配，以帮助映射符合条件的 [!DNL Commerce] 产品。 映射后，Amazon将激活与定价、数量、改写以及订单和产品同步相关的活动。

定义这些映射值会增加进行精确匹配的可能性，从而最大限度地减少手动匹配产品清单的需要。 将属性添加为 [预设置任务](./amazon-pre-setup-tasks.md)，则Amazon销售渠道在Amazon和 [!DNL Commerce].

如果仅创建Amazon ASIN属性（不为每个产品添加ASIN值），则您的 [!DNL Commerce] 产品可能不会自动与您的Amazon列表匹配。 您可以 [手动分配](./creating-assigning-catalog-products.md) 您的产品。 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您手动匹配某个产品，并且想要更新该产品的ASIN、UPC或其他数据元素，则必须在两个位置更新数据。 在 [!DNL Commerce] 目录和Amazon列表中的 [!DNL Amazon Seller Central] 帐户。

最佳做法是映射这些属性和值（如果可用）。 无需完成此映射，但这有利于进行产品匹配，并且需要在Amazon和 [!DNL Commerce].

如果要添加属性，请参阅 [为Amazon匹配创建产品属性](./ob-creating-magento-attributes.md).

## 配置 [!UICONTROL Catalog Search] 设置

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Catalog Search]_中。

1. 对于 **[!UICONTROL ASIN]**，选择您为Amazon ASIN值创建的产品属性。

   一个信息([!DNL Amazon Standard Identification Number])是由十个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。

1. 对于 **[!UICONTROL EAN]**，选择您为Amazon EAN值创建的产品属性。

   欧洲文章编号(EAN)是条形码标准，是12位或13位产品标识代码。 每个EAN都唯一标识产品、制造商及其属性；通常，EAN将作为条形码打印在产品标签或包装上。 Amazon要求使用EAN代码来提高搜索结果质量和目录质量。 您可以从制造商处获取EAN。

1. 对于 **[!UICONTROL GCID]**，选择您为Amazon GCIN值创建的产品属性。

   全局目录标识符(GCID)是指没有UPC代码或ISBN的产品的ID。 Amazon的Brand Registry允许您注册为品牌所有者，并为产品创建唯一ID。

1. 对于 **[!UICONTROL ISBN]**，选择您为Amazon ISBN值创建的产品属性。

   国际标准书号(ISBN)是唯一的商业书籍标识码条形码。 每个ISBN代码都唯一地标识一本书。 ISBN有10位或13位。 2007年1月1日之后分配的所有ISBN都有13位数字。

1. 对于 **[!UICONTROL UPC]**，选择您为Amazon UPC值创建的产品属性。

   通用产品代码(UPC)是一个12位条形码，广泛用于美国的零售包装。

1. 对于 **[!UICONTROL General Search]**，请选择要用于常规搜索匹配的产品属性。

   此属性是您可以选择匹配的属性 [!DNL Commerce] 产品添加到相应的Amazon列表。 常规搜索使用目录中的关键词搜索。 因此，建议使用 [!DNL Commerce] 包含相关关键字（如产品SKU或产品名称）的属性。 常规搜索可能会返回许多可能的匹配项，在这种情况下，您可以从可能的匹配项中选择相应的Amazon列表。 此字段的常见选择是 `Product Name`.

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![目录搜索](assets/amazon-catalog-search.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一块，用于标识项目。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]. ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。 |
| [!UICONTROL EAN (European Article Number)] | 12位或13位产品标识码。 欧洲文章编号(EAN)是条形码标准，是12位或13位产品标识代码。 每个EAN都唯一标识产品、制造商及其属性；通常，EAN将作为条形码打印在产品标签或包装上。 Amazon要求使用EAN代码来提高搜索结果质量和目录质量。 您可以从制造商处获取EAN。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | 全局目录标识符(GCID)是指没有UPC代码或ISBN的产品的ID。 Amazon的品牌注册允许您注册为品牌所有者，并为可能没有UPC或ISBN的产品创建唯一ID。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 10位或13位唯一商业书籍标识符条形码。 国际标准书号(ISBN)是唯一的商业书籍标识码条形码。 每个ISBN代码都唯一地标识一本书。 ISBN有10位或13位。 2007年1月1日之后分配的所有ISBN都有13位数字。 |
| UPC（通用产品代码） | 12位的条形码。 通用产品代码(UPC)是一个12位条形码，广泛用于美国的零售包装。 |
| [!UICONTROL General Search] | 选择属性。 此属性是您可以选择匹配的属性 [!DNL Commerce] 产品添加到相应的Amazon列表。 常规搜索使用目录中的关键词搜索。 因此，建议使用 [!DNL Commerce] 包含相关关键字（如产品SKU或产品名称）的属性。 常规搜索可能会返回许多可能的匹配项，在这种情况下，您可以从可能的匹配项中选择相应的Amazon列表。 此字段的常见选择是 `Product Name`. |

**快速访问** - [!UICONTROL Listing Settings] 章节

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
