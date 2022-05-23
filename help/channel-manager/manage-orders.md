---
title: 管理沃尔玛市场订单
description: 查看和管理 [!DNL Walmart Marketplace] 订购 [!DNL Channel Manager] Adobe Commerce和Magento Open Source。
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: ec85dc2496c22cd8173c550ca35f2bd207501c19
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 管理沃尔玛市场订单

[!DNL Walmart Marketplace] 订单数 [!DNL Commerce] 产品清单自动同步到 [!DNL Channel Manager] 在沃尔玛处理订单后。 同步完成后，您可以通过选择 **[!UICONTROL Orders]** 从连接的渠道存储视图(位于 [!DNL Channel Manager].

![渠道经理订单视图管理Walmart Marketplace订单](assets/orders-dashboard-view.png)

>[!NOTE]
>
>最长可能需要35分钟 [!DNL Walmart Marketplace] 显示顺序 [!DNL Channel Manager] 订单列表。 [!DNL Walmart] 需要大约30分钟才能处理传入的订单并将它们发送到 [!DNL Channel Manager]. 在渠道管理器收到订单后，大约需要再多五分钟来创建并显示订单，在Adobe Commerce或Magento Open Source中。

## 审核订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 打开 [!UICONTROL Channel Manager Marketplace Stores] 页面。

1. 在商店登入行中选择铅笔图标以打开商店视图。

1. 要查看订单信息，请选择*[!UICONTROL *Orders]**。

1. 通过检查 **[状态](#about-order-status)** 列以获取有关订单的信息。

## 查看订单详细信息

从市场收到订单并将其导入Adobe Commerce或Magento Open Source后，请使用 [!DNL Commerce] 订单ID，用于在Adobe Commerce中查看订单。

从 **[!UICONTROL Orders]**，选择 **[!UICONTROL Commerce Order Number]** 打开 [!DNL Commerce] 订单详细信息。

![Walmart Marketplace订单的商务订单详细信息视图](assets/order-detail-with-external-order-id.png)

### 订单控件和列描述

下表介绍了可用于“订单”的控件和列。

**控件[!UICONTROL Orders]**
| **控制**                    | **描述**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     |通过选择 [!UICONTROL Order Status] 卡片。                                                                                        | |错误消息详细信息 |将鼠标悬停在 [!UICONTROL Error Status] 以查看详细错误消息。                                                                      | | [!UICONTROL View order detail] |要查看订单详细信息，请选择 [!DNL Commerce] 订单编号 [!UICONTROL Order] 表。 然后，使用 [!DNL Commerce] 订单选项来处理订单。 |

**列描述**

| 字段 | 描述 |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | 在 [!DNL Walmart Marketplace]. 首次将订单导入时 [!DNL Channel Manager]，则仅会显示沃尔玛订单号。 当 [!DNL Commerce] 订单，则 [!DNL Walmart] 订单号存储在 [!UICONTROL External ID] 产品属性。 |
| [!DNL Commerce]  订单编号 | 分配给 [!DNL Commerce]  从创建的订单 [!DNL Walmart Marketplace] 订单。 |
| 项目 | 订购的项目数 [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | 订购物料的总成本。 |
| [!UICONTROL Date Created] | 在 [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | 订单必须发运的日期才能满足 [!DNL Walmart Marketplace] 要求。 |
| [!UICONTROL Order Status] | 指示 [!DNL Commerce] 订单工作流。 成功将产品添加到 [!DNL Channel Manager] 当您在 [!DNL Walmart Marketplace]. 如果操作失败，则列表会显示错误状态。 修正错误后， [!DNL Channel Manager] 重试操作并更新状态。 |

| [!UICONTROL Error description]    |通过 *错误* status.|

### 关于订单状态

[!UICONTROL Order Status] 提供有关 [!DNL Walmart Marketplace] 从Adobe Commerce或Magento Open Source管理的订单。 订单状态更新发生在 [!DNL Channel Manager] 从以下任一位置接收更新的订单信息 [!DNL Walmart Marketplace] 或 [!DNL Commerce] 订单系统。 订单可以具有以下状态：

* **[!UICONTROL Open]** — 从 [!DNL Walmart Marketplace] 准备在Adobe Commerce或Magento Open Source中审核和处理。

   在客户从 [!DNL Walmart Marketplace]，则打开顺序最多可能需要35分钟才能在连接的渠道的顺序工作区中显示。 [!DNL Commerce] 需要大约30分钟才能处理传入的订单并将它们发送到 [!DNL Channel Manager]. 在渠道管理器收到订单后，需要再花5分钟来创建和显示 [!DNL Commerce] 订单。

* **[!UICONTROL Processed]** — 已从 [!DNL Commerce] 存储。

   要显示所有已发运、已取消和已退还的订单，请选择 **已处理** 状态卡。

* **[!UICONTROL Canceled]** — 已从 [!DNL Commerce] 存储。

   订单取消完成后， [!DNL Commerce] 库存数量更新以反映返回的项目。 然后， [!DNL Channel Manager] 同步更新到 [!DNL Walmart Marketplace].

* **[!UICONTROL Refunded]** — 已从 [!DNL Commerce] 存储。

   退款完成后， [!DNL Commerce] 更新库存数量以反映已退回的项目。 然后， [!DNL Channel Manager] 同步更新到 [!DNL Walmart Marketplace].

* **[!UICONTROL Error]** — 有错误的订单。 订单更新操作失败时，可能会发生错误。 例如，如果 [!DNL Channel Manager] 无法从沃尔玛收到新订单。 如果 [!DNL Channel Manager] 无法将订单发运或取消更新发送至 [!DNL Walmart Marketplace].

* **[!UICONTROL Error description]** — 提供有关因缺少信息或值无效、发运详细信息不正确或订单取消失败等问题而发生订单错误的详细信息。 描述可帮助确定 [!DNL Commerce] 实例或 [!DNL Walmart Marketplace].
