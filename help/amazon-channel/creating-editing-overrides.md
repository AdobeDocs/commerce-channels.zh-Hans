---
title: 创建和编辑Amazon sales channel覆盖
description: 使用AmazonSales Channel覆盖可将您的更改应用于单个Amazon列表或多个列表。
feature: Sales Channels, Products, Configuration
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---

# 创建和编辑覆盖

您可以创建和覆盖列表，或编辑或删除已应用于列表的覆盖。 覆盖为特定列表设置定义的值。

## 为单个列表创建覆盖

查看&#x200B;_[!UICONTROL Inactive]_、_[!UICONTROL Active]_&#x200B;和&#x200B;_[!UICONTROL Ineligible]_选项卡上的列表时，_[!UICONTROL Create Override]_&#x200B;操作可用。

1. 查看&#x200B;_[!UICONTROL Products Listings]_页面（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_和_[!UICONTROL Ineligible]_&#x200B;选项卡）上的列表。

1. 在&#x200B;_[!UICONTROL Action]_列中，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Create Override]**以打开产品列表覆盖页。

   ![创建Amazon列表覆盖](assets/amazon-select-create-override.png){width="220"}

1. 为确保您查看正确的列表，请验证&#x200B;_[!UICONTROL Listing Details]_。

1. 确定正在创建的覆盖类型。

   您可以为列表定义单个改写类型或任何类型组合（“价格”、“处理时间”、“条件”、“卖方附注”）。

   - **价格** — 单击&#x200B;**[!UICONTROL Change Listing Price]**&#x200B;并输入您为&#x200B;**[!UICONTROL Price Override]**&#x200B;定义的价格值。
   - **处理时间** — 单击&#x200B;**[!UICONTROL Change Handling Time]**&#x200B;并输入&#x200B;**[!UICONTROL Handling Time Override]**&#x200B;的已定义时间值（以天为单位）。
   - **条件** — 单击&#x200B;**[!UICONTROL Change Condition]**&#x200B;并为&#x200B;**[!UICONTROL Condition Override]**&#x200B;选择正确的选项。
   - **卖方备注** — 单击&#x200B;**[!UICONTROL Change Seller Notes]**&#x200B;并输入&#x200B;**[!UICONTROL Seller Notes Override]**&#x200B;的备注文本。

1. 单击&#x200B;**[!UICONTROL Save Listing Override]**。

   “_[!UICONTROL Product Listing Overrides]_”页面关闭。 列表的状态更改为`Relist in Progress`。 更改将使用您的下一个数据同步（如在cron设置中所配置）发布到Amazon。 该列表也将添加到_[!UICONTROL Overrides]_&#x200B;选项卡。

以下示例显示了一个覆盖，该覆盖定义了新价格`$55`、新处理时间`1 day`、新条件`Used; Like New`以及新卖方备注文本。

![示例Amazon列表覆盖](assets/amazon-overrides-edit.png){width="600" zoomable="yes"}

## 编辑或删除单个列表的覆盖 {#edit-override-single-listing}

在&#x200B;_[!UICONTROL Overrides]_选项卡上查看列表时，_[!UICONTROL Edit Overrides]_&#x200B;操作可用。

1. 查看&#x200B;_[!UICONTROL Product Listings]_页面（_[!UICONTROL Overrides]_&#x200B;选项卡）上的列表。

1. 在&#x200B;_[!UICONTROL Action]_列中，单击&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**。

   将打开&#x200B;_[!UICONTROL Product Listing Overrides]_页面。

   ![选择Amazon列表覆盖](assets/amazon-select-edit-overrides.png){width="125"}

1. 为确保您覆盖正确的列表，请验证&#x200B;_[!UICONTROL Listing Details]_。

1. 要编辑&#x200B;_[!UICONTROL Override]_设置，请为要更改的类型（价格、处理时间、条件、卖方备注）定义部分。

   若要保持覆盖类型相同，请选择`No Change To <override type>` （默认值）。 此设置使以前定义的覆盖值保持不变。

   - **价格** — 单击&#x200B;**[!UICONTROL Change Listing Price]**&#x200B;并输入您为&#x200B;**[!UICONTROL Price Override]**&#x200B;定义的价格值。
   - **处理时间** — 单击&#x200B;**[!UICONTROL Change Handling Time]**&#x200B;并输入&#x200B;**[!UICONTROL Handling Time Override]**&#x200B;的已定义时间值（以天为单位）。
   - **条件** — 单击&#x200B;**[!UICONTROL Change Condition]**&#x200B;并为&#x200B;**[!UICONTROL Condition Override]**&#x200B;选择正确的选项。
   - **卖方备注** — 单击&#x200B;**[!UICONTROL Change Seller Notes]**&#x200B;并输入&#x200B;**[!UICONTROL Seller Notes Override]**&#x200B;的备注文本。

1. 要删除覆盖类型，请为每个要删除的类型单击&#x200B;**删除**。 如果未删除，则先前定义的值将保留在覆盖中。

