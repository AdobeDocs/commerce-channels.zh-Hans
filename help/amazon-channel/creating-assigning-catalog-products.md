---
title: 创建和分配产品
description: AmazonSales Channel提供了[!UICONTROL New Third Party]选项卡，以帮助创建和分配与Amazon列表匹配的商务目录产品。
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# 创建和分配产品

查看&#x200B;_[!UICONTROL New Third Party]_选项卡时，您可以将[!DNL Commerce]目录产品与现有的Amazon列表相匹配。 此匹配有两个选项。 您可以将列表分配给现有目录产品，也可以使用列表中的信息创建目录产品。 当您的Amazon列表与[!DNL Commerce]目录不自动匹配时，这些选项会很有帮助。

要使用Amazon销售渠道的完整功能集，必须将产品匹配（或分配）到Amazon列表。

从Amazon列表创建目录产品时：

- **ASIN**&#x200B;将变为[!DNL Commerce] SKU
- **产品列表名称**&#x200B;将变为目录列表名称
- **Price**&#x200B;和&#x200B;**Quantity**&#x200B;从Amazon列表导入

其余必要设置由创建过程中选择的[!DNL Commerce]产品设置决定。

创建并匹配列表后，该列表会从&#x200B;_[!UICONTROL New Third Party]_选项卡中删除，并显示在_[!UICONTROL Active]_&#x200B;选项卡中。

## 将单个目录产品分配给Amazon列表

1. 在[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡上查看您的产品清单。

1. 在列表中查找要分配的列表，单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**，然后单击&#x200B;**[!UICONTROL Assign Catalog Product]**。

   此操作将打开&#x200B;_[!UICONTROL Assign Magento Catalog Product]_页面。

1. 使用[工作区控件](./workspace-controls.md)浏览或过滤列表，并找到与列表匹配的相应目录产品。

1. 当列表中出现正确的产品时，单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Assign Catalog Product]**。

您的产品和列表现已匹配。 Amazon销售渠道现在可以与Amazon共享产品和列表数据，并管理您的列表及其信息，包括列表价格、运价、库存/数量、订单信息和状态等。

## 使用Amazon列表信息创建单个目录产品

1. 在[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡上查看您的产品清单。

1. 在[!DNL Commerce]目录中找到要创建的列表，单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Select]**，然后单击&#x200B;**[!UICONTROL Create New Catalog Product]**。

   此操作将打开&#x200B;_[!UICONTROL Create Magento Catalog Product]_页面。

1. 完成产品的目录设置。

   - 将&#x200B;**[!UICONTROL Enable Product(s)]**&#x200B;切换设置为`Yes`或`No`（必需）。

      |是|选择使产品符合[!DNL Commerce]店面销售条件。|
|否|选择使产品不符合[!DNL Commerce]店面销售的条件。|

   - 对于&#x200B;**[!UICONTROL Categories]**，为产品分配类别（可选）。

      要选择产品的类别，请单击向下箭头并选中类别复选框。 完成后单击&#x200B;**[!UICONTROL Done]**。

   - 对于&#x200B;**[!UICONTROL Website Ids]**，选择要关联产品的网站（商店）。

      此列表中的选项取决于您的[!DNL Commerce] [存储配置](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}设置。

   - 对于&#x200B;**[!UICONTROL Attribute Set Id]**（必需），选择一个选项。

      `Default` 是默认选项。此列表中的选项取决于您配置的[!DNL Commerce] [属性集](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}。

   - 对于&#x200B;**[!UICONTROL Visibility]**，为新产品选择一个选项。

      |**[!UICONTROL Not Visible Individually]**（默认）|该产品未包含在您的店面列表中，但可能作为其他产品的变体提供。|
|**[!UICONTROL Catalog]**|产品显示在您的目录列表中。|
|**[!UICONTROL Search]**|产品可用于搜索操作。|
|**[!UICONTROL Catalog and Search]**|产品包含在目录列表中并可用于搜索操作。|

   - 对于&#x200B;**[!UICONTROL Assign Tax Class]**，选择产品的选项。

      此列表中显示的选项取决于您配置的[税类](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}。

   - 完成后，单击&#x200B;**[!UICONTROL Create Catalog Products]**。

目录产品在[!DNL Commerce]目录中创建，并分配给从中创建该产品的Amazon列表。 现在，该列表与现有的Amazon列表相匹配，因此该列表会从&#x200B;_[!UICONTROL New Third Party]_选项卡中删除，并显示在_[!UICONTROL Active]_&#x200B;选项卡中。

