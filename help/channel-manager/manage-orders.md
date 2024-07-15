---
title: '查看并管理来自 [!DNL Channel Manager]的订单'
description: '使用 [!DNL Channel Manager] 查看并管理Adobe Commerce和Magento Open Source的 [!DNL Walmart Marketplace] 订单。'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# 查看和跟踪来自[!DNL Channel Manager]的订单

[!DNL Commerce]产品的[!DNL Walmart Marketplace]订单数据在[!DNL Walmart]处理订单后自动同步到[!DNL Channel Manager]。

在[!DNL Commerce]端，成功的同步会触发以下操作：

- [!DNL Channel Manager]向沃尔玛发送订单确认。

- 已从沃尔玛订单创建相应的[!DNL Commerce]订单。

- 更新的订单信息显示在[!DNL Channel Manager]订单仪表板上。

在店面管理员中，您可以通过打开Sales Channel商店并选择&#x200B;**[!UICONTROL Orders]**&#x200B;来查看[!DNL Channel Manager]中的订单数据。

![渠道经理订单视图，用于管理[!DNL Walmart Marketplace]个订单](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Walmart Marketplace]订单最多可能需要35分钟才能显示在[!DNL Channel Manager]订单列表中。 [!DNL Walmart]大约需要30分钟来处理传入订单并将它们发送到[!DNL Channel Manager]。 渠道管理器收到订单后，大约需要五分钟才能在Adobe Commerce或Magento Open Source中创建并显示订单。

## 订单控件和列说明

下表描述了可用于“订单”的控件和列。

[!UICONTROL Orders]**的**&#x200B;控件

<table>
<tr>
<td><strong>控件</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>通过选择[!UICONTROL Order Status]卡片之一对视图进行排序。</td>
</tr>
<tr>
<td>状态详细信息</td>
<td>提供有关订单错误和退货请求的信息。 要查看订单的退货信息和退款状态，请选择<strong>[!UICONTROL Return requested]</strong>文本以打开[!UICONTROL Returns]仪表板。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>要查看订单详细信息，请在[!UICONTROL Order]表中选择[!DNL Commerce]订单编号。 然后，使用[!DNL Commerce]订单选项处理该订单。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>要修改通道配置，请选择通道Walmart连接凭据、映射的属性或装运标识符，设置则选择[!UICONTROL Order]表中的[!DNL Commerce]订单号。 然后，使用[!DNL Commerce]订单选项处理该订单。</td>
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
<td>在[!DNL Walmart Marketplace]中分配给订单的采购订单编号。 当订单最初导入到[!DNL Channel Manager]时，只显示[!DNL Walmart]订单编号。 创建[!DNL Commerce]订单时，[!DNL Walmart]订单编号存储在[!UICONTROL External ID]产品属性中。</td>
</tr>
<tr>
<td>[!DNL Commerce] 订单编号</td>
<td>分配给从[!DNL Walmart Marketplace]订单创建的[!DNL Commerce]订单的编号。</td>
</tr>
<tr>
<td>项目</td>
<td>在[!DNL Walmart Marketplace]上排序的项数。</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>订购物料的总成本。</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>将订单提交到[!DNL Walmart Marketplace]的日期转换为本地时区。</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>订单必须发货以符合转换为本地时区的[!DNL Walmart Marketplace]要求的日期。
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>必须向客户交付订单以满足转换为本地时区的[!DNL Walmart Marketplace]要求的日期。</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>为订单选择的[[!DNL Walmart Marketplace]配送方式](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29)。</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>时间戳，指示订单数据上次在[!DNL Channel Manager]内更新为本地时区的时间。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>指示[!DNL Commerce]订单工作流中的当前订单状态。 从[!DNL Walmart Marketplace]导入的订单的初始状态为_Open_。 当处理[!DNL Commerce]个订单并且[!DNL Channel Manager]成功将装运、部分装运和取消更新同步到[!DNL Walmart Marketplace]时，会发生其他状态更新。</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>提供有关存在错误或退款请求的订单的更多详细信息。</td>
</tr>
</table>

## 订单状态

[!UICONTROL Order Status]提供有关从Adobe Commerce或Magento Open Source管理的[!DNL Walmart Marketplace]订单的当前状态的信息。 当[!DNL Channel Manager]从[!DNL Walmart Marketplace]或[!DNL Commerce]订单系统收到更新的订单信息时，会发生订单状态更新。 订单可以具有以下状态：

- **[!UICONTROL Shipped]** — 从[!DNL Commerce]应用商店发运的订单。 当订单发货时，[!DNL Channel Manager]向[!DNL Walmart Marketplace]发送更新以更新沃尔玛上的发货状态并提供该发货的订单跟踪编号。 如果沃尔玛签发了“退货商品授权”表格，则订单在发运后可以部分或全部退款。 请参阅[退货和退款](return-refund-orders.md)。

