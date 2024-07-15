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

产品列表操作设置是应用商店列表设置的一部分。 列表设置可从[存储仪表板](./amazon-store-dashboard.md)访问。

这些设置定义您的目录与Amazon的交互方式。 这些设置：

- 指示是否将您符合Amazon资格要求的[!DNL Commerce]目录产品自动发送到您的[!DNL Amazon Seller Central]帐户以创建列表。

- 设置订单的默认处理时间。 此值定义处理和发运订单所需的天数。 例如，如果某人选择2天装运，则在处理完成并将包裹交给承运人之前，该装运转移时间不会开始。 总交货时间为（处理时间+运输时间+任何假日）。

## 配置设置

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Product Listing Actions]_部分。

1. 对于&#x200B;**[!UICONTROL Automatic List Action]** （必需），请选择一个选项：

   - `Automatically List Eligible Products` — （默认）选择您希望何时将[!DNL Commerce]目录产品(符合Amazon的资格要求)自动发布到Amazon并创建Amazon列表。

   - `Do Not Automatically List Eligible Products` — 选择何时手动选择符合条件的[!DNL Commerce]目录产品并创建Amazon列表。 选择后，符合列表条件并包含所有必需信息的目录产品将显示在[_[!UICONTROL Ready to List]_](./ready-to-list.md)选项卡上，以便手动发布到Amazon。

1. 对于&#x200B;**[!UICONTROL Default Handling Time]**（必需），输入装运前提前期所需的天数。

   默认值为`2`天。

   >[!NOTE]
   >
   >此默认处理时间值仅对通过Amazon sales channel创建的Amazon列表有效。 在您的[!DNL Amazon Seller Central]帐户中创建的任何Amazon列表都使用Amazon中设置的默认处理时间。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![产品列表操作](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | 选项：<ul><li>**[!UICONTROL Automatically List Eligible Products]** — （推荐）选择您希望何时将[!DNL Commerce]目录产品(符合Amazon的资格要求)自动发布到Amazon并创建Amazon列表。 选择后，不显示[_[!UICONTROL Ready to List]_](./ready-to-list.md)选项卡。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** — 选择何时手动选择符合条件的[!DNL Commerce]目录产品并创建Amazon列表。 选择后，符合列表条件并包含所有必需信息的目录产品将显示在[_[!UICONTROL Ready to List]_](./ready-to-list.md)选项卡上，以便手动发布。</li></ul> |
| [!UICONTROL Default Handling Time] | 表示订单处理和发运通常需要的天数的数值。 默认值为`2`。 此值用于在[!DNL Commerce]中创建并发布到Amazon的Amazon列表。 在与[!DNL Commerce]集成之前，Amazon列表的默认处理时间不受此设置的影响。<br><br>在Amazon sales channel中定义的值不会替换现有Amazon列表中定义的默认处理时间。 启用&#x200B;**[!UICONTROL Handling Time Override]**&#x200B;后将其删除时，订单的处理时间将恢复到此处定义的值。<br><br>如果您的产品具有不同的处理时间，则可以在产品特定的级别创建处理时间覆盖。 您可以在[_[!UICONTROL Overrides]_](./overrides.md)选项卡中管理处理时间覆盖，从而灵活地管理产品履行。 如果产品的[!DNL Commerce]中没有处理时间覆盖，则处理时间默认值是Amazon列表中定义的值。<br><br>处理时间是区域属性。 当列表的值发生更改时，该更改将影响在同一地区存在的所有Amazon存储中共享[!DNL Amazon Seller SKU]的所有列表（在[存储集成](./store-integration.md)中定义）。 但是，更改北美区域中共享[!DNL Amazon Seller SKU]的值不会影响具有不同定义区域的存储中列出的相同产品。 创建日期最早的区域的存储控制“默认处理时间”设置的优先级。 |

**快速访问** - [!UICONTROL Listing Settings]分区

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
