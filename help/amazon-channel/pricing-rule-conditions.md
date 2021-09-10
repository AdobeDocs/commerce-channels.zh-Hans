---
title: 价格规则条件
description: 使用价格规则条件确定哪些产品符合上市价格规则的条件。
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html: 
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 757
ht-degree: 0%

---

# 价格规则条件

条件决定了哪些产品符合价格规则。 定义Amazon定价规则的条件遵循与在[!DNL Commerce]中定义[购物车价格规则](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){:target=&quot;_blank&quot;}的条件相同的逻辑和过程。

>[!IMPORTANT]
>
>如果您的价格规则适用于[!DNL Commerce]目录中的所有产品，请将此部分留空。

单击条件中任何以粗体显示的区域可查看各种选项。

## 示例：构建价格规则条件

此过程可以是简单的，也可以是详细的，具体取决于您的目录配置。 您可以定义条件，以便当`ALL`或`ANY`的条件`TRUE`或`FALSE`对应某个产品时，该产品符合要应用的定价规则的条件。

条件基于您的[产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}。 要将规则应用于所有产品，请将条件部分留空。

>[!NOTE]
>
>如果要根据特定产品属性定义条件，则必须在属性的[Storefront Properties](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}中将属性的&#x200B;**Use for Promo Rule Conditions**&#x200B;设置为`Yes`。

![价格规则条件 — 行1](assets/ob-price-rules-condition-1.png)

此示例定义了一个规则，该规则对`Books`类别中定义的所有产品都适用25%的折扣。

规则语句具有两个粗体链接，单击该链接后，将显示该条件语句部分的选项。 如果在保存条件时不更改粗体选项，则该规则将适用于您的所有产品。

- 单击&#x200B;**[!UICONTROL ALL]**&#x200B;并选择`ALL`或`ANY`。
- 单击&#x200B;**[!UICONTROL TRUE]**，然后选择`TRUE`或`FALSE`。
- 要将规则应用于所有产品，请保持条件不变。

您可以通过更改这些值的组合来创建不同的条件。 在本例中，使用了以下条件：

`If ALL of these conditions are TRUE:`

1. 要显示应用该条件的可用属性，请单击条件行开头的添加（![添加图标](assets/btn-add-grn.png)）图标，然后选择该条件所依据的属性。

   **[!UICONTROL Conditions Combination]**  — 选择在现有条件内 `All/Any` 创建 `True/False` 另一组和条件。

   ![价格规则条件组合](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]**  — 可用的产品属性取决于 [属性](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}的设置。要在列表中显示某个属性，必须在[storefront属性](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}中将该属性的&#x200B;*[!UICONTROL Use for Promo Rule Conditions]*&#x200B;设置为`Yes`。

   - 对于&#x200B;**[!UICONTROL Product Attribute]**，选择要定义为条件基的属性。 在本例中，所选条件为`Category`。

      ![价格规则条件 — 第2行，第2部分](assets/ob-price-rule-condition-2.png)

      所选条件显示在语句中，然后再显示两个粗体链接。 选项会因您选择的产品属性而异。

      设置属性后，无法对其进行编辑。 要更改属性，必须删除行并添加新属性。 可以通过单击条件行末尾的删除（![删除图标](assets/btn-del-red.png)图标）来删除条件行。

   - 单击&#x200B;**[!UICONTROL is]**&#x200B;并选择描述产品满足条件的比较运算符。

      对于此示例，比较运算符为`is`。 可用选项取决于在上一步中选择的属性，并可能包含不同的比较选项。 选项可以包括匹配值，不包括或包括值中的至少一个，以及大于、等于和小于数值。 在此示例中，选项为`is`和`is not`。

   - 单击&#x200B;**[!UICONTROL ...]**&#x200B;并选择条件所基于的属性值。 选项取决于属性的设置。

      系统可能会提示您选择一个选项或为条件输入一个值。 在本例中，该字段显示为空。 要为规则选择类别，请单击选择器图标（![选择器图标](assets/btn-chooser.png)）以显示选择选项。 此规则适用于&#x200B;_Books_，选中&#x200B;**[!UICONTROL Books]**&#x200B;复选框。 类别数字中填充。 要接受类别选择，请单击绿色复选标记图标（![复选标记图标](assets/btn-check-mark-green.png)）。

      ![价格规则条件 — 第2行，第3部分](assets/ob-price-rule-condition-3.png)

      所选项目将显示在语句中以完成条件。

      ![价格规则条件 — 第2行，第4部分](assets/ob-price-rule-condition-4.png)

      此示例条件已完成。 如上所述，此条件表示[!DNL Commerce]目录中任何具有已定义“Book”类别(`4`)的产品均符合此定价规则。 您可以添加更多条件行以进一步缩小符合条件的产品范围。

1. 要向语句中添加其他条件行，请返回到步骤1并重复该过程，直到所有所需条件都完成。

   您可以随时通过单击行末尾的删除（![删除图标](assets/btn-del-red.png)）图标来删除条件语句的行。
