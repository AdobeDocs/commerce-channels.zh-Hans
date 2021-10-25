---
title: “示例：定义条件”
description: 创建上市规则时，应定义条件以标识要在Amazon Marketplace中列出的商务目录产品。
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 示例：定义条件

## 条件

单击条件中任何以粗体显示的区域可查看各种选项。

**如果选定网站中的所有产品均符合条件，请勿添加条件。**

>[!NOTE]
>
>有一组复杂的后端进程可直接与Amazon的系统通信。 根据您尝试列出的项目数以及Amazon系统可能有多忙（例如“黑色星期五”），您的项目可能需要一些时间才能在Amazon上列出。

请参阅 [创建购物车价格规则](https://docs.magento.com/user-guide/marketing/price-rules-catalog-create.html){target=&quot;_blank&quot;}。

## 定义条件

此过程可以是简单的，也可以是详细的，具体取决于您的目录设置。 您可以设置条件，以便在 `ALL` 或 `ANY` 定义条件的 `TRUE` 或 `FALSE` 对于产品，该产品有资格在Amazon上列出。

条件基于现有产品属性值。 要将规则应用于所有产品，请将条件部分留空。

>[!NOTE]
>
>如果要根据特定产品属性定义条件，请将 **[!UICONTROL Use for Promo Rule Conditions]** 将属性设置为 `Yes`. 您可以在 [店面属性](https://docs.magento.com/user-guide/catalog/product-attributes-add.html)属性的{target=&quot;_blank&quot;}页。

![条件 — 第1行](assets/ob-listing-rule-conditions-start.png)

此示例中的规则定义了一个规则，用于设置具有 _AmazonFBA_ 属性设置为 `Yes`.

规则语句具有两个粗体链接，单击该链接时，将显示该语句部分的选项。 如果在保存条件时不更改粗体选项，则该规则适用于您的所有产品。

- 单击 **[!UICONTROL ALL]** 选择 `ALL` 或 `ANY`.
- 单击 **[!UICONTROL TRUE]** 选择 `TRUE` 或 `FALSE`.
- 要将规则应用于所有产品，请保持条件不变。

您可以通过更改这些值的组合来创建不同的条件。 在本例中，使用了以下条件：

`If ALL of these conditions are TRUE:`

1. 单击添加(![“添加”图标](assets/btn-add-grn.png))图标，并选择要作为条件基础的属性，如条件组合或产品属性。

   - **[!UICONTROL Conditions Combination]**  — 选择允许您创建另一组 `All/Any` 和 `True/False` 条件。

      ![条件组合](assets/ob-conditions-combinations.png)

   - **[!UICONTROL Product Attribute]**  — 产品属性取决于属性的设置。 要使某个属性显示在列表中，必须将其配置为在促销规则条件中使用。 请参阅 _用于促销规则条件_ in [产品属性](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}。

      在 **[!UICONTROL Product Attribute]**，选择要用作条件基础的属性。 在本例中，所选条件为 `Amazon FBA`.

      ![条件行2，第2部分](assets/ob-condition-attribute-dropdown.png)

      所选条件显示在语句中，然后再显示两个粗体链接。 选项会因您选择的产品属性而异。

      设置属性后，便无法更改该属性。 要更改属性，必须删除行并添加新属性。 您可以通过单击删除(![“删除”图标](assets/btn-del-red.png))图标。

      1. 单击 **[!UICONTROL is]** 并选择描述产品满足条件的比较运算符。

         对于此示例，比较运算符为 `is`. 可用选项取决于在上一步中选择的属性。 选项可以包括不同的比较选项，如匹配值，不包括或包括值中的至少一个值，以及大于、等于和小于数值。 在本例中，选项包括 `is` 和 `is not`.

      1. 单击 **[!UICONTROL ...]** 并选择条件所基于的属性值。

         选项取决于属性的设置。 系统可能会提示您选择一个选项，或输入条件的文本或数值。 在本例中，选择 `Yes`.

         所选项目将显示在语句中以完成条件。

         ![条件行2，第3部分](assets/ob-listing-rule-condition-is.png)
   此条件已完成。 如上所述，此条件表示 [!DNL Commerce] 将Amazon FBA属性设置为值的目录 `Yes` 有资格在Amazon地区和商店上市。 您可以添加更多条件行以进一步缩小符合条件的产品范围。

1，要向语句中添加另一个条件行，请返回到步骤1并重复该过程，直到所有所需条件都完成。

您可以随时通过单击删除(![“删除”图标](assets/btn-del-red.png))图标。
