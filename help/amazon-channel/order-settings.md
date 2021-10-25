---
title: 订单设置
description: Use the Order settings to determine how Amazon orders are imported into and processed in your Commerce store.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# 顺序设置

订单设置定义是否以及如何在中导入和处理Amazon订单 [!DNL Commerce] 和可在 [存储仪表板](./amazon-store-dashboard.md).

The order import settings are set to `Enabled` by default, which means that your Amazon orders appear on the store dashboard and create corresponding [!DNL Commerce] orders. Imported orders can be managed in the [!DNL Commerce] [Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;} workflow.

>[!NOTE]
>
>Regardless of your order settings, Amazon orders that existed before your store integration are not imported.

之后 [存储集成](./store-integration.md) 完成后，您可以更改顺序设置。 If you set your order settings to `Disabled`, Amazon orders are displayed on the store dashboard but must be managed in your [!DNL Amazon Seller Central] account.

在Amazon上创建订单后，不会立即将其导入 [!DNL Commerce]. Amazon分配 `Pending` 新创建订单的状态。 在Amazon验证订单和付款方式后，订单的状态将更改为 `Unshipped`. 此状态更改会触发订单导入，并且 [!DNL Commerce] 创建匹配的对应顺序。

从Amazon导入的订单可以在 [!DNL Commerce] [订单工作流](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}。 另请参阅 [管理订单](./managing-orders.md).

## 配置订单设置 {#configure-order-settings}

1. Click **[!UICONTROL Order Settings]** on the store dashboard.