## 使用其Amazon列表信息创建多个目录产品

1. 在[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡上查看您的产品清单。

1. 选择要为其创建目录产品的列表。

   您可以在左侧列中选择单个复选框，也可以单击左上角列中的向下箭头，然后选择&#x200B;**[!UICONTROL Select All]**&#x200B;或&#x200B;**[!UICONTROL Select All on this Page]**。

1. 在&#x200B;_[!UICONTROL Actions]_下，单击&#x200B;**[!UICONTROL Create New Catalog Product(s)]**。

1. 要接受确认消息并打开&#x200B;_[!UICONTROL Create Magento Catalog Product]_页面，请单击&#x200B;**[!UICONTROL OK]**。

1. 完成产品的目录设置。

   >[!NOTE]
   >为多个选定列表创建目录产品时，输入的产品设置将应用于所有列表。

   - 将&#x200B;**[!UICONTROL Enable Product(s)]**&#x200B;切换设置为`Yes`或`No`（必需）。

      |是|选择使产品符合[!DNL Commerce]店面销售条件。|
|否|选择使产品不符合[!DNL Commerce]店面销售的条件。|

   - 对于&#x200B;**[!UICONTROL Categories]**，为产品分配类别（可选）。

      要选择产品的类别，请单击向下箭头并选中类别复选框。 完成后，单击&#x200B;**完成**。

   - 对于&#x200B;**[!UICONTROL Website Ids]**，选择要关联产品的网站（商店）。

      此列表中的选项取决于您的[!DNL Commerce] [存储配置](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}设置。

   - 对于&#x200B;**[!UICONTROL Attribute Set Id]**（必需），选择一个选项。

      `Default` 是默认选项。此列表中的选项取决于您配置的[!DNL Commerce] [属性集](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}。

   - 对于&#x200B;**[!UICONTROL Visibility]**，为新产品选择一个选项。

      |**[!UICONTROL Not Visible Individually]**（默认）|该产品未包含在您的店面列表中，但可能作为其他产品的变体提供。|
|**[!UICONTROL Catalog]**|产品显示在您的目录列表中。|
|**[!UICONTROL Search]**|产品可用于搜索操作。|
|**[!UICONTROL Catalog and Search]**|产品包含在目录列表中并可用于搜索操作。|

   - 对于&#x200B;**[!UICONTROL Assign Tax Class]**，选择产品的选项。

      此列表中显示的选项取决于您配置的[税类](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}。

   - 完成后，单击&#x200B;**[!UICONTROL Create Catalog Products]**。

目录产品在[!DNL Commerce]目录中创建，并分配给从中创建该目录的Amazon列表。 如果列表现在与各自的Amazon列表相匹配，则将从[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)选项卡中删除列表，并显示在[_[!UICONTROL Active]_](./active-listings.md)选项卡中。

![创建商务目录产品](assets/amazon-magento-catalog-product.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Enable Product(s)] | （必需）如果启用，则产品将显示在[!DNL Commerce]店面中。 如果禁用，则产品不会显示在[!DNL Commerce]店面中。 |
| [!UICONTROL Categories] | 您可以输入新产品的类别名称，或通过单击向下箭头选择类别以显示选项。 选项取决于您的[类别](https://docs.magento.com/user-guide/catalog/category-create.html){target=&quot;_blank&quot;}配置。 |
| [!UICONTROL Website Ids] | （必需）选择要关联产品的网站（商店）。 选项取决于您的[!DNL Commerce] [存储配置](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}设置 |
| 属性集Id | 选择属性集。 选项取决于您配置的[!DNL Commerce] [属性集](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}。 |
| [!UICONTROL Visibility] | 选项：<ul><li>**[!UICONTROL Not Visible Individually]**  — 产品在店面中不可见( [!DNL Commerce] 变体产品最常见)。</li><li>**[!UICONTROL Catalog]**  — 允许通过与产品在网站中关联的类别访问产品。</li><li>**搜索**  — 仅允许通过搜索工具找到产品。</li><li>**[!UICONTROL Catalog and Search]**  — 允许通过类别结构和使用搜索工具访问产品。</li></ul> |
| [!UICONTROL Assign Tax Class] | 为新产品分配税类。 选项取决于您配置的[税类](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}。 |