1. 单击&#x200B;**[!UICONTROL Save Listing Override]**。

   “_[!UICONTROL Product Listing Overrides]_”页面关闭。 列表的状态更改为`Relist in Progress`。 更改将使用您的下一个数据同步（如在cron设置中所配置）发布到Amazon。 如果尚未列出，则列表也会添加到_[!UICONTROL Overrides]_&#x200B;选项卡中。

正在附带&#x200B;_创建覆盖_&#x200B;示例。 以下示例显示对之前创建的覆盖的编辑，该编辑定义了新价格`$50`，删除了处理时间覆盖，并保留以前的条件和卖方备注覆盖。

![编辑或删除覆盖](assets/amazon-overrides-edit-2.png){width="600" zoomable="yes"}
__

## 编辑或删除多个列表的覆盖 {#edit-override-multiple-listings}

_[!UICONTROL Edit Listing Overrides]_操作在_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Overrides]_&#x200B;和&#x200B;_[!UICONTROL Ineligible]_选项卡上可用。

>[!NOTE]
>
>由于您正在修改多个列表的覆盖，因此在修改单个列表时，_[!UICONTROL Listing Details]_部分不会按原样显示。

1. 查看&#x200B;_[!UICONTROL Products Listings]_页面（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Overrides]_&#x200B;和&#x200B;_[!UICONTROL Ineligible]_选项卡）上的列表。

1. 选中要修改的每个列表左侧列中的复选框。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Edit Listing Overrides]**。

   将打开&#x200B;_[!UICONTROL Product Listing Overrides]_页面。

   ![选择Amazon列表覆盖](assets/amazon-actions-edit-listing-overrides.png){width="200"}

1. 要编辑&#x200B;_[!UICONTROL Override]_设置，请为要更改的类型（价格、处理时间、条件、卖方备注）定义部分。

   若要保持覆盖不变，请选择`No Change To <override type>`（默认）。 此设置使以前定义的覆盖值保持不变。

   - **价格** — 单击&#x200B;**[!UICONTROL Change Listing Price]**&#x200B;并输入您为&#x200B;**[!UICONTROL Price Override]**&#x200B;定义的价格值。
   - **处理时间** — 单击&#x200B;**[!UICONTROL Change Handling Time]**&#x200B;并输入&#x200B;**[!UICONTROL Handling Time Override]**&#x200B;的已定义时间值（以天为单位）。
   - **条件** — 单击&#x200B;**[!UICONTROL Change Condition]**&#x200B;并为&#x200B;**[!UICONTROL Condition Override]**&#x200B;选择正确的选项。
   - **卖方备注** — 单击&#x200B;**[!UICONTROL Change Seller Notes]**&#x200B;并输入&#x200B;**[!UICONTROL Seller Notes Override]**&#x200B;的备注文本。

1. 要删除覆盖类型，请为每个要删除的类型单击&#x200B;**[!UICONTROL Remove]**。 如果未删除，则先前定义的值将保留在覆盖中。

1. 单击&#x200B;**[!UICONTROL Save Listing Override]**。

   “_[!UICONTROL Product Listing Overrides]_”页面关闭。 清单的状态更改为`Relist in Progress`。 更改将使用您的下一个数据同步（如在cron设置中所配置）发布到Amazon。 如果尚未列出，则列表也会添加到_[!UICONTROL Overrides]_&#x200B;选项卡中。

### 覆盖类型

| 覆盖 | 描述 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Override] | 价格覆盖定义了列表的价格。 此覆盖优先于所有自动设置，直到覆盖被删除。<br><br>要覆盖产品的价格，请选择&#x200B;**[!UICONTROL Change Listing Price]**&#x200B;并输入&#x200B;**[!UICONTROL Price Override]**&#x200B;的新价格。 |
| [!UICONTROL Handling Time Override] | 处理时间覆盖定义处理和发运产品所需的时间（以天为单位）。 处理时间覆盖优先于所有自动和默认处理时间设置，直到覆盖被删除。<br><br>_[!UICONTROL Handling Time Override]_框中存在的值是您在[列表设置](./listing-settings.md)中定义的默认处理时间或您定义的覆盖处理时间。 如果删除了处理时间覆盖，则列表将默认为在列表设置中定义的处理时间。<br><br>要定义处理时间覆盖，请选择&#x200B;**[!UICONTROL Change Handling Time]**并输入&#x200B;**[!UICONTROL Handling Time Override]**的新处理时间（以天为单位）。 |
| [!UICONTROL Condition Override] | 要覆盖列表条件，请选择&#x200B;**[!UICONTROL Change Condition]**&#x200B;并从&#x200B;**条件覆盖**&#x200B;中选择新条件。 |
| [!UICONTROL Seller Notes Override] | 对于目录中使用`New`以外的条件定义的产品，可以添加卖家备注，向潜在购买者进一步详细说明您的产品及其条件。 您可以为`New`条件产品输入卖方备注覆盖，但Amazon不显示该备注。<br><br>要覆盖卖方备注，请选择&#x200B;**[!UICONTROL Change Seller Notes]**&#x200B;并输入&#x200B;**[!UICONTROL Seller Notes Override]**&#x200B;的新备注。 |