- **[!UICONTROL Partially Shipped]** — 某些项目标记为已发货，而其他项目正在等待发运的订单。 当订单中的商品装运时，[!DNL Channel Manager]向[!DNL Walmart Marketplace]发送更新以将装运状态更新为沃尔玛上的&#x200B;_[!DNL Partially Shipped]_，并提供装运的订单跟踪编号。

- **[!UICONTROL Canceled]** — 已从[!DNL Commerce]存储区取消的订单。

  订单取消完成后，[!DNL Commerce]库存数量会更新以反映返回的物料。 然后，[!DNL Channel Manager]将更新同步到[!DNL Walmart Marketplace]。

- **[!UICONTROL Return requested]** — 如果沃尔玛商城请求退回已发运的订单项目，则[!UICONTROL Status details]列中将显示一个`Return requested`链接。 选择链接将打开[!UICONTROL Returns]仪表板以查看退货并管理退款流程。

- **[!UICONTROL Error]** — 有错误的订单。 当订单更新操作失败时，可能会出现错误。 例如，如果[!DNL Channel Manager]无法从沃尔玛接收新订单，则会发生错误。 如果[!DNL Channel Manager]无法向[!DNL Walmart Marketplace]发送订单装运或取消更新，也可能发生这种情况。 如果操作失败，“订单”页将显示订单的&#x200B;_错误_&#x200B;状态。 有关详细信息，请参阅[修复订单错误](process-orders.md#fix-shipping-and-cancellation-errors)。

- **[!UICONTROL Status details]** — 提供有关由于缺少信息或无效值、装运详细信息不正确或订单取消失败等问题而发生的订单错误的详细信息。 该描述帮助确定[!DNL Commerce]实例上或[!DNL Walmart Marketplace]上是否出现错误。

>[!NOTE]
>
>如果订单物料以多次装运方式发送，则[!DNL Channel Manager]中的订单状态反映最后一个可用的订单状态。 例如，如果第一个项目出货，并且在将订单更新同步到[!DNL Channel Manager]和[!DNL Walmart Marketplace]时未返回任何错误，则[!DNL Channel Manager]订单状态为&#x200B;_[!UICONTROL Partially Shipped]_。 如果第二个项目已发运且[!DNL Channel Manager]返回错误，则订单状态将更新为_[!UICONTROL Error]_。

## 查看订单

1. 从管理员中，选择&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**&#x200B;以打开[!UICONTROL Channel Manager Marketplace Stores]页面。

1. 通过选择商店条目行中的眼睛图标来打开商店视图。

1. 要查看订单信息，请选择*[!UICONTROL *Orders]**。

1. 通过检查&#x200B;**[状态](#order-status)**&#x200B;列获取有关顺序的信息并确定后续步骤。

## 复查订单详细信息

从市场收到订单并将其导入到您的Sales Channel Store后，请使用[!DNL Commerce]订单ID在Adobe Commerce中查看订单详细信息。

从&#x200B;**[!UICONTROL Orders]**&#x200B;中，选择&#x200B;**[!UICONTROL Commerce Order Number]**&#x200B;以打开[!DNL Commerce]订单详细信息。

[!DNL Walmart Marketplace]订单的![Commerce订单详细信息视图](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

在Commerce店面中，从[!DNL Walmart Marketplace]导入的订单在订单数据中包含以下附加信息：

- **付款信息和送货方式** — 从沃尔玛导入的订单包括以下付款和送货字段值：

   - **[!UICONTROL Offline Channel Payment]** — 指示[!DNL Walmart Marketplace]脱机处理订单付款。

   - **[!UICONTROL External Order Number]** — 显示[!DNL Walmart Marketplace]订单编号。

   - **[!UICONTROL Channel Shipping - Value]** — 指示通过[!DNL Walmart Marketplace]处理运费。

   - **[!UICONTROL Cancellation Reason]** — 仅当从[!DNL Walmart Marketplace]导入的订单被取消时，此字段才显示。 取消原因包括：

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **订购的项目** — 此部分列出了所有Commerce订单上的订购项目。 [!UICONTROL Qty]列提供订单项目的状态历史记录。 例如，如果订单已开票、发运和退款，则您可以查看状态转换。

  ![订单详细信息订购项状态历史记录[!DNL Walmart Marketplace]个订单](assets/order-detail-status-history.png){width="600" zoomable="yes"}

从导航菜单中选择[!UICONTROL Invoice]和[!UICONTROL Credit Memo]选项，以查看项目发票和退款详细信息。 您还可以直接从Sales Channel Store的[[!UICONTROL Returns]](return-refund-orders.md)仪表板访问贷项通知单。
