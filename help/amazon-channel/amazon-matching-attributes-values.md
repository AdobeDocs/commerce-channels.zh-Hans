---
title: 查看Amazon属性映射
description: 验证链接的商务属性的值，以便在商务和Amazon之间正确同步。
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# 查看Amazon属性映射

在将Amazon属性映射到[!DNL Commerce]属性时，Amazon销售渠道会跟踪并提供所有Amazon值的可过滤列表。 使用此页可验证链接的[!DNL Commerce]属性的值是否在[!DNL Commerce]和Amazon之间正确同步。 您可以查看已链接或未链接到[!DNL Commerce]属性的Amazon属性的同步值。 要创建或编辑Amazon属性，请参阅[创建和编辑属性](./creating-attributes.md)。

_Amazon值_&#x200B;因您查看的属性类型和Amazon属性而异。 例如，列出的`Label`的Amazon值将是文本值，而`AmazonListPrice`将是数值。 状态指示是否已导入Amazon值。

## 查看属性值

1. 在&#x200B;_[!UICONTROL Admin]_侧栏中，转到&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Create]**或&#x200B;**[!UICONTROL Edit]**。

1. 单击&#x200B;**[!UICONTROL Matching Attribute Values]**&#x200B;选项卡。

   具有相应[!DNL Commerce]目录产品的列表在&#x200B;_Magento产品SKU_&#x200B;列中显示链接的值。 单击链接可打开相应的目录产品详细信息页面。 产品详细信息页面上对Amazon属性所做的更改不会同步回Amazon销售渠道。

>[!TIP]
>要编辑列表的映射或将其分配给目录产品，请参阅[更新必需信息](./amazon-manually-update-incomplete-listing.md)。

![查看属性值](assets/amazon-managing-attribute-values.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Region] | 在商店集成期间，在&#x200B;**[!DNL Amazon Marketplace]国家/地区**&#x200B;中定义的销售活动区域。 |
| [!UICONTROL Magento Product SKU] | 指示与Amazon商店同步的[!DNL Commerce]产品。 值是由[!DNL Commerce]分配并链接到目录中产品的产品ID。 要在[!DNL Commerce]中打开产品，请单击链接。 |
| [!UICONTROL ASIN] | 指示由Amazon分配给产品以进行产品标识的Amazon标准标识号(ASIN)10个字符的字母数字唯一标识符。 |
| [!UICONTROL Amazon Value] | 指示所选属性的值。 Amazon值会因您查看的属性类型和Amazon属性而异。 例如，列出的`Label`的Amazon值将是文本值，而`AmazonListPrice`将是数值。 状态指示是否已导入Amazon值。 |
| [!UICONTROL Status] | 指示属性值是否已导入到[!DNL Commerce]中，并且已链接到[!DNL Commerce]属性。 选项：`Not Imported` / `Imported` |
