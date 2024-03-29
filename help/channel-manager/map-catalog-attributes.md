---
title: 映射目录属性
description: '映射属性以匹配[DNL！ Commerce]产品到现有 [!DNL Walmart Marketplace] 列出并同步数据 [!DNL Channel Manager] 和 [!DNL Walmart].'
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 映射目录属性

从以下位置连接列表之前： [!DNL Commerce] 到 [!DNL Walmart Marketplace]，您必须至少映射一个来自 [!DNL Commerce] 目录到沃尔玛的相应标识符。

需要此步骤才能匹配 [!DNL Commerce] 产品到现有 [!DNL Walmart] 列出并同步产品数据 [!DNL Commerce] 和 [!DNL Walmart]. 此 [!DNL Commerce] 产品必须至少有一个产品属性与所需的以下产品标识符（产品ID）之一 [!DNL Walmart].

**必填 [!DNL Walmart] 产品ID**

| **接受类型** | **名称** | **用途** | **可接受位数** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 全球贸易项目 | 一般用途，全球使用 | 14位 |
| ISBN | 国际标准书号 | 平装本、精装本和电子书 | 10位或13位 |
| ISSN | 国际标准序列号 | 8位数的序列号，用于识别所有媒体和电子媒体上传送的各类杂志、期刊、报纸和期刊 | 8位 |
| UPC | 通用产品代码 | 标准零售跟踪代码 | 12位 |

如果目录没有匹配的属性， [添加或转换现有目录属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

## 映射唯一标识符

1. 从 **[!UICONTROL Listings]** 或 **[!UICONTROL Orders]** 销售渠道商店的页面，选择 **[!UICONTROL Channel Settings]**.

1. 开启 **[!UICONTROL Channel Settings]**，选择 **[!UICONTROL Map Attributes]**.

   - 查找 [!DNL Walmart Marketplace] 要映射的属性。

   - 从中选择相应的属性 [!DNL Commerce] 存储目录。

     以下示例映射 [!UICONTROL Walmart Marketplace UPC] 产品目录中的UPC属性。

     ![映射产品匹配条件的属性](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - 选择 **[!UICONTROL Save]**.
