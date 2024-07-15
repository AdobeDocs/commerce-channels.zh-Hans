---
title: 映射装运承运人
description: '''映射属性以匹配[DNL！ Commerce]产品到现有 [!DNL Walmart Marketplace] 列表并在 [!DNL Channel Manager] 和 [!DNL Walmart]之间同步数据。'
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 映射装运承运人

在您[处理[!DNL Walmart Marketplace]订单的订单发运](process-orders.md#ship-an-order)之前，请将Walmart首选发运承运人映射到[!DNL Commerce]中的相应承运人，以便在[!DNL Walmart]和[!DNL Commerce]之间同步发运数据。

未映射到首选运营商的Commerce运营商在[!DNL Walmart]上标记为&#x200B;*[!UICONTROL Other Carrier]*。

**先决条件**

在映射装运承运人之前，请完成以下任务：

1. 查看[!DNL Walmart Marketplace]的准时交付](https://sellerhelp.walmart.com/s/guide?article=000009473)的[运营商方法和配送最佳实践。

1. 验证[!DNL Commerce]存储区中的[[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html)和[[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html)配置，以确保已为[!DNL Walmart Marketplace sales]优化配置。

## 映射装运承运人

1. 从&#x200B;**[!UICONTROL Listings]**&#x200B;或&#x200B;**[!UICONTROL Orders]**&#x200B;页面中，选择&#x200B;**[!UICONTROL Channel Settings]**。

1. 在&#x200B;**[!UICONTROL Channel Settings]**&#x200B;上，选择&#x200B;**[!UICONTROL Shipping Carriers]**。

   ![映射装运承运人](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. 对于列出的每个[!DNL Walmart]首选运营商，如果该运营商可用，请从下拉列表中选择[!DNL Commerce]运营商名称。

1. 选择&#x200B;**[!UICONTROL Save]**&#x200B;以应用配置。

