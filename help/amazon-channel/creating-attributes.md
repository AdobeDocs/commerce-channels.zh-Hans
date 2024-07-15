---
title: 创建和编辑Amazon销售渠道的属性
description: AmazonSales Channel提供了“属性”视图，可帮助您查看当前的Amazon属性和链接的Commerce属性。
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# 创建和编辑属性

在通过Amazon销售时创建或更新[!DNL Commerce]属性并更新商店。 通过Amazon销售渠道主页的&#x200B;[_[!UICONTROL Attributes]_视图](./attributes-view.md)查看当前Amazon属性并链接[!DNL Commerce]属性。_[!UICONTROL Action]_&#x200B;列显示该属性的可用操作。 您可以为未链接的Amazon属性创建和映射新的[!DNL Commerce]属性，也可以编辑现有[!DNL Commerce]属性及其到Amazon属性的映射。

创建和更新属性时，您可能需要验证[!DNL Commerce]和Amazon产品的属性值。 如果不从Amazon同步和导入值，则这些值可能会有所不同。 若要查看这些属性的Amazon值，请参阅[查看Amazon属性映射](./amazon-matching-attributes-values.md)。 如果要更改这些值，您可以[编辑或创建Amazon与[!DNL Commerce]之间的映射](./amazon-manually-update-incomplete-listing.md)。

## 创建属性 {#create-an-attribute}

这些步骤将创建一个[!DNL Commerce]属性并将其映射到Amazon属性。 根据配置，值可能会在目录之间开始同步。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Create Attribute]**。

1. 要启用Amazon值与链接的[!DNL Commerce]属性的同步，请将&#x200B;**[!UICONTROL Is Active]**&#x200B;设置为`Yes`。

   当设置为`Yes`时，值将根据您的配置进行同步。

1. 为&#x200B;**[!UICONTROL Select Magento Product Attribute]**&#x200B;选择`Create New Magento Attribute`。

   该属性映射到为&#x200B;**[!UICONTROL Amazon Attribute Name]**&#x200B;选择的属性。

1. 输入&#x200B;**[!UICONTROL Magento Product Attribute Name]**。

1. 输入&#x200B;**[!UICONTROL Magento Product Attribute Code]**。

   此值必须全部小写且不加空格。

1. 对于&#x200B;**[!UICONTROL Attribute Set Ids]**，选择要分配的属性集。

   通常，属性是属性集的一部分，例如具有蓝色、绿色、黄色和红色属性的颜色集。

1. 对于&#x200B;**[!UICONTROL Type]**，选择属性值的类型，如文本和数字。

   此选项影响属性的允许值。

1. 对于&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**，设置为`Yes`以允许该属性可用于促销条件中的参数。

1. 对于&#x200B;**[!UICONTROL Used in Search]**，如果属性和值可用于产品搜索，则设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Comparable on Storefront]**，如果属性值可以在Amazon的“比较依据”功能中使用，则设置为`Yes`。

1. 为属性选择[!DNL Commerce] [作用域](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings)，然后选择一个或多个要将Amazon值导入的存储视图。

   如果范围设置为`Global`，则在创建属性后无法更改&#x200B;_[!UICONTROL Store View]_。

   如果选择`All Store Views (Global)`，它将同步并保存所有Amazon存储视图的值。 您可能只想将值同步到特定的存储视图。

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute Settings]**。

保存后，您可能想要编辑属性以检查设置并匹配属性的Amazon和[!DNL Commerce]值。 您还可以指示Amazon值是否应覆盖[!DNL Commerce]值。

