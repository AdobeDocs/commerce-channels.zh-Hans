---
title: 产品列表条件
description: 使用“产品列表条件”设置将您的商务产品映射到Amazon产品条件，如“新”或“翻新”。
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# 产品列表条件

产品清单条件设置是您的商店清单设置的一部分。 您可以访问[存储功能板](./amazon-store-dashboard.md)上的列表设置。

Amazon要求产品列表具有定义的条件。 如果您的所有产品都是相同的条件，则可以选择一个Amazon条件选项，以将您的所有产品表示为全局条件值。 标准Amazon条件包括：

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
>如果您销售续订（翻新）产品，则必须注册[!DNL Amazon Renewed Program]。 请参阅[续订的产品](./renewed-products.md)。

但是，如果目录包含不同条件（如“新建”、“已用”和“已翻新”）的产品，则必须选择&#x200B;**[!UICONTROL Assign Condition Using Product Attribute]**。 此设置允许您将[!DNL Commerce]条件属性和值映射到Amazon列表的条件。

在[预设置任务](./amazon-pre-setup-tasks.md)期间，建议您为产品条件创建[!DNL Commerce]产品属性。 如果您在各种条件下提供产品，并且尚未创建条件属性，请参阅[在 [!DNL Commerce]](./ob-creating-magento-attributes.md)中创建产品属性。 创建条件属性后，您可以为[!DNL Commerce]目录中的每个产品分配条件值。

## 配置设置

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;**[!UICONTROL Product Listing Condition]**&#x200B;部分。

1. 对于&#x200B;**[!UICONTROL Listing Product Condition]**，选择一个选项。

   为所有列表的全局条件值选择一个标准的Amazon条件。 默认设置为`New`。

   如果您的产品/列表具有不同的条件，请选择`Assign Condition Using Product Attribute`以在显示的其他字段中定义产品条件设置。

1. 对于&#x200B;**条件属性**，选择[!DNL Commerce]属性以映射每个标准Amazon条件属性的值。

   如果您在`Used`或`Collectible`条件中有产品，但您没有进一步区分，则可以映射到单个`Used`或`Collectible` Amazon条件，并将其他条件留空。 此方法会将您的所有`Used`或`Collectible`条件映射到单个Amazon Used或Coluble条件。

   例如，您的产品有一个`Used`条件。 映射时，您可以选择是要映射到Amazon条件`Used; Like New`、`Used; Very Good`、`Used; Good`还是`Used; Acceptable`。 只填写所需Amazon条件的字段，将其他`Used`选项设置为`--Select Option--`。 在示例图像中，`Used`条件中的所有[!DNL Commerce]产品都映射到Amazon `Used; Very Good`条件。

   您还可以为条件输入描述性文本，但`New`除外。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![产品列表条件](assets/amazon-product-listing-condition.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Listing Product Condition] | 您的产品列表的条件。 选项：`New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>如果您销售的是单个产品条件，请选择一个标准的Amazon条件。 如果您的[!DNL Commerce]目录包含各种条件的产品，请选择`Assign Condition Using Product Attribute`。 |
| [!UICONTROL Condition Attribute] | 用于定义产品条件的[!DNL Commerce]属性。 选择您创建以映射到Amazon条件属性的Mangeto属性。 在[预设置任务示例](./ob-creating-magento-attributes.md)中，建议将其命名为`Amazon Condition`。 选择后，将显示用于映射标准Amazon条件的其他字段。 |
| [!UICONTROL Additional Condition fields] | 对于每个标准Amazon条件，选择相应的条件。 这些选项是您在[创建Amazon条件属性](./ob-creating-magento-attributes.md)时添加的条件标签。<br><br>如果您在或条件中 `Used` 包含 `Collectible` 产品，但未进一步区分，则可以映射到单个或Amazon `Used` 条件，并 `Collectible` 将其他条件留空。此方法将所有`Used`或`Collectible`条件映射到单个Amazon Used或Coluble条件。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
