---
title: Amazon sales channel — 产品列表条件
description: 使用产品列表条件设置将您的Commerce产品映射到Amazon产品条件，例如“新增”或“已翻新”。
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 产品列表条件

产品列表条件设置是商店列表设置的一部分。 您可以访问 [存储仪表板](./amazon-store-dashboard.md).

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
>如果您销售已续订（翻新）的产品，则必须注册 [!DNL Amazon Renewed Program]. 请参阅 [续订的产品](./renewed-products.md).

但是，如果您的目录包含不同条件的产品（例如“新建”、“已使用”和“已翻新”），则必须选择 **[!UICONTROL Assign Condition Using Product Attribute]**. 此设置允许您映射 [!DNL Commerce] 条件属性和值添加到Amazon列表的条件。

时段 [预设置任务](./amazon-pre-setup-tasks.md)，建议您创建 [!DNL Commerce] 产品条件的产品属性。 如果您以各种条件提供产品，但尚未创建条件属性，请参阅 [在中创建产品属性 [!DNL Commerce]](./ob-creating-magento-attributes.md). 创建条件属性后，您可以为中的每项产品分配一个条件值。 [!DNL Commerce] 目录。

## 配置设置

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 **[!UICONTROL Product Listing Condition]** 部分。

1. 对象 **[!UICONTROL Listing Product Condition]**，选择一个选项。

   为所有清单的全局条件值选择一个标准Amazon条件。 默认设置为 `New`.

   如果您的产品/列表具有不同的条件，请选择 `Assign Condition Using Product Attribute` 在显示的其他字段中定义产品条件设置。

1. 对象 **条件属性**，选择 [!DNL Commerce] 属性来映射每个标准Amazon条件属性的值。

   如果您的产品 `Used` 或 `Collectible` 条件，但无法进一步区分，您可以映射到单个 `Used` 或 `Collectible` Amazon条件并将其余项留空。 此方法将映射您的所有 `Used` 或 `Collectible` 单“Amazon已使用”或“可收集”条件的条件。

   例如，您有一个 `Used` 产品的条件。 映射时，您可以选择是否要映射到Amazon条件 `Used; Like New`， `Used; Very Good`， `Used; Good`，或 `Used; Acceptable`. 仅填写所需Amazon条件的字段，然后填写其他 `Used` 选项设置为 `--Select Option--`. 在示例图像中，所有 [!DNL Commerce] 中的产品 `Used` 条件已映射到Amazon `Used; Very Good` 条件。

   您还可以为条件输入描述性文本，但 `New`.

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![产品列表条件](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | 产品清单的条件。 选项： `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>如果您销售单个产品条件，请选择其中一个标准Amazon条件。 如果您的 [!DNL Commerce] 目录包含处于各种状态的产品，请选择 `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | 此 [!DNL Commerce] 定义产品条件的属性。 选择您创建的要映射到Amazon条件属性的“磁铁”属性。 在 [预设置任务示例](./ob-creating-magento-attributes.md) 建议将其命名为 `Amazon Condition`. 选择后，将显示用于映射标准Amazon条件的其他字段。 |
| [!UICONTROL Additional Condition fields] | 对于每个标准Amazon条件，选择相应的条件。 选项是您在以下情况下添加的条件标签： [已创建Amazon条件属性](./ob-creating-magento-attributes.md).<br><br>如果您的产品 `Used` 或 `Collectible` 条件，但无法进一步区分，您可以映射到单个 `Used` 或 `Collectible` Amazon条件并将其余项留空。 此方法映射所有 `Used` 或 `Collectible` 单“Amazon已使用”或“可收集”条件的条件。 |

**快速访问** - [!UICONTROL Listing Settings] 部分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