![创建属性设置](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | 指示此属性是否为Amazon和[!DNL Commerce]之间的实时和主动同步。 设置为`Yes`以确保Amazon和[!DNL Commerce]中的属性值保持所选属性的同步。 |
| 选择Magento产品属性 | 指示要链接到所列Amazon属性名称的选定属性。 创建属性时，请选择`Create New Magento Attribute`。 |
| [!UICONTROL Amazon Attribute Name] | 显示您选择的Amazon属性的名称。 选定的属性链接到此Amazon属性。 您无法通过[!DNL Commerce]编辑此值。 |
| [!UICONTROL Magento Product Attribute Name] | 指示属性名称或“标签”。 |
| [!UICONTROL Magento Product Attribute Code] | 指示属性代码，全部用小写字符表示，不带空格。 |
| [!UICONTROL Attribute Set Ids] | 指示要为其分配属性的属性集。 属性往往是属性集的一部分，例如具有蓝色、绿色、黄色和红色属性的颜色集。 |
| [!UICONTROL Type] | 指示属性值的值类型，如文本和数字。 选择将影响属性的允许值。 |
| [!UICONTROL Use for Promo Rule Conditions] | 切换到`Yes`以允许该属性可用于促销条件中的参数。 |
| [!UICONTROL Used in Search] | 指示属性和值是否可用于产品搜索。 |
| [!UICONTROL Comparable on Storefront] | 指示属性值是否可以在Amazon的“比较依据”功能中使用。 |
| [!UICONTROL Magento Product Attribute Scope] | 指示属性的[范围](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings)。 选项： Global / Store View<br>当设置为`Global`时，在创建属性后无法编辑Store View。 |
| [!UICONTROL Store Views (to import values into to)] | 仅在范围设置为`Store View`时显示。 选择将Amazon属性值同步到的[存储视图](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html)。 选择`All Store Views (Global)`将更新所有[!DNL Commerce]存储视图中的值。 |

## 编辑属性 {#edit-an-attribute}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Edit]**。

1. 要启用或禁用将Amazon值同步到链接的[!DNL Commerce]属性，请将&#x200B;**Is Active**&#x200B;设置为`Yes`或`No`。

   当设置为`Yes`时，值将根据您的配置进行同步。

1. 对于&#x200B;**[!UICONTROL Select Magento Product Attribute]**，验证或更新要映射到所选&#x200B;**[!UICONTROL Amazon Attribute Name]**&#x200B;的属性。

1. 指示是否希望传入Amazon属性值覆盖现有属性值。

   例如，您可能不希望将Amazon中的价格覆盖到[!DNL Commerce]中。

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** — 保留值，保留[!DNL Commerce]和Amazon存储的其他值。

   - **[!UICONTROL Overwrite Existing Magento Values]** — 使用传入的Amazon值覆盖[!DNL Commerce]产品目录中的值。

1. 如果可供编辑，请选择一个或多个&#x200B;**[!UICONTROL Store Views (to import Amazon values into)]**。

   如果属性是使用`Global`作用域创建的，则在创建属性后无法更改&#x200B;_存储视图_。

   如果选择`All Store Views (Global)`，它将同步并保存所有存储视图的值。 您可能只想将值同步到特定的存储视图。

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute Settings]**。

![编辑属性设置](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | 指示此属性是否为Amazon和[!DNL Commerce]之间的实时和主动同步。 设置为`Yes`以确保Amazon和[!DNL Commerce]中的属性值保持所选属性的同步。 |
| [!UICONTROL Select Magento Product Attribute] | 指示要链接到列出的Amazon属性名称的选定[!DNL Commerce]属性。 如果要更改链接的[!DNL Commerce]属性，请从下拉列表中选择其他属性。 值根据配置进行同步。 |
| [!UICONTROL Amazon Attribute Name] | 显示[!DNL Amazon Seller Central]中定义的Amazon属性的名称。 选定的[!DNL Commerce]属性链接到此Amazon属性。 您无法通过[!DNL Commerce]编辑此值。 |
| [!UICONTROL Overwrite Existing Value] | 指示Amazon属性值是否覆盖现有[!DNL Commerce]值，从而影响具有此[!DNL Commerce]属性的所有产品。<ul><li>**不覆盖现有Magento值** - （默认）保留[!DNL Commerce]值，保留[!DNL Commerce]和Amazon存储的其他值。</li><li>**覆盖现有Magento值** — 将Amazon值保存在[!DNL Commerce]产品目录中的[!DNL Commerce]值上。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 如果属性是使用`Global`范围创建的，则在编辑该属性时不会显示。 指示已创建[!DNL Commerce] [作用域](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings)并将其设置为`Store View`。 |
| [!UICONTROL Store Views (to import values into to)] | 选择要将Amazon属性值同步到的[!DNL Commerce] [存储视图](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html)。 选择`All Store Views (Global)`将更新所有存储视图中的值。 |
