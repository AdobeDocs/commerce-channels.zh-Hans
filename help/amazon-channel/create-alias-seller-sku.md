---
title: 创建别名Amazon销售商SKU
description: 您可以使用Alias Amazon销售方SKU从Commerce目录产品创建多区域Amazon列表。
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# 创建别名Amazon销售商SKU

An [!DNL Alias Amazon Seller SKU] 用于通过中的相同产品创建Amazon列表 [!DNL Commerce] 目录。 如果您是有经验的Amazon销售人员，则可能熟悉 [Amazon全球SKU](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} 以及特定于市场的SKU，用于库存和配送。 遵循Amazon销售渠道的类似原则，Amazon销售方SKU控制多区域级别的产品列表信息，并且 [!DNL Alias Amazon Seller SKU] 可用于控制区域特定级别的产品列表信息。

此函数可用于执行两个函数：

- 创建 [!DNL Alias Amazon Seller SKU] 对于您的其中一个 [!DNL Commerce] 目录产品，以控制特定于区域的列表信息。

   **示例**：您在美国和加拿大都是卖家。 请记住，在设置期间，只能为每个Amazon销售渠道商店分配一个Amazon区域。 因此，您有一家Amazon销售渠道商店，它有一个定义的美国地区，还有一家定义加拿大地区的商店。 两个商店共享您的 [!DNL Commerce] 用于跨区域列出信息(包括Amazon销售方SKU和ASIN产品属性)的目录。 因此，目录产品的清单在两个商店中是相同的，可共享定价、库存/数量和其他产品属性。 但是，您的加拿大商店库存来自加拿大位置，而您的美国商店库存来自美国位置。 因此，您应该单独控制每个商店的清单数量。 要完成此类特定于区域的控制，您可以创建Alias Amazon销售方SKU。

   基本上，您可以创建一个Amazon销售者SKU，该SKU链接到相同的目录产品，并可用于在该区域重新发布相同的列表。

- 创建 [!DNL Alias Amazon Seller SKU] 并匹配您的其中一个 [!DNL Commerce] 将产品编录到两个Amazon列表。

   **示例**：您有一个与Amazon列表匹配的目录产品。 由于Amazon通常有多个代表同一产品的列表，因此您会发现同一产品的另一个Amazon列表，但Amazon已为该列表分配了另一个ASIN。 要增加要包括的产品可见性，您需要将目录产品与不同的ASIN匹配，并为两个ASIN值创建列表。 要完成此操作，您可以创建Amazon销售人员SKU别名。

   基本上，您可以创建 [!DNL Alias Amazon Seller SKU] 可将单个目录产品与第二个Amazon列表进行匹配，并为新匹配的ASIN创建列表。 在此方案中，您将拥有同一目录产品的两个Amazon列表。

   创建别名Amazon销售商SKU后，您可以使用列表设置、规则和覆盖来控制该区域的列表信息。 可以为列表按区域定义的产品属性包括数量/库存、履行方法、条件、产品资格和处理时间。

## 用于特定于区域的目的 {#region-specific}

查看 _[!UICONTROL Product Listings]_页面(_[!UICONTROL Inactive]_， _活动_， _不合格_，或 _已结束_ 选项卡)。

1. 下 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Create Alias Seller SKU]**.

1. 对象 **[!UICONTROL Assign New Seller SKU]**，请输入一个唯一的字母数字值。

   此值必须是唯一的（不适用于目录中的任何其他产品或别名）。

1. 对象 **[!UICONTROL Assign New ASIN]**，不做更改。

   此值将自动填充与您的目录产品匹配的产品ASIN。 更改此值会根据ASIN将您的目录产品与两个Amazon列表相匹配。

1. 切换 **[!UICONTROL Remove Existing Seller SKU]** 选项。

   - `Yes`  — 选择删除列表并使用提供的新信息创建列表。

   - `No`  — 选择创建列表并保持旧列表不变。

1. 单击 **[!UICONTROL Save Listing Update]**.

## 用于将一个目录产品与两个Amazon列表进行匹配

1. 查看 _[!UICONTROL Product Listings]_页面(_[!UICONTROL Inactive]_， _[!UICONTROL Active]_，_[!UICONTROL Ineligible]_，或 _[!UICONTROL Ended]_选项卡)。

1. 下 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Create Alias Seller SKU]**.

1. 对象 **[!UICONTROL Assign New Seller SKU]**，请输入一个唯一的字母数字值。

   此值必须是唯一的（不适用于目录中的任何其他产品或别名）。

1. 对象 **[!UICONTROL Assign New ASIN]**，请输入一个唯一的字母数字值。

   此值将自动填充与您的目录产品匹配的产品ASIN。 更改此值会根据ASIN将您的目录产品与两个Amazon列表相匹配。

1. 切换 **[!UICONTROL Remove Existing Seller SKU]** 选项。

   - `Yes`  — 选择删除列表并使用提供的新信息创建列表。

   - `No`  — 选择创建其他列表并保持旧列表不变。

1. 单击 **[!UICONTROL Save Listing Update]**.

![创建别名Amazon销售商SKU](assets/amazon-alias-sku-create.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | 输入要链接到原始Amazon卖方SKU的新的唯一字母数字值。 此数字仅供Amazon销售渠道用于匹配您的目录产品。 您可以使用任何SKU值，但此值只能在目录中使用一次。 |
| [!UICONTROL Assign New ASIN] | 为要与目录产品匹配的列表输入ASIN值。 仅当将单个目录产品与ASIN匹配以便同一产品的另一个列表时，才修改此字段。 此值必须与Amazon分配的ASIN匹配，否则Amazon不会拒绝此列表。 |
| [!UICONTROL Remove Existing Seller SKU] | 选项：<ul><li>**[!UICONTROL Yes]**  — 选择删除列表并使用提供的新信息创建列表。 新列表将显示在 _[!UICONTROL Active]_选项卡，旧列表移至_&#x200B;已结束&#x200B;_选项卡。</li><li>**[!UICONTROL No]**  — 选择创建其他列表并保持旧列表不变。 创建新列表后，两个列表都会显示在“活动”选项卡中。</li></ul> |
