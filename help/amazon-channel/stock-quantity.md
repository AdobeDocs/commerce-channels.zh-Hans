---
title: AmazonSales Channel- [!UICONTROL Stock/Quantity]
description: 要控制Commerce商店中的产品数量详细信息同步到 [!DNL Amazon Seller Central] 帐户，更新库存/数量设置。
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

*[!UICONTROL Stock/Quantity]* 设置是商店列表设置的一部分。 列表设置可从以下位置访问： [存储仪表板](./amazon-store-dashboard.md).

这些设置用于同步您网站上的 [!DNL Commerce] 店面数量与您的数量 [!DNL Amazon Seller Central] 帐户。 此工具功能强大，可通过向买方显示紧迫性而用于其他广告，同时保持库存井然有序。 例如，一些商家可能在他们的仓库中存有150件特定SKU的商品，并且希望确保Amazon购物者可以购买其所有库存。 其他商家可能希望一次只列出一个项目，给最终用户造成稀缺感。 在这种情况下，请将 *[!UICONTROL Maximum Listed Quantity]* 到 `1`.

数量是一个区域属性，它基于 **[!UICONTROL Amazon Marketplace Country]** 设置定义期间 [存储集成](./store-integration.md). 当对产品的数量进行更改时，该更改会影响共享该产品的所有Amazon列表 [!DNL Amazon Seller SKU] 在同一个国家/地区销售的Amazon商店中。 对共享的更改 [!DNL Amazon Seller SKU] 不会影响您为其他国家/地区设置的Amazon商店。 您的第一个集成的Amazon存储（具有最早的创建日期）控制数量设置中的优先级。

>[!NOTE]
>
>对于Adobe Commerce和Magento Open Source 2.3.x用户，Amazon sales channel支持使用Inventory management扩展，而无需任何其他设置。 请参阅 [管理库存](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## 配置库存/数量设置 {#configure-stock--quantity-settings}

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 **[!UICONTROL Stock / Quantity]** 部分。

1. 对象 **[!UICONTROL Out-of-Stock Threshold]** （必需），为产品的最低数量输入一个数值，以保持产品符合其Amazon列表的条件。

   默认为 `0`. 如果您的 [!DNL Commerce] 产品库存低于此数量，则相应的Amazon列表没有资格通过Amazon进行销售。

1. 对象 **[!UICONTROL Maximum Listed Quantity]** （必需），为要在Amazon列表中显示的数量输入一个数值。

   此设置按输入的值列出所有符合条件的Amazon列表。 销售物料后，Amazon列表数量不会发生更改。 清单可用数量始终使用此值，即使实际产品数量高于或低于此值。 此设置通常在您不管理产品库存时使用。 例如，您的网站中可能有一个数量为80的产品， [!DNL Commerce] 目录。 设置为时 `10`，则Amazon列表始终显示可用数量 `10` 产品销售时不会改变。

1. 对象 **[!UICONTROL "Do Not Manage Stock" Quantity]** （必需），输入要为Amazon列表显示的数量值。

   Amazon要求您发布可用数量。 对象 [!DNL Commerce] 如果产品设置为不管理库存，但希望在Amazon上列出这些产品，则会发布此列表，并在此处输入可用数量。

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![库存/数量设置](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | 输入产品最低数量的数字值，以保持产品符合其Amazon列表的条件(默认值为 `0`)。<br><br>如果您的 [!DNL Commerce] 产品库存低于此数量，则相应的Amazon列表没有资格通过Amazon进行销售。 |
| [!UICONTROL Maximum Listed Quantity] | 输入要显示在Amazon列表中的数量的数值。<br><br>销售物料后，Amazon列表会重新发布并在此处输入数量。 此设置通常在您不管理产品库存时使用。<br><br>例如，您可以将“列出的最大数量”值输入为 `10`. 您的产品实际数量为 `80`. 因为您已将此值设置为 `10`，则Amazon列表始终显示可用数量 `10`. 可用数量始终随定义的值一起显示，即使库存数量较低也是如此。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | 输入Amazon清单的显示数量值。<br><br>Amazon要求您发布可用数量。 对象 [!DNL Commerce] 如果产品设置为不管理库存，但希望在Amazon上列出这些产品，则会发布列表，并在此处输入值的可用数量。 |

**快速访问** - [!UICONTROL Listing Settings] 部分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## 示例：列出的最大数量

在销售某个项目时，Amazon列表会按此数量重新列出该项目。

例如，如果您设置 *[!UICONTROL Maximum Listed Quantity]* 作为 `12`，Amazon列表显示数量为12，即使产品具有 [!DNL Commerce] 数量80：

![列出的最大数量示例1](assets/amazon-max-listed-quantity.png){width="300"}

如果您设置 *[!UICONTROL Maximum Listed Quantity]* 作为 `1`，列出了所有符合条件的产品以及 `1`. 售出物品后，系统会查找您的 [!DNL Commerce] 此外，如果存在其他库存，则在Amazon上重新提供该物料的数量 `1`.

此选项对于通常按1量订购的产品可能很有价值。 此外，它也会增加购物者在查看Amazon列表时的紧迫性。

![列出的最大数量示例2](assets/amazon-max-listed-quantity-1.png){width="300"}
