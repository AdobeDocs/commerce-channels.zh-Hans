---
title: 创建 [!DNL Commerce] Amazon属性
description: 在完成Amazon销售渠道载入流程之前，请确保您拥有所需的 [!UICONTROL Commerce] 产品属性。
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# 创建 [!DNL Commerce] Amazon属性

登录之前 [!DNL Amazon Seller Central] 帐户，则最好在 [!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}以映射您的产品列表。 完成入门后，您可以通过 [属性](./managing-attributes.md) 选项卡 [Amazon销售渠道主页](./amazon-sales-channel-home.md) 页面。

这些说明详细说明了如何创建 [!DNL Commerce] 属性来访问Amazon ASIN和Amazon条件。 建议创建其他属性，包括Amazon EAN、Amazon ISBN和Amazon UPC。 如果要将Amazon上市价格用作定价规则的价格来源，则可能还需要创建Amazon价格属性。 在入门过程中配置列表和定价设置时，会使用这些属性。 在创建Amazon列表以及更新和同步您的 [!DNL Commerce] 目录。

“目录搜索”设置允许您设置匹配的搜索参数，以帮助映射符合条件的 [!DNL Commerce] 产品。 映射后，Amazon将激活与定价、数量、改写以及订单和产品同步相关的活动。

定义这些值会增加进行精确匹配的可能性，从而最大限度地减少以后手动匹配产品清单的需要。 在载入中添加属性 [预设置任务](./amazon-pre-setup-tasks.md)，则Amazon销售渠道在Amazon和 [!DNL Commerce] 入门后。

如果仅创建Amazon ASIN属性（不为每个产品添加ASIN值），则您的 [!DNL Commerce] 产品可能不会自动与您的Amazon列表匹配。 您可以通过 _商店评论_. 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您为手动匹配的产品更新ASIN、UPC或其他数据元素，则必须在以下两处更新数据：您的 [!DNL Commerce] 目录和 [!DNL Amazon Seller Central] 帐户。

## 创建Amazon ASIN产品属性

1. 登录 [!DNL Commerce] 管理员。

1. 单击 **[!UICONTROL Stores]** 的双曲余切值。

1. 在 _[!UICONTROL Attributes]_，单击&#x200B;**[!UICONTROL Product]**.

1. 要打开属性属性，请单击 **[!UICONTROL Add New Attribute]**.

1. 对于 **[!UICONTROL Default Label]**，输入 `Amazon ASIN` （属性的名称）。

1. 对于 **[!UICONTROL Catalog Input Type for Store Owner]**，选择 `Text Field`.

1. 对于 **[!UICONTROL Values Required]**，选择 `No`.

   尽管在Amazon上列出产品需要Amazon ASIN，但您的某些目录产品可能未在Amazon上列出。

1. 展开 _[!UICONTROL Advanced Attribute Properties]_，并设置选项：

   - 对于 **[!UICONTROL Attribute Code]**，输入 `amazon_asin`.

   - 对于 **[!UICONTROL Scope]**，选择 `Global`.

   - 对于 **[!UICONTROL Unique Value]**，选择 `No`.

   - 对于 **[!UICONTROL Input Validation for Store Owner]**，选择 `None`.

   - 对于 **[!UICONTROL Add to Column Options]**，选择 `Yes`.

   - 对于 **[!UICONTROL Use in Filter Options]**，选择 `Yes`.

1. 单击 **[!UICONTROL Save Attribute]**.

![Amazon ASIN属性](assets/creating-asin-attribute.png)

## 创建Amazon条件产品属性

1. 登录 [!DNL Commerce] 管理员。

1. 单击 **[!UICONTROL Stores]** 的双曲余切值。

1. 在 _[!UICONTROL Attributes]_，单击&#x200B;**[!UICONTROL Product]**.

1. 要打开属性属性，请单击 **[!UICONTROL Add New Attribute]**.

1. 对于 **[!UICONTROL Default Label]**，输入 `Amazon Condition` （属性的名称）。

1. 对于 **[!UICONTROL Catalog Input Type for Store Owner]**，选择 `Dropdown`.

   的 _[!UICONTROL Manage Options (Values of your Attribute)]_的上界。

1. 对于 **[!UICONTROL Values Required]**，选择 `No`.

1. 对于 **[!UICONTROL Manage Options (Values for your Attribute)]**，添加每个条件选项。

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

1. 选择 **[!UICONTROL Is Default]** 选项。

1. 在 _[!UICONTROL Admin]_列中，输入所添加条件的标签的文本(例如 `New`, `Used`和 `Used-Like New`)

1. 单击 **[!UICONTROL Add Option]** 以根据需要添加更多选项。

1. 展开 _[!UICONTROL Advanced Attribute Properties]_，并设置选项。

   - 对于 **[!UICONTROL Attribute Code]**，输入 `amazon_condition`.

   - 对于 **[!UICONTROL Scope]**，选择 `Global`.

   - 对于 **[!UICONTROL Unique Value]**，选择 `No`.

   - 对于 **[!UICONTROL Input Validation for Store Owner]**，选择 `None`.

   - 对于 **[!UICONTROL Add to Column Options]**，选择 `Yes`.

   - 对于 **[!UICONTROL Use in Filter Options]**，选择 `Yes`.

1. 单击 **[!UICONTROL Save Attribute]**.

![Amazon条件属性](assets/creating-amazon-condition-attribute.png)

![下一个图标](assets/btn-next.png) [**继续添加或验证API密钥**](./amazon-verify-api-key.md)
