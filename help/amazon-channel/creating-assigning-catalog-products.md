---
title: 为Amazon销售渠道创建和分配产品
description: AmazonSales Channel提供 [!UICONTROL New Third Party] 选项卡以帮助创建和分配包含Amazon列表的匹配Commerce目录产品。
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# 创建和分配产品

查看时 _[!UICONTROL New Third Party]_选项卡，您可以 [!DNL Commerce] 将产品目录添加到现有Amazon列表。 此匹配有两个选项。 您可以将列表分配给现有目录产品，也可以使用列表中的信息创建目录产品。 当您的Amazon列表未自动与您的匹配时，这些选项非常有用 [!DNL Commerce] 目录。

要使用Amazon销售渠道的完整功能集，必须将您的产品与Amazon列表进行匹配（或分配）。

从Amazon列表创建目录产品时：

- 此 **ASIN** 变为 [!DNL Commerce] SKU
- 此 **产品列表名称** 成为目录列表名称
- 此 **价格** 和 **数量** 从Amazon列表中导入

其余必要设置由 [!DNL Commerce] 您在创建期间选择的产品设置。

创建并匹配列表后，这些列表将从 _[!UICONTROL New Third Party]_选项卡，并显示在_[!UICONTROL Active]_ 选项卡。

## 将单个目录产品分配给Amazon列表

1. 查看您的产品列表 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡。

1. 在列表中查找要分配的列表，单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列，然后单击&#x200B;**[!UICONTROL Assign Catalog Product]**.

   此操作将打开 _[!UICONTROL Assign Magento Catalog Product]_页面。

1. 使用浏览或筛选列表 [工作区控件](./workspace-controls.md) 并找到适合列出的目录产品。

1. 当正确的产品出现在列表中时，单击 **[!UICONTROL Assign Catalog Product]** 在 _[!UICONTROL Action]_列。

您的产品和列表现已匹配。 Amazon sales channel现在可以与Amazon共享产品和列表数据，并管理您的列表及其信息，包括列表价格、发货价、库存/数量、订单信息和状态等。

## 使用Amazon列表信息创建单个目录产品

1. 查看您的产品列表 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡。

1. 查找您要在 [!DNL Commerce] 目录，单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列，然后单击&#x200B;**[!UICONTROL Create New Catalog Product]**.

   此操作将打开 _[!UICONTROL Create Magento Catalog Product]_页面。

1. 完成产品的目录设置。

   - 设置 **[!UICONTROL Enable Product(s)]** 切换到 `Yes` 或 `No` （必需）。

     |是|选择使产品符合您的 [!DNL Commerce] 店面销售。| |否|选择使产品不符合 [!DNL Commerce] 店面销售。|

   - 对象 **[!UICONTROL Categories]**，为产品分配类别（可选）。

     要选择产品的类别，请单击向下箭头并选中类别复选框。 单击 **[!UICONTROL Done]** 完成后。

   - 对象 **[!UICONTROL Website Ids]**，选择要关联产品的网站（店面）。

     此列表中的选项取决于 [!DNL Commerce] [存储配置](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 设置。

   - 对象 **[!UICONTROL Attribute Set Id]** （必需），选择一个选项。

     `Default` 是默认选项。 此列表中的选项取决于 [!DNL Commerce] [属性集](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) 您已配置。

   - 对象 **[!UICONTROL Visibility]**，为新产品选择一个选项。

     |**[!UICONTROL Not Visible Individually]** （默认）|此产品未包含在您的店面清单中，尽管它可能作为其他产品的变体提供。| |**[!UICONTROL Catalog]**|产品显示在您的目录列表中。| |**[!UICONTROL Search]**|该产品可用于搜索操作。| |**[!UICONTROL Catalog and Search]**|产品包含在目录列表中，可用于搜索操作。|

   - 对象 **[!UICONTROL Assign Tax Class]**，为产品选择一个选项。

     此列表中显示的选项取决于 [税种](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) 您已配置。

   - 完成后，单击 **[!UICONTROL Create Catalog Products]**.

目录产品是在以下位置创建的： [!DNL Commerce] 目录并分配到从中创建它的Amazon列表。 由于该列表现在与现有的Amazon列表相匹配，因此将从列表中删除该列表。 _[!UICONTROL New Third Party]_选项卡，并显示在_[!UICONTROL Active]_ 选项卡。

## 使用其Amazon列表信息创建多个目录产品

1. 查看您的产品列表 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡。

1. 选择要为其创建目录产品的列表。

   您可以选中左栏中的各个复选框，也可以单击左上栏中的向下箭头并选择 **[!UICONTROL Select All]** 或 **[!UICONTROL Select All on this Page]**.

1. 下 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Create New Catalog Product(s)]**.

