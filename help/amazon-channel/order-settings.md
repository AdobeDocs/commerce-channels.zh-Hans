---
title: 订单设置
description: 使用“订单”设置确定如何将Amazon订单导入到您的商店并在其中进行处理。
redirect_from: /sales-channels/asc/ob-order-settings.html: 
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1462
ht-degree: 0%

---

# 顺序设置

顺序设置定义在[!DNL Commerce]中导入和处理Amazon订单的情况和方式，并可在[存储功能板](./amazon-store-dashboard.md)上访问该订单。

默认情况下，订单导入设置将设置为`Enabled`，这意味着您的Amazon订单显示在商店仪表板上并创建相应的[!DNL Commerce]订单。 可以在[!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}工作流中管理导入的订单。

>[!NOTE]
>
>无论您的订单设置如何，都不会导入存储集成之前存在的Amazon订单。

[存储集成](./store-integration.md)完成后，您可以更改顺序设置。 如果将订单设置设置为`Disabled`，则Amazon订单会显示在商店仪表板上，但必须在您的[!DNL Amazon Seller Central]帐户中进行管理。

在Amazon上创建订单后，不会立即将其导入[!DNL Commerce]。 Amazon会为新创建的订单分配`Pending`状态。 在Amazon验证订单和付款方式后，订单的状态将更改为`Unshipped`。 此状态更改会触发订单导入，并且[!DNL Commerce]会创建一个匹配的对应顺序。

从Amazon导入的订单可以在[!DNL Commerce] [订单工作流](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}中管理。 另请参阅[管理订单](./managing-orders.md)。

## 配置订单设置 {#configure-order-settings}

1. 单击存储仪表板上的&#x200B;**[!UICONTROL Order Settings]**。

1. 对于&#x200B;**[!UICONTROL Import Amazon Orders]**（必需），选择一个选项：

   - `Disabled`  — 选择从Amazon接收新订单时，您不想 [!DNL Commerce] 在中创建相应订单的时间。选择后，此页面上的所有其他字段都将被禁用。

   - `Enabled`  — （默认）选择在从Amazon收到新订 [!DNL Commerce] 单时要创建相应订单的时间。[!DNL Commerce] 根据Amazon状态和库存级别创建订单。

      >[!NOTE]
      >
      >要在[!DNL Commerce] [订单](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}工作流中管理Amazon订单，必须将“导入Amazon订单”设置为`Enabled`。 当设置为`Disabled`时，您的Amazon订单没有相应的[!DNL Commerce]订单号，无法在[!DNL Commerce]中管理。 您可以在[!DNL Amazon Seller Central]帐户中管理这些订单。

1. 对于&#x200B;**[!UICONTROL Import Amazon Orders Into Magento Store]**，选择在[!DNL Commerce]中创建相应订单时，与哪个[!DNL Commerce]存储Amazon订单相关联。

   此设置默认为在您[添加Amazon商店](./store-integration.md)时所选网站的“商店视图”。 如果要更改此设置，选项列表取决于您在配置中设置的[!DNL Commerce]存储。 请参阅[Stores](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){:target=&quot;_blank&quot;}。

1. 对于&#x200B;**[!UICONTROL Customer Creation]**，选择一个选项：

   - `No Customer Creation (guest)`  — （默认）选择您何时不想在中使用从Amazon订单导 [!DNL Commerce] 入的客户数据创建客户帐户。选择[!DNL Commerce]后，会像在[!DNL Commerce]中处理来宾结账一样处理导入的Amazon订单。

   - `Build New Customer Account`  — 选择您何时要在中使用随Amazon订单导 [!DNL Commerce] 入的客户数据创建新客户帐户。此选项可帮助根据Amazon订单构建客户数据库。

1. 对于&#x200B;**[!UICONTROL Order Number Source]**，选择一个选项：

   - `Build Using Magento Order Number`  — （默认）选择您何时要使用递增分配 [!DNL Commerce] 的订单ID为相应的Amazon订单创 [!DNL Commerce] 建唯一订单编号。

   - `Build Using Amazon Order Number`  — 选择您何时要使用相应 [!DNL Commerce] 的Amazon分配的订单号创建订单号。
   >[!NOTE]
   >
   >导入订单后，Amazon订单编号会显示在商店仪表板的&#x200B;_[!UICONTROL Recent Orders]_列表中。 在[!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}工作区中查看订单详细信息时，会显示[!DNL Commerce]订单编号。

