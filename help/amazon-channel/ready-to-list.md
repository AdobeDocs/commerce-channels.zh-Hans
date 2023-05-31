---
title: Amazon销售渠道 —  [!UICONTROL Ready to List]
description: Amazon Sales Channel提供了Ready to List选项卡，以帮助您查看符合条件但未自动列出的Commerce产品。
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

此 _[!UICONTROL Ready to List]_选项卡显示 [!DNL Commerce] 满足列表设置并准备好发布到Amazon as a的目录产品&#x200B;**新**列表。 与其他列表选项卡不同，此选项卡并不总是出现在 [_[!UICONTROL Product Listings]_](./managing-product-listings.md) 页面。

此 _[!UICONTROL Ready to List]_选项卡仅在 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) 在列表设置中，设置为 `Do Not Automatically List Eligible Products`. 此设置可告知Amazon sales channel，必须手动发布任何新的Amazon列表。

时间 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) 设置为 `Automatically List Eligible Products`，Amazon sales channel会自动发布符合条件的目录产品的新列表。 由于新列表会自动发布，因此 _[!UICONTROL Ready to List]_选项卡未显示。

下 _[!UICONTROL Actions]_：

- **[!UICONTROL Publish Product to Amazon]**：选择将列表重新发布到 [!DNL Amazon Marketplace]. 参见 [发布Amazon列表](./publish-listings-manually.md)

下 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列：

- **[!UICONTROL Publish On Amazon]**：选择将列表重新发布到 [!DNL Amazon Marketplace]. 参见 [发布Amazon列表](./publish-listings-manually.md).

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括 [列出活动日志](./product-listing-details.md#listing-activity-log)， [Buy Box竞争对手定价](./product-listing-details.md#buy-box-competitor-pricing)、和 [最低竞争对手价格](./product-listing-details.md#lowest-competitor-pricing). 此操作仅供查看。 无法对列表详细信息进行任何更改。 参见 [查看详细信息](./product-listing-details.md).

您可以手动选择几个选项 [将新列表发布到Amazon](./publish-listings-manually.md).

>[!NOTE]
>如果您有正在处理的列表，则列表的数量将显示在选项卡上方的消息中。

![准备列出](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的用于标识项目的唯一块。<br><br>ASIN表示 [!DNL Amazon Standard Identification Number]. ASIN是一个由10个字母和/或数字组成的唯一块，用于标识项目。 对于图书，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到它们的目录时，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 此 [条件](./product-listing-condition.md) 产品的。 |
| [!UICONTROL Landed Price] | 产品的上市价格加上装运价格。 |
| [!UICONTROL Amazon Quantity] | 当产品在Amazon上主动列出时的可用数量。 |
| [!UICONTROL Status] | 由Amazon定义的列表状态。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列并选择一个选项：<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### 列表准备就绪的常见原因

- **[!UICONTROL Ready to List]**  — 产品与Amazon ASIN匹配并计划列出。 如果 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) 在列表设置中，设置为 `Do Not Automatically List Eligible Products`，此状态表示准备好手动列出的产品。

- **[!UICONTROL List in Progress]**  — 产品列表已提交给Amazon，并等待Amazon的接受确认。
