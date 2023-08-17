---
title: '''查看和管理订单 [!DNL Channel Manager]’'
description: '''查看和管理 [!DNL Walmart Marketplace] 订单 [!DNL Channel Manager] 用于Adobe Commerce和Magento Open Source。”'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# 查看和跟踪订单 [!DNL Channel Manager]

[!DNL Walmart Marketplace] 订单数据 [!DNL Commerce] 产品自动同步到 [!DNL Channel Manager] 之后 [!DNL Walmart] 处理订单。

在 [!DNL Commerce] 成功同步将触发以下操作：

- [!DNL Channel Manager] 向沃尔玛发送订单确认函。

- 对应的 [!DNL Commerce] 订单是从沃尔玛订单创建的。

- 更新的订单信息将显示在 [!DNL Channel Manager] 订单仪表板。

在店面管理员中，您可以查看以下位置的订单数据 [!DNL Channel Manager] 打开sales channel store并选择 **[!UICONTROL Orders]**.

![要管理的渠道管理器订单视图 [!DNL Walmart Marketplace] 订单](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>可能最多需要35分钟才能完成 [!DNL Walmart Marketplace] 以在 [!DNL Channel Manager] 订单列表。 [!DNL Walmart] 大约需要30分钟来处理传入订单并将它们发送到 [!DNL Channel Manager]. 渠道管理器收到订单后，大约需要五分钟才能在Adobe Commerce或Magento Open Source中创建并显示订单。

## 订单控件和列说明

下表描述了可用于“订单”的控件和列。

**控件[!UICONTROL Orders]**

<table>
<tr>
<td><strong>控件</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>通过选择以下选项之一对视图进行排序： [!UICONTROL Order Status] 卡片。</td>
</tr>
<tr>
<td>状态详细信息</td>
<td>提供有关订单错误和退货请求的信息。 要查看订单的退货信息和退款状态，请选择 <strong>[!UICONTROL Return requested]</strong> 文本以打开 [!UICONTROL Returns] 仪表板。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>要查看订单详细信息，请选择 [!DNL Commerce] 中的订单编号 [!UICONTROL Order] 表格。 然后，使用 [!DNL Commerce] 订单选项以处理订单。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>要修改通道配置，请选择通道Walmart连接凭据、映射的属性或发运标识符，设置选择 [!DNL Commerce] 中的订单编号 [!UICONTROL Order] 表格。 然后，使用 [!DNL Commerce] 订单选项以处理订单。</td>
</tr>
</table>


**列描述**

<table>
<tr>
<td>字段</td>
<td>描述</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>在中分配给订单的采购订单编号 [!DNL Walmart Marketplace]. 当订单最初导入到时 [!DNL Channel Manager]，仅 [!DNL Walmart] 将显示订单编号。 当 [!DNL Commerce] 创建订单， [!DNL Walmart] 订单编号存储在 [!UICONTROL External ID] 产品属性。</td>
</tr>
<tr>
<td>[!DNL Commerce] 订单编号</td>
<td>分配给 [!DNL Commerce] 订单创建自 [!DNL Walmart Marketplace] 顺序。</td>
</tr>
<tr>
<td>项目</td>
<td>排序的项数 [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>订购物料的总成本。</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>将订单提交到的日期 [!DNL Walmart Marketplace] 转换为本地时区。</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>订单必须发货才能达到的日期 [!DNL Walmart Marketplace] 要求已转换为本地时区。
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>必须向客户交付订单才能满足的日期 [!DNL Walmart Marketplace] 要求已转换为本地时区。</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>该[[!DNL Walmart Marketplace] 配送方式](已为订单选择https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29。</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>指示上次更新订单数据的时间戳 [!DNL Channel Manager] 转换为本地时区。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>指示中的当前订单状态 [!DNL Commerce] 订单工作流。 从导入的订单的初始状态 [!DNL Walmart Marketplace] 是_Open_。 其他状态更新发生于 [!DNL Commerce] 订单已处理并且 [!DNL Channel Manager] 将发运、部分发运和取消更新成功同步到 [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>提供有关存在错误或退款请求的订单的更多详细信息。</td>
</tr>
</table>

## 订单状态

[!UICONTROL Order Status] 提供有关当前状态的信息， [!DNL Walmart Marketplace] 从Adobe Commerce或Magento Open Source管理的订单。 订单状态更新发生于 [!DNL Channel Manager] 从以下任一位置接收更新的订单信息： [!DNL Walmart Marketplace] 或 [!DNL Commerce] 订购系统。 订单可以具有以下状态：

- **[!UICONTROL Shipped]** — 已发运的订单来自 [!DNL Commerce] 商店。 当订单发送时， [!DNL Channel Manager] 发送更新到 [!DNL Walmart Marketplace] 更新沃尔玛上的发运状态，并提供发运的订单跟踪编号。 如果沃尔玛签发了“退货商品授权”表格，则订单在发运后可以部分或全部退款。 请参阅 [退货和退款](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** — 某些物料标记为已发运的订单，而其它物料则等待发运的订单。 当订单中的物料发运时， [!DNL Channel Manager] 发送更新到 [!DNL Walmart Marketplace] 要将装运状态更新为，请执行以下操作 _[!DNL Partially Shipped]_在沃尔玛上，并提供发货的订单跟踪号。

- **[!UICONTROL Canceled]** — 已取消的订单来自 [!DNL Commerce] 商店。

  订单取消完成后， [!DNL Commerce] 库存数量更新以反映退回的物料。 然后， [!DNL Channel Manager] 将更新同步到 [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]** — 如果沃尔玛商场要求退回已发运的订单项目，则 `Return requested` 链接显示在 [!UICONTROL Status details] 列。 选择链接将打开 [!UICONTROL Returns] 仪表板以查看退货并管理退款流程。

- **[!UICONTROL Error]** — 有错误的订单。 当订单更新操作失败时，可能会出现错误。 例如，在以下情况下会发生错误： [!DNL Channel Manager] 不能收到沃尔玛的新订单。 在以下情况下也会发生 [!DNL Channel Manager] 无法将订单发运或取消更新发送到 [!DNL Walmart Marketplace]. 如果操作失败，“订单”页将显示 _错误_ 订单的状态。 有关详细信息，请参阅 [修复订单错误](process-orders.md#fix-shipping-and-cancellation-errors)。

- **[!UICONTROL Status details]** — 提供有关由于缺少信息或无效值、发运详细信息不正确或订单取消失败等问题而出现的订单错误的详细信息。 该描述可帮助确定 [!DNL Commerce] 实例或在 [!DNL Walmart Marketplace].

>[!NOTE]
>
>如果订单物料通过多次发运发送，则订单状态为 [!DNL Channel Manager] 反映最后一个可用的订单状态。 例如，如果发运第一个项目，则在将订单更新同步到时未返回任何错误 [!DNL Channel Manager] 和 [!DNL Walmart Marketplace]， [!DNL Channel Manager] 订单状态为 _[!UICONTROL Partially Shipped]_. 如果第二个项目已发运并且 [!DNL Channel Manager] 返回错误，订单状态将更新为_[!UICONTROL Error]_.

## 查看订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 以打开 [!UICONTROL Channel Manager Marketplace Stores] 页面。

1. 通过选择商店条目行中的眼睛图标来打开商店视图。

1. 要查看订单信息，请选择*[!UICONTROL *Orders]**。

1. 获取有关订单的信息，并通过查看 **[状态](#order-status)** 列。

## 复查订单详细信息

从市场收到订单并导入到您的销售渠道商店后，请使用 [!DNL Commerce] 订单ID用于在Adobe Commerce中查看订单详细信息。

从 **[!UICONTROL Orders]**，选择 **[!UICONTROL Commerce Order Number]** 以打开 [!DNL Commerce] 订单详细信息。

![的商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

在Commerce店面中，订单导入自 [!DNL Walmart Marketplace] 订单数据中包括以下附加信息：

- **付款信息和送货方式** — 从Walmart导入的订单包括以下付款和装运字段的值：

   - **[!UICONTROL Offline Channel Payment]** — 指示订单付款由脱机处理 [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** — 显示 [!DNL Walmart Marketplace] 订单号。

   - **[!UICONTROL Channel Shipping - Value]** — 指示通过处理装运费用 [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** — 仅当从导入订单时，才会显示此字段 [!DNL Walmart Marketplace] 已取消。 取消原因包括：

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **已订购项目** — 此部分列出了所有Commerce订单上的订单项。 此 [!UICONTROL Qty] 列提供订单项目的状态历史记录。 例如，如果订单已开票、发运和退款，则您可以查看状态转换。

  ![订单详细信息订购物料状态历史记录 [!DNL Walmart Marketplace] 订单](assets/order-detail-status-history.png){width="600" zoomable="yes"}

通过选择 [!UICONTROL Invoice] 和 [!UICONTROL Credit Memo] 选项。 您还可以直接从以下位置访问贷项通知单： [[!UICONTROL Returns]](return-refund-orders.md) 在您的sales channel store中的仪表板。
