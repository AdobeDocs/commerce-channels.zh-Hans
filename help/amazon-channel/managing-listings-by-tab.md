---
title: 按状态/选项卡管理产品列表
description: 在管理Amazon列表时，您可以根据状态对列表应用操作。
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 按状态/选项卡管理产品列表

此 _[!UICONTROL Product Listings]_页面包含多个选项卡，您可以从中查看所有列表的状态，并将产品与Amazon列表进行匹配。

每个选项卡上的可用列表任务略有不同，但 [工作区控件](./workspace-controls.md) 相同，并允许您自定义为列表显示的数据。

下的选项 **[!UICONTROL Actions]** 可以将操作应用于多个列表，而下面的选项可以 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列仅将该操作应用于单个列表。

另请参阅 [按操作管理列表](./managing-listings-by-action.md).

![产品列表选项卡](assets/amazon-product-listings-tabs.png)

| 选项卡 | 描述 | 操作 |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | 显示您的 [!DNL Commerce] 目录产品符合您定义的列表设置，但缺少Amazon列表所需的信息。<br><br>如果 _[!UICONTROL Automatic List Action]_设置为 `Automatically List Eligible Products` 在您的 [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 设置，这些项目是您的&#x200B;**[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | 显示与您的产品不匹配的现有Amazon列表(基于从Amazon收到的信息) [!DNL Commerce] 目录。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>尝试自动匹配<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | 显示已准备好创建Amazon清单的目录产品，但您的应用商店未设置为自动发布新清单。 此选项卡用于手动发布新列表。<br><br>如果 _[!UICONTROL Automatic List Action]_设置为 `Do Not Automatically List Eligible Products` 在您的 [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 设置，这些项目是您的&#x200B;**[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | 显示已发布到Amazon的目录产品，但Amazon尚未批准其状态为活动的列表。 | [结束 在Amazon上列出](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到“由Amazon/商家履行”<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | 显示与您的产品匹配的Amazon列表 [!DNL Commerce] 目录，已发布到Amazon，并由Amazon标记为活动状态。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到“由Amazon/商家履行”<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 显示满足所定义覆盖标准并已应用覆盖的Amazon列表。 覆盖优先于任何其他帐户设置。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | 根据您定义的内容，显示不再符合条件的现有Amazon列表 [列表设置](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到“由Amazon/商家履行”<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | 显示您已从Amazon手动结束（删除）的Amazon列表。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 访问产品列表

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. 单击 **[!UICONTROL View Store]** 在商店卡上。

1. 在商店功能板上，单击 **[!UICONTROL Manage Listings]** 在 _[!UICONTROL Store Listings]_部分。
