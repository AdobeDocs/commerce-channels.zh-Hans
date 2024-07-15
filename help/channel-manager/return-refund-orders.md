---
title: 退货和退款单
description: 针对从 [!DNL Walmart Marketplace] 接收的Adobe Commerce和Magento Open Source的 [!DNL Channel Manager] 的退货请求签发全部或部分退款的说明。
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# 退货和退款单

当采购员请求退回通过[!DNL Walmart Marketplace]购买的订单项目时，沃尔玛会创建退货请求。 [!DNL Channel Manager]监视这些请求的市场渠道，并将返回的请求信息自动同步到渠道管理器。

在Commerce端，返回请求会启动以下工作流：

1. 渠道管理器创建一个具有已接收状态的相应返回请求，并将返回ID号([!UICONTROL RMA #])添加到[!UICONTROL Returns]仪表板。 在[!DNL Orders]仪表板上，与退货更新关联的订单的状态详细信息包含一个[!UICONTROL Return requested]链接，用于查看和处理退货。

1. 商家通过在[Adobe Commerce退款工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html)之后创建贷项通知单来处理与退货关联的退款。 所有退款均使用离线方法进行处理。

1. [!DNL Channel Manager]向Walmart marketplace发送退款更新，以便可以更新退货状态以反映从Adobe Commerce完成的退款。

在storefront Admin中，您可以通过打开Sales Channel Store并选择&#x200B;**[!UICONTROL Returns]**&#x200B;来查看和处理来自Channel Manager的退货。

![渠道经理退货仪表板，用于处理从[!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}收到的退货请求的退款

>[!NOTE]
>
>您只能处理已发运订单的退款。 在[!DNL Channel Manager]中，订单状态必须为[!UICONTROL Shipped]。 在[!DNL Walmart Marketplace]卖方帐户中，订单必须为[!UICONTROL Delivered]。

## 返回控件和列说明

下表描述了可用于[!DNL Channel Manager]返回的控件和列。

[!UICONTROL Returns]**的**&#x200B;控件

<table>
<tr>
<td><strong>控件</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>通过选择[!UICONTROL Return Status]卡片之一来筛选视图。</td>
</tr>
<tr>
<td>状态详细信息</td>
<td>对于状态为[!UICONTROL Received]或[!UICONTROL Refunded]的退货条目，您可以通过在“状态详细信息”列中选择链接文本来创建或查看退款的贷项通知单。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>要查看订单详细信息，请选择[!UICONTROL Order]表中的[!DNL Commerce]订单号以打开Commerce订单。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>要修改通道配置，请选择通道Walmart连接凭据、映射的属性或装运标识符，设置则选择[!UICONTROL Order]表中的[!DNL Commerce]订单号。 然后，使用[!DNL Commerce]订单选项处理该订单。</td>
</tr>
</table>

**列描述**

<table>
<tr>
<td><strong>字段</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>与从[!DNL Walmart Marketplace]收到的退货请求关联的退货授权号。 此号码由Walmart Marketplace [!UICONTROL Returns]在启动退货流程时生成。</td>
</tr>
<tr>
<td>[!DNL Commerce] 订单编号</td>
<td>与沃尔玛商城的退货请求中包含的项目关联的[!DNL Commerce]订单号。 通过选择订单编号查看订单详细信息。</td>
</tr>
<tr>
<td>已请求</td>
<td>请求返回的日期为[!DNL Walmart Marketplace]
转换为本地时间。</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>返回必须退款以符合[!DNL Walmart Marketplace] [要求](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f)的日期已转换为本地时间。</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>列出退货中列出的每个物料的SKU和数量。</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>要退款的退货物料的总值。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>指示[!DNL Commerce]退货工作流中的当前退货状态 — <i>已接收</i>、<i>已退款</i>或<i>错误</i>。</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>对于已接收和已退款的退货分录，状态详细信息会提供一个链接，用于访问退款处理的贷项通知单。 如果在Adobe Commerce与[!DNL Walmart marketplace]之间的[!DNL Channel Manager]同步过程中出现错误，则此字段提供错误描述。</td>
</tr>
</table>

## 返回状态

[!UICONTROL Return Status]提供了有关从Adobe Commerce或Magento Open Source管理的[!DNL Walmart Marketplace]返回请求的当前状态的信息。

当[!DNL Channel Manager]收到来自[!DNL Walmart Marketplace]的退货请求或创建[!DNL Commerce]贷项通知单以处理退货的退款时，将出现退货状态更新。

返回可具有以下状态：

* **[!UICONTROL Received]** — 这是从[!DNL Walmart Marketplace]存储区接收的返回请求的初始状态。 商家可以通过在[!UICONTROL Status details]中选择&#x200B;**[!UICONTROL Create credit memo]**&#x200B;来处理退货退款。

* **[!UICONTROL Refunded]** — 表示已创建贷项通知单以发放退回项目的退款。 商家可以通过在[!UICONTROL Status details]中选择&#x200B;**[!UICONTROL View credit memo]**&#x200B;来查看退款信息。

* **[!UICONTROL Error]** — 返回有错误的请求。 当来自沃尔玛的返回请求缺少数据或数据不正确时，可能会发生错误。 或者，如果[!DNL Channel Manager]无法向沃尔玛发送退款更新通知。

## 返回方案

以下方案描述了如何从[!DNL Channel Manager]为不同类型的退货请求发放退款。

* **全部退货** — 如果沃尔玛商城退货请求针对订单中的所有项目，请更新贷项通知单数量以退款所有项目。

* **部分退货** — 如果沃尔玛商城退货请求仅针对某些订单项目，请仅更新要退款的项目的贷项通知单数量。

* **退货已经通过沃尔玛商城退款** — 在某些情况下，退款会在[!DNL Walmart Marketplace]处理，然后再在渠道管理器中处理退款。 例如，如果Commerce订单在沃尔玛要求的48小时退款处理窗口内未退款，则沃尔玛会自动退款。 发生这种情况时，渠道管理器仍会将退货请求同步到Adobe Commerce，这样您就可以处理退货并签发贷项通知单。 此工作流可确保[!DNL Commerce]中的订单详细信息与Walmart Marketplace中的订单信息相匹配。

>[!NOTE]
>
> 退款更新最多可能需要五分钟才能同步到[!DNL Walmart Marketplace]。 您可以从[!DNL Channel Manager] [!UICONTROL Returns]仪表板检查当前返回状态。

## 处理退款请求

1. 为您的Sales Channel商店打开[!UICONTROL Returns]仪表板。

   * 从管理员中，选择&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**。

   * 通过选择销售渠道商店的眼睛图标来打开商店视图。

   * 您可以通过选择&#x200B;**[!UICONTROL Returns]**&#x200B;选项卡来查看退货。

     您还可以从[!UICONTROL Orders]页面访问返回信息。 查找具有退货请求的[!UICONTROL Shipped]订单。 然后，选择[!UICONTROL Status Details]列中的`Return requested`链接以查看和处理请求。

1. 从Returns表中，查找状态为&#x200B;*[!UICONTROL Received]*&#x200B;的返回。

1. 在项目列中，复查订单项目和要退款的数量的列表。

1. 通过签发贷项通知单来处理退款。

   * 从[!UICONTROL Status Details]列中，选择&#x200B;**[!UICONTROL Create credit memo]**&#x200B;以在[!DNL Commerce]中打开订单详细信息页面。

     如果订单尚未开票，则“订单详细信息”页将显示一则错误消息，提示您创建订单。 选择&#x200B;**[!UICONTROL Create invoice]**。 然后，[创建并保存发票](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html)。

   * 在订单详细信息页面上，选择&#x200B;**[!UICONTROL Credit Memo]**。

   * 在[!UICONTROL Credit Memo]的[!UICONTROL Items to Refund]部分中，更新返回请求中包含的项目的&#x200B;**[!UICONTROL Qty to refund]**&#x200B;和&#x200B;**[!UICONTROL Return to Stock]**&#x200B;信息。

     确保仅返回返回请求中列出的项目。

   * 要添加评论，请在&#x200B;**[!UICONTROL Credit Memo Comments]**&#x200B;中输入文本

   * 选择&#x200B;**[!UICONTROL Refund Offline]**。

完成退款后，[!DNL Channel Manager]将在[!UICONTROL Returns]仪表板中的退货状态更新为[!UICONTROL Refunded]，并将更新同步到Walmart以更新市场中的退货状态。


## 查看退货的退款信息

您可以从[!UICONTROL Returns]仪表板查看有关退货请求和退款处理的信息。

1. 打开销售渠道商店的“退货”功能板。

   * 从管理员中，选择&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**。

   * 通过选择销售渠道商店的眼睛图标来打开商店视图。

   * 选择&#x200B;**[!UICONTROL Returns]**。

1. 通过选择&#x200B;**[!UICONTROL Refunded]**&#x200B;状态卡查看退款订单。

1. 通过选择&#x200B;**[!UICONTROL View credit memo]**&#x200B;查看退货的退款详细信息。

   ![用于退款[!DNL Walmart Marketplace]订单的退货的贷项通知单](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>订单退款后，[!UICONTROL Orders]仪表板不显示退货信息。 要查看退货信息，请使用[!DNL Channel Manager]退货仪表板。 订单详情页面还提供了更详细的退货和退款信息。

## 修复返回错误

从[!DNL Walmart Marketplace]接收返回信息时，或当[!DNL Channel Manager]将状态更新从[!DNL Commerce]同步到[!DNL Walmart Marketplace]时，可能会发生错误。

如果返回更新的同步操作失败，[!DNL Channel Manager]返回仪表板将显示返回条目的&#x200B;*[!UICONTROL Error]*&#x200B;状态。 为确保退货和退款信息准确反映在沃尔玛商店帐户中，请手动更新[!DNL Walmart Marketplace]商店中的订单。
