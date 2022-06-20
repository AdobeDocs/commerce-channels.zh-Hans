---
title: '"管理 [!DNL Walmart Marketplace] 订单数”'
description: “查看和管理 [!DNL Walmart Marketplace] 订购 [!DNL Channel Manager] 为Adobe Commerce和Magento Open Source。”
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: eb57189ed866fffa064867d1de5ae9db5b32e283
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# 管理 [!DNL Walmart Marketplace] 订购

[!DNL Walmart Marketplace] 订单数据 [!DNL Commerce] 产品自动同步到 [!DNL Channel Manager] after [!DNL Walmart] 处理顺序。

在商务端，成功的同步会触发以下操作：

- [!DNL Channel Manager] 向沃尔玛发出订单确认。

- 根据沃尔玛订单创建相应的商务订单。

- 更新的订单信息显示在 [!DNL Channel Manager] 订单仪表板。

在店面管理员中，您可以查看 [!DNL Channel Manager] 打开销售渠道商店并选择 **[!UICONTROL Orders]**.

![要管理的渠道管理器订单视图 [!DNL Walmart Marketplace] 订购](assets/orders-dashboard-view.png)

>[!NOTE]
>
>最长可能需要35分钟 [!DNL Walmart Marketplace] 显示顺序 [!DNL Channel Manager] 订单列表。 [!DNL Walmart] 需要大约30分钟才能处理传入的订单并将它们发送到 [!DNL Channel Manager]. 在渠道管理器收到订单后，大约需要再多五分钟来创建并显示订单，在Adobe Commerce或Magento Open Source中。

## 订单控件和列描述

下表介绍了可用于“订单”的控件和列。

**控件[!UICONTROL Orders]**
| **控制**                    | **描述**                                                                                                                                                                                                                                                                  | |—|—| | [!UICONTROL Filter orders]     |通过选择 [!UICONTROL Order Status] 卡片。                                                                                                                                                                                                           | |错误描述 |提供有关具有错误状态的订单的更多详细信息。                                                                                                                                                                                                            | | [!UICONTROL View order detail] |要查看订单详细信息，请选择 [!DNL Commerce] 订单编号 [!UICONTROL Order] 表。 然后，使用 [!DNL Commerce] 订单选项来处理订单。                                                                                                                    | | [!UICONTROL Channel Settings]  |要修改渠道配置，请选择渠道Walmart连接凭据、映射的属性或发运标识符，然后设置选择 [!DNL Commerce] 订单编号 [!UICONTROL Order] 表。 然后，使用 [!DNL Commerce] 订单选项来处理订单。 |


**列描述**

