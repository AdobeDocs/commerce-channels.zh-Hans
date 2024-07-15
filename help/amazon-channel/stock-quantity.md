---
title: AmazonSales Channel- [!UICONTROL Stock/Quantity]
description: 要控制将产品数量详细信息从Commerce商店同步到 [!DNL Amazon Seller Central] 帐户，请更新库存/数量设置。
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

*[!UICONTROL Stock/Quantity]*&#x200B;设置是商店列表设置的一部分。 列表设置可从[存储仪表板](./amazon-store-dashboard.md)访问。

这些设置用于将产品数量详细信息从您的[!DNL Commerce]店面同步到[!DNL Amazon Seller Central]帐户上的数量。 此工具功能强大，可通过向买方显示紧迫性而用于其他广告，同时保持库存井然有序。 例如，一些商家可能在他们的仓库中存有150件特定SKU的商品，并且希望确保Amazon购物者可以购买其所有库存。 其他商家可能希望一次只列出一个项目，给最终用户造成稀缺感。 在这种情况下，将&#x200B;*[!UICONTROL Maximum Listed Quantity]*&#x200B;设置为`1`。

数量是区域属性，基于[存储集成](./store-integration.md)期间定义的&#x200B;**[!UICONTROL Amazon Marketplace Country]**&#x200B;设置。 当对产品的数量进行更改时，该更改会影响在同一个国家/地区销售的Amazon商店中共享该[!DNL Amazon Seller SKU]的所有Amazon列表。 对美国共享[!DNL Amazon Seller SKU]的更改不会影响您为其他国家/地区设置的Amazon商店。 您的第一个集成的Amazon存储（具有最早的创建日期）控制数量设置中的优先级。

>[!NOTE]
>
>对于Adobe Commerce和Magento Open Source 2.3.x用户，Amazon sales channel支持使用Inventory management扩展，而无需任何其他设置。 请参阅[管理库存](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}。

## 配置库存/数量设置 {#configure-stock--quantity-settings}

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;**[!UICONTROL Stock / Quantity]**&#x200B;部分。

1. 对于&#x200B;**[!UICONTROL Out-of-Stock Threshold]**（必需），请输入产品最低数量的数值，以保持产品符合其Amazon列表的条件。

   默认值为`0`。 如果您的[!DNL Commerce]产品库存低于此数值，则相应的Amazon列表没有资格通过Amazon进行销售。

1. 对于&#x200B;**[!UICONTROL Maximum Listed Quantity]**（必需），请输入要在Amazon列表中显示的数量的数值。

   此设置按输入的值列出所有符合条件的Amazon列表。 销售物料后，Amazon列表数量不会发生更改。 清单可用数量始终使用此值，即使实际产品数量高于或低于此值。 此设置通常在您不管理产品库存时使用。 例如，您的[!DNL Commerce]目录中可能有数量为80的产品。 将设置为`10`后，Amazon列表将始终显示可用数量`10`，并且在对产品进行销售时不会发生更改。

1. 对于&#x200B;**[!UICONTROL "Do Not Manage Stock" Quantity]**（必需），请输入要显示给Amazon清单的数量值。

   Amazon要求您发布可用数量。 对于设置为不管理库存但希望在Amazon上列出的[!DNL Commerce]产品，将发布此列表，并在此处输入可用数量。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![库存/数量设置](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | 输入产品最低数量的数字值，以保持产品符合其Amazon列表的条件（默认值为`0`）。<br><br>如果您的[!DNL Commerce]产品库存低于此数值，则相应的Amazon列表没有资格通过Amazon进行销售。 |
| [!UICONTROL Maximum Listed Quantity] | 输入要显示在Amazon列表中的数量的数值。<br><br>在销售物料时，Amazon列表将重新发布并在此处输入数量。 此设置通常在您不管理产品库存时使用。<br><br>例如，您输入“列出的最大数量”值为`10`。 您的产品实际数量为`80`。 由于您将此值设置为`10`，因此Amazon列表始终显示可用数量`10`。 可用数量始终随定义的值一起显示，即使库存数量较低也是如此。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | 输入Amazon清单的显示数量值。<br><br>Amazon要求您发布可用数量。 对于设置为不管理库存但希望在Amazon上列出它们的[!DNL Commerce]产品，将发布此列表，其中具有此处输入的值的可用数量。 |

**快速访问** - [!UICONTROL Listing Settings]分区

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

例如，如果将&#x200B;*[!UICONTROL Maximum Listed Quantity]*&#x200B;设置为`12`，则Amazon列表显示的数量为12，即使产品的[!DNL Commerce]数量为80也是如此：

![列出的最大数量示例1](assets/amazon-max-listed-quantity.png){width="300"}

如果您将&#x200B;*[!UICONTROL Maximum Listed Quantity]*&#x200B;设置为`1`，则将列出所有符合条件的产品，数量为`1`。 售出某个项目后，系统会查找您的[!DNL Commerce]产品，如果存在其他库存，则会在Amazon上将该项目的数量重新命名为`1`。

此选项对于通常按1量订购的产品可能很有价值。 此外，它也会增加购物者在查看Amazon列表时的紧迫性。

![列出的最大数量示例2](assets/amazon-max-listed-quantity-1.png){width="300"}
