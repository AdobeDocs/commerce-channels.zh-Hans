---
title: Amazon列表不完整
description: Amazon销售渠道提供 [!UICONTROL Incomplete] 选项卡，以帮助您识别并满足不完整的Amazon列表的资格要求。
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Amazon列表不完整

此 _[!UICONTROL Incomplete]_选项卡列出了 [!DNL Commerce] 将符合Amazon资格要求的产品编录(在 [上市规则](./listing-rules.md))，但缺少Amazon所需的信息(例如Amazon ASIN或定义的产品条件)。

列表不完整有四种可能的原因，每种原因均由其状态标识。

| 状态 | 原因 | 操作 |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 缺少条件 | Amazon接受各种条件下的列表(例如 _新建_， _翻新_， _已使用：如新_)列表须符合界定条件。 | 更新所需信息并手动 [分配条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) 加入一个清单。 |
| 无法分配到Amazon列表 | 将此列表自动匹配到您的目录失败。 如果找不到匹配项，则列表无法由AmazonSales Channel管理 | 更新所需信息并手动 [分配ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) 与列表匹配的目录产品。 |
| 找到多个匹配项 | 将此列表自动匹配到您的目录失败。 如果找到多个可能的匹配项，则必须为您的产品选择正确的匹配项。 | 更新所需信息并手动 [选择产品匹配项](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) 产品和列表。 |
| 具有变量 | 如果您的产品具有变体，例如可用于不同大小或颜色的T恤，则必须选择目录中的变体进行正确分配并与列表匹配 | 更新所需信息并手动 [选择正确的变体](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) 以分配并匹配此列表。 |

>[!NOTE]
>当不完整的列表与您的目录产品正确匹配时，列表会从 _[!UICONTROL Incomplete]_选项卡，并发布到Amazon，其中基于 [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 设置。

上的可用操作 _[!UICONTROL Incomplete]_选项卡包括：

下 _[!UICONTROL Actions]_：

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**：选择以启动将Amazon列表数据与 [!DNL Commerce] 目录。 如果产品未自动匹配，请重新访问您的 [_[!UICONTROL Catalog Search]_](./catalog-search.md) 个选项。 如果列表在更新后不自动匹配 _[!UICONTROL Catalog Search]_选项，您可以在 [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) 操作。

下 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列：

- **[!UICONTROL Update Required Info]**：当列表与您的目录不自动匹配时选择。 您可以手动 [将目录产品与列表匹配](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)，手动 [分配ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) 与目录匹配项，或者 [分配缺少的条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) 供列名。

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括 [列出活动日志](./product-listing-details.md#listing-activity-log)， [Buy Box竞争对手定价](./product-listing-details.md#buy-box-competitor-pricing)、和 [最低竞争对手定价](./product-listing-details.md#lowest-competitor-pricing). 此操作仅供查看。 无法对列表详细信息进行任何更改。 请参阅 [查看详细信息](./product-listing-details.md).

>[!NOTE]
>
>如果您有正在处理的列表，则列表数会显示在选项卡上方的消息中。

![Amazon列表不完整](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

Amazon sales channel主页共享一些常见的 [工作区控件](./workspace-controls.md) 允许您自定义显示的数据。

| 列 | 描述 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一用于标识项目的块。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]. ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到其目录时，会创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 此 [条件](./product-listing-condition.md) 产品的。 |
| [!UICONTROL Landed Price] | 产品的上市价格加上装运价格。 |
| [!UICONTROL Amazon Quantity] | Amazon上主动列出产品时的可用数量。 |
| [!UICONTROL Status] | 由Amazon定义的列表状态。 请参阅上面的“状态”表。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作的列表。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列并选择一个选项：<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
