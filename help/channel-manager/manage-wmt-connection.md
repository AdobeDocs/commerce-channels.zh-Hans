---
title: 管理沃尔玛商城连接
description: '''更新API凭据以授权[DNL！ Commerce]商店视图和 [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] 产品清单，并同步 [!DNL Commerce] 和沃尔玛之间的库存、价格、订单和运送数据。'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 映射装运承运人

在您[处理[!DNL Walmart Marketplace]订单的订单发运](process-orders.md#ship-an-order)之前，请将Walmart首选发运承运人映射到[!DNL Commerce]中的相应承运人，以便在[!DNL Walmart]和[!DNL Commerce]之间同步发运数据。

未映射到首选运营商的Commerce运营商在[!DNL Walmart]上标记为&#x200B;*[!UICONTROL Other Carrier]*。

**先决条件**

查看[!DNL Marketplace Seller account]的[沃尔玛要求](walmart-requirements.md)。

## 更新连接凭据

1. 在sales channel store的[!UICONTROL Listings]页面上，选择&#x200B;**[!UICONTROL Channel Settings]**。

1. 在&#x200B;**[!UICONTROL Channel Settings]**&#x200B;上，选择&#x200B;**[!UICONTROL Walmart Connection]**。

1. 要修改凭据，请选择&#x200B;**[!UICONTROL Change Credentials]**

   ![更新Walmart API凭据以授权连接](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. 输入&#x200B;**[!UICONTROL Walmart Client ID]**&#x200B;和&#x200B;**[!UICONTROL Walmart Client Secret]**。

1. 选择&#x200B;**[!UICONTROL Save]**&#x200B;以应用配置。
