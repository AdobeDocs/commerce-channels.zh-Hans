---
title: 上市规则
description: 使用上市规则可确定作为Amazon Marketplace列表发布的商务目录产品。
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# 上市规则

您可以访问存储在[存储功能板](./amazon-store-dashboard.md)中的列表规则。

上市规则定义规则，以确定Amazon销售渠道发布到Amazon的产品。 这些规则提供了许多选项，可用于创建简单到复杂的规则，以将产品作为列表包含或排除。 每个规则都包含设置产品列表资格要求的条件。

您的列表规则会持续与[!DNL Commerce]目录同步。 添加符合上市规则所设资格要求的新[!DNL Commerce]产品时，这些产品会自动处理以在Amazon上列出。

- 如果您希望将所有产品发布到Amazon列表，请勿为您的上市规则定义任何条件。

- 如果要限制发布到Amazon的目录产品中的哪些产品，可定义列表规则条件。 定义Amazon列表规则的条件与定义[购物车价格规则](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}的条件的逻辑和过程相同。

- 如果您的列表规则排除某个产品，则该产品的资格状态将更改为`Ineligible`。 不合格的产品不会发布到Amazon。

- 如果不符合条件的产品已列在Amazon上，并且您将Amazon列表与[!DNL Commerce]目录产品相匹配，则Amazon列表的数量将更改为`0`，以防止产品销售。 Amazon列表可以[手动删除](./end-listings-manually.md)。

数量和资格状态的更改会影响所有在市场上共享Amazon销售商SKU的列表，这些市场中存在的商店销售在同一地区（在[商店集成](./store-integration.md)期间，如&#x200B;_[!UICONTROL Amazon Marketplace Country]_中定义）。 但是，对一个区域中共享的[!DNL Amazon Seller SKU]所做的更改不会影响其他国家/地区的产品Amazon列表。

![上市规则](assets/ob-listing-rules.png)

## 配置列表规则设置

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Rules]**。

1. 为要在Amazon上列出的产品的资格定义所需的条件。

请参阅[示例：定义条件](./ob-define-condition-example.md)。

| 字段 | 描述 |
|---|---|
| [!UICONTROL Websites] | 可用选项取决于您在[!DNL Commerce]配置中设置的[websites](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}。 为Amazon上列出的合格产品选择网站。 只能选择一个网站，因为每个网站需要在Amazon销售渠道中创建唯一的Amazon商店。 |
| [!UICONTROL Conditions] | 用于定义Amazon地区内产品资格的[!DNL Commerce]属性。 请参阅[示例：定义条件](./ob-define-condition-example.md)。 |

## 条件工作区

单击条件中任何以粗体显示的区域可查看各种选项。

- 如果所选网站中的所有产品均符合条件，请勿添加条件。
- 有一组复杂的后端进程可直接与Amazon的系统通信。 根据您尝试列出的项目数以及Amazon系统可能有多忙（例如“黑色星期五”），您的项目可能需要一些时间才能在Amazon上列出。

有关条件的更多信息，请参阅[描述条件](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}。

## 列出规则预览

在修改列表规则的条件定义时，可以单击&#x200B;**[!UICONTROL Preview Changes]**&#x200B;以应用规则更改并查看列表受到的影响。 在保存列表规则更改之前，在此列表预览功能中验证您的列表。

您的Amazon列表将根据您的规则和定义的条件进行比较。 然后，您可以查看：

- 哪些产品会根据您当前的[!DNL Amazon Seller Central]帐户变为不合格状态
- 哪些产品从不合格状态移回合格状态
- 哪些产品属于新的Amazon列表，并从符合条件的[!DNL Commerce]产品添加到您的Amazon列表中

列表预览功能允许您预览潜在的Amazon列表，并对列表规则进行任何必要的调整。

您的潜在Amazon列表会填充&#x200B;_[!UICONTROL Listing Preview]_页面上三个选项卡之一的列表：

- **[!UICONTROL Ineligible Listings]**  — 根据您当前的上市规则及条件，所列产品不符合Amazon上市资格。

   不合格的产品不会发布到Amazon。 如果不符合条件的产品已列在Amazon上，并且您将Amazon列表与[!DNL Commerce]目录产品相匹配，则Amazon列表的数量将更改为`0`，以防止产品销售。 要手动删除列表，请参阅[结束Amazon列表](./end-listings-manually.md)。 此处未列出不符合Amazon要求的产品。 这些产品列在[不活动列表选项卡](./inactive-listings.md)中。

- **[!UICONTROL Eligible Listings]**  — 根据您当前的上市规则及条件，所列产品符合Amazon上市资格，并符合Amazon要求。此列表包括您现有的导入Amazon列表（如果在[列表设置](./third-party-listing-settings.md)中将&#x200B;**导入第三方列表**&#x200B;设置为`Import Listing`）。

- **[!UICONTROL New Listings]**  — 列出的产品包括您 [!DNL Commerce] 的目录产品，这些产品根据您当前的上市规则和条件，新符合Amazon上市资格，并创建和发布新的Amazon列表。

### 查看列表预览

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Rules]**。

1. 查看或添加您的[列表规则](./listing-rules.md)。

1. 修改[列表规则条件](./ob-define-condition-example.md)。

1. 单击&#x200B;**[!UICONTROL Preview Changes]**。

1. 在&#x200B;_[!UICONTROL Ineligible Listings]_、_[!UICONTROL Eligible Listings]_&#x200B;和&#x200B;_[!UICONTROL New Listings]_选项卡中查看并确认您的列表。

1. 如果列表符合您的预期，请单击&#x200B;**[!UICONTROL Save and close]**。

   如果您的列表没有按预期显示，请单击&#x200B;**[!UICONTROL Back]**&#x200B;并修改您的规则和条件，直到列表符合您的预期。

![列出规则预览](assets/amazon-listing-rule-preview.png)

### 列出预览记录

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Product ID] | 添加时分配给[!DNL Commerce]目录产品的唯一顺序编号。 |
| [!UICONTROL Thumbnail] | 显示主产品图像的缩略图。 |
| [!UICONTROL Name] | 在[!DNL Commerce] [产品网格](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}中管理的产品名称。 |
| [!UICONTROL Type] | 在[!DNL Commerce]产品网格中管理的产品类型。 |
| [!UICONTROL Attribute Set] | 用作产品模板的属性集的名称，在[!DNL Commerce]产品网格中进行管理。 |
| [!UICONTROL SKU] | 分配给产品并在[!DNL Commerce]产品网格中管理的唯一库存单位。 |
| [!UICONTROL Visibility] | 指示在[!DNL Commerce]产品网格中管理产品的位置。 选项：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| 状态 | 指示在[!DNL Commerce]产品网格中管理的产品的状态。 选项：`Enabled` / `Disabled` |

![列出预览工作流](assets/listing-preview-flowchart.png)
