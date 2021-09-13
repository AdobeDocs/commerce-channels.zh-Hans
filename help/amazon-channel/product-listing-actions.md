---
title: 产品列表操作
description: 使用产品列表操作设置定义商务目录如何与Amazon交互。
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 产品列表操作

产品清单操作设置是您的商店清单设置的一部分。 可从[存储功能板](./amazon-store-dashboard.md)访问列表设置。

这些设置定义目录与Amazon的交互方式。 以下设置：

- 指示是否自动将符合Amazon资格要求的[!DNL Commerce]目录产品发送到您的[!DNL Amazon Seller Central]帐户以创建列表。

- 设置订单的默认处理时间。 此值定义处理和发运订单所需的天数。 例如，如果某人选择2天的发运，则在处理完成并将包装交付给承运人之前，不会开始该发运的中转时间。 总交付时间为（处理时间+过境时间+任何假日）。

## 配置设置

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Listing Settings]**。

1. 展开&#x200B;_[!UICONTROL Product Listing Actions]_部分。

1. 对于&#x200B;**[!UICONTROL Automatic List Action]**（必需），选择一个选项：

   - `Automatically List Eligible Products`  — （默认）选择您希望何时自动 [!DNL Commerce] 发布到Amazon并创建Amazon列表(符合Amazon的资格要求)的目录产品。

   - `Do Not Automatically List Eligible Products`  — 选择您希望手动选择符合条件的目录产 [!DNL Commerce] 品并创建Amazon列表的时间。选择后，[_[!UICONTROL Ready to List]_](./ready-to-list.md)选项卡上会显示符合列表标准并包含所有必需信息的目录产品，以便手动发布到Amazon。

1. 对于&#x200B;**[!UICONTROL Default Handling Time]**（必需），输入装运前提前期所需的天数。

   默认值为`2`天。

   >[!NOTE]
   >
   >此默认处理时间值仅对通过Amazon销售渠道创建的Amazon列表有效。 在[!DNL Amazon Seller Central]帐户中创建的任何Amazon列表都使用Amazon中设置的默认处理时间。

1. 完成后，单击&#x200B;**[!UICONTROL Save listing settings]**。

![产品列表操作](assets/amazon-product-listing-actions.png)

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Automatic List Action] | 选项：<ul><li>**[!UICONTROL Automatically List Eligible Products]**  — （推荐）选择您希望何时 [!DNL Commerce] 将目录产品(满足Amazon的资格要求)自动发布到Amazon并创建Amazon列表。选择后，不会显示[_[!UICONTROL Ready to List]_](./ready-to-list.md)选项卡。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]**  — 选择您希望手动选择符合条件的目录产 [!DNL Commerce] 品并创建Amazon列表的时间。选择后，符合列表标准并包含所有必需信息的目录产品将显示在[_[!UICONTROL Ready to List]_](./ready-to-list.md)选项卡上，以便手动发布。</li></ul> |
| [!UICONTROL Default Handling Time] | 表示处理和发运订单所花费的天数的数值。 默认值为`2`。 此值用于在[!DNL Commerce]中创建并发布到Amazon的Amazon列表。 与[!DNL Commerce]集成之前Amazon列表的默认处理时间不受此设置的影响。<br><br>在Amazon销售渠道中定义的值不会替换现有Amazon列表中定义的默认处理时间。启用&#x200B;**[!UICONTROL Handling Time Override]**&#x200B;并将其删除后，订单的处理时间将还原为此处定义的值。<br><br>如果您的产品具有不同的处理时间，则可以在产品特定的级别创建处理时间覆盖。您可以在[_[!UICONTROL Overrides]_](./overrides.md)选项卡中管理处理时间覆盖，从而灵活地管理产品履行。 如果某产品的[!DNL Commerce]中没有处理时间覆盖，则处理时间默认值是Amazon列表中定义的值。<br><br>“处理时间”是区域属性。更改列表的值时，该更改会影响所有Amazon存储中共享[!DNL Amazon Seller SKU]且存在于同一区域（在[存储集成](./store-integration.md)中定义）的所有列表。 但是，更改北美地区共享[!DNL Amazon Seller SKU]的值不会影响在具有不同定义区域的商店中列出的相同产品。 创建日期最早的区域的存储可控制“默认处理时间”设置的优先级。 |

**快速访问**  — 部 [!UICONTROL Listing Settings] 分

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
