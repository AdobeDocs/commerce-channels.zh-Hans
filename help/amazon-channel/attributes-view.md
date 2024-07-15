---
title: Amazon列表的属性
description: AmazonSales Channel提供了[!UICONTROL Attributes]选项卡来监控Amazon和Commerce属性的列表以及它们如何映射以便进行产品匹配。
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Amazon列表的属性

_[!UICONTROL Attributes]_视图显示您的Amazon和[!DNL Commerce]属性列表。 该列表还指示已为产品匹配映射的属性。 有关详细信息，请参阅[管理属性](./managing-attributes.md)。

![属性视图](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

从&#x200B;_[!UICONTROL Attributes]_视图中，您和查看表中的属性设置，并[创建或编辑](./creating-attributes.md)属性。

## 查看您的属性列表

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，然后查看您的属性列表。

1. 根据需要创建或编辑属性：

   - 要[创建](./creating-attributes.md#create-an-attribute)并定义该属性的匹配属性值，请单击&#x200B;**[!UICONTROL Create]**。

   - 要停用或[编辑属性的设置](./creating-attributes.md#edit-an-attribute)或匹配的属性值，请单击&#x200B;**[!UICONTROL Edit]**。

     编辑属性包括更改用于产品匹配的属性映射。

| 字段 | 描述 |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | 在[商店集成](./store-integration.md)期间在&#x200B;**[!DNL Amazon Marketplace]国家/地区**&#x200B;中定义的销售活动国家/地区。 |
| [!UICONTROL ID] | 创建属性时由[!DNL Commerce]生成的通用属性值。 |
| [!UICONTROL Amazon Attribute Name] | 从Amazon导入的属性的名称。 |
| [!UICONTROL Product Catalog Attribute Code] | 如果映射，则为匹配目录和列出产品而分配给映射到&#x200B;_[!UICONTROL Amazon Attribute Name]_的[!DNL Commerce]属性。 |
| [!UICONTROL Overwrite Magento Values] | 如果在属性设置中将属性设置为`Overwrite Existing Magento Values`，则表显示`Enabled`。 “已启用”表示从Amazon收到属性的更新产品信息时，新信息会更新（覆盖）[!DNL Commerce]目录中产品的相应信息。 它还会影响[!DNL Commerce]商店中列出的产品。 |
| 状态 | 指示属性值是否已导入[!DNL Commerce]并映射到[!DNL Commerce]属性。 选项： `Enabled` / `Disabled` |
| 操作 | 指示可用于该属性的任务选项。 选项： `Create` / `Edit` |
