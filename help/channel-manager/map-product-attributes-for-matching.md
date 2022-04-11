---
title: 配置产品匹配
description: 将用于将商务产品与现有Walmart Marketplace列表匹配的属性映射到
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# 配置产品匹配

在将列表发布到Walmart Marketplace之前，请将产品目录属性中的至少一个唯一标识符映射到所需的Walmart Marketplace产品标识符之一。 要匹配Walmart Marketplace上的产品，需要执行此步骤。

对于产品匹配，商务产品在目录属性中必须至少具有以下一个产品标识符（产品ID）。

**必需的Walmart产品ID**

| **接受类型** | **名称** | **用途** | **可接受位数** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 全球贸易项目 | 通用用途，在全球范围内使用 | 14位 |
| ISBN | 国际标准书号 | 平装书、精装书和电子书 | 10位或13位 |
| ISSN | 国际标准序列号 | 8位序列号，用于识别所有媒体印刷和电子印刷的各类杂志、期刊、报纸和期刊 | 8位 |
| ISBN | 国际标准书号 | 平装、精装和电子 | 12位 |

如果您的目录中具有不同类型的产品ID属性，请将其转换为所需类型之一。 然后，将其映射到Channel Manager商店的列表配置中相应的Walmart Marketplace属性。

## 配置产品属性设置

1. 在 [!UICONTROL Listings] 页面，在 *草稿* 状态。

1. 选择 **[!UICONTROL Settings]**.

   - 查找要映射的Walmart Marketplace属性。

   - 从存储目录中选择相应的属性。

      以下示例将Walmart Marketplace UPC属性映射到产品目录中的UPC属性。
   ![映射产品匹配条件的属性](assets/products-map-attributes-for--match.png)

   - 选择 **[!UICONTROL Save]**.


## 更新映射的属性配置

通过更新映射的属性设置，更改匹配产品的商务产品标识符。

例如，您可以根据SKU进行匹配，而不是根据Commerce UPC产品属性代码来匹配产品。 或者，映射其他属性以改进匹配。

1. 从 **[!UICONTROL Listings]**，选择 **[!UICONTROL Settings]**.

1. 在映射属性窗体中，根据需要更改映射的属性配置。
