---
title: 按操作管理Amazon产品列表
description: 在管理Amazon列表时，您可以将操作应用于单个或多个列表。
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# 按操作管理Amazon产品列表

此 _[!UICONTROL Product Listings]_页面包含多个选项卡，您可以从中查看所有列表的状态，并将产品与Amazon列表进行匹配。

每个选项卡上的可用列表任务略有不同，但 [工作区控件](./workspace-controls.md) 相同，并允许您自定义为列表显示的数据。

下的选项 **[!UICONTROL Actions]** 可以将操作应用于多个列表，而下面的选项可以 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列仅将该操作应用于单个列表。

另请参阅 [按状态管理列表/选项卡](./managing-listings-by-tab.md).

| 操作 | 描述 | 选项卡 |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 用于通过匹配过程将不完整产品移回。 要尝试重新匹配，您必须修改 [列表](./listing-settings.md) 和 [目录搜索](./catalog-search.md) 设置，以增加自动匹配的可能性。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 通过选择要匹配的列表、输入要匹配的ASIN或分配缺少的条件，手动将目录产品与Amazon列表匹配。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | 查看有关活动产品的其他信息，包括列表活动日志，该日志显示了对单个SKU/产品所做的更改。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | 创建 [!DNL Commerce] 使用随Amazon列表导入的信息对产品进行编目。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 尝试自动匹配 | 尝试自动匹配 [!DNL Commerce] 目录和您的Amazon列表。 要尝试重新匹配，您必须修改 [列表](./listing-settings.md) 和 [目录搜索](./catalog-search.md) 设置，以增加自动匹配的可能性。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | 手动选择中的现有产品 [!DNL Commerce] 并将其分配给Amazon列表。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | 创建 [!DNL Commerce] 使用随Amazon列表导入的信息对产品进行编目。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （成批活动）用于重新列出已结束的列表，或人工列出符合列表规则条件，但符合您指定的合格产品。 _[!UICONTROL Product Listing Actions]_未设置为 `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （单个列表操作）用于重新列出已结束的列表。 在以下情况下，此操作还用于手动列出符合列表规则资格的产品 _[!UICONTROL Product Listing Actions]_未设置为 `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （成批活动）用于手动结束和删除Amazon上存在的产品的列表。 只要结束的列表符合您的上市规则资格，就可以将其重新列出。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （成批活动）人工编辑现有的“改写”，以便为单个列表设置价格、处理时间、条件和卖方附注文本，而忽略其它列表默认值、设置和规则。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 手动创建“覆盖”，为单个列表设置价格、处理时间、条件和卖方备注文本，而忽略其他列表默认值、设置和规则。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | 如果与目录产品匹配的ASIN必须修改（例如：如果产品与错误列出的ASIN匹配），则使用。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 可以提供两个功能：<br><br>可用于在您的目录产品与两个Amazon列表之间创建1对2关系。 示例： Amazon的产品以不同的ASIN值列出。 您可以将一个目录产品与产品的两个ASIN列表进行匹配。<br><br>可用于控制不同Amazon地区的列表。 示例：您有一个目录产品，该产品具有根据Amazon地区（美国地区为FBA，加拿大地区为FBM）定义的不同发运方法。 要控制库存/数量，您可以创建一个别名卖方SKU，然后使用不同的卖方SKU重新列出该区域中的相同产品。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 用于修改与产品关联的履行方法(由Amazon履行：FBA或由商家履行：FBM)。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （单个列表操作）用于手动结束和删除Amazon上存在的产品的列表。 只要结束的列表符合您的上市规则资格，就可以将其重新列出。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （单个列表操作）手动编辑现有的“覆盖”，该操作可为单个列表设置价格、处理时间、条件和卖方备注文本，而忽略其他列表默认值、设置和规则。 | [[!UICONTROL Overrides]](./overrides.md) |

## 访问产品列表

1. 在 _管理员_ 侧栏，转到 **营销** > _渠道_ > **AmazonSales Channel**.

1. 单击 **查看存储** 在商店卡上。

1. 在商店功能板上，单击 **管理列表** 在 _商店列表_ 部分。
