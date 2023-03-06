---
title: 库存/数量
description: 要控制Commerce商店中的产品数量详细信息同步到 [!DNL Amazon Seller Central] 帐户，更新“库存/数量”设置。
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 库存/数量

*[!UICONTROL Stock/Quantity]* 设置是商店列表设置的一部分。 列表设置可从以下位置访问： [存储仪表板](./amazon-store-dashboard.md).

这些设置用于同步产品数量详细信息 [!DNL Commerce] 店面数量与您的数量 [!DNL Amazon Seller Central] 帐户。 此工具功能强大，可以通过向买方显示紧迫性来用于其他广告，同时保持库存井然有序。 例如，某些商户的仓库中可能有150件特定SKU的库存，并希望确保Amazon购物者可以购买其所有库存。 其他商家可能希望一次只列出一个项目，给最终用户造成稀缺感。 在这种情况下，请将 *[!UICONTROL Maximum Listed Quantity]* 到 `1`.

数量是区域属性，基于 **[!UICONTROL Amazon Marketplace Country]** 设置定义期间 [存储集成](./store-integration.md). 当对产品的数量进行更改时，该更改会影响共享该产品的所有Amazon列表 [!DNL Amazon Seller SKU] 在同一个国家/地区销售的Amazon商店中。 对共享的更改 [!DNL Amazon Seller SKU] 不会影响您为其他国家/地区设置的Amazon商店。 您的第一个Amazon存储区已集成（具有最早的创建日期），可控制数量设置中的优先级。

>[!NOTE]
>
>对于Adobe Commerce和Magento Open Source 2.3.x用户，Amazon sales channel支持使用Inventory management扩展，而无需任何其他设置。 参见 [管理库存](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## 配置库存/数量设置 {#configure-stock--quantity-settings}

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 **[!UICONTROL Stock / Quantity]** 部分。

1. 对象 **[!UICONTROL Out-of-Stock Threshold]** （必需），输入产品最小数量的数值，以使产品符合其Amazon列表的条件。

   默认为 `0`. 如果您的 [!DNL Commerce] 产品库存低于此数量，则相应的Amazon列表不符合通过Amazon进行销售的资格。

1. 对象 **[!UICONTROL Maximum Listed Quantity]** （必需），为要在Amazon列表中显示的数量输入一个数值。

   此设置按输入的值列出所有符合条件的Amazon列表。 销售物料后，Amazon列表数量不会发生更改。 可用清单数量始终使用此值，即使实际产品数量更高或更低也是如此。 此设置通常在您不管理产品库存时使用。 例如，您可能有一个产品在 [!DNL Commerce] 目录。 设置为时 `10`时，Amazon列表始终显示可用数量 `10` 产品销售时不会更改。

1. 对象 **[!UICONTROL "Do Not Manage Stock" Quantity]** （必需），输入要为Amazon列表显示的数量值。

   Amazon要求您发布可用数量。 对象 [!DNL Commerce] 如果产品设置为不管理库存，但希望在Amazon上列出这些产品，则会发布此列表，并在此处输入可用数量。

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![库存/数量设置](assets/amazon-stock-quantity.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | 输入产品最小数量的数字值，以保持产品符合其Amazon列表的条件(默认值为 `0`)。<br><br>如果您的 [!DNL Commerce] 产品库存低于此数量，则相应的Amazon列表不符合通过Amazon进行销售的资格。 |
| [!UICONTROL Maximum Listed Quantity] | 输入要在Amazon列表中显示的数量的数值。<br><br>销售物料后，Amazon列表会重新发布并在此处输入数量。 此设置通常在您不管理产品库存时使用。<br><br>例如，您可以将“列出的最大数量”值输入为 `10`. 您的产品实际数量为 `80`. 因为您已将此值设置为 `10`时，Amazon列表始终显示可用数量 `10`. 可用数量始终随定义的值一起显示，即使库存数量较低也是如此。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | 输入Amazon清单的显示数量值。<br><br>Amazon要求您发布可用数量。 对象 [!DNL Commerce] 如果产品设置为不管理库存，但是您想要在Amazon上将其列出，则会发布该列表，其中包含此处输入的值的可用数量。 |

**快速访问** - [!UICONTROL Listing Settings] 区域

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## 示例：列出的最大数量

在销售某个物料后，Amazon列表会按此数量重新列出该物料。

例如，如果您设置 *[!UICONTROL Maximum Listed Quantity]* 作为 `12`，Amazon列表显示的数量为12，即使产品具有 [!DNL Commerce] 数量80：

![列出的最大数量示例1](assets/amazon-max-listed-quantity.png)

如果您设置了 *[!UICONTROL Maximum Listed Quantity]* 作为 `1`，则所有符合条件的产品都以一定数量列出 `1`. 售出物品后，系统会查找您的 [!DNL Commerce] 产品，如果存在其他库存，则在Amazon上重新提供该物料的数量 `1`.

此选项对于通常按1数量订购的产品可能很有价值。 此外，它也会增加购物者在查看Amazon列表时的紧迫感。

![列出的最大数量实例2](assets/amazon-max-listed-quantity-1.png)
