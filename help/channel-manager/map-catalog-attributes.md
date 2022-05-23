---
title: 映射目录属性
description: 映射用于匹配的属性[DNL! 商务]产品到现有 [!DNL Walmart Marketplace] 列表和同步数据 [!DNL Channel Manager] 和 [!DNL Walmart].
source-git-commit: dfe56db25bb569ad70fb1036d539797bbb126dd5
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# 映射目录属性

在从发布列表之前 [!DNL Commerce] to [!DNL Walmart Marketplace]，则必须从 [!DNL Commerce] Walmart中相应标识符的目录。
需要此步骤才能匹配 [!DNL Commerce] 现有产品 [!DNL Walmart] 列表和同步产品数据 [!DNL Commerce] 和 [!DNL Walmart].

对于产品匹配，商务产品必须至少具有一个与以下产品标识符（产品ID）中的一个匹配的产品属性， [!DNL Walmart].

**必需的Walmart产品ID**

| **接受类型** | **名称** | **用途** | **可接受位数** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 全球贸易项目 | 通用用途，在全球范围内使用 | 14位 |
| ISBN | 国际标准书号 | 平装书、精装书和电子书 | 10位或13位 |
| ISSN | 国际标准序列号 | 8位序列号，用于识别所有媒体印刷和电子印刷的各类杂志、期刊、报纸和期刊 | 8位 |
| UPC | 通用产品代码 | 标准零售跟踪代码 | 12位 |

如果您的目录没有与以下类型之一匹配的属性， [添加或转换现有目录属性](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## 映射唯一标识符

1. 在 [!UICONTROL Listings] 页面，选择 **[!UICONTROL Settings]**.

   - 查找要映射的Walmart Marketplace属性。

   - 从 [!DNL Commerce] 存储目录。

      以下示例将Walmart Marketplace UPC属性映射到产品目录中的UPC属性。
   ![映射产品匹配条件的属性](assets/products-map-attributes-for-match.png)

   - 选择 **[!UICONTROL Save]**.


## 更新映射的属性配置

通过更新映射的属性设置，更改匹配产品的商务产品标识符。

例如，您可以根据SKU进行匹配，而不是根据Commerce UPC产品属性代码来匹配产品。 或者，映射其他属性以改进匹配。

1. 从 **[!UICONTROL Listings]**，选择 **[!UICONTROL Settings]**.

1. 在映射属性窗体中，根据需要更改映射的属性配置。
