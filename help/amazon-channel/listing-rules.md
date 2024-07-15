---
title: Amazon销售渠道 — [!UICONTROL Listing Rules]
description: 使用列表规则可确定作为Commerce Marketplace列表发布的Amazon目录产品。
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

您可以访问[存储仪表板](./amazon-store-dashboard.md)中存储的列表规则。

上市规则定义了用于确定哪些产品将发布到Amazon的Amazon的规则。 这些规则提供了许多选项，可用于创建简单到复杂的规则，以将产品作为列表进行包含或排除。 每个规则都包含一些条件，用于设置产品列表资格的要求。

您的列表规则会不断与您的[!DNL Commerce]目录同步。 在添加新[!DNL Commerce]产品以满足上市规则设置的资格要求时，将自动处理这些产品以将其在Amazon中列出。

- 如果您希望将所有产品发布到Amazon列表，请不要为上市规则定义任何条件。

- 如果要限制发布到Amazon的目录产品，请定义上市规则条件。 定义Amazon列表规则的条件遵循与定义[购物车价格规则](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html)的条件相同的逻辑和过程。

- 如果您的列表规则不包括产品，则该产品的资格状态将更改为`Ineligible`。 不符合条件的产品将不会发布到Amazon。

- 如果Amazon上已列出不合格产品，并且您将Amazon列表与您的[!DNL Commerce]目录产品匹配，则Amazon列表的数量将更改为`0`以防止产品销售。 Amazon列表可以[手动删除](./end-listings-manually.md)。

数量和资格状态的更改会影响为同一地区的商店销售（在[商店集成](./store-integration.md)期间在&#x200B;_[!UICONTROL Amazon Marketplace Country]_中定义）而存在的市场中所有共享Amazon销售者SKU的列表。 但是，在一个地区对共享[!DNL Amazon Seller SKU]所做的更改不会影响该产品在其他国家/地区的Amazon列表。

![列表规则](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## 配置列表规则设置

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Rules]**。

1. 针对在Amazon上列出的产品资格定义所需条件。

请参阅[示例：定义条件](./ob-define-condition-example.md)。

| 字段 | 描述 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | 可用选项取决于您在[!DNL Commerce]配置中设置的[网站](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html)。 为Amazon上列出的符合条件的产品选择网站。 只能选择一个网站，因为每个网站都需要在Amazon销售渠道中创建唯一的Amazon商店。 |
| [!UICONTROL Conditions] | 用于定义[!DNL Commerce]属性，以获取Amazon地区的产品资格。 请参阅[示例：定义条件](./ob-define-condition-example.md)。 |

## 条件工作区

在条件中以粗体显示的任何区域都可以单击来查看各种选项。

- 如果所选网站中的所有产品都符合条件，请勿添加条件。
- 要直接与Amazon的系统通信，需要有一组复杂的后端流程。 根据您尝试列出的项目数量以及Amazon的系统可能有多忙（例如“黑色星期五”），在Amazon上列出您的项目可能需要一些时间。

有关条件的详细信息，请参阅[描述条件](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html)。

## 列表规则预览

在修改列表规则的条件定义时，您可以单击&#x200B;**[!UICONTROL Preview Changes]**&#x200B;以应用规则更改并查看列表如何受到影响。 在保存列表规则更改之前，在此列表预览功能中验证您的列表。

Amazon列表会与您的规则和定义的条件进行比较。 然后，您可以查看：

- 根据您当前的[!DNL Amazon Seller Central]帐户，哪些产品将移至不合格状态
- 哪些产品从不合格状态移回合格状态
- 哪些产品是新的Amazon列表，并通过符合条件的[!DNL Commerce]产品添加到您的Amazon列表

列表预览允许您预览潜在的Amazon列表，并对列表规则进行任何必要的调整。

您的潜在Amazon列表会在以下三个选项卡之一中填充到&#x200B;_[!UICONTROL Listing Preview]_页面上：

- **[!UICONTROL Ineligible Listings]** — 根据您当前的上市规则和条件，列出的产品不符合Amazon的上市条件。

  不符合条件的产品将不会发布到Amazon。 如果Amazon上已列出不合格产品，并且您将Amazon列表与您的[!DNL Commerce]目录产品匹配，则Amazon列表的数量将更改为`0`以防止产品销售。 要手动删除列表，请参阅[结束Amazon列表](./end-listings-manually.md)。 此处不列出不符合Amazon要求的产品。 这些产品列在[非活动列表选项卡](./inactive-listings.md)上。

- **[!UICONTROL Eligible Listings]** — 根据您当前的上市规则和条件，已上市产品符合Amazon上市资格并符合Amazon要求。 此列表包括您导入的现有Amazon列表（如果您在[列表设置](./third-party-listing-settings.md)中将&#x200B;**导入第三方列表**&#x200B;设置为`Import Listing`）。

- **[!UICONTROL New Listings]** — 列出的产品包括您的[!DNL Commerce]目录产品，这些产品根据您当前的列表规则和条件新符合Amazon列表的条件，并且创建和发布新的Amazon列表。

### 查看列表预览

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Rules]**。

1. 查看或添加您的[列表规则](./listing-rules.md)。

1. 修改您的[列表规则条件](./ob-define-condition-example.md)。

1. 单击&#x200B;**[!UICONTROL Preview Changes]**。

1. 在&#x200B;_[!UICONTROL Ineligible Listings]_、_[!UICONTROL Eligible Listings]_&#x200B;和&#x200B;_[!UICONTROL New Listings]_选项卡中查看并确认您的列表。

1. 如果清单符合您的预期，请单击&#x200B;**[!UICONTROL Save and close]**。

   如果您的列表未按预期显示，请单击&#x200B;**[!UICONTROL Back]**&#x200B;并修改您的规则和条件，直到您的列表符合您的预期。

![列表规则预览](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### 列出预览记录

| 字段 | 描述 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | 添加时分配给[!DNL Commerce]目录产品的唯一序列号。 |
| [!UICONTROL Thumbnail] | 显示主要产品图像的缩略图。 |
| [!UICONTROL Name] | 在[!DNL Commerce] [产品网格](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html)中管理的产品名称。 |
| [!UICONTROL Type] | 在[!DNL Commerce]产品网格中管理的产品类型。 |
| [!UICONTROL Attribute Set] | 用作产品模板的属性集的名称，在[!DNL Commerce]产品网格中管理。 |
| [!UICONTROL SKU] | 分配给产品的唯一库存单位，在[!DNL Commerce]产品网格中管理。 |
| [!UICONTROL Visibility] | 指示在[!DNL Commerce]产品网格中管理产品的可见位置。 选项：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| 状态 | 指示在[!DNL Commerce]产品网格中管理的产品的状态。 选项： `Enabled` / `Disabled` |

![正在列出预览工作流](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
