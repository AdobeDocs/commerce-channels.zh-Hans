---
title: Amazon sales channel — 产品列表操作
description: 使用产品列表操作设置来定义Commerce目录与Amazon的交互方式。
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 产品列表操作

产品列表操作设置是应用商店列表设置的一部分。 列表设置可从以下位置访问： [存储仪表板](./amazon-store-dashboard.md).

这些设置定义目录与Amazon的交互方式。 这些设置：

- 指示您的 [!DNL Commerce] 符合Amazon资格要求的目录产品会自动发送给贵机构的 [!DNL Amazon Seller Central] 创建列表的帐户。

- 设置订单的默认处理时间。 此值定义处理和发运订单所需的天数。 例如，如果某人选择“2天装运”，则只有在处理完成并将包裹交给承运人之后，该装运中转时间才会开始。 总交货时间为（处理时间+运输时间+任何假日）。

## 配置设置

1. 单击 **[!UICONTROL Listing Settings]** 在商店仪表板上。

1. 展开 _[!UICONTROL Product Listing Actions]_部分。

1. 对象 **[!UICONTROL Automatic List Action]** （必需），选择一个选项：

   - `Automatically List Eligible Products`  — （默认）选择您所需的时间 [!DNL Commerce] 目录产品(符合Amazon的资格要求)以自动发布到Amazon并创建Amazon列表。

   - `Do Not Automatically List Eligible Products`  — 选择何时要手动选择符合条件的应用程序 [!DNL Commerce] 编录产品并创建Amazon列表。 选择后，符合列表条件并包含所有必需信息的目录产品将显示在 [_[!UICONTROL Ready to List]_](./ready-to-list.md) 选项卡，以手动发布到Amazon。

1. 对象 **[!UICONTROL Default Handling Time]** （必需），输入发运前提前期所需的天数。

   默认值为 `2` 天。

   >[!NOTE]
   >
   >此默认处理时间值仅对通过Amazon sales channel创建的Amazon列表有效。 在中创建的任何Amazon列表 [!DNL Amazon Seller Central] 帐户使用Amazon中设置的默认处理时间。

1. 完成后，单击 **[!UICONTROL Save listing settings]**.

![产品列表操作](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | 选项：<ul><li>**[!UICONTROL Automatically List Eligible Products]**  — （推荐）选择您所需的时间 [!DNL Commerce] 目录产品(符合Amazon的资格要求)以自动发布到Amazon并创建Amazon列表。 选择后， [_[!UICONTROL Ready to List]_](./ready-to-list.md) 选项卡未显示。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]**  — 选择要手动选择符合条件的时机 [!DNL Commerce] 编录产品并创建Amazon列表。 选择后，符合列表条件并包含所有必需信息的目录产品将显示在 [_[!UICONTROL Ready to List]_](./ready-to-list.md) 选项卡进行手动发布。</li></ul> |
| [!UICONTROL Default Handling Time] | 表示订单处理和发运通常所用的天数的数值。 默认值为 `2`. 此值用于在中创建的Amazon列表 [!DNL Commerce] 并发布到Amazon。 Amazon列表在与集成之前的默认处理时间 [!DNL Commerce] 不受此设置的影响。<br><br>Amazon sales channel中定义的值不会替换现有Amazon列表中定义的默认处理时间。 当 **[!UICONTROL Handling Time Override]** 启用后删除，订单的处理时间将恢复到此处定义的值。<br><br>如果您的产品具有不同的处理时间，则可以在产品特定的级别创建处理时间覆盖。 您可以在中管理处理时间覆盖 [_[!UICONTROL Overrides]_](./overrides.md) 选项卡，让您能够灵活地管理产品交付。 如果中没有处理时间覆盖 [!DNL Commerce] 对于产品，处理时间的默认值为在Amazon列表中定义的值。<br><br>“处理时间”是区域属性。 当一个列表的值发生更改时，该更改将影响共享该列表的所有列表 [!DNL Amazon Seller SKU] 存在于同一区域的所有Amazon商店中(定义于 [存储集成](./store-integration.md))。 但是，更改共享的值 [!DNL Amazon Seller SKU] 在北美区域，不会影响具有不同已定义区域的商店中列出的相同产品。 创建日期最早的区域的存储将控制“默认处理时间”设置的优先级。 |

**快速访问** - [!UICONTROL Listing Settings] 区域

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
