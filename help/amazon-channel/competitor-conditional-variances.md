---
title: “智能重定价规则：竞争者条件差异”
description: 通过创建智能的重新定价规则，根据竞争者定价和产品状况确定Amazon的上市价格。
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# 智能重定价规则：竞争者条件差异

智能重定价规则的部分包括：

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

智能的重新定价规则使用Amazon竞争者的定价来确定您的上市价格。 竞争对手是列出您在Amazon上列出的相同产品的其他销售商。

如果产品存在具有相同条件的，则基本匹配价格为具有相同条件的[最低竞争者](./lowest-competitor-pricing.md)价格。 如果没有竞争者产品与您的条件匹配，则基本匹配价格随后将通过其他可用竞争者条件（从“新建”、“翻新”开始，然后继续通过可用条件）。 在找到条件后，基本匹配价格将是该条件内的最低价格。

如果您的产品列出了条件`Used; Good`且基本匹配价格，而竞争对手在相同条件下以较低价格获得相同产品，则使用竞争者价格。 如果竞争者不存在具有相同条件的竞争者，则系统将检查下一个条件为`New`的竞争者。 如果找到具有该条件的竞争者，则使用最低价格。

## 配置竞争者条件差异

在&#x200B;_[!UICONTROL Competitor Conditional Variances]_部分中定义条件差异。

对于&#x200B;**[!UICONTROL Conditional Variance]**，选择一个选项：

- `Use all competitor's product conditions`  — （默认）选择您希望产品何时与任何可用条件进行比较（如果所列条件不存在匹配项）。

- `Use Only Matching Competitor's Product Condition`  — 选择您希望产品在同一条件下仅与竞争对手的产品进行比较的时间。如果不存在匹配项，则产品的定价将采用[Listing Price](./listing-price.md)中定义的&#x200B;_Magento价格来源_。

- `Apply Variance (if competitor's product condition differs)`  — 选择首先尝试根据匹配的产品条件进行比较。如果不存在匹配条件，则会对产品条件和最低竞争者的条件应用差异（以百分比表示）。

   选择&#x200B;_[!UICONTROL Apply Variance]_功能后，将为您的每个Amazon条件显示其他差异字段。 当您提供的产品与竞争对手的情况不同时，此功能允许您使用智能重定价规则。 要了解条件差异背后的计算，您必须首先了解所有差异都由基本匹配价格确定。

   显示的条件差异选项基于您的`Condition`列表设置，这些设置使用[!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}映射到条件值。 对于所有映射的条件，您可以定义1-100的方差百分比。 例外是可收集的，在这种情况下，可应用大于100的百分比。

![智能重定价规则 — 竞争者条件差异](assets/amazon-competitor-cond-variances.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | 选项： <ul><li>**[!UICONTROL Use all competitor's product conditions]**  — 如果将产品列在的条件不存在匹配项，则此选项与任何可用条件均匹配。它首先尝试匹配您的条件，然后按照从`New`条件到`Used; Acceptable`的方式工作。</li><li>**[!UICONTROL Use only matching competitor's product condition]**  — 此选项与您产品的条件相匹配。如果不存在匹配项，则产品价格为&#x200B;_[!UICONTROL Magento Price Source]_。</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** — 此选项首先会尝试根据您的产品条件进行匹配。 如果不存在匹配条件，则它会对您的产品条件和最低竞争者的条件应用差异（以百分比表示）。</li></ul><br><br>根据“条件”的列表设置显示的条件方差选项，这些设置是使用产品属性 [!DNL Commerce] [](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}映射到条件值的。对于所有映射的条件，可以表示1-100的方差百分比。 例外是可收集的，在这种情况下，可应用大于100的百分比。<br><br>当您提供的产品与竞争对手的情况不同时，此功能允许您使用智能重定价规则。要了解条件差异背后的计算，您必须首先了解所有差异都由基本匹配价格确定。 |

## 计算条件方差基数

- 基本匹配条件差异(BMC)=基本匹配价格竞争者的条件差异。 使用前面的示例，BMC是`New`条件的变量。
- 商户条件差异(MCV)=产品条件的差异。 使用前面的示例，MCV = `Used; Good`条件的变量。
- 基本匹配价格(BMP)= $7.99（如上所述）

条件方差基的计算公式为：

![条件方差基计算公式](assets/amazon-cond-variance-calc-1.png)

## 示例

条件差异设置如下：

![条件变量设置](assets/amazon-cond-variances.png)

- BMC = 100（竞争者条件=新）
- MCV = 80(商户条件=已使用；好)
- BMP = $7.99（基本匹配价格=匹配竞争者条件的最低价格）

![条件方差基计算示例](assets/amazon-cond-variance-calc-2.png)

使用上述条件差异基数计算，条件差异基数= $6.39。此计算是用于价格规则活动的竞争者价格来源，详见[价格调整](./price-adjustment.md)。
