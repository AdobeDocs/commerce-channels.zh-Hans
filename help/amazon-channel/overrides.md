---
title: 覆盖
description: AmazonSales Channel提供了覆盖选项卡，以帮助您识别和管理在Amazon列表中应用覆盖的方式。
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# 覆盖

_[!UICONTROL Overrides]_选项卡显示您已对其应用覆盖的Amazon列表。 覆盖是特定于列表的设置，可使用该设置将定义的值设置为列表。 应用于列表的覆盖定义了列表的设置，而不考虑其他定义的列表设置或列表符合条件的规则。 当对列表应用覆盖时，该列表会显示在_[!UICONTROL Overrides]_&#x200B;选项卡中。 覆盖中定义的值将显示在列表的相应列中。 可以应用四种类型的覆盖：价格、处理时间、条件和销售者票据。

## 覆盖类型

| 类型 | 描述 |
|---|---|
| 价格 | 设置列表价格的覆盖，忽略该列表的所有其他价格设置。 <br><br>**示例**:您定义了适用于目录特定类别中所有产品的20%折扣价格规则。您的产品是新市场产品，需求很高，因此即使产品属于该类别，您也不希望将折扣价格应用于列表。 您可以选择[创建价格改写](./creating-editing-overrides.md#edit-override-single-listing)的列表，并定义价格改写中的列表价格。 |
| 处理时间 | 设置列表处理时间的覆盖，忽略列表设置中设置的默认处理时间。<br><br>**示例**:您的列表的默认处理时间设置为2天。您的产品很脆弱，需要额外一天来确保其特殊的装运包装。 您可以查看列表， [创建处理时间覆盖](./creating-editing-overrides.md#edit-override-single-listing)，并在三天内定义处理时间。<br><br>**注意：** 不适用于设置为的产 `Fulfilled by Amazon`品。 |
| 条件 | 一个覆盖，用于设置列表的条件值，而不考虑分配给列表的条件属性。<br><br>**示例**:您目录中的大多数产品都是“新条件”，但您的产品处于“翻新”状态。您可以查看列表， [创建条件override](./creating-editing-overrides.md#edit-override-single-listing)，并为列表定义Prinned条件。<br><br>**注意：** 不适用于设置为的产 `Fulfilled by Amazon`品。 |
| 卖家说明 | 定义列表&#x200B;_卖家说明_&#x200B;部分的覆盖。 此字段可用于添加与产品或所应用覆盖相关的其他信息，通常用于描述“非新”产品的条件。 此字段中的文本将随购物者的列表一起显示。 无法为条件值`New`的列表添加卖家注释。 <br><br>**示例**:您的产品处于状 `Refurbished` 态。通常情况下，此条件下的产品不包括任何手册或文档，但您对此产品有不同的供应商，其中包括手册。 您可以查看列表（[创建销售者注释覆盖](./creating-editing-overrides.md#edit-override-single-listing)），并添加此列表特有的关于手册的文本注释，以便购物者知道其中包含该注释。<br><br>**注意**:如果产品的定义条件为 `New`，则可以输入销售商附注改写，但Amazon不显示产品的销售商 `New` 附注。 |

您可以为[单个列表](./creating-editing-overrides.md#edit-override-single-listing)创建、编辑或删除覆盖。 在&#x200B;_[!UICONTROL Inactive]_、_[!UICONTROL Active]_&#x200B;和&#x200B;_[!UICONTROL Ineligible]_选项卡上，可以单击_[!UICONTROL Action]_&#x200B;列中的&#x200B;**[!UICONTROL Select]**&#x200B;并选择&#x200B;**[!UICONTROL Create Override]**。 _[!UICONTROL Edit Overrides]_操作仅在列表应用了覆盖后才可用，该列表可在_[!UICONTROL Overrides]_&#x200B;选项卡上查看。

您还可以创建、编辑或删除对[多个列表](./creating-editing-overrides.md#edit-override-multiple-listings)的覆盖。 在&#x200B;_[!UICONTROL Inactive]_、_[!UICONTROL Active]_&#x200B;和&#x200B;_[!UICONTROL Ineligible]_选项卡上，可以单击_[!UICONTROL Action]_&#x200B;列中的&#x200B;**[!UICONTROL Select]**&#x200B;并选择&#x200B;**[!UICONTROL Edit Listing Overrides]**。

删除覆盖会告知列表使用由列表设置和规则定义的值。

在定义覆盖时，您还可以选择输入单种覆盖类型或这些类型的任意组合。

请参阅[创建和编辑覆盖](./creating-editing-overrides.md)。

>[!NOTE]
>
>如果您正在处理列表，则列表数量会显示在选项卡上方的消息中。

![“覆盖”选项卡](assets/amazon-overrides.png)

Amazon销售渠道主页共享一些常用的[工作区控件](./workspace-controls.md)，这些控件允许您自定义显示的数据。

## 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | 由Amazon分配给产品以标识产品、选项、价格和制造商的SKU（库存单位）。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的唯一块，用于标识项目。<br><br>ASIN表示Amazon标准标识号。ASIN是由10个字母和/或数字组成的唯一块，用于标识项目。 对于书籍，ASIN与ISBN号相同，但对于所有其他产品，在将项目上传到其目录后，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与项目相关的更多详细信息。 |
| [!UICONTROL Condition Override] | 覆盖中定义的新条件。 如果应用于列表的覆盖不是条件覆盖，则`Not Selected`将出现在此列中。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Seller Notes Override] | 在改写中定义的新卖方注释。 如果应用于列表的覆盖不是此类型的覆盖，则此列为空。 |
| [!UICONTROL Handling Override] | 在覆盖中定义的新处理时间（以天为单位）。 如果应用于列表的覆盖不是处理时间覆盖，则此列为空。 |
| [!UICONTROL List Price Override] | 在覆盖中定义的新上市价格。 如果应用于列表的改写不是价格改写，则`N/A`将出现在此列中。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用操作，请在&#x200B;_[!UICONTROL Action]_列中单击&#x200B;**[!UICONTROL Select]**并选择一个选项：<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
