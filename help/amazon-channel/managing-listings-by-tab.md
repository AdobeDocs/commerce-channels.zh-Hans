---
title: 按状态/选项卡管理Amazon产品列表
description: 在管理Amazon列表时，可以根据状态对列表应用操作。
feature: Sales Channels, Products
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# 按状态/选项卡管理Amazon产品列表

_[!UICONTROL Product Listings]_页面包含多个选项卡，您可以从中查看所有列表的状态，并将您的产品与Amazon列表进行匹配。

每个选项卡上的可用列表任务略有不同，但[工作区控件](./workspace-controls.md)相同，允许您自定义为列表显示的数据。

**[!UICONTROL Actions]**&#x200B;下的选项可以将操作应用于多个列表，而&#x200B;_[!UICONTROL Action]_列中&#x200B;**[!UICONTROL Select]**下的选项仅将操作应用于单个列表。

另请参阅[按操作管理列表](./managing-listings-by-action.md)。

![产品列表选项卡](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| 选项卡 | 描述 | 操作 |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | 显示您的[!DNL Commerce]目录产品，这些产品符合您定义的列表设置，但缺少Amazon列出产品所需的信息。<br><br>如果在您的[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)设置中将&#x200B;_[!UICONTROL Automatic List Action]_设置为`Automatically List Eligible Products`，则这些项目是您的&#x200B;**[!UICONTROL In Progress Listings]**。 | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | 显示与[!DNL Commerce]目录中的产品不匹配的现有Amazon列表(基于从Amazon收到的信息)。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>尝试自动匹配<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | 显示已准备好创建Amazon清单的目录产品，但您的应用商店设置为不自动发布新清单。 此选项卡用于手动发布新列表。<br><br>如果在您的[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)设置中将&#x200B;_[!UICONTROL Automatic List Action]_设置为`Do Not Automatically List Eligible Products`，则这些项目是您的&#x200B;**[!UICONTROL In Progress Listings]**。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | 显示已发布到Amazon的目录产品，但Amazon尚未批准其列为“活动”状态。 | Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到由Amazon/商家履行的[结束列表<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | 显示与您的[!DNL Commerce]目录中的产品匹配、已发布到Amazon并且已被Amazon置于活动状态的Amazon列表。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到Amazon/商家已履行的工作<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 显示符合已定义覆盖的条件并已应用覆盖的Amazon列表。 覆盖优先于任何其他帐户设置。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | 根据您定义的[列表设置](./listing-settings.md)，显示不再符合条件的现有Amazon列表。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>切换到Amazon/商家已履行的工作<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | 显示已从Amazon手动结束（删除）的Amazon列表。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 访问产品列表

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击商店信息卡上的&#x200B;**[!UICONTROL View Store]**。

1. 在商店仪表板上，单击&#x200B;_[!UICONTROL Store Listings]_部分中的&#x200B;**[!UICONTROL Manage Listings]**。
