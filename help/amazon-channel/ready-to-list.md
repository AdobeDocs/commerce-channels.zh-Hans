---
title: 准备列表
description: Amazon销售渠道提供“准备列表”选项卡，以帮助您查看符合资格但未自动列出的商务产品。
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

的 _[!UICONTROL Ready to List]_选项卡 [!DNL Commerce] 目录产品，这些产品符合您的列表设置，并可以作为&#x200B;**新建**列表。 与其他列表选项卡不同，此选项卡并非总是显示在 [_[!UICONTROL Product Listings]_](./managing-product-listings.md) 页面。

的 _[!UICONTROL Ready to List]_选项卡 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) 在列表设置中，将设置为 `Do Not Automatically List Eligible Products`. 此设置可告知Amazon销售渠道，任何新的Amazon列表都必须手动发布。

When [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) 设置为 `Automatically List Eligible Products`,Amazon销售渠道会自动发布符合条件的目录产品的新列表。 由于新列表是自动发布的，因此 _[!UICONTROL Ready to List]_选项卡。

在 _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**:选择将列表重新发布到 [!DNL Amazon Marketplace]. 请参阅 [发布Amazon列表](./publish-listings-manually.md)

在 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列：

- **[!UICONTROL Publish On Amazon]**:选择将列表重新发布到 [!DNL Amazon Marketplace]. 请参阅 [发布Amazon列表](./publish-listings-manually.md).

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括 [列出活动日志](./product-listing-details.md#listing-activity-log), [Buy Box竞争者定价](./product-listing-details.md#buy-box-competitor-pricing)和 [竞争者定价最低](./product-listing-details.md#lowest-competitor-pricing). 此操作仅用于查看。 列表详细信息中不能进行任何更改。 请参阅 [查看详细信息](./product-listing-details.md).

您有一些手动选项 [将新列表发布到Amazon](./publish-listings-manually.md).

>[!NOTE]
>如果正在处理列表，则列表数量会显示在选项卡上方的消息中。

![准备列表](assets/amazon-ready-to-list.png)

## 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | 由Amazon分配给产品以标识产品、选项、价格和制造商的SKU（库存单位）。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一块，用于标识项目。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]. ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 的 [条件](./product-listing-condition.md) 产品。 |
| [!UICONTROL Landed Price] | 产品的上市价格加其运价。 |
| [!UICONTROL Amazon Quantity] | 产品主动列在Amazon上时的可用数量。 |
| [!UICONTROL Status] | 列表的状态，由Amazon定义。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用操作，请单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列，然后选择选项：<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### 准备列表的常见原因

- **[!UICONTROL Ready to List]**  — 产品与Amazon ASIN匹配，并计划列出。 如果 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) 在列表设置中，将设置为 `Do Not Automatically List Eligible Products`，此状态表示已准备好手动列出的产品。

- **[!UICONTROL List in Progress]**  — 产品清单已提交至Amazon，正在等待Amazon的验收确认。
