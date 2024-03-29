---
title: 管理沃尔玛商城连接
description: '''更新API凭据以授权[DNL！ Commerce]商店视图和 [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] 产品列表，并在以下位置同步库存、价格、订单和装运数据： [!DNL Commerce] 还有沃尔玛。'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 映射装运承运人

在您之前 [处理订单发运](process-orders.md#ship-an-order) 对象 [!DNL Walmart Marketplace] 订单，将沃尔玛首选的发货运营商映射到 [!DNL Commerce] 以便装运数据能够在 [!DNL Walmart] 和 [!DNL Commerce].

未映射到首选运营商的商务运营商将标记为 *[!UICONTROL Other Carrier]* 日期 [!DNL Walmart].

**先决条件**

审核 [沃尔玛要求](walmart-requirements.md) 对于 [!DNL Marketplace Seller account].

## 更新连接凭据

1. 在 [!UICONTROL Listings] 销售渠道商店的页面，选择 **[!UICONTROL Channel Settings]**.

1. 开启 **[!UICONTROL Channel Settings]**，选择 **[!UICONTROL Walmart Connection]**.

1. 要修改凭据，请选择 **[!UICONTROL Change Credentials]**

   ![更新Walmart API凭据以授权连接](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. 输入 **[!UICONTROL Walmart Client ID]** 和 **[!UICONTROL Walmart Client Secret]**.

1. 选择 **[!UICONTROL Save]** 以应用配置。