1. 对于&#x200B;**[!UICONTROL Order Status]**（必需），选择一个选项：

   - `Default Order Status`  — （默认）选择您希望何时为新创建的从Amazon导入的订单分配您为新订单定义的默认订单状态。新订单的默认状态（除非您为新订单创建了自定义订单状态）为`Pending`。 请参阅[处理订单](https://docs.magento.com/user-guide/sales/order-processing.html){:target=&quot;_blank&quot;}。

   - `Custom Order Status`  — 选择希望何时为从Amazon导入的新创建订单分配默认以外的状态。

   - `Processing Order Status`  — 将设置为 **[!UICONTROL Order Status]** 时启用 `Custom Order Status`。选择要用于从Amazon导入的新创建订单的状态。 此字段中的选项基于[!DNL Commerce]中的默认状态选项。 请参阅[订单状态](https://docs.magento.com/user-guide/sales/order-status.html)。 您还可以创建要在此处显示以供选择的自定义订单状态。 要创建自定义订单状态，请参阅[自定义订单状态](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}。

1. 完成后，单击&#x200B;**[!UICONTROL Save order settings]**。

![顺序设置](assets/amazon-order-settings.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Import Amazon Orders] | 选项：<ul><li>**[!UICONTROL Disabled]**  — 选择从Amazon接收新订单时，您不想 [!DNL Commerce] 在中创建相应订单的时间。选择后，此页面上的所有其他字段都将被禁用。</li><li>**[!UICONTROL Enabled]**  — （默认）选择在从Amazon收到新订 [!DNL Commerce] 单时要创建相应订单的时间。[!DNL Commerce] 根据Amazon状态和库存级别创建订单。</li></ul><br><br>`Enabled` 必须选择在中管理Amazon订 [!DNL Commerce]单。选择`Disabled`后，您的Amazon订单将显示在商店仪表板上，但订单必须在您的[!DNL Amazon Seller Central]帐户中进行管理。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | 选择在[!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}工作区中创建Amazon订单时，与哪个[!DNL Commerce]存储这些订单关联。 此设置默认为在您添加Amazon商店](./store-integration.md)时所选[!DNL Commerce]网站的“商店视图”。 [如果要更改此设置，选项列表取决于您在配置中设置的[!DNL Commerce]存储。 请参阅[Stores](https://docs.magento.com/user-guide/stores/stores-all-stores.html){:target=&quot;_blank&quot;}。 |
| [!UICONTROL Customer Creation] | 选项：<ul><li>**[!UICONTROL No Customer Creation (guest)]**  — （默认）选择您何时不想在中使用从Amazon订单导 [!DNL Commerce] 入的客户数据创建客户帐户。选中此选项后，会告知[!DNL Commerce]以处理导入的Amazon订单的方式与处理来宾结账的方式相同。</li><li>**[!UICONTROL Build New Customer Account]**  — 选择您何时要使用随Amazon订单导入的 [!DNL Commerce] 客户数据在客户数据库中创建新客户帐户。此选项可帮助根据您的Amazon订单构建[!DNL Commerce]客户数据库。</li></ul> |
| 订单编号来源 | 选项：<ul><li>**[!UICONTROL Build Using Magento Order Number]**  — （默认）选择您何时要使用递增分配 [!DNL Commerce] 的订单ID为相应的Amazon订单创 [!DNL Commerce] 建唯一订单编号。 </li><li>**使用Amazon订单号构建**  — 选择您何时要使用相应的 [!DNL Commerce] Amazon分配的订单号创建订单号。</li></ul> |
| 待定订单 | 选项：<ul><li>**[!UICONTROL Do Not Reserve Quantity]**  — 选择不希望库存数量受 [!DNL Commerce] Amazon订单影响的时间。选择是否将Amazon用于履行流程(FBA)。 选择并接收Amazon订单后，订购数量不会影响您的[!DNL Commerce]库存数量。</li><li>**[!UICONTROL Reserve Quantity]**  — 选择您希望何时在库存数量中“保留”Amazon订单中的订 [!DNL Commerce] 单数量。选择并收到Amazon订单后，订购数量将“保留”在您的[!DNL Commerce]库存数量中，以防止您的[!DNL Commerce]库存“过度销售”。 “保留”数量不能通过[!DNL Commerce]店面购买。</li></ul> |
| [!UICONTROL Order Status] | 选项：<ul><li>**[!UICONTROL Default Order Status]**  — （默认）选择您希望何时为新创建的从Amazon导入的订单分配新订单的默认订单状态。新订单的默认状态（除非您为新订单创建了自定义订单状态）为`Pending`。 请参阅[处理订单](https://docs.magento.com/user-guide/sales/order-processing.html)。</li><li>>**[!UICONTROL Custom Order Status]** — 选择您希望何时为从Amazon导入的新创建订单分配默认以外的状态。 选择&#x200B;**[!UICONTROL Processing Order Status]**&#x200B;后，您可以选择要用于从Amazon导入的新创建订单的状态。</li></ul> |
| [!UICONTROL Processing Orders Status] | 将&#x200B;_[!UICONTROL Order Status]_设置为`Custom Order Status`时启用。 选择要分配给新订单的订单状态。 此字段中的选项取决于[!DNL Commerce]中的默认状态选项。 请参阅[订单状态](https://docs.magento.com/user-guide/sales/order-status.html){:target=&quot;_blank&quot;}。 您还可以创建要在此显示的自定义订单状态。 要创建自定义订单状态，请参阅[自定义订单状态](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}。 |

## [!DNL Commerce] 订单创建

[!DNL Commerce] 将根据以下状态和库存条件为Amazon订单创建订单。

### 使用库存管理创建订单

>[!NOTE]
>
>仅在Adobe商务和Magento Open Source2.3.x集成中受支持。

| 履行渠道 | [!DNL Commerce] 库存状态 | Amazon订单状态 | [!UICONTROL Create Magento Order] 设置 | 库存保留 |
|---|---|---|---|---|
| FBA | In-stock<br>Out-of-stock<br>不管理 | 待定 | 否 | 否 |
| FBA | In-stock<br>Out-of-stock<br>不管理 | 待定可用性 | 否 | 否 |
| FBA | In-stock<br>Out-of-stock<br>不管理 | 已取消 | 否 | 否 |
| FBA | In-stock<br>Out-of-stock<br>不管理 | 错误 | 否 | 否 |
| FBA | In-stock<br>Out-of-stock<br>不管理 | 未发货 | 否 | 否 |
| FBA | In-stock<br>Out-of-stock<br>不管理 | PartiallyShipped | 否 | 否 |
| FBA | 库存<br>不管理 | 已发运 | 是 | 否 |
| FBA | 缺货 | 已发运 | 否 | 否 |
| FBM | In-stock<br>Out-of-stock<br>不管理 | 待定 | 否 | 否 |
| FBM | In-stock<br>Out-of-stock<br>不管理 | 待定可用性 | 否 | 否 |
| FBM | In-stock<br>Out-of-stock<br>不管理 | 已取消 | 否 | 否 |
| FBM | In-stock<br>Out-of-stock<br>不管理 | 错误 | 否 | 否 |
| FBM | 库存<br>不管理 | 未发货 | 是 | 是 |
| FBM | 缺货 | 未发货 | 否 | 否 |
| FBM | 库存<br>不管理 | PartiallyShipped | 是 | 是 |
| FBM | 缺货 | PartiallyShipped | 否 | 否 |
| FBM | 库存<br>不管理 | 已发运 | 是 | 是 |
| FBM | 缺货 | 已发运 | 否 | 否 |

>[!NOTE]
>如果Amazon订单以`Partially Shipped`或`Shipped`状态导入，则创建的库存保留适用于订单中的所有物料。 Amazon销售渠道不会补偿以前发运的项目。
>
>如果订单由Amazon(FBA)履行，但物料处于`out of stock`状态，则[!DNL Commerce]无法创建相应的订单。 这是库存管理集成的一个限制。
