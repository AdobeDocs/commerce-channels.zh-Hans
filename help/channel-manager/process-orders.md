---
title: 处理订单
description: 发运和取消说明 [!DNL Walmart Marketplace] Adobe Commerce和Magento Open Source的订单。
source-git-commit: 90ccbecd6d1433ae1312d79f7ae2d34c8f381b97
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# 处理订单

如果您使用Adobe Commerce和Magento Open Source订单管理来管理 [!DNL Commerce] 商店销售，流程 [!DNL Walmart Marketplace] 使用类似工作流从商务中获取订单。

在Commerce中处理订单时，渠道管理器会同步更新到 [!DNL Walmart Marketplace]. 此更新可确保来自Commerce的订单状态和发运信息与 [!DNL Walmart Marketplace].

* **订单发运**- Walmart要求所有发货的跟踪编号。 如果库存数量不足以填满整个订单，则创建部分发运。 在您提交发运后，订单更新将同步到 [!DNL Walmart Marketplace]. 然后，沃尔玛会通知客户订单状态和送货详细信息。

* **订单取消** — 当您取消 [!DNL Walmart Marketplace] 沃尔玛要求取消订单。 取消原因包括在发送给客户的订单取消通知中。 取消原因也显示在 [!DNL Commerce] 订单付款信息。

>[!NOTE]
>
> 订单更新最多可以在五分钟内同步到 [!DNL Walmart Marketplace]. 要检查订单状态，请返回到 [!DNL Channel Manager] 订单页面。

## 发运订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 通过选择销售渠道商店的眼睛图标打开商店视图。

1. 要查看 [!DNL Walmart Marketplace] 订购，选择*[!UICONTROL *Orders]**。

1. 在“订单”表中，通过选择 **商务订单编号**.

1. 通过选择 **[!UICONTROL Ship]**.

   ![Walmart Marketplace订单的商务订单详细信息视图](assets/order-detail-with-external-order-id.png)

   * 要选择运输承运人并添加跟踪编号，请选择 **[!UICONTROL Add tracking number]**.

   * 根据需要填写其余的送货单。 请参阅 [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) 以了解详细说明。

1. 提交装运后，跟踪 [订单状态](manage-orders.md#about-order-status) in [!DNL Channel Manager] 验证更新是否已发送到 [!DNL Walmart Marketplace].

## 取消订单

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 选择销售渠道商店的眼睛图标以打开商店视图。

1. 要查看 [!DNL Walmart Marketplace] 订购，选择*[!UICONTROL *Orders]**。

1. 在“订单”表中，通过选择 **商务订单编号** 来取消。

![Walmart Marketplace订单的商务订单详细信息视图](assets/order-detail-with-external-order-id.png)

1. 取消订单。

   * 选择 **取消** 从“订单详细信息”菜单。

   * 在 [!UICONTROL Cancel Order] 表单，选择 **取消原因**.

   ![Walmart Marketplace订单的商务订单详细信息视图](assets/cancel-order-reason-selector.png)

   * 选择 **取消订单**.


1. 验证更新是否已发送到 [!DNL Walmart Marketplace] 通过检查 [订单状态](manage-orders.md#about-order-status) in [!DNL Channel Manager].
