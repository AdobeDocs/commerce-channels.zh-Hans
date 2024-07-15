---
title: Amazon列表的履行者设置
description: 使用“履行者”设置来确定如何履行（发运）Amazon列表中的订单。
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Amazon列表的履行者设置

_[!UICONTROL Fulfilled By]_设置是商店列表设置的一部分。 列表设置可从[存储仪表板](./amazon-store-dashboard.md)访问。

这些设置定义履行（或发货）订单的一方。 如果所有订单都通过一种方法完成，请在贸易商（您）或Amazon之间选择。 如果您计划完成您所在位置的订单并使用Amazon，则最佳实践是使用第三个选项并配置[!DNL Commerce]产品属性。

- **[!UICONTROL Fulfilled by Merchant]** — 选择您是否作为商家完成所有订单。 下达订单后，库存将从您的[!DNL Commerce]目录中扣除。

- **[!UICONTROL Fulfilled by Amazon]** — 选择Amazon是否履行所有订单。 使用此选项，在下达订单时不会从[!DNL Commerce]目录中扣除产品库存。 Amazon已履行订单的库存库存存储并从其仓库中扣除。 在分配此选项之前，您必须在[!DNL Amazon Seller Central]帐户中验证您的产品是否符合&#x200B;_由Amazon履行_ (FBA)履行的条件。 FBA清单直接通过您的[!DNL Amazon Seller Central]帐户进行管理。 使用此履行方法，Amazon销售渠道不会在[!DNL Commerce]和Amazon之间共享数量更新。 因此，您在Amazon Sales Channel中并非可以使用“数量设置”中描述的所有营销工具。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** — 如果您的产品可能由您和Amazon履行，则可能需要创建一个[!DNL Commerce]产品属性，其值为“由商家履行”和“由Amazon履行”。 为每个产品设置此值表示谁将履行订单。

履行方法是区域属性，基于[存储集成](./store-integration.md)期间定义的&#x200B;**[!UICONTROL Amazon Marketplace Country]**&#x200B;设置。 进行更改后，该更改会影响在您的Amazon商店中共享了[!DNL Amazon Seller SKU]的所有Amazon列表，这些列表在同一地区销售（在[商店集成](./store-integration.md)期间的&#x200B;_[!UICONTROL Amazon Marketplace Country]_中定义）。 对美国共享[!DNL Amazon Seller SKU]的更改不会影响您为其他区域（如存储集成期间所定义）设置的Amazon存储。

>[!NOTE]
>
>当订单由Amazon (FBA)履行并且订单已导入时，您可以在订单详细信息中看到某些字段的虚数据。 查看[Amazon订单详细信息](./amazon-order-details.md)。

## 配置[!UICONTROL Fulfilled By]设置 {#configure-fulfilled-by-settings}

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Fulfilled By]_部分。

1. 对于&#x200B;**[!UICONTROL Product Fulfilled By]**，请选择履行（发货）订单的人员：

   - `Fulfilled by Merchant` — 商家履行订单。

   - `Fulfilled by Amazon` - Amazon仓库履行订单。

   - `Assign Fulfilled By Using Magento Product Attribute` - [!DNL Commerce]属性指示每个产品订单的履行者。

     如果已选择，请选择要在&#x200B;**[!UICONTROL Fulfilled by Attribute]**&#x200B;中映射的[!DNL Commerce]属性。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![完成者设置](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| 字段 | 描述 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | 选项：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM)选择是否履行订单。 下达订单后，库存将从您的[!DNL Commerce]目录中扣除。 创建新产品时，将分配“已履行商家”的履行方法。</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA)选择Amazon是否履行订单。 使用此履行方法，在下达订单时不会从[!DNL Commerce]目录中扣除产品库存。 创建产品后，将使用&#x200B;_[!UICONTROL Fulfilled by Amazon (FBA)]_作为履行类型来创建该产品。 确保您的产品符合[!DNL Amazon Seller Central]帐户中的FBA履行条件。 FBA清单也通过您的[!DNL Amazon Seller Central]帐户直接管理。 使用此履行方法，不会推出相对于您的[!DNL Commerce]目录的数量更新，因此您无法使用[库存/数量设置](./stock-quantity.md)中介绍的某些营销工具。</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** — 选择您是否具有现有的[!DNL Commerce]特性以确定它是商户履行的特性还是由Amazon履行的特性。 选择后，**[!UICONTROL Fulfilled by Attribute]**&#x200B;将启用。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | 选择用于确定履行方法的[!DNL Commerce]属性。<br><br>例如，如果属性为&#x200B;_履行者_，而您选择属性值为`Fulfilled By Merchant`或`Fulfilled By Amazon (FBA)`，则系统将该值用作新产品的履行类型。 作为商人，您应确保您的产品符合[!DNL Amazon Seller Central]帐户中的FBA履行资格。 FBA库存也通过您的Amazon卖方帐户直接管理。<br><br>选项取决于您为Amazon产品设置的属性。 |

**快速访问** - [!UICONTROL Listing Settings]分区

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
