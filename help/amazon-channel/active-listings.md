---
title: 有效的Amazon列表
description: Amazon Sales Channel提供了Active选项卡来监视活动的Amazon列表以及与您的Adobe Commerce目录中的产品匹配的列表。
feature: Sales Channels, Products, Merchandising, Catalog Management
exl-id: c9105abc-74d6-442b-8d7a-e5aaea8872e4
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# 有效的Amazon列表

此 _[!UICONTROL Active]_选项卡显示 [!DNL Amazon Marketplace] 与中的产品匹配的产品 [!DNL Commerce] 目录。

上的可用操作 _[!UICONTROL Active]_选项卡包括：

下 _[!UICONTROL Actions]_：

- **[!UICONTROL End Listing(s) on Amazon]**：选择以从删除所有选定的列表 [!DNL Amazon Marketplace]. 请参阅 [结束Amazon列表](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**：选择以更改列表的覆盖设置。 请参阅 [覆盖](./overrides.md) 或 [编辑或删除覆盖](./creating-editing-overrides.md#edit-override-single-listing).

下 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列：

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括 [列出活动日志](./product-listing-details.md#listing-activity-log)， [Buy Box竞争对手定价](./product-listing-details.md#buy-box-competitor-pricing)、和 [最低竞争对手定价](./product-listing-details.md#lowest-competitor-pricing). 此操作仅供查看。 无法对列表详细信息进行任何更改。 请参阅 [查看详细信息](./product-listing-details.md).

- **[!UICONTROL Create Override]**：选择创建覆盖并将其应用于此列表。 请参阅 [创建覆盖](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**：选择以修改分配给您的目录产品的ASIN。 如果目录中的产品与错误的ASIN匹配，请使用此操作。 请参阅 [编辑分配的ASIN](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**：选择创建别名SKU，该SKU可用于从同一目录产品创建Amazon列表。 请参阅 [创建别名卖方SKU](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：选择以更改与订单关联的履行方法。 请参阅 [配置完成者设置](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**：选择以从列表中删除列表 [!DNL Amazon Marketplace]. 请参阅 [结束Amazon列表](./end-listings-manually.md).

>[!NOTE]
>
>如果您正在处理列表，则列表数将显示在选项卡上方的消息中。

![活动列表](assets/amazon-active-listings.png){width="700" zoomable="yes"}

Amazon sales channel主页共享一些常见的 [工作区控件](./workspace-controls.md) 允许您自定义显示的数据。

| 列 | 描述 |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一用于标识项目的块。 <br><br>ASIN代表 [!DNL Amazon Standard Identification Number]. ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到其目录时，会创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 此 [条件](./product-listing-condition.md) 产品的。 |
| [!UICONTROL Landed Price] | 产品的上市价格加上装运价格。 |
| [!UICONTROL Amazon Quantity] | 产品在Amazon上主动列出后的可用数量。 |
| [!UICONTROL Status] | 由Amazon定义的列表状态。 |
| [!UICONTROL Buy Box Won] | 产品清单是否赢得了 [Buy Box](./buy-box-competitor-pricing.md) 位置。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作的列表。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列来显示您的选项：<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
