---
title: 按状态/选项卡管理产品列表
description: 在管理Amazon列表时，您可以根据状态对列表应用操作。
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 按状态/选项卡管理产品列表

_[!UICONTROL Product Listings]_页面包含多个选项卡，您可以从中查看所有列表的状态，并将产品与Amazon列表进行匹配。

每个选项卡上可用的列表任务略有不同，但[工作区控件](./workspace-controls.md)是相同的，允许您自定义为列表显示的数据。

**[!UICONTROL Actions]**&#x200B;下的选项可以将该操作应用于多个列表，而&#x200B;_[!UICONTROL Action]_列中&#x200B;**[!UICONTROL Select]**下的选项则只能将该操作应用于单个列表。

另请参阅[按操作管理列表](./managing-listings-by-action.md)。

![“产品列表”选项卡](assets/amazon-product-listings-tabs.png)

| 选项卡 | 描述 | 操作 |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | 显示符合您定义的列表设置但缺少Amazon列表所需信息的[!DNL Commerce]目录产品。<br><br>如果 _[!UICONTROL Automatic List Action]_在您的设 `Automatically List Eligible Products` 置中 [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 设置为，则这些项目是您的&#x200B;**[!UICONTROL In Progress Listings]**项目。 | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | 显示与[!DNL Commerce]目录中的产品不匹配的现有Amazon列表(基于从Amazon收到的信息)。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>尝试自动匹配<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | 显示已准备好创建Amazon列表的目录产品，但您的商店未设置为自动发布新列表。 此选项卡用于手动发布新列表。<br><br>如果 _[!UICONTROL Automatic List Action]_在您的设 `Do Not Automatically List Eligible Products` 置中 [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 设置为，则这些项目是您的&#x200B;**[!UICONTROL In Progress Listings]**项目。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | 显示已发布到Amazon但Amazon尚未批准将列为“活动”状态的目录产品。 | [ AmazonSwitch上的EndListing(s)](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>到由Amazon/Merchant履行<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | 显示与[!DNL Commerce]目录中的某个产品相匹配的Amazon列表，这些列表已发布到Amazon，且由Amazon处于“活动”状态。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到由Amazon/Merchant履行<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 显示符合已定义覆盖条件且已应用覆盖的Amazon列表。 优先于任何其他帐户设置。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | 根据您定义的[列表设置](./listing-settings.md)，显示不再符合条件的现有Amazon列表。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到由Amazon/Merchant履行<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | 显示已手动从Amazon中结束（删除）的Amazon列表。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 访问产品列表

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击存储卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在存储仪表板上，单击&#x200B;_[!UICONTROL Store Listings]_部分中的&#x200B;**[!UICONTROL Manage Listings]**。
