---
title: Amazon列表的履行者设置
description: 使用“履行者”设置确定如何履行（发运）Amazon清单中的订单。
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Amazon列表的履行者设置

_[!UICONTROL Fulfilled By]_设置是商店列表设置的一部分。 列表设置可从以下位置访问： [存储仪表板](./amazon-store-dashboard.md).

这些设置定义履行（或发运）订单的一方。 如果所有订单都通过一种方法完成，请在贸易商（您）或Amazon之间进行选择。 如果您计划完成您所在位置的订单并使用Amazon，则最佳实践是使用第三个选项并配置 [!DNL Commerce] 产品属性。

- **[!UICONTROL Fulfilled by Merchant]**  — 选择您作为商家是否履行所有订单。 下订单后，库存将从您的帐户中扣除 [!DNL Commerce] 目录。

- **[!UICONTROL Fulfilled by Amazon]**  — 选择Amazon是否履行所有订单。 使用此选项，产品库存不会从您的报表中扣除。 [!DNL Commerce] 目录。 Amazon已履行订单的库存库存存储并从其仓库中扣除。 在分配此选项之前，您必须验证 [!DNL Amazon Seller Central] 您的产品有资格使用的帐户 _由Amazon履行_ (FBA)履行。 FBA库存直接通过 [!DNL Amazon Seller Central] 帐户。 使用此履行方法，Amazon Sales Channel不会将数量更新共享到 [!DNL Commerce] 和Amazon。 因此，并非数量设置中所述的所有营销工具在Amazon sales channel中均可用。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 如果您的产品可能由您和Amazon履行，则可能需要创建 [!DNL Commerce] 具有“由商家履行”和“由Amazon履行”值的产品属性。 为每个产品设置此值表示谁履行了订单。

履行方法是一个区域属性，并且基于 **[!UICONTROL Amazon Marketplace Country]** 设置定义于 [存储集成](./store-integration.md). 进行更改后，该更改会影响共享该更改的所有Amazon列表 [!DNL Amazon Seller SKU] 在您的Amazon商店中销售相同地区的产品(如中定义的 _[!UICONTROL Amazon Marketplace Country]_期间 [存储集成](./store-integration.md))。 对共享的更改 [!DNL Amazon Seller SKU] 不会影响Amazon为其他区域设置的商店（在商店集成期间定义）。

>[!NOTE]
>
>当订单由Amazon (FBA)履行并且订单已导入时，您可以在订单详细信息中看到某些字段的虚数据。 参见 [Amazon订单详细信息](./amazon-order-details.md).

## 配置 [!UICONTROL Fulfilled By] 设置 {#configure-fulfilled-by-settings}

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Fulfilled By]_部分。

1. 对象 **[!UICONTROL Product Fulfilled By]**，选择履行（发运）订单的人员：

   - `Fulfilled by Merchant`  — 商家履行订单。

   - `Fulfilled by Amazon` - Amazon仓库履行订单。

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] 属性指明每个产品订单的履行人。

      如果已选择，请选择 [!DNL Commerce] 要映射的属性 **[!UICONTROL Fulfilled by Attribute]**.

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![履行者设置](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | 选项：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM)选择是否履行订单。 下订单后，库存将从您的帐户中扣除 [!DNL Commerce] 目录。 创建新产品时，将分配“已履行商家”的履行方法。</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA)选择Amazon是否履行订单。 使用此履行方法，产品库存不会从您的产品清单中扣除 [!DNL Commerce] 目录。 创建产品时，创建产品时使用了 _[!UICONTROL Fulfilled by Amazon (FBA)]_作为履行类型。 确保您的产品符合贵机构内满足FBA要求的条件 [!DNL Amazon Seller Central] 帐户。 FBA库存也直接通过 [!DNL Amazon Seller Central] 帐户。 使用此履行方法，不会推出相对于您的产品的数量更新 [!DNL Commerce] 目录，因此无法使用中介绍的某些营销工具 [库存/数量设置](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 选择您是否拥有 [!DNL Commerce] 确定它是由商家履行还是由Amazon履行的属性。 选择后， **[!UICONTROL Fulfilled by Attribute]** 启用。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | 选择 [!DNL Commerce] 用于确定履行方法的属性。<br><br>例如，如果属性为 _履行者_ 并且您选择属性值为 `Fulfilled By Merchant` 或 `Fulfilled By Amazon (FBA)`，系统将该值用作新产品的履行类型。 作为商家，您应该确保您的产品有资格在您的 [!DNL Amazon Seller Central] 帐户。 FBA库存也可通过您的Amazon卖方帐户直接管理。<br><br>选项取决于您为Amazon产品设置的属性。 |

**快速访问** - [!UICONTROL Listing Settings] 区域

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
