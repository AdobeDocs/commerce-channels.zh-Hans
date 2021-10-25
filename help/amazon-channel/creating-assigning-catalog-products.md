---
title: 创建和分配产品
description: AmazonSales Channel提供 [!UICONTROL New Third Party] 选项卡，帮助创建和分配与Amazon列表匹配的商务目录产品。
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# 创建和分配产品

查看 _[!UICONTROL New Third Party]_选项卡，您可以 [!DNL Commerce] 将产品目录添加到现有Amazon列表。 此匹配有两个选项。 您可以将列表分配给现有目录产品，也可以使用列表中的信息创建目录产品。 当您的Amazon列表不自动与 [!DNL Commerce] 目录。

要使用Amazon销售渠道的完整功能集，必须将产品匹配（或分配）到Amazon列表。

从Amazon列表创建目录产品时：

- 的 **阿辛** 变为 [!DNL Commerce] SKU
- 的 **产品列表名称** 成为目录列表名称
- 的 **价格** 和 **数量** 从Amazon列表导入

其余的必要设置由 [!DNL Commerce] 您在创建过程中选择的产品设置。

创建并匹配列表后，将从 _[!UICONTROL New Third Party]_选项卡，并显示在_[!UICONTROL Active]_ 选项卡。

## 将单个目录产品分配给Amazon列表

1. 在 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡。

1. 在列表中查找要分配的列表，单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列，然后单击&#x200B;**[!UICONTROL Assign Catalog Product]**.

   此操作将打开 _[!UICONTROL Assign Magento Catalog Product]_页面。

1. 使用 [工作区控件](./workspace-controls.md) 并找到与列表匹配的相应目录产品。

1. 当列表中出现正确的产品时，单击 **[!UICONTROL Assign Catalog Product]** 在 _[!UICONTROL Action]_列。

您的产品和列表现已匹配。 Amazon销售渠道现在可以与Amazon共享产品和列表数据，并管理您的列表及其信息，包括列表价格、运价、库存/数量、订单信息和状态等。

## 使用Amazon列表信息创建单个目录产品

1. 在 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡。

1. 在 [!DNL Commerce] 目录，单击 **[!UICONTROL Select]** 在 _[!UICONTROL Action]_列，然后单击&#x200B;**[!UICONTROL Create New Catalog Product]**.

   此操作将打开 _[!UICONTROL Create Magento Catalog Product]_页面。

1. 完成产品的目录设置。

   - 已设置 **[!UICONTROL Enable Product(s)]** 切换至 `Yes` 或 `No` （必需）。

      |是|选择使产品符合您的 [!DNL Commerce] 店面销售。| |否|选择使产品不符合您的 [!DNL Commerce] 店面销售。|

   - 对于 **[!UICONTROL Categories]**，为产品分配类别（可选）。

      要选择产品的类别，请单击向下箭头并选中类别复选框。 单击 **[!UICONTROL Done]** 完成。

   - 对于 **[!UICONTROL Website Ids]**，选择要关联产品的网站（商店）。

      此列表中的选项取决于您的 [!DNL Commerce] [存储配置](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}设置。

   - 对于 **[!UICONTROL Attribute Set Id]** （必需），选择一个选项。

      `Default` 是默认选项。 此列表中的选项取决于您的 [!DNL Commerce] [属性集](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}。

   - 对于 **[!UICONTROL Visibility]**，请为新产品选择一个选项。

      |**[!UICONTROL Not Visible Individually]** （默认）|产品未包含在您的店面列表中，但可以作为其他产品的变体使用。| |**[!UICONTROL Catalog]**|产品显示在您的目录列表中。| |**[!UICONTROL Search]**|产品可用于搜索操作。| |**[!UICONTROL Catalog and Search]**|产品包含在目录列表中并可用于搜索操作。|

   - 对于 **[!UICONTROL Assign Tax Class]**，请选择产品的选项。

      此列表中显示的选项取决于 [税种](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}。

   - 完成后，单击 **[!UICONTROL Create Catalog Products]**.

目录产品在 [!DNL Commerce] 目录，并分配给创建该目录的Amazon列表。 由于列表现在与现有Amazon列表匹配，因此该列表将从 _[!UICONTROL New Third Party]_选项卡，并显示在_[!UICONTROL Active]_ 选项卡。

