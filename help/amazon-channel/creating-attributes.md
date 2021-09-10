---
title: 创建和编辑属性
description: AmazonSales Channel提供“属性”视图，以帮助您查看当前的Amazon属性和链接的商务属性。
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# 创建和编辑属性

在通过Amazon销售时创建或更新[!DNL Commerce]属性，并更新商店。 通过Amazon销售渠道主页的&#x200B;[_[!UICONTROL Attributes]_视图](./attributes-view.md)查看当前Amazon属性和链接的[!DNL Commerce]属性。_[!UICONTROL Action]_&#x200B;列显示属性的可用操作。 您可以为未链接的Amazon属性创建并映射新的[!DNL Commerce]属性，也可以编辑现有的[!DNL Commerce]属性及其到Amazon属性的映射。

在创建和更新属性时，您可能需要验证[!DNL Commerce]和Amazon产品的属性值。 如果您不同步并从Amazon导入值，则这些值可能会不同。 要查看这些属性的Amazon值，请参阅[审核Amazon属性映射](./amazon-matching-attributes-values.md)。 如果要更改这些值，可以[编辑或创建Amazon和[!DNL Commerce]之间的映射](./amazon-manually-update-incomplete-listing.md)。

## 创建属性 {#create-an-attribute}

这些步骤将创建一个[!DNL Commerce]属性，并将其映射到Amazon属性。 根据配置，值可能会开始在目录之间同步。

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Create Attribute]**。

1. 要启用将Amazon值同步到链接的[!DNL Commerce]属性，请将&#x200B;**[!UICONTROL Is Active]**&#x200B;设置为`Yes`。

   当设置为`Yes`时，值会根据您的配置进行同步。

1. 为&#x200B;**[!UICONTROL Select Magento Product Attribute]**&#x200B;选择`Create New Magento Attribute`。

   该属性映射到为&#x200B;**[!UICONTROL Amazon Attribute Name]**&#x200B;选择的。

1. 输入&#x200B;**[!UICONTROL Magento Product Attribute Name]**。

1. 输入&#x200B;**[!UICONTROL Magento Product Attribute Code]**。

   此值必须全部为小写，不带空格。

1. 对于&#x200B;**[!UICONTROL Attribute Set Ids]**，选择要分配的属性集。

   通常，属性是属性集的一部分，例如，对于具有蓝色、绿色、黄色和红色属性的颜色的集。

1. 对于&#x200B;**[!UICONTROL Type]**，选择属性值的类型，如文本和数字。

   此选项会影响属性的允许值。

1. 对于&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**，设置为`Yes`以允许该属性可用于促销条件中的参数。

1. 对于&#x200B;**[!UICONTROL Used in Search]**，如果可以在产品搜索中使用属性和值，则设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Comparable on Storefront]**，如果属性值可用于Amazon的“比较方式”功能，则设置为`Yes`。

1. 为属性选择[!DNL Commerce] [范围](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}，然后选择一个或多个存储视图以将Amazon值导入。

   如果范围设置为`Global`，则在创建属性后，无法更改&#x200B;_[!UICONTROL Store View]_。

   如果选择`All Store Views (Global)`，它将同步并保存值到所有Amazon存储视图。 您可能只想将值同步到特定的存储视图。

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute Settings]**。

保存后，您可能需要编辑属性以查看该属性的设置以及与Amazon和[!DNL Commerce]值的匹配情况。 您还可以指示Amazon值是否应覆盖[!DNL Commerce]值。

