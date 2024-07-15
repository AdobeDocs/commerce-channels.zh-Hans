---
title: 为Amazon销售渠道创建和分配产品
description: AmazonSales Channel提供了[!UICONTROL New Third Party]选项卡来帮助创建和分配具有Amazon列表的匹配Commerce目录产品。
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# 创建和分配产品

查看&#x200B;_[!UICONTROL New Third Party]_选项卡时，您可以将[!DNL Commerce]目录产品与现有的Amazon列表相匹配。 此匹配有两个选项。 您可以将列表分配给现有目录产品，也可以使用列表中的信息创建目录产品。 当您的Amazon列表与您的[!DNL Commerce]目录不自动匹配时，这些选项非常有用。

要使用Amazon销售渠道的完整功能集，必须将您的产品与Amazon列表进行匹配（或分配）。

从Amazon列表创建目录产品时：

- **ASIN**&#x200B;成为[!DNL Commerce] SKU
- **产品列表名称**&#x200B;成为目录列表名称
- **价格**&#x200B;和&#x200B;**数量**&#x200B;已从Amazon列表中导入

其余必要设置由您在创建期间选择的[!DNL Commerce]产品设置决定。

创建并匹配列表后，这些列表将从&#x200B;_[!UICONTROL New Third Party]_选项卡中移除并显示在_[!UICONTROL Active]_&#x200B;选项卡中。

## 将单个目录产品分配给Amazon列表

1. 在[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡上查看您的产品清单。

1. 查找要分配到该列表中的列表，单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**，然后单击&#x200B;**[!UICONTROL Assign Catalog Product]**。

   此操作打开&#x200B;_[!UICONTROL Assign Magento Catalog Product]_页面。

1. 使用[工作区控件](./workspace-controls.md)浏览或筛选列表，并找到与列表匹配的相应目录产品。

1. 当正确的产品出现在列表中时，单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Assign Catalog Product]**。

您的产品和列表现已匹配。 Amazon sales channel现在可以与Amazon共享产品和列表数据，并管理您的列表及其信息，包括列表价格、发货价、库存/数量、订单信息和状态等。

## 使用Amazon列表信息创建单个目录产品

