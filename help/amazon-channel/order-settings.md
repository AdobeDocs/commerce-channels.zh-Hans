---
title: Amazon订单设置
description: 使用订单设置可确定如何将Amazon订单导入您的Commerce商店并在该商店中进行处理。
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Amazon订单设置

订单设置定义是否以及如何将Amazon订单导入到[!DNL Commerce]中并在[商店仪表板](./amazon-store-dashboard.md)中进行处理。

默认情况下，订单导入设置设为`Enabled`，这意味着您的Amazon订单出现在商店仪表板上，并创建相应的[!DNL Commerce]订单。 可以在[!DNL Commerce] [订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作流中管理导入的订单。

>[!NOTE]
>
>无论您的订单设置如何，都不会导入应用商店集成之前存在的Amazon订单。

在[存储集成](./store-integration.md)完成后，您可以更改订单设置。 如果将订单设置设置为`Disabled`，则Amazon订单会显示在商店仪表板上，但必须在[!DNL Amazon Seller Central]帐户中进行管理。

在Amazon中创建订单时，不会立即将其导入[!DNL Commerce]。 Amazon将`Pending`状态分配给新创建的订单。 在Amazon验证订单和付款方式后，订单的状态将更改为`Unshipped`。 此状态更改将触发订单导入，[!DNL Commerce]将创建一个匹配的相应订单。

从Amazon导入的订单可在[!DNL Commerce] [订单工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)中进行管理。 另请参阅[管理订单](./managing-orders.md)。

## 配置订单设置 {#configure-order-settings}

1. 单击商店仪表板上的&#x200B;**[!UICONTROL Order Settings]**。

1. 对于&#x200B;**[!UICONTROL Import Amazon Orders]** （必需），请选择一个选项：

   - `Disabled` — 在从Amazon收到新订单时，选择您不想在[!DNL Commerce]中创建相应订单的时间。 选中后，将禁用此页上的所有其他字段。

   - `Enabled` — （默认）在从Amazon收到新订单时，选择创建对应的[!DNL Commerce]订单的时间。 [!DNL Commerce]订单是根据Amazon状态和库存水平创建的。

     >[!NOTE]
     >
     >导入Amazon订单必须设置为`Enabled`才能在[!DNL Commerce] [订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作流中管理Amazon订单。 当设置为`Disabled`时，您的Amazon订单没有相应的[!DNL Commerce]订单编号，无法在[!DNL Commerce]中管理。 您可以在[!DNL Amazon Seller Central]帐户中管理这些订单。

1. 对于&#x200B;**[!UICONTROL Import Amazon Orders Into Magento Store]**，选择在[!DNL Commerce]中创建相应订单时，Amazon订单与哪个[!DNL Commerce]存储相关联。

   当您[添加了Amazon商店](./store-integration.md)时，此设置默认为所选网站的“商店视图”。 如果要更改此设置，则选项列表取决于您在配置中设置的[!DNL Commerce]存储。 查看[商店](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html)。

1. 对于&#x200B;**[!UICONTROL Customer Creation]**，请选择一个选项：

   - `No Customer Creation (guest)` — （默认）当您不想使用从Amazon订单导入的客户数据在[!DNL Commerce]中创建客户帐户时，选择此选项。 选择后，[!DNL Commerce]处理导入的Amazon订单的方式与处理[!DNL Commerce]中的来宾结帐的方式相同。

   - `Build New Customer Account` — 选择何时使用随Amazon订单导入的客户数据在[!DNL Commerce]中创建新客户帐户。 此选项有助于根据Amazon订单构建客户数据库。

1. 对于&#x200B;**[!UICONTROL Order Number Source]**，请选择一个选项：

   - `Build Using Magento Order Number` — （默认）当您要使用[!DNL Commerce]增量分配的订单ID为相应的Amazon订单创建唯一的[!DNL Commerce]订单编号时，请选择此选项。

   - `Build Using Amazon Order Number` — 选择何时要使用对应的Amazon分配的订单编号创建[!DNL Commerce]订单编号。

   >[!NOTE]
   >
   >导入订单后，Amazon订单编号将显示在商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_列表中。 在[!DNL Commerce] [订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作区中查看订单详细信息时显示[!DNL Commerce]订单编号。

1. 对于&#x200B;**[!UICONTROL Order Status]** （必需），请选择一个选项：

   - `Default Order Status` — （默认）选择何时希望为从Amazon导入的新创建订单分配您为新订单定义的默认订单状态。 新订单的默认状态（除非您为新订单创建了自定义订单状态）为`Pending`。 请参阅[处理订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)。

   - `Custom Order Status` — 选择何时希望为从Amazon导入的新创建订单分配默认状态以外的状态。

   - `Processing Order Status` — 当&#x200B;**[!UICONTROL Order Status]**&#x200B;设置为`Custom Order Status`时启用。 选择要用于从Amazon导入的新创建订单的状态。 此字段中的选项基于[!DNL Commerce]中的默认状态选项。 查看[订单状态](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html)。 您还可以创建自定义订单状态，以在此处显示以供选择。 要创建自定义订单状态，请参阅[自定义订单状态](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status)。

1. 完成后，单击&#x200B;**[!UICONTROL Save order settings]**。

![订单设置](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | 选项：<ul><li>**[!UICONTROL Disabled]** — 在从Amazon收到新订单时，选择您不想在[!DNL Commerce]中创建相应订单的时间。 选中后，将禁用此页上的所有其他字段。</li><li>**[!UICONTROL Enabled]** — （默认）在从Amazon收到新订单时，选择创建对应的[!DNL Commerce]订单的时间。 [!DNL Commerce]订单是根据Amazon状态和库存水平创建的。</li></ul>必须选择<br><br>`Enabled`才能在[!DNL Commerce]中管理Amazon订单。 选择`Disabled`后，您的Amazon订单会显示在商店仪表板上，但必须在[!DNL Amazon Seller Central]帐户中管理这些订单。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | 选择在[!DNL Commerce] [订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)工作区中创建Amazon订单时与哪个[!DNL Commerce]商店关联。 当您[添加了Amazon商店](./store-integration.md)时，此设置默认为[!DNL Commerce]所选网站的“商店视图”。 如果要更改此设置，则选项列表取决于您在配置中设置的[!DNL Commerce]存储。 查看[商店](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html)。 |
| [!UICONTROL Customer Creation] | 选项：<ul><li>**[!UICONTROL No Customer Creation (guest)]** — （默认）当您不想使用从Amazon订单导入的客户数据在[!DNL Commerce]中创建客户帐户时，选择此选项。 选择此选项后，此选项会告知[!DNL Commerce]以处理访客结帐的方式处理导入的Amazon订单。</li><li>**[!UICONTROL Build New Customer Account]** — 选择何时使用随Amazon订单导入的客户数据在[!DNL Commerce]客户数据库中创建新客户帐户。 此选项有助于根据Amazon订单构建[!DNL Commerce]客户数据库。</li></ul> |
| 订单号Source | 选项：<ul><li>**[!UICONTROL Build Using Magento Order Number]** — （默认）当您要使用[!DNL Commerce]增量分配的订单ID为相应的Amazon订单创建唯一的[!DNL Commerce]订单编号时，请选择此选项。 </li><li>**使用Amazon订单编号生成** — 选择何时使用相应的Amazon分配的订单编号创建[!DNL Commerce]订单编号。</li></ul> |
| 待处理订单 | 选项：<ul><li>**[!UICONTROL Do Not Reserve Quantity]** — 选择何时不希望您的[!DNL Commerce]库存数量受您的Amazon订单影响。 选择您是否将Amazon用于履行流程(FBA)。 选择并接收Amazon订单后，订购数量不会影响您的[!DNL Commerce]库存数量。</li><li>**[!UICONTROL Reserve Quantity]** — 当您希望Amazon订单中的订单数量在[!DNL Commerce]库存数量中为“预留”时，请选择此选项。 选择并且您收到Amazon订单后，订购的数量将“预留”在您的[!DNL Commerce]库存数量中，以防止您的[!DNL Commerce]库存“过度销售”。 “预留”数量不能通过您的[!DNL Commerce]店面购买。</li></ul> |
| [!UICONTROL Order Status] | 选项：<ul><li>**[!UICONTROL Default Order Status]** — （默认）选择何时要将从Amazon导入的新创建订单分配给新订单的默认订单状态。 新订单的默认状态（除非您为新订单创建了自定义订单状态）为`Pending`。 请参阅[处理订单](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)。</li><li>**[!UICONTROL Custom Order Status]** — 选择何时希望为从Amazon导入的新创建订单分配默认状态以外的状态。 选择后，**[!UICONTROL Processing Order Status]**&#x200B;允许您选择要用于从Amazon导入的新创建订单的状态。</li></ul> |
| [!UICONTROL Processing Orders Status] | 当&#x200B;_[!UICONTROL Order Status]_设置为`Custom Order Status`时启用。 选择要分配给新订单的订单状态。 此字段中的选项取决于[!DNL Commerce]中的默认状态选项。 查看[订单状态](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html)。 您还可以创建要在此处显示的自定义订单状态。 要创建自定义订单状态，请参阅[自定义订单状态] |

## [!DNL Commerce]订单创建

基于以下状态和库存条件，为Amazon订单创建[!DNL Commerce]个订单。

### 使用Inventory management创建订单

>[!NOTE]
>
>仅在Adobe Commerce和Magento Open Source 2.3.x集成中受支持。

| 履行渠道 | [!DNL Commerce]库存状态 | Amazon订单状态 | [!UICONTROL Create Magento Order]设置 | 预留库存 |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | 缺货<br>缺货<br>不管理 | 待处理 | 否 | 否 |
| FBA | 缺货<br>缺货<br>不管理 | Pendingavailability | 否 | 否 |
| FBA | 缺货<br>缺货<br>不管理 | 已取消 | 否 | 否 |
| FBA | 缺货<br>缺货<br>不管理 | 错误 | 否 | 否 |
| FBA | 缺货<br>缺货<br>不管理 | 未发货 | 否 | 否 |
| FBA | 缺货<br>缺货<br>不管理 | 已部分装运 | 否 | 否 |
| FBA | 库存<br>不管理 | 已发货 | 是 | 否 |
| FBA | 缺货 | 已发货 | 否 | 否 |
| FBM | 缺货<br>缺货<br>不管理 | 待处理 | 否 | 否 |
| FBM | 缺货<br>缺货<br>不管理 | Pendingavailability | 否 | 否 |
| FBM | 缺货<br>缺货<br>不管理 | 已取消 | 否 | 否 |
| FBM | 缺货<br>缺货<br>不管理 | 错误 | 否 | 否 |
| FBM | 库存<br>不管理 | 未发货 | 是 | 是 |
| FBM | 缺货 | 未发货 | 否 | 否 |
| FBM | 库存<br>不管理 | 已部分装运 | 是 | 是 |
| FBM | 缺货 | 已部分装运 | 否 | 否 |
| FBM | 库存<br>不管理 | 已发货 | 是 | 是 |
| FBM | 缺货 | 已发货 | 否 | 否 |

>[!NOTE]
>如果Amazon订单以`Partially Shipped`或`Shipped`状态导入，则创建的库存预留适用于订单中的所有项目。 Amazon sales channel不对以前发运的项目进行补偿。
>
>如果订单已由Amazon (FBA)履行，但某个项目处于`out of stock`状态，[!DNL Commerce]无法创建对应的订单。 这是Inventory management集成的限制。
