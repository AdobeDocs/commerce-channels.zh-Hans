---
title: ‘入门：创建列表规则'
description: 完成Amazon销售渠道载入流程时，请创建初始上市规则，以便为您的 [!DNL Commerce] 产品生成Amazon列表。
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 入门：创建列表规则

上市规则可以在载入期间定义，但也可以随时修改。 入门后，您可以访问存储[功能板](./amazon-store-dashboard.md)上的[列表规则](./listing-rules.md)。

## 在载入过程中创建列表规则

1. 连接存储后，单击添加的存储的&#x200B;**[!UICONTROL View Store]**。

   显示存储区[功能板](./amazon-store-dashboard.md)，并显示`No products listed to Amazon`消息。

1. 单击&#x200B;**[!UICONTROL Preview and List Eligible Products]**。

   此时将显示&#x200B;_[!UICONTROL Listing Rules]_页面。

1. 为要在Amazon上列出的产品资格定义所需的条件，然后单击&#x200B;**[!UICONTROL Preview changes]**，或单击&#x200B;**[!UICONTROL Preview changes]**&#x200B;以跳过此步骤。

   请参阅[示例：定义条件](./ob-define-condition-example.md)。

1. 在列表预览中查看您的列表：

   ![列出预览](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]**  — 根据您当前的列表规则设置，此选项卡上列出的产品不符合Amazon列表的条件。

      不合格的产品不会发布到Amazon。 如果不符合条件的产品已列在Amazon上，并且您将Amazon列表与[!DNL Commerce]目录产品相匹配，则Amazon列表的数量将更改为`0`，以防止产品销售。 要手动从Amazon中删除列表，请参阅[结束Amazon列表](./end-listings-manually.md)。 此处未列出不符合Amazon要求的产品。 这些产品列在[[!UICONTROL Inactive Listings]选项卡](./inactive-listings.md)上。

      要将`Ineligible`列表更改为`Eligible`列表，请重复此过程并修改您的列表规则。

   - **[!UICONTROL Eligible Listings]**  — 根据您当前的列表规则设置，此选项卡上列出的产品有资格获得Amazon列表，并符合Amazon要求。此选项卡包括导入的现有Amazon列表（如果在[列表设置](./listing-settings.md)中将&#x200B;**[!UICONTROL Import Third Party Listings]**&#x200B;设置为`Import Listing`）。

   - **[!UICONTROL New Listings]**  — 此选项卡上列出的产品包括您 [!DNL Commerce] 的目录产品，根据您当前的列表规则设置，这些产品新近有资格获得Amazon列表，并创建Amazon列表。

1. 完成后，单击&#x200B;**[!UICONTROL Save and Close]**。

   将打开存储[功能板](./amazon-store-dashboard.md)。

在上载存储完成后，将启动[!DNL Commerce]和Amazon之间的信息同步。 您的Amazon列表会导入到[!DNL Commerce]中，并尝试与[!DNL Commerce]目录中的产品进行匹配。

您可以在商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_部分查看Amazon订单信息。 请参阅[存储功能板](./amazon-store-dashboard.md)或[管理订单](./managing-orders.md)。

>[!IMPORTANT]
>
>一些重要的商店设置（列表、定价、规则、履行等）具有新商店的默认值。 要确保根据您的特定需求设置您的存储，请查看[存储设置](./default-store-settings.md) 。

![下一](assets/btn-next.png) [**个图标继续默认商店设置**](./default-store-settings.md)
