---
title: Amazon列表的属性
description: AmazonSales Channel提供 [!UICONTROL Attributes] 选项卡，用于监视Amazon和Commerce属性的列表以及如何映射它们以进行产品匹配。
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Amazon列表的属性

此 _[!UICONTROL Attributes]_视图显示您的Amazon列表和 [!DNL Commerce] 属性。 该列表还指示已为产品匹配映射的属性。 有关更多信息，请参阅 [管理属性](./managing-attributes.md).

![属性视图](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

从 _[!UICONTROL Attributes]_查看、您和查看表格中的属性设置和 [创建或编辑](./creating-attributes.md) 属性。

## 查看您的属性列表

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. 单击 **[!UICONTROL Attributes]** 在左侧菜单中，找到Amazon属性，并查看属性列表。

1. 根据需要创建或编辑属性：

   - 至 [创建](./creating-attributes.md#create-an-attribute) 并定义属性的匹配属性值，请单击 **[!UICONTROL Create]**.

   - 要取消激活或 [编辑设置](./creating-attributes.md#edit-an-attribute) 或属性的“匹配属性值”，请单击 **[!UICONTROL Edit]**.

     编辑属性包括更改用于产品匹配的属性映射。

| 字段 | 描述 |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | 中定义的销售活动的国家/地区  **[!DNL Amazon Marketplace]国家/地区** 期间 [存储集成](./store-integration.md). |
| [!UICONTROL ID] | 生成的通用属性值 [!DNL Commerce] 创建属性时。 |
| [!UICONTROL Amazon Attribute Name] | 从Amazon导入的属性的名称。 |
| [!UICONTROL Product Catalog Attribute Code] | 如果已映射， [!DNL Commerce] 分配给映射到的属性 _[!UICONTROL Amazon Attribute Name]_用于匹配目录和列出产品。 |
| [!UICONTROL Overwrite Magento Values] | 如果属性设置为 `Overwrite Existing Magento Values` 在“属性设置”中，该表显示 `Enabled`. “已启用”表示从Amazon收到属性的更新产品信息时，新信息会更新（覆盖）中产品的相应信息。 [!DNL Commerce] 目录。 它还可能会影响您网站上的 [!DNL Commerce] 商店。 |
| 状态 | 指示属性值是否已导入到 [!DNL Commerce] 并映射到 [!DNL Commerce] 属性。 选项： `Enabled` / `Disabled` |
| 操作 | 指示可用于该属性的任务选项。 选项： `Create` / `Edit` |
