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

创建或更新 [!DNL Commerce] 属性。 查看当前Amazon属性和链接的 [!DNL Commerce] 属性 [_[!UICONTROL Attributes]_视图](./attributes-view.md) Amazon销售渠道主页的URL。 的_[!UICONTROL Action]_ 列显示属性的可用操作。 您可以创建并映射新 [!DNL Commerce] 属性，或者，您也可以编辑现有的 [!DNL Commerce] 属性及其到Amazon属性的映射。

在创建和更新属性时，您可能需要验证 [!DNL Commerce] 和Amazon产品。 如果您不同步并从Amazon导入值，则这些值可能会不同。 要查看这些属性的Amazon值，请参阅 [审核Amazon属性映射](./amazon-matching-attributes-values.md). 如果要更改这些值，您可以 [编辑或创建映射](./amazon-manually-update-incomplete-listing.md) 在Amazon和 [!DNL Commerce].

## 创建属性 {#create-an-attribute}

这些步骤将创建 [!DNL Commerce] 属性，并将其映射到Amazon属性。 根据配置，值可能会开始在目录之间同步。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. 单击 **[!UICONTROL Attributes]** 在左侧菜单中，找到Amazon属性，然后单击 **[!UICONTROL Create Attribute]** 在 _[!UICONTROL Action]_列。

1. 启用将Amazon值同步到链接的 [!DNL Commerce] 属性，设置 **[!UICONTROL Is Active]** to `Yes`.

   当设置为 `Yes`，则值会根据您的配置进行同步。

1. 选择 `Create New Magento Attribute` 表示 **[!UICONTROL Select Magento Product Attribute]**.

   该属性映射到为 **[!UICONTROL Amazon Attribute Name]**.

1. 输入 **[!UICONTROL Magento Product Attribute Name]**.

1. 输入 **[!UICONTROL Magento Product Attribute Code]**.

   此值必须全部为小写，不带空格。

1. 对于 **[!UICONTROL Attribute Set Ids]**，选择要分配的属性集。

   通常，属性是属性集的一部分，例如，对于具有蓝色、绿色、黄色和红色属性的颜色的集。

1. 对于 **[!UICONTROL Type]**，请选择属性值的类型，如文本和数字。

   此选项会影响属性的允许值。

1. 对于 **[!UICONTROL Use for Promo Rule Conditions]**，设置为 `Yes` 以允许该属性可用于促销条件中的参数。

1. 对于 **[!UICONTROL Used in Search]**，设置为 `Yes` 属性和值是否可用于产品搜索。

1. 对于 **[!UICONTROL Comparable on Storefront]**，设置为 `Yes` 是否可在Amazon的“比较方式”功能中使用属性值。

1. 选择 [!DNL Commerce] [范围](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}作为属性，然后选择一个或多个存储视图以将Amazon值导入。

   如果范围设置为 `Global`, _[!UICONTROL Store View]_在创建属性后无法更改。

   如果您选择 `All Store Views (Global)`，它会同步值并将其保存到所有Amazon存储视图。 您可能只想将值同步到特定的存储视图。

1. 完成后，单击 **[!UICONTROL Save Attribute Settings]**.

保存后，您可能想要编辑属性以查看设置并与Amazon和 [!DNL Commerce] 属性的值。 您还可以指示Amazon值是否应覆盖 [!DNL Commerce] 值。

