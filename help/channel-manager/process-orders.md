---
title: 处理订单
description: '''发货和取消说明 [!DNL Walmart Marketplace] Adobe Commerce和Magento Open Source的订单。”'
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 处理订单

晚于 [!DNL Walmart Marketplace] 订单已确认并成功发送至 [!DNL Channel Manager]，您使用 [商务订单管理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) 以处理订单。

渠道管理器将更新同步到 [!DNL Walmart Marketplace] 确保订单状态和发运信息来自 [!DNL Commerce] 匹配中跟踪的数据 [!DNL Walmart Marketplace].

* **订单装运** — 沃尔玛要求所有发货都要有跟踪号。 如果某些物料缺货，您可以创建部分发运以发送当前可用的物料。 在您提交发运后，订单更新将同步到 [!DNL Walmart Marketplace]. 然后，沃尔玛会通知客户订单状态和发货详情。

* **订单取消** — 当您取消 [!DNL Walmart Marketplace] 订单取消通知中包含了取消订单的原因。 取消原因也显示在 [!DNL Commerce] 订单付款信息。 在您提交取消后，库存更新将同步到 [!DNL Walmart Marketplace]. 然后，沃尔玛会通知客户订单状态和发货详情。

  在店面，您必须取消整个订单。 [!DNL Commerce] 不允许部分取消。

* **退款请求** — 如果要求沃尔玛商场退回已发运的订单，则 [!UICONTROL Status details] 包含指向返回的链接。 退货及退款由本公司的 [返回](return-refund-orders.md) 仪表板。

当处理商务订单并且 [!DNL Channel Manager] 将发运、部分发运和取消更新成功同步到 [!DNL Walmart Marketplace]，订单处理完成。 已发运订单的退货请求和退款由 [返回](return-refund-orders.md) 仪表板。

>[!NOTE]
>
> 同步订单更新最多可能需要五分钟 [!DNL Walmart Marketplace]. 要检查订单状态，请返回 [!DNL Channel Manager] 订单页面。

## 发送订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 通过选择销售渠道商店的眼睛图标来打开商店视图。

1. 查看 [!DNL Walmart Marketplace] 订单，选择 **[!UICONTROL Orders]**.

1. 在“订单”表格中，通过选择 **[!UICONTROL Commerce Order Number]**.

1. 通过选择，为全部或部分订单创建并提交装运 **[!UICONTROL Ship]**.

   ![的商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * 选择装运承运人，并通过选择添加跟踪编号 **[!UICONTROL Add tracking number]**.

     ![的商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * 根据需要完成其余的送货单。 参见 [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) 以获取详细说明。

1. 提交装运后，跟踪 [订单状态](manage-orders.md#about-order-status) 在 [!DNL Channel Manager] 验证更新是否已发送到 [!DNL Walmart Marketplace].

订单发运后，您可以处理全部或部分退款 [!DNL Channel Manager] 根据从收到的退货请求，确定订单中包含的物料 [!DNL Walmart Marketplace]. 参见 [退货单和退款单](return-refund-orders.md).

## 取消订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 通过选择销售渠道商店的眼睛图标来打开商店视图。

1. 查看 [!DNL Walmart Marketplace] 订单，选择*[!UICONTROL Orders]**。

1. 在“订单”表格中，打开 [订单详细信息页面](manage-orders.md#view-order-detail) 通过选择 **[!UICONTROL Commerce Order Number]** ，以取消订单。

   ![的商务订单详细信息视图[!DNL Walmart Marketplace]订购](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. 取消订单。

   * 选择 **取消** 从“订单详细信息”菜单中。

   * 在 [!UICONTROL Cancel Order] 表单中，选择 **[!UICONTROL Cancellation reason]**.

   ![的商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * 选择 **[!UICONTROL Cancel Order]**.

1. 提交取消后，跟踪 [订单状态](manage-orders.md#about-order-status) 在 [!DNL Channel Manager] 验证更新是否已发送到 [!DNL Walmart Marketplace].

## 修复订单错误

在订单同步过程中可能会出错，从 [!DNL Walmart Marketplace]，或者在发运、部分发运和取消的订单更新流程中进行更新。

如果发运、部分发运或取消更新的同步操作失败， [!DNL Channel Manager] “订单”页面显示 _错误_ 订单的状态。 为确保发货信息和订单取消信息准确反映在Walmart Marketplace帐户中，请手动更新以下文件中的订单： [!DNL Walmart Marketplace] 商店。