1. 要接受确认消息并打开 _[!UICONTROL Create Magento Catalog Product]_页面，单击&#x200B;**[!UICONTROL OK]**.

1. 完成产品的目录设置。

   >[!NOTE]
   >为多个选定列表创建目录产品时，输入的产品设置将应用于所有列表。

   - 设置 **[!UICONTROL Enable Product(s)]** 切换到 `Yes` 或 `No` （必需）。

     |是|选择使产品符合您的 [!DNL Commerce] 店面销售。| |否|选择使产品不符合 [!DNL Commerce] 店面销售。|

   - 对象 **[!UICONTROL Categories]**，为产品分配类别（可选）。

     要选择产品的类别，请单击向下箭头并选中类别复选框。 单击 **完成** 完成后。

   - 对象 **[!UICONTROL Website Ids]**，选择要关联产品的网站（店面）。

     此列表中的选项取决于 [!DNL Commerce] [存储配置](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 设置。

   - 对象 **[!UICONTROL Attribute Set Id]** （必需），选择一个选项。

     `Default` 是默认选项。 此列表中的选项取决于 [!DNL Commerce] [属性集](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) 您已配置。

   - 对象 **[!UICONTROL Visibility]**，为新产品选择一个选项。

     |**[!UICONTROL Not Visible Individually]** （默认）|此产品未包含在您的店面清单中，尽管它可能作为其他产品的变体提供。| |**[!UICONTROL Catalog]**|产品显示在您的目录列表中。| |**[!UICONTROL Search]**|该产品可用于搜索操作。| |**[!UICONTROL Catalog and Search]**|产品包含在目录列表中，可用于搜索操作。|

   - 对象 **[!UICONTROL Assign Tax Class]**，为产品选择一个选项。

     此列表中显示的选项取决于 [税种](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) 您已配置。

   - 完成后，单击 **[!UICONTROL Create Catalog Products]**.

目录产品是在 [!DNL Commerce] 目录并分配到从中创建它的Amazon列表。 由于这些列表现在与它们各自的Amazon列表相匹配，因此将从列表中移除这些列表。 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡，并显示在 [_[!UICONTROL Active]_](./active-listings.md) 选项卡。

![创建Commerce目录产品](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | （必需）如果启用，产品将在 [!DNL Commerce] 店面。 如果禁用，产品将不会显示在您的 [!DNL Commerce] 店面。 |
| [!UICONTROL Categories] | 您可以输入新产品的类别名称，也可以通过单击向下箭头显示选项来选择类别。 具体选项取决于贵机构的 [类别](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) 配置。 |
| [!UICONTROL Website Ids] | （必需）选择要关联产品的网站（店面）。 具体选项取决于贵机构的 [!DNL Commerce] [存储配置](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 设置 |
| 属性集ID | 选择属性集。 选项取决于您配置的 [!DNL Commerce] [属性集](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | 选项：<ul><li>**[!UICONTROL Not Visible Individually]**  — 您的页面中看不到该产品 [!DNL Commerce] storefront（最常见于变体产品）。</li><li>**[!UICONTROL Catalog]**  — 允许通过网站中与产品关联的类别访问产品。</li><li>**Search**  — 允许仅通过搜索工具找到产品。</li><li>**[!UICONTROL Catalog and Search]**  — 允许通过类别结构和使用搜索工具访问产品。</li></ul> |
| [!UICONTROL Assign Tax Class] | 将税分类分配给新产品。 选项取决于您配置的 [税种](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
