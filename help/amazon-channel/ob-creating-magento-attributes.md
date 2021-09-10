---
title: 为Amazon创建 [!DNL Commerce] 属性
description: 在完成Amazon销售渠道载入过程之前，请确保您具有所需的[!UICONTROL Commerce]产品属性。
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# 为Amazon创建[!DNL Commerce]属性

在载入[!DNL Amazon Seller Central]帐户之前，最好添加[!DNL Commerce] [产品属性](https://docs.magento.com/user-guide/stores/attributes-product.html){:target=&quot;_blank&quot;}以映射产品列表。 完成入门后，您可以通过[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面的[属性](./managing-attributes.md)选项卡管理产品属性。

这些说明详细说明了如何为Amazon ASIN和Amazon条件创建[!DNL Commerce]属性。 建议创建其他属性，包括Amazon EAN、Amazon ISBN和Amazon UPC。 如果要将Amazon上市价格用作定价规则的价格来源，则可能还需要创建Amazon价格属性。 在入门过程中配置列表和定价设置时，会使用这些属性。 在创建Amazon列表以及更新[!DNL Commerce]目录并将其与Amazon列表同步时，还可以使用这些属性。

“目录搜索”设置允许您设置匹配的搜索参数，以帮助将符合条件的[!DNL Commerce]产品与Amazon列表进行映射。 映射后，Amazon将激活与定价、数量、改写以及订单和产品同步相关的活动。

定义这些值会增加进行精确匹配的可能性，从而最大限度地减少以后手动匹配产品清单的需要。 将属性添加为载入[预设置任务](./amazon-pre-setup-tasks.md)的一部分，Amazon销售渠道在载入过程中自动匹配您的产品，并在载入后在Amazon和[!DNL Commerce]之间同步产品数据，这种可能性更大。

如果仅创建Amazon ASIN属性（不为每个产品添加ASIN值），则您的[!DNL Commerce]产品可能不会自动与您的Amazon列表匹配。 您可以通过&#x200B;_Store Review_&#x200B;手动匹配您的产品。 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您为手动匹配的产品更新ASIN、UPC或其他数据元素，则必须在以下两处更新数据：[!DNL Commerce]目录和[!DNL Amazon Seller Central]帐户中的列表。

## 创建Amazon ASIN产品属性

1. 登录[!DNL Commerce]管理员。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Stores]**。

1. 在&#x200B;_[!UICONTROL Attributes]_部分中，单击&#x200B;**[!UICONTROL Product]**。

1. 要打开属性属性，请单击&#x200B;**[!UICONTROL Add New Attribute]**。

1. 对于&#x200B;**[!UICONTROL Default Label]**，输入`Amazon ASIN`（属性的名称）。

1. 对于&#x200B;**[!UICONTROL Catalog Input Type for Store Owner]**，选择`Text Field`。

1. 对于&#x200B;**[!UICONTROL Values Required]**，选择`No`。

   尽管在Amazon上列出产品需要Amazon ASIN，但您的某些目录产品可能未在Amazon上列出。

1. 展开&#x200B;_[!UICONTROL Advanced Attribute Properties]_部分并设置选项：

   - 对于&#x200B;**[!UICONTROL Attribute Code]**，输入`amazon_asin`。

   - 对于&#x200B;**[!UICONTROL Scope]**，选择`Global`。

   - 对于&#x200B;**[!UICONTROL Unique Value]**，选择`No`。

   - 对于&#x200B;**[!UICONTROL Input Validation for Store Owner]**，选择`None`。

   - 对于&#x200B;**[!UICONTROL Add to Column Options]**，选择`Yes`。

   - 对于&#x200B;**[!UICONTROL Use in Filter Options]**，选择`Yes`。

1. 单击&#x200B;**[!UICONTROL Save Attribute]**。

![Amazon ASIN属性](assets/creating-asin-attribute.png)

## 创建Amazon条件产品属性

1. 登录[!DNL Commerce]管理员。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Stores]**。

1. 在&#x200B;_[!UICONTROL Attributes]_部分中，单击&#x200B;**[!UICONTROL Product]**。

1. 要打开属性属性，请单击&#x200B;**[!UICONTROL Add New Attribute]**。

1. 对于&#x200B;**[!UICONTROL Default Label]**，输入`Amazon Condition`（属性的名称）。

1. 对于&#x200B;**[!UICONTROL Catalog Input Type for Store Owner]**，选择`Dropdown`。

   出现&#x200B;_[!UICONTROL Manage Options (Values of your Attribute)]_部分。

1. 对于&#x200B;**[!UICONTROL Values Required]**，选择`No`。

1. 对于&#x200B;**[!UICONTROL Manage Options (Values for your Attribute)]**，添加每个条件选项。

   标准Amazon条件包括：

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. 单击&#x200B;**[!UICONTROL Add Option]**。

1. 为希望作为默认选择的条件选择&#x200B;**[!UICONTROL Is Default]**&#x200B;选项。

1. 在&#x200B;_[!UICONTROL Admin]_列中，输入要添加条件的标签的文本（如`New`、`Used`和`Used-Like New`）

1. 根据需要，单击&#x200B;**[!UICONTROL Add Option]**&#x200B;以添加更多选项。

1. 展开&#x200B;_[!UICONTROL Advanced Attribute Properties]_部分并设置选项。

   - 对于&#x200B;**[!UICONTROL Attribute Code]**，输入`amazon_condition`。

   - 对于&#x200B;**[!UICONTROL Scope]**，选择`Global`。

   - 对于&#x200B;**[!UICONTROL Unique Value]**，选择`No`。

   - 对于&#x200B;**[!UICONTROL Input Validation for Store Owner]**，选择`None`。

   - 对于&#x200B;**[!UICONTROL Add to Column Options]**，选择`Yes`。

   - 对于&#x200B;**[!UICONTROL Use in Filter Options]**，选择`Yes`。

1. 单击&#x200B;**[!UICONTROL Save Attribute]**。

![Amazon条件属性](assets/creating-amazon-condition-attribute.png)

![下一](assets/btn-next.png) [**个图标继续添加或验证API密钥**](./amazon-verify-api-key.md)
