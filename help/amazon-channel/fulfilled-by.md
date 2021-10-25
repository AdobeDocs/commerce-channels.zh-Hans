---
title: 履行者
description: 使用“履行者”设置确定如何履行（发运）Amazon列表中的订单。
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# 履行者

_[!UICONTROL Fulfilled By]_设置是商店列表设置的一部分。 列表设置可从 [存储仪表板](./amazon-store-dashboard.md).

这些设置定义履行（或发运）订单的交易方。 如果您的所有订单都使用一种方法完成，请在商家（您）或Amazon之间进行选择。 如果您计划执行来自您所在地的订单并使用Amazon，则最好使用第三个选项并配置 [!DNL Commerce] 产品属性。

- **[!UICONTROL Fulfilled by Merchant]**  — 选择商户是否完成所有订单。 下订单后，库存将从 [!DNL Commerce] 目录。

- **[!UICONTROL Fulfilled by Amazon]**  — 选择Amazon是否履行所有订单。 使用此选项，不会从 [!DNL Commerce] 目录。 Amazon已履行订单的库存库存将存储并从其仓库中扣除。 在分配此选项之前，必须在 [!DNL Amazon Seller Central] 您的产品符合 _由Amazon履行_ (FBA)履约。 FBA库存通过 [!DNL Amazon Seller Central] 帐户。 使用此履行方法，Amazon销售渠道不会在两者之间共享数量更新 [!DNL Commerce] 和Amazon。 因此，并非所有数量设置中描述的营销工具都可在Amazon销售渠道中供您使用。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 如果您和Amazon可能履行了您的产品，则可能需要创建 [!DNL Commerce] 具有“由商家履行”和“由Amazon履行”值的产品属性。 为每个产品设置此值时，将指示谁履行了订单。

履行方法是区域属性，根据 **[!UICONTROL Amazon Marketplace Country]** 在 [存储集成](./store-integration.md). 进行更改后，该更改会影响所有共享该更改的Amazon列表 [!DNL Amazon Seller SKU] 在Amazon店中销售的 _[!UICONTROL Amazon Marketplace Country]_时段 [存储集成](./store-integration.md))。 对共享的 [!DNL Amazon Seller SKU] 在美国，不会影响为其他区域（在商店集成期间定义）设置的Amazon商店。

>[!NOTE]
>
>当订单由Amazon(FBA)履行并且订单已导入时，您可以在订单详细信息中看到某些字段的虚拟数据。 请参阅 [Amazon订单详细信息](./amazon-order-details.md).

## 配置 [!UICONTROL Fulfilled By] 设置 {#configure-fulfilled-by-settings}

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Fulfilled By]_中。

1. 对于 **[!UICONTROL Product Fulfilled By]**，选择完成（发运）顺序：

   - `Fulfilled by Merchant`  — 商人履行订单。

   - `Fulfilled by Amazon` -Amazon仓库履行订单。

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] 属性指示谁按产品完成了订单。

      如果已选择，请选择 [!DNL Commerce] 要映射的属性 **[!UICONTROL Fulfilled by Attribute]**.

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![履行者设置](assets/amazon-fulfilled-by.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | 选项：<ul><li>**[!UICONTROL Fulfilled by Merchant]** -(FBM)选择您是否履行了订单。 下订单后，库存将从 [!DNL Commerce] 目录。 创建新产品后，将分配“商户已履行”的履行方法。</li><li>**[!UICONTROL Fulfilled by Amazon]** -(FBA)选择Amazon是否履行订单。 使用此履行方法，不会从您的 [!DNL Commerce] 目录。 产品创建后，会使用 _[!UICONTROL Fulfilled by Amazon (FBA)]_作为履行类型。 确保您的产品符合在 [!DNL Amazon Seller Central] 帐户。 FBA库存也直接通过 [!DNL Amazon Seller Central] 帐户。 使用此履行方法时，数量更新不会相对于您的 [!DNL Commerce] 目录，因此您无法使用 [库存/数量设置](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 选择您是否拥有 [!DNL Commerce] 属性，用于确定商户是已履行还是Amazon已履行。 选择后， **[!UICONTROL Fulfilled by Attribute]** 启用。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | 选择 [!DNL Commerce] 用于确定履行方法的属性。<br><br>例如，如果属性为 _履行者_ 然后选择属性值作为 _[!UICONTROL Fulfilled By Merchant]_或_[!UICONTROL Fulfilled By Amazon (FBA)]_，则系统会将该值用作新产品的履行类型。 作为商家，您应确保您的产品符合FBA在 [!DNL Amazon Seller Central] 帐户。 FBA库存也直接通过您的Amazon卖家帐户管理。<br><br>选项取决于您为Amazon产品设置的属性。 |

**快速访问** - [!UICONTROL Listing Settings] 章节

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
