---
title: '入门：创建列表规则'
description: 在完成AmazonAmazon销售渠道入门培训流程时，创建初始列表规则以便为您的 [!DNL Commerce] 产品。
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 入门：创建列表规则

上市规则可以在用户引导期间定义，也可以随时修改。 新用户引导后，您可以访问 [上市规则](./listing-rules.md) 在商店中 [仪表板](./amazon-store-dashboard.md).

## 在新用户引导期间创建列表规则

1. 连接存储后，单击 **[!UICONTROL View Store]** （对于添加的存储区）。

   商店 [仪表板](./amazon-store-dashboard.md) 显示为 `No products listed to Amazon` 消息。

1. 单击 **[!UICONTROL Preview and List Eligible Products]**.

   此 _[!UICONTROL Listing Rules]_页面。

1. 为在Amazon上列出的产品资格定义所需条件，然后单击 **[!UICONTROL Preview changes]**，或单击 **[!UICONTROL Preview changes]** 跳过此步骤。

   参见 [示例：定义条件](./ob-define-condition-example.md).

1. 在“列表预览”中查看列表：

   ![列表预览](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]**  — 根据您当前的列表规则设置，此选项卡上列出的产品不符合Amazon列表的条件。

      不符合条件的产品不会发布到Amazon。 如果Amazon上已列出不合格产品，并且您将Amazon列表与您的 [!DNL Commerce] 目录产品，Amazon列表的数量更改为 `0` 以防止产品销售。 要手动从Amazon中删除列表，请参阅 [结束Amazon列表](./end-listings-manually.md). 此处不列出不符合Amazon要求的产品。 这些产品在 [[!UICONTROL Inactive Listings] 选项卡](./inactive-listings.md).

      要更改 `Ineligible` 列为 `Eligible` 列出，重复此过程并修改您的列出规则。

   - **[!UICONTROL Eligible Listings]**  — 根据您当前的列表规则设置，此选项卡上列出的产品有资格加入Amazon列表，并且有资格符合Amazon要求。 此选项卡包括已导入的现有Amazon列表(如果您具有 **[!UICONTROL Import Third Party Listings]** 设置为 `Import Listing` 在您的 [列表设置](./listing-settings.md))。

   - **[!UICONTROL New Listings]**  — 此选项卡上列出的产品包括 [!DNL Commerce] 根据当前的列表规则设置新建符合Amazon列表条件的目录产品并创建Amazon列表。

1. 完成后，单击 **[!UICONTROL Save and Close]**.

   商店 [仪表板](./amazon-store-dashboard.md) 打开。

完成载入商店后，信息会在 [!DNL Commerce] 和Amazon的启动。 您的Amazon列表已导入到 [!DNL Commerce] 并尝试与中的产品进行匹配 [!DNL Commerce] 目录。

Amazon您可以在 _[!UICONTROL Recent Orders]_区段。 参见 [存储仪表板](./amazon-store-dashboard.md) 或 [管理订单](./managing-orders.md).

>[!IMPORTANT]
>
>有一些重要的商店设置（列表、定价、规则、履行等）具有新商店的默认值。 要确保您的商店设置为满足您的特定需求，请查看您的 [存储设置](./default-store-settings.md) .

![“下一步”图标](assets/btn-next.png) [**继续使用默认存储设置**](./default-store-settings.md)
