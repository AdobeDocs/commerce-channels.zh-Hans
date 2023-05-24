---
title: 覆盖
description: AmazonSales Channel提供了“覆盖”选项卡，以帮助您识别和管理如何在Amazon列表中应用覆盖。
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# 覆盖

此 _[!UICONTROL Overrides]_选项卡显示您已应用覆盖的Amazon列表。 覆盖是特定于列表的设置，可用于将定义的值设置为列表。 无论其他已定义的列表设置或列表适用于的规则如何，应用于列表的覆盖都会定义列表的设置。 将覆盖应用于列表后，该列表将显示在_[!UICONTROL Overrides]_ 选项卡。 覆盖中定义的值将显示在列表的相应列中。 有四种类型的覆盖可以应用：价格、处理时间、条件和卖方备注。

## 覆盖类型

| 类型 | 描述 |
|---|---|
| 价格 | 设置列表价格的改写，它将忽略列表的所有其它价格设置。 <br><br>**示例**：您定义了一个20%折扣价格规则，该规则适用于您目录的特定类别中的所有产品。 您有一个新产品，而且需求量很大，因此即使该产品属于该类别，您也不希望将折扣价应用于列表。 您可以选择列表， [创建价格覆盖](./creating-editing-overrides.md#edit-override-single-listing)，并在价格覆盖中定义上市价格。 |
| 处理时间 | 设置列表的处理时间的覆盖，忽略在列表设置中设置的默认处理时间。<br><br>**示例**：列表的默认处理时间设置为2天。 您有一个易碎的产品，需要额外的一天来确保其特殊的包装用于运输。 您可以查看列表， [创建处理时间覆盖](./creating-editing-overrides.md#edit-override-single-listing)，并将处理时间定义为三天。<br><br>**注意：** 不可用于设置为的产品 `Fulfilled by Amazon`. |
| 条件 | 一种覆盖，它设置清单的条件值，而不考虑分配给清单的条件属性。<br><br>**示例**：您的目录中的大多数产品都处于新状态，但您的产品却处于翻新状态。 您可以查看列表， [创建条件覆盖](./creating-editing-overrides.md#edit-override-single-listing)，并定义列表的翻新条件。<br><br>**注意：** 不可用于设置为的产品 `Fulfilled by Amazon`. |
| 卖方备注 | 定义 _卖方备注_ 部分。 此字段可用于添加与所应用产品或覆盖相关的其他信息，通常用于描述“非新”产品的条件。 此字段中的文本随购物者的列表一起显示。 无法为条件值为的列表添加卖方备注 `New`. <br><br>**示例**：您有一个产品正在使用 `Refurbished` 条件。 通常情况下，此状态下的产品不包含任何手册或文档，但您对此产品有不同的供应商，其中包括手册。 您可以查看列表， [创建卖方备注覆盖](./creating-editing-overrides.md#edit-override-single-listing)，并添加您手册中此列表特有的文本注释，以便购物者知道此注释包含在内。<br><br>**注释**：如果产品具有的定义条件 `New`，您可以输入卖方笔记覆盖，但Amazon不显示卖方笔记 `New` 产品。 |

您可以创建、编辑或删除覆盖 [单一列表](./creating-editing-overrides.md#edit-override-single-listing). 在 _[!UICONTROL Inactive]_，_[!UICONTROL Active]_、和 _[!UICONTROL Ineligible]_选项卡，您可以单击&#x200B;**[!UICONTROL Select]**在_[!UICONTROL Action]_ 列并选择 **[!UICONTROL Create Override]**. 此 _[!UICONTROL Edit Overrides]_仅当列表应用了覆盖并在以下位置查看时，操作才可用_[!UICONTROL Overrides]_ 选项卡。

您还可以创建、编辑或删除覆盖 [多个列表](./creating-editing-overrides.md#edit-override-multiple-listings). 在 _[!UICONTROL Inactive]_，_[!UICONTROL Active]_、和 _[!UICONTROL Ineligible]_选项卡，您可以单击&#x200B;**[!UICONTROL Select]**在_[!UICONTROL Action]_ 列并选择 **[!UICONTROL Edit Listing Overrides]**.

删除覆盖可告知列表使用由列表设置和规则定义的值。

定义改写时，您还可以选择输入单个改写类型或类型组合。

参见 [创建和编辑覆盖](./creating-editing-overrides.md).

>[!NOTE]
>
>如果您有正在处理的列表，则列表的数量将显示在选项卡上方的消息中。

![“覆盖”选项卡](assets/amazon-overrides.png)

Amazon sales channel home pages有一些共同之处 [工作区控件](./workspace-controls.md) 允许您自定义显示的数据。

## 默认列

| 列 | 描述 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazon为产品分配的SKU（库存单位），用于标识产品、选件、价格和制造商。 |
| [!UICONTROL ASIN] | 由10个字母和/或数字组成的用于标识项目的唯一块。<br><br>ASIN表示Amazon标准标识号。 ASIN是一个由10个字母和/或数字组成的唯一块，用于标识项目。 对于图书，ASIN与ISBN编号相同，但对于所有其他产品，当项目上传到它们的目录时，将创建一个新的ASIN。 您可以在Amazon的产品详细信息页面上找到项目ASIN，以及与该项目相关的更多详细信息。 |
| [!UICONTROL Condition Override] | 覆盖中定义的新条件。 如果应用于列表的覆盖不是条件覆盖， `Not Selected` 将显示在此列中。 |
| [!UICONTROL Product Listing Name] | 产品的名称。 |
| [!UICONTROL Seller Notes Override] | 覆盖中定义的新卖方备注。 如果应用于列表的覆盖不是这种类型的覆盖，则此列为空。 |
| [!UICONTROL Handling Override] | 覆盖中定义的新处理时间（以天为单位）。 如果应用于列表的覆盖不是处理时间覆盖，则此列为空。 |
| [!UICONTROL List Price Override] | 覆盖中定义的新上市价格。 如果应用于列表的覆盖不是价格覆盖， `N/A` 将显示在此列中。 |
| [!UICONTROL Action] | 可应用于特定列表的可用操作列表。 要应用操作，请在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL Select]**并选择一个选项：<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