![创建属性设置](assets/amazon-attribute-settings-create.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Is Active] | 指示此属性是否处于实时状态并在Amazon与[!DNL Commerce]之间进行主动同步。 设置为`Yes`，以确保Amazon和[!DNL Commerce]中的属性值与选定属性保持同步。 |
| 选择Magento产品属性 | 指示您要链接到列出的Amazon属性名称的选定属性。 创建属性时，请选择`Create New Magento Attribute`。 |
| [!UICONTROL Amazon Attribute Name] | 显示您选择的Amazon属性的名称。 所选属性链接到此Amazon属性。 不能通过[!DNL Commerce]编辑此值。 |
| [!UICONTROL Magento Product Attribute Name] | 指示属性名称或“标签”。 |
| [!UICONTROL Magento Product Attribute Code] | 指示属性代码，全部以小写字符表示，不带空格。 |
| [!UICONTROL Attribute Set Ids] | 指示要将属性分配到的属性集。 属性往往属于属性集的一部分，例如，对于具有蓝色、绿色、黄色和红色属性的颜色的属性集。 |
| [!UICONTROL Type] | 指示属性值的值类型，如文本和数字。 选择会影响属性的允许值。 |
| [!UICONTROL Use for Promo Rule Conditions] | 切换到`Yes`，以允许该属性可用于促销条件中的参数。 |
| [!UICONTROL Used in Search] | 指示属性和值是否可用于产品搜索。 |
| [!UICONTROL Comparable on Storefront] | 指示属性值是否可在Amazon的“比较方式”功能中使用。 |
| [!UICONTROL Magento Product Attribute Scope] | 指示属性的[范围](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}。 选项：全局/存储视图<br>如果设置为`Global`，则在创建属性后，无法编辑存储视图。 |
| [!UICONTROL Store Views (to import values into to)] | 仅当作用域设置为`Store View`时才显示。 选择将Amazon属性值同步到的[存储视图](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}。 选择`All Store Views (Global)`会更新所有[!DNL Commerce]存储视图中的值。 |

## 编辑属性 {#edit-an-attribute}

1. 在&#x200B;_Admin_&#x200B;侧栏中，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**。

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Attributes]**，找到Amazon属性，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Edit]**。

1. 要启用或禁用Amazon值与链接的[!DNL Commerce]属性的同步，请将&#x200B;**Is Active**&#x200B;设置为`Yes`或`No`。

   当设置为`Yes`时，值会根据您的配置进行同步。

1. 对于&#x200B;**[!UICONTROL Select Magento Product Attribute]**，验证或更新要映射到所选&#x200B;**[!UICONTROL Amazon Attribute Name]**&#x200B;的属性。

1. 指示您是否希望传入的Amazon属性值覆盖现有属性值。

   例如，您可能不希望将价格从Amazon覆盖到[!DNL Commerce]中。

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]**  — 保留值，并保留和Amazon存储区 [!DNL Commerce] 的不同值。

   - **[!UICONTROL Overwrite Existing Magento Values]**  — 使用传入的Amazon值 [!DNL Commerce] 覆盖产品目录中的值。

1. 如果可进行编辑，请选择一个或多个&#x200B;**[!UICONTROL Store Views (to import Amazon values into)]**。

   如果属性是在`Global`范围中创建的，则在创建属性后，将无法更改&#x200B;_存储视图_。

   如果选择`All Store Views (Global)`，它将同步并保存所有存储视图的值。 您可能只想将值同步到特定的存储视图。

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute Settings]**。

![编辑属性设置](assets/amazon-attribute-settings-edit.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Is Active] | 指示此属性是否处于实时状态并在Amazon与[!DNL Commerce]之间进行主动同步。 设置为`Yes`，以确保Amazon和[!DNL Commerce]中的属性值与选定属性保持同步。 |
| [!UICONTROL Select Magento Product Attribute] | 指示您希望链接到所列Amazon属性名称的选定[!DNL Commerce]属性。 如果要更改链接的[!DNL Commerce]属性，请从下拉列表中选择其他属性。 值会根据配置进行同步。 |
| [!UICONTROL Amazon Attribute Name] | 显示[!DNL Amazon Seller Central]中定义的Amazon属性的名称。 选定的[!DNL Commerce]属性链接到此Amazon属性。 不能通过[!DNL Commerce]编辑此值。 |
| [!UICONTROL Overwrite Existing Value] | 指示Amazon属性值是否覆盖现有的[!DNL Commerce]值，从而影响具有此[!DNL Commerce]属性的所有产品。<ul><li>**请勿覆盖现有Magento值**  — （默认）会保留值，并 [!DNL Commerce] 保留和Amazon存储区 [!DNL Commerce] 的不同值。</li><li>**覆盖现有Magento值**  — 保存Amazon值，使其大于产 [!DNL Commerce] 品目录 [!DNL Commerce] 中的值。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 如果属性是使用`Global`范围创建的，则在编辑属性时不显示。 指示已创建[!DNL Commerce] [范围](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}并将其设置为`Store View`。 |
| [!UICONTROL Store Views (to import values into to)] | 选择[!DNL Commerce] [存储视图](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}，以将Amazon属性值同步到该视图。 选择`All Store Views (Global)`会更新所有存储视图中的值。 |
