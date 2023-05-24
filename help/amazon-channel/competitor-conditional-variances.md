---
title: '智能重新定价规则：竞争对手条件差异'
description: 通过创建智能重新定价规则，根据竞争对手的定价和产品的条件确定您的Amazon上市价格。
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 智能重新定价规则：竞争对手条件差异

智能重新定价规则的部分包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

智能重新定价规则使用Amazon竞争对手的定价来确定您的上市价格。 竞争对手是其他销售商，它们列出的产品与您在Amazon上列出的产品相同。

如果存在具有相同条件的产品，则基本匹配价格为 [最低竞争对手](./lowest-competitor-pricing.md) 相同条件的价格。 如果没有与您的条件相匹配的竞争对手产品，则基本匹配价会经过其它可用的竞争对手条件，从新增、翻新开始，然后继续通过可用条件计算。 找到条件后，基本匹配价格将是该条件中的最低价格。

如果您有一个产品列出条件 `Used; Good` 基本匹配价，竞争对手以较低的价格在相同的条件下拥有相同的产品，则使用竞争对手的价格。 如果不存在具有相同条件的竞争对手，则系统会检查是否存在具有下一个条件的竞争对手，即 `New`. 如果找到满足该条件的竞争对手，则使用最低价格。

## 配置竞争对手条件差异

在中定义条件差异 _[!UICONTROL Competitor Conditional Variances]_部分。

对象 **[!UICONTROL Conditional Variance]**，选择一个选项：

- `Use all competitor's product conditions`  — （默认）选择要将产品与任何可用条件进行比较的时间（如果列出的条件不存在匹配项）。

- `Use Only Matching Competitor's Product Condition`  — 选择何时希望您的产品仅与相同条件下的竞争对手产品进行比较。 如果不存在匹配项，则产品定价为 _Magento价格来源_ 在中定义 [挂牌价](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)`  — 选择以首先尝试与匹配的产品条件进行比较。 如果不存在匹配条件，则会应用相对于您的产品条件和最低竞争对手条件的方差（以百分比表示）。

   当 _[!UICONTROL Apply Variance]_选择功能，则为每个Amazon条件显示其他方差字段。 通过此功能，您可以在提供与竞争对手处于不同状态的产品时使用智能的重新定价规则。 要了解条件差异背后的计算，您必须首先了解所有差异都是根据基本匹配价格确定的。

   显示的条件差异选项基于您的列表设置 `Condition` 映射到条件值的属性 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. 对于所有映射的条件，您可以定义差异百分比1-100。 可收集项目则属于例外，在这种情况下，可应用大于100的百分比。

![智能重新定价规则 — 竞争对手条件差异](assets/amazon-competitor-cond-variances.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | 选项： <ul><li>**[!UICONTROL Use all competitor's product conditions]**  — 如果用于列出产品的条件不存在匹配项，则此选项将针对任何可用条件进行匹配。 它首先尝试匹配您的条件，然后通过 `New` 完成情况 `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]**  — 此选项与产品的条件匹配。 如果不存在匹配项，则产品价格为 _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]**  — 此选项首先会尝试根据产品条件进行匹配。 如果不存在匹配条件，则会应用相对于您的产品条件和最低竞争对手条件的方差（以百分比表示）。</li></ul><br><br>根据您为条件列出的设置显示的条件差异选项，这些条件使用映射到条件值 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. 对于所有映射的条件，可以表示差异百分比1-100。 可收集项目则属于例外，在这种情况下，可应用大于100的百分比。<br><br>通过此功能，您可以在提供与竞争对手处于不同状态的产品时使用智能的重新定价规则。 要了解条件差异背后的计算，您必须首先了解所有差异都是根据基本匹配价格确定的。 |

## 计算条件方差基数

- 基本匹配条件差异(BMC) =基本匹配价格竞争对手条件的差异。 使用前面的示例，BMC是 `New` 条件。
- 商家条件差异(MCV) =产品条件的差异。 使用前面的示例，MCV =的方差 `Used; Good` 条件。
- 基本匹配价(BMP) = $7.99（如上所述）

条件方差基数的计算公式如下：

![条件方差基计算公式](assets/amazon-cond-variance-calc-1.png)

## 示例

条件方差设置如下：

![条件方差设置示例](assets/amazon-cond-variances.png)

- BMC = 100（竞争者条件=新建）
- MCV = 80（商家条件=已使用；良好）
- BMP = $7.99 （基本匹配价=匹配竞争对手条件的最低价格）

![条件方差基计算示例](assets/amazon-cond-variance-calc-2.png)

使用上面的条件差异基数计算，条件差异基数= $6.39。此计算方式是用于价格规则操作的竞争对手价格来源，详见 [价格调整](./price-adjustment.md).
