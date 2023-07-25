---
title: 查看Amazon属性映射
description: 验证链接的Commerce属性的值，以便在Commerce和Amazon之间正确同步。
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 查看Amazon属性映射

将Amazon属性映射到 [!DNL Commerce] 属性，Amazon sales channel跟踪并提供所有Amazon值的可过滤列表。 使用此页可验证链接的值 [!DNL Commerce] 属性在之间正确同步 [!DNL Commerce] 和Amazon。 您可以查看已链接或未链接至的Amazon属性的同步值 [!DNL Commerce] 属性。 要创建或编辑Amazon属性，请参阅 [创建和编辑属性](./creating-attributes.md).

此 _Amazon Value_ 根据您查看的属性类型和Amazon属性而有所不同。 例如，下面列出的Amazon值： `Label` 将是一个文本值，而 `AmazonListPrice` 会是一个数字化的数字。 状态指示Amazon值是否已导入。

## 查看您的属性值

1. 在 _[!UICONTROL Admin]_侧栏，转到&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. 单击 **[!UICONTROL Attributes]** 在左侧菜单中，找到Amazon属性，然后单击 **[!UICONTROL Create]** 或 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 单击 **[!UICONTROL Matching Attribute Values]** 选项卡。

   具有相应 [!DNL Commerce] 目录产品在中显示链接的值 _[!UICONTROL Magento Product SKU]_列。 单击链接将打开相应的目录产品详细信息页面。 对产品详细信息页面上的Amazon属性所做的更改不会同步回Amazon销售渠道。

>[!TIP]
>要编辑清单的映射或将其分配给目录产品，请参阅 [更新必需信息](./amazon-manually-update-incomplete-listing.md).

![查看属性值](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | 中定义的销售活动的区域 **[!DNL Amazon Marketplace]国家/地区** 存储集成期间。 |
| [!UICONTROL Magento Product SKU] | 指示 [!DNL Commerce] 产品与Amazon商店同步。 值是由分配的产品ID [!DNL Commerce] 并链接到目录中的产品。 在中打开产品 [!DNL Commerce]中，单击链接。 |
| [!UICONTROL ASIN] | 指示Amazon为产品标识而分配给产品的Amazon标准标识号(ASIN) 10个字符的字母数字唯一标识符。 |
| [!UICONTROL Amazon Value] | 指示所选属性的值。 Amazon值因您查看的属性类型和Amazon属性而异。 例如，下面列出的Amazon值： `Label` 将是一个文本值，而 `AmazonListPrice` 会是一个数字化的数字。 状态指示Amazon值是否已导入。 |
| [!UICONTROL Status] | 指示属性值是否已导入到 [!DNL Commerce] 并链接到 [!DNL Commerce] 属性。 选项： `Not Imported` / `Imported` |
