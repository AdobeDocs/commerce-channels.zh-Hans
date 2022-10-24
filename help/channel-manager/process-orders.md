---
title: 处理订单
description: “发运和取消说明” [!DNL Walmart Marketplace] Adobe Commerce和Magento Open Source的订单。
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 958f91f0303b823f164e60e56d8dbe4e8c2380f6
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# 处理订单

之后 [!DNL Walmart Marketplace] 已确认订单，并已成功将订单发送到 [!DNL Channel Manager]，您使用 [商务订单管理](https://docs.magento.com/user-guide/sales/orders-workspace.html) 来处理订单。

Channel Manager将更新同步到 [!DNL Walmart Marketplace] 以确保订单状态和发运信息 [!DNL Commerce] 与 [!DNL Walmart Marketplace].

* **订单发运**- Walmart要求所有发货的跟踪编号。 如果某些物料无现货，您可以创建部分发运以发送当前可用的物料。 在您提交发运后，订单更新将同步到 [!DNL Walmart Marketplace]. 然后，沃尔玛会通知客户订单状态和送货详细信息。

* **订单取消** — 当您取消 [!DNL Walmart Marketplace] 沃尔玛要求在发送给客户的订单取消通知中包含取消原因。 取消原因也显示在 [!DNL Commerce] 订单付款信息。 提交取消后，库存更新将同步到 [!DNL Walmart Marketplace]. 然后，沃尔玛会通知客户订单状态和送货详细信息。

   在店面，您必须取消整个订单。 [!DNL Commerce] 不允许部分取消。

* **退款请求** — 如果要求Walmart Marketplace退货，则 [!UICONTROL Status details] 包括指向返回的链接。 退货和退款均从 [返回结果](return-refund-orders.md) 功能板。

处理商务订单并 [!DNL Channel Manager] 成功将装运、部分装运和取消更新同步到 [!DNL Walmart Marketplace]，则订单处理完成。 已发运订单的退货请求和退货均从 [返回结果](return-refund-orders.md) 功能板。

>[!NOTE]
>
> 订单更新可能最多需要五分钟才能同步到 [!DNL Walmart Marketplace]. 要检查订单状态，请返回到 [!DNL Channel Manager] 订单页面。

## 发运订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 通过选择销售渠道商店的眼睛图标打开商店视图。

1. 要查看 [!DNL Walmart Marketplace] 订单，选择 **[!UICONTROL Orders]**.

1. 在“订单”表中，通过选择 **商务订单编号**.

1. 通过选择 **[!UICONTROL Ship]**.

   ![商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/order-detail-with-external-order-id.png)

   * 选择运输承运人，并通过选择 **[!UICONTROL Add tracking number]**.

      ![商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/order-shipment-add-tracking-number.png)


   * 根据需要填写其余的送货单。 请参阅 [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) 以了解详细说明。

1. 提交装运后，跟踪 [订单状态](manage-orders.md#about-order-status) in [!DNL Channel Manager] 验证更新是否已发送到 [!DNL Walmart Marketplace].

在发运订单后，您可以处理来自 [!DNL Channel Manager] 根据从 [!DNL Walmart Marketplace]. 请参阅 [退货订单](return-refund-orders.md).

## 取消订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 选择销售渠道商店的眼睛图标以打开商店视图。

1. 要查看 [!DNL Walmart Marketplace] 订购，选择*[!UICONTROL *Orders]**。

1. 在“订单”(Orders)表格中，打开 [订购详细信息页面](manage-orders.md#view-order-detail) 选择 **商务订单编号** 来取消。

   ![商务订单详细信息视图[!DNL Walmart Marketplace]订购](assets/order-detail-with-external-order-id.png)

1. 取消订单。

   * 选择 **取消** 从“订单详细信息”菜单。

   * 在 [!UICONTROL Cancel Order] 表单，选择 **取消原因**.
   ![商务订单详细信息视图 [!DNL Walmart Marketplace] 订购](assets/cancel-order-reason-selector.png)

   * 选择 **取消订单**.


1. 提交取消后，跟踪 [订单状态](manage-orders.md#about-order-status) in [!DNL Channel Manager] 验证更新是否已发送到 [!DNL Walmart Marketplace].

## 修复订单错误

在订单同步过程中，可能会从 [!DNL Walmart Marketplace]，或在更新发运、部分发运和取消的订单流程中。

如果发运、部分发运或取消更新的同步操作失败，则 [!DNL Channel Manager] 订购页面显示 _错误_ 订单的状态。 为确保发运信息和订单取消信息准确反映在Walmart Marketplace帐户中，请在您的 [!DNL Walmart Marketplace] 存储。


