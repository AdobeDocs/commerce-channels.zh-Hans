---
title: 库存/数量
description: 要控制将产品数量详细信息从您的商务商店同步到您的 [!DNL Amazon Seller Central] 帐户，请更新“库存/数量”设置。
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# 库存/数量

*[!UICONTROL Stock/Quantity]* 设置是商店列表设置的一部分。可从[存储功能板](./amazon-store-dashboard.md)访问列表设置。

这些设置用于将产品数量详细信息从[!DNL Commerce]店面同步到[!DNL Amazon Seller Central]帐户上的数量。 此工具功能强大，可通过向购买者显示紧急情况并保持库存有序来用于其他广告。 例如，某些商户的仓库中可能有150个特定SKU的物料，并且希望确保Amazon购物者可以购买其所有库存。 其他商家可能希望一次只列出一个项目，以给最终用户造成稀缺感。 在这种情况下，将&#x200B;*[!UICONTROL Maximum Listed Quantity]*&#x200B;设置为`1`。

数量是区域属性，它基于在[存储集成](./store-integration.md)期间定义的&#x200B;**[!UICONTROL Amazon Marketplace Country]**&#x200B;设置。 当对产品数量进行更改时，该更改会影响在您的Amazon商店中共享该[!DNL Amazon Seller SKU]的所有在同一国家/地区销售的Amazon列表。 对美国共享的[!DNL Amazon Seller SKU]所做的更改不会影响您为其他国家/地区设置的Amazon商店。 集成的第一个Amazon商店（具有最早的创建日期）控制着数量设置中的优先级。

>[!NOTE]
>
>对于Adobe商务和Magento Open Source2.3.x用户，Amazon销售渠道支持使用库存管理扩展，而无需进行任何其他设置。 请参阅[管理清单](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){:target=&quot;_blank&quot;}。

## 配置库存/数量设置 {#configure-stock--quantity-settings}

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;**[!UICONTROL Stock / Quantity]**&#x200B;部分。

1. 对于&#x200B;**[!UICONTROL Out-of-Stock Threshold]**（必需），输入产品最低数量的数值，以使产品符合Amazon列表的条件。

   默认值为`0`。 如果您的[!DNL Commerce]产品库存低于此数量，则相应的Amazon列表不符合通过Amazon进行销售的条件。

1. 对于&#x200B;**[!UICONTROL Maximum Listed Quantity]**（必需），输入要在Amazon列表中显示的数量的数值。

   此设置会以输入的值列出您符合条件的Amazon列表。 销售物料后，Amazon列表数量不会更改。 即使实际产品数量较高或较低，可用的列表数量也始终使用此值。 当您不管理产品库存时，通常会使用此设置。 例如，您的[!DNL Commerce]目录中可能有一个数量为80的产品。 将设置为`10`时，Amazon列表始终显示`10`的可用数量，并且在产品进行销售时不会发生更改。

1. 对于&#x200B;**[!UICONTROL "Do Not Manage Stock" Quantity]**（必需），输入要为Amazon列表显示的数量值。

   Amazon要求您发布可用数量。 对于设置为不管理库存但希望将其列在Amazon上的[!DNL Commerce]产品，将发布该列表，并在此处输入可用数量。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![库存/数量设置](assets/amazon-stock-quantity.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | 输入产品最低数量的数值，以使产品符合Amazon列表的条件（默认值为`0`）。<br><br>如果您的 [!DNL Commerce] 产品库存低于此数量，则相应的Amazon列表不符合通过Amazon进行销售的条件。 |
| [!UICONTROL Maximum Listed Quantity] | 输入要在Amazon列表中显示的数量的数值。<br><br>当物料售出时，Amazon列表会重新发布并包含此处输入的数量。当您不管理产品库存时，通常会使用此设置。<br><br>例如，您输入“列出的最大数量”值 `10`。产品的实际数量为`80`。 由于您已将此值设置为`10`，因此Amazon列表始终显示可用数量`10`。 即使库存数量较低，可用数量也始终随定义的值一起显示。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | 为Amazon列表的显示数量输入一个值。<br><br>Amazon要求您发布可用数量。对于设置为不管理库存但希望将其列在Amazon上的[!DNL Commerce]产品，将发布该列表，其中包含此处输入值的可用数量。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## 示例：最大列出数量

当物料售出时，Amazon列表会按此数量重新确定物料。

例如，如果将&#x200B;*[!UICONTROL Maximum Listed Quantity]*&#x200B;设置为`12`，则Amazon列表显示的数量为12，即使产品的数量为[!DNL Commerce] 80:

![最大列出数量实例1](assets/amazon-max-listed-quantity.png)

如果将&#x200B;*[!UICONTROL Maximum Listed Quantity]*&#x200B;设置为`1`，则所有符合条件的产品都将列出数量为`1`的产品。 在销售某个物料后，系统会查看您的[!DNL Commerce]产品，如果存在额外库存，则在Amazon上重新列出数量为`1`的物料。

此选项对于通常订购量为1的产品可能很有价值。 此外，在查看Amazon列表时，这也会增加购物者的紧急程度。

![最大列出数量示例2](assets/amazon-max-listed-quantity-1.png)
