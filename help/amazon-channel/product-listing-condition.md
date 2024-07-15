---
title: Amazon sales channel — 产品列表条件
description: 使用产品列表条件设置将您的Commerce产品映射到Amazon产品条件，如“新增”或“已翻新”。
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 产品列表条件

产品列表条件设置是商店列表设置的一部分。 您可以访问[商店仪表板](./amazon-store-dashboard.md)上的列表设置。

Amazon要求产品列表必须具备定义的条件。 如果所有产品条件相同，则可以选择一个Amazon条件选项，以将所有产品表示为全局条件值。 标准Amazon条件包括：

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>如果您销售已续订（翻新）的产品，则必须注册[!DNL Amazon Renewed Program]。 查看[续订的产品](./renewed-products.md)。

但是，如果您的目录包含处于不同状态（例如“新建”、“已使用”和“已翻新”）的产品，则必须选择&#x200B;**[!UICONTROL Assign Condition Using Product Attribute]**。 此设置允许您将[!DNL Commerce]条件属性和值映射到Amazon列表的条件。

在[预设置任务](./amazon-pre-setup-tasks.md)期间，建议您为产品条件创建[!DNL Commerce]产品属性。 如果您以各种条件提供产品，但尚未创建条件属性，请参阅[在 [!DNL Commerce]](./ob-creating-magento-attributes.md)中创建产品属性。 创建条件属性后，您可以为[!DNL Commerce]目录中的每个产品分配一个条件值。

## 配置设置

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;**[!UICONTROL Product Listing Condition]**&#x200B;部分。

1. 为&#x200B;**[!UICONTROL Listing Product Condition]**&#x200B;选择一个选项。

   为所有清单的全局条件值选择一个标准Amazon条件。 默认设置为`New`。

   如果您的产品/清单具有不同的条件，请选择`Assign Condition Using Product Attribute`以在显示的其他字段中定义产品条件设置。

1. 对于&#x200B;**条件属性**，选择[!DNL Commerce]属性以映射每个标准Amazon条件属性的值。

   如果您的产品处于`Used`或`Collectible`条件，但无法进一步区分，则您可以映射到单个`Used`或`Collectible`Amazon条件，并将其他条件留空。 此方法将您的所有`Used`或`Collectible`条件映射到单个“已使用”或“可收集”Amazon条件。

   例如，您的产品只有一个`Used`条件。 映射时，您可以选择是要映射到Amazon条件`Used; Like New`、`Used; Very Good`、`Used; Good`还是`Used; Acceptable`。 仅填写所需Amazon条件的字段，将其他`Used`选项保留设置为`--Select Option--`。 在示例图像中，`Used`条件中的所有[!DNL Commerce]产品都映射到Amazon `Used; Very Good`条件。

   您还可以为条件输入描述性文本，`New`除外。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![产品列表条件](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | 产品清单的条件。 选项： `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>如果您销售单个产品条件，请选择其中一个标准Amazon条件。 如果您的[!DNL Commerce]目录包含各种条件的产品，请选择`Assign Condition Using Product Attribute`。 |
| [!UICONTROL Condition Attribute] | 定义产品条件的[!DNL Commerce]属性。 选择您创建的要映射到Amazon条件属性的“磁铁”属性。 在[预设置任务示例](./ob-creating-magento-attributes.md)中，建议将其命名为`Amazon Condition`。 选择后，将显示用于映射标准Amazon条件的其他字段。 |
| [!UICONTROL Additional Condition fields] | 对于每个标准Amazon条件，选择相应的条件。 这些选项是您在[创建Amazon条件属性](./ob-creating-magento-attributes.md)时添加的条件标签。<br><br>如果您的产品处于`Used`或`Collectible`条件，但无法进一步区分，则您可以映射到单个`Used`或`Collectible`Amazon条件，并将其他条件留空。 此方法将所有`Used`或`Collectible`条件映射到单个“已使用”或“可收集”Amazon条件。 |

**快速访问** - [!UICONTROL Listing Settings]分区

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
