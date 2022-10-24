---
title: 退货和退款订单
description: '"关于对收到的回访请求发出全额或部分退款的说明 [!DNL Walmart Marketplace] 从 [!DNL Channel Manager] 为Adobe Commerce和Magento Open Source。”'
source-git-commit: e9d2f53a955956a2b5086649d9ac18cc982ef4e3
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# 退货和退款订单

当采购员请求退回通过 [!DNL Walmart Marketplace]，沃尔玛会创建一个退货请求。 [!DNL Channel Manager] 监控这些请求的市场渠道，并自动将回访请求信息同步到渠道管理器。

在商务端，返回请求会启动以下工作流：

1. 渠道管理器创建具有接收状态的相应返回请求，并添加返回ID号([!UICONTROL RMA #]) [!UICONTROL Returns] 功能板。 在 [!DNL Orders] 功能板，与退货更新关联的订单的状态详细信息以包含 [!UICONTROL Return requested] 链接以查看和处理返回。

1. 商户通过在 [Adobe Commerce退款工作流](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). 所有退款均使用离线方法进行处理。

1. [!DNL Channel Manager] 向Walmart marketplace发送退款更新，以便更新退货状态，以反映从Adobe Commerce完成的退款。

在店面管理员中，您可以通过打开销售渠道商店并选择 **[!UICONTROL Returns]**.

![Channel Manager返回功能板以处理从 [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>您只能处理已发运订单的退款。 在 [!DNL Channel Manager]，则订单状态必须为 [!UICONTROL Shipped]. 在 [!DNL Walmart Marketplace] 卖家账户，订单必须 [!UICONTROL Delivered].

## 返回控件和列描述

下表介绍了可用的控件和列 [!DNL Channel Manager] 返回。

**控件[!UICONTROL Returns]**

<table>
<tr>
<td><strong>控制</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>通过选择 [!UICONTROL Return Status] 卡片。</td>
</tr>
<tr>
<td>状态详细信息</td>
<td>对于包含的返回条目 [!UICONTROL Received] 或 [!UICONTROL Refunded] 状态时，您可以通过选择“状态详细信息”列中的链接文本来创建或查看退款的贷项通知单。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>要查看订单详细信息，请选择 [!DNL Commerce] 订单编号 [!UICONTROL Order] 表格打开商务订单。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>要修改渠道配置，请选择渠道Walmart连接凭据、映射的属性或发运标识符，设置选择 [!DNL Commerce] 订单编号 [!UICONTROL Order] 表。 然后，使用 [!DNL Commerce] 订单选项来处理订单。</td>
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
<td>与从接收的退货请求关联的退货授权号 [!DNL Walmart Marketplace]. 此数字由Walmart Marketplace生成 [!UICONTROL Returns] 启动返回进程时。</td>
</tr>
<tr>
<td>[!DNL Commerce] 订单编号</td>
<td>的 [!DNL Commerce] 与来自Walmart Marketplace的退货请求中包含的项目关联的订单号。 通过选择订单编号来查看订单详细信息。</td>
</tr>
<tr>
<td>请求</td>
<td>在 [!DNL Walmart Marketplace]
转换为本地时间。</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>必须退回才能满足的日期 [!DNL Walmart Marketplace] [要求](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f)已转换为本地时间。</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>列出退货中列出的每个项目的SKU和数量。</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>退回的物项要退还的总值。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>指示 [!DNL Commerce] 返回工作流 — <i>已接收</i>, <i>已退回</i>或 <i>错误</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>对于已接收和已退回的退货条目，状态详细信息提供一个链接，用于访问贷项通知单以进行退款处理。 如果在 [!DNL Channel Manager] Adobe Commerce与 [!DNL Walmart marketplace]，此字段提供错误描述。</td>
</tr>
</table>

## 返回状态

[!UICONTROL Return Status] 提供有关 [!DNL Walmart Marketplace] 返回从Adobe Commerce或Magento Open Source管理的请求。

在 [!DNL Channel Manager] 接收来自的返回请求 [!DNL Walmart Marketplace] 或 [!DNL Commerce] 创建贷项通知单以处理返回项目的退款。

返回可以具有以下状态：

* **[!UICONTROL Received]** — 这是从 [!DNL Walmart Marketplace] 存储。 商户可通过选择 **[!UICONTROL Create credit memo]** 在 [!UICONTROL Status details].

* **[!UICONTROL Refunded]** — 指示已创建贷项通知单以为返回的项目发出退款。 商户可以通过选择 **[!UICONTROL View credit memo]** 在 [!UICONTROL Status details].

* **[!UICONTROL Error]** — 返回有错误的请求。 当来自Walmart的返回请求缺少数据或数据不正确时，可能会发生错误。 或者，如果 [!DNL Channel Manager] 无法向沃尔玛发送退款更新通知。

## 返回方案

以下方案介绍如何为来自的不同类型返回请求发出退款 [!DNL Channel Manager].

* **完全返回** — 如果Walmart Marketplace返回请求适用于订单中的所有项目，请更新贷项通知单数量以退回所有项目。

* **部分返回** — 如果Walmart Marketplace返回请求仅针对某些订单项目，则仅针对要退还的项目更新贷项通知单数量。

* **已通过Walmart Marketplace退还退货** — 在某些情况下，会在 [!DNL Walmart Marketplace] 在渠道管理器中处理返回之前。 例如，如果在沃尔玛要求的48小时退款处理窗口内未退回商务订单，则沃尔玛会自动退款订单。 发生此情况时，渠道管理器仍会将回访请求同步到Adobe Commerce，以便您可以处理回访并发出贷项通知单。 此工作流可确保 [!DNL Commerce] 与Walmart Marketplace中的订单信息匹配。

>[!NOTE]
>
> 退款更新最多可能需要五分钟才能同步到 [!DNL Walmart Marketplace]. 您可以从 [!DNL Channel Manager] [!UICONTROL Returns] 功能板。

## 处理退款请求

1. 打开 [!UICONTROL Returns] 销售渠道商店的仪表板。

   * 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 通过选择销售渠道商店的眼睛图标打开商店视图。

   * 您可以通过选择 **[!UICONTROL Returns]** 选项卡。

      您还可以从 [!UICONTROL Orders] 页面。 查找 [!UICONTROL Shipped] 具有退货请求的订单。 然后，选择 `Return requested` 链接 [!UICONTROL Status Details] 列来查看和处理请求。

1. 在“返回”(Returns)表格中，查找包含 *[!UICONTROL Received]* 状态。

1. 在“项目”列中，复查订单项目列表和要退款的数量。

1. 通过发出贷项通知单处理退款。

   * 从 [!UICONTROL Status Details] 列，选择 **[!UICONTROL Create credit memo]** 要在 [!DNL Commerce].

      如果订单尚未开票，则“订单详细信息”页会显示一条错误消息，提示您创建一个订单。 选择 **[!UICONTROL Create invoice]**. 然后， [创建并保存发票](https://docs.magento.com/user-guide/sales/invoices.html).

   * 在“订单详细信息”页面上，选择 **[!UICONTROL Credit Memo]**.

   * 在 [!UICONTROL Items to Refund] 部分 [!UICONTROL Credit Memo]，更新 **[!UICONTROL Qty to refund]** 和 **[!UICONTROL Return to Stock]** 返回请求中包含的项目的信息。

      确保仅返回返回请求中列出的项目。

   * 要添加评论，请在 **[!UICONTROL Credit Memo Comments]**

   * 选择 **[!UICONTROL Refund Offline]**.

退款完成后， [!DNL Channel Manager] 更新 [!UICONTROL Returns] 功能板至 [!UICONTROL Refunded] 并将更新同步到沃尔玛，以更新市场中的退货状态。


## 查看退货的退款信息

您可以从 [!UICONTROL Returns] 功能板。

1. 打开销售渠道商店的退货功能板。

   * 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 通过选择销售渠道商店的眼睛图标打开商店视图。

   * 选择 **[!UICONTROL Returns]**.

1. 通过选择 **[!UICONTROL Refunded]** 状态卡。

1. 通过选择 **[!UICONTROL View credit memo]**.

   ![退还退货的贷项通知单 [!DNL Walmart Marketplace] 订购](assets/refund-credit-memo-for-marketplace-order.png)

>[!NOTE]
>
>在订单被退还后， [!UICONTROL Orders] 功能板不显示返回信息。 要查看返回信息，请使用 [!DNL Channel Manager] 返回功能板。 有关退货和退款的详细信息，请参阅订单详细信息页面。

## 修复返回错误

从收到返回信息时，可能会出错 [!DNL Walmart Marketplace]，或 [!DNL Channel Manager] 从同步状态更新 [!DNL Commerce] to [!DNL Walmart Marketplace].

如果返回更新的同步操作失败，则 [!DNL Channel Manager] 返回功能板显示 *[!UICONTROL Error]* 返回条目的状态。 为确保退货和退款信息准确反映在Walmart Marketplace帐户中，请在 [!DNL Walmart Marketplace] 存储。


