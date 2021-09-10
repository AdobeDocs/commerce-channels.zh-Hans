---
title: 属性
description: AmazonSales Channel提供了[!UICONTROL Attributes]选项卡，用于监视Amazon和商务属性的列表以及它们如何映射以进行产品匹配。
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 属性

_[!UICONTROL Attributes]_视图显示您的Amazon和[!DNL Commerce]属性列表。 该列表还指示已映射以进行产品匹配的属性。 有关更多信息，请参阅[管理属性](./managing-attributes.md)。

![属性视图](assets/amazon-attributes-view.png)

从&#x200B;_[!UICONTROL Attributes]_视图中，查看表中的属性设置，并[创建或编辑](./creating-attributes.md)属性。

## 查看属性列表

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，并查看属性列表。

1. 根据需要创建或编辑属性：

   - 要创建[](./creating-attributes.md#create-an-attribute)并定义属性的匹配属性值，请单击&#x200B;**[!UICONTROL Create]**。

   - 要停用或编辑属性的设置](./creating-attributes.md#edit-an-attribute)或匹配属性值，请单击&#x200B;**[!UICONTROL Edit]**。[

      编辑属性包括更改属性映射以用于产品匹配。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Country] | 在[存储集成](./store-integration.md)期间，在&#x200B;**[!DNL Amazon Marketplace]国家/地区**&#x200B;中定义的销售活动所在的国家/地区。 |
| [!UICONTROL ID] | 创建属性时由[!DNL Commerce]生成的一般属性值。 |
| [!UICONTROL Amazon Attribute Name] | 从Amazon导入的属性的名称。 |
| [!UICONTROL Product Catalog Attribute Code] | 如果已映射，则分配给[!DNL Commerce]属性以映射到&#x200B;_[!UICONTROL Amazon Attribute Name]_以匹配目录和列出产品。 |
| [!UICONTROL Overwrite Magento Values] | 如果在“属性设置”中将属性设置为`Overwrite Existing Magento Values`，则表会显示`Enabled`。 启用表示当从Amazon收到属性的更新产品信息时，新信息会更新（覆盖）[!DNL Commerce]目录中产品的相应信息。 它还会影响[!DNL Commerce]商店中列出的产品。 |
| 状态 | 指示属性值是否已导入到[!DNL Commerce]中并映射到[!DNL Commerce]属性。 选项：`Enabled` / `Disabled` |
| 操作 | 指示属性可用的任务选项。 选项：`Create` / `Edit` |