1. 在[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡上查看您的产品清单。

1. 在[!DNL Commerce]目录中查找要创建的列表，在&#x200B;_[!UICONTROL Action]_列中单击&#x200B;**[!UICONTROL Select]**，然后单击&#x200B;**[!UICONTROL Create New Catalog Product]**。

   此操作打开&#x200B;_[!UICONTROL Create Magento Catalog Product]_页面。

1. 完成产品的目录设置。

   - 将&#x200B;**[!UICONTROL Enable Product(s)]**&#x200B;切换设置为`Yes`或`No`（必需）。

     |是|选择使产品适用于您的[!DNL Commerce]店面销售。|
|否|选择使产品不符合[!DNL Commerce]店面销售的资格。|

   - 为&#x200B;**[!UICONTROL Categories]**&#x200B;分配产品的类别（可选）。

     要选择产品的类别，请单击向下箭头并选中类别复选框。 完成后单击&#x200B;**[!UICONTROL Done]**。

   - 对于&#x200B;**[!UICONTROL Website Ids]**，选择要关联产品的网站（店面）。

     此列表中的选项取决于您的[!DNL Commerce] [存储配置](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html)设置。

   - 对于&#x200B;**[!UICONTROL Attribute Set Id]** （必需），请选择一个选项。

     `Default`是默认选项。 此列表中的选项取决于您已配置的[!DNL Commerce] [属性集](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html)。

   - 对于&#x200B;**[!UICONTROL Visibility]**，请选择新产品的选项。

     |**[!UICONTROL Not Visible Individually]** （默认）|此产品未包含在您的店面清单中，尽管它可能作为其他产品的变体提供。|
|**[!UICONTROL Catalog]**|产品出现在您的目录列表中。|
|**[!UICONTROL Search]**|该产品可用于搜索操作。|
|**[!UICONTROL Catalog and Search]**|产品包含在目录列表中，可用于搜索操作。|

   - 对于&#x200B;**[!UICONTROL Assign Tax Class]**，请选择产品的选项。

     此列表中显示的选项取决于您配置的[税类](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html)。

   - 完成后，单击&#x200B;**[!UICONTROL Create Catalog Products]**。

目录产品在您的[!DNL Commerce]目录中创建，并分配给创建该产品的Amazon列表。 由于该列表现在与现有的Amazon列表匹配，因此该列表将从&#x200B;_[!UICONTROL New Third Party]_选项卡中移除并显示在_[!UICONTROL Active]_&#x200B;选项卡中。

## 使用其Amazon列表信息创建多个目录产品

1. 在[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡上查看您的产品清单。

1. 选择要为其创建目录产品的列表。

   您可以选择左侧列中的单个复选框，也可以单击左上列中的向下箭头并选择&#x200B;**[!UICONTROL Select All]**&#x200B;或&#x200B;**[!UICONTROL Select All on this Page]**。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Create New Catalog Product(s)]**。

1. 要接受确认消息并打开&#x200B;_[!UICONTROL Create Magento Catalog Product]_页面，请单击&#x200B;**[!UICONTROL OK]**。

1. 完成产品的目录设置。

   >[!NOTE]
   >为多个选定列表创建目录产品时，输入的产品设置将应用于所有列表。

   - 将&#x200B;**[!UICONTROL Enable Product(s)]**&#x200B;切换设置为`Yes`或`No`（必需）。

     |是|选择使产品适用于您的[!DNL Commerce]店面销售。|
|否|选择使产品不符合[!DNL Commerce]店面销售的资格。|

   - 为&#x200B;**[!UICONTROL Categories]**&#x200B;分配产品的类别（可选）。

     要选择产品的类别，请单击向下箭头并选中类别复选框。 完成后单击&#x200B;**完成**。

   - 对于&#x200B;**[!UICONTROL Website Ids]**，选择要关联产品的网站（店面）。

     此列表中的选项取决于您的[!DNL Commerce] [存储配置](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html)设置。

   - 对于&#x200B;**[!UICONTROL Attribute Set Id]** （必需），请选择一个选项。

     `Default`是默认选项。 此列表中的选项取决于您已配置的[!DNL Commerce] [属性集](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html)。

   - 对于&#x200B;**[!UICONTROL Visibility]**，请选择新产品的选项。

     |**[!UICONTROL Not Visible Individually]** （默认）|此产品未包含在您的店面清单中，尽管它可能作为其他产品的变体提供。|
|**[!UICONTROL Catalog]**|产品出现在您的目录列表中。|
|**[!UICONTROL Search]**|该产品可用于搜索操作。|
|**[!UICONTROL Catalog and Search]**|产品包含在目录列表中，可用于搜索操作。|

   - 对于&#x200B;**[!UICONTROL Assign Tax Class]**，请选择产品的选项。

     此列表中显示的选项取决于您配置的[税类](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html)。

   - 完成后，单击&#x200B;**[!UICONTROL Create Catalog Products]**。

目录产品在您的[!DNL Commerce]目录中创建，并分配给创建该目录的Amazon列表。 由于这些列表现在与它们各自的Amazon列表匹配，因此这些列表将从[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡中删除并显示在[_[!UICONTROL Active]_](./active-listings.md)选项卡中。

![创建Commerce目录产品](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | （必需）如果启用，产品将显示在您的[!DNL Commerce]店面中。 如果禁用，产品将不会显示在您的[!DNL Commerce]店面中。 |
| [!UICONTROL Categories] | 您可以输入新产品的类别名称，也可以通过单击向下箭头显示选项来选择类别。 选项取决于您的[类别](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html)配置。 |
| [!UICONTROL Website Ids] | （必需）选择要关联产品的网站（店面）。 选项取决于您的[!DNL Commerce] [存储配置](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html)设置 |
| 属性集ID | 选择属性集。 选项取决于您配置的[!DNL Commerce] [属性集](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html)。 |
| [!UICONTROL Visibility] | 选项：<ul><li>**[!UICONTROL Not Visible Individually]** — 该产品在您的[!DNL Commerce]店面中不可见（最常见于变体产品）。</li><li>**[!UICONTROL Catalog]** — 允许通过网站中与产品关联的类别访问产品。</li><li>**搜索** — 仅允许通过搜索工具找到产品。</li><li>**[!UICONTROL Catalog and Search]** — 允许通过类别结构和使用搜索工具访问产品。</li></ul> |
| [!UICONTROL Assign Tax Class] | 将税分类分配给新产品。 选项取决于您配置的[税类](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html)。 |
