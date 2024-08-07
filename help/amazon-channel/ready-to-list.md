---
title: Amazon销售渠道 — [!UICONTROL Ready to List]
description: Amazon Sales Channel提供了Ready to List选项卡，以帮助您查看符合条件但未自动列出的Commerce产品。
feature: Sales Channels, Products, Merchandising
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

_[!UICONTROL Ready to List]_选项卡显示您的[!DNL Commerce]目录产品，这些产品符合您的列表设置并准备好作为&#x200B;**新**列表发布到Amazon。 与其他列表选项卡不同，此选项卡并不总是出现在[_[!UICONTROL Product Listings]_](./managing-product-listings.md)页面上。

仅当列表设置中的[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)设置为`Do Not Automatically List Eligible Products`时，_[!UICONTROL Ready to List]_选项卡才会显示。 此设置告知Amazon销售渠道，任何新的Amazon列表都必须手动发布。

当[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)设置为`Automatically List Eligible Products`时，Amazon Sales Channel会自动发布符合条件的目录产品的新列表。 由于新列表会自动发布，因此不会显示&#x200B;_[!UICONTROL Ready to List]_选项卡。

在&#x200B;_[!UICONTROL Actions]_下：

- **[!UICONTROL Publish Product to Amazon]**：选择将列表重新发布到[!DNL Amazon Marketplace]。 查看[Publish和Amazon列表](./publish-listings-manually.md)

在&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**下：

- **[!UICONTROL Publish On Amazon]**：选择将列表重新发布到[!DNL Amazon Marketplace]。 请参阅[Publish an Amazon列表](./publish-listings-manually.md)。

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括[列表活动日志](./product-listing-details.md#listing-activity-log)、[Buy Box竞争者定价](./product-listing-details.md#buy-box-competitor-pricing)和[最低竞争者定价](./product-listing-details.md#lowest-competitor-pricing)。 此操作仅供查看。 无法对列表详细信息进行任何更改。 查看[查看详细信息](./product-listing-details.md)。

有一些选项可手动[将新列表发布到Amazon](./publish-listings-manually.md)。

>[!NOTE]
>如果您正在处理列表，则列表数将显示在选项卡上方的消息中。

![准备列出](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## 默认列

| 列 | 描述 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一用于标识项目的块。<br><br>ASIN代表[!DNL Amazon Standard Identification Number]。 ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到其目录时，会创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 产品的[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 产品的上市价格加上装运价格。 |
| [!UICONTROL Amazon Quantity] | Amazon上主动列出产品时的可用数量。 |
| [!UICONTROL Status] | 由Amazon定义的列表状态。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作的列表。 要应用操作，请单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**并选择一个选项：<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### 准备列出列表的常见原因

- **[!UICONTROL Ready to List]** — 产品与Amazon ASIN匹配，已计划列出。 如果将列表设置中的[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)设置为`Do Not Automatically List Eligible Products`，则此状态表示可以手动列出的产品。

- **[!UICONTROL List in Progress]** — 产品列表已提交给Amazon，并等待Amazon的接受确认。
