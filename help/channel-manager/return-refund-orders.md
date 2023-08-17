---
title: 退货和退款单
description: 为收到的退货请求签发全部或部分退款的说明 [!DNL Walmart Marketplace] 从 [!DNL Channel Manager] 用于Adobe Commerce和Magento Open Source。
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# 退货和退款单

当采购员请求退货通过采购的订单项目时 [!DNL Walmart Marketplace]，沃尔玛会创建一个退货请求。 [!DNL Channel Manager] 监视这些请求的市场渠道，并将返回的请求信息自动同步到渠道管理器。

在商业方面，返回请求会启动以下工作流：

1. 渠道管理器使用接收状态创建相应的返回请求，并添加返回ID号([!UICONTROL RMA #])到 [!UICONTROL Returns] 仪表板。 在 [!DNL Orders] 仪表板，与退货更新关联的订单的状态详细信息，以包括 [!UICONTROL Return requested] 查看和处理退货的链接。

1. 商家通过以下方式创建贷项通知单，来处理与退货关联的退款 [Adobe Commerce退款工作流](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). 所有退款均使用离线方法进行处理。

1. [!DNL Channel Manager] 向沃尔玛商城发送退款更新消息，以便更新退货状态，从而反映Adobe Commerce已完成的退款。

在店面管理员中，您可以通过打开销售渠道商店并选择 **[!UICONTROL Returns]**.

![渠道经理退货控制面板用于处理从收到的退货请求的退款 [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>您只能处理已发运订单的退款。 在 [!DNL Channel Manager]，订单状态必须为 [!UICONTROL Shipped]. 在 [!DNL Walmart Marketplace] 卖方帐户，订单必须 [!UICONTROL Delivered].

## 返回控件和列说明

下表介绍了可用于的控件和列 [!DNL Channel Manager] 返回。

**控件[!UICONTROL Returns]**

<table>
<tr>
<td><strong>控件</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>通过选择 [!UICONTROL Return Status] 卡片。</td>
</tr>
<tr>
<td>状态详细信息</td>
<td>对于返回条目，使用 [!UICONTROL Received] 或 [!UICONTROL Refunded] 状态，您可以通过在“状态详细信息”列中选择链接文本来创建或查看退款的贷项通知单。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>要查看订单详细信息，请选择 [!DNL Commerce] 中的订单编号 [!UICONTROL Order] 用于打开Commerce订单的表。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>要修改通道配置，请选择通道Walmart连接凭据、映射的属性或发运标识符，设置选择 [!DNL Commerce] 中的订单编号 [!UICONTROL Order] 表格。 然后，使用 [!DNL Commerce] 订单选项以处理订单。</td>
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
<td>与从接收的退货请求关联的退货授权号 [!DNL Walmart Marketplace]. 此数字由沃尔玛商城生成 [!UICONTROL Returns] 何时启动退货流程。</td>
</tr>
<tr>
<td>[!DNL Commerce] 订单编号</td>
<td>此 [!DNL Commerce] 与沃尔玛商城的退货请求中包含的物品关联的订单号。 通过选择订单编号查看订单详细信息。</td>
</tr>
<tr>
<td>已请求</td>
<td>请求返回的日期 [!DNL Walmart Marketplace]
转换为本地时间。</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>必须退款才能达到的日期 [!DNL Walmart Marketplace] [要求](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f)转换为当地时间。</td>
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
<td>指示中的当前返回状态 [!DNL Commerce] 返回工作流 — <i>已接收</i>， <i>已退款</i>，或 <i>错误</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>对于已接收和已退款的退货分录，状态详细信息会提供一个链接，用于访问退款处理的贷项通知单。 如果在以下期间发生错误： [!DNL Channel Manager] Adobe Commerce与之间的同步过程 [!DNL Walmart marketplace]，此字段提供错误描述。</td>
</tr>
</table>

## 返回状态

[!UICONTROL Return Status] 提供有关当前状态的信息， [!DNL Walmart Marketplace] 从Adobe Commerce或Magento Open Source管理的返回请求。

在以下情况下会发生返回状态更新 [!DNL Channel Manager] 接收来自的返回请求 [!DNL Walmart Marketplace] 或当 [!DNL Commerce] 创建贷项通知单以处理退回项目的退款。

返回可具有以下状态：

* **[!UICONTROL Received]** — 这是从收到的返回请求的初始状态 [!DNL Walmart Marketplace] 商店。 商家可以通过选择 **[!UICONTROL Create credit memo]** 在 [!UICONTROL Status details].

* **[!UICONTROL Refunded]** — 表示已创建贷项通知单以发放退回项目的退款。 商家可以通过选择查看退款信息 **[!UICONTROL View credit memo]** 在 [!UICONTROL Status details].

* **[!UICONTROL Error]** — 返回有错误的请求。 当来自沃尔玛的返回请求缺少数据或数据不正确时，可能会发生错误。 或者，如果 [!DNL Channel Manager] 无法将退款更新通知发送给沃尔玛。

## 返回方案

以下情形描述了如何从为不同类型的退货请求签发退款 [!DNL Channel Manager].

* **完全返回** — 如果Walmart Marketplace退货请求适用于订单中的所有项目，请更新贷项通知单数量以退回所有项目。

* **部分返回** — 如果Walmart Marketplace退货请求只针对某些订单项目，请只更新要退款的项目的贷项通知单数量。

* **退货已通过沃尔玛市场退款** — 在某些情况下，退款的处理日期为 [!DNL Walmart Marketplace] ，然后再在渠道管理器中处理返回。 例如，如果Commerce订单未在Walmart要求的48小时退款处理窗口内退款，则Walmart会自动退款。 发生这种情况时，渠道管理器仍会将退货请求同步到Adobe Commerce，这样您就可以处理退货并签发贷项通知单。 此工作流可确保中的订单详细信息 [!DNL Commerce] 与沃尔玛商城的订单信息相匹配。

>[!NOTE]
>
> 退款更新最多可能需要五分钟才能同步到 [!DNL Walmart Marketplace]. 您可以从以下位置检查当前返回状态： [!DNL Channel Manager] [!UICONTROL Returns] 仪表板。

## 处理退款请求

1. 打开 [!UICONTROL Returns] 您的sales channel store的功能板。

   * 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 通过选择销售渠道商店的眼睛图标来打开商店视图。

   * 您可以通过选择 **[!UICONTROL Returns]** 选项卡。

     您还可以从以下位置访问返回信息： [!UICONTROL Orders] 页面。 查找 [!UICONTROL Shipped] 具有退货请求的订单。 然后，选择 `Return requested` 中的链接 [!UICONTROL Status Details] 列以查看和处理请求。

1. 在Returns表中，查找包含 *[!UICONTROL Received]* 状态。

1. 在项目列中，复查订单项目和要退款的数量的列表。

1. 通过签发贷项通知单来处理退款。

   * 从 [!UICONTROL Status Details] 列，选择 **[!UICONTROL Create credit memo]** 在中打开订单详细信息页面 [!DNL Commerce].

     如果订单尚未开票，则“订单详细信息”页将显示一则错误消息，提示您创建订单。 选择 **[!UICONTROL Create invoice]**. 然后， [创建并保存发票](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * 在订单详细信息页面上，选择 **[!UICONTROL Credit Memo]**.

   * 在 [!UICONTROL Items to Refund] 的部分 [!UICONTROL Credit Memo]，更新 **[!UICONTROL Qty to refund]** 和 **[!UICONTROL Return to Stock]** 退货请求中包含的物料信息。

     确保仅返回返回请求中列出的项目。

   * 要添加注释，请在 **[!UICONTROL Credit Memo Comments]**

   * 选择 **[!UICONTROL Refund Offline]**.

完成退款后， [!DNL Channel Manager] 更新中的返回状态 [!UICONTROL Returns] 报告面板目标 [!UICONTROL Refunded] 并将更新同步到沃尔玛，以更新市场中的退货状态。


## 查看退货的退款信息

您可以从以下网站查看有关退货请求和退款处理的信息 [!UICONTROL Returns] 仪表板。

1. 打开销售渠道商店的“退货”功能板。

   * 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 通过选择销售渠道商店的眼睛图标来打开商店视图。

   * 选择 **[!UICONTROL Returns]**.

1. 通过选择 **[!UICONTROL Refunded]** 状态卡。

1. 通过选择查看退货的退款详细信息 **[!UICONTROL View credit memo]**.

   ![用于退款的贷项通知单 [!DNL Walmart Marketplace] 订购](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>订单退款后， [!UICONTROL Orders] 仪表板不显示返回信息。 要查看退货信息，请使用 [!DNL Channel Manager] 返回仪表板。 订单详情页面还提供了更详细的退货和退款信息。

## 修复返回错误

从接收返回信息时，可能会出错 [!DNL Walmart Marketplace]，或 [!DNL Channel Manager] 从同步状态更新 [!DNL Commerce] 到 [!DNL Walmart Marketplace].

如果返回更新的同步操作失败， [!DNL Channel Manager] 退货仪表板显示 *[!UICONTROL Error]* 退货条目的状态。 为确保退货和退款信息准确反映在沃尔玛商店帐户中，请手动更新您网站上的 [!DNL Walmart Marketplace] 商店。
