---
title: 处理订单
description: 发运和取消说明 [!DNL Walmart Marketplace] Adobe Commerce和Magento Open Source的订单。
source-git-commit: 5670639697550b2d7fee67dd29be9c6278d5782b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 处理订单

如果您使用Adobe Commerce和Magento Open Source订单管理来管理 [!DNL Commerce] 商店销售，您处理 [!DNL Walmart Marketplace] 使用类似工作流从商务中获取订单。

在Commerce中处理订单时，渠道管理器会同步更新到 [!DNL Walmart Marketplace]. 此更新可确保商务中的产品库存和订单状态与 [!DNL Walmart Marketplace] 并通知沃尔玛向客户发送订单状态和送货信息。

>[!NOTE]
>
> 订购更新最多可能需要五分钟才能同步到 [!DNL Walmart Marketplace]. 要检查订单状态，请返回 [!DNL Channel Manager] 订单。

## 发运订单

从Commerce发运订单时，您使用 [[!DNL Commerce Order Management] 发运工作流](https://docs.magento.com/user-guide/sales/order-ship.html). 提交订单后，更新将同步到 [!DNL Walmart Marketplace]. 然后，沃尔玛会通知客户订单状态和送货详细信息。

**先决条件**

在发运订单之前，请确认 [渠道运输设置和运营商配置](map-shipping-carriers.md) met [!DNL Walmart Marketplace requirements].

### 创建并提交发运

当您运送 [!DNL Walmart Marketplace] 订购自 [!DNL Commerce]，则必须添加跟踪编号。 客户在从接收的发运通知中接收跟踪编号 [!DNL Walmart].

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 打开 [!UICONTROL Channel Manager Marketplace Stores] 页面。

1. 通过选择销售渠道商店的眼睛图标打开商店视图。

1. 要查看 [!DNL Walmart Marketplace] 订购，选择*[!UICONTROL *Orders]**。

1. 在“订单”表中，通过选择 **商务订单编号**.

1. 通过选择 **[!UICONTROL Ship]**.

   - 要选择运输承运人并添加跟踪编号，请选择 **[!UICONTROL Add tracking number]**.

   - 根据需要填写其余的送货单。 请参阅 [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) 以了解详细说明。

1. 提交装运后，跟踪 [订单状态](manage-orders.md#about-order-status) in [!DNL Channel Manager] 验证更新是否已发送到 [!DNL Walmart Marketplace].

## 取消订单

当您取消 [!DNL Walmart Marketplace] 沃尔玛要求取消订单。 当订单取消更新至沃尔玛时，取消原因将包含在发送给客户的取消通知中。

取消原因也显示在 [!DNL Commerce] 订单付款信息。

1. 在管理员中，选择 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 打开 [!UICONTROL Channel Manager Marketplace Stores] 页面。

1. 选择销售渠道商店的眼睛图标以打开商店视图。

1. 要查看 [!DNL Walmart Marketplace] 订购，选择*[!UICONTROL *Orders]**。

1. 在“订单”表中，通过选择 **商务订单编号** 来取消。

   ![Walmart Marketplace订单的商务订单详细信息视图](assets/order-detail-with-external-order-id.png)

1. 取消订单。

   - 选择 **取消** 从“订单详细信息”菜单。

   - 在“取消订单”窗体中，选择 **取消原因**.

      ![Walmart Marketplace订单的商务订单详细信息视图](assets/order-detail-with-external-order-id.png)

   - 选择 **取消订单**.

1. 验证更新是否已发送到 [!DNL Walmart Marketplace] 通过检查 [订单状态](manage-orders.md#about-order-status) in [!DNL Channel Manager].