## 使用其Amazon列表信息创建多个目录产品

1. 在 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡。

1. 选择要为其创建目录产品的列表。

   您可以在左侧列中选择单个复选框，也可以单击左上角列中的向下箭头，然后选择 **[!UICONTROL Select All]** 或 **[!UICONTROL Select All on this Page]**.

1. 在 _[!UICONTROL Actions]_，单击&#x200B;**[!UICONTROL Create New Catalog Product(s)]**.

1. 接受确认消息并打开 _[!UICONTROL Create Magento Catalog Product]_页面，单击&#x200B;**[!UICONTROL OK]**.

1. 完成产品的目录设置。

   >[!NOTE]
   >为多个选定列表创建目录产品时，输入的产品设置将应用于所有列表。

   - 已设置 **[!UICONTROL Enable Product(s)]** 切换至 `Yes` 或 `No` （必需）。

      |是|选择使产品符合您的 [!DNL Commerce] 店面销售。| |否|选择使产品不符合您的 [!DNL Commerce] 店面销售。|

   - 对于 **[!UICONTROL Categories]**，为产品分配类别（可选）。

      要选择产品的类别，请单击向下箭头并选中类别复选框。 单击 **完成** 完成。

   - 对于 **[!UICONTROL Website Ids]**，选择要关联产品的网站（商店）。

      此列表中的选项取决于您的 [!DNL Commerce] [存储配置](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}设置。

   - 对于 **[!UICONTROL Attribute Set Id]** （必需），选择一个选项。

      `Default` 是默认选项。 此列表中的选项取决于您的 [!DNL Commerce] [属性集](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}。

   - 对于 **[!UICONTROL Visibility]**，请为新产品选择一个选项。

      |**[!UICONTROL Not Visible Individually]** （默认）|产品未包含在您的店面列表中，但可以作为其他产品的变体使用。| |**[!UICONTROL Catalog]**|产品显示在您的目录列表中。| |**[!UICONTROL Search]**|产品可用于搜索操作。| |**[!UICONTROL Catalog and Search]**|产品包含在目录列表中并可用于搜索操作。|

   - 对于 **[!UICONTROL Assign Tax Class]**，请选择产品的选项。

      此列表中显示的选项取决于 [税种](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}。

   - 完成后，单击 **[!UICONTROL Create Catalog Products]**.

目录产品在 [!DNL Commerce] 目录，并分配给创建该目录的Amazon列表。 由于列表现在与各自的Amazon列表相匹配，因此将从 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 选项卡，并显示在 [_[!UICONTROL Active]_](./active-listings.md) 选项卡。

![创建商务目录产品](assets/amazon-magento-catalog-product.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Enable Product(s)] | （必需）如果启用，则产品将显示在 [!DNL Commerce] 店面。 如果禁用，则不会在 [!DNL Commerce] 店面。 |
| [!UICONTROL Categories] | 您可以输入新产品的类别名称，或通过单击向下箭头选择类别以显示选项。 选项取决于您的 [类别](https://docs.magento.com/user-guide/catalog/category-create.html){target=&quot;_blank&quot;}配置。 |
| [!UICONTROL Website Ids] | （必需）选择要关联产品的网站（商店）。 选项取决于您的 [!DNL Commerce] [存储配置](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;&quot;设置 |
| 属性集Id | 选择属性集。 选项取决于您配置的 [!DNL Commerce] [属性集](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}。 |
| [!UICONTROL Visibility] | 选项：<ul><li>**[!UICONTROL Not Visible Individually]**  — 产品在 [!DNL Commerce] storefront（变体产品最常见）。</li><li>**[!UICONTROL Catalog]**  — 允许通过与产品在网站中关联的类别访问产品。</li><li>**搜索**  — 仅允许通过搜索工具找到产品。</li><li>**[!UICONTROL Catalog and Search]**  — 允许通过类别结构和使用搜索工具访问产品。</li></ul> |
| [!UICONTROL Assign Tax Class] | 为新产品分配税类。 选项取决于您配置的 [税种](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}。 |
