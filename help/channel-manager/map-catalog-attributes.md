---
title: 映射目录属性
description: '''映射属性以匹配[DNL！ Commerce]产品到现有 [!DNL Walmart Marketplace] 列表并在 [!DNL Channel Manager] 和 [!DNL Walmart]之间同步数据。'
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 映射目录属性

在将列表从[!DNL Commerce]连接到[!DNL Walmart Marketplace]之前，必须将[!DNL Commerce]目录中的至少一个唯一标识符映射到沃尔玛中的相应标识符。

必须执行此步骤才能将[!DNL Commerce]产品与现有[!DNL Walmart]列表匹配，并在[!DNL Commerce]和[!DNL Walmart]之间同步产品数据。 [!DNL Commerce]产品必须至少有一个产品属性与[!DNL Walmart]所需的以下产品标识符之一（产品ID）匹配。

**所需的[!DNL Walmart]产品ID**

| **接受的类型** | **名称** | **目的** | **可接受的位数** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 全球贸易项目 | 一般用途，全球使用 | 14位 |
| ISBN | 国际标准书号 | 平装本、精装本和电子书 | 10位或13位 |
| ISSN | 国际标准序列号 | 8位数的序列号，用于识别所有媒体和电子媒体上传送的各类杂志、期刊、报纸和期刊 | 8位 |
| UPC | 通用产品代码 | 标准零售跟踪代码 | 12位 |

如果目录没有匹配的属性，请[添加或转换现有的目录属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)。

## 映射唯一标识符

1. 从销售渠道商店的&#x200B;**[!UICONTROL Listings]**&#x200B;或&#x200B;**[!UICONTROL Orders]**&#x200B;页面中，选择&#x200B;**[!UICONTROL Channel Settings]**。

1. 在&#x200B;**[!UICONTROL Channel Settings]**&#x200B;上，选择&#x200B;**[!UICONTROL Map Attributes]**。

   - 查找要映射的[!DNL Walmart Marketplace]属性。

   - 从[!DNL Commerce]存储目录中选择对应的属性。

     以下示例将[!UICONTROL Walmart Marketplace UPC]属性映射到产品目录中的UPC属性。

     ![映射产品匹配条件的属性](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - 选择&#x200B;**[!UICONTROL Save]**。
