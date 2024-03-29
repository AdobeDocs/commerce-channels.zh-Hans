---
title: 为Amazon创建Commerce属性
description: 在完成Amazon sales channel新用户引导过程之前，确保您已满足需要 [!UICONTROL Commerce] 产品属性。
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# 为Amazon创建Commerce属性

载入之前 [!DNL Amazon Seller Central] 帐户，最佳做法是添加 [!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) 以映射您的产品列表。 完成载入后，您可以通过以下方式管理产品属性 [属性](./managing-attributes.md) 选项卡 [Amazon sales channel主页](./amazon-sales-channel-home.md) 页面。

以下说明详细介绍了如何创建 [!DNL Commerce] Amazon ASIN和Amazon条件的属性。 建议创建其他属性，包括Amazon EAN、Amazon ISBN和Amazon UPC。 如果要使用Amazon的上市价格作为定价规则的价格来源，则可能还希望创建Amazon价格属性。 在新用户引导期间配置您的列表和定价设置时，将使用这些属性。 在创建Amazon列表以及更新和同步时，也可以使用这些属性 [!DNL Commerce] 将您的Amazon列表编入目录。

目录搜索设置允许您设置有助于映射符合条件的匹配搜索参数 [!DNL Commerce] 产品与Amazon列表。 在映射后，Amazon会激活与定价、数量、覆盖以及订单和产品同步相关的操作。

定义这些值会增加完全匹配的可能性，从而最大限度地减少以后手动匹配产品清单的需求。 在载入过程中添加属性 [预设置任务](./amazon-pre-setup-tasks.md)，Amazon销售渠道具有更大的潜力，可以在产品上线期间自动匹配您的产品，并在Amazon和之间同步产品数据 [!DNL Commerce] 入职后。

如果只创建Amazon ASIN属性（不添加每个产品的ASIN值），则您可以 [!DNL Commerce] 产品可能不会自动匹配您的Amazon列表。 您可以通过以下方式手动匹配产品 _商店评论_. 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您为手动匹配的产品更新ASIN、UPC或其他数据元素，则必须同时更新以下两个位置的数据： [!DNL Commerce] 目录和列表 [!DNL Amazon Seller Central] 帐户。

## 创建Amazon ASIN产品属性

1. 登录 [!DNL Commerce] 管理员。

1. 单击 **[!UICONTROL Stores]** 左侧菜单中的。

1. 在 _[!UICONTROL Attributes]_部分，单击&#x200B;**[!UICONTROL Product]**.

1. 要打开属性属性，请单击 **[!UICONTROL Add New Attribute]**.

1. 对象 **[!UICONTROL Default Label]**，输入 `Amazon ASIN` （属性的名称）。

1. 对象 **[!UICONTROL Catalog Input Type for Store Owner]**，选择 `Text Field`.

1. 对象 **[!UICONTROL Values Required]**，选择 `No`.

   尽管Amazon ASIN需要在Amazon上列出产品，但您的某些目录产品可能未在Amazon上列出。

1. 展开 _[!UICONTROL Advanced Attribute Properties]_并设置以下选项：

   - 对象 **[!UICONTROL Attribute Code]**，输入 `amazon_asin`.

   - 对象 **[!UICONTROL Scope]**，选择 `Global`.

   - 对象 **[!UICONTROL Unique Value]**，选择 `No`.

   - 对象 **[!UICONTROL Input Validation for Store Owner]**，选择 `None`.

   - 对象 **[!UICONTROL Add to Column Options]**，选择 `Yes`.

   - 对象 **[!UICONTROL Use in Filter Options]**，选择 `Yes`.

1. 单击 **[!UICONTROL Save Attribute]**.

![Amazon ASIN属性](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## 创建“Amazon条件”产品属性

1. 登录 [!DNL Commerce] 管理员。

1. 单击 **[!UICONTROL Stores]** 左侧菜单中的。

1. 在 _[!UICONTROL Attributes]_部分，单击&#x200B;**[!UICONTROL Product]**.

1. 要打开属性属性，请单击 **[!UICONTROL Add New Attribute]**.

1. 对象 **[!UICONTROL Default Label]**，输入 `Amazon Condition` （属性的名称）。

1. 对象 **[!UICONTROL Catalog Input Type for Store Owner]**，选择 `Dropdown`.

   此 _[!UICONTROL Manage Options (Values of your Attribute)]_部分。

1. 对象 **[!UICONTROL Values Required]**，选择 `No`.

1. 对象 **[!UICONTROL Manage Options (Values for your Attribute)]**，添加每个条件选项。

   标准Amazon条件包括：

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. 单击 **[!UICONTROL Add Option]**.

1. 选择 **[!UICONTROL Is Default]** 您希望作为默认选择的条件的选项。

1. 在 _[!UICONTROL Admin]_列中，输入要添加的条件的标签的文本(例如 `New`， `Used`、和 `Used-Like New`)

1. 单击 **[!UICONTROL Add Option]** 以根据需要添加更多选项。

1. 展开 _[!UICONTROL Advanced Attribute Properties]_并设置选项。

   - 对象 **[!UICONTROL Attribute Code]**，输入 `amazon_condition`.

   - 对象 **[!UICONTROL Scope]**，选择 `Global`.

   - 对象 **[!UICONTROL Unique Value]**，选择 `No`.

   - 对象 **[!UICONTROL Input Validation for Store Owner]**，选择 `None`.

   - 对象 **[!UICONTROL Add to Column Options]**，选择 `Yes`.

   - 对象 **[!UICONTROL Use in Filter Options]**，选择 `Yes`.

1. 单击 **[!UICONTROL Save Attribute]**.

![Amazon条件属性](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![“下一步”图标](assets/btn-next.png) [**继续添加或验证API密钥**](./amazon-verify-api-key.md)
