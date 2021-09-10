---
title: 列表不完整
description: Amazon销售渠道提供[!UICONTROL Incomplete]选项卡，帮助您识别并满足您未完成的Amazon列表的资格要求。
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# 列表不完整

_[!UICONTROL Incomplete]_选项卡列出了符合Amazon资格要求的[!DNL Commerce]目录产品（在[列表规则](./listing-rules.md)中定义），但缺少Amazon所需的信息(如Amazon ASIN或定义的产品条件)。

列表不完整可能有四个原因，每个原因都由其状态确定。

| 状态 | 原因 | 操作 |
|--- |--- |--- |
| 缺少条件 | Amazon接受各种条件（如&#x200B;_New_、_Frening_、_已使用的列表）：Like New_)列表需要定义条件。 | 更新所需信息并手动[将条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition)分配给列表。 |
| 无法分配到Amazon列表 | 此列表与目录的自动匹配失败。 如果未找到匹配项，则列表无法由AmazonSales Channel管理 | 更新所需信息并手动[将ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)分配给目录产品以与列表匹配。 |
| 找到多个匹配项 | 此列表与目录的自动匹配失败。 如果找到多个可能的匹配项，则必须为您的产品选择正确的匹配项。 | 更新所需信息，然后手动[为产品和列表选择产品匹配](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)。 |
| 具有变体 | 如果您的产品具有变体(例如T恤衫，该T恤衫的大小或颜色不同，则必须在目录中选择变体，才能正确分配该变体并将其与列表匹配 | 更新所需信息，然后手动[选择正确的变体](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants)以分配并匹配此列表。 |

>[!NOTE]
>如果未完成的列表与您的目录产品正确匹配，则该列表会从&#x200B;_[!UICONTROL Incomplete]_选项卡中移动，并根据您的[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)设置发布到Amazon。

_[!UICONTROL Incomplete]_选项卡上的可用操作包括：

在&#x200B;_[!UICONTROL Actions]_下：

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**:选择启动将Amazon列表数据与目录匹配的自动 [!DNL Commerce] 流程。如果产品不自动匹配，请重新访问列表信件中的[_[!UICONTROL Catalog Search]_](./catalog-search.md)选项。 如果列表在更新&#x200B;_[!UICONTROL Catalog Search]_选项后不自动匹配，则可以在[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)操作中手动匹配产品。

在&#x200B;_[!UICONTROL Action]_列的&#x200B;**[!UICONTROL Select]**下：

- **[!UICONTROL Update Required Info]**:选择列表何时与目录不自动匹配。您可以手动[将目录产品与列表](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)匹配，手动[将ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)分配给目录匹配，或者[将缺少的条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition)分配给列表。

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括列 [表活动日志](./product-listing-details.md#listing-activity-log)、 [Buy Box竞争者定价](./product-listing-details.md#buy-box-competitor-pricing)和最低竞 [争者定价](./product-listing-details.md#lowest-competitor-pricing)。此操作仅用于查看。 列表详细信息中不能进行任何更改。 请参阅[查看详细信息](./product-listing-details.md)。

>[!NOTE]
>
>如果正在处理列表，则列表数量会显示在选项卡上方的消息中。

![Amazon列表不完整](assets/amazon-incomplete-listings.png)

Amazon销售渠道主页共享一些常用的[工作区控件](./workspace-controls.md)，这些控件允许您自定义显示的数据。

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | 由Amazon分配给产品以标识产品、选项、价格和制造商的SKU（库存单位）。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一块，用于标识项目。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]。ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 产品的[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 产品的上市价格加其运价。 |
| [!UICONTROL Amazon Quantity] | 产品主动列在Amazon上时的可用数量。 |
| [!UICONTROL Status] | 列表的状态，由Amazon定义。 请参阅上面的状态表。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用某个操作，请单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**，然后选择一个选项：<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
