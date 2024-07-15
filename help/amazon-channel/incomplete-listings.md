---
title: Amazon列表不完整
description: Amazon sales channel提供了[!UICONTROL Incomplete]选项卡，以帮助您识别不完整的Amazon列表并满足其资格要求。
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Amazon列表不完整

_[!UICONTROL Incomplete]_选项卡列出了满足您的Amazon资格要求（在您的[列表规则](./listing-rules.md)中定义）但缺少Amazon所需的信息(例如Amazon ASIN或定义的产品条件)的[!DNL Commerce]目录产品。

列表不完整有四种可能的原因，每种原因均由其状态标识。

| 状态 | 原因 | 操作 |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 缺少条件 | Amazon接受各种条件（如&#x200B;_New_、_Refluished_、_Used： Like New_）下的列表需要定义的条件。 | 更新所需信息并手动[将条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition)分配给列表。 |
| 无法分配到Amazon列表 | 将此列表自动匹配到您的目录失败。 如果找不到匹配项，则列表无法由AmazonSales Channel管理 | 更新所需信息并手动[将ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)分配给目录产品以与列表匹配。 |
| 找到多个匹配项 | 将此列表自动匹配到您的目录失败。 如果找到多个可能的匹配项，则必须为您的产品选择正确的匹配项。 | 更新所需信息并手动[为产品和列表选择产品匹配项](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)。 |
| 具有变量 | 如果您的产品具有变体，例如可用于不同大小或颜色的T恤，则必须选择目录中的变体进行正确分配并与列表匹配 | 更新所需信息并手动[选择要分配并匹配此列表的正确变体](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants)。 |

>[!NOTE]
>当不完整的列表与您的目录产品正确匹配时，该列表将从&#x200B;_[!UICONTROL Incomplete]_选项卡中移出，并根据您的[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)设置发布到Amazon。

_[!UICONTROL Incomplete]_选项卡上的可用操作包括：

在&#x200B;_[!UICONTROL Actions]_下：

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**：选择以启动将Amazon列表数据与[!DNL Commerce]目录匹配的自动流程。 如果产品不自动匹配，请重新访问列表设置中的[_[!UICONTROL Catalog Search]_](./catalog-search.md)选项。 如果列表在更新&#x200B;_[!UICONTROL Catalog Search]_选项后不自动匹配，您可以在[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)操作中手动匹配产品。

在&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**下：

- **[!UICONTROL Update Required Info]**：当列表与您的目录不自动匹配时选择。 您可以手动[将目录产品与列表匹配](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)，手动[将ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)分配给目录匹配项，或[为列表分配缺少的条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition)。

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括[列表活动日志](./product-listing-details.md#listing-activity-log)、[Buy Box竞争者定价](./product-listing-details.md#buy-box-competitor-pricing)和[最低竞争者定价](./product-listing-details.md#lowest-competitor-pricing)。 此操作仅供查看。 无法对列表详细信息进行任何更改。 查看[查看详细信息](./product-listing-details.md)。

>[!NOTE]
>
>如果您有正在处理的列表，则列表数会显示在选项卡上方的消息中。

![不完整的Amazon列表](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

Amazon sales channel主页共享一些常用的[工作区控件](./workspace-controls.md)，这些控件允许您自定义显示的数据。

| 列 | 描述 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一用于标识项目的块。<br><br>ASIN代表[!DNL Amazon Standard Identification Number]。 ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到其目录时，会创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 产品的[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 产品的上市价格加上装运价格。 |
| [!UICONTROL Amazon Quantity] | Amazon上主动列出产品时的可用数量。 |
| [!UICONTROL Status] | 由Amazon定义的列表状态。 请参阅上面的“状态”表。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作的列表。 要应用操作，请单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**并选择一个选项：<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
