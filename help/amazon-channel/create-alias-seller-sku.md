---
title: 创建别名Amazon销售商SKU
description: 您可以使用别名Amazon销售商SKU，从您的商务目录产品中创建多区域Amazon列表。
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# 创建别名Amazon销售商SKU

[!DNL Alias Amazon Seller SKU]用于根据[!DNL Commerce]目录中的相同产品创建Amazon列表。 如果您是经验丰富的Amazon销售商，则可能熟悉[Amazon全局SKU](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target=&quot;_blank&quot;}和特定于市场的SKU，以用于库存和运输。 按照Amazon销售渠道的类似原则，Amazon销售商SKU会在多区域级别控制产品列表信息，并且[!DNL Alias Amazon Seller SKU]可用于在特定区域级别控制产品列表信息。

此函数可用于执行两项功能：

- 为某个[!DNL Commerce]目录产品创建[!DNL Alias Amazon Seller SKU] ，以控制特定于区域的列表信息。

   **示例**:您是美国和加拿大地区的卖家。请记住，您的每个Amazon销售渠道商店在设置过程中只能分配一个Amazon地区。 因此，您有一家Amazon销售渠道商店，其中规定了美国地区，另一家商店则规定了加拿大地区。 这两家商店共享您的[!DNL Commerce]目录，以便在两个地区(包括Amazon销售商SKU和ASIN产品属性)中列出信息。 因此，目录产品在两个商店中的列表将相同，共享定价、库存/数量和其他产品属性。 但是，您在加拿大的库存来自加拿大，您在美国的库存来自美国。 因此，您应该单独控制每个商店的列表数量。 要完成此类特定于区域的控制，您可以创建别名Amazon销售商SKU。

   实际上，您可以创建一个别名Amazon销售商SKU，该SKU链接到同一目录产品，并可用于重新发布该区域中的同一列表。

- 创建一个[!DNL Alias Amazon Seller SKU]，并将其中一个[!DNL Commerce]目录产品与两个Amazon列表进行匹配。

   **示例**:您有一个与Amazon列表匹配的目录产品。由于Amazon经常有多个表示同一产品的列表，因此您会发现同一产品的Amazon另一个列表，但Amazon已为该列表分配了不同的ASIN。 要提高产品可见性以包含在内，您需要将目录产品与不同的ASIN匹配，并为这两个ASIN值创建列表。 要实现此目的，您可以创建别名Amazon销售商SKU。

   实际上，您可以创建一个[!DNL Alias Amazon Seller SKU]，用于将单个目录产品与第二个Amazon列表进行匹配，并为新匹配的ASIN创建列表。 在此方案中，您将拥有同一目录产品的两个Amazon列表。

   创建别名Amazon销售商SKU后，您可以使用列表设置、规则和覆盖来控制区域的列表信息。 可以按区域为列表定义的产品属性包括数量/库存、履行方法、条件、产品资格和处理时间。

## 用于特定于区域的目的 {#region-specific}

查看&#x200B;_[!UICONTROL Product Listings]_页面（_[!UICONTROL Inactive]_、_活动_、_不合格_&#x200B;或&#x200B;_已结束_&#x200B;选项卡）上的列表。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Create Alias Seller SKU]**。

1. 对于&#x200B;**[!UICONTROL Assign New Seller SKU]**，输入唯一的字母数字值。

   此值必须唯一（不用于目录中的任何其他产品或别名）。

1. 对于&#x200B;**[!UICONTROL Assign New ASIN]**，不进行任何更改。

   此值会自动填充与您的目录产品匹配的产品ASIN。 根据ASIN将此值更改为将您的目录产品匹配到两个Amazon列表。

1. 根据需要切换&#x200B;**[!UICONTROL Remove Existing Seller SKU]**&#x200B;选项。

   - `Yes`  — 选择删除列表，然后使用提供的新信息创建列表。

   - `No`  — 选择创建列表并保持旧列表不变。

1. 单击&#x200B;**[!UICONTROL Save Listing Update]**。

## 用于将单个目录产品与两个Amazon列表进行匹配

1. 查看&#x200B;_[!UICONTROL Product Listings]_页面（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Ineligible]_&#x200B;或&#x200B;_[!UICONTROL Ended]_选项卡）上的列表。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Create Alias Seller SKU]**。

1. 对于&#x200B;**[!UICONTROL Assign New Seller SKU]**，输入唯一的字母数字值。

   此值必须唯一（不用于目录中的任何其他产品或别名）。

1. 对于&#x200B;**[!UICONTROL Assign New ASIN]**，输入唯一的字母数字值。

   此值会自动填充与您的目录产品匹配的产品ASIN。 根据ASIN将此值更改为将您的目录产品匹配到两个Amazon列表。

1. 根据需要切换&#x200B;**[!UICONTROL Remove Existing Seller SKU]**&#x200B;选项。

   - `Yes`  — 选择删除列表，然后使用提供的新信息创建列表。

   - `No`  — 选择创建另一个列表，并保持旧列表不变。

1. 单击&#x200B;**[!UICONTROL Save Listing Update]**。

![创建别名Amazon销售商SKU](assets/amazon-alias-sku-create.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | 输入要链接到原始Amazon销售商SKU的新的唯一字母数字值。 此数字仅由Amazon销售渠道用来与您的目录产品匹配。 您可以使用任何SKU值，但该值在您的目录中只能使用一次。 |
| [!UICONTROL Assign New ASIN] | 输入与目录产品匹配的列表的ASIN值。 仅当将单个目录产品与ASIN匹配以供同一产品的另一个列表时，才修改此字段。 此值必须匹配Amazon分配的ASIN，否则列表将不会被Amazon拒绝。 |
| [!UICONTROL Remove Existing Seller SKU] | 选项：<ul><li>**[!UICONTROL Yes]**  — 选择删除列表，然后使用提供的新信息创建列表。新列表显示在&#x200B;_[!UICONTROL Active]_选项卡中，并且旧列表移至_ Ended _选项卡。</li><li>**[!UICONTROL No]**  — 选择创建另一个列表，并保持旧列表不变。创建新列表后，这两个列表都会显示在“活动”选项卡中。</li></ul> |
