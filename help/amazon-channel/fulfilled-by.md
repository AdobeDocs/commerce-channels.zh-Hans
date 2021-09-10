---
title: 履行者
description: 使用“履行者”设置确定如何履行（发运）Amazon列表中的订单。
redirect_from: /sales-channels/asc/ob-fulfilled-by.html: 
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 618
ht-degree: 0%

---

# 履行者

_[!UICONTROL Fulfilled By]_设置是商店列表设置的一部分。可从[存储功能板](./amazon-store-dashboard.md)访问列表设置。

这些设置定义履行（或发运）订单的交易方。 如果您的所有订单都使用一种方法完成，请在商家（您）或Amazon之间进行选择。 如果您计划执行来自您所在地的订单并使用Amazon，则最好使用第三个选项并配置[!DNL Commerce]产品属性。

- **[!UICONTROL Fulfilled by Merchant]**  — 选择商户是否完成所有订单。下订单后，库存将从[!DNL Commerce]目录中扣除。

- **[!UICONTROL Fulfilled by Amazon]**  — 选择Amazon是否履行所有订单。使用此选项，下单后不会从[!DNL Commerce]目录中扣除产品库存。 Amazon已履行订单的库存库存将存储并从其仓库中扣除。 在分配此选项之前，您必须在[!DNL Amazon Seller Central]帐户中验证您的产品是否符合&#x200B;_由Amazon_(FBA)履行的条件。 FBA库存通过[!DNL Amazon Seller Central]帐户直接管理。 使用此履行方法，Amazon销售渠道不会在[!DNL Commerce]和Amazon之间共享数量更新。 因此，并非所有数量设置中描述的营销工具都可在Amazon销售渠道中供您使用。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 如果您和Amazon可能履行了您的产品，您可能希望创建一个产品属性，其 [!DNL Commerce] 中的值为“由商家履行”和“由Amazon履行”。为每个产品设置此值时，将指示谁履行了订单。

实现方法是区域属性，它基于在[存储集成](./store-integration.md)期间定义的&#x200B;**[!UICONTROL Amazon Marketplace Country]**&#x200B;设置。 进行更改后，该更改会影响在您的Amazon商店中共享该[!DNL Amazon Seller SKU]的所有Amazon列表，这些列表在同一区域销售（在[商店集成](./store-integration.md)期间定义）。 _[!UICONTROL Amazon Marketplace Country]_对美国共享的[!DNL Amazon Seller SKU]所做的更改不会影响为其他区域（在存储集成期间定义）设置的Amazon存储。

>[!NOTE]
>
>当订单由Amazon(FBA)履行并且订单已导入时，您可以在订单详细信息中看到某些字段的虚拟数据。 请参阅[Amazon订单详细信息](./amazon-order-details.md)。

## 配置[!UICONTROL Fulfilled By]设置 {#configure-fulfilled-by-settings}

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Fulfilled By]_部分。

1. 对于&#x200B;**[!UICONTROL Product Fulfilled By]**，选择完成（发运）订单的人：

   - `Fulfilled by Merchant`  — 商人履行订单。

   - `Fulfilled by Amazon` -Amazon仓库履行订单。

   - `Assign Fulfilled By Using Magento Product Attribute`  — 属性指 [!DNL Commerce] 示谁在每件产品中履行了订单。

      如果已选择，请选择要在&#x200B;**[!UICONTROL Fulfilled by Attribute]**&#x200B;中映射的[!DNL Commerce]属性。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![履行者设置](assets/amazon-fulfilled-by.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | 选项：<ul><li>**[!UICONTROL Fulfilled by Merchant]** -(FBM)选择您是否履行了订单。下订单后，库存将从[!DNL Commerce]目录中扣除。 创建新产品后，将分配“商户已履行”的履行方法。</li><li>**[!UICONTROL Fulfilled by Amazon]** -(FBA)选择Amazon是否履行订单。使用此履行方法，在下订单时，产品库存不会从[!DNL Commerce]目录中扣除。 创建产品后，将创建该产品，并将&#x200B;_[!UICONTROL Fulfilled by Amazon (FBA)]_作为履行类型。 确保您的产品符合[!DNL Amazon Seller Central]帐户内FBA履行的条件。 FBA库存也通过[!DNL Amazon Seller Central]帐户直接管理。 使用此履行方法时，数量更新不会相对于您的[!DNL Commerce]目录推送出去，因此您无法使用[库存/数量设置](./stock-quantity.md)中描述的某些营销工具。</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 选择您的现有属性是 [!DNL Commerce] 否确定商家履行了该属性，还是Amazon履行了该属性。选择&#x200B;**[!UICONTROL Fulfilled by Attribute]**&#x200B;后，将启用。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | 选择用于确定履行方法的[!DNL Commerce]属性。<br><br>例如，如果属性为“履 _行_ 者”，并且您选择属性值 _[!UICONTROL Fulfilled By Merchant]_作为或_[!UICONTROL Fulfilled By Amazon (FBA)]_，则系统会将该值用作新产品的履行类型。作为商家，您应确保您的产品符合[!DNL Amazon Seller Central]帐户内FBA履行条件。 FBA库存也直接通过您的Amazon卖家帐户管理。<br><br>选项取决于您为Amazon产品设置的属性。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