1. 对于 **[!UICONTROL Import Amazon Orders]** （必需），选择选项：

   - `Disabled`  — 选择您不想在 [!DNL Commerce] 从Amazon收到新订单时。 选择后，此页面上的所有其他字段都将被禁用。

   - `Enabled`  — （默认）选择要创建对应的时间 [!DNL Commerce] 从Amazon收到新订单时的订单。 [!DNL Commerce] 根据Amazon状态和库存级别创建订单。

      >[!NOTE]
      >
      >导入Amazon订单必须设置为 `Enabled` 管理Amazon订单 [!DNL Commerce] [订购](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作流。 当设置为 `Disabled`，则您的Amazon订单没有对应的 [!DNL Commerce] 订单号，无法在 [!DNL Commerce]. 您可以在 [!DNL Amazon Seller Central] 帐户。

1. 对于 **[!UICONTROL Import Amazon Orders Into Magento Store]**，选择 [!DNL Commerce] 存储在中创建相应订单时与关联的Amazon订单 [!DNL Commerce].

   此设置默认为在您 [添加了Amazon商店](./store-integration.md). 如果要更改此设置，选项列表取决于 [!DNL Commerce] 存储您在配置中设置的。 请参阅 [商店](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target=&quot;_blank&quot;}。

1. For **[!UICONTROL Customer Creation]**, choose an option:

   - `No Customer Creation (guest)` - (Default) Choose when you do not want to create a customer account in [!DNL Commerce] using the imported customer data from the Amazon order. 选择后， [!DNL Commerce] 处理导入的Amazon订单的方式与处理来宾结帐的方式相同 [!DNL Commerce].

   - `Build New Customer Account`  — 选择要在 [!DNL Commerce] 使用随Amazon订单一起导入的客户数据。 此选项可帮助根据Amazon订单构建客户数据库。

1. 对于 **[!UICONTROL Order Number Source]**，选择选项：

   - `Build Using Magento Order Number`  — （默认）选择要创建唯一 [!DNL Commerce] 相应Amazon订单的订单号使用 [!DNL Commerce] 增量分配的订单ID。

   - `Build Using Amazon Order Number`  — 选择要创建 [!DNL Commerce] 订单编号。
   >[!NOTE]
   >
   >导入订单后，Amazon订单编号显示在 _[!UICONTROL Recent Orders]_列表。 的 [!DNL Commerce] 在 [!DNL Commerce] [订单数](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作区。

1. 对于 **[!UICONTROL Order Status]** （必需），选择选项：

   - `Default Order Status`  — （默认）选择您希望何时为新创建的从Amazon导入的订单分配您为新订单定义的默认订单状态。 新订单的默认状态（除非您为新订单创建了自定义订单状态）为 `Pending`. 请参阅 [处理订单](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}。

   - `Custom Order Status`  — 选择希望何时为从Amazon导入的新创建订单分配默认以外的状态。

   - `Processing Order Status`  — 在 **[!UICONTROL Order Status]** 设置为 `Custom Order Status`. 选择要用于从Amazon导入的新创建订单的状态。 此字段中的选项基于 [!DNL Commerce]. 请参阅 [订单状态](https://docs.magento.com/user-guide/sales/order-status.html). 您还可以创建要在此处显示以供选择的自定义订单状态。 要创建自定义订单状态，请参阅 [自定义订单状态](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}。

1. 完成后，单击 **[!UICONTROL Save order settings]**.

![顺序设置](assets/amazon-order-settings.png)

| 字段 | 描述 |
|---|---|
| [!UICONTROL Import Amazon Orders] | 选项：<ul><li>**[!UICONTROL Disabled]**  — 选择您不想在 [!DNL Commerce] 从Amazon收到新订单时。 选择后，此页面上的所有其他字段都将被禁用。</li><li>**[!UICONTROL Enabled]**  — （默认）选择要创建对应的时间 [!DNL Commerce] 从Amazon收到新订单时的订单。 [!DNL Commerce] 根据Amazon状态和库存级别创建订单。</li></ul><br><br>`Enabled` 必须选择在 [!DNL Commerce]. When `Disabled` 选择后，您的Amazon订单会显示在商店仪表板上，但订单必须在 [!DNL Amazon Seller Central] 帐户。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | 选择 [!DNL Commerce] 存储在中创建Amazon订单时，与关联的 [!DNL Commerce] [订单数](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}工作区。 此设置默认为 [!DNL Commerce] 在您 [添加了Amazon商店](./store-integration.md). 如果要更改此设置，选项列表取决于 [!DNL Commerce] 存储您在配置中设置的。 See [Stores](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | 选项：<ul><li>**[!UICONTROL No Customer Creation (guest)]**  — （默认）选择您不希望在 [!DNL Commerce] 使用从Amazon订单导入的客户数据。 选择此选项后，将告知 [!DNL Commerce] 处理导入的Amazon订单的方式与处理来宾结帐的方式相同。</li><li>**[!UICONTROL Build New Customer Account]**  — 选择要在 [!DNL Commerce] 使用随Amazon订单一起导入的客户数据的客户数据库。 此选项可帮助构建 [!DNL Commerce] 客户数据库。</li></ul> |
| 订单编号来源 | 选项：<ul><li>**[!UICONTROL Build Using Magento Order Number]**  — （默认）选择要创建唯一 [!DNL Commerce] 相应Amazon订单的订单号使用 [!DNL Commerce] 增量分配的订单ID。 </li><li>**使用Amazon订单号构建**  — 选择要创建 [!DNL Commerce] 订单编号。</li></ul> |
| 待定订单 | Options:<ul><li>**[!UICONTROL Do Not Reserve Quantity]**  — 选择不希望 [!DNL Commerce] 受您的Amazon订单影响的库存数量。 选择是否将Amazon用于履行流程(FBA)。 选择后，您会收到Amazon订单，订购数量不会影响您的 [!DNL Commerce] 库存数量。</li><li>**[!UICONTROL Reserve Quantity]**  — 选择您希望Amazon订单中的订单数量在 [!DNL Commerce] 库存数量。 选择并收到Amazon订单后，订购的数量将“保留”在 [!DNL Commerce] 库存数量，以防止您 [!DNL Commerce] “超卖”的股票。 “保留”数量不能通过 [!DNL Commerce] 店面。</li></ul> |
| [!UICONTROL Order Status] | Options:<ul><li>**[!UICONTROL Default Order Status]**  — （默认）选择您希望何时为新创建的从Amazon导入的订单分配新订单的默认订单状态。 新订单的默认状态（除非您为新订单创建了自定义订单状态）为 `Pending`. 请参阅 [处理订单](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]**  — 选择希望何时为从Amazon导入的新创建订单分配默认以外的状态。 选择后， **[!UICONTROL Processing Order Status]** 允许您选择要用于从Amazon导入的新创建订单的状态。</li></ul> |
| [!UICONTROL Processing Orders Status] | 在 _[!UICONTROL Order Status]_设置为 `Custom Order Status`. 选择要分配给新订单的订单状态。 此字段中的选项取决于 [!DNL Commerce]. 请参阅 [订单状态](https://docs.magento.com/user-guide/sales/order-status.html){target=&quot;_blank&quot;}。 您还可以创建要在此显示的自定义订单状态。 要创建自定义订单状态，请参阅 [自定义订单状态](https://docs.magento.com/user-guide/sales/order-status-custom.html){target=&quot;_blank&quot;}。 |

## [!DNL Commerce] order creation

[!DNL Commerce] 将根据以下状态和库存条件为Amazon订单创建订单。

### 使用库存管理创建订单

>[!NOTE]
>
>仅在Adobe Commerce和Magento Open Source2.3.x集成中受支持。

| 履行渠道 | [!DNL Commerce] 库存状态 | Amazon订单状态 | [!UICONTROL Create Magento Order] 设置 | 库存保留 |
|---|---|---|---|---|
| FBA | In-stock<br>Out-of-stock<br>Do Not Manage | Pending | 否 | 否 |
| FBA | 现车<br>缺货<br>不管理 | 待定可用性 | 否 | No |
| FBA | 现车<br>缺货<br>不管理 | 已取消 | 否 | 否 |
| FBA | 现车<br>缺货<br>不管理 | 错误 | 否 | 否 |
| FBA | 现车<br>缺货<br>不管理 | 未发货 | 否 | 否 |
| FBA | In-stock<br>Out-of-stock<br>Do Not Manage | PartiallyShipped | 否 | 否 |
| FBA | 现车<br>不管理 | 已发运 | Yes | No |
| FBA | Out-of-stock | Shipped | 否 | No |
| FBM | 现车<br>缺货<br>不管理 | Pending | 否 | 否 |
| FBM | In-stock<br>Out-of-stock<br>Do Not Manage | 待定可用性 | 否 | 否 |
| FBM | 现车<br>缺货<br>不管理 | 已取消 | 否 | 否 |
| FBM | 现车<br>缺货<br>不管理 | 错误 | 否 | 否 |
| FBM | 现车<br>不管理 | 未发货 | 是 | 是 |
| FBM | 缺货 | 未发货 | 否 | 否 |
| FBM | 现车<br>不管理 | PartiallyShipped | 是 | 是 |
| FBM | 缺货 | PartiallyShipped | 否 | 否 |
| FBM | 现车<br>不管理 | 已发运 | 是 | 是 |
| FBM | 缺货 | 已发运 | No | 否 |

>[!NOTE]
>If an Amazon order is imported in a `Partially Shipped` or `Shipped` status, the inventory reservation that is created is for all items in the order. Amazon销售渠道不会补偿以前发运的项目。
>
>如果订单由Amazon(FBA)履行，但物料在 `out of stock` 状态， [!DNL Commerce] 无法创建相应的订单。 这是库存管理集成的一个限制。
