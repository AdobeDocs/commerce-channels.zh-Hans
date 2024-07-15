---
title: 为Amazon创建Commerce属性
description: 在完成Amazon Sales Channel新用户引导过程之前，请确保您具有所需的[!UICONTROL Commerce]产品属性。
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 为Amazon创建Commerce属性

在登录[!DNL Amazon Seller Central]帐户之前，最佳做法是添加[!DNL Commerce] [产品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)以映射您的产品列表。 完成入门培训后，您可以通过[Amazon销售渠道主页](./amazon-sales-channel-home.md)页面的[属性](./managing-attributes.md)选项卡来管理您的产品属性。

这些说明详细说明了如何为Amazon ASIN和Amazon条件创建[!DNL Commerce]属性。 建议创建其他属性，包括Amazon EAN、Amazon ISBN和Amazon UPC。 如果要使用Amazon的上市价格作为定价规则的价格来源，则可能还希望创建Amazon价格属性。 在新用户引导期间配置您的列表和定价设置时，将使用这些属性。 在创建Amazon列表以及将[!DNL Commerce]目录更新并与Amazon列表同步时，也可以使用这些属性。

目录搜索设置允许您设置匹配的搜索参数，这些参数有助于将合格的[!DNL Commerce]产品映射到Amazon列表。 在映射后，Amazon会激活与定价、数量、覆盖以及订单和产品同步相关的操作。

定义这些值会增加完全匹配的可能性，从而最大限度地减少以后手动匹配产品清单的需求。 将属性添加为载入[预设置任务](./amazon-pre-setup-tasks.md)的一部分，Amazon销售渠道在载入期间自动匹配您的产品以及在载入后Amazon和[!DNL Commerce]之间同步产品数据的可能性更高。

如果仅创建Amazon ASIN属性（不添加每个产品的ASIN值），则您的[!DNL Commerce]产品可能会自动与您的Amazon列表不匹配。 您可以通过&#x200B;_商店评论_&#x200B;手动匹配您的产品。 但是，手动匹配不会创建共享和同步产品数据所需的数据元素。

>[!IMPORTANT]
>
>如果您为手动匹配的产品更新ASIN、UPC或其他数据元素，则必须更新两个位置的数据：您的[!DNL Commerce]目录和[!DNL Amazon Seller Central]帐户中的列表。

## 创建Amazon ASIN产品属性

1. 登录[!DNL Commerce]管理员。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Stores]**。

1. 在&#x200B;_[!UICONTROL Attributes]_部分中，单击&#x200B;**[!UICONTROL Product]**。

1. 要打开属性属性，请单击&#x200B;**[!UICONTROL Add New Attribute]**。

1. 对于&#x200B;**[!UICONTROL Default Label]**，输入`Amazon ASIN` （属性的名称）。

1. 对于&#x200B;**[!UICONTROL Catalog Input Type for Store Owner]**，请选择`Text Field`。

1. 对于&#x200B;**[!UICONTROL Values Required]**，请选择`No`。

   尽管Amazon ASIN需要在Amazon上列出产品，但您的某些目录产品可能未在Amazon上列出。

1. 展开&#x200B;_[!UICONTROL Advanced Attribute Properties]_部分并设置选项：

   - 对于&#x200B;**[!UICONTROL Attribute Code]**，输入`amazon_asin`。

   - 对于&#x200B;**[!UICONTROL Scope]**，请选择`Global`。

   - 对于&#x200B;**[!UICONTROL Unique Value]**，请选择`No`。

   - 对于&#x200B;**[!UICONTROL Input Validation for Store Owner]**，请选择`None`。

   - 对于&#x200B;**[!UICONTROL Add to Column Options]**，请选择`Yes`。

   - 对于&#x200B;**[!UICONTROL Use in Filter Options]**，请选择`Yes`。

1. 单击&#x200B;**[!UICONTROL Save Attribute]**。

![Amazon ASIN属性](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## 创建“Amazon条件”产品属性

1. 登录[!DNL Commerce]管理员。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Stores]**。

1. 在&#x200B;_[!UICONTROL Attributes]_部分中，单击&#x200B;**[!UICONTROL Product]**。

1. 要打开属性属性，请单击&#x200B;**[!UICONTROL Add New Attribute]**。

1. 对于&#x200B;**[!UICONTROL Default Label]**，输入`Amazon Condition` （属性的名称）。

1. 对于&#x200B;**[!UICONTROL Catalog Input Type for Store Owner]**，请选择`Dropdown`。

   将显示&#x200B;_[!UICONTROL Manage Options (Values of your Attribute)]_部分。

1. 对于&#x200B;**[!UICONTROL Values Required]**，请选择`No`。

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

1. 在&#x200B;_[!UICONTROL Admin]_列中，输入要添加的条件的标签文本（如`New`、`Used`和`Used-Like New`）

1. 单击&#x200B;**[!UICONTROL Add Option]**&#x200B;以根据需要添加更多选项。

1. 展开&#x200B;_[!UICONTROL Advanced Attribute Properties]_部分并设置选项。

   - 对于&#x200B;**[!UICONTROL Attribute Code]**，输入`amazon_condition`。

   - 对于&#x200B;**[!UICONTROL Scope]**，请选择`Global`。

   - 对于&#x200B;**[!UICONTROL Unique Value]**，请选择`No`。

   - 对于&#x200B;**[!UICONTROL Input Validation for Store Owner]**，请选择`None`。

   - 对于&#x200B;**[!UICONTROL Add to Column Options]**，请选择`Yes`。

   - 对于&#x200B;**[!UICONTROL Use in Filter Options]**，请选择`Yes`。

1. 单击&#x200B;**[!UICONTROL Save Attribute]**。

![Amazon条件属性](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![下一个图标](assets/btn-next.png) [**继续添加或验证API密钥**](./amazon-verify-api-key.md)
