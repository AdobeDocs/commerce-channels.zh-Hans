---
title: 不合格的列表
description: Amazon销售渠道提供[!UICONTROL Ineligible]选项卡，以帮助您根据当前的上市规则管理不符合列表条件的项目。
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 不合格的列表

_[!UICONTROL Ineligible]_选项卡显示当前在Amazon上发布，但根据您当前的上市规则不符合上市条件的所有产品的列表。 如果以前的产品符合条件，并且修改了上市规则，使其现在不合格，则与产品关联的数量将降至0，并且该产品将标记为_&#x200B;不合格&#x200B;_。 但是，它仍存在于[!DNL Amazon Seller Account]上。

要将产品移出&#x200B;_[!UICONTROL Ineligible]_选项卡，您可以[修改上市规则](./listing-rules.md)，使您的产品符合条件。

_[!UICONTROL Ineligible]_选项卡上的可用操作包括：

在&#x200B;_[!UICONTROL Actions]_下：

- **[!UICONTROL End Listing(s) on Amazon]**:选择从中删除所有选定的列 [!DNL Amazon Marketplace]表。请参阅[结束Amazon列表](./end-listings-manually.md)。

- **[!UICONTROL Edit Listing Overrides]**:选择更改列表的覆盖设置。请参阅[覆盖](./overrides.md)或[编辑或删除覆盖](./creating-editing-overrides.md#edit-override-single-listing)。

在&#x200B;_[!UICONTROL Action]_列的&#x200B;**[!UICONTROL Select]**下：

- **[!UICONTROL View Details]**：选择查看列表详细信息，包括列 [表活动日志](./product-listing-details.md#listing-activity-log)、 [Buy Box竞争者定价](./product-listing-details.md#buy-box-competitor-pricing)和最低竞 [争者定价](./product-listing-details.md#lowest-competitor-pricing)。此操作仅用于查看。 列表详细信息中不能进行任何更改。 请参阅[查看详细信息](./product-listing-details.md)。

- **[!UICONTROL Create Override]**：选择创建覆盖并将其应用于此列表。请参阅[创建覆盖](./creating-editing-overrides.md)。

- **[!UICONTROL Edit Assigned ASIN]**：选择修改分配给目录产品的ASIN。如果目录中的某个产品与错误的ASIN匹配，则会使用此操作。 请参阅[编辑已分配的ASIN](./edit-assigned-asin.md)。

- **[!UICONTROL Create Alias Seller SKU]**：选择创建别名SKU，该别名SKU可用于从同一目录产品创建Amazon列表。请参阅[创建别名销售商SKU](./create-alias-seller-sku.md)。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：选择更改与订单关联的履行方法。请参阅[配置完成者设置](./fulfilled-by.md#configure-fulfilled-by-settings)。

- **[!UICONTROL End Listing]**：选择从中删除列 [!DNL Amazon Marketplace]表。请参阅[结束Amazon列表](./end-listings-manually.md)。

>[!NOTE]
>如果您正在处理列表，则列表数量会显示在选项卡上方的消息中。

![不合格的Amazon列表](assets/amazon-ineligible-listings.png)

Amazon销售渠道主页共享一些常用的[工作区控件](./workspace-controls.md)，这些控件允许您自定义显示的数据。

## 默认列

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | 由Amazon分配给产品以标识产品、选项、价格和制造商的SKU（库存单位）。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一块，用于标识项目。<br><br>ASIN代表 [!DNL Amazon Standard Identification Number]。ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Condition] | 产品的[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 产品的上市价格加其运价。 |
| [!UICONTROL Amazon Quantity] | 产品主动列在Amazon上时的可用数量。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用某个操作，请单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**，然后选择一个选项：<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[创建覆盖](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
