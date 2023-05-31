---
title: 不符合条件的Amazon列表
description: Amazon销售渠道提供 [!UICONTROL Ineligible] 选项卡帮助您管理项目，但根据您当前的列表规则，这些项目不符合列表资格。
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# 不符合条件的Amazon列表

此 _[!UICONTROL Ineligible]_选项卡显示当前在Amazon上发布但根据您当前的上市规则不符合上市资格的所有产品的列表。 如果之前的产品符合条件，并且修改了上市规则使其现在不符合条件，则与产品相关的数量将下降为0，并且该产品将标记为_&#x200B;不合格&#x200B;_. 但是，它仍存在于您的 [!DNL Amazon Seller Account].

要将产品移出 _[!UICONTROL Ineligible]_选项卡，您可以 [修改您的上市规则](./listing-rules.md) 以使您的产品符合条件。

上的可用操作 _[!UICONTROL Ineligible]_选项卡包括：

下 _[!UICONTROL Actions]_：

- **[!UICONTROL End Listing(s) on Amazon]**：选择以从列表中删除所有选定的列表 [!DNL Amazon Marketplace]. 参见 [结束Amazon列表](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**：选择以更改列表的覆盖设置。 参见 [覆盖](./overrides.md) 或 [编辑或删除覆盖](./creating-editing-overrides.md#edit-override-single-listing).

下 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列：

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括 [列出活动日志](./product-listing-details.md#listing-activity-log)， [Buy Box竞争对手定价](./product-listing-details.md#buy-box-competitor-pricing)、和 [最低竞争对手价格](./product-listing-details.md#lowest-competitor-pricing). 此操作仅供查看。 无法对列表详细信息进行任何更改。 参见 [查看详细信息](./product-listing-details.md).

- **[!UICONTROL Create Override]**：选择创建覆盖并将其应用于此列表。 参见 [创建覆盖](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**：选择以修改分配给您的目录产品的ASIN。 当目录中的产品与错误的ASIN匹配时，将使用此操作。 参见 [编辑分配的ASIN](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**：选择创建别名SKU，该SKU可用于从同一目录产品创建Amazon列表。 参见 [创建别名卖方SKU](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：选择以更改与订单关联的履行方法。 参见 [配置履行者设置](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**：选择以从列表中删除列表 [!DNL Amazon Marketplace]. 参见 [结束Amazon列表](./end-listings-manually.md).

>[!NOTE]
>如果您有正在处理的列表，则列表的数量将显示在选项卡上方的消息中。

![不符合条件的Amazon列表](assets/amazon-ineligible-listings.png){width="600" zoomable="yes"}

Amazon sales channel home pages有一些共同之处 [工作区控件](./workspace-controls.md) 允许您自定义显示的数据。

## 默认列

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的用于标识项目的唯一块。<br><br>ASIN表示 [!DNL Amazon Standard Identification Number]. ASIN是一个由10个字母和/或数字组成的唯一块，用于标识项目。 对于图书，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到它们的目录时，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 此 [条件](./product-listing-condition.md) 产品的。 |
| [!UICONTROL Landed Price] | 产品的上市价格加上装运价格。 |
| [!UICONTROL Amazon Quantity] | 当产品在Amazon上主动列出时的可用数量。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列并选择一个选项：<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[创建覆盖](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