![创建属性设置](assets/amazon-attribute-settings-create.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Is Active] | 指示此属性是否处于实时状态并在Amazon和 [!DNL Commerce]. 设置为 `Yes` 以确保属性值来自Amazon和 [!DNL Commerce] 保持选定属性的同步。 |
| 选择Magento产品属性 | 指示您要链接到列出的Amazon属性名称的选定属性。 创建属性时，选择 `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | 显示您选择的Amazon属性的名称。 所选属性链接到此Amazon属性。 无法通过 [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | 指示属性名称或“标签”。 |
| [!UICONTROL Magento Product Attribute Code] | 指示属性代码，全部以小写字符表示，不带空格。 |
| [!UICONTROL Attribute Set Ids] | 指示要将属性分配到的属性集。 属性往往属于属性集的一部分，例如，对于具有蓝色、绿色、黄色和红色属性的颜色的属性集。 |
| [!UICONTROL Type] | 指示属性值的值类型，如文本和数字。 选择会影响属性的允许值。 |
| [!UICONTROL Use for Promo Rule Conditions] | 切换到 `Yes` 以允许该属性可用于促销条件中的参数。 |
| [!UICONTROL Used in Search] | 指示属性和值是否可用于产品搜索。 |
| [!UICONTROL Comparable on Storefront] | 指示属性值是否可在Amazon的“比较方式”功能中使用。 |
| [!UICONTROL Magento Product Attribute Scope] | 指示 [范围](https://docs.magento.com/user-guide/configuration/scope.html)属性的{target=&quot;_blank&quot;}。 选项：全局/商店视图<br>当设置为 `Global`，则在创建属性后无法编辑“商店视图”。 |
| [!UICONTROL Store Views (to import values into to)] | 仅当范围设置为 `Store View`. 选择 [商店视图](https://docs.magento.com/user-guide/stores/websites-stores-views.html)将Amazon属性值同步到的{target=&quot;_blank&quot;}。 选择 `All Store Views (Global)` 更新了所有 [!DNL Commerce] 存储视图。 |

## 编辑属性 {#edit-an-attribute}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. 单击 **[!UICONTROL Attributes]** 在左侧菜单中，找到Amazon属性，然后单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 启用或禁用将Amazon值同步到链接的 [!DNL Commerce] 属性，设置 **处于活动状态** to `Yes` 或 `No`.

   当设置为 `Yes`，则值会根据您的配置进行同步。

1. 对于 **[!UICONTROL Select Magento Product Attribute]**，验证或更新要映射到所选属性的属性 **[!UICONTROL Amazon Attribute Name]**.

1. 指示您是否希望传入的Amazon属性值覆盖现有属性值。

   例如，您可能不希望将价格从Amazon覆盖到 [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]**  — 保留值，并保留 [!DNL Commerce] 和Amazon店。

   - **[!UICONTROL Overwrite Existing Magento Values]**  — 覆盖 [!DNL Commerce] 具有传入Amazon值的产品目录。

1. 如果可供编辑，请选择一个或多个 **[!UICONTROL Store Views (to import Amazon values into)]**.

   如果属性是使用 `Global` 范围、 _存储视图_ 在创建属性后无法更改。

   如果您选择 `All Store Views (Global)`，它会同步并将值保存到所有存储视图。 您可能只想将值同步到特定的存储视图。

1. 完成后，单击 **[!UICONTROL Save Attribute Settings]**.

![编辑属性设置](assets/amazon-attribute-settings-edit.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Is Active] | 指示此属性是否处于实时状态并在Amazon和 [!DNL Commerce]. 设置为 `Yes` 以确保属性值来自Amazon和 [!DNL Commerce] 保持选定属性的同步。 |
| [!UICONTROL Select Magento Product Attribute] | 指示选定的 [!DNL Commerce] 属性。 如果要更改链接的 [!DNL Commerce] 属性，请从下拉列表中选择其他属性。 值会根据配置进行同步。 |
| [!UICONTROL Amazon Attribute Name] | 显示Amazon属性的名称，该属性在 [!DNL Amazon Seller Central]. 选定的 [!DNL Commerce] 属性链接到此Amazon属性。 无法通过 [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | 指示Amazon属性值是否会覆盖现有 [!DNL Commerce] 值，影响具有此 [!DNL Commerce] 属性。<ul><li>**请勿覆盖现有Magento值**  — （默认）保留 [!DNL Commerce] 值，保留不同的值 [!DNL Commerce] 和Amazon店。</li><li>**覆盖现有Magento值**  — 在 [!DNL Commerce] 值 [!DNL Commerce] 产品目录。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 如果属性是使用 `Global` 范围。 指示 [!DNL Commerce] [范围](https://docs.magento.com/user-guide/configuration/scope.html)已创建{target=&quot;_blank&quot;}并将其设置为 `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | 选择 [!DNL Commerce] [商店视图](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}，要将Amazon属性值同步到其中。 选择 `All Store Views (Global)` 更新所有商店视图中的值。 |
