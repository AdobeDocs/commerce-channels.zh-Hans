---
title: 价格规则条件
description: 使用价格规则条件确定哪些产品符合上市价格规则的条件。
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# 价格规则条件

条件决定了哪些产品符合价格规则。 定义Amazon定价规则的条件与定义 [购物车价格规则](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}(位于 [!DNL Commerce].

>[!IMPORTANT]
>
>如果您的价格规则适用于 [!DNL Commerce] 目录，然后将此部分留空。

单击条件中任何以粗体显示的区域可查看各种选项。

## 示例：构建价格规则条件

此过程可以是简单的，也可以是详细的，具体取决于您的目录配置。 您可以定义条件，以便在 `ALL` 或 `ANY` 条件为 `TRUE` 或 `FALSE` 对于产品，产品符合要应用的定价规则。

条件基于 [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}。 要将规则应用于所有产品，请将条件部分留空。

>[!NOTE]
>
>如果要根据特定产品属性定义条件， **用于促销规则条件** ，因为属性必须设置为 `Yes` 在 [店面属性](https://docs.magento.com/user-guide/stores/attribute-product-create.html)属性的{target=&quot;_blank&quot;}。

![价格规则条件 — 行1](assets/ob-price-rules-condition-1.png)

此示例定义了一个规则，该规则会将25%的折扣应用于 `Books` 类别。

规则语句具有两个粗体链接，单击该链接后，将显示该条件语句部分的选项。 如果在保存条件时不更改粗体选项，则该规则将适用于您的所有产品。

- 单击 **[!UICONTROL ALL]** 选择 `ALL` 或 `ANY`.
- 单击 **[!UICONTROL TRUE]**，然后选择 `TRUE` 或 `FALSE`.
- 要将规则应用于所有产品，请保持条件不变。

您可以通过更改这些值的组合来创建不同的条件。 在本例中，使用了以下条件：

`If ALL of these conditions are TRUE:`

1. 要显示适用该条件的可用属性，请单击添加(![“添加”图标](assets/btn-add-grn.png))图标，然后选择要作为条件基础的属性。

   **[!UICONTROL Conditions Combination]**  — 选择创建另一组 `All/Any` 和 `True/False` 条件。

   ![价格规则条件组合](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]**  — 可用的产品属性取决于 [属性的设置](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target=&quot;_blank&quot;}。 要在列表中显示属性， *[!UICONTROL Use for Promo Rule Conditions]* ，因为属性必须设置为 `Yes` 在 [店面属性](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target=&quot;_blank&quot;}。

   - 对于 **[!UICONTROL Product Attribute]**，选择要定义为条件基础的属性。 在本例中，所选条件为 `Category`.

      ![价格规则条件 — 第2行，第2部分](assets/ob-price-rule-condition-2.png)

      所选条件显示在语句中，然后再显示两个粗体链接。 选项会因您选择的产品属性而异。

      设置属性后，无法对其进行编辑。 要更改属性，必须删除行并添加新属性。 您可以通过单击删除(![“删除”图标](assets/btn-del-red.png) 图标。

   - 单击 **[!UICONTROL is]** 并选择描述产品满足条件的比较运算符。

      对于此示例，比较运算符为 `is`. 可用选项取决于在上一步中选择的属性，并可能包含不同的比较选项。 选项可以包括匹配值，不包括或包括值中的至少一个，以及大于、等于和小于数值。 在本例中，选项包括 `is` 和 `is not`.

   - 单击 **[!UICONTROL ...]** 并选择条件所基于的属性值。 选项取决于属性的设置。

      系统可能会提示您选择一个选项或为条件输入一个值。 在本例中，该字段显示为空。 要为规则选择类别，请单击选择器图标(![选择器图标](assets/btn-chooser.png))以显示选择选项。 此规则适用于 _书籍_，选择 **[!UICONTROL Books]** 复选框。 类别数字中填充。 要接受类别选择，请单击绿色复选标记图标(![复选标记图标](assets/btn-check-mark-green.png))。

      ![价格规则条件 — 第2行，第3部分](assets/ob-price-rule-condition-3.png)

      所选项目将显示在语句中以完成条件。

      ![价格规则条件 — 第2行，第4部分](assets/ob-price-rule-condition-4.png)

      此示例条件已完成。 如上所述，此条件表示 [!DNL Commerce] 具有已定义的书籍类别(`4`)符合此定价规则的条件。 您可以添加更多条件行以进一步缩小符合条件的产品范围。

1. 要向语句中添加其他条件行，请返回到步骤1并重复该过程，直到所有所需条件都完成。

   您可以随时通过单击删除(![“删除”图标](assets/btn-del-red.png))图标。
