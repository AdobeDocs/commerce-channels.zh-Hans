---
title: 管理Walmart Marketplace连接
description: '''更新API凭据，以授权[DNL! 商务]商店视图和 [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] 产品清单，并同步库存、价格、订单和发运数据 [!DNL Commerce] 还有沃尔玛。'
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 地图运输承运人

在您之前 [处理订单发运](process-orders.md#ship-an-order) 表示 [!DNL Walmart Marketplace] 订购，将沃尔玛首选的运输公司映射到 [!DNL Commerce] 以便在 [!DNL Walmart] 和 [!DNL Commerce].

未映射到首选运营商的商业运营商将标记为 *[!UICONTROL Other Carrier]* on [!DNL Walmart].

**先决条件**

审阅 [沃尔玛要求](walmart-requirements.md) 对于 [!DNL Marketplace Seller account].

## 更新连接凭据

1. 在 [!UICONTROL Listings] 页面，选择 **[!UICONTROL Channel Settings]**.

1. 开 **[!UICONTROL Channel Settings]**，选择 **[!UICONTROL Walmart Connection]**.

1. 要修改凭据，请选择 **[!UICONTROL Change Credentials]**

   ![更新Walmart API凭据以授权连接](assets/update-connection-credentials.png)

1. 输入 **[!UICONTROL Walmart Client ID]** 和 **[!UICONTROL Walmart Client Secret]**.

1. 选择 **[!UICONTROL Save]** 以应用配置。