| 字段 | 描述 |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Walmart Order Number] | 在 [!DNL Walmart Marketplace]. 首次将订单导入时 [!DNL Channel Manager]，仅 [!DNL Walmart] 此时会显示订单编号。 当 [!DNL Commerce] 订单，则 [!DNL Walmart] 订单号存储在 [!UICONTROL External ID] 产品属性。 |
| [!DNL Commerce] 订单编号 | 分配给 [!DNL Commerce] 从创建的订单 [!DNL Walmart Marketplace] 订单。 |
| 项目 | 订购的项目数 [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | 订购物料的总成本。 |
| [!UICONTROL Date Ordered] | 在 [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | 订单必须发运的日期才能满足 [!DNL Walmart Marketplace] 要求。 |
| [!UICONTROL Deliver By Date] | 必须将订单交付给客户以满足要求的日期 [!DNL Walmart Marketplace] UTC格式的要求。 |
| [!UICONTROL Ship Method] | 的 [[!DNL Walmart Marketplace] 装运方法](https://sellerhelp.walmart.com/s/guide?article=000007893) 已选择。 |
| [!UICONTROL Last Update At] | 指示上次更新订单数据的时间戳(在 [!DNL Channel Manager] UTC格式。 |
| [!UICONTROL Status] | 指示 [!DNL Commerce] 订单工作流。 从导入的订单的初始状态 [!DNL Walmart Marketplace] is _打开_. 在处理商务订单并 [!DNL Channel Manager] 成功将装运、部分装运和取消更新同步到 [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description] | 通过 _[!UICONTROL Error]_状态。 |

## 订单状态


[!UICONTROL Order Status] 提供有关 [!DNL Walmart Marketplace] 从Adobe Commerce或Magento Open Source管理的订单。 订单状态更新发生在 [!DNL Channel Manager] 从以下任一位置接收更新的订单信息 [!DNL Walmart Marketplace] 或 [!DNL Commerce] 订单系统。 订单可以具有以下状态：

- **[!UICONTROL Shipped]** — 从 [!DNL Commerce] 存储。 当命令发出时， [!DNL Channel Manager] 向发送更新 [!DNL Walmart Marketplace] 要更新Walmart上的发运状态，并提供装运的订单跟踪编号。

- **[!UICONTROL Partially Shipped]** — 某些物料标记为已发运，而其他物料等待发运的订单。 当订单中的物料发运时， [!DNL Channel Manager] 向发送更新 [!DNL Walmart Marketplace] 要将发运状态更新为在沃尔玛上单独发运，并提供发运的订单跟踪编号。

- **[!UICONTROL Canceled]** — 已从 [!DNL Commerce] 存储。

   订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的项目。 然后， [!DNL Channel Manager] 同步更新到 [!DNL Walmart Marketplace].

- **[!UICONTROL Error]** — 有错误的订单。 订单更新操作失败时，可能会发生错误。 例如，如果 [!DNL Channel Manager] 无法从沃尔玛收到新订单。 如果 [!DNL Channel Manager] 无法将订单发运或取消更新发送至 [!DNL Walmart Marketplace]. 如果操作失败，“订单”页将显示 _错误_ 订单的状态。 有关详细信息，请参阅 [修复订单错误](process-orders.md#fix-shipping-and-cancellation- errors)。

- **[!UICONTROL Error description]** — 提供有关因缺少信息或值无效、发运详细信息不正确或订单取消失败等问题而发生订单错误的详细信息。 描述可帮助确定 [!DNL Commerce] 实例或 [!DNL Walmart Marketplace].

>[!NOTE]
>
>如果订单物料以多批发运发送，则 [!DNL Channel Manager] 反映最后一个可用订单状态。 例如，如果第一个项目发运，并且在将订单更新同步到时未返回任何错误 [!DNL Channel Manager] 和 [!DNL Walmart Marketplace], [!DNL Channel Manager] 订单状态为 _[!UICONTROL Partially Shipped]_.  如果第二件物料已发运并 [!C渠道管理器] 返回错误，顺序状态将更新为_[!UICONTROL Error]_.

## 审核订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 打开 [!UICONTROL Channel Manager Marketplace Stores] 页面。

1. 在商店登入行中选择眼睛图标以打开商店视图。

1. 要查看订单信息，请选择*[!UICONTROL *Orders]**。

1. 通过检查 **[状态](#about-order-status)** 列以获取有关订单的信息。

## 查看订单详细信息

从市场收到订单并将其导入Adobe Commerce或Magento Open Source后，请使用 [!DNL Commerce] 订单ID，用于在Adobe Commerce中查看订单。

从 **[!UICONTROL Orders]**，选择 **[!UICONTROL Commerce Order Number]** 打开 [!DNL Commerce] 订单详细信息。

![商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/order-detail-with-external-order-id.png)

在商务店面中，从 [!DNL Walmart Marketplace] 在订单数据中包含以下其他信息：

- **支付信息与发货方法** — 从Walmart导入的订单包括以下付款和发运字段值：

   - **[!UICONTROL Offline Channel Payment]** — 指示订单付款的脱机处理方式 [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** — 显示 [!DNL Walmart Marketplace] 订单编号。

   - **[!UICONTROL Channel Shipping - Value]** — 表示运费通过 [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** — 仅当从导入的订单 [!DNL Walmart Marketplace] 取消。 取消原因包括：

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

