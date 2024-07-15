---
title: 创建别名Amazon销售商SKU
description: 您可以使用别名Amazon销售商SKU从Commerce目录产品创建多区域Amazon列表。
feature: Sales Channels, Products
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# 创建别名Amazon销售商SKU

[!DNL Alias Amazon Seller SKU]用于从您的[!DNL Commerce]目录中的同一产品创建Amazon列表。 如果您是有经验的Amazon销售商，则可能熟悉[Amazon全球SKU](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"}以及特定于市场的SKU，以便进行库存和发运。 按照Amazon销售渠道的类似原则，Amazon销售者SKU可以在多区域级别控制产品列表信息，并且[!DNL Alias Amazon Seller SKU]可用于在特定区域级别控制产品列表信息。

此函数可用于执行两个函数：

- 为您的[!DNL Commerce]目录产品之一创建[!DNL Alias Amazon Seller SKU]以控制特定于区域的列表信息。

  **示例**：您同时是美国和加拿大地区的销售商。 请记住，在设置过程中，只能为每个Amazon销售渠道商店分配一个Amazon区域。 Amazon因此，您有一个销售渠道商店，它有一个定义的美国地区；另一个商店，它有一个定义加拿大地区。 两个商店都共享您的[!DNL Commerce]目录，以便在两个区域之间列出信息，包括Amazon销售方SKU和ASIN产品属性。 因此，目录产品的清单在两个商店中都将是相同的，即共享定价、库存/数量和其他产品属性。 但是，您的加拿大商店库存来自加拿大位置，而您的美国商店库存来自美国位置。 因此，您应该单独控制每个商店的清单数量。 要实现此类特定于区域的控制，您可以创建Alias Amazon销售方SKU。

  基本上，您可以创建一个别名Amazon销售商SKU，该SKU链接到相同的目录产品，并可用于在该区域重新发布相同的列表。

- 创建一个[!DNL Alias Amazon Seller SKU]并将您的[!DNL Commerce]目录产品之一与两个Amazon列表相匹配。

  **示例**：您有一个与Amazon列表匹配的目录产品。 由于Amazon经常有多个代表同一产品的列表，因此您会发现同一产品的其他Amazon列表，但Amazon已为该列表分配了不同的ASIN。 要增加要包括的产品可见性，您需要将目录产品与不同的ASIN相匹配，并为两个ASIN值创建列表。 要完成此操作，您可以创建别名Amazon销售商SKU。

  基本上，您可以创建可用于将单个目录产品与第二个Amazon列表匹配的[!DNL Alias Amazon Seller SKU]，并为新匹配的ASIN创建列表。 在此方案中，您将拥有同一目录产品的两个Amazon列表。

  创建别名Amazon销售商SKU后，您可以使用列表设置、规则和覆盖来控制该区域的列表信息。 可以为列表按区域定义的产品属性包括数量/库存、履行方法、条件、产品资格和处理时间。

## 用于区域特定的目的 {#region-specific}

查看&#x200B;_[!UICONTROL Product Listings]_页面上的列表（_[!UICONTROL Inactive]_、_活动_、_不合格_&#x200B;或&#x200B;_已结束_&#x200B;选项卡）。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Create Alias Seller SKU]**。

1. 对于&#x200B;**[!UICONTROL Assign New Seller SKU]**，请输入唯一的字母数字值。

   此值必须是唯一的（不适用于目录中的任何其他产品或别名）。

1. 对于&#x200B;**[!UICONTROL Assign New ASIN]**，不做任何更改。

   此值将自动填充与您的目录产品匹配的产品ASIN。 更改此值会根据ASIN将您的目录产品与两个Amazon列表相匹配。

1. 根据需要切换&#x200B;**[!UICONTROL Remove Existing Seller SKU]**&#x200B;选项。

   - `Yes` — 选择删除列表并使用提供的新信息创建列表。

   - `No` — 选择创建列表并保持旧列表不变。

1. 单击&#x200B;**[!UICONTROL Save Listing Update]**。

## 用于将一个目录产品与两个Amazon列表进行匹配

1. 查看&#x200B;_[!UICONTROL Product Listings]_页面（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Ineligible]_&#x200B;或&#x200B;_[!UICONTROL Ended]_选项卡）上的列表。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Create Alias Seller SKU]**。

1. 对于&#x200B;**[!UICONTROL Assign New Seller SKU]**，请输入唯一的字母数字值。

   此值必须是唯一的（不适用于目录中的任何其他产品或别名）。

1. 对于&#x200B;**[!UICONTROL Assign New ASIN]**，请输入唯一的字母数字值。

   此值将自动填充与您的目录产品匹配的产品ASIN。 更改此值会根据ASIN将您的目录产品与两个Amazon列表相匹配。

1. 根据需要切换&#x200B;**[!UICONTROL Remove Existing Seller SKU]**&#x200B;选项。

   - `Yes` — 选择删除列表并使用提供的新信息创建列表。

   - `No` — 选择创建另一个列表并保持旧列表不变。

1. 单击&#x200B;**[!UICONTROL Save Listing Update]**。

![创建别名Amazon销售商SKU](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Assign New Seller SKU] | 输入要链接到原始Amazon销售商SKU的新的唯一字母数字值。 此号码仅供Amazon销售渠道用于匹配您的目录产品。 您可以使用任何SKU值，但此值在目录中只能使用一次。 |
| [!UICONTROL Assign New ASIN] | 输入要与目录产品匹配的列表的ASIN值。 仅当将单个目录产品与ASIN匹配以便同一产品的另一个列表时，才修改此字段。 此值必须与Amazon分配的ASIN匹配，否则Amazon不会拒绝此列表。 |
| [!UICONTROL Remove Existing Seller SKU] | 选项：<ul><li>**[!UICONTROL Yes]** — 选择删除列表并使用提供的新信息创建列表。 新列表出现在&#x200B;_[!UICONTROL Active]_选项卡中，而旧列表移至_&#x200B;已结束&#x200B;_选项卡。</li><li>**[!UICONTROL No]** — 选择创建另一个列表并保持旧列表不变。 创建新列表后，两个列表都会显示在“活动”选项卡中。</li></ul> |
