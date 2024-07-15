---
title: 创建Amazon列表规则
description: 在完成Amazon销售渠道入门培训流程时，创建初始列表规则以生成 [!DNL Commerce] 产品的Amazon列表。
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 创建Amazon列表规则

上市规则可以在载入期间定义，也可以随时修改。 上线后，您可以在商店[仪表板](./amazon-store-dashboard.md)上访问[列表规则](./listing-rules.md)。

## 在新用户引导期间创建列表规则

1. 连接存储后，为添加的存储单击&#x200B;**[!UICONTROL View Store]**。

   存储[仪表板](./amazon-store-dashboard.md)随`No products listed to Amazon`消息一起出现。

1. 单击&#x200B;**[!UICONTROL Preview and List Eligible Products]**。

   此时会显示&#x200B;_[!UICONTROL Listing Rules]_页面。

1. 为在Amazon上列出的产品资格定义所需条件，然后单击&#x200B;**[!UICONTROL Preview changes]**，或单击&#x200B;**[!UICONTROL Preview changes]**&#x200B;跳过此步骤。

   请参阅[示例：定义条件](./ob-define-condition-example.md)。

1. 在“列表预览”中查看您的列表：

   ![列表预览](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** — 根据您当前的列表规则设置，此选项卡上列出的产品不符合Amazon列表的条件。

     不符合条件的产品将不会发布到Amazon。 如果Amazon上已列出不合格产品，并且您将Amazon列表与您的[!DNL Commerce]目录产品匹配，则Amazon列表的数量将更改为`0`以防止产品销售。 要从Amazon中手动删除列表，请参阅[结束Amazon列表](./end-listings-manually.md)。 此处不列出不符合Amazon要求的产品。 这些产品列在[[!UICONTROL Inactive Listings]选项卡](./inactive-listings.md)上。

     若要将`Ineligible`列表更改为`Eligible`列表，请重复此过程并修改您的列表规则。

   - **[!UICONTROL Eligible Listings]** — 根据您当前的列表规则设置，此选项卡上列出的产品符合Amazon列表的条件，并且符合Amazon要求。 此选项卡包括已导入的现有Amazon列表（如果您在[列表设置](./listing-settings.md)中将&#x200B;**[!UICONTROL Import Third Party Listings]**&#x200B;设置为`Import Listing`）。

   - **[!UICONTROL New Listings]** — 此选项卡上列出的产品包括您的[!DNL Commerce]目录产品，这些产品根据您当前的列表规则设置新符合Amazon列表资格并创建Amazon列表。

1. 完成后，单击&#x200B;**[!UICONTROL Save and Close]**。

   存储[仪表板](./amazon-store-dashboard.md)打开。

完成载入商店后，[!DNL Commerce]与Amazon之间的信息同步已启动。 您的Amazon列表已导入到[!DNL Commerce]中，并尝试与[!DNL Commerce]目录中的产品匹配。

您可以在商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分中查看您的Amazon订单信息。 查看[存储信息板](./amazon-store-dashboard.md)或[管理订单](./managing-orders.md)。

>[!IMPORTANT]
>
>有一些重要的商店设置（列表、定价、规则、履行等）具有新商店的默认值。 要确保您的商店已针对特定需求进行设置，请查看[商店设置](./default-store-settings.md) 。

![下一个图标](assets/btn-next.png) [**继续使用默认商店设置**](./default-store-settings.md)
