---
title: Amazon sales channel — 价格规则条件
description: 使用价格规则条件来确定哪些产品符合上市价格规则的条件。
feature: Sales Channels, Price Rules
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# 价格规则条件

条件决定了哪些产品符合价格规则。 定义Amazon定价规则的条件遵循与定义条件相同的逻辑和流程。 [购物车价格规则](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) 在 [!DNL Commerce].

>[!IMPORTANT]
>
>如果您的价格规则适用于您购买的所有产品， [!DNL Commerce] 目录，然后将此部分留空。

在条件中以粗体显示的任何区域都可以单击来查看各种选项。

## 示例：构建价格规则条件

此过程可能简单也可能详细，具体取决于您的目录配置。 您可以定义条件，以便 `ALL` 或 `ANY` 条件之一为 `TRUE` 或 `FALSE` 对于产品，则该产品符合要应用的定价规则的条件。

条件基于 [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). 要将规则应用于所有产品，请将条件部分留空。

>[!NOTE]
>
>如果要基于特定产品属性定义条件， **用于促销规则条件** 属性的ID必须设置为 `Yes` 在您的 [店面属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) 属性的。

![价格规则条件 — 行1](assets/ob-price-rules-condition-1.png){width="600" zoomable="yes"}

此示例定义了一个规则，该规则对 `Books` 类别。

规则语句具有两个粗体链接，单击这两个链接时，将显示条件语句该部分的选项。 如果保存条件而不更改粗体选项，则该规则将应用于您的所有产品。

- 单击 **[!UICONTROL ALL]** 并选择 `ALL` 或 `ANY`.
- 单击 **[!UICONTROL TRUE]**，然后选择 `TRUE` 或 `FALSE`.
- 要将规则应用于所有产品，请保持条件不变。

您可以通过更改这些值的组合来创建不同的条件。 对于此示例，使用以下条件：

`If ALL of these conditions are TRUE:`

1. 要显示条件适用的可用属性，请单击添加(![“添加”图标](assets/btn-add-grn.png))图标，然后选择要作为条件基础的属性。

   **[!UICONTROL Conditions Combination]**  — 选择创建另一组 `All/Any` 和 `True/False` 现有条件中的条件。

   ![价格规则条件组合](assets/ob-conditions-combinations.png){width="500"}

   **[!UICONTROL Product Attribute]**  — 可用的产品属性取决于 [属性的设置](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html). 对于要在列表中显示的属性， *[!UICONTROL Use for Promo Rule Conditions]* 属性的ID必须设置为 `Yes` 在店面物业里。

   - 对象 **[!UICONTROL Product Attribute]**，选择要定义为条件基础的属性。 在本例中，选定的条件为 `Category`.

     ![价格规则条件 — 行2，第2部分](assets/ob-price-rule-condition-2.png){width="500"}

     选定的条件会显示在语句中，其后是两个粗体链接。 选项因您选择的产品属性而异。

     设置属性后，无法对其进行编辑。 要更改属性，必须删除该行并添加新属性。 您可以通过单击删除(![“删除”图标](assets/btn-del-red.png) 图标（位于行的末尾）。

   - 单击 **[!UICONTROL is]** 并选择描述产品要满足的条件的比较运算符。

     在本例中，比较运算符为 `is`. 可用选项取决于上一步骤中选择的属性，可能包括不同的比较选项。 选项可以包括匹配值，不包括或包括值、大于、等于和小于数值中的至少一个。 在此示例中，选项包括 `is` 和 `is not`.

   - 单击 **[!UICONTROL ...]** 并选择条件所依据的属性值。 选项取决于属性的设置。

     系统可能会提示您选择一个选项或输入条件的值。 对于此示例，字段显示为空白。 要为规则选择类别，请单击选择器图标(![“选择器”图标](assets/btn-chooser.png))，显示您的选择选项。 此规则用于 _书籍_，选择 **[!UICONTROL Books]** 复选框。 将填充类别编号。 要接受您的类别选择，请单击绿色复选标记图标(![复选标记图标](assets/btn-check-mark-green.png))。

     ![价格规则条件 — 行2，第3部分](assets/ob-price-rule-condition-3.png){width="500"}

     选定的项目会显示在语句中，以完成条件。

     ![价格规则条件 — 第2行，第4部分](assets/ob-price-rule-condition-4.png){width="500"}

     此示例条件已完成。 如前所述，此条件表示您的产品中 [!DNL Commerce] 已定义帐簿类别的目录(`4`)符合此定价规则的条件。 您可以添加更多条件行，以进一步缩小合格产品的范围。

1. 要向语句中添加其他条件行，请返回到步骤1并重复该过程，直到所有所需条件都完成。

   您可以随时通过单击删除(![“删除”图标](assets/btn-del-red.png))图标。
