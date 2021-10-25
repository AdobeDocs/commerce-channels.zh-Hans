---
title: 属性
description: AmazonSales Channel提供 [!UICONTROL Attributes] 选项卡，以监视Amazon和商务属性列表以及它们如何映射以进行产品匹配。
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 属性

的 _[!UICONTROL Attributes]_视图显示您的Amazon和 [!DNL Commerce] 属性。 该列表还指示已映射以进行产品匹配的属性。 有关更多信息，请参阅 [管理属性](./managing-attributes.md).

![属性视图](assets/amazon-attributes-view.png)

从 _[!UICONTROL Attributes]_查看，并查看表和 [创建或编辑](./creating-attributes.md) 属性。

## 查看属性列表

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. 单击 **[!UICONTROL Attributes]** 在左侧菜单中，找到Amazon属性，并查看属性列表。

1. 根据需要创建或编辑属性：

   - 至 [创建](./creating-attributes.md#create-an-attribute) 并为属性定义匹配属性值，单击 **[!UICONTROL Create]**.

   - 停用或停用 [编辑设置](./creating-attributes.md#edit-an-attribute) 或属性的匹配属性值，单击 **[!UICONTROL Edit]**.

      编辑属性包括更改属性映射以用于产品匹配。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Country] | 在中定义的销售活动的国家/地区  **[!DNL Amazon Marketplace]国家/地区** 时段 [存储集成](./store-integration.md). |
| [!UICONTROL ID] | 生成的通用属性值 [!DNL Commerce] 创建属性时。 |
| [!UICONTROL Amazon Attribute Name] | 从Amazon导入的属性的名称。 |
| [!UICONTROL Product Catalog Attribute Code] | 如果已映射，则 [!DNL Commerce] 分配到的属性 _[!UICONTROL Amazon Attribute Name]_用于匹配目录和列出产品。 |
| [!UICONTROL Overwrite Magento Values] | 如果将属性设置为 `Overwrite Existing Magento Values` 在“属性设置”中，该表显示 `Enabled`. 启用表示当从Amazon收到属性的更新产品信息时，新信息会更新（覆盖）您 [!DNL Commerce] 目录。 它还会影响 [!DNL Commerce] 商店。 |
| 状态 | 指示是否已将属性值导入 [!DNL Commerce] 并映射到 [!DNL Commerce] 属性。 选项： `Enabled` / `Disabled` |
| 操作 | 指示属性可用的任务选项。 选项： `Create` / `Edit` |
