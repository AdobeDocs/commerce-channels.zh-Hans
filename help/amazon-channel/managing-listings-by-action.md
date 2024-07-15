---
title: 按操作管理Amazon产品列表
description: 在管理Amazon列表时，可以将操作应用于单个或多个列表。
feature: Sales Channels, Products
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 按操作管理Amazon产品列表

_[!UICONTROL Product Listings]_页面包含多个选项卡，您可以从中查看所有列表的状态，并将您的产品与Amazon列表进行匹配。

每个选项卡上的可用列表任务略有不同，但[工作区控件](./workspace-controls.md)相同，允许您自定义为列表显示的数据。

**[!UICONTROL Actions]**&#x200B;下的选项可以将操作应用于多个列表，而&#x200B;_[!UICONTROL Action]_列中&#x200B;**[!UICONTROL Select]**下的选项仅将操作应用于单个列表。

另请参阅[按状态管理列表/选项卡](./managing-listings-by-tab.md)。

| 操作 | 描述 | 选项卡 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 用于通过匹配过程将不完整产品移回。 若要尝试重新匹配，必须修改[列表](./listing-settings.md)和[目录搜索](./catalog-search.md)设置以增加自动匹配的可能性。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 通过选择要匹配的列表、输入要匹配的ASIN或分配缺少的条件，手动将目录产品与Amazon列表匹配。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | 查看有关活动产品的其他信息，包括列表活动日志，该日志显示了对单个SKU/产品所做的更改。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | 使用随Amazon列表一起导入的信息创建[!DNL Commerce]目录产品。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 尝试自动匹配 | 根据搜索条件设置，尝试在[!DNL Commerce]目录与Amazon列表之间自动匹配。 若要尝试重新匹配，必须修改[列表](./listing-settings.md)和[目录搜索](./catalog-search.md)设置以增加自动匹配的可能性。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | 手动选择[!DNL Commerce]目录中的现有产品，并将其分配给Amazon列表。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | 使用随Amazon列表一起导入的信息创建[!DNL Commerce]目录产品。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （成批操作）用于重新列出已结束的列表，或手动列出符合列表规则资格但&#x200B;_[!UICONTROL Product Listing Actions]_未设置为`Automatically list new products`的产品。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （单个列表操作）用于重新列出已结束的列表。 此操作还用于在&#x200B;_[!UICONTROL Product Listing Actions]_未设置为`Automatically list new products`时手动列出符合列表规则资格的产品。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （成批活动）用于手动结束和删除Amazon上存在的产品的列表。 已结束的列表只要符合您的上市规则资格，就可以重新列出。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （成批活动）人工编辑现有的“改写”，以设置单个列表的价格、处理时间、条件和卖方附注文本，忽略其它列表默认值、设置和规则。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 手动创建一个“覆盖”，为单个列表设置价格、处理时间、条件和卖方备注文本，而忽略其他列表默认值、设置和规则。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | 如果与目录产品匹配的ASIN必须修改（例如：如果产品与错误列出的ASIN匹配），则使用。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 可以提供两种功能：<br><br>可用于在目录产品与两个Amazon列表之间创建一对二关系。 示例： Amazon的产品以不同的ASIN值列出。 您可以将一个目录产品与产品的两个ASIN列表相匹配。<br><br>可用于控制其他Amazon地区的列表。 示例：您有一个目录产品，该产品根据Amazon地区定义了不同的发运方法（美国地区为FBA，加拿大地区为FBM）。 要控制库存/数量，您可以创建别名销售商SKU，然后使用不同的销售商SKU在该区域中重新列出相同的产品。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 用于修改与产品关联的履行方法(由Amazon履行：FBA或由商家履行：FBM)。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （单个列表操作）用于手动结束和删除Amazon上存在的产品的列表。 已结束的列表只要符合您的上市规则资格，就可以重新列出。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （单个列表操作）手动编辑现有的“覆盖”，该覆盖为单个列表设置价格、处理时间、条件和卖方备注文本，而忽略其他列表默认值、设置和规则。 | [[!UICONTROL Overrides]](./overrides.md) |

## 访问产品列表

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**营销** > _渠道_ > **AmazonSales Channel**。

1. 单击商店卡上的&#x200B;**查看商店**。

1. 在商店信息板上，单击&#x200B;_商店列表_&#x200B;部分中的&#x200B;**管理列表**。
